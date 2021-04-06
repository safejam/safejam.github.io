# initial infrastructure setup

Used previous ami called  'proxy - internal'

Added 'acl all src 0.0.0.0/0' to /etc/squid3/squid.conf to allow access from anywhere

Added 'http_access allow all' (instead of http_access allow localnet)

CHANGED VPC DHCP OPTIONS BACK TO AMAZON-PROVIDED DNS (could not resolve names with remote-browser DCs switched off)

Created new DHCP options for CloudFlare's 1.1.1.1 service but used 1.1.1.3 & 1.0.0.3 which includes protection from malware and adult sites.


References:

https://stackoverflow.com/questions/42901716/how-do-i-allow-access-to-all-requests-through-squid-proxy-server



Updates and Digest Authentication
-----------------------------------------------
Sudo apt-get update && sudo apt-get upgrade

Sudo apt-get install apache2-utils (required for digest authentication)

Cd /etc/squid

Sudo touch passwd


Changing the owner and restricting access isn’t strictly required, but it’s good practice since the file’s contents will contain unsalted MD5-hashed passwords:
```
# chown proxy.proxy passwd
# chmod 640 passwd
```

Realm=mysafeinternet
Username=adam
Password=mysafeinternet

Sudo htdigest /etc/squid/passwd mysafeinternet adam

<Using password 'mysafeinternet'>

Test authentication with:

/usr/lib/squid3/digest_file_auth - c /etc/squid/passwd
Type
"adam":"mysafeinternet"
The hash is returned successfully


Update squid.conf
------------------
Removed all the acls for safe ports etc just to focus on the auth_users

auth_param digest program /usr/lib/squid3/digest_file_auth -c /etc/squid/passwd
auth_param digest realm mysafeinternet
auth_param digest children 2
acl auth_users proxy_auth REQUIRED
http_access allow auth_users (Instead of allow all or named ports)
http_port 13128 (change from default for obscurity)

References
https://blog.mafr.de/2013/06/16/setting-up-a-web-proxy-with-squid/> 
https://wiki.squid-cache.org/Features/Authentication
