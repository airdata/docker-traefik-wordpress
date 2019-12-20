# Docker: Wordpress
Dockerfile for Wordpress with mSMTP client.

docker-compose file includes:
 - Traefik 
 - Wordpress
 - MariaDB
 - Adminer
 - Backup

## Setup
1. clone the repo
2. edit .env file
3. create msmtp/msmtprc from provided msmtprc.example

## Network settings:
The stack is divided into two networks, backend and frontend.

the idea behind splitting the stack into two networks
is to block the access of the reverse proxy to the backend containers.

both networks are unique and will be named with stackname_networname such as:

- docker-wordpress_backend
- docker-wordpress_frontend


Author: [Airdata][Airdata].

[Airdata]: https://rumen-lishkov.com