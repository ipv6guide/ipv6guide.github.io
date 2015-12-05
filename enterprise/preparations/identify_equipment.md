---
title: Identify equipment
---

Most enterprise equipment that has been sold in the last decade has support
for IPv6 in some way.  Unfortunately not all equipment is equally ready for
IPv6.  Some equipment does not support IPv6 at all.  Such equipment will
need to be replaced.

Introducing a new technology involves a lot of compatibility and dependency
checking.

Compatibility and dependency checking
=====================================
There are many places that could have dependencies on the network protocols
used.  Because IPv4 has been the standard protocol for many years almost all
devices and applications can work well with it.  While IPv6 has been
available for more than a decade there are many devices and applications
that haven't been properly prepared for it.  We recognise the following
classes of devices and applications:

1. Disturbed by IPv6
2. Oblivious to IPv6
3. Compatible with IPv6
4. Feature parity for IPv6
5. Enhanced for IPv6

1: Disturbed by IPv6
--------------------
The first class is a real problem.  This class is mostly seen with
applications that haven't taken IPv6 into account despite the fact that the
operating system provides IPv6.  Examples are applications that assume IPv4
data structures, log file parsers that can't parse IPv6 addresses,
applications that store the client IP address in a database field that
doesn't support IPv6 etc.

2: Oblivious to IPv6
--------------------
For devices and applications in the second class their function in the
network determines what the impact will be.  For devices on the edge of the
network it might not cause any problems as long as the network is
dual-stacked (providing both IPv4 and IPv6).  Such devices and applications
can be used with IPv4-only, ignoring IPv6 running next to it.

For network devices and applications the impact varies.  If IP is only used
for management (e.g.  pure layer-2 devices) the impact is the same as with
edge devices.  But for devices and applications in this class that are
actively involved in IP networking this is a problem.  Such devices and
applications must be upgraded or replaced.

Even when not a problem today everything in this class will prevent you from
migrating to IPv6-only in the near or far future.  This means that you will
have to keep supporting both IPv4 and IPv6 throughout your network.  Running
two networking protocols increases complexity and maintenance costs.  The
end goal should be to phase out IPv4 at some point in time.

3: Compatible with IPv6
-----------------------
This class consists of devices and applications that can perform their most
important, but not all, features using IPv6, or where the configuration for
IPv6 is adds a lot of complexity.  Examples are:

- routers that can route IPv6 packets but can only be managed over IPv4
- mail servers that can receive mail over IPv6 but don't provide full spam
  protection
- switches that can do DHCP snooping for IPv4 but not for IPv6
- load balancers that don't support all load-balancing strategies for IPv6
- firewalls that have completely separate rules for IPv4 and IPv6, requiring
  everything to be configured twice

Whether the limitations are a problem depends on the function and situation. 
In some situations it might be acceptable to keep such a device or
application, in other situations upgrading or replacing it might be
necessary.

4: Feature parity for IPv6
--------------------------
This is the minimal class you should aim for.  Devices and applications in
this class provide the same feature set for IPv4 and IPv6.  Fortunately
there are many applications that fall in this category.  Unfortunately there
are still many networking devices that don't.  Whether that is a problem
depends on your needs.  If a device doesn't provide full feature parity but
you already know that you are never going to use the missing features anyway
you can consider that as feature parity.

5: Enhanced for IPv6
--------------------
Feature parity is not the highest classification though.  While IPv6 is very
similar to IPv4 in many aspects it can be very different in other aspects. 
Some examples are features like RA-Guard, firewalls being capable of
detecting IPv6-specific attacks etc.  Other examples are devices that can
use the huge IPv6 address space to e.g.  simplify addressing and management.

Investment strategy
===================
Enterprises should adopt a policy that prohibits buying class 1 and 2
devices.  Such devices will require you to keep supporting IPv4, preventing
you from optimising your network and reducing operational costs in the
future.  Class 3 devices might be acceptable if you can live with the
missing features.  This should be decided on a case-by-case basis and if
possible discouraged.  Class 4 and 5 should be strongly preferred.

It is a very good idea to fit replacements into an existing equipment
replacement cycles.  That way implementing IPv6 will not be a huge extra
cost and cause accelerated deprecation of existing investments.

When planning a RFP process, use
[RIPE-554](https://www.ripe.net/publications/docs/ripe-554) or a similar
list as requirements for IPv6 capabilities for you newly purchased equipment
and services.  All major vendors know about these lists, which also makes it
easier to find equipment whose capabilities match the requirements on the
list.

Practical advice
================
Build a spreadsheet with equipment, its IPv6 capability level and
replacement cycles.  This list will also serve you for later transition and
implementation planning purposes.
