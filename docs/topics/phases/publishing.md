# Publishing

Once the [draft circulation](public_awareness.md) phase is complete, the next step is
publishing the vulnerability document to whatever channels have been
identified during previous phases.

Some vendors have a specific website that lists all their security
advisories to date.
Others might email the disclosure to a user mailing list or a security mailing list such as [Full Disclosure](https://seclists.org/fulldisclosure/){:target="_blank"}.

Reporters often choose to publish their findings
in a presentation or paper, or post it to a mailing list or blog.
A common goal for reporters in the CVD process is to synchronize
their publication with the vendor's response. As a result,
near-simultaneous publication occurs quite often.

It is generally courteous for the vendor and reporter to contact each
other after disclosure to inform one another that the disclosure went
through as planned and provide URLs to the published
documents.

## Where to Publish

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

Publicly disclosing the existence of a vulnerability and the
availability of its fix is usually considered to be the primary goal of
the CVD process.

Vendors will often provide vulnerability information:

- On the vendor's public website. Many vendors offer a
    security-focused section within the support section of their online
    offerings.
- To a public mailing list or a vendor-specific list

Vendors of bespoke software or products with highly focused customer
bases are sometimes reasonably confident that they can reach their
affected users directly.

These vendors often publish vulnerability and fix information:

- On a customer-only site
- Via a customer support mailing list
- By individually notifying customers, for example through the
    technical sales channel

However, even with a well-organized customer contact database, it can be
difficult for a vendor to be certain that all relevant decision makers
are reached in a timely manner. Hence, we recommend that vendors publish
at least basic vulnerability and fix announcements to their public
website in addition to whatever direct customer contact communications
they provide.
