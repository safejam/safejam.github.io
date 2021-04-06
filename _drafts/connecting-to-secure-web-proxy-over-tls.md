https://wiki.squid-cache.org/Features/HTTPS

Chrome

The Chrome browser is able to connect to proxies over TLS connections if configured to use one in a PAC file or command line switch. GUI configuration appears not to be possible (yet).

More details at http://dev.chromium.org/developers/design-documents/secure-web-proxy

Firefox

The Firefox 33.0 browser is able to connect to proxies over TLS connections if configured to use one in a PAC file. GUI configuration appears not to be possible (yet), though there is a config hack for embedding PAC logic.

There is still an important bug open:

    Using a client certificate authentication to a proxy: https://bugzilla.mozilla.org/show_bug.cgi?id=209312 

If you have trouble with adding trust for the proxy cert, there is a process by Patrick McManus to workaround that. 






# From http://dev.chromium.org/developers/design-documents/secure-web-proxy

 Secure Web Proxy
Introduction
A secure web proxy is a web proxy that the browser communicates with via SSL, as opposed to clear text.  In insecure public networks, such as airports or cafes, browsing over HTTP may leave the user vulnerable to cookie stealing, session hijacking or worse.  A secure web proxy can add a significant layer of defense in these cases.
Using a Secure Web Proxy with Chrome
To make use of a secure web proxy, Chrome needs to be configured to use a proxy auto-config file which specify the HTTPS proxy type.  For example:


function FindProxyForURL(url, host) { return "HTTPS secure-proxy.example.com:443"; }


This pac file can be specified by starting Chrome with the --proxy-pac-url=... command line argument, or through the settings dialog.  Please be aware that other browser do not support the HTTPS proxy type in a .pac file, so modifying the system-wide proxy configuration to use such a .pac file might be inadvisable.

Alternatively, a secure web proxy can be specified by using the --proxy-server=https://<proxy>:<port> command line argument.  For example:


chrome --proxy-server=https://secure-proxy.example.com:443


Since the communication between Chrome and the proxy uses SSL, next protocol negotiation will be used.  If the servers supports HTTP/2, then the proxy will act as an HTTP/2 Proxy.

Running a Secure Web Proxy
While all the details of running a secure web proxy are out of scope for this document, here are two suggestions.  If you are already running a web proxy, you use stunnel to convert it into a secure web proxy.  For example:

stunnel -f -d 443 -r localhost:8080 -p cert.pem 

This would cause stunnel to listen for SSL connections on port 443 and send any HTTP requests to the web proxy running on port 8080.

Alternatively, the popular proxy program Squid appears to offer support for running as a secure web proxy via the https_port directive.

Debugging Certificate Errors
Debugging certificate errors for a secure web proxy may be difficult because the certificate information is not readily visible. Certificate information is captured in NetLogs (capture with chrome://net-export, view with https://netlog-viewer.appspot.com/). Alternatively, without the proxy configured, navigate directly to the proxy's endpoint (e.g. https://123.123.123.123:1234/) in a new tab and you'll get the typical certificate error experience shown for server certificate errors. After that page works without error, reconfigure the secure web proxy. 

# From http://www.squid-cache.org/Doc/config/https_port/

Squid configuration directive https_port

Available in: 4   3.5   3.4   3.3   3.2   2.7   3.1   3.0   2.6  

This directive is not available in the 3.3 version of Squid.

For older versions than 3.3 see the linked pages above
Configuration Details:
Option Name:	https_port
Replaces:	
Requires:	--with-gnutls or --with-openssl
Default Value:	none
Suggested Config: 	


	Usage:  [ip:]port [mode] tls-cert=certificate.pem [options]

	The socket address where Squid will listen for client requests made
	over TLS or SSL connections. Commonly referred to as HTTPS.

	This is most useful for situations where you are running squid in
	accelerator mode and you want to do the TLS work at the accelerator
	level.

	You may specify multiple socket addresses on multiple lines,
	each with their own certificate and/or options.

	The tls-cert= option is mandatory on HTTPS ports.

	See http_port for a list of modes and options.
    http://www.squid-cache.org/Doc/config/http_port/

    

