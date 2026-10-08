# Security Engagement

1. Pre-Engagement
   1. Scope Definition (Security and Privacy)
      * **In-Scope:** Clearly define the systems, applications, and data that the pen tester can target.
      * **Out-of-Scope:** Specify what's off-limits, like critical production systems or sensitive data.
      * **Authorized Attacks:** Outline the types of attacks the pen tester can perform (e.g., password spraying, social engineering attempts).
      * **Severity Levels:** Define the acceptable risk levels for identified vulnerabilities (critical, high, medium, low).
      * **Deliverables and Timeline:** Specify the format and timeframe for the pen test report.
      * **Objectives:** Clearly define the goals of the red team exercise (e.g., compromise a specific system, steal data, disrupt operations).
      * **Targets:** Specify the assets the red team can target, potentially including physical locations, personnel, and IT systems.
      * **Rules of Engagement (ROE):** Define acceptable actions and limitations for the red team (e.g., no data deletion or disruption of critical services).
      * **Reporting:** Outline the format and timeframe for the red team report, including identified vulnerabilities and recommendations.

   2. Regulations
      1. Penetration testing often involves auditing compliance with relevant regulations.

         **1. Identify Applicable Regulations:**

         * **Industry:** Start by understanding the industry your organization operates in. Different sectors have specific regulations (e.g., healthcare: HIPAA, finance: PCI DSS).
         * **Location:** Consider regional and national regulations that might apply (e.g., GDPR in Europe, CCPA in California).
         * **Data Storage:** If you store sensitive data (e.g., credit card numbers, health information), specific data privacy regulations might apply.

         **2. Prioritize Regulations:**

         * **Risk Assessment:** Conduct a risk assessment to identify the most critical regulations based on the potential impact of non-compliance.
         * **Data Sensitivity:** Focus on regulations that govern the type of data you handle (e.g., if you deal with health data, prioritize HIPAA compliance).
         * **Likelihood of Audit:** Consider the likelihood of regulatory audits and prioritize regulations with higher audit frequency.

         **3. Mapping Regulations to Pen Testing Scope:**

         * **Compliance Controls:** Many regulations outline specific security controls. Integrate testing of these controls into your pen testing scope.
         * **Vulnerability Focus:** Align your pen testing strategy with the vulnerabilities most likely to violate relevant regulations.
         * **Reporting Requirements:** Tailor your pen test reports to address the specific requirements of the regulations being audited.

   3. Frameworks

      Security and risk frameworks provide a structured approach for assessing and managing security posture.

      1. **Industry Standards:**
         * Look for frameworks recognized within your industry (e.g., PCI DSS for finance, NIST Cybersecurity Framework for general IT).
      2. **Regulatory Requirements:**
         * Some regulations mandate adherence to specific frameworks (e.g., HIPAA and HITRUST for healthcare).
      3. **Threat Landscape:**
         * Choose a framework that addresses the current threat landscape and relevant attack vectors.
      4. **Organizational Needs:**
         * Consider your organization's size, maturity, and specific security goals when selecting a framework.

      **Popular Frameworks for Pen Testing Validation and Recommendations:**

      * **NIST Cybersecurity Framework (CSF):**
        * Provides a comprehensive framework for managing cybersecurity risk, useful for identifying gaps and recommending control enhancements.
      * **MITRE ATT\&CK Framework:**
        * Categorizes attacker tactics, techniques, and procedures (TTPs), helping you map pen test findings to real-world threats and identify security control gaps.
      * **ISO 27001:**
        * Offers a risk-based approach to information security management, aiding in aligning pen test recommendations with your overall security posture.
      * **COBIT 5:**
        * Focuses on aligning IT with business goals, valuable for ensuring security recommendations support business objectives.

      **Leverage Frameworks by:**

      1. **Mapping Controls:**
         * Map security controls identified in the chosen framework to pen test findings.
         * This helps determine if existing controls are adequate or need improvement.
      2. **Threat Modeling:**
         * Utilize frameworks like MITRE ATT\&CK to understand how identified vulnerabilities align with real-world attacker behavior.
         * This strengthens future recommendations by addressing likely attack scenarios.
      3. **Risk Assessment:**
         * Integrate risk assessment methodologies from chosen frameworks to prioritize recommendations.
         * This ensures you focus on the vulnerabilities that pose the greatest risk.

   4. Standards

      **Compliance-driven Standards:**

      * **PCI DSS (Payment Card Industry Data Security Standard):**
        * Essential for organizations that handle credit card information. Defines security requirements for cardholder data environments.
      * **HIPAA (Health Insurance Portability and Accountability Act):**
        * Protects sensitive patient data in the healthcare industry. Outlines security measures to safeguard electronic protected health information (ePHI).
      * **GDPR (General Data Protection Regulation):**
        * Applies to organizations processing the personal data of EU citizens. Emphasizes data protection principles and security controls.
      * **SOC 2 (Service Organization Controls):**
        * Focuses on internal controls relevant to security, availability, integrity, confidentiality, and privacy (SAAICP) for service providers.

      **General Security Frameworks:**

      * **NIST Cybersecurity Framework (CSF):**
        * Provides a comprehensive, voluntary framework for managing cybersecurity risk. Offers guidance for identifying, protecting, detecting, responding to, and recovering from cyber threats.
      * **ISO 27001 (Information Security Management Systems):**
        * Defines best practices for an Information Security Management System (ISMS) that includes information asset identification, risk assessment, and control implementation.
      * **COBIT 5 (Control Objectives for Information and Related Technology):**
        * Governs the alignment of IT with business goals. Useful for ensuring pen test recommendations support broader security objectives.

      **Penetration Testing Methodologies:**

      * **PTES (Penetration Testing Execution Standard):**
        * Provides a comprehensive methodology for conducting pen tests. Outlines phases like planning, execution, reporting, and post-engagement activities.
      * **OSSTMM (Open-Source Security Testing Methodology Manual):**
        * Offers a scientific methodology for network penetration testing and vulnerability assessment. Provides a structured approach for pen testers.

   5. Rules of engagement

      The Rules of Engagement (ROE) are a crucial document in any penetration testing engagement. They outline the expectations for both the client (organization) and the penetration tester, ensuring a smooth and successful assessment. Here's a detailed explanation of the elements you mentioned:

      **1. Exclusions:**

      This section clearly defines what is **out of scope** for the pen test. This might include:

      * **Specific systems:** Critical production systems that cannot be disrupted can be excluded.
      * **Data types:** Highly sensitive data, like personally identifiable information (PII), might be off-limits for testing.
      * **Attack methods:** Certain aggressive attack techniques (e.g., Denial-of-Service attacks) might be prohibited to avoid system downtime.

      **2. Test Cases:**

      This section may or may not be included, depending on the engagement type. If present, it outlines specific scenarios or vulnerabilities the pen tester will focus on.

      **Here are two approaches to Test Cases:**

      * **White-box testing:** The client provides a list of known vulnerabilities or weaknesses for the pen tester to verify and exploit.
      * **Black-box testing:** The pen tester has minimal prior knowledge and is expected to discover vulnerabilities independently.

      **3. Escalation Process:**

      This section defines how critical findings or unexpected events will be communicated and addressed during the pen test. It typically involves a step-by-step process:

      * **Initial discovery:** The pen tester reports the finding to a designated point of contact on the client's team.
      * **Severity assessment:** Both parties collaborate to assess the severity of the finding and its potential impact.
      * **Decision-making:** Based on the severity, a decision is made on how to proceed (e.g., pause testing, adjust scope, implement temporary mitigation).

      **4. Testing Window:**

      This section defines the specific timeframe during which the pen testing activities will be conducted. It includes:

      * **Start and end date/time:** Clearly defines the authorized testing period.
      * **Testing hours:** Specifies the time window within each day when testing can occur (e.g., weekdays from 9 AM to 5 PM).
      * **Notification:** Outlines how the client will be notified before testing commences.

      **Additional Considerations for a Comprehensive ROE:**

      * **Roles and Responsibilities:** Defines the roles and responsibilities of key personnel involved in the pen test (e.g., client team members, pen testers).
      * **Communication Channels:** Specifies the preferred communication methods for reporting findings, escalation issues, and general project updates.
      * **Confidentiality:** Emphasizes the importance of confidentiality regarding the pen test activities and findings.
      * **Deliverables:** Defines the format and expected content of the final pen test report.

      By establishing a clear and detailed ROE, both the client and the pen tester can ensure a safe, productive, and successful pen testing engagement.

   6. Agreement Types

      Here's a table summarizing the key differences:

      | Agreement Type                 | Focus                               | Example                          | Key Elements                                                           |
      | ------------------------------ | ----------------------------------- | -------------------------------- | ---------------------------------------------------------------------- |
      | Non-Disclosure Agreement (NDA) | Protecting confidential information | Sharing trade secrets            | Definition of confidential information, permitted uses, duration       |
      | Master Service Agreement (MSA) | Ongoing services framework          | Cloud service provider agreement | Scope of services, pricing, service levels, termination                |
      | Statement of Work (SOW)        | Project specifics within an MSA     | Cloud service migration project  | Project scope, timeline, deliverables, acceptance criteria             |
      | Terms of Service (ToS)         | Using a website or service          | Social media platform terms      | Acceptable user behavior, limitations of liability, dispute resolution |

   7. Target Selection in Penetration Testing: Choosing Your Attack Surface

      In penetration testing, target selection is crucial. It defines the attack surface, the specific areas you'll focus on to identify vulnerabilities. Here's how the options you mentioned factor into target selection:

      **1. CIDR Ranges:**

      * A notation for identifying a block of IP addresses. It combines the network address with a subnet mask to define the range of valid IP addresses within that block. (e.g., 192.168.1.0/24 represents 256 possible IP addresses from 192.168.1.0 to 192.168.1.255).
      * Specifying a CIDR range can be useful for testing internal networks or a large group of devices within a specific network segment.

      **2. Domain:**

      * A human-readable name that translates to an IP address. It represents a website or organization on the internet (e.g., \[invalid URL removed]).
      * Targeting a domain can be the starting point for identifying web servers, applications, and subdomains associated with that organization.

      **3. IP addresses:**

      * A unique numerical identifier assigned to a device on a network. It allows for communication and data exchange between devices.
      * Targeting specific IP addresses can be useful for focusing on individual devices like web servers, databases, or critical infrastructure components.

      **4. URL (Uniform Resource Locator):**

      * A specific address that locates a web page or resource on the internet. It includes the protocol (e.g., http, https), domain name, and specific path to the resource (e.g., \[invalid URL removed]).
      * Targeting specific URLs allows for testing individual web pages, applications, or functionalities within a website.

      **Choosing the Right Target:**

      The best target selection method depends on the specific engagement and the information available. Here are some factors to consider:

      * **Engagement Scope:** The scope might specify a particular domain, IP range, or specific web application.
      * **Attack Scenario:** The chosen target should align with the simulated attack scenario (e.g., targeting internal network for a breach attempt vs. focusing on a specific web application for vulnerability assessment).
      * **Information Gathering:** Initial reconnaissance might reveal additional details about the target network or infrastructure, influencing target selection.

      Clear and well-defined target selection is essential for a focused and efficient penetration testing engagement.

   8. Assessment Types
      1. **Web Application Penetration Testing:**
         * Focuses on identifying vulnerabilities in web applications and websites.
         * Techniques include testing login forms, user input validation, and server-side logic.
      2. **Network Penetration Testing:**
         * Assesses the security posture of a computer network.
         * Involves identifying weaknesses in network devices, firewalls, and configurations. Techniques include scanning for vulnerabilities and simulating attacker methods.
      3. **Mobile Application Penetration Testing:**
         * Evaluates the security of mobile apps for smartphones and tablets.
         * Focuses on vulnerabilities in app functionality, data storage, and communication channels.
      4. **Cloud Penetration Testing:**
         * Assesses the security of cloud infrastructure and services.
         * Involves testing for vulnerabilities in cloud storage, compute resources, and access controls.
      5. **API Penetration Testing:**
         * Focuses on identifying vulnerabilities in Application Programming Interfaces (APIs) that connect different applications.
         * Techniques involve testing authentication mechanisms, data validation, and authorization controls.
      6. **Application Penetration Testing (Broader term):**
         * Encompasses web application, mobile app, and potentially other types of application security assessments.
         * Focuses on vulnerabilities within the application code, functionality, and data handling.
      7. **Wireless Network Penetration Testing:**
         * Evaluates the security of Wi-Fi networks and wireless access points.
         * Techniques involve testing for encryption strength, unauthorized access points, and potential weaknesses in wireless protocols.

   9. ### Shared Responsibility in Penetration Testing

      Penetration testing is a collaborative effort, and each party involved has specific responsibilities to ensure a successful and secure engagement. Here's a breakdown of the key players and their roles:

      **1. Customer Responsibilities:**

      * **Defining Scope:** Clearly define the target systems, applications, and data in scope for the pen test.
      * **Providing Access:** Grant the pen tester necessary access to systems and data to perform the assessment.
      * **Understanding Risk:** Acknowledge the potential risks involved in penetration testing and implement necessary safeguards.
      * **Communication:** Maintain clear communication with the pen tester throughout the engagement.
      * **Remediation:** Address identified vulnerabilities and implement mitigation strategies based on the pen test report.

      **2. Penetration Tester Responsibilities:**

      * **Ethical Conduct:** Adhere to a strict code of ethics, ensuring they only exploit vulnerabilities with authorization and avoid causing harm.
      * **Methodology:** Follow a structured methodology for conducting the pen test, ensuring a comprehensive assessment.
      * **Vulnerability Testing:** Identify, exploit, and document potential vulnerabilities in the target systems and applications.
      * **Reporting:** Deliver a detailed report outlining the findings, including severity levels, exploit details, and recommendations for remediation.
      * **Communication:** Maintain clear communication with the customer throughout the engagement, addressing questions and concerns.

      **3. Third-Party Responsibilities:**

      * **Subcontractors:** If the pen tester uses subcontractors, they are responsible for ensuring their ethical conduct and adherence to the agreed-upon scope.
      * **Bug Bounty Platforms:** If using a bug bounty platform, the platform provider is responsible for facilitating communication and managing vulnerability submissions ethically.

      **4. Hosting Provider Responsibilities:**

      * **Infrastructure Security:** Maintain the security of their underlying infrastructure that hosts the customer's systems and applications.
      * **Shared Responsibility Model:** Clearly communicate their security responsibilities as part of their service agreement, outlining what they are responsible for and what falls on the customer.

   10. ### Legal and Ethical Considerations in Penetration Testing

       Penetration testing is a powerful tool for improving security, but it's crucial to approach it with legal and ethical considerations in mind.

       **1. Authorization Letters:**

       * Always obtain written authorization from the owner of the system or application before conducting a pen test. This protects you from legal repercussions and demonstrates a commitment to ethical practices.
       * The authorization letter should clearly define the scope of the pen test, acceptable attack methods, and limitations. It should also acknowledge the potential risks involved.

       **2. Mandatory Reporting Requirements:**

       * **Certain industries:** Regulations in some sectors (e.g., healthcare: HIPAA) might mandate reporting of identified vulnerabilities within a specific timeframe.
       * **Data breaches:** Data breach notification laws might require reporting security incidents that expose sensitive data.
       * **Contractual obligations:** Contracts with third-party vendors might have clauses requiring the reporting of security vulnerabilities discovered during engagements.

       **3. Penetration Testing Risks:**

       **Business Impact:**

       * **Downtime:** Penetration testing activities might cause temporary disruptions to systems and applications, impacting business operations.
       * **Data Loss:** In rare cases, there's a slight risk of data loss if vulnerabilities are not exploited carefully and mitigation strategies are not in place.
       * **Reputational Damage:** If a pen test reveals significant vulnerabilities, it could potentially damage the organization's reputation, especially if the findings are not addressed promptly.

       **Mitigating Penetration Testing Risks:**

       * **Clear Scope Definition:** A well-defined scope minimizes the risk of unintended consequences by outlining authorized activities.
       * **Communication:** Clear communication with stakeholders helps manage expectations and minimize disruption during the pen test.
       * **Testing Environment:** If possible, conduct the pen test in a non-production environment to avoid impacting live systems and data.
       * **Backup and Recovery:** Ensure proper backups are in place to facilitate swift recovery in case of any unforeseen incidents.

       **Additional Legal and Ethical Considerations:**

       * **Confidentiality:** Maintain strict confidentiality regarding the target system, vulnerabilities identified, and the pen test process.
       * **Non-malicious Intent:** Always conduct pen testing with good intentions and avoid exploiting vulnerabilities beyond the authorized scope.
       * **Data Protection:** Handle any sensitive data encountered during the pen test with care and adhere to relevant data protection regulations.

2. ### Notification and Communication in Penetration Testing: Building a Collaborative Process

   Effective communication is the cornerstone of a successful penetration testing engagement. It fosters collaboration between the pen tester and the client, ensuring everyone is on the same page throughout the process. Here's a detailed breakdown of the key elements you mentioned:

   **Communication Channels:**

   * **Email Communication:** While email is a common method for initial contact, sending reports, and general updates, it has limitations. Consider the sensitivity of the information. For highly confidential findings, explore secure platforms that encrypt data and restrict access with granular permissions.
   * **Secure Distribution:** For vulnerabilities with severe business impact or those exposing sensitive data, prioritize secure report distribution channels. Cloud-based platforms with features like access controls, encryption, and audit trails can provide a more secure way to share sensitive information.

   **Communication Content:**

   * **Articulation of Risk, Severity, and Impact:** Don't just report technical jargon. Clearly explain the nature of the vulnerabilities, their severity levels (critical, high, medium, low), and the potential business impact if they are exploited. Quantify the impact whenever possible (e.g., potential financial loss due to data exfiltration or downtime caused by a service outage).
   * **Business Impact Analysis:** Move beyond technical details and translate vulnerabilities into business consequences. Explain how identified weaknesses could disrupt operations, cause financial loss due to data breaches or regulatory fines, or damage the organization's reputation through public exposure.

   **Communication Processes:**

   * **Peer Review:** Penetration testers should have a rigorous peer review process in place. This ensures the accuracy and completeness of findings before they are reported to the client. Peer reviewers can identify potential oversights or misinterpretations, strengthening the overall quality of the assessment.
   * **Escalation Path:** Define a clear escalation process for urgent findings or unexpected events during the pen test. This helps ensure critical vulnerabilities are addressed promptly. The escalation process should outline the steps to be taken, who should be notified (depending on the severity), and the expected response timeframe.
   * **Root Cause Analysis:** Don't just report symptoms; dig deeper to identify the underlying reasons behind vulnerabilities. This goes beyond identifying the technical flaw and helps the client implement effective remediation strategies. For example, a finding might reveal a SQL injection vulnerability in a web application. The root cause analysis might uncover inadequate input validation routines or missing database access controls.
   * **Stakeholder Alignment:** Tailor communication to different audiences. Technical details might be appropriate for IT teams working on remediation, while business leaders might need a high-level overview of risks and mitigation plans with a clear focus on the business impact. Consider using different communication methods or reports customized for each stakeholder group.

   **Additional Considerations:**

   * **Frequency:** Maintain regular communication with the client throughout the engagement, not just at the beginning and end. This keeps everyone informed, fosters trust, and allows for course correction if needed.
   * **Clarity:** Use clear, concise language that avoids overly technical jargon. Strive for transparency while maintaining confidentiality. If technical terms are necessary, provide clear explanations or definitions.
   * **Client Acceptance:** The client should formally acknowledge receipt and acceptance of the final pen test report. This signifies their understanding of the findings, commitment to addressing the identified vulnerabilities, and serves as a record of the engagement.
