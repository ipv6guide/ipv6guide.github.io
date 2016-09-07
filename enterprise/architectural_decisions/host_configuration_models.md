---
title: Host Configuration Models
---

Introduction
============
Remember when IPv6 was invented, DHCP (v4) didn't exist. They included in the IPv6, a mechanism we call SLAAC. The idea was that MAC address would used as interface identifier, but MAC address is only 48 bits. Needed to pad out to 64-bits, so added fffe.
 
Make the point that the interface identifier is 64 bits. Add link to 'What was the reason for 64 bits as interface identifier in the first place' [link to addressing bit]

Briefly mention has IPv6 has Router Advertisement functionality [Explain Neighbour Discovery somewhere]

Benefits of Static - Useful for infrastructure, but not where you have to manage users.

Benefits of SLAAC - simplest system for networks where you don't have to manage users (guest networks). Provides host address, default router and recursive DNS. All operating systems support this, and 'out-of-the-box' option. Minimal maintenance, provides privacy and can't track users, but that's also a disadvantage in some scenarios.

Benefits of DHCPv6 - more complex in setting-up, but provides more predictability in addressing and logging, where users need to be managed. More options can be provided to be hosts, but doesn't give default route.

Make the point Networks may have to combine different autoconfiguration models, or even use a variety of models on the same network.

Decision Processes
==================
Don't follow IPv4 practices blindly, as there are IPv6 options that may simplify things. However, there are IPv6 models that can be used with existing systems, but you may miss out on some of the major advantages of IPv6.

What style of managed network? Start with most simple option - SLAAC, but if you need address stability and predicability for forensics, stable DNS, access control then think about DHCPv6. The other reason is that you have a managed IPv4 network and don't want to change all your tools.

Approaches
==========
Static - this is not an autoconfiguration mechanism. Used for infrastructure - servers, routers, switches, management ports, dumb non-mobile devices. Manually configure IP address, default route and optionally DNS server, the same as IPv4.

Managed - enable RAs on router, ensure autonomous flag is off (0), and other flags to on (1). Don't try to get DHCPv6 to set default route, because there's no option. Install DHCPv6 server, configure it, observe log file for new leases to fix stable addresses (DHCPv6 is not a unique identifier of machine, DUID is used). End devices that don't support DHCPv6 won't get address.

Unmanaged - all IPv6 capable devices default to SLAAC. Enable RAs on router, ensure autonomous flag is on (1), other configuration is on (1). If router supports rDNS information in RA packets, configure that and client will receive IPv6 DNS if client understands that (Windows doesn't). Otherwise client will rely on IPv4 DNS server if that's available. If client doesn't support rDNS and you want it to use IPv6 DNS, then install DHCPv6 without address leases - set 'other' bit in RA packet to On (1), then client get DNS information from DHCPv6.

How does the end host select the IPv6 address in an unmanaged scenario?

The SLAAC mechanism uses the prefix information from the RA packet, sends the default route back to the source. There are multiple ways how to use this prefix information from the host - EUI64 (extended MAC, extra bits are FFFE, flip 7th bit), privacy addresses (RFC 4941, random identifiers - Windows) - MD5 hash over last 64 bits, address duplication detection, interface has totally unique addresses, one with status autoconf, the other status temporary that changes over time. 

Privacy mechanisms are generating temporary addresses that are used for outgoing connections and no services are listening. So these change and can't easily be logged or traced. Accessible services use the permanent addresses, but not exposed to the outside world.

Use Cases
=========



FAQ
===
What happens if you do something different to /64 for the interface identifier.
What happens if you turn off router advertisements
Where do I put the default gateway in DHCPv6
