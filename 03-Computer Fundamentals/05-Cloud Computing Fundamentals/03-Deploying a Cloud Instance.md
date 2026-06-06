# Cloud Computing Fundamentals

## Deploying a Cloud Instance

### Overview

One of the most powerful features of cloud computing is the ability to create, modify, and manage computing resources within minutes. Instead of purchasing physical servers, organizations can deploy virtual machines on demand and pay only for the resources they use.

In this exercise, a cloud environment similar to Amazon Web Services (AWS) is used to deploy infrastructure for a cybersecurity training platform. This demonstrates how Infrastructure as a Service (IaaS) enables organizations to provision and manage virtual computing resources quickly and efficiently.

---

## Main Concept

### What is a Cloud Instance?

A cloud instance is a virtual computer running inside a cloud provider's infrastructure.

Cloud instances provide:

```text
CPU
RAM
Storage
Networking
Operating System Support
```

These virtual computers can run applications, websites, databases, cybersecurity labs, and other workloads.

In AWS terminology, a cloud instance is called:

```text
EC2 (Elastic Compute Cloud)
```

---

## How It Works

### Step 1: Select a Region

Before deploying resources, a geographical region must be selected.

A region represents a physical location where cloud resources will be hosted.

Examples:

```text
North America
Europe
Asia Pacific
South America
```

Benefits of choosing the correct region:

```text
Lower Latency
Better User Experience
Regulatory Compliance
Improved Performance
```

---

### Step 2: Create Virtual Machines

Cloud providers allow users to create virtual computers called instances.

Example deployment:

#### Application Interface Server

```text
Instance Name: application-interface
Instance Type: t3.micro
Status: Running
```

Purpose:

```text
Host Frontend Application
Manage User Access
Provide Web Interface
```

---

#### Cybersecurity Practice Machine 1

```text
Instance Name: study-machine-1
Instance Type: m5.large
Status: Running
```

Purpose:

```text
Security Training
Lab Exercises
Testing Environment
```

---

#### Cybersecurity Practice Machine 2

```text
Instance Name: study-machine-2
Instance Type: m5.large
Status: Running
```

Purpose:

```text
Additional User Capacity
Training Simulations
Cybersecurity Practice
```

---

### Step 3: Monitor Running Instances

After deployment:

```text
Cloud Console
      ↓
Instances Section
      ↓
View Resource Status
```

Administrators can:

```text
Start Instances
Stop Instances
Restart Instances
Delete Instances
Monitor Usage
```

---

### Step 4: Analyze Billing

Cloud providers continuously calculate costs based on resource usage.

Billing depends on:

```text
Instance Type
Runtime Duration
Storage Usage
Network Usage
```

Larger instances generally cost more than smaller instances.

---

### Step 5: Optimize Costs

When resources are not required:

```text
Stop Instance
      ↓
Reduce Costs
```

Example:

```text
study-machine-1 → Stopped
study-machine-2 → Stopped
```

Result:

```text
Lower Monthly Expenses
```

This demonstrates one of the biggest advantages of cloud computing:

```text
Pay Only For What You Use
```

---

## Important Components

### EC2 (Elastic Compute Cloud)

#### What is EC2?

EC2 is a cloud service that provides virtual computers on demand.

Capabilities:

```text
Run Applications
Host Websites
Deploy Databases
Create Security Labs
Support Enterprise Services
```

Benefits:

```text
Scalable
Flexible
Cost Effective
Globally Available
```

---

### Instance Types

#### What is an Instance Type?

An instance type defines the hardware resources allocated to a virtual machine.

Includes:

```text
CPU
RAM
Performance Characteristics
```

---

### t3.micro

Characteristics:

```text
Small Resource Allocation
Low Cost
Lightweight Workloads
```

Common Uses:

```text
Small Websites
Development Servers
Testing Applications
```

---

### m5.large

Characteristics:

```text
Higher CPU Capacity
More Memory
Better Performance
```

Common Uses:

```text
Training Platforms
Application Servers
Cybersecurity Labs
```

---

### Region

A geographical location where cloud resources are hosted.

Benefits:

```text
Reduced Network Delay
Improved Reliability
Regulatory Compliance
```

Examples:

```text
US East
Europe West
Asia Pacific
```

---

### Billing System

Cloud providers track resource consumption automatically.

Factors affecting cost:

```text
Running Instances
Storage Usage
Network Traffic
Additional Services
```

Cost optimization is a key responsibility of cloud administrators.

---

## Advantages / Benefits

### Rapid Deployment

Infrastructure can be deployed within minutes.

---

### Scalability

Resources can increase or decrease as needed.

---

### Cost Control

Organizations only pay for active resources.

---

### Flexibility

Different instance sizes can be selected based on workload requirements.

---

### Global Availability

Applications can be deployed in multiple regions worldwide.

---

### Easy Resource Management

Cloud consoles provide centralized administration tools.

---

## Key Characteristics

* EC2 instances are virtual computers in the cloud.
* Instance types determine CPU and memory allocation.
* Regions determine where resources are physically hosted.
* Cloud infrastructure can be deployed quickly.
* Billing is based on resource consumption.
* Stopping unused instances reduces operational costs.
* Cloud environments support rapid scaling and flexibility.
* IaaS provides full control over operating systems and applications.

---

## Example

### Cybersecurity Training Platform Deployment

#### Initial Deployment

```text
application-interface
Type: t3.micro
Status: Running

study-machine-1
Type: m5.large
Status: Running

study-machine-2
Type: m5.large
Status: Running
```

Purpose:

```text
Provide Web Access
Support Student Labs
Enable Cybersecurity Training
```

---

### Cost Optimization Scenario

During development:

```text
No Active Students
```

Action:

```text
Stop study-machine-1
Stop study-machine-2
```

Result:

```text
Reduced Resource Consumption
Reduced Cloud Costs
```

This demonstrates how cloud resources can be adjusted dynamically according to demand.

---

## Key Notes

### Important AWS Concepts

#### EC2

```text
Virtual Computer In The Cloud
```

---

#### Instance Type

```text
Defines CPU And Memory Resources
```

Examples:

```text
t3.micro
m5.large
```

---

#### Region

```text
Physical Location Of Cloud Resources
```

---

#### Billing

```text
Usage-Based Pricing Model
```

---

### Cost Optimization Methods

```text
Stop Unused Instances
Use Smaller Instance Types
Monitor Resource Usage
Scale Only When Needed
```

---

### Cloud Service Model

This exercise demonstrates:

```text
Infrastructure as a Service (IaaS)
```

Because the user manages:

```text
Virtual Machines
Operating Systems
Applications
Configurations
```

While the provider manages:

```text
Physical Hardware
Networking Infrastructure
Data Centers
```

---

## Learning Outcome

After completing this section, I understood how cloud infrastructure can be deployed and managed using virtual computing resources such as EC2 instances. I learned how regions determine the geographical location of cloud resources, how instance types define computing capacity, and how cloud environments can be provisioned within minutes. I also gained practical knowledge of Infrastructure as a Service (IaaS), resource management, cost monitoring, and cloud cost optimization techniques such as stopping unused instances. Additionally, I learned how organizations use cloud platforms to deploy scalable, flexible, and globally accessible applications while maintaining control over their operating systems and workloads.
