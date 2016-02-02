---
title: Routability
---

To use your IPv6 addresses on the internet they need to be routed. How this
is done depends on the type of addresses you have chosen.

IPv6 address from your ISP
==========================

When you use [IPv6 address from your ISP](../use_PA) you don't need to concern
yourself with routing those addresses on the internet. The addresses are part
of the larger block of your ISP and they will take care of the routing. This
is by far the easiest way to connect to the internet, but it is also the least
flexible. You are dependent on your ISP to provide good connectivity, so
choose a reliable one.

Provider independent addresses
==============================

When you have your own [provider independent addresses](../use_PI) you have
much more control. ISPs can take care of the routing for you and save you a
lot of work and responsibility. But the addresses are under your control and
when you want you can take your addresses to another ISPs and let them route
them.

You also have the choice to do the routing yourself and connect to multiple
ISPs at the same time. This provides redundancy and flexibility. If one ISP
has an outage you will still be reachable through the other ones. You also
have the option to connect directly to internet exchange points. You have
the flexibility to set up the routing for your organisation the way you want
it, but this also brings the responsibility of maintaining that routing. This
requires work and knowledge about protocols like BGP.

Your own provider addresses
===========================

If you have chosen to [become an LIR](../become_LIR) you get your own huge
block of addresses. The way you route these on the internet is the same as
with provider independent addresses. Both are addresses you have control
over, and technically there is no difference in how you route them.

The big difference between these addresses and provider independent addresses
is that you use them to provide connectivity to others. This can be to third
parties, in which case you operate as an ISP, but you can also provide
connectivity to business units, departments or other sites within your own
organisation. You have full freedom in choosing which routing technologies
you use (static routing, BGP, DHCPv6 Prefix Delegation etc) to provide this
connectivity. This does require better knowledge of routing technology.
