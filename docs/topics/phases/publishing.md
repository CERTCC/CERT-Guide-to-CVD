# Publishing

Once the draft circulation phase is complete, the next step is
publishing the vulnerability document to whatever channels have been
identified during previous phases.

Some vendors have a specific website that lists all their security
advisories to date. Others might email the disclosure to a user mailing
list or a security mailing list such as Full Disclosure \[2\] or BugTraq
\[1\]. Reporters themselves may also chose to disclose by posting the
advisory to a mailing list or including it in a personal or company
blog. A common goal for reporters in the CVD process is to synchronize
their publication with the vendor's response. As a result,
near-simultaneous publication occurs quite often.

It is generally courteous for the vendor and reporter to contact each
other after disclosure to inform one another that the disclosure went
through as planned and provide URLs to the published
documents.]

## Vulnerability Identifiers

!!! info inline end "ID Assignments Trigger Downstream Workflows"

    Many system deployers use vulnerability scanning tools to discover
    systems on their network that need to have patches applied. In turn,
    many vulnerability scanning tools depend on public vulnerability
    databases such as NVD. Furthermore, NVD entries are largely dependent on
    CVE ID assignments. 

    ```mermaid
    ---
    title: CVE IDs in the Vulnerability Response Flow
    ---
    flowchart TD
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

Many vulnerability reports can be similar, and sometimes a vendor or
coordinator might receive multiple reports of similar vulnerabilities at
the same time.
Sometimes this is due to [independent discovery](../../tutorials/troubleshooting/independent_discovery.md).
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


## Product Versioning

A related issue arises when vendors fail to increment their product
version numbers when issuing a fix for one or more vulnerabilities. This
makes it much harder for coordinators, vulnerability database providers,
vulnerability scanning tool vendors, and deployers to differentiate
systems affected by a vulnerability from those that are not.


## Where to Publish


Publicly disclosing the existence of a vulnerability and the
availability of its fix is usually considered to be the primary goal of
the CVD process.

!!! note inline end "Public Information is not the Same as Publicity"

    Information about a vulnerability can be _available_ to the public without it being _publicized_.
    Examples include:
    
    - A commit comment in a code repository for an open source project might indicate that a vulnerability has been fixed
    - An exploit might be made available on a public web site without being associated with a vulnerability ID or patch release
    - A binary diff of two released versions of the same software can be sufficient for an analyst to recognize that a vulnerability was fixed

    In each of these cases, the existence of the vulnerability should be considered to be public information, 
    but these fall short of being considered *publicized*.
    If the goal of the CVD process is for the fixes for vulnerable software to be *deployed*,
    then simply making the information public is insufficient -- it must be *publicized*.


Vendors will often provide vulnerability information:

-   On the vendor's public website. Many vendors offer a
    security-focused section within the support section of their online
    offerings.
-   To a public mailing list or a vendor-specific list
    

Vendors of bespoke software or products with highly focused customer
bases are sometimes reasonably confident that they can reach their
affected users directly. 

These vendors often publish vulnerability and fix information:

-   On a customer-only site
-   Via a customer support mailing list
-   By individually notifying customers, for example through the
    technical sales channel



However, even with a well-organized customer contact database, it can be
difficult for a vendor to be certain that all relevant decision makers
are reached in a timely manner. Hence, we recommend that vendors publish
at least basic vulnerability and fix announcements to their public
website in addition to whatever direct customer contact communications
they provide.

## References

1.  Security Focus, "BugTraq Archive," \[Online\].
    Available: [http://www.securityfocus.com/archive/1](http://www.securityfocus.com/archive/1). \[Accessed 23 May 2017\].
2.  [Seclists.org](http://seclists.org/),
    "Full Disclosure Mailing List," \[Online\].
    Available: [http://seclists.org/fulldisclosure/](http://seclists.org/fulldisclosure/). \[Accessed 23 May 2017\].
5.  Sharwood, Simon. "Intel didn't tell CERTS, govs, about Meltdown
    and Spectre because they couldn't help fix it." 23 February
    2018. [https://www.theregister.co.uk/2018/02/23/meltdown_spectre_letters_to_congress/](https://www.theregister.co.uk/2018/02/23/meltdown_spectre_letters_to_congress/)



