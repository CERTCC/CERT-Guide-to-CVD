



1.  [CERT Guide to CVD](index.html)
2.  [The CERT Guide to Coordinated Vulnerability
    Disclosure](The-CERT-Guide-to-Coordinated-Vulnerability-Disclosure_47677443.html)


# [ CERT Guide to CVD : 4. Phases of CVD ]{#title-text} {#title-heading .pagetitle}




Created by [ Allen D. Householder]{.author}, last modified by [
user-8b192]{.editor} on 2021-05-25



*[\"You go through phases. You have to reinvent reasons for playing, and
one year\'s answer might not do for another.\"\
-Yo-Yo Ma]{style="color: rgb(23,43,77);text-decoration: none;"}*

*[\
]{style="color: rgb(23,43,77);text-decoration: none;"}*

T[[here are a number of proposed models of the CVD process that have
slightly varying phases \[1,2,3,4\].
]{style="color: rgb(23,43,77);text-decoration: none;"}]{style="color: rgb(23,43,77);text-decoration: none;"}

[[Below, we adapt a version of the ISO/IEC 30111 \[5\] process with more
phases to better describe what we have seen at the
CERT/CC:]{style="color: rgb(23,43,77);text-decoration: none;"}]{style="color: rgb(23,43,77);text-decoration: none;"}*[\
]{style="color: rgb(23,43,77);text-decoration: none;"}*

-   **Discovery** -- A researcher (not necessarily an academic one)
    discovers a vulnerability by using one of numerous tools and
    processes.
-   **Reporting** -- A researcher submits a vulnerability report to a
    software or product vendor, or a third-party coordinator if
    necessary.
-   **Validation and Triage** -- The analyst validates the report to
    ensure accuracy before action can be taken and prioritizes reports
    relative to others.
-   **Remediation** -- A remediation plan (ideally a software patch, but
    could also be other mechanisms) is developed and tested.
-   **Public Awareness** -- The vulnerability and its remediation plan
    is disclosed to the public.
-   **Deployment** -- The remediation is applied to deployed systems.\
    \

A mapping of CVD phases to CVD roles is provided in Table 2. 


+----------+----------+----------+----------+----------+----------+
| *        | **       | **Re     | **       | **Coord  | **De     |
| *Roles** | Finder** | porter** | Vendor** | inator** | ployer** |
|          |          |          |          |          |          |
| **       |          |          |          |          |          |
| Phases** |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| **Dis    | Finds    | \        | \        | \        | \        |
| covery** | vulnera  |          |          |          |          |
|          | bilities |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| **Rep    | Prepares | Reports  | Receives | Receives | \        |
| orting** | report   | vuls to  | reports  | reports\ |          |
|          |          | v        |          | Acts as  |          |
|          |          | endor(s) |          | reporter |          |
|          |          | and/or   |          | proxy    |          |
|          |          | coor     |          |          |          |
|          |          | dinators |          |          |          |
+----------+----------+----------+----------+----------+----------+
| **Va     | \        | \        | V        | V        | \        |
| lidation |          |          | alidates | alidates |          |
| and      |          |          | reports  | reports  |          |
| Triage** |          |          | r        | r        |          |
|          |          |          | eceived\ | eceived\ |          |
|          |          |          | Pri      | Pri      |          |
|          |          |          | oritizes | oritizes |          |
|          |          |          | report   | report   |          |
|          |          |          | for      | for      |          |
|          |          |          | response | response |          |
+----------+----------+----------+----------+----------+----------+
| **Remed  | \        | Confirms | Prepares | Coo      | \        |
| iation** |          | fix      | patches\ | rdinates |          |
|          |          |          | Develops | mu       |          |
|          |          |          | advice,  | ltiparty |          |
|          |          |          | wor      | r        |          |
|          |          |          | karounds | esponse\ |          |
|          |          |          |          | Develops |          |
|          |          |          |          | advice,  |          |
|          |          |          |          | wor      |          |
|          |          |          |          | karounds |          |
+----------+----------+----------+----------+----------+----------+
| **Public | P        | P        | P        | P        | Receives |
| Awa      | ublishes | ublishes | ublishes | ublishes | report   |
| reness** | report   | report   | report   | report   |          |
+----------+----------+----------+----------+----------+----------+
| **Depl   | \        | \        | \        | \        | Deploys  |
| oyment** |          |          |          |          | fix or   |
|          |          |          |          |          | mi       |
|          |          |          |          |          | tigation |
+----------+----------+----------+----------+----------+----------+


*Table 2:* *Mapping CVD Roles to Phases*

\

We will next discuss each of these phases in more detail.

-   [4.1 Discovery](4.1-Discovery_47677467.html)
-   [4.2 Reporting](4.2-Reporting_47677468.html)
-   [4.3 Validation and Triage](4.3-Validation-and-Triage_47677469.html)
-   [4.4 Remediation](4.4-Remediation_47677470.html)
-   [4.5 Gaining Public
    Awareness](4.5-Gaining-Public-Awareness_47677471.html)
-   [4.6 Promote Deployment](4.6-Promote-Deployment_47677472.html)



\< [3.6. Other Roles and
Variations](3.6.-Other-Roles-and-Variations_47677465.html) \| [4.1
Discovery](4.1-Discovery_47677467.html) \>



## References {#id-4.PhasesofCVD-References}

1.  [ISO/IEC, \"ISO/IEC 29147:2014 Information technology---Security
    techniques---Vulnerability disclosure,\"
    2014.]{style="color: rgb(23,43,77);text-decoration: none;"}
2.  [S. Christey and C. Wysopal, \"Responsible Vulnerability Disclosure
    Process draft-christey-wysopal-vuln-disclosure-00.txt,\"
    February 2002. \[Online\]. Available:
    [https://tools.ietf.org/html/draft-christey-wysopal-vuln-disclosure-00](https://tools.ietf.org/html/draft-christey-wysopal-vuln-disclosure-00){.external-link
    rel="nofollow"}. \[Accessed 17 May
    2017\].]{style="color: rgb(23,43,77);text-decoration: none;"}
3.  [ISO/IEC, \"ISO/IEC 30111:2013 Information technology---Security
    techniques---Vulnerability handling processes,\"
    2013.]{style="color: rgb(23,43,77);text-decoration: none;"}
4.  [J. T. Chambers and J. W. Thompson, \"National Infrastructure
    Advisory Council Vulnerability Disclosure Framework Final Report and
    Recommendations by the Council,\" 13 January 2004. \[Online\].
    Available:
    [https://www.dhs.gov/xlibrary/assets/vdwgreport.pdf](https://www.dhs.gov/xlibrary/assets/vdwgreport.pdf){.external-link
    rel="nofollow"}. \[Accessed 17 May
    2017\].]{style="color: rgb(23,43,77);text-decoration: none;"}
5.  [ISO/IEC, \"ISO/IEC 30111:2013 Information technology---Security
    techniques---Vulnerability handling processes,\"
    2013.]{style="color: rgb(23,43,77);text-decoration: none;"}

\






Document generated by Confluence on 2023-10-27 14:58 -0400






