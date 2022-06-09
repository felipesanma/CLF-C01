# Pricing, Billing and Governance

## Understanding AWs Pricing

**Pricing**; there are 3 fundamental drivers of cost

* Compute; hourly from launch to temination
* Storage; data you store in the cloud
* Outbound data transfer; data in flight moving between systems

**Free Offer Types**; there are 3 different types of **free** offers available depending on the service you choose

* 12 months free; 12 months free usage following your initial sign-up date to AWS
* Always free; offers do not expires and are available to all AWS customers
* Trials; short-term free trials starting from the date you activate a particular service

### Examples
**EC2 Pricing**; don't forget, there are 5 ways to pay for Amazon EC2 instances

* On-Demand; you pay by the hour or by the second without pre-paying
* Savings Plan; commit to compute usage measured per hour for a 1 or 3 years term
* Reserved instances; commit to use for 1 or 3 years pay regardless of usage
* Spot Instances; instances only launch if spare capacity is available
* Dedicated Hosts; An entire physical just for you

**Lambda Pricing**; don't forget how you're charged when using Lambda

* Number of requests; **includes** test invokes from the console
* Code execution time; from execution **start**, in response to events, to **stop**
* Always free; 1,000,000 requests/month are always free

### Total Cost of Ownership (TCO)

TCO is a financial estimate that helps you understand both the **direct** and **indirect** costs of AWS

**Application Discovery Service**; gelps you plan migration project to the AWS Cloud

**Ways to reduce your TCO using AWS**
* Minimize capital expenditures
* Utilize Reserved Instances
* Right size your resources

### AWS Price List API

Allows you to query the price of AWS services

## Understanding Billing Services

**Budgets**; allows you to set custom budgets that alert you when your costs or usage **exceed** your budget amount
* Improve planning and cost control
* Budget alerts
* Buget Types..
    * Cost Budgets: plan how much you want to spend on a service
    * Usage Bugets: plan how much you want to use on one or more services
    * Reservation Budgets

**Cost and Usage Report**: contains the most comprehensive set of cost and usage data.

**Cost Explorer**: allows you to visualize and forecast your costs and usage over time (view 12 past months)

*Cost Allocation Tags*: Tags are sueful for tracking spend.


## Governance Services

Governance and management services help you maintain control over cost, compliance, and security across your AWS accounts.

**Organizations**: allows you to centrally manage multiple AWS accounts under one umbrella
* Group multiple accounts
* Single payment for all accounts
* Automate account creation
* Allocate resources and apply policies across accounts

An organization is an entity you create to **consolidate multiple** AWS accounts into one.

The root organization pays for all member accounts using **consolidated billing** 

**Service control policies (SCP's)**: are used to enforce permissions you want **everyone** in the organization to follow

**Control Tower**: helps you ensure your accounts conform to company-wide policies
* Helps set up **new accounts** using a multi-account strategy
* Works directly with AWs Organizations
* Enforces the best use of services across accounts
* Provides a dashboard to manage accounts

**System Manager**: gives you visibility and control over your AWs resources
* Automate operational tasks on your resources
* Group resources and take action
* Patch and run commands on multiple EC2 instances or manage RDS instances

**Trusted Advisor**: provides real-time guidance to help you provision your resources following AWS best practices
* Checks your account and makes recommendations
* Helps you see service limits
* Helps you understand best practices

**License Manager**: helps you manage software licenses
* Manage on-premises and AWS licenses
* Track licenses for Oracle, Microsoft, SAP, and more

**Certificate Manager**: helps you provision and manage SSL/TLS certificates
* Provides public and private certificates for free
* Integrates with Elastic Load Balancing, API Gateway, and more

## Utilizing Management Services

Support you as you preapre for planned events, product launches, and migrations.


