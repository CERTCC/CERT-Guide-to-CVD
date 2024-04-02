# Independent Discovery

<!--start-->If one person can find a vulnerability, somebody else can, too.
When multiple parties independently discover the same vulnerability, it
can complicate the CVD process.<!--end-->

!!! example inline end "Research on Independent Discovery"

    Research has shown that vulnerabilities are often independently
    discovered.
    [Andy Ozment](https://web.archive.org/web/20220718203842id_/http://infosecon.net/workshop/pdf/10.pdf)
    showed that "vulnerability rediscovery occurs 'in the
    wild' and that it is not particularly uncommon."
    [Finifter and colleagues](https://www.usenix.org/conference/usenixsecurity13/technical-sessions/presentation/finifter),
    reviewing a dataset of Chrome vulnerabilities, identified 15
    out of 668 (2.25%) that had been independently discovered by multiple
    parties. They go on to mention similar rates for Firefox
    vulnerabilities.
    [Ablon and Bogart](https://www.rand.org/content/dam/rand/pubs/research_reports/RR1700/RR1751/RAND_RR1751.pdf)
    studied a stockpile of zero day vulnerabilities, estimating that "after a year approximately 5.7
    percent have been discovered and disclosed by others."
    [Herr and Schneier](https://ssrn.com/abstract=2928758)
    find browser vulnerabilities having rediscovery rates
    between 11% and 20% annually for the years 2013-2015. For Android
    vulnerabilities during the 2015-2016 timeframe, they found an annual
    rediscovery rate of 22%.

!!! question "What is to be done when the CVD process is underway for a vulnerability, and a seemingly independent report of the same vulnerability arrives?"

    Options include:

    1. accelerating public disclosure or 
    2. continuing with the CVD process.



## Accelerate Public Disclosure

One approach is to accelerate the disclosure timeline, possibly
disclosing immediately. This approach assumes that if a vulnerability
has been found and reported by multiple individuals acting
independently, then it must be an easy vulnerability to find. This in
turn implies that others who haven't reported it may also be aware of
its existence, thereby increasing the likelihood of its availability to
adversaries.

## Continue with the CVD Process

While we find this to be a reasonable conclusion, CVD participants
should be wary of duplicate reports that are not independent. Truly
independent discovery does yield some indication of the difficulty of
finding a vulnerability. But vulnerability finders and security
researchers talk to each other, and they sometimes hunt in the same
places. An announcement of interesting vulnerabilities in a product can
spur others to turn their attention and tools to that product. Even a
casual "I've been looking at product X and found some interesting
things" can put someone else on the hunt for vulnerabilities in product
X. Any judgement of independence should consider the degree to which
there is community interest in a product. As the popularity of products
wax and wane through their lifespan, so too will security researcher
attention.

<div class="grid" markdown>

!!! example "Heartbleed and Duplicate Reports"

    An example of a coordination failure occurred during the vulnerability
    disclosure of Heartbleed. Two organizations, Codenomicon and Google,
    both discovered the vulnerability around the same time. When the
    vulnerability was reported a second time to the OpenSSL team, the team
    assumed a possible leak and the vulnerability was quickly disclosed
    publicly ([source](http://www.smh.com.au/it-pro/security-it/heartbleed-disclosure-timeline-who-knew-what-and-when-20140414-zqurk.html)). A more coordinated response may have allowed further
    remediation to be available immediately at disclosure time.

!!! example "Bug Bounties and Duplicate Reports"

    Even more insidious is a phenomenon we've observed in bug bounty
    scenarios. Because they pay for reports, bug bounties can
    unintentionally provide incentives for finders to share their reports
    with others prior to reporting, allowing multiple individuals to report
    the same bug, and potentially share in a larger payout. CVD is a social
    game: as such, its incentives affect participants' behavior.

</div>

!!! tip "Consider Options on a Case-by-Case Basis"

    Rather than prescribing a single rule that independent discovery should
    immediately trigger release of the vulnerability information, we suggest
    that CVD participants discuss the implications of rediscovery on a
    case-by-case basis in order to decide the best course of action for the
    particular case.

{% include-markdown "../recipes/_x15.md" heading-offset=1 %}

