# Évaluation Technique: Clone de l'Interface Instagram 

## Présentation du Projet

Cette étude de cas consiste à développer une application mobile qui reproduit fidèlement l'interface Instagram. 
L'application doit permettre de s'authentifier, d'accéder au feed utilisateur, et d'interagir avec les publications via un système de "like".

## Fonctionnalités Requises

### 1. Authentification

![Maquette interface authentification](../assets/login-instagram.jpg)


**Objectif:** Reproduire fidèlement l'interface d'authentification d'Instagram.

**Spécifications:**

- Implémenter les scénarios d'authentification suivants:
  - `muser1/mpassword1` → Authentification réussie
  - `muser2/mpassword2` → Authentification réussie
  - `muser3/mpassword3` → Affichage du message d'erreur: "Ce compte a été bloqué."
  - Toute autre combinaison → Affichage du message d'erreur: "Informations de connexion invalides"
- Soigner l'expérience utilisateur avec des transitions et validations appropriées
- Après authentification, afficher directement l'écran "**Feed** suivant

### 2. Feed utilisateur

Reproduire le design Instagram avec des images provenant de l'API Unsplash.

**Objectif:** Développer une interface de visualisation d'images utilisant l'API Unsplash.

**Spécifications:**
- Intégrer l'API [Unsplash](https://unsplash.com/developers) (nécessite la création d'un compte développeur)
- Afficher les images 
- Implémenter un système de pagination ou d'infinite scrolling pour optimiser le chargement
- Gérer les états de chargement et d'erreur de manière élégante

### 3. Système de Likes

**Objectif:** Permettre de "liker" les images et conserver leurs préférences.

**Spécifications:**
- Ajouter une icône de "like" clairement visible sous chaque image
- Implémenter un état visuel distinct pour les images déjà "likées" par l'utilisateur connecté
- Synchroniser ces données avec une base de données côté client
- Assurer que les "likes" sont persistants entre les sessions

## Contraintes Techniques

- Utiliser **Flutter** ou **ReactNative (avec ou sans Expo)**
- **Qualité du code:** Structure claire, commentaires pertinents, et respect des bonnes pratiques

## Critères d'Évaluation

- Fidélité à la maquette d'authentification fournie
- Fonctionnalité de l'intégration avec l'API Unsplash
- Performance et optimisation (notamment pour le chargement des images)
- Qualité de l'interface utilisateur et expérience utilisateur
- Propreté et maintenabilité du code

## Livrables

- Lien vers le repository GitHub contenant le code source complet du projet
- Instructions claires pour l'installation et le lancement du projet en local
- Documentation des choix techniques effectués (dans un fichier README.md)

---

Bonne chance dans la réalisation de ce projet d'évaluation! N'hésitez pas à faire preuve de créativité tout en respectant les contraintes et fonctionnalités demandées. 