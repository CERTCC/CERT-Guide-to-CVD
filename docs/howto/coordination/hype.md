# Hype, Marketing, and Unwanted Attention

!!! example inline end "Branded Vulnerabilities"

    In recent years we've witnessed the rise of branded vulnerabilities, including
    [Heartbleed](https://nvd.nist.gov/vuln/detail/CVE-2014-0160),
    [Poodle](https://nvd.nist.gov/vuln/detail/CVE-2014-3566),
    [Badlock](https://nvd.nist.gov/vuln/detail/CVE-2016-2118),
    [Shell Shock](https://nvd.nist.gov/vuln/detail/CVE-2014-6271),
    [GHOST](https://nvd.nist.gov/vuln/detail/CVE-2015-0235),
    [Spectre and Meltdown](https://nvd.nist.gov/vuln/detail/CVE-2017-5753).

<!--start-->Is a branded vulnerability more dangerous than one without?
Not in any technical sense, no. Instead, what it does is
draw additional attention&mdash;which can lead to vendors being
forced to adjust the priority of the vulnerability cases they're
working on and allocate resources toward addressing whatever 
vulnerability is getting the hype.<!--end--> 

!!! question "Are branded vulnerabilities good or bad for internet security?"
    
    The only good answer is the lesson of the Taoist [parable of the farmer and the horse](https://en.wikipedia.org/wiki/The_old_man_lost_his_horse): "Maybe."



## The Streisand Effect

Attempts to squash true information once it's been revealed tends not
only to spread the information more widely, but also to backfire on
whoever is trying to conceal it.
The [name](https://www.techdirt.com/articles/20150107/13292829624/10-years-everyones-been-using-streisand-effect-without-paying-now-im-going-to-start-issuing-takedowns.shtml),
coined by [Mike Masnick](https://www.techdirt.com/user/mmasnick/),
comes from a case involving
the removal of online photos of a famous celebrity's house. The
attempt to suppress the photos only drew attention to them resulting in
many more people seeing them than would have otherwise.

This scenario comes up from time to time in CVD cases. Often it takes
the form of a vendor trying to suppress the publication of a report
about a vulnerability in its product, with some threat of legal action
if the information is released. As we've discussed previously, the
knowledge that a vulnerability exists in some feature of a product can
be sufficient for a knowledgeable individual to rediscover the
vulnerability. The legal threats usually serve to amplify the discussion
of the case within the security community, which draws more attention to
the vendor and its products at the same time it demotivates reporters'
willingness to participate in the CVD process. Even more problematic is
that when such attention comes to focus on the vendors' products, it is
very likely that additional vulnerabilities will be found&mdash;while
simultaneously less likely that anyone will bother to report them to the
vendor before disclosing them publicly. 

!!! tip "Beware The Power of Spite"

    Vendors should not underestimate spite as a motivation for vulnerability discovery.


{% include-markdown "../recipes/_x20.md" heading-offset=1 %}
{% include-markdown "../recipes/_x05.md" heading-offset=1 %}
