# The CERT&reg; Guide to Coordinated Vulnerability Disclosure

!!! tip inline end "Original Report"

    The CERT Guide to Coordinated Vulnerability Disclosure was originally published as
    [CMU/SEI-2017-SR-022](https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=503330)

    This web version is an evolution of that original report.

This is the web edition of *The CERT® Guide to Coordinated Vulnerability
Disclosure*. We've reproduced the original report here in its entirety
to make it easier to find the topic you're looking for. We're also in
the process of revising the guide based on feedback we've received
since its original publication. Got a suggestion? [Submit it
here](https://github.com/CERTCC/CERT-Guide-to-CVD/issues).

<!-- for vertical spacing -->
<br/>
---

!!! abstract

    Security vulnerabilities remain a problem for vendors and deployers of
    software-based systems alike. Vendors play a key role by providing fixes
    for vulnerabilities, but they have no monopoly on the ability to
    discover vulnerabilities in their products and services. Knowledge of
    those vulnerabilities can increase adversarial advantage if deployers
    are left without recourse to remediate the risks they pose. Coordinated
    Vulnerability Disclosure (CVD) is the process of gathering information
    from vulnerability finders, coordinating the sharing of that information
    between relevant stakeholders, and disclosing the existence of software
    vulnerabilities and their mitigations to various stakeholders including
    the public. The CERT Coordination Center has been coordinating the
    disclosure of software vulnerabilities since its inception in 1988. This
    document is intended to serve as a guide to those who want to initiate,
    develop, or improve their own CVD capability. In it, the reader will
    find an overview of key principles underlying the CVD process, a survey
    of CVD stakeholders and their roles, and a description of CVD process
    phases, as well as advice concerning operational considerations and
    problems that may arise in the provision of CVD and related services.

## CVD Quick Start

When we finished the first version of [The CERT Guide to Coordinated Vulnerability
Disclosure](https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=503330),
we noticed folks kept commenting on its length. Feedback we have
received in the intervening time has convinced us that there is a need
for a more succinct way to get started with CVD without requiring
someone to read every word in the Guide. To that end, we offer this CVD
Quick Start to act as a meta-guide to the Guide.


[The _CERT Guide to CVD_ in a Nutshell](tutorials/cvd_in_a_nutshell) contains an
overview of the entire document, and is a good place for all readers to
become familiar with what's in the guide without necessarily poring
over the details. Where you go from there depends on what you're trying
to achieve.

<div class="grid cards" markdown>

- **Finders, Reporters, Vendors, and Coordinators**

    ---

    If you're a [*researcher*](topics/roles/finder.md),
    [*vendor*](topics/roles/vendor.md), or [*coordinator*](topics/roles/coordinator.md) trying to coordinate a disclosure and you need help, you might
    want to start with 
    [Troubleshooting Coordinated Vulnerability Disclosure](howto/coordination/cvd_recipes.md)
    to find the problem area(s) you're currently dealing with.
    From there you can follow the links into the document for more details.

- **Vendor PSIRTs**

    ---

    If you're a [*vendor*](topics/roles/vendor.md) trying to establish a vendor product security
    incident response team (PSIRT), you may be interested in
    [Principles](topics/principles/index.md),
    [Preparation](howto/preparation/index.md), and
    [Operation](howto/operation/index.md)
    as starting points. Additionally, you can use
    [Troubleshooting Coordinated Vulnerability Disclosure](howto/coordination/cvd_recipes.md)
    as a rubric of scenarios to consider when planning your operational processes.
    [Disclosure Policy Resources](reference/disclosure_policy_templates.md)
    contains links to a number of disclosure policy examples and
    templates.

- **Coordinators**

    ---

    If you're a [*coordinator*](topics/roles/coordinator.md) spinning up your CVD capability, you
    should become familiar with the
    [Principles](topics/principles/index.md),
    [Roles](topics/roles/index.md),
    [Coordination](howto/coordination/index.md),
    and
    [Operation](howto/operation/index.md) sections.
    The [Reference](reference/index.md) section may also be useful to you.

- **Policy-Makers**

    ---

    If you're a *policy-maker* (or influencer thereof), the
    sections
    [HowTo Overview](howto/index.md),
    [Principles](topics/principles/index.md),
    [Roles](topics/roles/index.md),
    and [Phases](topics/phases/index.md) are probably most useful to you
    to start, but there are many edge cases in
    [Troubleshooting Coordinated Vulnerability Disclosure](howto/coordination/cvd_recipes.md)
    that are worth considering when you're thinking about writing policy
    that sets out how things are expected to be done.
    [Disclosure Policy Resources](reference/disclosure_policy_templates.md) 
    contains links to a number of disclosure policy examples and
    templates.

</div>

Of course, we think it's best if you eventually become familiar with
the entire site, but hopefully the hints above will help you find
the most effective places to start.

