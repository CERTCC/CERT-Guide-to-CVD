!!! warning "Use caution with TLP:RED and TLP:AMBER+STRICT"
 

    We have found that TLP:RED is too restrictive for an organization to effectively respond to a vulnerability.
    For example, the analyst who receives a TLP:RED report might not be able to share it with their manager or their team.
    In a Vendor context, this might mean that the person who receives the report cannot share it with the team responsible for fixing the vulnerability.

    TLP:AMBER+STRICT might be okay for a Reporter working with a single Vendor only, or when a Vendor 
    wants retain control over the disclosure process to other Vendors or Coordinators.
    However, it limits the ability of the receiving party to engage others who might be able to help.
    A Vendor in receipt of a TLP:AMBER+STRICT report cannot share it with their upstream or downstream Vendors.
    Nor can they share it with Coordinators who might be able to help them reach other affected parties.
    Similarly, a Coordinator in receipt of a TLP:AMBER+STRICT report cannot share it with other Coordinators or Vendors,
    which severely limits their ability to assist with the coordination process.
    It is not impossible to do CVD with TLP:AMBER+STRICT, but it is more difficult and less effective.

    Therefore we recommend TLP:AMBER for most cases prior to public disclosure. 

    TLP:GREEN can be useful for cases nearing public disclosure, for example when necessary to engage critical infrastructure
    through ISACs, ISAOs, or other trusted channels. In some larger multiparty cases, TLP:GREEN might be useful to reach
    a broader audience of potentially affected vendors, deployers and other stakeholders. However, the use of TLP:GREEN 
    should be carefully considered, as it may be more likely to lead to unintended public disclosure.

    TLP:CLEAR is more appropriate for cases where the vulnerability is already public.

    Finally, we observe that CVD is usually geared towards eventually reaching TLP:CLEAR, with TLP:GREEN being sometimes
    a necessary stopping-off point for certain stakeholders.
