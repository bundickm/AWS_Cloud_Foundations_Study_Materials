# Module 3 - AWS Global Infrastructure Overview

[Slides](http://d8rg5deuq9171.cloudfront.net/handouts/Slides/AcademyCloudFoundations_Module_03.pdf)

## Objectives / Topics

- Identify the difference between AWS Regions, Availability Zones, and edge locations
- Identify AWS service and service categories

<br/>

## Labs / Activities

- [Knowledge Check](https://www.aws.training/Details/Curriculum?transcriptid=-NscDQNnt0KwQEi-zYfB8Q2&id=43078#modules)
- [Lab: AWS Management Console](https://labs.vocareum.com/main/main.php) -- [Labs Instructions](http://d8rg5deuq9171.cloudfront.net/handouts/Vocareum%20scripts/Lab%20X%20-%20Sandbox.pdf)
- [AWS Global Infrastructure Activity](http://d8rg5deuq9171.cloudfront.net/handouts/Activities/Module%203%20Activity%20-%20AWS%20Global%20Infrastructure.pdf)

<br/>

## Section 1: AWS Global Infrastructure

The [AWS Global Infrastructure](https://infrastructure.aws/) is designed and built to deliver a flexible, reliable, scalable, and secure cloud computing environment with high-quality global network performance.

### **AWS Regions**

An AWS Region is a geographical area.

- Data replication across Regions is controlled by you.
- Communicationbetween Regions uses AWS backbone network infrastructure.
- Each Region provides full redundancy and connectivity to the network.
- A Region typically consists of two or more Availability Zones

When selecting a region consider the following:

- Laws - Data governance and legal requirements
- Proximity - Select regions close to your customers for reduced latency
- Availability - Some services are region locked
- Cost - Cost varies by region

Each Availability Zone is a fully isolated partition of the AWS infrastructure. There are currently 69 Availability Zones worldwide.

- Availability Zones consist of discrete data centers
- They are interconnected with other Availability Zones by using high-speed private networking
- They are designed for fault isolation
- You choose your Availability Zones but AWS recommends replicating data and resources across Availability Zones for resiliency.

### **AWS Data Centers**

- AWS data centers are designed for security. Each data center has redundant power, networking, and connectivity, and is housed in a separate facility.
- Data centers are where the data resides and data processing occurs. A data center typically has 50,000 to 80,000 physical servers

 AWS provides a global network of 187 Points of Presence locations:

- Consists of 176 edge locations - where end users access services located at AWS
- 11 Regional edge caches - cache copies of your infrequent content close to your users
- Used with **Amazon CloudFront** -  a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, all within a developer-friendly environment.

AWS Infrastructure Features:

1. Elasticity and scalability - dynamically adapts to capacity and growth needs
2. Fault-tolerance - Continues operating properly in the presence of a failure due to built-in redundancy of components
3. High availability - High operational performance with minimized downtime and no human intervention

<br/>

## Section 2: AWS Services and Service Category Overview

### **Foundation Services**

- Compute
- Networking
- Storage

### **Service Categories**

23 different product or service categories, and each category consists of one or more services. The course covers the most common categories and the ones likely to be on the foundations exam.

#### AWS Storage Services

- [Amazon Simple Storage Services (S3)](https://aws.amazon.com/s3/) - object storage service that offers industry-leading scalability, data availability, security, and performance.
- [Amazon Elastic Block Storage (EBS)](https://aws.amazon.com/ebs) - an easy to use, high performance block storage service designed for use with Amazon Elastic Compute Cloud (EC2) for both throughput and transaction intensive workloads at any scale.
- [Amazon Elastic File System (EFS)](https://aws.amazon.com/efs/) - a simple, scalable, fully managed elastic NFS file system for use with AWS Cloud services and on-premises resources. 
- [Amazon Simple Storage Service Glacier](https://aws.amazon.com/glacier/) - a secure, durable, and extremely low-cost Amazon S3 cloud storage classes for data archiving and long-term backup.

#### AWS Compute Services

- [Amazon EC2](https://aws.amazon.com/ec2/) - a web service that provides secure, resizable compute capacity in the cloud.
- [Amazon EC2 Auto Scaling](https://aws.amazon.com/ec2/autoscaling/) - helps to maintain application availability and allows you to automatically add or remove EC2 instances according to conditions you define.
- [Amazon Elastic Container Services (ECS)](https://aws.amazon.com/ecs/) - a fully managed container orchestration service.
- [Amazon EC2 Container Registry (ECR)](https://aws.amazon.com/ecr/) -  a fully-managed Docker container registry that makes it easy for developers to store, manage, and deploy Docker container images.
- [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/) - an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.
- [AWS Lambda](https://aws.amazon.com/lambda/) - lets you run code without provisioning or managing servers.
- [Amazon Elastic Kubernetes Services (EKS)](https://aws.amazon.com/eks/) - a fully managed [Kubernetes](https://en.wikipedia.org/wiki/Kubernetes) service.
- [AWS Fargate](https://aws.amazon.com/fargate/) - a serverless compute engine for containers that works with both Amazon Elastic Container Service (ECS) and Amazon Elastic Kubernetes Service (EKS).

#### AWS Database Services

- [Amazon Relational Database Service (RDS)](https://aws.amazon.com/rds/) - makes it easy to set up, operate, and scale a relational database in the cloud.
- [Amazon Aurora](https://aws.amazon.com/rds/aurora/) -  a MySQL and PostgreSQL-compatible relational database built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases.
- [Amazon Redshift](https://aws.amazon.com/redshift/) - a fully managed, petabyte-scale data warehouse service in the cloud.
- [Amazon DynamoDB](https://aws.amazon.com/dynamodb/) - a key-value and document database that delivers single-digit millisecond performance at any scale.

#### Networking and Content Delivery Services

- [Amazon VPC](https://aws.amazon.com/vpc/) - lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define.
- [Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/) - automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, IP addresses, and Lambda functions.
- [Amazon CloudFront](https://aws.amazon.com/cloudfront/) - a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, all within a developer-friendly environment.
- [AWS Transit Gateway](https://aws.amazon.com/transit-gateway/) - a service that enables customers to connect their Amazon Virtual Private Clouds (VPCs) and their on-premises networks to a single gateway.
- [Amazon Route 53](https://aws.amazon.com/route53/) - a highly available and scalable cloud Domain Name System (DNS) web service.
- [AWS Direct Connect](https://aws.amazon.com/directconnect/) - a cloud service solution that makes it easy to establish a dedicated network connection from your premises to AWS.
- [AWS VPN](https://aws.amazon.com/vpn/) - lets you establish a secure and private encrypted tunnel from your network or device to the AWS global network.

#### Security, Identity, and Compliance Services

- [AWS Identity and Access Management (IAM)](https://aws.amazon.com/iam/) -  enables you to manage access to AWS services and resources securely.
- [AWS Organizations](https://aws.amazon.com/organizations/) - helps you centrally govern your environment as you grow and scale your workloads on AWS.
- [Amazon Cognito](https://aws.amazon.com/cognito/) - lets you add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily.
- [AWS Artifact](https://aws.amazon.com/artifact/) - a central resource for compliance-related information that matters to you.
- [AWS Key Management Service (KMS)](https://aws.amazon.com/kms/) - makes it easy for you to create and manage cryptographic keys and control their use across a wide range of AWS services and in your applications.
- [AWS Shield](https://aws.amazon.com/shield/) - a managed Distributed Denial of Service (DDoS) protection service that safeguards applications running on AWS.

#### Cost Management Services

- [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/) - contains the most comprehensive set of AWS cost and usage data available, including additional metadata about AWS services, pricing, and reservations (e.g., Amazon EC2 Reserved Instances (RIs)).
- [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/) - gives you the ability to set custom budgets that alert you when your costs or usage exceed (or are forecasted to exceed) your budgeted amount.
- [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) - an easy-to-use interface that lets you visualize, understand, and manage your AWS costs and usage over time.

#### AWS Management and Governance Services

- [AWS Management Console](https://aws.amazon.com/console/) - brings AWS right to your computer or mobile phone with a secure, easy-to-access, web-based portal.
- [AWS Config](https://aws.amazon.com/config/) - a service that enables you to assess, audit, and evaluate the configurations of your AWS resources.
- [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/) - a monitoring and observability service built for DevOps engineers, developers, site reliability engineers (SREs), and IT managers.
- [AWS Auto Scaling](https://aws.amazon.com/autoscaling/) - monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.
- [AWS Command Line Interface (CLI)](https://aws.amazon.com/cli/) -  a unified tool to manage your AWS services. With just one tool to download and configure, you can control multiple AWS services from the command line and automate them through scripts.
- [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/) - an online tool that provides you real time guidance to help you provision your resources following AWS best practices.
- [AWS Well-Architected Tool](https://aws.amazon.com/well-architected-tool/) - helps you review the state of your workloads and compares them to the latest AWS architectural best practices.
- [AWS CloudTrail](https://aws.amazon.com/cloudtrail/) - a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account.

<br/>

[Lab: AWS Management Console](https://labs.vocareum.com/main/main.php) -- [Labs Instructions](http://d8rg5deuq9171.cloudfront.net/handouts/Vocareum%20scripts/Lab%20X%20-%20Sandbox.pdf)

[AWS Global Infrastructure Activity](http://d8rg5deuq9171.cloudfront.net/handouts/Activities/Module%203%20Activity%20-%20AWS%20Global%20Infrastructure.pdf)
