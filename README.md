# Rapport
    
 Créer une application basée sur une architecture micro-service qui permet de gérer les factures contenant des produits et appartenant à un client.

# Travail à faire :
  1-Créer le micro-service customer-service qui permet de gérer les clients
  
  2-Créer le micro-service inventory-service qui permet de gérer les produits
  
  3-Créer la Gateway Spring cloud Gateway avec une Configuration statique du système de routage
  
  4-Créer l'annuaire Eureka Discrovery Service
  
  5-Faire une configuration dynamique des routes de la gateway
  
  6-Créer le service de facturation Billing-Service en utilisant Open Feign
  
  7-Créer un client Web Angular (Clients, Produits, Factures)
  
  8-Déployer le serveur keycloak :
  
       . Créer un Realm
       
       . Créer un client à sécuriser
       
       . Créer des utilisateurs
       
       . Créer des rôles
       
       . Affecter les rôles aux utilisateurs
       
       . Tester les différents modes d'authentification avec Postman en montrant les contenus de Access-Token, Refresh Token
       
  9-Sécuriser les micro-services et le frontend angular en déployant les adaptateurs Keycloak
  
  10-Ajouter des Fonctionnalités supplémentaires de votre choix
  
  11-Livrable : Un Repository Github contenant :
  
       . Le code source de l'ensemble des micro-services et du frontend
       
       . Le rapport montrant les différentes étapes dans le fichier README.MD  
       
 # Partie 1 : le micro-service customer-service qui permet de gérer les clients
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/img.png)
# Partie 2 : Créer le micro-service inventory-service qui permet de gérer les produits
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p2.png)
# Partie 3 : Créer la Gateway Spring cloud Gateway avec une Configuration statique du système de routage
• Configuration statique : 1ère méthode

![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p3.png)
# Partie 4 : Créer l'annuaire Eureka Discrovery Service
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p4.png)
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p4-1.png)
# Partie 5 : Faire une configuration dynamique des routes de la gateway
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p5.png)
# Partie 6 : Créer le service de facturation Billing-Service en utilisant Open Feign
• La liste des factures dans la base de données H2

![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p6.png)
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p6-1.png)
# Partie 7 : Créer un client Web Angular (Clients, Produits, Factures)
• Créer un projet Angular avec la commande : "ng new project_name"

![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p7.png)
# Partie 8 : Déployer le serveur keycloak
• Téléchargement et installation de keycloak

![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p8.png)
# Partie 9 : Sécuriser les micro-services et le frontend angular en déployant les adaptateurs Keycloak
• Préparer l’environnement Keycloak :

• Démarrer keycloak avec la comande "kc.bat start-dev"

• Accéder à la console d’administration après la création d’un administrateur

• Créer un realm qui va comporter les applications à sécuriser, les users, les rôles …
![image](




