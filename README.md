# Scalable Web Application with Load Balancing on AWS

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazonaws)
![EC2](https://img.shields.io/badge/Amazon%20EC2-Compute-orange?logo=amazonec2)
![ALB](https://img.shields.io/badge/Application_Load_Balancer-Load_Balancing-blue)
![AutoScaling](https://img.shields.io/badge/Auto_Scaling-High_Availability-green)
![RDS](https://img.shields.io/badge/Amazon_RDS-Database-blue?logo=amazonrds)
![S3](https://img.shields.io/badge/Amazon_S3-Object_Storage-green?logo=amazons3)

## 📖 Project Overview

This project demonstrates the deployment of a **highly available and scalable web application architecture on AWS**.

The application is hosted on multiple Amazon EC2 instances running Apache and PHP. Incoming traffic is distributed across instances using an **Application Load Balancer (ALB)**, while **Auto Scaling Groups (ASG)** automatically maintain healthy instances and scale resources based on demand.

The architecture uses **Amazon RDS MySQL** as the backend database service and **Amazon S3** for storing static content such as images and uploads.

The infrastructure is designed following AWS best practices for **scalability, high availability, automation, and security**.

---

## 🏗️ Architecture Diagram

![Scalable Web Application Architecture](https://raw.githubusercontent.com/PrasannaVelanV/Scalable-Web-Application-with-Load-Balancing/main/Architecture%20Diagram%20-%20Scalable%20Web%20Application%20with%20Load%20Balancing.png)

---

## 🚀 Architecture Components

### Networking Layer

* Custom VPC
* Internet Gateway
* Public Subnets across multiple Availability Zones
* Security Groups

### Web/Application Layer

* Application Load Balancer (ALB)
* EC2 Launch Template
* Auto Scaling Group
* Apache Web Server
* PHP Application

### Database Layer

* Amazon RDS MySQL
* Private/Internal database service
* Database Security Groups

### Storage Layer

* Amazon S3 Bucket
* Static image and file storage

---

## 🛠️ AWS Services Used

| Service                   | Purpose                             |
| ------------------------- | ----------------------------------- |
| Amazon EC2                | Hosts web applications              |
| Application Load Balancer | Distributes incoming traffic        |
| Auto Scaling Group        | Automatically scales EC2 instances  |
| Launch Template           | Standardizes EC2 configuration      |
| Amazon RDS                | Backend relational database         |
| Amazon S3                 | Stores static files and images      |
| Amazon VPC                | Isolated networking environment     |
| Security Groups           | Controls network access             |
| Internet Gateway          | Enables internet connectivity       |
| Route 53                  | Concept only (ALB DNS used instead) |

---

## ✨ Features

* Highly available architecture across multiple Availability Zones
* Automatic traffic distribution using Application Load Balancer
* Automatic scaling using Auto Scaling Groups
* Health checks and automatic instance replacement
* Centralized database using Amazon RDS MySQL
* Static file hosting using Amazon S3
* Automated EC2 provisioning using Launch Templates and User Data scripts
* Secure communication using Security Groups

---

## 📂 Project Structure

```bash
Scalable-Web-Application-with-Load-Balancing/
│
├── Screenshots/
├── architecture-diagram.png
├── Scalable Web Application with Load Balancing.pdf
├── README.md
```



---

## 🔐 Security Implementation

* Web servers allow HTTP/HTTPS traffic from the Load Balancer.
* SSH access restricted to trusted IP addresses.
* RDS database access allowed only from EC2 Security Groups.
* Security Groups isolate communication between tiers.
* Database instances remain inaccessible from the public internet.

---

## ⚙️ High Availability and Scalability

This architecture ensures high availability by:

* Deploying EC2 instances across multiple Availability Zones.
* Using an Application Load Balancer to distribute traffic.
* Automatically replacing unhealthy EC2 instances.
* Dynamically scaling infrastructure based on application load.

---

## ⚙️ Prerequisites

Before deployment, ensure the following prerequisites are available:

* AWS Account
* AWS CLI configured
* IAM permissions to create AWS resources
* Basic knowledge of AWS networking concepts

---

## 🚀 Deployment Workflow

1. Create a custom VPC and public subnets.
2. Configure Internet Gateway and route tables.
3. Create Security Groups.
4. Configure Launch Template with User Data scripts.
5. Create an Auto Scaling Group.
6. Deploy EC2 instances.
7. Configure Application Load Balancer.
8. Deploy Amazon RDS MySQL.
9. Create and configure Amazon S3 bucket.
10. Access the application using the ALB DNS endpoint.

---

## 📊 Architecture Benefits

* High Availability
* Scalability
* Fault Tolerance
* Automated Recovery
* Improved Performance
* Reduced Operational Overhead

---

## 🎯 Skills Demonstrated

* AWS Networking
* Amazon EC2
* Application Load Balancer (ALB)
* Auto Scaling Groups
* Launch Templates
* User Data Automation
* Amazon RDS MySQL
* Amazon S3 Integration
* Security Groups
* High Availability Architecture
* Cloud Architecture Design

---

## 🔮 Future Enhancements

* Add Route 53 custom domain integration
* Implement HTTPS using AWS Certificate Manager (ACM)
* Deploy instances in private subnets
* Add CloudWatch monitoring and alarms
* Integrate CI/CD using GitHub Actions
* Add AWS WAF for additional security

---

## 🧹 Resource Cleanup

To avoid unnecessary AWS charges, delete the following resources when no longer required:

* Auto Scaling Group
* Launch Template
* Application Load Balancer
* EC2 Instances
* RDS Database
* S3 Bucket
* Security Groups
* VPC Resources

---

## 👨‍💻 Author

### Prasanna Velan

- GitHub: https://github.com/PrasannaVelanV
- LinkedIn: [www.linkedin.com/in/prasannavelanv](https://www.linkedin.com/in/prasanna-velan-v/)
- Portfolio: [https://github.com/PrasannaVelanV](https://prasannavelanv.netlify.app/)

---

## ⭐ Support

If you found this project useful, please consider giving this repository a star.
