---
title : "Application Tier"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2. </b> "
---

1. First, we need zip code then copy to EC2 Public

![EC2](/images/302/001.png)

2. Check received or not

![EC2](/images/302/002.png)

3. Copy backend.zip to EC2 Private - Application

![EC2](/images/302/003.png)

4. SSH to EC2 Private - Application and check
![EC2](/images/302/004.png)

5. Install unzip then unzip backend.zip

![EC2](/images/302/005.png)
![EC2](/images/302/006.png)

6. Create user backend, create directory /projects and move folder backend to

![EC2](/images/302/008.png)

7. chown, chmod folder backend, check

![EC2](/images/302/009.png)

8. Install python, pip, venv

![EC2](/images/302/010.png)
![EC2](/images/302/011.png)
![EC2](/images/302/012.png)

9. Create virtualenv - environment for python to run the project, then activate this virtual environment

![EC2](/images/302/014.png)

10. Install project's dependencies  

```
pip install -r requirements.txt
```

![EC2](/images/302/015.png)


11. Change ip database to Database tier's ip

![EC2](/images/302/017.png)
![EC2](/images/302/016.png)


12. Run project, error with database

![EC2](/images/302/018.png)

13. Change Security Group Private Subnet, add rule TCP port 27017 of MongoDB

![EC2](/images/302/025.png)

14. Run project again, successful 

![EC2](/images/302/019.png)

15. Then, we use nginx as revert proxy for backend, install

![EC2](/images/302/020.png)

16. Create a new file, name as fastapi_nginx in the direct : /etc/nginx/sites-enabled/ , has this content :

![EC2](/images/302/021.png)

17. Checking syntax of nginx and restart 

![EC2](/images/302/022.png)

18. Restart project, now nginx is running as revert proxy, forward request from port 80 to port 8000.

![EC2](/images/302/024.png)