# DevSecOps

**DevSecOps** is a collaborative approach to integrating security practices throughout the entire **Software Development Lifecycle (SDLC)**. This ensures security is a shared responsibility, leading to faster delivery of secure software.

## Secure SDLC

* **Threat modeling:** Identify potential security risks in the early stages of development.
* **Secure coding practices:** Use secure coding principles and tools to prevent vulnerabilities from being introduced in the code.
* **Security testing:** Perform various security tests throughout the SDLC, including static code analysis, dynamic application security testing (DAST), and penetration testing.
* **Vulnerability management:** Identify, prioritize, and remediate vulnerabilities discovered during testing.

## Secure Environments

* **Dev, Test, and Prod environments:** Each environment should be isolated and have different security controls in place based on their purpose.
* **Infrastructure security:** Harden your infrastructure by applying security best practices to operating systems, network configurations, and cloud environments.

## DevSecOps Tools

* **Security information and event management (SIEM):** Aggregates and analyzes security data from various sources to identify threats.
* **Configuration management tools:** Automate infrastructure provisioning and configuration, ensuring consistency and security across environments.
* **Static code analysis (SCA) tools:** Analyze code for security vulnerabilities and coding errors.
* **Container security tools:** Scan container images for vulnerabilities and misconfigurations.
* **Cloud security tools:** Provide various security features for cloud-based infrastructure.

### Pipeline Security

## Secure Development Pipeline

* **Pipeline automation:** Automate security checks into the continuous integration/continuous delivery (CI/CD) pipeline. This allows for early detection and fixing of security issues.
* **Source code security:** Integrate SCA tools into the pipeline to scan code for vulnerabilities and coding errors as it is written.
* **Automated code testing:** Utilize tools like DAST to perform automated security testing throughout the pipeline.
* **Dependency management:** Manage dependencies securely by using trusted repositories and identifying vulnerabilities in dependencies.
* **CI/CD:** Implement secure CI/CD practices, such as using least privilege access and immutable infrastructure.
* **Environment security:** Ensure security controls are in place for each stage of the pipeline environment, including build servers, test environments, and deployment stages.

###

**Threats to the pipeline:** Attacking the Pipeline, Exploiting Vulnerabilities in the Pipeline, Defending the Pipeline

* **Compromised credentials:** Attackers can exploit weak credentials to gain access to the pipeline and inject malicious code.
* **Vulnerable tools and libraries:** Vulnerabilities in pipeline tools and libraries can be exploited to gain access to the pipeline or compromise the software being built.
* **Supply chain attacks:** Malicious code can be introduced through compromised dependencies or third-party components.

## Defending the pipeline

* **Implement strong authentication and authorization controls for access to the pipeline.**
* **Keep pipeline tools and libraries up-to-date with the latest security patches.**
* **Use secure coding practices and perform security testing on custom code used in the pipeline.**
* **Monitor pipeline activity for suspicious behavior and implement intrusion detection systems.**

### Infrastructure as Code and Security

## Infrastructure as Code (IaC)

* IaC tools like Terraform, Vagrant, and Docker allow you to define and manage infrastructure in code.
* This enables automation, consistency, and repeatability in infrastructure provisioning.

## Security Considerations

* **Secret management:** Sensitive information like passwords and API keys should be securely stored and managed using dedicated secret management tools.
* **Vulnerability management:** Regularly scan IaC code for vulnerabilities in the used tools and configuration settings.
* **Least privilege:** Implement least privilege access for users interacting with IaC tools and provisioned infrastructure.

## Exploiting IaC vulnerabilities

* Attackers can exploit vulnerabilities in IaC tools and configurations to gain unauthorized access to infrastructure, inject malicious code, or disrupt operations.

## Mitigating these risks

* **Use secure coding practices when writing IaC code.**
* **Follow best practices for IaC security, such as using separate environments for development, testing, and production.**
* **Regularly audit IaC code and infrastructure configurations for security vulnerabilities.**

### Tools and Technologies for Secure SDLC, Environments, and Tools:

## Secure SDLC

* **Threat modeling:** STRIDE, Trike, Microsoft Threat Modeling Tool
* **Secure coding practices:** CWE Top 25, CERT Secure Coding Standards
* **Static code analysis (SCA) tools:** SonarQube, Fortify SAST, Codacy
* **Dynamic application security testing (DAST) tools:** Acunetix, Netsparker, Burp Suite
* **Penetration testing tools:** Kali Linux, Metasploit Framework

## Secure Environments

* **Configuration management tools:** Ansible, Chef, Puppet
* **Infrastructure security tools:** Qualys Vulnerability Management Platform, Azure Security Center, AWS Security Hub
* **SIEM tools:** Splunk, Elastic Stack (ELK), Sumo Logic

### Tools and Technologies for Security in the Pipeline:

**Pipeline automation:** Jenkins, GitLab CI/CD, Azure DevOps Pipelines

* **Source code security:** Snyk, WhiteSource, Dependency Track
* **Automated code testing:** DAST tools mentioned above, OWASP ZAP
* **Dependency management:** Nexus Repository Manager, Artifactory
* **CI/CD security tools:** Aqua Security Cloud Native Security Platform, Prisma Cloud

### Tools and Technologies for Defending the Pipeline:

* **Multi-factor authentication (MFA):** Google Authenticator, Duo Security
* **Identity and Access Management (IAM):** Okta, Azure Active Directory, AWS Identity and Access Management (IAM)
* **Secret management tools:** HashiCorp Vault, AWS Secrets Manager, Azure Key Vault
* **Log management and SIEM tools:** Mentioned above

### Tools and Technologies for Infrastructure as Code (IaC):

* **IaC tools:** Terraform, Ansible, Chef, Puppet
* **Cloud DevOps platforms:** AWS CloudFormation, Azure Resource Manager, Google Cloud Deployment Manager
* **Secret management tools:** Mentioned above
* **IaC vulnerability scanning tools:** Terraform Security, Snyk IaC, CloudSploit

### Dev vs. DevSecOps: Fostering Collaboration and Security

**DevOps** and **DevSecOps** are both methodologies that aim to improve software development and delivery. However, they focus on different aspects of the process:

* **DevOps:** Focuses on **collaboration, automation, and communication** between development (Dev) and operations (Ops) teams. Its goal is to shorten the development lifecycle and deliver features faster and more reliably.
  * Tools and Techniques: CI/CD pipelines, containerization (Docker), infrastructure as code (Terraform), configuration management (Ansible)
* **DevSecOps:** Extends DevOps by integrating **security practices** throughout the entire software development lifecycle (SDLC). It aims to build security in from the beginning, preventing vulnerabilities and ensuring secure software delivery.
  * DevSecOps builds upon DevOps practices and adds security elements:
    * Security testing tools (static code analysis, DAST)
    * Secure coding practices and training
    * Secret management and access control
    * Vulnerability scanning for infrastructure

**Here's an analogy:** Imagine building a house.

* **DevOps** streamlines the process by ensuring the construction crew (Dev) and the painters/electricians (Ops) work together efficiently. Communication is clear, materials are readily available, and the house is built quickly.
* **DevSecOps** adds a security inspector to the team. The inspector ensures the foundation is strong, the electrical wiring is safe, and there are no fire hazards. Security is considered throughout the building process, not just as an afterthought.

### Waterfall vs. Agile: Traditional vs. Iterative Development

**Waterfall** and **Agile** are two different project management methodologies used in software development.

* **Waterfall:** This is a **sequential** approach where each stage of development (planning, design, development, testing, deployment) is completed before moving on to the next. It's rigid and requires clear upfront requirements.
  * Advantages:
    * Clear roadmap, easy to track progress
    * Suitable for well-defined projects with stable requirements
  * Disadvantages:
    * Slow to adapt to changes
    * High risk of late-stage defects due to inflexible structure
* **Agile:** This is an **iterative** approach where development happens in short cycles (sprints) with continuous feedback and adaptation. Requirements are continuously refined throughout the process.
  * Advantages:
    * More flexible and adaptable to changing requirements
    * Faster feedback loop, allowing for earlier bug detection
  * Disadvantages:
    * Can be challenging for large projects or those with strict deadlines
    * Requires strong communication and collaboration within the team

## Choosing the right approach depends on the project's nature

* **Waterfall** might be suitable for projects with well-defined requirements that are unlikely to change significantly.
* **Agile** is a better fit for projects with evolving requirements or where user feedback is crucial for shaping the final product.

**DevOps and Agile often go hand-in-hand.** Both methodologies emphasize collaboration, continuous improvement, and rapid delivery. DevSecOps integrates security practices seamlessly into an Agile workflow, ensuring secure software development throughout short, iterative cycles.

### The DevOps Lifecycle: Streamlining Software Delivery

The DevOps lifecycle is a continuous loop that automates and integrates the processes involved in software development, testing, deployment, and monitoring. It emphasizes collaboration and communication between development and operations teams to deliver features faster and more reliably.

Here's a breakdown of key aspects within the DevOps lifecycle:

1. **Continuous Integration (CI):**
   * Developers frequently commit their code changes to a shared repository (like Git).
   * Automated builds and tests are triggered upon each commit, identifying bugs early in the development cycle.
   * Tools: Jenkins, GitLab CI/CD, Azure Pipelines
2. **Continuous Delivery/Continuous Deployment (CD):**
   * CI pipelines ensure code is always in a deployable state.
   * CD automates the deployment process to various environments (development, testing, production).
   * There are two approaches:
     * **Continuous Delivery (CD):** Automatically deploys code changes to a staging environment for manual review before pushing to production.
     * **Continuous Deployment (Continuous Delivery with Automatic Deployment):** Automatically deploys approved code changes directly to production.
   * Tools: Similar to CI tools, some offer built-in CD functionality. Additionally, tools like Spinnaker and ArgoCD are specifically designed for CD.
3. **Infrastructure as Code (IaC):**
   * Infrastructure (servers, networks, etc.) is defined as code (e.g., Terraform, Ansible). This allows for:
     * **Automation:** Infrastructure provisioning and configuration are automated, reducing human error and inconsistency.
     * **Repeatability:** Infrastructure can be easily recreated or scaled based on code.
     * **Version Control:** IaC code can be version controlled like any other code, allowing for rollback if needed.
4. **Configuration Management:**
   * Tools (Ansible, Chef, Puppet) automate the configuration of servers and applications, ensuring consistency across environments.
   * This eliminates manual configuration errors and simplifies management.
5. **Orchestration:**
   * Orchestration tools (Kubernetes, Docker Swarm) manage the deployment and scaling of containerized applications.
   * They automate tasks like:
     * Starting and stopping containers
     * Scaling applications based on demand
     * Load balancing traffic across containers
6. **Monitoring:**
   * Applications and infrastructure are continuously monitored for performance, errors, and security threats.
   * Tools (Prometheus, Grafana, Datadog) provide real-time insights and alerts for potential issues.
   * Monitoring allows for proactive problem identification and faster resolution.
7. **Microservices:**
   * Applications are broken down into smaller, independent services with well-defined APIs.
   * This enables:
     * **Faster Development and Deployment:** Smaller services can be developed and deployed independently.
     * **Scalability:** Individual services can be scaled independently based on their needs.
     * **Resilience:** Failure in one service doesn't necessarily impact the entire application.

**Microservices and containerization (using Docker) often go hand-in-hand with DevOps.** They promote modularity and independent deployments, making the overall system more flexible and scalable.

By implementing these practices, DevOps fosters a culture of collaboration and automation, leading to faster and more reliable software delivery with improved quality and security.

### Shift Left: Catching Issues Early in the Development Lifecycle

**Shift left** is a philosophy in software development that emphasizes **identifying and addressing potential problems earlier** in the development lifecycle (SDLC). Traditionally, many security and quality checks occurred later in the process, closer to deployment. Shift left aims to move these activities "left" on the timeline, ideally catching issues before they become costly bugs or security vulnerabilities.

Here's why shifting left is important:

* **Earlier detection:** Catching issues early is cheaper and easier to fix than waiting until later stages.
* **Improved quality:** By addressing issues early, you deliver higher-quality software with fewer bugs.
* **Faster delivery:** Fixing issues early avoids delays caused by rework and late-stage bug fixes.
* **Enhanced security:** Integrating security practices from the beginning reduces the risk of vulnerabilities.

Here are some ways to implement a shift left approach:

* **Security testing:** Perform static code analysis, unit testing, and other security checks early and throughout the development process.
* **Threat modeling:** Identify potential security risks early in the design phase.
* **Infrastructure as Code (IaC):** Automating infrastructure provisioning ensures consistent and secure configurations from the start.
* **Code reviews:** Encourage frequent code reviews to catch potential issues early.
* **DevOps:** By automating and integrating development and operations activities, security best practices are woven into the entire workflow.

Here are some specific examples of how shifting left can be applied:

* **Security:** Shifting left could involve using tools to scan code for vulnerabilities during development, rather than waiting for a dedicated security testing phase.
* **Quality:** Developers could write unit tests as they code, ensuring functionality is working correctly as they go.
* **Performance:** Tools could be used to analyze code for potential performance bottlenecks during development, allowing for early optimization.

## Benefits of Shift Left

* Reduced costs from fixing bugs later in the development cycle.
* Increased software quality and reliability.
* Faster time to market by catching issues early and avoiding delays.
* Improved security posture by integrating security practices throughout development.

## Challenges of Shift Left

* Requires a cultural shift within development teams, potentially requiring training and adoption of new tools and processes.
* May require upfront investment in tools and training.

Reference:

<https://www.appknox.com/blog/history-of-devops>

## In this section

* ✅ [Static Application Security Testing (SAST)](static-application-security-testing-sast/README.md) · 4/5 pages written
* ✅ [Interactive Application Security Testing (IAST)](interactive-application-security-testing-iast.md)
* ✅ [Dynamic Application Security Testing (DAST)](dynamic-application-security-testing-dast.md)
* 🚧 [SCA](sca.md)
* ✅ [Wazuh SIEM and XDR](wazuh-siem-and-xdr/README.md) · 3/3 pages written
* ✅ [DevSecOps](devsecops.md)
