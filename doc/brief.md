# Cahier des Charges — Application Web SmartChat AI Manager

---

## 1. Présentation Générale du Projet

L’objectif de l’application SmartChat AI Manager est de proposer une plateforme de conversation intelligente permettant aux utilisateurs d’interagir avec une IA, de sauvegarder leurs conversations, de les organiser et d’améliorer la qualité de l’expérience grâce à un système de mémoire, de recherche et de classement.

Cette application vise à offrir :

- une expérience de discussion textuelle fluide avec une IA,
- la possibilité de structurer les conversations par groupe thématique (travail, études, projets, etc.),
- un historique des discussions accessible à tout moment,
- un système de retour sur la qualité des réponses.

L’application sera développée avec React (Frontend), Laravel (Backend) et MySQL (Base de données).

---

## 2. Enjeux et Problèmes Actuels

Actuellement, les utilisateurs d’outils IA ne disposent pas :

- d’un espace structuré de gestion de conversations personnelles,
- d’un classement thématique,
- de mémoires persistantes par conversation,
- d’une organisation simple de multiples discussions simultanées.

Les outils actuels n’offrent qu’une simple liste chronologique difficilement exploitable, sans mécanisme d’évaluation, ni personnalisation.

SmartChat AI Manager devra remédier à ces limites par :

- une organisation par groupes,
- un stockage et une indexation des conversations,
- une recherche interne,
- une classification flexible,
- une expérience personnalisée.

---

## 3. Objectifs Fonctionnels (vision globale)

L’application devra permettre :

### Au niveau utilisateur
- Inscription et connexion,
- Modification des informations de profil,
- Sélection du style de réponse (courte ou détaillée),
- Notation des réponses de l’IA.

### Au niveau conversation
- Création d’une discussion avec IA,
- Réponse automatique et cohérente de l’IA,
- Génération automatique du titre de la conversation,
- Mémoire persistante sur les derniers messages,
- Organisation en groupes,
- Recherche par titre ou contenu.

### Au niveau interface
- Mode clair et mode sombre,
- Sidebar de navigation,
- Interface intuitive utilisable sur différents supports.

---

## 4. Périmètre du Projet

### Inclus dans le périmètre
- Développement back-end et front-end complet,
- Authentification utilisateur,
- Système IA conversationnel,
- Gestion des groupes de conversations,
- Notation des réponses IA,
- API REST sécurisée,
- Base de données relationnelle,
- Interface responsive.

### Exclus de la version initiale
- Réseaux sociaux et authentification externe,
- Paiement et abonnements,
- Applications mobiles natives,
- Partage public externe.

---

## 5. Contraintes Techniques

### Architecture
- Frontend développé en React,
- Backend développé en Laravel (API REST),
- Base de données MySQL,
- Format d’échange JSON.

### Technologies imposées
- React + React Router,
- Laravel avec API Resources,
- MySQL,
- Authentification via JWT ou Sanctum,
- TailwindCSS recommandé.

### Sécurité
- Hashage sécurisé des mots de passe,
- Contrôle d’accès basé sur utilisateur connecté,
- Limitation de l’accès sans authentification,
- Protection CSRF et validation des entrées.

### Système IA
- Réponses conditionnées par l'entrée utilisateur,
- Génération automatisée du nom de la conversation,
- Contexte conservé sur les cinq à dix derniers messages.

---

## 6. Structure Organisationnelle des Données (conceptuel)

La modélisation détaillée sera réalisée en UML.

Les entités centrales attendues sont :

| Entité        | Description |
|---------------|-------------|
| User          | Informations utilisateur |
| Conversation  | Instance de discussion |
| Message       | Message IA ou utilisateur |
| Group         | Catégorisation de conversations |

Relations prévues :

- Un utilisateur possède plusieurs conversations,
- Une conversation contient plusieurs messages,
- Un utilisateur possède plusieurs groupes,
- Un groupe contient plusieurs conversations,
- Une conversation peut avoir une ou plusieurs évaluations.

---

## 7. Livrables Attendues

### Documentation d'analyse
- Diagrammes UML (cas d'utilisation et classes),
- Cahier des user stories.

### Documentation technique
- Modèle conceptuel de données,
- Documentation des endpoints API,
- Schéma de l’architecture logicielle,
- Scripts SQL de création de base.

### Partie logicielle
- Application opérationnelle,
- API fonctionnelle et sécurisée,
- Code source versionné sur Git,
- Script d’installation ou fichier README.

---

## 8. MVP (Version Minimale Requise)

La version minimale du projet devra couvrir les éléments suivants :

- Inscription et connexion utilisateur,
- Déconnexion,
- Diplay tutorial module
- Création d’une conversation IA,
- Génération automatique du nom de conversation,
- Réponses IA contextualisées,
- Mémorisation limitée des messages,
- Sidebar d’accès aux conversations,
- Création et gestion d’un groupe,
- Drag-and-drop d’une conversation vers un groupe,
- Modification du profil utilisateur,
- Mode sombre et mode clair.

Aucun module additionnel ne doit être implémenté avant validation complète de ce périmètre.

---

## 9. Critères d’Évaluation

### Critères techniques fondamentaux
- Respect intégral du périmètre MVP,
- Fonctionnement sécurisé de l’authentification,
- Base de données conforme et fonctionnelle,
- Architecture claire et modulable,
- Documentation fournie.

### Bonus supplémentaires possibles
- Export PDF de conversation,
- Recherche avancée multi-critères,
- Suggestions automatiques de regroupement,
- Historisation graphique des notes IA,
- Export CSV des conversations.

---

# Cadre des Fonctionnalités — Version Initiale

## Fonctionnalités MVP obligatoires

### Authentification
- Inscription,
- Connexion,
- Déconnexion,
- Modification profil.

### Gestion des Conversations
- Création de conversation IA,
- Échanges utilisateur ↔ IA,
- Suppression conversation.

### Mémoire IA
- Conservation de cinq à dix messages.

### Groupes
- Création de groupe,
- Renommage de groupe,
- Classement par glisser-déposer.

### Interface Utilisateur
- Sidebar filtrant groupes et conversations,
- Page de chat responsive,
- Mode clair / sombre.

---

## Extension possible après MVP
- Exportation / importation,
- Historique complet,
- Analyse statistique,
- Pages publiques partagées,
- Automatisation de regroupement.

---

## Travail préalable obligatoire

Avant démarrage du développement, le développeur devra préparer :

- User stories détaillées,
- Maquettes Figma,
- Diagrammes UML,
- Planning de développement.


