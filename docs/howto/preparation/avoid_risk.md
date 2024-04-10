# Avoid Unnecessary Risk in Finding Vulnerabilities

<!--start-->Looking for vulnerabilities in software and hardware is a critical part of
the security ecosystem. However, it is important to do so in a way that
minimizes the potential for harm to others.<!--end-->
This section provides advice for
finders and vendors on how to avoid unnecessary risk when finding
vulnerabilities.

<div class="grid" markdown>

!!! tip "Advice for Finders"

    Finders should exercise an appropriate degree of care when performing
    vulnerability research. This will help to alleviate legal concerns and
    limit the potential for damage to others.
    Vulnerability research should of course be performed on equipment that
    the finder is authorized to use for the purpose. If the research is
    performed on behalf of an organization such as a private security firm
    or university, permission should be obtained before attempting research
    on organization-owned equipment. 

!!! tip "Advice for Vendors"

    Likewise, organizations should make the rules and process for obtaining
    permission very clear and easy to find. For example, a form or email
    address provided on an intranet page might be sufficient. Employees
    hired specifically to find vulnerabilities should be briefed on
    necessary rules and provided with concrete permission as part of the
    on-boarding process. Failure to adequately document permissible scope
    and authority for vulnerability testing can lead to frustration and
    other negative consequences with various legal ramifications.

</div>

## Types of Risk

There are several types of risk that should be considered when
performing vulnerability research. These include operational risk,
safety risk, and legal risk.

<div class="grid" markdown>

!!! warning "Operational Risk"

    In general, the software or devices tested should not be production
    systems that support or have access to real data or users. When
    possible, dedicated, controlled testing environments should be
    established. Such a testing environment often consists of virtual
    machines (VMs) in a virtual network firewalled off from any production
    network. Even as a finder in a controlled testing scenario, you should
    keep in mind the potential for unintended consequences (i.e., the
    unknown unknowns). Always try to limit the potential for unintended
    negative impact of testing, even within your controlled environment. If
    the impact cannot be constrained to a controlled environment with
    relatively known consequences, do not attempt to test your exploit and
    instead report your findings directly to the vendor.

!!! warning "Safety Risk"

    [Safety-critical systems](https://ieeexplore.ieee.org/document/1007998)
    have been defined as "systems whose failure
    could result in loss of life, significant property damage, or damage to
    the environment." A high degree of caution is both appropriate
    and necessary when testing the security of safety-critical systems, such
    as medical devices, industrial equipment, or vehicles. A proof of
    concept exploit to demonstrate a vulnerability on a traditional computer
    might cause a calculator to pop up on the screen. A proof of concept
    exploit on a car might cause it to behave erratically, potentially
    leading to injury or death. Testing or demonstrating safety-critical
    systems outside a controlled environment, or when there is any chance of
    harming unwitting bystanders is unacceptable under any
    circumstances.

</div>

!!! warning "Legal Risk"

    Depending on the circumstances, finders may be subject to a
    non-disclosure agreement (NDA) regarding any vulnerabilities found. This
    is often the case when vulnerability testing is performed on behalf the
    vendor whether directly as an employee, or under contract as part of a
    consulting firm or as a freelance consultant. Finders should be aware of
    this possibility and consider the legal implications of any relevant
    NDAs before reporting a vulnerability to any third party.

    That said, vendors are strongly encouraged to avoid requiring NDAs of
    reporters if at all possible. Many finders prefer to avoid the legal
    entanglements that NDAs entail and will be discouraged from reporting
    vulnerabilities when an NDA is involved.  This can leave vendors unaware
    of potential threats to their products and services and in turn, their
    users.
    
    Additionally, in some environments, such as medical devices, healthcare,
    education, or financial information systems, there may be legal
    consequences to accessing real data (under
    [HIPAA](https://www.hhs.gov/hipaa/),
    [FERPA](https://ed.gov/policy/gen/guid/fpco/ferpa/index.html),
    [COPPA](https://www.ftc.gov/enforcement/rules/rulemaking-regulatory-reform-proceedings/childrens-online-privacy-protection-rule),
    and similar laws, industry standards such as [PCI DSS](https://www.pcisecuritystandards.org/pci_security/),
    etc.), so we again reiterate the need to perform research only in
    controlled test environments, preferably with fake data.
    
    For more information on the legal implications of vulnerability
    disclosure, we refer you to the [*EFF's Coders' Rights Project
    Vulnerability Reporting FAQ*](https://www.eff.org/issues/coders/vulnerability-reporting-faq).
