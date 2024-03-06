# Monitoring

CVD participants should maintain some level of monitoring for external activity that may materially affect their
prioritization or decision-making while handling a case.

!!! info inline end "CERT RMM Monitoring Process Area"

    The [Monitoring Process Area](https://insights.sei.cmu.edu/library/monitoring-mon-cert-rmm-process-area/) (MON)
    of the [CERT Resilience Management Model](https://insights.sei.cmu.edu/library/cert-resilience-management-model-cert-rmm-collection/) (CERT-RMM) 
    includes practices surrounding monitoring for security events, incidents, and other operationally relevant information.
    The CERT-RMM is a process improvement model designed to help organizations to improve their operational resilience.

## What to monitor for

While cybersecurity monitoring is a practice unto itself, there are some specific things that CVD participants should be on the lookout for
because they can affect the handling of a case. Items most directly relevant include:

| Type of Activity                        | Description                                                                               |
|-----------------------------------------|-------------------------------------------------------------------------------------------|
| Early publication outside of an embargo | Information about a vulnerability or exploit is made public before the embargo is lifted. |
| Exploit made public                     | An exploit for a vulnerability is made public.                                            |
| Attacks observed                        | Attacks are observed in the wild.                                                         |
| Parallel discovery                      | Someone else finds the same vulnerability.                                                |

Although usually less-specific to individual cases, the following are also important to monitor for anyone involved
in vulnerabilty management:

| Type of Information   | Description                                                               |
|-----------------------|---------------------------------------------------------------------------|
| Other vulnerabilities | Other vulnerabilities are discovered that may affect your infrastructure. |
| Adversary "chatter"   | Adversaries discussing a vulnerability or exploit.                        |
| New TTPs              | New adversary tactics, techniques, or procedures are observed.            |

## Information Sources

The following are some of the sources that CVD participants might choose to monitor:

| Monitoring Source        | Description                                                                                                                                                           |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inventory                | Paying attention to your infrastructure so you know what you have at risk.                                                                                            |
| Threat Feeds             | Paying attention to the world so that you have some sense of what adversary capabilities are. You want to know when adversaries gain new capabilities, like new TTPs. |
| Threat Hunting           | Paying attention to what adversaries are potentially doing on your infrastructure.                                                                                    |
| DFIR & Malware analysis  | Paying attention to what has already happened and the artifacts left behind by adversaries to notice when they gain new capabilities.                                 |
| Media reports            | Paying attention to what the world knows about vulnerabilities and exploits.                                                                                          |
| Conference presentations | Paying attention to what the technical and research community knows about vulnerabilities and exploits.                                                               |

!!! tip "Advice for Vendors"

    Vendors need to monitor for public information about security vulnerabilities in their products. Knowing about attacks and published exploits is key.

!!! tip "Advice for Deployers"

    Deployers need to monitor for public information about security vulnerabilities in the systems they have deployed (including reports coming as a result of the vendor's CVD process). They need to be on the lookout for fix announcements, mitigation advice, exploits, and attacks.
