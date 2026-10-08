# Security Baselines

* Asset pre hardening
  * Group policy Objects (GPO's)
  * Mobile Device Management )(MDM)
* Regulatory compliance
  * Sarbanes-Oxley Act (SOX)
  * Health Insurance Portability and Accountability Act (HIPAA)
  * Federal Information Security Management Act (FISMA)
  * Payment Card Industry Data Security Standard (PCI DSS)
  * General Data Protection Regulation (GDPR)
  * California Consumer Privacy Act (CCPA)
  * Gramm Leach Bliley Act (GLBA)
* Baselining
  * Network devices (switches, routers, firewalls, and so on)
  * Windows systems: servers and clients
  * Linux/Unix systems
  * Storage/file servers
  * Database servers
  * Web servers
  * Application servers
  * Operational Technology (OT)
  * Internet of Things (IoT).
* Windows environment baselining
* For Windows Server:
* Windows Domain Controller (DC) Server,
* Windows Server Internet Information Services (IIS),
* Windows SQL Database Server,
* Windows DNS Server,
* Windows Remote Desktop Services
* For a Windows client:
* Windows standard client (user workstation)
* Privileged Access Workstation (PAW)
* Windows virtual client
* OT
* IoT clients
*  Some examples of policies may include acceptable use policy, change management policy, disaster recovery policy, privacy policy, information security program policy
  * Security updates
  * Encryption
  * Firewall
  * Password policy, Multi-Factor Authentication (MFA), and biometrics
  * Local administrative access strategy
  * Security protection tools and antivirus
  * Compliance and protection policies
  * Data loss prevention and information protection
* Few of the windows standards
  * All Windows workstations will be configured using Windows Update for Business and Windows servers using WSUS or Azure Update Management. Update schedules will be defined and documented by business use case.
  * All Windows servers and end-user workstations will be encrypted using BitLocker and/or Azure Disk Encryption.
  * A Windows firewall will be enabled and configured on all Windows end-user devices and servers. Connection rules will be documented.
  * A PIN and biometrics with Windows Hello must be used, and accounts will be required to use a password with a minimum of 12 characters. Passwords must contain a lower case, upper case, numerical, and special character and are required to be changed annually.
  * MFA will be required for all users accessing the corporate environment and resources.
  * There will be no standard user accounts assigned with local admin access on any Windows device.
  * All Windows end-user devices and servers will be enabled with Microsoft Defender for Endpoint.
  * Compliance policies for conditions such as device risk and minimum OS version will be assigned and enforced with Conditional Access on Windows devices.
  * Unified labeling with data loss prevention and information protection will be deployed to all Windows end-user devices.
* Security Frameworks
  * Control Objectives for Information and Related Technology (COBIT): <https://www.isaca.org/resources/cobit>
  * International Standards Organization 27000 Family (ISO): <https://www.iso.org/isoiec-27001-information-security.html>
  * National Institute of Standards and Technology (NIST) Framework for Improving Critical Infrastructure Cybersecurity, also known as the NIST Cybersecurity Framework: <https://www.nist.gov/cyberframework>
  * NIST SP 800-53: Security and Privacy Controls for Federal Information Systems and Organizations: <https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final>
  * NIST SP 800-171: Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations: <https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final>
  * Health Information Trust Alliance Common Security Framework (HITRUST CSF): <https://hitrustalliance.net/hitrust-csf/>
* <https://www.nist.gov/cyberframework/online-learning/five-functions>
* <https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.04162018.pdf>
* <https://www.nintex.com/process-automation/process-mapping/>
