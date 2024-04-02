# Prioritization

Once the receiver of a report has [validated](validation.md) the report
as in scope, credible, and valid, the next question is how to allocate resources to the report.
Not every report can be addressed immediately, so prioritization is necessary.

At the most basic level, prioritization can be thought of as a simple binary decision:

```mermaid
flowchart TD
    when[When do we act?]
    now[Now]
    defer[Not now]
    when --> now
    when --> defer
```

In practice, however, prioritization can be more complex.
Much of what we have to say about prioritization is already covered in our
documentation of [SSVC](https://certcc.github.io/SSVC), the Stakeholder-Specific Vulnerability Categorization.


!!! question "Who Receives Reports?"

    The receiver of a report is typically a [vendor](../roles/vendor.md), but it could also be a
    [coordinator](../roles/coordinator.md) or a [deployer](../roles/deployer.md).

{% include-markdown "../../howto/coordination/prioritization.md" heading-offset=1 %}
