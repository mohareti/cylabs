---
description: "The Domain Name System (DNS) acts as the internet's phonebook, translating human-readable domain names (like google.com) into machine-readable IP addresses (like 8.8.8.8) that computers use to communicate."
---

# DNS

The Domain Name System (DNS) acts as the internet's phonebook, translating human-readable domain names (like google.com) into machine-readable IP addresses (like 8.8.8.8) that computers use to communicate.

## 1. DNS Lookups

* When you enter a domain name in your web browser, your computer initiates a DNS lookup.
* The request goes to your local DNS resolver (often provided by your internet service provider).
* The resolver queries various DNS servers iteratively until it finds the authoritative name server for the specific domain.
* The authoritative name server responds with the corresponding IP address.
* Your browser receives the IP address and connects to the website's server.

## 2. Reverse DNS Lookups

* Translating an IP address back to a domain name
* Identifying the owner of a server associated with a suspicious IP address.
* Investigating potential phishing attempts where the sender's email address might be spoofed.

## 3. Conducting DNS Lookups

Several methods exist for conducting DNS lookups:

* **Using your computer's command prompt:**
  * **Windows:** Open Command Prompt and type `nslookup <domain_name>`.
  * **Mac/Linux:** Open Terminal and type `dig <domain_name>`.
* **Online DNS lookup tools:** Websites like MXToolbox or DNSLookup provide free tools to perform DNS lookups.
* DNS records are not always publicly available. Privacy-focused organizations might choose to hide certain information.
* Reverse DNS lookups might not always return a domain name, especially for dynamic IP addresses assigned by ISPs.
* Combining DNS lookups with other OSINT techniques can yield valuable insights for investigations.
