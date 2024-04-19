# Basic Vulnerability Report Form

Organizations that need to receive vulnerability reports should have a form that helps them collect the necessary
information.
This form should be easy to use and understand, and should help the reporter provide the information needed to
understand and address the vulnerability.
Specific details may vary depending on the organization's needs and its role(s) in the CVD process
([Vendor](../topics/roles/vendor.md), [Coordinator](../topics/roles/coordinator.md), etc.), but
much of the content will be the same across organizations.

This page contains a report example based on the CERT/CC's [Vulnerability
Reporting Form](https://www.kb.cert.org/vuls/report/), and is not meant to be exhaustive of all possibilities.
Please modify the sections and format as necessary to better suit your
needs.

## Vulnerability Report

!!! question "Tell us about the Vulnerability"

    - Software/Product(s) containing the vulnerability 
    - Vulnerability Description
    - How may an attacker exploit this vulnerability? (Proof of Concept)
    - What is the impact of exploiting this vulnerability? (What does an attacker gain that the attacker didn't have before?)
    - How did you find the vulnerability? (Be specific about tools and versions you used.)
    - When did you find the vulnerability?

!!! question "What are your disclosure plans?"

    - Have you already reported this vulnerability to the following vendors and organizations? YES | NO
    - Is this vulnerability being publicly discussed? YES | NO
      
      - If yes, provide URL:
    
    - Is there evidence that this vulnerability is being actively exploited? YES | NO

      - If yes, then provide URL/evidence.

    - I plan to publicly disclose this vulnerability YES/NO

      - ...on this date (Please include your time zone.)
      - ...at this URL

!!! question "What are your contact details?"

    - Name
    - Organization
    - Email
    - PGP Public Key (ASCII Armored or a URL) 
    - Telephone
    - May we provide your contact information to third parties? YES | NO
    - Do you want to be publicly acknowledged in a disclosure? YES | NO

!!! question "Any Additional Information?"

    - Vendor Tracking ID, CERT Tracking ID, or CVE ID if known:
    - Additional Comments:
