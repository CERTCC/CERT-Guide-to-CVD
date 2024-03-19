# Roles in CVD

Certain roles are critical to the Coordinated Vulnerability Disclosure
process, as described in the following sections:

<div class="grid cards" markdown>

- :material-magnify: [**Finder (Discoverer)**](finder.md) -- the individual or organization that identifies the vulnerability
- :material-message-alert: [**Reporter**](reporter.md) -- the individual or organization that notifies the vendor of the vulnerability
- :material-code-braces: [**Vendor**](vendor.md) -- the individual or organization that created or maintains the product that is vulnerable
- :material-server: [**Deployer**](deployer.md) -- the individual or organization that must deploy a patch or take other remediation action
- :material-arrow-decision: [**Coordinator**](coordinator.md) -- an individual or organization that facilitates the coordinated response process
- :octicons-people-16: [**Other Roles**](other_roles.md) -- other roles that may be involved in the CVD process

</div>

!!! tip "Participants Can Play Multiple Roles"

    It is possible and often the case that individuals and organizations
    play multiple roles. For example, a cloud service provider might act as
    both vendor and deployer, while a researcher might act as both finder
    and reporter. A vendor may also be both a deployer and a coordinator. In
    fact, the CERT/CC has played all five roles over time, although not
    usually simultaneously.

## Relationships Between Roles

Although a more detailed description of the CVD process is provided in [Phases of CVD](../phases/index.md), a simple sketch of the relationships
between these roles is shown in the figure below.

```mermaid
---
title: CVD Role Relationships
---
flowchart TB
    subgraph A[Often Same Entity]
        Reporter([Reporter])
        Finder([Finder])
    end
    Vendor([Vendor])
    Coordinator([Coordinator])
    Deployer([Deployer])
        
    Finder -->|shares vul<br/>info with| Reporter
    Reporter -->|reports<br/>vul to| Vendor
    Vendor -->|coordinates<br/>with| Reporter
    Reporter -.->|reports<br/>vul to| Coordinator
    Coordinator -.->|coordinates<br/>with| Vendor
    Coordinator -.->|coordinates<br/>with| Reporter
    Vendor -.->|coordinates<br/>with| Coordinator
    Vendor -->|provides vul info<br/>and/or patch to| Deployer
    Deployer -->|provides</br>feedback to| Vendor
    Coordinator -.->|provides vul<br/>info to| Deployer
    Reporter -.->|provides vul<br/>info to| Deployer
    
```

An even simpler sketch of the relationships between these roles is shown in the figure below.

```mermaid
---
title: Coordination Relationships in CVD
---
flowchart TB
    subgraph C[Coordination]
        direction LR
        subgraph A[Often<br/>Same<br/>Entity]
            reporter([Reporter])
            finder([Finder])
        end
        vendor([Vendor])
        subgraph D[Sometimes<br/>Included]
            coordinator([Coordinator])
            deployer([Deployer])
        end
    end
    public([Public])
    
    finder <--> reporter
    reporter <--> vendor
    vendor <-.-> coordinator
    reporter <-.-> coordinator
    vendor <-.-> deployer
    coordinator <-.-> deployer
    reporter <-.-> deployer
    C -->|publish| public
```
