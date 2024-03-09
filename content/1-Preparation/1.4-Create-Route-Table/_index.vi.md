---
title : "Tạo Route Table"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 1.4. </b> "
---

### Tạo Security Group cho máy chủ nằm trong Public subnet

1. Trong giao diện **VPC**

    - Chọn **Route Tables**
    - Chọn **Create route table**

![VPC](/images/104/001.png)

2. Tiến hành cấu hình **Route table**

    - Name, nhập **Route table-Public**
    - VPC, chọn **Workshop1** VPC. VPC id sẽ được tự động điền vào.
    - Chọn **Cretae route table**

![VPC](/images/104/002.png)

3. Hoàn thành tạo Route table

![VPC](/images/104/003.png)

4. Thực hiện **Edit route**

    - Chọn **Actions**
    - Chọn **Edit routes**

![VPC](/images/104/004.png)

5. Trong giao diện **Edit routes**

    - Chọn **Add route**
    - Điền phần **Destination CIDR** : **0.0.0.0/0** đại diện cho Internet.
    - Trong phần **Target** chọn **Internet Gateway**, sau đó chọn **Internet Gateway** chúng ta đã tạo. **Internet Gateway ID** sẽ được tự động điền.
    - Chọn **Save changes**

![VPC](/images/104/005.png)

6. Gắn 2 Public subnet vào

    - Chọn **subnet associations**
    - Chọn **Edit subnet associations**
    - Chọn đúng 2 subnet public chúng ta đã tạo
    - Chọn **Save associations**

![VPC](/images/104/006.png)
![VPC](/images/104/007.png)

7. Hoàn thành và kiểm tra lại **Subnet associations**

![VPC](/images/104/008.png)
