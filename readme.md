## Pre-requisites
### Configure firewall?
eg
    ufw default deny incoming
    ufw default allow outgoing
    ufw allow ssh
    ufw allow 80/tcp
    ufw allow 443/tcp
    ufw enable

### Install Docker and docker-compose

Install Docker (see https://docs.docker.com/install/linux/docker-ce/ubuntu/)

### Install docker-compose

Install Docker Compose (see https://docs.docker.com/compose/install/)

### Install Git
see https://git-scm.com/docs
On ubuntu

    apt install git

## Install nextcloud stack

    su -
    cd /opt
    git clone https://github.com/gridmon/nextcloud-ssl.git nextcloud

Alternatively, if you dont want to use git (handy for getting updates though) - browse to github and download a zipped copy of the project.

### Configure nextcloud env vars
Change all the your* values to suit your site ie MYSQL_DATABASE, LETSENCRYPT_EMAIL

    cd nextcloud
    vi .env

### Start nextcloud stack
    docker-compose up -d

