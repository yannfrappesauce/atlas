# CRITERES_EVALUATION

**Statut :** actif — échelles v1 à valider par l'ingénieur avant notation.

**Règle :** chaque critère est noté de 1 à 5. Chaque note doit être justifiée par une donnée sourcée (colonne `source_*` dans la matrice) et alignée sur une ancre. Aucune note intuitive.

**Convention :** 3 = "acceptable, sans particularité forte". 5 = "excellent, avantage marqué". 1 = "défavorable, à considérer comme handicap".

---

## 1. Potentiel marché

Taille et vitalité du marché B2C français (canal envisagé).

| Note | Ancre |
|---|---|
| 1 | Marché faible ou en déclin, demande incertaine, peu de canaux actifs |
| 2 | Marché de niche, quelques centaines à quelques milliers d'unités/an |
| 3 | Marché existant et compétitif, plusieurs milliers d'unités/an |
| 4 | Marché important, plusieurs dizaines de milliers d'unités/an, demande visible |
| 5 | Marché de masse, plusieurs centaines de milliers d'unités/an, demande soutenue et croissante |

**Source attendue :** études de marché publiques, GfK, IRI, Xerfi si accessibles ; à défaut, extrapolation raisonnée à partir des volumes marketplace (à documenter comme `[HYP]`).

## 2. Marge brute potentielle

(Prix de vente marché cible − coût complet estimé) / prix de vente marché cible.

| Note | Ancre |
|---|---|
| 1 | < 20 % — non viable pour un acteur petit sans effet volume |
| 2 | 20 – 30 % — tendu, absorbe mal les imprévus |
| 3 | 30 – 40 % — acceptable |
| 4 | 40 – 55 % — confortable |
| 5 | > 55 % — marge premium |

**Source attendue :** prix marché moyen sur 3+ canaux + estimation coût complet via calculateur v0 (à construire).

## 3. Capital requis avant Gate 2

Estimation TTC de la trésorerie nécessaire jusqu'à disposer de devis fournisseurs comparables + prototypes échantillons.

| Note | Ancre |
|---|---|
| 1 | > 3 000 € — **VETO V1** (DEC-0003), candidat éliminé |
| 2 | 2 500 – 3 000 € — proche du plafond |
| 3 | 1 500 – 2 500 € |
| 4 | 800 – 1 500 € |
| 5 | < 800 € |

**Note :** ce critère est plus lourd pour le score de lancement que pour le score stratégique — les pondérations reflètent cette distinction.

## 4. Densité valeur / poids

Rapport prix de vente / poids unitaire (€/kg approx.). Détermine le coût relatif du transport et des retours.

| Note | Ancre |
|---|---|
| 1 | < 3 €/kg (produit très lourd, faible prix) — transport et retours pèsent lourd |
| 2 | 3 – 6 €/kg |
| 3 | 6 – 15 €/kg |
| 4 | 15 – 40 €/kg |
| 5 | > 40 €/kg — logistique légère |

## 5. Saisonnalité

Répartition des ventes sur l'année.

| Note | Ancre |
|---|---|
| 1 | > 70 % des ventes concentrées sur 3 mois — cash immobilisé sur cycle annuel |
| 2 | 50 – 70 % sur 3 mois |
| 3 | Saison marquée (5–6 mois) |
| 4 | Ventes réparties, léger pic saisonnier |
| 5 | Ventes réparties sur 12 mois |

**Source attendue :** Google Trends sur 5 ans, données marketplace saisonnières.

## 6. Complexité réglementaire

Charge de conformité avant mise sur le marché (RSGP, REP, normes sectorielles, RC produits).

| Note | Ancre |
|---|---|
| 1 | Risque réglementaire élevé ou mal cerné, veto V2 possible ; produits à feu ouvert, contact alimentaire direct, sécurité enfant |
| 2 | Obligations lourdes, normes sectorielles avec essais spécifiques requis |
| 3 | Obligations identifiables et gérables, sans essais lourds |
| 4 | RSGP générique + REP emballages, sans exigences sectorielles spécifiques |
| 5 | Contraintes faibles et bien connues, retour d'expérience abondant |

## 7. Complexité SAV

Coût et fréquence probables des retours et interventions.

| Note | Ancre |
|---|---|
| 1 | Produit fragile ou volumineux ; un retour coûte > 30 % de la marge unitaire |
| 2 | Retours fréquents anticipés, casse en transport probable |
| 3 | SAV gérable avec pièces simples |
| 4 | SAV rare, produit robuste, pièces standard |
| 5 | Quasi aucun SAV probable |

## 8. Différenciation possible

Espace de différenciation face aux concurrents établis (au-delà du prix).

| Note | Ancre |
|---|---|
| 1 | Commodité fortement copiée, différenciation impossible à faible échelle |
| 2 | Différenciation cosmétique uniquement (couleur, packaging) |
| 3 | Différenciation possible par qualité perçue et/ou design |
| 4 | Différenciation par usage, matériaux ou service (garantie étendue, notice, pièces) |
| 5 | Différenciation technique ou d'usage substantielle et défendable |

## 9. Valeur d'apprentissage

Ce que le projet enseignera à ATLAS si mené jusqu'au bout (indépendant du succès commercial).

| Note | Ancre |
|---|---|
| 1 | Apprentissage faible ou peu transférable à d'autres familles de produits |
| 2 | Apprentissage limité à cette catégorie |
| 3 | Apprentissages utiles pour plusieurs familles proches |
| 4 | Apprentissage structurant sur ≥3 étapes de la méthode (import, logistique, SAV, marketing…) |
| 5 | Apprentissage structurant sur l'ensemble de la méthode ATLAS, très largement transférable |

**Note :** ce critère pèse plus dans le score de lancement (justification du "produit d'apprentissage") que dans le score stratégique.

---

## Pondérations proposées (à valider par l'ingénieur)

Les valeurs ci-dessous sont **indicatives** et doivent être arbitrées avant la première notation.

| Critère | Poids stratégique | Poids lancement |
|---|---|---|
| 1. Potentiel marché | 20 | 10 |
| 2. Marge brute potentielle | 20 | 15 |
| 3. Capital requis avant Gate 2 | 5 | 25 |
| 4. Densité valeur/poids | 10 | 10 |
| 5. Saisonnalité | 5 | 10 |
| 6. Complexité réglementaire | 10 | 10 |
| 7. Complexité SAV | 5 | 5 |
| 8. Différenciation possible | 20 | 5 |
| 9. Valeur d'apprentissage | 5 | 10 |
| **Total** | **100** | **100** |

**Différences clés :** le score de lancement pénalise davantage un capital lourd, valorise davantage la valeur d'apprentissage et la saisonnalité. Le score stratégique valorise davantage marché et différenciation.

Ces pondérations sont **des propositions à arbitrer** dans `JOURNAL_EVALUATIONS.md` avant toute notation.
