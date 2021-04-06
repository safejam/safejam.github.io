---
layout: post
title:  "When should I use a VPN?"
date:   2021-04-06 16:13:37 +0100
categories: VPNs
---

Don't use VPN services.
No, seriously, don't. You're probably reading this because you've asked what VPN service to use, and this is the answer.

Note: The content in this post does not apply to using VPN for their intended purpose; that is, as a virtual private (internal) network. It only applies to using it as a glorified proxy, which is what every third-party "VPN provider" does.

A Russian translation of this article can be found here, contributed by Timur Demin.
A Turkish translation can be found here, contributed by agyild.
There's also this article about VPN services, which is honestly better written (and has more cat pictures!) than my article.
Why not?
Because a VPN in this sense is just a glorified proxy. The VPN provider can see all your traffic, and do with it what they want - including logging.

But my provider doesn't log!
There is no way for you to verify that, and of course this is what a malicious VPN provider would claim as well. In short: the only safe assumption is that every VPN provider logs.

And remember that it is in a VPN provider's best interest to log their users - it lets them deflect blame to the customer, if they ever were to get into legal trouble. The $10/month that you're paying for your VPN service doesn't even pay for the lawyer's coffee, so expect them to hand you over.

But a provider would lose business if they did that!
I'll believe that when HideMyAss goes out of business. They gave up their users years ago, and this was widely publicized. The reality is that most of their customers will either not care or not even be aware of it.

But I pay anonymously, using Bitcoin/PaysafeCard/Cash/drugs!
Doesn't matter. You're still connecting to their service from your own IP, and they can log that.

But I want more security!
VPNs don't provide security. They are just a glorified proxy.

But I want more privacy!
VPNs don't provide privacy, with a few exceptions (detailed below). They are just a proxy. If somebody wants to tap your connection, they can still do so - they just have to do so at a different point (ie. when your traffic leaves the VPN server).

But I want more encryption!
Use SSL/TLS and HTTPS (for centralized services), or end-to-end encryption (for social or P2P applications). VPNs can't magically encrypt your traffic - it's simply not technically possible. If the endpoint expects plaintext, there is nothing you can do about that.

When using a VPN, the only encrypted part of the connection is from you to the VPN provider. From the VPN provider onwards, it is the same as it would have been without a VPN. And remember, the VPN provider can see and mess with all your traffic.

But I want to confuse trackers by sharing an IP address!
Your IP address is a largely irrelevant metric in modern tracking systems. Marketers have gotten wise to these kind of tactics, and combined with increased adoption of CGNAT and an ever-increasing amount of devices per household, it just isn't a reliable data point anymore.

Marketers will almost always use some kind of other metric to identify and distinguish you. That can be anything from a useragent to a fingerprinting profile. A VPN cannot prevent this.

So when should I use a VPN?
There are roughly two usecases where you might want to use a VPN:

You are on a known-hostile network (eg. a public airport WiFi access point, or an ISP that is known to use MITM), and you want to work around that.
You want to hide your IP from a very specific set of non-government-sanctioned adversaries - for example, circumventing a ban in a chatroom or preventing anti-piracy scareletters.
In the second case, you'd probably just want a regular proxy specifically for that traffic - sending all of your traffic over a VPN provider (like is the default with almost every VPN client) will still result in the provider being able to snoop on and mess with your traffic.

However, in practice, just don't use a VPN provider at all, even for these cases.

So, then... what?
If you absolutely need a VPN, and you understand what its limitations are, purchase a VPS and set up your own (either using something like Streisand or manually - I recommend using Wireguard). I will not recommend any specific providers (diversity is good!), but there are plenty of cheap ones to be found on LowEndTalk.

But how is that any better than a VPN service?
A VPN provider specifically seeks out those who are looking for privacy, and who may thus have interesting traffic. Statistically speaking, it is more likely that a VPN provider will be malicious or a honeypot, than that an arbitrary generic VPS provider will be.

So why do VPN services exist? Surely they must serve some purpose?
Because it's easy money. You just set up OpenVPN on a few servers, and essentially start reselling bandwidth with a markup. You can make every promise in the world, because nobody can verify them. You don't even have to know what you're doing, because again, nobody can verify what you say. It is 100% snake-oil.

So yes, VPN services do serve a purpose - it's just one that benefits the provider, not you.

This post is licensed under the WTFPL or CC0, at your choice. You may distribute, use, modify, translate, and license it in any way.

Before you comment: Be aware that any non-constructive comments will be removed. This includes advertising for VPN providers (yes, even when you phrase the marketing claims like a question), trolling, harassment, insults towards other people, claims that have already been addressed in the article, and so on.

If your comment isn't a genuine question or a concrete counterargument supported by evidence, it probably doesn't belong here.

@touya-akira
touya-akira commented on 1 Dec 2015
The post is fine but the headline is wrong. Especially since you clearly state valid use-cases for a VPN. So, yes, there are reasons to use a VPN. (Another use-case, probably covered in 2) is access to country-restricted services like netflix, bbc, etc). You just should never rely on a VPN to guarantee your anonymity.

@nv-vn
nv-vn commented on 1 Dec 2015
You just should never rely on a VPN to guarantee your anonymity

same goes for Tor or any other privacy service. you should always take as many measures as possible to prevent yourself from being tracked if you want to guarantee anonymity.

@joepie91
Owner
Author
joepie91 commented on 1 Dec 2015
@DynamicShitposter420 You're welcome to contribute to the discussion in a constructive manner (whether agreeing or not), but if all you're going to do is attacking me and trolling, then you can go elsewhere.

The post is fine but the headline is wrong. Especially since you clearly state valid use-cases for a VPN.

Yes, and this is intentional. My experience is that, whenever any claim is made of a VPN being even remotely usable for some usecases, people immediately assume that that includes theirs. This way, people need to read and understand the actual content of the article (and its described limitations and valid usecases) before drawing a conclusion.

Additionally, the concerns for "VPN services" remain applicable. You should still self-host your VPN.

@touya-akira
touya-akira commented on 2 Dec 2015
I disagree, if the use-case is avoiding DMCA letters and alike. It's way too complicated to set it up in a way so it is not tied to your name. The vast majority of torrenters lack the ability to set up a VPS (let alone make sure it's anonymous) and run VPN servers securely. A VPN provider is the better solution.

@joepie91
Owner
Author
joepie91 commented on 2 Dec 2015
If you are not capable of obtaining a VPS anonymously, you are also not capable of obtaining a VPN anonymously, so this does not make a difference. It also still does not address the privacy concerns. If you just want to torrent and use a different service as a pincushion, then what you want is a proxy, not a VPN.

@touya-akira
touya-akira commented on 3 Dec 2015
How does it matter that you're not able to obtain a VPN anonymously (we are talking about IP-address I suppose)? Your point in the original is that you're never anonymous to the VPN (which is why you shouldn't trust them). However, they don't pass on data to DMCA litigation companies (unless we are talking about HMA and alike who clearly state in their ToS that they log & pass on data).

As for proxies, how are they more secure? Also, please tell me where I get a 1Gbit proxy with unlimited traffic and ideally port forwarding, I'd definitely be using that.

@apostolisd
apostolisd commented on 28 Dec 2015
Ok, but if you use TOR and VPN?

@johwest
johwest commented on 11 Jan 2016
A better solution is pay voor use from usenet and torrents ,so that your no longer afraid for trouble.
Now cost VPN money.

@weissjeffm
weissjeffm commented on 28 Mar 2016
How does using your own VPS help? It's still easy for someone to trace the IP to your VPS and then to you.

@atoponce
atoponce commented on 18 Apr 2016
I think the take-away here is not not fool yourself into thinking that VPN is some sort of short-cut for Tor. In other words, don't fool yourself into thinking you're anonymous, and for the love of everything good and holy, don't think that your VPN will go to jail for your activities.

However, I use VPN services all the time (for example, https://freevpn.ninja). There are times when either:

I am behind a restrictive firewall, such as at a public library or a church.
I need to get into an internal network with other clients, such as my browser.
And I don't buy the argument that your IP address is not a valuable asset to trackers and ad companies. Some website owners block Tor, because they cannot get honest GeoIP lookups out of a client when the request comes out af a Tor exit relay. In fact, the whole point of Tor is to obfuscate your source IP address, while remaining encrypted between the Tor client and the relays.

However, as mentioned, don't have any false ideas about your security or anonymity when using VPN services. Understand the tech and your risks using the tech. That applies for anything, not just VPN and Tor.

@1n1r2
1n1r2 commented on 16 Jul 2016
VPN services have been bothering me since forever. This is the first article I have found to address my concerns.

Yes: VPN builds a secure tunnel
No: It does not protect my private communication
It's a giant keylogger on the net that I have given permission to steal my keystrokes.

It merely funnels the secure keystrokes through a proxy that can log them.

I think I'm safer logging in directly to secure connections ( https: ) to a specific site.

Talk me down, please. Why should I trust any single portal ( even if they do have multiple
connection sites ) to monitor my internet traffic ? Oh sure, it might be preferable in an
insecure environment like an airport terminal or coffee shop.

I trusted my employer's VPN while I was working, but I'm retired now.

Still looking for more articles or discussion to address my paranoia.

@karanssh
karanssh commented on 31 Jul 2016
This makes absolutely no sense.

Do not use HideMyAss, Expat Shield, Hotspot Shield because they datamine/keep logs.

Do not use ProXPN, at 300kbp for free, you are going to limit your speeds to around 31KBs/s. Not only that but they do not use a open source client and the level of security is not confirmed to be completely secure.

VPNReactor is confirmed to have logs, but you are welcome to use it. They have a 30 minute time limit, then you have to wait another 30 minutes.

Do not use TOR or Ultrasurf, Although some software take advantage of it, these tools are meant for threatened bloggers, anonymous free speech and whistleblowing, not so you can download the latest Justin Bieber album.

Personally, I prefer to run my own VPN for $10/$15 a year using a cheap 128MB VPS from either Prometeus [the best] or Ramnode. You can also use it for other such as running a very small seedbox or web seed, or a tiny bittorrent tracker. The problem with this is that if you use legitimate details, the VPN could be traced back to you, but that's the same with VPNs that use a dedicated IP address who will cut you off, but using a shared IP address could mean a couple of software conflicts.

@GnstheGrain
GnstheGrain commented on 8 Sep 2016
I wish more input would comes in on that nice thread..
I totally agree with https://gist.github.com/joepie91/5a9909939e6ce7d09e29#but-how-is-that-any-better-than-a-vpn-service
But then again, VPS provider such as DO or Linode does have your IP address and Logs. which is enought for any warrant to fuck you up.

@Rich700000000000
Rich700000000000 commented on 20 Sep 2016 • 
You're still connecting to their service from your own IP, and they can log that.

two paragraphs later:

Your IP address is a largely irrelevant metric in modern tracking systems.

Also:

If you absolutely need a VPN, and you understand what its limitations are, purchase a VPS and set up your own. I will not recommend any specific providers (diversity is good!), but there are plenty of cheap ones to be found on LowEndBox.

Statistically speaking, it is more likely that a VPN provider will be malicious or a honeypot, than that an arbitrary generic VPS provider will be.

So let me get this straight: VPNs aren't anonymous, so I should give my credit card to Digitalocean instead?
Statistically speaking, it is more likely that a VPS provider will give you up if a cop so much as glances in their direction, where as a reputable VPN company will at least attempt to push back.
Most all VPS providers are anti-p2p, which is what most people use a vpn for.
Go on, find me a VPS with unlimited bandwidth, forever. I'll be waiting.
I think your main problem is that you're mixing up threat models. If I wanted total anonymity, I'd have a laptop with the usb ports hot-glued shut in an anti-EMP bag under my bed, running Tails off of a flash drive, only connect to wifi stolen from the neighbors with a yagi antenna two meters across, use tor AND run my own tor relay so that they couldn't determine the origin of the traffic.

But I don't want to do that. I want to read FanFiction without being judged by the sysadmins at Comcast. Which is why I have a VPN.

Also, you are NOT going to stand there and tell me that EVERY VPN SERVICE IN EXISTACE is a honeypot. That's not a safe assumption, that's stallman-meets-alexjones paranoid. Do you know how much that would cost? How complex that would be?
There have been court cases:

https://torrentfreak.com/vpn-providers-no-logging-claims-tested-in-fbi-case-160312/

And all they could do was shrug their shoulders.

Also, ever heard of a Warrant Canary?

TLDR: FUD 0/10, FUD with rice 0.01/10

@Con7e
Con7e commented on 30 Nov 2016
I agree with @Rich700000000000 .

The question here is: who can you trust more, your ISP or your VPN provider? Your ISP must not be trusted by default (especially now in the UK), hence a decent VPN provider is your best bet, the "lesser of the two evils".

@gwigz
gwigz commented on 1 Dec 2016
What about plausible deniability, with a shared IP?

@jameshadley
jameshadley commented on 30 Dec 2016 • 
I'm glad you're shining a light on public ignorance around VPN/proxy services but I don't agree that VPN services are useless. Most large/popular sites now use/require TLS and it is often the case that the visitor would prefer that the VPN provider were able to see the packet headers than their own ISP.

Why? Your own ISP have a lot of other information about you and, especially in the UK, are relied upon to supply the Government with personal information. It is less likely that a VPN provider would immediately divulge metadata to a government to which it does not answer - and it has less personal information about its customers than the residential/commercial ISP.

Sure, setting up your own is better in some ways. In others, it's not. For example, a commercial VPN will share IPs so it's harder to correlate packets leaving your home/office connection with packets arriving somewhere else. That said, for most people, the overwhelming feeling is expedience. When you have a full time job, a family and so on, a commercial VPN means one less thing to worry about.

Actually, I would not be surprised if several of the large, well-known, well-funded US-based VPN services are honeypots. But of course, there is plenty of choice and a bit of research can go a long way.

@nikki2150
nikki2150 commented on 4 Jan 2017
Never had a vpn and I've been sharing files for a long time, never had a summons from the MPAA or any other agency, never set foot in a court. Logically these snoop agencies can't monitor everyone's activity, it would cost a fortune. The cases where people have been taken to court for file sharing are few and far between in the UK where I live, I feel many of these VPN services are sold on a fear factor. UK ISP's will surrender your personal details if threatend with a court summons, proving that you were the person responsible for sharing the file is the difficult part.

@tsjnachos117
tsjnachos117 commented on 5 Jan 2017 • 
I do agree with many of the points made in this article. However, I'm not so sure it's a good idea to reject VPN services altogether. Rather, it seems to me like a better solution is to use VPN services with caution.

There are advantages to using a VPN over a proxy. For one thing, since VPN providers usually have their own websites, it's usually not too hard to find a privacy policy (although, as pointed out in the article, verifying that the provider is doing what said policy says is nearly-impossible). Whenever I search for a proxy, I'm usually greeted with a webpage, which in turn is just a list of IP addresses and ports (presumably from third party servers). Tracking down each address to find anything resembling a privacy policy is far too complicated for many users. On top of which, there might not be any such policy to find, so it's really had to know what's being logged, and what isn't.

Most VPN providers like to brag about the encryption they use. Although it can be hard to know for sure what encryption is actually being used (many providers like to say "advanced" or "military grade" without really specifying which encryption method is actually being used), that's still better than many proxies, which might not be using any encryption at all. (PS: avoid using old protocols like PPTP. PPTP is particularly bad, since it only supports a few encryption techniques, all of which have become outdated. I generally recommend OpenVPN.)

Also, since proxies don't route everything (only apps configured to use said proxies), there's no guarantee your browser's extensions (Java, Silverlight, Flash, etc.), which are often run in separate executable processes, will also be routed. If they are not routed, you can generally expect said extension to leak your IP address. On top of which, many browsers will leak the users' public IP address, even if you don't have any such addons installed. For example, Firefox is prone to WebRTC leaks, and DNS leaks. If you are using a VPN, Firefox will only leak your VPN provider's IP address, NOT your actual IP address (or, at least that's my experience on Ubuntu, when NetworkManager is set to create a virtual "tun" device).

Of course, hiding your IP address is only the first step in protecting your privacy. Hardening your browser is equally important. If you use a browser that supports a large number of addons (Mozilla Firefox, Google Chrome, Chromium, etc), you'll find plenty of privacy-enhancing addons like Privacy Badger, NoScript, HTTPS Everywhere (or as I like to call it, "HTTPS wherever possible, including pages that offer HTTPS, but for some reason refuse to use it by default". Doesn't exactly roll off the tongue, does it?), uBlock Origin, DecentralEyes (Firefox only), and a boatload of others. Setting your user agent to whatever the most popular OS is (probably Windows 7 at the time of this writing) can help you blend into the crowd. It's also a good idea to get a canvas-blocking addons to prevent canvas fingerprinting. Last but not least, make sure to wipe your browsing info regularly. This is especially true for cookies, offline/HTML storage, and LSOs (aka "Flash Cookies"), as this information could easily be used to identify you.

As a final note, I'd like to mention the fact that all the privacy protection in the world won't mean a thing if you don't use said protection wisely. The TOR project, which aims to provide privacy through encrypted proxy-like relays (which, in turn, can be hosted by anyone who's willing to donate some of their bandwidth), has a very good list of DOs and DONTs, which can easily be applied to VPNs as well. Essentially, you compromise your privacy protections by identifying yourself (typically by clicking the "login" button) to a website, especially privacy-invading sites like Google and Facebook.

@RobertasVis
RobertasVis commented on 24 Jan 2017
How about Open Source & Decentralized VPN? What do you think - would it help solve at least part of the problem?

@arkbg1
arkbg1 commented on 25 Jan 2017
Could you recommend any proxies? I'm asking for a friend.

@Trauma7
Trauma7 commented on 15 Feb 2017
He is absolutely correct! I am speaking from experience. From being betrayed by over a dozen of them. From the highest to lowest priced and recognizable free ones. If you are being stalked or tracked, an employee in an internet service provider ( any one they find you connecting to ) can and will betray you with the name of the VPN you are using. Then they move on to the VPN to betray you, with either two types of paper if you know what i mean. Do not listen to the lies! All VPN's have the ability, can and to monitor your connection to them.

@Trauma7
Trauma7 commented on 15 Feb 2017
The last should read; can and will monitor your connection to them. Even to the point of knowing the mac address of your device when you try to log on with a ISP unbeknownst to them.

@k0nsl
k0nsl commented on 3 Mar 2017
LOL, @nukeop.

@Rocksarecool
Rocksarecool commented on 29 Mar 2017
Let's not forget to mention about how VPNs beg you so hard to pay them
It's very rare to find a free VPN
Every free VPN contains MB at the end all want you to pay money.
Seriously is there other way to stay secured?

@ghost
ghost commented on 5 Apr 2017
I always thought the concept of a "VPN provider" was a bit of an oxymoron. I'd argue the most commonly intended implementation of a VPN is to bridge two private (trusted) networks over an insecure network, as opposed to knowingly letting some guy MITM all your traffic.

@farinspace
farinspace commented on 5 May 2017 • 
Excellent read, highly recommend that anyone who stumbles upon this page, go back and wade through the comments:

see: https://gist.github.com/joepie91/5a9909939e6ce7d09e29#gistcomment-1838431
see: https://gist.github.com/joepie91/5a9909939e6ce7d09e29#gistcomment-1963364
see: https://gist.github.com/joepie91/5a9909939e6ce7d09e29#gistcomment-1959840
see: https://gist.github.com/joepie91/5a9909939e6ce7d09e29#gistcomment-1637023

Your computer communicates i many ways you likely are not even aware of, email checking in the background, twitter checking, auto Facebook heart beat, apple server heart beat, iCloud pinging, browser logged into different services, etc. etc .. connecting with a VPN at a software level or even at a router level still exposes these communications on the same "line" you think is private. You likely need an entirely new device, purpose based, not associated with your identity ... and also consider from which network you establish a connection from (e.g. your ISP).

Additionally keep in mind that timestamps and IP addresses will both likely lead to the tracking down of accounts that are associated with your VPN or VPS leading to your identity.

As @jameshadley mentioned, many of these so-called secure VPNs could very well be honeypots.

As @joepie91 mentioned if you are not able to obtain a VPN, VPS anonymously there exists enough data to trace back to your identity.

@mottosso
mottosso commented on 16 May 2017
I disagree, if the use-case is avoiding DMCA letters and alike.

This has been my use-case as well. I've also found it useful to access pages otherwise restricted by country, such as streaming South Park from their official page. Not interested in security or anonymity.

@Blargyblarg
Blargyblarg commented on 17 May 2017
I was considering a VPN service because I generally tether my pc to my phone and use my phone's unlimited data since the ISP's in my area suck so much donkey ass. I ran my unrestricted tethering data out then just used an app to tether it and prevent the bandwidth restriction from affecting me. Since the network congestion on my phone is basically non-existent my speed is pretty good compared to what I got from landline ISPs even after exceeding the monthly limit and being given lower priority. However, I'd very much like to avoid any unnecessary questions regarding my usage (lots of pc gaming). Would a VPN service help with that?

@KarmmenElektra
KarmmenElektra commented on 20 May 2017
I would usually agree with you but there are many good services out there, you just need to know which one to choose from the myriad of providers, many are bad, many keep logs of what you are doing, but there a few of them that are quite reliable. Some even offer free trials for you to test their software before purchasing anything, i would advise you to look into some lists of the best vpn services in 2017 .

@kezzydrew23
kezzydrew23 commented on 28 May 2017
You all should check out Mysterium an opensource and decentralized VPN This definitely could solve the problem. It's equally built on a block chain technology @nukeop

@blhyip518
blhyip518 commented on 31 May 2017 • 
I find many reviews at google seach results.How much credibility do you think as they talk? such as this one.
Best VPN Services of 2017 – Top VPN in the World
https://itday.com/vpn/best-vpn-services-of-2017/

@jjssoftware
jjssoftware commented on 11 Jun 2017
You are on a known-hostile network (eg. a public airport WiFi access point, or an ISP that is known to use MITM)

This is now increasingly becoming a problem where ISPs are being handed the power to do whatever they like with their customers' metadata. If you're in the position of having no choice but to use an ISP that has this power and you're in doubt as to whether your usage data is being sold, monitored or you're being traffic shaped due to what the ISP believes you're doing, this strengthens the case for using a VPN.

Legislation is moving to make ISPs hostile to their own customers and for the moment use of VPNs are not criminalized, but who knows how long this will be the case.

purchase a VPS and set up your own

This statement is a "stop, wait" moment because this is subject to exactly the same argument and consideration as But my provider doesn't log! and There is no way for you to verify that. Unless you own an entire data center and own all the tin and edge devices that the VPS depends on, there's no way to know if the VPS provider is retaining network logs or not. This presents exactly the same problem you have if you use a public VPN service - how can you fully trust the VPS host provider?

This gist is biased towards positing arguments against end users using VPN services and the issues in that area. However there's a whole other scenario that this gist doesn't touch upon at all: consider a business that is co-located with two branches that are connected via VPN technology for sharing sensitive business data between the offices. The business might use a regular ISP with static IPs either end or a private WAN circuit provided via some telecoms provider.

Clearly there's no commercial VPN service in play here in this B2B scenario, the VPN servers is / are hosted within the business on private hardware, the VPN technology in use will be a flavor of exactly the same VPN technology used by all commercial VPN service providers and in this case we have true end to end tunnel encryption. In this scenario it's 100% incorrect to make a sweeping generalization statement of "do not use a VPN" because this type of setup works and can be trusted.

Where does that leave us? For personal user use where encrypted tunneled traffic leaves the VPN and exits onto the internet I agree that the implementation and use of any VPN involves a certain amount of trust. Whether you use a public commercial service or you host your own VPN server on a remote VPS makes no difference to this fact. Whatever the type of VPN, the weak link is the part you don't have full control of - the part just after where the traffic leaves the tunnel and becomes regular non-tunneled / non encrypted traffic. In other words if you must use a VPN for general internet use, choose carefully before you put your trust in any provider.

For the record, for my own personal use case I lean towards a self hosted VPN as being the best option.

@sofiahambly
sofiahambly commented on 12 Jun 2017
Personally, I am using Express VPN for last two years and I have never experienced any kind of problem till now. The only Trusted VPN service I would like to recommend. Express VPN providing me with best promising service. It is better to go safe and go for trusted VPN service and provide strong encryption rather than to wasting money on not so good VPN Service Providers. https://www.reviewsdir.com/best-encrypted-vpn-providers/

@szepeviktor
szepeviktor commented on 17 Jun 2017 • 
I lease a $3 VPS and use PuTTY as a SOCKS proxy. Firefox is set to use it.

Benefits:

continuous connection - don't have to wait for TCP to build up
datacenter networking and DNS resolvers
IPv6 access
fixed IP address
@EdRoxter
EdRoxter commented on 19 Jun 2017
@1n1r2 https://gist.github.com/joepie91/5a9909939e6ce7d09e29#gistcomment-1827407

Yes: VPN builds a secure tunnel
No: It does not protect my private communication
It's a giant keylogger on the net that I have given permission to steal my keystrokes.
It merely funnels the secure keystrokes through a proxy that can log them.

While this is true for proxies (HTTP[S] proxies) because they have to "break" TLS encryption by design, it's not true for VPN software that configures a routing set on your PC to route all traffic over the VPN provider's servers. This happens on another OSI level than classic proxying, so with a VPN connection your traffic to the site you're logging into (Apple ID, Microsoft Account, whatever) is still end-to-end encrypted. You can validate this by looking at the TLS certificate when you're visiting the website.

@muzikman
muzikman commented on 12 Jul 2017 • 
How do I avoid the automated emails after I download torrents that are being watched? That's the only reason I wanted to use a VPN. I don't want to get busted downloading torrents directly.

I have been doing a lot of research on VPN's the past month. I tried a few out for free. Tried to trick some services to see if it worked and it did. I read some interesting information from PIA about DNS Leaking, etc..... Yes, of course they will tell you want you want to hear. It's a business.

If a VPN isn't what I am looking for to download torrents safely, is there anything that will?

Also - Is it true that ISPs will throttle your bandwidth based on the source/content? If so, wouldn't a VPN prevent this?

Thanks,
Matt

@f1r4s
f1r4s commented on 6 Aug 2017
Personally, i would love to be a bot in this fucking world and be one of Fast-flux network!

I think if Fast-flux techniques lead us to be using it as our proxy we will be in safe place... !

@IllIlllIlIll
IllIlllIlIll commented on 19 Aug 2017
Then
How Do you trust your vps server provider,.
And What's more how about the ISP for your vps server provider.

@kamilla
kamilla commented on 21 Aug 2017 • 
The post is interesting and does raise many valuable points and issues, but I still agree on more with touya-akira, atoponce, Rich700000000000 and other well reasoned arguments.

I wasn't so interested in my privacy before. I always thought that I wasn't doing anything that I wouldn't mind anyone to know. And if I did do something that I wanted to keep in private, I used TOR and other countermeasures to hide my online actions. I never thought that those anti-piracy letters that were already been sent in the US could be threat at all here in Finland. And as you can guess, I was wrong. Anti-piracy-letter-blackmailers landed in Finland about 2-3 years ago in big way. Lawsuits began to appear and even then I thought that those charges would never hold. I was wrong again. I was stunned to see the Finnish District Court gave a verdict where the defendant was sentenced as guilty and ordered to pay enormous amounts of compensation. (800 euros / one TV episode that he was downloading (or missclicked, the sentence based on still capture and no proofs of complete downloads or even sharing 1 byte were made at all)). Just few weeks after that I got my first blackmail-letter from Hedman & Partners (the legal battle is still ongoing).

After the incident I started to search VPN providers and found very promising one, NordVPN (this is not a commercial! make your own decisions!), that at least promised to not log anything and offered other nice features, so I decided to try that. Now it's been almost 2 years without a single blackmail-letter. My friends with no VPN have got those letters and few of them even have had to pay the amount in court decision (or they didn't want to start a big legal battle against evil blackmailing companies, in which they couldn't be sure to have won here in Finland). So yes, VPN has done a great job for me and I keep trusting them way more than I would for example my ISP, that initially was the one who gave thousands and thousands of IP addresses and personal information to blackmailing companies like Hedman Partners. Thank god it was decided now year ago, that it is illegal to hand over thousands of IPs and identified data based only on IP address logs on the wiretapping-tool (that itself did and does share way more data than any individual as they have to join to torrent swarm to get any data).

I definitely trust more to my VPN than I trust for my government for example. And what comes to VPS and other self hosted systems, why on the earth would you trust them more to not give your private information than VPN provider that allows anonymous registration and payments? And even if you could get VPS anonymously. The glorified proxy as you see the VPN as, offers more security because of its shared IP. And at least I haven't read any story about VPN company (at least here in Europe) that would have given its customers personal data and connection logs (if they even exist) to government officials or blackmailing companies. There are also some legal battles concerning the logging and they have all dried out to see that there were no logs, as others have already mentioned.

Of course VPN is not a magic tool to hide you or anything. You need to know what it is and what are you doing with it. Same goes for TOR and other privacy offering services. They are next to nothing when used incorrectly. But not all VPN:s are evil, even if some of the free ones are. (Who even uses free VPN and thinks that they are not trying to exploit you? I know, money is not a guarantee to make service better, but still)

@g33klord
g33klord commented on 8 Sep 2017
Here by VPN you mean "third party VPN service provider". What if I have set up my own VPN servers. With projects like Algo (https://github.com/trailofbits/algo) It has become very easy to setup your own VPN server.

I don't want my ISP to see what I am browsing.

@tdemin
tdemin commented on 10 Sep 2017
@g33klord the article mentions this as a preferred way to do things if you still have to use a VPN. So, the article has got you covered. 😉

@icyunv98
icyunv98 commented on 12 Sep 2017
Nice article. I assume that there's really no such thing as anonymity on the world wide web. That being said i do use a vpn so that i stop getting those warnings from my isp.

@AsyaKarapetyan
AsyaKarapetyan commented on 19 Sep 2017
I disagree. Using a VPN is safe especially when you use free wi-fi in public places and can be easily hacked. Here is an article which explains how VPN works https://vpnclientapp.com/blog/what-is-vpn/

@yangyichris
yangyichris commented on 27 Sep 2017
I use OpenVPN for several years, but now I think softether is the best encrypted VPN protocol, here is a post discuss about it,
https://privatevpnservice.com/softether-vpn/
And set up a VPN by yourself on vps is easy, but i dont want to take my time to do it :)

@notjoe
notjoe commented on 30 Sep 2017
Hey there,

VPNs are probably even worse than your ISP assuming you're not using a trusted VPN. Think about it for a minute. Your ISP has less to gain by stealing your packetz than a rogue VPN Provider.

@nf3
nf3 commented on 9 Nov 2017
I wrote an article in this same vein on what are the important criteria in choosing (or not choosing a VPN as this original gist would recommend). My article address many of the points that this gist touch upon.
https://www.magnumvpn.com/vpn-providers.html

And like many of the commentors, I agree and recommend that TOR plus a VPN is the the current best privacy practice in order to shield yourself from 3rd party eyes.

@nukeop
nukeop commented on 11 Nov 2017
Article sponsored by the NSA

@Klinsen
Klinsen commented on 10 Dec 2017
For me, a VPN is an important tool. In my country there are always restrictions to sensitive content which isn't all the time sensitive. If you want freedom on the net then a VPN is for you. on the other hand, it can even protect you from Hackers Yeah hackers https://www.bestvpndeals.com/can-vpn-protect-from-hackers/

@emilyanncr
emilyanncr commented on 11 Dec 2017 • 
There's quite a few analytical inaccuracies in this article but my primary issue is the statement that all VPN providers log traffic. That is simply not true. Recently, IP Vanish, Private Internet Access and other VPNs have suspended operations in Russia because Russian laws conflict with their no-log policy. In a case in March of last year, the FBI subpoenaed Private Internet Access for their logs and PIA refused stating:
“Our company was subpoenaed by the FBI for user activity logs relating to this matter,” London Trust Media Executive Chairman Andrew Lee informs TorrentFreak.

“After scrutinizing the validity of the subpoena and confirming it, we restated as we always do the content of our privacy policy and then we notified the agent that we do not log any user activity. The agent confirmed his understanding of our company’s policy and position and then pursued alternative leads.

“This report makes it clear that PIA does not log user activity and we continue to stand by our commitment to our users.” (https://torrentfreak.com/vpn-providers-no-logging-claims-tested-in-fbi-case-160312/)

@Bomper
Bomper commented on 19 Dec 2017 • 
This article started well, but got a lot of junk and spam comments. Gists don't send notifications, so @joepie91 never came back in 2+ years.

Anyways, the most reliable source (recommended by the EFF) for comparing VPN services is https://thatoneprivacysite.net/vpn-section/. From there you can look up VPNs that don't log, are located outside major surveillance jurisdictions ("5 eyes"), have good business ethics etc. Mullvad.net is one of the best. It accepts Bitcoin and the first three hours are free. Their support is quite remarkable - I got a reply to the only issue I had with them in under an hour. You don't have to use their app - you can use the standard OpenVPN service that works on Mac, Windows and Linux, so there's no way to get malware from Mullvad.

@pablospe
pablospe commented on 2 Jan 2018
The mysterium network (a decentralized VPN) has been mentioned. I was wondering your opinion about this, and if this could be a solution to the current VPN problems mentioned here; namely, the need to trust in VPS or VPN providers.

@frazras
frazras commented on 7 Feb 2018
@joepie91 would the perfect VPN be a service that offers preconfigured VPNs on your own secured VPS with an encrypted hard disk?

@rosoposo
rosoposo commented on 14 Feb 2018
BTW, I use a private VPN server which can be setup on aws in a few minutes https://github.com/webdigi/AWS-VPN-Server-Setup

No logging on server side guaranteed. AWS could monitor but I do not think of that as an issue for my use cases.

@bramswenson
bramswenson commented on 14 Feb 2018
Better yet, seek out reasonable advice from those proven to be invested in our privacy: https://ssd.eff.org/

@medatlas
medatlas commented on 14 Feb 2018
Saying that VPN providers log all traffic is a big assumption! First, It’s impossible to log trillions of GBs daily. Second, your traffic is supposed to go through a secure tunnel between you and your provider. Third, it’s easy to know if your provider decrypts your traffic: simply view SSL certificate of the website that you are visiting and see if your VPN provider replaces it with its own. If SSL certificate is issued to the website that you are visiting then you are safe. Some providers offer a second layer of encryption and in this case they need to work as MITM. If you own an iPhone an App called Inspect can help you to view SSL certificates. Regarding ISPs, they have no interest to decrypt your traffic unless a big brother asks them to do so! ISPs still have interest in some metadata that FCC allow them to collect and sell. So the decision to use VPN or not depends on what you want to achieve and what are your risks to be victim of spying or stalking!

@lordgreg
lordgreg commented on 14 Feb 2018
You forgot to add one crucial point about VPN. Where the server is located (country). Meaning the law prosecution triggers more in some countries and less in another.

And... how is home VPN same as VPN in country XYZ? my VPN is always my VPN address. VPN provider elsewhere adds at least one layer aka. another ip. And where is your data retention time mentioned? You're missing some big points in your article.

However, its written in a way people should consider using own brain before buying a VPN service.

@iamandrewluca
iamandrewluca commented on 14 Feb 2018
If I'm providing VPN Services. Am I in any danger? For example government wants info about some customers and I don't want to provide it.

@HelioCampos
HelioCampos commented on 14 Feb 2018
@CHEF-KOCK if they (police) start their search in the destination, they will have the content you were looking for. All they will require from your vpn provider is where this connection come from and not its content. And this is the only data the a vpn or a vps provider could log and handle. Any way, there are good cases to use a vps and vpn providers, like living in countries that free speach is forbidden, so I would like to provide an alternative to commercial vpn. Its the Streisand project that automate the configuration of a number of tool to surf anonymously: https://github.com/StreisandEffect/streisand/blob/master/README.md
Again, it should not be used to access private contents or for hacking because it would be wrong and it would give the police an excuse to go after you and your IP in the vps provider than in your ISP.

@ghost
ghost commented on 14 Feb 2018
Would strongly recommend this for setting up your own vpn, super easy to use:
https://github.com/trailofbits/algo

@robdunne-uom
robdunne-uom commented on 14 Feb 2018
Security advice that 99.9% of Internet users can’t implement is garbage information.

@igorescobar
igorescobar commented on 14 Feb 2018
It's easier to hack into your neighbors WiFi do what you got to do and get out :*

@hollerith
hollerith commented on 14 Feb 2018
If it makes no difference then why not? You are always on a known-hostile network (i.e. EVERY NETWORK). VPN is a misnomer - it is not truly 100% private. However, most paid for services are good enough to bypass ISP. You could set up your own, extend your network slightly to bypass your ISP, appear in different locales, https://github.com/trailofbits/algo is easy enough, on a cheap cloud provider. If you do implement VPN make sure you route DNS through your VPN. If you want absolute nation-state proof privacy - it can't really be had that easily as even TOR is pretty well mapped now. You're gonna need a bigger boat.

@Pushergene
Pushergene commented on 14 Feb 2018
This is just bullshit. ProtonVPN is very secure and should be used. Others like Hotspotshield and Betternet should not be used.
https://epiphany12.github.io/
here you can see very trusted VPNS in good countries.
This Post is OLD! Stop trusting this useless shit. Some VPNs can provide 90% Anonymity.

@ttlequals0
ttlequals0 commented on 14 Feb 2018 • 
Shameless plug, but there is a reason why I made this https://github.com/ttlequals0/autovpn

I can make disposable VPN endpoints anywhere in the world.

Pros
I pay as I need no monthly subscription.

You always will have a fresh endpoint, making it unlikely to compromised without you knowing.

Cons
This is not meant to be used for illegal activities but more of a way to protect your self on hostile networks.

There is a lack of anonymity because you have an AWS account tied to credit card.

There is an inherent trust in AWS. They probably log and most likely don't monitor traffic

@Pushergene
Pushergene commented on 15 Feb 2018 • 
@ttlequals0

Payment Method is not so important... Because your payment won't be written in the Logs. If the Service is Trustworthy, your payment informations won't be compromised. Its just about what VPN-Service you are paying for. It's important where the VPN is based at. They have to respect the Laws, so it means they can't just say they cannot see what you are doing while using the VPN. And in some countries there's no data retention law. US VPN's should not be used.

ISP's react to requests for data informations from lawyers when it's about filesharing. Good VPN's ignore requests from lawyers because theres no court order.
Some Countries dont have Data Retention laws and are outside US and EU. For example ExpressVPN, NordVPN, VPN.ac, Perfect-Privacy, ProtonVPN are in good countries.

@alanhogan
alanhogan commented on 15 Feb 2018
rather ill-considered. the advice to set up your own proxy / host your own VPN trades a lot of things away just to make sure you are not being logged by a VPN service. Your cost is probably more, reliability probably less, and your traffic may be much more readily identifiable as 'you' because instead of sharing an address with other customers, it’s … just you. Take into account the reasons someone may want a VPN.

@mhsabbagh
mhsabbagh commented on 15 Feb 2018
Those people in the comments linking to their own articles/websites trying to bring in few visitors/customers are pathetic.

@megawattz
megawattz commented on 16 Feb 2018 • 
I would only direct certain traffic through a VPN, not everthing. Dedicate one browser to be the VPN browser.

Why? Because IP Address is not the only identifying data you are sending. Cookies, E-Tags and other methods can identify you uniquely and VPNs don't block any of that. Also a VPN will direct ALL traffic, not just browser traffic. Who knows what your apps are transmitting? If you send ANY identifying data thought the VPN then the attacker can associate THAT data with your non-identifying data by assuming the same TCP addresses showing indentifying data are yours. Also ONLY use HTTPS websites, never HTTP. A VPN does not decrypt your HTTPS connection. i.e. you cannot be attacked by a man-in-the-middle. (Unless the NSA has co-opted all digital certificates which is actually a distinct possibility)

Dedicate one browser as the private browser, that and only that uses the VPN. Opera has a built in VPN. Also always use the incognito or privacy mode also. This deletes cookies after your session so you can only be identified as "this person" for your session, and no longer. Set the browser to NOT retain 3rd party cookies to reduce tracking in general.

Now, all your vanilla traffic you use your normal, open browser. "Look NSA, I'm just a solid citizen, taking my vaccines, watching CNN and voting for Hillary". But for stuff that has any degree of controversy, use the private VPN dedicated browser. "Look Chief, this isn't our guy. This is Mr. Brain Dead American zombie wanker. He's not into anything weird". (wink wink, nudge nudge, say no more)

@nordvpnsucks
nordvpnsucks commented on 18 Feb 2018
I do not know how or why but my personal experience has shown me that using vpn is LESS secure then not using vpn. I started using vpn about a month ago and things have been worse, not better, in relation to privacy.

@MichaelVPN
MichaelVPN commented on 18 Feb 2018 • 
This is a bunch of crap. You make valid points but you forget that without a VPN you still have to trust the ISP that you are using. Even when you build your own VPN, there are so many drawbacks that come with that. Limited locations, limited app support, network experience and so many other things that are required to do it right which the 99% consumers has no awareness off.

Basically, your VPN provider becomes your ISP. Your write up assumes every VPN provider is malicious. This couldn't be further from the truth and while you can't verify what they do with your encryption keys and data, you HAVE to trust some entity...and I would much rather trust a VPN company versus an ISP who 1000% is going to track me and resell my data and browsing activity. You can find a huge list of VPNs and everything about them at vpn.com.

As for your reference of a glorified proxy is terrible too. A proxy uses no encryption which is exactly what differentiates it from a VPN. Regardless of who has access to this encryption (you, your ISP, or your VPN provider), a VPN offers a lot more benefits than a "glorified proxy" or simply not using one altogether.

@mr25thfret
mr25thfret commented on 20 Feb 2018
Great read (comments included). Much appreciated.

@wenell
wenell commented on 22 Feb 2018
Well, I don't think all VPNs are log users activities. I thought there is no need to use VPN after the read user's reviews. I really feel that I should need to use VPN. I use VPN all the time and on all devices like Laptop and Smartphone, etc. without VPN I feel like unsafe because I pay the bills via credit card while using public wifi. I don't think all VPN provider log users activities because they claim that they do not log users activities and I think I am using log less VPN. I don't know if they record activities, but we can trust them there no other way.

@dmzpkts
dmzpkts commented on 23 Feb 2018
They finally let you out of jail Sven????

This "article" was written by a person who had his IRC server rooted, and compromised all of the users across his network. The group responsible released over a million lines of chatlogs. Joepie found them and apparently thought that echoing the word "cocks" into the file would delete the rest...

Nope.

See for yourselves.

" Towards the end of this dump, we just stopped taking backups and left tail -f
running. joepie97 found the hook, just a little too late (a million PMs in
the PM log alone). He then ran: "echo 'cocks' > ._IRCD". Interestingly,
neither Stanford, nor Gentoo developers, nor the EFF list "echo 'cocks'>file"
as a secure deletion method. As such, we proceeded to take the latest copy
directly off the HDD (sed cocks). Check out the Files section for the
chanlogs & PM logs. "
https://www.exploit-db.com/papers/42901/

Sven Slootweg is no one to listen to when it comes to security.

@ghost
ghost commented on 25 Feb 2018
For slightly better privacy during browsing - use a VPN combined with a cloud based browser in private mode like silo or puffin. Website attributes it to cloud ip, all cookies are sent to and stored on cloud server, cannot correlate it with windows update logs, VPN knows you are visiting the domain cloudmosa, nothing is stored locally unless you download it. I wouldn't do my banking on it though.

@contrawise
contrawise commented on 26 Feb 2018
Now that US ISPs are allowed to sniff our data legally and share it, I believe a carefully selected commercial VPN service is more likely to be looking out for my privacy than my ISP. I only have a couple of ISPs to choose from, and both have shown themselves to be quite self-centered. I'll take my chances with my respected VPN provider.

@rojagit
rojagit commented on 16 Mar 2018
I tend to trust PIA (though their client sucks) just with the statement 'no one has been busted yet using PIA'

https://www.privateinternetaccess.com/forum/discussion/19273/am-i-really-anonymous

@JohnMasonVPN
JohnMasonVPN commented on 26 Mar 2018 • 
Kinda agree with you here. Earlier VPNs used to be a good tool, but now there's more than 100 different VPNs, some of them using shared/cloud 3rd party servers, many have fake "no logs", although claiming so (hint: PureVPN & HideMyass: https://thebestvpn.com/118-vpns-logging-policy).

If you really need a VPN, you should try using the ones that allow anonymous payment options such as Mullvad or ExpressVPN. Just my 2 cents...

@shipdog7
shipdog7 commented on 27 Mar 2018
26 of the 115 most popular VPNs are secretly keeping tabs on you. Do a search and look it up. A recent investigation into 115 of the world’s most popular VPN services revealed that many are antithetical to their stated claims. To build trust, providers make promises not to track users through logs or other identifying information. But as a popular VPN comparison site found out, this isn’t always true. The Best VPN recently peeked under the hood of over 100 of the biggest VPN services. All told, 26 of them collect three or more important log files that could contain personal and identifying information — things like your IP address, location, bandwidth data, and connection timestamps.

@ricardokittrell11
ricardokittrell11 commented on 30 Mar 2018
I successfully do transactions with LiviaCoins. You can try it but you will have to thank me later.﻿

@galik
galik commented on 31 Mar 2018 • 
AirVPN Have printed a personal rebuttal to this article here: https://airvpn.org/topic/26206-rebuttal-of-article-dont-use-vpn-services/

Obviously you can make wild claims about any group of businesses, accusing them of whatever you like. That doesn't mean that all of them are.

@Geraner
Geraner commented on 31 Mar 2018 • 
It remembers me about another interesting article regarding this topic.
Are VPN providers more trustworthy than your ISP?

@IfitissoRedditorsarereallyclever
IfitissoRedditorsarereallyclever commented on 17 Apr 2018
I thank you from the bottom of my heart because you sure have the guts!
I was tired, tired of Redditors, because everyone is making this VPN providers popular by saying some bullshit and then everyone follow that opinion like sheep. Idiots, they're called, because they speak without any knowledge at all, without any knowledge of IT security whatsoever. You sure showed of being able to use the brain to think. Indeed, all these people trusting random business about their data are just fools. These fools are even here, offended since the article make them believe they're wasting money (indeed, they don't know the value of money, too), just have a look at the comments. I think VPN is a geek trend like Bose is for headphones. But every time I look info about them I get 90% of people who doesn't provide any reason behind their statements, it took me a while to find this.

Hackers have often been arrested under the stupid VPN protection. Surely, any VPN providers who claim to don't log you and care about your privacy will protect users while they browse Pornhub, but none will do if there are serious legal issues, as the police won't stop if that's the case (in USA, FBI don't give a fu** about people watching porn and protecting their anonimity..., but it gives a shi** if someone seriously break the law. Elsewhere, it's the same). As a proof of what I'm saying, not even one serious hacker would trust a VPN provider as safe for their tasks and their job. Now, since you do need to believe your fantasy and illusions, since we're not speaking about privacy or security, but of a trend, like Bose, Apple, or an expensive car, I'll leave you to continue defending your super VPN provider. After all, they're nothing more than a business making money, they must be good at marketing to make their products sell, so it's their intention to make you believe they're a beneficial organization. People need illusions, 'cause people need to spend money as a status quo. That is why VPN mostly exist. It's not anyone is evil, it's just business, and the geeks are the one who are going to buy. Anyway, most of the user don't really need anonymity so any VPN is fine as it is their ISP (the author spoke about P2P and scare-letters, indeed). If it'll come the time somehow you'll want to protect your anonymity from the worst of the case, first you'll realize it is actually impossible, then you'll do your best instead of believing some company advertising shit.
It's all for today.

PS/TL;DR: I was seriously wondering if we have the brain for something, cause the more I googled, the more I just found the same stuff said over and over without any logic behind it, regarding VPN. The ones who defend themselves they're just ridiculous. I want to see a VPN provider not giving out their logs in the case of an illegal issue (i.e. killer), then you can say they don't keep logs... Of course it won't happen, since the lawyer is cost and they're a Company, they won't pay out of their pockets. This is like the encryption and the $5 wrench, https://imgs.xkcd.com/comics/security.png (no matter the efforts, some idiot will still believe their encrypted porn collection is safe).
I've put many efforts at empathizing the porn thing to make people realize most of this VPN users don't need anonymity, it's just the cool thing of it. I also use proxy, VPN and stuff sometimes, but I realize they're not safe and I do only to bypass country restrictions, anyway.
I'd recommend anyone to head over to Tails site and have a good read of what anonymity really is, what is your fingerprint (no, not the browser, yours...) and why true anonymity is impossible. Those FAQ and articles on that website were written by people who know about security, and who research before opening their mouth.
Thank you, author, again, since you go against the general mainstream opinions.

@AndersonKay
AndersonKay commented on 20 Apr 2018
First of all, why there is a translation to russian? When Russia is actually one of the most who needs a vpn?((https://www.zdnet.com/article/google-amazon-drawn-into-telegram-ban-as-russia-blocks-1-8-million-ip-addresses/ )
Secondly, there is a tough difference between proxy and vpn: proxy only changes your IP, and vpn actually encrypts your activity, so you wouldnt call vpn a ‘glorified proxy’ because it is false.
Thirdly, about data retention laws - the countries which doesnt have those laws are usually outside US and EU, so you would want to look at ProtonVPN or NordVPN (based in Panama).

@49e94b8f256530dc0d41f740dfe8a4c1
49e94b8f256530dc0d41f740dfe8a4c1 commented on 16 Jun 2018 • 
Heres how I see it. VPN provider services are safe for small time crooks. VPN services, Tor and all other encryption technologies that have humans involved are all just toys providing a false sense of security. If they want to catch you, they will catch you irregardless. The three letter agencies are increasingly everywhere. From processor manufacturers; Intel to CA Authorities; Verisign.

But catching you means investing in a good and talented forensic and legal team. Resources are scarce. They have to make choices. So if the cost of catching you is greater than the damage you make, you are left alone. You are sent annoying letters. A random opportunist who wants to exploit the law and rip you off might take the golden opportunity. But if the damage you make the industry in the long run is greater than the cost of catching you, you'll get got in a few months. The internet is a large place and you probably fucked up years or a decade ago leaving pieces of yourself in your uniquely fingerprintable machines. I'm sure there is some incriminating information about you lying around somewhere. In the event of an indictment, a VPN service provider might consult with lawyers and weigh the risk of taking on your case.

They might want the publicity. Any publicity is good publicity they say. Sometimes the lawyers will tell the board, "we can't win the case." And nobody really wants to go to jail or lose their cash cow for you and your 100 € p.a subscription.

@duketwo
duketwo commented on 16 Jun 2018
The article itself is pretty awkward to read. Some of the opinions make up for it at least. @nukeop

@mmendescortes
mmendescortes commented on 16 Jun 2018
Dude, change the title...

There are uses for a VPN... Like setting up a bridged network to link computers... I used a bridged VPN with DHCP and a Squid proxy in order to unify my local machines with my cellphone and any computer I might need to use while traveling... This way I can access files, ssh and other services from anywhere in the same way I do in my home...

Yes, you said truths...

But this post title is a bait! It nearly discouraged me from using a vpn... A while ago, when I was trying to find a way to unify my machines, servers and mobile devices, I saw your post and it nearly made me give up the idea for using a VPN...

Please, change your title...

@jcanfield
jcanfield commented on 17 Jun 2018
As most of the commenters pointed out, the title is misleading. Yes, you point out Note: The content in this post does not apply to using VPN for their intended purpose; that is, as a virtual private (internal) network. It only applies to using it as a glorified proxy, which is what every third-party "VPN provider" does. but you could still change it. Maybe Reasons not to use VPN Services (Outside of their intended purpose) or something. Just a thought.

@Piv475
Piv475 commented on 27 Jun 2018
I know nothing of the ins and outs of VPN VPS TOR etc. But the simple way of looking at all of them if you expect to hide your activity is: how difficult is it for a government agency to form a vpn? they already do it and you may be using it. Do not be fooled into thinking "they can't do that, it would be illegal" (I am ex special forces and believe me they do many things that are not legal, it is all about being found out, and they have far greater resources than you will ever have). It is a collective information center for corruption and illegal activities. You all then use it, sell your wares, buy your dope, whine about spies, worry about information theft, steal films and music, whatever it is that you feel the need to hide. If you cant hide it yourself, it is not to be trusted.

@moti-safer
moti-safer commented on 14 Aug 2018
Well , SaferVPN has a real "No log policy" explained here: No log VPN

@krisives
krisives commented on 27 Aug 2018
@moti-safer There is no way to prove that a VPN is not logging or has not been forced by law (via warrant) to intercept communications. Probably better to use Tor.

@ilmaisin
ilmaisin commented on 1 Sep 2018
@galik I stopped reading on the "A proxy tunnels (and not necessarily encrypts) only TCP traffic (proxies can not support UDP)" part. There certainly are proxies for UDP traffic too. SOCKS5 can do that for example.

@CzarnaMamba
CzarnaMamba commented on 3 Sep 2018
VPNs are a real money maker, thus that protonvpn case for instance.

@jorj1
jorj1 commented on 11 Sep 2018
Just a comment for those crazy about logs and setting up their own VPN: You're aware that logging still happens, right ? It is just at your ISP level instead of a VPS or VPN provider. Logging is everywhere.

Note for the author: you're still biased and made an article just for the sake of having some traffic and this is the part I don't understand, why would you need it ? Make your own blog and put these kind of clickbait titles to score some pennies from advertising ads.

Dear seekers, use VPN for what it is because it is a wonderful tool. For any other purposes, accept the drawback. Simple as that.

@cacarr-pdxweb
cacarr-pdxweb commented on 14 Sep 2018
The rebuttal to this at AirVPN is thorough and highly persuasive:

https://airvpn.org/topic/26206-rebuttal-of-article-dont-use-vpn-services/

@Jon-guy30
Jon-guy30 commented on 14 Sep 2018
If you want security and privacy you need to use open-source tools. Things like Tor, opensource encryption tools like Veracrypt and special purpose operating systems like TAILS. And if you want to hide the fact you're using Tor from your ISP, an obfuscated bridge (check Tor project home page) is the best tool for that. If you want maximum privacy use "Pluggable Transports". And if a website resource is blocked through geo-blocking you can go to the torrc file and add "ExitNodes {DE}" without quotes to force the exit node to a specific country. And once you're finished just comment it out. Again, check the Tor project website. When looking for privacy and security tips always go to the Tor project webpage (and in case of Veracrypt go to their webpage), do not rely on opinions from other people. Always verify opinions/facts.

Even when using the vanilla Tor network (no bridges) it's still hard to detect any one single person. Yes, the ISP can see you're on Tor (and websites can identify you're on tor), but they can't see what you're doing, it'll look like any other net activity, especially if you use it often enough. And you won't look suspicious if you try to use it as your main web browser. Use the security sliders provided by Tor button to disable active elements, I personally use the safer and safest settings. Do not go to noscript and change the configurations. Only enable javascript selectively and temporarily.

Tor is not slow, you can watch youtube videos on it (just don't fullscreen the web browser, resize it instead, use theater mode!). At most the delay can be 30 seconds when loading a webpage, for me it's mostly 5-15 seconds, faster if you disable active elements. You're not that impatient are you?

Finally, be smart. Don't reveal identifying information such as names, your actual primary and personal email addresses. Basically don't do anything you're already doing on the clearnet over the Tor network and vice versa. Don't login to google and facebook if you have those accounts on the clearnet, they'll know who you are. Only use accounts created with Tor on Tor! And if you're shopping, don't you're personal bank card, use a pre-paid one (non-renewable). Also ALWAYS verify checksums AND GPG signatures of software you download if they provide them.

AND if you still want a VPN or a similar service, build your own! A VPN is a single point of failure. Yes it provides better privacy, but not anonymity!

TAILS is better if you want your entire computer routed through Tor.

@fixitrod
fixitrod commented on 14 Sep 2018
Bottom line, if your not communicating from a secure point to a secure point through the VPN (or encrypted path) there's an inherent risk and a point that can be argued.

You could even argue the encryption could be compromised on the point to point encrypted path. For traffic to get from A to B and back again there's a way to "decode" it.

But, what ISP is going to take the lengthy amount of time to decode it when there are much easier targets to spend their time on?

@system123
system123 commented on 17 Nov 2018
Using a VPS and running your own VPN is pointless. The only reason VPNs etc work are because you hide amongst other people. If you running your own VPN, on a VPS which you own and you are the only user of this VPN you might as well not bother. Even if the VPS is anonymous if you are the only IP connecting to it you just uncovered yourself.

@paragonie-scott
paragonie-scott commented on 7 Jan 2019
@system123 Congrats, you just discovered the motivation for Tor.

@ParityError
ParityError commented on 13 Jan 2019
If connected to the internet there's always a way to find you...

@ayellowbeard
ayellowbeard commented on 6 Feb 2019
I will never forget the one time I forgot to turn on ExpressVPN to torrented a particular movie, after which, a month later I got a copyright warning email from my ISP naming the particular movie I "supposedly" downloaded.
I also have subscribed to an anonymous proxies for the last few years but am not sure how well it does it's job and so for the last couple of years have used additional encryption beyond what the VPN uses. Lately I'm experimenting with reverse proxies to see how well they work.

@MajinKaan
MajinKaan commented on 25 Feb 2019 • 
ExpressVPN laughs at this pathethic post. The Turkish government found absolutely nothig when they seized one of their servers.
https://torrentfreak.com/vpn-server-seized-to-investigate-russian-ambassadors-assassination-1171219/

@sudha73
sudha73 commented on 6 Mar 2019
I think VPN is a must yeah things might be different with various brands but for me, I have been using Express VPN and it seems to be best for me
https://technoidhub.com/security/pros-cons-vpn-android-phones-need/7757/

@strypey
strypey commented on 11 Mar 2019
Another legitimate reason for using a commercial VPN not mentioned in the original piece is to get access to unfiltered internet. This is useful for people using nosy ISPs that throttle or block some forms of traffic, and for anyone behind government filters like the Great Firewall of China. Because so many people use commercial VPNs in a country like China, it doesn't make the user particularly interesting (especially if they're an ex-pat). But if a user rents a VPS, and uses it to set up their own VPN, there's a risk they'll stand out like dog's balls, and attract more targeted surveillance.

@skyerjoe
skyerjoe commented on 2 Apr 2019
Here by VPN you mean "third party VPN service provider". What if I have set up my own VPN servers. With projects like Algo (https://github.com/trailofbits/algo) It has become very easy to setup your own VPN server.

I don't want my ISP to see what I am browsing.

The same problem with possibly logging ur hosting provider.

regards

@ghost
ghost commented on 13 Apr 2019
Joepie, you are hilariously wrong.

You realize there have been VPN providers that have been PROVEN to retain no logs? Some have been subpoenaed by courts but were unable to comply for requests for logs due to them not existing. In other cases, such as in the case of perfect-privacy (a vpn service that has been existence for a decade longer "joepie91" has been a known community figure), they had their servers RAIDED by police without warning and had two servers seized that turned up absolutely nothing.

It is true for all but 3-5 VPN providers that their claims to no logs are useless, but there are at-least 3 that have been forced by law enforcement to test that case (often for very high profile and extreme cases).

Its laughable because this post makes me think that it was inspired by your groups enormous failure of using HIDEMYASS... dude that was originally started by a former AOLer/web template creator Zymic if I recall correctly. It was one of the newest VPNs on the market when companies like perfect-privacy had existed and been the VPN of choice in the "community" even when the number of personal VPN providers online numbered at probably less than 10.

This article speaks volumes of your ignorance on VPNs and their history.

btw are you in contact with viraL by chance, i knew him prolly a decade before he got involved with your former groups exploits and when he was still kid holding an online marriage between himself and a girl on a game called activeworlds. id love to catch up with that goofball

@ghost
ghost commented on 13 Apr 2019 • 
Joepie91, you are hilariously wrong.

You realize there have been VPN providers that have been PROVEN to retain no logs? Some have been subpoenaed by courts but were unable to comply for requests for logs due to them not existing. In other cases, such as in the case of perfect-privacy (a vpn service that has been existence for a decade longer "joepie91" has been a known community figure), they had their servers RAIDED by police without warning and had two servers seized that turned up absolutely nothing.

It is true for all but 3-5 VPN providers that their claims to no logs are useless, but there are at-least 3 that have been forced by law enforcement to test that case (often for very high profile and extreme cases).

Its laughable because this post makes me think that it was inspired by your groups enormous failure of using HIDEMYASS... dude that was originally started by a former AOLer/web template creator Zymic if I recall correctly. It was one of the newest VPNs on the market when companies like perfect-privacy had existed and been the VPN of choice in the "community" even when the number of personal VPN providers online numbered at probably less than 10.

This article speaks volumes of your ignorance on VPNs and their history.

btw are you in contact with viraL by chance, i knew him prolly a decade before he got involved with your former groups exploits and when he was still kid holding an online marriage between himself and a girl on a game called activeworlds. id love to catch up with that goofball

@gincow
gincow commented on 25 Apr 2019
disagree, if the use-case is avoiding DMCA letters and alike.

For my purposes, I have the following setup: a VPN on its own VPS for privacy focused online activities and another VPN (commercial provider) that only tunnels P2P traffic.

So I can trust my own VPN setup and trust a VPN provider with my P2P traffic only.

Incidentally, I find the list of leaked data from VPN leaks (vpnleaks.com) quite remarkable.

@k9t9
k9t9 commented on 26 Apr 2019
`There are roughly two usecases where you might want to use a VPN

You totally ignore a third usecase and that is when certain services / apps / locations / informations are totally blocked and unavailable.
I think that a trip to China / Turkey / Iran etc.. would make you realize a whole of a lot more about why VPN are needed ..

@sudhabhise
sudhabhise commented on 29 Apr 2019
i think using free VPN is no good https://technoidhub.com/app/why-not-to-use-free-vpn-service/10509/ correct me if i am wrong?

@nyuszika7h
nyuszika7h commented on 10 May 2019
Setting up your own server as a VPN/proxy for circumventing geoblocks is not always easy, as many services block known hosting provider IPs. There are VPNs specifically offering residential IPs or other IPs that are guaranteed to work with those services.

@flaing
flaing commented on 12 May 2019
this is true. because no company would risk to not debug, while debugging needs logs.
but vpn services are still very good for couple of reasons. in usecases you may want to have couple of VPNs.

@logizadav
logizadav commented on 13 May 2019
OP is correct VPN's are broken TLS/SSL is also broken depending on who is looking at your traffic pretty much half the internet is broken. Goodbye.

@guijob
guijob commented on 20 Jun 2019
These arguments are so generic that I could use them to prevent people from even using social media, cloud services ... even a computer or a phone in general. It's all about choosing a reliable service instead of the type service at all.

@viraladmin
viraladmin commented on 25 Jun 2019 • 
First, hats off to the OP for making a post that 3 and a half years later is still controversial enough to get comment.

Setting that aside, lets address all the serious elephant in the room no one seems to be talking about. Everyone both agreeing and disagreeing with this thread seems to be thinking backwards. VPN's (and TOR, i2p, or any other means of hiding identity) is done to mask the users activities, not to mask the user. If some entity knows who they are trying to track, tracking the user is simple (and VPS with a VPN and/or Proxy installed won't prevent this either). They start at the IP, they get the logs of the user, if the logs lean to a VPN, they get he logs of the VPN, if the logs of the VPN lead to TOR, they try to set up nodes to track the user from the VPN to the node (this is much harder with TOR now using a Guard nodes that don;t expire for months at a time).

My point is, if someone is targeting you and they have resources, its only a matter of time. They will trace the steps until they find you.

This however, does not discredit the use of VPN's, TOR, i2p or other such measures because more often than not, its not that anyone is targeting a user, its that that they are targeting a users activities and then trying to back-trace to the user. THIS IS CONSIDERABLY HARDER to do - so much harder in fact, that the masses can get away.

Lets use people buying and selling drugs over hidden services through tor. First a government has to try to seize a website over tor, then after that, they have to try to setup nodes to track IP's to those services, then they have to get logs from a VPN basically saying "We can see someone accessed tor through your VPN and we have enough logs of when this user did that for you to hand over your logs so we can try to map them back to their ISP", and then contact the ISP to find out who that user is.

Anyone who thinks this is easy because mega-entities and governments have the resources, is vastly kidding themselves. It takes governments months and months and months, years at times, just to track users of a single website. This is why drugs, child pornography, whistle blowing, and everything else illegal thrives on the hidden web and why you don't hear of new arrests every few months, but rather every few years. This is why with the exception of a couple MASSIVE cases most people are not caught through tracking, but through user stupidity (using postal service to sell drugs, tracking pedophiles based on faces in videos, backgrounds, furniture, etc.).

As such, claiming VPN's (which are really just glorified proxies with massive more bandwidth), TOR, ip2, or any other services are useless and shouldn't be used, is vastly misinformed. They are not foolproof. Nothing about using a computer is except perhaps liking yourself in a lead room with no networking capability. However the idea is to make it so massively hard that unless you are some hardcore criminal (a pedophile, a hitman, etc) that governments and mega entities won't bother. If you use services like these o pirate software, movies, games and the likes, most are not going to spend the money to even bother to find out who you are. If you are the sick and deranged however, you are not going to be protected. Given enough time (and they have all the time in the world) they WILL eventually find you.

So absolutely VPN's are useful. They are just not foolproof. There is a massive difference.

@metalstorm2019
metalstorm2019 commented on 5 Jul 2019
I will make this short, sweet and to the point. Not all VPN'S are the same. If you live in the US or certain other countries then using a VPN in those countries is useless. Five Eyes etc. are countries that have treaties to serve you up when you use a VPN. So if your using a VPN in any of those countries its a waste of money and effort simply put. I read all the comments on this article and no one here spoke of this and that leads me to feel everyone here is either ill informed or a parasite to mislead the masses. Also the people posting affiliate links to the VPN they are providing to make a buck should be ashamed of themselves. You don't give a crap you just spam your affiliate links. I fully expect my post to be removed because it cuts straight to the real agenda of this post and its commentators. Do your research stay away from the five eyes nine eyes fourteen eye VPN hosted countries that's just some healthy advice. I have an excel sheet of 168 VPN companies that details exactly what they offer and where they stand on all the world policies but i cant attach it. Also you want to make sure that the VPN has a warrant canary. Message me if you want to review it.

This is from Wiki:

The Five Eyes, often abbreviated as FVEY, is an anglophone intelligence alliance comprising Australia, Canada, New Zealand, the United Kingdom and the United States. These countries are parties to the multilateral UKUSA Agreement, a treaty for joint cooperation in signals intelligence.[1][2][3]

The origins of the FVEY can be traced back to the post–World War II period, when the Atlantic Charter was issued by the Allies to lay out their goals for a post-war world. During the course of the Cold War, the ECHELON surveillance system was initially developed by the FVEY to monitor the communications of the former Soviet Union and the Eastern Bloc, although it is now used to monitor billions of private communications worldwide.[4][5]

In the late 1990s, the existence of ECHELON was disclosed to the public, triggering a major debate in the European Parliament and, to a lesser extent, the United States Congress. As part of efforts in the ongoing War on Terror since 2001, the FVEY further expanded their surveillance capabilities, with much emphasis placed on monitoring the World Wide Web. The former NSA contractor Edward Snowden described the Five Eyes as a "supra-national intelligence organisation that does not answer to the known laws of its own countries".[6] Documents leaked by Snowden in 2013 revealed that the FVEY have been spying on one another's citizens and sharing the collected information with each other in order to circumvent restrictive domestic regulations on surveillance of citizens.[7][8][9][10]

In spite of continued controversy over its methods, the Five Eyes relationship remains one of the most comprehensive known espionage alliances in history.[11]

NSA Headquarters, Fort Meade, Maryland, United States

ASIO central office, Canberra, Australia

GCHQ, Cheltenham, Gloucestershire, United Kingdom

CSE, Ottawa, Ontario, Canada
Since processed intelligence is gathered from multiple sources, the intelligence shared is not restricted to signals intelligence (SIGINT) and often involves defence intelligence as well as human intelligence (HUMINT) and geospatial intelligence (GEOINT). The following table provides an overview of most of the FVEY agencies involved in such forms of data sharing.[1]

@ghost
 ghost commented on 5 Jul 2019
Many do not realize that you can setup a VPN on your personal router for
less than these companies charge - register a domain, setup dynamic dns and
OpenVPN on your home router (get an Asus for example) and you are protected
when using public networks. However, you should always assume all your
activity is public and can be traced back to you. You can protect content
with encryption but not the address. Paying for anonymous browsing is a
waste of money.
On Fri, Jul 5, 2019 at 2:47 AM metalstorm2019 ***@***.***> wrote:
 I will make this short, sweet and to the point. Not all VPN'S are the
 same. If you live in the US or certain other countries then using a VPN in
 those countries is useless. Five Eyes etc. are countries that have treaties
 to serve you up when you use a VPN. So if your using a VPN in any of those
 countries its a waste of money and effort simply put. I read all the
 comments on this article and no one here spoke of this and that leads me to
 feel everyone here is either ill informed or a parasite to mislead the
 masses. Also the people posting affiliate links to the VPN they are
 providing to make a buck should be ashamed of themselves. You don't give a
 crap you just spam your affiliate links. I fully expect my post to be
 removed because it cuts straight to the real agenda of this post and its
 commentators. Do your research stay away from the five eyes nine eyes
 fourteen eye VPN hosted countries that's just some healthy advice. I have
 an excel sheet of 168 VPN companies that details exactly what they offer
 and where they stand on all the world policies but i cant attach it. Also
 you want to make sure that the VPN has a warrant canary. Message me if you
 want to review it.

 This is from Wiki:

 The Five Eyes, often abbreviated as FVEY, is an anglophone intelligence
 alliance comprising Australia, Canada, New Zealand, the United Kingdom and
 the United States. These countries are parties to the multilateral UKUSA
 Agreement, a treaty for joint cooperation in signals intelligence.[1][2][3]

 The origins of the FVEY can be traced back to the post–World War II
 period, when the Atlantic Charter was issued by the Allies to lay out their
 goals for a post-war world. During the course of the Cold War, the ECHELON
 surveillance system was initially developed by the FVEY to monitor the
 communications of the former Soviet Union and the Eastern Bloc, although it
 is now used to monitor billions of private communications worldwide.[4][5]

 In the late 1990s, the existence of ECHELON was disclosed to the public,
 triggering a major debate in the European Parliament and, to a lesser
 extent, the United States Congress. As part of efforts in the ongoing War
 on Terror since 2001, the FVEY further expanded their surveillance
 capabilities, with much emphasis placed on monitoring the World Wide Web.
 The former NSA contractor Edward Snowden described the Five Eyes as a
 "supra-national intelligence organisation that does not answer to the known
 laws of its own countries".[6] Documents leaked by Snowden in 2013 revealed
 that the FVEY have been spying on one another's citizens and sharing the
 collected information with each other in order to circumvent restrictive
 domestic regulations on surveillance of citizens.[7][8][9][10]

 In spite of continued controversy over its methods, the Five Eyes
 relationship remains one of the most comprehensive known espionage
 alliances in history.[11]

 NSA Headquarters, Fort Meade, Maryland, United States

 ASIO central office, Canberra, Australia

 GCHQ, Cheltenham, Gloucestershire, United Kingdom

 CSE, Ottawa, Ontario, Canada
 Since processed intelligence is gathered from multiple sources, the
 intelligence shared is not restricted to signals intelligence (SIGINT) and
 often involves defence intelligence as well as human intelligence (HUMINT)
 and geospatial intelligence (GEOINT). The following table provides an
 overview of most of the FVEY agencies involved in such forms of data
 sharing.[1]

 —
 You are receiving this because you commented.
 Reply to this email directly, view it on GitHub
 <https://gist.github.com/5a9909939e6ce7d09e29?email_source=notifications&email_token=ACK22A4JS4HRVQL4PMJMLITP53VBVA5CNFSM4HILFQFKYY3PNVWWK3TUL52HS4DFVNDWS43UINXW23LFNZ2KUY3PNVWWK3TUL5UWJTQAFU2AG#gistcomment-2962435>,
 or mute the thread
 <https://github.com/notifications/unsubscribe-auth/ACK22A7ECXYOP626CTOIF23P53VBVANCNFSM4HILFQFA>
 .
-- 
Allen Jensen
@viraladmin
viraladmin commented on 5 Jul 2019
metalstorm2019 - Your paranoia defies all logic and actually comes across as someone who would be part of some government agency trying to convince its citizens that "there is no point so just don't bother". Its factually inaccurate based on cases that have taken place in the US justice system.

Quoting SirFuzzo

"You realize there have been VPN providers that have been PROVEN to retain no logs? Some have been subpoenaed by courts but were unable to comply for requests for logs due to them not existing. In other cases, such as in the case of perfect-privacy (a vpn service that has been existence for a decade longer "joepie91" has been a known community figure), they had their servers RAIDED by police without warning and had two servers seized that turned up absolutely nothing."

Based on your 'its useless to bother' belief - that would be an impossibility because these "eyes" are all seeing gods that no one can ever hide from if they are in those countries. Apparently, the US justice system must have just forgotten to check their magical logs since they can see all and know all.

What I will say is here is there is no reason to trust any company claiming they don't store logs unless they have proven through seizures that they actually don't have logs. I will also say if you are setting up your own VPN on a random VPS or dedicated server, there is absolutely 0 protections that the hosting company won't have a copy of your activities.. in fact pretty much all server hosting companies and colo providers are logging.

However everything one does online should relate to their risk factor. If all one wants to do is bypass netflix location blocks, who the provider is shouldn't make a craps bit of difference... because no one cares what you watch on netflix.

I do agree with you that all people considering a vpn, should chose wisely (keeping their risk factor in mind). I would add to that, trust nothing but your own research... even others with "lists" they have "personally compiled". You never know who is on the other end of a keyboard. After all we are on a microsoft owned website.

I will make this short, sweet and to the point. Not all VPN'S are the same. If you live in the US or certain other countries then using a VPN in those countries is useless. Five Eyes etc. are countries that have treaties to serve you up when you use a VPN. So if your using a VPN in any of those countries its a waste of money and effort simply put. I read all the comments on this article and no one here spoke of this and that leads me to feel everyone here is either ill informed or a parasite to mislead the masses. Also the people posting affiliate links to the VPN they are providing to make a buck should be ashamed of themselves. You don't give a crap you just spam your affiliate links. I fully expect my post to be removed because it cuts straight to the real agenda of this post and its commentators. Do your research stay away from the five eyes nine eyes fourteen eye VPN hosted countries that's just some healthy advice. I have an excel sheet of 168 VPN companies that details exactly what they offer and where they stand on all the world policies but i cant attach it. Also you want to make sure that the VPN has a warrant canary. Message me if you want to review it.

@metalstorm2019
metalstorm2019 commented on 5 Jul 2019
metalstorm2019 - Your paranoia defies all logic and actually comes across as someone who would be part of some government agency trying to convince its citizens that "there is no point so just don't bother". Its factually inaccurate based on cases that have taken place in the US justice system.

Quoting SirFuzzo

"You realize there have been VPN providers that have been PROVEN to retain no logs? Some have been subpoenaed by courts but were unable to comply for requests for logs due to them not existing. In other cases, such as in the case of perfect-privacy (a vpn service that has been existence for a decade longer "joepie91" has been a known community figure), they had their servers RAIDED by police without warning and had two servers seized that turned up absolutely nothing."

Based on your 'its useless to bother' belief - that would be an impossibility because these "eyes" are all seeing gods that no one can ever hide from if they are in those countries. Apparently, the US justice system must have just forgotten to check their magical logs since they can see all and know all.

What I will say is here is there is no reason to trust any company claiming they don't store logs unless they have proven through seizures that they actually don't have logs. I will also say if you are setting up your own VPN on a random VPS or dedicated server, there is absolutely 0 protections that the hosting company won't have a copy of your activities.. in fact pretty much all server hosting companies and colo providers are logging.

However everything one does online should relate to their risk factor. If all one wants to do is bypass netflix location blocks, who the provider is shouldn't make a craps bit of difference... because no one cares what you watch on netflix.

I do agree with you that all people considering a vpn, should chose wisely (keeping their risk factor in mind). I would add to that, trust nothing but your own research... even others with "lists" they have "personally compiled". You never know who is on the other end of a keyboard. After all we are on a microsoft owned website.

I will make this short, sweet and to the point. Not all VPN'S are the same. If you live in the US or certain other countries then using a VPN in those countries is useless. Five Eyes etc. are countries that have treaties to serve you up when you use a VPN. So if your using a VPN in any of those countries its a waste of money and effort simply put. I read all the comments on this article and no one here spoke of this and that leads me to feel everyone here is either ill informed or a parasite to mislead the masses. Also the people posting affiliate links to the VPN they are providing to make a buck should be ashamed of themselves. You don't give a crap you just spam your affiliate links. I fully expect my post to be removed because it cuts straight to the real agenda of this post and its commentators. Do your research stay away from the five eyes nine eyes fourteen eye VPN hosted countries that's just some healthy advice. I have an excel sheet of 168 VPN companies that details exactly what they offer and where they stand on all the world policies but i cant attach it. Also you want to make sure that the VPN has a warrant canary. Message me if you want to review it.

@viraladmin My point is this. If you use a company in any of the countries that have the agreement you will never be private no matter how hard you try. They keep logs and will give you up when asked to simple as that. Like I stated if your going to use a VPN and pay for it use one from a company in a country that is not in agreement to hand over any data whether they keep logs or not. The canary feature defeats the gag order as the VPN company is not alerting the compromised individual directly. I agree with what you stated about if all your doing is watching Netflix who cares. But if your going to pay a company for VPN service do it correctly.

@hjyoung1
hjyoung1 commented on 7 Jul 2019
https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/

@antekone
antekone commented on 4 Aug 2019
If anyone is reading the comments in this thread, please note that there are lots of throw-away accounts made only to advertise VPN providers. Before you read an opinion, click on the username to verify this user has an account with some content first.

@kkinder
kkinder commented on 4 Aug 2019
I want the 2 minutes I wasted reading that back.

@mehditlili
mehditlili commented on 9 Aug 2019
Dude your forgot Netflix!!! Good luck unblocking the US content with a proxy.

@JonnyBanana
JonnyBanana commented on 10 Aug 2019
How about Open Source & Decentralized VPN? What do you think - would it help solve at least part of the problem?

nice idea dude!

@dcormier
dcormier commented on 16 Aug 2019
PureVPN have the following section in their privacy policy:

We DO NOT keep any record of your browsing activities, connection logs, records of the VPN IPs assigned to you, your original IPs, your connection time, the history of your browsing, the sites you visited, your outgoing traffic, the content or data you accessed, or the DNS queries generated by you.

And yet, they were able to be quite helpful to the prosecution in a cyberstalking case (PDF link).

@robertovalerio
robertovalerio commented on 16 Aug 2019
+1 for https://github.com/trailofbits/algo

Easy to set up and destroy and it works with cheap online virtual servers from AWS, Digital Ocean etc. You can recreate a new personal VPN every other week with running a script for 10 minutes.

@zexa
zexa commented on 27 Aug 2019
Yeah, hosting your own VPN with algo is cool and stuff, but I'd like to decrease the scope of this whole discussion and mention, that as per my interpretation of the this article, the author was talking about commercial VPN's.

That being said, I do a agree that there is no way to confirm that a VPN is not logging my data and as the author also mentioned, you can make all the promises in the world claiming to be transparent even though in reality you can be doing all sorts of stuff behind the scenes.

For a split second I had the thought, that maybe people would be interested in having a VPN which would grant you read-only access to the whole system. That being said, as I mentioned in the previous paragraph, you can still be doing all sorts of things behind the scenes, such as log the packets on a gateway machine.

VPNs, for the sake of privacy, are a lost cause. The whole idea is based on trust and it's impossible to trust in a commercial for profit company. Even a non-commercial company cannot be trusted, as it's an unsustainable business model.

@DockJumper86
DockJumper86 commented on 15 Oct 2019
Ok. So there is a lot of truth in here and a lot of BS that should be cleared out. Most of you obviously don't understand anything about the OSI layers and the routing protocols. The anonymous nature of your traffic can absolutely be verified.

VPN's use layer 2 and 3 routing/encryption protocols like L2TP paired with IPSec. The TLS connections you make to the websites are all layer 5-6 so they have no interaction with the VPN's routing. As long as you are not using HTTP only then no, the VPN providers cannot see your traffic. I don't know where people got that. SSL/TLS connections are END-to-END, meaning your browser to whatever server you are talking to. Nobody in between can see what that is. That is great and all as long as you trust the server because they will certainly have your information, unless you use a VPN which will obfuscate your real IP. So if anybody showed up to them (who runs the server) then they will only be able to point to the VPN address. Then IF the VPN logs than it could possibly go back to you, but not with any data, only traffic analysis.

Now this is where I will say that I don't fully trust or know if my VPN provider logs or not (they say they don't). But I operate on the internet as if they do anyways, making sure to use HTTPS. And if I REALLY wanted to be sure about it then you can use TOR inside of your VPN connection. With this all your VPN can see is that you are using TOR, nothing else. The only place in the link that might be able to see your traffic (besides the server again) is the exit node. BUT AGAIN, only if you're not using HTTPS. Only way to get back to you in this case is traffic analysis across ALL of the TOR nodes utilized in a connection, but even that doesn't work EXACTLY because the path changes and because most TOR nodes keep absolutely zero information about past connections. And who in the world is really going to go track down every single TOR node, traffic analysis that stuff back to the VPN service, then back to you... at this point maybe take a good hard look at what you're doing on the internet, maybe it's time for some new lifestyle choices.

Now all of that being said theres always ways to leak data whether through things like Javascript, cookies, or even just accidentally leaving Facebook logged in or some other identifying service in which that traffic can be analyzed and paired with the traffic you're trying to keep hidden. So take the necessary steps to make sure all cookies auto destruct, turn off scripting, caching, saving of any kind on your browser and make sure that the browser (or torrent client) is the ONLY application accessing the internet.

The last thing that I want to say is there is this assumption on here that VPN's are gonna turn you over in a heartbeat to agencies. Here is the thing, if they log, probably yes. But think about the real legal reason for VPN's to NOT LOG. If government agencies show up at their door it is by far in the VPN's BEST interest to not have anything to show. They aren't NOT cooperating, they just don't have any data. Nothing the agency can do since it's not illegal. If they have the logs they either A) have to turn them over and risk losing their business since nobody will want to use them again or B) not turn them over and have to deal with the law enforcement.

Sorry, this is the real last thing I want to say. The recommendation ever of using a proxy over a VPN is ridiculous. A VPN is basically a proxy that encrypts the data between you and the proxy. So the idea that a proxy would ever serve some purpose BETTER than a VPN is just not correct.

@KiokiN
KiokiN commented on 17 Oct 2019
Many VPNs have been audited to make sure they aren't tracking user data, and their no log policies have been proven in court, where it would be perjury to not provide them. I find VPNs to be extremely necessary in privacy! First of all, you won't get in legal trouble when pirating content if you are careful. Also script kiddies can't DDOS you or socially engineer a Comcast phone representative to get your private information, or SWAT you if you are a online figure.

@153
153 commented on 23 Oct 2019
Remember to always use Tor before connecting to your VPN.

@bdmorin
bdmorin commented on 23 Oct 2019
The number of ways this post incorrectly uses the term proxy is mind boggling. A VPN doesn't proxy, it moves your point of origin, a proxy makes requests for you.

I don't disagree with the premise, however saying "proxy" is irresponsibily wrong.

@jonpaulh
jonpaulh commented on 23 Oct 2019
What about plausible deniability, with a shared IP?

Everytime you make a request you use the shared IP and a port. For security purposes law enforcement require those providing ip addresses to keep a record of who had them, when it comes to CGNAT providers retain both the IP and the ports used. So when law enforcement comes knocking, they just provide the IP and port and from this the ISP can determine who the user was at the time.
This applies to CGNAT from your ISP. When we talk about using a shared connection ie internet cafe or similar this is an extra layer of anonymity as the ISP is tied to the cafe and in no way yourself. But as the article states fingerprinting devices is much more advanced than just taking the IP used.
Best bet is to dress all in black, hack into an internet cafe wifi and connect from far away (wouldn't want thos cameras seeing you). Use tails OS with VPN and TOR, download that copy of live action Lion King and then high tail it out of there burning both the laptop and clothes and then throw the ashes into the bottom of a lake. Lastly move countries and change identity, free to watch that sweet downloaded illegal pirated movie.

@qmdnls
qmdnls commented on 24 Oct 2019
While I agree with the general sentiment of this post, I do think a bit more nuance couldn't hurt. Most of this depends entirely on your threat model and without first establishing a threat model it's hard to say whether a VPN can be a viable alternative. I completely agree with you that the vast majority of VPN services are snake oil however and should not be trusted though. Thank you for this post.

@irfanbaigse
irfanbaigse commented on 24 Oct 2019
Best choice I can say, If you have some tech knowledge you can go ahead deploy your own vpn and pay only for the server billed monthly
https://github.com/trailofbits/algo
few commands your vpn is online and good to use.
t2.micro instance is a good choice for personal use on AWS.

@slrslr
slrslr commented on 24 Oct 2019
Article can be more helpful if contains link to a wir€guard setup tutorial on various linux distributions. i only know about openvpn setup tutorial, but it has some limitations.

@joepie91
Owner
Author
joepie91 commented on 24 Oct 2019
@bdmorin A VPN, in the setup that VPN providers use, does precisely what a proxy does; it makes requests for you. They're just TCP/UDP packets rather than eg. HTTP connections (which, incidentally, is also true for SOCKS proxies). The usage of term "proxy" here is absolutely correct.

It also doesn't "move the point of origin" any more than an (encrypted) SOCKS proxy does; which is to say, it does do that conceptually, but the traffic still originates from your own system from a technical perspective. "Moving the point of origin" also isn't mutually exclusive with "making requests on your behalf"; both proxies and VPNs (in this setup) do both.

@craftxbox
craftxbox commented on 25 Oct 2019
I have not read through this entire comment section yet, but I did see someone telling people NOT to use tor. Please, do use tor. Using tor for mundane, non-important tasks improves the security of the entire network, as the more people using tor for no reason significantly obfuscates the people who DO have a reason to be using tor.

@thisgood178
thisgood178 commented on 25 Oct 2019
I like it because at sunny side we have it and it blocks EVERY THING AND OT IS SO STUPID and so I learned from this to hate sunny side and to love this

@viraladmin
viraladmin commented on 25 Oct 2019
No matter how many times its stated on this gist it won't make it true - VPN's are NOT like proxies. I don't care if we are talking socks proxies or any other type. Proxies do not encrypt the traffic. Proxies do not run at the OS level. Saying things like "you should be using https" means you are limited in your views of what a VPN actually does and what a proxy actually does.

Sure you should be using https but even if you are, that doesn't prevent your ISP from seeing what you are visiting nor what you are doing, If you think otherwise you need to learn more. If the ISP can't see the site you are visiting, it also can't route whatever the site is sending to your IP. They absolutely can see what you are doing even on https.

Moreover however, not every service online is a webserver and not every service offers a form of encryption. It won't matter how much you plug a proxy into a service client, your ISP can still see it. Take downloading torrents as an example. Your ISP can still see you are downloading torrents even through a proxy. The peers and seeds can't see who your ISP is, but your ISP can see them and what you download if they cared enough to check. Sure you could get a client that supports encrypting - but this is not a default behavior of most torrent clients - and then you have to configure the client to use a proxy. Depending on the service they may not even offer you the ability to enter a proxy in their settings.

A VPN encrypts data sent between you and the VPN, between the VPN and you, between the ISP and you and between the VPN and service it is talking to. This makes it impossible for your ISP to snoop on what you are doing. A VPN runs OS level - meaning every single thing you do over the internet will be routed through the VPN, not a per app setup as is the case with a proxy.

I don't even understand how this is a discussion. However don't take my word for it, test it for yourself. Get yourself a proxy and then open a command prompt. Without downloading any special software issue a 'ping google.com' command. Google can see you pinged them and your ISP can see you pinged them. Run a traceroute/tracert command on google, Every hop can see you and so can your ISP. Sure you could likely find downloadable apps that will allow you to route through a proxy but do you really want to find a special version of every single networking command and every client used to connected to a server just to use an unencrypted proxy?

A VPN provider would automatically route every single one of these commands and services through the VPN and encrypt the data both ways.

Equally anyone saying you don't need (or shouldn't use) a VPN with TOR has no idea what they are talking about. Using netflow and similar types of techniques, users on TOR have been exposed plenty of times. Its many governments top priority to find out who users are across tor and there have been countless exploits performed over the years. (read up on some methods such as https://mice.cs.columbia.edu/getTechreport.php?techreportID=1545&format=pdf&)

Putting a VPN between you and the exit node prevents potential risks.

It seems so many people are confused about what a VPN does verse a proxy. Seriously do your own research - there is a ton of it out there. Don't trust a single source based solely on comments where there is a clear disagreement between comments.

@DockJumper86
DockJumper86 commented on 25 Oct 2019
I mainly agree with what you said except for a couple of small points. Saying you don't "NEED" a VPN with Tor is kinda dependent on what your need is. Tor is really good at what it does but you can always add another layer of abstraction which is what the VPN does. It's a good thing most usually.

However, your assertion that your ISP can see your https traffic is interesting. I'd love to hear more on why you say that. Now obviously they can see where the packet is being routed. But the data inside, to determine anything meaningful, is encrypted. So maybe some clarification on that?

@viraladmin
viraladmin commented on 25 Oct 2019 • 
I am suggesting everyone should in fact use a VPN as an added layer even with tor - check that again :). With all things relating to privacy one should evaluate their own security risk and decide if that practice is important to them.

As for https I will quote https://www.privatetunnel.com/news/how-isps-can-still-track-users-on-https-sites/

"Think of your ISP like your mail carrier. It’s their job to deliver your letters, magazines, and packages. Our website, similarly, is sending you a letter containing this reply, displaying the text and images on the site. You pay the mail carrier for sending and receiving your packages. If you spend a higher amount, you get packages within two days, or overnight. The more you pay, the faster packages move.

HTTPS encrypts the package’s contents. Your carrier can’t see what’s inside the boxes or envelopes. You might compare it to using security envelopes when mailing sensitive information. However, your carrier still needs to know that it’s coming from you and going to the recipient. You can’t encrypt this information, or it will end up in the unknown bin. This means your carrier is able to track who you’re exchanging packages with, whether it’s this blog, Facebook, your bank website, or Netflix."

Whats meaningful is clearly subjective. Do you want your ISP knowing what sites you visit, if you are just viewing or if you are downloading, ect. Its exactly that information that advertisers use to target ads. They don't need to know the detailed information to gather data about you. They can see if you are visiting gay porn, teen porn, rape porn, hacking sites, how to build bombs sites, 3d gun printing websites.... etc. etc. etc. etc.

@Sphinxs
Sphinxs commented on 30 Oct 2019
@iguit0

@marinegundoctor
marinegundoctor commented on 4 Nov 2019
Only one person mentioned the i2p protocol. From what I know of it, it seems more secure than TOR or a VPN.

@BossyBigBoss
BossyBigBoss commented on 7 Nov 2019
I think the take-away here is not not fool yourself into thinking that VPN is some sort of short-cut for Tor. In other words, don't fool yourself into thinking you're anonymous, and for the love of everything good and holy, don't think that your VPN will go to jail for your activities.

However, I use VPN services all the time (for example, https://aeroshield.me). There are times when either:

* I am behind a restrictive firewall, such as at a public library or a church.

* I need to get into an internal network with other clients, such as my browser.
And I don't buy the argument that your IP address is not a valuable asset to trackers and ad companies. Some website owners block Tor, because they cannot get honest GeoIP lookups out of a client when the request comes out af a Tor exit relay. In fact, the whole point of Tor is to obfuscate your source IP address, while remaining encrypted between the Tor client and the relays.

However, as mentioned, don't have any false ideas about your security or anonymity when using VPN services. Understand the tech and your risks using the tech. That applies for anything, not just VPN and Tor.

You have to be very tech savvy to setup your own vpn. And even this doesn't guarantee you anything. Your server can be hacked as many others servers all over the world. For me it's easy to pay for all these things to any trustworthy VPN service and enjoy it without headache.

@kisai
kisai commented on 18 Nov 2019 • 
Article sponsored by the NSA

actually the NSA is very interested in you acquiring VPN services, in particular the ones they finance. starting a VPN is something that is relatively cheap, so any of the Intelligence agencies can easily include it in their own budget. the Chief Data Officer of Telefonica a Spanish telecom giant gave a talk about how they started a VPN just for research and they obviously spied on everyone. So no buddy, a VPN doesn't mean you a thing or that you are protecting yourself from the NSA.

We should stop calling this things VPNs because they are just as the article says glorified proxies, nothing more. A VPN is in fact private is something you host and something you use among private servers only.

@joepie91
Owner
Author
joepie91 commented on 18 Nov 2019
@Kisal: the Chief Data Officer of Telefonica a Spanish telecom giant gave a talk about how they started a VPN just for research and they obviously spied on everyone.

Out of curiosity, do you have a link to that? Would be interesting to learn more about that particular case.

@2635599
2635599 commented on 18 Nov 2019 • 
i see we have a complete crackpot liar that should be banned completely from the internet. vpn's are your friend.

@aedicted
aedicted commented on 23 Nov 2019
@viraladmin

Just a few remarks as some of your statements although regularity used by many aren't universally correct either:

No matter how many times its stated on this gist it won't make it true - VPN's are NOT like proxies.

It depends on the exact definition as purely language based, one could say that a VPN acts as "your proxy" as well in terms of requesting things for you. However, within technical literature I very well agree, the difference is that a VPN provides a tunneled private (not to be confused with encryption or privacy) network while a proxy normally only takes care about single connection requests.

Proxies do not encrypt the traffic.

VPNs don't necessarily either. Nowadays, for sure it is almost always the case, but the definiton of a VPN where "private" originally only refers to have a private network tunneled through another, doesn't require any encryption.

Proxies do not run at the OS level.

I guess that's rather a question of the concrete technical implementation than of any fundamental difference.

Sure you should be using https but even if you are, that doesn't prevent your ISP from seeing what you are visiting nor what you are doing

That statement isn't correct in its generalization. The URL and thus "what one is visiting" will be encrypted.

If the ISP can't see the site you are visiting, it also can't route whatever the site is sending to your IP.

What they will get as correctly assumed being a technical necessity is the corresponding IP address. Due to the lack of the concrete domain name, that may or may not enable them to link it to a specific website. Often enough, many sites share the same IP destination and distinguish the call through the HTTP header only.

They absolutely can see what you are doing even on https.

Taking the topic DNS aside, they can see what destinations one routing-wise calls up for, but so they can when establishing a connection to a VPN endpoint.

A VPN encrypts data sent between you and the VPN, between the VPN and you, between the ISP and you and between the VPN and service it is talking to.

Given strict interpretation of things, your mistake is to throw different "default behaviours in the wild" into one box and then declaring those differences as immanent. While a VPN can be run without encryption, so can the overall connection through a proxy be encrypted.

meaning every single thing you do over the internet will be routed through the VPN, not a per app setup as is the case with a proxy.

That also depends on the concrete routing settings. It is perfectly feasible to route only specific destinations through a VPN (split tunneling).

I don't even understand how this is a discussion.

...

Sure you could likely find downloadable apps that will allow you to route through a proxy but do you really want to find a special version of every single networking command and every client used to connected to a server just to use an unencrypted proxy?

I think what the creator of this thread joepie91 wanted to hint on (being reasonable or not) was that today's marketed VPN products actually sell you a "waste product" as instead of using a VPN's original application which is to provide access to a private network through another, the customer only gets to use the internet access attached to that private network, effectively showing similarities to a more simple proxy connection. Hence he probably was rather concentrating on the "political differences" than on the technical ones.

It seems so many people are confused about what a VPN does verse a proxy.

Apparently, yes.

Seriously do your own research - there is a ton of it out there.

Where can I sign this?

Don't trust a single source based solely on comments where there is a clear disagreement between comments.

"always allow to question yourself" to be added.

@viraladmin
viraladmin commented on 23 Nov 2019
@edicted

I agree with most of what you said except this:

What they will get as correctly assumed being a technical necessity is the corresponding IP address. Due to the lack of the concrete domain name, that may or may not enable them to link it to a specific website. Often enough, many sites share the same IP destination and distinguish the call through the HTTP header only.

A VPN in no way protects your DNS queries. It doesn't matter if 1000 websites are hosted on the same IP address. Your ISP does not need to distinguish from the http header, they need only monitor your DNS queries to see what website you visited.

@aedicted
aedicted commented on 23 Nov 2019
Keep in mind that one doesn't necessarily have to use the DNS server of the ISP in question, nor the one of the VPN provider nor any actually.

In most cases, DNS queries would be routed through the VPN as well by default so your ISP don't get to see them if you use any different provider or setup your own.

Same can be true with SOCKS proxies which support remote dns lookups.

In general, it boils down to whom you grant your trust as at some point, one has to trust the endpoint to forward the data to the intended destination.

@devasia2112
devasia2112 commented on 24 Nov 2019
I'm using dnscrypt-proxy with .ovpn files it seems to work well.
Even if i'm not connected to the vpn, i still protecting my dns queries.. but i have to trust the public dns servers, i'm not running a private one.

@shibme
shibme commented on 25 Nov 2019
Even SSL/TLS aren't technically safe enough considering the CA can issue two different and yet identical certificates.

@viralarchitect
viralarchitect commented on 2 Dec 2019
I don't understand why articles like this one downplay the value of your IP address. The string of numbers themselves don't mean much, but if you pair it with a timestamp, you can get an ISP to trace it directly back to the customer using it at that time. I know there are shady VPN providers out there, but using one adds a layer of obfuscation between your ISP and the destination you connected to.

If you want to be truly un-trackable, you need to begin the entire process before ever buying a computer or phone.

Pay a stranger to walk into the store with cash and buy you a burner phone and laptop.
Only use a LiveCD distribution of Linux with all of the privacy tools including the Tor broswer.
Connect using a VPN that you paid for with bitcoin
Never connect to the internet at home or work, always be on the move going to different locations.
Always change up your browsing habits because even that alone can be used to identify you.
Even if you do all of this, there are still chinks in the armor. If you and the person who bought your computer / phone were ever together in view of a security camera. Even bitcoin isn't completely anonymous and can be used to trace back to you.

The point is that you want to add enough layers of security and obfuscation that the amount of effort required to successfully track you costs more than the person tracking you is willing to pay.

@fr-ez
fr-ez commented on 3 Dec 2019
@kisai: the Chief Data Officer of Telefonica a Spanish telecom giant gave a talk about how they started a VPN just for research and they obviously spied on everyone. So no buddy, a VPN doesn't mean you a thing or that you are protecting yourself from the NSA.

Perhaps are you referring to this video of Chema Alonso? https://www.youtube.com/watch?v=0QT4YJn7oVI

They did it by setting up a proxy and a warning to people that connect to it, not a vpn. Pretty interesting, though.

@sigjosh
sigjosh commented on 5 Dec 2019
I use ExpressVPN. I've used their paid service for almost a decade at this point. I use it for only a couple of very specific purposes, and I've never encountered a problem in that regard. In the case of this service possibly logging user data and lying to customers about it, maybe read this article they published on their site: https://www.expressvpn.com/blog/pwc-audits-expressvpn-servers-to-confirm-essential-privacy-protections/

ExpressVPN doesn't push their advertising in the same way NordVPN does. ExpressVPN is so confident in their user's privacy that they paid for well-known, 3rd-party auditors to come in and inspect their code, their servers, and interview their employees. They even published a PDF copy of the results of that audit, as well as the full audit case. You claim that any VPN service that charges roughly $10/month is most likely logging your data anyway, and that you're at the mercy of these providers, but at least I pay for a service I know I can trust. I trust them because they've proven that I can by subjecting themselves to outside auditors and publishing their findings publicly.

@devasia2112
devasia2112 commented on 6 Dec 2019 • 
@sigjosh seems like you are marketing ExpressVPN. nah!!
Anyone could pay a third part to audit their software, the question is: After the auditors leave the company, are you sure the same audited code will remain in production?
A PDF or whatever document means absolutely nothing in this context. You just want to believe you are safe and I do understand that.
Just saying, companies have copies of their environment each copy for a specific purpose. Go figure.

@thesoothsayer123
thesoothsayer123 commented on 6 Dec 2019
Good thread. Almost 5 years old and still kicking.

I think it's been established in the comments so far that a commercial VPN is neither useless nor infallible when it comes to privacy.

Regarding choices of commercial VPNs, what hasn't been discussed yet is that it's important to consider the country the VPN is based out of, as this country will have specific laws regarding data retention for commercial entities. Laws regarding what they can and cannot retain, how long they can retain it, who and and under what circumstances they can release that data to, etc.

For example the US doesn't currently have any laws requiring mandatory data retention, so if a VPN from there advertises they don't keep logs on users then it MAY be true (going all tinfoil hat over "Five Eyes" doesn't change the reality of encryption). On the other hand if a VPN is based out of a country with a mandatory data retention law and they advertise no logs on users, then I'd obviously be suspicious of this claim.

If you're not concerned that your VPN stores some information about you and are more concerned with how much information they can store and what they are allowed to sell to third parties, then that's something to consider as well.

Using a commercial VPN does require you to place a large amount of trust that they and their service are operating as advertised, no matter what. To that end, there's no substitute for having an understanding of what the benefits and limitations of a VPN are and how these fit into your required privacy needs. Setting up one's own VPS may be unfeasible for most internet users, however I don't think acquiring some base knowledge on how the internet works is beyond the scope of most people.

@Naleksuh
Naleksuh commented on 19 Dec 2019
how much more condescending than every title being "But I ___!"

@isu17
isu17 commented on 20 Dec 2019
What a bunch of opinionated bs. VPN exist for a reason and if you have 2 brain cells left, and you need them and know what they are you can sure make sense of how and why to use them. Sure the $5 from some youtube promo wont be the one you are looking for, and sure there is a market for quick cash from normies that dont know why they are buying it, but coming to github and spilling such low bait bs is just insulting.

@h1z1
h1z1 commented on 24 Dec 2019 • 
So much disinformation holy shit. Not sure how many of you are Russian or Chinese trolls.

Way too many 'points' to destroy but for the record

"VPN is not a Proxy"
.. is arguing symantics. VPN can be used as a Proxy or a Proxy can be used as a VPN. "VPN" doesn't mean any specific kind of technology rather it's a .. Virtual Private Network. SSL VPN's are also a thing (based entirely in your browser). Off the top of my head Citrix and Cisco (non-ipec) are two examples of this.
Conversely, a Proxy is NOT limited to HTTP nor any other protocol. It need not have any security at all, merely acting as gateway connecting two points .. by proxy. They are very common for edge acceleration.

Your Government doesn't need to break encryption so long as standards bodies continue to undermine the Internet for them. Whatever legal ramifications exist between calling something a proxy and vpn has absolutely no bearing on what they are. Encryption is also banned outright in several countries, I'd highly suggest people actually do some research.

Regarding interception itself, as someone who has been saying this for now ^Wtoo long - no shit. SSL and by extension TLS are fucking AWFUL protocols. They were -designed- to allow interception by providers like Cloudflare, Akamai, Cisco, Sandvine, etc. The need the ability to ascertain what certificate to present which lead to bastard abominations like SNI still breaking massive parts of the internet.

Good god why was this linked from Reddit?

@jpeizer
jpeizer commented on 10 Jan 2020
I draw issues from this post. I've read a number of comments and I'm sure it's been mentioned already, but I have a few things to state.

Nothing is 100% If you want to connect to the internet you are going to have to trust somebody. If you use a proxy, you trust the hosting solution, even if it's within your own dwelling, you are trusting your ISP. The internet backbone is made of up multiple companies, and the routes it takes to get to the backbone are even more. Without proper and secure encryption, each hope can be logged, analyzed, and distributed. SSL/TLS will only get you so far. Using a VPN does provide added security beyond what has been mentioned by the OP.

The point of a VPN in addition to what has been mentioned is to simply add another layer of security. Security is not a single vault. You need multiple layers in order to gain security. Even if you use every tool in the world, you will never reach 100%, but again, that's not the point.

The OP's case about a VPN being able to be seen by your VPN provider can be fixed by using two VPN providers. As long as encryption is properly used on both it splits the security and encrypted traffic so no one provider will have full access. Message me if you want more details on this...

As has been stated before, the use of different tools varies based upon your needs. But to spread around that a VPN has no role in this at all is out right false. I use a VPN that I trust more then the networks I connect to and the internet providers I deal with. Using this along with a verity of other tools and techniques has let me get away from a lot of advertisement tracking efforts.

One last thing. I don't suggest to a single person that they host their own proxy or VPN. To do so means you need to have extensive knowledge of networking, system safeguards, and other system setups to ensure the server is resistant to attacks. This is a reason legitimate 3rd party VPN's exists; So you don't have to worry about the environment.

@xNeonHD
xNeonHD commented on 22 Jan 2020
LOL @ all these triggered people in the comments!!

It's been like, what, 5 years? And yet I still see so many butthurt comments 😂😂

Jeeeez you people, can't you see his point? He is being argumentative for a reason here, and it's to emphasize the fact VPNs aren't as safe as most people thought it to be, and by most people I mean the average internet user. He's not trying to downplay the benefits of VPN services, it's a cynical critique on the VPN business as a whole.

I god damn appreciate the way he wrote this. These kinds of "corporations deceiving sheep-minded consumers" scenarios gets me incredibly furious.

@Skeletorwashere
Skeletorwashere commented on 27 Jan 2020
If you are using a VPN, welcome to the club. . . . The “you are now on a list club.” As I still use guardian for overseas travels their are things I simply don’t do on my phone anymore, or on my own ISP or server. A man named Jacob Appelbaum has many things you can learn from about these and other similar tech related issues.

@chrcoluk
chrcoluk commented on 24 Feb 2020 • 
Author I guess isnt in the UK?

Two prime reasons for UK peeps to use a VPN.

1 - Avoid DCMA stuff, as whilst they could with enough effort still track people, they wont bother, they just go for the low hanging fruit.
2 - USA Streaming services, say no more, better netflix library, youtube content etc. in America.

I agree on the logging stuff though, its highly likely that is snake oil. I also agree on the profit levels, VPN's are now averaging £10 month for a one month plan which is ridiculous, to emphasise my point, netflix can spend billions on content, "and" the bandwidth required to serve you that content, and netflix is "cheaper" than your average VPN provider. They charge what they do because they probably have people signing up in their droves to get round geo restrictions. Also the discount for 3 years is stupid high, which probably more reflects the actual cost to provide the service, but they so unconfident that they can keep hold of subscribers (one has to ask why) they are massively overcharging for short term subs.

@dxgldotorg
dxgldotorg commented on 6 Mar 2020 • 
Isn't #1 illegal? You're generally not going to get a DMCA notice sent your way unless you are infringing copyrights, like when uploading while torrenting infringing content.

@AlienProber
AlienProber commented on 6 Mar 2020
Can't speak to other countries but here in the state if you get the channel a show is on you are legally entitled to download or record a copy for your personal use. Xfinity / Comcast has a nasty habit of sending out DMCA notices for shows you get. This happens cause the party making the report didn't bother to do their research and find out from Comcast if you get a channel that carries the show.

@chrcoluk
chrcoluk commented on 15 Mar 2020
#1 is legal if you not distributing, otherwise illegal, I never said was legal I just said it was a reason to use a VPN.

@dxgldotorg
dxgldotorg commented on 15 Mar 2020
@chrcolu

#1 is legal if you not distributing, otherwise illegal, I never said was legal I just said it was a reason to use a VPN.

BitTorrent by design distributes what it downloads. Thus any DMCA you get isn't because you failed to use a VPN service but because you offered content that infringes the complainant's rights.

@chrcoluk
chrcoluk commented on 15 Mar 2020 • 
Correction.
"any DMCA you get isn't because you failed to use a VPN service but because you offered content that infringes the complainant's rights and didnt mask your ip.

For reference torrents can be made to download only, there is workarounds, now I dont use torrents on copyrighted content, my post is based on what others have commented on in public, but this discussion isnt about copyright, and whats legal or illegal, but simply for reasons of using a VPN.

The DMCA notices in the UK are done in a very lazy low cost and possibly even automated manner, they are likely just scanning for consumer uk based ip addresses in swarms, if they find one, automatic notice to isp, who then sends an automatic letter. All this done without even needing the court. So bear in mind, there is also false positives, lack of proof issues, making your comment inaccurate as you assume the notices are 100% proven, you cannot make that assumption.

So again as I said, if you use a VPN, you prevent these automated notices from reaching you.

@dxgldotorg
dxgldotorg commented on 15 Mar 2020
Wouldn't masking your IP make it more illegal as it would be willful infringement?

@chrcoluk
chrcoluk commented on 15 Mar 2020 • 
Dont know, but those handling the notices simply dont care, they just scanning for UK ip's which is why its effective. There isnt anyone manually checking ip's and doing tracking of VPN providers and such.

They not willing to put resources into these notices, they more about scaring people than anything else.

@affiliatepayday
affiliatepayday commented on 15 Mar 2020
dxgldotorg you are kind of funny. Why are you concerned so much about whether something is or isn't legal? I would bet 60% or more of VPN usage is to do illegal things. For example if someone in china routes through a VPN, its generally to evade Chinese bans, which by their laws would be illegal. In some countries they don't view copyright laws the same way US , UK, and EU do and instead they think freedom of information should be available to everyone. To them people evading copyright is just as much acceptable as it is to most Americans for people in china to evade bans. So again why do you care if someone is using VPNs for things deemed illegal by their country.

@h1z1
h1z1 commented on 15 Mar 2020
There isnt anyone manually checking ip's and doing tracking of VPN providers and such.

They are called "security companies". See cloudflare, Google, Microsoft (Azure), etc. They all maintain extensive lists of vpn providers. There are also publicly funded abominations operating under usually educational research grants, which exist for no other reason but outting people. See internet-census.org, shodan, etc. Bastard organizations to say the least.

Then you have active attacks against vpn providers that attempt to get them flagged by bullshit blacklists like Google's capatcha. Once Google thinks you're a problem, they will make your life online a jailed, living hell. There's no way off it either. One of the attacks is impossible for most people to defend against and that is simple backscatter.

@chrcoluk
chrcoluk commented on 15 Mar 2020
Perhaps have I should have been more specific, as I didn't think anyone would misunderstand what I wrote,

I meant no one from the UK consumer isp DCMA team would be manually checking these non UK ip's not no one at all on the internet.

@h1z1
h1z1 commented on 15 Mar 2020
I know what you wrote, the response was specifically about tracking vpn hosts. It is done. As for consumer ISPs, I highly doubt a UK or anywhere else, would honor a takedown request for IPs they do not own. The DMCA is of course American.

@agyild
agyild commented on 26 Mar 2020
Hi, just a quick FYI. I have translated the text into Turkish and made it available here. Cheers.

@joepie91
Owner
Author
joepie91 commented on 26 Mar 2020
@agylid Thanks! I've added it to the list of translations.

@Naleksuh
Naleksuh commented on 27 Mar 2020
Ah so joepie has seen people debunk his conspiracy theories he just ignores like youtube

@joepie91
Owner
Author
joepie91 commented on 27 Mar 2020
@Naleksuh Nope, I'm just not at all interested in rehashing the same discussion over and over again, with people who clearly haven't put in the effort to understand what's already been written.

If you want a response from me, come up with something that hasn't already been addressed before, and present/ask it constructively. Show that you're willing to put in the time and good faith, and so will I. Don't, and then neither will I. It's pretty simple really.

@Naleksuh
Naleksuh commented on 27 Mar 2020
Good faith? Is titling all your sections "But I _____ !" good faith? Seems like you don't have good faith for anyone using a vpn

@joepie91
Owner
Author
joepie91 commented on 27 Mar 2020 • 
See above, not interested in arguing with people with your combative attitude. And that's the last I will say about it, since this is spamming up people's e-mail notifications.

@thisgood178
 thisgood178 commented on 29 Mar 2020
Will you stop texting me this is very anoing JUST STOP PLZZ I DONT KNOW WHAT TO DO
…
@thisgood178
 thisgood178 commented on 29 Mar 2020
________________________________
From: Sven Slootweg <notifications@github.com>
Sent: Friday, March 27, 2020 7:41 PM
To: joepie91 <joepie91@noreply.github.com>
Cc: thisgood178 <BJMARI10@outlook.com>; Comment <comment@noreply.github.com>
Subject: Re: joepie91/vpn.md

@joepie91 commented on this gist.
…
@GildedHonour
GildedHonour commented on 21 Apr 2020 • 
Will you stop texting me this is very anoing JUST STOP PLZZ I DONT KNOW WHAT TO DO

No!!!! Otherwise, who else will have to suffer?
@thisgood178

@joepie91
Owner
Author
joepie91 commented on 28 Apr 2020
Yes, I remove all comments that read like advertising for a provider, including ones phrased as questions. There has been entirely too much provider shilling on this thread over the years.

It doesn't matter how much time has passed, the model of VPN services is inherently flawed and will forever remain that way. Regardless of the provider, and regardless of whether it's been 1 year or 10 years since this post.

Protonmail is absolutely not run by CERN, by the way, it's marketing bullshit. Some of the people involved once worked for CERN or MIT, and they're misusing that to make themselves look more legitimate. It makes no more sense than claiming that HideMyAss is run or endorsed by Walmart because someone is involved who once worked at Walmart stocking shelves.

@GildedHonour
GildedHonour commented on 28 Apr 2020
Protonmail is absolutely not run by CERN, by the way, it's marketing bullshit. Some of the people involved once worked for CERN or MIT, and they're misusing that to make themselves look more legitimate.

Do you have proof?

@GildedHonour
GildedHonour commented on 28 Apr 2020
Also, is there any possible way to prove a claim of any VPN firm that they don't keep logs?

@JimboUS
JimboUS commented on 28 Apr 2020 • 
Yes, I remove all comments that read like advertising for a provider, including ones phrased as questions. There has been entirely too much provider shilling on this thread over the years.

It doesn't matter how much time has passed, the model of VPN services is inherently flawed and will forever remain that way. Regardless of the provider, and regardless of whether it's been 1 year or 10 years since this post.

Protonmail is absolutely not run by CERN, by the way, it's marketing bullshit. Some of the people involved once worked for CERN or MIT, and they're misusing that to make themselves look more legitimate. It makes no more sense than claiming that HideMyAss is run or endorsed by Walmart because someone is involved who once worked at Walmart stocking shelves.

Hi, I totally understand your position but this comment and question was an honest attempt to present the issue to the audience of this thread here for any valuable inputs by the readers here, both positive and negative. That's all!
Perhaps, someone reading this has certain information that Proton VPN is not all it's cracked up to be, etc., and that'll be helpful to all readers.

If you'd be kind enough to reinstate the question/comment it'll be appreciated as it may generate valuable information to everyone's benefit.
If you do not wish to reinstate it, I understand and respect your position.
Thanks in any case!

@GildedHonour
GildedHonour commented on 30 Apr 2020 • 
Also want to note that 90% of people using VPN don't give a rat's ass about privacy or anonymity, like this shit OP wrote blanket generalizing VPN use.

How do you know? How did you measure the 90%?

Most people use VPN to bypass regional restriction and/or throttling so I don't understand this sensationalised crap

How do you know about the "most"?

@JimboUS
JimboUS commented on 1 May 2020
Also want to note that 90% of people using VPN don't give a rat's ass about privacy or anonymity, like this shit OP wrote blanket generalizing VPN use.

How do you know? How did you measure the 90%?

Most people use VPN to bypass regional restriction and/or throttling so I don't understand this sensationalised crap

How do you know about the "most"?

There have been a lot of responses here on the usefulness of VPNs but since the thread owner heavily edits and deletes these posts they do not appear here but they are auto emailed to the posters.

Having said that, one of the usefulness of VPNs will be protecting anonymous speech, like for example posting here anonymously without being traced back to the real IP, or submitting an anonymous editorial/information email to a newspaper/web site, etc., again without being traced back to the real IP.
Going thru one or a few VPN providers, free/paid, and and then thru an anonymous email site like ProtonMail should be a very safe way of ensuring this anonymity with no possible tracing back to the originating IP by anyone or by any agencies.

@JimboUS
JimboUS commented on 1 May 2020
Perhaps, the thread owner will allow constructive comments on the pluses and minuses of ProtonMail and ProtonVPN.
It will benefit all readers here.

@GildedHonour
GildedHonour commented on 1 May 2020
There have been a lot of responses here on the usefulness of VPNs but since the thread owner heavily edits and deletes these posts they do not appear here but they are auto emailed to the posters.

I'm not asking what it seems to you based on the amount of people who made a comment here.

I'm asking "where did you the number 90% and "the most" "?

@JimboUS
JimboUS commented on 1 May 2020 • 
There have been a lot of responses here on the usefulness of VPNs but since the thread owner heavily edits and deletes these posts they do not appear here but they are auto emailed to the posters.

I'm not asking what it seems to you based on the amount of people who made a comment here.

I'm asking "where did you the number 90% and "the most" "?

I'm not the one who posted that.
I just quoted your reply to that person.
That post has been deleted by the thread owner.
That post was emailed to me and is:

@amirasyraf commented on this gist.

Most people use VPN to bypass regional restriction and/or throttling so I don't understand this sensationalised crap

Cause the fuckin morons that would continually lie by claiming all VPN's are bad and worthless will do and say anything to get there way.
Also want to note that 90% of people using VPN doesn't give a rat's ass about privacy or anonymity, like this shit OP wrote blanket generalizing VPN use. They just want to consume their content and download their torrents at non-throttled speed.

Most places also don't have things like Hollywood/MPAA or RIAA or whatever copyright body who would nose around and sue people. Hence, most don't care.

The thread owner will probably also delete this post.
That's what happens when there is a discontinuity of posts since they are deleted.
You may wish to respond by email to that poster above you originally quoted.

@joepie91
Owner
Author
joepie91 commented on 1 May 2020
Perhaps, the thread owner will allow constructive comments on the pluses and minuses of ProtonMail and ProtonVPN.

Constructive discussion is fine. I'm just removing non-constructive comments, and I've actually added a note about that yesterday to the end of the post, since things seem to be getting a bit out of hand here lately. Throwing insults at others, for example, is a one-way trip to the trashbin.

Having said that, one of the usefulness of VPNs will be protecting anonymous speech, like for example posting here anonymously without being traced back to the real IP, or submitting an anonymous editorial/information email to a newspaper/web site, etc., again without being traced back to the real IP.

This is precisely what VPN services (which are not the same thing as "VPNs") are not suitable for, because you cannot know whether the provider is keeping identifiable data.

This is what Tor is for, which is actually designed to ensure this on a technical level, unlike VPN software. But recommending Tor doesn't sell subscriptions.

@shoeper
shoeper commented on 1 May 2020
Fully agree with @joepie91. If you really care about anonymity use Tor and do not use VPN. The latter is like playing russian roulette. Even when using Tor one has to be very careful to stay anonymous.

@AlienProber
AlienProber commented on 1 May 2020
Fully agree with @joepie91. If you really care about anonymity use Tor and do not use VPN. The latter is like playing russian roulette. Even when using Tor one has to be very careful to stay anonymous.

Tes use Tor only and have a BILLION and one things you can't do online. No fuckin thank you.

@JimboUS
JimboUS commented on 1 May 2020
Fully agree with @joepie91. If you really care about anonymity use Tor and do not use VPN. The latter is like playing russian roulette. Even when using Tor one has to be very careful to stay anonymous.

Yes use Tor only and have a BILLION and one things you can't do online. No fuckin thank you.

Of course, if one does not know all there is to know and is not careful with using Tor, anonymity can and will be compromised.
Also, as the poster above stated, using Tor is pretty restrictive with other online activities.

Now, VPN on the other hand is very easy to use but providing anonymity has been seriously challenged.
It has been stated multiple times here and elsewhere that the major, if only, drawback of VPN in providing complete IP anonymity is the level of TRUST one has with the VPN provider.
Does the VPN provider log, does it record, does it track, is it susceptible to secret government warrants to provide all this retained information, are all serious concerns about VPN providers and if one cares about complete anonymity VPN providers are not to be trusted for that, especially those VPN providers located in the five/fourteen eyes countries and/or countries with weak privacy laws.
Moreover, one can be all but certain that certain governmental agencies with unlimited resources have set up and are operating VPN providers around the world that have gained great reputations and reviews over the years and are today considered totally private/secure/trustworthy VPN providers.

But, if a completely anonymous system were to be set up, like that claimed by ProtonMail combined with ProtonVPN, that strongly encrypts but does not log/record/track, and is located in a neutral country with very strong privacy laws like Switzerland, it should be completely anonymous and easy to use. Even if government warrants were issued to provide the server data, there will be nothing there to provide.
Also, using 256 AES and two VPN hops it'll make such VPN totally anonymous and non-penetrable.
Theoretically speaking that's possible, and such VPN/email system will be very easy to use.

Again, the problem arises with the country's governmental/judicial reach with gag warrants/laws, etc.
Warrant canaries can be useful in some countries but are not foolproof.
The Swiss banking system was a secretive system until one day it wasn't, and it resulted in severe consequences for those who trusted the system. Same with Panama where a very well known VPN provider is currently located.
Also, another critical wrench-in-the-gears of a VPN provider are the employees involved and their abilities to somehow record all traffic for certain periods of time, hourly/daily/weekly/monthly/etc. even though the company's servers do not do that.
Employees leaking such supposedly non-recordable VPN data, as it happened in the Switzerland and Panama banking systems leaks will be catastrophic for all involved.

@joepie91
Owner
Author
joepie91 commented on 1 May 2020
But, if a completely anonymous system were to be set up, like that claimed by ProtonMail combined with ProtonVPN, that strongly encrypts but does not log/record/track, and is located in a neutral country with very strong privacy laws like Switzerland, it should be completely anonymous and easy to use.

For the umpteenth time: this is not verifiable, at all. It still requires trust in your VPN provider. This is effectively no different from any other VPN provider, everything else is just window dressing. Your entire narrative is no different from the very misleading claims that this article was written to address. It doesn't add anything new.

So no, there are no systems that are "completely anonymous" but without the constraints of Tor. Tor is the best you're going to get, short of any revolutionary leaps in technology.

@JimboUS
JimboUS commented on 2 May 2020
But, if a completely anonymous system were to be set up, like that claimed by ProtonMail combined with ProtonVPN, that strongly encrypts but does not log/record/track, and is located in a neutral country with very strong privacy laws like Switzerland, it should be completely anonymous and easy to use.

For the umpteenth time: this is not verifiable, at all. It still requires trust in your VPN provider. This is effectively no different from any other VPN provider, everything else is just window dressing. Your entire narrative is no different from the very misleading claims that this article was written to address. It doesn't add anything new.

So no, there are no systems that are "completely anonymous" but without the constraints of Tor. Tor is the best you're going to get, short of any revolutionary leaps in technology.

You're right in today's real VPN provider world NOTHING IS VERIFIABLE, and it is a serious issue of TRUST.
Everyone agrees with that and my entire post raised that point very clearly in several places.
The above quoted paragraph Is a WHAT IF, THEORETICAL statement that "Theoretically speaking that's possible, and such VPN/email system will be very easy to use."

If you operated such a VPN/email system, similar to the one claimed by some VPN providers like the ProtonVPN/email system, and I or anyone else subscribing to it knew you personally and trusted and verified you, that makes it a totally anonymous VPN system since you've already been personally trusted and verified!
I would not be playing Russian roulette as the other poster above noted in using real world VPN providers.

Old Russian proverb used by U.S. President Ronald Reagan during the cold war: "TRUST BUT VERIFY".

@joepie91
Owner
Author
joepie91 commented on 2 May 2020
It isn't possible "theoretically speaking" either. The model used by VPN providers is fundamentally not anonymous. Even if you used a service by someone you know personally, you knowing them personally ties you to the service.

@JimboUS
JimboUS commented on 3 May 2020
It isn't possible "theoretically speaking" either. The model used by VPN providers is fundamentally not anonymous. Even if you used a service by someone you know personally, you knowing them personally ties you to the service.

Not if he has millions of users and he does not know if I'm one of them.
Just like Tor, the more (Tor)/VPN users that utilize the servers, the more hidden the traffic becomes, and perfect anonymity can be achieved.
Especially if I go thru a couple of VPN hops with both being free with no payment service for additional anonymity.
AES 256 can fundamentally be cracked given enough time and resources and so can anonymity thru a VPN like the one in the above example.
Heck, as far as anyone knows AES 256 may already be able to be cracked in a couple of days by a super agency like the NSA/GCHQ/China MSS/etc. and no one will know about it.
The key words here are "time an resources".
Taking dozens of years or a lifetime to crack a person's anonymity makes that person essentially anonymous.
The only instance anyone/any super agency will spend that amount of time and resources will be some existential threat to mankind, but by the time the crack happens it'll probably be too late to stop the threat.

You stated that "The model used by VPN providers is fundamentally not anonymous."
That would be true when that "model" involves payment.
In case of a free VPN service that guarantees no logs/no recordings/no tracking/no storing/no sharing, like ProtonVPN, etc., it seems that true anonymity is possible if that guarantee holds.
And it's far-far easier to use than Tor.

As far as Tor is concerned, privacy and anonymity goes out of the window if and when law enforcement and other governmental agencies, or even private entities, set up their own nodes in the Tor network and track all traffic thru them.
Also, to use Tor safely a user must be a PhD Computer Scientist, or someone like Ed Snowden, it requires quite a bit of work.
Using it without really understanding what you are doing and what may be required at each step can be downright dangerous.
Using PGP when it first came out a few decades ago was also pretty involved and definitely was not for everyone. Things have improved since then and perhaps something far more refined, easy to use, and safe will replace Tor.

So, we end up at the next best thing for the vast majority of online users who desire privacy and reasonable anonymity, the VPN!
Heck, if it's going to take dozens of years, if ever, to crack someone's anonymity thru the FREE ProtonVPN/Email or similar services, it's worth it since no one will devote the time and resources to do that.

@LupusMichaelis
LupusMichaelis commented on 8 May 2020
Translated in French (first draft, i need to read again later, and any French speaking person's welcome to help): https://gist.github.com/LupusMichaelis/9084391b7451c0e35c53c79c5a5e2deb

While looking if any fork were a French translation, I stumbled upon a Korean, a Japanese and a Polish translation.

@atoponce
atoponce commented on 17 May 2020 • 
It isn't possible "theoretically speaking" either. The model used by VPN providers is fundamentally not anonymous. Even if you used a service by someone you know personally, you knowing them personally ties you to the service.

Not if he has millions of users and he does not know if I'm one of them.

Suppose he has 100 million subscribers to his VPN service, you being one of them. Then your anonymity has a security level of approximately log2(100,000,000) ~= 26-bits of security. That's small enough to use network profiling on packets with a laptop and a little bit of time to discover if you are one of his subscribers. If you could raise that security to something north of 100 bits however, requiring 2^100 subscribers on the service, then I would say you have a fair shot at true anonymity, provided you're not careless with your execution.

Unfortunately, there aren't that many people on the planet.

@jbmorris289
jbmorris289 commented on 26 May 2020
Eh. I don't use VPN services also partly because I'd rather not pay monthly/yearly(?) for something I don't use very often and in long terms. That would be kind of weird. I self-host my VPN and use it to keep hackers and sniffers off my traffic on Public WiFi.

@atoponce
atoponce commented on 27 May 2020
New video just released by Kitboga that supports @joepie91's argument, by clearly illustrating why VPN services are lying to you.

https://www.youtube.com/watch?v=CNRdHQJ9AMk

@Naleksuh
Naleksuh commented on 1 Jun 2020
New video just released by Kitboga that supports @joepie91's argument, by clearly illustrating why VPN services are lying to you.

https://www.youtube.com/watch?v=CNRdHQJ9AMk

It supports that VPN companies are making false advertisements, which nobody ever denied. It does not, at any point, say that it is a bad idea to use a VPN nor is such a statement true

@atoponce
atoponce commented on 1 Jun 2020
It does not, at any point, say that it is a bad idea to use a VPN nor is such a statement true

Neither does this Gist. It clearly points out there are times when using a VPN is valuable:

For its intended purpose to access an internal network.
Using it on a known-hostile network.
Circumventing firewall filters.
@AlienProber
AlienProber commented on 1 Jun 2020
It does not, at any point, say that it is a bad idea to use a VPN nor is such a statement true

Neither does this Gist. It clearly points out there are times when using a VPN is valuable:

For its intended purpose to access an internal network.
Using it on a known-hostile network.
Circumventing firewall filters.
The whole video is an attempt to get peeps to give any privacy they have. That is all this thread is about.

@miniyarov
miniyarov commented on 18 Jun 2020
This is very totally legit that public VPN services are complete trash. Online anonymity is very hard. However, you can still create your own VPN server on cloud providers for at least have some privacy while you are on an untrusted network.

Because of this reason, I created zudvpn.com - It is a free and open-source mobile application that's used to deploy private VPN server on major Cloud Providers!

Github repo: https://github.com/zudvpn/ZudVPN

@Kein
Kein commented on 19 Jul 2020
Dont do VPN, use Shadowsocks and V2Ray

@qorg11
qorg11 commented on 19 Jul 2020
Just made a spanish translation of this: https://gist.github.com/qorg11/89b2122180d5df7d180148ecad992a82

@cauerego
cauerego commented on 28 Jul 2020 • 
privacy and anonymity are fundamentally wrong concepts. misleading at best.

but there's no good short explanation of why. as far as i know.

we should focus at transparency in layers, and stop wasting time on anonymity building.

https://cregox.net/privacy

however, if all you care for is spoofing location to watch movies or series on netflix, i rather support digital piracy instead! even while it is more inconvenient, or plain hard to simply "hit play".

@taylorjdawson
taylorjdawson commented on 28 Jul 2020
But, if a completely anonymous system were to be set up, like that claimed by ProtonMail combined with ProtonVPN, that strongly encrypts but does not log/record/track, and is located in a neutral country with very strong privacy laws like Switzerland, it should be completely anonymous and easy to use.

For the umpteenth time: this is not verifiable, at all. It still requires trust in your VPN provider. This is effectively no different from any other VPN provider, everything else is just window dressing. Your entire narrative is no different from the very misleading claims that this article was written to address. It doesn't add anything new.

So no, there are no systems that are "completely anonymous" but without the constraints of Tor. Tor is the best you're going to get, short of any revolutionary leaps in technology.

image

Looks like you can route through Tor with ProtonVPN

@ekardian
ekardian commented on 9 Aug 2020
no privacy, satellite above us, the only privacy we have is our mind - me

@qorg11
qorg11 commented on 9 Aug 2020
ECHELON is always listening ;)

@Halofivebroken
Halofivebroken commented on 28 Aug 2020
I think if you are going to torrent a few times a year or just want to protect yourself from a hostile network a VPN will fill your needs because if shit were to hit the fan the copyright owners are not going to be bothered with the guy that downloaded a few things. They want the anime fan that downloaded terabytes of data. In this case do yourself a favor and spend that $10 a month on Crunchy Roll or Viz Entertainment instead of a VPN. Bottom line it's the internet there is no such thing as 100% privacy yes a VPN will hide you from annoying copyright violation letters but as with any ISP or website your info is tracked and logged basically someone always knows what you are doing and if you want 100% privacy unplug the ethernet cable and shut off the WiFi.

@Halofivebroken
Halofivebroken commented on 1 Sep 2020 • 
@SecretAgentAgentX

"Sorry but spend the money to get a good VPN. Idiots like you should be beat to death with their own computer."

Okay ol wise one enlighten us on what VPN we should get and pay for since you seem to know more than the OP. Quit trying to be shady and respond on the forum. Also I'm not going to reply to your immature insult. Also with Rise UP VPN that is a legit VPN that has been tested by many people why should we pay for something anyone with half a brain and an active internet connection can download for free? Bottom line is Rise Up is free but it is susceptible to the same issues Nord Express VPN or any of the other big names talking up their military level encryption. If someone is so paranoid about their privacy unplug your pc from the wall and power down your cellphone with torrenting and file sharing you are taking a risk at all times why? Because if you are infringing copyrights you are breaking the law bottom line and as the guy said and as the guy said they log to save their own asses from the RIAA etc. Because news flash a federal search warrant can undo any level privacy you can think of because well bro they have all the servers and the code to the encryption. So please tell us who is immune to this we all want to know because I will get that service now.

@Naleksuh
Naleksuh commented on 3 Sep 2020
I notice comments calling out OP on their incompetence are mysteriously being deleted....afraid of a little criticism?

@AlienProber
AlienProber commented on 3 Sep 2020
What do you expect since GOAThub is now owned by Microsour.

@joepie91
Owner
Author
joepie91 commented on 4 Sep 2020
@Naleksuh As explicitly pointed out at the end of the article:

Be aware that any non-constructive comments will be removed. This includes advertising for VPN providers (yes, even when you phrase the marketing claims like a question), trolling, harassment, insults towards other people, claims that have already been addressed in the article, and so on.

@atoponce
atoponce commented on 25 Sep 2020
TechCrunch weighed in, although light on the details and seems to advocate paying for 3rd party VPN over free, which is in direct conflict with this Gist, it at least provided the story behind UFO VPN's "no logging" hypocrisy.

https://techcrunch.com/2020/09/24/free-vpn-bad-for-privacy/

@JimboUS
JimboUS commented on 26 Sep 2020
But, if a completely anonymous system were to be set up, like that claimed by ProtonMail combined with ProtonVPN, that strongly encrypts but does not log/record/track, and is located in a neutral country with very strong privacy laws like Switzerland, it should be completely anonymous and easy to use.

For the umpteenth time: this is not verifiable, at all. It still requires trust in your VPN provider. This is effectively no different from any other VPN provider, everything else is just window dressing. Your entire narrative is no different from the very misleading claims that this article was written to address. It doesn't add anything new.
So no, there are no systems that are "completely anonymous" but without the constraints of Tor. Tor is the best you're going to get, short of any revolutionary leaps in technology.

image

Looks like you can route through Tor with ProtonVPN

Yes, routing through Tor with ProtonVPN is possible but it's only available for the paid version not the free version, and only through certain VPN countries/nodes.
Since you must pay it's not anonymous unless you use Bitcoin or a similar cryptocurrency, and this complicates things.

Also, the TechCrunch article mentioned right above is pretty light and it should not be relied upon as a bible.

The best free anonymous VPN that I've found so far is the one mentioned above but the free version combined with its free email service.
Using it/registering for it from a public WiFi provides additional anonymity as long as that area is not under video surveillance and that excludes all airports/public transit/etc.
Using another free VPN to register for it will provide an extra layer of anonymity as long as you never use that service ever again.

Also, it must be kept in mind that using Tor is not fool proof since no one knows where some of the nodes lead and the owners of those nodes.
Given the extensive resources of the various countries' national security agencies/services, if they think you are a crucial threat they probably have top secret ways of finding you that are not and may never be public knowledge.

Now, if for instance, you want to just send an anonymous letter to a newspaper you'll be truly anonymous since no one will spend the time and resources to ID you as long as your letter does not threaten the end of humanity.

@jasperweiss
jasperweiss commented on 26 Sep 2020
@JimboUS using ProtonVPN's Tor servers has no benefit over the regular ProtonVPN servers and will only degrade your browsing experience due to the added latency and constant captcha's. The reason being that your traffic goes to ProtonVPN's server which then routes it through Tor itself. And thus your traffic is still exposed to the VPN server.

Instead, just use the Tor Browser on your own device.

@JimboUS
JimboUS commented on 30 Sep 2020
@JimboUS using ProtonVPN's Tor servers has no benefit over the regular ProtonVPN servers and will only degrade your browsing experience due to the added latency and constant captcha's. The reason being that your traffic goes to ProtonVPN's server which then routes it through Tor itself. And thus your traffic is still exposed to the VPN server.

Instead, just use the Tor Browser on your own device.

Yes, understood.

But, as I've stated here, one of the weakest links is the capability of the user:

As far as Tor is concerned, privacy and anonymity goes out of the window if and when law enforcement and other governmental agencies, or even private entities, set up their own nodes in the Tor network and track all traffic thru them.
Also, to use Tor safely a user must be a PhD Computer Scientist, or someone like Ed Snowden, it requires quite a bit of work.
Using it without really understanding what you are doing and what may be required at each step can be downright dangerous.
Using PGP when it first came out a few decades ago was also pretty involved and definitely was not for everyone.
Things have improved since then and perhaps something far more refined, easy to use, and safe will replace Tor.

And, "your own device" better be used in a no video surveillance public WiFi and it better be a throw away device that can be safely destroyed and discarded after each use or after a very limited # of uses.

Depending on where you live and what you are doing that requires complete Tor anonymity, using Tor in you own every-day device, in your own home or office, with your own registered ISP, is foolish and unsafe IMHO.

@atoponce
atoponce commented on 1 Oct 2020 • 
As far as Tor is concerned, privacy and anonymity goes out of the window if and when law enforcement and other governmental agencies, or even private entities, set up their own nodes in the Tor network and track all traffic thru them.

The Tor client automatically rotates its path through the Tor network picking three nodes at random every 30 minutes. Even if law enforcement and other governmental agencies or private entities have setup their own nodes in the Tor network, there is no guarantee that your Tor client will use all of them for its circuit, or even some of them for that matter.

A valid threat is if your entry and exit nodes are controlled by the same organization, then some traffic profiling could be done to identify the originator of the requests, but this would only be valid for 30 minutes, before your Tor client negotiates a new circuit through the network.

Also, to use Tor safely a user must be a PhD Computer Scientist, or someone like Ed Snowden, it requires quite a bit of work.

No. To use Tor safely, most people will only need to install the Tor browser, as they'll largely only be using it for web requests.

Using it without really understanding what you are doing and what may be required at each step can be downright dangerous.

What is your threat model and who is your adversary? If you're trying to hide illegal activity, and you're reckless with your Tor behavior, then sure, you could leak your activities to law enforcement, and get arrested. So if your adversary is the law, and your threat model is getting exposed for unethical behavior, then you have a point.

But if you're using it for benign purposes, such as checking your email, or logging into Facebook, then your adversary is the passive eavesdropper and your threat model is perhaps embarrassment. But don't forget that even though you are using Tor, if the underlying protocol is TLS, as is the case with HTTPS, then your adversary still has the same hurdles to overcome with regular encrypted network transit off the Tor network as they do on.

Using PGP when it first came out a few decades ago was also pretty involved and definitely was not for everyone.

It's still not for everyone. Friends don't let friends use PGP.

using Tor in you own every-day device, in your own home or office, with your own registered ISP, is foolish and unsafe IMHO.

I find that opinion naive. I use Tor with the Spotify desktop client and with my Thunderbird email client, because I can. I use Orbot on my phone when on public wifi to browse social media, send chats, surf the web, and send email. Using Tor for completely benign activities should be encouraged, not discouraged. It's completely safe, and to say otherwise implies you know vulnerabilities about Tor than others do, in which case you should file bug reports.

@JimboUS
JimboUS commented on 1 Oct 2020 • 
Thank you for your kind response!

This is a site that checks anonymity:
https://proxy6.net/en/privacy

@jawz101
jawz101 commented on 3 Oct 2020 • 
This VPN provider craze is stupid. "I want to browse my bank site through RDP over Tor on a VPN I trust." Each tiny packet gets that much bigger with encryption overhead and must be encrypted and decrypted for each layer of the process.

And then you waste your time trying to find a VPN Provider in neutral territory and won't tamper with your service. It's an obsession.

When I hear "what is your threat model?" I think someone turned into an advertisement I want to block.

@CrendKing
CrendKing commented on 23 Oct 2020 • 
VPN works the same way as password, as lock on the door. They are deterrence, not a mean to permanently solve the problem. If someone really wants to break in, they will find a way in. The question is if the deterrence would increase the cost of attack enough that it's no longer economic to attack to begin with.

Imagine there are two neighboring houses. One use a crappy lock on the door, and the other doesn't have a lock. They look exactly the same from outside. If you are thief, which one do you break in? Same for VPN, those who use would always pose higher attack cost than those who don't. That inherently make them safer.

Extending from that, VPN with better jurisdiction/reputation/wire protocol etc should make them more deterrent. But it doesn't mean crappy, free VPNs are completely pointless.

@joepie91
Owner
Author
joepie91 commented on 23 Oct 2020
@CrendKing This analogy makes zero sense. Again, using a VPN service just means that you are proxying all your traffic through a third party of dubious trustworthiness - this is an additional risk, unlike with a lock, which does not carry additional security risks.

@CrendKing
CrendKing commented on 23 Oct 2020
Assuming the VPN provider is not actively undermining a targeted user, how is it additional risk? If you are not using VPN, you are an open book. Zero security. Anybody can listen or mitm your traffic if the channel is not secured. Not to mention, most average people already funnel their traffic through their ISP, and ISP can monitor, log or modify the traffic.

The worst case of using a VPN is they don't add any security, essentially replacing ISP. How trustworthy the ISP is comparing to VPN of course varies from person to person.

@joepie91
Owner
Author
joepie91 commented on 23 Oct 2020
Assuming the VPN provider is not actively undermining a targeted user, how is it additional risk?

This assumption is false.

If you are not using VPN, you are an open book. Zero security. Anybody can listen or mitm your traffic if the channel is not secured.

Using a VPN does not change this.

Not to mention, most average people already funnel their traffic through their ISP, and ISP can monitor, log or modify the traffic.

Correct. Using a VPN service is just changing who your ISP is. The difference is that your ISP has a lot to lose (they have physical infrastructure investments, contracts, etc.) whereas a VPN provider can just close up shop, rent a few servers the next day and start up under a new name with zero consequences.

The worst case of using a VPN is they don't add any security, essentially replacing ISP.

No, the worst case - which is going to be the case for almost everyone in practice - is that the VPN service provider is less trustworthy than their ISP.

The criticism here isn't that VPN services are "imperfect". The criticism is that they don't do what they promise at all, and will often actually make things worse in a way that they don't disclose to the user. If VPN services were trustworthy, they wouldn't be throwing false claims of 'more privacy' and 'better security' and 'encryption' at you.

@CrendKing
CrendKing commented on 23 Oct 2020 • 
This assumption is false.

When I say "actively undermine", I mean they proactively sell a specific person that might be celebrity or politician to some hacker group or foreign government for money. For average joe, it's a question how much my usage data on their server is worth, and how much can be extracted by the buyer if sold in bulk. It is basically a economic problem.

Using a VPN does not change this.

You said yourself in the section of "So when should I use a VPN?" that in a well known hostile environment, using VPN can provide minimum obfuscation, if not security. As far as I know, all VPN requires encrypted channel, so at least it protected against eavesdroppers from this part of the network.

The difference is that your ISP has a lot to lose

ISP also has a lot to gain because they have monopoly. VPN can't because there's competition. If my ISP injects ads to my webpage, there is nothing I can do. If my VPN does that, I just switch to another. Or like you said, self host my own.

they wouldn't be throwing false claims of 'more privacy' and 'better security' and 'encryption' at you.

I hate their false advertisement, but they do so because they have competition, while ISP usually does not. Of course this varies from countries and areas. I agree if you live in a place where there are healthy ISP competitions, ISP is more trustworthy than average VPN providers. Unfortunately I don't.

@joepie91
Owner
Author
joepie91 commented on 23 Oct 2020
When I say "actively undermine", I mean they proactively sell a specific person that might be celebrity or politician to some hacker group or foreign government for money. For average joe, it's a question how much my usage data on their server is worth, and how much can be extracted by the buyer if sold in bulk. It is basically a economic problem.

That level of targeting is not necessary for a VPN service provider to be adversarial towards its users; especially considering the extremely low operational and startup costs of a VPN provider, and the low amount of scrutiny they get (both legal and social), it very quickly becomes attractive for such a provider to have a side-hustle regarding their user's data, or at the very least not try too hard to protect them from adversaries.

(As evidenced by nearly every VPN service provider having grossly misconfigured network and client setups. Every time a researcher so much as looks at these things funny, heaps of vulnerabilities and misconfigurations fall out.)

You said yourself in the section of "So when should I use a VPN?" that in a well known hostile environment, using VPN can provide minimum obfuscation, if not security. As far as I know, all VPN requires encrypted channel, so at least it protected against eavesdroppers from this part of the network.

Correct, it encrypts the traffic to the VPN provider. The crucial part is that after the VPN provider, the traffic is still just as plaintext as it ever was. This means that someone can still eavesdrop/MITM traffic, they just need to do so at a different point than before. It has not become any fundamentally harder.

In a known-hostile environment, you are not trying to protect from arbitrary eavesdroppers; you are trying to protect from a specific, explicitly-untrusted party. This is not the situation that the vast majority of VPN users find themselves in.

ISP also has a lot to gain because they have monopoly. VPN can't because there's competition. If my ISP injects ads to my webpage, there is nothing I can do. If my VPN does that, I just switch to another. Or like you said, self host my own.

In many (if not most) countries, ISPs do not have monopolies. Not every country is like the US.

I hate their false advertisement, but they do so because they have competition, while ISP usually does not. Of course this varies from countries and areas. I agree if you live in a place where there are healthy ISP competitions, ISP is more trustworthy than average VPN providers. Unfortunately I don't.

A party which falsely advertises is not trustworthy, regardless of whether they "have competition" or not. If your view is that false advertisement is a logical and unavoidable consequence of competition, then I have to wonder why you believe that "competition" is actually a good thing here at all.

@CrendKing
CrendKing commented on 23 Oct 2020
the extremely low operational and startup costs of a VPN provider

Not every VPN provider falls into this category. It's hard to imagine those highly reputable ones would decide to sell their assets and close shop overnight. I'm not talking about security here. I'm saying the reputation of a brand itself is valuable, and it's usually not profitable to do a one-time deal than milking their users for long time. Thus there is good incentive for users to choose VPN provider just based on the length of operation.

They might have vulnerabilities and misconfigurations, but is it worse than peoples' Windows 7 machine?

Not every country is like the US

US is not much different.

I have to wonder why you believe that "competition" is actually a good thing here at all.

I'm speaking as an technical person. When I use VPN, I know exactly what I'm looking for and why I do it. I don't care about anything in their brochure, and only care about stuff matters to me. However, I'm not most VPN providers target audience. Average joe is their target audience. They need to use those flashy talking point to attract users, even though they are objectively false.

In the end, average people who blindly trusted their advertisement are at lose because they expected too much, and used VPN the wrong way. But my point is, VPN as a tool inherently has their use. Instead of just telling people "VPN is just bad, never use it", we should educate people what it is and how to use it, not as Swiss knife, but as scalpel, unless the technical part is proven to be too much for them to understand, which I'm not very sure.

@ghost
ghost commented on 24 Oct 2020
This is a site that checks anonymity:
https://proxy6.net/en/privacy

This site says I'm using a 'proxy' and that it can 'detect open ports' when I'm just connecting to it over my normal connection. Zuh?

@levi0214
levi0214 commented on 24 Oct 2020
I guess this post is not wrote for Chinese people.
If I don't use VPN I can't even open this page, seriously.
Gist is banned, and many Github projects are banned too.
Can you believe that....

@darvell
darvell commented on 26 Oct 2020
It is a shame I cannot provide proof of what I am about to mention, nor go in to details without having an army of lawyers on me which goes against the rules for commenting but, just something of interest from the 8 years I was in the industry. Always wanted to comment on this with some insights. As this little comment does not refer to any business I personally worked with, I feel it is safe to add it to the discussion as a public comment.

A lot of the off-shore businesses are generally US ran, just with the business entity in a tax haven under the guise of being 'more secure' as a marketing point. A lot of these were fly by night operations which held the same structure, one owner, one sysadmin that worked as 3 -4 'support staff' on top and generally would die within about 6-12 months after mass marketing campaigns. It was common to see about 10+ new ones yearly, I have seen at least >50 companies that were engaged in this until their business idea of 'whmcs + openvpn + cheap vps = $$' turned out to not make sense . Some still exist today, having established false loyalty. This always upset me greatly, privacy is supposed to be for the end user, not the business owner. I think the point I want to make is for those who aren't so technically inclined to roll their own, don't assume seeing a company that resides in a known tax haven means "they can't do anything to us!", it is the worst marketing lie in that industry and disgusting.

This sort of knowledge is easy to work out without even being in the industry, none of that knowledge came from knowing people, just simple research with public information. I have always been surprised that people do not call it out or look in to it.

From experience and without violating anything confidential, i'll note not every big provider is doing something shady and just making money, though, admittedly I am biased after being in one of them so feel free to take that with a grain of salt. There is a big issue of not being able to provide transparency without giving away your secrets, it's a big catch-22. I personally may be able to say that there really is no logging or anything strange happening in a provider but, it's easy to dismiss that claim as no business will open source their everything and show the full stack. Capitalism and paranoia in action, I guess.

You brought up some very interesting points when this was first published, some very important ones that do need real public discussion but it is difficult for a business to engage with as admitting this even exists automatically implies in others mind that it's truthful and defending against any of it is just taken as shilling/marketing. There's also the issue of the business world tends to always want a layer of separation between being 'the company' and the actual people within them who tend to actually be quite passionate about netsec/privacy. This is not always the case as mentioned earlier with some insights on the fly-by-night companies but the fear of being 'too transparent' (which, I still do not understand how that is a bad thing in any way, shape or form but I am not made for the corporate world) makes it difficult to establish real genuine trust between the operators and the users.

@JimboUS
JimboUS commented on 27 Oct 2020
Regarding one's comfort level with using Tor, one must be fully aware of Tor's capabilities and limitations.
Just as an example, these sources do not inspire confidence that depending on one's activities' severity level that person will not be located and ID'd:

https://metrics.torproject.org/

https://medium.com/coinmonks/tor-nodes-explained-580808c29e2d

https://hackertarget.com/tor-exit-node-visualization/

Given the relatively small # of Tor nodes, +/-6,500, and given that various nations' national and international intelligence/security services have almost unlimited resources and top secret tech capabilities that may be unknown today, 5, 9, 14, etc.???, eyes, it would be foolish to rely on Tor, or VPN for that matter, for completely hidden anonymity, again depending on the threat severity of one's actions and the length of time using Tor from a specific device and location.

If one foolishly uses and relies on Tor for anonymity, and is sniffed out to present a high threat level, sooner or later he'll be located and ID'd.
Constantly changing locations, devices, and software can and will provide almost complete anonymity and traceability, but it will be pretty expensive.

Now, if Tor had tens of millions of nodes it would provide a pretty good comfort level.
Heck, 6,500 nodes can exist in a relatively small area in NSA's huge underground facility in Utah!!!
As it has been stated multiple times, the internet network is never anonymous for long, especially when human error and carelessness is factored in!!!

@mrpmohiburrahman
mrpmohiburrahman commented on 30 Oct 2020
Off-topic question:
why using gist? why not publishing the article on websites ?

@joepie91
Owner
Author
joepie91 commented on 30 Oct 2020
@mrpmohiburrahman I've had some issues with my blog setup which I haven't gotten around to fixing yet, so until I fix that, I'm posting various things into a gist instead because it doesn't take a lot of work. This article will probably move to my blog soon though, especially considering how miserably bad Gist's moderation features are.

@uint
uint commented on 1 Nov 2020
I've always found the whole idea of using a "VPN service" kind of sketchy for the exact reasons you mentioned. Thanks for confirming my doubts!

@TRPB
TRPB commented on 3 Nov 2020
If you're in the UK the Food Standards Agency, Gambling Commission and pretty much every government agency can force your ISP to hand over all your internet logs. The ISP also has to keep logs of your data under law.

Whether a VPN is any better has yet to be tested in law, but it at least is an extra hurdle. Your ISP is definitely logging what you do and must give it to the government when asked (even without a warrant) your VPN supposedly is not keeping these logs (which if you look at NordVPN's audits is apparently true) and doesn't (yet) have the same laws governing it.

https://en.wikipedia.org/wiki/Investigatory_Powers_Act_2016

@yell0w4x
yell0w4x commented on 13 Nov 2020 • 
Because it's easy money

Providing quality service in every domain is not that easy as could be in first glance.

The traffic after VPN is of course (by design) is not encrypted, but it's encrypted when leaves your host and pass through the ISP and farther networks until reaches VPN server. It's better than nothing. Also VPN makes applications use different DNS (configured by VPN) in solid way, not the DNS of your ISP that hides the domains you are visiting from ISP (government). So public places Internet access also becomes safer.

Also as VPN is the network. All of your devices connected to same VPN server are reachable for each other regardless of the connection method and Internet providers. You can easily and safely transfer files and documents between them. It's handy to send files between your mobile phone that is on LTE and your home PC e.g. not changing the connection of the devices.

So I would encourage everyone using VPN and If you don't trust VPN providers for some reason setup own VPN server within VPS. Though in this case VPS provider is involved, but they don't concentrate on VPN service and I doubt they spy on VPS traffic by default (as VPN providers may). Also this way could be much cheaper especially in case of a lot of simultaneous connections. For VPS (enough for VPN) the cost may vary in $3.5 - $5 per month.

If you just concern about your legal traffic and the decency of the VPN provider it's better to use own VPS based server.

Some time ago I created a service for friends to easily setup a VPN on Ubuntu powered servers. Recently I decided to publish it. The repo is here https://github.com/vpn41/vpn41 and the website is https://vpn4.one/. I wanted everyone with no special skills and knowledge would be able to setup own VPN server.

@vpnwary
vpnwary commented on 9 Dec 2020
Thanks for the article! Always had some concerns like that and never have come across an article that had the same views! Nice to know there’s people who think in and outside the box! VPNS are great but we are all at someone’s mercy when it comes to the Internet.

@Susanoo1337
Susanoo1337 commented on 28 Dec 2020
I know this is an article from 5 years ago, and most of the points no longer apply anymore since VPN use has shifted over the years, but it's still pretty high up on Googles SEO, so might as well point out that for the sake of region-unlocking Netflix alone, you're better and cheaper served using a VPN.

In countries with armies of over-zealous lawyer firms hunting people who Torrent copyrighted content, you're well off with a few bucks a month for whatever minimal protection you get from a VPN in that regard. For everything else might as well use Tor.

Sure, your average Joe falling for the claims of "military grade encryption" and "absolute privacy" might not know what he's getting into, but they're also not going to read a random article on github. The rest of us should know better.

@joepie91
Owner
Author
joepie91 commented on 28 Dec 2020
I know this is an article from 5 years ago, and most of the points no longer apply anymore

This is false. The points still apply just as much as they did 5 years ago. Nothing has changed.

@hhhgf
 hhhgf commented on 29 Dec 2020
Still facts
…
@ClarkFieseln
ClarkFieseln commented on 6 Jan
wow...I've learnt something important today...something that confirms that my current work is really meaningful, and I believe there are more and more people like you and me on this world every time...and I'm glad about that...because only that way we'll be able to achieve real privacy..which is a "human right"...here one of my contributions:
https://www.codeproject.com/Articles/5161775/Audio-Chat-for-Pretty-Good-Concealing-AC4PGC-Part
Another VERY IMPORTANT contribution follows soon...I'll let you know so you can consider it in future and spread it in a fantastic way...as you can do for sure...thank you!

@CurrentWave
CurrentWave commented on 7 Jan
So well put, this article explained the 'why' and I'm very thankful.

I'd like to read more on this topic of: internet-security what works and what doesn't do what you think it does :D
Any suggestions?

Thank you so much,

@DieseKartoffel
DieseKartoffel commented on 11 Jan • 
Great read, much appreciated. While I think OPs argument is a bit out of line, as laid out by @Rich700000000000 for example, I still think it is a crucial base for a critical discussion. It definitely did not lose its relevance over the years. However, I am worried about an insight I have made in the recent days, while looking for a VPN provider myself. This has not been discussed in this thread which is why I want to throw it in:

While most of the big providers claim that they do not save any logs, they all commonly forbid certain usage behavior in their Terms of Services (I read through the Terms of Service of NordVPN, ExpressVPN, ProtonVPN and Private Internet Access). Each of them stated, with varying wording, something like the following:

"If you don't abide by the following rules, we can permanently ban your account without any notice or comment at any time we wish:

If you use our VPN for Hacking (Port Scanning, sending Phishing Mails, Spam...)
If you use our VPN for anything other than lawful purposes (such as transmit copyrighted data)
If you use our VPN to harass others, promote bigotry or discrimination, or being hateful in general
If you use our VPN for anything that we do not seem appropriate"
After reading a variation of this at pretty much every VPN provider, I was wondering about mainly 2 things:

How and when is a users traffic classified under these points? Who decides that traffic is "insulting" for example? Who decides when a line is crossed when it comes to being hateful?

If the communication is encrypted, how do the services test traffic for certain content and behaviour? How would banning an account for not following these rules be accomplished in practise, without decrypting and scanning the traffic the user sends?

While VPN providers claim not be logging your traffic (in most cases), does this also include they can not read and analyse your traffic and, in addition, save behavior information that are not traffic logs about their users?

EDIT (1 hour later): I went with the naive approach and sent a few of the providers a support ticket with my questions. Just for complete informations sake, I want to publish one of the responses. I cleared the VPN providers name to refrain from promoting in any way:

Hallo ****,
We are contacting you regarding your recent chat with one of our customer success agents.
**** strictly keeps no logs of your activity online. That means we do not track the time or duration of the online session, and neither do we keep logs of IP addresses or servers used, websites visited or files downloaded. In other words, none of your private and secure data is logged and gathered at any time.
Our ToS is based on trust and we trust our users not to indulge in illegal or harmful behavior. There is no way that we could track or decrypt users traffic, so the only way we can ban or suspend the account is when user himself informs us about his violations.

@devasia2112
 devasia2112 commented on 12 Jan
@felix
A VPN encrypt traffic only from your device to the VPN server, from the
VPN server to the website been visited it is not encrypted by the VPN.
Websites may be using TLS but it is another topic...

I had my own VPN service, it was not commercial but it could, but I do
not want to lie to the folks out there. I am able to read every single
word coming from any device, if it is not encrypt end to end, or using
PGP or other means of encryption.

Be aware! nothing is 100% safe as claimed. You are a way better using
Tor without any VPN or just encrypt every single bit of data you wish to
traffic between your network and the other end.

I used to commit the same naive stupid confusion, I once trusted
marketing. ;D
…
@sidneyterminelli
sidneyterminelli commented on 16 Jan • 
I have read almost all of the VPN TOS, even those that boast of having legal offices out of the eyes of the 16. Well, I would never pay even 1 cent/month to have to accept a contract where are such Limitations of liability from the provider of service and indemnification of all the staff (which is not even listed in the contract). They taught me that money is not wasted.

@williamd5
williamd5 commented on 17 Jan • 
This is bullshit. VPN stands for Virtual Private Network and is an indisposable element of many corporations. For instance, working from home will often require you to use a company VPN to utilise some resources.

I understand what you mean; services like {insert name of company here} and whatnot, but that also makes no sense. Yes, commercial providers of VPN services will log your requests 99.99% of the cases, but what's wrong with that? Your ISP logs all of your traffic as well! In case you are a criminal and looking to really hide your steps, maybe the real solution is not to be a criminal.
Based on the points that you make, it seems like you are very technically aware of what exactly VPN is, so I assume this post is for people who are not either. I would only assume that most people who are looking for VPN services actually do it so that they can fool IP-geolocation and bypass simple region restrictions (being a developer myself I can actually say it's super easy to know if someone's IP is legit or if the IP belongs to an ISP that offers hosting services, based on the AS number).
To sum things up

VPN is essential for many people and corporations

And by the way, you can also set up your own VPN connection very very easily on a cheap server. Find a provider that fits your budget (I actually found one for $7/year. OpenVZ servers are just fine for VPN proxies), pick the location from their list that you would like to use, find one of the many tutorials (yes, including videos on youtube) and voila! No programming involved, I promise. You could also get away with just running a simple installation bash script.

@miniyarov
miniyarov commented on 21 Jan
This is very totally legit that public VPN services are complete trash. Online anonymity is very hard. However, you can still create your own VPN server on cloud providers for at least have some privacy while you are on an untrusted network.

Because of this reason, I created zudvpn.com - It is a free and open-source mobile application that's used to deploy private VPN server on major Cloud Providers!

Github repo: https://github.com/zudvpn/ZudVPN

I see that there has been hot debate on public VPN but ZudVPN offers you to deploy your own server on major cloud providers.
It is now on Apple App Store https://apps.apple.com/us/app/zudvpn-personal-vpn-on-cloud/id1517610454

@darvell
darvell commented on 22 Jan
@osousa You're aware your link just goes to yet another VPN affiliate site? That's how they all work.

@joepie91
Owner
Author
joepie91 commented on 22 Jan
As has been very clearly pointed out, repeatedly in the comments, as well as in the post itself, anything that looks like advertising gets deleted.

@nOji
nOji commented on 29 Jan
I got more annoyed as I kept reading this article.

@peterjosvai
peterjosvai commented on 31 Jan
👍
I've just read it... five years after publication... and honestly, this is such a brilliant type of activism... I'm totally mind-blown :)
"enlightening" -- informing people... of how the info-system around them, which they absolutely trust, actually works...
I mean, wow! :)

this is also a very cool writing, I enjoyed every paragraph of it :)

thanks, big time ☆☆☆☆☆

@comment02
comment02 commented on 1 Feb
Hello, I am Kirsty I want to share my testimony with all of you, Dr Obodo gave me the possibility to start my new and happy life with my lover. The commitment and Marriage spells worked beyond my imagination, I am now happily married to my lover. Contact Dr Obodo now on +234 8155425481

@SilverPaladin
SilverPaladin commented on 6 Feb
How does using your own VPS help? It's still easy for someone to trace the IP to your VPS and then to you.

if your goal is to get American netflix, you can use your own VPN to get it, and not be concerned about exposing your whole internet traffic to the vpn provider.

@keydelk
keydelk commented on 15 Feb
I used a VPN when I visited China a few years ago so I would have access to services like Google and Facebook. However, it does significantly slow down the connection speed (especially out of China, where the nearest entry points are out of S. Korea or Vietnam) so I wouldn't use it for everyday web activities. Perhaps if I wanted to watch content that is blocked in my geographic area (which I think is a really stupid idea that should be eliminated), but based on my interests and location, this hasn't been much of an issue.

@jkelly2477
jkelly2477 commented on 16 Feb
This isn't really a comment but a question... Forgive me if i sound like an idiot but im pretty new and rely on myself to learn and teach myself. Any guidance is appreciated. So if i use a VPN+TOR w/DNS/Proxy server???+disable webrtc then take my 'given' IP gather the info on it change my location to those coordinates and change my timezone to match, how safe am i?

@keydelk
keydelk commented on 16 Feb
@jkelly2477 - I'm not a security expert, but I do know people in the industry. Adding multiple layers like a VPN + TOR + Proxy server would definitely make it harder for someone to track your activity. Also, you should use a privacy focused browser, Firefox is pretty good or the TOR Browser - definitely not Chrome as it builds in a lot of tracking.
This would make it hard for most people to track you - but if a nation-state really wanted to find you, they probably could. But in >99% of the cases, they are not that interested in your online activity. Even China doesn't care that much about foreigners using VPNs to get around their "Great Firewall" if you're not causing trouble.

@actuallyasmartname
actuallyasmartname commented on 17 Feb • 
I don't really give a fuck to even use a VPN. I've had my own experiences with malicious VPNs. You never know if your favorite provider is using your IP for their own advantage. I just use https, I'm not risking any of my info to be leaked by a fake VPN that claims to be a real VPN.

@devasia2112
 devasia2112 commented on 20 Feb
I am using WHONIX for now.
…
@mariogarcc
mariogarcc commented on 22 Feb
- Someone: "But gods don't exist!"
- This guy: "🤓🖐 ummm acshually, there is no way for you to verify that. In short, the only safe assumption is that every god exists."

@ClarkFieseln
ClarkFieseln commented 28 days ago • 
As I promised in my last comment here the new article I posted to Code Project (with code!) and the link to the GitHub repository:
https://www.codeproject.com/Articles/5295970/Audio-Chat-for-Quite-Good-Privacy-AC4QGP
https://github.com/ClarkFieseln/AC4QGP
"Chat using "enhanced" end-to-end-encryption and modulation of audio signal in isolated device, ensuring privacy, anonymity and cybersecurity."
There you may find an example on how to protect your data and your identity "without" need of a VPN.
The uses-cases covered there are not exactly the same, and the tool is not yet wide spread. But this shows that there are actually many possibilities to improve our online privacy.
By the way, here again a link to another tool which may help you visualize network traffic in real-time and get rid of suspicious/malicious activities:
https://www.codeproject.com/Articles/5269206/IP-Radar-2

@markus-zhang
markus-zhang commented 17 days ago
Heres how I see it. VPN provider services are safe for small time crooks. VPN services, Tor and all other encryption technologies that have humans involved are all just toys providing a false sense of security. If they want to catch you, they will catch you irregardless. The three letter agencies are increasingly everywhere. From processor manufacturers; Intel to CA Authorities; Verisign.

But catching you means investing in a good and talented forensic and legal team. Resources are scarce. They have to make choices. So if the cost of catching you is greater than the damage you make, you are left alone. You are sent annoying letters. A random opportunist who wants to exploit the law and rip you off might take the golden opportunity. But if the damage you make the industry in the long run is greater than the cost of catching you, you'll get got in a few months. The internet is a large place and you probably fucked up years or a decade ago leaving pieces of yourself in your uniquely fingerprintable machines. I'm sure there is some incriminating information about you lying around somewhere. In the event of an indictment, a VPN service provider might consult with lawyers and weigh the risk of taking on your case.

They might want the publicity. Any publicity is good publicity they say. Sometimes the lawyers will tell the board, "we can't win the case." And nobody really wants to go to jail or lose their cash cow for you and your 100 € p.a subscription.

How do you get real secure connections then? Maybe it's impossible?

@devasia2112
 devasia2112 commented 17 days ago
from utopia website


      Why Utopia is not open source?

We may disclose certain parts of code, specifically related to
communication and encryption. However, the decentralized protocol will
not be released. Utopia is very knowledge-intensive software. A lot of
time, effort and resources went into this product, and we do not want to
share all of our know-how as it will result in forks which in turn may
result in instability of our main network. Fork will lead to the
division of the community, while our intention is the unification of the
community of like-minded individuals. The bottom line here is that a lot
of software is closed source, and this does not hurt them a bit. In
addition, we will audit our code.


No thanks, closed source.
…
@thewhiterabbit88
thewhiterabbit88 commented 14 days ago
Whats a good resource for a do it yourself vpn no paid 3rd party service at all.

@atoponce
atoponce commented 14 days ago
Whats a good resource for a do it yourself vpn no paid 3rd party service at all.

Wireguard

@hackers-terabit
hackers-terabit commented 14 days ago
My opinion:

Always use a VPN to access Internet destinations unless you have a specific and good reason not to
Mind you I did not say a VPN service, but a VPN tunnel, although it is advantageous for certain users to use VPN service providers instead of hosting their own server.

Why should you use a VPN?
Before we talk about that let me correct one assertion that a VPN is a "glorified proxy". It is not! A proxy accepts connections on behalf of clients then it creates connections to the ultimate destination, relaying the traffic as a middleman. A VPN on the other hand tunnels the traffic.
The distinction is important because where a connection your client is initiating terminates is very important because your session security protocols such as TLS establish trust between a client and the termination server of a client-server connection. So for example, if you trust your local country's certificate authority or your corporate network's PKI , assuming a proxy is configured in the middle will show the connection is secure (although HTTP(S) proxies generally speaking require explicit configuration, but transparent proxies exist).

A VPN is not a glorified proxy because when you assess the risk of using proxy compared to a VPN tunnel, with a VPN you can compensate for the risk introduced by the middle-box (VPN tunnel termination or proxy server) server by using the aforementioned connection security protocols such as TLS.

If we agree that VPN is not just a glorified proxy, then let's talk about why you should Always use a VPN tunnel.

When discussing a security solution one should always consider what information they are securing (data) against being compromised using what means (vulnerability) and from whom (threat). So how can I say one should Always use a VPN tunnel when I don't know any of these answers at any level of specificity for all users?

Data
While I can only assume we all agree that confidential data should remain confidential from disclosure to uninteneded parties, even non-confidential data is useful to threat actors. Yes, metadata correlation (what seemingly useless information combined with timing and other details to tell a story about your activity) is a threat to privacy but more than that , insecure protocols are still widely used (such as TCP and SMTP as an example),even if you almost never use them, the one time you use them is all attackers need, not always to compromise the confidentiality of the information but also to tamper with its integrity and inject content that can be used to compromise arbitrary hosts.

For example, attackers can redirect HTTP traffic to download malware or to inject authentication forms (phishing). SMTP traffic can be abused to tamper with attachments and links inside the email to achieve a similar end. Bottom-line: Even if the data is not valuable to you in terms of confidentiality, attackers only need one instance of you trusting seemingly benign data to achieve a harmful end; By default data should be shared and trusted explicitly not implicitly.

Threat
Most (tech-savvy) people assume MITM attacks are too difficult to carry out against them by any adversary that would target them. At a large scale a good example of this that I can give you is the VPNFilter attack that affected over half a million devices, most of these users will never know they were affected by this threat.

Historically there have been several LAN-based attacks as well such as DHCP spoofing,ARP spoofing and DNS poisoning which I will not describe in any detail here. At a much larger context, entire countries have intentionally hijacked and manipulated content both for their own citizens and against network traffic of adversary nations' users (BGP hijacking and DPI capable nation-scale IDS such as the GFW as an example).

MITM threats are plenty, both targeted attacks and dragnet collection by sophisticated nation states,unknown criminal actors and even small time criminals taking advantage of open-wifi.

Vulnerability
I suppose in this case there isn't much to explain about how insecure protocols compromise data confidentiality and integrity. But I will say this, much trust is placed on protocols such as WPA2,WPA3 and TLS. How vulnerable your network connection is depends on a lot of things, for example WPA2 and 3 have documented weakness that require varying degree of conditions and difficulty to exploit, but the more concerning part is how access point firmware is patched about as frequently as poorly maintained IoT devices. If that is not a concern, TLS leaks by default the server name (usually domain name) you are connecting to which could be considered as metadata collection from a data privacy perspective. I state these to highlight that even more popular and trusted protocols (by most people at least) are as good as how they are implemented in real life.

So back to the topic: A properly configured VPN tunnel adds a security control against would be threats that would exploit vulnerabilities to compromise or weaponize data.

But why should I trust VPN providers over hostile middle-boxes?
I believe this is the goal of the original post. You shouldn't,not blindly at least.

Using a VPN tunnel for security means using it to "hedge" risk not to eliminate it. Trust in this context is not a zero-sum game. You don't need to trust a VPN provider just as you don't need to trust your local ISP,government ,inaccessible router or criminals in general.

If your data leaves the properly secured and maintained devices in network, it is no longer under your control. Using a VPN provider to access the internet is a way to make a calculated transfer of risk as it relates to this loss of control. You transfer the loss of control over your data from your local ISP (and ISP provided gear) to a 3rd party. If you are confident that your local ISP (or coffeeshop,campus wifi,corporate wifi,etc...) is more trust worthy than absolutely any VPN provider then consider that these organizations you trust may not have a choice in their hostility against you. If they are not obligated by law or ill-intending then they will be abused by hostile actors (as in the case of VPNFilter).

My argument for VPN providers is this: A good VPN service provider has a clear and provable incentive and investment in their reputation. Some VPN providers stand to lose multi-millions and possibly their whole business if it ever becomes public that they acted in hostility against their users. You are specifically paying for this protection! Of course if you select a VPN provider without researching their business including who owns it,what jurisdiction do they operate in and what else will their business lose if their VPN service suffers reputational harm then you're making a big mistake. like any business that operates on selling trust, there are and will always be ill-intended VPN service providers.

VPN service vs self-hosted VPN
Ok, maybe you still distrust all VPN providers. Just setup your own VPN, there are excellent services to assist you with this such as tailscale or cloudflare's 1.1.1.1 VPN.
If you are tech-savvy you can probably setup your own OpenVPN or Wireguard server on a rented VPS. I have no problem with that but there are tradeoffs to consider.

For one, unlike a VPS provider a VPN service provider specifically stakes their reputation on not being hostile to the security of your network traffic but even if that was not an issue, why would a shady VPS provider be any more secure than an equally shady VPN service provider?

Lastly, if being tracked between services you access over the internet is a concern for you then using a static IP address is undesirable. Even if you change IP addresses frequently , you would still be the only person using those IPs at any given moment. VPN service providers allow you to share a public IP with the rest of their customers which results in reduction of your uniquely identifiable fingerprint.

LAN security
As mentioned before, a VPN, even if it terminates at your LAN Firewall secures your data from otherwise hostile devices in your network or in an untrusted network. Trust shouldn't be assumed, security should be proactive not reactive.

Last words
With the throughput of modern processors and networks, configuring a VPN by default eliminates an entire class of security vulnerabilities. Whether you terminate your VPN at your firewall, a VPS provider or hedge risk by making a well researched decision to transfer your data trust boundary to a third party, VPN tunnels are a good best practice. Of course, there can arise specific reasons where your data would be better secured or you might obtain better performance (where the tradeoff is appropriate) by avoiding a VPN tunnel and I don't think that is an issue in itself. But by default, making an educated decision on where your data-trust boundary ends will improve and not harm your connection security.

@joepie91 Thanks for starting this discussion, let me know your thoughts if you ever have time.

@enterpixel
enterpixel commented 13 days ago • 
I highly disagree with your opinion on most parts of your argumentation.
I use a VPN Service which sits in panama, and they have a giant reputation in the "dark" scene, and trust.
The only attack which somebody "can" do is a Man-In-The-Middle-Attack for AES decryptions, but that is the worst case, and your data will not be AVAILABLE ENCRYTED for the attacker: They can see your internet traffic, "BUT" not define you as the user.

My next point is your IP is hidden and nobody can see (when using obfuscated vpn) that you are using a VPN service. They can only do that by manually analyzing the data packages you send and receive.

@JimboUS
JimboUS commented 7 days ago • 
Here is some very good info on Privacy, VPNs, and alternatives:

https://www.nytimes.com/guides/privacy-project/how-to-protect-your-digital-privacy?action=click&pgtype=Article&state=default&module=styln-digital-privacy&region=BELOW_MAIN_CONTENT&context=storylines-guide

https://www.nytimes.com/wirecutter/guides/what-is-a-vpn/

https://www.nytimes.com/wirecutter/reviews/best-vpn-service/#the-competition

https://www.accessnow.org/help/

And remember: Tor is pretty good as long as you're not a government agency target.
A super government agency like the NSA/GCHQ/China MSS/etc., will find you in good time and no one will know about it.

And beyond VPN:

https://www.nytimes.com/interactive/2021/03/18/magazine/facial-recognition-clearview-ai.html?utm_source=pocket-newtab

(May wish to check some of my posts and other responses to them beginning in March/April 2020)

@atoponce
atoponce commented 19 hours ago
Whats a good resource for a do it yourself vpn no paid 3rd party service at all.

https://wireguard.com/quickstart