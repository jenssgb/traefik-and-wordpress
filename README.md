# Traefik and Wordpress
A simple compose script wich will allow you to run traefik and wordpress with MySQL and docker.

# Please note
- This is for lab and testing purposes only.
- For safety reasons it is absolutely necessary to deal with all elements in detail.  

# How to use:
- Register a domain 
- Add the IP Adress of your Linux Server to the Domain DNS A-Record
- Open Port 80 (HTTP) 443 (HTTPS) & 8080 (Traefig UI) to your Server inbound
- Clone the Code to your Linux Server 
- Check if docker and docker compose is installed 
- Change the strings (See below) 
- Start the strack:
- Testing: docker compose up (with logs)
- Production: docker compose up -d (no logs ; detached mode)
- Start the wordpress installer in your browser (https://example.com)
- See the Traefik UI in your browser (http://example.com:8080)


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
      
      
