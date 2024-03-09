---
title : "Tạo Internet Gateway"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 1.3. </b> "
---

1. Trong giao diện **VPC**

    - Chọn **Internet Gateways**
    - Chọn **Create internet gateway**

![VPC](/images/103/001.png)

1. Thực hiện cấu hình

    - Name tag, nhập **Internet Gateway**
    - Chọn **Create internet gateway**

![VPC](/images/103/002.png)

3. Hoàn thành tạo **Internet Gateway**

4. Thực hiện **Attach VPC**

    - Chọn **Actions**
    - Chọn **Attach to VPC**
    - Chọn **Workshop1**, VPC ID sẽ được tự động điền.
    - Chọn **Attach intermet gateway**

![VPC](/images/103/003.png)
![VPC](/images/103/004.png)

5. Khi attach thành công **State** internet gateway sẽ chuyển sang **Attached**

![VPC](/images/103/005.png)
