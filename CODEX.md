# CODEX.md

Règles opposables à Codex intervenant dans le dépôt ATLAS.

## Rôle

Codex intervient principalement pour :
- scripts d'automatisation (PowerShell, Python) ;
- extraction et parsing de données (avis clients, devis PDF, catalogues) ;
- calculs structurés (calculateur coût complet, scoring) ;
- traitements CSV et normalisation.

## Règles fermes

1. **Aucune automatisation sans ROI démontré.** Le seuil est écrit dans `100_REFERENTIELS/REF_190_IA.md` quand ce référentiel s'active. Avant cela : chaque script doit servir un livrable de gate identifié.
2. **Aucun script hors besoin réel du projet.** L'infrastructure est gelée : pas de launcher, bootstrap projet, générateur de templates, tant qu'aucun besoin ATLAS ne l'exige.
3. **Priorité aux formats simples et diff-friendly** : CSV, Markdown, PowerShell, Python. Éviter les binaires et formats propriétaires sauf nécessité.
4. **Aucun secret dans les scripts ni dans les fichiers versionnés.** Les clés API vivent hors dépôt (variable d'environnement). Un fichier `.env.example` peut exister ; `.env` doit être dans `.gitignore`.
5. **Scripts idempotents par défaut.** Réexécutable sans effet de bord.
6. **Toute opération batch sur fichiers exige un audit post-action indépendant** (règle héritée de la doctrine générale : ne pas se fier au log d'exécution du script pour valider le résultat).

## Prochain objectif

Aucun besoin d'automatisation avant le Gate 0. Le P0 se fait à la main. Codex sera activé à P1 pour l'analyse d'avis clients concurrents, si le produit retenu le justifie.
