# PAQUET_PASSATION_ATLAS

**Objectif :** permettre à toute IA (ChatGPT, Claude AI, Claude Code, Codex) ou humain de reprendre ATLAS **sans perte de contexte** et sans avoir à relire l'historique des conversations.

Ce document est le **point d'entrée obligatoire** pour toute reprise. Il est autoportant : il contient les décisions clés et pointe vers les fichiers qui font foi.

---

## 1. Nature et statut

- ATLAS est un **programme d'ingénierie produit**, pas une société ni une marque.
- Statut : initialisation v1, **Gate 0 en cours** (sélection du produit pilote).
- Terminologie : on dit **projet pilote**, pas *démonstrateur*.

## 2. Portefeuille et priorité

- TEKNEC (inclut Video Toolkit) : activité principale.
- HCF : marque e-commerce indépendante.
- ATLAS : programme indépendant, potentiellement co-porté avec Julien Gottieb (associé potentiel, à consulter avant décision engageante).
- Priorité de charge : **TEKNEC > ATLAS**.

## 3. Décisions critiques (verrous)

| Sujet | Décision | Ref |
|---|---|---|
| Capital maximal avant Gate 2 | **3 000 € TTC** | DEC-0003 |
| Structure juridique | Non décidée avant Gate 2 | DEC-0002, DEC-0013 |
| Julien Gottieb | Associé potentiel à consulter | DEC-0014 |
| Sauvegarde | Remote GitHub privé par dépôt actif | DEC-0005, DEC-0015 |
| Notation P0 | Échelle 1–5 ancrée, chaque note sourcée | DEC-0006, DEC-0011 |
| Scoring | 2 scores (stratégique + lancement), pas de 3e score risque | DEC-0012 |
| Risque | Traité par vetos hors scoring | DEC-0010 |
| Kill criteria | Liste écrite pour arrêt du projet pilote | DEC-0004 |
| Méthode | Validée par résultat observable + franchissement de gate | DEC-0007 |
| Promotion transverse | À la 2e utilisation | DEC-0016 |
| Modèle Claude par défaut | Sonnet | DEC-0018 |

## 4. Règles de gouvernance

- **Règle Stage Gate** : toute action ATLAS doit servir le prochain gate, sinon → `BACKLOG.md`.
- **Règle documentaire** : une décision non inscrite dans `JOURNAL_DECISIONS.md` n'existe pas. Le journal est append-only.
- **Règle just-in-time** : aucun référentiel ne se rédige avant d'être tiré par un gate.
- **Garde-fou méthode** : "améliorer la méthode" ne sort jamais d'un gate. Un livrable de gate est un artefact opposable (CDC envoyé, RFQ reçues, prototype réceptionné, produit vendu).

## 5. Rôles des IA (règle multi-IA)

- **ChatGPT** : recherche web, challenge, vérification, technique amont.
- **Claude AI (web)** : critique, consolidation, architecture, arbitrages.
- **Claude Code (local)** : exécution fichiers, Git, scripts.
- **Codex** : code, automatisations, extraction structurée.

Les modifications réelles du dépôt passent par Claude Code ou humain. ChatGPT et Claude AI ne modifient pas le dépôt directement.

## 6. Interdictions

- Ne pas inventer de données marché, prix, sources, normes, chiffres.
- Ne pas remplir les référentiels `REF_*` à blanc.
- Ne pas créer de nouvelle architecture (dossier, taxonomie) sans décision journalisée.
- Ne pas créer de dossier produit spécifique (`2XX_<nom>`) avant que le Gate 0 ne l'ait retenu.
- Ne pas considérer qu'une décision existe si elle n'est pas dans `JOURNAL_DECISIONS.md`.
- Ne pas confondre méthode et résultat commercial.

## 7. Prochain Gate — G0

**Objectif :** choisir objectivement le produit pilote ATLAS parmi les candidats initiaux, ou décider l'arrêt.

**Candidats initiaux :**
1. Brasero
2. Salon de jardin métal
3. Pergola
4. Jardinière métal
5. Table / banc extérieur

**Livrables attendus pour franchir G0 :**
- Critères d'évaluation ancrés dans `CRITERES_EVALUATION.md` (déjà proposés, à valider par l'ingénieur).
- Application des vetos (DEC-0010) sur chaque candidat avant notation.
- Matrice `MATRICE_MULTICRITERE.csv` renseignée avec sources pour chaque note.
- Score stratégique et score de lancement calculés.
- Décision inscrite dans `JOURNAL_DECISIONS.md` : produit retenu (ou arrêt) + création du dossier `2XX_<NOM>`.

## 8. Documents clés (index)

| Fichier | Rôle |
|---|---|
| `000_CADRE/DM_ATLAS_CADRE.md` | Cadre, règles, index |
| `000_CADRE/JOURNAL_DECISIONS.md` | **Source de vérité pour les décisions** |
| `000_CADRE/REGISTRE_RISQUES.md` | Risques et mitigations |
| `000_CADRE/BACKLOG.md` | Actions différées hors gate courant |
| `000_CADRE/BACKLOG_VERIFICATIONS.md` | Points [AV] à vérifier sur source primaire |
| `000_CADRE/QO_QUESTIONS_OUVERTES.md` | Questions actives |
| `000_CADRE/ROADMAP.md` | Séquence des gates |
| `100_REFERENTIELS/REF_100_METHODE.md` | Stage gates + méthode P0 complète |
| `200_PRODUITS/000_SELECTION_PRODUIT/` | Travail actif de sélection |

## 9. En cas de doute

- **Une info existe-t-elle vraiment ?** → Cherche dans `JOURNAL_DECISIONS.md`. Si absente : elle n'existe pas.
- **Une action est-elle légitime ?** → Sert-elle le prochain gate ? Sinon → `BACKLOG.md`.
- **Une donnée doit-elle entrer dans un livrable ?** → Est-elle sourcée ? Sinon → pas d'entrée, ou inscription en `[HYP]` / `[AV]`.
- **Une décision doit-elle être révisée ?** → Ajouter une nouvelle DEC dans le journal, ne pas modifier l'ancienne.
