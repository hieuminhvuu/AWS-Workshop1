---
title : "Clean up resource"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

1. Terminate EC2 Instances

    - Access to Amazon EC2 console.
    - On the left navigator, select Intances
    - Select all EC2 Instance related to the lab.
    - Select **Instance state**
    - Select **Terminate instance**

![EC2](/images/400/001.png)
![EC2](/images/400/002.png)


2. Delete NAT Gateway 

    - Xóa NAT Gateway và Elastic IP Address. AWS sẽ thu tiền cho các EIP lãng phí nên bạn cần kiểm tra kỹ để tránh bị trừ chi phí ngoài ý muốn.
    - Access to Amazon VPC console 
    - On the left navigator, click NAT Gateway.
    - Select NAT Gateway.
    - Click Action.
    - Click Delete NAT Gateway.

![EC2](/images/400/003.png)
![EC2](/images/400/004.png)

1. Elastic IP Address

    - Delete Elastic IP Address.
    - Access to Amazon VPC console 
    - On the left navigator, click Elastic IP.
    - Select created Elastic IP Address.
    - Click Action.
    - Click Release Elastic IP Address
    - Click Release.

![EC2](/images/400/005.png)
![EC2](/images/400/006.png)

1. Delete all related Subnet 

![EC2](/images/400/007.png)
![EC2](/images/400/008.png)

5. Delete VPC

![EC2](/images/400/009.png)
![EC2](/images/400/010.png)