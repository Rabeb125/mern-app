# Utiliser l'image de base node:lts-alpine
FROM node:lts-alpine

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier les fichiers package*.json
COPY package*.json ./

# Installer les dépendances avec npm install
RUN npm install

# Copier le reste des fichiers du serveur
COPY . .

# Exposer le port 9000
EXPOSE 9000

# Définir une variable d'environnement pour la connexion MongoDB
ENV MONGO_URI=mongodb://mongo:27017/mern

# Démarrer l'application avec npm start
CMD ["npm", "start"]
