---
title: Gaining Operational Experience with IPv6
---
When you start thinking about IPv6 deployment in your network, build isolated environment to get acquainted with configuring and using IPv6 protocol, and understanding IPv6 concepts. After you get operational experience, start thinking about lab environment to test devices, applications and features needed for production environment. Testing has been done by other people though, and you can rely on some of this and only test for your specific scenarios. 

Building a test environment
===
Obtain IPv6 router and switch (see other document), get an IPv6 compliant host, look for an IPv6 tunnel (need path to outside world)/upstream provider, get HE certification
Aim is to get comfortable enough with system - give border router with IPv6 enabled to ISP that supports IPv6. 

What to ask from your service provider about IPv6 - reference

Build recursive DNS server 
Build web server
Build another router and enable an IGP - start segmenting prefix delegation, get acquainted with basic networking concepts, functions and services.
Try out network sniffers - tcpdump, wireshark
Once basic scenarios are tested, starting rolling out in production environment.
Think about security policy first and foremost. Start from upstream, build a firewall (or see if existing can be used), start enabling IPv6 on core network, then configure OSPF/IS-IS. Think about enabling IPv6 in network segment that system and/or network administrators are using and can gain experience.
Roll-out to rest of network. Ensure helpdesk is familar with Ripe-631.
Enable IPv6 on public facing services - DNS, web server. Until you add AAAA record, users will not use IPv6 to access your services.
If you want to test your services, create virtual host, use different IP address and add AAAA record for a particular URL. See if everything works. You'll see problems such as hardcoded IPv4 addresses, images served from IPv4-only URLs. 
Once services have been test, then add AAAA to enable production services.

What are the recommendations for getting training?
    Consider getting a reputable consultant
    Send out network engineers for training, get those engineers to train IT department, helpdesk (ripe-631) and software engineers
    How current is the training material?
    Local IPv6 Task Force / Summits
    
Requirements for upstream provider
    
    
    
    


