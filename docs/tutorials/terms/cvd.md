# Coordinated Vulnerability Disclosure

!!! abstract "Coordinated Vulnerability Disclosure"

    Coordinated Vulnerability Disclosure is the process of gathering
    information from vulnerability finders, coordinating the sharing of that
    information between relevant stakeholders, and disclosing the existence
    of software vulnerabilities and their mitigations to various
    stakeholders, including the public. 

CVD is an important aspect of any successful [Vulnerability Response](vulnerability_response.md) (VR) process.
CVD inputs are [vulnerability reports](../../topics/phases/reporting.md) arising from [vulnerability discovery](vulnerability_discovery.md) practices.
CVD outputs for [product](products_instances.md) vulnerabilities (software or hardware) usually include fixes or mitigation advice as well
as [vulnerability report documents](../../topics/phases/publishing.md) or vulnerability database records, typically with some formal identifier
(e.g.,
[CVE](https://www.cve.org),
[VU#](https://www.kb.cert.org/vuls),
[BID](https://en.wikipedia.org/wiki/Bugtraq)).

!!! tip "CVD is not exclusive to software product vulnerabilities"

    Many operational ([instance](products_instances.md)) vulnerabilities such as router misconfigurations, website
    vulnerabilities, or cloud service problems can be fixed in situ by the [vendor](../../topics/roles/vendor.md),
    who as the operator of the service or instance, also acts as the [deployer](../../topics/roles/deployer.md).
    Althouth it is less common for these types of vulnerabilities to be disclosed publicly, they can
    still be addressed through a CVD process.
    Often these vulnerabilities are reported to the deployer directly, possibly as part of a Vulnerability Disclosure Program (VDP).

[ISO/IEC 29147](https://www.iso.org/standard/72311.html) defines Vulnerability Disclosure as follows:

!!! quote "ISO/IEC 29147:2014 Information technology&mdash;Security techniques&mdash;Vulnerability disclosure"

    Vulnerability disclosure is a process through which vendors and
    vulnerability finders may work cooperatively in finding solutions that
    reduce the risks associated with a vulnerability. It encompasses
    actions such as reporting, coordinating, and publishing information
    about a vulnerability and its resolution.

    The goals of vulnerability disclosure include the following: a)
    ensuring that identified vulnerabilities are addressed; b) minimizing
    the risk from vulnerabilities; c) providing users with sufficient
    information to evaluate risks from vulnerabilities to their systems;

The stakeholders&mdash;in other words, the people who care about the
existence of a vulnerability&mdash;vary on a case by case basis, but
typically include those below:

- the [reporter](../../topics/roles/finder.md) or [finder](../../topics/roles/finder.md) of the vulnerability (often an independent
    security researcher)
- the [vendor](../../topics/roles/vendor.md) (developer) of the component that contains the
    vulnerability (See also *originating vendor* in [MPCVD](../../howto/coordination/mpcvd.md))
- [vendors](../../topics/roles/vendor.md) that utilize the component containing the vulnerability in
    their own products (See also *downstream vendors* in [MPCVD](../../howto/coordination/mpcvd.md))
- [coordinators](../../topics/roles/coordinator.md), vulnerability databases, or other organizations that
    specialize in incident response and vulnerability handling
- [deployers](../../topics/roles/deployer.md) and the general public / consumers who purchase and use products containing the vulnerable component

Disclosure, in turn, is the process by which information about a
vulnerability (ideally with advice for mitigating or fixing it) is
released to consumers of the product, and more generally, the public at
large. *There is no single "right" way to do this.* Sometimes,
vulnerability information is disclosed in a blog post by the finder of
the vulnerability, or emailed to a security mailing list. Sometimes the
vendor issues a security advisory to its customers or to the public. At
the CERT/CC, we publish [Vulnerability Notes](https://www.kb.cert.org/vuls) on our website, often in
parallel with other parties (i.e., the finder of the vulnerability
and/or the vendor of the vulnerable product).

!!! tip "Opinions Differ on Disclosure"

    A lack of agreement within the security community persists
    on whether, and under what conditions, vulnerability information should
    be disclosed to vendors, other stakeholders, and the public.
    Different people sometimes hold strongly differing opinions
    about the disclosure of software vulnerabilities. These differences tend
    to center on the timing of a vulnerability report's release, the type
    and degree of details included, and the audience to whom the report is
    provided.
    
    As a result, the character of information in a vulnerability report can
    vary greatly. Some reports only warn of a general vulnerability in a
    specific product. Others are more detailed and provide actual examples
    of how to attack the flaw (these examples are called "proof of concept
    code," often shortened to "PoC").

It is worth reiterating that disclosure is not a [singular event](../cvd_is_a_process.md) even for
a single vulnerability. For more on the different phases of the CVD process,
see [Phases](../../topics/phases/index.md).

!!! question "Who is *Responsible* Here?"

    You may be familiar with the term [*responsible disclosure*](https://datatracker.ietf.org/doc/draft-christey-wysopal-vuln-disclosure/)
    and
    wonder how it's different from CVD. The history of *responsible
    disclosure* makes for a long story best told over adult beverages at a
    hotel bar during a security conference, so we won't go into it here.
    Without belaboring the topic, the sticking point comes down to the fact
    that what constitutes _responsible_ behavior is a matter of opinion
    that is always framed within the values of whoever is using the term.

    The vendors cry, "Disclosing a vulnerability without an available patch
    is not responsible!" "Not fixing this vulnerability quicker is not
    responsible!" the finders retort. Meanwhile, the deployer asks,
    "Who's responsible for fixing this?" while knowing the answer all too
    well.

    ```mermaid
    sequenceDiagram
        actor F as Finder
        actor V as Vendor
        actor D as Deployer
        
        V ->> F: Disclosure<br/>without a patch<br/>is irresponsible!
        F ->> V: Not fixing<br/>this vulnerability quicker<br/>is irresponsible!
        D ->> D: Who's responsible<br/>for fixing this?
    ```

    Because of the inherent value judgement and lack of agreement on
    its definition, the CERT/CC, along with [numerous](https://www.microsoft.com/en-us/msrc/cvd)
    [other](https://www.cisa.gov/coordinated-vulnerability-disclosure-process)
    [organizations](https://www.enisa.europa.eu/news/enisa-news/coordinated-vulnerability-disclosure-policies-in-the-eu),
    advocates for the use of the term *Coordinated Vulnerability Disclosure
    (CVD)* to reduce misunderstanding and promote cooperation.
