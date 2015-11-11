# docker-drupal

A drupal development environment

This repository contains a docker-compose.yml file that will deploy some containers that I find usefull for drupal development.
It includes the following services:

* drupal: Image with apache, drush, cron and nullmailer. It runs at port 8080
* mariadb: Image with the mariadb
* phpmyadmin: Image with phpmyadmin. It runs at port 8081
* mailcatcher: Image with mailcatcher. it runs at port 9999


# Installation:

1. Add your drupal files in the www/ directory. 
2. Create a settings.php files with the mysql creadentials found in the docker-compose.yml 
3. Run docker-compose up -d to start the containers
4. The db files will be created in the db/ directory
5. All outgoing emails will be delivered to the mailcather. You can acceess mailcatcher from your browser.


# Contents

It uses the following images:
* https://hub.docker.com/r/msti/drupal/
* https://hub.docker.com/_/mariadb/
* https://hub.docker.com/r/nazarpc/phpmyadmin/
* https://hub.docker.com/r/zolweb/docker-mailcatcher/
