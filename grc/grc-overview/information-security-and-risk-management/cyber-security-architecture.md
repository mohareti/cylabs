---
description: "Primary Objective: Maintaining and conducting business operations in a secure environment."
---

# Cyber Security Architecture

Primary Objective: Maintaining and conducting business operations in a secure environment.

* Organization: what are business needs
* Information: which are critical for business

Cyber Security Architecting:

* help you to translate organization's strategic requirements into actionable improvements in securing most valuable assets.

* Review and implement wide range of InfoSec paradigms
* including the foundations of risk management
* implementing processes and controls
* designing information systems securely
* managing the day-to-day activities required to ensure security is maintained in organization.

Security Model: CIA Triad

* Confidentiality
  * Which security control we in placed to achieve this
    * Data encryption : data at rest
    * Hashing : data in transit (file integrity monitoring)
      * Sha 256
      * Sha 512
    * MFA (IAM and user access)
      * Privilege Access Management
      * Password rotations and policies
      * Secret Management
    * Physical Security
    * Default deny for critical data and infrastructure
      * Documented approval from leadership
      * Proper auditing/activity log management
* Integrity
  * Encryption policies to achieve integrity when data at rest
  * Hashing policies to achieve integrity when data at transit
* Availability
  * High availability of services or access to data.
    * What is org Disaster Recovery Plan?
    * What is org Business Continuity Plan?
    * Fail over clustering
    * Site reliability
    * Site resiliency
    * Automatic failover
    * Load balancing
    * Redundant components of software and hardware
      * Cold, hot and warm sites

AAA

Cyber Security Framework : NIST

* What is our organization mission and vision
* what are security objectives and goals
* What are Critical Business Assets and Operations
* Inspire and  align with the security framework which closely tie with organization mission and objective

Keywords

* Risk
* Assets
* Threats
* Vulnerabilities
* Likelihood
* Impact
* Information security risk
* Security event
* Risk  scores
* Risk Assessment : to determine the impact of threat exploiting a vulnerability
* Risk Management : identify, evaluate, prioritize risks, developing mitigating controls, provide transparency and accountability

* Risk Appetite
* Risk Treatment
* Risk Acceptance
* Risk Transfer
* Risk reduction
* Risk Avoidance
* Residual risk

How many security events happened last year

How much risk associated with it

What is our organization risk score

Information security risk management vs cyber security risk management

Which asset inventory we are using

How accurate it is

How often it get updated

Asset

* Types of Assets
  * Physical
  * Digital
  * Non reputational assets
* Asset Owners
* Asset Classification
* Asset Name
* Asset IP range
* Asset Description
* Asset Notes

Asset Discovery

Asset Inventory

Asset Register

List to collect

* All windows servers managed by SCCM team
* All Linux Servers managed by SCCM team
* All windows desktops managed by SCCM team
* All Linux desktops managed by SCCM team
* Board approved software applications
* All Network Equipment
  * Routers
  * Switches
  * WAF
  * Load Balancers
  * Wi-Fi Assess points
  * Network Security control applications and solutions
* Domain Names
* IP ranges
* Virtual Instances
* Data backups
* Patch Management servers
* Active Directory
* Domain controllers
* DNS servers
* FTP servers
* Application servers
* Database servers
* Network Attached Storage

What are our Threats and Threat Actors

* Malicious outsiders
  * Script kiddies
  * Group actors
  * State sponsored actors
* Malicious insiders
* Accidental insiders
* Environmental threats

How to perform basic risk assessment to implement an Information Security Management System

How to mitigate the risks

What legal regulations Organization need to follow

How cyber security incident investigations run

How organization compliance structure

Which compliance management tool we are using

How to monitor compliance posture

What is our compliance landscape

What are the compliance requirements

What is our threat landscape

What is our compliance risk

What and which audit requirements need for organization

Which security questionnaires we follow and who are responsible

Do we manage/process

* Personally Identifiable Information (PII)
* Protected Health Information (PHI)

Which privacy regulations we need to follow

* GDPR
* COPPA
* HIPPA
* CCPA

Compliance

* PCI DSS
* SOX
* FISMA

Standards to follow

* ISO 27001
* ISO 27018

Information Security policies

Information security procedures

Information security playbooks

Maintain security awareness program

Managing threat party risks

Shared Responsibility Models

* Cloud Service Provider
* SaaS
* PaaS
* IaaS
* Source code repositories
* Accounting
* HR
* DLP
* SIEM

What are service level agreements

Vendor security assessment questionnaire

<https://opensource.google/projects/vsaq>

How we are implementing Defense in depth

How we are implementing Zero Trust

What's our risk management and governance approach

Information Security Policies Training at the time of onboarding

Social Engineering attacks training

* Do they properly advertising

On Boarding

* User account creation
* IAM policies review
* Level of Assess and permissions review
* Asset Allocation
* Badging permissions review
* Security Awareness Training
* CMDB : user and asset information
* How to block safeguard the asset if we lose it, Remote access of the asset in case of loss ?
* DLP Data Loss Prevention Policies ?
* Removeable media use case policies ?
