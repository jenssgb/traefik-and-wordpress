# Traefik and Wordpress
A simple compose script wich will allow you to run traefik and wordpress with MySQL and docker.

# Replace the following strings
      

Traefik Container:

      - "--certificatesresolvers.myresolver.acme.email=<<<<< PLEASE ADD >>>>>>"


Wordpress Container:

      WORDPRESS_DB_USER: <<<<< PLEASE ADD >>>>>> 
      WORDPRESS_DB_PASSWORD: <<<<< PLEASE ADD >>>>>> 
      WORDPRESS_DB_NAME: <<<<< PLEASE ADD >>>>>> 
      
      - "traefik.http.routers.whoami.rule=Host(`<<<<< PLEASE ADD YOUR DOMAIN>>>>>>`)"
      
Database Container:

      MYSQL_DATABASE: <<<<< PLEASE ADD >>>>>> 
      MYSQL_USER: <<<<< PLEASE ADD >>>>>> 
      MYSQL_PASSWORD: <<<<< PLEASE ADD >>>>>> 
      
      
