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
to respond to an incident when the need arises.

!!! info "CSIRT Resources"

    The Forum of Incident Response and Security Teams (FIRST) created the
    [CSIRT Services Framework](https://www.first.org/standards/frameworks/csirts/csirt_services_framework_v2.1).
    It covers the services that a CSIRT might provide, organized into five service areas:
    Information Security Event Management, Information Security Incident Management,
    Vulnerability Management, Situational Awareness, and Knowledge Transfer.

    Additionally, the CERT Division of the Software Engineering Institute at Carnegie
    Mellon University has created a collection of
    [CSIRT Resources](https://insights.sei.cmu.edu/library/resources-for-creating-a-csirt/).

### CSIRT with National Responsibility

!!! example inline end "National CSIRTs"

    Just a few examples of National CSIRTs include:

    - [CISA](https://www.cisa.gov)
    - [National Cyber Security Centre](https://www.ncsc.gov.uk)
    - [JPCERT/CC](https://www.jpcert.or.jp/english/)
    - [NCSC-NL](https://www.ncsc.nl)

CSIRTs with National Responsibility, also known as, National CSIRTs,
are designated by a country or economy to have specific responsibilities
in cyber protection for the country or economy. A National CSIRT can be
inside or outside of government, but must be specifically recognized by
the government as having responsibility in the country or economy.
In addition to functioning as a clearing house for incident response
across government departments and agencies, CSIRTs with National
Responsibility often have some degree of responsibility or oversight for
coordinating vulnerability response across their nation's critical
infrastructure.

!!! info "National CSIRT Resources"

    The CERT Division has compiled a collection of [National CSIRT Resources](https://insights.sei.cmu.edu/library/natcsirt-resources/).

### Product Security Incident Response Team (PSIRT)

{% include-markdown "../../_includes/_psirt_example.md" %}

Product Security Incident Response Teams (PSIRTs) have
emerged as a specialized form of CSIRT, allowing vendors to focus their
response to product security issues. Although not all vendors have
dedicated PSIRTs, vulnerability response is sufficiently different from
security incident response that larger vendor organizations can usually
justify having a distinct function to deal with it. PSIRTs usually
provide an interface to the outside world to receive vulnerability
reports as well as serving as a central coordinator between internal
departments for the organization's vulnerability response for its
products. When reporting a vulnerability to a vendor, the reporter will
usually be communicating with the vendor's PSIRT.

{% include-markdown "../../_includes/_first_psirt.md" %}

## Security Research Organizations

!!! example inline end "Security Research Organizations"

    Some examples of organizations that might coordinate vulnerabilities they find include

    - managed security service providers
    - government agencies
    - academic research teams
    
    Additionally, vendors of products or services sometimes combine their PSIRT’s vulnerability response
    capability with their externally facing coordination capability.

Organizations that perform security research on other vendors’ products in the course of their
own business sometimes establish their own coordination capability in order to handle the
disclosure process for the vulnerabilities they find. A wide variety of organizations perform this
kind of security research, whether for profit or for non-commercial reasons.

Furthermore, organizations that provide vulnerability management and scanning tools and
services are often well-positioned to act as a disclosure coordinator for the vulnerabilities their
products detect. This applies especially when those vulnerabilities have not already been
disclosed to either the vendor or the public. Alternatively, organizations such as these may
choose to partner with another coordinating organization in order to promote transparency
and reduce the perception of bias in their vulnerability disclosure process.

## Bug Bounty Programs

Many individual vendors have established bug bounty programs to compensate security
researchers for their efforts in discovering vulnerabilities in the vendor’s products. Creation of
a bug bounty program has been noted as an indicator of maturity in vendors’ vulnerability
response efforts.

!!! warning "Bug Bounty Programs and Vulnerability Coordination"

    Bug bounty programs by themselves are not the same as a vulnerability coordination capability.
    Bug bounty programs are a way to incentivize security researchers to report vulnerabilities to the vendor.
    Importantly, they do not inherently create the internal plumbing necessary to respond to those vulnerabilities.
    In some cases, vendor bug bounty programs are enabled by other companies that provide tools and services 
    to facilitate vulnerability coordination.

## Vulnerability Disclosure Platforms and Commercial Brokers

!!! example inline end "Commercial Vulnerability Disclosure Platforms"
    - [BugCrowd](https://www.bugcrowd.com)
    - [HackerOne](https://www.hackerone.com)
    - [SynAck](https://www.synack.com)
    - [Cobalt Labs Inc.](https://cobalt.io/)

Not all vulnerability reporting programs include bug bounties.
In recent years, a new class of coordinator has emerged in the form of commercial vulnerability disclosure
platform providers.

Companies such as those at right offer turnkey solutions for
vendors who want to bootstrap their own vulnerability response program.

## Information Sharing and Analysis Organizations (ISAOs) and Centers (ISACs)

!!! example inline end "ISACs"

    The [National Council of ISACs](https://www.nationalisacs.org/member-isacs-3) lists
    over two dozen ISACs in the United States, each focused on a different sector of critical infrastructure.

[Information Sharing and Analysis Organizations](https://www.isao.org/) (ISAOs) and
[Information Sharing and Analysis Centers](https://www.nationalisacs.org/)
(ISACs) are non-government entities that serve various roles in
gathering, analyzing, and disseminating critical infrastructure
cybersecurity information across private sector organizations of various
sizes and capabilities. These organizations are increasingly involved
in the coordination and deployment of vulnerability mitigations.
Furthermore, we have observed a growing interest from critical
infrastructure sectors engaging with the
coordination of the vulnerability discovery, disclosure, and remediation
processes.

## Traditional Coordinators

!!! example inline end "Third-Party Coordinators"
    - [CERT/CC](https://www.kb.cert.org)
    - [JPCERT/CC](https://www.jpcert.or.jp/english/)
    - [NCSC-NL](https://www.ncsc.nl)
    - [NCSC-FI](https://www.kyberturvallisuuskeskus.fi/en/)

While most CVD programs help address the CVD needs of individual vendors, there still are
vulnerabilities that require larger scale coordination. In particular, Multi-Party Coordinated
Vulnerability Disclosure (MPCVD) remains a challenge for many organizations.
As individual
vendors have become more mature in their handling of vulnerabilities in their products, the
role of MPCVD has increased in importance for more traditional vulnerability coordinators.
