# P0_SELECTION_PRODUIT

**Statut :** actif — Gate 0 en cours
**Livrable de gate :** décision de sélection (produit retenu ou arrêt) inscrite dans `JOURNAL_DECISIONS.md`.
**Méthode de référence :** `100_REFERENTIELS/REF_100_METHODE.md §4`.

---

## 1. Objectif

Sélectionner objectivement le produit pilote ATLAS parmi les candidats initiaux, ou décider l'arrêt d'ATLAS si aucun candidat ne franchit la grille.

## 2. Candidats initiaux

1. Brasero
2. Salon de jardin métal
3. Pergola
4. Jardinière métal
5. Table / banc extérieur

D'autres candidats peuvent être ajoutés avant clôture de P0, à condition d'appliquer la même grille.

## 3. Séquence

**Étape 1 — Fixation des pondérations** (ingénieur, avant collecte)
- Fixer les 9 pondérations pour le **score stratégique**.
- Fixer les 9 pondérations pour le **score de lancement**.
- Justifier chaque pondération (courte phrase) dans `JOURNAL_EVALUATIONS.md`.
- Somme des pondérations = 100 par score.

**Étape 2 — Application des vetos** (avant notation)
- Pour chaque candidat, vérifier les 5 vetos (V1 à V5, cf. REF_100 §4.4).
- Un veto appliqué = candidat éliminé, colonne `vetos` de la matrice renseignée avec l'ID, colonne `decision` = "ÉLIMINÉ".
- Un candidat éliminé n'est pas noté.

**Étape 3 — Collecte factuelle** (IA, sources publiques)
- Pour chaque critère et chaque candidat non éliminé, collecter la donnée sourcée.
- Colonne `source_<critère>` renseignée pour chaque note.
- Fourchettes de prix marché : plusieurs sources croisées (marketplaces, sites marques, comparateurs).
- Volume marché : estimations sourcées, pas d'invention. `[HYP]` explicite si donnée non disponible.

**Étape 4 — Notation** (ingénieur uniquement)
- Attribuer une note 1–5 par critère selon les ancres de `CRITERES_EVALUATION.md`.
- Une note = une ancre + une donnée sourcée.
- Notes intuitives interdites.

**Étape 5 — Calcul des scores**
- Score stratégique = Σ (note × pondération stratégique) / 100.
- Score de lancement = Σ (note × pondération lancement) / 100.

**Étape 6 — Décision Gate 0**
- Analyse comparative des deux scores.
- Le produit retenu peut être le premier au score de lancement, même s'il n'est pas premier au score stratégique (choix explicite de "produit d'apprentissage").
- Décision inscrite dans `JOURNAL_DECISIONS.md` (DEC-XXXX) avec justification.
- Création du dossier `200_PRODUITS/2XX_<NOM>/` uniquement à cette étape.

## 4. Livrables

- [ ] Pondérations fixées et journalisées.
- [ ] Vetos appliqués à chaque candidat.
- [ ] Collecte factuelle avec sources pour chaque note.
- [ ] Matrice complète (`MATRICE_MULTICRITERE.csv`).
- [ ] Journal d'évaluation renseigné.
- [ ] Décision Gate 0 inscrite dans le journal des décisions.

## 5. Critère d'arrêt ATLAS

Si aucun candidat ne survit à l'application des vetos, ou si tous les candidats survivants ont un score de lancement inférieur à un seuil que l'ingénieur juge insuffisant compte tenu du plafond capital, la décision de Gate 0 est **arrêt d'ATLAS**. Le dépôt est archivé, un REX final est produit.
