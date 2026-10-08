# Volume Shadow Copy Service

Volume Shadow Copy Service (VSS)

## What is the Volume Shadow Copy Service (VSS)?

* **Built-in Backup Mechanism:** VSS is a Windows service that creates point-in-time snapshots (called "shadow copies") of files and volumes.
* **Data Restoration:** These shadow copies are often used for backup purposes and allow users or system administrators to restore files or previous system states.

## How is VSS Abused by Attackers?

* **Ransomware – Deleting Backups:** Ransomware attacks often aim to encrypt files and then delete shadow copies to cripple the victim's ability to recover without paying the ransom.
* **Data Exfiltration:** Attackers may access shadow copies to steal sensitive data, even if the original file is well-protected.
* **Persistence:** In rare cases, malware might manipulate shadow copies to create a hidden storage location for malicious files, making it harder to detect and remove.

## Detection and Threat Hunting Techniques

1. **Command-Line Monitoring**
   * **vssadmin.exe:** Attackers often use the built-in VSS command-line tool (`vssadmin.exe`) to delete or manipulate shadow copies. Monitor for:
     * `vssadmin delete shadows` commands
     * Commands with parameters like `/all` or `/for=C:` indicating bulk deletion.
   * **wmic.exe:** Attackers may also use the Windows Management Instrumentation Command-line (WMIC) for similar actions. Look for patterns like `shadowcopy delete`.
2. **Security Logs and Event Viewer**
   * **Event IDs:** Search for relevant Event IDs in the System and Application logs:
     * **7036:** The VSS service entered a running or stopped state, indicating its use.
     * Event IDs related to shadow copy creation, deletion, etc. (The exact IDs may vary)
   * **Log Analysis:** Correlate unusual or excessive VSS activity (like bulk deletions) with other suspicious events on the system.
3. **File System Monitoring**
   * Look for rapid deletion of files in directories known to store shadow copies. This might indicate an attempt to disrupt the backup process.
4. **Anomaly Detection**
   * Establish a baseline of normal VSS activity on your systems. Deviations (spikes in shadow copy deletion, unexplained usage outside of backup times) might indicate malicious activity.

## Challenges

* **Legitimate vs. Malicious:** vssadmin.exe is a legitimate tool, making attribution difficult based on its presence alone. Context (time of day, other events) is key.
* **Obfuscation:** Malware authors may try to disguise their usage of VSS tools.

## Important Notes

* **Backup Maintenance:** Having offline or physically isolated backups is crucial to mitigate ransomware scenarios where attackers delete shadow copies.
* **Threat Intelligence:** Regularly update your threat intelligence feeds to stay informed about the latest TTPs (Tactics, Techniques, Procedures) used by attackers targeting VSS.
