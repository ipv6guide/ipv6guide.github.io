---
title: Implementation
---

Now that you have [prepared](../preparations) everything and made the
necessary [architectural decisions](../architectural_decisions) it is time
to start implementing!

You should first [talk to your ISP(s)](isp_criteria) about IPv6.  All
respectable ISPs should be able to provide you with IPv6 connectivity these
days, so if your ISP doesn't provide IPv6 then you should seriously consider
switching to a different one.  Besides making sure your ISP provides you
with the required services now is also the time to start an [RFP](rfp) to
upgrade or replace the equipment and services that don't provide all the
IPv6 features that you need.

When deploying a new protocol like IPv6 it is important to get advice and
support from someone who already has experience with the deployment. 
Getting a [consultant](consultant_criteria) that can help with the IPv6
project can help you avoid mistakes.

One of the most common mistakes when implementing IPv6 is to treat the IPv6
address space like IPv4.  It is a good idea to use [IP Address Management
(IPAM)](ipam) tools from the start.  With the enormous amount of address
space that IPv6 provides you keeping track of everything in a spreadsheet or
text document will quickly become cumbersome.  Using the right tools from
the start will save you a lot of work later on.

With the help of your IPv6 consultant you should write an [implementation
plan](plan).  This plan describes the way IPv6 is going to be deployed and
the order in which IPv6 is going to be deployed in the different parts of
your enterprise network.

When deploying IPv6 do not forget to include IPv6 network and services
[monitoring](monitoring).  If IPv6 breaks your service will break for at
least a part of your user base.  Make sure that you notice IPv6 related
outages so that you can provide the same level of service on both IPv4 and
IPv6.

While deploying IPv6 [document](documentation) the results in such a way
that your colleagues and other ICT departments know how your network is
built with both IPv4 and IPv6.  Make sure it contains all information that
is required to understand the choices that have been made.  Your knowledge
of IPv6 is probably more advanced than that of your colleagues at this
point, and many things that seem intuitive and common sense still need to be
explained for those not yet as experienced.

Integrating IPv6 in your existing infrastructure is hard work.  It would be
a waste of time and money if other projects deploy IPv4-only solutions that
need extra work later to become IPv6 capable.  It is important that IPv6 is
taken into account in all future ICT projects so that you don't need to keep
catching up.

Most mainstream equipment has been well tested with IPv6. If you start using
new features or equipment that isn't mainstream (yet) you might want to set up a
[validation lab](validation_lab) to verify that everything works as it should.
