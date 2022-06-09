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

Design systems that works consistently and recover quickly

* Recover from failure automatically
* Reduce idle resources
* Scale horizontally for resilience
* Manage change through automation
* Test recovery procedures

### Performance Efficiency

Effective use of computing resources to meet system and business requirements while removing bottlenecks

* Use serverless architectures first
* Use multi-region deployments
* Delegate tasks to a cloud vendor
* Experiment with virtual resources

### Cost Optimizations

Delivering optimum and resilient solutions at the least cost to the user

* Utilize consumption-based pricing
* Implement cloud Financial Management
* Measure overall efficiency
* Pay only for resources your applications requires


## IAM

Control access to your AWS services and resources

* Secure your cloud resources
* You define who has access
* You define what they can do
* A free global service

### Identities VS Access

* Identities: who can access your resources
    * Root user
    * Individual users
    * Groups
    * Roles
* Access: what resources they can access
    * Policies
    * AWS managed policies
    * Customer managed policies
    * Permissions boundaries

### Authentication VS Authorization

* Authentication: who?
    * Where you present your identity and provide verification

* Authorization: what?
    * Determines wchich services and resources the authenticated identity has access to

## IAM users, groups

* Users: Users are **entities** you create in **IAM** to represent **person** or **application** needing to access your **AWS resources**

* Groups: collection of **IAM users** that helps you apply common access controls to all group members


## Understanding IAM Permissions

* Roles: define access permissions and are temporarily assumed by an IAM user or service

    * You assume a role to perform a task in a single session
    * Assumed by any user or service that needs it
    * Access is assigned using policies
    * You grant users in one AWS account access to resources in another AWs account

* Policies: you manage permissions for IAM users, groups, and roles by creating a policy document in **JSON** format and attaching it


### Best practices

1. Enable MFA for priviliged users (root and administrative)
2. Implement strong password policies
3. Create individual users instead of using root
4. Use roles for EC2 instances


### IAM Credential Report

Lists all users in your account and the status of thier various credentials


## Application Security services

Software based security tools available to help you **monitor** and **protect** your resources

**Firewalls**: prevent unauthorized access to your networks by inpsecting incoming and outgoing traffic against security rules you've defined

* WAF (Web Application Firewall)
    * Helps protecting your web applications against common web attacks / common attack patterns
        * SQL injection
        * Cross-site scripting

**DDoS (Distributed Denial of Services)**: A DDoS attack causes a traffic jam on a website or web application in an attempt to cause it to crash

* Shield
    * Is a managed DDoS protection service
        * *Always-on* detection
        * Shield standard is **free**
            * Provides **free** protection against common and frequently occurring attacks
        * Shield advanced
            * Provides enhanced protections and 24/7 access to AWS experrts for a **free**
            * Supported on..
                * CloudFront
                * Route 53
                * ELB
                * AWS Global Accelerator

* Macie
    * Discover and protct sensitive data
        * Uses machine learning
        * Evalutes S3 environment
        * Uncoverss PII


* Config
    * Allows you to assess, audit, and evaluate the configuration of your resources.
        * Track configuration changes over the time
        * Delivers configuration history file to S3
        * Notificactions vis SNS of every configuration change.

* GuardDuty
    * Threath detection system that uncovers unauthorized behavior
        * Built-in detection for EC2, S3, and IAM
        * Reviews CloudTrail, VPC Flow Logs, and DNS logs

* Inspector
    * Works with EC2 instances to uncover and report vulnerabilities
        * Agent installed on EC2 instance
        * Report vulnerabilities found
        * Checks access from the internet, remote root login, vulnerable software versions

* Artifact
    * Offers on-demand access to AWS security and compliance reports
        * Central repository for compliance reports from third-party auditors
            * Service Organization Controls (SOC) reports
            * Payment Card Industry (PCI) reports

* Cognito
    * Helps you control access to mobile and web applications
    * Provides authentication and authorization


## Utilizing Data Encryption and Secrets Management Services

Data encryption **encode** data so it cannot be read by unauthorized users

### Data in flight vs at rest

* Data in flight; data that is **moving** from one location to another
* Data at rest; data that is **inactive** or stored for **later use**

## Services

* Key Management Service (KMS)
    * Allows you to generate and store encryption keys
        * Key generator
        * Store and control keys
        * AWS manages encryption keys
        * Automatically enabled for certain services

* CloudHSM (Cloud Hardware Security Module)
    * Hardware security module used to generate encryption keys
        * Dedicated hardware for security
        * Generate and manage your **own** encryption keys
        * AWS does **not** access to your keys

* Secrets Manager
    * Allows you to manage and retrive **secrets** (passwords or keys)
        * Rotate, manage, and retrieve secrets
        * Encrypt secrets at rest
        
