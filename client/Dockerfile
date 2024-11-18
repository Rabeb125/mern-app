# Utiliser l'image de base node:lts-alpine
FROM node:lts-alpine

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier les fichiers package*.json
COPY package*.json ./

# Installer les dépendances avec npm install
RUN npm install

# Copier le reste des fichiers du client
COPY . .

# Construire l’application React avec npm run build
RUN npm run build

# Installer un serveur HTTP léger pour servir les fichiers statiques
RUN npm install -g serve

# Exposer le port 3000
EXPOSE 3000

# Démarrer le serveur pour servir les fichiers de build
CMD ["serve", "-s", "build", "-l", "3000"]
