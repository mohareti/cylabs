# Risk Management

* Understanding current organization security environment and posture
  * Understanding critical information security issues faced/facing by organization
  * Initiating cyber security best practices
  * Developing modern Cyber Security program with Defense in Depth and Zero Trust
  * Developing Cyber Security Strategies to mitigate threats
* Directing/Managing
  * Asset Management
    * High valued assets
    * Critical assets for operations
  * Cyber Physical Security Management
  * Hardware Security Management
  * IOT/OT/SCADA Security Management
  * Cyber Security Operations
    * SIEM
      * Audit log management
    * SOC
      * SOC Playbooks
    * SOAR
    * Incident Response
      * Identifying
      * Containing
      * Eradicating
      * recovering
    * Security breach management
      * Ransomware
      * Data loss
    * Shadow IT
  * Cloud Security Management
    * Cloud Security Architecture
    * Cloud Security tools
      * CASB, CWPP, CSPM
    * Security attacks
    * Cloud security frameworks
      * CSA, cloud adoption frameworks
      * Cloud computing policy
      * Cloud storage policy
    * Zero trust on cloud
  * SecDevOps/DevSecOps/Security Engineering
    * Shift left with security in DevOps Pipeline
    * Security Misconfigurations
    * Security automation
      * Infrastructure as code
    * Data Encryption
      * Symmetric
      * Asymmetric
      * Hashing
      * Encoding
      * Key exchange
      * Certificates
      * Digital signature
    * Data Privacy
  * Application Security
  * Secure Coding and software development
  * Security Awareness
    * Security First
    * Security Situational Awareness
  * Cryptography, Data Security and Protection
  * Vulnerability and Patch Management
    * Build
    * Audit
    * Review
  * Network Security/Perimeter security
    * Layered security controls
    * NGFW, NSM, IDS/IPS, Load Balancers, Proxies,
    * VPN, IPsec
  * Endpoint Security
    * End-user Security
    * EDR, XDR, HIDS,HIPS, EPP, FIM, Sandboxing, whitelist/blocklist
    * Malware defense
  * Cyber Security Governance, Risk,  Compliance Management
    * Risk Assessment and Management
    * Information security Management
    * Security policies
      * Business continuity
      * Disaster Recovery
    * Cyber Security Maturity Models
  * Cyber Security Architecture
    * Zero Trust Model
      * Zero trust network access
  * Cyber Security Frameworks and controls
    * NIST cyber security framework
    * CIS critical controls
    * CMMC
    * NIST SP 800-171
    * NIST SP 800-53
  * Cyber Defense architecture and frameworks
    * MITRE ATT\&CK
  * Cyber Security Standards
  * Cyber Security Reporting
  * Cyber Gap Analysis
  * Cyber Security Strategic Plan
  * Security workflow and relationships among multiple teams
  * Cyber Security Budget Management
  * Cyber Security Team performance, growth, learning
  * Penetration Testing/Red Team
  * Bring your own device policies
  * Remote work policies
  * Cyber Security product and services SLA's
  * Developing Non-Disclosure Agreements
  * Cyber Threat Landscape
    * Threat actors
    * Nation state attacks
    * TTP's
    * Critical business operations
    * Stakeholders
  * Organization business goals and vision
  * Security metrics
    * Weekly
    * Monthly
    * Quarterly

Architecture

* Defense in Depth
* Zero Trust
* NIST

What you need to understand:

* TCP/IP
* OSI Model
  * Layered protocols
  * Layer 2: ARP, VLAN
* IPv4 Protocol suite
* IPV6
* Network protocols and services
* Nonroutable protocols

News to Follow

Companies to Follow:

Knowledge Base:

* IETF RFC
* MITRE Attack framework
* CVE
* Exploit DB
* <http://bit.ly/2bfCqgR>
* <https://nvd.nist.gov/vuln/search>
* <https://csrc.nist.gov/publications/detail/sp/800-115/final>
* <https://www.ncsc.gov.uk/collection/cloud-security?curPage=/collection/cloud-security/implementing-the-cloud-security-principles>

Security Assessment Standards:

* PCI DSS
* NIST SP 500-83
* CJIS

Worms and Cyber Attacks for further study

* Stuxnet
* Petya
* Non petya
* Saudi Aramco cyber attack
* Sony pictures hack
* Target Hack

Vulnerabilities further study

* Heartbleed
* Shellshock

Assessment logics

Static analysis

Static code analysis

Configuration analysis

Dynamic testing

Network pentesting

Web application testing

Api testing

Cofiguration testing

Social enginering

Recon

Scan

Identify

Investigate

Exploit

Kali linux assuring security by pentesting by tedi heriyanto, lee allen and shakeel ali

Mastering kali linux for advanced penetration testing by rober w\.beggs

Nmap

\--script dns-srv-enum --script-args dns-srv-enum.domain=ebay.com

Fierce -dns

Threat modeling

Heap management algorithms

Books To Read

1. Mastering Kali Linux for Advanced Penetration Testing by Robert W Beggs
2. Kali Linux: Assuring Security by Penetration Testing by Tedi Heriyanto, Lee Allen and Shakeel Ali

Application Security/DevSecOps

Saturday, May 14, 2022

9:43 AM

Vulnerability Scanning

Friday, July 26, 2019

10:23 PM

Nmap

Nessus

Rapid 7 Nexpose

Fingerprinting

Network probing

Nvd.nist.gov

Exploit-db.com

Seclists.org

Hacker one

Securityfocus

Packet strom

Cert vulnerability notes

Scadavulns.com

Immunitysec.com

Coresecurity.com

Metasploit

NIST SP 800-115

Showmount

Dig

Snmpwallk

Define the Security Assessment objective

* Testing enforced policies
* Testing coverage of Audit requirements
*  what is the ultimate goal and objective

Build Scope:

* Design the boundaries which need to be covered
* Networks, Vlan's, IP Ranges, Applications, assets, People
* Scan scope
* How many firewall palced, acl's
* How DNS resolution works
* Id DNS data accurate

* Stages
  * Reconnaissance
    * Identify everything and map the network
    * Which services and ports opened
  * Vulnerability Scan
  * Reviewing the vulnerabilities
  * Possibility of exploitation

Publicly Available Data:

* Websearch engines
* Whois
* Dns servers
* Email addresses
* Telephone numbers
* Usernames
* Bruteforce grinding
* Social engineering
* Publicly exposed databaases
* Historical usuage of same username and password
* Subdomains
* Search engines
  * Google, Bing
* Netcraft
* Shodan
* Censys
* Domain tools
* Linked in
* Whois
* Bgp.he.net hurricane
* Ip who is
* DNS enumeration
* DNS zone Trasfer

Network Scanning

* Detecting IP ranges, Vlans, Hostnames, Network devices, Mac Addresses
* Is ping scan works ?

ICMP type 8 and 13

Nmap -PEPM -sP -vvv -n Iprange

Ping -b broadcast address

Vulnerability Assessment

Saturday, May 14, 2022

10:39 AM

Is any of identified services does have vulenrabilites ?

What is the criticality

Is it impact the business

Is it impact CIA triad

Detecting and Assessing Attack Surface \[useful for threat hunting too}

* Users
  * Social engineering attacks
  * Clickjacking
  * Publicly exposed user creds and databases
* Client assets
  * Vulnerable applications, browsers
  * Credential dumping

* Client network
  * HTTPs session hijacking
  * SSH bruteforcing
* Communication network
* Communication infrastructure
* Application Servers
  * Command injection
  * Session management
* Database Servers

Threat Modeling

 need further reading

Vulnerability Exploitation

Saturday, May 14, 2022

10:42 AM

Is there rate limit for sign in acitivity

Running bruteforce

Threat Modeling and  Hunting

Saturday, May 14, 2022

11:26 AM

Threat Modeling

Threat Hunting

Def:

proactive and iterative search

validation of all assets connected in organizations network

Hwo to start ?

* Hypothesis
  * Phishing emails
  * Anomalies behaviors
  * Drive on download
  * Credential hijack
  * Unusual external connections
* detect anomalies
* Data collection
  * Endpoint
  * Firewall
  * Application
  * Network
* Analysis
  * What connections received at time of incident
  * Remote TeamViewer logins
  * SMB 1
* Hypothesis Validation
  * Conclusion
* Reporting

Reference :

Pyramid of pain

Detecting and Assessing Attack Surface

* Users
  * Social engineering attacks
  * Clickjacking
  * Publicly exposed user creds and databases
* Client assets
  * Vulnerable applications, browsers
  * Credential dumping

* Client network
  * HTTPs session hijacking
  * SSH bruteforcing
* Communication network
* Communication infrastructure
* Application Servers
  * Command injection
  * Session management
* Database Servers

Know you network diagram ?

Know your assets ?

How many departments ?

How many servers in DMZ ?

Which firewall we have ? How many ?

Which router we have ?

Which switch we have ?

Which WAF we using ?

Desktops

Windows

Linux

Test network

Servers

Windows

Linux

Vm environment

Printers

IOT/SCADA

(get IP ranges all we have)

Which security controls we have

Which preventive controls we have

Which detective controls we have

What do we need?  Centralized log collection

What is logging?

Syslog port numbers

* Regex for threat hunting on raw logs

Log sources

* Firewall logs
* IDS/IPS
* VPN
* Proxies
* Endpoint/edr
* MFA failure attempts/2Factor
* Authentication logs
* Autherizaiton logs

What do we do? Understand known good patterns, detect the signatures to identify indicators of compromise

What is IOC’s and IOA’s

* Indicator of compromise
* Indicator of Attack

What is a threat Intelligence?

We can’t completely relies on threat intelligence

Because IP’s, DNS, File signatures changes

Focus on behavioural threat intelligence

* Github used as c2c, how to detect that
* Cloud servuces and CDN’s are often abused

What are host intrusion detection system?

What are network intrusion detection systems?

suricata

Oranization to maintain security posture

* Run periodic audit and internal pentest

Vulnerability Management

What is the scope ?

Which audit cortrols we need to follow ?

Who is doing the patches ?

Who responsible for patching ?

Research:

1. Is logging disabled on any device or asset
2. Is antivirus disabled on any device
3. Malware persistence mechanisms
4. Tools
5. * Empire
   * Dnscat2

What we are doing reactive, we need proactive

* Managing SOC alerts
* Check logs for suspect activity
* Check dashboards for unusual activity
* Monitor and respond to EDR alerts
* These are all reactive activities
* Threat hunting is a proactive process

How to perform asset integrity

Network threat hunting

* C2 communication/threat hunting
  * Outbound connections
  * Dns over http
    * TXT records
  * Using zeek
  * Connection persistence, happening more often
  * Longest  network connections
  * Total time the pair has in contact
  * Data exfiltration data size
  * Expected dns traffic
  * Dns traffic and certificate match
  * Moving data to random ip
  * Unique client signature
  * Self signed cerificates
  * Abnormal protocol usauage
  * External IP reputation check
  * Failed sign in, connectins, protocol  communications
* Beacons activity with respect to time
  * Repetitive connections ip’s and FQDN
  * Connections to cdn
    * Which threat actors use which cdn
    * Beacon detection using kmeans clustering

Types of threat hunting

* Active
  * Asset isolation
  * Memory forensics
* Passive
  * Review packets
  * Review siem logs

Threat Hunting using Firewall

What is network jitter

Detection of cobaltstirke c2 communication

Detect heartbeat

Session size

Connection to TeamViewer

To avoid false positives

* Check connection persistence
* What is valid use case
* Legit need
  * NTP
  * Windows notification services
  * Checking for patches
* Outbound protocols
  * 5222 chrome remote desktop
  * 5800 and 590x vnc
  * 502 modbus
* C2 tunnelling
* Standard ports for unexpected apps
* Applications using not standard ports

Counter cyber terroirism

Check for common web vulnerability strings and useragents

* /etc/passwd

Review LolBins

* Windows
* Linux
* MacOS

Further research Questions

Saturday, May 14, 2022

12:53 PM

Ransomware groups which generate both keys on victim machine

Which programs/processes doesn't follow DEP and ASLR

How threat actors bypass ASLR or memory restrictions

Code ideas and questions

Saturday, May 14, 2022

1:18 PM

Information gathering scripts

Subdomain enumeration methodologies

ASN Lookup

Search engine search for sensitive files download

File header sensitive data

Pdf/doc/text/ sensitive keywords search

Comments grabber

Github/gitlabsearch

Network Security Assessment

Friday, February 18, 2022

11:32 AM

Google Project Zero

Exploitation software defect

Defense and depth

MITRE Framework

CVE database

NIST Framework

NIST Vulnerability Database

NIST 800-115

NIST 53

NIST vulnerability database

Exploit database

CERT security notes

NSA DevSecOps

NSA IAM

DISA

CSEG CHECK

 \- CHECK Fundamental Principles

PCI DSS

HITRUST

HIPPA

ISO 27001

PTES

* PreEngagement
* Intelligence Gathering
  * Reconnaissance
    * DNS
    * Subdomains
    * ASN
    * Webservers
    * Mail servers
    * VPN
    * User names/emails
  * Port scans
    * TCP, UDP, 65536
  * Identifying networks and hosts
* Threat Modeling
* Vulnerability Analysis
  * Nmap, Tenable
  * Service fingerprinting
  * Network probing

* Exploitation
* Post-Exploitation
* Reporting

System administration

* Windows
  * Netbios
  * SMB
  * RPC Services
  * Users
  * Groups
  * Shares
  * Domains
  * Password Policies
* Linux
  * RPC services
  * NFS services
  * R services (rsh, rexec, rlogin)
* Best practices
* OS internals

Computer networking

* OSI layers
* TCP/IP
* Network protocols
  * FTP, SMTP, HTTP
* X86 processor registers
* Fundamentals of Cryptographic
* OWASP Top 10

Network Security Assessment

* Cyber Risk Management
* Information Assurance process
* Security assessment workflows and tactics
* DDOS attacks
* Man-in-the-middle Attacks

What is client business ?

What is the criticality in business?

Critical Assets ?

Cyber Gap Analysis

Asset classification

Who are our adversaries

* State sponsored
* Criminals

What is our attack surface ?

Which are exposed

* External network and infrastructure
* Users
* Web application

Network Exploitation strategies

Network defense strategies

* Network segmentation
* Zerotrust policies
* Defendable networks

Vulnerability Assessment

* Vulnerability Classes
* Adversary types

Network Discovery

* External Network Mapping
  * Ports and Services
* Local Network Discovery
  * Asset Discovery
  * Network Sniffing
* IP Network Scanning
  * Scan Types
  * IDS evasion
  * Low-level packet analysis
* Common Network protocols and services analysis
  * SSH
  * FTP
  * Kerberos
  * SNMP
  * VNC
  * Common ports
* Microsoft Services
  * Netbios
  * SMB version
  * RPC
  * RDP
* Mail Services
  * O365
  * SSO
  * MFA
  * SMTP
  * POP3
  * IMAP
  * Transport Rules
  * Information Leak
  * BruteForce attacks
* VPN Services
  * Ipsec
* TLS/SSL services
  * Data security on transit
* Web Application Architecture
  * OWASP Top 10
    * XXE
    * API abuse
    * Privilege escalation
  * Vulnerable frameworks
  * Serialization Bugs
    * Python pickel
    * Yaml
    * Java
  * Business Logic
    * Compression techniques
    * Encoding techniques
    * Parsing mechanism
    * Rendering
    * Shell shock
  * Security Assessment
    * Source code
    * Configurations
      * Server
      * Infrastructure
      * Architecture
  * Dynamic Testing
    * Network infrastructure
    * Web services (API mobile applications)
      * REST API
        * Fuzzing
      * SOAP API

* Data Storage
  * Storage protocols
* Assessment Process
  * DNS Information retrieval
  * Network mapping
  * Network Probing
    * ICMP, TCP,UDP
  * TCP Service banner grabbing
  * SNMP enumeration
    * MIB
  * Router and Switches enumeration
    * Telnet, TFTP
  * User enumeration
    * Compromised user accounts

* OT
  * SCADA
  * IOT
