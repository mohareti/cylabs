---
description: "Windows Registry Editor (regedit.exe) and key registry locations to monitor for signs of malicious activity."
---

# Windows Registry

Windows Registry Editor (regedit.exe) and key registry locations to monitor for signs of malicious activity.

## What is the Registry Editor (regedit.exe)?

* **Hierarchical Database:** The Windows Registry is a massive database storing system-wide and program-specific configuration settings, hardware information, user preferences, and more.
* **Registry Editor:** Allows you to directly view and edit entries (keys and values) within the registry.
* **Caution:** Incorrect changes to the registry can seriously damage your system. Proceed with extreme care.

## Key Registry Locations for Auditing Malicious Activity

Here are common registry hives and keys attackers often target:

* **HKEY\_LOCAL\_MACHINE (HKLM) \Software\Microsoft\Windows\CurrentVersion\Run and RunOnce:** These keys control programs that start automatically at system boot or user login. Malware often adds persistence mechanisms here.
* **HKLM\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\Run:** Similar to the above, an additional location for autostart programs.
* **HKLM\SYSTEM\CurrentControlSet\Services:** Stores information about system services. Malware might create new services here or modify existing ones.
* **HKEY\_CURRENT\_USER (HKCU) \Software\Microsoft\Windows\CurrentVersion\Run and RunOnce:** The user-specific versions of autostart keys. Malware might target these to only affect the compromised user account.
* **HKCU\Software\Microsoft\Internet Explorer\Main:** Stores Internet Explorer settings. Malware may modify these for browser redirects, data interception, or other tampering.
* **HKCU\Software\Classes:** Defines file associations. Malware could modify these to execute malicious code when specific file types are opened.

## What to Look For

* **Suspicious Keys and Values:** Unknown entries (especially with unusual names) in the locations mentioned above warrant investigation.
* **Modification of Autostart Entries:** Check for new entries you don't recognize that point to unfamiliar executable files.
* **Changes to Browser or System Settings:** Look for unexpected modifications in internet settings, proxy configurations, or system-level policies.
* **Hidden Keys:** Malware may try to hide registry entries by manipulating their properties.

## Important Considerations

* **Attribution Is Difficult:** Finding a malicious registry entry doesn't always directly identify the specific piece of malware.
* **Time is Crucial:** Malware may modify the registry and immediately trigger actions or remain dormant for prolonged periods.
* **Baseline Comparisons:** Having a "clean" snapshot of a system's registry is invaluable for comparison during incident investigations.
* **Malware Obfuscation:** Malware can use techniques to disguise registry entries.

## Additional Resources

* Microsoft has documentation detailing the structure of the registry: <https://docs.microsoft.com/en-us/windows/win32/sysinfo/registry>.
* Security blogs and threat intelligence sites often release reports detailing specific registry keys and values employed by different malware families.
