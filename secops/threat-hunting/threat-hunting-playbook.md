# Threat Hunting Playbook

Threat hunting

* Organization mission
* Threat Actors targeting Aviation Industry
* What are the critical assets and businesses
* Who targeting DFW Airport
* Do any third party companies targeted in process of attacking us
* Which exploits are used for attacks
* Which APT targets us

* Hypothesis
  * AISAC and recent TTP's and cyber attacks
  * Blind spots in organization
  * Tools and techniques used by Threat Actors
  * Data infiltration and Exfiltration Techniques
  * IOC's and adversary TTP's
  * Investigate
    * TTPS
    * Analytics
* Creating threat detection rules
* Collecting Malware Samples  and fetch new patterns and TTP's
* Getting alerts to Incident Response
* Security Analytics and

Before starting Threat Hunting

Which Threat Actors targeting

* Aviation ports
* Airline, Transport Industry
* Geo Political

Focus on attack techniques

Focus on critical assets and information

* Crown Jewels Analysis (CJA)

Threat hunting Models/Framework

* Diamond Model of Intrusion Analysis
* MITRE ATTACK
* BAS Threat Library (picus)

List of threat hunting tools

* Data sources from MITRE attack
* Data visibility
* Historical data for threat hunting

* Threat Hunting Maturity Model\
  breach attack simulation model
* Sqrrl

Know thy self

* Reconnaissance
* Osint
* Asset inventory
* Network segmentation
* Patching
* Backup

Pyramid of pain

Threat hunting

* Start with applications
* Browser plugins
* System level event
* Host perimeter
* Edge firewalls

Tools

* Phishing catcher
* Dnstwist
* Gnuplot
* Apiify
* Query isc api for IP based threat intel
* Domain\_Stats from sans

Cloud attacks

* Need to implement logging
* Password spraying
* One dirve log analysis
* Cloudtrail logs

Know normal

* Local users
* ASEP's  entry points
* Trusted Root certs
* Entropy in filenames
* Entropy in dns
* Freq in dns and filenames
* Services
* Open ports
* In and outbound communication
* Arp entries
* Software installed
* Processes
* Authorized hosts files
* Host file
* DNS  and IP
* Same first name and last name and sender email address changed
* Email forwarding rules
* User at risk
* Sign in infected device
* Sign in from unknown location
* Understanding user privileges
* Singn in anonymous vpn, tor,
* Dropbox kind of tool communication
* Use of I2p, Tor, socks
* Slow in application performance
* Autstart program and scripts
* Unique processes
* Host
  * profiling by segments
  * profiling by zones
    * Windows servers
    * Linux servers
    * Developers
    * Testing team
    * Database team
    * HR ateam
    * Procurement team
    * Legacy systesm
    * PCI environment
    * Extranet
    * Network team
    * Production
    * Dev
    * Tst
    * PCN/SCADA/IOT/OT
    * High value/business critical
    * Process injection attempts
    * DLL sideloading
    * File deletes
    * Hunting Powershell Obfuscation with Linear Regression
  * Network
    * Site to site vpns
    * Long connections
    * Vpn acitivity
    * Beaconing activity
  * Jpcertcc.github.io
  * Dnsespinoge
  * DNSSEC
  * Security trails dns change
  * Domain fronting
  * National cyber security centere TLS interception
  * RITA TLS interception
  * Recursive dns name servers
  * Authorative dns name server
* Tools
  * ELK
  * OS Query
  * Fleet Kolide
  * Powershell Kansa

* Seen first time
  * File names
  * Processes
  * Processes had a file
  * Processes running from main memory
  * Most common and most rare
    * Files
    * Processes
    * Applications
    * registries
    * Ip's
    * Dns
    * Domain
    * Email sender
    * Wmi commands
    * Powershell
    * Users
    * Groups
    * Ports
    * Services
  * Signals
    * Account discorvery
    * Account creation
    * Account modification
    * Clearing logs
    * Process from ZIP file
    * Link file execution
    * Iso file execution
    * Modification of autorun key
    * Modification of registry key
    * Autoruns directory
      * Parent location of autoruns
      * Enabled autoruns
      * Disabled autoruns
      * Autoruns by catetory
      * Unknown signer autoruns
      * Autoruns from
        * Exe
        * Dll
        * Vbs
        * Ps1
        * Sys
        * Drv
        * Ax
        * cpl
    * Execution from temp directory
    * File name /process name with random letter
    * Webshells
      * W3wp.exe
      * Php-cgi.exe
      * China chopper
    * Shimcache hunting
    * Top executions by endpoint
    * Lowest execution by endpoint
    * Single character binaries
    * Execution form temp
    * Suspicious binaries
    * Total unique applications
    * Hunting with yara
      * Loki ioc  scanner
    * Threathunter playbook
      * Cyberdog
      * OTRF

* Honey tokens
  * Spn's
  * Credentials
  * Files
  * Folders
  * User-agents

Tools

C:\Windows\system32\cmd.exe /C whoami /groups\
C:\Windows\system32\cmd.exe /C tasklist /v\
C:\Windows\system32\cmd.exe /C netstat -na | findstr "EST"\
C:\Windows\system32\cmd.exe /C systeminfo\
C:\Windows\system32\cmd.exe /C ipconfig /displaydns\
C:\Windows\system32\cmd.exe /C wmic /Namespace:\\\root\SecurityCenter2 Path AntiVirusProduct Get displayName,pathtoSignedProductExe\
wmic /Namespace:\\\root\SecurityCenter2 Path AntiVirusProduct Get displayName,pathtoSignedProductExe\
netstat -an\
net user\
net use\
net view /all\
netstat -an\
net user\
net use\
net view /all\
net view /all /domain\
cmd.exe /c "reg.exe save hklm\security c:\windows\temp\xqjxxkmbrx"\
reg.exe save hklm\security c:\windows\temp\xqjxxkmbrx\
cmd.exe /c "reg.exe save hklm\system c:\windows\temp\kjmohmuk"\
reg.exe save hklm\system c:\windows\temp\kjmohmuk\
cmd.exe /c "reg.exe save hklm\sam c:\windows\temp\emmbnafzjtwq"\
reg.exe save hklm\sam c:\windows\temp\emmbnafzjtwq\
net share\
C:\Windows\system32\net1 share\
net config workstation\
C:\Windows\system32\net1 config workstation\
net group "Domain Admins"\
C:\Windows\system32\net1 group "Domain Admins"\
route print\
net localgroup\
C:\Windows\system32\net1 localgroup\
ipconfig /all\
tasklist /V\
net share\
C:\Windows\system32\net1 share\
net config workstation\
C:\Windows\system32\net1 config workstation\
net group "Domain Admins"\
C:\Windows\system32\net1 group "Domain Admins"\
route print\
net localgroup\
C:\Windows\system32\net1 localgroup\
ipconfig /all\
tasklist /V\
net config workstation\
C:\Windows\system32\net1 config workstation\
nslookup -type=any %%userdnsdomain%%\
net config workstation\
C:\Windows\system32\net1 config workstation\
nslookup -type=any %%userdnsdomain%%

C:\\\Windows\\\system32\\\whoami.exe"  /user

C:\\\Windows\\\system32\\\whoami.exe" /groups

"C:\\\Windows\\\system32\\\net.exe" group "domain admins" /domain

netstat • net view • net use • net session

nltest /domain\_trusts /all\_trusts

whoami /upn

Adfind <http://www.joeware.net/freetools/tools/adfind/>

netsh firewall set opmode disable\
net stop security center\
net stop WinDefend

\\"C:\\\Windows\\\System32\\\cmd.exe\\" /c vssadmin delete shadows /all /quiet \&amp; wmic shadowcopy delete &; bcdedit /set {default} bootstatuspolicy ignoreallfailures &; bcdedit /set {default} recoveryenabled no &; wbadmin delete catalog -quiet\
vssadmin delete shadows /all /quiet\
wmic shadowcopy delete\
bcdedit /set {default} bootstatuspolicy ignoreallfailures\
bcdedit /set {default} recoveryenabled no\
wbadmin delete catalog -quiet

adfind -f objectcategory=computer -csv name cn OperatingSystem dNSHostName > some.csv"

adfind -gcb -sc trustdmp >  trustdmp.txt

* Unauthorized RDP connections
* Failed RDP attempts
* Persistent connections
* Longest connections
* Beacon connections detection, may connection repeatatively
* What is the operational and business needs for the connections
* Protocol usage
* Abnormal protocol usage
* IP reputation check
* C2 beacon detection
* C2 long connections , 5 hours
* C2 behind the CDN
* Zeek+ja3
* Self signed cerificates
* Teamviewer connection
* Certificate analysis
* Detection of tunneling
* Rare useragents
* Destination IP lookup
  * IP reputation
  * ASN
  * Whois
  * Geo location
  * Ptr records
* Abuseipdb
* Alienvault
* Censys.io
* Dns.google/query?name
* Onyphe.io
* Security trails
* Shodan
* virustotal

* Executions of cobaltstrike payload
* Data exfiltration
  * 7zip
  * Mega
* Using PsExec

* Most common protocol usage
* suspicious IP/Domains lookup with Alexa/Cisco million domains list (need to use automation script)
* Investigate suspicious domain certificates to find similar malicious or impersonating domains
* Disabling the endpoint security events, script execution activity (ex: PS, JS, DLL followed by download activity)
* .rdp files in environment
* .hta files in environment
* .iso files in environment
* .ink files in environment
* Passwords.txt in environment
* Network Recon Activity
  * Using windows utilities
* Password Dumping activity tools
  * Mimikatz
  * Lass.exe dumping
* Additional tools
  * Lazangne
  * RDPV
  * NirSoft Tools
* Network port scan activity
* windows utilities such as WMI, wmic, taskkill, WEVTUTIL, sc, net.exe to kill processes and remove logs from the system
* Utilman.exe to manipulate/disable cmd.exe
* writing a rule to detect findstr.exe
* Hunting for password protected zip files ( need to check possibilities)
* WScript to  downloading files
* DLL dropping in %appdata% with different file format
* Regsrv32 loads DLL
* Ping beaconing/ICMP
* VNC protocol usage
* RDP protocol usage connections to and from public IP range
* FTP protocol usage
* Detecting Cobalt Strike activity
* Powershell download (invoke-webrequest)
* Persistence using schedule task
* wermgr.exe process injection
* Svchost.exe process injection
* ARP for enumeration
* Word document with macro

Kenny addition(Feel Free to Delete):

* Check LastPass Use
* Check robots.txt
* Check Cookies storage

VPN's

* Compromising VPN services
* Brute forcing VPN services
* User Sign In activity Bruteforce/impersonation attacks
* Zero-Day and vulnerability attacks on VPN services

Threat Hunting for Log4J exploitation:

* <https://www.microsoft.com/security/blog/2021/12/11/guidance-for-preventing-detecting-and-hunting-for-cve-2021-44228-log4j-2-exploitation/>
* <https://awakesecurity.com/blog/threat-hunting-for-log4j-exploits-on-the-network/>
* <https://unit42.paloaltonetworks.com/apache-log4j-vulnerability-cve-2021-44228/>
* <https://www.paloaltonetworks.com/blog/security-operations/hunting-for-log4j-cve-2021-44228-log4shell-exploit-activity/>
* <https://www.crowdstrike.com/blog/how-to-baseline-and-hunt-log4shell-with-the-crowdstrike-falcon-platform/>
* <https://blogs.opentext.com/log4j-vulnerability-explained-and-how-to-respond/>

Tools:

Arctic Wolf Tool

* <https://github.com/rtkwlf/wolf-tools/blob/main/log4shell/README.md>
* <https://www.msspalert.com/cybersecurity-news/log4j-vulnerability-scanners-and-detection-tools-list-for-mssps-and-threat-hunters/>

ToDo :

PaloAlto Useragent search

* <https://docs.paloaltonetworks.com/pan-os/8-1/pan-os-web-interface-help/objects/objects-security-profiles-url-filtering/url-filtering-settings.html>

Verify the attack simulation :

Packet capture capabilities from Paloalto firewall

* <https://knowledgebase.paloaltonetworks.com/KCSArticleDetail?id=kA10g000000ClTJCA0>

Initial Access :

* SocGholish (delivered via injected JavaScript on compromised websites.)

Execution :

* Upon downloading malicious windows executable file executed by following  -k and -pass
* Use of PsExec to push out ransomware
* Wipes the recycle bin folder of every drive
* Deleting shadow copies (local backups) by first listing them using WMI query SELECT \* FROM Win32\_ShadowCop
* Encrypts network shares and Exchange Mailbox if set in its configuration flag
* Uses pointed files when encrypting .lnk files

Persistence :

* LockBit 3.0 is capable of injecting a DLL into memory via reflective loading
* drops an .ico file in the %PROGRAMDATA% folder
* Disabling of Windows Defender and additional security controls  (third party antivirus/endpoint solutions)
* Establishing persistence to run Cobalt Strike beacon.

Information Gathering :

* specific PowerShell scripts containing two layers of obfuscated code
* Use of information gathering tools such as Bloodhound and Seatbelt.

Privilege escalation :

* UAC (user account control) bypass

Lateral Movement :

* Lateral movement leveraging RDP and Cobalt Strike.
* lateral movement through a group policy update, as long as there is a -gspd parameter provided

Exfiltration:

* Use of 7zip to collect data for exfiltration.
* Exfiltration of data to Mega\[.]nz

Clearing Tracks :

* drops and executes a .tmp file decrypted from the binary, instead of using cmd.exe

Remediation :

Best practices for mitigating the risk of a ransomware attack include\[1]:

* Following the 3-2-1 rule, which involves backing up files in three copies in two different formats, with one copy stored off-site. This is a precautionary measure to avoid data loss in case of a ransomware attack.
* Remaining vigilant against socially engineered emails to reduce the risk of a ransomware infection, as ransomware is commonly spread through malicious spam email attachments.
* Keeping applications and programs up to date. Regular patching ensures that software vulnerabilities that ransomware actors could exploit as entry points can be addressed in a timely fashion.
* Organizations can benefit from a multilayered approach that can help guard possible entry points into a system (endpoint, email, web, and network).

Comments :

1. There are similarities between black matter ransomware and lockbit3.0

References for TTP’s :

1. <https://www.virustotal.com/gui/file/c597c75c6b6b283e3b5c8caeee095d60902e7396536444b59513677a94667ff8/detection>
2. <https://app.any.run/tasks/837578ac-093b-4df2-85fc-aa08738d3dce/>

Security Vendors Analysis Report:

1. <https://www.trendmicro.com/en_us/research/22/g/lockbit-ransomware-group-augments-its-latest-variant--lockbit-3-.html>
2. <https://www.nozominetworks.com/blog/blackmatter-ransomware-technical-analysis-and-tools-from-nozomi-networks-labs/>
3. <https://research.nccgroup.com/2022/08/19/back-in-black-unlocking-a-lockbit-3-0-ransomware-attack/>
4. <https://blogs.vmware.com/security/2022/10/lockbit-3-0-also-known-as-lockbit-black.html>
5. <https://wazuh.com/blog/detecting-lockbit-3-0-ransomware-with-wazuh/>
6. <https://www.sentinelone.com/labs/lockbit-3-0-update-unpicking-the-ransomwares-latest-anti-analysis-and-evasion-techniques/>

References:

<https://alparslanakyildiz.medium.com/malicious-file-document-analysis-285654e5a59e>

<https://medium.com/walmartglobaltech/reverse-engineering-an-obfuscated-malicious-macro-3fd4d4f9c439>

<https://www.picussecurity.com/resource/blog/emotet-technical-analysis-part-1-reveal-the-evil-code>

<https://tech-zealots.com/threat-lab/deobfuscating-emotet-vba-macro-like-a-pro/>

Malware Families

* Beacon
* SystemBC
* Metasploit
* HiveLocker
* Qakbot
* ALPHV
* LOCKBIT
* BASTA

Phishing

* Qbot
* Emotet
* Iced ID
* Bumblebee
* Phosphorus
* ursnif

Drive by Download

* Gootloader
* Zloader

Other Attack Scenarios:

* SEO Poisoning

Bruteforce

* RDP
* SQL server

Ransomware :

* BlackByte ransomware
* Royal Road Weaponize
* LockBit 3.0 ransomware group
* BianLian ransomware
* Medusa
* Conti
* Sodinokibi

Recon Tool

* Dragon Juice
* TankTrap powershell utility

Info stealer:

* Form Book

Darkweb:

* Breach forums

Vulnerabilities

* Exchange : Proxy shell
* Manage engine support center plus
* CVE-2020-1472 (Zerologon) and CVE-2021-44077 (referring to ManageEngine SupportCenter Plus)

Suspicious execution:

* PowerShell execution
* WMI
* Windows commands
* Service execution
* Scheduled Task
* Malicious link from documents
* COM execution

Remote Access

* AnyDesk
* Tactical RMM
* Atera

Using run keys for persistence

App data folder with DLL files

Run Key to execute a PowerShell script via a LNK file

Scheduled Tasks to execute their payloads

IIS webshell

Process injection scenario

DLL Injection

Valid accounts misuse

IOC's

<https://otx.alienvault.com/>

<https://virustotal.com>

Abush.ch

IP assigned to ORG

<https://bgp.he.net/>

IP Lookup

<https://ipinfo.io/>

<https://whatismyipaddress.com/>

<https://www.showmyip.com/>

Publicly exposed assets

<https://dnsdumpster.com/>

<https://crt.sh>

<https://censys.io>

Url Scan

<https://Urlscan.io>

 <https://www.spamhaus.org/>

Sandbox

{% embed url="<https://browserling.com>" %}

Forensicdots.de/dotspotter

Malapi.io

Urlscan.io

Publicwww\.com

Osinttechniques.com

Malpedia

Objective-see.org

Hijacklibs.net

Lolbas-project.github.io

Gtfobins.github.io

Lots-project.com

Mxtoolbox super tool

Malshare.com

Abuse.ch

Virustotal.com

OSINTCurio.us

CCSS Forum (<https://www.ccssforum.org/>), and URLHaus (<https://urlhaus.abuse.ch/>)

<https://www.virusbulletin.com/>
