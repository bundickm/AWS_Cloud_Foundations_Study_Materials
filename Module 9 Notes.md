# Module 9 - Cloud Architecture

[Slides](http://d8rg5deuq9171.cloudfront.net/handouts/Slides/AcademyCloudFoundations_Module_09.pdf)

## Objectives / Topics

- Describe the AWS Well-Architected Framework, including the five pillars
- Identify the design principles of the AWS Well-Architected Framework
- Explain the importance of reliability and high availability
- Identify how AWS Trusted Advisor helps customers
- Interpret AWS Trusted Advisor recommendations

<br/>

## Labs / Activities

- [Knowledge Check](https://www.aws.training/Details/Curriculum?transcriptid=-NscDQNnt0KwQEi-zYfB8Q2&id=43078#modules)

<br/>

## Section 1: AWS Well-Architected Framework

- A guide for designing infrastructures that are, secure, high-performing, resilient, and efficient
- A consistent approach to evaluating and implementing cloud architectures
- A way to provide best practices that were developed through lessons learned by reviewing customer architectures
- There are 5 pillars to the Well-Architected Framework: Operational Excellence, Security, Reliability, Performance Efficiency, and Cost Optimization
- The [AWS Well-Architected Tool](https://aws.amazon.com/well-architected-tool/) helps you to implement the Well-Architected Framework

### **Operational Excellence**

**Focus**: Run and monitor systems to deliver business value, and to continually improve supporting processes and procedures.

#### Key Topics

- Managing and automating changes
- Responding to events
- Defining standards to successfully manage daily operations

#### Design Principles

- Perform operations as code
- Annotate documentation
- Make frequent, small, reversible changes
- Refine operations procedures frequently
- Anticipate failure
- Learn from all operational events and failures

#### Operational Excellence Questions

Prepare

- How do you determine what your priorities are?
- How do you design your workload so that you can understand its state?
- How do you reduce defects, ease remediation, and improve flow into production?
- How do you mitigate deployment risks?
- How do you know that you are ready to support a workload?

Operate

- How do you understand the health of your workload?
- How do you understand the health of your operations?
- How do you manage workload and operations events?

Evolve

- How do you evolve operations?

### **Security**

**Focus:** Protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies.

#### Key Topics

- Identifying and managing who can do what
- Establishing controls to detect security events
- Protecting systems and services
- Protecting confidentiality and integrity of data

#### Design Principles

- Implement a strong identity foundation
- Enable traceability
- Apply security at all layers
- Automate security best practices
- Protect data in transit and at rest
- Keep people away from data
- Prepare for security events

#### Security Questions

Identity and access management

- How do you manage credentials and authentication?
- How do you control human access?
- How do you control programmatic access?

Detective Controls

- How do you detect and investigate security events?
- How do you defend against emerging security threats?

Infrastructure Protection

- How do you protect your networks?
- How do you protect your compute resources?

Data Protection

- How do you classify your data?
- How do you protect your data at rest?
- How do you protect your data in transit?

Incident Response

-How do you respond to an incident?

### **Reliability**

**Focus:** Prevent and quickly recover from failures to meet business and customer demand.

#### Key Topics

- Setting up
- Cross-project requirements
- Recovery planning
- Handling change

#### Design Principles

- Test recovery procedures
- Automatically recover from failure
- Scale horizontally to increase aggregate system availability
- Stop guessing capacity
- Manage change in automation

#### Reliability Questions

Foundations

- How do you manage service limits?
- How do you manage your network topology?

Change Management

- How does your system adapt to changes in demand?
- How do you monitor your resources?
- How do you implement change?

Failure Management

- How do you back up data?
- How does your system withstand component failure?
- How do you test resilience?
- How do you plan for disaster recovery?

### **Performance Efficiency**

**Focus:** Use IT and computing resources efficiently to meet system requirements and to maintain that efficiency as demand changes and technologies evolve.

#### Key Topics

- Selecting the right resource types and sizes based on workload requirements
- Monitoring performance
- Making informed decisions to maintain efficiency as business needs evolve

#### Design Principles

- Democratize advanced technologies
- Go global in minutes
- Use serverless architectures
- Experiment more often
- Have mechanical sympathy

#### Performance Efficiency Questions

Selection

- How do you select the best performing architecture?
- How do you select your compute solution?
- How do you select your storage solution?
- How do you select your database solution?
- How do you select your networking solution?

Review

- How do you evolve your workload to take advantage of new releases?

Monitoring

- How do you monitor your resources to ensure they are performing as expected?

Tradeoffs

- How do you use tradeoffs to improve performance?

### **Cost Optimization**

**Focus:** Run systems to deliver business value at the lowest price point.

#### Key Topics

- Understanding and controlling when money is being spent
- Selecting the most appropriate and right number of resource types
- Analyzing spending over time
- Scaling to meeting business needs without overspending

#### Design Principles

- Adopt a consumption model
- Measure overall efficiency
- Stop spending money on data center operations
- Analyze and attribute expenditure
- Use managed and application-level services to reduce cost of ownership

#### Cost Optimization Questions

Expenditure Awareness

- How do you govern usage?
- How do you monitor usage and cost?
- How do you decommission resources?

Cost-Effective Resources

- How do you evaluate cost when you select services?
- How do you meet cost targets when you select resource type and size?
- How do you use pricing models to reduce cost?
- How do you plan for data transfer changes?

Matching Supply and Demand

- How do you match supply of resources with demand?

Optimizing Over Time

- How do you evaluate new services?

<br/>

## Section 2: Reliability and Availability

### **Reliability**

- A measure of your system’s ability to provide functionality when desired by the user
- System includes all system components: hardware, firmware, and software
- Probability that your entire system will function as intended for a specified period
- Mean time between failures (MTBF) = total time in service/number of failures

#### Metrics

- Mean Time to Failure (MTTF)
- Mean Time to Repair (MTTR)
- Mean Time Between Failures (MTBF) = MTTF + MTTR

### **Availability**

- Normal operation time / total time
- A percentage of uptime (for example, 99.9 percent) over time (for example, 1 year)
- Number of 9s – Five 9s means 99.999 percent availability

#### High Availability

- System can withstand some measure of degradation while still remaining available
- Downtime is minimized
- Minimal human intervention is required

#### Availability Factors

- Fault tolerance: The built-in redundancy of an application's components and its ability to remain operational.
- Scalability: The ability of an application to accommodate increases in capacity needs without changing design.
- Recoverability: The process, policies, and procedures that are related to restoring service after a catastrophic event.

<br/>

## Section 3: AWS Trusted Advisor

AWS Trusted Advisor is an online tool that provides real-time guidance to help you provision your resources following AWS best practices. It looks at your entire AWS environment and gives you real-time recommendations in five categories: Cost Optimization, Performance, Security, Fault Tolerance, Service Limits. You can use AWS Trusted Advisor to help you optimize your AWS environment as soon as you start implementing your architecture designs.

<br/>

---

<br/>

[Knowledge Check](https://www.aws.training/Details/Curriculum?transcriptid=-NscDQNnt0KwQEi-zYfB8Q2&id=43078#modules)

[Making Your Environment Highly Available](https://lambdaschool.zoom.us/rec/play/vJYqJLz9qW83Ht2W5ASDV_NwW427J_-shHId8_dfnUyyASQEMQauYuRAYOVN2USEQO5XkzmRU_3hRFuc?continueMode=true&_x_zm_rtaid=36nX6fUIT0u2AWS4Hfv6Dg.1587074669552.4a38e847d19f1fd4fd48607050191196&_x_zm_rhtaid=342) --- [Password](https://lambdaschoolstudents.slack.com/archives/GUL2Y3H17/p1586917358295500) --- [Walkthrough Instructions](https://docs.google.com/document/d/1VWhsH47UVoHPL47KbgIcht0SnITa_dnWh2QTnoP1F2w/edit#)
