---
title : "Web Tier"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3. </b> "
---

1. Install unzip and unzip code from file frontend.zip

![EC2](/images/303/001.png)
![EC2](/images/303/002.png)

2. Same as Application Tier, we also create a directory and user for the frontend project

![EC2](/images/303/003.png)
![EC2](/images/303/004.png)

3. Change the backend url to the ip of Application tier EC2

![EC2](/images/303/005.png)
![EC2](/images/303/006.png)

4. Install node, npm

5. Install nginx

![EC2](/images/303/007.png)
![EC2](/images/303/008.png)

6. Build the project, after the build is completed, a folder named **build** will be created

```
npm run build
```

![EC2](/images/303/009.png)

7. Use nginx as a web server: create an nginx file named react.conf at the path **/etc/nginx/conf.d/**. Add content (like photos). Then restart nginx

![EC2](/images/303/010.png)
![EC2](/images/303/011.png)
![EC2](/images/303/012.png)


8. Use nginx to revert the proxy: create a file named react_nginx at the path **/etc/nginx/sites-enabled/ with the content:

![EC2](/images/303/013.png)

9. Open additional HTTP port 80 of Security Group - Public subnet

![EC2](/images/303/018.png)

10. nginx will forward requests from port 80 to port 3000 running the project, now access the project using the EC2 Public ip

![EC2](/images/303/014.png)

11. Error 500. This error occurs because we have not granted permission to another user to access the **build** folder. We just need to check which user nginx is, here it is www-data, then add it to the group **frontend**

![EC2](/images/303/015.png)
![EC2](/images/303/016.png)

12. Done, our website is already working via EC2's IP port 80.

![EC2](/images/303/017.png)