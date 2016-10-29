---
title: Routing protocols
---

When deploying a new protocol like IPv6 it is tempting to also start looking at
different routing protocols. But IPv6 already will provide new concepts for your
engineers to grasp. It is therefore recommended to keep the IPv6 routing
protocols as similar to what you have for IPv4 as possible.

|  IPv4  | IPv6   |
| ------ | ------ |
| EIGRP  | EIGRP  |
| OSPFv2 | OSPFv3 |
| IS-IS  | IS-IS  |
| BGP    | BGP    |

When setting up BGP sessions set up separate sessions for IPv4 and IPv6. While
it is possible to exchange IPv6 routes over an IPv4 BGP session and vice versa
it will cause many operational problems. There are "hacks" to solve that, but
the increased complexity will make mistakes that break the network very likely.
Setting up separate BGP sessions for IPv6 is a bit of extra work, but the
simplicity of the setup greatly outweighs that.
