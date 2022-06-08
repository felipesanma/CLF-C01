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