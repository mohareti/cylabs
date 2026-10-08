# Threat hunting scenarios

* Most common protocol usage
    * VNC protocol usage
    * RDP protocol usage connections to and from public IP range
    * FTP protocol usage
  * suspicious IP/Domains lookup with Alexa/Cisco million domains list
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
    * Mimikatz fetching domain admin kerberos
    * Lass.exe dumping
  * Additional tools
    * Lazangne
    * RDPV
    * NirSoft Tools
    * psexec
  * Network port scan activity
  * windows utilities such as WMI, wmic, task kill, WEVTUTIL, sc, net.exe to kill processes and remove logs from the system
  * Utilman.exe to manipulate/disable cmd.exe
  * rule to detect findstr.exe
  * WScript to  downloading files
  * DLL dropping in %appdata% with different file format
  * Regsrv32 loads DLL
  * Ping beaconing/ICMP
  * .js files downloading dll's
  * Detecting Cobalt Strike activity
  * PowerShell download (invoke-webrequest)
  * Persistence using schedule task
  * wermgr.exe process injection
  * Svchost.exe process injection
  * ARP for enumeration
  * Word document with macro
  * .onion traffic
  * TOR traffic
  * Chisel, a tunneling tool transported over HTTP and secured via SSH
  * AnyDesk, LogMeIn, and Atera
  * Group policy changes monitoring
  * Anti virus change policies
  * Windows Restart Manager to determine whether targeted files are currently in use or
  * blocked by other applications
  * AV tamper tool
  * Check LastPass Use
  * Check robots.txt
  * Check Cookies storage
  * Excel.exe -< regsvr32.exe -s : to download malicious files
  * Powershell activity with base64
  * DNS over HTTP
  * DNS over TLS
  * Outbound activity  to suspicious
  * Power shell to DNS request (potential download
  * Canary tokens
  * Cobalt Strike traffic
  * Visiting cloud hosting ( box)
  * Pasting sites
  * NMAP installed devices
  * Wireshark installed
  * System, Security and Application Windows event logs wiped
  * Microsoft Windows Defender AntiSpyware Protection disabled
  * Microsoft Windows Defender AntiVirus Protection disabled
  * Volume shadow copies deleted
  * Normal boot process prevented
  * Known IOCs – Logged Processes
  * wevtutil.exe cl system
  * wevtutil.exe cl security
  * wevtutil.exe cl application
  * vssadmin.exe delete shadows /all /quiet
  * wmic.exe SHADOWCOPY /nointeractive
  * wmic.exe shadowcopy delete
  *  Get-WMIObject  : wmi activity
  * bcdedit.exe /set {default} bootstatuspolicy ignoreallfailures
  * bcdedit.ex
  * Identify processes related to backups, antivirus/anti-spyware, and file copying and then terminating those processes to facilitate file encryption.
  * Stop the volume shadow copy services and remove all existing shadow copies via vssadmin on command line or via PowerShell.
  * Delete Windows event logs, specifically the System, Security and Application logs
  * removes virus definitions and disables all portions of Windows Defender and other common antivirus programs in the system registry
  * set {default} recoveryenabled no devices
  * Most, Least and outliner
  * Installed applications
  * Installed servers (Tomcat, HTTP servers)
  * Detecting different browsers in use
  * Detecting browser plugins
  * Cobalt strike Activity
  * PsExec
  * BITSadmin
  * Wmi
  * Pchunter
  * Programs which are not signed
  * Hunting torrents traffic
  * SSDP
  * Microsoft sharing the installation packages
  * Peer to Peer antivirus scans
  * Microsoft computer browser service annnouncements
  * ARP Traffic
  * Dropbox discovery broadcasts
  * kerborosting  detection
  * password spraying
  *  Transfer of Darkside malware over HTTP/S
  *  Email Darkside malware as a ZIP attachment
  *  Transfer of Darkside malware over HTTP/S
  *  Email Darkside malware as a ZIP attachment
  * Pre-execution phase of Darkside malware
  * Write Darkside malware to disk
  *  Create and Start a Service
  * Masquerading
  *  Discover Remote Systems using PowerShell
  * Collect Files using ZIP
  * \#6127 - Extract LSASS memory dump using PowerShell and Rundll32
  * \#5307 - Event Triggered Execution using PowerShell Profile
  * \#5107 - Stop a service using net stop command
  * \#3820 - Extract credentials stored in a browser using WebBrowserPassView
  * \#312 - Obfuscation of EXE inside Encrypted ZIP over HTTP protocol
  * \#2611 - Extract system date using PowerShell
  * \#214 - Scheduled task creation over SMB
  * \#1693 - Collect Windows system data using CMD
  * \#1269 - Creating Windows schedule task (schtasks)
  * \#110 - Covert data asset exfiltration using HTTP/s POST
  * \#109 - Covert data asset exfiltration using HTTP/s GET
  * \#106 - Covert data exfiltration using HTTP (GET)
  * \#105 - Covert data asset exfiltration using HTTP (URI)
  * \#2174 - Extract users and groups using net.exe (Windows)
  * \#2164 - Scheduled Task
  * \#6369 - Communication with Darkside using HTTP (Infiltration)
  * \#6370 - Communication with a real malicious Darkside server using HTTP/S (Infiltration)
  * rubess program to dump
  * Non signed applications
  * VPN's
    * Compromising VPN services
    * Brute forcing VPN services
    * User Sign In activity Bruteforce/impersonation attacks
    * Zero-Day and vulnerability attacks on VPN services
  * using single factor logins via Remote Desktop Protocol (RDP)
  * virtual private networks (VPNs)
  * Any DGA domains
    * What is the age
    * Who created it
    * Who is the registrant
  * Browser plugins
  * exfiltrate data likely using a combination of Clone
  * cloud storage service Mega.nz
  * Tools usage :
    * Windows native tools
    * Windows event viewer
    * WMI activity
    * DCOM\
      WinRM
    * Event Tracing for Windows (ETW)
  * Most common protocols
    * FTP services
    * IRC service
    * Unix RPC services
    * SMB services 135-139
    * RDP
    * Wmic
    * DNS
    * ICMP
    * DHCP
    * PXE
    * LLMNR 5355,  NBT\_NS, mDNS 5353
    * WPAD
    * OSPF
    * EIGRP
    * VRRP
    * HSRP
    * Network discovery protocols (IPV4 and IPV6)
    * Plaintext username and passwords
    * Weak Cipher
    * No SSL/TLS
    * Adminpages
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
  * Detection rules <https://www.elastic.co/guide/en/security/current/rules-ui-create.html>
  * Windows documentation
  * PyXie RAT and a Logmein signed binary used to load the RAT
  * Sharphound <https://bloodhound.readthedocs.io/en/latest/data-collection/sharphound.html>
  * activiyt arround ntds.dit
  * Psexec
  * Group policies
  * Word document with macro
  * Notepad file followed by xsl file
  * Wmic calling xsl file
  * Registry key for persistence
  * Auditing scheduled tasks
  * Powershell empire c2
  * <https://github.com/its-a-feature/Mythic>
  * .lnk files
* advanced port scanner
* advanced IP scanner
* powershell empire
* koadic
* psexec
* mimikatz
* disableing windows defender
* deleting system restore snapshots  and shodow copies
* winscp for data exfiltration
* cryptoPP C++ library for data encryption
* AES and RSA encryption
* file extension .pysa
* mutex object creation
* drive enumeration
* file enumeration
*  is file bigger than 1 kb
* is file whitelisted encryption
* is file blacklisted encryption
* event ID's
* 4624/4672 sucessful network logon as admin
* 5140 share mount
* 106/200/201/141 show sched tasks
* 4634 logoff

An unpacked PE file contains sections such as .text, .data, .idata, .rsrc, and .reloc

packed files contain specific section names, such as UPX0, .aspack, .stub, and so on

 CreateToolhelp32Snapshot Windows application programming interface (API) to iterate through running processes

Process Injection:\
spawning new processes in a suspended state,

allocating memory within them,

 writing malicious code into this created memory space (process hollowing)

injecting a thread into an existing process.

\
Following api calls used for process injection

\
CreateToolHelp32Snapshot

* VirtualAllocEx
* WriteProcessMemory
* CreateRemoteThread
* NtCreateThreadEx
* QueueThreadAPC

DLL injection

CreateToolHelp32Snapshot  : to iterate process

utilize VirtualAlloc and WriteProcessMemory to write the path for a malicious DLL\
the malicious process will utilize CreateRemoteThread in order to force the process to load the malicious library.

PE Injection:\
malware will create address space utilizing VirtualAlloc, then write a PE directly into the memory address space using WriteProcessMemory, and ensure code execution by utilizing CreateRemoteThread or similar undocumented APIs such as NTCreateThreadEx.

Thread execution hijacking\
suspend an existing thread of a process. First, the malware will suspend the thread, utilize VirtualAlloc to clear memory space for the path of the DLL, and inject the path to the DLL and a call to LoadLibrary in order to load the malicious DLL into the existing thread in the process. The malware will then instruct the thread to resume.

AppInit DLLs, AppCert DLLs, Image File Execution Options\

HKLM\Software\Microsoft\Windows NT\CurrentVersion\Windows\Appinit\_Dlls

HKLM\Software\Wow6432Node\Microsoft\Windows NT\CurrentVersion\Windows\Appinit\_Dlls

HKLM\System\CurrentControlSet\Control\Session Manager\AppCertDlls

HKLM\Software\Microsoft\Windows NT\CurrentVersion\image file execution options

Image File Execution Options

 Process hallowing

Virtual alloc

Writeprocess memory

Sysmon porcess ID's

calling mshta.exe to open malicious HTA files or calling binaries from SMB shares.\
 TCP on ports 139 and 445 inbound
