# Server-Side Request Forgery (SSRF)

**SSRF (Server-Side Request Forgery)** is a security vulnerability that occurs when an attacker can manipulate a web application into making unauthorized requests to internal or external resources. SSRF allows the attacker to abuse the application's functionality to send requests to internal network services or external web services on behalf of the application, potentially leading to data exposure, unauthorized access, or attacks against other systems. Here's an explanation of SSRF with examples:

## Example 1 - Internal Service Access

Suppose you have a web application that allows users to input a URL and then fetches the content of that URL to display it on the user's dashboard. However, the application doesn't properly validate or sanitize the user-provided URL. An attacker can abuse this by providing an internal IP address or an internal service URL, like `http://192.168.0.10/admin`, as the input. The web application, when processing the request, may fetch the content from the internal service, potentially exposing sensitive information.

## Example 2 - Cloud Metadata Service Abuse

Many cloud environments provide metadata services accessible from within virtual machines. These metadata services contain information about the instance, such as its IP address, security groups, and IAM roles. An attacker can use SSRF to send requests to the metadata service from a compromised application to extract sensitive information. For instance, a malicious request might look like this:

```text
http://169.254.169.254/latest/meta-data/iam/security-credentials/role-name
```

This request could reveal AWS IAM credentials if the compromised application is running within an AWS EC2 instance.

## Example 3 - Remote Port Scanning

An attacker can leverage SSRF to scan ports on internal network devices by sending requests to different IP addresses and ports. If the application doesn't properly validate user input, the attacker can provide URLs like `http://internal-server:22` or `http://192.168.0.1:3306` to test for open ports on internal network devices.

To prevent SSRF vulnerabilities, developers should implement the following security measures:

1. **Input Validation:** Validate and sanitize all user-provided URLs and restrict them to allowed domains and protocols.
2. **Whitelisting:** Maintain a whitelist of allowed domains and only permit requests to those domains.
3. **Use of APIs:** If your application must make requests to external resources, consider using APIs instead of allowing arbitrary URL input.
4. **Network Segmentation:** Implement strict network segmentation to isolate internal services from the public internet.
5. **Security Updates:** Keep all software, libraries, and frameworks up to date to patch known SSRF vulnerabilities.
6. **Access Control:** Implement proper access controls and permissions to ensure that users can only access authorized resources.
7. **Content Inspection:** Perform content inspection of fetched data to ensure it doesn't contain malicious payloads.

By addressing these measures, developers can mitigate the risk of SSRF and protect their applications from this potentially dangerous vulnerability.
