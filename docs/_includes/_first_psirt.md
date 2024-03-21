!!! info "FIRST PSIRT Services Framework"

    !!! info inline end ""

        ```mermaid
        ---
        title: PSIRT Services Framework
        ---
        
        flowchart TD
            subgraph sa[Service Areas]
            direction TB
            sa1[Stakeholder<br/>Ecosystem<br/>Management]
            sa2[Vulnerability<br/>Discovery]
            sa3[Vulnerability<br/>Triage]
            sa4[Vulnerability<br/>Remediation]
            sa5[Vulnerability<br/>Disclosure]
            sa6[Training &<br/>Education]
            end
            of[Organizational<br/>Foundations]
            of ~~~ sa
            sa1 ~~~ sa2
            sa2 ~~~ sa3
            sa6 ~~~ sa4
            sa4 ~~~ sa5

        ```

    FIRST has published a
    [PSIRT Services Framework](https://www.first.org/standards/frameworks/psirts/psirt_services_framework_v1.1) that
    provides a comprehensive guide to the services that a PSIRT can provide.
    It is organized into Service Areas, Services, Functions, and Sub-Functions.
    The diagram at right shows the top-level Service Areas.
