# Legal and Regulatory Issues {#sec:legal_issues}

## DMCA and CFAA

Things we might include: DVD decryption code.

John Deere and the right-to-repair controversy.

"Safe harbor" might not mean what you think it means. Organizations
might choose not to prosecute, but that does not mean you are protected
from criminal prosecution by law enforcement.

Pointer to EFF stuff.

## Wassenaar Arrangement

"Zero Day exploit capability" as a meaningless term. Current status\...

## 2020 BOD

## 2021 Cybersecurity EO

## something about EU?

GDPR and CVD?

Do we know anything about EU CVD status?

## Canada

## International Trade Sanctions and CVD

Individuals and organizations conducting [CVD]{acronym-label="CVD"
acronym-form="singular+short"} on a global scale might encounter a
challenge at the intersection of [CVD]{acronym-label="CVD"
acronym-form="singular+short"} and international trade sanctions imposed
by their home government. Here we present an anecdote from our own
experience at the [CERT/CC]{acronym-label="CERT/CC"
acronym-form="singular+short"} (in the United States), highlighting how
we approached and worked through a related issue a few years ago. Our
experiences here are provided as examples only, none of what follows
should be taken as legal advice. We include this with the observation
that organizations in other countries may be subject to similar
requirements imposed by their respective governments.

The [OFAC]{acronym-label="OFAC" acronym-form="singular+full"} within the
U.S. Department of the Treasury administers and enforces economic and
trade sanctions based on U.S. foreign policy and national security
goals.[@0]

> U.S. persons must comply with OFAC regulations, including all U.S.
> citizens and permanent resident aliens regardless of where they are
> located, all persons and entities within the United States, all U.S.
> incorporated entities and their foreign branches. In the cases of
> certain programs, foreign subsidiaries owned or controlled by U.S.
> companies also must comply. Certain programs also require foreign
> persons in possession of U.S.-origin goods to comply.

As a vendor, reporter, or coordinator in the U.S., should you become
aware that an individual or organization participating in a
[CVD]{acronym-label="CVD" acronym-form="singular+short"} case is named
on [OFAC]{acronym-label="OFAC" acronym-form="singular+short"}'s
[SDN]{acronym-label="SDN" acronym-form="singular+short"}[^1], you need
to decide whether you are willing to continue coordinating with the
sanctioned party. You may already know that your reporter or the
organization is on an [OFAC]{acronym-label="OFAC"
acronym-form="singular+short"} list. If they know, they'll often tell
you.

U.S.-based organizations participating in CVD internationally may need
to engage their legal counsel to request a review of the sanctions list.
~~Take care when using the sanctions list search application, as common
names may result in a false-positive result.~~

Should it be necessary, [CVD]{acronym-label="CVD"
acronym-form="singular+short"} participants can work with their legal
counsel and the [CISA]{acronym-label="CISA"
acronym-form="singular+full"} to obtain a license from
[OFAC]{acronym-label="OFAC" acronym-form="singular+short"}[^2]. ~~The
[CERT/CC]{acronym-label="CERT/CC" acronym-form="singular+short"} has on
two occasions contacted [CISA]{acronym-label="CISA"
acronym-form="singular+short"} for support in obtaining an
[OFAC]{acronym-label="OFAC" acronym-form="singular+short"} license.~~
Inform the [SDN]{acronym-label="SDN" acronym-form="singular+short"} that
you are in the process of obtaining an [OFAC]{acronym-label="OFAC"
acronym-form="singular+short"} license and ask for their patience and
understanding. Maintain your flexibility, as the approval and issuance
of a License can take 30 to 60 days.

~~For this discussion, the reporter or organization associated with the
reporter is on the sanctioned list.~~

Once you have been granted a Cyber-Related Sanctions Regulations License
you must follow the requirements. The CERT/CC has been party to two
licenses. These licenses had four sections:

1. A description of the authorization. In our case, it stated that the
    License was being issued to [CISA]{acronym-label="CISA"
    acronym-form="singular+short"} and listed the other parties, known
    as *Licensees*, which have been authorized to engage with the
    [SDN]{acronym-label="SDN" acronym-form="singular+short"} "for the
    purpose of addressing certain software vulnerabilities that threaten
    U.S. companies, as described in the Application."

2. A set of limitations on the license. In our case, the license
    indicated that the [SDN]{acronym-label="SDN"
    acronym-form="singular+short"} is subject to the "blocked property"
    requirement: there can be no transaction of property.

3. Record keeping and reporting requirements. The
    [CERT/CC]{acronym-label="CERT/CC" acronym-form="singular+short"} met
    this requirement by maintaining copies of email records and database
    entries separately to facilitate timely reporting. The
    [OFAC]{acronym-label="OFAC" acronym-form="singular+short"} License
    required a report every 90 days as well as a detailed final report
    no later than 30 days following the expiration of the License. As
    the time, all reports needed to be physically mailed to the
    Department of the Treasury.

4. A description of license dependencies, including the expiration date
    for the License.

~~Section 4 states the "License is limited to the facts and
circumstances specified in the Application."~~ If you are working
directly with [CISA]{acronym-label="CISA"
acronym-form="singular+short"}, you will need to create a compliance
plan. Where possible, limit the number of your personnel impacted by the
compliance plan. Request participation from your legal department for
creation and implementation of the compliance plan. Your compliance plan
will state who is involved, that they agreed to abide by the blocked
property restriction, and the frequency of which you will be reporting
contact with the [SDN]{acronym-label="SDN"
acronym-form="singular+short"}. The [CERT/CC]{acronym-label="CERT/CC"
acronym-form="singular+short"} Compliance Plan consisted of two pages.
Personnel involved in the coordination efforts will be asked to sign an
Individual Compliance Certification, indicating they have read and
understand the requirements of the License and agree to comply.

~~Conduct the coordination effort with special attention to the meeting
your [CVD]{acronym-label="CVD" acronym-form="singular+short"} goals and
recording all correspondence with the [SDN]{acronym-label="SDN"
acronym-form="singular+short"}.~~ A potential for breaking the license
agreement comes with bug bounty programs. ~~Remember, the
[OFAC]{acronym-label="OFAC" acronym-form="singular+short"} License
strictly enforces the "blocked property" requirement, and does not allow
for material transactions or rewards.~~ ~~Maintain your recordkeeping
and submit timely reports.~~ ~~Continue to submit timely reports whether
or not there is any new correspondence.~~ ~~In these cases, the report
can simply state "no communications have occurred since the last
report."~~ ~~Submit your final report and you're done!~~

## China Data Security Law 2021

Section 7.1 requires network product providers to verify and assess the
risk of reported vulnerabilities, reporting to upstream vendors as
necessary. Section 7.2 mandates reporting to the Ministry of Industry
and Information Technology's cyber security threat and vulnerability
information sharing program within 2 days

> The DSL's provisions require all Chinese security researchers, Chinese
> businesses, and &mdash; most notably &mdash; foreign companies with a
> footprint inside China to report any zero-day vulnerability to the
> Chinese Ministry of Industry and Information Technology (MIIT) within
> two days of a vulnerability's discovery. The DSL also prohibits
> affected entities from "collect\[ing\], sell\[ing\], or publish\[ing\]
> information on network product security vulnerabilities" and outlaws
> sharing vulnerabilities with any "overseas organizations or
> individuals other than network product providers."

from [@0]

[^1]: <https://home.treasury.gov/policy-issues/financial-sanctions/specially-designated-nationals-and-blocked-persons-list-sdn-human-readable-lists>

[^2]: A license is an authorization from [OFAC]{acronym-label="OFAC"
    acronym-form="singular+short"} to engage in a transaction that
    otherwise would be prohibited.
