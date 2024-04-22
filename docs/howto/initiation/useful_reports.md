# Providing Useful Information in a Vulnerability Report

<!--start-->Reporting a vulnerability requires that the vulnerability is
well-documented. This typically means providing high-quality and actionable
information to the vendor or coordinator.<!--end-->

This information should be detailed enough to allow the vendor to understand
the vulnerability and take appropriate action to fix it.

!!! example "What to Include in a Vulnerability Report"

    When reporting a vulnerability, it is important to include the following
    information:

    -   The exact product version(s) affected
    -   A description of how the vulnerability was discovered (including
    what tools were used) or what you were doing when you encountered
    the vulnerability
    -   Proof of concept (PoC) code or reproduction instructions
    demonstrating how the vulnerability might be exploited
    -   Ideally, a suggested patch, remediation, or mitigation action(s) if the reporter is
    aware of how to fix the vulnerability
    -   Description of the impact of the vulnerability and attack scenario
    -   Any time constraints (for example, give a date of publication or
    presentation at a conference if you know)

<!-- TODO add some references to other folks talking about good reports -->

!!! tip "Use the Common Weakness Enumeration (CWE) or Common Attack Pattern Enumeration and Classification (CAPEC)"

    Reporters that do not provide enough information to a vendor or
    coordinator may find their reports delayed or even rejected. Using the
    [Common Weakness Enumeration](https://cwe.mitre.org){:target="_blank"} or
    the [Common Attack Pattern Enumeration and Classification](https://capec.mitre.org){:target="_blank"}
    as a reference might be helpful to describe the
    type of vulnerability you have found and common ways to fix it the
    problem.
