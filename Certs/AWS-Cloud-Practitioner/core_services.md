# AWS Core Services

## Compute Services

**Elastic Compute Cloud (EC2):** Virtual Server running on AWS, configurable by number of virtual CPUs, GBs of RAM, size/type of storage, and network speed. You only pay for what you use and when you use it, scalable.

**Elastic Beanstalk:** Deploy and scale web applications by uploading code, services deployed using Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker. It automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring. There is no additional charge for Elastic Beanstalk - you pay only for the AWS resources needed to store and run your applications.

**Elastic Load Balancing:** Distributes incoming traffic across multiple replicated servers so one single server is not overloaded, fault-tolerant, scalable, secure, and monitor the health of servers.

**Lambda:** Run code (lambda function) in response to an event, automatically runs uploaded code and scales applications, and pay only for the compute time you consume and each event trigger. 

**Lightsail:** Preconfigured and ready-to-use OS, web applications, and development stacks, scalable with your project's growth, cost-effective monthly fees, one-click-to-launch services. 

**Availability Zones:** Data Centers around the world, independent of each other in network and power, almost 6 dozen AZs around the world. 

**Regions:** Made up of two or more AZs, currently two dozen regions around the world.

**High Availability:** 

- High available resources may have duplicate copies in multiple AZs or even Regions
- Resiliency: Ability to provide uninterrupted performance, even during natural disasters
- Redundancy: Having multiple copies of the data in different data centers
- Architect your AWS Cloud Infrastructure to protect against downtimes cause by natural disasters or power outages


## Storage
**Simple Storage Service (S3):** Object storage service, storing each file as separate entity (object), high availability, security, and performance, scalable, charged only for what you used.

**Elastic Block Store (EBS):** External hard drive, block storage service, raw, unformatted block device attached to an EC2 instance, can add multiple EBS volumes to one EC2 instance, available as a file system or hard drive, dynamically change configurations to attached volumes via the AWS Console, automatically replicated within its Availability Zones, very similar to a zip file.

**Snowball:** Data migration tool, hardware solution, AWS will physically ship you a Snowball to move your data onto and ship back, no transfer fee, only pay for S3 storage. 

**Storage Gateway:** Hybrid cloud storage with local caching. A 'gate' that connects your onsite users and devices to resources stored in the AWS Cloud with minimal latency. 
- **File Gateway:** An asynchronous configuration of the AWS Storage Gateway service that provides your applications a file interface to seamlessly store files as objects in Amazon S3, and access them using industry standard file protocols. Local cache to provide low-latency access to recently accessed files
- **Volume Gateway:** Upload files in blocks (like virtual hard drives), asynchronous backed up as point-in-time snapshots and stored as Elastic Block Store snapshots. 

    o	**Stored volume:** complete copy on-premise; sends snapshots to AWS
  
    o	**Cached volume:** keep most recently accessed data on-premises; complete copy on AWS




## Database
**DynamoDB:**

**Relational Database Service (RDS):**

**Amazon Aurora:**

**Amazon Redshift:**
