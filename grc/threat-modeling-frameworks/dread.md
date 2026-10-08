---
description: "DREAD is a risk assessment model used in cybersecurity to prioritize security threats based on five key factors."
---

# DREAD

DREAD is a risk assessment model used in cybersecurity to prioritize security threats based on five key factors. It's a mnemonic that stands for:

* **Damage Potential:** This refers to the severity of the potential damage that a threat could cause if it's successful. This might include financial losses, data breaches, reputational harm, or disruption of critical operations. The higher the potential damage, the greater the risk.
* **Reproducibility:** This assesses how easily an attacker can replicate the exploit or threat. If an attack is easily reproducible with readily available tools, it poses a higher risk compared to a complex, one-off exploit.
* **Exploitability:** This evaluates the existing vulnerabilities within a system that could be leveraged by the threat. If a system has strong security measures in place and the attack requires a complex series of vulnerabilities to be exploited, the risk is lower.
* **Affected Users:** This considers the number of users or systems that could be impacted by the threat. A widespread attack affecting a large number of users poses a greater risk compared to a targeted attack on a single individual.
* **Discoverability:** This assesses how easily the threat can be identified and detected. If a vulnerability or attack method is readily detectable through security tools or monitoring, it allows for quicker mitigation and reduces the risk.

## Using DREAD

* Each category within DREAD is typically assigned a rating on a scale (often 0-10), with higher values indicating a greater risk factor.
* The individual ratings for each category are then averaged to obtain an overall risk score for the threat.
* Based on the overall DREAD score, organizations can prioritize their security efforts by focusing on addressing the threats with the highest scores first. This helps them allocate resources efficiently and mitigate the most critical risks.

## Limitations of DREAD

* **Subjectivity:** The rating system within DREAD can be subjective, as the perceived impact and exploitability might vary depending on the organization's specific context and priorities.
* **Limited Scope:** DREAD focuses primarily on the technical aspects of a threat and might not fully account for broader business considerations beyond the technical impact.

**DREAD remains a simple and effective tool for initial threat assessment and prioritization. It provides a quick way to categorize and compare various security threats, allowing organizations to make informed decisions about resource allocation and security mitigation strategies.**

Here's a quick comparison of STRIDE and DREAD:

* **STRIDE:** Focuses on different types of threats (Spoofing, Tampering, etc.) and helps identify potential vulnerabilities.
* **DREAD:** Focuses on assessing the severity and exploitability of identified threats to prioritize risks.
