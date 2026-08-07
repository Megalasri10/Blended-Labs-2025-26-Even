# Lab 5 – Build a Database Server (AWS)

## Author

* **Name**: Megala M S
* **Register Number**: 212225040230

---

## Objective

The objective of this experiment is to understand how to deploy and configure a database server in AWS. This lab focuses on launching an EC2 instance, installing a database management system (DBMS), configuring basic database settings, creating a sample database, and validating connectivity to the database server.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing VPC and EC2 knowledge (from previous labs)
* Basic knowledge of Linux commands and SQL

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Security Groups
* SSH Client (Terminal / PuTTY)
* MySQL / MariaDB / PostgreSQL (any one)

---

## Tasks Performed

### Task 1: Launch EC2 Instance for Database Server

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type and configure key pair and security group.

---

### Task 2: Configure Security Group for Database Access

Modify the security group to allow:

* SSH (Port 22) for remote access
* Database port (e.g., MySQL – 3306 or PostgreSQL – 5432)

---

### Task 3: Connect to EC2 Instance

Connect to the EC2 instance using SSH from your local machine.

---

### Task 4: Install Database Server

Install a database server software such as MySQL, MariaDB, or PostgreSQL on the EC2 instance using package manager commands.

---

### Task 5: Start and Configure Database Service

Start the database service and configure basic settings such as root password and user privileges.

---

### Task 6: Create a Sample Database

Create a sample database and a table inside it. Insert a few records into the table.

---

### Task 7: Test Database Connectivity

Test the database server by connecting to it locally or remotely and performing basic SQL queries.

---

## Workflow (Student Explanation)
First, I logged in to the AWS Management Console.

I navigated to the EC2 Dashboard.

I explored the Elastic Block Store (EBS) section under EC2.

I observed different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

I clicked on “Volumes” and selected “Create Volume.”

I chose the required volume type (General Purpose SSD – gp3).

I entered the desired storage size (for example, 8 GB).

I selected the same Availability Zone as my running EC2 instance.

I clicked on “Create Volume” to create the EBS volume.

After the volume was created, I selected the volume and clicked on “Attach Volume.”

I selected my running EC2 instance and attached the volume as a new device (for example, /dev/xvdf).

I connected to my EC2 instance using SSH from the terminal.

I checked the attached disk using the command lsblk to verify the new volume.

I formatted the attached volume using the command: sudo mkfs -t ext4 /dev/xvdf

I created a directory to mount the volume using: sudo mkdir /mnt/ebs

I mounted the volume to the directory using: sudo mount /dev/xvdf /mnt/ebs

I verified that the volume was mounted successfully using the df -h command.

I created sample files inside the mounted directory using: sudo touch /mnt/ebs/sample.txt

I stored some sample data inside the file.

I rebooted the EC2 instance from the AWS Console.

After rebooting, I reconnected to the instance using SSH.

I checked the mounted directory and verified that the stored data was still available.
---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Instance for Database Server
<img width="1920" height="1200" alt="Screenshot 2026-08-06 183505" src="https://github.com/user-attachments/assets/8fd16260-b2ad-4534-bc7e-b48cef32bbba" />

---

### Screenshot 2: Database Service Running
<img width="1920" height="1200" alt="Screenshot 2026-08-06 183930" src="https://github.com/user-attachments/assets/80f13625-8a35-4ef7-90c2-cdeb004cbbf1" />


---

### Screenshot 3: Sample Database and Table
<img width="1920" height="1200" alt="Screenshot 2026-08-06 184525" src="https://github.com/user-attachments/assets/09fbeb7c-f213-44ef-b4de-41a68e253397" />

---

## Result

This experiment demonstrated how to build a database server in AWS using an EC2 instance. By installing and configuring a DBMS, creating a sample database, and testing connectivity, the fundamentals of hosting and managing a cloud-based database server were underst
