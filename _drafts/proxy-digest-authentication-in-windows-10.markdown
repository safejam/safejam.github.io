# Problem
Our organization has implemented a proxy server which uses credentials to allow internet access to web browsers and apps.

I know that one can configure the proxy settings using Internet Settings > Local LAN Settings > Proxy Server Settings, but there is no place to enter the login credentials. I take it the assumption is that the Proxy is usually configured to accept AD credentials, but my PC is not on the domain, so I have to find another way to add the relative credentials to access internet.

I have successfully configured other apps to use specific credentials via their proxy settings interface (FireFox allows to add credentials to specific proxy settings), but other apps makes us of the windows configured proxy settings and there are no allowance for supplying credentials.

I have even tried running the program as a specific domain user, but as the PC is not on the domain, this option is not successful.

Any suggestions to add specific credentials to windows proxy settings?

# Solution
Setting up the Proxy Settings:

In the Windows 10 menu, I went to settings (WinKey+I) and searched for "Configure Proxy Settings". Select Internet Settings > Local LAN Settings >Proxy Server Settings.

Select the option to make use of a proxy server, and enter the Server Address and Port

Setting up the credentials for the Proxy Server:

In Windows 10 menu, go to Settings (WinKey+I) and search for "Credential Manager". Under Windows Credentials, add a new entry for Windows Credentials. Enter the Proxy Server address (without the port number), your domain user name and the password.

Once these details are active, you should be able to make use of the proxy server under your custom entered user credentials.

Just remember to deactivate the "Use a Proxy Server" setting (first step) when browsing from outside the network where the proxy is required. 