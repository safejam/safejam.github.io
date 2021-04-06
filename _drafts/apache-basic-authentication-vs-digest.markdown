# Source
https://stackoverflow.com/questions/20910207/is-apache-digest-authentication-more-secure-or-than-basic-or-not

# Question
On the Authorization intro page, Apache tells us that:

Apache supports one other authentication method: AuthType Digest. This method is implemented by mod_auth_digest and is much more secure.

while on the mod_auth_digest page, Apache tells us that:

This module implements HTTP Digest Authentication (RFC2617), and provides an alternative to mod_auth_basic where the password is not transmitted as cleartext. However, this does not lead to a significant security advantage over basic authentication. On the other hand, the password storage on the server is much less secure with digest authentication than with basic authentication.

Can someone clarify these seemingly contradictory statements for me? I understand that both ways of handling passwords are vulnerable to replay attacks (unless you're also using SSL) but that seems like a separate issue.

# Answer

With basic authentication the password is sent nearly plain (base64 encoded) to the server and on the server side it gets hashed and compared against the hashed password (stored in htpasswd file or similar). With digest authentication the hashed password is sent to the server (with some server defined data added so replay attacks will not work). But to verify the password you need to have the plain password on the server side (or something close to the plain password). This means, that if the attacker gets access to the htpasswd file it needs to crack all the passwords before they can be used for basic authentication, while if it gets access to the htdigest file it can use it directly for digest authentication.

In summary: basic auth is less secure on the wire, but way more secure to store on the server. Best choice of both would be therefore to use basic auth with SSL. But, both authentication techniques have the disadvantage, that there is no way for a session timeout or explicit logouts, e.g. the browser will stay logged in until it gets closed. This makes attacks like CSRF easier.


# References
https://httpd.apache.org/docs/2.4/mod/mod_auth_basic.html

https://httpd.apache.org/docs/2.4/mod/mod_auth_digest.html