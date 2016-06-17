---
title: IPv4/IPv6 FAQ
---

History
=======
Many questions about the history of the internet come up regularly:

- **Early adopters of IPv4 got bigger allocations than I can get as a
  newcomer. That’s not fair!<sup>[[1]](#f1)</sup>**

  Well, I arrived late at the station and the train left without waiting for
  me. That’s not fair either.

  Everyone who has IP space obtained it using the allocation policies that
  were in effect at that time. These policies have changed over the years
  as the Internet community and its needs have changed. As reserves of
  IPv4 addresses dwindled, allocation policies have become more restrictive
  to reflect that run-out. Current policy aims to make small amounts of IPv4
  available to new entrants so they can connect their IPv6 networks to the
  legacy Internet.

  Until someone invents time travel, it won’t be possible to turn back the
  clock and apply today’s policies to the circumstances which prevailed 
  10-20 years ago. All we can do now is run down the last reserves of IPv4
  in the least-worst way possible. This is going to inconvenience everyone.
  But frankly, the only realistic way now for any LIR to grow their network
  is to deploy IPv6.

- **According to IANA, 240/4 is reserved.
  Why can’t we use it?<sup>[[1]](#f1)</sup>**

  First off, there is no guarantee that space could be used if it was made
  available. There are an unknown (and probably large) number of devices on
  the Internet which are hard-coded to ignore these “Class E” addresses.
  These devices would have to be replaced or upgraded. In some cases -- 
  legacy systems, embedded firmware -- this may be impractical. Many
  firewalls and routers would have to be reconfigured too because they use
  filters which treat addresses in this 240/12 prefix as bogus.

  Before the current allocation policy was adopted, the Internet consumed
  around one /8 of IPv4 space each month. So if 240/4 could be made
  available for allocation, it would only delay the exhaustion of IPv4 by a
  little over a year.

  The IETF has made various attempts to make this historical Class E space
  available for allocation. These have all failed. Future efforts to do this
  are likely to fail too.

  The inconvenient truth is no matter what we do with IPv4, there simply
  isn’t enough address space to go round. IPv6 is the only way to be sure
  we can issue a unique, routable IP address to everything and everyone who
  wants one.

RIPE/RIPE NCC specific
======================

- **Why’s the current policy called “last /8”?<sup>[[1]](#f1)</sup>**

  This name is a little misleading. The current IPv4 allocation policy came
  into effect when the RIPE NCC first had to make an allocation from 185/8,
  the last /8 it received from IANA. That’s why the term “last /8” became
  widely adopted. It’s misleading because the policy applies to all IPv4
  allocations by the RIPE NCC, not just those from 185/8. Some LIRs will get
  their final allocation of a /22 from 185/8 while others will get these
  from other available address blocks held by the RIPE NCC.

---

<b id="f1">[1]</b> Contributed by Jim Reid
