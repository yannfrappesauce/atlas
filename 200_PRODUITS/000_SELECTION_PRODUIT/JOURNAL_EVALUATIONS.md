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
