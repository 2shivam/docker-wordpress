# docker-wordpress
This repo contains Docker file for WordPress instance setup on local system using docker container.
Create a folder wp-docker.
Create a docker-compose.yaml file.
The WordPress environment which we are setting up contains three Docker services listed below:
 1. A service for providing and serving WordPress
 2. A service for the MySQL database
 3. A service for providing and serving phpMyAdmin
Inside the services section we’ve added the first service definition which is named wordpress.
The volumes property is used to mount to container directory /var/www/html/wp-content to the local folder wp-content. Everything which is inserted into the local folder will be made available in the corresponding container folder. If you want to install a backup of any existing website you can just copy the content of the wp-content folder from your production WP installation to the local wp-content folder to make it available to that WorkPress instance.
As a second service we’ve added db to our Docker setup.
As a third service we’re adding phpMyAdmin to our Docker setup.
To start the this services "docker-compose up".
To run these services in detached mode run"docker-compose up -d".
To stop services run "docker-compose stop".
To start services again run "docker-compose start".
To stop and remove services run "docker-compose down".
To stop and remove services and also remove the volumes created run "ocker-compose down --volumes".
To access wordpress open the url "http://localhost:8080". 
To access myphpadmin open the url "http://localhost:3333".
