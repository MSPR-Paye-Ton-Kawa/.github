# PS-2024-MSPR-Data

## 📚 Projet Scolaire | MSPR

Juin-Septembre 2024

Groupe : Juliette, Flavien, Yasmine & Colas

### 📌 Consignes du projet : 

Objectif principal : 

Développer une application web pour la société fictive PayeTonKawa, spécialisée dans l'import et la vente de café, en adoptant une architecture basée sur des micro-services.

Modules à développer :

API Clients : Gestion des informations clients, authentification et autorisation des utilisateurs.

API Produits : Gestion des produits, catalogues et inventaires.

API Commandes : Gestion des commandes, suivi des livraisons et facturation.

Méthodologie : 

Adopter une approche Agile, avec des livraisons itératives des fonctionnalités principales. Utilisation d'un backlog et d'outils de gestion de projet comme Jira ou Trello.


### 🐱 Notre projet :

## Prérequis

- Docker doit être installé et en cours d'exécution sur votre machine.

## Configuration de RabbitMQ

1. **Lancer RabbitMQ** :
   - Exécutez la commande suivante pour démarrer un conteneur RabbitMQ avec l'interface de gestion :
     ```sh
     docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:4.0-management
     ```

2. **Accéder à l'interface de gestion RabbitMQ** :
   - Ouvrez votre navigateur et accédez à l'URL suivante :
     ```
     http://localhost:15672
     ```
   - Connectez-vous avec les identifiants par défaut (utilisateur : `guest`, mot de passe : `guest`).

## Lancer les API

Option 1. **Lancer toutes les API une à une** :
   - Assurez-vous que tous les projets (gateway, produit, client et commande) sont configurés pour utiliser Docker.
   - Naviguez vers le répertoire de chaque projet et exécutez la commande suivante pour construire et démarrer les conteneurs Docker :
     ```sh
     docker-compose up --build
     ```
   - Répétez cette commande pour chaque projet (gateway, produit, client et commande).

Option 2.  **Lancer toutes les API en même temps** :

   Pour lancer tous les services en même temps, suivez ces étapes :
   
   1. **Naviguez vers le répertoire `api_gateway`** :
      - Ouvrez un terminal ou une invite de commande.
      - Naviguez vers le répertoire `api_gateway` de votre projet.
   
   2. **Exécutez le script `start.sh`** :
      - Tapez la commande suivante dans le terminal :
        ```sh
        ./start.sh
        ```
      - Ce script tirera les dernières images Docker de chaque API depuis Docker Hub et démarrera tous les services en utilisant Docker Compose.

## Consommer les API

Une fois que toutes les API sont en cours d'exécution, vous pouvez les consommer via le webshop ou Postman.

### Utilisation du Webshop

1. **Accéder au Webshop** :
   - Ouvrez votre navigateur et accédez à l'URL du webshop.
   - Utilisez l'interface du webshop pour interagir avec les API.

### Utilisation de Postman

1. **Ouvrir Postman** :
   - Lancez l'application Postman.

2. **Importer la collection Postman** :
   - Importez la collection Postman fournie avec ce projet.
   - Utilisez les requêtes de la collection pour interagir avec les API.

## Structure du Projet

- **gateway** : Projet de la passerelle API.
- **produits** : Projet de l'API des produits.
- **clients** : Projet de l'API des clients.
- **commandes** : Projet de l'API des commandes.
- **webshop** : Projet du webshop : dashboard de gestion des API à destination de l'équipe PayeTonKawa.


### 💻 Applications et langages utilisés :

- C#, Sqlite
- Visual Studio


## 🌸 Merci !
© J-IFT
