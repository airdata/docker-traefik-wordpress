# Docker: Wordpress
 [![CircleCI](https://img.shields.io/circleci/project/github/airdata/docker-traefik-wordpress.svg)](https://circleci.com/gh/airdata/docker-traefik-wordpress) 

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

## Run 
```
docker-compose up -d
```

## Endpoints
### Traefik Dashboard
http://traefik-wordpress.docker.localhost:8080/dashboard

### Wordpress
http://wordpress.docker.localhost

### Adminer - DB GUI
http://adminer.wordpress.docker.localhost

## Network settings:
The stack is divided into two networks, backend and frontend.

The idea behind splitting the stack into two networks
is to block the access of the reverse proxy to the backend containers. \
Both networks are unique and will be named with stackname_networname such as: \

- docker-traefik-wordpress_backend
- docker-traefik-wordpress_backend


Author: [Airdata][Airdata].

[Airdata]: https://rumen-lishkov.com