# Roles in CVD

Certain roles are critical to the Coordinated Vulnerability Disclosure
process, as described in the following sections:

<div class="grid cards" markdown>

- [**Finder (Discoverer)**](finder.md) -- the individual or organization that identifies the vulnerability
- [**Reporter**](reporter.md) -- the individual or organization that notifies the vendor of the vulnerability
- [**Vendor**](vendor.md) -- the individual or organization that created or maintains the product that is vulnerable
- [**Deployer**](deployer.md) -- the individual or organization that must deploy a patch or take other remediation action
- [**Coordinator**](coordinator.md) -- an individual or organization that facilitates the coordinated response process

</div>

!!! tip "Participants Can Play Multiple Roles"

    It is possible and often the case that individuals and organizations
    play multiple roles. For example, a cloud service provider might act as
    both vendor and deployer, while a researcher might act as both finder
    and reporter. A vendor may also be both a deployer and a coordinator. In
    fact, the CERT/CC has played all five roles over time, although not
    usually simultaneously.

## Relationships Between Roles

Although a more detailed description of the CVD process is provided in Section 4, a simple sketch of the relationships
between these roles is shown in the figure below.

```mermaid
---
title: CVE Role Relationships
---
flowchart TD
    subgraph A[Often Same Entity]
        Reporter
        Finder
    end
    Finder -->|shares vul info with| Reporter
    Reporter -->|reports vul to| Vendor
    Vendor -->|coordinates with| Reporter
    Reporter -.->|reports vul to| Coordinator
    Coordinator -.->|coordinates with| Vendor
    Coordinator -.->|coordinates with| Reporter
    Vendor -.->|coordinates with| Coordinator
    Vendor -->|provides vul info<br/>and/or patch to| Deployer
    Deployer -->|provides</br>feedback to| Vendor
    Coordinator -.->|provides vul<br/>info to| Deployer
    Reporter -.->|provides vul<br/>info to| Deployer
    
```
