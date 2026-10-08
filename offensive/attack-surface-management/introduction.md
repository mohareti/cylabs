---
description: "Attack Surface Management (ASM) is a cybersecurity practice that involves identifying, assessing, and monitoring an organization's digital attack surface."
---

# Introduction

Attack Surface Management (ASM) is a cybersecurity practice that involves identifying, assessing, and monitoring an organization's digital attack surface. The attack surface comprises all the points of exposure where an attacker could potentially breach an organization's security. ASM helps organizations gain visibility into their attack surface, assess vulnerabilities, and implement mitigation strategies to reduce risks effectively. Below is a strategy for Attack Surface Management using various tools and techniques to understand and manage the attack surface comprehensively.

## 1. Domain Registration

* Use domain registrar tools and services to monitor domain registrations and ownership changes.
* Identify potentially malicious domains registered by unauthorized parties.

## 2. ASN (Autonomous System Number)

* Utilize ASN lookup tools to identify the autonomous systems associated with your organization.
* Monitor for unexpected or unauthorized ASNs that may indicate routing attacks.

## 3. IP Ranges

* Maintain an inventory of IP address ranges owned or used by your organization.
* Continuously monitor for unauthorized IP addresses or subnets.

## 4. Sub-Domains

* Use sub-domain enumeration tools to discover all sub-domains associated with your organization.
* Regularly scan and assess sub-domains for vulnerabilities.

## 5. Certificate Information

* Employ certificate transparency logs to track SSL/TLS certificate issuance for your domains.
* Monitor for unauthorized certificates or certificate expirations.

## 6. SAS Applications

* Implement application discovery tools to identify Software as a Service (SaaS) applications in use.
* Evaluate the security posture of each SAS application and assess access controls.

## 7. Storage Systems

* Maintain an inventory of storage systems, including cloud and on-premises solutions.
* Monitor access controls, encryption, and data exposure risks.

## 8. Public Cloud Infrastructure

* Utilize cloud security posture management (CSPM) tools to assess cloud configurations.
* Continuously monitor for misconfigurations, open ports, and unauthorized access.

## 9. Containers

* Employ container security tools to assess container images and runtime security.
* Monitor for vulnerable images and unauthorized deployments.

**10. Internet-Facing Applications/Servers:** - Conduct regular vulnerability assessments and penetration testing on internet-facing systems. - Implement Web Application Firewalls (WAFs) and intrusion detection systems (IDS) for real-time protection.

**11. Social Engineering/Phishing:** - Conduct employee training and awareness programs to mitigate social engineering risks. - Monitor for phishing campaigns targeting your organization.

**12. Compromised Email/User Accounts:** - Implement multi-factor authentication (MFA) to protect user accounts. - Monitor for suspicious account activity and compromised credentials.

**13. Third-Party and Nth Party Services:** - Assess the security posture of third-party vendors and services. - Monitor for changes in service providers and their security practices.

**14. Web Applications:** - Continuously scan web applications for vulnerabilities, including OWASP Top Ten risks. - Implement web application firewalls (WAFs) and secure coding practices.

**15. Hypervisor:** - Regularly update and patch hypervisor software. - Implement access controls and monitoring for virtualized environments.

**16. Email Gateway:** - Configure email gateways with SPF, DKIM, and DMARC records to prevent email spoofing. - Monitor email traffic for phishing attempts and malicious attachments.

**17. Security Controls (SPF, DKIM, DMARC Record):** - Implement SPF, DKIM, and DMARC records to enhance email security. - Continuously validate email authentication settings.

**18. Network Infrastructure:** - Conduct network vulnerability scans and penetration tests. - Monitor network traffic for anomalies and intrusion attempts.

**19. Routers, Firewalls, CDNs, VPNs, Load Balancers:** - Regularly update and patch network devices. - Implement access controls, encryption, and monitoring for network security.

**20. End User:** - Educate end users about security best practices and awareness. - Conduct security awareness training and simulated phishing exercises.

**21. Application Exploitation, Browser Exploitation, Drive-By Download:** - Continuously monitor for security vulnerabilities in applications and browsers. - Employ web security scanning tools and browser security settings.

**22. SEO Poisoning Attacks, Phishing, Session Hijacking:** - Implement security controls to detect and mitigate SEO poisoning, phishing, and session hijacking. - Monitor web traffic and user sessions for anomalies.

**23. Publicly Exposed API:** - Audit and secure APIs, including authentication and authorization mechanisms. - Monitor API traffic for suspicious activity and access.

**24. Source Code Repositories:** - Secure source code repositories and implement access controls. - Continuously scan code repositories for secrets and vulnerabilities.

**25. Google Hacking Database Search Queries, Shodan, Censys:** - Use search queries and specialized search engines (e.g., Shodan, Censys) to discover exposed assets and vulnerabilities.

Here is a list of both commercial and open-source tools for Attack Surface Management (ASM):

## Commercial ASM Tools

1. **Nessus:**
   * Description: Nessus is a comprehensive vulnerability assessment tool that can be used for ASM to discover and assess assets, vulnerabilities, and attack surface exposures.
   * Website: [Tenable Nessus](https://www.tenable.com/products/nessus)
2. **Qualys AssetView:**
   * Description: Qualys AssetView offers continuous asset discovery and monitoring, helping organizations understand and manage their attack surface.
   * Website: [Qualys AssetView](https://www.qualys.com/solutions/asset-inventory-management/)
3. **Rapid7 InsightVM:**
   * Description: InsightVM by Rapid7 provides vulnerability management and ASM capabilities to help organizations gain visibility into their attack surface and mitigate risks.
   * Website: [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)
4. **Tenable.io Lumin:**
   * Description: Tenable.io Lumin is a cloud-based solution that offers ASM features, including asset discovery and vulnerability management, with a focus on risk-based prioritization.
   * Website: [Tenable.io Lumin](https://www.tenable.com/products/tenable-io/lumin)
5. Expanse:
   * Description: Expanse provides a comprehensive attack surface management platform that helps organizations discover and manage their internet assets, including exposures and risks.
   * Website: [Expanse](https://www.expanse.com/)
6. RiskIQ:
   * Description: RiskIQ offers ASM solutions for discovering and managing internet-facing assets, monitoring digital threats, and identifying potential attack vectors.
   * Website: [RiskIQ](https://www.riskiq.com/)

## Open-Source ASM Tools

1. **Amass:**
   * Description: Amass is an open-source tool that helps security professionals perform network mapping and attack surface identification by enumerating subdomains and other assets.
   * GitHub: [Amass on GitHub](https://github.com/OWASP/Amass)
2. **Sublist3r:**
   * Description: Sublist3r is an open-source subdomain enumeration tool that can assist in ASM by finding subdomains associated with a target domain.
   * GitHub: [Sublist3r on GitHub](https://github.com/aboul3la/Sublist3r)
3. Shodan:
   * Description: Shodan is a search engine for discovering internet-connected devices and services. It can be used for ASM to identify exposed assets.
   * Website: [Shodan](https://www.shodan.io/)
4. Censys:
   * Description: Censys is another search engine for internet-connected devices and services, similar to Shodan, and can be used for ASM purposes.
   * Website: [Censys](https://censys.io/)
5. SpiderFoot:
   * Description: SpiderFoot is an open-source reconnaissance tool that automates footprinting and reconnaissance for ASM, helping to identify assets and vulnerabilities.
   * GitHub: [SpiderFoot on GitHub](https://github.com/smicallef/spiderfoot)
6. OWASP Amass:
   * Description: OWASP Amass is an open-source project focused on DNS and IP enumeration. It helps with ASM by discovering subdomains and other assets.
   * GitHub: [OWASP Amass on GitHub](https://github.com/OWASP/Amass)

These tools, both commercial and open-source, can be valuable assets in your Attack Surface Management efforts, helping you identify, assess, and manage your organization's digital attack surface effectively. The choice of tool may depend on your specific needs, budget, and the scale of your attack surface.
