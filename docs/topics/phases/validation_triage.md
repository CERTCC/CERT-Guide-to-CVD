# Validation and prioritization

When a vendor or coordinator receives a vulnerability report, it's
usually necessary to prioritize it along with other vulnerability
reports already in progress, new feature development, and possibly other
non-security bug fixes. As a result, there are a few considerations to
be made in dealing with incoming reports.

When a vendor or coordinator receives a vulnerability report, it's usually necessary to prioritize it along with other vulnerability reports already in progress, new feature development, and possibly other non-security bug fixes.
As a result, there are a few considerations to be made in dealing with incoming reports.
These essentially boil down to three questions:

!!! question "Questions to Consider"

    1. Is the report in scope?
    2. Is the report credible and valid?
    3. What priority should the report be given?

## Scope

A CVD participant's scope determines which cases they can and should handle.
A vendor's scope is usually the set of their products, along with any components their products depend on
{== (see \S\ref{sec:complicated_supply_chains} for more on software supply chains). ==}
For many vendors, EoL software might be out of scope by default, but sometimes it is worth considering as in-scope.
For example, vendors may choose to provide fixes for vulnerabilties in EoL software if the software only recently went out of support and the vulnerability has a severe impact.

A coordinator also has a scope defined by their specific constituency and mission.
For example, a CSIRT within a government agency might have a scope limited to systems operated by that agency.
Other government CSIRTs might have responsibility for systems across the entire government.
Some ISAOs have a scope to cover vulnerabilities in a specific infrastructure sector or industry.

Regardless what a CVD participant's scope is, it is usually easiest to determine whether a received report meets their
scope criteria before proceeding to validate the report.
If a report arrives and would be out of scope even if true, there will be no need to proceed with judging its credibility.
CVD participants should decide what to do about out of scope reports separately, before the vulnerability coordination
triage decision begins.
A judgement that a report is out of scope need not result in simply dropping the case, however.
The case might be handed off to a more appropriate vendor or coordinator for whom it would be in scope, for example.
Additional discussion of CVD scope is given in {== \S\ref{sec:policy_mgt}. ==}

{% include-markdown "./validation.md" heading-offset=1 %}
{% include-markdown "./prioritization.md" heading-offset=1 %}
