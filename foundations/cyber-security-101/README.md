# Cyber Security 101

### The CIA Triad: Cornerstone of Information Security

The CIA Triad is a foundational model in information security that represents the three core objectives for protecting information assets: Confidentiality, Integrity, and Availability.

* **Confidentiality:** Ensuring only authorized users can access and view sensitive information.
* **Integrity:** Maintaining the accuracy and completeness of data, preventing unauthorized modification.
* **Availability:** Guaranteeing authorized users have timely and reliable access to information when needed.

## How Security Controls Uphold Confidentiality

* **Access Control:** Restricting access to information systems and data based on user roles and permissions. This ensures only authorized users can view sensitive information. (e.g., requiring login credentials, user groups)
* **Multi-Factor Authentication (MFA):** Adding an extra layer of security beyond passwords. MFA requires users to provide additional verification factors, like a code from their phone, to access sensitive data.
* **Role-Based Access Control (RBAC):** Assigning permissions based on a user's role within the organization. This limits access to data that's not relevant to their job function.
* **Encryption:** Transforming data into an unreadable format using encryption algorithms. Even if intercepted, attackers cannot access the information without the decryption key.

## How Security Measures Ensure Integrity

* **Logging:** Recording all activities and changes made to data. Logs provide an audit trail that helps identify unauthorized modifications and maintain data integrity.
* **Blockchain:** A distributed ledger technology that creates an immutable record of transactions. Any changes to the data are recorded and verifiable, ensuring data integrity.
* **Cryptographic Hashes:** Generating a unique fingerprint (hash) of a data file. Any modification to the data will change the hash, allowing detection of tampering.
* **Digital Signatures:** Electronically signing data to verify its origin and prevent unauthorized modifications.

## How Attacks Impact Availability

* **Denial-of-Service (DoS) attacks:** Overwhelming a system with traffic, making it unavailable to legitimate users. This disrupts availability by preventing authorized access to information.
* **Ransomware attacks:** Encrypting data and demanding a ransom for decryption. This attack directly impacts availability by making data inaccessible to authorized users.
* **Malware:** Malicious software that can disrupt system functions or corrupt data. Malware can render systems unusable and impact data availability.

**Remember, security is an ongoing process.** Continuously evaluate and update your security controls to address evolving threats and maintain a strong security posture based on the CIA Triad principles.

Cybersecurity principles are the foundational guidelines that help organizations and individuals protect their information systems, data, and devices from cyber threats. These principles act as a roadmap for building a robust security posture and mitigating cyber risks. Here are the core principles commonly used in the field:

## 1. Governance

* **Leadership and Commitment:** Senior management plays a crucial role in establishing a culture of cybersecurity awareness and prioritizing security initiatives. This includes allocating resources, defining security policies, and ensuring compliance.
* **Risk Management:** Organizations need to identify, assess, and prioritize cybersecurity risks. This involves understanding potential vulnerabilities in systems and data, the threats that could exploit them, and the impact of a successful attack.
* **Compliance:** Following relevant security regulations and industry standards helps ensure a baseline level of security controls are in place.

## 2. Protect

* **Defense in Depth:** Implement multiple layers of security controls to create a layered defense against cyberattacks. This could include firewalls, intrusion detection/prevention systems, data encryption, and secure coding practices.
* **Least Privilege:** Grant users and systems the minimum level of access permissions necessary to perform their tasks. This principle minimizes the potential damage if a system or account is compromised.
* **Patch Management:** Regularly patching operating systems, software applications, and firmware with the latest security updates is essential to address known vulnerabilities and prevent attackers from exploiting them.
* **Data Security:** Sensitive data should be protected at rest (stored data), in transit (being transferred), and in use (accessed by authorized users). This involves encryption, access controls, and data loss prevention techniques.

## 3. Detect

* **Security Monitoring:** Continuously monitor network activity, system logs, and user behavior for suspicious activity that might indicate a potential attack.
* **Vulnerability Scanning:** Regularly scan systems and networks for known vulnerabilities to identify and address weaknesses before attackers exploit them.
* **Incident Response:** Have a plan in place to respond to security incidents effectively. This includes procedures for identifying, containing, eradicating, and recovering from a cyberattack.

## 4. Respond and Recover

* **Incident Response Plan:** As mentioned under "Detect," a well-defined incident response plan outlines the steps to take when a security breach occurs. This plan should include roles and responsibilities, communication protocols, and recovery procedures.
* **Business Continuity and Disaster Recovery:** Organizations need a plan to restore critical business operations and data in case of a cyberattack, natural disaster, or other disruptions. Regular backups and redundancy measures are crucial for achieving fast recovery.
* **Lessons Learned:** After a security incident, it's vital to analyze what happened and learn from the experience. This helps improve future security posture and prevent similar incidents from happening again.

By adhering to these core cybersecurity principles, organizations and individuals can significantly reduce their risk of cyberattacks and protect their valuable information assets. Remember, cybersecurity is an ongoing process, and these principles should be continuously reviewed and adapted as technology and threats evolve.

### Defense in Depth: A Layered Approach to Cybersecurity

Defense in Depth (DiD) is a fundamental cybersecurity strategy that utilizes multiple layers of security controls to safeguard information systems, devices, and data. It's like building a castle with multiple walls, moats, and guards – each layer acting as a barrier that makes it more difficult for attackers to infiltrate the core.

## Why Defense in Depth?

* **No Single Point of Failure:** If one layer is breached, the others can still provide some level of protection and slow down attackers, buying time for detection and response.
* **Improved Security Posture:** By layering controls, you address vulnerabilities from various angles, making it more challenging for attackers to find a successful exploit.
* **Enhanced Resilience:** A DiD approach allows your defenses to adapt and provide some level of protection even against unknown threats.

## Security Controls for a Layered Defense

Here are some security controls categorized by the layers they typically address in a defense-in-depth strategy:

## 1. Perimeter Security

* **Firewalls:** Act as a barrier between your internal network and the external world, filtering incoming and outgoing traffic based on security policies.
* **Intrusion Detection/Prevention Systems (IDS/IPS):** Monitor network traffic and system activity for malicious behavior, potentially blocking attacks before they succeed.
* **DDoS Protection:** Mitigates Distributed Denial-of-Service attacks that aim to overwhelm systems with traffic.

## 2. Network Security

* **Network Segmentation:** Divides the network into smaller segments, limiting the spread of a potential breach and the impact it can have.
* **Access Control Lists (ACLs):** Define rules for network access, allowing only authorized devices and users to connect to specific resources.
* **VPN (Virtual Private Network):** Encrypts data traffic over public networks like the internet, securing communication between remote users and the network.

## 3. System and Device Security

* **Operating System Hardening:** Securing operating systems by disabling unnecessary services, applying security updates, and configuring strong passwords.
* **Antivirus and Anti-Malware Software:** Detects and removes malicious programs that can infect devices and steal data.
* **Application Whitelisting:** Only allows approved applications to run on devices, preventing unauthorized software execution.

## 4. Data Security

* **Data Encryption:** Transforms data into an unreadable format using encryption algorithms, protecting sensitive information even if intercepted.
* **Data Loss Prevention (DLP):** Prevents sensitive data from being exfiltrated from the organization through unauthorized channels.
* **Data Classification:** Classifying data based on its sensitivity helps prioritize security measures and controls for different types of data.

## 5. User Education and Awareness

* **Security Awareness Training:** Educates users about cybersecurity threats, best practices for secure behavior, and how to identify phishing attempts or social engineering tactics.
* **Password Management:** Enforces strong password policies and encourages the use of multi-factor authentication (MFA) for added login security.
* **Incident Reporting:** Provides clear channels for users to report suspicious activity or potential security incidents, allowing for faster response and mitigation.

## Real-World Examples

* **Firewall:** Imagine a firewall as the castle's outer wall, the first line of defense against intruders.
* **Vulnerability Assessment:** Regularly scanning your systems for vulnerabilities is like inspecting the castle walls for weaknesses and repairing them before attackers can exploit them.
* **Data Encryption:** Encrypting data is like locking away valuables in a secure chest within the castle, adding an extra layer of protection even if an attacker breaches the outer defenses.

By implementing a comprehensive defense-in-depth strategy and layering various security controls, organizations can significantly improve their cybersecurity posture and make it much harder for attackers to succeed. Remember, cybersecurity is an ongoing process, and these controls need to be continuously reviewed, updated, and adapted to address evolving threats.

## Principle of Least Privilege (POLP)

* The foundation of secure access control. It dictates that users and systems should be granted the **minimum permissions** necessary to perform their intended tasks. This principle minimizes the potential damage if an account is compromised because the attacker's access is limited.

## Hardening the System

* The process of strengthening a system's security posture by reducing its attack surface. Here's how it aligns with POLP:
  * **Removing unnecessary services and users:** Eliminating unused accounts and services reduces potential entry points for attackers. Fewer accounts with limited privileges make it harder to gain a foothold.
  * **Avoiding Privilege Creep:** Over time, users' permissions can gradually expand beyond what's necessary. Regularly reviewing and revoking unnecessary privileges ensures users only have the minimum access they currently require. This aligns with POLP by minimizing user permissions.

## Just-in-Time (JIT) Access

* A security practice that grants temporary access to specific resources only when needed and for a limited duration. This further restricts access compared to a static permission assignment. JIT complements POLP by providing temporary elevated access only when absolutely necessary.

## Annual Recertification Campaign

* A periodic review process that verifies whether users still require the access permissions they have. This helps prevent privilege creep and ensures that only authorized users have access to sensitive resources. Recertification campaigns indirectly support POLP by keeping user permissions in check.

## Here's an analogy

Imagine a secure building:

* **POLP:** Assigning specific keys (permissions) to tenants only for the areas they need to access (e.g., apartment key, not master key).
* **Hardening the System:** Removing unnecessary doors and windows (unused services/users) and reinforcing existing ones (security updates).
* **Just-in-Time Access:** Granting a temporary key to a repair person (elevated access) only for the duration of the repair.
* **Annual Recertification Campaign:** Reviewing tenant occupancy and ensuring they still have a valid reason to hold their keys (access permissions).

By implementing these principles together, you create a layered security approach that minimizes risks and makes it more difficult for attackers to exploit vulnerabilities in your systems.

**Separation of Duties (SoD)**, also known as segregation of duties, is a fundamental security principle that aims to prevent fraud, errors, and unauthorized access to sensitive information or systems. It works by distributing tasks and responsibilities across different individuals or teams, ensuring no single person has complete control over a critical process.

Here's how separation of duties helps enhance security:

* **Reduced Risk of Fraud:** By dividing tasks, it becomes more difficult for a single person to manipulate data or commit fraudulent activities. For example, someone initiating a financial transaction shouldn't also be the one approving it.
* **Improved Accuracy:** Distributing tasks can lead to better error detection as different individuals review and verify each other's work.
* **Enhanced Accountability:** With clear ownership of specific tasks, it's easier to identify who is responsible for errors or security breaches.

## Implementing Separation of Duties

Here are some ways to implement SoD in your organization:

* **Transaction Processing:** Separate the initiation, authorization, and recording of financial transactions. For instance, someone creating a purchase order shouldn't be the one approving it or processing the payment.
* **Data Access Control:** Grant users access to data only based on their job requirements. Someone processing payroll shouldn't have access to confidential employee information beyond salaries.
* **Physical Security:** Limit access to physical assets like cash or servers to authorized personnel.

## Benefits of Separation of Duties

* **Stronger Security Posture:** Reduces the risk of internal threats and malicious activities.
* **Improved Accuracy and Efficiency:** Distributing tasks can lead to better quality control and streamlined workflows.
* **Enhanced Regulatory Compliance:** Many regulations require organizations to implement SoD controls for sensitive processes.

## Examples of Separation of Duties

* **Banking:** A teller cannot approve their own loan applications.
* **Accounting:** The person recording transactions shouldn't reconcile bank statements.
* **IT Security:** The administrator who creates user accounts shouldn't also have access to grant elevated privileges.

**Remember, separation of duties is an ongoing process. Regularly review your security policies and access controls to ensure they remain effective.**

Security by Design is a proactive approach to cybersecurity that integrates security considerations throughout the entire software development lifecycle (SDLC), from the initial concept to deployment and maintenance. Here's a breakdown of this concept and two key practices within it:

## Security by Design Principles

* **Early and Continuous Integration:** Security considerations are addressed from the beginning of the development process, not as an afterthought. This helps identify and address security vulnerabilities early on, reducing the cost and complexity of fixing them later.
* **Threat Modeling:** Proactively identifying and analyzing potential threats and vulnerabilities associated with the software being developed. This allows developers to build in safeguards against these threats from the start.
* **Secure Coding Practices:** Using secure coding techniques and methodologies to minimize the introduction of vulnerabilities during development. This includes practices like proper input validation and sanitization to prevent common attacks like injection attacks.
* **Secure Architecture:** Designing the software architecture with security in mind, considering factors like authentication, authorization, data encryption, and secure communication protocols.
* **Security Testing:** Continuously integrating security testing throughout the development process to identify and address vulnerabilities before the software is deployed. This includes static code analysis, dynamic application security testing (DAST), and penetration testing.

## Benefits of Security by Design

* **Reduced Risk of Vulnerabilities:** By proactively addressing security concerns throughout development, the likelihood of vulnerabilities being introduced and exploited is significantly reduced.
* **Faster Time to Market:** Integrating security early can streamline the development process by avoiding the need for extensive security fixes later on.
* **Lower Development Costs:** Early identification and mitigation of security issues is generally less expensive than fixing them after deployment.
* **Improved Software Quality:** Security by Design leads to more robust and secure software overall.

## Examples of Security by Design Practices

* **Shift Left:** This concept emphasizes moving security testing and considerations as far left (earlier) in the development lifecycle as possible. This allows for earlier vulnerability detection and correction.
* **Shared Responsibility:** In cloud computing environments, security is a shared responsibility between the cloud provider and the customer. The cloud provider is responsible for the security of the underlying infrastructure, while the customer is responsible for securing their data and applications deployed on the cloud platform.

## Shift Left (Security Left Shift)

Shift Left focuses on integrating security practices earlier in the development lifecycle. Here are some ways this is achieved:

* **Security training for developers:** Equipping developers with the knowledge and skills to write secure code from the start.
* **Static code analysis tools:** Automatically scanning code for potential vulnerabilities during development.
* **Secure coding libraries and frameworks:** Using libraries and frameworks that promote secure coding practices and reduce the risk of introducing vulnerabilities.
* **Early integration of security testing:** Including security testing activities (unit testing, code reviews) as early as possible in the development process.

By shifting security left, organizations can identify and address vulnerabilities early, leading to more secure and reliable software.

## Shared Responsibility

In cloud computing, security is a shared responsibility model. Here's a breakdown of the responsibilities:

* **Cloud Provider:**
  * Secures the underlying infrastructure (physical servers, network, storage).
  * Provides secure cloud platform services with features like access control and encryption.
* **Customer:**
  * Secures their data and applications deployed on the cloud platform.
  * Manages user access controls and permissions.
  * Configures security settings for cloud services they use.

Understanding this shared responsibility model is crucial for ensuring security in the cloud. Both the cloud provider and the customer need to play their part in securing the environment and data.

By adopting Security by Design principles, including practices like Shift Left and Shared Responsibility, organizations can significantly improve their overall security posture and develop more secure and reliable software applications.

Absolutely! The Keep It Simple and Stupid (KISS) principle applies very well to cybersecurity. Here's the gist in a way that's easy to understand:

## Don't make security complicated!

Here are some KISS security tips for everyday users:

* **Strong Passwords & MFA:** Create strong, unique passwords for all your accounts and enable Multi-Factor Authentication (MFA) whenever possible. Think of passwords like your house keys - don't use the same one for everything, and add an extra layer of security with a lock (MFA).
* **Software Updates:** Keep your operating system, applications, and firmware updated with the latest security patches. These updates are like fixing holes in your digital fence, so attackers can't get in.
* **Beware Phishing:** Don't click on suspicious links or open attachments from unknown senders. Phishing emails try to trick you into revealing personal information or clicking on malicious links, like someone pretending to be your bank asking for your login details. If something seems fishy, don't click!
* **Be Careful What You Share Online:** Think before you post personal information or sensitive data online. Once it's out there, it's hard to control who sees it.
* **Secure Your Wi-Fi:** Use a strong password for your Wi-Fi network and avoid using public Wi-Fi for sensitive activities like online banking. Public Wi-Fi is like an open coffee shop - anyone can be lurking around.
* **Back Up Your Data:** Regularly back up your important data to an external drive or cloud storage. This way, if something happens to your device, you won't lose your precious files. Think of it like having a fireproof safe for your digital memories.

By following these simple KISS security practices, you can significantly reduce your risk of cyberattacks and protect your data. Remember, even small steps can make a big difference!

Security by obscurity (also known as security through obscurity) is a cybersecurity approach that relies on keeping the details of a security system or its vulnerabilities secret. The idea is that if attackers don't know how the system works or where the weaknesses are, they won't be able to exploit them.

Here's an analogy: Imagine you have a hidden room in your house secured by a complex lock. An attacker wouldn't know the room exists, let alone how to open the lock.

## Why is Security by Obscurity Considered Weak?

* **Unreliable:** Secrecy is hard to maintain. If the details of the system are leaked or discovered through reverse engineering, the entire security crumbles.
* **Focus on Hiding, Not Strengthening:** It focuses on hiding weaknesses instead of addressing them directly. A strong security system should be robust even if its inner workings are known.
* **False Sense of Security:** Relying solely on obscurity can lead to a false sense of security, neglecting other essential security measures.

## Security by Obscurity vs. Security Through Design

A more reliable approach is **Security by Design**. This proactive strategy incorporates security considerations throughout the entire development process, building strong defenses from the ground up. It's like building a secure house with strong locks, alarms, and good lighting, not just hiding the valuables inside.

## Is Security by Obscurity Completely Useless?

While not a primary defense, security by obscurity can be used as a **supplementary layer** in certain situations. For example:

* **Obfuscating code:** Slightly scrambling code can make it a little more difficult for attackers to understand its functionality, but it shouldn't be the only security measure.
* **Using non-standard port numbers:** While not foolproof, using less common port numbers can make automated attacks slightly less likely to target the system.

**Remember:** Security by obscurity should never be the sole security strategy. It's essential to implement robust security controls and practices alongside other methods to truly protect your systems and data.

Cyber security architecture is the blueprint for an organization's overall information security strategy. It's like a well-designed castle defense plan, outlining the tools, technologies, policies, and procedures used to safeguard critical systems, data, and devices.

## Here's what cyber security architecture involves

* **Identifying Assets and Threats:** The first step involves understanding what needs to be protected. This includes critical data, systems, applications, and infrastructure. Security architects also need to identify potential threats and vulnerabilities that could exploit these assets.
* **Designing Secure Infrastructure:** This involves selecting and configuring security controls like firewalls, intrusion detection systems, and data encryption to create a layered defense. Imagine the castle walls, moats, and guard towers working together to slow down attackers.
* **Defining Access Controls:** Security architects define who has access to what resources and information. This includes user authentication and authorization policies, ensuring only authorized users can access specific systems and data. Think of it like assigning keys to specific people for different areas of the castle.
* **Implementing Security Policies:** Clear policies are created to outline acceptable security practices for users, such as password complexity requirements and responsible data handling procedures. These policies are like the rules everyone in the castle must follow to maintain security.
* **Incident Response Planning:** The plan outlines how the organization will respond to security incidents, such as data breaches or cyberattacks. This includes procedures for identifying, containing, eradicating, and recovering from such events. Imagine having a fire drill plan for the castle in case of an attack.

## Benefits of a strong cyber security architecture

* **Proactive Defense:** By planning and implementing security measures in advance, organizations can be better prepared to prevent cyberattacks or minimize their impact.
* **Reduced Risk:** A well-designed architecture identifies and addresses vulnerabilities, leading to a lower risk of security breaches.
* **Improved Efficiency:** Standardized security controls and procedures streamline security operations and make it easier to manage.
* **Scalability:** A flexible architecture can adapt and grow as an organization's security needs evolve.

**In essence, cyber security architecture plays a critical role in protecting organizations from cyber threats by providing a comprehensive and strategic approach to information security.** It's an ongoing process that requires continuous monitoring, review, and adaptation to keep pace with the ever-changing threat landscape.

### Cyber Security Architecture Building Blocks:

A strong cyber security architecture is like a well-fortified castle, with different layers working together to defend your data and systems. Here's a breakdown of some key components you mentioned:

* **MFA (Multi-Factor Authentication):** An extra layer of security for logins, requiring users to provide more than just a username and password. This could be a code from your phone, a fingerprint scan, or a security key. Think of it as a secondary lock on your castle gate, making it harder for attackers to gain entry even if they steal your password (like a key).
* **MDM (Mobile Device Management):** A system for managing and securing mobile devices like smartphones and tablets used within an organization. MDM allows IT to enforce security policies, distribute apps, and remotely wipe lost or stolen devices. Imagine having a central armory for managing and securing all the guards' weapons (mobile devices) in the castle.
* **EDR (Endpoint Detection and Response):** A system that continuously monitors devices (endpoints) for suspicious activity that might indicate a cyberattack. EDR can detect and respond to threats in real-time, helping to prevent breaches or minimize their impact. Think of having vigilant guards patrolling the castle grounds, constantly on the lookout for suspicious activity.
* **Data Encryption:** The process of transforming data into an unreadable format using encryption algorithms. This ensures that even if attackers manage to steal data, they cannot access the information without the decryption key. Imagine storing valuables in locked chests within the castle, adding an extra layer of protection even if someone breaks in.
* **Firewall:** A security barrier that controls incoming and outgoing network traffic based on predefined security policies. A firewall acts like the castle gate, only allowing authorized traffic (people) to enter and exit.

These are just a few examples of security controls used in cyber security architecture. The specific tools and technologies will vary depending on the organization's size, industry, and security needs. But by implementing a layered approach that combines these elements, organizations can significantly improve their overall security posture and protect themselves from cyber threats.

The Security Lifecycle, also known as the Information Security Lifecycle (ISL), is a framework that outlines the ongoing process of protecting an organization's information assets. It's a cyclical process, meaning you revisit and refine each stage as your security needs evolve. Here's a breakdown of the key phases:

## 1. Risk Analysis

* This is the foundation of the security lifecycle. It involves identifying, understanding, and prioritizing the security risks your organization faces. This includes:
  * Identifying critical assets: data, systems, applications, devices.
  * Recognizing potential threats: cyberattacks, data breaches, unauthorized access.
  * Assessing vulnerabilities: weaknesses in systems or processes that could be exploited.
  * Evaluating the impact: potential damage caused by a successful attack.

## 2. Policies and Procedures

* Based on the risk analysis, this stage defines clear policies and procedures to manage those risks. These policies outline:
  * Acceptable use of IT resources.
  * Password complexity requirements.
  * Data classification and handling procedures.
  * Incident response protocols.
  * Employee security awareness training programs.

## 3. Architecture Building

* This stage involves designing the technical infrastructure to implement the security policies. This includes:
  * Selecting and configuring security controls like firewalls, intrusion detection systems, and data encryption.
  * Defining network segmentation to isolate sensitive data.
  * Implementing access controls to restrict unauthorized access.
  * Choosing security tools for endpoint protection and vulnerability scanning.

## 4. Implementation

* This phase involves putting the security architecture into action. It includes:
  * Installing and configuring security hardware and software.
  * Setting up user accounts and access permissions.
  * Integrating security tools with existing systems.
  * Providing security awareness training to employees.

## 5. Administration and Maintenance

* Security is an ongoing process. This stage focuses on:
  * Regularly updating security software and firmware with the latest patches.
  * Monitoring security logs for suspicious activity.
  * Performing vulnerability assessments and penetration testing to identify and address weaknesses.
  * Reviewing and updating security policies and procedures as needed.

## 6. Audit and Assessment

* This stage involves verifying the effectiveness of the security controls. It includes:
  * Security audits to identify any gaps or weaknesses in the security posture.
  * Penetration testing to simulate real-world cyberattacks and assess the system's resilience.
  * Reviewing incident response procedures to ensure they are effective.

By following these phases and continuously improving your security posture, you can significantly reduce your risk of cyberattacks and protect your valuable information assets.

Cyber security frameworks

* NIST CSF  v2

Cyber security is a vast field, and to effectively address all the potential threats, organizations need to consider various domains. These domains represent different areas where security controls and practices are implemented. Here's a breakdown of some of the most crucial domains you mentioned:

## 1. Identity and Access Management (IAM)

* Focuses on managing user identities and access to organizational resources.
* Ensures only authorized users can access specific systems and data based on their roles and permissions.
* Examples of IAM controls: multi-factor authentication (MFA), single sign-on (SSO), user provisioning and deprovisioning.

## 2. Endpoint Security

* Secures devices like laptops, desktops, smartphones, and tablets used by employees.
* Protects endpoints from malware, phishing attacks, unauthorized access, and data breaches.
* Examples of endpoint security controls: antivirus software, application whitelisting, endpoint detection and response (EDR).

## 3. Network Security

* Safeguards the organization's computer network infrastructure.
* Controls incoming and outgoing network traffic to prevent unauthorized access and malicious activity.
* Examples of network security controls: firewalls, intrusion detection/prevention systems (IDS/IPS), network segmentation.

## 4. Application Security

* Focuses on securing applications and software used by the organization.
* Aims to prevent vulnerabilities in applications from being exploited by attackers.
* Examples of application security practices: secure coding practices, vulnerability scanning, penetration testing.

## 5. Data Security

* Protects the confidentiality, integrity, and availability of sensitive organizational data.
* Ensures data is protected at rest (stored), in transit (being transferred), and in use (accessed).
* Examples of data security controls: data encryption, data classification, data loss prevention (DLP).

## 6. Logging and Monitoring

* Continuously monitors and records security-related events on systems and networks.
* Provides valuable information for detecting suspicious activity, investigating security incidents, and identifying potential threats.
* Examples of logging and monitoring tools: security information and event management (SIEM), log management systems.

## 7. Incident Response

* Defines the plan for responding to security incidents like cyberattacks and data breaches.
* Outlines procedures for identifying, containing, eradicating, and recovering from security incidents.
* Ensures a swift and coordinated response to minimize the impact of an incident.

These domains are interconnected, and a strong security posture requires a comprehensive approach that addresses all of them. By implementing appropriate security controls and practices in each domain, organizations can significantly improve their overall cybersecurity posture and protect themselves from evolving cyber threats.

## In this section

* ✅ [Introduction to Cyber Security and core concepts](introduction-to-cyber-security-and-core-concepts.md)
* ✅ [Getting Started into Cyber Security Career](getting-started-into-cyber-security-career.md)
* ✅ [Online Cybersecurity Practice Labs to Sharpen Your Skills](online-cybersecurity-practice-labs-to-sharpen-your-skills.md)
* ✅ [Cyber Security Interview Q&A](cyber-security-interview-qanda/README.md) · 2/2 pages written
* ✅ [Certification Preparation](certification-preparation/README.md) · 3/3 pages written
* ✅ [The Security Engineer Role](the-security-engineer-role.md)
* ✅ [CISSP](cissp.md)
