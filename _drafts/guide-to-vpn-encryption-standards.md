from https://proprivacy.com/vpn/guides/vpn-encryption-the-complete-guide



Welcome to ProPrivacy!

    Our Bloggers ▼
    Our Privacy Tools ▼
    About Us ▼

    VPNs ▼
    Storage & Backup ▼
    Password Managers ▼
    Email ▼
    Ad Blockers ▼
    Open Source ▼
    Other ▼

    VPN
    Guides
    VPN Guides
    OpenVPN vs IKEv2 vs PPTP vs L2TP/IPSec vs SSTP - Ultimate Guide to VPN...

OpenVPN vs IKEv2 vs PPTP vs L2TP/IPSec vs SSTP - Ultimate Guide to VPN Encryption

Category:
    Guides
Last Updated:
    June 30, 2020
Comments:
    29

Douglas Crawford
Written by Douglas Crawford

A Virtual Private Network (VPN) encrypts all data as it travels between your computer and a VPN server. In this Complete VPN Encryption Guide, we take a detailed look at what encryption is, and how it is used in VPN connections.

Perhaps most importantly, we will explain the array of encryption terms used by VPN services. It is our hope that, after reading through this guide, you will have a greater understanding of this complex subject and that you will be better able to assess the security claims made by VPN providers.
Preliminaries

If you are unsure about what a VPN is and what one can do for you, please check out our VPNs for Beginner's Guide. 

Our aim is to present the key features of VPN encryption in as simple terms as possible. Although there is no getting away, from the fact that encryption is a complex subject.

If even the term encryption causes your eyes to start glazing over, but you still want to know what to look out for in a good VPN service, you can jump straight to summaries using the Table of Contents.
What Is Encryption?

    Begin at the beginning," the King said, very gravely, "and go on till you come to the end: then stop.&rdquo;
    Lewis Carroll, Alice in wonderland

The simplest analogy is that encryption is a lock. If you have the correct key, then the lock is easy to open. If someone does not have the correct key but wants to access the contents of a strongbox (that is, your data) protected by that lock, then they can try to break the lock.

In the same way that the lock securing a bank vault is stronger than the one securing a suitcase, some encryption is stronger than other encryption.

If you want a VPN with the strongest encryption, check out our most secure VPNs list for more information.
The Basics

When you were a kid, did you ever play the game in which you created a "secret message” by substituting one letter of the message with another? The substitution was made according to a formula picked by you.

You might, for example, have substituted each letter of the original message with one three letters behind it in the alphabet. If anyone else knew what this formula was, or was able to work it out, then they would be able to read your "secret message.”

In cryptography jargon, what you were doing was "encrypting” the message (data) according to a very simple mathematical algorithm. Cryptographers refer to this formula as a "cipher.” To decrypt it, you need the key. This is a variable parameter which determines the final output of the cipher. Without this parameter, it is impossible to decrypt the cipher.

    If someone wants to read an encrypted message but does not have the key, then they must try to "crack” the cipher. When the encryption uses a simple letter substitution cipher, cracking it is easy. The encryption can be made more secure, however, by making the mathematical algorithm (the cipher) more complex.

You could, for example, substitute every third letter of the message with a number corresponding to the letter.
Encryption Key Length

Modern computer ciphers are very complex algorithms. Even with the help of supercomputers, these are very difficult to crack, if not impossible for all practical purposes. The crudest way to measure the strength of a cipher is by the complexity of the algorithm used to create it.

The more complex the algorithm, the harder the cipher is to crack using what we call a brute force attack.

A brute force attack if a very primitive form of attack is (also known as an exhaustive key search), that basically involves trying every combination of numbers possible until the correct key is found.

Computers perform all calculations using binary numbers: zeros and ones. The complexity of a cipher depends on its key size in bits - the raw number of ones and zeros necessary to express its algorithm, where each zero or one is represented by a single bit.

This is known as the key length and also represents the practical feasibility of successfully performing a brute force attack on any given cipher.

The number of combinations possible (and therefore the difficulty to brute force them) increases exponentially with key size. Using the AES cipher (see later):

Key Size Cominations

To put this into perspective:

    In 2011, the fastest supercomputer in the word was the Fujitsu K. This was capable of an Rmax peak speed of 10.51 petaflops. Based on this figure, it would take Fujitsu K 1.02 x 10^18 - around one billion billion (one quintillion) - years to crack a 128-bit AES (Advanced Encryption Standard) key by force. This is older than the age of the universe (13.75 billion years).
    The most powerful supercomputer in the world now (2017) is the Sunway TaihuLight in China. This beast is capable of a peak speed of 93.02 petaflops. This means that the most powerful computer in the world would still take some 885 quadrillion years to brute force a 128-bit AES key.
    The number of operations required to brute force a 256-bit cipher is 3.31 x 10^56. This is roughly equal to the number of atoms in the universe!

Computer Ciphers

While encryption key length refers to the amount of raw numbers involved, ciphers are the mathematics – the actual formulas or algorithms - used to perform the encryption. As we have just seen, brute forcing modern computer ciphers is wildly impractical.

It is weaknesses (sometimes deliberate) in these cipher algorithms that can lead to encryption being broken. This is because the output of the (badly designed) cipher may still reveal some structure from the original information before encryption. This creates a reduced set of possible combinations to try, which in effect reduces the effective key length.

The Blowfish cipher, for example, is vulnerable to an attack that exploits the mathematics behind the birthday problem in probability theory. The study of weaknesses in cryptographic algorithms is known as cryptoanalysis.

Longer key lengths compensate for such weaknesses, as they greatly increase the number of possible outcomes.

Instead of attacking the cipher itself, an adversary can attack the key itself. This can affect a particular site or certain software product. But the security of the cipher algorithm is still intact, and other systems that utilize the same algorithm but have a secure generation of keys are unaffected by the break.
Cipher Key Length

How strong a cipher is depends on both the mathematics of the cipher itself, plus its key length as expressed in bits. For this reason, ciphers are usually described along with the key length used.

So AES-256 (the AES cipher with a 256-bit key length) is usually considered stronger than AES-128. Note that I say usually because we are dealing with very complex mathematics here (see my notes on AES later).

Note Icon2 01 150X150

It is important to note that key length alone is not a good indicator of a cipher’s strength. It is the combination of key length and cipher that matters. Ciphers used for asymmetric encryption, for example, use much longer key sizes than those used for symmetric encryption to provide the equivalent protection.

Key Size Comparison

This table is a little out of date, as it does not take into consideration newer attacks that have been discovered on RSA. It is also worth noting that the elliptic curve and Diffie-Hellman variants of RSA are much stronger than traditional ones. But hopefully, you get the idea.

Note Icon2 01 150X150

One thing to note is that the higher the key length, the more calculation involved, so the more processing power needed. This impacts the speed at which data can be encrypted and decrypted. VPN providers and suchlike must, therefore, decide how best to balance security vs. practical usability when choosing encryption schemes. There are some VPN providers who have managed to strike this fine balance well. For more information, check out our fast VPNs guide.

We discuss the main ciphers used by various VPN protocols a little later, but the most common ciphers that you will likely encounter are Blowfish and AES. In addition to this, RSA is used to encrypt and decrypt a cipher’s keys, and SHA-1 or SHA-2 is used as the hash function to authenticate data.

Asymmetric encryptionAsymmestric encryption
Perfect Forward Secrecy

Perfect Forward Secrecy (PFS) is also referred to as using ephemeral encryption keys, or just Forward Secrecy (FS) by those uncomfortable with using the word "perfect.”

Most modern secure online communication relies on SSL/TLS. It is used by HTTPS websites and the OpenVPN protocol. TLS (Transport Layer Security) is an asymmetric encryption protocol. Using an asymmetric cipher means that data is secured using a public key, which is made available to everyone. It can only be decrypted, however, by an intended recipient who holds the correct private key.

    This private key must be kept secret. If it is stolen or cracked by an adversary, then that adversary can easily intercept and read any communications secured by it.

Unfortunately, it is common for servers or even entire companies to use just one private encryption key to secure all communications. Why? Because it’s easy. However, if that key is compromised then an attacker can access all communications encrypted with it.

This private encryption key, therefore, becomes a "master key” that can be used to unlock all communications with a server or company. The NSA is known to have exploited this weakness in order to collect vast reams of supposedly secure data.

The solution is Perfect Forward Secrecy. This is a system whereby a new and unique private encryption key is generated for each session. It is a simple idea, even if the Diffie-Hellman exchange maths is complex. It means that each TLS session has its own set of keys. Hence the term "ephemeral keys” – they are used once and then disappear.

There is, therefore, no "master key” that can be exploited. Even if a session is compromised, it is only that session that is compromised – not all the other sessions anybody has with that server or company!

Although uncommon, it is even possible to refresh PFS keys within a session (for example, every hour). This further limits the amount of data that can be intercepted by an adversary, even if a private key is compromised.

When I wrote this article on the subject a few years ago, use of Perfect Forward Secrecy for both HTTPS websites and OpenVPN connections were woefully rare. Fortunately, this situation has changed somewhat. Although by no means universal, use of ephemeral keys has greatly increased of late.

Useful Guides
The Best VPN Services to use in 2021 | Top VPN Providers for all Devices Tested
The cheapest VPN services if you're on a budget
10 Best VPNs for the USA to use in 2021

VPN Encryption Protocols

    A VPN protocol is the set of instructions (mechanism) used to negotiate a secure encrypted connection between two computers. A number of such VPN protocols are commonly supported by commercial VPN services. The most notable of these are PPTP, L2TP/IPSec, OpenVPN, SSTP, and IKEv2.

I look at each of these below, but OpenVPN is now the industry standard VPN protocol used by commercial VPN services - for good reason. It is very secure and can be used on almost all VPN-capable devices. I will, therefore, spend additional digital ink discussing OpenVPN in detail.
PPTP
PROS

    Client built in to just about all platforms
    Very easy to set up

CONS

    Very insecure
    Definitely compromised by the NSA
    Easily blocked

What is PPTP?

It is a VPN protocol only, and relies on various authentication methods to provide security. Among commercial VPN providers, this is almost invariably MS-CHAP v2. The encryption protocol (similar to a standard cipher) used by PPTP is Microsoft Point-to-Point Encryption (MPPE).

Point-to-Point Tunneling Protocol (PPTP) was developed by a consortium founded by Microsoft for creating VPN over dial-up networks. As such, PPTP has long been the standard protocol for corporate VPN networks.

PPTP is available as standard on just about every VPN-capable platform and device. It is easy to set up, without the need to install additional software. This ensures that PPTP remains a popular choice both for business VPNs and commercial VPN services.

It also has the advantage of requiring a low computational overhead to implement… so it’s quick!

    Unfortunately, PPTP is not secure. At all. Although now usually only found using 128-bit encryption keys, in the years since it was first bundled with Windows 95 OSR2 back in 1999, a number of security vulnerabilities have come to light.

The most serious of these is the possibility of un-encapsulated MS-CHAP v2 Authentication. Using this exploit, PPTP has been cracked within two days. Microsoft has patched the flaw, but has itself issued a recommendation to use L2TP/IPsec or SSTP instead.

It should come as no surprise that the NSA almost certainly decrypts PPTP encrypted communications as standard. Even more worrying is that the NSA collected vast amounts of older data that was encrypted back when PPTP was considered secure. It can almost certainly decrypt this legacy data as well.

PPTP requires both TCP port 1723 and the GRE protocol. It is easy to firewall GRE, which makes it easy to block PPTP connections.
L2TP/IPsec
PROS

    Usually considered secure
    Easy to set up
    Available on all modern platforms
    Faster than OpenVPN (maybe)

CONS

    May be compromised by the NSA (unproven)
    Likely deliberately weakened by the NSA (unproven)
    Can struggle with restrictive firewalls
    Often implemented badly

What is L2TP and IPsec?

Layer 2 Tunneling Protocol (L2TP) is built in to almost all modern operating systems and VPN-capable devices. It is therefore just as easy and quick to set up as PPTP.

On its own, L2TP does not provide any encryption or confidentiality to traffic that passes through it, so it is usually implemented with the IPsec authentication suite (L2TP/IPsec). Even if a provider only refers to either L2TP or IPsec (as some do), it almost certainly actually means L2TP/IPSec.

L2TP/IPsec can use either the 3DES or AES ciphers. 3DES is vulnerable to Meet-in-the-middle and Sweet32 collision attacks, so in practice you are unlikely to encounter it these days.

    Problems can arise because the L2TP/IPSec protocol uses only a limited number of ports. This can this cause complications when used behind NAT firewalls. This reliance on fixed ports also makes the protocol fairly easy to block.

L2TP/IPsec encapsulates data twice, which slows things down. This is offset by the fact that encryption/decryption occurs in the kernel and L2TP/IPsec allows multi-threading. OpenVPN does not. The result is that L2TP/IPsec is theoretically faster than OpenVPN.

L2TP/IPsec using the AES cipher has no major known vulnerabilities, and if properly implemented may still be secure. However, Edward Snowden’s revelations have strongly hinted at the standard being compromised by the NSA.

John Gilmore is a security specialist and founding member of the Electronic Frontier Foundation. He explains, it is likely that IPSec was deliberately weakened during its design phase.

    An arguably much bigger problem is that many VPN services implement L2TP/IPsec poorly. Specifically, they use pre-shared keys (PSKs) that can be freely downloaded from their websites.

These PSKs are only used to authenticate the connection, so even if compromised, the data remains securely encrypted using AES. An attacker could, however, use the pre-shared key to impersonate a VPN server. It could then eavesdrop on encrypted traffic, or even inject malicious data into the connection.

Note Icon2 01 150X150

Summary

Despite some largely theoretical issues, L2TP/IPsec is generally regarded as being secure if openly published pre-shared keys are not used. Its built-in compatibility with a great many devices can make it a very good choice.
SSTP
PROS

    Very secure
    Completely integrated into Windows
    Microsoft support
    Can bypass most firewalls

CONS

    Proprietary standard owned by Microsoft

What is SSTP?

SSTP is a type of encryption that uses SSL 3.0 and offers similar advantages to OpenVPN. This includes the ability to use TCP port 443 to evade censorship. Tight integration with Windows can make it easier to use and more stable than OpenVPN on that platform.

Unlike OpenVPN, however, SSTP is a proprietary standard owned by Microsoft. This means that the code is not open to public scrutiny. Microsoft’s history of cooperating with the NSA, and speculation about possible backdoors built in to the Windows operating system, do not inspire confidence in the standard.

Secure Socket Tunneling Protocol (SSTP) was introduced by Microsoft in Windows Vista SP1. Although it is now available for Linux VPNs, and even Mac OS X, it is still primarily a Windows-only platform.

Another issue is that SSL v3.0 is vulnerable to what is known as the POODLE attack, and now therefore not recommended. Whether this issue also affects SSTP is unclear, but again, hardly inspires confidence.

Note Icon2 01 150X150

Summary

On paper, SSTP offers many of the advantages of OpenVPN. Being a proprietary Microsoft standard, however, badly undermines its credibility.
IKEv2
PROS

    Fast
    Stable - especially when switching network or reconnecting after a lost internet connection
    Secure (if AES is used)
    Easy to set up (at least at the user-end!)
    Protocol is supported on Blackberry devices

CONS

    Not supported on many platforms
    Implementing IKEv2 at the server-end is tricky, which is something that could potentially result in issues developing
    Only trust open source implementations

What is IKEv2?

Internet Key Exchange version 2 (IKEv2) was jointly developed by Microsoft and Cisco. It is natively supported by Windows 7+, Blackberry, and iOS devices. This is why a lot of iOS VPN services use IKEv2 instead of OpenVPN.

    Independently developed compatible versions of IKEv2 have been developed for Linux and other operating systems. Many of these iterations are open source. As always, I suggest being wary of anything developed by Microsoft. Open source versions of IKEv2, however, should have no issues.

IKEv2 is part of the IPsec protocol suite. It ensures traffic is secure by handing the SA (Security Association) attribute within IPsec and improves on IKEv1 in many ways. IKEv2 is thus sometimes referred to as IKEv2/IPsec. IKEv1, on the other hand, is often referred simply as IPsec. 

Dubbed VPN Connect by Microsoft, IKEv2 is particularly good at automatically re-establishing a VPN connection when users temporarily lose their internet connections. For example, when entering or leaving a train tunnel.

Because of its support for the Mobility and Multihoming (MOBIKE) protocol, IKEv2 is also highly resilient to changing networks. This makes IKEv2 a great choice for cell phone users who regularly switch between home WiFi and mobile connections, or who regularly move between hotspots.

IKEv2 is not as common as L2TP/IPSec as it is supported on many fewer platforms (although this situation is changing fast). It is, however, considered at least as good as, if not superior to, L2TP/IPsec in terms of security, performance (speed), stability and the ability to establish (and re-establish) a connection.
OpenVPN
PROS

    Very secure (if PFS is used)
    Highly configurable
    Open-source
    Can bypass firewalls
    Needs third-party software

What is OpenVPN?

OpenVPN is an open-source technology that uses the OpenSSL library and TLS protocols, along with an amalgam of other technologies, to provide a strong and reliable VPN solution. It is now the industry standard VPN protocol used by commercial VPN services - for good reason.

One of OpenVPN’s major strengths is that it is highly configurable. It is natively supported by no platform, but is available on most platforms via third-party software. Custom OpenVPN clients and apps are often available from individual VPN providers, but the core open source code is developed by the OpenVPN project.

Many developers and contributors to the OpenVPN project also work for OpenVPN Technologies Inc., which oversees the project.

OpenVPN runs best on a UDP port, but it can be set to run on any port (see notes later). This includes TCP port 443, which is used by regular HTTPS traffic. Running OpenVPN over TCP port 443 makes it hard to tell VPN connections apart from the kind of secure connections used by banks, email services, and online retailers. This makes OpenVPN very hard to block.

Another advantage of OpenVPN is that the OpenSSL library used to provide encryption supports a number of ciphers. In practice, however, only Blowfish and AES are commonly used by commercial VPN services. I discuss these below.

In light of information obtained from Edward Snowden, it seems that as long as Perfect Forward Secrecy is used, then OpenVPN has not been compromised or weakened by the NSA.

A recent crowdsourced audit of OpenVPN is now complete, as is another one funded by Private Internet Access. No serious vulnerabilities that affect the privacy of users were discovered. A couple of vulnerabilities were discovered that made OpenVPN servers potentially open to a Denial of Service (DoS) attack, but these have been patched in OpenVPN 2.4.2.

OpenVPN is usually regarded as the most secure VPN protocol available and is widely supported across the VPN industry. I will, therefore, discuss OpenVPN encryption in detail below.
OpenVPN Encryption

OpenVPN encryption comprises two parts – data channel encryption and control channel encryption. Data channel encryption is used to secure your data. Control channel encryption secures the connection between your computer and the VPN server.

Any defense is only as strong as its weakest point, so it is unfortunate that some VPN providers use a much stronger encryption on one channel than the other (usually stronger on the control channel).

It is not uncommon, for example, to see a VPN service advertised as using an AES-256 cipher with RSA-4096 handshake encryption and SHA-512 hash authentication. This sounds very impressive until you realize that it only refers to control channel encryption and not the data channel, which is encrypted with mere Blowfish-128 with SHA1 hash authentication. This is done for marketing reasons only.

If different encryption is used on the data and control channels, then the true strength of the OpenVPN connection is measured by the weaker encryption suite used.

For maximum security, both the data and control channel encryption should be as strong as possible. However, the stronger the encryption used, the slower the connection will be, which is why some providers scrimp on data channel encryption.

Control channel encryption is also called TLS encryption because TLS is the technology used to securely negotiate the connection between your computer and the VPN server. This is the same technology used by your browser to securely negotiate a connection to an HTTPS-encrypted website.

    Control channel encryption consists of a cipher, handshake encryption, and hash authentication.
    Data channel encryption consists of a cipher and hash authentication.

VPN providers often use the same level of encryption for both control and data channels. In our reviews and "traffic light” tables, we only list them separately if different values are used for each channel.

If we state that a provider uses an AES-256 cipher, this means that an AES-256 cipher is used for both the control and data channels.*

(*This should be the case, at least. Some legacy reviews do not meet our current guidelines, but these should be phased out in time).

Useful Guides
10 best VPNs for Windows PCs in 2021
10 Best VPNs for Mac in 2021 | VPN software for MacOS
8 Best VPN for Linux in 2020 | VPNs with GUIs & Privacy Features for all Distros

Ciphers

OpenVPN can use a number of symmetric-key ciphers in order to secure data on both control and data channels. In practice, the only ones used by commercial VPN providers are Blowfish, AES, and (very rarely) Camellia.
Blowfish

Blowfish-128 is the default cipher used by OpenVPN. Key sizes can in theory range from 32 bits to 448 bits, but Blowfish-128 is the only version you are likely to encounter in the wild.

    Blowfish is often considered secure enough for casual purposes, but has known weaknesses. It was created by renowned cryptographer Bruce Schneier, who in 2007 said, "at this point, though, I’m amazed it’s still being used.”

In our view, use of Blowfish-128 is acceptable as a second line of defense on the OpenVPN data channel. It should not, however, be considered secure when used on the control channel.
AES

AES has become the VPN industry-wide "gold standard” symmetric-key cipher. AES is NIST-certified and is almost universally considered very secure. AES-256 is used by the US government for protecting "secure” data.

The fact that it has a 128-bit block size rather than Blowfish’s 64-bit block size also means that it can handle larger files (over 4 GB) better than Blowfish. In addition to this, the AES instruction set benefits from built-in hardware acceleration on most platforms.

    AES is usually available in 128-bit and 256-bit key sizes (192-bit AES also exists). AES-128 remains secure as far as anyone is aware. Given what we now know about the extent of the NSA’s assault on encryption standards, however, most experts agree that AES-256 provides a higher security margin.

Just to ensure that no-one ever finds this subject too easy, though, there is some debate on this issue. AES-128 has a stronger key schedule than AES-256, which leads some very eminent experts to argue that AES-128 is actually stronger than AES-256.

The general consensus, however, is that AES-256 is stronger.
Camellia

Camellia is a modern secure cipher and is at least as secure and quick as AES. It is available in key sizes of 128, 192 and 256 bits. Thanks to NIST certification and its use by the US government, however, AES is almost always used instead of Camellia.

    But as I discuss below, there are reasons to not trust NIST-certified ciphers. The fact that Camellia is a non-NIST cipher is the main reason to choose it over AES. This option is only rarely available, however.

It is also worth noting that Camellia is not nearly as well-tested for weakness as AES.
Handshake Encryption

    In order to securely negotiate a connection between your device and a VPN server, OpenVPN uses a TLS handshake. This allows the OpenVPN client and VPN server to establish the secret keys with which they communicate.

To protect this handshake, TLS usually uses the RSA public-key cryptosystem. This is an encryption and digital signature algorithm used to identify TLS/SSL certificates. It can, however, also use a Diffie-Hellman or ECDH key exchange instead.
RSA

RSA is an asymmetric encryption system - a public key is used to encrypt the data, but a different private key is used to decrypt it. It has been the basis for security on the internet for the last 20 years or so.

It is now well-established that RSA with a key length of 1024-bits (RSA-1024) or less is not secure, and has almost certainly been cracked by the NSA. There has consequently been a concerted move among internet companies to migrate away from RSA-1024.

    Unfortunately, we still that find some VPN services continue to use RSA-1024 to protect handshakes. This is not good.

RSA-2048 and higher is still considered secure. On its own, RSA does not provide Perfect Forward Secrecy (PFS). This can, however, be implemented by including a Diffie-Hellman (DH) or Elliptic curve Diffie-Hellman (ECDH) key exchange in its cipher suite.

In this case, the strength of the DH or ECDH key does not matter as it is being used only to provide Perfect Forward Secrecy. The connection is secured using RSA.

    Because it can cause confusion, I’ll also note that the RSA cryptosystem has nothing to do with the disgraced US tech firm RSA Security LLC. This company deliberately weakened its flagship BSAFE encryption products after being bribed $10 million by the NSA.

Diffie-Hellman and ECDH

An alternative (rival) handshake encryption that is sometimes used by OpenVPN is the Diffie-Hellman (DH) cryptographic key exchange. This usually has a key length of 2048-bits or 4096-bits. Note that anything less than DH-2048 should be avoided due to susceptibility to the logjam attack.

    The main advantage of a Diffie-Hellman handshake over RSA is that it natively provides Perfect Forward Secrecy. As already noted, however, simply adding a DH key exchange to an RSA handshake achieves a similar end.

Diffie-Hellman has caused huge controversy over its re-use of a limited set of prime numbers. This makes it vulnerable to being cracked by a powerful adversary, such as the NSA. Diffie-Hellman on its own, therefore, does not make for secure handshake encryption. It is fine, however, when used as part of an RSA cipher suite.

Elliptic curve Diffie-Hellman (ECDH) is a newer form of cryptography that is not vulnerable to this attack. This is because it uses the properties of a particular type of algebraic curve instead of large prime numbers to encrypt connections.

ECDH can be used as part of an RSA handshake to provide Perfect Forward Secrecy, or can securely encrypt a handshake on its own (with an ECDSA signature). This also provides PFS.

ECDH key length starts at 384-bits. This is considered secure, but when used on its own to secure a TLS handshake, the longer the better (in terms of security, anyway).
SHA Hash Authentication

This is also referred to as data authentication or hash message authentication code (HMAC).

    Secure Hash Algorithm (SHA) is a cryptographic hash function used (among other things) to authenticate data and SSL/TLS connections. This includes OpenVPN connections.

It creates a unique fingerprint of a valid TLS certificate, which can be validated by any OpenVPN client. Even the tiniest change is detectable. If the certificate is tampered with, this will immediately be detected and the connection refused.

This is important in preventing a Man-in-the-middle (MitM) attack, where an adversary attempts to divert your OpenVPN connection to one of its own servers instead of your VPN provider. It could do this, for example, by hacking your router.

If an adversary can crack the hash of your provider’s genuine TLS certificate, it can reverse the hash to create a forged certificate. Your Open VPN software would then authenticate the connection as genuine.
Is SHA Secure?

When used to protect HTTPS websites, SHA-1 is broken. This has been known about for some time. SHA-1 websites can still be found, but are being phased out. Most browsers will now issue a warning when you try to connect to a website secured with SHA-1.

SHA-2 and SHA-3 hash functions are now recommended instead, and are secure. SHA-2 includes SHA-256, SHA-384, and SHA-512. However…

OpenVPN only uses SHA for HMAC. I don’t think it useful to go into too much detail here, but SHA hash authentication is part of the HMAC algorithm. Attacking HMAC embedded with SHA-1 is much harder than just attacking the SHA-1 hash function itself.

In other words, HMAC SHA-1 as used by OpenVPN is considered secure and there is Mathematical proof of this. Of course, HMAC SHA-2 and HMAC SHA-3 are even more secure! Indeed, the recent OpenVPN audit recognizes that HMAC SHA-1 is secure, but recommends transitioning to HMAC SHA-2 or HMAC SHA-3 instead.

Useful Guides
10 Best VPN apps for Android phones and tablets
10 Best VPN Apps For iOS (iPhone and iPad) in 2021 | Find Fast & Secure VPN Services
7 best VPNs for gaming in 2021 ( fast & secure) | Can VPNs to reduce ping?

Notes
NIST

AES, RSA, SHA-1, and SHA-2 were all developed and/or certified by the United States National Institute of Standards and Technology (NIST). This is a body that by its own admission works closely with the NSA in the development of its ciphers.

Given what we now know of the NSA’s systematic efforts to weaken or build backdoors into international encryption standards, there is every reason to question the integrity of NIST algorithms.

NIST, of course, strongly refutes such allegations:

"NIST would not deliberately weaken a cryptographic standard.”

It has also invited public participation in a number of upcoming proposed encryption standards, in a move designed to bolster public confidence.

The New York Times, however, accused the NSA of circumventing NIST-approved encryption standards by either introducing undetectable backdoors or subverting the public development process to weaken the algorithms.

This distrust was further bolstered when RSA Security (a division of EMC) privately told customers to stop using an encryption algorithm that reportedly contains a flaw engineered by the NSA. This algorithm had also been endorsed by NIST.

Furthermore, Dual_EC_DRBG (Dual Elliptic Curve Deterministic Random Bit Generator) is an encryption standard engineered by NIST. It has been known to be insecure for years.

In 2006 the Eindhoven University of Technology in the Netherlands noted that an attack against it was easy enough to launch on "an ordinary PC.” Microsoft engineers also flagged up a suspected backdoor in the algorithm.

Despite these concerns, where NIST leads, the industry follows. Microsoft, Cisco, Symantec, and RSA all include the algorithm in their product’s cryptographic libraries. This is in large part because compliance with NIST standards is a prerequisite to obtaining US government contracts.

NIST-certified cryptographic standards are pretty much ubiquitous worldwide, throughout all areas of industry and business that rely on privacy. This makes the whole situation rather chilling.

Perhaps precisely because so much relies on these standards, cryptography experts have been unwilling to face up to the problem.
AES-CBC vs AES-GCM

Until recently the only AES cipher that you were likely to encounter in the VPN world was AES-CBC (Cipher Block Chaining). This refers to the block cipher mode, a complex subject that is not really worth going into here. Although CBC may theoretically have some vulnerabilities, the general consensus is that CBC is secure. CBC is, indeed, recommended in the OpenVPN manual.

OpenVPN now also supports AES-GCM (Galios/Counter Mode).

    GCM provides authentication, removing the need for a HMAC SHA hashing function.
    It is also slightly faster than CBC because it uses hardware acceleration (by threading to multiple processor cores).

AES-CBC remains the most common mode in general use, but we are now beginning to encounter AES-GCM "in the wild." Given the advantages of GCM, this trend is only likely to continue. From a cryptographic perspective, tho9ugh, both AES-CBC, and AES-GCM are very secure.
OpenVPN UDP vs. OpenVPN TCP

OpenVPN can run over TCP (Transmission Control Protocol) or UDP (User Datagram Protocol).

    TCP = reliable. Whenever a computer sends a network packet using TCP, it waits for confirmation that the packet has arrived before sending the next packet. If no confirmation is received, it will resend the packet. This is known as error-correction. There is "guaranteed delivery” of all data, but it can be quite slow.
    UDP = fast. Using UDP, no such error correction is performed. Packets are simply sent and received with no acknowledgments or retries. This makes UDP much faster than TCP, but less reliable.

If given the choice, I suggest using the faster UDP protocol unless you experience connection problems. This is the default strategy adopted by most VPN providers.
Defeat Censorship with OpenVPN on TCP Port 443

One of the great advantages of OpenVPN is that it can be run over any port, including TCP port 443. This is the port used by HTTPS, the encrypted protocol that secures all secure websites.

Without HTTPS, no form of online commerce, such as shopping or banking, would be possible. It is therefore very rare for this port to be blocked.

As a bonus, VPN traffic on TCP port 443 can be routed inside the TLS encryption in the same way as is used by HTTPS. This makes it much harder to spot using advanced Deep Packet Inspection techniques. TCP port 443 is, therefore, the favored port for evading VPN blocks.

Many VPN providers offer the ability to change the port number used by OpenVPN using their custom software.

Even if yours does not, many VPN providers do actually support OpenVPN using TCP port 443 at the server level. You can switch to it with a simple edit to your OpenVPN configuration (.ovpn) file. It is, therefore, worth asking your VPN provider about this.

It is worth noting that network engineers dislike this tactic as TCP over TCP is very inefficient. When it comes to defeating censorship, however, it often works.

SSTP uses TCP port 443 by default.
Summaries
VPN Protocols

    PPTP is very insecure and should be avoided. While its ease of setup and cross-platform compatibility are attractive, L2TP/IPsec has the same advantages and is much more secure.
    L2TP/IPsec is a good VPN solution for non-critical use. This is especially true on legacy devices that do not support OpenVPN. It has, however, been severely compromised by the NSA.
    SSTP offers most of the advantages of OpenVPN, but is primarily only a Windows protocol. This does mean that it is better integrated into the OS, but it is poorly supported by VPN providers thanks to this limitation. In addition to this, its proprietary nature and the fact that is was created by Microsoft mean that I, for one, don’t trust it.
    IKEv2 is a very good (secure and fast) protocol. Mobile users, in particular, may even prefer it to OpenVPN due to its improved ability to reconnect when an internet connection is interrupted. For Blackberry users, it is pretty much the only option available. Use open-source versions where possible.
    OpenVPN is the recommended VPN protocol under most circumstances. It is fast, reliable, secure, and open source. It has no real downsides, per se., but to be truly secure it is important that it is implemented well. This means strong encryption with Perfect Forward Secrecy.

OpenVPN Encryption

When it comes to encryption, the devil is in the detail. It is common to see VPNs providers say they use "ultra-strong 256-bit” AES OpenVPN encryption, but this does not, in reality, tell us very much. AES-256 is indeed a strong cipher, but if other aspects of the encryption suite used are weak, then your data will not be secure.

    Cipher – this protects your actual data. AES-256 is now the industry standard and is recommended.
    Handshake – this secures your connection to the VPN server. RSA-2048+ or ECDH-384+ are secure. Importantly RSA-1024 and Diffie-Hellman handshakes are not.
    Hash authentication – creates a unique fingerprint, which is used to validate data and TLS certificates (that is, to check that the server you are connecting to really is the one you think you are connecting to). HMAC SHA-1 is absolutely fine, but HMAC SHA-2 (SHA-256, SHA-384, and SHA-512) and HMAC SHA-3 are even more secure! Note that hash authentication is not required if the AES-GCM cipher is used.
    Perfect Forward Secrecy (PFS) – this ensures that new encryption keys are created for each session. OpenVPN should not be considered secure unless PFS is implemented. This can be done either by including a Diffie-Hellman or ECDH key exchange in an RSA handshake, or a DH or ECDH handshake.
    Encryption is only as secure as its weakest point. This means that encryptions settings should be strong on both the data and control channels.
    Using higher bit lengths for ciphers and keys is almost always more secure, but this comes at a cost in speed.

OpenVPN will negotiate ciphers between client and server at will. Unless very specific parameters are defined, OpenVPN may default to weak settings. At a minimum, OpenVPN will default to Blowfish-128 cipher, RSA-1024 handshake with no PFS, and HMAC SHA-1 hash authentication.
Conclusion

Hopefully, you now have a better understanding of what makes for a secure VPN connection. When it comes to properly configuring a VPN, however, encryption is only half the story. The other half is ensuring that no traffic enters or leaves your computer outside of the VPN connection.

To learn more about this, please check out our Complete Guide to IP Leaks.
Written by: Douglas Crawford

Has worked for almost six years as senior staff writer and resident tech and VPN industry expert at ProPrivacy.com. Widely quoted on issues relating cybersecurity and digital privacy in the UK national press (The Independent & Daily Mail Online) and international technology publications such as Ars Technica.
Liked it? Share it!
Facebook
Twitter
LinkedIn
Recommended Reading
How to hide OpenVPN traffic – A Beginner's Guide

Last updated:
    January 16, 2019

The 10 most secure VPN services to keep you safe online in 2021

Last updated:
    March 4, 2021

OpenVPN over TCP vs. UDP

Last updated:
    June 23, 2013

The Ultimate Online Privacy Guide

Last updated:
    July 29, 2020

29 Comments
Lorraine
on May 17, 2018
Reply
Thank you for your excellent article.
Eng. Tarek Herik 4000 (R).
on November 26, 2017
Reply
Hi Douglas Please write about Softether protocol ( it is number 1 protocol )
https://cdn.proprivacy.com/storage/images/proprivacy/02/member-dougjpg-avatar-image-default-1png-avatar-image-default-minpng-avatar_image-small.png
Douglas Crawford replied to Eng. Tarek Herik 4000 (R).
on November 27, 2017
Reply
Hi , I discuss SoftEther in this article, but yes - I should add it to this guide when I have a spare moment..
johnny
on November 19, 2017
Reply
In fact Elliptic curves NIST P-224, P-256 and P-384 are not considered secure ( https://safecurves.cr.yp.to ). Apparently the only one that is not mention has bad is the NIST P-521 that the authors seem to agree has a good elliptic curve... "strangely" enough is almost impossible to find it in real use... because the standards where manipulate to avoid has much as possible people from using precisely this one. If you use OpenSSL it is there in the options, but nothing/ no one seems to use it.
https://cdn.proprivacy.com/storage/images/proprivacy/02/member-dougjpg-avatar-image-default-1png-avatar-image-default-minpng-avatar_image-small.png
Douglas Crawford replied to johnny
on November 20, 2017
Reply
Hi johnny, ECDH usually uses the Curve25519 elliptic curve. This is listed as "Safe" on the page you link link to.
kristy foster
on August 18, 2017
Reply
what are the security risks with using L2TP/IPsec (pre-shared key) with PAP Authentication if the tunnel is actually encrypted... also could you didn't mention EAP or Protected EAP (PEAP) using a certificate server for VPN wouldn't this be more secure then IKEv2
https://cdn.proprivacy.com/storage/images/proprivacy/02/member-dougjpg-avatar-image-default-1png-avatar-image-default-minpng-avatar_image-small.png
Douglas Crawford replied to kristy foster
on August 22, 2017
Reply
Hi kristy, I have not mentioned the authentication methods you list because they they are not used by any commercial VPN service that I am aware of. At some point I may delve deeper and extend this article into a more general technical guide to VPN technology, but that is not a priority at the moment.
Show More Got Something to Say?
Table of Contents

    Preliminaries
    What Is Encryption?
    VPN Encryption Protocols
    PPTP
    L2TP/IPsec
    SSTP
    IKEv2
    OpenVPN
    Ciphers
    Handshake Encryption
    SHA Hash Authentication
    Notes
    Summaries
    Conclusion

Comparisons

    VPN Comparisons
    Cloud Comparisons
    Password Manager Comparisons
    Email Comparisons
    Ad Blocker Comparisons
    Privacy Service Comparisons

Guides

    VPN Guides
    Cloud Guides
    Password Manager Guides
    Email Guides
    Ad Blocker Guides
    Privacy Service Guides

Reviews

    VPN Reviews
    Cloud Reviews
    Password Manager Reviews
    Email Reviews
    Ad Blocker Reviews
    Privacy Service Reviews

Our Mission

ProPrivacy is the leading resource for digital freedom. Founded in 2013, the site’s mission is to help users around the world reclaim their right to privacy.
Our Team

Our Team
Newsletter signup
Want to keep up to date on the latest privacy news?
Get our helpful guides and the latest privacy news sent straight to your inbox!
Email Address
I accept the Privacy Policy.
I'm older than 13.
We promise never to share your email address, ever.
ProPrivacy Logo
About Us Press Hub Interview Hub Charities We Support Contact Us
© 4Choice Ltd. 2021, All Rights Reserved
Disclaimer
Privacy Policy
Sitemap
