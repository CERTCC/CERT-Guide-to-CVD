!!! warning "Use caution with <span style="color:#FF2B2B;background-color:#000000">**TLP:RED**</span> and <span style="color:#FFC000;background-color:#000000">**TLP:AMBER+STRICT**</span>"
 

    We have found that <span style="color:#FF2B2B;background-color:#000000">**TLP:RED**</span> is too restrictive for an organization to effectively respond to a vulnerability.
    For example, the analyst who receives a <span style="color:#FF2B2B;background-color:#000000">**TLP:RED**</span> report might not be able to share it with their manager or their team.
    In a Vendor context, this might mean that the person who receives the report cannot share it with the team responsible for fixing the vulnerability.

    <span style="color:#FFC000;background-color:#000000">**TLP:AMBER+STRICT**</span> might be okay for a Reporter working with a single Vendor only, or when a Vendor 
    wants retain control over the disclosure process to other Vendors or Coordinators.
    However, it limits the ability of the receiving party to engage others who might be able to help.
    A Vendor in receipt of a <span style="color:#FFC000;background-color:#000000">**TLP:AMBER+STRICT**</span> report cannot share it with their upstream or downstream Vendors.
    Nor can they share it with Coordinators who might be able to help them reach other affected parties.
    Similarly, a Coordinator in receipt of a <span style="color:#FFC000;background-color:#000000">**TLP:AMBER+STRICT**</span> report cannot share it with other Coordinators or Vendors,
    which severely limits their ability to assist with the coordination process.
    It is not impossible to do CVD with <span style="color:#FFC000;background-color:#000000">**TLP:AMBER+STRICT**</span>, but it is more difficult and less effective.

    Therefore we recommend <span style="color:#FFC000;background-color:#000000">**TLP:AMBER**</span> for most cases prior to public disclosure. 

    <span style="color:#33FF00;background-color:#000000">**TLP:GREEN**</span> can be useful for cases nearing public disclosure, for example when necessary to engage critical infrastructure
    through ISACs, ISAOs, or other trusted channels. In some larger multiparty cases, <span style="color:#33FF00;background-color:#000000">**TLP:GREEN**</span> might be useful to reach
    a broader audience of potentially affected vendors, deployers and other stakeholders. However, the use of <span style="color:#33FF00;background-color:#000000">**TLP:GREEN**</span> 
    should be carefully considered, as it may be more likely to lead to unintended public disclosure.

    <span style="color:#FFFFFF;background-color:#000000">**TLP:CLEAR**</span> is more appropriate for cases where the vulnerability is already public.

    Finally, we observe that CVD is usually geared towards eventually reaching <span style="color:#FFFFFF;background-color:#000000">**TLP:CLEAR**</span>, with <span style="color:#33FF00;background-color:#000000">**TLP:GREEN**</span> being sometimes
    a necessary stopping-off point for certain stakeholders.
