# Docker-Symfony

With this Docker-Symfony-Stack it's possible to setup a local development environment in seconds. Every component is selected for running Symfony 6 in a flavored way.
Currently it has only .env configuration for MariaDB but as soon as possible it'll have also for others such as MySQL and PostgreSQL.

## Getting started
Copy the .env.dist file and edit the entries to your needs:
```
cp .env.dist .env
```

Only start docker-compose to start your environment:
```
docker-compose up
```

After booting the container, you can use composer and the symfony cli insight the php-apache container:
```
docker exec -it my_symfony-apache-php bash
symfony check:requirements
composer create-project symfony/skeleton ./
```

## Installed Packages
You have three container running: Apache-PHP, MariaDB and Adminer.
- [Web-App](http://localhost)
- [Adminer](http://localhost:8080)
