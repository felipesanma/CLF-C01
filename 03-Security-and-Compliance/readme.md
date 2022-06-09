# Security

## Shared Responsability Model

AWS responsability

* Security **of** the cloud
    * Regions, edge locations, and AZs
    * Control access to its data centers
    * Maintains networking components (UPS, generators, CRAC units)
* Any managed services
    * RDS, S3, ECS, Lambda

Your responsability

* Security **in** the cloud
* **How** the services are implemented and managing your application data
* Security configuration
    * Securing your account and API calls
    * Rotating credentials
    * Restricting internet access from your VPCs
* Patching
    * Guest operating system (OS) on your EC2 instances, wchich includes updates and security patches
* Identity and Access Management
* Network Traffic
    * Network Traffic protection, wchich includes security group **firewall** configuration
* Installed Software
    * Your application code, installed software. You should frquently scan for and patch vulnerabilities in your code

### Report abuse of AWS resources

Contact the **AWS Trust & Safety** team using the *Report Amazon AWS abuse* form or by contacting **abuse@amazonaws.com**


## Well-Architected Framework

5 pillars describe design principles and best practices for running workloads in the cloud

### Operational Excellence

Create applications that effectively support production workloads

* Plan for and anticipate failure
* Deploy smaller, reversible changes
* Script operations as code
* Learn from failure and refine

### Security

Putting mechanisms in place that help protect your systems and data

* Automate security tasks
* Encrypt data in transit and at rest (use KMS)
* Assing onlye the least privileges required
* Track who did what and when
* Ensure security at all application layers

### Reliability



### Performance Efficiency



### Cost Optimizations


