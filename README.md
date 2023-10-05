# version de docker utilisé
> version: '3.9'

# Service que je veux creer
services:

  # web:
    
 # (nom de l'image qui sera creer)
    image: nginx 
 # (nom du contenaire qui sera lancer apartir de l'image nginx)
    container_name: iginx-container
 # volumes:
   # (mapper le dossier src a html de nginx)
    - ./src:/usr/share/nginx/html
 # ports:
   # (mapper le port 80 du contenaire au port 8080 du pc)
 - "8080:80"
     # (commande qui sera executer pour lancer nginx)
    command: [nginx-debug, '-g', 'daemon off;']