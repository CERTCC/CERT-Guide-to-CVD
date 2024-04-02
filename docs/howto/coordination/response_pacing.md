# Response Pacing and Synchronization

<!--start-->Problems can arise when the multiple parties involved in CVD function at
different operational tempos. Different organizations have different
priorities and development schedules, which can lead to some parties
wanting to move faster than others.<!--end-->

In both the vertical and horizontal supply
chain cases discussed in [Multiparty CVD](mpcvd.md), synchronized timing of disclosure to the
public can be difficult to coordinate. The originating vendor(s) will
usually want to release a patch announcement to the public as soon as it
is ready. This can, however, put users of downstream products at
increased risk. As a result, coordinators sometimes find it necessary to
make the difficult choice to withhold notification from a vendor in a
complicated multiparty disclosure case if that vendor cannot be trusted
to cooperate with the coordination effort.

!!! tip "When One Party Wants to Release Early"

    In a multiparty coordination scenario, some vendors may want to release
    early to protect their customers. They have a good point: should _Vendor
    A_'s customers be kept vulnerable just because _Vendor B_ is taking longer
    to prepare its response? Yet an equally strong counterargument can be
    made: should customers of _Vendor B_ be exposed to additional risk because
    _Vendor A_ was faster at its vulnerability response process? 

    ```mermaid
    stateDiagram-v2
        direction LR
    notify: Notify<br/>Vendors
    State2: Vendor A<br/>Fix Development
    State5: Vendor A<br/>Ready
    State3: Vendor B<br/>Fix Development
    State6: Vendor B<br/>Ready
    State4: Public<br/>Disclosure
    state fork_state <<fork>>
    [*] --> notify
    notify --> fork_state
    fork_state --> State2
    fork_state --> State3
    State2 --> State5
    State3 --> State6
    state join_state <<join>>
    State5 --> join_state
    State6 --> join_state
    join_state --> State4
    State4 --> [*]
    ```

    There is no
    single right answer to this dilemma. The best you can do is keep the
    communication channels open and try to reduce the amount of surprise
    among participants. Planning for contingencies can be a useful exercise
    too&mdash;the focus of such a contingency should be how to respond if
    information about the vulnerability got out before you were ready for
    it.

## Motivating Cooperation Across Cases

CVD process discussions tend to focus on the handling of individual
vulnerability cases rather than the social fabric surrounding
vulnerability coordination we construct over time. Shifting away from
the individual units of work to the social structure can suggest a way
out of some of the more contentious points in any given case.

!!! info inline end "Axelrod's Principles on the Evolution of Cooperation"

    Robert Axelrod's book _The Evolution of Cooperation_ is a classic 
    text on the topic. Axelrod's [work](https://ee.stanford.edu/~hellman/Breakthrough/book/pdfs/axelrod.pdf)
    showed that the most successful strategies in repeated games follow certain principles, which we
    include here for reference:
        
    - Don’t be envious
    - Don’t be the first to defect
    - Reciprocate both cooperation and defection
    - Don’t be too clever

We previously described the multiparty delay problem. Game theory
provides us with the prisoners' dilemma as model for thinking about
this concern. The main takeaway from research into the prisoners'
dilemma is that by shifting one's perspective to considering a repeated
game, it's possible to find better solutions than would be possible in
a one-shot game with no history. The recognition that it's a repeated
game leads to improved cooperation among players who would otherwise be
motivated to act solely in their own self-interest in each round.

One approach we've found to work is to remind the parties involved that
this will likely not be the last multiparty vulnerability coordination
effort in which they find themselves. A vendor that repeatedly releases
early will likely get left out of future coordination efforts. Because
of this, the quicker vendors might be motivated to delay so they get the
vulnerability information the next time. 

!!! tip "The Repeated Game"

    Perhaps most important for
    those wanting to release early is to remember that this is a repeated
    game; you might be first one ready to publish this time but that may not
    always be the case. Consideration for the other parties involved in any
    given case can yield better outcomes in the long run.

In the end, everyone benefits from vendors improving their vulnerability
response processes, so helping the laggards become more efficient can
sometimes become a secondary goal of the coordination process.

