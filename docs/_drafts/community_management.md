# Community Management

Remediating system vulnerabilities requires groups of people to work together to achieve a common goal.
From the initial discovery of a vulnerability to the final deployment of a patch, many different stakeholders are involved in the process.
Organizations that serve as Coordinators of the vulnerability disclosure process must manage relationships with these stakeholders to ensure that the process is successful.
Often, these organizations must also manage relationships with other organizations that are not directly involved in the vulnerability disclosure process but are affected by it.
We refer to these groups of people as "communities of interest."

!!! tip "_Community Management_ is closely related to _Policy Management_"

    [_Policy Management_](./policy_management.md) is about defining the rules and guidelines that govern the
    vulnerability disclosure process
    for a particular organization or community.
    Disclosure policies define the scope of the organization's interest in vulnerability reports, the exceptions
    to the policy, and the safe harbor provisions for reporters.
    They can also include requirements for who will be engaged during the disclosure process and how they will be engaged.
    
    In contrast, _Community Management_ is about the relationships that an organization must maintain with the people and
    organizations involved in the vulnerability disclosure process over time.
    This includes maintaining relationships with the people who report vulnerabilities, the vendors who must fix them, and the deployers who must install the fixes.
    
    One might think of _Policy Management_ as defining the rules of the game, while _Community Management_ is about
    developing and maintaining a pool of players who are willing to play by those rules.

## Communities of Interest

We can categorize the communities of interest in the vulnerability disclosure process in several ways.

### By Role

One way is to categorize them by their role in the process.

#### Finder/Reporter Communities

<!-- security conferences, online communities, social media -->

<!--
Maintaining good relationships with the finder/reporter community.
Outreach, conferences, etc.
-->

#### Vendor/Developer Communities

<!-- commercial software vendors, service providers, open source projects -->

#### Deployer/Operator Communities

<!-- system administrators, IT managers, security operations teams, operational technology staff -->

#### Coordinator Communities

<!-- Coordinators, incident response teams, CSIRTs, PSIRTS, etc. -->

### By Technology Affinity

Another way to categorize communities of interest is by the technology type affected by the vulnerability.
Often used by Coordinators

<!--
often associated with protocols, standards, or generalized technology implementations
DNS, routing, IPv6, VOIP, UEFI, SNMP, TCP,

cross-cutting technologies such as libraries, architectures, or programming languages
many vendors might have affected products
source of many MPCVD cases
-->

### By Industry Affinity

<!-- ISACs and ISAOs, industry groups, trade associations, etc. -->

### By Geography or Jurisdiction

<!-- national CSIRTs, regional CSIRTs, local governments, industry groups, etc. -->

<!-- Revise/rewrite this.

 
Some content from elsewhere might move here. 
Close to policy, but more operational.
Who do you include in a notification? 
Who do you exclude? How do you maintain relationships outside of individual case handling? 
etc.

For coordinators, each case in the CVD process affects some set of stakeholders.
One way of organizing stakeholders is by technology type.
For example, the CERT/CC groups vendors into groups by technology (networking, operating systems, DNS, etc.). 
When a case arrives that affects multiple vendors' products in the networking space (like VU\#962459), we will notify the vendors in the networking group.

Of course, this means we need to be able to trust the vendors we notify with that information.
The more fundamental the technology, the larger the group we need to notify.
The larger the group we notify, the more likely it is for information to leak early.
This creates a tension: the deeper the problem is, the more things are affected by it, but the shorter the embargo needs to be to avoid early disclosure.
-->

