# Coordinated Vulnerability Disclosure is a Process, Not an Event 

A process is 

!!! quote "Oxford Living Dictionaries (English)"
    [process](https://en.oxforddictionaries.com/definition/process): a series of actions or steps taken in 
    order to achieve a particular end

Publishing a document is an action. Releasing a
fix is an action. And while both of these are common events within the
CVD process, they do not define it. Perhaps the simplest description of
the CVD process is that it starts with at least one individual becoming
aware of a vulnerability in a product. This discovery event immediately
divides the world into two sets of people: those who know about the
vulnerability, and those who don't. From that point on, those belonging
to the set that knows about the vulnerability iterate on two questions:

1.  What actions should I take in response to this knowledge?
2.  Who else needs to know what, and when?

The CVD process continues until the answers to these questions are
"nothing," and "nobody."

Simple enough? Hardly. If it were, this documentation would be considerably
shorter. But with this simple iterator in mind, we'll be better able to
frame our discussion.

Ideally, product and service vulnerabilities would be either discovered
by the vendor (developer) of the software product or service itself or
reported to the vendor by a third party (finder, reporter). Informing
vendors enables them to take action to address and correct
vulnerabilities. In most cases, the vendor is the party best suited to
correct the vulnerability at its origin. Vendors typically remediate
vulnerabilities by developing and releasing an update to the product,
also known as a patch. However, often the vendor issuing an update is
just the first step towards remediation of the installed base of
vulnerable systems. Deployers must still ensure that patches are
deployed in a timely manner to the systems they need to protect. A more
detailed discussion of [Roles in CVD](../roles/index.md) is available.



