# Évaluation Technique: Développement Backend & API

## Présentation du Projet

Ce test technique est conçu pour évaluer les compétences en développement backend et API. L'objectif est de créer un serveur qui expose plusieurs endpoints permettant de générer des utilisateurs fictifs, d'importer ces données en base, de gérer l'authentification et d'accéder aux profils utilisateurs selon différents niveaux d'autorisation.

## Objectif

Développer un backend qui expose les APIs suivantes :

### 1. Génération d'utilisateurs

**Requête**
```http
GET /api/users/generate
```

**Spécifications :**
- **Authentification requise :** Non
- **Paramètres :** 
  - `count`: nombre d'utilisateurs à générer
- Générer un fichier JSON contenant le nombre d'utilisateurs demandé
- Le téléchargement du fichier doit se déclencher automatiquement dans le navigateur

**Format de réponse :**
```json
[{
    "firstName": "string",
    "lastName": "string",
    "birthDate": "date",
    "city": "ville",
    "country": "code iso2",
    "avatar": "url d'une image",
    "company": "string",
    "jobPosition": "string",
    "mobile": "numéro de téléphone",
    "username": "identifiant de connexion",
    "email": "adresse email",
    "password": "mot de passe aléatoire entre 6 et 10 caractères",
    "role": "admin ou user"
}]
```

**Exigences :**
- Utiliser une bibliothèque appropriée (comme Faker) pour générer des données réalistes
- Le champ `role` doit être soit "admin" soit "user"
- Éviter les valeurs génériques de type "example", "test", etc.

### 2. Import d'utilisateurs

**Requête**
```http
POST /api/users/batch
Content-Type: multipart/form-data
```

**Spécifications :**
- **Authentification requise :** Non
- **Paramètres :** 
  - `file`: fichier JSON à importer
- Importer les utilisateurs en base de données
- Vérifier les doublons sur email et username (champs uniques)
- Encoder les mots de passe avant stockage (ne pas les stocker en clair)

**Réponse attendue :**
- Résumé du traitement avec :
  - Nombre total d'enregistrements
  - Nombre d'enregistrements importés avec succès
  - Nombre d'enregistrements non importés

### 3. Authentification

**Requête**
```http
POST /api/auth
Content-Type: application/json
```

**Corps de la requête :**
```json
{
  "username": "string",
  "password": "string"
}
```

**Spécifications :**
- Le champ `username` peut contenir soit le username soit l'email de l'utilisateur
- Générer un token JWT contenant l'email de l'utilisateur

**Réponse attendue :**
```json
{
  "accessToken": "valeur du jeton JWT"
}
```

### 4. Consultation de mon profil

**Requête**
```http
GET /api/users/me
```

**Spécifications :**
- **Authentification requise :** Oui (JWT)
- Retourne les informations de l'utilisateur associé au token JWT

### 5. Consultation du profil d'un utilisateur

**Requête**
```http
GET /api/users/{username}
```

**Spécifications :**
- **Authentification requise :** Oui (JWT)
- **Autorisations :**
  - Les utilisateurs avec le rôle "admin" peuvent consulter n'importe quel profil
  - Les utilisateurs avec le rôle "user" ne peuvent consulter que leur propre profil

## Contraintes Techniques

- **Stack technique :**
  - NodeJS
  - TypeScript
  - Express ou Fastify
- **Base de données :** Au choix (MongoDB, PostgreSQL, SQLite, etc.)
- **Port :** L'application doit démarrer sur le port 9090
- **Documentation :** L'API doit être documentée avec Swagger/OpenAPI
- **Tests :** Des tests unitaires sont fortement recommandés

## Critères d'Évaluation

- Qualité et structure du code
- Respect des bonnes pratiques (sécurité, performance)
- Gestion des erreurs
- Documentation de l'API
- Qualité des tests

## Livrables

- Lien vers le repository GitHub contenant le code source complet du projet
- Instructions détaillées pour l'installation et le démarrage du projet
- Documentation des choix techniques effectués (dans un fichier README.md)


---

Bonne chance dans la réalisation de ce projet d'évaluation ! N'hésitez pas à démontrer vos compétences techniques et votre rigueur dans le développement d'APIs.