---
title : "Workshop 1"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---
# Deploy three-tier web app with only EC2

### Overall
In this Workshop, I will share how to use EC2 only in Public and Private Subnets to deploy a three-tier website. Details about the technology of each tier are as follows:

- Database Tier: MongoDB
- Application Tier: Fastapi - Python
- Web Tier: React - JavaScript

The article shares from creating resources on AWS to the details of deploying on each EC2.

Here is the architecture image of the Workshop:

![Architecture](/images/001.png) 

### Content
 1. [Preparation](1-Preparation) \
 2. [Create Ec2](2-Create-EC2) \
 3. [Setup Tiers](3-Setup-Tiers) \
 4. [Clean up](4-Clean-up)