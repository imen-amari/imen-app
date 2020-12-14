#Manipulation
# instalation des packages
npm install
# lancement du serveur en dev mode ( changement en temps reel )
npm start
# lancement du server en mode production
npm run build


#Dockerfile
creation du fichier docker file avec les options demandé

# Creation de l'image docker 
docker build -t imen:dev .

# Lancement du container
winpty docker run \
    -it \
    --rm \
    -v ${PWD}:/app \
    -v /app/node_modules \
    -p 3001:3000 \
    -e CHOKIDAR_USEPOLLING=true \
    imen:beta