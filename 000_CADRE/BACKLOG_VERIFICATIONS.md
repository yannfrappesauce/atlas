# BACKLOG_VERIFICATIONS

**Règle :** tout point marqué `[AV]` doit être vérifié sur source primaire avant d'être utilisé comme fait dans un livrable de gate.

Un point AV validé donne lieu à :
1. mise à jour du statut ci-dessous (Vérifié, avec date et lien vers la source) ;
2. intégration du fait dans le référentiel pertinent avec citation de source ;
3. déblocage des livrables qui dépendaient de ce point.

**Statut :** Ouvert · En cours · Vérifié · N/A

| ID | Point à vérifier | Source primaire | Déclencheur | Statut |
|---|---|---|---|---|
| AV-01 | Code NC applicable au produit retenu au Gate 0 | RITA / Douane.gouv.fr | P4 (dépend du produit) | Ouvert |
| AV-02 | Droits de douane associés au code NC | TARIC / RITA | P4 | Ouvert |
| AV-03 | Mesures antidumping UE éventuelles selon origine | TARIC | P5 (si sourcing hors UE) | Ouvert |
| AV-04 | Applicabilité MACF/CBAM (chapitre douanier + seuils de minimis) | Règlement (UE) 2023/956 + actes d'exécution | P4 (si acier ou aluminium) | Ouvert |
| AV-05 | REP emballages : éco-organisme + identifiant unique ADEME dès la 1re unité | ADEME / éco-organisme | P4 | Ouvert |
| AV-06 | REP produit selon catégorie (bricolage/jardin, éléments d'ameublement, etc.) | ADEME | P4 | Ouvert |
| AV-07 | Obligations RSGP/GPSR (règlement UE 2023/988) — dossier technique, notice, étiquetage | EUR-Lex / DGCCRF | P4 | Ouvert |
| AV-08 | Norme EN 1860-1 barbecues combustible solide (obligatoire suite DEC-0022) | AFNOR / EUR-Lex | P3-P4 (bloquant) | Ouvert |
| AV-09 | Coût d'une RC exploitation + RC produits pour la catégorie du produit retenu | Devis 2–3 assureurs | Avant P9 | Ouvert |
| AV-10 | Disponibilité d'un futur signe de marque commerciale (classes pertinentes selon produit) | Recherche INPI | Avant tout actif de marque | Ouvert |
| AV-11 | Obligations AGEC (Triman, information tri, disponibilité pièces détachées, indice éventuel) | Legifrance / DGCCRF | P4 | Ouvert |
| AV-12 | Régime TVA à l'import (autoliquidation via CA3 depuis 2022) et impact trésorerie | Douane.gouv.fr / impots.gouv.fr | P8 | Ouvert |
| AV-13 | Reglement CE 1935/2004 contact alimentaire (declenche par DEC-0022) | EUR-Lex / DGCCRF | P3-P4 (bloquant) | Ouvert |
