# Bug Bounty & Web Recon

Web Application Security and OWASP Top 10: An In-Depth Guide

Web application security is a branch of information security that deals specifically with the security of websites, web applications, and web services. At a high level, it draws on principles of application security but applies them specifically to internet and web systems.

## Approach to Web Application Security

1. **Asset Discovery:**
   * Identifying all assets within the scope of the organization's digital infrastructure. This includes servers, applications, and APIs.
2. **Scope Definition:**
   * Clearly outlining what needs to be tested, including the range of IP addresses, domain names, and applications.
3. **Subdomain Enumeration:**
   * Horizontal enumeration involves discovering subdomains across a broad spectrum of the target domain.
   * Vertical enumeration focuses on a single subdomain to uncover deeper levels or additional services.
4. **Open Ports and Services:**
   * Identifying accessible ports and services is crucial as they can be entry points for attacks.
5. **Web Hosting Software, Misconfigurations, Exploits:**
   * Reviewing the software stack for known vulnerabilities and misconfigurations that could lead to exploits.
6. **Application Frameworks:**
   * Understanding the frameworks on which applications are built to identify specific security concerns.
7. **Custom Code or Commercial Off-The-Shelf (COTS) Software:**
   * Assessing the security posture of custom-developed applications as well as pre-packaged software.
8. **Application Libraries:**
   * Libraries can have vulnerabilities, and each should be assessed for potential risks.
9. **Integrations:**
   * External integrations can introduce security vulnerabilities and need thorough assessment.

## Browser Plugins and CLI Tools for Security

* **Wappalyzer:** Identifies technologies used on websites.
* **Whatruns:** Discovers technologies and tools running on any website.
* **Webanalyze:** Command-line tools for web analytics.

## Nuclei - Automated Web Vulnerability Scanner

* A command-line tool used for scanning web vulnerabilities. It takes inputs such as lists of URLs (`httprobe.txt`) and applies various templates (`-t`) to discover vulnerabilities including brute-force attacks, known CVEs, DNS issues, file-based vulnerabilities, and more.

**Jaeles Scanner, Retire.js, Vulners Burp Extension, Intrigue Core, Sn1per, and Gofingerprint:**

* These are various tools used to scan for vulnerabilities within web applications.

## Port Scanning with Naabu

* A fast port scanner designed to quickly scan thousands of ports and identify available services.

## Content Discovery Tools

* A set of tools such as Trubointruder, Gobuster, Ffuf, Dirsearch, Wfuzz, Feroxbuster, and Dirbuster, which are used to find existing and hidden content on web servers.

## Wordlist and Content Discovery

* Utilizing various wordlists and content discovery tools to find resources that are not readily visible, such as API endpoints, directories, files, etc.

## Application Testing

* **Data Storage and Transmission:**
  * Assessing how the application stores and sends data, including security measures for data at rest and in transit.
* **User Identification:**
  * Analyzing how the application identifies and authenticates users, ensuring proper access control mechanisms are in place.

## Spidering Tools

* **ZAP (Zed Attack Proxy):** A penetration testing tool for finding vulnerabilities in web

applications.

* **Burp Suite:** An integrated platform for performing security testing of web applications.
* **Gospider:** A tool that automates the process of finding URLs from web domains.
* **Hackrawler:** A tool for discovering endpoints and files.
* **Xlinkfinder:** Used for finding hidden links and endpoints in web applications.

## OWASP Top 10

The OWASP Top 10 is a standard awareness document for developers and web application security. It represents a broad consensus about the most critical security risks to web applications. As of the latest edition, the OWASP Top 10 includes:

1. **Injection Flaws:** Such as SQL, NoSQL, OS, and LDAP injection, where untrusted data is sent to an interpreter as part of a command or query.
2. **Broken Authentication:** Application functions related to authentication and session management are often implemented incorrectly, allowing attackers to compromise passwords, keys, or session tokens.
3. **Sensitive Data Exposure:** Many web applications do not properly protect sensitive data such as financial, healthcare, and PII.
4. **XML External Entities (XXE):** Poorly configured XML processors evaluate external entity references within XML documents.
5. **Broken Access Control:** Restrictions on what authenticated users are allowed to do are often not properly enforced.
6. **Security Misconfiguration:** This is the most common issue and happens due to insecure default configurations, incomplete or ad hoc configurations, open cloud storage, misconfigured HTTP headers, and verbose error messages containing sensitive information.
7. **Cross-Site Scripting (XSS):** XSS flaws occur whenever an application includes untrusted data in a new web page without proper validation or escaping.
8. **Insecure Deserialization:** This leads to remote code execution, replay attacks, injection attacks, and privilege escalation attacks.
9. **Using Components with Known Vulnerabilities:** Components, such as libraries, frameworks, and other software modules, run with the same privileges as the application.
10. **Insufficient Logging & Monitoring:** Insufficient logging and monitoring, coupled with missing or ineffective integration with incident response, allows attackers to further attack systems, maintain persistence, pivot to more systems, and tamper, extract, or destroy data.

## Techniques to Bypass Security Controls

Attackers are constantly developing new techniques to bypass security controls. These can include:

* Using obfuscation techniques to hide malicious payloads.
* Exploiting zero-day vulnerabilities, which are unknown to the software vendor.
* Phishing attacks to gain user credentials.
* Man-in-the-middle (MITM) attacks to intercept data.
* Using RATs (Remote Access Trojans) to gain unauthorized access to systems.

## Programming Languages Used in Ransomware Development

Ransomware can be developed using various programming languages, each with its own level of difficulty for reverse engineering. Some of the languages used include Go, Nim, Rust, C, C++, .NET, C#, Java, Python, Perl, JavaScript, PowerShell, WebAssembly, and Delphi.

Understanding the complexities of web application security is crucial for protecting against threats. Organizations must adopt a multi-layered approach, utilizing both automated tools and manual expertise to thoroughly assess and secure their web applications. This includes keeping up-to-date with the OWASP Top 10, regularly scanning for vulnerabilities, and educating developers and security teams about the latest threats and mitigation strategies.

## In this section

* ✅ [Getting Started in Bug Bounty Hunting](getting-started-in-bug-bounty-hunting.md)
* ✅ [Subdomain Enumeration](subdomain-enumeration.md)
* ✅ [Subdomain Takeover: Understanding the Risks and Prevention](subdomain-takeover-understanding-the-risks-and-prevention.md)
* ✅ [Tools and Technologies](tools-and-technologies.md)
