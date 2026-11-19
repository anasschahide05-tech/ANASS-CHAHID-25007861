# CI01 — Prévision des exportations marocaines (ENCG Settat, S7 CI, BD & DS)

**Étudiant :** Anass Chahid · **Code Apogée :** [à compléter] · **Groupe :** [à compléter]
**Enseignant :** A. Larhlimi · **Épreuve :** Contrôle continu Partie B (2 h, individuel)

## Question
Un modèle Ridge construit sur l'historique récent des flux prévoit-il mieux les exportations marocaines de l'année suivante (par chapitre SH2 et par pays de destination) que la règle naïve « l'an prochain = cette année » ?

## Données
UN Comtrade (https://comtradeplus.un.org/) : exportations du Maroc, partenaires individuels, chapitres SH2, annuel, USD courants. Procédure d'extraction : `docs/fiche_CI01.md`. Placer le CSV dans `data/raw/`. Date d'extraction : [à renseigner].

## Exécution
```bash
pip install -r requirements.txt
jupyter notebook notebooks/projet_CI01.ipynb   # ou Google Colab
```
Exécuter les cellules dans l'ordre (graine fixée à 42, chemins relatifs). Les figures sont enregistrées dans `figures/`.

## Contenu du dépôt
`notebooks/projet_CI01.ipynb` · `rapport/rapport.pdf` · `presentation/` (6 diapositives PDF + source) · `video/demonstration.mp4` (ou lien ci-dessous) · `figures/` · `docs/` · `DECLARATION_IA.md` · `requirements.txt`

Lien vidéo (si non déposée) : [à compléter]
