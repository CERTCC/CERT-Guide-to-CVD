# Validating Reports

When a [vendor](../../topics/roles/vendor.md) or [coordinator](../../topics/roles/coordinator.md)
receives a vulnerability report, it's usually necessary to prioritize it along with other
vulnerability reports already in progress, new feature development, and possibly other non-security bug fixes.
As a result, there are a few considerations to be made in dealing with incoming reports.
These essentially boil down to three questions:

!!! question "Questions to Consider"

    1. Is the report in scope?
    2. Is the report credible and valid?
    3. What priority should the report be given?
    
    We tackle the first two questions in this section, and the third in the [next section](prioritization.md).

## Scope

A CVD participant's scope determines which cases they can and should handle.
A vendor's scope is usually the set of their products, along with any components their products depend on.

!!! tip "End-of-Life Software and Scope"

    For many vendors, End-of-Life (EoL) software might be out of scope by default, but sometimes it is worth considering as in-scope.
    For example, vendors may choose to provide fixes for vulnerabilties in EoL software if the software only recently went out of support and the vulnerability has a severe impact.

!!! example "Scope for a Coordinating CSIRT"

    A coordinator also has a scope defined by their specific constituency and mission.
    For example, a CSIRT within a government agency might have a scope limited to systems operated by that agency.
    Other government CSIRTs might have responsibility for systems across the entire government.
    Some ISAOs have a scope to cover vulnerabilities in a specific infrastructure sector or industry.

Regardless what a CVD participant's scope is, it is usually easiest to determine whether a received report meets their
scope criteria before proceeding to validate the report.
If a report arrives and would be out of scope *even if* true, there will be no need to proceed with judging its credibility.
CVD participants should decide what to do about out of scope reports separately, before the vulnerability coordination
validation and prioritization decisions begin.

!!! tip "Handing off Out-of-Scope Reports"

    A judgement that a report is out of scope need not result in simply dropping the case.
    The case might be handed off to a more appropriate vendor or coordinator for whom it would be in scope, for example.

## Recognizing High-Quality Reports

<!--start-->Not all reports are actionable. Some reports may under-specify the
problem, making it difficult or impossible to reproduce. Some may
contain irrelevant details. Some will be well written and concise, but
many will not. Some reports could describe problems that are already
known or for which a fix is already in the pipeline.<!--end-->

In easy cases, a simple description of the vulnerability, a screenshot,
or a copy/pasted snippet of code is all that is necessary to validate
that a report is likely accurate. In more complex scenarios, stronger
evidence and/or more effort might be required to confirm the
vulnerability. Responsive vendors should ensure analysts have access to
appropriate resources to test and validate bugs, such as virtual
machines (VMs), a testing network, and debuggers.

{% include-markdown "./_report_credibility.md" heading-offset=2 %}

## Addressing Validation Problems

Not all reports you receive will be immediately actionable. Some reports
may be vague, ambiguous, or otherwise difficult to validate. Here are
a few tips for dealing with such reports:

<div class="grid" markdown>

!!! tip "Consider Reporter Reputation"

    It may be that reproducing the vulnerability is beyond the capability or
    time available by the first-tier recipient at the vendor or coordinator. Most often
    this occurs when the conditions required to exploit the vulnerability
    are difficult to reproduce in a test environment. In this case, the
    triager can weigh the reputation of the reporter against the claims
    being made in the report and the impact if they were to be true. You
    don't want to dismiss a report of a serious vulnerability just because
    it is unexpected. A reporter with a high reputation might give weight to
    an otherwise low-quality report (although in our experience finders and
    reporters with a high reputation tend to have earned that reputation by
    submitting high-quality reports).

!!! warning "Be cautious of low-quality reports"

    The possibility also exists that someone could be sending you reports to
    waste your time, or erroneously believes the report is much more serious
    than your analysis suggests. Not all reports you receive warrant your
    attention. It is usually reasonable to decline reports if you provide
    the reporter with a summary of your analysis and the ability to appeal
    (presumably by providing the needed clarifying information).

!!! tip "Follow up promptly with the reporter"

    If, as the recipient of a report, you encounter difficulty in reproducing the vulnerability, follow
    up with the reporter promptly and courteously; be sure to be specific about what you tried
    so that the reporter can provide effective advice. In such cases, the receiver might place the
    report in a wait state while additional information is requested from the reporter.

!!! tip "Advice for Reporters"

    Reporters should review [Reporting](../../topics/phases/reporting.md) to
    ensure the report contains enough details for the recipient to verify
    and reproduce a vulnerability. Be as specific as you can. Vendors that
    follow up with questions are doing the right thing, and attempting to
    validate your report; be friendly and courteous and attempt to provide
    as much detail and help as you can.

</div>
