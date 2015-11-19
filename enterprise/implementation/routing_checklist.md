---
title: Routing checklist
---

* Do you support and publish the full IPv6 BGP Routing Table?
    * If not what portion of the BGP Routing Table do you support?
    * Are full IPv6 global routes available to end customers?
* Do you host and provide the access to a “looking glass” IPv6 BGP router,
  for the troubleshooting purposes?
* Do you accept and announce /48 blocks?
* What is the smallest prefix you accept?
* What is the smallest prefix your upstream providers accept from you?  Are
  there any restrictions on prefix advertisements?
* What percentage of your IPv4 peers to you currently peer with for IPv6?
* Are you partitioned from any other major networks?  (i.e.  lacking global
  reachability to other major networks) (Reference)?
    * Will the provider disclose its list of IPv6 peerings, indicating which
      IPv6 peerings are native and which are tunneled?
* Does the provider have a policy in place regarding deployment of tunnels
  on its backbone network or with peerings?
    * In other words, is there any IPv6 tunneling on the provider’s backbone
      network, and if peerings with other providers currently exist which
      are tunneled, does/will the provider have a policy in place which will
      mandate peerings with providers be native?
    * What MTU restrictions or standards are in place for any tunnels?
