# Policy Management

Policy management for CVD consists of two areas of focus: external
and internal policy. External policy includes choosing disclosure and
embargo policies. Internal policy needs to address how vulnerability
reports are shared within the organization. We cover each of these
below.

<div class="grid cards" markdown>

- Disclosure Policy
- Embargo Policy
- Internal Case Handling Policy

</div>

## Disclosure Policy

For those responsible for implementing the CVD process, defining a
disclosure policy is an important first step. A well-defined policy
makes it clear what other participants in the CVD process can expect
when they engage with you and establishes good relationships between
finders, reporters, vendors, coordinators, and other stakeholders.

A disclosure policy typically describes what CVD stakeholders (finders,
reporters, vendors, coordinators) can expect in terms of these factors:

Scope

:   A description of the scope of issues to which the policy applies.
    This scope should be as explicit as possible, especially when there
    are specific boundaries of concern to the organization. If a bounty
    is to be paid for some classes of vulnerability reports, the scope
    definition should clearly delineate which kinds of reports will be
    eligible for the bounty. See
    {== §[\[sec:cvd_scope\]](#sec:cvd_scope){reference-type="ref"
    reference="sec:cvd_scope"} ==} for how scope is applied to report
    intake.

Exceptions

:   Any exceptional conditions that may alter the typical flow of the
    process. Common examples include evidence of attacks
    ({== §[\[sec:tr_exploit_public\]](#sec:tr_exploit_public){reference-type="ref"
    reference="sec:tr_exploit_public"} ==}) or vulnerabilities with safety
    or critical infrastructure impact
    ({== §[\[sec:tr_ci_impact\]](#sec:tr_ci_impact){reference-type="ref"
    reference="sec:tr_ci_impact"} ==}).

Safe Harbor

:   Should your organization choose to explicitly disavow legal
    retribution against reporters who otherwise follow the policy, that
    fact should be clearly laid out in the policy document.

Report quality requirements

:   It's okay to require reports to meet a certain level of quality
    before committing to taking action on them. See
    {== §[\[sec:validating_reports\]](#sec:validating_reports){reference-type="ref"
    reference="sec:validating_reports"} ==} for more on report quality
    assessment. However, it's also useful to judiciously apply the
    principle of robustness here: "In general, an implementation should
    be conservative in its sending behavior, and liberal in its
    receiving behavior" [@rfc760].

Preferred Communication Language(s)

:   If the organization has preferences for specific (human) languages
    for reports, the policy should specify this. That said, English is
    usually acceptable as a default.

Contact Information

:   How should reports be submitted? How can you be reached? See
    {== §[\[sec:reporting_for_vendors\]](#sec:reporting_for_vendors){reference-type="ref"
    reference="sec:reporting_for_vendors"} ==} for advice to vendors on
    improving the reporting experience for reporters.

Timing

:   Setting expectations for response timelines of the various
    milestones in a vulnerability report case can be helpful too. Most
    important are expected time to acknowledge receipt of a report and a
    default disclosure timeframe if one has been defined. An
    acknowledgement timeframe of 24-48 hours is common for vendors and
    coordinators, while 45-90 days seems to be the normal range for
    disclosures these days. That said, we recommend that both vendors
    and reporters treat policy-declared disclosure timeframes as the
    starting point of a negotiation process rather than a hard deadline.

A few examples of vulnerability disclosure policies can be found in
Appendix
[\[apx:policy_templates\]](#apx:policy_templates){reference-type="ref"
reference="apx:policy_templates"}.

RFC 2350 provides recommendations on how to publish information about
your CSIRT and disclosure policy and procedures [@rfc2350].

### Embargo policy

#### Embargo entry criteria

Fix not deployed. Not public. No exploits public. No attacks observed.
($fpxa$)

#### Embargo exit criteria

Timer expired. Exploit public ($pX$). Attacks observed ($pA$). Fix ready
($Vfdp \xrightarrow{F} VFdp$) Fix deployed ($VFDp \xrightarrow{D} VFDp$)
etc.

<!-- Some orgs have rules about who they include.
See Meltdown/Spectre responses from Apple, Microsoft, Google, Intel, etc.
Possibly other published policies.
Gist is often something about those able to materially support understanding or development of fixes.
Fingers-on-keyboards-that-can-get-stuff-done and
Brains-that-can-explain-edge-cases.

Consider adding commentary on who benefits from an embargo.
If it's protecting users from exposure to attacks prior to fix readiness $.f.p.a$, fine.
If it's protecting companies or organizations from bad PR, not ok.

Related to the above, but somewhat distinct:
Most of the complexity of CVD and especially MPCVD evaporates if we take the need for long embargoes away and just focus on increasing $Vfd... \xrightarrow{F,D} VFD...$ speed.
Yes, that is to idealistic to achieve across the board.
But for every case where you can eliminate the need for complicated secret-keeping schemes, you can focus more attention on the cases where it remains necessary.
Much of the ``pretend it's government classification'' stuff is not much more than an expensive and cumbersome LARP.
No, REDACTED, you can't force everyone into an NDA just because you have giant piles of money to spend on lawyers.
Tone this down, obviously.

-->

### Coordinating Further Downstream

Vulnerabilities having the potential for significant impact can lead to
coordination efforts beyond the traditional product vendor space.
Infrastructure and service providers are sometimes brought in early, if
there are mitigations that can be deployed in advance of the
availability of a fix. This can be especially helpful in cases where the
vulnerability may affect the infrastructure necessary to distribute the
patch in the first place.

### Do You Include Deployers?

Be careful to consider fairness though: By what criteria should you
notify service provider X but not service provider Y? At some point, the
complexity of who knows what gets high enough that the likelihood of a
leak goes to 1, and you might as well go public.

### Do You Include Governments?

<!--
Talk about tradeoffs of including governments/regulators. 
Fairness. 
Which governments?
Acknowledge difficulty of threading this needle.
See \fullref{sec:tr_ci_impact}, \fullref{sec:role_gov}
-->

## Internal case handling policy

<!-- 
Cover things like 
how reports pass through different parts of the organization,
escalation procedures,
notification channels,
sharing rules between groups,
information handling rules,
etc.
-->