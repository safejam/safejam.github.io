---
layout: post
title:  "Introduction to VPNs"
date:   2021-04-20 19:47:17 +0100
# tags: VPNs
categories: intro-level vpn
excerpt_separator: <!--more-->
---
#### **What is a Virtual Private Network (VPN)?**

Think of it as a tunnel. It has a start point (usually your own computer) and an end point (usually a server). 

<!--more-->

![VPN introduction](/assets/vpn-introduction.jpg)

## What does a VPN do?

When using a VPN you are tunnelling your data between your VPN client (installed on your computer) and the VPN Server (installed somewhere else).

Your data within the tunnel is secured from everyone else because it is encrypted.

When you browse the internet via a VPN, web sites detect that your connection is from the VPN server, not your computer.

## What doesn't a VPN do?

1. Prevent cookies (that you may need to provide consent for) storing personal data on your computer for use by other web sites

2. Encrypt your data 100% of the time. If you visit a web site with plain old HTTP, then that connection is NOT encrypted from the VPN Server to the web site.

3. Stopping web site data from being stored on your computer, making it, and you, susceptible to inbound threats such as malware and ransomware.

4. Provide anonymity. You may prevent home network users and your Internet Service Provider (ISP) from seeing your data, but someone will, because the tunnel terminates at the VPN server before any onward connections.