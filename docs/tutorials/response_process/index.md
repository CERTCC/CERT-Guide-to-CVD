# An Overview of the Coordination Process

<!--start-->
Although the coordination process can be complex at times,
we can describe the general process in a few steps. The rest of this
guide goes into more detail on each of these steps and what else might happen along the way.
<!--end-->

{% include-markdown "../../_includes/_what_is_coord.md" heading-offset=1 %}

## Ideal Disclosure Process

When a reporter is working directly with the vendor, the coordinated
disclosure process generally proceeds as follows:

1. A reporter learns of a vulnerability (either directly as a user or
    researcher, or indirectly from someone else)
2. Reporter finds vulnerable product's vendor, reports vulnerability
    to vendor directly
3. Vendor analyzes the report, verifies information is correct, and
    quickly acknowledges reporter

    ```mermaid
    flowchart TD
        reporter([Reporter])
        vendor([Vendor])
        reporter -->|1 learns of vul| reporter
        reporter -->|2 reports vul| vendor
        vendor -->|3 acknowledges| reporter
    ```

4. Vendor provides information to reporter regarding patching the issue
    and the timeframe until the patch is released publicly, reporter
    agrees to publish on the same day
5. Reporter may test the patch before public release and provide
    findings to vendor
6. Toward the end of the timeframe, before the patch is released, both
    vendor and reporter draft security advisories and share with each
    other for comment

    - If the vendor is a [CVE Numbering Authority](https://www.cve.org/ProgramOrganization/CNAs){:target="_blank"} (CNA), the vendor will assign a CVE ID
    - Otherwise, the reporter or vendor may [request a CVE ID](https://www.cve.org/ReportRequest/ReportRequestForNonCNAs){:target="_blank"} from the CVE Program

    ```mermaid
    flowchart TD
        reporter([Reporter])
        vendor([Vendor])
        vendor -->|4 provides patch info| reporter
        reporter -->|5 tests patch| vendor
        vendor <-->|6 share draft<br/>advisories| reporter
    ```

7. The patch for the vulnerability may be released privately to affected
   downstream vendors (customers/users of the vulnerable product) first
8. On an agreed-upon date, public security advisories are published
   detailing the issue, and how to obtain the patch or mitigate the
   issue

    - typically, the vendor will release an advisory simultaneously
        with the reporter publishing an advisory on a blog,
        social media, or mailing list, or via a conference presentation

9. Once the vulnerability is public, (typically fairly quickly, especially if the
      vendor is a CNA), the CVE record will be published to the [CVE List](https://www.cve.org/Downloads){:target="_blank"}.
10. After the CVE record is published, the [National Vulnerability Database](https://nvd.nist.gov/){:target="_blank"} (NVD)
        will publish its entry on the CVE ID, which provides extra information like vulnerability scoring.

    ```mermaid
    flowchart TD
        reporter([Reporter])
        vendor([Vendor])
        public([Public])
        cve([CVE List])
        nvd([NVD])
        vendor -->|7 release patch| public
        vendor -->|8 publish advisory| public
        reporter -->|8 publish advisory| public
        vendor -->|9 CVE record| cve
        cve -->|10 CVE record| nvd
        cve -->|10 CVE record| public
        nvd -->|11 NVD entry| public
   
    ```

End result: vulnerability is mitigated or addressed in some manner,
tracked with a CVE ID, and the public is informed through advisories
about how to obtain the mitigation.

## Complications

The above description is very idealized, while every coordinated
disclosure case is somewhat unique and may have special handling
requirements or constraints. The important idea is the word
*coordinated*: the formula presented above can be tweaked as much as
necessary as long as both parties are kept in the loop (coordinate!).

In some simple cases, should a vendor become unresponsive, some
reporters will proceed to publishing a security advisory. This is
common, especially in cases where the vulnerability was initially
established but then no date is set for a patch release. This is fine to
do, but CERT/CC recommends to first reach out to the vendor with a draft
of your advisory before publishing.

However, other cases can be more complex, such as reports that affect
multiple vendors, only some of which are responsive to the reporter. In
general, the CERT/CC is here to help with scenarios that go "off the
rails". This can include many different reasons, such as:

- Reporter is new to coordination and disclosure and would like some
    guidance on reporting and disclosing vulnerabilities
- Vendor is new to coordination and disclosure; the vendor may be
    unreachable by the reporter, or the vendor may request guidance on
    handling the report and establishing operations for future reports
- Multiple vendors are suspected of being affected, and the reporter
    either has received no reply or is even unsure exactly who is
    affected
- Vendor and Reporter disagree on the existence or severity of a
    vulnerability; CERT/CC may be able to provide independent testing
    and analysis

In these cases you might contact the CERT/CC for assistance.

{% include-markdown "../../_includes/_report_certcc.md" heading-offset=1 %}

<div class="grid" markdown>

!!! question "I'm a reporter, what should I do next?"

    See the [Reporter Response Process](./reporter.md) for more information on what to do when you find a vulnerability.

!!! question "I'm a vendor, what should I do next?"

    See the [Vendor Response Process](./vendor.md) for more information on what to do when you receive a report of a vulnerability.

!!! question "I'm a deployer, what should I do next?"

    See the [Deployer Response Process](./deployer.md) for more information on what to do when you receive a report of a vulnerability.

!!! tip "For More Information"

    We have a lot more to say about the coordination process.
    For more on the general topic, see the [How-To](../../howto/index.md) section of this site.
    For specific advice on complications that can arise during the coordination process,
    see the [Troubleshooting CVD](../../howto/coordination/cvd_recipes.md) section of this site.

</div>
