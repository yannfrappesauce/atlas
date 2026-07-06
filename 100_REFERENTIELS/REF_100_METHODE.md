# REF_100_METHODE

**Version :** 1.0
**Statut :** actif (section P0 complète, sections P1–P10 en squelette exigible)
**Dépendances aval :** tous les autres REF sont tirés par les gates définis ici.

---

## 1. Principe général

Le projet est piloté par **Stage Gates**.

Chaque phase produit un ou plusieurs **livrables opposables** (artefacts existants, pas des intentions), soumis à un **critère de sortie** avant passage au gate suivant.

Aucune phase suivante ne s'engage sans **décision explicite de passage** inscrite dans `000_CADRE/JOURNAL_DECISIONS.md`.

## 2. Vue d'ensemble

| Phase | Objet | Livrables opposables | Critère de sortie (Gate) |
|---|---|---|---|
| **P0** | Sélection produit pilote | Matrice multicritère renseignée + décision | **G0** : produit retenu ou arrêt |
| **P1** | Étude marché du produit retenu | Analyse concurrence, avis clients, canaux, prix, volumes plausibles | Marge brute estimée ≥ seuil + canal choisi |
| **P2** | Analyse produit | Fonctions, cinématique, efforts, matériaux candidats, modes de défaillance, teardown d'1–2 concurrents | Modes de défaillance identifiés et hiérarchisés |
| **P3** | CDC design-to-cost | CDC coté avec exigences d'essais, analyse de risques sécurité intégrée | CDC complet, opposable aux fabricants |
| **P4** | Conformité | Classement NC, normes applicables, REP, notice, dossier technique initialisé | Périmètre réglementaire soldé, coûts intégrés au calculateur |
| **P1→P4 combinés** | — | — | **G1** : coût complet estimé compatible + périmètre réglementaire chiffré + canal identifié |
| **P5** | Sourcing / RFQ | ≥5 fabricants (dont ≥1 UE si QO-07 validée), NNN signés, devis normalisés | **G2** : coût complet réel ≤ coût cible |
| **P6** | Prototypes | Golden sample, protocole d'essais (thermiques, corrosion, stabilité, assemblage) | Essais passés, golden sample contractualisé |
| **P7** | Pré-série et inspection | Inspection tierce partie, plan AQL, corrections | **G3** : qualité + conformité documentées avant paiement du solde |
| **P8** | Import / industrialisation | Incoterm, transitaire, assurance, dédouanement, contrôle réception | **G4** : stock ou proto réceptionné conforme |
| **P9** | Lancement commercial | Fiches, contenu, photos, pricing final, mise en vente | **G5** : RC produits active + obligations REP remplies avant 1re vente |
| **P10** | SAV / REX | DB_REX alimentée, taux SAV, CDC v2 | REX intégré, boucle fermée |

## 3. Kill criteria (rappel)

À tout gate, le projet pilote est arrêté si un des critères de DEC-0004 est constaté. À distinguer des vetos P0 (§4.4), qui portent sur l'élimination d'un candidat au stade de la sélection.

---

# 4. Phase P0 — Sélection du produit pilote

## 4.1 Principe

- L'IA collecte les données factuelles.
- L'ingénieur décide :
  - des pondérations ;
  - des notes ;
  - de l'application des vetos ;
  - de la décision finale.

Cette séparation est fondamentale : la pondération traduit une stratégie d'entreprise et n'est pas délégable à un modèle.

## 4.2 Candidats initiaux

- Brasero
- Salon de jardin métal
- Pergola
- Jardinière métal
- Table / banc extérieur

D'autres candidats peuvent être ajoutés avant la clôture de P0, à condition de leur appliquer la même grille.

## 4.3 Double score

Deux scores distincts sont calculés :

- **Score stratégique** : quel produit est intrinsèquement le meilleur candidat sur le long terme ?
- **Score de lancement** : quel produit est le meilleur à lancer maintenant, compte tenu du capital limité, du besoin d'apprentissage et du délai avant premier cash ?

Un candidat peut être stratégiquement meilleur mais opérationnellement inadapté : c'est la comparaison des deux scores qui informe la décision, pas un score unique.

Aucun troisième score de risque. Le risque est traité par vetos (§4.4).

## 4.4 Vetos P0 (élimination avant notation)

Un candidat est **éliminé sans notation** si l'un des vetos suivants s'applique :

- V1 : capital requis avant Gate 2 estimé > 3 000 € TTC (DEC-0003).
- V2 : obstacle réglementaire rédhibitoire identifié.
- V3 : délai probable avant premier cash incompatible avec la priorité projet.
- V4 : coût complet estimé incompatible avec le prix marché constaté.
- V5 : absence probable de fournisseur satisfaisant sur le canal envisagé.

Chaque veto appliqué est justifié dans `JOURNAL_EVALUATIONS.md` avec source.

## 4.5 Critères de notation

Les critères et leurs échelles ancrées sont définis dans `200_PRODUITS/000_SELECTION_PRODUIT/CRITERES_EVALUATION.md`.

**Critères actifs (v1) :**
1. Potentiel marché
2. Marge brute potentielle
3. Capital requis avant Gate 2
4. Densité valeur / poids
5. Saisonnalité
6. Complexité réglementaire
7. Complexité SAV
8. Potentiel de différenciation
9. Valeur d'apprentissage

**Pondérations :** à fixer par l'ingénieur avant notation, distinctes pour le score stratégique et le score de lancement. Les pondérations sont inscrites dans `JOURNAL_EVALUATIONS.md` avec justification.

## 4.6 Sortie Gate 0

Décision inscrite dans `JOURNAL_DECISIONS.md` :
- Produit retenu **ou** arrêt ATLAS.
- Si produit retenu : création du dossier `200_PRODUITS/2XX_<NOM_PRODUIT>/` avec placeholders P1–P10.
- Si arrêt : REX capitalisé, journal soldé, dépôt maintenu en archive.

---

# 5. Phases P1 à P10 — squelette

Chaque phase active fera l'objet d'un développement dans son propre référentiel ou dans le dossier produit, tiré par le besoin. Le squelette ci-dessous est **normatif quant aux livrables et critères de sortie**, non prescriptif sur la manière.

Les référentiels transverses (`REF_110` à `REF_195`) restent en placeholder jusqu'à activation par la phase concernée.

## Contenu à venir (activation par gate)

- **P1** → `REF_110_MARCHE.md` + `200_PRODUITS/2XX_.../P1_ETUDE_MARCHE.md`
- **P2** → `REF_145_ANALYSE_PRODUIT_UNIVERSELLE.md` (naissance) + `P2_ANALYSE_PRODUIT.md`
- **P3** → `REF_150_QUALITE.md` (template CDC) + `REF_140_MATERIAUX.md` (section produit) + `P3_CDC.md`
- **P4** → `REF_120_REGLEMENTAIRE.md` + `CONFORMITE/` dans le dossier produit
- **P5** → `REF_130_SOURCING.md` + `RFQ/` dans le dossier produit
- **P6–P7** → `REF_150_QUALITE.md` (essais et AQL) + `TESTS/` dans le dossier produit
- **P8** → `REF_160_LOGISTIQUE.md`
- **P9** → `REF_170_FINANCES.md` (pricing final) — la doctrine coût complet et le calculateur v0 sont eux tirés dès P1
- **P10** → `REF_180_SAV.md` + `REF_195_REX.md`
- **transverse continu** → `REF_190_IA.md` (automatisations, activées avec ROI démontré)
