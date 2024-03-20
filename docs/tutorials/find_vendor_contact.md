# Finding Vendor Contacts

!!! example inline end "How Things Get Complicated"

    Any number of factors can lead to difficulty in making the initial
    connection between a would-be reporter and the party or parties that can
    do something about the vulnerability they want to report.

    - Sometimes products outlive vendors. This can even happen in open source projects
    where the code is still out there but the team that built it has
    scattered to the winds. 
    - Companies go bankrupt. 
    - People change jobs. 
    - Maybe Vendor A included a library from Vendor B, who licensed it from C, but
    they only got a binary executable and didn't get the source code; and
    Vendor C is a spinoff of a conglomerate going through bankruptcy
    proceedings in a different country where they don't speak your
    language. 

Making initial contact with a vendor can sometimes be more difficult
than it should be. Here is a list of techniques we've used to figure
out how to reach a vendor we've never spoken with before.

## Common Methods

!!! tip "Search the web or the vendor's web site for relevant phrases"
 
    - "report a vulnerability"
    - "security"
    - "report a bug"
    - "bug bounty"
    - "vulnerability disclosure policy"
    - "security@" + company name
    - company name + "PSIRT"
 
!!! tip "Search for a `security.txt` file"

    See if the vendor has a `security.txt` file, often found at
    `www.example.com/.well_known/security.txt` or sometimes
    at `www.example.com/security.txt`
    ([securitytxt.org](https://securitytxt.org/) , [IETF
    Draft](https://tools.ietf.org/html/draft-foudil-securitytxt-09))

!!! tip "Check the following sources"

    - Vulnerability disclosure / bug bounty service providers
    ([BugCrowd](https://www.bugcrowd.com/), [Synack](https://www.synack.com/), [HackerOne](https://www.hackerone.com/), etc.)
    - The Forum of Incident Response and Security Teams (FIRST) [member directory](https://www.first.org/members/teams/)
    - The [CVE Partner List](https://www.cve.org/PartnerInformation/ListofPartners)

!!! warning "Avoid posting vulnerability details in public"

    We recommend you avoid posting vulnerability details in public
    when making initial contact when possible. For example,
    reporters might instead post an issue to a public bug tracker
    requesting that the vendor provide a secure method of
    communication instead of just posting the vulnerability details
    directly in a publicly visible issue.

!!! tip "Search open source code repositories to find developer contacts"

    - [Github](https://www.github.com/)
    - [GitLab](https://gitlab.com/)
    - [SourceForge](https://sourceforge.net/)
    
    - If no direct contact information can be found, posting to the
    Issues page of a project asking how they'd like to receive
    vulnerability reports can be useful.

!!! tip "Submit a bug report through the vendor's online bug tracker"

    If given the option to mark it as security-related, please do so as this often restricts viewing to just the vendor.

!!! tip "Reach out through social media"
    
    Social media can occasionally be a useful way to make initial contact with a vendor when other methods fail.

    - [Twitter](https://twitter.com/)
    - [LinkedIn](https://www.linkedin.com/)

!!! tip "Try emailing commonly used addresses"

    Sending an email to commonly used addresses can sometimes be useful.

    - `support@`
    - `security@`
    - `abuse@`
    - `info@`
    - `sales@`

!!! tip "Use the vendor's contact form"

    Many vendors have a "Contact Us" form on their web site that can be used to make initial contact.

!!! tip "Make a phone call to the vendor"

    Sometimes the best way to reach a vendor is to make a phone call.


!!! tip "Less common, but occasionally useful"

    We have rarely had to resort to these techniques, but they have been
    occasionally useful.

    -   Send a fax (yes, we've actually done this in the 21st century)
    -   Send [snail mail](https://insights.sei.cmu.edu/blog/reach-out-and-mail-someone/) to an executive 

        -   If you have access to resources like [LexisNexis](https://www.lexisnexis.com/), you can often find the names of executives in technical 
            roles as a starting point.
        -   If message delivery confirmation is desired, in the US you can send [certified mail](https://faq.usps.com/s/article/Certified-Mail-The-Basics) with signature verification.
            The recipient must sign to receive the mail, and you'll get a signed receipt back.

## When all that fails

Some vendors remain unreachable even after a number of reasonable good faith attempts to reach them&mdash;and by
reasonable we mean considerably less than exhausting the entire list above.
Some vendors just do not seem to want to be reached, and that is their prerogative.
However, we have found that experience is often the best teacher.
When a vendor gets surprised by the publication of a vulnerability in their product and it is clear from the report
that attempts to notify them were made but failed, it can prompt the vendor to re-evaluate their vulnerability
intake and handling processes to make it easier to reach them in the future.

{% include-markdown "./troubleshooting/recipes/_x03.md" heading-offset=1 %}
