!!! tip "CVD Platforms and Turnkey Services"

    !!! example inline end "CVD Platform Providers"

        Some popular CVD platform providers include:

        - [BugCrowd](https://bugcrowd.com/)
        - [HackerOne](https://www.hackerone.com)
        - [SynAck](https://www.synack.com)
        - [Cobalt](https://cobalt.io/)

    A number of third-party CVD platforms now exist to facilitate
    communication between vendors and reporters. Although
    they are often referred to as bug bounty platforms, the _bounty_
    aspect is in fact optional&mdash;vendors can use CVD platforms to
    receive reports without needing to compensate reporters unless they
    choose to do so. 


    CVD platforms provide a secure communications channel (HTTPS) for
    reporters to communicate with vendors. These platforms generally allow
    two-way communications, making it easy for ongoing discussion between
    vendor and reporter. This channel is usually hosted by a third party in
    a software-as-a-service model, which may be important to some
    organizations that are not able to maintain their own infrastructure due
    to resource constraints. Of course, having vulnerability information
    hosted on third-party infrastructure may also present a data privacy
    risk to some organizations, so it is important to consult internal
    policies before determining if a CVD platform fits your organization's
    needs and requirements.

    !!! example "DoD's Vulnerability Disclosure Program"

        The U.S. Department of Defense (DoD) has a [Vulnerability Disclosure
        Program](https://www.dc3.mil/Missions/Vulnerability-Disclosure/Vulnerability-Disclosure-Program-VDP/)
        (VDP) that uses a [CVD platform](https://hackerone.com/deptofdefense)
        to receive reports from
        security researchers. The DoD VDP is a public program that allows
        security researchers to report vulnerabilities in DoD websites and
        systems. The DoD VDP is a good example of a CVD platform that
        is used to facilitate communication between reporters and vendors,
        even without an explicit bug bounty program. Reporters to the DoD VDP
        are not compensated monetarily for their reports, but they are able to
        gain recognition and reputation points within the CVD platform that can
        lead to future opportunities for paid work.

    !!! note "CVD Platforms and Account Creation"

        An important note regarding these platforms is that the CVD platform by
        its nature requires a login. As explained [previoiusly](./secure_comms.md),
        requiring an account may discourage some reporters or other
        organizations from joining the platform, locking them out of discussion.
        Organizations should consider whether the benefits of using a CVD
        service outweigh this concern.
