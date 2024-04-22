# Common Challenges in Vulnerability Analysis and Response

!!! info inline end "Origins of this page"

    The content on this page began as a list of challenges in vulnerability analysis and response for
    IoT systems in our blog post
    [_What's Different About Vulnerability Analysis and Discovery in Emerging Networked Systems?_](https://insights.sei.cmu.edu/cert/2015/01/-whats-different-about-vulnerability-analysis-and-discovery-in-emerging-networked-systems.html){:target="_blank"}.
    We have since recognized that many of these challenges are not unique to IoT, but are
    common to many emerging networked systems, including AI/ML systems.

In 2014-2015, the CERT/CC conducted a study of vulnerability discovery, analysis, and response for IoT systems.
At the time, we referred to these systems as "emerging networked systems" to emphasize that they were not traditional
computing systems, and the term "IoT" was not yet in common use.
From that study, we identified a number of challenges that seemed to distinguish IoT systems from traditional computing systems.
However, we have since recognized that many of these challenges are not unique to IoT, but are common to many
emerging networked systems, including AI/ML systems. Our current perspective is that these are general challenges
that can affect different types of systems in different ways.

!!! note "About This List"

    The following list of challenges is based on our original analysis of IoT systems, but we have updated the text to
    reflect the broader applicability of these challenges to other emerging networked systems. Over time, we expect to
    expand this list to include additional challenges we encounter.
    Each item is labeled with tags indicating which system types are most affected by the issue. 

    <div class="grid cards" markdown>

    -  The tags are as follows:

        ---
        - **AI/ML** : Artificial Intelligence/Machine Learning
        - **IoT**: Internet of Things
        - **Mobile**: Mobile applications
        - **Web**: Web applications
        - **Traditional**: Traditional computing systems

    - The symbols indicate the relevance of the issue to each system type:

        ---
        - :material-check-all: The issue is highly relevant to the system type.
        - :material-check: The issue is somewhat relevant to the system type.
        - :octicons-circle-slash-16: The issue is not usually relevant to the system type.

    </div>

!!! warning "Limited Instrumentation"

    **AI/ML** :material-check-all: |
    **IoT** :material-check-all: |
    **Mobile** :material-check: |
    **Web** :material-check-all: |
    **Traditional** :octicons-circle-slash-16:

    The vulnerability analyst's ability to instrument the system in order to test its security can be limited.

    AI/ML systems can be difficult to instrument because their operation is often opaque, even to the developers who 
    created them. That is, while it may be possible to observe the inputs and outputs of the system, the internal
    operations of the system may be difficult to observe or interpret.
    Many IoT systems comprise embedded devices that are effectively black boxes at the network level.
    
    Web applications operated by other parties can be difficult to instrument, especially if the application is
    not under the control of the analyst. This is especially true if the application is a black box, such as a SaaS
    application.

    On the surface, this limitation might appear to be beneficial to the security of the system in question:
    after all, if it's hard to create an analysis environment, it might be difficult to find vulnerabilities in the system.
    However, the problem is that while a determined and/or well-resourced attacker can overcome such obstacles and 
    get on with finding vulnerabilities, a lack of instrumentation can make it difficult even for the vendor to 
    adequately test the security of its own products.

!!! warning "Less Familiar System Architectures"

    **AI/ML** :material-check-all: |
    **IoT** :material-check-all: |
    **Mobile** :material-check: |
    **Web** :octicons-circle-slash-16: |
    **Traditional** :octicons-circle-slash-16:

    AI/ML systems can run on a variety of hardware architectures, including GPUs, FPGAs, and custom ASICs.
    
    IoT systems can run on a variety of hardware architectures, including ARM, MIPS, and others.
    
    Mobile systems tend to run on ARM architectures, which are increasingly common in the mobile and IoT spaces.
    But a single smartphone can contain multiple system-on-a-chip processors with different architectures
    (for bluetooth, wifi, gps, etc.), so the analyst may need to understand multiple architectures to fully analyze
    the system.
    
    These architectures are often different from those most often encountered by the typical vulnerability analyst,
    who is likely to be most familiar with x86 and IA64 architectures.
    Although this limitation is trivially obvious at a technical level, many vulnerability researchers and analysts
    will have to overcome this skill gap if they are to remain effective at finding and remediating vulnerabilities in IoT
    and AI/ML systems.

!!! warning "Limited User Interfaces"

    **AI/ML** :material-check-all: |
    **IoT** :material-check-all: |
    **Mobile** :octicons-circle-slash-16: |
    **Web** :octicons-circle-slash-16: |
    **Traditional** :octicons-circle-slash-16:

    Many AI/ML systems operate as black boxes behind an API, with no user interface at all.

    Meanwhile, the user interfaces for IoT devices are often limited, especially in comparison to traditional computing systems.
    For some IoT devices, the only user interface is a smartphone app, which may not provide the level of detail needed
    to perform a security analysis.

    Thus, significant effort can be required just to provide input or get the feedback needed to perform security 
    analysis work.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  

!!! warning "Proprietary Protocols"

    **AI/ML** :material-check: |
    **IoT** :material-check-all: |
    **Mobile** :material-check: |
    **Web** :octicons-circle-slash-16: |
    **Traditional** :material-check:


    IoT systems often use proprietary protocols, especially at the application layer.
    Although the spread of HTTP/HTTPS continues in this space as it has in the traditional and mobile spaces, there are many extant protocols that are poorly documented or wholly undocumented.

    AI/ML and mobile systems may use proprietary protocols as well, but there
    is often a more standardized API for interacting with the system as a whole, so this limitation is less severe in
    those contexts.

    Some special-purpose traditional software also uses proprietary protocols, but the prevalence of open standards
    in traditional computing systems means that this limitation is encountered less frequently in that context as well.

    Regardless, the effort required to identify and understand higher level protocols, given sometimes scant information
    about them, can be daunting.
    Techniques and tools for network protocol inference and reverse engineering can be effective tactics.
    However, if vendors were more open with their protocol specifications, much of the need for that effort would be obviated. 

!!! warning "Lack of Updatability"

    **AI/ML** :material-check: |
    **IoT** :material-check-all: |
    **Mobile** :octicons-circle-slash-16: |
    **Web** :octicons-circle-slash-16: |
    **Traditional** :octicons-circle-slash-16:


    Unlike most other devices (laptops, PCs, smartphones, tablets), many IoT are either non-updateable or require 
    significant effort to update.

    AI/ML systems can be designed to be updated, but it may not always be easy to do so, especially if the system is
    dependent on a specific version of a library or other component such as a model sourced from a third party.

    Systems that cannot be updated become less secure over time as new vulnerabilities are found and novel attack 
    techniques emerge.
    Because vulnerabilities are often discovered long after a system has been delivered, systems that lack facilities 
    for secure updates once deployed present a long-term risk to the networks in which they reside.
    This design flaw is perhaps the most significant one already found in many IoT, and if not corrected across the board,
    could lead to years if not decades of increasingly insecure devices acting as reservoirs of infection or as 
    platforms for lateral movement by attackers of all types.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |

!!! warning "Lack of Security Tools"

    **AI/ML** :material-check-all: |
    **IoT** :material-check-all: |
    **Mobile** :material-check: |
    **Web** :octicons-circle-slash-16: |
    **Traditional** :octicons-circle-slash-16:

    Security tools used for prevention, detection, analysis, and remediation in traditional computing systems have 
    evolved and matured significantly over a period of decades. And while in many cases similar concepts apply to IoT and
    AI/ML systems,
    the practitioner will observe a distinct gap in available tools when attempting to secure or even observe such a 
    system in detail. 

    Packet capture and decoding, traffic analysis, reverse engineering and binary analysis, and the 
    like are all transferable as concepts if not directly as tools, yet the tooling is far weaker when you get outside 
    of the realm of Windows and Unix-based (including macOS) operating systems running on x86/IA64 architectures.
    This affects both IoT and AI/ML systems, as the latter often run on specialized hardware and software platforms
    with similar limitations.

!!! warning "Vulnerability Scanning Tool and Database Bias"

    **AI/ML** :material-check-all: |
    **IoT** :material-check-all: |
    **Mobile** :material-check: |
    **Web** :material-check: |
    **Traditional** :octicons-circle-slash-16:


    Vulnerability scanning tools largely look for known vulnerabilities. They, in turn, depend on vulnerability 
    databases for their source material. However, databases of known vulnerabilities&mdash;[CVE](https://www.cve.org){:target="_blank"},
    the [National Vulnerability Database](https://nvd.nist.gov){:target="_blank"} (NVD), [Japan Vulnerability Notes](https://jvn.jp/en/){:target="_blank"}.
    (JVN) and the [CERT Vulnerability Notes Database](https://www.kb.cert.org/vuls){:target="_blank"}&mdash;are heavily biased by their 
    history of tracking vulnerabilities in traditional computing systems (e.g., Windows, Linux, macOS, Unix and variants).
    Recent conversations with these and other vulnerability database operators indicate that the need to expand coverage
    into Mobile, IoT, AI/ML, and Web systems is either a topic of active investigation and discussion or a work 
    already in progress. However, we can expect the existing gap to remain for some time as these capabilities ramp up.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           

!!! warning "Inadequate Threat Models"

    **AI/ML** :material-check-all: |
    **IoT** :material-check-all: |
    **Mobile** :material-check: |
    **Web** :material-check: |
    **Traditional** :material-check:

    Overly optimistic threat models are common among emerging networked systems.
    Many AI/ML systems and IoT devices are developed with what can only be described as 
    naive threat models that drastically underestimate the hostility of the environments into which the system will be 
    deployed.

    Undocumented threat models are still threat models, even if they only exist in the assumptions made by 
    the developer.
    
    Even in cases where the developers of the main system are security-knowledgeable, they are often 
    composing systems out of components or libraries that may not have been developed with the same degree of security 
    consideration. This weakness is especially pernicious in power- or bandwidth-constrained systems where the goal of 
    providing lightweight implementations supersedes the need to provide a minimum level of security. We believe this is 
    a false economy that only defers a much larger cost when the system has been deployed, vulnerabilities are discovered, 
    and remediation is difficult.

!!! warning "Third-party library vulnerabilities"

    **AI/ML** :material-check-all: |
    **IoT** :material-check-all: |
    **Mobile** :material-check-all: |
    **Web** :material-check-all: |
    **Traditional** :material-check-all:

    We observe pervasive use of third-party libraries with neither recognition of nor adequate planning for how to fix 
    or mitigate the vulnerabilities they inevitably contain. When a developer embeds a library into a system, that system 
    can inherit vulnerabilities subsequently found in the incorporated code. Although this is true in the traditional 
    computing world, it is even more concerning in contexts where many libraries wind up as binary blobs and are simply 
    included in the software or firmware as such. This is common to both IoT, where drivers might be included as binary
    blobs, and AI/ML, where models might be included as opaque objects.
    Lacking the ability to analyze this black box code either in manual source code 
    reviews or using most code analysis tools, vendors may find it difficult to examine the code's security.

!!! warning "Unprepared Vendors"

    **AI/ML** :material-check-all: |
    **IoT** :material-check-all: |
    **Mobile** :material-check-all: |
    **Web** :material-check: |
    **Traditional** :material-check:


    Often we find that new vendors are not prepared to receive and handle vulnerability reports from outside parties, 
    such as the security researcher community. 

    Many also lack the ability to perform their own vulnerability discovery within their development lifecycle.
    These difficulties tend to arise from one of two causes:
    
    1. The vendor is comparatively small or new and has yet to form a product security incident response capability.
    2. The vendor has deep engineering experience in its domain but has not fully incorporated the effect of 
    network-enabling its products into its engineering quality assurance (this is related to the inadequate threat 
    model point above). Typically, vendors in this group may have very strong skills in safety engineering or 
    regulatory compliance, yet their internet security capability is lacking.

    Our experience is that many new vendors are surprised by the vulnerability disclosure process.
    We frequently find ourselves having conversations that rehash decades of vulnerability 
    coordination and disclosure debates with vendors who appear to experience something similar to the
    [Kübler-Ross stages of grief](https://en.wikipedia.org/wiki/Five_stages_of_grief){:target="_blank"} during the process 
    (denial, anger, bargaining, depression, and acceptance).

!!! warning "Unresolved Vulnerability Disclosure Debates"

    **AI/ML** :material-check-all: |
    **IoT** :material-check-all: |
    **Mobile** :material-check-all: |
    **Web** :material-check-all: |
    **Traditional** :material-check-all:

    In the traditional computing arena, most vendors and researchers have 
    settled into a reasonable rhythm of allowing the vendor some time to fix vulnerabilities prior to publishing a 
    vulnerability report more widely. Software as a service (SAAS) and software distributed through app stores can often 
    fix and deploy patches to most customers quickly. On the opposite end of the spectrum, we find many IoT and embedded 
    device vendors for whom fixing a vulnerability might require a firmware upgrade or even physical replacement of 
    affected devices. Conversations with the AI/ML community are even more varied -- it's not always clear what
    policy expectations are in that space, nor what "fixing" a vulnerability might mean in that context.

    This diversity of requirements forces vendors and researchers alike to reconsider their expectations 
    with respect to the timing and level of detail provided in vulnerability reports based on the systems affected
    In the past few years, the shift toward IoT has brought different stakeholders into the vulnerability disclosure
    debate, and we expect that the AI/ML community will bring even more new perspectives to the table.

    The point is not that there is a single right answer to "resolve the debate". Instead, the CERT/CC emphasizes the
    necessity of continuing the conversation and adapting solutions to the diverse needs of the stakeholders,
    communities, and the systems they are trying to protect. What works for some groups may not work for others, but
    we're committed to helping all parties find a way to work together effectively.

<!--
more problems to address

- lack of secure update mechanisms
- difficulty localizing vulnerabilities in a system to a specific component
- lack of a common language for discussing vulnerabilities
- policy uncertainty (of the system, not the disclosure policy)
- capital cost of test environments
- security is a cost center, not a profit center

-->
