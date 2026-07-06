# 400_OUTILS

Ce dossier contient les outils opérationnels du dépôt ATLAS.

## Structure

- **`calculateurs/`** — modèles XLSX/Python paramétriques (coût complet en tête).
- **`scripts/`** — scripts PowerShell et Python (extraction, normalisation, batch).
- **`templates/`** — modèles de documents (RFQ, CDC, notice, dossier technique, etc.), créés à mesure.
- **`prompts/`** — prompts consolidés adressés aux IA (Claude, ChatGPT, Codex) pour des tâches récurrentes.

## Règle

Aucun outil créé sans usage tiré par un gate.

Premier outil probablement nécessaire : `calculateurs/COUT_COMPLET_v0.xlsx`, à construire en début de P1 (voir `000_CADRE/BACKLOG.md#BL-004`).
