# AWS Cloud Practitioner – EC2 Web Server & SFTP Configuration

## Project Overview

This project demonstrates how to deploy and configure cloud infrastructure using Amazon Web Services. The objective is to create Windows and Linux virtual servers, configure web servers, assign Elastic IP addresses, and enable secure file transfer using SFTP.

## Technologies & Services Used

* Amazon EC2
* Elastic IP
* Windows Server
* IIS Web Server
* Linux (Amazon Linux)
* Apache Web Server
* SSH
* SFTP

---

# Project Tasks

## 1. Create Windows EC2 Instance

A Windows Server instance was launched using Amazon EC2.

### Steps

1. Login to AWS Management Console
2. Navigate to EC2 Dashboard
3. Launch a new instance
4. Select Windows Server AMI
5. Choose instance type (t2.micro)
6. Configure security group with RDP access
7. Launch the instance

### Result

Successfully created and connected to Windows EC2 instance using Remote Desktop.

---

## 2. Configure IIS Web Server

Internet Information Services (IIS) was installed on the Windows server.

### Steps

1. Connect to the Windows instance using RDP
2. Open Server Manager
3. Add Roles and Features
4. Select Web Server (IIS)
5. Install IIS

### Result

IIS web server was successfully installed and the default web page was accessible.

---

## 3. Configure Elastic IP for Windows Server

Elastic IP was allocated and associated with the Windows EC2 instance.

### Steps

1. Navigate to Elastic IP in EC2 dashboard
2. Allocate new Elastic IP
3. Associate the Elastic IP with the Windows instance

### Result

The web server can be accessed using a static public IP.

---

## 4. Create Linux EC2 Instance

A Linux server was launched using Amazon Linux.

### Steps

1. Launch EC2 instance
2. Select Amazon Linux AMI
3. Configure security group (SSH & HTTP)
4. Launch instance with key pair

### Result

Successfully connected to the instance using SSH.

---

## 5. Configure Apache Web Server

Apache HTTP Server was installed on the Linux instance.

### Commands Used

```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```

### Result

Apache web server started successfully and the default webpage was accessible via browser.

---

## 6. Configure Elastic IP for Linux Server

Elastic IP was assigned to the Linux EC2 instance.

### Result

The Apache web server became accessible using the static Elastic IP address.

---

## 7. Configure SFTP for Secure File Transfer

A new user was created for secure file transfer using SFTP.

### Commands Used

```bash
sudo adduser sftpuser
sudo passwd sftpuser
```

Files were uploaded using an SFTP client.

### Result

Files were successfully uploaded to the server using SFTP.

---

# Testing

* Verified web server accessibility through browser.
* Confirmed file uploads using SFTP.
* Checked file presence using Linux terminal commands.

---

# Project Outcome

This project successfully demonstrated:

* Cloud instance deployment
* Web server configuration
* Static IP assignment
* Secure file transfer
* Basic cloud infrastructure management

---

# Author

Student: (Your Name)
Course: AWS Cloud Practitioner Training
Institution: Sri Eshwar College of Engineering
Trainer: Aravindraj G
