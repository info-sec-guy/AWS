# Security in the Cloud :closed_lock_with_key:

**AWS Shared Responsibility Model:** Amazon Web Services (AWS) is responsible for security __of__ the cloud (AWS), that includes physical security of data centers, hardware, software, and networking. Customers are responsible for security __in__ the Cloud, protecting customer data, data encryption, Identity and Access Management (IAM), patching operating systems of virtual machines(VMs), and configuring firewalls.

**The 5 Pillars of the AWS Well-Architected Framework (CROPS):**
1. Cost Optimization
2. Reliability
3. Operational Excellence
4. Performance Efficiency
5. Security

**Security Pillar:** 
- **Identity and Access Management (IAM):** Actively manage all-users and enforce least privilege. 
- **Detective Controls:** Enable traceability to determine *'who did what and when'*, actively monitor alerts, and audit actions and changes to an environment in real time. 
- **Infrastructure Protection:** Apply security on all layers of the infrastructure. For example, a virtual server would require multiple layers like subnet, load balancer, and the operating system. Security best practices should be automated to save time and money when scaling.  
- **Incident Response:** Intervene, invetigate, and deal with all security events. Once the issue is resolved, update the incident management process, and continue to learn from the past mistakes and security events. 

**Least Privilege in AWS:** Use IAM to govern access, access can be granted to users, resources, and other AWS services. Determine what type of access a user needs in order to accomplish his work and craft policies to perform only those specific tasks.

**AWS Compliance Programs:** The [AWS Compliance Program](https://aws.amazon.com/compliance/programs/) helps customers to understand the robust controls in place at AWS to maintain security and compliance in the cloud. By tying together governance-focused, audit-friendly service features with applicable compliance or audit standards, AWS Compliance Enablers build on traditional programs, helping customers to establish and operate in an AWS security control environment.

**Recommended Security Practices:** 
1. Shared Responsibility Model
2. Security Pillar of Well-Architected Framework
3. Least Privilege

**Secutiy Services**
- **IAM:** Permissions are global and any access setting will be true accross all regions. 

- **Manage Users:** Create users in IAM and assign them security credentials, set very precise permissions, user access available through the AWS Management Console. Programmatic access is done through applications directly accessing resources instead of human interaction needed.  

- **Manage IAM Roles:** Create roles to manage permissions and accessability. An entity assumes a role to obtain temporary security credentials to make API calls to your resources. 

- **Manage Federated Users:** Use an identity management solution using SAML 2.0 or an AWS federation to enable single sign-on (SSO) to your AWS accounts. 

**AWS WAF :warning::** Layer 8 security that protects web applications running on AWS Cloud from common web exploits, firewall service for web applications, web traffic visibility, cost-effective, protects against web attacks, easy to deploy and maintain. 

**AWS Shield :shield::** Provides detection and automatic mitigations for layers 3 and 4, minimizes effects of DDoS attacks to your apps, helps minimize app downtime and latency when an attack happens. There are two tiers of AWS Shield - `Standard` and `Advanced`.
- **Standard:** Enabled by defatult for free, protects web apps against majority of common DDoS attacks, great when you combine with CloudFront and Route 53.
- **Advanced:** Continous 24/7 access to AWS DDoS Response Team, real-time visibility into events, integrates with AWS WAF, higher-level protection, automated app traffic monitoring, financial protections against DDoS-related spikes in changes for EC2, Elastic Load Balancers, CloudFront, and Route 53. Available globally on all CloudFront and Route 53 Edge locations. 

**AWS Inspector :mag::** Automated security assessment service to help improve security and compliance of applications deployed on AWS. Automatically assess for exposure, vulnerabilities, and derivations from best practices and standards, generates detailed reports to help check for vulnerabilities, security teams can access validating that tests were performed. Identify application security issues, integrate security into DevOps, and increase development agility. 

**AWS Trusted Advisor :credit_card::** Reduce costs, increase performance, and improve security. Guides provisioning and recommendations of resources to follow AWS best practices, scans your infrastructure and advises you on *'how it is or is not'* following AWS best practices. Based on five categories; `Cost Optimization`, `Performance`, `Security`, `Fault Tolerance`, and `Service Limits`.  

**AWS GuardDuty :guardsman::** Protect your AWS accounts, workloads, and data with intelligent threat detection and continous monitoring. 24/7 threat detection service, easy to deploy, analyzes events to send actionable alerts via CloudWatch, and uses machine learning, anomaly detection, and integrated threat intelligence to identify potential threats. 
