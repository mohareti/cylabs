# Security Controls

## Technical Controls

* **System Hardening:** This involves configuring systems with the most secure settings possible. This might include disabling unnecessary services, removing unused accounts, and applying strict access controls.
* **Sanitize User Input/Parameterize:** This refers to validating and filtering all user input to prevent malicious code injection attacks. Parameterization involves using placeholders in queries to prevent attackers from manipulating data through user input fields.
* **Multi-Factor Authentication (MFA):** This adds an extra layer of security by requiring a second factor (e.g., code from a smartphone app) besides a username and password to access systems.
* **Encryption:** This process scrambles data using a key, making it unreadable without decryption. Encryption protects data at rest (stored) and in transit (being transferred).
* **Process-level Remediation:** This involves identifying and fixing vulnerabilities within specific software processes instead of patching the entire application.
* **Patch Management:** This refers to the systematic process of acquiring, testing, and deploying security patches to address vulnerabilities in software and operating systems.
* **Key Rotation:** Regularly changing encryption keys used to protect sensitive data ensures continued security even if an attacker gains access to an old key.
* **Certificate Management:** Issuing, distributing, and revoking digital certificates used for secure communication and authentication requires proper management to maintain trust and prevent misuse.
* **Secrets Management Solution:** This refers to dedicated software tools for securely storing, managing, and controlling access to sensitive credentials like passwords and encryption keys.
* **Network Segmentation:** Dividing the network into smaller segments with restricted access between them limits the potential impact of a security breach.
* **Infrastructure Security Controls:** These encompass various technical measures to secure IT infrastructure, including firewalls, intrusion detection/prevention systems (IDS/IPS), and vulnerability scanning tools.

## Operational Controls

* **Job Rotation:** Regularly rotating employee duties can help prevent collusion and detect potential fraudulent activities.
* **Time-of-Day Restrictions:** Limiting access to critical systems or data to specific times can reduce the window of opportunity for unauthorized access.
* **Mandatory Vacations:** Enforced time off helps ensure employees are not constantly working, potentially overlooking security lapses due to fatigue.
* **User Training:** Educating users about cybersecurity threats, best practices for secure behavior (e.g., strong passwords, not clicking suspicious links), and procedures for reporting suspicious activity is crucial.

## Administrative Controls

* **Role-Based Access Control (RBAC):** This assigns user permissions based on their job function, granting access only to the resources they need to perform their duties.
* **Secure Software Development Life Cycle (SDLC):** Implementing security measures throughout the entire software development process, from design and coding to testing and deployment, helps build secure applications from the ground up.
* **Minimum Password Requirements:** Enforcing strong password complexity requirements (length, character types) makes them more difficult to crack.
* **Policies and Procedures:** Formal documents outlining acceptable use of IT resources, data security protocols, incident response procedures, and other security-related guidelines are essential.

### Physical Security Controls: Protecting Your Hardware

Physical security controls are a crucial line of defense within an organization's overall cybersecurity strategy. They safeguard physical IT infrastructure, data centers, and other critical assets from unauthorized access, theft, or environmental damage. Here's a closer look at the specific controls you mentioned:

* **Access Control Vestibule:** Also known as a mantrap or security interlock, this is a double-doored entryway that requires authorized access to enter and exit. This prevents unauthorized individuals from tailgating someone with valid access through a single doorway.
* **Biometric Controls:** These systems rely on unique personal characteristics (fingerprint, iris scan, facial recognition) for user identification and access control. They offer a high level of security compared to traditional methods like key cards or passwords.
* **Video Surveillance:** Security cameras strategically placed around buildings, server rooms, and other sensitive areas provide visual monitoring and recording of activity. This deters unauthorized access attempts and aids in forensic investigations after a security incident.
* **Security Fences and Gates:** Physical barriers surrounding critical areas restrict unauthorized physical access to a perimeter.
* **Security Guards:** Trained personnel patrolling facilities and monitoring access points provide an active layer of physical security.
* **Locking Mechanisms:** Securing equipment cabinets, server racks, and data storage devices with sturdy locks prevents unauthorized tampering or theft.
* **Environmental Controls:** Maintaining proper temperature, humidity, and power conditions within data centers and server rooms ensures optimal operation of IT equipment and prevents damage from environmental factors.

## Importance of Layering Controls

The most effective security approach involves layering physical controls with other security measures. Here's an example:

* **Access control vestibule:** Prevents unauthorized physical entry.
* **Biometric access control:** Grants access only to authorized personnel with valid biometric data.
* **Video surveillance:** Records activity within the secured area for monitoring and potential investigation.

By combining these controls, organizations create a more robust security posture that significantly reduces the risk of successful physical attacks on critical IT infrastructure.

## Additional Considerations

* **Physical security controls should be integrated with logical security controls** (e.g., network access control, user authentication) for a holistic approach.
* **Regular security assessments** should be conducted to identify vulnerabilities in physical security measures.
* **Security awareness training** for employees should include procedures for reporting suspicious physical security breaches.

## In this section

* 🚧 [Preventive](preventive.md)
* 🚧 [Deterrent](deterrent.md)
* 🚧 [Detective](detective.md)
* 🚧 [Corrective](corrective.md)
* 🚧 [Compensating](compensating.md)
* 🚧 [Directive](directive.md)
