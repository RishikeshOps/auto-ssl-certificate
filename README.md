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

With these simple steps, you can secure your web application running on Docker with Let's Encrypt SSL certificates.

Don't forget to star the repository if you found this useful :)
