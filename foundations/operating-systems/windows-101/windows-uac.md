# Windows UAC

Windows User Account Control (UAC)

## What is UAC?

* **Security Layer:** UAC is a Windows security feature designed to prevent unauthorized changes to the system.
* **Prompts:** When a program needs administrative privileges, UAC triggers a prompt, requiring the user to either approve or deny the requested elevation.
* **Goal:** Limit the potential for malware to silently obtain administrator-level access and make harmful changes.

## Types of UAC Attacks

* **UAC Bypass:** These attacks attempt to execute malicious code with elevated privileges without triggering a UAC prompt. Techniques can include:
  * **DLL Hijacking:** Exploiting vulnerabilities in how programs load DLL files to inject malicious code.
  * **Fileless UAC Bypasses:** Using existing, trusted Windows binaries for malicious activities (e.g., through tools like PowerShell).
* **UAC Prompt Spoofing/Social Engineering:** Aim to trick the user into clicking "Yes" on a fake UAC prompt, authorizing the malware. These attacks often disguise the malicious program as legitimate software updates or installers.
* **Consent Fatigue:** Repeatedly bombard the user with legitimate UAC prompts with the hope that they'll get tired of them and carelessly approve a malicious request.

## Why target UAC?

* **Elevated Privileges:** Bypassing or subverting UAC allows attackers to gain the administrative power they need to install rootkits, disable security features, steal sensitive data, or cause major system damage.

## How to Protect Yourself

* **Keep System and Software Updated:** Patches fix known vulnerabilities attackers exploit for UAC bypasses.
* **Run as Standard User:** Avoid using an admin account for everyday tasks to limit the damage if malware successfully gets elevated privileges.
* **Scrutinize UAC Prompts:** Pay close attention to the publisher and what the program is requesting. Don't blindly approve prompts.
* **Consider a Security Solution:** Antivirus and anti-malware software can offer additional layers of protection and may detect malicious behavior.

## Examples of UAC Attacks (Simplified)

* **DLL Hijacking Example:** An attacker places a malicious DLL with the same name as a legitimate DLL in a directory a program is likely to search. When the program executes, UAC bypass occurs if it loads the malicious DLL, allowing the attacker's code to run with elevated privileges.
* **Social Engineering Example:** Malware displays a fake UAC prompt resembling a system update. An unsuspecting user who clicks "Yes" unwittingly grants administrative privileges to the malware.

## Important Notes

* UAC is not a foolproof security mechanism and can be bypassed.
* User vigilance is a crucial defense against these kinds of attacks.
