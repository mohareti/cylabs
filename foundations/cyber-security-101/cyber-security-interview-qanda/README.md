# Cyber Security Interview Q&A

#### 1. What is the difference between Symmetric and Asymmetric encryption?

**Symmetric Encryption** uses the same key for encryption and decryption. It is faster and suitable for encrypting large volumes of data. For example, when you access a secure archive on your computer, the software encrypts the contents using a password you set. When you need to view the files, you use the same password to decrypt them.

**Asymmetric Encryption** involves a pair of keys, one for encryption (public key) and one for decryption (private key). It is commonly used for secure communications over the Internet. For instance, when you send an encrypted email using PGP, you encrypt the message with the recipient's public key. Only the recipient can decrypt it using their private key.

#### 2. What is a three-way handshake?

A three-way handshake is a method used in TCP/IP networks to establish a connection between a client and a server. It involves three steps:

* **SYN**: The client sends a SYN (synchronize) message to the server.
* **SYN-ACK**: The server responds with a SYN-ACK (synchronize-acknowledge) message.
* **ACK**: The client sends an ACK (acknowledge) message back to the server.

Example: When you open a website, your browser (client) and the website's server perform a three-way handshake to establish a TCP connection before any data is exchanged.

#### 3. What are the response codes that can be received from a Web Application?

Web application response codes are HTTP status codes that indicate whether a specific HTTP request has been successfully completed. Examples include:

* **200 OK**: Successful request.
* **301 Moved Permanently**: The resource has been moved to a new URL.
* **404 Not Found**: The requested resource could not be found.
* **500 Internal Server Error**: A generic error message when the server encounters an unexpected condition.

#### 4. What is the difference between HIDS and NIDS?

**HIDS (Host-based Intrusion Detection System)** monitors and analyzes the internals of a computing system as well as the network packets on its network interfaces. An example would be antivirus software on a PC that monitors the system's files and alerts users of any suspicious activity.

**NIDS (Network-based Intrusion Detection System)** monitors and analyzes network traffic for signs of intrusion across the network. For example, a NIDS could be placed on a subnet to monitor and analyze traffic going to and from devices on that subnet for unusual patterns.

#### 5. What are the steps to set up a firewall?

Setting up a firewall typically involves:

* **Defining Security Policies**: Determine which traffic is allowed or blocked.
* **Installing the Firewall**: Deploy the firewall device or software between your internal network and the gateway to the external network.
* **Configuring Rules**: Set up rules that match your security policies.
* **Testing**: Verify that the rules work as expected.
* **Maintenance**: Regularly update the firewall with new threats and security patches.

Example: A small business may set up a firewall to allow only web and email traffic into the network while blocking all other ports by default.

#### 6. Explain SSL Encryption

SSL (Secure Sockets Layer) encryption is a protocol for establishing a secure link between a web server and a browser, ensuring that all data passed between them remains private. It uses a combination of public-key and symmetric-key encryption to secure a connection.

**Example**: When you log in to your online banking website, SSL encrypts the communication, so your login credentials are secure. The browser verifies the server's SSL certificate to ensure the legitimacy of the website.

#### 7. What steps will you take to secure a server?

To secure a server, you would:

* **Install Updates**: Regularly update the server's operating system and software.
* **Configure Firewalls**: Set up and configure firewalls to control incoming and outgoing traffic.
* **Implement Intrusion Detection Systems**: Use HIDS or NIDS to monitor for suspicious activity.
* **Use Strong Authentication**: Implement multi-factor authentication and strong password policies.
* **Limit Access**: Give users the least privileges necessary, and use access control lists.

**Example**: A company secures its customer database server by implementing a firewall that restricts all traffic except for port 443 (HTTPS), setting up a HIDS to monitor system changes, and requiring two-factor authentication for all administrators.

#### 8. What are some of the common Cyberattacks?

Common cyberattacks include:

* **Phishing**: Deceptive emails that trick users into revealing sensitive information.
* **DDoS Attacks**: Overwhelming a service with traffic to make it unavailable.
* **Ransomware**: Malware that encrypts a user's data and demands payment for the decryption key.
* **SQL Injection**: Exploiting vulnerabilities in a database-driven website to execute malicious SQL statements.

#### 9. What is a Brute Force Attack? How can you prevent it?

A brute force attack involves trying many passwords or passphrases with the hope of eventually guessing correctly. To prevent it:

* **Implement Account Lockout Policies**: After a certain number of failed attempts, lock the account.
* **Use CAPTCHA**: Prevent automated systems from performing brute force attacks.
* **Employ Strong Password Policies**: Require complex passwords that are hard to guess.

**Example**: A web application could lock user accounts for 15 minutes after three incorrect password attempts to thwart brute force attacks.

#### 10. Brute Force is a way of finding out the right credentials by repetitively trying all the permutations and combinations possible.

An example of this could be a hacker using a program to enter all possible combinations of letters, numbers, and symbols to crack a password-protected system.

#### 11. What is Port Scanning?

Port scanning is the act of systematically scanning a computer's ports to find vulnerabilities. It's often used by attackers to find open ports that can be exploited to gain unauthorized access to a computer system.

**Example**: An IT administrator might use a port scanner to check for open ports on their network as part of a security audit to ensure that only necessary ports are open and all others are securely closed.

#### 12. What are the different layers of the OSI model?

The OSI model has seven layers, each with distinct functions:

1. **Physical Layer**: Manages the physical transmission of data over network devices.
2. **Data Link Layer**: Ensures reliable transmission of data across a physical network link.
3. **Network Layer**: Manages the delivery of packets from source to destination.
4. **Transport Layer**: Provides reliable data transfer services to the upper layers.
5. **Session Layer**: Manages sessions between applications.
6. **Presentation Layer**: Translates data between the application layer and the network.
7. **Application Layer**: Provides network services to the applications of the user.

**Example**: When you send an email, the Application layer interfaces with the email software, the Presentation layer encrypts the message, the Session layer establishes a connection, the Transport layer manages end-to-end communication, the Network layer directs the email to the server, the Data Link layer frames the email for transit, and the Physical layer transmits the data.

#### 13. Explain MITM (Man-In-The-Middle) attack and how to prevent it?

A MITM attack is when a hacker secretly intercepts and possibly alters the communication between two parties who believe they are directly communicating with each other.

## Prevention Methods

* **Encryption**: Using protocols like SSL/TLS ensures that data cannot be read if intercepted.
* **Authentication**: Ensuring the parties you're communicating with are who they say they are, using certificates.
* **Secure Networks**: Using VPNs to encrypt all traffic, even if intercepted, the data is unreadable.

**Example**: If an attacker places themselves between a user and a banking website, they could intercept the user's login credentials. The bank prevents this by using HTTPS, which encrypts the data in transit, making it unreadable to the attacker.

#### 14. Explain DDOS attack and how to prevent it?

A DDoS (Distributed Denial of Service) attack aims to make a machine or network resource unavailable to its intended users by overwhelming it with a flood of Internet traffic.

## Prevention Methods

* **Bandwidth Overprovisioning**: Having more bandwidth than you typically need can absorb the traffic surge.
* **Defensive Technologies**: Firewalls, anti-DDoS services, and intrusion prevention systems can detect and mitigate attacks.
* **Architecture**: Designing networks with resilience in mind can reduce the impact of attacks.

**Example**: A large e-commerce site might use a cloud-based DDoS protection service that can detect and reroute malicious traffic away from its network to prevent service disruption.

#### 15. Explain XSS attack and how to prevent it?

Cross-Site Scripting (XSS) attacks occur when an attacker injects malicious scripts into content from otherwise trusted websites.

## Prevention Methods

* **Input Sanitization**: Ensure all user input is sanitized, invalidating any scripts before they are processed.
* **Content Security Policy (CSP)**: Implement CSP headers to restrict where resources can be loaded from.
* **Encoding**: Encode data before it's used in HTML output to prevent the browser from executing it as code.

**Example**: A social media site might prevent XSS by automatically encoding any "<" or ">" characters into their HTML entity equivalents when users post content, so any attempted scripts are displayed as plain text rather than executed.

#### 16. What is an ARP and how does it work?

Address Resolution Protocol (ARP) is a protocol used to map an IP address to a physical machine address that is recognized in the local network.

**Example**: When your computer wants to send data to another device on the same local network, it uses ARP to translate the IP address into the MAC address, which is necessary for the data to be correctly routed to the destination machine on the LAN.

#### 17. Address Resolution Protocol (ARP)

ARP is used for mapping an Internet Protocol address (IP address) to a physical machine address that is recognized on the local network. When a device wants to communicate with another device on the same local network, it broadcasts an ARP request to find out the MAC address associated with the IP address.

**Example**: If your computer has an IP packet to send to another computer, it checks its ARP cache to see if there is a MAC address corresponding to the intended IP address. If not, it broadcasts an ARP request. The computer with the IP address responds with its MAC address, the communication can proceed, and the MAC address is cached for future reference.

#### 18. What are salted hashes?

Salted hashes are an enhancement to password hashing, a security measure that adds additional random data to a password before it's hashed. The salt ensures that the same password will have a different hash each time, making it much more difficult for attackers to use precomputed tables (like rainbow tables) to crack the password.

**Example**: Two users with the same password "password123" will have different hash values when salt is added. Thus, if one hash is cracked, it does not compromise the security of the other user's password.

#### 19. Explain SSL and TLS

SSL (Secure Sockets Layer) and TLS (Transport Layer Security) are cryptographic protocols designed to provide secure communication over a computer network. TLS is the successor to SSL and offers better security.

**Example**: When you visit a website with HTTPS in the URL, your browser is using TLS/SSL to create an encrypted channel with the server, ensuring that the data exchanged cannot be intercepted or tampered with by third parties.

#### 20. Explain SQL Injection and how to prevent it?

SQL Injection is a code injection technique that might destroy your database. It is one of the most common web hacking techniques. It can be prevented by using prepared statements with parameterized queries, not exposing database errors on the frontend, and performing regular security testing.

**Example**: A website with a search box that directly takes user input and passes it to a SQL query could be vulnerable to SQL Injection if someone types in a SQL command instead of a search term. The prevention method would be to treat user input as data, not as a part of the SQL command.

#### 21. Why is DNS monitoring important?

DNS monitoring is essential because it can help detect malicious activities, such as DNS hijacking or cache poisoning. Monitoring can also ensure that the DNS service remains available, performs well, and provides accurate responses to DNS queries.

**Example**: If your company's website suddenly redirects to a different site, DNS monitoring could alert you to possible DNS hijacking.

#### 22. What port does ping work over?

Ping operates by sending Internet Control Message Protocol (ICMP) Echo Request messages to the destination host and waiting for an Echo Reply. ICMP, used by the ping command, doesn't operate over a port but rather at the network layer.

**Example**: When you ping a computer, you don't use a port but rather send an ICMP request directly to the IP address.

#### 23. If you had to both compress and encrypt data during a transmission, which would you do first?

You should compress data before encrypting it. Compression reduces the size of the data, which can then be encrypted more efficiently. Also, encryption tends to make data appear random, which can negate the effects of compression if done afterwards.

**Example**: When sending a large file over a secure channel, you might zip the file first to reduce its size and then encrypt it before transmission.

#### 24. How would you defend against a cross-site scripting (XSS) attack?

To defend against XSS attacks, implement content security policies that restrict the sources of executable scripts, validate and sanitize all user inputs to ensure that they do not contain executable content, use anti-XSS libraries and frameworks that automatically escape user input, and employ secure coding practices.

**Example**: A web application uses input from a URL query string to display a greeting on a page without validation. An attacker could exploit this by sending a URL containing a script that executes on the page. To prevent this, the application should encode or strip out potentially dangerous characters from the input before rendering it on the page.

#### 25. What does RDP stand for and what is its assigned port?

RDP stands for Remote Desktop Protocol, which is used for remote connections to other computers. The default port for RDP is TCP 3389.

**Example**: An IT administrator needs to perform maintenance on a server located in a remote data center. They use an RDP client to remotely access the server's desktop environment via port 3389 to perform the necessary tasks.

#### 26. What is the difference between symmetric and asymmetric encryption?

Symmetric encryption uses the same key for both encryption and decryption, while asymmetric encryption uses a pair of keys, one for encryption (public key) and one for decryption (private key).

**Example**: In symmetric encryption, if Alice and Bob share a secret key, Alice can encrypt a message using this key, and Bob can decrypt it using the same key. In asymmetric encryption, Alice can encrypt a message using Bob's public key, and only Bob can decrypt it using his private key.

#### 27. What is the difference between UDP and TCP?

UDP (User Datagram Protocol) is a connectionless protocol that sends data without establishing a connection and doesn't guarantee delivery. TCP (Transmission Control Protocol) is a connection-oriented protocol that establishes a connection and ensures all data is transmitted reliably.

**Example**: Streaming a live video might use UDP for faster transmission with acceptable loss of some data packets, whereas sending an email would use TCP to ensure all data arrives in the correct order and without loss.

#### 28. What is Snort?

Snort is an open-source network intrusion detection system (NIDS) that can perform real-time traffic analysis and packet logging on IP networks.

**Example**: A network administrator uses Snort to monitor network traffic for signs of intrusion attempts or other suspicious activity, helping to detect and mitigate potential threats.

#### 29. What is the fastest way to crack a hashed password?

The fastest way to crack a hashed password is by using precomputed rainbow tables, which contain a list of hashes for a range of possible passwords, or by performing a brute-force attack using powerful hardware that can try many combinations quickly.

**Example**: An attacker who has gained access to a database of hashed passwords may use rainbow tables to quickly find matching plaintext passwords if the hashes are unsalted.

#### 30. What are the default ports for HTTP and for HTTPS?

The default port for HTTP (Hypertext Transfer Protocol) is 80, and for HTTPS (HTTP Secure) is 443.

**Example**: When you visit a website with HTTP, your web browser connects to the web server on port 80. If the website is secured with HTTPS, the browser connects on port 443, initiating a TLS handshake to secure the communication.

#### 31. What kind of cookie would a spyware attack typically use?

Spyware attacks might use tracking cookies, which are small data files used to collect information about a user's browsing habits without their knowledge or consent.

**Example**: A user visits a website that installs a tracking cookie on their computer. This cookie records the user's browsing activities and sends the information to a third party, which could use it for targeted advertising or more malicious purposes such as identity theft.

#### 32. Can you explain the SolarWinds attack?

The SolarWinds attack was a sophisticated supply chain attack where malicious code was inserted into the SolarWinds Orion software updates. This allowed attackers to compromise the systems of organizations that installed the compromised updates.

**Example**: A government agency using SolarWinds Orion unknowingly installed an update containing a backdoor. Attackers used this backdoor to gain access to the agency's network, allowing them to spy on sensitive communications and steal data over several months.

#### 33. What are some common ways that TLS is attacked, and/or what are some ways it’s been attacked in the past?

Common TLS attacks include man-in-the-middle (MITM) attacks, where an attacker intercepts and possibly alters communications between two parties. Other attacks exploit vulnerabilities in the implementation of the protocol, like the Heartbleed bug.

**Example**: An attacker might position themselves between a user and a website to intercept and decrypt TLS-secured traffic if they can exploit weaknesses in the TLS protocol or its implementation, such as using outdated encryption algorithms.

#### 34. What are some examples of symmetric encryption algorithms?

Some examples of symmetric encryption algorithms include AES (Advanced Encryption Standard), DES (Data Encryption Standard), and Blowfish.

**Example**: AES is commonly used for securing sensitive data. For instance, when you perform online banking, your transactions may be encrypted with AES to prevent unauthorized access to your financial data during transmission.

#### 35. What are some examples of asymmetric encryption algorithms?

Examples of asymmetric encryption algorithms are RSA (Rivest–Shamir–Adleman), ECC (Elliptic Curve Cryptography), and Diffie-Hellman key exchange.

**Example**: RSA is often used in digital certificates for HTTPS websites. When you connect to an HTTPS-secured website, your browser uses RSA to encrypt the initial communication and verify the server's identity.

#### 36. What’s more secure, SSL, TLS, or HTTPS?

TLS (Transport Layer Security) is the successor to SSL (Secure Sockets Layer) and is more secure due to improvements and the addressing of vulnerabilities found in earlier versions of SSL. HTTPS (Hypertext Transfer Protocol Secure) is an application protocol that uses either SSL or TLS to secure communications over a computer network.

**Example**: When accessing a bank website, your browser will establish a secure connection using TLS over HTTPS, ensuring that your financial data is transmitted securely.

#### 37. How exactly does traceroute/tracert work at the protocol level?

Traceroute/tracert works by sending a sequence of Internet Control Message Protocol (ICMP) echo requests or User Datagram Protocol (UDP) packets to a destination, with incrementally increasing Time-to-Live (TTL) values. Each router along the path is required to decrement the TTL value of a packet, and if the TTL value reaches zero, the packet is discarded and the router sends back an ICMP "Time Exceeded" message to the sender, revealing the router's IP address.

**Example**: To diagnose network issues, an IT specialist may use traceroute to map out the path packets take from their computer to the destination server. This helps identify where the packets are being delayed or lost.

#### 38. Can you describe rainbow tables?

Rainbow tables are precomputed tables used for reversing cryptographic hash functions, primarily for cracking password hashes. They are a time-memory trade-off technique where the time to crack a hash is reduced by using large precomputed tables containing the hash output for every possible input.

**Example**: An attacker could use rainbow tables to quickly find the password corresponding to a hashed password recovered from a database, assuming the hash was not salted.

#### 39. What is the ATT\&CK framework?

The MITRE ATT\&CK framework is a knowledge base of adversary tactics and techniques based on real-world observations. It is used as a foundation for the development of specific threat models and methodologies in the cybersecurity industry.

**Example**: A security team might use the ATT\&CK framework to understand an attacker's behavior, identify the techniques they might use, and develop defenses accordingly.

#### 40. Can you briefly describe the four most widely-used threat-hunting techniques?

The four widely-used threat-hunting techniques include:

1. **Baselining**: Establishing a norm for network behavior and searching for anomalies.
2. **Indicator of Compromise (IoC) Searching**: Looking for known signs of compromise.
3. **Indicators of Attack (IoA) Searching**: Identifying activities that could indicate an attack.
4. **Machine Learning and Advanced Analytics**: Using algorithms to detect unusual patterns that may indicate a threat.

**Example**: A threat hunter might establish a baseline of normal user login times and locations. If they detect a login at an unusual time or from a geographically distant location, it could trigger an investigation for potential unauthorized access.

#### 41. Apart from the ATT\&CK threat model, what are some other threat-hunting models that can be used?

Other threat-hunting models include the Cyber Kill Chain, the Diamond Model of Intrusion Analysis, and the Pyramid of Pain. Each of these models offers a different framework for understanding and responding to cyber threats.

**Example**: A security analyst might use the Cyber Kill Chain to identify and disrupt a cyber-attack at various stages, from reconnaissance to actions on objectives, thus preventing attackers from achieving their goals.

#### 42. Can you define Endpoint Detection and Response (EDR)?

Endpoint Detection and Response (EDR) is a cybersecurity solution that continuously monitors end-user devices to detect and respond to cyber threats. EDR platforms provide tools for threat detection, investigation, and response actions.

**Example**: If an employee's device starts communicating with a known malicious IP address, an EDR tool could alert the security team and automatically quarantine the device to prevent further compromise.

#### 43. What is a PCAP file?

A PCAP (Packet CAPture) file is a data file created by network sniffing tools that captures network packets that pass over a computer network. It serves as a record of network traffic and can be analyzed for troubleshooting and forensic purposes.

**Example**: After a suspected data breach, network analysts might review PCAP files to determine what data was transmitted out of the network and to where.

#### 44. Do you know what is a Cuckoo Sandbox?

Cuckoo Sandbox is an automated malware analysis system. It can run files in an isolated environment, or sandbox, to observe their behavior and report on any suspicious activities without risking the host system.

**Example**: An email attachment suspected to be malicious can be run through Cuckoo Sandbox to check if it attempts to make unauthorized network connections or modify system files.

#### 45. Can you explain SIEM?

Security Information and Event Management (SIEM) is a comprehensive solution that provides real-time analysis of security alerts generated by applications and network hardware. It aggregates and correlates data to identify anomalies and potential threats.

**Example**: A SIEM system could correlate an alert from a network intrusion detection system with an unusual login failure from a system log to detect a potential attack.

#### 46. Can you explain UEBA?

User and Entity Behavior Analytics (UEBA) uses machine learning to understand the normal behavior of users and entities within an IT environment and to detect deviations that could indicate a cyber threat.

**Example**: UEBA might detect that a user is downloading an unusually large amount of data, which could indicate a compromised account or an insider threat.

#### 47. Can you explain Honeynet?

A Honeynet is a network of virtual honeypots, which are decoy systems designed to be compromised by an attacker. Honeynets are used to study the attack strategies and gather threat intelligence.

**Example**: A company might set up a Honeynet to attract attackers, allowing them to monitor the attackers' behavior in a controlled environment and thereby improving their defensive strategies.

#### 48. What Threat Intel feeds are you familiar with?

Threat intelligence feeds are streams of data that provide up-to-date information on potential or current threats. Examples include feeds from commercial cybersecurity firms, industry groups, and open-source intelligence.

**Example**: A network administrator might subscribe to a feed that reports on new vulnerabilities discovered in commonly used software to ensure timely patching.

#### 49. What is your favorite EDR and why?

This is subjective and would depend on the analyst's experience with different EDR tools. They might prefer an EDR for its user interface, the comprehensiveness of its detection capabilities, or its integration with other security tools.

**Example**: An analyst might prefer an EDR like Crowdstrike Falcon for its cloud-based analytics and lightweight agent that doesn't impact end-user performance.

#### 50. What is your favorite SIEM and why?

Similar to EDR tools, preference for SIEM tools can be based on personal experience, the specific needs of the environment it's being used in, and the features it offers.

**Example**: An analyst may favor Splunk for its advanced data processing capabilities and extensive app ecosystem that allows for custom functionality tailored to their organization's needs.

51. What is Vulnerability
52. What is Risk
53. What is difference between vulnerability assessment vs Penetration Testing
54. what is difference between Penetration Testing vs Red Teaming

## In this section

* ✅ [Careers in Cybersecurity](careers-in-cybersecurity.md)
