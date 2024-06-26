# How to Find Vulnerabilities

Whether you are a security researcher, a product security engineer, or a
vulnerability coordinator, you may be interested in learning about the
techniques commonly used to find vulnerabilities.
Below , we have compiled a list of techniques that are commonly used to find vulnerabilities in
information systems.

!!! info "About this page"

    In 2014 CERT performed a study of
    [vulnerability discovery techniques for IoT systems](https://insights.sei.cmu.edu/blog/vulnerability-discovery-for-emerging-networked-systems/){:target="_blank"}.
    As we reviewed the literature, we found a number of techniques in common use. 
    Many of the techniques listed below are common to vulnerability discovery in the traditional computing and
    mobile world.
    Some may also prove useful in finding vulnerabilities in AI/ML systems.

!!! question "Are IoT Systems Really that Different?"

    From a security perspective, even mobile systems have a head start, although they are not as far along as traditional
    computing platforms. 
    The fact is that many of the vulnerabilities found
    thus far in IoT would be considered trivial&mdash;and rightly so&mdash;in the
    more mature market of servers and desktop computing. Yet the relative
    scale of the IoT market makes even trivial vulnerabilities potentially
    risky in aggregate.

In the tips below, we summarize the techniques we observed in the
literature, ranked in approximately descending order of
popularity at the time. Although it has been a few years since we
conducted this study, we believe that the techniques are still relevant
today, although their relative popularity may have shifted.

!!! tip "Reading documentation"

    This includes product data sheets, protocol specifications, Internet Drafts and RFCs, manufacturer documentation and
    specs, patents, hardware documentation, support sites, bug trackers, discussion forums, FCC filings, developer 
    documentation, and related information.

!!! tip "Reverse engineering"

    In most cases, this consists of reverse engineering (RE) binary firmware or other software to understand its function.
    However, there are instances in which merely understanding a proprietary file format is sufficient to direct further
    analyses.
    Hardware RE appears in some research, but has not been as prevalent as RE of software or file formats.

!!! tip "Protocol analysis"

    Understanding the communication protocols used by a system is vital to identifying remotely exploitable
    vulnerabilities.
    This technique can take the form of simply sniffing traffic to find mistrusted input or channels, or reverse 
    engineering a proprietary protocol enough to build a fuzzer for it.
    Decoding both the syntax and semantics can be important.
    In wireless systems, this technique can also take the form of using a software defined radio (SDR) to perform signal
    analysis, which for this purpose is essentially protocol analysis at a lower level of the stack.

!!! tip "Threat modeling and simulation"

    Threat modeling from the attacker perspective was mentioned in a handful of papers, as was modeling and simulation
    of either the system or its protocols for further analysis using mathematical techniques such as game or graph theory.

!!! tip "Fuzzing"

    Generating randomized input is a common way to test how a system deals with arbitrary input.
    Fuzzing network protocols is a common method cited in a number of reports.

!!! tip "Input or traffic generation and spoofing"

    Unlike fuzzing, spoofing usually consists of constructing otherwise valid input to a system to cause it to exhibit
    unexpected behavior.
    Constructing bogus input from a valid or trusted source also falls into this category.

!!! tip "Scanning"

    Because most IoT are composed of multiple components, each of which may have its own architecture and code base, 
    it is often the case that a researcher can find known vulnerabilities in systems simply by using available 
    vulnerability scanning tools such as Nessus or Metasploit.

!!! tip "Hardware hacking"

    This technique involves interfacing directly with the electronics at the circuit level.
    It is a form of physical-level reverse engineering and can include mapping circuits and connecting with JTAG to 
    dump memory state or firmware.

!!! tip "Debugging"

    This technique uses software-based or hardware-based debuggers.
    JTAG is a common hardware debugging interface mentioned in many reports.

!!! tip "Writing code"

    This technique involves developing custom tools to assist with extracting, characterizing, and analyzing data to
    identify vulnerabilities.

!!! tip "Application of specialized knowledge and skills"

    In some cases, just knowing how a system works and approaching it with a security mindset is sufficient to find
    vulnerabilities.
    Examples include RFID and ModBus.
