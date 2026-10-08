---
description: "MITRE ATT\&CK stands for Adversarial Tactics, Techniques, and Common Knowledge."
---

# MITRE ATT&CK

MITRE ATT\&CK stands for Adversarial Tactics, Techniques, and Common Knowledge. It's a globally accessible knowledge base that serves as a living document of adversary tactics and techniques used in cyber attacks. ATT\&CK categorizes these tactics into distinct groups, providing a standardized way to discuss attacker behaviors and improve cyber defenses.

Here's a breakdown of the main categories in the MITRE ATT\&CK framework, along with some additional details and examples for each:

## 1. Reconnaissance

This category focuses on the initial information gathering phase of an attack. Techniques in this category involve activities like identifying targets, discovering system vulnerabilities, and learning about the target environment. Here, attackers are akin to spies, gathering intel to plan their next moves. Some examples include:

* **Social Engineering:** Attackers might impersonate IT support staff, trick employees into revealing login credentials through phishing emails, or exploit social media to gather information about a company's personnel and infrastructure.
* **Scanning:** Attackers use automated tools to scan a target network for open ports, identify devices and services, and search for known vulnerabilities in software versions. This is like probing the defenses of a castle to find weak points.
* **Phishing:** Deceptive emails or messages are crafted to appear legitimate, luring victims into clicking malicious links or downloading attachments that install malware. Phishing emails might impersonate a trusted source like a bank or a colleague, and often prey on urgency or curiosity to trick users into clicking.

## 2. Initial Access

This category covers techniques used by attackers to gain a foothold on a target network or system. Once they have initial access, they can establish persistence, escalate privileges, and move laterally within the network. This is the initial intrusion phase, where attackers breach the perimeter defenses and establish a foothold. Some examples include:

* **Exploiting Public-Facing Applications:** Attackers target vulnerabilities in web applications, VPNs, or other internet-facing services. This might involve exploiting unpatched software or finding weaknesses in authentication mechanisms.
* **Physical Attacks:** In some cases, attackers might gain physical access to devices or systems through social engineering or bypassing physical security measures. This could involve stealing a laptop or compromising a server room with stolen credentials.
* **Supply Chain Attacks:** A more sophisticated approach involves compromising a trusted third-party vendor to gain access to their customers' systems. Attackers might target software vulnerabilities in the vendor's product or inject malicious code during the supply chain process.

## 3. Persistence

Once attackers gain initial access, they often employ techniques to maintain their foothold within the system. Persistence allows them to continue accessing the system even after a reboot or security measures are implemented. This is akin to planting a listening post within enemy territory to maintain a presence and gather further intelligence. Some examples include:

* **Installing Malware:** Attackers might deploy malicious software that provides them with remote access and control over the system. This malware can be designed to hide its presence and evade detection.
* **Creating Hidden Accounts:** Attackers might create unauthorized user accounts with administrator privileges to maintain access and avoid suspicion. These accounts can be carefully disguised to blend in with legitimate accounts.
* **Modifying System Configuration:** Attackers may change system settings to disable security software, automate malicious tasks, or establish persistence mechanisms that ensure continued access even after a system restart.

## 4. Privilege Escalation

Attackers often seek to elevate their privileges within a system to gain access to more sensitive resources and perform more damaging actions. Imagine a thief breaking into a house; they might initially settle for stealing valuables on the ground floor, but they would aim to escalate their access by finding keys to unlock safes or security codes to access higher-value items. Some examples include:

* **Exploiting Local File Inclusion (LFI) vulnerabilities:** Attackers might trick applications into executing arbitrary code on the server. This can give them a foothold on the system and potentially allow them to escalate privileges to gain administrative control.
* **Patch Tampering:** In a more sophisticated attack, attackers might modify legitimate software patches to contain malicious code. When the patch is applied, the attacker code is executed, potentially granting them escalated privileges.
* **Pass-the-Hash Attacks:** Attackers might steal password hashes (scrambled versions of passwords) and use them to authenticate to other systems. This allows them to move laterally across the network without needing to crack the actual passwords.

By understanding the tactics and techniques outlined in the MITRE ATT\&CK framework, organizations can develop more effective defense strategies. They can prioritize patching vulnerabilities, implement security awareness training to counter social engineering attempts, and deploy detection and response mechanisms to identify and stop attackers in their tracks.
