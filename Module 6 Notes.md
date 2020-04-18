# Module 6 - Compute

[Slides](http://d8rg5deuq9171.cloudfront.net/handouts/Slides/AcademyCloudFoundations_Module_06.pdf)

## Objectives / Topics

- Provide an overview of different AWS compute services in the cloud
- Demonstrate why to use Amazon Elastic Compute Cloud (Amazon EC2)
- Identify the functionality in the EC2 console•Perform basic functions in Amazon EC2 to build a virtual computing environment
- Identify Amazon EC2 cost optimization elements
- Demonstrate when to use AWS Elastic Beanstalk
- Demonstrate when to use AWS Lambda
- Identify how to run containerized applications in a cluster of managed servers

<br/>

## Labs / Activities

- [Knowledge Check](https://www.aws.training/Details/Curriculum?transcriptid=-NscDQNnt0KwQEi-zYfB8Q2&id=43078#modules)
- [Lab: Introduction to Amazon EC2](https://labs.vocareum.com/main/main.php) --- [Lab Instructions](http://d8rg5deuq9171.cloudfront.net/handouts/Vocareum%20scripts/Lab%203%20-%20EC2.pdf)
- [Lab: AWS Lambda](https://labs.vocareum.com/main/main.php) --- [Lab Instructions](http://d8rg5deuq9171.cloudfront.net/handouts/Vocareum%20scripts/Lab%20X%20-%20Lambda.pdf)
- [Lab: AWS Elastic Beanstalk](https://labs.vocareum.com/main/main.php) --- [Lab Instructions](http://d8rg5deuq9171.cloudfront.net/handouts/Vocareum%20scripts/Lab%20X%20-%20Beanstalk.pdf)

<br/>

## Section 1: Compute Services Overview

AWS offers many compute services

- EC2
- EC2 Auto Scaling
- Elastic Container Registry (ECR)
- Elastic Container Service
- VMware Cloud on AWS
- Elastic Beanstalk
- Lambda
- Elastic Kubernetes Service (EKS)
- Lightsail
- Batch
- Fargate
- Outposts
- Serverless Application Repository

The optimal compute service or services that you use will depend on your use case, some aspects to consider:

- What is your application design?
- What are your usage patterns?
- Which configuration settings will you want to manage?

<br/>

## Section 2: Amazon Elastic Compute Cloud (EC2)

### **Overview**

- Provides virtual machines — referred to as EC2 instances — in the cloud
- Gives you full control over the guest operating system (Windows or Linux) on each instance
- You can launch instances of any size into an Availability Zone anywhere in the world with just a few clicks or a line of code, and they are ready in minutes
- Resizable compute capacity
- You can launch instances from Amazon Machine Images (AMIs)
- You can control traffic to and from instances
- Provides tools to build failure resilient applications and isolate them from common failure scenarios

### **Launching an EC2 Instance**

These are the nine key decisions to make when you create an EC2 instance by using the AWS Management Console Launch Instance Wizard.

1. Select Amazon Machine Image (AMI)
   - Is a template that is used to create an EC2 instance (a virtual machine)
   - Contains a Windows or Linux operating system and often has some software pre-installed
   - AMI choices:
     - Quick Start – Linux and Windows AMIs that are provided by AWS
     - My AMIs – Any AMIs that you created
     - AWS Marketplace – Pre-configured templates from third parties
     - Community AMIs – AMIs shared by others; use at your own risk
2. Select an Instance Type
   - Optimized to fit different use cases
   - The instance type that you choose determines
     - Memory (RAM)
     - Processing power (CPU)
     - Disk space and disk type (Storage)
     - Network performance
   - Instance type categories
     - General purpose
     - Compute optimized
     - Memory optimized
     - Storage optimized
     - Accelerated computing
   - Instance types offer family, generation, and size (Example - `t3.large`: Family - `T`, Generation - `3`, Size - `large`)
   - Networking Features
     - The network bandwidth (Gbps) varies by instance type.
     - To maximize networking and bandwidth performance of your instance type enable enhanced networking and if you have interdependent instances, launch them into a cluster placement group.
     - Enhanced networking types are supported on most instance types. Enhanced networking types:
       - Elastic Network Adapter (ENA): Supports network speeds of up to 100 Gbps.
       - Intel 82599 Virtual Function interface: Supports network speeds of up to 10 Gbps.
3. Specify Network Settings
   - Where should the instance be deployed? Identify the VPC and optionally the subnet
   - Should a public IP addressbe automatically assigned?
   - You can have multiple networks, such as different ones for development, testing and production
4. Attach IAM Role (optional)
   - Will software on the EC2 instance need to interact with other AWS services? If yes, attach an appropriate IAM Role. IAM Roles can be attached at any time, not just launch.
   - An AWS Identity and Access Management (IAM) role that is attached to an EC2 instance is kept in an instance profile.
5. User Data Script (optional)
   - Specify a user data script at instance launch. Use user data scripts to customize the runtime environment of your instance
   - Script executes the first time the instance starts
6. Specify Storage
   - Configure the root volume
   - Attach additional storage volumes(optional). For each volume, specify:
     - Disk Size (in GB)
     - Volume type (SSDs or HDDs)
     - If the volume will be deleted when the instance is terminated
     - If encryption should be used
   - Storage Options:
     - Amazon Elastic Block Store (Amazon EBS) –
       - Durable, [block-level storage](https://en.wikipedia.org/wiki/Block-level_storage) volumes.
       - You can stop the instance and start it again, and the data will still be there.
     - Amazon EC2 Instance Store
       - Storage is provided on disks that are attached to the host computer where the EC2 instance is running.
       - If the instance stops, data stored here is deleted.
     - Other options for storage (not for the root volume)
       - Mount an Amazon Elastic File System (EFS) file system.
       - Connect to Amazon Simple Storage Service (S3).
7. Add Tags
   - Consists of a key and an optional value.
   - Tagging is how you can attach metadata to an EC2 instance
   - Potential benefits: Filtering, automation, cost allocation, and access control.
8. Security Group Settings
   - A security group is a set of firewall rules that control traffic to the instance
   - When you launch an instance, you associate one or more security groups with it
   - Create rules that specify the source, which ports that network communications can use and the protocol (TPC, UDP, ICMP)
   - Modify the rules for a security group at any time; the new rules are automatically applied to all instances that are associated with the security group
9. Identify or Create the Key Pair
   - At instance launch, you specify an existing key pair or create a new key pair
   - A key pair consists of a public key that AWS stores and a private key file that you store
   - It enables secure connections to the instance
   - For Windows AMIs – Use the private key to obtain the administrator password that you need to log in to your instance
   - For Linux AMIs – Use the private key to use SSH to securely connect to your instance

### **Miscellaneous**

Consider using an Elastic IP Address if you require a persistent public IP address.

Instance metadata can be viewed in browser or a terminal window, and can be used to configure or manage a running instance

Amazon CloudWatch can be used to monitor an EC2 instance to provide near-real-time metrics, charts, and 15 months of historical data. CloudWatch has basic monitoring (no additional cost) or detailed monitoring.

[Lab: Introduction to Amazon EC2](https://labs.vocareum.com/main/main.php) --- [Lab Instructions](http://d8rg5deuq9171.cloudfront.net/handouts/Vocareum%20scripts/Lab%203%20-%20EC2.pdf)

<br/>

## Section 3: Amazon EC2 Cost Optimization

### **Amazon Pricing Models**

On-Demand Instances

- Pay by the hour
- No long-term commitments.
- Eligible for the AWS Free Tier.

Dedicated Hosts

- A physical server with EC2 instance capacity fully dedicated to your use.

Dedicated Instances

- Instances that run in a VPC on hardware that is dedicated to a single customer.

Spot Instances

- Instances run as long as they are available and your bid is above the Spot Instance price.
- They can be interrupted by AWS with a 2-minute notification
- Interruption options include terminated, stopped or hibernated
- Prices can be significantly less expensive compared to On-Demand
Instances
- Good choice when you have flexibility in when your applications can run.

Reserved Instances

- Full, partial, or no upfront payment for instance you reserve
- Discount on hourly charge for that instance
- 1-year or 3-year term

Scheduled Reserved Instances

- Purchase a capacity reservation that is always available on a recurring schedule you specify
- 1-year term

Per second billing available for On-Demand Instances, Reserved Instances, and Spot Instances that run Amazon Linux or Ubuntu

### **Four Pillars of Cost Optimization**

Right Size

- Provision instances to match the need - CPU, memory, storage, and network throughput
- Use Amazon CloudWatch metrics to dowsize as needed - How idle are instances? When?
- Best practice: Right size, then reserve

Increase Elasticity

- Stop or hibernate Amazon EBS-backed instances that are not actively in use
- Use automatic scaling to match needs based on usage

Optimal Pricing Model

- Leverage the right pricing model for your use case
- Optimize and combine purchase types
  - Examples: Use On-Demand Instance and Spot Instances for variable workloads, use Reserved Instances for predictable workloads
- Consider serverless solutions (AWS Lambda)

Optimize Storage Choices

- Reduce costs while maintaining storage performance and availability
- Resize EBS volumes and change EBS volume types
- Delete EBS snapshots that are no longer needed
- Identify the most appropriate destination for specific types of data

### **Wrap-up**

Cost optimization is an ongoing process.

- Define and enforce cost allocation tagging
- Define metrics, set targets, and review regularly.
- Encourage teams to architect for cost
- Assign the responsibility of optimization to an individual or to a team

<br/>

## Section 4: Container Services

### **Container Basics**

Containers are a method of operating system virtualization.

- Repeatable
- Self-contained execution environments
- Software runs the same in different environments
- Faster to launch and stop or terminate than virtual machines

Docker is a software platform that enables you to build, test, and deploy applications quickly. Containers are created from a template called an image.

### **Amazon Elastic Container Service (ECS)**

- A highly scalable, fast, container management service
- Key benefits
  - Orchestrates the execution of Docker containers
  - Maintains and scales the fleet of nodes that run your containers
  - Removes the complexity of standing up the infrastructure
- Integrated with features that are familiar to Amazon EC2 service users
  - Elastic Load Balancing
  - Amazon EC2 security groups
  - Amazon EBS volumes
  - IAM roles

Do you want to manage the Amazon ECS cluster that runs the containers?

- If yes, create an Amazon ECS cluster backed by Amazon EC2 (provides more granular control over infrastructure)
- If no, create an Amazon ECS cluster backed by AWS Fargate (easier to maintain, focus on your applications)

Amazon Elastic Container Registry (ECR) is a fully managed Docker container registry that makes it easy for developers to store, manage, and deploy Docker container images.

### **Amazon Elastic Kubernetes Service (EKS)**

What is Kubernetes?

- Kubernetes is open source software for container orchestration
  - Deploy and manage containerized applicationsat scale
  - The same toolset can be used on premises and in the cloud
- Complements Docker
  - Docker enables you to run multiple containers on a single OS host
  - Kubernetes orchestrates multiple Docker hosts (nodes)
- Automates container provisioning, networking, load distribution and scaling

Amazon Elastic Kubernetes Service (Amazon EKS)

- Enables you to run Kubernetes on AWS
- Certified Kubernetes conformant (supports easy migration)
- Supports Linux and Windows containers
- Compatible with Kubernetes community tools and supports popular Kubernetes add-ons
- Use Amazon EKS to manage clusters of Amazon EC2 compute instances and run containers that are orchestrated by Kubernetes on those instances

<br/>

## Section 5: Introduction to AWS Lambda

- Serverless computing enables you to build and run applications and services without provisioning or managing servers.
- Supports multiple programming languages.
- Provides built-in fault tolerance and automatic scaling.
- An event source is an AWS service or developer-created application that triggers a Lambda function to run.
- Pay-per-use pricing
- The maximum memory allocation for a single Lambda function is 3,008 MB.
- The maximum execution time for a Lambda function is 15 minutes
- Deployment package size = 250 MB unzipped, including layers

[Lab: AWS Lambda](https://labs.vocareum.com/main/main.php) --- [Lab Instructions](http://d8rg5deuq9171.cloudfront.net/handouts/Vocareum%20scripts/Lab%20X%20-%20Lambda.pdf)

<br/>

## Section 6: Introduction to Elastic Beanstalk

- An easy way to get web applications up and running
- A managed service that automatically handles
  - Infrastructure provisioning and configuration
  - Deployment
  - Load balancing
  - Automatic scaling
  - Health monitoring
  - Analysis and debugging
  - Logging
- No additional charge for Elastic Beanstalk, pay only for the underlying resources that are used
- It supports web applications written for common platforms
- You upload your code and Elastic Beanstalk automatically handles the deployment

[Lab: AWS Elastic Beanstalk](https://labs.vocareum.com/main/main.php) --- [Lab Instructions](http://d8rg5deuq9171.cloudfront.net/handouts/Vocareum%20scripts/Lab%20X%20-%20Beanstalk.pdf)

<br/>

---

<br/>

[Knowledge Check](https://www.aws.training/Details/Curriculum?transcriptid=-NscDQNnt0KwQEi-zYfB8Q2&id=43078#modules)

[AWS Lambda Functions and Autoscaling Video](https://www.youtube.com/watch?v=CPCJAhYk2FE) --- [Walkthrough Instructions](https://docs.google.com/document/d/1K8XQhXQhNJSTlIM2FrO5pktcMRk382pjpdVmLjpSuqc/edit)

[Build a Password-Protected Website with Lambda and CloudFront](https://lambdaschool.zoom.us/rec/play/65wqceygqj43TNDHswSDVKArW9S0L_-sgCdP__MPmU3mB3BQNAeuY7ARZ7NVRbyLAoLEU_duW_Sg6diU?continueMode=true&_x_zm_rtaid=36nX6fUIT0u2AWS4Hfv6Dg.1587074669552.4a38e847d19f1fd4fd48607050191196&_x_zm_rhtaid=342) --- [Accompanying Blog](https://medium.com/@austinlasseter/build-a-password-protected-website-using-aws-lambda-and-cloudfront-3743cc4d09b6)

[Build, Train, and Deploy a ML Model to SageMaker](https://aws.amazon.com/getting-started/tutorials/build-train-deploy-machine-learning-model-sagemaker/) --- [Supporting Notebook](https://github.com/austinlasseter/sagemaker_tutorials/blob/master/xgboost-tutorial.ipynb)

[SageMaker Technical Deep Dive Playlist](https://www.youtube.com/playlist?list=PLhr1KZpdzukcOr_6j_zmSrvYnLUtgqsZz)

[Deploy a Python App with Plotly Dash and Elastic Beanstalk](https://lambdaschool.zoom.us/rec/play/usZ_c7-rpjI3GdSc4wSDV6V4W429Jv-s13Ab_fIMnkizWnQFOgevMrVGZrC3U2z3x3Ncj9i5q8e3q_IH?continueMode=true&_x_zm_rtaid=36nX6fUIT0u2AWS4Hfv6Dg.1587074669552.4a38e847d19f1fd4fd48607050191196&_x_zm_rhtaid=342) --- [Accompanying Blog](https://medium.com/@austinlasseter/deploying-a-dash-app-with-elastic-beanstalk-console-27a834ebe91d)
