# Azure Security

* Cloud Shared Security Responsibility Model
  * Few controls need to focus
    * Physical Security
    * Host Security/client/end point protection
    * Network controls
    * Application Security controls
    * Identity and Access Management
    * Data Classification
* Azure Subscription
  * How many subscriptions we have now ?
* Azure Tenants
  * Tenant ID
* \*\*\* Azure AD might have collection of subscriptions based on the cloud services onboarded
* Cloud based Identity and Access management service
* Azure Active Directory :
* Azure AD Rest API calls on port 80,443
* Authentication and Authorization protocol's :
* AML, WS-Federation, OpenID Connect, Oauth, SAML 2.0  over HTTPS/HTTP
* Kerberos, which is used by on-premises AD.
* Uses federation services, ADFS
* Azure AD helps,
* authentication with SaaS
* Applications hosted on Azure
* Authentication management, cloud and on prem applications
* Traditional AD :
* LDAP (389) and LDAPs (686)
* Uses kerberos for authentication
* User and Groups on organization units and group policy objects
* Service principles
* External Users UPN's
  * Need regular audit
* Custom domain on Azure\
  DNS configuration
* Azure AD Licensing and what features we have
  * Identity Protection
  * Privileged Identity Management
  * Azure AD Identity Security
* Azure Groups
  * Security groups
  * MS 365 groups
* Azure AD roles : access to azure AD
* Azure AD RBAC roles  : access to Azure resources
* Application Registration on Azure
* Azure AD Connect : synchronization of on prem AD to cloud AD
* Domain Join
* Attack scenarios:
  * Compromised credentials
  * Azure AD authentication brute force
* Logs:
  * Azure AD auth on 443, 80
  * AD on LDAP 389, 686
  * Azure AD Modern authentication protocols
  * Monitoring GPO changes
  * Kerberos authentication activity
    * UDP 88
    * TCP 88
    * TCP 2105
    * TCP 544
    * TCP 1 -1023
    * TCP 32000-65535
  * NTLM authentication activity
  * Azure AD Built in roles review
* Reference:
* <https://learn.microsoft.com/en-us/azure/security/fundamentals/>
* <https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/>
* <https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/>
