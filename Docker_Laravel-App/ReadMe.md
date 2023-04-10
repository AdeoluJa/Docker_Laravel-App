# **DOCKER LARAVEL APP**

## __STEPS TAKEN USING AWS EC2 INSTANCE__
<br>

### __*Install Docker*__
<li> Using the docker install process, docker and docker compose are installed on the instance.
<br>
See link below:

[Install Docker on Ubuntu 220.04](https://docs.docker.com/engine/install/ubuntu/)

[Install Docker Compose](https://docs.docker.com/compose/install/linux/)

<br>

### __*Git Clone Laraval Repo*__
<li> Using https://github.com/f1amy/laravel-realworld-example-app.git the laravel app was download to my local machine and then push to my current repo so that the Laravel app could be ran from my repo. As you can see the Laravel app is on my Repository.

<br>
<br>


### __*Edit the Web.php*__
<li> Uncomment out a few things in web.php in routes folder in the laravel app so that the laravel page will show on the browser and not a 404 page.

<br>

*See the screenshot below*
<br>
![web.php](./images/web-php.png)
<br>
<br>

### __*Create the docker folder*__
<li> Using "mkdir docker" you will create a docker file directory in the laravel app folder. Inside the folder you will create the mysql folder, nginx folder and php folder.

<br>

*See the screenshot below*
<br>
![docker folder](./images/docker.png)
<br>
<br>

### __*mysql folder*__
<li> This will house the content of the db.cnf.

<br>

*See the screenshot below*
<br>
![db.cnf](./images/db-cnf.png)
<br>
<br>

### __*nginx folder*__
<li> This will house the content of the laravel.conf.

<br>

*See the screenshot below*
<br>
![lavaral.conf](./images/laravel-conf.png)
<br>
<br>

### __*php folder*__
<li> This will house the content of the php.ini.

<br>

*See the screenshot below*
<br>
![php.ini](./images/php-ini.png)
<br>
<br>


### __*Create Dockerfile*__
<li> Contents of the Dockerfile. This file will be in the docker directory created above.

<br>

*See the screenshot below*
<br>
![Dockerfile](./images/dockerfile.png)
<br>
<br>

### __*Create .env*__
<li> Copy the .env example in the laravel app and edit the new .env file created.

<br>

*See the screenshot below of edit*
<br>
![.env](./images/db.png)
<br>
<br>

### __*Create docker-compose.yml*__
<li> Create a docker-compose.yml.

<br>

*See the content below*
<br>
![docker-compose.yml](./images/docker-compose.png)
<br>
<br>



## __Docker Commands to Run After the Above__
<br>

<li> sudo docker-compose build app
<br>

*See the output below*
<br>
![build app](./images/build-app1.png)
<br>
![build app](./images/build-app2.png)
<br>

<br>

<li> sudo docker-compose up -d
<br>

*See the output below*
<br>
![up-d](./images/up-d.png)
<br>
<br>

<li> sudo docker-compose ps
<br>

*See the output below*
<br>
![ps](./images/ps.png)
<br>
<br>

<li> sudo docker-compose exec app ls -l
<br>

*See the output below*
<br>
![ls-l](./images/ls-l.png)
<br>
<br>

<li> sudo docker-compose exec app rm -rf vendor composer.lock
<br>

<li> sudo docker-compose exec app composer install
<br>

*See the output below*
<br>
![composer install](./images/composer-install.png)
<br>
<br>

<li> sudo docker-compose exec app php artisan key:generate
<br>

*See the output below*
<br>
![artisan](./images/artisan.png)
<br>
<br>

NOTE: No migration was run on this laravel app
<br>
<br>
<br>
<br>


## __LARAVEL APP SHOWING ON IP ADDRESS__
<br>

*See the output below*
![ip Address](./images/ip.png)
<br>

<br>
