# Contact Management

From a reporter's perspective, the contact management process can be
relatively simple. For most reporters, the contact management process simply consists of
finding and bookmarking a vendor's security contact page, or
maintaining a vendor's email address and PGP/GPG key in compatible mail
client software.

Contact management becomes vitally important to
multiparty CVD, and is a particular concern for third-party
coordinators.

!!! tip "Finding Vendor Contacts"

    Finding vendor contacts can be difficult. Not all vendors include
    contact information in an easily searchable page, such as a Contact Us
    page linked from the vendor's homepage.
    See [Finding Vendor Contacts](../initiation/find_vendor_contact.md) for more information.

!!! warning "Avoid Posting Vulnerability Details in Public"

    In order to protect privacy during the disclosure process, mailing lists
    or simply carbon-copying all recipients to a single message is likely
    not an acceptable action in most scenarios. Vendors in many cases would
    like to keep their vulnerability information private except for what is
    specifically intended to be shared. 

!!! example "CERT/CC's Approach to Contact Management"

    For the first few decades of the CERT/CC's existence, we developed and maintained a collection of
    in-house tools and scripts to perform contact and key management.
    These tools auto-generated individual encrypted emails, one for each vendor we attempted to reach.
    In this way, we could maintain privacy up front, with the option to introduce two vendors should there be
    mutual interest in collaboration. This approach was particularly useful for smaller cases. It serves as an example of a
    _hub and spoke_ topology for each case.

    However, we eventually realized that this approach was not scalable to larger cases involving multiple vendors,
    and much of our coordination work was shifting toward multiparty cases.
    With the rollout of the [VINCE platform](https://github.com/CERTCC/VINCE){:target="_blank"}, we have shifted to a _shared bus_ topology
    for our cases, in which the reporter, vendors, and coordinators all have access to the same case information and
    can communicate with each other in a shared space.
    While we still have some manual processes for making the initial contact with vendors, the VINCE platform 
    allows vendors to manage their own contact information and PGP keys within the system.
    This has enabled us to scale our operations to handle more cases involving many more vendors,
    and has made it easier for us to bring in third-party coordinators to assist with
    cases when necessary.

    We cover communication topologies for CVD in [Response Pacing and Synchronization](../coordination/response_pacing.md).
