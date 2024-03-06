# Discovery

Aside from the simplest applications, software development is difficult,
complex, and prone to error. As a result, the likelihood that any given
software-based product or component is free of vulnerabilities is
extremely low. For vendors, this implies the need to create a response
capability to handle vulnerability reports, whether those reports come
from sources internal or external to the vendor.

!!! question "Why Look for Vulnerabilities?"

    Ultimately, we can't fix vulnerabilities we don't know about. While
    software engineering best-practices, code audits, testing (including
    fuzzing), and application security testing are important parts of the
    development lifecycle, security research is important for rooting out
    hidden vulnerabilities. Some organizations may have in-house expertise
    to find and identify security vulnerabilities, but most will not. For
    some vendors, encouraging independent vulnerability finders may be the
    only way to stay on top of the latest trends in vulnerability research
    and exploitation techniques.

!!! tip "Be Wary of Null Results"

    Many organizations hire application security testers or code auditors to
    look for vulnerabilities. While such testing is certainly important and
    commendable, it is important to understand that absence of evidence is
    not always evidence of absence.
    [Rumsfeld's point about unknown unknowns](https://en.wikipedia.org/wiki/There_are_unknown_unknowns)
    applies here.

    > Reports that say that something hasn’t happened are always interesting to me,
    > because as we know, there are known knowns; there are things we know we know.
    > We also know there are known unknowns; that is to say we know there are some
    > things we do not know. But there are also unknown unknowns – the ones we don’t
    > know we don’t know.

    A clean audit or pen test report should not be taken as
    evidence that the software is free of vulnerabilities. All
    software-based systems have problems we're not even aware of and so we
    don't even know to look for them. Because such vulnerabilities may
    exist and can be exploited without warning, vendors and deployers should
    establish their VR capability in preparation for this eventuality.

{% include-markdown "../../howto/avoid_risk.md" heading-offset=1 %}
