# ROADMAP ATLAS

**Vue :** séquence des Stage Gates et livrables associés. Aucun engagement de date : la roadmap est *conditionnelle*, chaque gate étant franchi ou non selon les critères de sortie définis dans `REF_100_METHODE.md`.

## Gates

| Gate | Phase | Objet | Critère de sortie |
|---|---|---|---|
| **G0** | P0 | Sélection du produit pilote | Produit retenu par la grille multicritère (ou arrêt) |
| **G1** | P1 → P4 | Étude marché, analyse produit, CDC, conformité | Coût complet estimé compatible + marge brute estimée ≥ seuil + canal identifié + périmètre réglementaire chiffré |
| **G2** | P5 | Sourcing et RFQ | Coût complet réel ≤ coût cible (≥5 fabricants dont ≥1 UE si QO-07 validée) |
| **G3** | P6–P7 | Prototypes, essais, pré-série, inspection | Qualité et conformité documentées **avant** paiement du solde |
| **G4** | P8 | Import et réception | Stock ou proto réceptionné conforme |
| **G5** | P9 | Lancement commercial | RC produits active + obligations REP remplies avant 1re vente |
| — | P10 | SAV / REX | DB_REX alimentée, CDC v2, boucle fermée vers le candidat suivant ou arrêt |

## État actuel

- **Gate en cours :** G0 (P0 — Sélection du produit pilote).
- **Livrables attendus :** matrice multicritère renseignée, critères d'évaluation ancrés, journal d'évaluation, décision de gate.

## Prochaines actions

1. Renseigner `200_PRODUITS/000_SELECTION_PRODUIT/CRITERES_EVALUATION.md` (échelles 1–5 déjà proposées, à valider).
2. Collecter les données factuelles pour chaque candidat initial (Brasero, Salon de jardin métal, Pergola, Jardinière métal, Table/banc extérieur).
3. Renseigner `MATRICE_MULTICRITERE.csv` colonne par colonne avec sources.
4. Appliquer les vetos (DEC-0010) avant notation.
5. Décision Gate 0 → produit retenu (ou arrêt) → création du dossier produit `2XX_<NOM>` uniquement à ce moment.

## Après le Gate 0

La roadmap détaillée post-G0 (P1–P10) sera précisée dans le dossier du produit retenu, selon ses spécificités. Les référentiels transverses `REF_1XX` seront activés au fil des besoins tirés par les gates.
