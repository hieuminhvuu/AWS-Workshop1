---
title : "Tạo Subnet"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 1.2. </b> "
---

1. Trong giao diện **VPC**

    - Chọn **Subnets**
    - Chọn **Create subnet**

![VPC](/images/102/001.png)


1. Trong giao diện **Create subnet**

    - Chọn **Workshop1** VPC
    - Subnet name, nhập **Public Subnet 1**
    - Chọn AZ **eu-north-1a**
    - IPv4 CIDR block, nhập **10.10.1.0/24** theo kiến trúc mô tả
    - Chọn **Create subnet**

![VPC](/images/102/002.png)
![VPC](/images/102/003.png)

3. Hoàn thành tạo **subnet**

![VPC](/images/102/004.png)

4. Tương tự, tạo thêm 3 **subnet** nữa
    - **Public subnet 2** với CIDR là **10.10.2.0/24** nằm trong Availability Zone **eu-north-1b**
    - **Private subnet 1** với CIDR là **10.10.3.0/24** nằm trong Availability Zone **eu-north-1a**
    - **Private subnet 2** với CIDR là **10.10.4.0/24** nằm trong Availability Zone **eu-north-1a**

![VPC](/images/102/005.png)

5. Trong giao diện **VPC**

    - Chọn **Subnets**
    - Chọn **Public Subnet 1**
    - Chọn **Actions**
    - Chọn **Edit subnet settings**

![VPC](/images/102/006.png)

6. Trong mục **Auto-assign IP settings**

    - Chọn **Enable auto-assign publi IPv4 address**
    - Chọn **Save**

![VPC](/images/102/007.png)
![VPC](/images/102/008.png)

7. Sau đó thực hiện tương tự với **Public subnet 2**.

![VPC](/images/102/009.png)