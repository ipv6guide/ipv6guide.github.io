===
title: Host Configuration Models
===
Remember when IPv6 was invented, DHCP (v4) didn't exist. They included in the IPv6, a mechanism we call SLAAC. The idea was that MAC address would used as interface identifier, but MAC address is only 48 bits. Needed to pad out to 64-bits, so added fffe. 
Make the point that the interface identifier is 64 bits. Add link to 'What was the reason for 64 bits as interface identifier in the first place' [link to addressing bit]

Briefly mention has IPv6 has Router Advertisement functionality [Explain Neighbour Discovery somewhere]

Benefits of Static - Useful for infrastructure, but not where you have to manage users.

Benefits of SLAAC - simplest system for networks where you don't have to manage users (guest networks). Provides host address, default router and recursive DNS. All operating systems support this, and 'out-of-the-box' option. Minimal maintenance, provides privacy and can't track users, but that's also a disadvantage in some scenarios.

Benefits of DHCPv6 - more complex in setting-up, but provides more predictability in addressing and logging, where users need to be managed. More options can be provided to be hosts, but doesn't give default route.

Make the point Networks may have to combine different autoconfiguration models, or even use a variety of models on the same network.

Decision Processes
Don't follow IPv4 practices blindly, as there are IPv6 options that may simplify things. However, there are IPv6 models that can be used with existing systems, but you may miss out on some of the major advantages of IPv6.

What style of managed network? Start with most simple option - SLAAC, but if you need address stability and predicability for forensics, stable DNS, access control then think about DHCPv6. The other reason is that you have a managed IPv4 network and don't want to change all your tools.

Approaches

Static - this is not an autoconfiguration mechanism. Used for infrastructure - servers, routers, switches, management ports, dumb non-mobile devices. Manually configure IP address, default route and optionally DNS server, the same as IPv4.

Managed - 

Unmanaged - 

Manage






Use Cases


---
FAQ
---
What happens if you do something different to /64
What happens if you turn off router advertisements
