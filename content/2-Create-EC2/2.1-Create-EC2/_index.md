---
title : "Create EC2"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1. </b> "
---

1. Access to **AWS Management Console**

    - Find **EC2**
    - Choose **EC2**

![EC2](/images/201/001.png)

2. In the **EC2** interface

    - Chọn **Instances**
    - Chọn Launch **instances**

![EC2](/images/201/002.png)

3. Name and tags của instance, as **EC2 Public - Web**

![EC2](/images/201/003.png)

4. ImpleSelect **AMI**

    - Select **Quick Start**
    - Select **Ubuntu Server 22.04**
    - Select **AMI**

![EC2](/images/201/004.png)

5. Implement Instance type 

![EC2](/images/201/005.png)

6. Select Create new key pair

![EC2](/images/201/006.png)

7. In the **Cretae key pair** interface

    - **Key pair name**, as **Workshop1** (Optional name, you can set any).
    - **Key pair type**, as **RSA**
    - **Private key file format**, choose **.pem**

![EC2](/images/201/007.png)

8. Implement **Network**

    - **VPC**, Select **Workshop1**
    - **Subnet**, Select **Public Subnet 1**
    - **Auto-assign public IP**, Select **Enable**
    - **Firewall (Security Group)**, Select **Select existing security group**
    - Select **Public subnet - SG**
    - Select **Launch instance**

![EC2](/images/201/008.png)

9. Finish creating instance

![EC2](/images/201/009.png)

10. Wait about 5 minutes **Status check** will be turn **2/2 checks passed**

![EC2](/images/201/010.png)

### Same the way, create EC2 in Private subnet

![EC2](/images/201/011.png)
![EC2](/images/201/012.png)
![EC2](/images/201/013.png)
![EC2](/images/201/014.png)
![EC2](/images/201/015.png)
![EC2](/images/201/016.png)
![EC2](/images/201/017.png)
![EC2](/images/201/018.png)
![EC2](/images/201/019.png)
![EC2](/images/201/020.png)

11. Finish creating 3 instances

![EC2](/images/201/021.png)

