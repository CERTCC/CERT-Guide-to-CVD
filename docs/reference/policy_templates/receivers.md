# Vulnerability Disclosure Policy Templates for Receivers

<!--start-->This collection of policy statement templates describe expectations for organizations
receiving vulnerability reports.<!--end-->
Report Receivers might include
[Vendors](../../topics/roles/vendor.md),
[Coordinators](../../topics/roles/coordinator.md),
[Deployers](../../topics/roles/deployer.md),
or other organizations that receive vulnerability reports.

## Tips and Usage Notes

{% include-markdown "./_usage.md" %}
{% include-markdown "./_terminology.md" %}
{% include-markdown "./_consistency_warning.md" %}

## Template Policy Statements

`ORGANIZATION` SHALL deal in good faith with Reporters who discover, test, and report vulnerabilities or indicators of vulnerabilities in accordance with these guidelines.

## General

* `ORGANIZATION` MAY modify the terms of this policy or terminate the policy at any time.

* `ORGANIZATION` SHALL use information reported to this program for defensive purposes only; to mitigate or remediate vulnerabilities in our networks or applications, or the applications of our vendors.

## Case handling

* `ORGANIZATION` MAY, at our discretion, decline to coordinate or publish a vulnerability report. This decision is generally based on the scope and severity of the vulnerability and our ability to add value to the coordination and disclosure process.

* In the event that`ORGANIZATION` declines to coordinate a vulnerability report, the Reporter SHOULD proceed to coordinate with any other affected vendor(s). Additionally, the Reporter MAY proceed with public disclosure at their discretion.

* `ORGANIZATION` SHALL investigate every reported vulnerability and strive to ensure that appropriate steps are taken to mitigate risk and remediate reported vulnerabilities.

* `ORGANIZATION` SHALL, to the best of our ability, validate the existence of the vulnerability

* `ORGANIZATION` SHALL determine an appropriate timeframe for mitigation development and deployment for vulnerabilities reported in systems it controls.

## Coordination with reporters

* `ORGANIZATION` SHALL acknowledge receipt of vulnerability reports via email within`SLC`.

* `ORGANIZATION` MAY contact the Reporter for further information.

* `ORGANIZATION` SHALL inform the Reporter of the results of our validation, as appropriate, and accordingly provide status updates as remediation of the vulnerability is underway.

* `ORGANIZATION` SHALL include credit to the reporter in any published vulnerability report unless otherwise requested by the reporter.

* In the event that`ORGANIZATION` chooses to publicly disclose the reported vulnerability,`ORGANIZATION` SHALL recognize your contribution to improving our security if you are the first to report a unique vulnerability, and your report triggers a code or configuration change.

* `ORGANIZATION` MAY forward the name and contact information of the Reporter to any affected vendors unless otherwise requested by the reporter.

* `ORGANIZATION` SHALL forward the name and contact information of the reporter to the affected vendors unless otherwise requested by the reporter.

* `ORGANIZATION` SHALL advise the reporter of significant changes in the status of any vulnerability he or she reported to the extent possible without revealing information provided to us in confidence.

* `ORGANIZATION` MAY adjust its publication timeframe to accommodate reporter constraints if that timing is otherwise compatible with this policy. In most cases such an adjustment would be expected to represent a delay rather than an acceleration of the publication schedule. Examples include delaying publication to coincide with conference presentations.

* `ORGANIZATION` SHALL NOT require Reporters to enter into a customer relationship, non-disclosure agreement (NDA) or any other contractual or financial obligation as a condition of receiving or coordinating vulnerability reports.

## Coordination with vendors

* In the event that`ORGANIZATION` determines the reported vulnerability is consequent to a vulnerability in a generally available product or service,`ORGANIZATION` MAY report the vulnerability to the affected vendor(s), service provider(s), or third party vulnerability coordination service(s) in order to enable the product or service to be fixed.

* `ORGANIZATION` SHALL make a good faith effort to inform vendors of reported vulnerabilities prior to public disclosure.

* `ORGANIZATION` SHALL forward vulnerability reports to the affected vendor(s) as soon as practical after we receive the report.

* `ORGANIZATION` SHALL apprise any affected vendors of our publication plans and negotiate alternate publication schedules with the affected vendors when required.

* `ORGANIZATION` SHALL provide the vendor the opportunity to include a vendor statement within our public disclosure document.

* `ORGANIZATION` SHALL NOT withhold vendor-supplied information simply because it disagrees with our assessment of the problem.

* `ORGANIZATION` SHALL notify affected vendors of any public disclosure plans.

* `ORGANIZATION` SHALL NOT reveal information provided in confidence by any vendor.

* `ORGANIZATION` SHALL act in accordance with the expectations of Reporters set forth in this policy when acting as a Reporter to other organizations (vendors, coordinators, etc.).

## Coordination with others

* `ORGANIZATION` MAY engage the services of a third party coordination service (e.g., CERT/CC, DHS CISA) to assist in resolving any conflicts that cannot be resolved between the Reporter and`ORGANIZATION`.

* `ORGANIZATION` MAY, at our discretion, provide reported vulnerability information to anyone who can contribute to the solution and with whom we have a trusted relationship, including vendors (often including vendors whose products are not vulnerable), service providers, community experts, sponsors, and sites that are part of a national critical infrastructure, if we believe those sites to be at risk.

## Public disclosure

* `ORGANIZATION` SHALL determine the type and schedule of our public disclosure of the vulnerability.

* `ORGANIZATION` MAY disclose reported vulnerabilities reported to the public N days after the initial report, regardless of the existence or availability of patches or workarounds from affected vendors.

* `ORGANIZATION` MAY disclose vulnerabilities to the public earlier or later than N days due to extenuating circumstances, including but not limited to active exploitation, threats of an especially serious (or trivial) nature, or situations that require changes to an established standard.

* `ORGANIZATION` MAY consult with the Reporter and any affected vendor(s) to determine the appropriate public disclosure timing and details.

* `ORGANIZATION` SHALL balance the need of the public to be informed of security vulnerabilities with vendors' need for time to respond effectively.

* `ORGANIZATION`'s final determination of a publication schedule SHALL be based on the best interests of the community overall.

* `ORGANIZATION` SHALL publish public disclosures via`PUBLICATION CHANNEL`.

* `ORGANIZATION` MAY disclose to the public the prior existence of vulnerabilities already fixed by`ORGANIZATION`, including potentially details of the vulnerability, indicators of vulnerability, or the nature (but not content) of information rendered available by the vulnerability.

* `ORGANIZATION` SHALL make our disclosure determinations based on relevant factors such as but not limited to: whether the vulnerability has already been publicly disclosed, the severity of the vulnerability, potential impact to critical infrastructure, possible threat to public health and safety, immediate mitigations available, vendor responsiveness and feasibility for creating an upgrade or patch, and vendor estimate of time required for customers to obtain, test, and apply the patch. Active exploitation, threats of an especially serious nature, or situations that require changes to an established standard may result in earlier or later disclosure.

* `ORGANIZATION` MAY disclose product vulnerabilities`SLC` after the initial contact is made, regardless of the existence or availability of patches or workarounds from affected vendors in cases where a product is affected and the vendor is unresponsive, or fails to establish a reasonable timeframe for remediation.
