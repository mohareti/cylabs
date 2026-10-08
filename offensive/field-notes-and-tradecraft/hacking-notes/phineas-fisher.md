# Phineas Fisher

Title: Hacker Phineas Fisher and the Tools of the Trade

Introduction:

Hacking has always been a game of cat and mouse between cybersecurity experts and those looking to exploit vulnerabilities. One such hacker, known as Phineas Fisher, gained notoriety for their audacious cyber-attacks on prominent organizations and individuals. In this article, we will explore some of the resources and tools Phineas Fisher used to carry out their cyber exploits.

1. Procdump64 and Strings64:

Phineas Fisher was known to utilize powerful tools like Procdump64 and Strings64 to extract valuable information from compromised systems. Procdump64 is a Windows command-line utility that can be used to create memory dumps of running processes. The following command demonstrates its usage:

```text
procdump64 /accepteula -r -ma PID_del_browser
```

Once a memory dump is obtained, Strings64 comes into play. Strings64 is a utility that extracts human-readable strings from binary files. Phineas Fisher used it to search for sensitive data, such as PHPSESSID, in memory dump files:

```text
strings64 /accepteula *.dmp | findstr PHPSESSID 2> null
```

2. PowerSploit - Get-Keystrokes.ps1:

PowerSploit is a collection of PowerShell scripts used for offensive security purposes. Among its many capabilities, one script, Get-Keystrokes.ps1, allows attackers to capture keystrokes on compromised systems. Phineas Fisher might have leveraged this script to gather valuable information, including usernames and passwords, from victims.

[PowerSploit GitHub](https://github.com/PowerShellMafia/PowerSploit/blob/master/Exfiltration/Get-Keystrokes.ps1)

3. LOLBAS (Living Off The Land Binaries And Scripts):

LOLBAS is a project that catalogs various legitimate binaries and scripts that can be abused by attackers for malicious purposes. Phineas Fisher likely used LOLBAS to identify binaries and scripts that blend in with the legitimate system, making it harder for defenders to detect their activities.

[LOLBAS Project](https://lolbas-project.github.io/)

4. Exploit-DB Paper and WiFi-Libre Forum:

Phineas Fisher's exploits and methods have been documented in various places. The Exploit-DB paper and the WiFi-Libre forum are valuable resources for understanding their techniques and the tools they employed.

[Exploit-DB Paper](https://www.exploit-db.com/papers/41914)

[Wifi-Libre Forum](https://www.wifi-libre.com/topic-1268-italia-se-rinde-y-deja-de-buscar-a-phineas-fisher.html)

5. Wired Article and Motherboard Video:

The Wired article and Motherboard video shed light on some of Phineas Fisher's most notorious exploits, including their involvement in the Silk Road 2 hack. These resources provide insights into their motivations and tactics.

[Wired Article](https://www.wired.com/2015/05/silk-road-2/)

[Motherboard Video](https://motherboard.vice.com/en_us/article/59wwxx/fbi-airs-alexandre-cazes-alphabay-arrest-video)

6. Problem Steps Recorder (PSR):

Phineas Fisher demonstrated creativity by using the Problem Steps Recorder (PSR) remotely with Metasploit. PSR is a Windows utility designed for troubleshooting, but it can be exploited by attackers to capture screenshots and record user actions.

[Cyber Arms Blog](https://cyberarms.wordpress.com/2016/02/13/using-problem-steps-recorder-psr-remotely-with-metasploit/)

7. Empire and Metasploit:

Phineas Fisher relied on penetration testing frameworks like Empire and Metasploit to gain unauthorized access to systems, maintain persistence, and exfiltrate data. These frameworks provide a wide range of exploits and post-exploitation tools.

[Empire GitHub](https://github.com/EmpireProject/Empire)

[Metasploit Framework GitHub](https://github.com/rapid7/metasploit-framework)

8. HackTricks:

The HackTricks book is a comprehensive resource that covers various hacking techniques, including brute force attacks. Phineas Fisher may have referred to this resource for guidance on different attack vectors and strategies.

[HackTricks Book](https://book.hacktricks.xyz/brute-force)

Conclusion:

Phineas Fisher's hacking exploits demonstrated not only technical prowess but also a deep understanding of the tools and resources available to cybercriminals. While their actions may have raised ethical concerns, they serve as a reminder of the ongoing battle between cybersecurity professionals and those seeking to exploit vulnerabilities for personal gain or ideological reasons. It is crucial for organizations and individuals to stay vigilant and implement robust security measures to defend against such threats.
