---
title : "Create NAT Gateway"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.3. </b> "
---

### Create an Elastic IP

1. Access to **EC2**

    - Select **Elastic IPs**
    - Select **Allocate Elastic IP address**

![EC2](/images/203/001.png)

2. In the **Allocate Elastic IP address** interface

    - **Public IPv4 address pool**, choose **Amazon’s pool of IPv4 addresses**
    - Select **Allocate**

![EC2](/images/203/002.png)

3. We have just successfully created a Public IP Address

![EC2](/images/203/003.png)

### Create NAT Gateway

4. Access to **VPC**

    - Choose **NAT Gateways**
    - **Create NAT gateway**

![EC2](/images/203/004.png)

5. In the NAT gateway interface

    - **Name**, as **NAT gateway**
    - **Subnet**, select **Public subnet 2**
    - **Connectivity type**, select **Public**
    - **Elastic IP allocation ID**, select created **Elastic IP**.

![EC2](/images/203/005.png)

6. Select Create NAT gateway

![EC2](/images/203/006.png)
![EC2](/images/203/007.png)

### Create Route table - Private and associate private subnet

7. In the **VPC** interface

    - Select **Route Tables**
    - Select **Create route table**

![EC2](/images/203/008.png)

8. In the **Route table** interface

    - **Name**, as **Route table - Private**
    - **VPC**, as **Workshop1** vpc
    - Select **Cretae route table**

![EC2](/images/203/009.png)

9. Finish creating **Route table - Private**

![EC2](/images/203/010.png)

10. In the **Route table - Private** interface:

    - Select **Subnet Associations**
    - Select **Edit subnet associations**

![EC2](/images/203/011.png)

11. In the **Edit subnet associations** interface

    - Select 2 private subnet
    - Select **Save associations**

![EC2](/images/203/012.png)

12. In the **Route table - Private** interface

    - Select **Routes**
    - Select **Edit routes**

![EC2](/images/203/013.png)

13. In the **Edit routes** interface

    - Select **Add route**
    - Select **Destination: 0.0.0.0/0**
    - **Target**: **NAT Gateway**
    - Select **Save changes**

![EC2](/images/203/014.png)

14. Checking **Routes**

![EC2](/images/203/015.png)

15. Check whether 2 Private EC2 can ping to the internet. The results here are ok.

![EC2](/images/203/016.png)
![EC2](/images/203/017.png)
