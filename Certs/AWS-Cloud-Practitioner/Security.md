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
