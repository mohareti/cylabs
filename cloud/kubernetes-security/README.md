# Kubernetes Security

* Kubernetes Architecture
* Kubernetes Attack Surface
  * Control Plane
    * etcd
    * master nodes
* Kubernetes Secure Configurations
  * Public traffic to cluster is proxied through load balancer
  * Cluster RBAC
* Kubernetes Threat Model
* Tools
  * Penetration Testing tool : <https://github.com/inguardians/peirates>
  * Trivy Vulnerability scanner : <https://github.com/aquasecurity/trivy>
  * Deepce : Docker Enumeration <https://github.com/stealthcopter/deepce>
* Attack Paths
  * subdomain enumeration -> S3 bucket scan
  * Web application exploitation -> api call exploitation -> RCE ->SSRF -> access to pods
    * Ex: java struts running on internet facing pod (CVE-2017-5638)
  * Nuclei templates -> subdomains/api's

References:

1. <https://www.gitops.tech/>
2. <https://control-plane.io/posts/hardening-git-for-gitops/>
3. <https://www.aquasec.com/blog/kubernetes-vulnerability-security-threat/>
4. <https://www.microsoft.com/en-us/security/blog/2021/03/23/secure-containerized-environments-with-updated-threat-matrix-for-kubernetes/>
5. <https://attack.mitre.org/matrices/enterprise/containers/>
6. <https://github.com/OWASP/Docker-Security/blob/main/dist/owasp-docker-security.pdf>
7. <https://research.nccgroup.com/2017/11/23/kubernetes-security-consider-your-threat-model/>

## In this section

* ✅ [AKS Security](aks-security.md)
* 🚧 [kube-hunter](kube-hunter.md)
* 🚧 [Kubescape](kubescape.md)
