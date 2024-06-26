# Report Credibility

!!! ssvc inline end "SSVC's Report Credibility Decision Point"

    The content in this section is adapted from the CERT/CC's [Stakeholder-Specific Vulnerability Categorization (SSVC)](https://certcc.github.io/SSVC/){:target="_blank"}
    [Report Credibility Decision Point](https://certcc.github.io/SSVC/reference/decision_points/report_credibility/){:target="_blank"} documentation.

An analyst should start with a presumption of credibility and proceed toward disqualification.
The reason for this is that, as a coordinator, occasionally doing a bit of extra work on a bad report is preferable to rejecting legitimate reports.
This is essentially stating a preference for false positives over false negatives with respect to credibility determination.

There are no ironclad rules for this assessment, and other coordinators may find other guidance works for them.
Credibility assessment topics include indicators for and against credibility, perspective, topic, and relationship to report scope.

## Credibility Indicators

The credibility of a report is assessed by a [balancing test](https://lsolum.typepad.com/legaltheory/2013/08/legal-theory-lexicon-balancing-tests.html){:target="_blank"}.
The indicators for or against are not commensurate, and so they cannot be put on a scoring scale, summed, and weighed.

!!! note Credibility Definition

    A report may be treated as credible when either

    1. the vendor confirms the existence of the vulnerability or
    2. independent confirmation of the vulnerability by an analyst who is neither the reporter nor the vendor.

    If neither of these confirmations are available, then the report credibility
    depends on a balancing test among the following indicators.

!!! tip "Indicators for Credibility"

    Indicators in favor of credibility include when the report

    - is specific about what is affected
    - provides sufficient detail to reproduce the vulnerability.
    - describes an attack scenario.
    - suggests mitigations.
    - includes proof-of-concept exploit code or steps to reproduce.
    - neither exaggerates nor understates the impact.

    Additionally, screenshots and videos, if provided, support the written text of the report and do not replace it.

!!! warning "Indicators against Credibility"

    Indicators against credibility include when the report

    - is “spammy” or exploitative (for example, the report is an attempt to upsell the receiver on some product or service).
    - is vague or ambiguous about which vendors, products, or versions are affected (for example, the report claims that all “cell phones” or “wifi” or “routers” are affected).
    - is vague or ambiguous about the preconditions necessary to exploit the vulnerability.
    - is vague or ambiguous about the impact if exploited.
    - exaggerates the impact if exploited.
    - makes extraordinary claims without correspondingly extraordinary evidence (for example, the report claims that exploitation could result in catastrophic damage to some critical system without a clear causal connection between the facts presented and the impacts claimed).
    - is unclear about what the attacker gains by exploiting the vulnerability. What do they get that they didn't already have? For example, an attacker with system privileges can already do lots of bad things, so a report that assumes system privileges as a precondition to exploitation needs to explain what else this gives the attacker.
    - depends on preconditions that are extremely rare in practice, and lacks adequate evidence for why those preconditions might be expected to occur (for example, the vulnerability is only exposed in certain non-default configurations—unless there is evidence that a community of practice has established a norm of such a non-default setup).
    - claims dire impact for a trivially found vulnerability. It is not impossible for this to occur, but most products and services that have been around for a while have already had their low-hanging fruit major vulnerabilities picked. One notable exception would be if the reporter applied a completely new method for finding vulnerabilities to discover the subject of the report.
    - is rambling and is more about a narrative than describing the vulnerability. One description is that the report reads like a food recipe with the obligatory search engine optimization preamble.
    - conspicuously misuses technical terminology. This is evidence that the reporter may not understand what they are talking about.
    - consists of mostly raw tool output. Fuzz testing outputs are not vulnerability reports.
    - lacks sufficient detail for someone to reproduce the vulnerability.
    - is just a link to a video or set of images, or lacks written detail while claiming “it's all in the video”. Imagery should support a written description, not replace it.
    - describes a bug with no discernible security impact.
    - fails to describe an attack scenario, and none is obvious.

    Two additional indicators of non-credible reports are:
    
    - The reporter is known to have submitted low-quality reports in the past.
    - The analyst’s professional colleagues consider the report to be not credible.

!!! question "Why isn't poor grammar on this list?"

    We considered adding poor grammar or spelling as an indicator of non-credibility.
    On further reflection, we do not recommend that poor grammar or spelling be used as an indicator of low report quality, as many reporters may not be native to the receiver's language.
    Poor grammar alone is not sufficient to dismiss a report as not credible.
    Even when poor grammar is accompanied by other indicators of non-credibility, those other indicators are sufficient to make the determination.

## Credibility of what to whom

We are interested in the coordinating analyst's assessment of the credibility of a report.
This is separate from the fact that a reporter probably reports something because *they* believe the report is credible.

The analyst should assess the credibility of the report of the vulnerability, not the claims of the impact of the vulnerability.
A report may be credible in terms of the fact of the vulnerability's existence even if the stated impacts are inaccurate.
However, the more extreme the stated impacts are, the more skepticism is necessary.
For this reason, “exaggerating the impact if exploited” is an indicator *against* credibility.
Furthermore, a report may be factual but not identify any security implications; such reports are bug reports, not vulnerability reports, and are considered out of scope.

A coordinator also has a scope defined by their specific constituency and mission.
A report can be entirely credible yet remain out of scope for your coordination practice.
Decide what to do about out of scope reports separately, before the vulnerability coordination prioritization decision begins.
If a report arrives and would be out of scope even if true, there will be no need to proceed with judging its credibility.
