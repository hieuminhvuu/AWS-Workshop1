---
title : "Tạo VPC"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 1.1. </b> "
---

1. Truy cập giao diện **AWS Management Console**
    - Tìm **VPC**
    - Chọn **VPC**

![VPC](/images/101/001.png)

1. Trong giao diện **VPC**
    - Chọn **Yours VPC**
    - Chọn **Create VPC**

![VPC](/images/101/002.png)


3. Tiến hành các bước tạo VPC
    - **Resource**, chọn **VPC only**
    - **Name tag**, nhập **Workshop1**
    - **IPv4 CIDR**, nhập **10.10.0.0/16**
    - Chọn **Create VPC**

![VPC](/images/101/003.png)
![VPC](/images/101/004.png)


4. Hoàn thành tạo **VPC**

![VPC](/images/101/005.png)


5. Xem chi tiết VPC vừa tạo. Kiểm nếu chưa **Enable DNS resolution and DNS Hostname**

    - Vào **Edit VPC setting**
    - Chọn **DNS setting**
    - Chọn và **Save**.

![VPC](/images/101/006.png)
