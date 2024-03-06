# Reporting

Anyone who becomes aware of a vulnerability that does not appear to have
been remediated should report the vulnerability to the vendor. One
should not assume that a vendor is aware of a specific vulnerability
unless it has already been publicly reported, whether by the vendor or
elsewhere. The easier it is to report vulnerabilities to a vendor, the
less likely that the vendor will be surprised by vulnerability reports
disclosed directly to the public.

!!! tip "Advice for Reporters"

    **Providing Useful Information**
    
    Reporting a vulnerability requires that the vulnerability is
    well-documented. This typically means providing the following
    information:

    -   The exact product version(s) affected
    -   A description of how the vulnerability was discovered (including
    what tools were used) or what you were doing when you encountered
    the vulnerability
    -   Proof of concept (PoC) code or reproduction instructions
    demonstrating how the vulnerability might be exploited
    -   Ideally, a suggested patch or remediation action if the reporter is
    aware of how to fix the vulnerability
    -   Description of the impact of the vulnerability and attack scenario
    (Kymberlee Price discusses the importance of providing a clear
    attack scenario in her article \[2\]).
    -   Any time constraints (for example, give a date of publication or
    presentation at a conference if you know)

    Reporters that do not provide enough information to a vendor or
    coordinator may find their reports delayed or even rejected. Using CWE
    \[3\] or CAPEC \[4\] as a reference might be helpful to describe the
    type of vulnerability you have found and common ways to fix it the
    problem.

An example of a template for a vulnerability report, based on the
CERT/CC's own Vulnerability Reporting Form (VRF) \[5\], is provided
in [Appendix
D](/confluence/pages/createpage.action?spaceKey=CVD&title=Appendix+D+%E2%80%93+Sample+Vulnerability+Disclosure+Document&linkCreation=true&fromPageId=47677468){.createlink}.
Vendors that require additional information to validate reports should
clearly document their specific requirements in their vulnerability
disclosure policy, reporting form, or process description.

!!! tip "Advice for Vendors"

    Vendors need a mechanism to receive vulnerability reports from others.
    This reporting mechanism should be easy enough to use that it encourages
    rather than discourages reports. It can be as simple as a dedicated
    email address for reporting security issues, a secure web form, or a bug
    bounty program. Aside from the technical aspects of encouraging
    reporting, vendors can also provide reporters with other incentives, as
    discussed
    in [Section ](2.4.-Incentivize-Desired-Behavior_47677454.md)[2.4](2.4.-Incentivize-Desired-Behavior_47677454.md).

### Create Secure Channels for Reporting

Whether you are a vendor or a coordinator, you need to have open
channels for communication with vulnerability finders and reporters. In
our experience, the most common means of communication is email. For
this reason, the CERT/CC recommends that vendors establish a specific
and well-publicized email alias such as \<<security@example.com>\> solely
for receipt of vulnerability reports.

However, since email is an insecure communications channel by default,
many vendors, reporters, and coordinators prefer to use encrypted mail
instead. Although x.509 encrypted mail exists, we have found
PGP-compatible tools such as GnuPG to be more widely used by CVD
participants. Vendors are encouraged to create and publish a PGP key
affiliated with the security email alias to allow the confidentiality of
sensitive reports to be maintained in transit.

{== TODO revise the following ==}

{== PGP / GnuPG, never popular outside of the infosec community, has been falling out of
favor. Critiques abound: <https://blog.cryptographyengineering.com/2014/08/13/>
whats-matter-with-pgp/ <https://moxie.org/2015/02/24/gpg-and-me.html> https:
//arstechnica.com/information-technology/2016/12/op-ed-im-giving-up-on-pgp/
Common complaints (summarize the above)...Nobody gets it right.
PGP-based operations are hard to manage at scale.
There are many ways to make mistakes with PGP, and the consequences of those mistakes can be severe.
Consider the threat: who are you trying to protect against?
Further problem: CVD is often a process requiring the interaction of teams of individuals
from different organizations. Encrypted email was designed more as a way of enabling in-
dividuals to communicate directly with each other. But what happens in team situations is
that the team usually has a single key. So everyone outside the team encrypts to that one
key. But on the receiving side the encrypted email is often decrypted and forwarded as plain
text with in the team. So in essence the email encryption is just serving as transport en-
cryption rather than end-to-end from sender mail client to receiver mail client. But other
technology like StartTLS already enables transport encryption. So what are we gaining by
encrypting the content? ==}

Alternatively, some vendors choose to offer a web form specifically for
receiving reports of security-related issues. Such forms can then
deliver the report directly to your security or engineering team. The
CERT/CC discourages reliance on general "Contact Us" web forms that
pass through an organization's communications or customer support
teams. Many finders will balk at having to get past these nontechnical
interfaces into the vendor. In addition, security messages often must be
triaged and processed differently than other incoming contacts.

Another possibility is to make use of a third-party bug bounty or
coordination platform. For more information on common CVD tools, see
{== TODO fixme [Section 7](7.-Operational-Considerations_47677492.md) ==}.

{== TODO We should maybe make a more concrete positive recommendation: If you’re starting a new
CVD program now, focus on encrypted transport + strong authentication. E.g., VINCE.
Don’t build a new process around PGP email. ==}

## References

1. Wassermann, Garrett. *Reach Out and Mail Someone.*6 August
    2015. [https://insights.sei.cmu.edu/cert/2015/08/reach-out-and-mail-someone.html](https://insights.sei.cmu.edu/cert/2015/08/reach-out-and-mail-someone.md)
2. K. Price, "Writing a bug report - Attack Scenario and Impact are
    key!" 2 August 2015. \[Online\].
    Available: [https://forum.bugcrowd.com/t/writing-a-bug-report-attack-scenario-and-impact-are-key/640](https://forum.bugcrowd.com/t/writing-a-bug-report-attack-scenario-and-impact-are-key/640). \[Accessed 17 May 2017\].
3. MITRE, "Common Weakness Enumeration (CWE)," \[Online\].
    Available: [https://cwe.mitre.org/](https://cwe.mitre.org/). \[Accessed 17 May 2017\].
4. MITRE, "Common Attack Pattern Enumeration and Classification,"
    \[Online\].
    Available: [https://capec.mitre.org/](https://capec.mitre.org/). \[Accessed 17 May 2017\].
5. CERT/CC, "Vulnerability Reporting Form," \[Online\].
    Available: [https://vulcoord.cert.org/VulReport/](https://vulcoord.cert.org/VulReport/). \[Accessed 17 May 2017\].

[
]
