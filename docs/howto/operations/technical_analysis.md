# Technical Analysis

While some CVD participants primarily collect, collate, and relay reports, others have the capability to perform
deeper technical analysis.
In [Phases](../../reference/phases/index.md), we make a distinction between report [validation](../../howto/operations/validation_and_triage.md)
and deeper analysis leading to problem isolation and remediation ([Remediation](../../howto/operations/remediation.md)).

For basic report validation, an organization might only need to be able to judge report credibility, set up test environments, and test scenarios appropriate to the report.

Deeper analysis might involve:

- Test case development and refinement
- Instrumentation and debugging
- Source code analysis
- Static binary code analysis (reverse engineering)
- Dynamic code analysis
- Root cause analysis

And so on.

## Test Bench and Virtualization

Having an internal testing infrastructure is vital to proper prioritization
and resolution of vulnerability reports as we discussed in
[Validation](../../topics/phases/validation.md) and [Prioritization](../../topics/phases/prioritization.md).
Not only is testing useful for confirming reports, or reproducing and isolating bugs; it can
also serve as a platform for an organization to develop its own
vulnerability discovery capability.

The analysts responsible for confirming incoming reports will over time
develop a familiarity with the ways in which a product is vulnerable,
and, given appropriate training and support, can begin to apply this
knowledge directly to the product without having to wait for
vulnerability reports to arrive from elsewhere. We have followed this
exact path at the CERT/CC: tools such as
[Dranzer](https://github.com/CERTCC/dranzer) and
[BFF](https://github.com/CERTCC/certfuzz)
came directly out of vulnerability analysts applying broad knowledge of
vulnerabilities gained from detailed analysis of reports toward the
development of automated discovery processes.

By far the easiest way to build a vulnerability testing infrastructure
is the use of virtualization technologies. Many different virtual
machine environments can be built for receivers of vulnerability reports
to verify or clarify the reports they receive.

At the CERT/CC, we maintain a firewalled testing network in which
virtual machines can be placed for testing. We also maintain a few
permanent pre-configured servers on this network (HTTP web servers,
etc.) to allow easy testing of certain classes of vulnerabilities, such
as "drive-by" browser downloads. Much of this infrastructure could be
replicated entirely in a virtual network within a single machine, or in
a cloud-based environment if desired.

Be sure your analysts have proper access to any necessary software
needed for testing. This includes maintaining appropriate software
licenses for proprietary software, although in many cases free and/or
open source alternatives are available.

Toolkits often include the
following:

- Virtualization platform, often a need to support multiple operating
    systems
- Debuggers
- Source code analysis tools
- Binary analysis tools (decompilers, etc.)
- Network sniffing tools
- Hex editors
- Text editors
- Visualization (often built into other tools)

Vendors with more hardware-centric products may need to additionally
maintain more physical gear or specialized test bench equipment in order
to have sufficient capacity to confirm reports.
