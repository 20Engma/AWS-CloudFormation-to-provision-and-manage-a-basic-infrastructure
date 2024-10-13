Project Overview:
Objective:

Create a dedicated infrastructure using AWS CloudFormation for the development team.
Deploy an Apache web server with HTTP access on a small Amazon EC2 instance.
Ensure the infrastructure is deployed in a dedicated VPC with a single public subnet.
Tools and Services:

AWS CloudFormation: For defining and provisioning the infrastructure using templates.
AWS Cloud9: As the development environment for modifying CloudFormation templates.
Amazon VPC: To create an isolated virtual network for the EC2 instance.
Amazon EC2: To host the Apache web server.
Security Groups: To manage network access to the EC2 instance.
CloudFormation Drift Detection: To detect manual changes made outside of the CloudFormation template.
Steps:
1. Modify CloudFormation Template:
Start with a base CloudFormation template.
Modify it to define a dedicated Amazon VPC with a single public subnet.
Add a t2.micro EC2 instance in the public subnet with an Apache web server installed.
Ensure HTTP access by opening port 80 in the Security Group attached to the EC2 instance.
2. Deploy the Infrastructure:
Use the modified CloudFormation template to create a stack via the AWS Management Console or AWS CLI.
Deploy the resources defined in the template, including the VPC, subnet, EC2 instance, and Security Group.
3. Verify the Web Page:
After the CloudFormation stack is created, verify the EC2 instance is running and accessible over HTTP by visiting the public IP address of the instance.
Ensure the Apache web server is correctly serving a simple web page.
4. Detect Drift:
Manually modify the Security Group (for example, by adding or removing rules).
Use AWS CloudFormation's Drift Detection feature to detect changes made manually outside the template.
5. Update Security Group via Change Set:
Create a change set to update the Security Group back to its expected state as defined in the CloudFormation template.
Execute the change set to apply the update.
Key Concepts:
VPC: A virtual private cloud for isolating your AWS resources.
EC2: A virtual server used for hosting the Apache web server.
Security Group: Acts as a firewall, controlling the inbound and outbound traffic to the EC2 instance.
CloudFormation Change Set: Allows you to review and apply changes to the stack before making them live.
Drift Detection: Detects differences between the resources defined in the CloudFormation template and the actual state of AWS resources.
Learning Outcomes:
Understanding how to create and modify AWS CloudFormation templates.
Deploying a web server using CloudFormation and validating its functionality.
Using CloudFormation's Drift Detection and Change Set features to detect and correct manual changes to the infrastructure.
