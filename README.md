## Spring Boot 01 — Gestion d’Étudiants via un Fichier Local

### Objectif du projet

Développer une application Spring Boot fournissant plusieurs web services REST permettant de lire, ajouter, supprimer et rechercher des étudiants.
Les données sont stockées dans un fichier local (par exemple etudiants.csv ou etudiants.json) déjà fourni.

Ce mini-projet permet aux étudiants de découvrir :

La manipulation de fichiers en Java

La création d’API REST avec Spring Boot

La sérialisation/désérialisation de données

Le routing, les DTO, les services et la logique métier

### Structure des données

Le fichier local contient une liste d’étudiants avec les champs suivants :

Champ	Description
nom	Nom de l’étudiant
prenom	Prénom de l’étudiant
sexe	Sexe (M/F/autre)
promo	Promotion de l’étudiant (ex: 2025)

Format libre : CSV ou JSON, selon ce qui est donné par l’enseignant.

🚀 Fonctionnalités à développer

Votre application Spring Boot devra exposer les endpoints REST suivants :

1️⃣ Récupérer la liste de tous les étudiants

GET /etudiants
→ Retourne l’ensemble des étudiants présents dans le fichier.

2️⃣ Ajouter un nouvel étudiant

POST /etudiants
→ Ajoute un étudiant dans le fichier local.
→ Le corps de la requête contient les informations de l’étudiant (JSON recommandé).

3️⃣ Supprimer un étudiant

DELETE /etudiants/{nom}
→ Supprime un étudiant en fonction de son nom et/ou prénom.
→ Vous êtes libres de choisir comment gérer les doublons.

4️⃣ Rechercher un étudiant par nom et/ou prénom

GET /etudiants/recherche?nom=...&prenom=...
→ Retourne la liste des étudiants correspondant aux critères.
