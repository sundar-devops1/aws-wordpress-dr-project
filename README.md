# AWS WordPress Disaster Recovery (DR) Project

## Project Overview

This project demonstrates the deployment of a production-style WordPress application on AWS using Amazon EC2, Amazon RDS MySQL, Application Load Balancer (ALB), AWS Certificate Manager (ACM), and a custom domain.

The project was designed to provide secure, scalable, and highly available web hosting with HTTPS enabled and Disaster Recovery (DR) considerations.

## Live Website

https://cloudbysundar.shop

## Architecture

Internet → Custom Domain → Application Load Balancer (HTTPS) → EC2 Instance (WordPress) → Amazon RDS MySQL

A secondary DR database instance was also created to demonstrate disaster recovery planning.

## AWS Services Used

* Amazon EC2
* Amazon RDS (MySQL)
* Application Load Balancer (ALB)
* AWS Certificate Manager (ACM)
* Amazon VPC
* Security Groups
* IAM
* CloudWatch (Basic Monitoring)
* GoDaddy Domain Management

## Features Implemented

* WordPress deployment on Amazon EC2
* Amazon RDS MySQL database integration
* Custom domain configuration
* SSL/TLS certificate implementation using ACM
* HTTPS access enabled
* HTTP to HTTPS redirection
* Application Load Balancer configuration
* Secure database connectivity
* Disaster Recovery database setup
* Security Group configuration and access control

## Deployment Steps

### 1. Infrastructure Setup
	
* Created AWS networking components
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
* Documented recovery architecture

## Screenshots

Project screenshots are available in the screenshots folder.

## Security Implementations

* HTTPS enforced using ACM certificate
* Security Group-based access control
* Private database access through AWS networking
* SSL/TLS encryption for web traffic

## Skills Demonstrated

* AWS Cloud Infrastructure
* Linux Administration
* WordPress Deployment
* Amazon RDS Administration
* Load Balancing
* SSL/TLS Configuration
* DNS Management
* Disaster Recovery Planning
* Cloud Security Fundamentals

## Future Enhancements

* Auto Scaling Group
* Route 53 Integration
* CloudWatch Alarms
* Automated Backups
* Infrastructure as Code using Terraform
* CI/CD Pipeline using GitHub Actions

## Author

Sundar Muthukumarasamy
AWS & DevOps Engineer

