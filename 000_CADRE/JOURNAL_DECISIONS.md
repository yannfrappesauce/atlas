# JOURNAL_DECISIONS

**Règle :** une décision non inscrite ici est réputée ne pas exister.
**Mode :** append-only. Toute nouvelle décision est ajoutée en bas. Une décision remplacée est marquée `REMPLACÉE PAR DEC-XXXX` sans être supprimée.

---

## DEC-0001 — Portefeuille de projets et priorité

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
- TEKNEC constitue l'activité principale (inclut Video Toolkit comme sous-projet).
- HCF est une marque e-commerce indépendante.
- ATLAS est un programme d'ingénierie produit indépendant.
- Priorité de charge : TEKNEC > ATLAS.

---

## DEC-0002 — Structure juridique ATLAS différée

**Date :** 2026-07-06
**Statut :** VALIDÉ
**Voir aussi :** DEC-0013, DEC-0014

**Décision :**
La structure juridique d'ATLAS reste volontairement non décidée.

Elle sera arrêtée après :
- validation commerciale du projet pilote (Gate 2 minimum) ;
- validation économique ;
- discussion avec les futurs associés, notamment Julien Gottieb.

Aucune société ne sera créée avant Gate 2.

---

## DEC-0003 — Capital maximal avant Gate 2

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
Le capital maximal engagé sur ATLAS avant Gate 2 est fixé à **3 000 € TTC**.

Ce plafond est un veto au sens de DEC-0010 : tout candidat P0 dont le capital requis avant Gate 2 dépasse ce plafond est éliminé sans notation.

---

## DEC-0004 — Kill criteria projet pilote

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
Le projet pilote est arrêté si l'un des critères suivants est constaté à un gate :
- plafond de capital dépassé (DEC-0003) ;
- coût complet incompatible avec le marché cible ;
- marge brute cible impossible à atteindre ;
- obstacle réglementaire majeur non contournable ;
- MOQ incompatible avec la trésorerie disponible ;
- aucun fournisseur satisfaisant identifié après 5 RFQ.

Ces critères sont des vetos, pas des notes pondérées.

**Distinction avec DEC-0010** : les vetos P0 éliminent un *candidat* au stade de la sélection ; les kill criteria arrêtent le *projet pilote* après sélection.

---

## DEC-0005 — Remote Git privé

**Date :** 2026-07-06
**Statut :** VALIDÉ
**Voir aussi :** DEC-0015

**Décision :**
Chaque dépôt actif possède un remote GitHub privé.

Ce choix est considéré comme sauvegarde minimale, pas comme nouveau chantier d'infrastructure. À mettre en place au premier commit du dépôt.

---

## DEC-0006 — Méthode de notation ancrée

**Date :** 2026-07-06
**Statut :** VALIDÉ
**Voir aussi :** DEC-0011

**Décision :**
Toutes les notes de matrice multicritère (P0 et suivantes) doivent être :
- ancrées sur une échelle 1–5 avec ancres factuelles ;
- justifiées par une donnée sourcée ;
- traçables dans le journal d'évaluation.

Aucune notation intuitive n'est autorisée.

---

## DEC-0007 — Validation de la méthode

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
Une étape de la méthode n'est validée qu'après avoir produit un résultat observable sur un projet réel et permis de franchir le Stage Gate correspondant.

La méthode complète est validée lorsque plusieurs produits ont traversé plusieurs gates.

Corollaire : "améliorer la méthode" n'est jamais une sortie de gate.

---

## DEC-0008 — Nature d'ATLAS

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
ATLAS est un programme d'ingénierie produit. ATLAS n'est actuellement ni une société ni une marque commerciale.

---

## DEC-0009 — Projet pilote (terminologie)

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
Le terme *démonstrateur* est remplacé par **projet pilote** dans toute la documentation ATLAS. Le premier produit doit valider tout ou partie du processus industriel et commercial, pas seulement un prototype.

---

## DEC-0010 — Vetos hors scoring

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
Le risque ne fait pas l'objet d'un troisième score. Les risques bloquants sont traités par des vetos éliminatoires hors scoring.

**Vetos P0 initiaux :**
- capital requis avant Gate 2 > 3 000 € TTC ;
- obstacle réglementaire rédhibitoire identifié ;
- délai avant premier cash incompatible avec la priorité projet ;
- coût complet estimé incompatible avec le prix marché constaté ;
- absence probable de fournisseur satisfaisant sur le canal envisagé.

Un candidat frappé d'un veto est éliminé sans notation.

---

## DEC-0011 — Échelle de notation ancrée

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
Chaque critère de P0 dispose d'une échelle 1 à 5 avec ancres factuelles définies dans `200_PRODUITS/000_SELECTION_PRODUIT/CRITERES_EVALUATION.md`. Chaque note dans la matrice doit citer la donnée qui la justifie (colonne `source_*`).

---

## DEC-0012 — Double score, pas de troisième

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
Deux scores sont calculés en P0 :
- **Score stratégique** : quel produit est intrinsèquement le meilleur candidat ?
- **Score de lancement** : quel produit est le meilleur à lancer maintenant, compte tenu du capital limité, du besoin d'apprentissage, du délai avant premier cash ?

Un candidat peut être stratégiquement meilleur mais opérationnellement inadapté ; c'est la comparaison des deux scores qui informe la décision, pas un score unique.

Aucun troisième score de risque : le risque est traité par vetos (DEC-0010).

---

## DEC-0013 — Structure juridique ATLAS différée (confirmation)

**Date :** 2026-07-06
**Statut :** VALIDÉ
**Voir aussi :** DEC-0002, DEC-0014

**Décision :**
Distinction à trois niveaux :
- **Niveau 1** — ATLAS = méthode de développement produit (actif intellectuel) ;
- **Niveau 2** — marque commerciale (à définir plus tard) ;
- **Niveau 3** — structure juridique (SAS, SARL, etc.) — décidée seulement après validation produit + modèle économique + associés identifiés.

---

## DEC-0014 — Julien Gottieb comme associé potentiel

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
ATLAS n'est pas considéré comme un projet nécessairement porté seul. Julien Gottieb (plusieurs sociétés existantes) est identifié comme associé potentiel à consulter avant toute décision juridique ou capitalistique engageante.

Cette décision n'engage pas Julien à ce stade ; elle inscrit son rôle possible dans la gouvernance.

---

## DEC-0015 — Sauvegarde par remote Git privé

**Date :** 2026-07-06
**Statut :** VALIDÉ
**Voir aussi :** DEC-0005

**Décision :**
Un remote GitHub privé est mis en place dès le premier commit. Constitue la sauvegarde minimale du dépôt. N'est pas comptabilisé comme nouveau chantier d'infrastructure au sens du gel infra.

---

## DEC-0016 — Règle de promotion transverse

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
Une méthode issue d'ATLAS devient un référentiel transverse TEKNEC uniquement à sa **2e utilisation** — c'est-à-dire lorsqu'un second projet la mobilise concrètement.

Ce critère remplace le flou "quand elle a prouvé sa valeur". Attendre un REX de deux projets est trop lent (coût d'opportunité) ; se contenter d'une seule utilisation ne permet pas de distinguer le générique du spécifique-projet.

Au moment de la promotion : REX formalisé + migration `git mv` + mise à jour des liens.

---

## DEC-0017 — Architecture initiale minimale

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
L'arborescence de départ est limitée à : `000_CADRE`, `100_REFERENTIELS`, `200_PRODUITS`, `300_DATA`, `400_OUTILS`, `900_ARCHIVES`.

Les dossiers `500_DOCUMENTS_EXTERNES`, `600_IMPORT`, `700_MARQUE`, `800_REX` proposés antérieurement sont **retirés** : sur-anticipation contraire à la règle just-in-time. Ils seront créés au moment où un livrable les rend nécessaires, chacun documenté par une décision au moment de sa création.

Aucun dossier produit spécifique (ex. `201_BRASERO`) n'est créé avant le Gate 0 : biais d'engagement à éviter.

---

## DEC-0018 — Modèle par défaut Claude

**Date :** 2026-07-06
**Statut :** VALIDÉ

**Décision :**
Modèle Claude par défaut pour l'exécution documentaire ATLAS : **Sonnet**. Opus/Fable réservé aux arbitrages d'architecture ou critiques de fond, avec justification.

Cette règle s'applique dans Claude Code (choix du modèle par session) et pour les prompts adressés à Claude AI (web).

---

## DEC-0019 - Revision periodique des ponderations P0

**Date :** 2026-07-06
**Statut :** VALIDE

**Decision :**
Trois points de controle des ponderations P0 :
1. Avant Gate 0 : une seule revision autorisee, uniquement si un critere se revele indiscriminant (>=4 candidats/5 obtiennent la meme note).
2. A chaque nouveau P0 : relecture obligatoire avant application.
3. A chaque Gate >=2 (franchi ou rate) : REX confronte la ponderation au resultat reel.

**Mecanisme :** entree EVAL dans JOURNAL_EVALUATIONS + DEC dans JOURNAL_DECISIONS + increment de version (v1, v2...). Colonne version_ponderations dans MATRICE_MULTICRITERE.csv.

---

## DEC-0020 - Rythme ATLAS periode P0

**Date :** 2026-07-06
**Statut :** VALIDE
**Reference :** QO-10

**Decision :**
Rythme alloue a ATLAS pendant la periode P0 : 20 h/semaine sur les semaines ou ATLAS est le projet actif.

**Precisions :**
- ATLAS est un projet a activation ponctuelle, pas continu. Les semaines sans ATLAS existent.
- DEC-0001 (TEKNEC > ATLAS) s'applique aux semaines de conflit hebdomadaire, pas au lissage global.
- Reexamen apres Gate 0 : le rythme post-P0 sera fixe par une nouvelle DEC.

**Kill criteria de rythme :**
- Si Gate 0 non atteint apres 3 semaines actives ATLAS : diagnostic explicite (methode inadaptee, candidats mal choisis, ou charge externe trop forte).

---

## DEC-0021 - Choix brasero hors matrice P0

**Date :** 2026-07-06
**Statut :** VALIDE (assume hors gouvernance standard)

**Decision :** Le brasero est retenu comme produit pilote sans passer la grille P0 complete.

**Justification :** interet personnel du porteur + refus d'investir 14-20h en selection multicriteres pour un premier produit sur lequel l'intuition est forte.

**Consequences assumees :**
- DEC-0007 (methode validee par resultat) et DEC-0016 (methode reproductible) ne s'appliquent pas au 1er produit ATLAS mais s'appliqueront au 2e produit.
- Angle mort documente : le perimetre 'amenagement interieur/exterieur' du DM_PROJET_ATLAS_V1 est une hypothese non validee, heritee de la redaction initiale (ChatGPT). Non conteste pour ce 1er produit.
- Pergola exclue du perimetre ATLAS (produit sur-mesure, EVAL-0002).
- Salon de jardin metal, Jardiniere metal, Table/banc exterieur : reportes au backlog (BL-010).

**Reference :** DEC-0014 (Julien Gottieb informe requis avant decision engageante ulterieure).
