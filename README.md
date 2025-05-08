# Évaluations Techniques FFK

Ce dépôt contient des tests d'évaluation technique conçus par [FFK](https://ffk.ci) pour évaluer différentes compétences de développement.

## Présentation

Ces évaluations visent à tester à la fois les connaissances techniques et les compétences en résolution de problèmes dans un contexte pratique.

## Tests Disponibles

Le dépôt comprend actuellement les évaluations suivantes :

### 1. Évaluation Frontend : Galerie d'Images avec Authentification

Une application NextJS qui implémente :
- Authentification utilisateur avec différents scénarios
- Galerie d'images utilisant l'API Unsplash
- Système de likes avec persistance d'état côté client

[Voir l'évaluation frontend](./evaluations/frontend-gallery.md)

### 2. Évaluation Backend : API de Gestion d'Utilisateurs

Une API Node.js (TypeScript, Express/Fastify) qui implémente :
- Génération d'utilisateurs fictifs
- Import d'utilisateurs en base de données
- Système d'authentification JWT
- Gestion des profils selon les rôles utilisateurs

[Voir l'évaluation backend](./evaluations/backend-users.md)

## Structure du Dépôt

```
/
├── evaluations/
│   ├── frontend-gallery    # Test frontend galerie d'images
│   ├── backend-users       # Test backend API utilisateurs
    ├── mobile-instagram    # Test Mobile
│   └── ...                 # Futurs tests
├── assets/                 # Ressources partagées (images, etc.)
└── README.md               # Documentation principale
```

## Comment Utiliser ce Dépôt

### Pour les Candidats

1. Choisissez l'évaluation correspondant au poste pour lequel vous postulez
2. Suivez les instructions détaillées dans le README du test spécifique
3. Soumettez votre solution selon les instructions de candidature

### Pour les Recruteurs

Ce dépôt peut être utilisé comme référence pour comprendre les compétences techniques que nous recherchons chez FFK.

## Contribution

Ce dépôt est maintenu par l'équipe technique de FFK. Pour toute question concernant ces évaluations, veuillez nous contacter directement.

