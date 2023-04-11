#  Let’s Encrypt on docker-compose


`init.sh` fetches and ensures the renewal of a Let’s
Encrypt certificate for one or multiple domains in a docker-compose
setup with nginx.

1. Clone this repository: `git clone https://github.com/wmnnd/nginx-certbot.git .`

2. Modify configuration ( Add Your domain ):
- Add domains and email addresses to init.sh
- Replace all occurrences of example.me with primary domain (the first one you added to init.sh) in data/nginx/nginx.conf

4. Run the init script:

        sudo bash init.sh

5. Run the server:

        docker-compose up 
