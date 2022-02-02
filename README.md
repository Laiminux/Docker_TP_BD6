# Docker_TP_BD6

Dans le terminal, palcez vous dans le répertoire contenant le docker-compose et tapez :
- docker-compose up -d --build 
pour rentrer dans un container :
- docker ps
récupérer l'id et entrer :
- docker exec -it <container_id> /bin/bash

Attention une fois dans le container vous serez en root donc pas besoin de sudo et vous serez automatiquement connecté en tant qu'utilisateur 'Omer' sur Postgresql. Pour se connecter 
à la database il suffira juste de :
- psql -d postgresql ( nom de la database )

## Si jamais le répertoire 10/main n'existe pas dans /etc/postgresql
Commencez par supprimer les deux containers, pour ça :
- docker stop $(docker ps -aq)
- docker rm $(docker ps -aq)
Retirer le caractère '#' dans les DEUX dockerfiles. Et relancer :
- docker-compose up -d --build 
### ATTENTION : 
Une fois fait, il faudra remettre le '#' derrière la ligne "RUN pg_createcluster ..."
