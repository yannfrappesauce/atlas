# CHANGELOG

**Note :** ce changelog documente les évolutions structurelles du dépôt ATLAS (arborescence, référentiels, gouvernance). Les décisions métier vivent dans `JOURNAL_DECISIONS.md`.

## v1.0 — 2026-07-06

### Créé
- Arborescence initiale : `000_CADRE`, `100_REFERENTIELS`, `200_PRODUITS`, `300_DATA`, `400_OUTILS`, `900_ARCHIVES`.
- Gouvernance complète : `DM_ATLAS_CADRE`, `JOURNAL_DECISIONS` (DEC-0001 à DEC-0018), `REGISTRE_RISQUES` (RSQ-01 à RSQ-10), `BACKLOG`, `BACKLOG_VERIFICATIONS` (AV-01 à AV-12), `QO_QUESTIONS_OUVERTES` (QO-01 à QO-10), `ROADMAP`, `PAQUET_PASSATION_ATLAS`.
- Référentiel méthode `REF_100_METHODE` avec stage gates P0–P10 et section P0 complète.
- Référentiels transverses `REF_110` à `REF_195` en placeholders (activation just-in-time).
- Section P0 : `P0_SELECTION_PRODUIT`, `CRITERES_EVALUATION` (échelles 1–5 ancrées, 9 critères), `MATRICE_MULTICRITERE.csv` (5 candidats initiaux, 32 colonnes), `JOURNAL_EVALUATIONS`.
- Bases de données CSV vides : 9 fichiers avec en-têtes normalisés.
- Racine : `README`, `CLAUDE.md`, `CODEX.md`, `.gitignore`.

### Écarté par rapport aux propositions antérieures
- Dossiers `500_DOCUMENTS_EXTERNES`, `600_IMPORT`, `700_MARQUE`, `800_REX` — sur-anticipation, création différée.
- Dossier `201_BRASERO` — biais d'engagement, création conditionnée au Gate 0.
- Objectif "DM 100–300 pages" — remplacé par référentiel modulaire tiré par les gates.
