---
title : "Tạo Security Group"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 1.5. </b> "
---

1. Trong giao diện **VPC**

    - Chọn **Security Group**
    - Chọn **Cretae security group**

![VPC](/images/105/001.png)

2. Thực hiện cấu hình **Security group**

    - **Security Group name**, nhập **Public subnet - SG**
    - **Description**, nhập **Allow SSH and Ping for servers in public subnet.**
    - Chọn **Workshop1** VPC

![VPC](/images/105/002.png)

3. Thực hiện cấu hình **Inbound rules**

    - Trong **Inbound rules**, click **Add rule**
    - Chọn **Type: SSH** và **Source: My IP. My IP** đại diện cho 1 địa chỉ public IPv4 bạn đang sử dụng(sẽ thay đổi khi bạn đổi mạng)
    - Chọn **Add rule** để thêm 1 rule mới.
    - Chọn **Type: All ICMP - IPv4** và **Source: Anywhere**. Cho phép ping từ bất kì địa chỉ IP nào.

![VPC](/images/105/003.png)

4. Kiểm tra **Outbound rules** và chọn **Cretae security group**

![VPC](/images/105/004.png)

5. Hoàn thành tạo security group cho máy chủ nằm trong Public subnet

![VPC](/images/105/005.png)

### Tương tự, tạo Security Group cho máy chủ nằm trong Private subnet

![VPC](/images/105/006.png)
![VPC](/images/105/007.png)
![VPC](/images/105/008.png)
![VPC](/images/105/009.png)

6. Hoàn thành tạo security group cho máy chủ nằm trong Private subnet

![VPC](/images/105/010.png)
