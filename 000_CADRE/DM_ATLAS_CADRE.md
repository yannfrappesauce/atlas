# DM_ATLAS_CADRE

**Version :** 1.0
**Statut :** cadre initial validé
**Source de vérité pour :** vision, gouvernance, règles, index

---

## 1. Nature d'ATLAS

ATLAS est un programme d'ingénierie produit.

ATLAS n'est actuellement :
- ni une société ;
- ni une marque commerciale.

Une marque pourra naître d'ATLAS. Une structure juridique pourra porter cette marque après validation économique du projet pilote et discussion avec les futurs associés potentiels, notamment Julien Gottieb (voir DEC-0002, DEC-0013, DEC-0014 dans `JOURNAL_DECISIONS.md`).

## 2. Objectif

Construire une méthode reproductible permettant de :
- sélectionner un produit ;
- comprendre son marché ;
- l'analyser techniquement ;
- rédiger son cahier des charges en design-to-cost ;
- traiter sa conformité ;
- sourcer son fabricant ;
- valider un prototype ;
- l'importer ou le faire fabriquer ;
- le commercialiser ;
- capitaliser le retour d'expérience.

L'objectif à long terme est que la méthode devienne un actif TEKNEC réutilisable au-delà d'ATLAS.

## 3. Projet pilote (terminologie)

Le terme officiel est **Projet Pilote**. Le mot *démonstrateur* est abandonné dans toute la documentation ATLAS (voir DEC-0009, DEC-0012).

Un projet pilote ne valide pas seulement un prototype : il valide progressivement l'ensemble du processus industriel et commercial, gate après gate.

## 4. Portefeuille et priorité

- **TEKNEC** est l'activité principale (inclut Video Toolkit).
- **HCF** est une marque e-commerce indépendante.
- **ATLAS** est un programme indépendant, potentiellement co-porté.
- **Priorité :** TEKNEC > ATLAS (voir DEC-0001).

## 5. Règles centrales

### 5.1 Règle Stage Gate

Toute action ATLAS doit servir le franchissement du prochain Stage Gate. Une action utile mais qui ne sert pas ce gate va dans `BACKLOG.md`. Le backlog physique existe : sans lui, "reporter au backlog" équivaut à jeter.

### 5.2 Règle documentaire

Une décision non inscrite dans `JOURNAL_DECISIONS.md` est réputée ne pas exister.

Le journal est **append-only** : on ajoute une nouvelle décision qui complète ou remplace, on ne réécrit jamais une ancienne. La lecture chronologique du journal permet de reconstituer la logique du projet.

Chaque module de gouvernance est **autoportant** : il ne dépend pas de la mémoire d'une conversation. Toute information critique existe soit dans un fichier, soit pas du tout.

### 5.3 Règle just-in-time

Aucun référentiel `REF_*` ne se rédige avant d'être tiré par un besoin du gate en cours. Rédiger à blanc génère de la dette documentaire et détruit la traçabilité entre la méthode et le réel.

Exception : les sections directement liées à la sécurité et à la conformité (REF_120) peuvent être activées de manière anticipée si un candidat P0 le nécessite.

### 5.4 Règle de promotion transverse

Une méthode issue d'ATLAS ne devient un référentiel transverse TEKNEC qu'à sa **2e utilisation** — c'est-à-dire lorsqu'un second projet la mobilise. Ce critère remplace le flou "quand elle a prouvé sa valeur". Une seule utilisation ne permet pas de distinguer le générique du spécifique-projet.

Au moment de la promotion : REX formalisé + migration `git mv` + mise à jour des liens dans les projets qui la référencent.

### 5.5 Règle multi-IA

- **ChatGPT** : recherche web, challenge de méthode, vérification, stratégie, technique amont.
- **Claude AI (web)** : critique, consolidation, architecture documentaire, arbitrages sur gros contexte.
- **Claude Code (local)** : exécution sur fichiers, Git, scripts, missions courtes et vérifiables.
- **Codex** : code, automatisations, extraction structurée, calculs.

Les modifications réelles du dépôt passent par Claude Code ou humain. ChatGPT et Claude AI ne modifient pas le dépôt directement.

### 5.6 Règle de notation ancrée

Toute note dans une matrice multicritère (P0 et suivantes) doit être :
- portée sur une échelle 1–5 avec ancres factuelles définies dans `CRITERES_EVALUATION.md` ;
- justifiée par une donnée sourcée (colonne `source_*` renseignée dans le CSV) ;
- traçable dans `JOURNAL_EVALUATIONS.md`.

Aucune notation intuitive n'est autorisée.

## 6. Vetos et kill criteria — distinction

Deux mécanismes distincts, à ne pas confondre :

- **Vetos P0** : critères d'élimination d'un candidat au stade de la sélection. Un candidat frappé d'un veto ne peut pas être noté ; il est éliminé de la matrice. Vetos définis dans `REF_100_METHODE.md §P0`.
- **Kill criteria projet pilote** : critères d'arrêt du projet pilote après le Gate 0. Peuvent se déclencher à n'importe quel gate. Liste dans DEC-0004.

## 7. Garde-fou méthode

**La méthode n'est jamais une sortie de gate.**

Une méthode ne se valide pas par sa complétude documentaire ; elle se valide par un résultat observable sur un projet réel qui franchit le gate correspondant. Un CDC amélioré n'est pas un livrable de P3 : le livrable est *le CDC opposable à un fabricant*. Une réflexion sur le sourcing n'est pas un livrable de P5 : le livrable est *les RFQ émises et les devis reçus*.

Si le candidat n°1 meurt à un gate, ATLAS relance le candidat n°2 par la même grille, ou s'arrête. "Améliorer la méthode" ne sort jamais d'un gate.

## 8. Infrastructure

L'infrastructure de développement est stabilisée hors ATLAS (voir dépôt `DEVOPS_STATION_IA`). Aucun nouveau chantier d'infrastructure n'est ouvert depuis ATLAS sans besoin réel démontré du projet.

## 9. Références internes

- `000_CADRE/JOURNAL_DECISIONS.md` — décisions append-only
- `000_CADRE/REGISTRE_RISQUES.md` — risques identifiés
- `000_CADRE/BACKLOG.md` — actions différées hors gate courant
- `000_CADRE/BACKLOG_VERIFICATIONS.md` — points [AV] à vérifier sur source primaire
- `000_CADRE/QO_QUESTIONS_OUVERTES.md` — questions ouvertes actives
- `000_CADRE/ROADMAP.md` — séquence des gates
- `000_CADRE/PAQUET_PASSATION_ATLAS.md` — synthèse de reprise
- `100_REFERENTIELS/REF_100_METHODE.md` — stage gates et méthode P0
