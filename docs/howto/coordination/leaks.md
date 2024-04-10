# Intentional or Accidental Leaks

Unfortunately, not everyone plays by the same rules.<!--start-->You might find
information you thought was shared in confidence showing up in some
non-confidential location. It might be a simple misunderstanding,
mismatched expectations, or in rare cases, a malicious act.<!--end-->

!!! example "Ways Information Can Leak"

    Sometimes information leaks out of the CVD process. 
    
    - Perhaps an email gets CC'ed to someone who didn't need to know. 
    - Somebody might talk too much at a conference.
    - Somebody could post that they just found a vulnerability in a product, providing no other details. 
    - Somebody might intentionally disclose the information to someone not involved in the supply chain for the fix.

!!! question "Questions to Ask When Information Leaks"

    Regardless of how it leaked, there are three major questions to ask:

    1. What information leaked?
    2. How did the information leak?
    3. How will you respond?

!!! warning "Even Partial Leaks Can Be Serious"

    As we note in [Disclosure Timing](../../howto/coordination/disclosure_timing.md), mere
    knowledge that a vulnerability exists in a certain component can
    sometimes be enough to enable a determined individual or organization to
    find it. While a partial leak of information isn't necessarily as
    serious as a detailed leak, it should at least trigger additional
    consideration of accelerating the disclosure timeline.

{% include-markdown "../recipes/_x11.md" heading-offset=1 %}
