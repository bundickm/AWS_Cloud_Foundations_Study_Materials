# Module 2 - Cloud Economics and Billing

[Slides](http://d8rg5deuq9171.cloudfront.net/handouts/Slides/AcademyCloudFoundations_Module_02.pdf)

## Objectives / Topics

- Explain the AWS pricing philosophy
- Recognize fundamental pricing characteristics
- Indicate the elements of total cost of ownership
- Discuss the results of the Simple Monthly Calculator
- Identify how to set up an organizational structure that simplifies billing and account visibility to review cost data.
- Identify the functionality in the AWS Billing Dashboard
- Describe how to use AWS Bills, AWS Cost Explorer, AWS Budgets, and AWS Cost and Usage Reports
- Identify the various AWS technical support plans and features

<br/>

## Labs / Activities

- [Knowledge Check](https://www.aws.training/Details/Curriculum?transcriptid=-NscDQNnt0KwQEi-zYfB8Q2&id=43078#modules)
- [Cost Calculator Activity](http://d8rg5deuq9171.cloudfront.net/handouts/Activities/Module%202%20Activity%20-%20Total%20Cost%20of%20Ownership.pdf) -- [Simple Monthly Calculator](https://calculator.s3.amazonaws.com/index.html)
- [Support Plans Scavenger Hunt](http://d8rg5deuq9171.cloudfront.net/handouts/Activities/Module%202%20Activity%20-%20Support%20Plan.pdf)

<br/>

## Section 1: Fundamentals of Pricing

### **Three Fundamental Cost Drivers with AWS**

1. Compute - charged by use time, varies by instance
2. Storage - charged per GB
3. Data Transfer - outbound transfers are aggregated and charged per GB, inbound transfers and data transfers between services in the same AWS Region typically have no charge

### **Paying for AWS**

- Pay for what you use
- Reserve and save up to 75% versus On-Demand
  - All Upfront Reserved Instance (AURI) -> Large Discount
  - Partial Upfront Reserved Instance (PURI) -> Lower Discount
  - No Upfront Payments Reserved Instance (NURI) -> Smallest Discount
- Scale and save as usage increases
  - Tiered pricing for services like S3, EBS, EFS
- Save as AWS grows
- Custom Pricing
  - Meet varying needs through custom pricing.
  - Available for high-volume projects with unique requirements.

#### The services below are free but there might be charges associated with other AWS services that are used alongside these services.

- Amazon VPC
- Elastic Beanstalk
- Auto Scaling
- AWS CloudFormation
- AWS Identity and Access Management

<br/>

## Section 2: Total Cost of Ownership

**Total Cost of Ownership (TCO):** The financial estimate to help identify direct and indirect costs of a system

- Compare the costs of running an entire infrastructure environment or specific workload on-premises versus on AWS
- Budget and build the business case for moving to the cloud

### **TCO Considerations**

1. Server Costs
   - Hardware: Server, rack chassis power distribution units (PDUs), top-of-rack (TOR) switches, and maintenance
   - Software: Operating system (OS), virtualization licenses, and maintenance
   - Facilities: Space, power, and cooling
2. Storage Costs
   - Hardware: Storage disks, storage area network (SAN) or Fibre Channel (FC) switches
   - Storage administration costs
   - Facilities: Space, power, and cooling
3. Network Costs
   - Network Hardware: Local area network (LAN) switches, load balancer bandwidth costs
   - Network administration costs
   - Facilities: Space, power, and cooling
4. IT Labor Costs
   - Server administration costs

[Cost Calculator Activity](http://d8rg5deuq9171.cloudfront.net/handouts/Activities/Module%202%20Activity%20-%20Total%20Cost%20of%20Ownership.pdf) -- [Simple Monthly Calculator](https://calculator.s3.amazonaws.com/index.html)

<br/>

## Section 3: Billing

### **AWS Organizations**

**AWS Organizations:** An account management service that enables you to consolidate multiple AWS accounts into an organization that you create and centrally manage. AWS Organizations includes account management and consolidated billing capabilities that enable you to better meet the budgetary, security, and compliance needs of a business.

#### Key Features and Benefits

- Policy based account management
- Group based account management
- Application programming interfaces (APIs) that automate account management
- Consolidated billing

#### Security

- Control access with AWS Identity and Access Management (IAM)
- IAM policiesenable you to allow or deny access to AWS services for users, groups, and roles.
- Service control policies (SCPs) enable you to allow or deny access to AWS services for individuals or group accounts in an organizational unit (OU).

#### Setup

1. Create organization
2. Create organizational units
3. Create service control policies
4. Test restrictions

#### Accessing AWS Organizations

- AWS Management Console
- AWS Command Line Interface (AWS CLI) tools
- Software Development Kits (SDKs)
- HTTPS Query Application Programming Interfaces (API)

### **AWS Billing and Cost Management**

**AWS Billing and Cost Management:** The service that you use to pay your AWS bill, monitor your usage, and analyze and control your costs.

#### Tools

- **AWS Budgets:** It gives you the ability to set custom budgets that alert you when your costs or usage exceed (or are forecasted to exceed) your budgeted amount. You can also use it to set reservation utilization or coverage targets and receive alerts when your utilization drops below the threshold you define.
- **AWS Cost and Usage Report:** Tracks your AWS usage and provides estimated charges associated with your account.
- **AWS Cost Explorer:** Visualize, understand, and manage AWS costs and usage over time.

<br/>

## Section 4: Technical Support

AWS Support offers a range of plans that provide access to tools and expertise that support the success and operational health of your AWS solutions. All support plans provide 24/7 access to customer service, AWS documentation, whitepapers, and support forums.

- Proactive Guidance: Technical Account Manager (TAM)
- Best Practices: AWS Trusted Advisor
- Account Assistance: AWS Support Concierge

### **Support Plans**

- **Basic Support:** Resource Center access, Service Health Dashboard, product FAQs, discussion forums, and support for health checks
- **Developer Support:** Support for early development on AWS
- **Business Support:** Customers that run production workloads
- **Enterprise Support:** Customers that run business and mission-critical workloads

Support response times vary based on plan and case severity. Basic offers no case support, all other support ranges from 24 hours to 15 minutes or less.

<br/>

---

<br/>

[Support Scavenger Hunt](http://d8rg5deuq9171.cloudfront.net/handouts/Activities/Module%202%20Activity%20-%20Support%20Plan.pdf)

[Knowledge Check](https://www.aws.training/Details/Curriculum?transcriptid=-NscDQNnt0KwQEi-zYfB8Q2&id=43078#modules)
