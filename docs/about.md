# About This Guide

!!! note "What This Guide Is Not"

    - *This is not a technical document.* You will not learn anything new about
    fuzzing, debugging, ROP gadgets, exploit mitigations, heap spraying,
    exception handling, or anything about how computers work by reading this
    report. What you will learn is what happens to that knowledge and how
    its dissemination is affected by the human processes of communications
    and social behavior in the context of remediating security
    vulnerabilities.

    - _This is not a history._ We won't spend much time at all on the history of 
    disclosure debates, or the fine details of whether collecting or
    dropping zero-days is always good or always bad. We will touch on these
    ideas only insofar as they intersect with the current topic of
    coordinated vulnerability disclosure.

    - _This is not an indictment._ We are not seeking to place blame on one
    party or another for the success or failure of any given vulnerability
    disclosure process. We've seen enough disclosure cases to know that
    people make choices based on their own values coupled with their
    assessment of a situation, and that even in cases where everyone agrees
    on what should happen, mistakes and unforeseeable events sometimes alter
    the trajectory from the plan.

    - _This is not a standard._ We assert no authority to bless the information
    here as "the way things ought to be done." In cases where standards
    exist, we refer to them, and this documentation is informed by them. In fact,
    we've been involved in creating some of them. But the recommendations
    made in this documentation should not be construed as "proper," "correct," or
    "ideal" in any way. As we'll show, disclosing vulnerabilities presents a
    number of difficult challenges, with long-reaching effects. The
    recommendations found here do, however, reflect our observation over the
    past few decades of what works (and what doesn't) in the pursuit of
    reducing the vulnerability of software and related products.

## What This Guide Is

This is a summary of what we know about a complex social process that
surrounds humans trying to make the software and systems they use more
secure. It's about what to do (and what not to) when you find a
vulnerability, or when you find out about a vulnerability. It's written
for vulnerability analysts, security researchers, developers, and
deployers; it's for both technical staff and their management alike.
While we discuss a variety of roles that play a part in the process, we
intentionally chose not to focus on any one role; instead we wrote for
any party that might find itself engaged in coordinating a vulnerability
disclosure.

We wrote it in an informal tone to make the content more approachable,
since many readers' interest in this documentation may have been prompted by
their first encounter with a vulnerability in a product they created or
care about. The informality of our writing should not be construed as a
lack of seriousness about the topic, however.

In a sense, this documentation is a travel guide for what might seem a foreign
territory. Maybe you've passed through once or twice. Maybe you've only
heard about the bad parts. You may be uncertain of what to do next,
nervous about making a mistake, or even fearful of what might befall
you. If you count yourself as one of those individuals, we want to
reassure you that you are not alone; you are not the first to experience
events like these or even your reaction to them. We're locals. We've
been doing this for a while. Here's what we know.
