FROM node:lts-alpine

RUN mkdir /app
WORKDIR /app
COPY package*.json ./
# Pour tirer profit du cache de docker, on fait le npm install avant la copie des sources
RUN npm i
COPY src src

CMD npm start

#Dans le terminal pour construire une image:
# lancer la commande : docker build -t hello-app .

# Pour lister les images dispo sur la machine :
# docker image ls

# pour éxécuter l'image
# docker run hello-app

#pour lister les conteneurs en cours d'éxécution : 
# docker ps

# pour stopper l'éxécution, récupérer l'id du container via docker ps puis:
# docker stop containerId

# pour démarrer le conteneur de façon détachée:
# docker run -d hello-app

# pour afficher les logs de l'application :
# L'option -f permet d'afficher les logs en continu.
# On peut récupérer la main en faisant Ctrl+C.
# Cela n'interrompt pas l'exécution du conteneur.
# docker logs -f containerId

# Afin d'établir la connexion entre ton client Docker et DockerHub, exécute la commande docker login et suis les instructions.

# Pour pousser l'image sur DockerHub : remplacer user par identifiant val0sch
# il faut d'abord compiler puis pousser
# docker build -t user/hello-app .
# docker push user/hello-app

# Pour récupérer l'image sur une autre machine :
# docker pull val0sch/hello-app
