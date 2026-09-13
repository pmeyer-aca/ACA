# Site de statistiques — ACA U18

Site statique (une seule page `index.html`) qui affiche les statistiques des deux
équipes U18 du club, à partir de fichiers Excel que vous mettez à jour vous-même.
Personne d'autre ne peut modifier quoi que ce soit : les visiteurs ne font que
consulter.

## 1. Fichiers à héberger ensemble

Ces 4 fichiers doivent toujours se trouver **au même endroit**, avec **ces noms
exacts** :

| Fichier | Contenu |
|---|---|
| `index.html` | La page elle-même (le code du site) |
| `data_equipe1.xlsx` | Classeur de suivi de saison — U18 Équipe 1 |
| `data_equipe2.xlsx` | Classeur de suivi de saison — U18 Équipe 2 |
| `entrainements.xlsx` | Fichier maître des présences aux entraînements (les deux équipes) |

Si l'un de ces fichiers est absent, la partie du site qui en dépend affiche un
message d'erreur au lieu de planter tout le site — les 3 autres continuent de
fonctionner normalement.

## 2. Mise en ligne (à faire une seule fois)

1. Créez un compte gratuit sur https://github.com si vous n'en avez pas.
2. Cliquez sur **New** (nouveau dépôt).
   - Nom : par exemple `aca-u18-stats`
   - Cochez **Public**
   - **Create repository**
3. **Add file > Upload files**, glissez-déposez les 4 fichiers listés ci-dessus,
   puis **Commit changes**.
4. **Settings > Pages** (menu de gauche) → sous **Branch**, choisissez `main` →
   **Save**.
5. Patientez 1-2 minutes, rechargez la page : l'adresse de votre site apparaît en
   haut (ex. `https://votre-pseudo.github.io/aca-u18-stats/`).
6. Partagez cette adresse au club. Elle ne change plus jamais, même après de
   futures mises à jour.

## 3. Mettre à jour les stats d'une équipe (après chaque match)

1. Renseignez votre classeur Excel comme d'habitude (onglets Matchs, Buts,
   Cartons, Convocations, Changements, Gardien...).
2. Sur GitHub, ouvrez `data_equipe1.xlsx` ou `data_equipe2.xlsx` (selon
   l'équipe concernée), cliquez sur l'icône crayon (ou supprimez puis
   **Add file > Upload files** pour le remettre), et uploadez votre fichier à
   jour **sous ce même nom exact**.
3. **Commit changes**.
4. La page se met à jour automatiquement (rechargez-la après une minute).

**Important :** ne renommez jamais ces fichiers — le site les cherche par leur
nom exact.

## 4. Mettre à jour les présences aux entraînements

Le fichier `entrainements.xlsx` est un fichier **maître qui s'enrichit chaque
semaine** (il garde tout l'historique de la saison), contrairement aux exports
bruts de l'outil de gestion (TeamSnap ou autre) qui ne couvrent que quelques
dates à la fois.

**Marche à suivre :**
1. Téléchargez le nouvel export depuis votre outil (couvrant les dates les plus
   récentes).
2. Envoyez ce fichier brut à Claude (dans une conversation du projet), en
   demandant de le fusionner dans le fichier maître.
3. Claude vous renvoie `entrainements.xlsx` mis à jour, prêt à remplacer
   l'ancien sur GitHub (même procédure qu'à la section 3 : uploadez-le au même
   endroit, sous le même nom).
4. Pensez aussi à **mettre à jour la copie de `entrainements.xlsx` dans les
   fichiers du projet Claude**, pour que la prochaine fusion reparte de la
   bonne version.

Le format attendu pour un export brut : une ligne d'en-tête avec les dates de
séance en colonnes (à partir de la colonne H), une deuxième ligne indiquant
l'équipe concernée pour chaque colonne (le texte doit contenir "U18-1" ou
"U18-2"), puis une ligne par joueur avec `1` dans les colonnes des séances où
il était présent. Le site répartit automatiquement les colonnes entre les deux
équipes.

## 5. Ajouter ou retirer un joueur

Si l'effectif d'une équipe change en cours de saison (nouveau joueur, licence
qui tombe, etc.), prévenez Claude — cela nécessite une petite modification du
classeur Excel concerné (au-delà d'un simple remplacement de fichier) pour que
les formules et le suivi restent cohérents.

## 6. Ce qu'affiche le site

Un sélecteur en haut de page permet de choisir entre 3 vues :

- **U18** — vue d'ensemble : un seul tableau "Utilisation joueurs" qui fusionne
  les statistiques des deux équipes (temps de jeu, buts, cartons, taux de
  convocation global et par équipe...).
- **U18 Équipe 1** / **U18 Équipe 2** — vue complète par équipe, avec 3
  onglets :
  - **Joueurs** : tableau d'utilisation joueurs (triable, filtrable),
    gardiens, top buteurs, top passeurs, suivi des absences par motif,
    fiche détaillée par joueur (buts, passes, cartons, temps de jeu, taux de
    convocation/titularisation, participation aux entraînements).
  - **Matchs** : bilan de la saison, liste des matchs (filtrable), détail par
    match avec composition, chronologie interactive du match (joueurs sur le
    terrain, buts, changements), tableaux détaillés.
  - **Entraînement** : grille de présence par séance, avec taux de
    participation par joueur.

## 7. Qui peut modifier quoi ?

- Les membres du club qui ont l'adresse du site peuvent uniquement
  **consulter**.
- Seule la personne ayant accès au dépôt GitHub peut mettre à jour les
  fichiers Excel et donc changer ce qui s'affiche.

---
*Conception : P. Meyer — dernière mise à jour de ce document : voir la date en
bas de la page du site elle-même.*
