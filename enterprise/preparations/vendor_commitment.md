---
title: Template for IPv6 vendor commitment
---

Introduction
============
More and more networks depend on IPv6, and those that don't use IPv6 yet will
very likely need it within the lifetime of the network equipment used. One of
the biggest showstoppers when deploying IPv6 is finding out that your equipment
vendor claimed to implement IPv6 when selling the equipment, but in practice
doesn't actively support it.

It is therefore recommended to ask vendors to make an official statement about
their endorsement and support of IPv6. This document can serve as a template
that can be used by governments, large enterprises and all other organisations
when seeking IPv6 such a statement from their vendors. It can also serve as an
aid to those people or organisations interested in tendering for government or
enterprise contracts.

Background
==========
While it might seem that a statement like this should not be necessary,
experience has shown that vendors sometimes don't take IPv6 seriously. For the
stability and manageability of our networks this needs to change.

Some examples of bad experiences from the field:

- Products that the vendor claims "supports IPv6" turns out to only support the
  bare minimum of IPv6 and lacks important functionality that is necessary to
  actually use it
  (also see [RIPE 554](https://www.ripe.net/publications/docs/ripe-554)).
- IPv6 features that are broken because they are not properly tested in a
  realistic environment.
- Products that support IPv6 but still need IPv4 to be configured as well.
  While this might not seem like a big problem, it will prevent you from
  simplifying and optimizing your network, and from saving money on valuable
  IPv4 addresses.
- Bug reports on missing or broken IPv6 functionality is treated as a "feature
  request" instead of a bug because IPv6 features are seen as a nice-to-have
  instead of as something mission critical.
- IPv6 seemed to work in a proof-of-concept setup, and later turned out to only
  function because the vendor's engineers made some custom "hacks" to get IPv6
  to work. None of the customer-facing interfaces (web based and command line)
  turned out to support IPv6, which made the equipment impossible to manage
  without getting the vendor's assistance for every single change.

All these situations cause operational problems, unacceptable delays and a lot
of frustration. It is better to make the vendor aware of the importance of IPv6
to your organisation before signing the contract than later when things are
going wrong in production.

Any vendor not willing to agree to such a statement in writing is deemed to be
unreliable for providing production quality products. Buying from such a vendor
should be considered a risk, which should be reflected in all relevant risk
assessments.

Statement template
==================
The vendor agrees, in writing, to the following:

- Vendor publicly endorses IPv6.
- Vendor's public and customer facing services will be IPv6-enabled. This
  includes the corporate website and each product/support site, as well as any
  customer support systems and other services required to use their products
  such as software and firmware download sites.
- Vendor will use their own products with IPv6 on their own productions networks
  (popularly called "eat their own dog food").
- Vendor will stipulate that their products operate with full functionality in
  an IPv6-only environment.
- Part of vendor's quality assurance testing for a product will be to test it
  in an IPv6-only environment.
- Vendor will treat any lack of support for IPv6 as a "bug", and not as just
  some missing "feature", and prioritise the bug report as such. This support
  of IPv6 includes:
  - All functionality that is supported on IPv4.
  - Any functionality required to run a secure and well-performing IPv6 network.
  - The ability to configure all IPv6 functionality through the regular user
    interfaces.
  - The ability to access all network-accessible user interfaces and management
    interfaces over IPv6.
- Vendor will have a corporate IPv6 manager or coordinator who works with all
  product line managers to make sure their products are embracing and supporting
  IPv6 in line with this vendor IPv6 commitment and to advocate its importance
  and status to C-level leadership in the company.
