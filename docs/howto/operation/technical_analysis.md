# Technical Analysis

While some CVD participants primarily collect, collate, and relay reports, others have the capability to perform
deeper technical analysis.
In [Phases](../../topics/phases/index.md), we make a distinction between report [validation](../../topics/phases/validation.md)
and deeper analysis leading to problem isolation and remediation ([Remediation](../../topics/phases/remediation.md)).

!!! tip "Depth of Analysis"

    The depth of analysis required will depend on the organization's capabilities and the nature of the vulnerability.
    For basic report validation, an organization might only need to be able to judge report credibility, set up test environments, and test scenarios appropriate to the report.

    Deeper analysis might involve:

    - Test case development and refinement
    - Instrumentation and debugging
    - Source code analysis
    - Static binary code analysis (reverse engineering)
    - Dynamic code analysis
    - Root cause analysis

## Test Environments

Having an internal testing infrastructure is vital to proper prioritization
and resolution of vulnerability reports as we discussed in
[Validation](../../topics/phases/validation.md) and [Prioritization](../../topics/phases/prioritization.md).
Be sure your analysts have proper access to any necessary software
needed for testing. This includes maintaining appropriate software
licenses for proprietary software, although in many cases free and/or
open source alternatives are available.

!!! tip "Toolkits"

    Analysts should have access to a toolkit of software to assist in
    their analysis. The contents of such a toolkit will vary depending on
    the organization's needs and capabilities.
    Toolkits often include the
    following:

    - Container or virtualization platform, often a need to support multiple operating
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

<div class="grid" markdown>

!!! tip "Virtualization and Cloud Infrastructure"

    By far the easiest way to build a vulnerability testing infrastructure
    is the use of virtualization technologies. Many different virtual
    machine environments can be built for receivers of vulnerability reports
    to verify or clarify the reports they receive.
    Containers are another useful option, but they are generally less isolated than
    virtual machines and may not be appropriate for all testing scenarios.

!!! tip "Dedicated Testing Resources"

    Not everything can be tested in a virtual environment, however. Some
    vulnerabilities are hardware-specific, or require specialized
    equipment to test. In these cases, it may be necessary to maintain a
    physical test bench.

</div>

!!! example "CERT/CC's Testing Infrastructure"

    At the CERT/CC, we maintain a firewalled testing network in which
    virtual machines can be placed for testing. We also maintain a few
    permanent pre-configured servers on this network (HTTP web servers,
    etc.) to allow easy testing of certain classes of vulnerabilities, such
    as "drive-by" browser downloads. Much of this infrastructure could be
    replicated entirely in a virtual network within a single machine, or in
    a cloud-based environment if desired.

## Tool Development

In some cases, it may be necessary to develop new tools to assist in
vulnerability analysis. This can be a significant investment of time and
resources, but can also pay off in the long run by making the analysis
process more efficient.

<div class="grid" markdown>
!!! tip "Vulnerability Report Analysis can Boost Internal Discovery"

    Not only is testing useful for confirming reports, or reproducing and isolating bugs; it can
    also serve as a platform for an organization to develop its own
    vulnerability discovery capability.
    The analysts responsible for confirming incoming reports will, over time,
    develop a familiarity with the ways in which a product is vulnerable,
    and, given appropriate training and support, can begin to apply this
    knowledge directly to the product without having to wait for
    vulnerability reports to arrive from elsewhere.

!!! example "Testing Infrastructure and Tool Development"

    We have followed this exact path at the CERT/CC: tools such as [Dranzer](https://github.com/CERTCC/dranzer){:target="_blank"} and
    [BFF](https://github.com/CERTCC/certfuzz){:target="_blank"} came directly out of vulnerability analysts applying broad knowledge of
    vulnerabilities gained from detailed analysis of reports toward the development of automated discovery processes.

</div>
