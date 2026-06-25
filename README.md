# Prédimensionnement Structure Métallique

Outil de prédimensionnement rapide de structures métalliques industrielles (IPE / HEA / HEB), conforme aux Eurocodes EC1 et EC3.

## Démonstration

👉 **[Ouvrir l'outil en ligne](https://ltourneur69-netizen.github.io/predimensionnement-structure-metallique/)**

## Fonctionnalités

- **Trame calculée automatiquement** à partir des dimensions globales et des portées maximales admissibles (formule `ceil(Dimension / Portée_max)`)
- **Charges en t/m²** par niveau (permanentes G + exploitation Q), converties en kN/m² selon EC1
- **Hauteur personnalisable par niveau** (prise en compte dans le schéma et le calcul de flambement)
- **Sélection guidée de la nuance d'acier** (S235 / S355 / S460) avec descriptif pour non-spécialistes
- **Validation en temps réel des portées** avec alertes colorées (valeurs irréalistes, hors plage)
- **3 onglets de résultats** :
  - Tableau des profils recommandés (poteaux HEA/HEB + poutres IPE)
  - Schéma de principe SVG (vue de face proportionnelle + vue en plan)
  - Note de calcul détaillée avec toutes les hypothèses
- **Presets d'usage** : Stockage · Industriel · Bureau · Parking
- **Mode sombre automatique** (suit les préférences système)
- **Impression** via Ctrl+P

## Méthode de calcul

| Élément | Méthode |
|---------|---------|
| Trame | `N_travées = ceil(Dimension / Portée_max)` |
| Poutres | Bi-appuyée — `M_sd = q·L²/8` — vérification plastique `W_pl` |
| Poteaux | Descente de charges cumulative + flambement `χ = 0.70` |
| Combinaison | EC1 : `E_d = γ_G·G + γ_Q·Q` |

## Limites de l'outil

> ⚠️ **Estimation préliminaire (±25%) pour phases d'avant-projet uniquement.**

Non pris en compte : vent (EC1-4), séisme (EC8), contreventements, vérification ELS (flèches), assemblages, effets du 2ᵉ ordre, charges dynamiques ou de fatigue.

## Utilisation

Fichier **100% autonome** — aucune dépendance, aucune installation.  
Ouvrir `predimensionnement_structure_metallique.html` dans n'importe quel navigateur moderne.

## Licence

MIT — libre d'utilisation, de modification et de redistribution.
