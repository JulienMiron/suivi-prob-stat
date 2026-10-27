# Suivi des remises — Probabilités et statistique pour ingénieurs, 4e édition

Page de suivi des fichiers remis à l'éditeur, chapitre par chapitre.

- `index.html` : la page (aucune dépendance externe).
- `suivi.json` : les données (titre, colonnes, chapitres, notes).

## Mettre à jour depuis la page

1. Ouvrir la page avec `?modifier` à la fin de l'adresse (ex. `…/suivi-prob-stat/?modifier`).
   Dans ce navigateur, le bouton « Modifier » restera ensuite visible au bas de la page.
2. Cliquer une case : **✓ Remis**, **une date de remise**, ou **TBD**. Les notes se modifient dans la zone de texte (une note par ligne).
3. Cliquer **Enregistrer**. La page écrit `suivi.json` dans ce dépôt (un commit par enregistrement).

Au premier enregistrement, la page demande un jeton GitHub. Pour le créer :
GitHub → Settings → Developer settings → Personal access tokens → **Fine-grained tokens** → Generate new token →
*Repository access : Only select repositories* (ce dépôt seulement) → *Permissions → Contents : Read and write*.

Le jeton reste dans le navigateur (stockage local) et n'est jamais écrit dans le dépôt.
« Oublier le jeton » le retire.

Les visiteurs sans jeton voient la page en lecture seule.

## États possibles dans `suivi.json`

- `"ok"` : remis / validé (✓ vert)
- `"AAAA-MM-JJ"` : en attente, date de remise prévue (en rouge si la date est dépassée)
- `"tbd"` : date à déterminer

Pour ajouter une colonne ou un chapitre, modifier `colonnes` et `lignes` directement dans `suivi.json`
(chaque ligne doit avoir autant d'états qu'il y a de colonnes).
