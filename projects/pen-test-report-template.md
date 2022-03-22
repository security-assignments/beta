---
title: Penetration Testing Report Template
---

<style>
blockquote {
  color: #0c5460;
  background-color: #d1ecf1;
  border-color: #bee5eb;
  position: relative;
  padding: 0.75rem 1.25rem;
  margin-bottom: 1rem;
  border-radius: 0.25rem;
}

.table {
  color: #343a40
}
</style>

This page provides a template for a penetration test vulnerability assessment
report. The rubric for each section can be found on the [assignment description
page]({{ site.baseurl }}{% link _projects/pen-test.md %}#rubric).

Remove all colored blocks from your final submission.

---

# Team [team-number] Penetration Testing Report

{: .alert .alert-warning }
_[List team member names here]_

# Executive Summary

{: .alert .alert-warning }
_One-page executive summary that highlights the
most important findings of your report._

---

> Must be no longer than one page. This should be written so that
> non-technical executives can understand.
>
> Describe the number of serious successful
> exploits and the amount of sensitive data you were
> able to obtain.
>
> Give a high-level summary of your recommendations
> to fix the problem.
>
> Don’t describe specifics or use technical terms
> that may be unfamiliar to a non-technical person in
> this section.

# 1.	Project Scope Description

{: .alert .alert-warning }
_Description of the scope of the project, objectives, and your authorization to perform the assessment_

---

> Includes the IP of the computer you
> are attacking, and dates and times that you are given permission to attempt to
> access it.
>
> This should be written so that non-technical executives can understand.

## 1.1.	Objectives

{: .alert .alert-warning }
_Place objectives from the agreement here._


## 1.2.	Authorization

{: .alert .alert-warning }
_A copy of your authorization to perform the threat assessment._

# 2.	Target of Assessment

{: .alert .alert-warning }
_Information about the server examined (i.e., OS, user accounts, applications installed, databases stored)._

---

> Give a brief description of major applications installed, web sites hosted, services running, and
> databases that exist (both database applications, such as MySQL, and information stored within those database
> applications).
>
> **Table -- Server Description**
>
> {: .table style="width: 600px" }
> | Key     | Value     |
> | :------------- | :------------- |
> | Operating System       |        |
> | MAC Address        |       |
> | User accounts       |        |
> | Services running       |        |
> | Major Applications installed       |        |
> | Web sites hosted       |        |
> | Databases, and stored information        |        |



# 3.	Relevant Findings

{: .alert .alert-warning }
_High-level description of vulnerabilities successfully exploited and sensitive data obtained._

---

> Organize for impact. This means you should discuss the most serious vulnerabilities first.
>
> This should be written so that non-technical executives can understand. Define technical terms and concepts described in
> the glossary section.
>
> List sensitive data obtained in the final subsection of section 3. Clearly state the names and paths of files accessed,
> and if secured, how you were able to access them. If files are too numerous to include in the main body of the report,
> list them in an appendix. If you obtain passwords, list what those passwords are._
>
> Include table entries for each exploit and sensitive data obtained.
> Give a brief 1–4 sentence overview of what you were able to accomplish. Then include a cross-reference to a subsection in
> section 4 with supporting details on how you performed the attack. Give a high-level recommendation on what to do to fix
> the problem, cross-referencing a subsection in section 5.
>
> Use the three table templates below.
>
> **Table -- Passwords Obtained**
>
> {: .table style="width: 300px" }
> | User | Password  |
> |:-----|:----------|
> | foo  | P@ssword1 |
> | bar  | monkey    |
>
>
> **Table -- Other Sensitive Information Obtained**
>
> {: .table }
> | Name | Description  | Cross-references |
> |:-----|:----------|-|
> | CEO Emails  | Sensitive emails from CEO criticizing a key corporate business partner | |
> | Customer database  | Customer Personally identifiable information (PII), including email addresses and passport numbers  | |
>
>
> **Table -- Vulnerable Services**
>
> {: .table }
> | Service  | Description  | Cross-references |
> |:-----|:----------|:--|
> | SSH  | The version of SSH installed on the server, WeakSSH, contained a backdoor... Because of this exploit, we were able to > obtain... Please refer to section 4.1 for further details. This problem can be remediated by uninstalling WeakSSH and installing > the latest version of OpenSSH. See section 5.1 for specific remediation steps. | 4.1, 5.1 |
> | FTP  | The server is running FTP application VeryNiceFTPd version X.Y.Z, which is vulnerable to... | Section 4.2, 5.2 |
>
>

# 4.	Supporting Details

{: .alert .alert-warning }
_Supporting details for each of the relevant details listed in the previous section. The detail
should be sufficient for another person to replicate the results of your main findings using your report._

---

> This section should be written so that a technical person can exactly replicate the steps that you performed. List every
> command/step used to perform the attack. This should follow the methodology discussed in class for the steps of
> vulnerability scanning, moving through to the exploitation lab material.
>
> Cross reference sections 3 and 5.
>
> See below for an example.
>
> >4.1.	SSH Backdoor (example)
> >
> >We discovered this vulnerability by… We performed this exploit by (list all steps) by:
> >
> > 1.
> >
> > 2.
> >
> > 3.
> >
> >Because of this exploit we were able to obtain… See section 3.1. See section 5.1 for recommended steps to fix this
> >vulnerability, see section … (end example)

# 5.	Vulnerability Remediation

{: .alert .alert-warning }
_Explanation for how to protect against vulnerabilities successfully exploited and sensitive data obtained. Provide
specific steps._

---

> This section should be written so that a technical person can know what she/he can do to fix the problem.
>
> Cross reference sections 3 and 4.
>
> See below for an example.
>
> > 5.1.	SSH Backdoor (example)
> >
> > Uninstall WeakSSH and install the latest version of OpenSSH. See sections 3.1 and 4.1. (end example)

# 6.	Glossary

{: .alert .alert-warning }
_Define technical terms used in the report here._

# 7.	Appendix A

{: .alert .alert-warning }
_Optional. Include here technical detail that is useful to include for replication or documentation purposes, but would
disrupt the flow of the report because of its length. Number appendices to make them easy to reference from the
“Supporting Details” section._

{: .alert .alert-danger }
_Do **not** submit a Nessus report!_
