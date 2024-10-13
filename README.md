
# AWS CloudFormation Project: Development Team Infrastructure Setup

## **Objective**
The goal of this project is to create a dedicated infrastructure for a development team using AWS CloudFormation. This involves deploying an Apache web server on an Amazon EC2 instance within a dedicated VPC. The infrastructure will be provisioned, managed, and updated using AWS CloudFormation templates.

### **Key Components:**
- **Amazon EC2**: To host the Apache web server.
- **Amazon VPC**: For creating an isolated network environment.
- **AWS CloudFormation**: For defining the infrastructure as code.
- **Security Groups**: For managing network access.

## **Steps**

### **1. Modify the CloudFormation Template**
- Begin with a base CloudFormation template.
- Modify the template to create:
  - A dedicated **Amazon VPC** with a single **public subnet**.
  - A **t2.micro EC2 instance** within the public subnet, which will run an Apache web server.
  - A **Security Group** that allows HTTP access (port 80).
  
### **2. Deploy the Infrastructure**
- Using AWS CloudFormation, create a **stack** to provision the infrastructure:
  - VPC
  - Public subnet
  - EC2 instance
  - Security Group
- The deployment can be executed using the **AWS Management Console** or **AWS CLI**.

### **3. Verify the Web Server**
- Once the stack is created, confirm that the EC2 instance is running.
- Access the instance via HTTP by visiting its public IP address.
- Ensure that the Apache web server serves a simple web page.

### **4. Use Drift Detection**
- Manually modify the **Security Group** (e.g., by adding/removing rules).
- Use AWS CloudFormation's **Drift Detection** feature to identify changes made outside the CloudFormation template.

### **5. Apply Changes via Change Set**
- Create a **change set** in CloudFormation to update the Security Group back to the expected state defined in the template.
- Review and execute the change set to apply the updates.

## **Key Concepts**
- **VPC**: Virtual Private Cloud for isolating AWS resources.
- **EC2**: Elastic Compute Cloud, used to host the web server.
- **Security Group**: A virtual firewall that controls traffic to the EC2 instance.
- **Change Set**: A mechanism to preview and apply changes to the CloudFormation stack.
- **Drift Detection**: A feature to detect differences between the actual state of the infrastructure and the CloudFormation template.

## **Learning Outcomes**
- Gain hands-on experience in creating and modifying AWS CloudFormation templates.
- Deploy a web server using CloudFormation and verify its functionality.
- Understand how to use **Drift Detection** and **Change Sets** to detect and correct manual changes made to the infrastructure.

---

