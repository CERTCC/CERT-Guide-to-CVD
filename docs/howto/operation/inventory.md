# Code and System Inventories

For both vendors and deployers, maintaining an inventory of dependencies
is a critical part of the vulnerability management process. Knowing what
you have deployed is the first step in being able to protect it.

## Deployer Perspective: What's in Your Network?

For deployers, maintaining an inventory of the software and hardware in
your network is a critical part of your vulnerability management
process. Knowing what you have deployed is the first step in being able
to protect it. This is especially important for software that is exposed
to the internet, but it is also important for software that is only used
internally. 

Even better than just knowing what you have deployed is being able to map
those deployed components to the important services they provide and the
missions they support. This can help you prioritize your response to
vulnerabilities based on the importance of the affected systems.

!!! tip "SSVC and risk-based prioritization"

    We developed the [Stakeholder-Specific Vulnerability Categorization](https://certcc.github.io/SSVC)
    (SSVC) framework to help organizations prioritize their vulnerability
    response efforts based on the importance of the affected systems to
    the organization's mission, along with exposure to adversaries.
    SSVC is a risk-based approach to vulnerability prioritization that
    can help organizations to focus their efforts on the most risk-relevant
    vulnerabilities first.


## Vendor Perspective: Dependencies and Supply Chain

As we discuss in [Multiparty CVD](../coordination/mpcvd.md),
software-based products are typically assembled from components rather
than written from scratch. Economies of scale apply to code, and most
organizations would consider it wasteful to write a feature from scratch
when that feature is available at a reasonable licensing cost for
inclusion into their own products. As a result, each product is not
merely the result of a single vendor's development process, but of an
entire supply chain. Libraries get included in other libraries, which
form subcomponents in the composition of larger and more complex
products.

!!! tip "Know Your Dependencies"

    For product vendors, an important part of the vulnerability response
    process is knowing what weaknesses your products might have. You can
    address this by clearly identifying any third-party libraries or
    utilities that are included with your products, and being alert and
    responsive to vulnerability disclosures in any third-party products that
    may affect your own products.

!!! tip "Software Bill of Materials (SBOM)"

    Because it is likely that your products will in turn be used
    as components in some other vendor's solution, it is increasingly a good
    practice to provide an inventory of components along with your product.
    Under the broad category of [Software Bill of Materials](https://www.cisa.gov/sbom)
    (SBOM), this practice is becoming more common in the software industry.
    A number of data formats and specifications have emerged in the software
    supply chain management space and are in use by product vendors already.

    These include the following

    - [Software Identification (SWID) Tags](http://tagvault.org/swid-tags/)
    - [Common Platform Enumeration (CPE)](https://nvd.nist.gov/products/cpe)
    - [The Software Package Data Exchange (SPDX)](https://spdx.org/)

    More than just a good practice, providing an SBOM can be a requirement
    in some industries. For example, the U.S. government has issued an
    [Executive Order](https://www.whitehouse.gov/briefing-room/presidential-actions/2021/05/12/executive-order-on-improving-the-nations-cybersecurity/)
    that mandates the use of SBOMs in software procurement.
    The National Telecommunications and Information Administration (NTIA)
    has also issued a report describing
    [_The Minimum Elements For a Software Bill of Materials_](https://www.ntia.doc.gov/report/2021/minimum-elements-software-bill-materials-sbom)


!!! example "Software Composition Analysis Tools"

    In recent years, a class of Software Composition Analysis tools (such
    as those offered by
    [Mend.io](https://www.mend.io/),
    [Synopsys](https://www.synopsys.com/software-integrity/security-testing/software-composition-analysis.html),
    [Sonatype](https://www.sonatype.com/),
    and
    [Revenera](https://www.revenera.com/software-composition-analysis))
    have come into use to identify potential licensing conflicts in
    commercial and open source products. Many of these tools are
    potentially useful to vendors looking to create an inventory of
    libraries and third-party components used in their products for
    security analysis purposes as well.

!!! tip "Monitoring For Vulnerabilities in Third-Party Components"

    As a vendor, identifying your products' third-party dependencies is
    only the first step. After that, you should take steps to ensure that
    your vulnerability response capability maintains awareness of any
    security-related announcements about those upstream products on which
    your product depends. Some component vendors offer special communication
    channels (e.g., a mailing list) for their licensees. If you've worked
    with a coordinator like the CERT/CC in the past, ask if you can be
    placed in a special notification list for a particular library or
    product.
    See more in [Monitoring](./monitoring.md).

