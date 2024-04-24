!!! tip "Policy statements should be clear and simple"

    Each item in a policy should cover a single expectation.
    Items should be clear and simple to facilitate interpretation by all participants.

!!! tip "Use RFC 2119-style language"

    Each item SHOULD use "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", 
    "MAY", and "OPTIONAL" consistent with their meaning in [RFC 2119](https://datatracker.ietf.org/doc/html/rfc2119). 
    RFC-style makes clear the distinction between expectations that are recommendations versus those that are requirements.

!!! tip "Use active voice"

    Write each policy expectation item in the active voice. This means every
    statement has a clear actor and an expectation on that actor. `ORGANIZATION`
    SHALL..., Reporter MAY..., etc.) Active voice makes it easy to
    recognize to whom the expectation applies.

!!! tip "Use imperative expectations of others and declarative expectations of self"

    In general, expectations of others should use "MAY", "SHOULD", "MUST", "MUST
    NOT", "REQUIRED", or "OPTIONAL". 

    Expectations that the`ORGANIZATION` sets for itself should prefer "SHALL"
    and "SHALL NOT" in place of "MUST" or "MUST NOT".
  
    Similarly, it seems unlikely that`ORGANIZATION` would use "SHOULD" to refer to
    its own behavior, rather preferring to use "SHALL", "SHALL NOT", or "MAY"
    formulations.

    Rationale: The policy creator is declaring limits and
    expectations on their own behavior, not recommending to others what they
    can/should/might do. In other words, use imperatives for others, declaratives
    for self.

!!! tip "Separate expectations by role"

    To the degree possible, separate expectations by role. For example, as we have
    done by splitting [reporters](Reporters.md)
    and [receivers](Receivers.md) into separate files.
    In a real policy,
    these would become different sections of the document.

!!! tip "Keep it simple / limit complexity"

    Limit the logical complexity of individual expectations. A single conditional
    is fine. Consider splitting statements containing multiple conditionals into
    separate statements.

!!! tip "Consider symmetry"

    Consider symmetry in policy expectation items. For example, if you expect
    politeness from Reporters, do you also commit to being polite?

!!! tip "Replace KEYWORDS with specifics"

    In our template statements, we use KEYWORDS to denote specifics that are
    stakeholder-specific. 

    Replace KEYWORDS with specifics that are relevant to your organization.

    For example, replace `ORGANIZATION` with your organization's name, or
    `SLC` with "45 days" if that's your organization's
    standard disclosure timeline.
