# Coordinator

Complicated or complex CVD cases can often benefit from the help of a
coordinator. A coordinator acts as a relay or information broker between
other stakeholders. Several types of coordinators with slightly
different roles and domains exist. We list a few here.

## Computer Security Incident Response Team (CSIRT)

A Computer Security Incident Response Team (CSIRT) is a service
organization that is responsible for receiving, reviewing, and
responding to computer security incident reports and activity. Their
services are usually performed for a defined constituency that could be
a parent entity such as a corporate, governmental, or educational
organization; a region or country; a research network; or a paid client.
A CSIRT can be a formalized team or an ad-hoc team. A formalized team
performs incident response work as its major job function. An ad-hoc
team is called together during an ongoing computer security incident or
to respond to an incident when the need arises
\[1\].

### CSIRT with National Responsibility

CSIRTs with National Responsibility, also known as, National CSIRTs,
are designated by a country or economy to have specific responsibilities
in cyber protection for the country or economy. A National CSIRT can be
inside or outside of government, but must be specifically recognized by
the government as having responsibility in the country or economy \[2\].
In addition to functioning as a clearing house for incident response
across government departments and agencies, CSIRTs with National
Responsibility often have some degree of responsibility or oversight for
coordinating vulnerability response across their nation's critical
infrastructure. US-CERT, part of the Department of Homeland Security,
has been designated as the national CSIRT for the United States. We
maintain a list of National CSIRTS on the CERT website
\[3\].]

### Product Security Incident Response Team (PSIRT)

Over time, Product Security Incident Response Teams (PSIRTs) have
emerged as a specialized form of CSIRT, allowing vendors to focus their
response to product security issues. Although not all vendors have
dedicated PSIRTs, vulnerability response is sufficiently different from
security incident response that larger vendor organizations can usually
justify having a distinct function to deal with it. PSIRTs usually
provide an interface to the outside world to receive vulnerability
reports as well as serving as a central coordinator between internal
departments for the organization's vulnerability response for its
products. When reporting a vulnerability to a vendor, the reporter will
usually be communicating with the vendor's PSIRT. For example, Cisco,
Oracle, Intel, Microsoft, Apple, Adobe, and others have established
internal PSIRTs. Many PSIRTs participate in the Forum for Incident
Response and Security Teams
\[4\].

## Security Research Organizations

Organizations that perform security research on other vendors’ products in the course of their
own business sometimes establish their own coordination capability in order to handle the dis-
closure process for the vulnerabilities they find. A wide variety of organizations perform this
kind of security research, whether for profit or for non-commercial reasons. Some examples in-
clude managed security service providers, government agencies, and academic research teams.
Some of these organizations are vendors of products or services themselves, and combine their
PSIRT’s vulnerability response capability with their externally facing coordination capability.
Furthermore, organizations that provide vulnerability management and scanning tools and
services are often well-positioned to act as a disclosure coordinator for the vulnerabilities their
products detect. This applies especially when those vulnerabilities have not already been
disclosed to either the vendor or the public. Alternatively, organizations such as these may
choose to partner with another coordinating organization in order to promote transparency
and reduce the perception of bias in their vulnerability disclosure process.

## Bug Bounty Programs

Many individual vendors have established bug bounty programs to compensate security re-
searchers for their efforts in discovering vulnerabilities in the vendor’s products. Creation of
a bug bounty program has been noted as an indicator of maturity in vendors’ vulnerability
response efforts.

However, bug bounty programs by themselves are not the same as a vulnerability coordination capability.
Bug bounty programs are a way to incentivize security researchers to report vulnerabilities to
the vendor. Importantly, they do not inherently create the internal plumbing necessary to
respond to those vulnerabilities.
In some cases, vendor bug bounty programs are enabled by other companies that provide tools
and services to facilitate vulnerability coordination.

## CVD Platforms and Commercial Brokers

Not all vulnerability reporting programs include bug bounties. In recent years, a new class of
coordinator has emerged in the form of commercial CVD platform providers. Companies such
as {== BugCrowd, HackerOne, Synack, and Cobalt ==} offer turnkey solutions for
vendors who want to bootstrap their own vulnerability response program.

## Information Sharing and Analysis Organizations (ISAOs) and Centers (ISACs)

Information Sharing and Analysis Organizations (ISAOs) and Centers
(ISACs) are non-government entities that serve various roles in
gathering, analyzing, and disseminating critical infrastructure
cybersecurity information across private sector organizations of various
sizes and capabilities \[13,14\]. These organizations have only begun to
emerge in earnest within the past few years, but they are already
actively involved in the coordination and deployment of vulnerability
mitigations. Furthermore, it seems likely that some number of critical
infrastructure sectors will need to become involved further in the
coordination of the vulnerability discovery, disclosure, and remediation
processes.

## Traditional Coordinators

While most CVD programs help address the CVD needs of individual vendors, there still are
vulnerabilities that require larger scale coordination. In particular, Multi-Party Coordinated
Vulnerability Disclosure (MPCVD) remains a challenge for many organizations. As individual
vendors have become more mature in their handling of vulnerabilities in their products, the
role of MPCVD has increased in importance for more traditional vulnerability coordinators
such as the {== CERT/CC [26], NCSC-NL [21], NCSC-FI [110], and JPCERT/CC ==}.

### References

1. [CERT Division, "CSIRT Frequently Asked Questions (FAQ)," Software
    Engineering Institute, \[Online\]. Available:
    [https://www.cert.org/incident-management/csirt-development/csirt-faq.cfm](https://www.cert.org/incident-management/csirt-development/csirt-faq.cfm)? \[Accessed 16 May
    2017\].]2.  [CERT Division, "Incident Management: Resources for National
    CSIRTs," Software Engineering Institute, \[Online\]. Available:
    [https://www.cert.org/incident-management/national-csirts/index.cfm](https://www.cert.org/incident-management/national-csirts/index.cfm). \[Accessed 16 May
    2017\].]3.  [CERT, "List of National CSIRTs," \[Online\]. Available:
    [https://www.cert.org/incident-management/national-csirts/national-csirts.cfm](https://www.cert.org/incident-management/national-csirts/national-csirts.cfm). \[Accessed 23 May
    2017\].]4.  [BugCrowd, "BugCrowd," \[Online\]. Available:
    [https://bugcrowd.com/](https://bugcrowd.com/). \[Accessed 23 May
    2017\].]5.  [FIRST, "FIRST Teams," \[Online\]. Available:
    [https://www.first.org/members/teams](https://www.first.org/members/teams). \[Accessed 16 May
    2017\].]6.  [BugCrowd, "BugCrowd," \[Online\]. Available:
    [https://bugcrowd.com/](https://bugcrowd.com/). \[Accessed 23 May
    2017\].]7.  [HackerOne, "HackerOne," \[Online\]. Available:
    [https://www.hackerone.com](https://www.hackerone.com). \[Accessed 23 May
    2017\].]8.  [SynAck, "SynAck," \[Online\]. Available:
    [https://www.synack.com](https://www.synack.com). \[Accessed 23 May
    2017\].]9.  [Cobalt Labs Inc., "Cobalt," \[Online\]. Available:
    [https://cobalt.io/](https://cobalt.io/). \[Accessed 23 May
    2017\].]10. [CERT, "Vulnerability Analysis," \[Online\]. Available:
    [https://www.cert.org/vulnerability-analysis/](https://www.cert.org/vulnerability-analysis/). \[Accessed 23 May
    2017\].]11. [National Cyber Security Centre Netherlands, "NCSC-NL,"
    \[Online\]. Available:
    [https://www.ncsc.nl/english](https://www.ncsc.nl/english). \[Accessed 23 May
    2017\].]12. [NCSC-FI, "Finnish Communications Regulatory Authority / National
    Cyber Security Centre Finland," \[Online\]. Available:
    [https://www.viestintavirasto.fi/en/cybersecurity.html](https://www.viestintavirasto.fi/en/cybersecurity.md).]13. [JPCERT/CC, "Japan Computer Emergency Response Team Coordination
    Center," \[Online\]. Available:
    [https://www.jpcert.or.jp/english/](https://www.jpcert.or.jp/english/). \[Accessed 16 May
    2017\].]14. [U.S. Department of Homeland Security, "Information Sharing and
    Analysis Organizations (ISAOs)," \[Online\]. Available:
    [https://www.dhs.gov/isao](https://www.dhs.gov/isao). \[Accessed 23 May
    2017\].]15. [National Council of ISACs, "National Council of ISACs,"
    \[Online\]. Available:
    [https://www.nationalisacs.org/](https://www.nationalisacs.org/). \[Accessed 23 May
    2017\].]
