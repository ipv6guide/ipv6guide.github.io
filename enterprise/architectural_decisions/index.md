---
title: Architectural decisions
---

When introducing IPv6 there are many architectural questions that have to be
answered.  One of the more fundamental ones is to think about the addressing
plan on a high level: 
Are you going to [use IPv6 address from your ISP](use_PA), 
are you going to [get provider independent addresses](use_PI) 
or are you going to [get your own huge block of addresses](become_LIR) 
to be able to assign addresses to all your sites and infrastructure?
Each choice has its own [advantages and disadvantages](discuss_PI_PA_LIR) that you'll have to consider.

If you have chosen to use your own addresses then you need to [make those
addresses reachable from the internet](routability).  Enterprises usually do
this by [buying transit connectivity](connect_transit) from one or more
ISPs.  If your enterprise consists of one or a few sites and they are all connected to
the same ISP, then this is quite straightforward, but there is a popular yet
complex situation: some enterprises have many sites, sometimes spread over
multiple countries or even multiple continents, but still want to use one
huge block of addresses to keep a consistent addressing plan.  We explore
the conflicting interests of the [routing table size vs simplified address
planning](routing_vs_addressing) and try to provide some [solutions that try
to optimise both](deaggregation_solutions).

Now that you have a better view of which addresses are available to you and
how to ensure routability (probably after going back and forth over the
previous paragraphs to investigate different scenarios) it is time to [write
an addressing plan](addressing_plan).  This will provide you with a
framework when deploying your IPv6 infrastructure.  Some network and
security engineers try to write their IPv6 addressing plan in such a way
that they can hide parts of their infrastructure by using
non-publicly-routed addresses.  There are several reasons why this is [a
worse idea than it seems](unroutable_infra_addresses).

And then it is time to think about the more technical aspects of your IPv6
architecture.  Because IPv6 doesn't use NAT many people are afraid of the
security implications of having public addresses throughout the network. 
The good news is: that is how the internet was designed!  Modern firewalls
provide the same or higher levels of protection as NAT devices, and more.  This is a
good time to [think about different types of firewalls and for what purpose
you are going to use them](consider_firewalls).

The next architectural decision to make is [which IGP routing protocol to
use](choose_igp).  This is about seeking a balance between keeping things
familiar for engineers, keeping IPv4 and IPv6 separate so that a problem
with one doesn't affect the other and making internal routing more efficient
and simple.

The last question to think about is something that usually doesn't even come
up with IPv4 networks: [whether to use DHCP](why_dhcp).  For IPv4 networks
the choice is easy: if you want automatic address assignment you need DHCP. 
But IPv6 provides you with more choice.  We [discuss the most common
deployment models](discuss_lan_models).  It is important to think about
these aspects of the different models and choose the best model for each
network.  It is not uncommon to use different models for different types
(servers, office, mobile devices, guests etc.) of networks so it is
important you understand all of them.

Depending on the complexity of the architecture you have designed you might
want to [build a lab](build_lab) to see if the choices you made work well in
practice. Especially if you are new to IPv6 detecting architectural mistakes at
this point will save a lot of time later.
