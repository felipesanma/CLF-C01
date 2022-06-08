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

