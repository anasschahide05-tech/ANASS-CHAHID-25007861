# Fiche du sujet CI01 — Prévision des exportations marocaines

- **Question (énoncé) :** prédire les exportations par produit et destination.
- **Modèles conseillés :** Ridge, Random Forest, boosting. **Retenu :** Ridge (algorithme principal, famille régression), Random Forest en alternative.
- **Sources :** S1 (UN Comtrade), S9 (Office des Changes, pour recoupement éventuel).

## Extraction UN Comtrade+ (à faire avant le TP)
1. Aller sur https://comtradeplus.un.org/ puis *Trade Data*.
2. Type : *Goods* ; fréquence : *Annual* ; classification : *HS* (dernière révision disponible).
3. Période : 2010 à la dernière année disponible (au moins 9 années ; un compte gratuit est parfois nécessaire).
4. Déclarant : *Morocco*. Flux : *Export*.
5. Partenaires : sélectionner **tous les pays individuellement** (ne pas cocher « World » seul). Mode de transport et code douanier : *All / Total*.
6. Produits : chapitres à 2 chiffres (*AG2*), tous.
7. Télécharger le CSV, le nommer `comtrade_maroc_export_SH2.csv` et le placer dans `data/raw/`. Noter la **date d'extraction** et la **licence / conditions d'utilisation** affichées par le site.

Si le téléchargement dépasse les limites de l'interface, découper par période et concaténer les fichiers (le notebook lit un seul CSV).

## Colonnes attendues (noms Comtrade+)
`refYear`, `flowCode`, `reporterDesc`, `partnerCode`, `partnerDesc`, `cmdCode`, `cmdDesc`, `primaryValue`. Le notebook reconnaît aussi quelques noms alternatifs.

## Références
- UN Comtrade : https://comtradeplus.un.org/
- scikit-learn, Ridge : https://scikit-learn.org/stable/modules/linear_model.html#ridge-regression
- Hoerl & Kennard (1970), *Ridge regression: biased estimation for nonorthogonal problems*, Technometrics.
