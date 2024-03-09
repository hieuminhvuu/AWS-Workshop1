---
title : "Tạo NAT Gateway"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.3. </b> "
---

### Tạo một địa chỉ Elastic IP

1. Truy cập **EC2**

    - Chọn **Elastic IPs**
    - Chọn **Allocate Elastic IP address**

![EC2](/images/203/001.png)

2. Trong giao diện **Allocate Elastic IP address**

    - **Public IPv4 address pool**, chọn **Amazon’s pool of IPv4 addresses**
    - Chọn **Allocate**

![EC2](/images/203/002.png)

3. Chúng ta vừa tạo thành công một địa chỉ Public IP Address

![EC2](/images/203/003.png)

### Tạo NAT Gateway

4. Truy cập vào **VPC**

    - Chọn **NAT Gateways**
    - **Create NAT gateway**

![EC2](/images/203/004.png)

5. Trong giao diện NAT gateway

    - **Name**, nhập **NAT gateway**
    - **Subnet**, chọn **Public subnet 2**
    - **Connectivity type**, chọn **Public**
    - **Elastic IP allocation ID**, chọn **Elastic IP** vừa tạo.

![EC2](/images/203/005.png)

6. Chọn Create NAT gateway

![EC2](/images/203/006.png)
![EC2](/images/203/007.png)

### Tạo Route table - Private và gáng vào các private subnet

7. Trong giao diện **VPC**

    - Chọn **Route Tables**
    - Chọn **Create route table**

![EC2](/images/203/008.png)

8. Trong giao diện **Route table**

    - **Name**, nhập **Route table - Private**
    - **VPC**, chọn **Workshop1** vpc
    - Chọn **Cretae route table**

![EC2](/images/203/009.png)

9. Hoàn thành tạo **Route table - Private**

![EC2](/images/203/010.png)

10. Trong giao diện **Route table - Private**

    - Chọn **Subnet Associations**
    - Chọn **Edit subnet associations**

![EC2](/images/203/011.png)

11. Trong giao diện **Edit subnet associations**

    - Chọn 2 private subnet
    - Chọn **Save associations**

![EC2](/images/203/012.png)

12. Trong giao diện **Route table - Private**

    - Chọn **Routes**
    - Chọn **Edit routes**

![EC2](/images/203/013.png)

13. Trong giao diện **Edit routes**

    - Chọn **Add route**
    - Chọn **Destination: 0.0.0.0/0**
    - **Target**: **NAT Gateway**
    - Chọn **Save changes**

![EC2](/images/203/014.png)

14. Kiểm tra lại **Routes**

![EC2](/images/203/015.png)

15. Kiểm tra từ 2 Private EC2 đã ping ra internet được chưa. Kết quả ở đây đã ok.

![EC2](/images/203/016.png)
![EC2](/images/203/017.png)
