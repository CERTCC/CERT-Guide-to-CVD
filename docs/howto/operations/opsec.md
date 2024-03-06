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
In general, vulnerability information should be
shared with the fewest number of people possible to effectively
coordinate and remediate a vulnerability prior to disclosure. Clearly
declaring the data's sensitivity can help to make that determination.

### Traffic light Protocol

The Traffic Light Protocol has been adopted for a standards-track by FIRST [@first_tlp]. By marking
a document with a TLP level-----{== Red, Amber, Green, or White ==}-----a sender can easily communicate the sensitivity of
vulnerability information and expectations about sharing it further. In
the context of CVD, the following applies:

- TLP:GREEN and TLP:AMBER are best suited for information shared
    between reporters, vendors, and coordinators during phases prior to
    public announcement of a vulnerability.

- If pre-publication announcements are made to deployers or other
    stakeholders, TLP:RED or TLP:AMBER could be a good fit.

- TLP:WHITE is most useful for public disclosures.

See Appendix [\[apx:tlp\]](#apx:tlp){reference-type="ref"
reference="apx:tlp"} for more on TLP.

## Don't Automatically Trust Reports

There are two reasons that organizations receiving vulnerability reports
should maintain a degree of wariness regarding the reports they receive.
The first is intentional misdirection of your CVD capability, which we
already discussed in [Section
4.3](4.3-Validation-and-Triage_47677469.md). The second is subtler, in
that the technical infrastructure you deploy to manage CVD cases can
potentially be affected by the vulnerabilities you are coordinating.

Vulnerability reports may contain hostile attachments&mdash;not necessarily
as an attack, but simply a reporter sending a proof-of-concept for your
review&mdash;so vendors and coordinators should design their report tracking
systems and process accordingly. Be sure attachments to vulnerability
reports are not opened automatically anywhere along the process. You
might also institute a policy that such attachments are only to be
opened within an isolated testing environment, not on production
systems.

CVD participants should keep in mind that their case tracking and email
systems themselves present attack surface and may be affected by the
very vulnerabilities they are designed to coordinate. We have witnessed
reports containing examples of image parsing vulnerabilities causing
problems for both webmail and ticketing systems that automatically
generate thumbnail previews of image attachments. Vendors and
coordinators concerned about such risks should consider the degree to
which their CVD support infrastructure is integrated with normal
business operations systems. In some scenarios, maintaining parallel
infrastructure may be preferable.

## Maintaining Pre-Disclosure Secrecy

The more people who know a secret, the more likely it is to leak. Simple
probability theory tells us that even if the probability of any given
party leaking is very low, the cumulative probability of a leak
increases exponentially with the number of parties involved
[@grimes2016viability].

Returning to our simple model, and the "Who needs to know what, when?"
question, multiparty disclosure highlights the need to balance
need-to-know with need-to-share. There are varying degrees of
need-to-know. Not everyone needs to know the same thing at the same
time. Patch originators are usually notified early in the process, since
their answer to "What do I need to do in response to this knowledge?"
(i.e., create a patch) is often on the critical path for any downstream
parties to be able to take action. Downstream vendors (patch consumers)
and deployers can be notified later.

### Complex Communications Reduce Trust

It's also important to be aware that not all participants along the
chain of disclosure will be equally trustworthy. That's not to say they
are actively malicious, just that they may have incompatible values or
priorities that lead them to disclose the existence of the vulnerability
to others earlier than you'd prefer.

{% include-markdown "./pgp.md" heading-offset=1 %}

## References

1. [FIRST, "TRAFFIC LIGHT PROTOCOL (TLP) FIRST Standards Definitions
    and Usage Guidance &mdash; Version 1.0," \[Online\]. Available:
    [https://www.first.org/tlp](https://www.first.org/tlp). \[Accessed 16 May
    2017\].]
