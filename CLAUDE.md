# CLAUDE.md

Règles opposables à Claude AI et Claude Code intervenant dans le dépôt ATLAS.

## Rôles

- **Claude AI (web)** : critique, consolidation documentaire, architecture, gros contexte, arbitrages.
- **Claude Code (local)** : exécution sur fichiers, Git, scripts, missions courtes et vérifiables.

## Règles fermes

1. **Aucun contenu métier inventé.** Aucune donnée marché, prix, source, norme, chiffre citée qui ne provienne pas d'une source vérifiable référencée dans le texte.
2. **Aucune décision créée sans passer par `000_CADRE/JOURNAL_DECISIONS.md`.** Une décision non inscrite est réputée ne pas exister. Le journal est append-only : on ajoute une nouvelle décision qui complète ou remplace, on ne réécrit jamais une ancienne.
3. **Aucun contenu ne va dans un référentiel `REF_*` sans besoin tiré par le Stage Gate en cours.** Rédiger à blanc viole la règle just-in-time.
4. **Aucune nouvelle architecture (dossier, catégorie, taxonomie) sans justification écrite dans le journal.**
5. **Aucun fichier créé hors de `060_ATLAS/`.** Si un besoin transverse à TEKNEC apparaît, l'inscrire au backlog TEKNEC séparé, pas ici.
6. **Toute mission doit servir le prochain Gate.** Si l'action utile ne le sert pas, elle va dans `BACKLOG.md`.
7. **Distinction obligatoire dans les fichiers** : `[FAIT]` établi et sourcé · `[HYP]` hypothèse à valider · `[DEC]` décision journalisée · `[RSQ]` risque · `[QO]` question ouverte · `[AV]` à vérifier sur source primaire.
8. **Sensibilité limitée aux données** : ATLAS ne contient à ce stade aucune donnée client ou personnelle. Ne rien importer depuis d'autres dépôts (Da Costa, HCF, Isabelle) sans décision explicite.
9. **Modèle par défaut** : Sonnet pour l'exécution documentaire courante. Opus/Fable réservé aux arbitrages d'architecture ou aux critiques de fond, avec justification.

## Prochain objectif

P0 — Sélection du produit pilote. Voir `100_REFERENTIELS/REF_100_METHODE.md` et `200_PRODUITS/000_SELECTION_PRODUIT/`.
