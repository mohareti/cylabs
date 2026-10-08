# XML External Entity (XXE)

**XXE (XML External Entity)** is a type of security vulnerability that occurs when an attacker can manipulate the processing of XML data in an application. XXE attacks exploit the inclusion of external entities within XML documents, leading to data disclosure, server-side request forgery (SSRF), denial of service (DoS), and other security risks.

There are several types of XXE attacks, and they can be categorized based on their impact and exploitation techniques:

1. **Entity Expansion Attack:**
   * In this type of XXE attack, the attacker injects malicious XML entities into an XML document to cause excessive entity expansion, leading to resource exhaustion or DoS.
   * **Example:** An attacker sends a crafted XML document containing a large number of nested entities, causing the server to run out of memory and crash.
2. **Parameter Entity Expansion Attack:**
   * Parameter entities in XML documents can be used to reference external entities, making them a target for exploitation. Attackers can use parameter entities to read sensitive files or execute SSRF attacks.
   * **Example:** An attacker injects a parameter entity in an XML document like `<!ENTITY % xxe SYSTEM "file:///etc/passwd">`. This entity can then be referenced to read the `/etc/passwd` file.
3. **Entity Expansion with External DTD:**
   * Attackers can reference external Document Type Definitions (DTDs) in their XML documents, which can lead to data disclosure or SSRF.
   * **Example:** An attacker submits an XML document that references an external DTD hosted on an attacker-controlled server. The DTD may include sensitive information or trigger an SSRF request.
4. **Blind XXE (Out-of-Band XXE):**
   * In this attack, the attacker exploits XXE without receiving direct responses. Instead, they send requests that trigger actions on the server or external systems whose interactions they can monitor out-of-band.
   * **Example:** An attacker submits a malicious XML document that triggers HTTP requests to an external server under their control. They monitor the external server's logs to gather information about the exploited system.
5. **Parameter Entity Expansion with Out-of-Band Data Exfiltration:**
   * Similar to Blind XXE, this attack involves parameter entities and external references, but it focuses on exfiltrating sensitive data out of the organization.
   * **Example:** An attacker injects a parameter entity that references an external DTD on their server. The DTD is designed to make DNS requests to send sensitive data to the attacker-controlled server.

To prevent XXE attacks, developers should follow these best practices:

* Disable external entity processing in XML parsers when not needed.
* Implement proper input validation and filtering to block malicious XML entities.
* Use XML libraries that support features like entity expansion disabling and DTD disallowance.
* Validate and sanitize user input before parsing XML data.
* Apply security headers, like Content Security Policy (CSP), to prevent external resource loading in XML documents.
* Regularly update and patch XML processing libraries to mitigate known XXE vulnerabilities.
