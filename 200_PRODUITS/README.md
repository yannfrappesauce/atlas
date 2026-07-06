# 200_PRODUITS

Ce dossier contient :

1. **`000_SELECTION_PRODUIT/`** — travail actif de sélection au stade P0. Contient la grille, la matrice, les critères et le journal d'évaluation.

2. **Dossiers produits `2XX_<NOM_PRODUIT>/`** — **créés uniquement au Gate 0** lorsqu'un produit est retenu.

## Règle stricte

Aucun dossier produit spécifique (par exemple `201_BRASERO`) n'est créé avant que le Gate 0 ne l'ait explicitement retenu. Créer un dossier produit à l'avance = biais d'engagement, contraire à la doctrine (voir `000_CADRE/JOURNAL_DECISIONS.md#DEC-0017`).

## Contenu type d'un dossier produit (à la création au Gate 0)

```
2XX_<NOM_PRODUIT>/
├── PROD_<NOM>_DOSSIER.md      dossier maître produit : statut, gates franchis, index local
├── P1_ETUDE_MARCHE.md
├── P2_ANALYSE_PRODUIT.md
├── P3_CDC.md
├── P4_CONFORMITE.md
├── P5_SOURCING_RFQ.md
├── P6_PROTOTYPES.md
├── P7_VALIDATION.md
├── P8_IMPORT.md
├── P9_LANCEMENT.md
├── P10_SAV_REX.md
├── RFQ/            RFQ émises + réponses fournisseurs
├── TESTS/          protocoles + résultats
└── CONFORMITE/     analyse de risques, notice, dossier technique
```

Les fichiers `PX_*.md` sont créés au moment où la phase est engagée, pas à l'avance.
