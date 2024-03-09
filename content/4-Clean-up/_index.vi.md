---
title : "Dọn dẹp tài nguyên"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

1. Terminate các EC2 Instance

    - Truy cập Amazon EC2 console tại địa chỉ EC2.
    - Trên thanh điều hướng bên trái, chọn Intances
    - Chọn tất cả EC2 Instance liên quan tới bài lab.
    - Chọn **Instance state**
    - Chọn **Terminate instance**

![EC2](/images/400/001.png)
![EC2](/images/400/002.png)


2. Xóa NAT Gateway 

    - Xóa NAT Gateway và Elastic IP Address. AWS sẽ thu tiền cho các EIP lãng phí nên bạn cần kiểm tra kỹ để tránh bị trừ chi phí ngoài ý muốn.
    - Truy cập trang Amazon VPC console tại địa chỉ VPC
    - Trên thanh điều hướng bên trái , click NAT Gateway.
    - Chọn NAT Gateway.
    - Click Action.
    - Click Delete NAT Gateway.

![EC2](/images/400/003.png)
![EC2](/images/400/004.png)

3. Elastic IP Address

    - Tiếp tục xóa Elastic IP Address.
    - Truy cập trang Amazon VPC console tại địa chỉ https://console.aws.amazon.com/vpc/
    - Trên thanh điều hướng bên trái , click Elastic IP.
    - Chọn Elastic IP Address chúng ta đã tạo.
    - Click Action.
    - Click Release Elastic IP Address
    - Click Release.

![EC2](/images/400/005.png)
![EC2](/images/400/006.png)

4. Xoá hết các Subnet liên quan

![EC2](/images/400/007.png)
![EC2](/images/400/008.png)

5. Xoá VPC

![EC2](/images/400/009.png)
![EC2](/images/400/010.png)