# AWS Core Services
* Compute
* Storage
* Database
* Network and content delivery
* Management tools 

## Compute Services

**Elastic Compute Cloud (EC2):** Virtual Server running on AWS, configurable by number of virtual CPUs, GBs of RAM, size/type of storage, and network speed. You only pay for what you use and when you use it, scalable

**Elastic Beanstalk:** Deploy and scale web applications by uploading code, services deployed using Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker. It automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring. There is no additional charge for Elastic Beanstalk - you pay only for the AWS resources needed to store and run your applications

**Elastic Load Balancing:** Distributes incoming traffic across multiple replicated servers so one single server is not overloaded, fault-tolerant, scalable, secure, and monitor the health of servers

**Lambda:** Run serverless code (lambda function) in response to an event, automatically runs uploaded code and scales applications, and pay only for the compute time you consume and each event trigger

**Lightsail:** Preconfigured virtul servers, and ready-to-use OS, web applications, and development stacks, scalable with your project's growth, cost-effective monthly fees, one-click-to-launch services

**Availability Zones:** Data Centers around the world, independent of each other in network and power, almost 6 dozen AZs around the world

**Regions:** Made up of two or more AZs, currently two dozen regions around the world

**High Availability:** 

- High available resources may have duplicate copies in multiple AZs or even Regions
- Resiliency: Ability to provide uninterrupted performance, even during natural disasters
- Redundancy: Having multiple copies of the data in different data centers
- Architect your AWS Cloud Infrastructure to protect against downtimes cause by natural disasters or power outages


## Storage
**Simple Storage Service (S3):** Object storage service, storing each file as separate entity (object), high availability, security, and performance, scalable, charged only for what you used

**Elastic Block Store (EBS):** External hard drive, block storage service, raw, unformatted block device attached to an EC2 instance, can add multiple EBS volumes to one EC2 instance, available as a file system or hard drive, dynamically change configurations to attached volumes via the AWS Console, automatically replicated within its Availability Zones, very similar to a zip file

**Snowball:** Data migration tool, hardware solution, AWS will physically ship you a Snowball to move your data onto and ship back, no transfer fee, only pay for S3 storage

**Storage Gateway:** Hybrid cloud storage with local caching. A 'gate' that connects your onsite users and devices to resources stored in the AWS Cloud with minimal latency
- **File Gateway:** An asynchronous configuration of the AWS Storage Gateway service that provides your applications a file interface to seamlessly store files as objects in Amazon S3, and access them using industry standard file protocols. Local cache to provide low-latency access to recently accessed files
- **Volume Gateway:** Upload files in blocks (like virtual hard drives), asynchronous backed up as point-in-time snapshots and stored as Elastic Block Store snapshots
                
     - **Stored volume:** complete copy on-premise; sends snapshots to AWS
     
     - **Cached volume:** keep most recently accessed data on-premises; complete copy on AWS

- **Tape Gateway:** Uses existing tape-based backup infrastructure to back up to virtual tapes, data stored locally then asynchronous uploaded to S3, data can be archived using Amazon Glacier.

## Database
**DynamoDB:** NoSQL database, secure, scalable, serverless, no need to provision, manage, or update your own servers, automatically scales.

**Relational Database Service (RDS):** Relational database, AWS takes care of the provisioning, monitoring, and maintaining of the database. Note: Existing database can be migrated using AWS Database Migration Service. Compatible with:
* PostgreSQL
* MariaDB
* Oracle Database
* Microsoft SQL Server
* Amazon Aurora
* MySQL

**Amazon Aurora:** Fully managed by RDS; no administration or provisioning necessary, relational databse, MySQL, and PostgreSQL compatible, no servers to provision or manage.

**Amazon Redshift:** The most popular and fastest cloud data warehouse. Fully managed, petabyte-scale data warehouse service, fast, cheap stores extremely large amounts of data collected from a wide ranges of source to analyze.


|Nonrelational Database (NoSQL)| Relational Database | 
|------------------------------|---------------------|
| DynamoDB                     | Amazon RDS          |  
|                              | Amazon Aurora       |  


## Network and Content Delivery
**Virtual Private Cloud (VPC):** Logically isolated sections in the cloud to provision resources, flexible, secure, allowing you to control almost every aspect of your virtual network, VPC automatically provisioned at AWS account signup.

**CloudFront:** Is a content delivery network (CDN), based on location of the user, origin of the website/application, location of the content delivery server, integrates with many AWS services to provide optimal performance and security. Makes loading websites/apps for end users faster using edge locations to cache files and resources. 

*Note: A user is able to retrieve data faster through an Edge Location*

|User                                          |Edge Locations                                  |Origin    | 
|----------------------------------------------|------------------------------------------------|----------|
|Download content from closest edge location   |Data center                                     |S3        |   
|Faster download than going to origin server   |Caching of data                                 |EC2       |  
|                                              |Downloads content for certain period of time    |ELB       | 

**Route 53:** Highly scalable cloud Domain Name System (DNS), reliably and cost-effectively route end users to your internet applications, connect user requests to infrastructure running on AWS, route users to infrastructure outside of AWS and DNS service. Integrates with other AWS services, simple to set up, fast, secure, cost-effective, automatically scales to handle large query volumes. It's basic functions are:
 * Domain Registration
 * DNS
 * Health check of web apps
 * Auto Naming for service discovery
 * Create websites/apps with high availability


## Management Tools
**CloudFormation:** Are templates/recipes for resource deployment in AWS, provision and deploy fully configured infrastructure, and they're free to use, you only pay for resources used in the templates. Provision multi-region, multi-tier application quickly with a text file written in JSON/YAML. Update or manage the templates (stacks) using AWS Management Console, CLI, or Software Development Kit (SDK).

**Infrastructure as Code:** Deploy IT infrastructure based on text file that specifies resources and configurations for each servvice being deployed. 

**CloudTrail:** Monitoring and auditing of IT infrastructure for compliance, user activity/API usage tracking, and risk auditing. Log and monitor account activities and event history. Simplify compliance audits. Discover/troubleshoot security and operational issues. Provide visibility into user/resource activities, automatically respond to security threats. Track actions taken through AWS Management Console, SDKs, and CLI tools. Review logs using CloudTrail event history, and deliver reports to S3 buckets or CloudWatch logs and events. Logging of data events has small fees. 

**CloudWatch:** Monitoring and management system for AWS infrastructure, negatively integrated with over 70 AWS services, gain system-wide visibility into resource utilization, application performance, and operational health. Get notifications in real time on data, metrics, and events. 


|CloudTrail   | CloudWatch           | 
|-------------|----------------------|
| Audits logs | Monitors             |  
|             | Can react to changes |  
