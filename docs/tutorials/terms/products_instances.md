# Products and Instances

In talking about things that have vulnerabilities, we try to maintain a
clear distinction between a *product* being vulnerable, and an *instance
of a product* being vulnerable.

!!! abstract "Product"

    A *product* is a software or hardware system that is released by a
    vendor or manufacturer. A product is a general concept that can be
    instantiated in many different ways.

!!! abstract "Instance"

    An *instance* is a specific deployment of a product. An instance is
    a concrete realization of a product that is running on a specific
    system.

One way to think about this distinction is to consider the difference between
the make and model of a car (the product) and a *specific* car (the instance).
In that context, the *product* is actually a category of cars that share certain characteristics,
components, and features. A specific car that belongs to that category would be considered
an *instance*.

!!! example "Product vs. Instance"

    Consider a vulnerability in Windows 11. Windows 11 is a _product_
    that is released by Microsoft. If there is a vulnerability in
    Windows 11, then the _product_ Windows 11 is vulnerable, as are all
    _instances_ of Windows 11 that have not been patched against the
    vulnerability.

    Now consider a specific server that is running Windows 11. This server is an
    _instance_ of the _product_ Windows 11. If the server has been configured
    in such a way that it is vulnerable to attack (e.g., it has not been
    patched against a vulnerability in the _product_ Windows 11),
    then the _instance_ of Windows 11 is vulnerable.

!!! tip "Why the Distinction Matters"

    Vulnerabilities affecting products may not always affect every instance
    of a product; for example, a vulnerability may require a special
    configuration or setup to be exploited, so any instance not in that
    configuration state would actually be unaffected by the vulnerability,
    despite the product at-large being vulnerable.

    Alternately, it is possible for an instance to be vulnerable even if the
    product is not. For example, a vulnerability may be introduced by a
    misconfiguration such as an insecure permission setting. In this case,
    the product itself would not be considered to have a vulnerability, but the instance
    would.

This distinction becomes important when one is talking about the
practices associated with [Vulnerability Management](vulnerability_management.md)
(VM)&mdash;namely
[*vulnerability scanning*](vulnerability_scanning.md)&mdash;in contrast to CVD and
[*vulnerability discovery*](vulnerability_discovery.md).

VM entails the identification of *instances* of a *product*
on which action must be taken to remediate known vulnerabilities in the
product. VM is concerned with the eradication of the *instances* of known
vulnerabilities in deployed systems, whereas CVD is concerned with the
repair of vulnerabilities at the *product* level.
