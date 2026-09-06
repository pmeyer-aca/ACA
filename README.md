# Site de stats ACA U18 — mode d'emploi

Ce dossier contient 2 fichiers à mettre en ligne ensemble :
- `index.html` — la page (à ne plus jamais modifier après la mise en ligne)
- `data.xlsx` — vos données (c'est CE fichier que vous remplacerez à chaque mise à jour)

La page lit `data.xlsx` directement dans le navigateur : vous n'avez jamais besoin de
toucher au code, seulement de remplacer ce fichier Excel.

## 1. Mise en ligne (à faire une seule fois)

1. Créez un compte gratuit sur https://github.com si vous n'en avez pas.
2. Cliquez sur le bouton **New** (nouveau dépôt / repository).
   - Nom : par exemple `aca-u18-stats`
   - Cochez **Public**
   - Cliquez sur **Create repository**
3. Sur la page du dépôt, cliquez sur **Add file > Upload files**, puis glissez-déposez
   `index.html` et `data.xlsx`. Cliquez sur **Commit changes**.
4. Allez dans **Settings > Pages** (menu de gauche).
   - Sous **Branch**, choisissez `main` puis **Save**.
5. Patientez 1 à 2 minutes, puis rechargez la page : l'adresse de votre site apparaît en haut
   (quelque chose comme `https://votre-pseudo.github.io/aca-u18-stats/`).
6. Partagez cette adresse aux membres du club (ex. par SMS, message d'équipe, etc.).
   Elle ne changera plus jamais, même lors des futures mises à jour.

## 2. Mettre à jour les statistiques (après chaque match)

1. Renseignez votre classeur Excel comme d'habitude (onglets Matchs, Buts, Cartons,
   Convocations, Changements...).
2. Enregistrez une copie de ce fichier sous le nom exact **`data.xlsx`** (respectez la
   casse et l'extension `.xlsx`).
3. Retournez sur votre dépôt GitHub, ouvrez le fichier `data.xlsx` existant, cliquez sur
   l'icône crayon (ou la corbeille pour le supprimer puis **Add file > Upload files** pour
   le remettre) et uploadez votre nouvelle version au même endroit, avec le même nom.
4. Cliquez sur **Commit changes**.
5. La page se met à jour automatiquement (rechargez-la après une minute) — vous n'avez
   rien d'autre à faire.

**Important :** le nom du fichier doit toujours rester `data.xlsx`, sinon la page ne le
retrouve plus.

## 3. Qui peut modifier quoi ?

- Les membres du club qui ont juste l'adresse du site peuvent seulement **consulter** les
  statistiques — ils ne peuvent rien modifier.
- Seule la personne qui a accès à ce dépôt GitHub (vous, avec votre compte) peut mettre à
  jour `data.xlsx` et donc changer ce qui s'affiche.

## 4. Ce qu'affiche la page

- **Onglet Équipe** : bilan victoires/nuls/défaites, buts pour/contre, liste des matchs
  (avec filtres par compétition et par lieu), graphique buts marqués/encaissés, bilan par
  niveau d'adversaire.
- **Onglet Joueurs** : classement filtrable et triable (cliquez sur un titre de colonne
  pour trier), recherche par nom, top buteurs, fiche détaillée par joueur (buts, passes,
  cartons, temps de jeu, taux de convocation/titularisation).

Les onglets Cartons et Changements de votre classeur ne sont pas encore très remplis :
c'est normal, les chiffres correspondants (cartons, etc.) afficheront simplement 0 tant
qu'il n'y a rien à compter.
