# Reasons to Engage a Coordinator

There are a number of reasons that a finder, reporter, or vendor may
wish to engage a third-party coordinator to assist with the CVD process.

## Reporter Inexperience

Novice reporters sometimes request assistance from coordinators to
increase the chances of a successful resolution to the vulnerability
they have found. Working with a coordinator for the first few cases can
help develop a reporter's knowledge of the CVD process. From the
coordinator's perspective, working with novice reporters serves to
transfer knowledge of CVD to the security research community, thereby
improving vulnerability response overall. We have found that novice
reporters usually learn quickly and are willing to do most of the
coordination effort themselves, but just need occasional advice on how
the process should work.

## Reporter Capacity

Seeing a CVD case through to resolution can at times be a protracted
process. Not all reporters have the time or resources to follow up on
vulnerabilities they've reported. In such situations, a coordinator can
help by offloading some of the effort. However, coordinators are often
limited in their capacity as well, and must accordingly prioritize the
cases they choose to take on. As a result, coordinators and reporters
alike should take care to set clear expectations with each other as to
what roles they expect to play in any given coordination case.

{% include-markdown "../tutorials/troubleshooting/recipes/_x01.md" heading-offset=1 %}

## Multiple Vendors Involved

At its most effective, CVD follows the supply chain affected by the
vulnerability. As a mental model, it can be useful to think of the
supply chain as horizontal or vertical. A horizontal supply chain
implies that many vendors need to independently make changes to their
products in order to fix a vulnerability. A vertical supply chain
implies that one vendor might originate the fix, but many other vendors
may need to update their products after the original fix is available.
Software libraries tend to have vertical supply chains. Protocol
implementations often have horizontal supply chains.

We discuss horizontal and vertical supply chains in [Section
5.4](5.4-Multiparty-CVD_47677477.md) below.

{% include-markdown "../tutorials/troubleshooting/recipes/_x09.md" heading-offset=1 %}

## CVD Disputes

Occasionally vendors and reporters have difficulty arriving at a
mutually acceptable response to the existence of a vulnerability.

Disputes can arise for many reasons, including the following:

- Whether the behavior described in the report is reproducible
- Whether the behavior described in the report has security
    implications
- The impact of the vulnerability to deployed systems
- Whether to publicly disclose the vulnerability
- How much detail to include in a public disclosure
- The timing of public disclosure
- Whether extensions should be made to deadlines set by one party or
    another, whether or not they have been mutually agreed to previously

In these situations, and many others, reporters and/or vendors may find
it useful to engage the services of a third-party coordinator to assist
with conflict resolution. Drawing on the experience and relative
neutrality of a third-party coordinator can often dissipate some of the
potential animosity that can arise in contentious cases.

{% include-markdown "../tutorials/troubleshooting/recipes/_x21.md" heading-offset=1 %}

## Major Infrastructure Impacts

In situations where a vulnerability has the potential for major impact
to critical infrastructure, it may be necessary to coordinate not only
with vendors to fix the vulnerable products, but also with major
deployers. The primary concern in these cases is to ensure that internet
and other critical infrastructure remains available so that deployers
and other network defenders can acquire and deploy the necessary
information and patches.

Luckily this scenario is rare, but we have seen it come up in cases
affecting internet routing, the Domain Name System (DNS), internet
protocols, and the like. Vulnerabilities that affect basic Internet
services such as DNS (which also serves as an example of a horizontal
supply chain) affect a massive number of vendors; a coordinator can help
contact and disseminate information to vendors, service providers, and
other critical organizations for quick remediation.
