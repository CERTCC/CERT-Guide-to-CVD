# Create Secure Channels for Reporting

Whether you are a vendor or a coordinator, you need to have open
channels for communication with vulnerability finders and reporters.
Secure communications can be nuanced to maintain in operation, so we have compiled
some advice about establishing and maintaining this capability.

## Web Forms and Portals

Most vulnerability reports have a similar structure, making a web form a
preferable method for receiving vulnerability reports for many
organizations.

!!! tip "Focus on Encrypted Transport and Strong Authentication"

    If you're starting a new CVD program, we recommend focusing on encrypted transport and strong authentication.
    Don't build a new process around PGP / GnuPG and email.
    Some vendors choose to offer a web form specifically for receiving reports of security-related issues.
    Such forms can then deliver the report directly to your security or engineering team.

!!! tip "Have a Dedicated Form for Security Reports"

    The CERT/CC discourages reliance on general "Contact Us" web forms that
    pass through an organization's communications or customer support
    teams. Many finders will balk at having to get past these nontechnical
    interfaces into the vendor. In addition, security messages often must be
    triaged and processed differently than other incoming contacts.

    To secure your web form, you will need to enable HTTPS
    and TLS, and obtain a TLS certificate from a Certificate Authority (CA).
    A free option is [Let's Encrypt](https://letsencrypt.org/){:target="_blank"}, maintained by the [Internet Security
    Research Group](https://www.abetterinternet.org/about/){:target="_blank"} (ISRG).

    Coordination tools like VINCE or coordination platforms can be a good choice, or
    you can make use of a third-party bug bounty or coordination platform.

!!! tip "Do you need a login to report?"

    TLS ensures that the transmission is secure, but does not authenticate
    who sent the report. If this is a requirement, you may also need to
    implement login accounts on your web form with adequate authentication
    mechanisms such as two-factor or X.509 certificates. However, this setup
    increases the complexity for reporters to provide information to you,
    and as a result is rare in practice and likely unnecessary. Once set up,
    an HTTPS web form provides an easy-to-use way for reporters to contact
    you with vulnerability reports and other information.

    However, a problem does come up: how do you acknowledge receipt of the report
    and continue the conversation?

    Possibilities include the following:

    - *Echoing back the message in a confirmation email.* The reporter
    knows you received the text, but now the text was sent in plain text
    email for everyone to read. It is unlikely you want to do this.

    - *Send a brief thank you message, but without details.* The reporter
    can now be assured that the report was received. But what if you
    have a follow up question for the reporter? It's likely you will
    need to send an email, which will require encryption to keep the
    details of the question and answer secure.

    - *Send a brief thank you message, and ask the reporter to log in to a
    portal to view the message conversation.* This resolves the issue of
    two-way secure communications, but now you need to establish a
    public-facing portal and manage portal credentials. This raises
    additional operational considerations, for example those below:

        - user account management and password changes

        - two-factor authentication or X.509 as possible requirement to ensure
        user identity

    Portal credential maintenance introduces more complications, and for
    many vendors may not be worth the effort. Another disadvantage of 
    using a portal is that vendors and organizations may be unwilling to
    create accounts on another vendor's portal. This may discourage
    multi-party communication and coordination, effectively preventing a
    vendor or reporter from participating in multi-party CVD.

{% include-markdown "./_cvd_platform.md" heading-offset=1 %}

## Email

Email is a simple, tried-and-true method of communication over the
Internet. Simply because everyone has access to it, email is likely to
remain a common way of receiving vulnerability reports and
communications.

<div class="grid" markdown>

!!! tip "Email is the Universal CVD API"

    In our experience, email is still a very common way to receive
    vulnerability reports. It serves as a sort of universal API for CVD,
    regardless of what other tools might be in use.
    For this reason, the CERT/CC recommends that vendors establish a specific
    and well-publicized email alias such as `security@example.com` solely
    for receipt of vulnerability reports, even if they have other
    communication channels available.

!!! warning "Email is Insecure by Default"

    Email by itself is not a secure medium. We recommend that emails
    containing sensitive information be encrypted \[2\]. This includes
    emails containing information about unpatched or otherwise sensitive
    vulnerabilities.

</div>

!!! tip "Avoid Using Personal Email Addresses for Security Contact"

    Because of the potential for organizational changes like
    employee promotions and turnover, having an individual's email address
    as a security point of contact is generally discouraged. A better
    solution is to establish an email account specifically for vulnerability
    reports and CVD activity. Many vendors choose to reserve an email
    address like `security@example.com` or `psirt@example.com` for
    this purpose.

!!! tip "Make Your Security Contact Information Easy to Find"

    The CERT/CC recommends that vendors make their security contact
    information easy to find, for example on the Contact Us page of their
    website.

    Ideally, an Internet search for `<vendorname> report vulnerability`
    should lead to that contact information. The security email account
    should be an alias that is forwarded to or shared by one or more people.
    This way, multiple team members can check the incoming mail and cover
    for each other when team members are out of the office. Even if the
    security team is only one person, having an alias makes it easier to
    adapt should that person leave the organization; to the outside world,
    no contact information needs to change.

    The IETF's [RFC 2350](https://datatracker.ietf.org/doc/html/rfc2350){:target="_blank"}
    _Expectations for Computer Security Incident Response_ (aka BCP-21) 
    suggests you include contact information as
    part of your overall CSIRT disclosure policy and process publication.
    [RFC 9116](https://datatracker.ietf.org/doc/html/rfc9116){:target="_blank"}
    _A File Format to Aid in Security Vulnerability Disclosure_
    See the [security.txt](https://securitytxt.org/){:target="_blank"} site for more.

!!! warning "Email is No Substitute for a Case Tracking System"

    Although receiving information via email is convenient, it is not a very
    good mechanism for tracking multiple cases at once. Rather than sending
    security emails to individual mailboxes, vendors, coordinators, and even
    large-scale reporters should consider setting up a web-based case
    tracking system instead. That way, received emails can automatically
    generate new cases or augment existing ones, which can then be assigned
    to team members and tracked as necessary. More on this topic can be
    found in [Case Tracking](case_tracking.md).

!!! tip "Managing Email Encryption"

    Although we primarily recommend web-based case tracking systems for
    managing communications in CVD, email encryption can still be useful
    for securing sensitive information in transit.

    Since email is an insecure communications channel by default,
    many vendors, reporters, and coordinators prefer to use encrypted mail
    instead. Although x.509 encrypted mail exists, we have found
    PGP-compatible tools such as GnuPG to be more widely used by CVD
    participants. Vendors are encouraged to create and publish a PGP key
    affiliated with the security email alias to allow the confidentiality of
    sensitive reports to be maintained in transit.

    A common choice used to be Thunderbird with [Enigmail](https://enigmail.net/index.php/en/){:target="_blank"}, but
    Thunderbird is no longer supported by the Enigmail project.
    Alternative mail clients for Enigmail include 
    [SeaMonkey](https://seamonkey-project.org/){:target="_blank"},
    [Epyrus](http://www.epyrus.org/){:target="_blank"} and [Postbox](https://postbox-inc.com/){:target="_blank"}.

    Other open source solutions such as Outlook with [gpg4win](https://www.gpg4win.org/){:target="_blank"}, or [KMail](https://apps.kde.org/kmail2/){:target="_blank"}
    with [KGpg](https://apps.kde.org/kgpg/){:target="_blank"} and/or [Kleopatra](https://www.openpgp.org/software/kleopatra/){:target="_blank"} 
    and proprietary solutions such as
    [PGP Encryption Desktop](https://techdocs.broadcom.com/us/en/symantec-security-software/information-security/symantec-encryption-desktop/11-0-0.html){:target="_blank"} also exist.
    A collection of email encryption tools can be found on 
    [OpenPGP](https://www.openpgp.org/software/){:target="_blank"}'s website.

!!! info "How Our Approach has Changed"

    The CERT/CC has used email as the primary means of communication for
    many years. However, as our operations have scaled up, we have found
    that email is not always the best way to manage multiple cases
    simultaneously. We have since developed a web-based case tracking
    system called [VINCE](https://www.kb.cert.org/vince/){:target="_blank"} to help us manage
    our cases more effectively.
    
    While email still has its place in our CVD operations, we have found that
    PGP / GnuPG is overly complicated for many of the folks we need to coordinate with,
    reporters and vendors alike.

!!! question "What happened to PGP/GnuPG?"

    PGP / GnuPG, never popular outside of the infosec community, has been falling out of
    favor in the past decade. 
    Some notable commentary includes:
    [What's the Matter with PGP?](https://blog.cryptographyengineering.com/2014/08/13/whats-matter-with-pgp/){:target="_blank"},
    [GnuPG and Me](https://moxie.org/2015/02/24/gpg-and-me.html){:target="_blank"}, and
    [I’m throwing in the towel on PGP, and I work in security](https://arstechnica.com/information-technology/2016/12/op-ed-im-giving-up-on-pgp/){:target="_blank"}.

    PGP and GnuPG are highly prone to user error, and the consequences of those errors can be severe 
    (e.g., sending a private key to the wrong person). The tools are also difficult to manage at scale.

    Encrypted email was intended for one-to-one communication, but in CVD, we often have teams of people
    from different organizations working together. In this scenario, the team often has a single key.
    Everyone outside the team encrypts to that one key, but on the receiving side,
    the email is often decrypted and forwarded as plain text within the team (e.g., posted to a case tracking system).
    For all practical purposes, the email encryption is just serving as transport encryption rather than end-to-end
    from sender mail client to receiver mail client. But other technology like StartTLS already enables transport encryption,
    and that is usually configured by mail server administrators who are more likely to get it right than individual users.
    It's not clear that the additional complexity adds much value.

    Finally, there is the question of what the threat model is. In other words, who are you trying to protect against?
    A highly skilled adversary can likely get access to the key material itself, or to the contents of the email in 
    plain text before encryption or after decryption. A less skilled adversary might be able to intercept the mail
    in transit, but if you're using StartTLS, that's already encrypted in transit.
