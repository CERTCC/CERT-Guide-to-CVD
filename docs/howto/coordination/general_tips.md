# What to Do When Things Go Wrong

<!--start-->While we can't tell you what to do in every possible combination of
contingencies that may arise in the CVD process, we can suggest a few
guidelines to help you navigate the complexity.<!--end-->

!!! tip "Keep Calm and Carry On"

    Although problems with the disclosure process can be stressful, it's
    better to keep emotions in check while resolving issues. Recall from
    [Presume Benevolence](../../topics/principles/presume_benevolence.md) 
    that a presumption
    of benevolence is helpful when navigating the CVD process. As we have
    described in [CVD Problem Solving](index.md),
    multiple things can go wrong in the disclosure process, but often these
    problems do not arise as a result of intentional acts of malice. So even
    if something has gone wrong, it's still good to give the benefit of the
    doubt to the good intentions of the involved stakeholders.

!!! tip "Avoid Legal Entanglements"

    Whatever the issue is in the context of a vulnerability disclosure,
    lawyers alone are rarely the right answer. Cease-and-desist letters tend
    to backfire as described in [Hype](hype.md).
    
    Responding with legal threats can have negative public relations effects
    in the long term for vendors as well:

    -   It gives the appearance that the vendor is more concerned about protecting its image than users' security.
    -   It can give the impression that the organization is bullying an individual.
    -   It can drive future researchers away from reporting the vulnerabilities they find.

<div class="grid cards" markdown>

!!! tip "Recognize the Helpers: Vendors"

    A person who shows up at your door to tell you about a
    vulnerability in your product is not the enemy. That person is your
    friend.

!!! tip "Recognize the Helpers: Finders/Reporters"

    A vendor who is responsive is doing better than many.

</div>

!!! tip "Recognize the Helpers: Everyone"

    !!! example inline end "CVD Motivations"
    
        [I am the Cavalry](https://www.iamthecavalry.org/motivations/) lists five motivations for security researchers:
        Protect, Puzzle, Prestige, Profit, and Protest/Patriotism.

    Give credit where it's due. 
    Many participants in CVD are there because they care about making things better.
    Recognizing them for their good work keeps them engaged and helps everybody in the long run.

!!! tip "Consider Publishing Early"

    Recall that the goal of CVD is to help users make more informed
    decisions about actions they can take to secure their systems. Sometimes
    it becomes obvious that the coordination of a disclosure has failed. In
    these cases, it may make more sense to publish earlier than expected
    than to continue to withhold information from those who could use it to
    defend their systems.
    
    See also [Leaks](leaks.md), [Independent Discovery](independent_discovery.md), and [Active Exploitation](active_exploitation.md).

!!! tip "Engage a Third-Party Coordinator"

    !!! example inline end "Third-Party Coordinators"

        Examples of third-party coorinators include the following:
    
        - CERT/CC
        - National CSIRTs that handle CVD cases
        - JPCERT/CC
        - NCSC-FI
        - NCSC-NL
        - Larger vendors (Google, Microsoft, etc.)
        - Bug bounty operators (BugCrowd, HackerOne, etc.)

    We have outlined a variety of ways in which the CVD process might not go
    as smoothly as you'd like, whether you are a finder, reporter, vendor,
    coordinator, or deployer. When problems arise that you're not prepared
    to handle, or even if you just need a quick opinion on what to do next,
    there are a number of coordinating organizations available to help.

!!! tip "Learn from the Experience"

    !!! example inline end "Retrospective Questions"

        As an example of questions to begin a retrospective discussion, consider
        this list derived from the [Scrum Alliance](https://resources.scrumalliance.org/Article/sprint-retrospective):

        -   What went well?
        -   What went wrong?
        -   What could we do differently to improve?

    Any process worth doing more than once is one worth improving. To that
    end, we recommend that participants in CVD take good notes. Hold a
    retrospective to identify things that went well, things that didn't,
    and explore changes you can make to your process for next time. This
    very document is in large part the result of notes taken during
    "lessons learned" sessions with vulnerability coordinators at the
    CERT/CC.

{% include-markdown "../../_includes/_report_certcc.md" heading-offset=1 %}
