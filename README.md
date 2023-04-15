#  Let’s Encrypt on docker-compose


If you're running a web application on Docker and want to secure it with SSL, Let's Encrypt is a great choice for getting a free SSL certificate. However, the process of obtaining and renewing a certificate can be tedious. This is where the init.sh script comes in.

`init.sh` fetches and ensures the renewal of a Let’s Encrypt certificate for one or multiple domains in a docker-compose setup with nginx. In this way, you can easily automate the process of obtaining and renewing SSL certificates for your web application.

## Before we begin, ensure that you have the following prerequisites:

- A domain name registered and pointed to your server's IP address
- Docker and Docker-Compose installed on your server
- Basic knowledge of Docker and Docker-Compose

1. To get started, you need to clone the repository available at `https://github.com/RishikeshOps/auto-ssl-certificate.git` Once you've cloned the repository, you need to modify the configuration as per your requirements.

2. Modify configuration 
- Add domains and email addresses to init.sh ( Add Your Domain & Email in init.sh, nginx.conf & also add your docker image in docker-compose.yml which you want to serve on domain using reverse proxy )
- Replace all occurrences of example.me with primary domain (the first one you added to init.sh) in data/nginx/nginx.conf
#### NOTE: Don't forget to change the port in the nginx.conf server block if your application is running on a different port.

3. Run the init script:

        sudo bash init.sh

- When you run this script, you will be prompted twice to select yes or no. make sure you select correctly. (YES Recommended )

###### After this you can Automate deployment by Github-Actions. Just you need to add pipline in your repo where your all code is stored and push changes in your github. You can refer this [Pipeline for building & deploying your application](https://github.com/RishikeshOps/Node-CICD-TODO/blob/master/.github/workflows/deploy.yml)

----------

In conclusion, this guide provides a complete solution for securing your domains with Let's Encrypt certificates in a Docker-Compose setup with Nginx. By following the steps outlined in this guide, you can ensure that your domains are secure and your SSL certificates are renewed automatically and continues deployment of aapplication.

Don't forget to star the repository if you found this useful :)
