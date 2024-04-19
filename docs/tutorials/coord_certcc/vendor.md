# Working with the CERT/CC

!!! info "Prerequisites"

    Review [Vendor Response Process](../response_process/vendor.md) first.

If you have received a notification from the CERT/CC about a vulnerability in your product,
you are likely looking for guidance on how to respond.
This page provides an overview of the process for working with the CERT/CC to address the vulnerability.

## Responding to a CERT/CC Vulnerability Notification

{% include-markdown "../../_includes/_certcc_policy_tip.md" heading-offset=1 %}

{== TODO review for accuracy given VINCE ==}
After reviewing the vulnerability report submitted, you can respond by
sending an email to [cert@cert.org.](mailto:cert@cert.org).
When doing so, be sure to include your VU# in the subject line, so that
our automated system can route your response to the analyst handling
your case. If you forget to add the VU# to the subject line of your
response email, our response may be delayed significantly.

{== TODO review for accuracy given VINCE ==}
We recommend encrypting your response email to
[cert@cert.org](mailto:cert@cert.org) with the CERT/CC\'s [PGP public key], in order to
maintain privacy until the public disclosure date. For more information
on using PGP or obtaining the CERT/CC's PGP key, please see [Sending
Sensitive Information](http://www.cert.org/contact/sensitive-information.cfm).

{== TODO review for accuracy given VINCE ==}
To fully communicate with the CERT/CC in a secure manner, we need your
organization's most up-to-date contact information, including your own
PGP public key. To update your information with us, please see our
[VINCE FAQ](https://vuls.cert.org/confluence/display/VIN/Frequently+Asked+Questions).

!!! tip "What does the CERT/CC look for in a response?"

    Typically, we would like the following questions answered in your
    organization's response:

    -   Is this report indicative of a real vulnerability? If not, can you
    provide details why you do not believe it is a vulnerability?
    -   Has this vulnerability already been addressed in a recent or
    upcoming release?
    -   If the vulnerability has not been addressed yet, when might the fix
    be available?
    -   Do you need any further information from the CERT/CC or the reporter
    in order to address this issue?

    {== TODO review for accuracy given VINCE ==}
    If you require extra information from the CERT/CC before a determination
    can be made, please feel free to contact us. The best way to do so is to
    send an email to [cert@cert.org](mailto:cert@cert.org) 
    with your VU# in the subject line, asking for more
    information. You may also call our phone number during business hours
    and an analyst will follow up with your message.

    We may also be able to arrange conference calls with analysts, or use
    other communication methods if requested.

## Publications and Vulnerability Disclosure

After 45 days or another agreed upon timeline, we publish
[Vulnerability Notes](http://www.kb.cert.org/vuls/)
to disclose the vulnerability and information on addressing the vulnerability if available.

!!! tip "Vendor Statements Are Welcome"

    We welcome Vendor Statements on any Vulnerability Note, even if the Note
    is already published. The Vendor Statement can consist of any statement
    or information you wish; we will copy this statement verbatim into our
    published Vulnerability Note.

    {== TODO review for accuracy given VINCE ==}
    To send a Vendor Statement, please email
    us at [cert@cert.org](mailto:cert@cert.org) with the VU# of the vulnerability in the subject line,
    and include you statement in the body of the email. This email should be
    PGP signed by your organization's key so we may verify its
    authenticity.

## Multiparty Coordination

The CERT/CC often coordinates with multiple vendors when a vulnerability
affects more than one product.
We refer to this as [Multiparty Coordinated Vulnerability Disclosure](../../howto/coordination/mpcvd.md) (MPCVD).

We can help coordinate the response to ensure that all affected parties are aware of the vulnerability and are
working to address it.

!!! tip "Coordinating with Other Vendors"

    If you discover a vulnerability that might affect more products than
    just your own (for example, you find a vulnerability in a widely-used
    open source library), please feel free to reach out to us to coordinate
    with all vendors at once.    
    {== TODO review for accuracy given VINCE ==}
    If desired, we can keep your organization anonymous when coordinating with other
    vendors.
