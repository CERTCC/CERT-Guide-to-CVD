# CVD Staffing Considerations

Staffing a CVD capability requires a mix of technical and soft skills.
The roles and responsibilities of a CVD team can vary depending on the
size of the organization, the volume of incoming reports, and the
organization's existing security posture.
Here we primarily focus on two specific issues related to maintaining a
healthy and effective CVD team:

- Skills development and training
- Avoiding analyst burnout

## Skills Development and Training

Vulnerability analysis and response may require networking and forensics
skills for certain classes of vulnerabilities, but often also requires
some mix of the following skills:

<div class="grid cards" markdown>

- **Technical Skills**

  - Programming skills, especially in common languages (C, C++, Python, Java)
  - Reverse engineering and debugging
  - Knowledge of low-level operating system features for Windows, Mac and/or Linux
  - Software security testing
  - Virtualization, containers, and some infrastructure automation
  - Knowledge of common vulnerabilities and exploits
  - (specialized) Hardware architecture and basic electrical engineering
  - (emerging) Knowledge of machine learning and AI

- **Soft Skills**

  - Curiosity and a desire to understand how things work
  - Interest in learning new technologies
  - Clear and concise written communications
  - Customer-service mindset
  - Ability to work under pressure
  - Ability to communicate with non-technical stakeholders
  - Ability to communicate with technical stakeholders

</div>

In most organizations, these skills will likely be dispersed among a
team of people rather than expecting a single person to be fluent with
all of these topics.

!!! info "FIRST CSIRT Services Framework"

    The FIRST [CSIRT Services Framework](https://www.first.org/standards/frameworks/csirts/csirt_services_framework_v2.1)
    addresses staffing considerations throughout, but we'll highlight a few items from _9 Service Area: Knowledge Transfer_:

    | Function | Purpose | Outcome |
    |----------|---------|---------|
    | 9.2.4 Mentoring | Develop a program for CSIRT staff, constituency members, or external trusted partners to learn from experienced staff through an established relationship. | Developed and trained staff are available with the requisite technical and soft skills and process understanding, and who are up to date based on the job roles and needs. |
    | 9.2.5 CSIRT staff professional development | Help staff members successfully and appropriately plan and develop their careers. | Developed and trained staff are available with the requisite technical and soft skills and process understanding, and who are up to date based on the job roles and needs. |

!!! info "FIRST PSIRT Services Framework"

    Even closer to the CVD process, the FIRST [PSIRT Services Framework](https://www.first.org/standards/frameworks/psirts/psirt_services_framework_v1.1)
    also addresses staffing considerations in multiple sections, but here we'd like to highlight _Service 6.1 Training the PSIRT_
  
    | Function | Purpose | Outcome |
    |----------|---------|---------|
    | 6.1.1 Technical training | Train the PSIRT Staff so that they understand the issue that is being reported and can adequately perform the initial triage before handing it off to teams responsible for developing, testing, and releasing fixes. | PSIRT Staff has sufficient technical training to perform their duties. |
    | 6.1.2 Communications Training | Ensure PSIRT Staff follows the communication policies of the organization while interacting with external entities thus eliminating any regulatory/legal issues that may result from improper communication. | PSIRT Staff will have sufficient communications training to perform their assigned duties with clear accuracy and no ambiguity in communications. |
    | 6.1.3 Process Training | Ensure there is a smooth flow of information in managing product security incidents which will result in timely resolution of issues. | PSIRT Staff will be sufficiently trained on internal processes so that they can perform their duties. |
    | 6.1.4 Tools Training | Identify tools to track the third-party components embedded in products so the vulnerabilities can be tracked and released in these components. | PSIRT Staff will have an understanding and be able to track third-party components within shipped products. |

## Beware Analyst Burnout

!!! info inline end "Security Analyst Burnout Articles"

    There are many articles and studies on the topic of security analyst burnout. Here are a few:

    - [It’s Time to Break the SOC Analyst Burnout Cycle](https://www.sans.org/blog/it-s-time-to-break-the-soc-analyst-burnout-cycle/)
    - [Defending the Defenders: Understanding and Preventing Security Analyst Burnout](https://www.bitdefender.com/blog/businessinsights/defending-the-defenders-understanding-and-preventing-security-analyst-burnout/)
    - [Building a Security Operations Center (SOC)](https://www.rsaconference.com/events/us12/agenda/sessions/683/building-a-security-operations-center-soc)
    - [Avoiding burnout: Ten tips for hackers working incident response](http://www.csoonline.com/article/2149900/infosec-careers/avoiding-burnout-ten-tips-for-hackers-working-incident-response.html)
    - [A human capital model for mitigating security analyst burnout](https://www.usenix.org/conference/soups2015/proceedings/presentation/sundaramurthy)

Some organizations may have a small enough flow of incoming
vulnerability reports that all the CVD-related roles can be fulfilled by
a single team, or even a single person. Other organizations might choose
to split the technical analysis roles apart from the more human-oriented
communication and coordination roles. No matter the arrangements, it is
important that vendors and coordinators establishing a CVD capability
mitigate the potential for analyst burnout. Burnout of security analysts
is well-documented phenomenon (see inset at right). Analysts working full-time in a
CVD process are at risk of this too.

A vendor's CVD capability may
receive a large amount of incoming reports each week, especially at
larger vendors. This can result in CVD staff becoming stressed and
having low job satisfaction, leading to lower quality of work and
ultimately employee attrition. The costs of lower quality work (e.g.,
missing an important report), employee turnover (e.g., hiring and
training a new analyst), and associated damage to the vendor's
reputation suggest that this problem should be addressed ahead of time
with reasonable precautions.
At the CERT/CC, we have attempted to
mitigate this issue with reasonable success by implementing the
suggestions below.
[Research](https://www.usenix.org/conference/soups2015/proceedings/presentation/sundaramurthy) has shown that many of
these are effective responses to commonly-held morale problems.

<div class="grid cards" markdown>

!!! tip "Reserve Capacity"

    Organizations
    may choose to have several team members, trained in the CVD process
    and tools, who can temporarily assist should a regular CVD analyst
    be unavailable for any reason, even if these additional team members
    do not typically do CVD day-to-day. Of course, handing off reports
    between temporary and full-time analysts leads to other operational
    concerns as previously discussed, so this must be done carefully.
    Organizations must also take care that these temporary team members
    are not pulled away from their own work so often that they
    themselves experience burnout.

!!! tip "Rotate Roles"

    A related possibility shared with us by a vendor is the possibility of
    *work rotation,* whereby team members are rotated in and out of CVD
    roles; rather than temporary, the rotation is permanent among a larger
    group of team members. An example would be an analyst spending one week
    in a CVD role, followed by two to three weeks on a different project or
    role. The same concerns in our prior discussion would apply;
    organizations must be careful to balance time in and out of CVD roles in
    order to maximize the effectiveness of the rotation.

!!! tip "Allow analyst independence"

    Generally, you should trust your
    analysts to make good decisions during the report prioritization process,
    and empower them to make CVD decisions. Allowing analyst autonomy
    with management's specific blessing provides relief to analysts
    attempting to prioritize reports. Many reports will be incomplete,
    inaccurate, unimportant, or not actionable; allowing analysts to
    make the judgment on which reports deserve priority and which should
    be closed may help reduce work-related stress.

!!! tip "Allot professional development time"

    Analysts schedule some
    time each week to focus on professional development or projects.
    During these times, the analyst is not expected to perform CVD
    duties. Providing this time in whole-day chunks is preferable to
    spreading it out across the week. It is also important that during
    these days the analyst not be disturbed; urgent tasks should be
    handled by other on-duty analysts as much as possible. This
    suggestion may be combined with work rotation to allow for regular
    project work outside of the scope of CVD.

!!! tip "Seek out automation"

    We have encouraged analysts to document
    procedures and processes that need updating or could even be
    automated. Prototypes can be implemented and rolled out to decrease
    the cognitive workload of analysts. Processes and tools should be
    reviewed regularly to ensure they are aiding the analyst, rather
    than fighting the analyst.

!!! tip "Well-Resourced Teams for CVD"

    Due to the possibility of burnout and the associated costs, the CERT/CC
    recommends that CVD capability be established within a well-resourced
    team or teams specifically created for this task, rather than
    concentrating the responsibilities to a small team, or even a single
    person. Our suggestions above may be helpful to combat analyst burnout,
    but do not form an exhaustive list of possible actions.

</div>
