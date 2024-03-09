---
title : "Tạo EC2"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1. </b> "
---

1. Truy cập **AWS Management Console**

    - Tìm **EC2**
    - Chọn **EC2**

![EC2](/images/201/001.png)

2. Trong giao diện **EC2**

    - Chọn **Instances**
    - Chọn Launch **instances**

![EC2](/images/201/002.png)

3. Name and tags của instance, nhập **EC2 Public - Web**

![EC2](/images/201/003.png)

4. Thực hiện chọn **AMI**

    - Chọn **Quick Start**
    - Chọn **Ubuntu Server 22.04**
    - Chọn **AMI**

![EC2](/images/201/004.png)

5. Thực hiện chọn Instance type 

![EC2](/images/201/005.png)

6. Chọn Create new key pair

![EC2](/images/201/006.png)

7. Trong giao diện **Cretae key pair**

    - **Key pair name**, nhập **Workshop1** (tên tùy chọn, bạn có thể đặt bất kỳ).
    - **Key pair type**, chọn **RSA**
    - **Private key file format**, chọn **.pem**

![EC2](/images/201/007.png)

8. Thực hiện cấu hình **Network**

    - **VPC**, chọn **Workshop1**
    - **Subnet**, chọn **Public Subnet 1**
    - **Auto-assign public IP**, chọn **Enable**
    - **Firewall (Security Group)**, chọn **Select existing security group**
    - Chọn **Public subnet - SG**
    - Chọn **Launch instance**

![EC2](/images/201/008.png)

9. Hoàn thành tạo instance

![EC2](/images/201/009.png)

10. Đợi khoảng 5 phút **Status check** sẽ chuyển sang **2/2 checks passed**

![EC2](/images/201/010.png)

### Tưởng tự, tạo EC2 nằm trong Private subnet

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

11. Hoàn thành tạo 3 instances

![EC2](/images/201/021.png)

