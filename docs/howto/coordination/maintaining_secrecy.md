# Maintaining Pre-Disclosure Secrecy

[Multiparty disclosure](mpcvd.md) highlights the need to balance need-to-know with need-to-share. 
<!--start-->The more parties involved in a case, and the longer the embargo period
lasts, the more likely a leak becomes.<!--end-->

!!! question "Who Needs to Know What, When?"

    There are varying degrees of need-to-know.
    Not everyone needs to know the same thing at the same time.
    Patch originators are usually notified early in the process, since their answer to
    "What do I need to do in response to this knowledge?" (i.e., create a patch)
    is often on the critical path for any downstream parties to be able to take action.
    Downstream vendors (patch consumers) and deployers can be notified later.

## The Risk of Leaks

Keeping secrets over time is hard.
[The more people who know a secret, the more likely it is to leak.](https://doi.org/10.1371/journal.pone.0147905)
Simple probability theory tells us that even if the probability of any
given party leaking is very low, the cumulative probability of a leak
increases exponentially with the number of parties involved.

!!! example "Larger Cases Face Increased Leak Risk"

    While it's hard to measure the actual probability of a leak in a given case,
    it's clear that the more parties involved, the more likely a leak becomes.
    For example, let's say that the probability of any given party leaking during
    a given case is $1$ in $1000$.
    If there are $10$ parties involved, the probability that
    none of them leak is $0.999^{10}$, or about 99%.
    If there are $100$ parties involved, the probability that none of them leak is only
    $0.999^{100}$, or about 90%.
    But if there are $1000$ parties involved, the probability that none of them leak is only $0.999^{1000}$, 
    or about 37%, meaning that the probability that at least one of them leaks is about 63%.

    Lest you think that $1000$ participants in a case is an unrealistic number, consider that
    in the Apache Log4j case [VU#930724](https://kb.cert.org/vuls/id/930724) 
    ([CVE-2021-44228](https://nvd.nist.gov/vuln/detail/CVE-2021-44228),
    [CVE-2021-4104](https://nvd.nist.gov/vuln/detail/CVE-2021-4104),
    [CVE-2021-45046](https://nvd.nist.gov/vuln/detail/CVE-2021-45046),
    the CERT/CC notified $1643$ vendors, and we're reasonably certain that we missed more than a few.

!!! tip "Keep Embargoes Short"

    Controlling the number of participants involved in a case is one way to reduce the risk of a leak.
    But if we want to reach all the vendors with affected products, we often can't avoid involving many parties.
    And every vendor involved is likely to have multiple people involved in the case.
    So even in a case with only a few vendors, the number of individuals involved can quickly grow into the hundreds.
    Furthermore, the broader the audience for an embargoed disclosure, the more likely that it will involve
    parties who are not used to handling embargoed information, or who have different values or priorities, 
    leading to a higher risk of a leak.

    A more reliable way to reduce the risk of a leak is to keep the embargo period as short as possible.
    The longer the embargo, the more likely a leak becomes, regardless of the number of parties involved.
    That doesn't mean you should rush the process (because that can lead to other problems including loss of 
    trust due to incomplet or incorrect patches), but it does mean you should beware the risks of a long embargo.


## Coordinating Further Downstream

Vulnerabilities having the potential for significant impact can lead to
coordination efforts beyond the traditional product vendor space.

!!! question "Do You Include Deployers?"

    Infrastructure and service providers are sometimes brought in early, if
    there are mitigations that can be deployed in advance of the
    availability of a fix. This can be especially helpful in cases where the
    vulnerability may affect the infrastructure necessary to distribute the
    patch in the first place.

    Be careful to consider fairness though: By what criteria should you
    notify _service provider X_ but not _service provider Y_? At some point, the
    complexity of who knows what gets high enough that the likelihood of a
    leak goes to 1, and you might as well go public.

!!! warning "Complex Communications Reduce Trust"

    It's also important to be aware that not all participants along the
    chain of disclosure will be equally trustworthy. That's not to say they
    are actively malicious, just that they may have incompatible values or
    priorities that lead them to disclose the existence of the vulnerability
    to others earlier than you'd prefer.
