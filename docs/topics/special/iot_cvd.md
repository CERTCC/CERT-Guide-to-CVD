# IoT and CVD

!!! info inline end "About this page"

    This IoT-focused CVD page is adapted from two CERT/CC Blog Posts:
    [*Vulnerability Discovery for Emerging Networked Systems*](https://insights.sei.cmu.edu/cert/2014/11/-vulnerability-discovery-for-emerging-networked-systems.html)
    and
    [*What's Different About Vulnerability Analysis and Discovery in Emerging Networked Systems?*](https://insights.sei.cmu.edu/cert/2015/01/-whats-different-about-vulnerability-analysis-and-discovery-in-emerging-networked-systems.html)

In this section, we turn our attention to the implications that the Internet of
Things brings to the CVD discussion. "Smart things" are expected to
outnumber traditional computers in the near future and will likely
surpass mobile phones not long thereafter. IoT will have implications to
the protection of privacy, opportunities for fraud and abuse, and
ensuring safety. Every vulnerable thing becomes a potential point of
leverage for an attacker to persist or maneuver laterally through a
network. Immature security on IoT devices can leak information that
could allow an attacker to gain a foothold.

Because many such systems and devices are expected to remain
operationally useful for years or even decades with minimal
intervention, it is especially important that their security be
thoroughly understood prior to deployment.

!!! quote "Dan Geer, [*Security of Things*](http://geer.tinho.net/geer.secot.7v14.txt), 7 May 2014"

    An advanced persistent threat, one that is difficult to discover,
    difficult to remove, and difficult to attribute, is easier in a
    low-end monoculture, easier in an environment where much of the
    computing is done by devices that are deaf and mute once installed or
    where those devices operate at the very bottom of the software stack,
    where those devices bring no relevant societal risk by their onesies
    and twosies, but do bring relevant societal risk at today's extant
    scales much less the scales coming soon.

## IoT Concerns

We have observed a number of issues in the course of work done by the
CERT Vulnerability Analysis team. These issues are summarized below.

<div class="grid" markdown>

!!! danger "IoT Devices as Black Boxes"

    We identified issues such as the inclusion of networked appliances in a
    larger system where the appliances provided networked services based on
    sensor data. Enterprise security policy treated the device as a black
    box rather than a general-purpose computer with regard to patch levels,
    included software, and so forth. The attack vector posed by the sensor
    data interface had not been considered either.

!!! danger "Unrecognized Subcomponents"

    In a number of projects, we observed that while many systems were
    composed of highly specified off-the-shelf and custom components, the
    vendors providing those systems often could not identify the third-party
    subcomponents present in the delivered codebase. The problem can be as
    simple as not identifying statically linked libraries or as complicated
    as dealing with complex supply chains for code components.

!!! danger "Long-Lived and Hard-to-Patch"

    We observed various devices with wireless data capabilities embedded
    within a larger system yet little or no ability to patch the fielded
    systems except within very sparse service windows. Instances where
    physical contact with the device is required in order to update it can
    be especially problematic once vulnerabilities are discovered
    See Dan Geer's [talk](http://geer.tinho.net/geer.secot.7v14.txt) at the Security of Things Forum for more on the
    "long-lived and not reachable" problem).

!!! danger "New Interfaces Bring New Threats"

    We also encountered smart grid devices built out of a traditional
    electrical component coupled to an embedded Linux system to provide
    networked services. In a deployment context, the device was treated as
    an appliance. However, the impact of potential vulnerabilities in the
    general-purpose operating system embedded in the device had not been
    fully addressed.

</div>

The threats posed by these systems given their current proliferation trajectory are
concerning.
Even as they become more common, it can be difficult to identify the threats posed to a network by IoT either alone or in
aggregate.

<div class="grid" markdown>
!!! tip "The Hidden Linux Problem"

    In the simplest sense one might think of it as a "hidden
    Linux" problem: How many devices can you find in your immediate
    vicinity containing some form of Linux? Do you know what their patch
    status is? Do you know how you'd deal with a critical vulnerability
    affecting them?

!!! tip "The Third-Party Library Problem"

    Furthermore, while the hidden Linux problem isn't going away any time
    soon, we believe the third-party library problem will long outlast it.
    How many vulnerable image parsers with a network-accessible attack
    vector share your home with you? How would you patch them?

</div>

## Summarizing the IoT's Impact on CVD

We anticipate that many of the current gaps in security analysis tools
and knowledge will continue to close over the next few years. However, it
may be some time before we can fully understand how the systems already
available today, let alone tomorrow, will impact the security of the
networks onto which they are placed. The scope of the problem does not
appear to contract any time soon.

We already live in a world where mobile devices outnumber traditional
computers, and IoT stand to dwarf mobile computing in terms of the sheer
number of devices within the next few years. As vulnerability discovery
tools and techniques evolve into this space, so must our tools and
processes for coordination and disclosure. Assumptions built into the
CVD process about disclosure timing, coordination channels, development
cycles, scanning, patching, and so on, will need to be reevaluated in
the light of hardware-based systems that are likely to dominate the
future internet.
