---
title : "Check connections"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.2. </b> "
---

1. Access to EC2

    - Select Instances
    - Select EC2 Public
    - Select Connect

![EC2](/images/202/001.png)

2. In the tab **Connect to instance** :
    - Select **SSH Client**
    - Copy the address sample

![EC2](/images/202/002.png)

3. Prepare the key
    - Move downloaded key to **~/.ssh** , this is the directory that specializes in storing ssh keys

![EC2](/images/202/003.png)

1. Before connect, we have to chmod 400 for key, then based on the sample ssh address in step 2, change the local key address to ssh to EC2 Public

![EC2](/images/202/004.png)

5. Try ping to internet, ping to 2 EC2 in Private Subnet

![EC2](/images/202/005.png)
![EC2](/images/202/006.png)

6. Copy the key from local to EC2 Public using the scp command, used to ssh to EC2 Private

![EC2](/images/202/007.png)

7. Check if you have received the key in EC2 public

![EC2](/images/202/008.png)

8. Before ssh, remember to chmod 400 for the key

![EC2](/images/202/009.png)

9. Use ssh key to 2 Private instances

![EC2](/images/202/010.png)
![EC2](/images/202/011.png)

10. Try pinging the internet from EC2 Private

![EC2](/images/202/012.png)

11. As a result, we cannot ping, in the next step we will configure.