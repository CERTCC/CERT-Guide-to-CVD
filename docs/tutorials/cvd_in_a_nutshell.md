# The _CERT Guide to CVD_ in a Nutshell

Software-based products and services have vulnerabilities&mdash;conditions
or behaviors that allow the violation of an explicit or implicit
security policy. This should come as no surprise to those familiar with
software. What many find surprising nowadays is just how many products
and services should be considered _software based_. The devices we depend
on to communicate and coordinate our lives, transport us from place to
place, and keep us healthy have in recent years become more and more
connected both to each other and to the world at large. As a result,
society has developed an increasing dependence on software-based
products and services along with a commensurate need to address the
vulnerabilities that inevitably accompany them.

Adversaries take advantage of vulnerabilities to achieve goals at odds
with the developers, deployers, users, and other stakeholders of the
systems we depend on. Notifying the public that a problem exists without
offering a specific course of action to remediate it can result in
giving an adversary the advantage while the remediation gap persists.
Yet there is no optimal formula for minimizing the potential for harm to
be done short of avoiding the introduction of vulnerabilities in the
first place. In short, vulnerability disclosure appears to be a [wicked
problem](../topics/principles/wicked_problem.md).

Coordinated Vulnerability Disclosure (CVD) is a process for reducing
adversary advantage while an information security vulnerability is being
mitigated. [CVD is a process, not an event.](cvd_is_a_process.md) Releasing a patch or
publishing a document are important events within the process, but do
not define it.

{% include-markdown "../_includes/_core_questions_of_cvd.md" heading-offset=1 %}


CVD should not be confused with [Vulnerability Management](terms/vulnerability_management.md) (VM).
VM encompasses the process downstream of CVD, once the vulnerability has
been disclosed and deployers must take action to respond. 

!!! info "What's on this Page?"

    <!--start-->The _CERT Guide to CVD in a Nutshell_ provides an overview of many of the topics covered
    later in this documentation, with links to more detailed information. We're providing
    it here as a preview of what's to come as you work through the remainder of the site.<!--end-->

{% include-markdown "../topics/index.md" heading-offset=1 %}
{% include-markdown "../howto/index.md" heading-offset=1 %}
<!-- 
{% include-markdown "../topics/principles/index.md" heading-offset=1 %}
{% include-markdown "../topics/roles/index.md" heading-offset=1 %}
{% include-markdown "../topics/phases/index.md" heading-offset=1 %}
{% include-markdown "../howto/preparation/index.md" heading-offset=1 %}
{% include-markdown "../howto/initiation/index.md" heading-offset=1 %}
{% include-markdown "../howto/coordination/index.md" heading-offset=1 %}
{% include-markdown "../howto/operation/index.md" heading-offset=1 %}
-->
{% include-markdown "../reference/index.md" heading-offset=1 %}
