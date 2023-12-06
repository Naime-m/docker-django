# docker-django

# Conteneurisation de l'API et de la base de données 

Ce projet a été effectué en conteneurisant une API réalisée avec Django Rest Framework et une base de données en utilisant Docker. Les étapes suivantes ont été effectuées :

## Conteneurisation de l'API (Dockerfile)

- Ouverture de l'API pour qu'elle soit accessible depuis l'extérieur du conteneur.
- Configuration des ports de l'API pour qu'ils soient accessibles.
- Mise en place des variables d'environnement nécessaires pour l'API.

## Conteneurisation de la base de données

- Configuration des variables d'environnement pour la base de données, y compris les identifiants de connexion, etc.
- Liaison de la base de données à l'API en utilisant les fonctionnalités de liaison avec le paramètre depend_on dans le fichier docker-compose.yml.
- Création de volumes pour la base de données afin de stocker les données de manière persistante.

## Push de l'image sur une registry privée

Enfin, le déploiement des conteneurs a été effectué en poussant l'image (conteneur) sur une registry Docker privée créée sur DockerHub. 

### Sécurité

Des mesures de sécurité ont été prises pour protéger les données sensibles dans les variables d'environnement et pour éviter la divulgation de données confidentielles.
