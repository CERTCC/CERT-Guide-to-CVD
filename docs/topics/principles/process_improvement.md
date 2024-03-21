# Process Improvement

<!--excerpt-start-->In reviewing their experience in the CVD process, participants should
capture ideas that worked well and note failures. This feedback can be
used to improve both the Software Development Lifecycle and the CVD
process itself.<!--excerpt-end-->

The CVD process can create a pipeline for regular patching cycles and
may reveal blocking issues that prevent a more efficient software patch
deployment mechanism. A successful program provides the vendor with a
degree of crowdsourcing for security research and testing of its
products. However, CVD should be considered complementary to a vendor's
internal research and testing as part of the Software Development
Lifecycle, not as a wholesale replacement for internally driven security
testing.

## CVD and the Security Feedback Loop

!!! example inline end "Milk or Wine"

    Andy Ozment and Stuart Schechter studied the impact of legacy code on the security
    of modern software and how large code changes might introduce 
    vulnerabilities in their 2006 paper
    [*Milk or Wine: Does Software Security Improve with Age?*](https://www.usenix.org/legacy/event/sec06/tech/full_papers/ozment/ozment.pdf)

    They found that over a 7.5 year span, nearly two-thirds of the lines of code in then-current versions
    of OpenBSD had not been altered during the study period. Furthermore, a similar fraction of reported vulnerabilities
    were present when the study began, representing accumulated security debt.
    The rate at which these foundational vulnerabilities were being reported was decreasing, but the decrease was not rapid.
    The median lifetime of foundational vulnerabilities was at least two and a half years.

A successful CVD program feeds vulnerability information back into the
vendor's Software Development Lifecycle. This information can result in
more secure development processes, helping to prevent the introduction
of vulnerabilities in the first place.
 
Yet the reality of today's software is that much of its legacy code was
not originally produced within a secure development process.
The positive news is that *foundational
vulnerabilities*&mdash;ones that existed in the very first release and
carried through the most recent version of the software&mdash;decay over
time. We can find them, fix them, and make the code base stronger
overall. However, the bad news is that as the low-hanging fruit of
foundational vulnerabilities are fixed, the remaining foundational
vulnerabilities tend to be more subtle or complex, making them
increasingly difficult to discover.


Furthermore, ongoing development and code changes can introduce new
vulnerabilities, making it unlikely for the security process to ever be
"finished." Even with modern architecture development and secure
coding practices, software bugs (and in particular security
vulnerabilities) remain a likely result as new features are added or
code is refactored. This can happen for many reasons, not all of them
technical. 

!!! example inline end "Bad Software Architecture is a People Problem"

    Kate Matsudaira's article in [ACM Queue](https://queue.acm.org/detail.cfm?id=2974011)
    highlights the difficulty of getting teams
    of people to work together, resulting in poor software architecture.
    While primarily concerned with maintainability
    and performance, bugs (including security vulnerability bugs) are
    an important side effect of inadequate architecture and teamwork
    process.

Another possibility is that, even with good internal processes and
teamwork, [no software model or specification can comprehensively account
for the variety of environments the software may operate in](https://www.computer.org/csdl/proceedings-article/csda/1998/03370026/12OmNrMHOcu). If we
cannot predict the environment, we cannot predict all the ways that
things may go wrong. In fact, [research](https://www.microsoft.com/en-us/research/blog/12-18-14-equation-of-a-fuzzing-curve-part-1-2/) has shown that it appears
[impossible](https://www.microsoft.com/en-us/research/blog/equation-of-a-fuzzing-curve-part-2-2/) to model or predict the number of vulnerabilities that may be
found through tools like fuzzing&mdash;and, by extension, [the number of
vulnerabilities that exist in a product](https://insights.sei.cmu.edu/library/an-analysis-of-how-many-undiscovered-vulnerabilities-remain-in-information-systems/). 


A successful CVD process helps encourage the search for and reporting of
vulnerabilities while minimizing harm to users. Developers supporting a
successful CVD process can expect to see the overall security of their
code improve over time as vulnerabilities are found and removed.

!!! tip "Expect Vulnerabilities to Persist"

    The best advice seems
    to be to assume that vulnerabilities will be found indefinitely into the
    future and work to ensure that any remaining vulnerabilities cause
    minimal harm to users and systems.

## Improving the CVD Process Itself

Feeding lessons learned back into the development process, CVD can:

- reduce creation of new vulnerabilities
- increase pre-release testing to find vulnerabilities

Participation in CVD may allow discussions between your developers and
security researchers on new tools or methods for vulnerability discovery
such as static analysis or fuzzing. These tools and methods can then be
evaluated for inclusion in ongoing development processes if they succeed
in finding bugs and vulnerabilities in your product. Essentially, CVD
can facilitate field testing of new analysis methods for finding bugs.
