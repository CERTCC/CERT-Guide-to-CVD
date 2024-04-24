# Vulnerability Disclosure Policy Templates for Reporters

<!--start-->This collection of policy statement templates describe expectations for reporters participating in a
vulnerability disclosure program.<!--end-->

## Tips and Usage Notes

{% include-markdown "./_usage.md" %}
{% include-markdown "./_terminology.md" %}
{% include-markdown "./_consistency_warning.md" %}

## Template Policy Statements

Reporters MUST adhere to the following guidelines.

## General

* Reporters MUST comply with all applicable`JURISDICTION` laws in connection with security research activities or other participation in this vulnerability disclosure program.

* Reporters SHOULD make a good faith effort to notify and work directly with the affected vendor(s) or service providers prior to publicly disclosing vulnerability reports.


## Scope of Authorized Testing

* Reporters MAY test`SYSTEM SCOPE` to detect a vulnerability for the sole purpose of providing`ORGANIZATION` information about that vulnerability.

* Reporters SHOULD only test against test accounts owned by the Reporter or with explicit permission from the account holder.

* Reporters MUST avoid harm to`ORGANIZATION`'s information systems and operations.

* Reporters MUST make every effort to avoid privacy violations, degradation of user experience, disruption to production systems, and destruction or manipulation of data.

* Reporters MUST stop testing once that testing has established that a vulnerability exists, or sensitive data has been encountered. Sensitive data includes personally identifiable information, financial information (e.g., account numbers), proprietary information or trade secrets.

* Reporters MUST NOT test any services not expressly listed in`SYSTEM SCOPE`, including any connected services

* Reporters MUST NOT exploit any vulnerability beyond the minimal amount of testing required to prove that the vulnerability exists or to identify an indicator related to that vulnerability.

* Reporters MUST NOT intentionally access the content of any communications, data, or information transiting or stored on`ORGANIZATION`'s information system(s) – except to the extent that the information is directly related to a vulnerability and the access is necessary to prove that the vulnerability exists.

* Reporters MUST NOT exfiltrate any data under any circumstances.

* Reporters MUST NOT intentionally compromise the privacy or safety of`ORGANIZATION`'s personnel, customers, the general public, or any legitimate third parties.

* Reporters MUST NOT use any exploit to compromise, alter, or exfiltrate data

* Reporters SHOULD NOT establish command line access and/or persistence

* Reporters MUST NOT exploit any vulnerabilities found to pivot to other systems.

* Reporters MUST NOT intentionally compromise the intellectual property or other commercial or financial interests of any`ORGANIZATION`'s personnel or entities, customers, or any legitimate third parties.

* Reporters MUST NOT cause a denial of any legitimate services in the course of their testing.

* Reporters MUST NOT perform physical access testing (e.g. office access, open doors, tailgating, or other trespass).

* Reporters MUST NOT conduct social engineering in any form of`ORGANIZATION` personnel or contractors.

* Reporters SHOULD contact`ORGANIZATION` at POINT OF CONTACT if at any point you are uncertain of whether to proceed with testing.


## Coordination with `ORGANIZATION`

* Reporters SHOULD submit vulnerability reports to`ORGANIZATION` via`REPORTING CHANNEL`.

* Reporters MAY be eligible for one or more bug bounties. See`BUG BOUNTY` for details where applicable.

* Reporters SHOULD submit high quality reports.

* Reporters SHOULD include sufficient descriptive details to permit`ORGANIZATION` and/or the affected vendor(s) to accurately reproduce the vulnerable behavior.

* Reporters SHOULD NOT report unanalyzed crash dumps or fuzzer output unless accompanied by a sufficiently detailed explanation of how they represent a security vulnerability.

* Reporters SHOULD report other vulnerabilities found incidental to their in-scope testing even if those vulnerabilities would be otherwise considered out-of-scope. For example, while testing an in-scope system the reporter finds it to be exposing data from out-of-scope system. These are still reportable vulnerabilities.

* Reporters MUST keep confidential any information about vulnerabilities discovered for`SLC` after you have notified`ORGANIZATION`. Notwithstanding, this expectation does not preclude Reporters from simultaneously coordinating the vulnerability report with other affected parties (vendors, service providers, coordinators, etc.)

* Reporters MAY include a proof-of-concept exploit if available.

* Reporters MAY request that their contact information be withheld from all affected vendor(s).

* Reporters MAY request not to be named in the acknowledgements of`ORGANIZATION`'s public disclosures.

* Reporters MUST NOT submit a high-volume of low-quality reports.

* Reporters MUST NOT require`ORGANIZATION` to enter into a customer relationship, non-disclosure agreement (NDA) or any other contractual or financial obligation as a condition of receiving or coordinating vulnerability reports.

* Reporters MUST NOT demand compensation in return for reporting vulnerability information reported outside of an explicit bug bounty program.

## Coordination with vendors

* In the event that the Reporter finds a vulnerability in a`ORGANIZATION``SYSTEM SCOPE` consequent to a vulnerability in a generally available product or service, the Reporter MAY report the vulnerability to the affected vendor(s), service provider(s), or third party vulnerability coordination service(s) in order to enable the product or service to be fixed.

## Coordination with others

* Reporters MAY engage the services of a third party coordination service (e.g., CERT/CC, DHS CISA) to assist in resolving any conflicts that cannot be resolved between the Reporter and`ORGANIZATION`.

* Reporters SHOULD NOT disclose any details of any extant`ORGANIZATION``SYSTEM SCOPE` vulnerability, or any indicators of vulnerability to any party not already aware at the time the report is submitted to`ORGANIZATION`.


## Public disclosure

* Reporters MAY disclose to the public the prior existence of vulnerabilities already fixed by`ORGANIZATION`, including potentially details of the vulnerability, indicators of vulnerability, or the nature (but not content) of information rendered available by the vulnerability.

* Reporters choosing to disclose to the public SHOULD do so in consultation with`ORGANIZATION`.

* Reporters MUST NOT disclose any incidental proprietary data revealed during testing or the content of information rendered available by the vulnerability to any party not already aware at the time the report is submitted to`ORGANIZATION`.
