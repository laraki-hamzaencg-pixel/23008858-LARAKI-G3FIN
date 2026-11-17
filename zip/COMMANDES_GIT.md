# Commandes Git (à lancer dans le dossier du dépôt)
```
git init
git branch -M main
git remote add origin https://github.com/VOTRE-IDENTIFIANT/23008858-Laraki-G3FIN.git

# Commit 1 : après la description des données
git add .
git commit -m "Description des donnees FRED et chargement"
git push -u origin main

# Commit 2 : après la modélisation
git add .
git commit -m "Preparation, modele et resultats"
git push

# Commit 3 : final
git add .
git commit -m "Analyse critique, conclusion, rapport, presentation"
git tag remise-finale
git push && git push origin remise-finale
```
Créer d'abord le dépôt **public** vide `23008858-Laraki-G3FIN` sur GitHub.
