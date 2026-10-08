# Windows Event Logs and IDs

## Types of Windows Event Logs

* **Application:** Events logged by specific programs and applications.
* **Security:** Tracks security-related events like logins, logoffs, privilege use, and policy changes. This is a critical log for threat hunting.
* **Setup:** Events related to software installation and setup processes.
* **System:** Logs events from Windows system components (e.g., drivers, services).
* **Forwarded Events:** Consolidates events from remote systems.

## Key Event IDs for Threat Hunters

(Note: This is not an exhaustive list, but some particularly valuable IDs)

## Security Log

* **4624: Successful Logon:** Tracks all successful login attempts, both local and network-based.
  * Threat Hunting Value: Establish a baseline of normal logins, track user activity, and look for anomalous logins or brute-force attacks.
* **4625: Failed Logon:** Records unsuccessful logins.
  * Threat Hunting Value: Identifies brute-force attempts, unauthorized access attempts, or accidental mistyping of credentials.
* **4672: Special privileges assigned to new logon:** Indicates when a user has been granted administrator or other elevated privileges.
  * Threat Hunting Value: Monitor for privilege escalation and unauthorized changes.
* **4720: A user account was created:** Tracks the creation of new accounts.
  * Threat Hunting Value: Detects threat actors attempting to create backdoors or additional accounts.
* **4798: A user's local group membership was enumerated:** Shows when someone investigates user groups on a system.
  * Threat Hunting Value: Can indicate reconnaissance activity by a threat actor to learn about the compromised machine.

## System Log

* **7045: A new service was installed:** Indicates the installation of new services.
  * Threat Hunting Value: Detecting new, potentially malicious services.
* **104, 1102: Event log cleared, Security log full:**
  * Threat Hunting Value: Can indicate an attacker covering their tracks by deleting logs.

## Additional Considerations

* **Log Volume:** Some Event IDs are noisier than others (like successful logins). Balance importance with log volume.
* **Event Context:** Event IDs alone aren't always conclusive. Correlate events for a clearer picture. Example: Multiple failed logins (4625) followed by one successful (4624) might indicate a breach.
* **Threat Intelligence:** Incorporate threat intelligence feeds to gain context about newly documented Event IDs related to specific attacks or malware.
* **Log Collection and Analysis:** Use SIEM tools or similar solutions to centralize logs from multiple systems to make analysis effective.
