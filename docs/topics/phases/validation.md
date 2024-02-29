# Validating Reports

Vulnerability reports received from potentially unknown sources may hold
inaccurate information. One of the first tasks for the receiver of a
report is to analyze the report's validity. A vulnerability report is
basically an assertion that some set of conditions exists that permits
an adversary to take some action in support of a goal. But just because
it was reported doesn't make it true. Replication of the salient claims
made in the report is an important step in the case handling process.

## Recognizing High-Quality Reports

Not all reports are actionable. Some reports may under-specify the
problem, making it difficult or impossible to reproduce. Some may
contain irrelevant details. Some will be well written and concise, but
many will not. Some reports could describe problems that are already
known or for which a fix is already in the pipeline.

In easy cases, a simple description of the vulnerability, a screenshot,
or a copy/pasted snippet of code is all that is necessary to validate
that a report is likely accurate. In more complex scenarios, stronger
evidence and/or more effort might be required to confirm the
vulnerability. Responsive vendors should ensure analysts have access to
appropriate resources to test and validate bugs, such as virtual
machines (VMs), a testing network, and debuggers.

It may be that reproducing the vulnerability is beyond the capability or
time available by the first-tier recipient at the vendor. Most often
this occurs when the conditions required to exploit the vulnerability
are difficult to reproduce in a test environment. In this case, the
triager can weigh the reputation of the reporter against the claims
being made in the report and the impact if they were to be true. You
don't want to dismiss a report of a serious vulnerability just because
it is unexpected. A reporter with a high reputation might give weight to
an otherwise low-quality report (although in our experience finders and
reporters with a high reputation tend to have earned that reputation by
submitting high-quality reports).

If there is difficulty in reproducing the vulnerability, follow up with
the reporter promptly and courteously; be sure to be specific about what
you tried so that the reporter can provide effective advice. In some
cases, a report might be placed in a holding pattern while additional
information is requested from the reporter.

The possibility also exists that someone could be sending you reports to
waste your time, or erroneously believes the report is much more serious
than your analysis suggests. Not all reports you receive warrant your
attention. It is usually reasonable to decline reports if you provide
the reporter with a summary of your analysis and the ability to appeal
(presumably by providing the needed clarifying information).

Reporters should review [Reporting](reporting.md) to
ensure the report contains enough details for the recipient to verify
and reproduce a vulnerability. Be as specific as you can. Vendors that
follow up with questions are doing the right thing, and attempting to
validate your report; be friendly and courteous and attempt to provide
as much detail and help as you can.

{% include-markdown "./_report_credibility.md" heading-offset=1 %}

## Addressing Validation Problems

!!! tip "Follow up promptly with the reporter"

    If, as the recipient of a report, you encounter difficulty in reproducing the vulnerability, follow
    up with the reporter promptly and courteously; be sure to be specific about what you tried
    so that the reporter can provide effective advice. In such cases, the receiver might place the
    report in a wait state while additional information is requested from the reporter.

!!! tip "Declining Reports"

    The possibility also exists that someone could be sending you reports to waste your time, or
    erroneously believes the report is much more serious than your analysis suggests. Not all re-
    ports you receive warrant your attention. It is usually reasonable to decline reports if you pro-
    vide the reporter with a summary of your analysis and the ability to appeal (presumably by
    providing the needed clarifying information).

Reporters should review §4.2 to ensure the report contains enough details for the recipient to
verify and reproduce a vulnerability. Be as specific as you can. Vendors that follow up with
questions are doing the right thing, and attempting to validate your report; be friendly and
courteous and attempt to provide as much detail and help as you can.