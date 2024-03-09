---
title : "Create VPC"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 1.1. </b> "
---

1. Access the **AWS Management Console** interface:
    - Find **VPC**
    - Choose **VPC**

![VPC](/images/101/001.png)

2. Within the **VPC** interface:
    - Select **Yours VPC**
    - Click on **Create VPC**

![VPC](/images/101/002.png)


3. Follow these steps to create a VPC:
    - **Resource**, click **VPC only**
    - **Name tag**, as **Workshop1**
    - **IPv4 CIDR**, as **10.10.0.0/16**
    - Click **Create VPC**

![VPC](/images/101/003.png)
![VPC](/images/101/004.png)


4. Complete the process of creating the VPC

![VPC](/images/101/005.png)


5. Review the details of the newly created VPC. Ensure that Enable DNS resolution and DNS Hostname is disabled:

    - Go to **Edit VPC setting**
    - Select **DNS setting**
    - Choose and **Save**.

![VPC](/images/101/006.png)
