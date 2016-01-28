---
title: Using IPv6 address from your ISP
---
When you get IPv6 connectivity from your ISP you should get a /48 prefix of IPv6
addresses per site by default. When you have multiple sites you should get a
/48 for each. For many organisations this is enough: it provides you with
65,536 subnets per site. You are probably not going to use all of them, but
having such a large block allows you to make a good
[addressing plans](addressing_plan) where you can group addresses in a logical
and useful way, not limited by scarcity.

Getting a block of IPv6 addresses from your ISP is easy. ISPs get a Provider
Aggregatable (PA) block from their Regional Internet Registry, and this block
provides plenty addresses to give each customer a /48. They usually provide
that /48 as part of the standard service. The downside of using your ISP's PA
addresses is that you use *their* addresses. When you want to connect to
multiple ISPs for redundancy you can't really get that because each ISP will
provide you with addresses from their own block. The addresses from one ISP
are not accessible through the other ISP. This also happens when you want to
change ISPs: you'll have to give the old block back to the ISP you are leaving
and you'll get a new block from your new ISP.

Because NAT isn't used with IPv6 you'll use your ISP's prefix for both your
externally accessible services and your internal networks. When changing ISPs
this means that you'll have to rennumber from the old addresses to the new
ones. With IPv6 this is easier to do than with IPv4. IPv6 is designed so that
using multiple addresses is normal. You can therefore connect the new ISP,
add their addresses to your network, and after everything has been migrated
you can remove the old ISP's addresses and cancel your connection to them.
Nevertheless, this can be a lot of work.

To summarise:
- Using your ISP's PA addresses is a good idea when:
  - You only connect to one ISP
  - You don't change ISPs often
- Using your ISP's PA addresses might *not* be a good idea when:
  - You want to connect to multiple ISPs
  - You change ISPs regularly
