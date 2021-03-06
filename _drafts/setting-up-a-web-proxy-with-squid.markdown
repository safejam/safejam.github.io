Setting up a Squid forward proxy can be a pretty daunting task since Squid is an extremely flexible piece of software. In this article, I’m going to provide a minimal non-caching, authenticated configuration. I have tested this with Squid 3.1.12 on Ubuntu 13.04, but with minor adjustments it should work for other systems as well.


First of all, we install Squid and some utilities that we need later:

# apt-get install squid apache2-utils
The proxy is going to use HTTP Digest authentication to authenticate users using a local password file. For larger setups, Squid can also authenticate against LDAP directories or Kerberos, but that’s beyond the scope of this article.

Now, let’s create a new password file (you have to be user root):

# cd /etc/squid3/
# touch passwd
# chown proxy.proxy passwd
# chmod 640 passwd
Changing the owner and restricting access isn’t strictly required, but it’s good practice since the file’s contents will contain unsalted MD5-hashed passwords.

Using the htdigest(1) utility from apache2-utils, we can add users to the password file or change passwords of existing users:

# htdigest /etc/squid3/passwd SurfinUSA matthias
Adding user matthias in realm SurfinUSA
New password:
Re-type new password:
#
The realm we pass on the command line has to be the same as the realm we use for Squid later. The format of the file is quite simple:

matthias:SurfinUSA:0fb904a2a976add85091cf0115db9d7b
It consists of username, realm, and an MD5 hash. The hash is calculated from the user name, realm and password:

$ echo -n matthias:SurfinUSA:secret | md5sum -
0fb904a2a976add85091cf0115db9d7b  -
$
To save us trouble later, we test whether the file works as intended. Squid uses external programs to authenticate users; for Digest authentication, it pipes username and realm to an external program (Update: renamed to digest_file_auth recently!) and if username and realm are known to the program, it returns the MD5 hash:

# /usr/lib/squid3/digest_pw_auth -c /etc/squid3/passwd
"matthias":"SurfinUSA"
0fb904a2a976add85091cf0115db9d7b
CTRL^D
#
Looks good, so we can move on to Squid itself. The default configuration file in /etc/squid3/squid.conf has 5800 heavily commented lines which makes it a bit unwieldy to edit. Since we don’t need Squid’s full power, it’s easier to start from an empty file. It turns out that this is all we need:

auth_param digest program /usr/lib/squid3/digest_pw_auth -c /etc/squid3/passwd
auth_param digest realm SurfinUSA
auth_param digest children 2

acl auth_users proxy_auth REQUIRED

http_access allow auth_users
http_access deny all

http_port 13128
The auth_param lines set up digest authentication. In our example, Squid runs two digest_pw_auth child processes for authenticating users. The acl line basically places all authenticated users in a group auth_users. Using the http_access command, only users from this group are allowed access, to all others, access is denied (careful, order matters for http_access!).

Finally, we let Squid listen on port 13128. To prevent script kiddies from attacking your proxy, we use a non-standard port (3128 is Squid’s default).

Finally, reload the configuration file:

# service squid3 reload
Check the log file in /var/log/squid3/cache.log for errors and if there are none, let’s test the proxy:

$ curl -i --proxy-digest -U matthias --proxy http://localhost:13128 URL
Enter proxy password for user 'matthias':
[...]
$
You should get the same web page that you’d get when calling curl URL without any proxy settings. If that worked, congratulations! You now have a working HTTP proxy that you can use from your web browser.

Our configuration doesn’t cache resources on disk, so it doesn’t use much disk space. The access log in /var/log/squid3/access.log, however, tends to get quite large over time. You may want to either configure log rotation or turn it off completely using the following command in squid.conf:

access_log none
Finally, a word of advice: HTTP traffic between your browser and the proxy is transmitted unencrypted, so you should not use this setup for transmitting sensitive information over an untrusted network. If you want protection between your browser and Squid, you would have to set up SSL connections using the https_port command (which Firefox doesn’t support).

For secure web surfing via a public Wifi network at a conference or a coffee shop consider using a SOCKS proxy using OpenSSH or a VPN.