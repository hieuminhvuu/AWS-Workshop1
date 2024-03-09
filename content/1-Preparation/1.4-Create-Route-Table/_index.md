---
title : "Create Route Table"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 1.4. </b> "
---

### Create Security Group for instance in Public subnet

1. In **VPC** interface

    - Select **Route Tables**
    - Select **Create route table**

![VPC](/images/104/001.png)

2. Implement **Route table**

    - Name, as **Route table-Public**
    - VPC, choose **Workshop1** VPC. VPC id will be auto-fill.
    - Select **Cretae route table**

![VPC](/images/104/002.png)

3. Finish creating Route table

![VPC](/images/104/003.png)

4. Implement **Edit route**

    - Select **Actions**
    - Select **Edit routes**

![VPC](/images/104/004.png)

5. In **Edit routes** interface

    - Select **Add route**
    - **Destination CIDR** as **0.0.0.0/0** representing the Internet
    - In the **Target** section, select **Internet Gateway**, then select the created **Internet Gateway**. **Internet Gateway ID** will be auto-fill.
    - Select **Save changes**

![VPC](/images/104/005.png)

1. Associate 2 Public subnet 

    - Select **subnet associations**
    - Select **Edit subnet associations**
    - Select the created 2 subnets public 
    - Select **Save associations**

![VPC](/images/104/006.png)
![VPC](/images/104/007.png)

7. Finish and review **Subnet associations**

![VPC](/images/104/008.png)
