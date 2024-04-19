# Working with the CERT/CC

!!! info "Prerequisites"

    Review [Vendor Response Process](../response_process/vendor.md) first.

If you have received a notification from the CERT/CC about a vulnerability in your product,
you are likely looking for guidance on how to respond.
This page provides an overview of the process for working with the CERT/CC to address the vulnerability.

## Responding to a CERT/CC Vulnerability Notification

{% include-markdown "../../_includes/_certcc_policy_tip.md" heading-offset=1 %}

When you receive a notification from the CERT/CC about a vulnerability in your product,
you should review the information provided and determine whether the report is accurate.
To do so, you can log into the
[Vulnerability Information and Coordination Environment (VINCE)](https://www.kb.cert.org/vince/) to view the report.

To learn more about how to coordinate with the CERT/CC on VINCE, please see our
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

    If you require extra information from the CERT/CC before a determination
    can be made, please feel free to reply within VINCE or by email.

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

    Vendor statements can be added directly to a case within VINCE.
    See [VINCE FAQ](https://vuls.cert.org/confluence/display/VIN/Frequently+Asked+Questions) for more.

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

    If desired, we can keep your organization anonymous when coordinating with other
    vendors.
