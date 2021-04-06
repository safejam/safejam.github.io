from https://securityboulevard.com/2019/03/openvpn-vs-ikev2-vs-l2tp-which-vpn-protocol-is-the-best/

A virtual private network (VPN) provides users with privacy and secure data when they browse the internet or engage in online activity. One of the most crucial elements of a VPN is the protocol that protects user anonymity from hackers, advertisement agencies and government entities.

The protocol determines how the VPN will secure data in transit. Providers offer a wide range of protocols based on computer operating systems, devices, performance and other aspects. Below, we examine three of the most widely used protocols in the industry: OpenVPN, IKEv2 and L2TP. Which one is best? Let’s take a closer look.
Register Today! Secure Coding Virtual Summit
Join us on March 24, 2021, to hear from industry-leading AppSec and DevSecOps practitioners, analysts, and visionaries as they share their best pro tips and power ups to level up your code security.

OpenVPN

OpenVPN is the most popular and recommended protocol by VPN experts. OpenVPN is versatile and highly secure, making it a mainstay of the virtual private network industry. The VPN is aptly named open because it relies on open source technologies such as OpenSSL encryption library or SSL V3/TLS V1 protocols.

In an OpenVPN platform, providers maintain, update and assess the technology. One of the reasons why an OpenVPN is so effective is because it shields users who engage in online activity in plain sight. Users are less vulnerable to hackers and less likely to be detected by government agencies or aggressive marketers.

According to this source, when data travels through the OpenVPN viewers cannot differentiate between an HTTPS and the SSL connection. The protocol can operate on any port while utilizing UDP or TCP protocols. This makes it easy for users to get around firewalls. Companies can utilize a wide range of strategies such as AES encryption, HMAC or OpenSLL when adding OpenVPN to their processes.

OpenVPNs require a third-party application because they are not supported by any platforms. Third-party providers such as iOS and Android, however, are supported. Although most companies offer customized OpenVPN configurations, they also allow users to personalize their own configuration.

So let’s summarize:
OpenVPN Pros:

    Bypasses most firewalls.
    Vetted by third parties.
    Offers top-level security.
    Works with multiple encryption methods.
    Can be configured and customized to suit any preference.
    Can bypass firewalls.
    Supports a wide range of cryptic algorithms.

OpenVPN Cons:

    Highly technical and complex setup.
    Relies upon third-party software.
    Desktop-strong, but mobile can be weak.

IKEv2

IKEv2 was designed as a joint project between Cisco Systems and Microsoft. It operates as a true protocol and controls the IPSec key exchange.

IKEv2 has the distinction of operating on non-mainstream platforms such as Linux, BlackBerry or other marginal platforms. However, it also comes with the Windows 7 operating system. Because of its ability to adapt, IKEv2 offers a consistent connection in various networks. So, if a connection drops, the IKEv2 helps the user maintain a VPN connection.

Like most protocols, IKEv2 meets user privacy demands. Since it offers support for MOBIKE, it can adapt to changes in any network. Therefore, if the user suddenly switches from a Wi-Fi connection to a data connection, IKEv2 can handle it flawlessly without losing the connection.

In summary:
IKEv2 Pros:

    Supports a wide range of encryption protocols.
    Offers high-level stability and consistent connectivity.
    Offers easy setup.
    Super-fast VPN protocol.

IKEv2 Cons:

    Limited support for platforms.
    Not immune to firewall blocks.

L2TP

The most notable characteristic of L2TP is its inability to operate alone. To offer encryption or protection for data in transit, it must be paired with IPSec.

L2TP is an extension of the PPTP protocol. It operates on a double encapsulation that includes a PPP connection on level one and an IPsec encryption on level two. While the L2TP protocol does support AES-256, stronger protocols can slow the performance.

Most desktop and mobile OSes contain L2TP, which makes implementation relatively simple. However, users and developers alike have noted that L2TP can be blocked by firewalls. What struggles it may have with firewalls, it more than makes up for in sender/receiver privacy.

The L2TP design prevents hackers from viewing or intercepting data in transit.

While the connection is secure, the protocol can be weak and slow. The connection can be hindered due to the traffic conversion into the L2TP format. Developers and users must also account for the additional layer of encryption.

Let’s look at the summary:
L2TP Pros:

    Available on nearly all devices and operating systems.
    Easy setup process.
    High levels of security that display some weaknesses.
    Multithreading improves performance.

L2TP Cons:

    Can be blocked by firewalls.
    Performance can be blocked.
    Double encapsulation can slow down performance.

Which Protocol is Best?

With the different elements of each protocol and their varying application, the best protocol depends on the needs of the developer and the users. While the OpenVPN may be considered the go-to protocol, there are several factors to consider.

The OpenVPN is speedy, versatile and secure. It’s also compatible with any operating system both on-site and remote. Users that want a problem-free, high-performance protocol should probably stick with OpenVPN.

Remember, however, that OpenVPNs requires a third-party. Developers that have an issue with this type of setup may want to turn to an L2TP or IKEv2. Some main considerations are security, speed, connectivity consistency and overall high performance. So, third-party support may not be high on the priority list.

And last, how will the configuration with all platforms and devices affect the overall performance of the service and network? Developers need to ask these questions from their client’s perspective. Can a developer provide exceptional service with a VPN that doesn’t provide the absolute best security or super-fast speed?

Taking everything into consideration, our belief is the OpenVPN is still the best protocol for all types of operating systems, devices and platforms.