# Appendix F - Additional Resources for Web Vulnerabilities 

# Summary {#AppendixFAdditionalResourcesforWebVulnerabilities-Summary}

The following is a list of resources on mitigating, remediating, and
preventing vulnerabilities, for system owners that receive a
vulnerability reports via their CVD process. After validation is
performed on the report, these resources assist in determining an
appropriate remediation response. 

Vulnerabilities present in current operational systems must be
remediated after a proper validation and risk assessment are performed.
Custom development should integrate secure coding practices, and risk
analysis should be performed before the custom web application is placed
on the internet in operation.

-   [Summary](#AppendixFAdditionalResourcesforWebVulnerabilities-Summary)
-   [Overview](#AppendixFAdditionalResourcesforWebVulnerabilities-Overview)
-   [Testing and Validation of Web
    Vulnerabilities](#AppendixFAdditionalResourcesforWebVulnerabilities-TestingandValidationofWebVulnerabilities)
    -   [Client-based Testing
        Tools](#AppendixFAdditionalResourcesforWebVulnerabilities-Client-basedTestingTools)
    -   [Web-based Testing
        Tools](#AppendixFAdditionalResourcesforWebVulnerabilities-Web-basedTestingTools)
-   [Vulnerability Remediation
    Resources](#AppendixFAdditionalResourcesforWebVulnerabilities-VulnerabilityRemediationResources)
-   [Development
    Resources](#AppendixFAdditionalResourcesforWebVulnerabilities-DevelopmentResources)

# Overview {#AppendixFAdditionalResourcesforWebVulnerabilities-Overview}

Vulnerability mitigation consists of two distinct processes.

First, during development and deployment, web applications should be
developed with secure coding practices after threat modeling, risk
analysis, and secure design are is performed. The application should be
deployed following best system administration practices. Testing tools
can be used identify vulnerabilities before the application is deployed.

Second, after deployment, vulnerabilities discovered in active
production web applications will need to be remediated based on
severity, impact, threat, and other risk factors. Testing tools can
again be used to identify vulnerabilities and help monitor deployed
applications.

Below are resources that may be useful for secure design and
development, testing and vulnerability identification, understanding
common web application vulnerabilities, and vulnerability mitigation and
remediation.

# Testing and Validation of Web Vulnerabilities {#AppendixFAdditionalResourcesforWebVulnerabilities-TestingandValidationofWebVulnerabilities}

To perform testing and validation of reported web vulnerabilities, we
recommend the use of[ a Windows virtual machine (VM) running a recent
version of Windows with Firefox, Chrome, Burp Suite, and OWASP ZAP
installed, along with any dependencies. Linux and/or Mac OS systems are
recommended for additional tool support, but are not
necessary.]{style="letter-spacing: 0.0px;"}

To the extent possible, validation is best performed from an open
*public internet*-like network. Enterprise web proxy or other filtering
or inspection systems can negatively affect the behavior of validation
tools. In many cases, it's possible to configure the tools to be
proxy-aware, however some proxy or inspection systems can prevent tools
from functioning properly. Firewall rules must allow necessary traffic,
usually (but not always) outbound connections to HTTP/S ports TCP 80 and
443. FTP and SMTP services have also been needed in validation.

## Client-based Testing Tools {#AppendixFAdditionalResourcesforWebVulnerabilities-Client-basedTestingTools}

+--------------+----------------------+-------------------------------+
| Tool         | Notes                | Link(s)                       |
+--------------+----------------------+-------------------------------+
| Virtual      | Due to the small     | [https://www                  |
| Machine      | chance that a report | .linux-kvm.org/page/Main_Page |
| Validation   | will contain         | ](https://www.linux-kvm.org/p |
| Workstation  | malicious a          | age/Main_Page){.external-link |
|              | proof-of-concept or  | rel="nofollow"}               |
|              | Trojan horse,        |                               |
|              | recovery and         | [https:                       |
|              | containment may be   | //www.vmware.com/](https://ww |
|              | easier if analysts   | w.vmware.com/){.external-link |
|              | use virtual machines | rel="nofollow"}               |
|              | for validation       |                               |
|              | workstations.        | [https://www.vi               |
|              |                      | rtualbox.org/](https://www.vi |
|              |                      | rtualbox.org/){.external-link |
|              |                      | rel="nofollow"}               |
|              |                      |                               |
|              |                      | (or any other virtualization  |
|              |                      | tool)                         |
+--------------+----------------------+-------------------------------+
| Web Browsers | Analysts should have | Internet Explorer             |
|              | access to Internet   |                               |
|              | Explorer, Firefox,   | [https://www.microsoft.com/en |
|              | Chrome, and Edge     | -us/download/internet-explore |
|              | with any necessary   | r.aspx](https://www.microsoft |
|              | enterprise           | .com/en-us/download/internet- |
|              | certificate          | explorer.aspx){.external-link |
|              | authorities          | rel="nofollow"}               |
|              | installed.           |                               |
|              |                      | Firefox                       |
|              |                      |                               |
|              |                      | [https:/                      |
|              |                      | /www.mozilla.org/en-US/firefo |
|              |                      | x/](https://www.mozilla.org/e |
|              |                      | n-US/firefox/){.external-link |
|              |                      | rel="nofollow"}               |
|              |                      |                               |
|              |                      | Chrome                        |
|              |                      |                               |
|              |                      | [https://www.google.c         |
|              |                      | om/chrome/](https://www.googl |
|              |                      | e.com/chrome/){.external-link |
|              |                      | rel="nofollow"}               |
|              |                      |                               |
|              |                      | Edge                          |
|              |                      |                               |
|              |                      | [https://ww                   |
|              |                      | w.microsoft.com/en-us/windows |
|              |                      | /microsoft-edge](https://www. |
|              |                      | microsoft.com/en-us/windows/m |
|              |                      | icrosoft-edge){.external-link |
|              |                      | s                             |
|              |                      | tyle="letter-spacing: 0.0px;" |
|              |                      | rel="nofollow"}               |
|              |                      |                               |
|              |                      | Safari                        |
|              |                      |                               |
|              |                      | [https://www.apple.           |
|              |                      | com/safari/](https://www.appl |
|              |                      | e.com/safari/){.external-link |
|              |                      | rel="nofollow"}               |
+--------------+----------------------+-------------------------------+
| Burp Suite   | Requires Java JRE.   | [https://portswigge           |
|              |                      | r.net/burp/](https://portswig |
|              |                      | ger.net/burp/){.external-link |
|              |                      | rel="nofollow"}               |
+--------------+----------------------+-------------------------------+
| OWASP ZAP    | Requires Java JRE.   | [                             |
|              |                      | https://github.com/zaproxy/za |
|              |                      | proxy/wiki/Downloads](https:/ |
|              |                      | /github.com/zaproxy/zaproxy/w |
|              |                      | iki/Downloads){.external-link |
|              |                      | rel="nofollow"}               |
+--------------+----------------------+-------------------------------+
| Firefox      | There are several    | Web Developer Add-on\         |
| Add-ons      | Firefox add-ons      | [https://addons.mozilla.o     |
|              | which can aid in     | rg/en-US/firefox/addon/web-de |
|              | validating reports.  | veloper/](https://addons.mozi |
|              |                      | lla.org/en-US/firefox/addon/w |
|              |                      | eb-developer/){.external-link |
|              |                      | rel="nofollow"}               |
|              |                      |                               |
|              |                      | Firebug\                      |
|              |                      | [https://addo                 |
|              |                      | ns.mozilla.org/en-US/firefox/ |
|              |                      | addon/firebug/](https://addon |
|              |                      | s.mozilla.org/en-US/firefox/a |
|              |                      | ddon/firebug/){.external-link |
|              |                      | rel="nofollow"}               |
|              |                      |                               |
|              |                      | Proxy Switcher\               |
|              |                      | [https://addons.mozilla.org   |
|              |                      | /en-US/firefox/addon/proxy-sw |
|              |                      | itcher/](https://addons.mozil |
|              |                      | la.org/en-US/firefox/addon/pr |
|              |                      | oxy-switcher/){.external-link |
|              |                      | rel="nofollow"}               |
|              |                      |                               |
|              |                      | Tamper Data\                  |
|              |                      | [https://addons.mozil         |
|              |                      | la.org/en-US/firefox/addon/ta |
|              |                      | mper-data/](https://addons.mo |
|              |                      | zilla.org/en-US/firefox/addon |
|              |                      | /tamper-data/){.external-link |
|              |                      | rel="nofollow"}               |
|              |                      |                               |
|              |                      | RESTClient\                   |
|              |                      | [https://addons.moz           |
|              |                      | illa.org/en-US/firefox/addon/ |
|              |                      | restclient/](https://addons.m |
|              |                      | ozilla.org/en-US/firefox/addo |
|              |                      | n/restclient/){.external-link |
|              |                      | rel="nofollow"}               |
|              |                      |                               |
|              |                      | Cookies Manager+\             |
|              |                      | [https://a                    |
|              |                      | ddons.mozilla.org/en-US/firef |
|              |                      | ox/addon/cookies-manager-plus |
|              |                      | /](https://addons.mozilla.org |
|              |                      | /en-US/firefox/addon/cookies- |
|              |                      | manager-plus/){.external-link |
|              |                      | rel="nofollow"}               |
+--------------+----------------------+-------------------------------+
| cURL         | Command-line         | [ht                           |
|              | interaction with     | tps://curl.haxx.se/](https:// |
|              | HTTP/HTTPS services. | curl.haxx.se/){.external-link |
|              |                      | rel="nofollow"}               |
+--------------+----------------------+-------------------------------+
| sqlmap       | Requires Python 2.7. | [http://sqlmap.org/](http:    |
|              |                      | //sqlmap.org/){.external-link |
|              |                      | rel="nofollow"}               |
+--------------+----------------------+-------------------------------+
| Metasploit   | \                    | [[https:                      |
| Framework    |                      | //www.rapid7.com/products/met |
|              |                      | asploit/download/](https://ww |
|              |                      | w.rapid7.com/products/metaspl |
|              |                      | oit/download/){.external-link |
|              |                      | rel="nofollow"}]{st           |
|              |                      | yle="color: rgb(171,34,22);"} |
+--------------+----------------------+-------------------------------+
| testssl.sh   | Requires Linux       | [https://testssl.sh/](https:  |
|              | platform.            | //testssl.sh/){.external-link |
|              |                      | rel="nofollow"}               |
+--------------+----------------------+-------------------------------+

## Web-based Testing Tools {#AppendixFAdditionalResourcesforWebVulnerabilities-Web-basedTestingTools}

Tools may be used during development as well as after deployment. Since
standards and best practices change over time, it is a good idea to
periodically re-test deployed applications.

+--------------+----------------------+-------------------------------+
| Tool         | Notes                | Link(s)                       |
+--------------+----------------------+-------------------------------+
| [S           | Website-based        | [https://securi               |
| ecurityheade | testing tool that    | tyheaders.io/](https://securi |
| rs.io](http: | checks a deployed    | tyheaders.io/){.external-link |
| //Securityhe | website for HTTP     | rel="nofollow"}               |
| aders.io){.e | header security best |                               |
| xternal-link | practices and        |                               |
| rel          | provides a list of   |                               |
| ="nofollow"} | recommended          |                               |
|              | standards and best   |                               |
|              | practices.           |                               |
+--------------+----------------------+-------------------------------+
| OWASP        | Explanations and     | [https://www.owasp.org/       |
| Security     | implementation       | index.php/OWASP_Secure_Header |
| Headers      | guidance for HTTP    | s_Project](https://www.owasp. |
| Project      | security headers.    | org/index.php/OWASP_Secure_He |
|              |                      | aders_Project){.external-link |
|              |                      | rel="nofollow"}               |
+--------------+----------------------+-------------------------------+
| SSL Labs     | Website-based        | [https://www.ssllabs.com/     |
| Server Test  | testing tool that    | ssltest/](https://www.ssllabs |
|              | checks if deployed   | .com/ssltest/){.external-link |
|              | website uses proper  | rel="nofollow"}               |
|              | SSL/TLS certificates |                               |
|              | and configuration.   |                               |
|              | The tool provides a  |                               |
|              | grade for the        |                               |
|              | website and          |                               |
|              | appropriate          |                               |
|              | recommendations if   |                               |
|              | any tests are        |                               |
|              | failed.              |                               |
+--------------+----------------------+-------------------------------+
| *            | Website-based        | [https://badssl.com/](https:  |
| *[Badssl.com | testing tool for     | //badssl.com/){.external-link |
| ](http://bad | ensuring clients     | rel="nofollow"}               |
| ssl.com/){.e | (not servers) are    |                               |
| xternal-link | properly configured  |                               |
| rel="        | for using SSL/TLS.   |                               |
| nofollow"}** | May not be necessary |                               |
|              | depending on the     |                               |
|              | service.             |                               |
+--------------+----------------------+-------------------------------+
| **OWASP      | Tool for detecting   | [https://w                    |
| WAP**        | vulnerabilities in   | ww.owasp.org/index.php/OWASP_ |
|              | PHP web              | WAP-Web_Application_Protectio |
|              | applications.        | n](https://www.owasp.org/inde |
|              |                      | x.php/OWASP_WAP-Web_Applicati |
|              |                      | on_Protection){.external-link |
|              |                      | rel="nofollow"}               |
+--------------+----------------------+-------------------------------+



# Vulnerability Remediation Resources {#AppendixFAdditionalResourcesforWebVulnerabilities-VulnerabilityRemediationResources}

Once the web application is deployed, the application, server, or other
components may need updates, patches, or other changes to address
vulnerabilities as they are discovered. In some cases, the system owner
or their developer will need to develop the mitigation or remediation.

  --------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------ ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Resource                                            Notes                                                                                                                                Link(s)
  How to Win Friends and Remediate Vulnerabilities    Whitepaper from SANS Institute with advice on setting up a remediation capability.                                                   [https://www.sans.org/reading-room/whitepapers/application/win-friends-remediate-vulnerabilities-34530](https://www.sans.org/reading-room/whitepapers/application/win-friends-remediate-vulnerabilities-34530) 
  Guide to Enterprise Patch Management Technologies   NIST report on managing patches for vulnerability remediation                                                                        [http://dx.doi.org/10.6028/NIST.SP.800-40r3](http://dx.doi.org/10.6028/NIST.SP.800-40r3) 
  SQL Injection Prevention                            Advice on avoiding and fixing SQL injection vulnerabilities from OWASP                                                               [https://www.owasp.org/index.php/SQL_Injection_Prevention_Cheat_Sheet](https://www.owasp.org/index.php/SQL_Injection_Prevention_Cheat_Sheet) 
  Cross-Site Scripting                                Advice on preventing and fixing cross-site scripting (XSS) vulnerabilities from Google.                                              [https://www.google.com/about/appsecurity/learning/xss/#PreventingXSS](https://www.google.com/about/appsecurity/learning/xss/#PreventingXSS)
  Common Weakness Enumeration (CWE)                   CWE provides a taxonomy of different types of vulnerabilities. Many CWE entries provide brief advice on potential mitigations.       [https://cwe.mitre.org/](https://cwe.mitre.org/) 
  CWE/SANS Top 25 Most Dangerous Software Errors      List of dangerous vulnerabilities, the *Insecure Interaction Between Components* section contains web application vulnerabilities.   [[https://www.sans.org/top25-software-errors/](https://www.sans.org/top25-software-errors/)]{style="color: rgb(171,34,22);"}
  OWASP Top Ten Project                               A list of the ten most critical web application security risks.                                                                      [[https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project)]{style="color: rgb(171,34,22);"}
  Web Application Security Consortium (WASC)          Collection of web application security resources.                                                                                    [[http://www.webappsec.org/](http://www.webappsec.org/)]{style="color: rgb(171,34,22);"}
  --------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------ ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Development Resources {#AppendixFAdditionalResourcesforWebVulnerabilities-DevelopmentResources}

A threat model of the service or web application being provided should
be developed earlier in the process to help make architecture decisions
that will keep the application more secure. Below are resources for
creating and using a threat model for development or deployment, as well
as secure coding development principles.

+---------------+----------------------------+-------------------------+
| Resource      | Notes                      | Link(s)                 |
+---------------+----------------------------+-------------------------+
| Threat        | "A [structured approach   | [https://owasp          |
| Modeling      | to application threat      | .org/www-community/Thre |
| Process by    | modeling that enables you  | at_Modeling_Process](ht |
| OWASP         | to identify, quantify, and | tps://owasp.org/www-com |
|               | address the security risks | munity/Threat_Modeling_ |
|               | associated with an         | Process){.external-link |
|               | application]{styl          | rel="nofollow"}         |
|               | e="color: rgb(0,0,0);"}." |                         |
+---------------+----------------------------+-------------------------+
| *Threat       | A book of material on how  | [https://th             |
| Modeling*     | to properly perform threat | reatmodelingbook.com](h |
| book by Adam  | modeling for a number of   | ttps://threatmodelingbo |
| Shostack      | scenarios. The author also | ok.com/){.external-link |
|               | offers training courses.   | rel="nofollow"}         |
+---------------+----------------------------+-------------------------+
| Open Web      | A short guide for secure   | [https:                 |
| Application   | coding principles          | //www.owasp.org/index.p |
| Security      | specifically tailored for  | hp/OWASP_Secure_Coding_ |
| Project       | web applications.          | Practices\_-\_Quick_Ref |
| (OWASP)       |                            | erence_Guide](https://w |
| Secure Coding |                            | ww.owasp.org/index.php/ |
| Guide         |                            | OWASP_Secure_Coding_Pra |
|               |                            | ctices_-_Quick_Referenc |
|               |                            | e_Guide){.external-link |
|               |                            | rel="nofollow"}         |
+---------------+----------------------------+-------------------------+
| CERT Secure   | Secure coding standards    | [https://www.secur      |
| Coding        | should be followed to      | ecoding.cert.org/](http |
| Standards     | avoid vulnerabilities as   | s://www.securecoding.ce |
|               | much as possible. CERT     | rt.org/){.external-link |
|               | provides coding standards  | rel="nofollow"}         |
|               | for common web application |                         |
|               | programming languages like |                         |
|               | Java and Perl. Note that   |                         |
|               | the standards were         |                         |
|               | developed for general      |                         |
|               | usage, and not all rules   |                         |
|               | may apply to web           |                         |
|               | applications.              |                         |
+---------------+----------------------------+-------------------------+
| The Basics of | Summary of important web   | [https://martinfowle    |
| Web           | application secure         | r.com/articles/web-secu |
| Application   | development practices.     | rity-basics.html](https |
| Security      |                            | ://martinfowler.com/art |
|               |                            | icles/web-security-basi |
|               |                            | cs.md){.external-link |
|               |                            | rel="nofollow"}         |
+---------------+----------------------------+-------------------------+
| Basic         | Microsoft web application  | [https://msd            |
| Security      | security advice.           | n.microsoft.com/en-us/l |
| Practices for |                            | ibrary/zdh19h94.aspx](h |
| Web           |                            | ttps://msdn.microsoft.c |
| Applications  |                            | om/en-us/library/zdh19h |
|               |                            | 94.aspx){.external-link |
|               |                            | rel="nofollow"}         |
+---------------+----------------------------+-------------------------+





























