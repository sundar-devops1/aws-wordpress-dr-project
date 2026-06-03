# AWS WordPress Disaster Recovery (DR) Project

## Project Overview

This project demonstrates the deployment of a production-style WordPress application on AWS using Amazon EC2, Amazon RDS MySQL, Application Load Balancer (ALB), AWS Certificate Manager (ACM), and a custom domain.

The project was designed to provide secure, scalable, and highly available web hosting with HTTPS enabled and Disaster Recovery (DR) considerations.

## Live Website

https://cloudbysundar.shop

## Architecture

Internet → Custom Domain → Application Load Balancer (HTTPS) → Amazon EC2 (WordPress) → Amazon RDS MySQL

A secondary DR database instance was also created to support disaster recovery planning and documentation.

## AWS Services Used

* Amazon EC2
* Amazon RDS (MySQL)
* Application Load Balancer (ALB)
* AWS Certificate Manager (ACM)
* Amazon VPC
* Security Groups
* IAM
* GoDaddy Domain Management

## Features Implemented

* WordPress deployment on Amazon EC2
* Amazon RDS MySQL integration
* Custom domain configuration
* SSL/TLS certificate implementation using ACM
* HTTPS enabled website access
* HTTP to HTTPS redirection
* Application Load Balancer configuration
* Secure connectivity between WordPress and RDS
* Disaster Recovery (DR) database setup
* Linux cron-based backup automation

## Backup Automation

As part of the Disaster Recovery strategy, automated backups were implemented using Linux Cron.

### Cron Job Configuration

```bash
0 2 * * * tar -czf /home/ec2-user/backups/wordpress-$(date +\%F).tar.gz /var/www/html
```

### Backup Process

* Runs daily at 2:00 AM
* Compresses the WordPress web directory
* Stores backup archives in `/home/ec2-user/backups`
* Supports recovery of website files in case of failure

## Deployment Steps

### 1. Infrastructure Setup

* Created VPC networking environment
* Configured Security Groups
* Launched Amazon EC2 instance

### 2. WordPress Installation

* Installed Apache, PHP, and required packages
* Downloaded and configured WordPress
* Connected WordPress to Amazon RDS

### 3. Database Setup

* Created Amazon RDS MySQL instance
* Configured database connectivity
* Created WordPress database

### 4. Load Balancer Setup

* Created Application Load Balancer
* Configured Target Group
* Registered EC2 instance
* Verified target health checks

### 5. Domain and SSL Configuration

* Purchased custom domain
* Configured DNS records
* Requested ACM certificate
* Completed DNS validation
* Enabled HTTPS listener
* Configured HTTP to HTTPS redirection

### 6. Disaster Recovery Planning

* Created DR database instance
* Implemented automated backup scheduling using Cron
* Documented recovery architecture

## Screenshots

Project screenshots are available in the screenshots folder.

## Security Implementations

* HTTPS enforced using ACM certificate
* Security Group-based access control
* SSL/TLS encryption for web traffic
* Restricted SSH access using security groups

## Skills Demonstrated

* AWS Cloud Infrastructure
* Linux Administration
* WordPress Deployment
* Amazon RDS Administration
* Load Balancing
* SSL/TLS Configuration
* DNS Management
* Disaster Recovery Planning
* Backup Automation
* Cloud Security Fundamentals

## Future Enhancements

* Amazon S3 backup storage
* Auto Scaling Group
* Route 53 integration
* CloudWatch monitoring and alarms
* Infrastructure as Code using Terraform
* CI/CD Pipeline using GitHub Actions

## Author

Sundar Ayyappan M
AWS & DevOps Engineer
