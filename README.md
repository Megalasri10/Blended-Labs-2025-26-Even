Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

Author

Name: Megala M S

Register Number: 212225040230

Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud
(EC2). This lab focuses on launching and managing a virtual server, understanding instance types and

AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations
such as start, stop, and terminate.
Prerequisites Basic understanding of cloud computing concepts AWS account or AWS Academy Lab
access Web browser with internet connectivity Basic knowledge of Linux commands (optional) Tools
Used AWS Management Console Amazon EC2 Key Pair Security Group SSH Client (PuTTY / Terminal)
Tasks Performed

Task 1: Explore Amazon EC2 Dashboard Explore the EC2 service dashboard in the AWS Management
Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security
Groups, and Elastic IPs.

Task 2: Launch an EC2 Instance Launch a new EC2 instance using Amazon Linux 2 AMI. Select an
appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance
name, key pair, and security group.

Task 3: Configure Security Group Configure a security group to allow inbound access:
SSH (Port 22) from your IP address HTTP (Port 80) from anywhere (0.0.0.0/0) This security group acts as
a firewall for the instance.

Task 4: Connect to EC2 Instance Connect to the running EC2 instance using SSH. Use the downloaded
key pair and connect via terminal or PuTTY.
For Amazon Linux:
ssh -i "keyname.pem" ec2-user@ 

Task 5: Perform Basic Instance Operations Perform the following
operations from the EC2 console:
Stop the instance Start the instance Reboot the instance Observe the state changes of the instance.

Task 6: Monitor EC2 Instance Monitor the EC2 instance using the Monitoring tab. Observe metrics such
as CPU utilization, network in/out, and instance status checks.

Task 7: Terminate EC2 Instance Terminate the EC2 instance after completing the experiment to avoid
unnecessary AWS charges.
Workflow (Student Explanation) (Write the steps you followed in your own words)

Output Screenshots (Attach 3) 
Screenshot 1: EC2 Dashboard / Instance List 
<img width="1920" height="1200" alt="Screenshot 2026-08-04 194706" src="https://github.com/user-attachments/assets/cad674cf-95fb-4a51-9bb2-65d786edde85" />

Screenshot 2: SSH Connection to Instance 
<img width="1920" height="1200" alt="Screenshot 2026-08-04 194617" src="https://github.com/user-attachments/assets/21d85a98-bc73-45c8-b8f8-214ebfbcfad9" />

Screenshot 3: Instance Monitoring / Status 
<img width="1920" height="1200" alt="Screenshot 2026-08-04 210422" src="https://github.com/user-attachments/assets/b34906c5-7ee5-42ac-b907-07b83eaa8a4f" />

Result: Thus, a private cloud on AWS involves using VPCs has been created for a dedicated, isolated
network where we can manage our resources and control access according to our requirements
