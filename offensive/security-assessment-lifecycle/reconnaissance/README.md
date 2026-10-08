---
description: "Information gathering is a critical phase in any cybersecurity assessment, vulnerability assessment, or penetration testing engagement."
---

# Reconnaissance

Information gathering is a critical phase in any cybersecurity assessment, vulnerability assessment, or penetration testing engagement. It involves collecting as much data as possible about a target system or organization to assess its security posture. In this blog post, we will explore various techniques and tools used for information gathering, covering both open-source and commercial options.

## Types of Information Gathering Techniques

Information gathering can be categorized into several techniques, each serving a specific purpose:

1. **Network Scanning:** Network scanning involves probing a target's network to discover open ports, services, and devices. It helps identify potential attack vectors.
   1. Protocol Scanning
   2. OS finger printing
   3. Protocol enumeration\
      • DNS enumeration

      • Directory enumeration\
      • Host discovery\
      • Share enumeration\
      • Local user enumeration\
      • Email account enumeration
   4. Wireless Enumeration
   5. Permission Enumeration
   6. Secrets Enumeration
2. **Host Discovery:** Host discovery focuses on locating active hosts within a network, including their IP addresses and MAC addresses.
3. **Service Enumeration:** Service enumeration aims to identify the services running on discovered hosts, along with version information, to assess their vulnerability.
4. **Web Enumeration:** This technique focuses on gathering information about web applications, such as identifying web servers, directories, and potential vulnerabilities.
   1. Banner Grabbing
   2. HTML Scraping
5. **Subdomain Enumeration:** Subdomain enumeration is the process of identifying subdomains associated with a target domain. Subdomains can reveal additional attack surfaces.
6. **Email Harvesting:** Email harvesting involves collecting email addresses associated with the target organization. These emails may be used for phishing or other social engineering attacks.
7. **Content Discovery:** Content discovery seeks to identify sensitive or hidden information on web servers, such as directories, files, and configuration files.
8. **Credential Harvesting:** This involves collecting usernames and passwords through various means, including phishing, credential stuffing, or publicly available leaked data.
9. **Threat Intelligence:** Gathering information about known threats and vulnerabilities related to the target organization can help assess the risk level.
10. Network Sniffing

## Tools for Information Gathering

Now, let's explore some popular tools used for information gathering, categorized by their specific purposes.

## Web Enumeration and Content Discovery

5. **HTTPScreenshot:**
   * HTTPScreenshot captures screenshots of web pages to visually inspect them. Usage example: `httpscreenshot -i targets.txt`.
6. **Recon-NG:**
   * Recon-NG is a powerful open-source framework for web reconnaissance and information gathering. It includes various modules for domain, subdomain, and email reconnaissance.
7. **theHarvester:**
   * TheHarvester is a tool for email, subdomain, and virtual host reconnaissance. Usage example: `theharvester -d target_domain -b google`.
8. **Discover:**
   * Discover is a tool for finding and extracting sensitive information from websites and files. Usage example: `discover -url http://example.com -o output_dir`.
9. **Have I Been Pwned:**
   * Have I Been Pwned is a website that allows you to check if your email address or password has been compromised in data breaches.

## Subdomain Enumeration

10. **Sublist3r:**
    * Sublist3r is a Python tool for enumerating subdomains of a target domain using search engines. Usage example: `python sublist3r.py -d target_domain`.
11. **Subbrute:**
    * Subbrute is a DNS subdomain enumeration tool that generates a list of potential subdomains for a target domain. Usage example: `subbrute.py target_domain`.
12. **Knock.py:**
    * Knock.py is a Python tool for performing subdomain enumeration using wordlists. Usage example: `knockpy.py -c target_domain`.

## GitHub Enumeration

13. **Gitrob:**
    * Gitrob is a tool for gathering sensitive information from GitHub repositories, including exposed credentials and other secrets. Usage example: `gitrob -save -access-token github_access_token -org target_organization`.
14. **GitAllSecrets:**
    * GitAllSecrets is another tool for scanning GitHub repositories for secrets, API keys, and other sensitive information. Usage example: `git-all-secrets -org target_organization`.

## Network and SSL Certificate Analysis

15. **Shodan:**
    * Shodan is a search engine for finding devices and services connected to the internet. It can be used to discover exposed services and vulnerabilities.
16. **Censys.io:**
    * Censys.io provides information about internet-connected devices, including SSL certificates, open ports, and banners.
17. **Dmitry:**
    * Dmitry is a command-line tool for gathering information about IP addresses, including DNS records, subdomains, and open ports. Usage example: `dmitry -winsefu target_domain`.
18. **Eyewitness:**
    * Eyewitness is a tool for taking screenshots of websites and services on a target domain. Usage example: `eyewitness -f targets.txt`.

Effective information gathering is a crucial step in assessing the security of a target system or organization. By using the right techniques and tools, security professionals can gather valuable data to identify vulnerabilities, potential attack vectors, and areas where improvements are needed. However, it's essential to use these tools responsibly and within legal and ethical boundaries, respecting the privacy and security of the target.

Scanning the internet for web applications and servers is a complex task that requires careful planning, ethical considerations, and the use of appropriate tools and techniques. In this blog post, we will explore the process of scanning the internet to discover various web applications and servers, including Redis databases, Jenkins servers, Apache Tomcat, Linux and Windows servers, Apache Airflow, WordPress, Joomla, and more. We will discuss the tools and techniques you can use for this purpose while emphasizing the importance of responsible and authorized scanning.

## Understanding the Scope

Before we dive into the tools and techniques, it's essential to understand the scope and purpose of your scanning efforts. Scanning the internet without proper authorization can have legal and ethical consequences. Always ensure you have permission or are performing scans for legitimate security research, vulnerability assessment, or penetration testing.

## Techniques and Tools

1. **Port Scanning with Nmap:**
   * Nmap (Network Mapper) is a versatile and widely-used tool for port scanning. It helps discover open ports and services on target hosts.
   * To scan for common web services like HTTP (port 80) and HTTPS (port 443), use the following command:

     ```bash
     nmap -p 80,443 target_ip_or_range
     ```
2. **Shodan:**
   * Shodan is a specialized search engine for discovering internet-connected devices and services. It allows you to search for specific services, software versions, and vulnerabilities.
   * For instance, to search for Redis databases, you can use the Shodan query `port:6379`.
3. **Censys.io:**
   * Censys.io is another search engine for internet-connected devices. It provides information about SSL certificates, open ports, and banners.
   * Use the web interface to apply filters based on service names to find specific services.
4. **Masscan:**
   * Masscan is a high-speed network scanner capable of scanning large IP ranges quickly.
   * To scan for Redis servers on port 6379, use the following command:

     ```text
     masscan -p6379 target_ip_range
     ```
5. **Python Scripts:**
   * Python scripts can be used to automate scanning processes. Libraries like `socket` can be helpful.
   * Here is a basic Python script to check if port 6379 (Redis) is open on a target IP:

     ```python
     import socket

     target_ip = "target_ip"
     port = 6379

     try:
         s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
         s.settimeout(2)
         s.connect((target_ip, port))
         print(f"Port {port} is open")
         s.close()
     except (socket.timeout, ConnectionRefusedError):
         print(f"Port {port} is closed")
     ```
6. **Web Application Scanners:**
   * Tools like Burp Suite, OWASP ZAP, and Nessus can identify web applications and vulnerabilities by analyzing HTTP requests and responses.

## Responsible Scanning

It cannot be stressed enough that responsible and authorized scanning is crucial. Always seek proper authorization, respect privacy and security, and adhere to ethical guidelines and responsible disclosure practices when conducting scans on the internet.

Scanning the internet for web applications and servers requires a combination of tools and techniques to identify potential targets and vulnerabilities. It is a task that should only be undertaken with the utmost care and respect for legal and ethical boundaries. When performed responsibly, internet scanning can contribute to improving cybersecurity and protecting against threats.

## Redis Databases

Redis databases are commonly used for caching and data storage. To discover Redis servers on the internet, you can use tools like Nmap or Masscan. For example, to scan for Redis servers on port 6379 with Nmap:

```bash
nmap -p 6379 target_ip_or_range
```

## Jenkins Servers

Jenkins is a popular automation server often used for continuous integration and continuous delivery (CI/CD). You can search for Jenkins servers using search engines like Shodan or Censys.io. For example, with Shodan:

```text
product:"Jenkins" port:8080
```

## Apache Tomcat

Apache Tomcat is a widely-used web application server for hosting Java-based web applications. To find Apache Tomcat servers on the internet, you can perform port scans with tools like Nmap or Masscan and look for port 8080 (default HTTP port for Tomcat) or other configured ports.

## Linux Servers

Scanning for Linux servers can be broad, as there are numerous services and configurations. To discover Linux servers, you can use Nmap, Shodan, or Censys.io. For specific services running on Linux, such as SSH (port 22) or FTP (port 21), use targeted scans with Nmap.

## Windows Servers

Similar to Linux servers, Windows servers can host various services. Port scanning with Nmap, Shodan, or Censys.io can help identify open ports and services on Windows servers. Common ports include 3389 for Remote Desktop Protocol (RDP) and 445 for SMB.

## Apache Airflow

Apache Airflow is an open-source platform for orchestrating complex data workflows. Scanning for Apache Airflow servers may require identifying the web interface, typically hosted on port 8080 or another configured port.

## WordPress

WordPress is a widely-used content management system (CMS). To find WordPress websites, you can use web crawling tools like Wappalyzer or specialized WordPress scanners like WPScan:

```bash
wpscan --url target_website
```

## Joomla

Joomla is another popular CMS. Similar to WordPress, you can search for Joomla websites using web crawling tools or specialized Joomla scanners like JoomScan:

```bash
joomscan -u target_website
```

## In this section

* ✅ [Active Recon](active-recon/README.md) · 4/17 pages written
* ✅ [Passive Reconnaissance](passive-reconnaissance/README.md) · 12/24 pages written
