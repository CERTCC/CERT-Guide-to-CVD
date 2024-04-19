# Operational Security

Operational security, often shortened to "opsec," is an important part
of CVD operations. Opsec includes your ability to maintain security and
confidentiality for information associated with vulnerability reports
prior to disclosure.

## Handling Sensitive Data

Some of the information that passes through a CVD process may include information on an
organization's internal processes, trade secrets, or even national
security interests in some scenarios. Proper precautions need to be
established. It is recommended that recipients treat all received data
as private unless explicitly given permission to share.

Of course, there is some ambiguity when you say private: does that mean
the information is for the whole organization? Just the
CVD team? Possibly even a single analyst?

!!! tip "Need-to-Know Principle"

    The "need-to-know" principle is a good starting point for determining
    who should have access to sensitive information. This principle
    states that only those who need to know the information to perform
    their job should have access to it.
    In general, vulnerability information should be
    shared with the fewest number of people possible to effectively
    coordinate and remediate or mitigate a vulnerability prior to disclosure. Clearly
    declaring the data's sensitivity can help to make that determination.

### Traffic light Protocol

The [Traffic Light Protocol](https://www.first.org/tlp){:target="_blank"} is managed by the Forum of Incident Response and Security Teams (FIRST).
It is a set of designations used to ensure that sensitive information is shared with the appropriate audience.
By marking a document with a TLP level, a sender can easily communicate the sensitivity of
information and expectations about sharing it further.

TLP 2.0 has five levels, each with a different meaning:

| Label | Description |
|-------|-------------|
| <span style="color:#FF2B2B;background-color:#000000">**TLP:RED**</span> | For the eyes and ears of individual recipients only, no further disclosure. |
| <span style="color:#FFC000;background-color:#000000">**TLP:AMBER+STRICT**</span> | Limited disclosure, recipients can only spread this on a need-to-know basis within their organization only. |
| <span style="color:#FFC000;background-color:#000000">**TLP:AMBER**</span> | Limited disclosure, recipients can only spread this on a need-to-know basis within their organization and its clients.|
| <span style="color:#33FF00;background-color:#000000">**TLP:GREEN**</span> | Limited disclosure, recipients can spread this within their community. |
| <span style="color:#FFFFFF;background-color:#000000">**TLP:CLEAR**</span> | Recipients can spread this to the world, there is no limit on disclosure. |

!!! tip "TLP Levels and CVD"

    We recommend using <span style="color:#FFC000;background-color:#000000">**TLP:AMBER**</span> for most cases prior to public disclosure.

    In the context of CVD, the following applies:

    - <span style="color:#33FF00;background-color:#000000">**TLP:GREEN**</span> and <span style="color:#FFC000;background-color:#000000">**TLP:AMBER**</span> are best suited for information shared between reporters, vendors, and coordinators during phases prior to
    public announcement of a vulnerability.

    - If pre-publication announcements are made to deployers or other stakeholders, 
    <span style="color:#FFC000;background-color:#000000">**TLP:AMBER+STRICT**</span> could be a good fit.

    - <span style="color:#FF2B2B;background-color:#000000">**TLP:RED**</span> would usually be reserved for very sensitive information.

    - <span style="color:#FFFFFF;background-color:#000000">**TLP:CLEAR**</span> is most useful for public disclosures.

{% include-markdown "../../_includes/tlp_red_amber_strict_warning.md" heading-offset=1 %}

## Don't Automatically Trust Reports

There are two reasons that organizations receiving vulnerability reports
should maintain a degree of wariness regarding the reports they receive.
The first is intentional misdirection of your CVD capability, which we
already discussed in [Validation](../../topics/phases/validation.md) and
[Prioritization](../../topics/phases/prioritization.md).
The second is subtler, in
that the technical infrastructure you deploy to manage CVD cases can
potentially be affected by the vulnerabilities you are coordinating.

Vulnerability reports may contain hostile attachments&mdash;not necessarily
as an attack, but simply a reporter sending a proof-of-concept for your
review&mdash;so vendors and coordinators should design their report tracking
systems and process accordingly.

!!! tip "Isolate Attachments"

    Be sure attachments to vulnerability
    reports are not opened automatically anywhere along the process. You
    might also institute a policy that such attachments are only to be
    opened within an isolated testing environment, not on production
    systems.

CVD participants should keep in mind that their [case tracking](case_tracking.md) and [email
systems](secure_comms.md) themselves present attack surface and may be affected by the
very vulnerabilities they are designed to coordinate. We have witnessed
reports containing examples of image parsing vulnerabilities causing
problems for both webmail and ticketing systems that automatically
generate thumbnail previews of image attachments.

!!! tip "Consider Separate Infrastructure"

    Vendors and
    coordinators concerned about such risks should consider the degree to
    which their CVD support infrastructure is integrated with normal
    business operations systems. In some scenarios, maintaining parallel
    infrastructure may be preferable.

### Complex Communications Reduce Trust

It's also important to be aware that not all participants along the
chain of disclosure will be equally trustworthy. That's not to say they
are actively malicious, just that they may have incompatible values or
priorities that lead them to disclose the existence of the vulnerability
to others earlier than you'd prefer.
