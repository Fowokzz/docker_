# docker_

deploy laravel app with docker.

I completed this project with the follwoing steps:

1. Install docker for Ubuntu using the convenient script here https://docs.docker.com/engine/install/ubuntu/ then installed docker compose with the commands below right after right after sudo apt-get update sudo apt-get install docker-compose-plugin

2. Cloned the Laravel project repository from https://github.com/f1amy/laravel-realworld-example-app

3. Edit the docker-compose file then create a docker folder in the app directory where Dockerfile is created

4. In this current repository, run docker-compose up -d to build images and create the containers.

To confirm that the endpoints were working fine , run docker exec -it php-container-id sh (replace "php-container-id" with the name of your php container id) and typed in the following commands in the container

php artisan key:generate
php artisan migrate
php artisan config:cache
php artisan migrate:fresh

Deploy the container on a digital ocean droplet and assigned IP Address: 178.62.34.46
