---
title: Provider Independent Addresses
---

There are many enterprises that only have one or a few locations and a small
network. Also, you might not have a network specialist that is familiar
with requesting and administrating IP addresses from a Regional Internet
Registry, like [RIPE NCC](https://www.ripe.net/) or
[ARIN](https://www.arin.net/). In that case, you can consider to request
Provider Independent IPv6 addresses. The minimum size of a PI block is a
/48 and more can be requested, but then you have to justify why you would
need more than a /48.

If you are located in the RIPE service region (Europe, Middle East and parts
of Central Asia), you have to find a
[member](https://www.ripe.net/participate/member-support/info/list-of-members)
of RIPE NCC that is willing to request the IPv6 addresses on your behalf. 
This is called a "[Sponsoring
LIR](https://www.ripe.net/manage-ips-and-asns/resource-management/faq/independent-resources/phase-three/what-is-a-sponsoring-lir)"
and they take care of the request and often the RIPE Database.

Your Provider Independent address block will be assigned to your enterprise,
so in the end you are responsible for your IPv6 addresses. The good news is
that you would never have to renumber your network, because you don't have
to return the addresses to your provider in case you are changing a
contract. Your sponsoring LIR probably will charge you with an
administrative of maintenance fee for your addresses. This is not unusual.

With Provider Independent addresses it is also possible that you announce
your block to multiple providers. This is called multihoming.

One thing is important to keep in mind: In the RIPE region, you can only get
PI IPv6 addresses if you only use them for your own infrastructure. 
Connecting customers with PI is not allowed. In that case, you will have to
[become a member](../become_LIR) of RIPE NCC or other RIR and get an IPv6
allocation.

Summary
-------

- Using your own PI addresses is a good idea when:
  - You want to connect to multiple ISPs
  - You want to be able to change ISPs
  - You don't want to renumber your network
- Using your own PI addresses might not be a good idea when:
  - You want to connect customers
