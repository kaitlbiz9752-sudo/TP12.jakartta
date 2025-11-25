
## Puisque github n'accepte pas les codes secret que j'ai dans mon projet application.yml j'ai posée mon dossier dans ke lien drive suivant :



## Clic ici :    


[# TP12.jakartta](https://drive.google.com/drive/folders/1NmwHNjOqW4OxVM3YlCNeINyk8WmPv8lb?usp=sharing)



# README – TP OAuth2 + OpenID Connect avec Spring Boot (Google)

##  Objectif du TP

L’objectif est de comprendre et mettre en œuvre :
- L’authentification déléguée via OAuth2
- L’identification avec OpenID Connect (OIDC)
- L’intégration d’un fournisseur externe d’identité (Google)
- La récupération des informations utilisateur
- La configuration de Spring Security

---

##  Étape 1 – Création du projet Spring Boot

Créer un projet sur : https://start.spring.io

Dépendances :
- Spring Web
- Spring Security
- OAuth2 Client
- Thymeleaf
- Lombok

Paramètres recommandés :
- Group : ma.ens.security
- Artifact : oauth2-client
- Java : 17 ou 21

---

##  Étape 2 – Configuration OAuth2 Google

1. Aller sur https://console.cloud.google.com
2. Créer un projet
3. Activer Google Identity API
4. Créer un identifiant OAuth2
5. Ajouter l’URL de redirection :
   http://localhost:8080/login/oauth2/code/google
6. Récupérer le Client ID et le Client Secret
7. Les utiliser dans application.yml

---

##  Étape 3 – Authentification automatique

Spring Security gère :
- La redirection vers Google
- Le retour vers l’application
- L’échange du code OAuth2 contre un Access Token + un ID Token
- Le login automatique

Aucun contrôleur /login n’est nécessaire.

---


![WhatsApp Image 2025-11-25 at 11 20 53](https://github.com/user-attachments/assets/f3ecafc7-092a-4792-b71d-70a9175d9429)



##  Étape 4 – Récupération du profil utilisateur

L’application expose une page /profile qui :
- récupère le nom,
- l’email,
- la photo de l’utilisateur
depuis l’ID Token Google.

---

##  Étape 5 – Configuration de Security

Spring Security permet de :
- déclarer les pages publiques
- protéger les routes sensibles
- définir la page d’accueil post-login
- gérer la déconnexion

---

##  Résultat de l’application

L’utilisateur peut :
- se connecter via Google
- être redirigé automatiquement
- consulter son profil
- se déconnecter proprement

---

## Vidéo Démonstrative :





https://github.com/user-attachments/assets/1802e772-2f1c-4062-bf23-1977a45e24eb






