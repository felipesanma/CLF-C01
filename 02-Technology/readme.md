# Technology

## EC2

Elastic Compute Cloud

Rent and manage virtual servers in the cloud -> *elastic compute power*

Let's say you deploy an EC2 instance, how to acces ?

### Methods to Access an EC2 instance

* AWS Managament Console
    * Configure and manage your instance via a web browser
* Secure Shell (SSH)
    * Establish a secure connection to your instance from your local laptop
* EC2 Instance Connect (EIC)
    * EIC allows you to use IAM policies to control SSH access to your instances, removing the need to manage SSH keys
* AWS System Manager
    * Allows you to manage your EC2 instances via a web browser or the AWS CLI

### EC2 Pricing Options

* On-Demand
    * You are billed **down to the second** based on the instance type
    * Use when..
        * Low cost without any upfront payment
        * Unpredictable workloads that **can't** be interrupted
        * Applications under development
        * Workloads will **not** run longer than a year

* Spot
    * Take advantage of **unused** EC2 capacity. Your requested is fulfilled **only** if capacity is available.
    * Use when..
        * Not concerned about the **start** or **stop** time of your application
        * Workloads **can** be interrupted
    * Cheapest option -> save up to 90% off On-Demand prices

* Reserved Instances
    * Allow you to commit to a specific instance type in a particular Region for 1 or 3 **years**
    * Use When..
        * Your application requires a **capacity reservation**
        * You can pay mone **upfront** in order to receive a discount on On-Demand prices.
    * You are required to sign a contract
    * Save up to 75% off On-Demand prices

* Dedicated Hosts
    * Allow you to pay for a physical server that is fully dedicated to running your instances.
    * The server is not shared with other customers
    * Use when..
        * You want to **bring your own** server-bound software **license** (Microsoft or Oracle)
        * You have a regulatory or corporate compliance requirements around tenancy model
    * Save up to 70% off On-Demand prices

* Savings Plan
    * Allows you to commit to compute usage (per hour) for 1 or 3 **years**
    * Use when..
        * Want to lower your bill aceoss multiple compute services
        * Want the flexibility to change compute services, instance types, operating systems or Regions.
    * Save up to 72% off On-demand prices
    * Savings can be shared across various compute services like EC2, Fargate and Lambda.

### Elastic Load Balancing

Automatically distributes your **incoming** application traffic across multiple EC2 instances

* Classic Load Balancers
* Application Load Balancers
* Gateway Load Balancers
* Network Load Balancers

### Auto-Scaling

Adds or replaces EC2 instances automatically across AZs, **based on need and changing demand**


## Server Migration Service (SMS)

Allows you to migrate on-premises server to AWS

* Migrates **on.premises** servers to AWS
* Server saved as a new **Amazon Machine Image** (AMI)
* Use **AMI** to launch servers as **EC2** instances

## Deployment and Infrastructure Management Services

This services help you quickly stand up new applications, automate the management of infrastructure, and provide real-time visibility into system health

### CloudFormation

Allos you to provision AWS resources using Infrastructure as a Code (IaaC)

* Provides a repeatable process fro provisioning resources
* Works with most AWS services
* Create templates for the resources you want to provision

### ElasticBeanstalk

Allows you to deploy your web applications and web services to **AWS**

* Orchestration service that provisions resources
* Automatically handles the deployment
* Monitors application health via a health dashboard

### OpsWorks

Allows you to use **Chef** or **Puppet** to automate the configuration of your servers and deploy code

* Deploy code and manage applications
* Manage on-premises servers or **EC2 instances**

## Exploring Auditing, Monitoring, and Logging Services

Give you insight into how well your systems are performing and help you proactively find and resolve errors

### CloudWatch

Collection of services that help you monitor and observe your cloud resources in real-time.

* Collects **metrics**, **logs** and **events**
* Detect **anomalies** in your environment
* Set **alarms**
* **Visualize** logs

1. CloudWatch Alarms
2. CloudWatch Logs
3. CloudWatch Metrics
    * time-series data.
4. CloudWatch Events
    * triger an event based on a condition

### Cloudtrail

Tracks user activity and API calls within your account

* Log and reatin account activity
* Track activity throug the console, SDKs, and CLI
* Identify which user made changes
* Detect unusual activity in your account

## Amazon Workspaces

Allows you to host virtual desktops in the cloud

* Virtualize Windows or Linux desktops
* Enables employees to work from home
