Adam reported that his youtube videos don't play

The squid access.log shows TCP_DENIED/407 for lots of youtube assets and advertising etc.

Basically, the digest authentication only works well in a browser or primary app (the iOS system-wide proxy includes user authentication), but not for apps (like YouTube) calling other external web assets.


From https://superuser.com/questions/351505/squid-logs-show-tcp-denied-407-error

Squid logs show “TCP_DENIED/407” error
Asked 9 years, 5 months ago
Active 4 years ago
Viewed 31k times

2


I'm using Squid 3.0

Example: I want to download software from cnet. After launching CNET Download.com Installer, I get an error:

Internet connection error

We're unable to connect to the download server. It seems that your internet connection is down or firewalled. Please check your internet and proxy setting then click the "Try Again" button below.

I checked Squid, and got the error:

1319791754.173      1 192.168.1.101 TCP_DENIED/407 2081 GET http://api.cnet.com/rest/v1.0/softwareProductLink? - NONE/- text/html
1319791754.396      1 192.168.1.101 TCP_DENIED/407 2194 GET http://www.w3.org/TR/html4/strict.dtd - NONE/- text/html
I searched for "TCP_DENIED/407" but I could not find a solution.

internet
proxy
squid
Share
Improve this question
Follow
edited Jun 12 '20 at 13:48

Community♦
1
asked Oct 28 '11 at 8:55

AAA-Super
4322 gold badges22 silver badges55 bronze badges
Add a comment
1 Answer

2

The 407 error is coming from squid, telling the calling application that it must provide authentication credential to continue.

With a browser, this is straightforward, it would pop-up asking for the credentials if it didn't already have them, and the user would type them in.

For non-interactive applications like a downloader, they should have a mechanism for entering the credentials into their configuration.