# Finder

!!! quote "ISO/IEC 29147:2014"

    Finder: individual or organization that identifies a potential
    vulnerability in a product or online service. Note that finders can be researchers, security companies, users, 
    governments, or coordinators.

In the interest of consistency, we will use this
definition of finder, although in other documentation we've used the
term discoverer for this same role. We do, however, distinguish between
the role of finder and the role of reporter, as seen in this section and
the next.

## Who Finds Vulnerabilities?

Vulnerabilities can be found by just about anyone. All it takes is for
someone to notice an unexpected or surprising behavior of a system.
Although it is common for independent security researchers to hunt
vulnerabilities as either a hobby or profession, finders need not
self-identify as security researchers or hackers.

!!! example "Vulnerabilities have been found by people of many backgrounds"

    - students and professional academics studying novel ways to exploit
    systems or protocols
    - open source developers who notice that a software bug has security
    implications
    - system administrators who recognize a vulnerability during the
    course of troubleshooting a system error
    - professional security analysts who observe a previously unknown
    product vulnerability while testing an organization's
    infrastructure during a penetration test engagement
    - people using software or web services who mistyped some input or
    simply clicked on the wrong thing
    - children who like to press buttons. A [BBC article](http://www.bbc.com/news/technology-26879185)
    describes how a 5-year old found a vulnerability in
    Microsoft's Xbox Live service just by holding down the space bar
    and was able to log in to his father's account without the password.


There are also organizations that look for vulnerabilities. Some of them
work under contract to vendors directly. Some work for the vendors'
customers who deploy the software. And some have independent motivation
to find vulnerabilities, perhaps to demonstrate their competence in
finding vulnerabilities in the interest of their security consulting
practice's business development.

Furthermore, vendors may choose to look for vulnerabilities in their own
products&mdash;a practice that we strongly encourage. This can be done via

- in-house expertise and testing
- contracted security testing
- solicited on a per-vulnerability basis using a bug bounty program

!!! example "Vendors Integrate Testing for Vulnerabilities into Development"

    Many vendors integrate testing for vulnerabilities into their development process.
    Microsoft, for example, includes static, dynamic,
    and fuzz testing for vulnerabilities in its phases of the [Security
    Development Lifecycle](https://www.microsoft.com/en-us/sdl/).
    The [Building Security In Maturity Model](https://www.bsimm.com/framework/) (BSIMM)
    suggests that many vendors in various industries already employ techniques in architecture
    analysis, code review, and security testing to find vulnerabilities as
    part of their development cycle.

### What Happens After a Vulnerability is Found?

!!! example inline end "First Steps After Finding a Vulnerability"

    The following flowchart illustrates the process of finding a
    vulnerability and the subsequent steps that might be taken.

    ```mermaid
    flowchart TD
        start([Vulnerability Found])
        compose_report[1. Compose a vulnerability report]
        provide_report[2. Provide the report to someone]
        prepare_document[3. Prepare & Publish]
        start --> compose_report
        compose_report --> provide_report
        provide_report -.->|optional| prepare_document
    
    ```

Regardless of who finds a vulnerability, there are a few common events
that follow the discovery:

1. The finder composes a vulnerability report, as discussed in [Reporting](../phases/reporting.md)
2. The finder (or reporter, if these are distinct individuals) provides
    that report to someone. Often the vulnerability report would be
    provided to the [vendor](vendor.md), but that's not always the case. Sometimes
    the report might be sent to a [coordinator](coordinator.md). If the vulnerability is
    discovered internally to a vendor, then the report may simply be
    forwarded to the responsible team within the organization&mdash;for
    example, filed as a security-related bug report. 
3. (Optional) Finders, reporters, vendors, or coordinators might
    [prepare a document to publish](../phases/public_awareness.md). The finder often wants to draw
    attention to his or her discovery and subsequent analysis by
    publishing a document, blog post, or conference presentation, to
    share the findings with a larger audience. Vendors typically want to
    publish a document as well to inform their users that action has
    been taken to resolve the problem, and to prompt their users to take
    any required remediation actions.


!!! tip "Regarding Non-Disclosure"

    It is of course [possible](../../howto/preparation/disclosure_choices.md) for a finder to find a vulnerability and tell
    no one. However, in that case there is no disclosure involved so we do
    not address that scenario further in this documentation.

## Reporter

The defining characteristic of vulnerability *reporters* is that they
originate the message that informs a vendor or coordinator of a
vulnerability.

!!! example "When the finder is not the reporter"

    In most cases, the *reporter* is also the [*finder*](finder.md) of the
    vulnerability. However, this is not always the case. For example, the
    finder might be an employee at an organization that also has in-house
    vulnerability coordinators who act as the communications liaison with
    the affected vendor(s).

    Alternatively, it could be that someone analyzing a piece of malware
    realized that it exploited a previously undisclosed vulnerability. In
    both cases, the party communicating the vulnerability information to the
    vendor is not the original finder.

That said, whether or not the
reporter is the original finder is often not as relevant as whether the
newly provided information is sufficient to determine the existence and
impact of the problem reported.


