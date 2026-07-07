# JOURNAL_EVALUATIONS

**Rôle :** trace toutes les décisions d'évaluation faites au stade P0 : arbitrage des pondérations, application des vetos, choix de notation quand plusieurs sources divergent, justifications qualitatives.

**Règle :** aucune note dans `MATRICE_MULTICRITERE.csv` sans entrée correspondante dans ce journal (arbitrage explicite) ou dans les colonnes `source_*` de la matrice (donnée factuelle sourcée).

**Format d'entrée :**

```
### EVAL-XXXX — [Candidat] — [Critère ou action]
Date :
Auteur :
Décision / Notation :
Justification :
Sources :
```

---

## Arbitrages transverses

### EVAL-0001 — Pondérations score stratégique

**Date :** *à renseigner au moment de la fixation*
**Auteur :**
**Décision :**
- Potentiel marché : __
- Marge brute potentielle : __
- Capital requis avant Gate 2 : __
- Densité valeur/poids : __
- Saisonnalité : __
- Complexité réglementaire : __
- Complexité SAV : __
- Différenciation possible : __
- Valeur d'apprentissage : __
- **Total : 100**

**Justification :**

---

### EVAL-0002 — Pondérations score de lancement

**Date :**
**Auteur :**
**Décision :**
- (idem structure, avec pondérations distinctes)
- **Total : 100**

**Justification :** (typiquement : plus de poids sur capital requis, valeur d'apprentissage et saisonnalité ; moins sur marché et différenciation qui sont des critères de long terme)

---

## Vetos appliqués

*Entrées à créer au fil de l'analyse candidat par candidat.*

### EVAL-VETO-XXXX — [Candidat] — [Veto VX]

**Date :**
**Auteur :**
**Veto invoqué :**
**Fait constaté :**
**Source :**
**Conséquence :** candidat éliminé.

---

## Notations candidat par candidat

*Une section par candidat, une sous-entrée par critère quand la notation demande arbitrage (données divergentes, hypothèse à formuler, etc.).*

### Brasero

*à renseigner*

### Salon de jardin métal

*à renseigner*

### Pergola

*à renseigner*

### Jardinière métal

*à renseigner*

### Table / banc extérieur

*à renseigner*

---

## Décision Gate 0

*À inscrire ici en synthèse, puis officialiser dans `000_CADRE/JOURNAL_DECISIONS.md` comme `DEC-XXXX — Résultat Gate 0`.*

---

## EVAL-0001 - Ponderations v1 (score strategique et lancement)

**Date :** 2026-07-06
**Auteur :** Yann Frappesauce
**Version :** v1

| Critere | Strat | Lancement |
|---|---|---|
| 1. Potentiel marche | 25 | 10 |
| 2. Marge brute potentielle | 25 | 20 |
| 3. Capital requis avant Gate 2 | 5 | 15 |
| 4. Densite valeur/poids | 10 | 10 |
| 5. Saisonnalite | 5 | 10 |
| 6. Complexite reglementaire | 15 | 15 |
| 7. Complexite SAV | 5 | 5 |
| 8. Differenciation possible | 10 | 5 |
| 9. Valeur d'apprentissage | 0 | 10 |
| **Total** | **100** | **100** |

**Justification :**
- Capital requis a 15 (pas 25) en lancement : evite double penalisation avec veto V1.
- Reglementaire a 15 : coherent avec la gravite des trous identifies (RSGP, REP, RC produits).
- Differenciation a 10 : critere subjectif en P0, ne merite pas 20.
- Valeur d'apprentissage a 0 strategique : l'apprentissage n'est pas une qualite intrinseque du produit.

**Revision autorisee** : voir DEC-0019 (avant Gate 0, si critere indiscriminant).

---

## EVAL-0002 - Retrait Pergola des candidats P0

**Date :** 2026-07-06
**Auteur :** Yann Frappesauce

**Decision :** Pergola retiree de la liste des candidats P0.

**Justification :** produit intrinsequement sur-mesure, incompatible avec le modele ATLAS (produit standardise importable ou fabricable en serie). Hors perimetre.

**Consequence :** 4 candidats restants (Brasero, Salon de jardin metal, Jardiniere metal, Table/banc exterieur).
