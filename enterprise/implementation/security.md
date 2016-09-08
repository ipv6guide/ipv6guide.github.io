---
title: Security
---

Look at IPv6 myths on Deploy360 blog
Reference them

Compare v4 to equivalent in v6
Tony Hain - briefings

IPv6 makes some things better, other things worse and most things are just different, but no more or less secure
Better
  Automated scanning and worm propagation is harder due to huge subnets
  Link-local addresing can limit infrastructure attacks
  IPsec will be routinely available for use where keys exist
Worse
  Lack of familiarity with IPv6 among operators.
  Multiple addresses per interface is a different concpt
  Immaturity of software in the next few years
  Improperly deployed transition techniques

ICMPv6 is a crucial component of an IPv6 network and basic functions of IPv6 rely on it. See RFC 4890 for more information.

Look at what you're doing with IPv4 - make sure tools are able log and interpret IPv6 correctly. Firewalls, intrusion detection systems, intrusion prevention systems, logging. Do you scan for both IPv4 and IPv6? Scraping tool.

Security managers that think you have to enumerate all hosts on a subnet - point to authoritative document

Using link-local for infrastructure is defined in RFC 7404 - easy to deploy in beginning, but harder to troubleshoot later. Don't see which interface you're talking to, keep things familiar with IPv4. 

IPv6 has been deployed in the largest networks, content providers, cloud providers for many years - the most severe bugs have probably been found, but most IPv6 code is less mature than their IPv4 equivalents and some bugs may still appear, although diminishing problem. 

Don't disable IPv6 in Windows - it's an unsupported configuration and required for certain services.

Use switches that support RA guard mechanism (ripe-554), DHCPv6 guard, and all other mechanism described in first hop security (Cisco White Paper, IPv6 snooping policy) or ask vendor to implement it. 

Write a document - ISPs and small business networks, recommendations on prefix delegation size and stability.




