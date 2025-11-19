# TP1 — Cartographier un dataset (RGPD & sécurité des données)

But principal
- Sensibiliser et appliquer des mesures simples de protection des données personnelles selon les principes du RGPD.
- Identifier les colonnes personnelles, sensibles et non‑identifiantes, proposer et appliquer des transformations (suppression, pseudonymisation, généralisation, bruit léger) pour réduire le risque d’identification.

Ce que fait le projet
- Génère un jeu de données synthétique représentatif.
- Propose une classification heuristique des colonnes (personnelle / sensibles / quasi‑identifiantes / non‑identifiantes).
- Permet d’ajuster manuellement la classification.
- Définit et applique un plan de protection colonne → mesure (drop, hash, bin, noise, keep, ...).
- Exporte un livrable (tableau de décisions) et le dataset transformé.

Fichiers clés
- Notebook principal : tp1_rgpd_cartographie.ipynb
- Sorties : outputs/livrable_cartographie.csv, outputs/dataset_anonymized.csv

Usage rapide
1. Ouvrir et exécuter tp1_rgpd_cartographie.ipynb.
2. Vérifier/ajuster la classification (CATEGORY_OVERRIDE).
3. Compléter/valider le plan de protection (plan_protection).
4. Exécuter l’application du plan et exporter les fichiers.

Remarques importantes
- Le hachage SHA‑256 utilisé est une pseudonymisation (nécessite gestion du sel).
- Le bruit appliqué n’est pas une garantie de Differential Privacy formelle ; pour une DP rigoureuse, appliquer des mécanismes sur des agrégats.
- Usage pédagogique uniquement — adapter les mesures pour un contexte production et un audit RGPD complet.

Licence
- Usage pédagogique.
```//