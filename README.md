# F16 : Loi d'Okun, chômage et croissance du PIB américain

**Auteur :** LARAKI Hamza, code Apogée 23008858, groupe G3FIN (S7 FIN).

**Résumé.** Je teste si une régression linéaire simple de la variation trimestrielle du taux de chômage sur la croissance du PIB réel des États-Unis fait mieux que deux règles naïves, et si le coefficient d'Okun est stable dans le temps.

## Problématique et résultats
Objectif fixé à l'avance : MAE du modèle inférieure d'au moins 10 % à celle de la meilleure référence, sur le test (2015 T1 à aujourd'hui).

| Modèle | MAE validation | MAE test | RMSE test | R² test |
|---|---|---|---|---|
| Moyenne (référence 1) | 0,241 | 0,500 | 1,553 | −0,001 |
| Dernière valeur (référence 2) | 0,208 | 0,703 | 2,435 | −1,461 |
| Régression linéaire | 0,203 | 0,433 | 1,127 | 0,473 |

Résultat : la régression bat la meilleure référence sur le test (MAE 0,433 contre 0,500, soit −13,4 %, objectif de 10 % atteint). Mais sans 2020 T2-T3, elle fait légèrement pire que les références (0,245 contre 0,213 et 0,217). Le coefficient d'Okun vaut b = −0,281 (IC 95 % : −0,317 à −0,245) et reste négatif sur 1948-2014.

## Données
- PIB réel `GDPC1` : https://fred.stlouisfed.org/series/GDPC1
- Taux de chômage `UNRATE` : https://fred.stlouisfed.org/series/UNRATE
- Licence : données publiques BEA et BLS diffusées par FRED (conditions à vérifier sur chaque page).
- Date d'extraction : voir `data/raw/LISEZMOI_extraction.txt`. Les fichiers bruts sont dans `data/raw/`.

## Installation
Python 3.10 ou plus récent, puis : `pip install -r requirements.txt`

## Exécution
Ouvrir `notebooks/projet_F16.ipynb` et faire « Redémarrer et tout exécuter » (environ 1 minute). Les figures sont écrites dans `figures/`.

## Structure du dépôt
```
23008858-Laraki-G3FIN/
├── README.md  requirements.txt  .gitignore  DECLARATION_IA.md
├── data/raw/  data/processed/
├── docs/ (fiche_sujet_F16.md, references.md)
├── notebooks/projet_F16.ipynb
├── src/   figures/   rapport/rapport.pdf   presentation/
```

## Références et IA
Voir `docs/references.md` et `DECLARATION_IA.md`.
