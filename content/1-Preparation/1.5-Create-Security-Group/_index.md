---
title : "Create Security Group"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 1.5. </b> "
---

1. In the **VPC** interface:

    - Select **Security Group**
    - Select **Cretae security group**

![VPC](/images/105/001.png)

2. Implement **Security group**

    - **Security Group name**, as **Public subnet - SG**
    - **Description**, as **Allow SSH and Ping for servers in public subnet.**
    - Choose **Workshop1** VPC

![VPC](/images/105/002.png)

3. Implement **Inbound rules**

    - Within **Inbound rules**, click **Add rule**
    - Select **Type: SSH** and **Source: My IP. (Use your public IPv4 address)
    - Select **Add rule** to add new rule.
    - Select **Type: All ICMP - IPv4** và **Source: Anywhere**. Accept ping from anywhere.

![VPC](/images/105/003.png)

4. Check **Outbound rules** and select **Cretae security group**

![VPC](/images/105/004.png)

5. Complete the creation of the security group for the server located in the Public subnet

![VPC](/images/105/005.png)

### Same the way, create Security Group for instance in Private subnet

![VPC](/images/105/006.png)
![VPC](/images/105/007.png)
![VPC](/images/105/008.png)
![VPC](/images/105/009.png)

6. Complete the creation of the security group for the server located in the Private subnet

![VPC](/images/105/010.png)