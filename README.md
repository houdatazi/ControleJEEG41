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
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9.png)
• Créer les clients : les applications à sécuriser

![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-1.png)

• Créer les users et les attribuer des mots de passe permanents et non pas temporaires
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-2.png)

• Créer les rôles
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-3.png)

• Affecter les rôles aux utilisateurs User1 => USER User2 => ADMIN+USER User3 => ADMIN+USER+MANAGER

Tester avec Postman
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-4.png)

• 1ère méthode de s’authentification : s’authentifier avec un mot de passe et récupérer l’access token Access_token => reste un objet jwt
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-5.png)

   => Access_token : reste un objet jwt  
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-6.png)

Changer les paramètres d’expiration de token : "Access token lifespan 10"
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-7.png)

• Exécution : la liste des produits
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-8.png)

•Ajouter les dépendances : spring security + adaptateur keycloak keycloak-spring-boot-starter

•Créer la configuration keycloak : @KeycloakConfiguration

•Fichier de configuration properties : ajuster les paramètres de configuration pour adapter keycloak

•Adapter cherche toujours le fichier keycloak.json pour les paramètres de configuration, c’est pour cela qu’on va créer une classe de configuration pour ne pas avoir cet changement et prendre en compte la configuration qui se trouve dans le fichier properties

•Après la configuration on accède aux produits et voilà le résultat :
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-9.png)

• Une fois authentifié on peut accéder à la liste des produits
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-10.png)

• On veut afficher par défaut une fois authentifié le username, c’est pour cela qu’on doit ajuster et ajouter quelques paramètres de configuration dans le fichier properties
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-11.png)

Sécuriser le 2ème micro service des fournisseurs
• Les mêmes classes de configuration (package sec)
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-12.png)

• Accéder à la liste des fournisseurs
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-13.png)
![image](https://github.com/houdatazi/ControleJEEG41/blob/main/img/p9-14.png)





