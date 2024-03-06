# Prioritization Heuristics

Even for the reports a vendor accepts as legitimate and worthwhile, it
is likely that the development team does not have time to address every
report at the moment it arrives. Thus, if a report is found to be valid,
the next question is how to allocate resources to the report. Most often
this requires some measure of how severe the vulnerability is. In some
scenarios, the vulnerability may be a critical flaw that requires
immediate action, while other cases might indicate a very rare and
hard-to-exploit vulnerability that should be given a low priority.

!!! tip inline end "Stakeholder-Specific Vulnerability Categorization (SSVC)"

    The CERT/CC's [Stakeholder-Specific Vulnerability Categorization](https://certcc.github.io/SSVC) (SSVC)
    provides a method for developing vulnerability management decision models
    that are tailored to the specific needs of different stakeholders.

There are a number of heuristics for evaluating the severity of
vulnerabilities. Perhaps the most commonly known of these is the [Common
Vulnerability Scoring System](https://www.first.org/cvss/) (CVSS). This system allows a short
standard description of the impact of a vulnerability and can be mapped
to a score between 1.0 and 10.0 to help prioritization. A related but
different metric is the [Common Weakness Scoring System](https://cwe.mitre.org/cwss/cwss_v1.0.1.html) (CWSS).
Whereas CVSS addresses the detailed impact of a specific vulnerability,
CWSS can be used to evaluate the impact of a class of weaknesses. While
scoring systems like CVSS and CWSS can be useful at establishing
relative severity among reports, care must be taken in their use since
scores do not always map well onto a vendor's or deployer's
priorities.

Vendors should ensure their analysts are trained in the chosen heuristic
and understand its strengths and weaknesses so that its result can be
overridden when necessary. We do not, for example, recommend blind
adherence to hard cutoffs such as "We only bother with reports that
have a CVSS score greater than 7.0." No vulnerability scoring system is
so precise. Ideally, whatever prioritization scheme is used should also
be made transparent to reporters so that the process is understood by
all stakeholders. Transparency in this part of the process can help
prevent frustration and confusion when reporter and vendor disagree on
severity of a vulnerability.
