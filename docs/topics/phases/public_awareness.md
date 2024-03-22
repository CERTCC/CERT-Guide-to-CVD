# Public Awareness

Public awareness of a vulnerability can be intentionally used to promote deployment of the fix.
However, that is not the only reason to draw the public's attention to the existence of a vulnerability.
Other reasons include providing a history of fixed security flaws, or facilitating research into the root causes of vulnerabilities.

For defenders, deploying patches requires effort and is often avoided
unless there is sufficient justification. Therefore it is important to
provide at least a brief description of the vulnerability in the release
notes for the updated code. Knowledge of the existence of a
vulnerability is often the key driver causing patches to be deployed.

## Disclosure Decisions

Even within the CVD process, there are still many decisions to be made
about the disclosure process. The audience, timing, and amount of
information released can vary because of a number of factors. These
choices might even vary from report to report, depending on the impact
and consequences of a particular vulnerability.

Generally, finders, reporters, vendors, and coordinators should consider
the following questions in establishing their policies and practices:

<div class="grid" markdown>

!!! question "Should you disclose at all?"

    Generally, the answer will be yes,
    but there may be factors that influence this decision. For example,
    some vulnerabilities, if exploited, could place lives in danger or
    cause severe socioeconomic harm. As a result, it may be prudent for
    reports of such vulnerabilities to be held indefinitely until the
    population of vulnerable systems has been reduced through patching
    or obsolescence. However, any decision to defer disclosure should be
    considered provisional or contingent on the continued absence of
    evidence of exploitation or adversarial knowledge of the
    vulnerability.

!!! question "What information will you disclose?"

    For example, will you
    publish all information about the vulnerability, including proof of
    concept code, or will you only release a brief description of the
    problem and a remediation? Generally speaking, there is a minimum
    amount of information required in order for a vulnerability report
    to be useful. Recall that the point of disclosure is to provoke some
    action, most often by deployers or any downstream vendors who were
    not already involved in the coordination process. If the details
    provided to the recipient are insufficient to cause that action to
    be taken, the disclosure process will not succeed.

!!! question "To whom will you disclose?"

    In most cases, the disclosure should
    be made publicly. However, in some scenarios the disclosure may be
    to a specific limited group. For example, if the pool of users is
    small and the vendor reaches out to every impacted user, a public
    disclosure may be unnecessary.

!!! question "Via what channel(s) will you disclose?"

    Will the vulnerability
    information be published on the vendor's website? The reporter's
    blog? One or more mailing lists?
    Will you draw attention to it on social media?

    There are pros and
    cons to most of these options that must be weighed. When available,
    an organization's communications or public relations groups should
    be involved in planning for the disclosure process. While it is
    usually neither possible nor practical to have every CVD case flow
    through them, leveraging their expertise in planning and developing
    the CVD capability can improve the process
    considerably.

</div>

!!! question "What is your expectation of others in disclosing further (or not)?"

    Be sure to discuss your expectations with all stakeholders and be
    prepared to negotiate.

!!! tip "Three Key Questions for Vendors"

    Vendors in particular will need to address three main questions in
    providing vulnerability and fix information to defenders:

    -   What information should be provided about the vulnerability?
    -   Where should this information be provided?
    -   What, if any, additional measures should be taken to draw attention
        to the existence of the vulnerability or the availability of its
        fix?

!!! tip "When to Engage a Coordinator"

    In multiparty CVD, private notifications to other vendors and even
    public disclosures by individual vendors may not sufficiently raise
    awareness or accurately reflect the scope of a vulnerability. Because of
    the role they play in conveying information to a broad audience of
    system deployers, trusted third parties (non-vendors) such as DHS CISA,
    the CERT/CC, or other coordinators can help notify affected vendors,
    facilitate technical analysis of the vulnerability and its impact, and
    amplify communications to the public.  When vendors provide advance
    notice of major vulnerabilities to the coordinator community, it allows
    the various coordinating organizations to prepare accurate remediation
    instructions for system deployers, and to publish that information in
    synchronization with the vendors' release of the patches. When that
    advance notification does not occur sufficiently early, as in the case
    of [Meltdown and Spectre](https://www.defenseone.com/technology/2018/02/how-long-did-us-government-know-about-spectre-and-meltdown/145776/), coordinators may be in a rush to
    understand the issue while preparing their advisories, leading to
    erroneous or inadequate advice to their constituencies.


## Vulnerability Identifiers

Many vulnerability reports can be similar, and sometimes a vendor or
coordinator might receive multiple reports of similar vulnerabilities at
the same time.
Sometimes this is due to [independent discovery](../../howto/troubleshooting/independent_discovery.md).
Other
times it reflects a report traversing multiple paths to arrive at its
destination within the CVD process. This is fairly common in cases where
a vulnerability affects products from multiple vendors. Using a common
identifier improves coordination as it ensures that all coordinating
parties can keep track of the issue.

!!! example "Common Vulnerability and Exposure (CVE) IDs"

    The most common identifier in use today is the [CVE ID](https://www.cve.org),
    which is
    meant as a globally unique identifier for a public vulnerability report.
    CVE IDs can be obtained from the CVE Project at MITRE or one of several
    [CVE Numbering Authorities](https://www.cve.org/PartnerInformation/ListofPartners)
    (CNAs) established by MITRE&mdash;typically the
    vendors of common software products themselves. Both reporters and
    vendors can request a CVE ID, but reporters should first check if the
    vendor they are coordinating with is already a CNA. This identifier
    should be included in any pre-disclosure shared drafts, so that all
    parties are aware of the common identifier.

!!! warning "ID Assignments Trigger Downstream Workflows"

    Many system deployers use vulnerability scanning tools to discover
    systems on their network that need to have patches applied. In turn,
    many vulnerability scanning tools depend on public vulnerability
    databases such as NVD. Furthermore, NVD entries are largely dependent on
    CVE ID assignments. 

    ```mermaid
    ---
    title: CVE IDs in the Vulnerability Response Flow
    ---
    flowchart LR
        cna[CVE Numbering<br/>Authority]
        cve[CVE ID]
        nvd[National<br/>Vulnerability<br/>Database]
        vst[Vulnerability<br/>Scanning<br/>Tools]
        deployer[System<br/>Deployer]
        cna -->|assigns| cve
        cve -->|ingested by| nvd
        nvd -->|is data source to| vst
        vst -->|scan findings| deployer
        nvd -->|triggers response process| deployer
    ``` 
    
    When vendors issue updates without acquiring CVE IDs
    for the vulnerabilities they address, the patch can go unnoticed by the
    vulnerability databases, scanning tools, and deployers. Therefore we
    strongly recommend that vendors acquire as many vulnerability IDs as
    necessary to clearly indicate which vulnerabilities are fixed by
    specific patches.

!!! warning "Avoid Silent Fixes"

    A **silent fix** occurs when the vendor knows about and fixes the vulnerability 
    but fails to mention the vulnerability's existence in the subsequent release
    notes accompanying the new version. 
    As a result, silent fixes are far less likely to be widely deployed than 
    ones that are clearly described.

!!! warning "Product Versions Should Increment After Fixes"

    A related issue arises when vendors fail to increment their product
    version numbers when issuing a fix for one or more vulnerabilities. This
    makes it much harder for coordinators, vulnerability database providers,
    vulnerability scanning tool vendors, and deployers to differentiate
    systems affected by a vulnerability from those that are not.


## Prepare and Circulate a Draft

Prior to public announcement of a vulnerability document, we find it
helpful to circulate a draft document describing the vulnerability to
give CVD participants an opportunity for discussion and commentary.


At a minimum, a draft advisory should be shared between the reporter and
vendor to reduce the likelihood of either party being taken by surprise.
Ideally, both parties should use this documentation to coordinate how much
information is being released, and what future expectations might exist.
Both parties also have the opportunity to correct erroneous information,
as well as verify that credit for discovering or reporting the
vulnerability is given to the correct person or organization. If
multiple vendors are affected, or there are affected downstream vendors
making use of the vulnerable software, it can be useful to share a draft
with some or all of the affected vendors for even more feedback. Be sure
to also discuss what channels to use for publication and disclosure.

!!! tip "Traffic Light Protocol"

    The Traffic Light Protocol (TLP) may be useful when sharing draft
    information. We discuss applications of TLP to CVD in [OpSec](../../howto/operations/opsec.md).

!!! tip "Vulnerability Disclosure Document"
    
    Examples of vulnerability disclosure documents are provided in the Reference section under [Advisory](../../reference/simple_advisory.md).

