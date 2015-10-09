Description
=====
A template project for running Symfony2 in Docker.

Usage
=====

Create a new git repo, add this as a git submodule.

Your directory structure should look like:

```
./SymfonyDockerTemplate/
./symfony/ # project files go here
```

To run everything:

```
cd ./SymfonyDockerTemplate
docker-compose up
```

To enter the setup with bash (after the containers are running):

```
sudo docker exec -it $(sudo docker ps -f name=php -q) bash
```

To initialise a new project:

```
cd ./symfony
wget https://getcomposer.org/composer.phar
sudo docker exec -it $(sudo docker ps -f name=php -q) bash
cd /var/www/symfony
composer create-project symfony/framework-standard-edition my_project_name
```

Credits
=====

http://vincent.composieux.fr/article/run-a-symfony-application-using-docker-and-docker-compose
