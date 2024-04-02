# Prioritization Heuristics

<!--start-->Even for the reports a vendor accepts as [valid](validation.md) (in scope, credible, and valid),
it is likely that the development team does not have time to address every
report at the moment it arrives. Thus, if a report is found to be valid,
the next question is how to allocate resources to the report.<!--end--> Most often
this requires some measure of how significant the vulnerability is compared
to other vulnerabilities that have been reported. In some
scenarios, the vulnerability may be a critical flaw that requires
immediate action, while other cases might indicate a very rare and
hard-to-exploit vulnerability that should be given a low priority.

!!! note inline end "Beware Misuse of Scoring Systems"

    In our 2021 article [_Time to Change the CVSS?_](https://doi.org/10.1109/MSEC.2020.3044475), we
    argued that many organizations misuse the Common Vulnerability Scoring System (CVSS) 
    by using it as a risk metric, when it was never intended to be used that way.
    Since that time, [CVSS version 4.0](https://www.first.org/cvss/v4.0/specification-document) has been released,
    and while it is a significant improvement over previous versions, it still has limitations.
    We have generally found that the information contained in the CVSS _vector_ is more useful than the _score_ itself.
    This led us to develop the [Stakeholder-Specific Vulnerability Categorization](https://certcc.github.io/SSVC) (SSVC) as a more flexible alternative.

There are a number of heuristics for evaluating the severity of
vulnerabilities. Perhaps the most commonly known of these is the [Common
Vulnerability Scoring System](https://www.first.org/cvss/) (CVSS). This system allows a short
standard description of the impact of a vulnerability and can be mapped
to a score between 1.0 and 10.0 to help prioritization. 

The [Common Weakness Scoring System](https://cwe.mitre.org/cwss/cwss_v1.0.1.html) (CWSS)
is a similar system that was intended to be used to assess the potential impact of a class of
weaknesses.
Whereas CVSS addresses the detailed impact of a specific vulnerability,
CWSS could be used to evaluate the impact of a class of weaknesses.

While scoring systems like CVSS and CWSS can be useful at establishing
relative severity among reports, care must be taken in their use since
scores do not always map well onto a vendor's or deployer's
priorities.

<br/><!-- for spacing -->

!!! tip "Stakeholder-Specific Vulnerability Categorization (SSVC)"

    The CERT/CC's [Stakeholder-Specific Vulnerability Categorization](https://certcc.github.io/SSVC) (SSVC)
    provides a method for developing vulnerability management decision models
    that are tailored to the specific needs of different stakeholders.

!!! tip "Heuristic Evaluation"

    Vendors, Coordinators, and Deployers should ensure their analysts are trained
    in the chosen heuristic
    and understand its strengths and weaknesses so that its result can be
    overridden when necessary. 

    We do not, for example, recommend blind
    adherence to hard cutoffs such as "We only bother with reports that
    have a CVSS score greater than 7.0." No vulnerability scoring system is
    so precise.

    Ideally, whatever prioritization scheme is used should also
    be made transparent to reporters so that the process is understood by
    all stakeholders. Transparency in this part of the process can help
    prevent frustration and confusion when CVD participants disagree on
    the priority given to a vulnerability.
