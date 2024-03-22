# Tools of the Trade

An organization's capabilities are supported by people, process, and
tools, and CVD is no different. This section covers some commonly used
tools.

[Secure communications channels](secure_comms.md)


## Bug Bounty Platforms

[ A number of third-party CVD platforms now exist to facilitate
communication between vendors and reporters \[11,12,13,14\]. Although
they are often referred to as bug bounty platforms, often the "bounty"
aspect is in fact optional&mdash;vendors can use bug bounty platforms to
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

An important note regarding these platforms is that the CVD platform by
its nature requires a login. As explained in our discussion in the last
section, requiring an account may discourage some reporters or other
organizations from joining the platform, locking them out of discussion.
Organizations should consider whether the benefits of using a CVD
service outweigh this
concern.]


## Code and System Inventories

As we discussed in [Section 5.4](5.4-Multiparty-CVD_47677477.md),
software-based products are typically assembled from components rather
than written from scratch. Economies of scale apply to code, and most
organizations would consider it wasteful to write a feature from scratch
when that feature is available at a reasonable licensing cost for
inclusion into their own products. As a result, each product is not
merely the result of a single vendor's development process, but of an
entire supply chain. Libraries get included in other libraries, which
form subcomponents in the composition of larger and more complex
products.

For product vendors, an important part of the vulnerability response
process is knowing what weaknesses your products might have. You can
address this by clearly identifying any third-party libraries or
utilities that are included with your products, and being alert and
responsive to vulnerability disclosures in any third-party products that
may affect your own
products.

In recent years, a class of Software Composition Analysis tools (such
as those offered by WhiteSource Software \[15\], Black Duck Software
\[16\], Sonatype \[17\], Synopsys \[18\], Flexera Software \[19\], and
the like) have come into use to identify potential licensing conflicts
in commercial and open source products. Many of these tools are
potentially useful to vendors looking to create an inventory of
libraries and third-party components used in their products for security
analysis purposes as
well.

As a vendor, identifying your products' third-party dependencies is
only the first step. After that, you should take steps to ensure that
your vulnerability response capability maintains awareness of any
security-related announcements about those upstream products on which
your product depends. Some component vendors offer special communication
channels (e.g., a mailing list) for their licensees. If you've worked
with a coordinator like the CERT/CC in the past, ask if you can be
placed in a special notification list for a particular library or
product.

Furthermore, since it is likely that your products will in turn be used
as components in some other vendors' solution, it can be a good
practice to provide an inventory of components along with your product.
A number of data formats and specifications have emerged in the software
supply chain management space and are in use by product vendors already.

These include the following

- Software Identification (SWID) Tags \cite{nist2018swid}
- Common Platform Enumeration (CPE) \cite{nist2016cpe}
- The Software Package Data Exchange (SPDX) \cite{spdx}

## References

1. [N. Brownlee and E. Guttman, "Expectations for Computer Security
    Incident Response," The Internet Society,
    1998.]2.  [CERT/CC, "Sending Sensitive Information," \[Online\]. Available:
    [https://www.cert.org/contact/sensitive-information.cfm](https://www.cert.org/contact/sensitive-information.cfm). \[Accessed 24 May
    2017\].]3.  [Symantec, "Symantec Desktop Email Encryption," \[Online\].
    Available:
    [https://www.symantec.com/products/information-protection/encryption/desktop-email-encryption](https://www.symantec.com/products/information-protection/encryption/desktop-email-encryption). \[Accessed 24 May
    2017\].]4.  [The GnuPG Project, "GNU Privacy Guard," \[Online\]. Available:
    [https://gnupg.org/](https://gnupg.org/). \[Accessed 24 May
    2017\].]5.  [B. Ramsdell and S. Turner, "RFC 5751 Secure/Multipurpose Internet
    Mail Extensions (S/MIME) Version 3.2 Message Specification,"
    January 2010. \[Online\]. Available:
    [https://tools.ietf.org/html/rfc5751](https://tools.ietf.org/html/rfc5751). \[Accessed 24 May
    2017\].]6.  [Internet Security Research Group (ISRG), "Let's Encrypt,"
    \[Online\]. Available:
    [https://letsencrypt.org/](https://letsencrypt.org/). \[Accessed 16 May
    2017\].]7.  [The Enigmail Project, "Enigmail," \[Online\]. Available:
    [https://www.enigmail.net/index.php/en/](https://www.enigmail.net/index.php/en/). \[Accessed 24 May
    2017\].]8.  [Gpg4win Initiative, "GNU Privacy Guard for Windows," \[Online\].
    Available:
    [https://www.gpg4win.org/](https://www.gpg4win.org/). \[Accessed 24 May
    2017\].]9.  ["KGpg," \[Online\]. Available:
    [https://utils.kde.org/projects/kgpg/](https://utils.kde.org/projects/kgpg/). \[Accessed 24 May
    2017\].]10. [G. Wassermann, "Reach Out and Mail Someone," 6 August 2015.
    \[Online\]. Available:
    [https://insights.sei.cmu.edu/cert/2015/08/reach-out-and-mail-someone.html](https://insights.sei.cmu.edu/cert/2015/08/reach-out-and-mail-someone.md). \[Accessed 24 May
    2017\]]11. [BugCrowd, "BugCrowd," \[Online\]. Available:
    [https://bugcrowd.com/](https://bugcrowd.com/). \[Accessed 23 May
    2017\].]12. [HackerOne, "HackerOne," \[Online\]. Available:
    [https://www.hackerone.com](https://www.hackerone.com). \[Accessed 23 May
    2017\].]13. [SynAck, "SynAck," \[Online\]. Available:
    [https://www.synack.com](https://www.synack.com). \[Accessed 23 May
    2017\].]14. [Cobalt Labs Inc., "Cobalt," \[Online\]. Available:
    [https://cobalt.io/](https://cobalt.io/). \[Accessed 23 May
    2017\].]15. [["White Source Software," \[Online\]. Available:
    [https://www.whitesourcesoftware.com/](https://www.whitesourcesoftware.com/). \[Accessed 24 May
    2017\].]    ]16. ["Black Duck Software," \[Online\]. Available:
    [https://www.blackducksoftware.com](https://www.blackducksoftware.com). \[Accessed 24 May
    2017\].]17. ["Sonatype," \[Online\]. Available:
    [https://www.sonatype.com/](https://www.sonatype.com/). \[Accessed 24 May
    2017\].]18. ["Synopsis," \[Online\]. Available:
    [https://www.synopsys.com/](https://www.synopsys.com/). \[Accessed 24 May
    2017\].]19. ["Flexera Software," \[Online\]. Available:
    [https://www.flexerasoftware.com/](https://www.flexerasoftware.com/). \[Accessed 24 May
    2017\].]20. [[TagVault.org](http://TagVault.org),
    "SWID Tags," \[Online\]. Available:
    [http://tagvault.org/swid-tags/](http://tagvault.org/swid-tags/). \[Accessed 16 May
    2017\].]21. [National Institute of Standards and Technology, "Common Platform
    Enumeration (CPE)," \[Online\]. Available:
    [https://scap.nist.gov/specifications/cpe/](https://scap.nist.gov/specifications/cpe/) \[Accessed 16 May
    2017\].]22. [SPDX Workgroup, "Software Package Data Exchange," \[Online\].
    Available: [https://spdx.org/](https://spdx.org/) . \[Accessed 16 May
    2017\].]23. [CERT, "Dranzer," \[Online\]. Available:
    [https://vuls.cert.org/confluence/display/tools/Dranzer](https://vuls.cert.org/confluence/display/tools/Dranzer){rel="nofollow"}.
    \[Accessed 24 May
    2017\].]24. [CERT, "BFF - Basic Fuzzing Framework," \[Online\]. Available:
    [https://vuls.cert.org/confluence/display/tools/CERT+BFF+-+Basic+Fuzzing+Framework](https://vuls.cert.org/confluence/display/tools/CERT+BFF+-+Basic+Fuzzing+Framework){rel="nofollow"}.
    \[Accessed 24 May
    2017\].]
