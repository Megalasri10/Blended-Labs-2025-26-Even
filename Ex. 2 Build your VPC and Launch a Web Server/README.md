# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: Megala M S
* **Register Number**: 212225040230

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

1.Create a VPC with a suitable IPv4 CIDR block, such as 10.0.0.0/16.

2.Create a public subnet inside the VPC, such as 10.0.1.0/24.

3.Create and attach an Internet Gateway (IGW) to the VPC to provide internet connectivity.

4.Create a route table and add a route 0.0.0.0/0 through the Internet Gateway.

5.Associate the route table with the public subnet.

6.Launch an EC2 instance in the public subnet and enable a public IPv4 address.

7.Configure the security group to allow SSH (port 22) and HTTP (port 80) traffic.

8.Connect to the EC2 instance using SSH or EC2 Instance Connect.

9.Install and start the Apache HTTP web server on the EC2 instance.

10.Create a simple HTML webpage and place it in the Apache web server's document directory.

11.Access the webpage using the EC2 instance's public IPv4 address in a web browser.

12.Verify the output and capture screenshots of the VPC/subnet, running EC2 instance, and web server webpage.
---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details
<img width="1920" height="1200" alt="Screenshot 2026-08-04 182121" src="https://github.com/user-attachments/assets/d695cbb2-e31e-454d-ab94-990c2d8f39cf" />
<img width="1920" height="1200" alt="Screenshot 2026-08-04 182404" src="https://github.com/user-attachments/assets/f2a98cf1-1a45-4a0a-a63d-70417cff018e" />
<img width="1920" height="1200" alt="Screenshot 2026-08-04 182525" src="https://github.com/user-attachments/assets/79f96956-2a94-4d52-911c-30e8dc997643" />

---

### Screenshot 2: EC2 Instance Running
<img width="1920" height="1200" alt="Screenshot 2026-08-04 182632" src="https://github.com/user-attachments/assets/65e35b75-5123-4c8a-83f9-ce89a9a90440" />
<img width="1920" height="1200" alt="Screenshot 2026-08-04 182727" src="https://github.com/user-attachments/assets/0790e8ca-c56a-4f38-93bb-8c2251756654" />
<img width="1920" height="1200" alt="Screenshot 2026-08-04 183313" src="https://github.com/user-attachments/assets/a70e316b-7dab-4ded-be37-fe321374fea1" />
<img width="1920" height="1200" alt="Screenshot 2026-08-04 183648" src="https://github.com/user-attachments/assets/25ab8ea5-509f-46c0-b5f3-aa3d5a188150" />


---

### Screenshot 3: Web Server Output in Browser
<img width="1311" height="657" alt="image" src="https://github.com/user-attachments/assets/8ee3bd8c-0edc-437d-b779-22dc7f3861ba" />

---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
