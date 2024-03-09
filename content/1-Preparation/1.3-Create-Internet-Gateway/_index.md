---
title : "Create Internet Gateway"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 1.3. </b> "
---

1. In the **VPC** interface

    - Select **Internet Gateways**
    - Select **Create internet gateway**

![VPC](/images/103/001.png)

1. Configure

    - Name tag, as **Internet Gateway**
    - Select **Create internet gateway**

![VPC](/images/103/002.png)

3. Finish creating **Internet Gateway**

4. Implement **Attach VPC**

    - Select **Actions**
    - Select **Attach to VPC**
    - Select **Workshop1**, VPC ID sẽ được tự động điền.
    - Select **Attach intermet gateway**

![VPC](/images/103/003.png)
![VPC](/images/103/004.png)

5. Once attached successfully, the State of the internet gateway will change to Attached

![VPC](/images/103/005.png)
