---
title : "Create Subnet"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 1.2. </b> "
---

1. In the VPC Interface:

    - Select **Subnets**
    - Select **Create subnet**

![VPC](/images/102/001.png)


1. In the **Create subnet** interface:

    - Select **Workshop1** VPC
    - Subnet name, as **Public Subnet 1**
    - Choose AZ **eu-north-1a**
    - IPv4 CIDR block, as **10.10.1.0/24** according to the architecture description
    - Select **Create subnet**

![VPC](/images/102/002.png)
![VPC](/images/102/003.png)

3. Finish Creating **subnet**

![VPC](/images/102/004.png)

1. Same, create 3 more **subnet** 
    - **Public subnet 2** với CIDR là **10.10.2.0/24** nằm trong Availability Zone **eu-north-1b**
    - **Private subnet 1** với CIDR là **10.10.3.0/24** nằm trong Availability Zone **eu-north-1a**
    - **Private subnet 2** với CIDR là **10.10.4.0/24** nằm trong Availability Zone **eu-north-1a**

![VPC](/images/102/005.png)

5. In **VPC** interface

    - Select **Subnets**
    - Select **Public Subnet 1**
    - Select **Actions**
    - Select **Edit subnet settings**

![VPC](/images/102/006.png)

6. Under **Auto-assign IP settings**

    - Select **Enable auto-assign publi IPv4 address**
    - Select **Save**

![VPC](/images/102/007.png)
![VPC](/images/102/008.png)

7. Same with **Public subnet 2**.

![VPC](/images/102/009.png)