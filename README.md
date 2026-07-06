# ATLAS

Programme d'ingénierie produit.

## Statut

Initialisation — version de référence v1.

## Nature d'ATLAS

ATLAS est un programme destiné à construire une méthode reproductible de sélection, qualification, sourcing, test, import éventuel, commercialisation et amélioration de produits physiques.

ATLAS n'est actuellement :
- ni une société ;
- ni une marque commerciale.

Une marque pourra naître d'ATLAS. Une structure juridique pourra porter cette marque après validation économique du projet pilote et discussion avec les futurs associés (voir DEC-0002, DEC-0013, DEC-0014).

## Règle principale

Toute action ATLAS doit servir le prochain Stage Gate. Sinon elle va dans `000_CADRE/BACKLOG.md`.

## Prochain objectif

**P0 — Sélectionner le produit pilote.** Cinq candidats initiaux, notation ancrée, vetos éliminatoires, décision de Gate 0 : produit retenu ou arrêt.

## Points d'entrée obligatoires pour toute reprise (IA ou humain)

1. `000_CADRE/PAQUET_PASSATION_ATLAS.md` — synthèse pour reprise sans contexte.
2. `000_CADRE/DM_ATLAS_CADRE.md` — cadre et règles.
3. `000_CADRE/JOURNAL_DECISIONS.md` — décisions validées (append-only, source de vérité).
4. `100_REFERENTIELS/REF_100_METHODE.md` — stage gates et méthode P0.
5. `200_PRODUITS/000_SELECTION_PRODUIT/` — travail actif.

## Arborescence

```
060_ATLAS/
├── 000_CADRE/            gouvernance : DM, décisions, risques, backlog, roadmap
├── 100_REFERENTIELS/     méthode et référentiels transverses (rédaction just-in-time)
├── 200_PRODUITS/         P0 sélection + dossier produit créé au Gate 0 uniquement
├── 300_DATA/             bases CSV (fournisseurs, devis, concurrents, coûts, REX...)
├── 400_OUTILS/           calculateurs, scripts, templates, prompts
└── 900_ARCHIVES/         versions antérieures conservées pour trace
```

Les dossiers non listés (documents externes, import, marque, etc.) seront créés au moment où un livrable les rend nécessaires. Aucune sur-anticipation.
