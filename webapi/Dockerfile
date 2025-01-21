# Utiliser l'image officielle de Go pour la compilation
FROM golang:1.21 AS builder

# Définir le répertoire de travail
WORKDIR /app

# Copier les fichiers source
COPY . .

# Télécharger les dépendances et compiler l'application
RUN go mod tidy && go build -o /main

# Exposer le port 8081
EXPOSE 8081

# Commande pour démarrer l'application
CMD ["/main"]