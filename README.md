# 4WEBD - Event Ticketing Platform

4WEBD est une plateforme SaaS de gestion de billetterie pour événements, concerts et spectacles.  
Le projet est conçu pour être modulaire, sécurisé et scalable, basé sur une architecture microservices.

## Fonctionnalités

- Authentification sécurisée (JWT)
- Gestion des utilisateurs (Admin, Utilisateur, Créateur d'événement)
- Création et gestion d'événements
- Achat et validation de billets
- Intégration d'un système de paiement
- Notifications (email/SMS) via file Redis
- Tableau de bord personnalisé
- Protection contre la survente (overbooking)

## Stack technique

### Frontend

- React (Create React App)
- React Router
- Axios
- Context API pour la gestion de l'authentification
- Intégration avec un API Gateway en Node.js (via http-proxy-middleware)

### Backend (Microservices)

- Node.js / Express
- PostgreSQL
- Docker / Docker Compose
- Redis
- JWT pour la gestion des sessions
- Jest / Supertest pour les tests unitaires
- Swagger pour la documentation API

### Microservices

| Microservice       | Description                                               |
|--------------------|-----------------------------------------------------------|
| `users-service`    | Gestion des comptes utilisateurs et de l'authentification |
| `events-service`   | Création, modification, suppression d'événements          |
| `tickets-service`  | Réservation, achat, contrôle de billets                   |
| `payments-service` | Traitement des paiements, validation des achats           |
| `notifications`    | Génération et envoi de notifications via Redis            |

## Installation et lancement

1. Cloner le dépôt :
   ```bash
   git clone https://github.com/ToycanNazir/4WEBD.git
   cd 4WEBD/evemt-tocket-saas

2. Lancer l’ensemble des services avec Docker :

   ```bash
    docker-compose up --build

3. Accéder à l’interface web :

     http://localhost:3000

4. Scripts utiles
Lancer les tests unitaires/integrations d’un microservice :
   ```bash
    cd nom-du-service
    npm install
    npm test

5. Générer la documentation Swagger (si disponible) : Accéder à :

   http://localhost:<PORT_DU_SERVICE>/api-docs


Auteur
Développé par Toycan Nazir dans le cadre du projet 4WEBD.



