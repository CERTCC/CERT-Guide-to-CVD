# Case and Bug Tracking

Case tracking systems such as bug trackers or trouble ticket systems are
often used by
[vendors](../../topics/roles/vendor.md),
[coordinators](../../topics/roles/coordinator.md), and
[reporters](../../topics/roles/finder.md) for tracking vulnerability
reports. Such systems can centralize the vulnerability
response process and provide the ability to track individual cases. Case
tracking systems also provide a means of collecting data about recurring
security issues and the performance of the response process itself.

!!! tip "Vulnerability Reports vs. Bug Reports"

    We have found it important to distinguish that vulnerability reports are
    not always bug reports. A single vulnerability report might contain
    information on more than one bug; alternately, it may describe a
    configuration issue that would not typically be considered a bug in the
    first place. In general, vulnerability reports and bug reports should be
    thought of as having a many-to-many relationship, allowing one or more
    vulnerability reports to be linked to one or more bug reports.

    That said, bug tracking systems can still be useful for vulnerability
    report tracking if this distinction is kept in mind, and the bug
    tracking system has the appropriate capabilities. 

!!! tip "MPCVD and Case Tracking"

    At the CERT/CC, we've found that more complicated CVD cases&mdash;for example the multiparty cases
    described in [MPCVD](../variation/mpcvd.md)&mdash;become more like projects than tickets.
    In the context of MPCVD, multiple organizations may be involved in the response
    process, and each organization may have its own case tracking system.

    We have been working on the development of a protocol for sharing case
    information across organizations, which we hope will help to address some of these
    challenges. The [Vultron Protocol](https://certcc.github.io/Vultron) is a work in progress
    that aims to provide interoperability across organizations' CVD processes.



