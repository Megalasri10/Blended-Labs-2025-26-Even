# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: Megala M S
* **Register Number**: 212225040230
---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)

1.First, I logged in to the AWS Management Console using my AWS account.

2.I searched for EC2 in the services section and opened the EC2 Dashboard.

3.I explored different sections like Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs to understand their functions.

4.I clicked on the “Launch Instance” button to create a new EC2 instance.

5.I selected Amazon Linux 2 AMI as the operating system.

6.I chose the t2.micro instance type because it is eligible for the AWS Free Tier.

7.I entered a name for my instance to identify it easily.

8.I created a new key pair, selected the PEM format, and downloaded it to my system.

9.I configured the security group settings.

10.I allowed SSH access on Port 22 only from my IP address.

11.I allowed HTTP access on Port 80 from anywhere (0.0.0.0/0).

12.I reviewed all the configurations and clicked on “Launch Instance.”

13.After launching, I waited until the instance state changed to “Running.”

14.I copied the public IP address of the instance from the EC2 dashboard.

15.I opened the terminal and navigated to the folder where the key pair file was saved.

16.I connected to the instance using the SSH command: ssh -i "keyname.pem" ec2-user@

17.I successfully logged in to the Amazon Linux server.

18.I went back to the EC2 console and selected the instance.

19.I clicked on “Stop” and observed the instance state changing to “Stopped.”

20.I clicked on “Start” and observed the state changing back to “Running.”

21.I also performed the “Reboot” operation and noticed that the instance restarted.

22.I opened the “Monitoring” tab to check CPU utilization and network metrics.

23.I observed the status checks to ensure the instance was running properly.

24.After completing the experiment, I selected the instance and clicked on “Terminate.”

25.I confirmed the termination and observed that the instance state changed to “Terminated.”

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List
<img width="1920" height="1200" alt="Screenshot 2026-08-04 194110" src="https://github.com/user-attachments/assets/15b79a83-284d-4297-8b60-57206da8b9eb" />
<img width="941" height="1007" alt="Screenshot 2026-08-04 194353" src="https://github.com/user-attachments/assets/fe0a3269-c20f-4e84-9910-b279ddbf6ea9" />

---

### Screenshot 2: SSH Connection to Instance
<img width="1920" height="1200" alt="Screenshot 2026-08-04 194617" src="https://github.com/user-attachments/assets/f7f38b05-1e95-4686-b39d-2a15d7f7b83d" />
<img width="1920" height="1200" alt="Screenshot 2026-08-04 194706" src="https://github.com/user-attachments/assets/6b7d0dd4-d32b-414b-b7f1-9c125bb92081" />
<img width="944" height="504" alt="image" src="https://github.com/user-attachments/assets/c67b7f3c-5932-4403-98ba-b64f8ff791f6" />



---

### Screenshot 3: Instance Monitoring / Status
<img width="1920" height="1200" alt="Screenshot 2026-08-04 210012" src="https://github.com/user-attachments/assets/d4c2166a-7226-41d4-a7dd-d6db8970e86f" />
<img width="1920" height="1200" alt="Screenshot 2026-08-04 210422" src="https://github.com/user-attachments/assets/e84cd9b5-9a44-44fe-9f12-3264d2515c1d" />


---

## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
