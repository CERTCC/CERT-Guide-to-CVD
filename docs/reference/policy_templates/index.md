# Vulnerability Disclosure Policy Templates

In recent years the CERT/CC has advised a number of organizations on their
vulnerability disclosure policies.
This section contains a collection of resources intended for use in
constructing a vulnerability disclosure policy. 
Here we are attempting to capture common
verbiage in order to help others develop or improve their own policies. We've
taken these items from a variety of vulnerability disclosure policies including
[our own](../certcc_disclosure_policy.md), generalized them, organized them by topic, and assembled them into this
collection.

This collection is a general set of templates from which you can derive and
spawn a disclosure policy for an organization. 

!!! tip "How to Use This Collection"

    This collection of example policy statements is meant to be remixed and adapted for different
    organizations and contexts. It is unlikely that any single organization would
    choose to adopt all of these items wholesale without some modification.


<div class="grid cards" markdown>

- :material-feather: [Style Guide](./style_guide.md)
  
    ---
    {%include-markdown "./style_guide.md" start="<!--start-->" end="<!--end-->" %}

- :material-set-left-center: [Setting Expectations for Reporters](./Reporters.md)
  
    ---
    {%include-markdown "./Reporters.md" start="<!--start-->" end="<!--end-->" %}  

- :material-set-center-right: [Setting Expectations for Receivers](./Receivers.md)
  
    ---
    {%include-markdown "./Receivers.md" start="<!--start-->" end="<!--end-->" %}

</div>


{% include-markdown "./_adjust_to_suit.md" %} 
{% include-markdown "./_usage.md" %}

!!! note "Use of RFC 2119 Language"

    We've taken the approach of using [RFC 2119](https://datatracker.ietf.org/doc/html/rfc2119)-style
    "MUST, SHALL, SHOULD..." language in active-voice sentences to describe what researchers/reporters and
    vendors/coordinators/recipients should expect of each other.


