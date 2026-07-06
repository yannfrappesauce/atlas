# REGISTRE_RISQUES

**Règle :** un risque non inscrit ici ne fait pas partie du raisonnement. Toute mitigation validée doit être répercutée dans le journal des décisions (référence `DEC-XXXX`).

**Légende gravité :** Basse / Moyenne / Haute
**Légende statut :** Ouvert (identifié, non mitigé) · Actif (mitigation en cours) · Traité (mitigation validée) · Réalisé (le risque s'est produit)

| ID | Domaine | Risque | Gravité | Mitigation | Statut |
|---|---|---|---|---|---|
| RSQ-01 | Réglementaire | Non-conformité produit selon le produit retenu (RSGP/GPSR, REP, normes sectorielles) | Haute | Analyse réglementaire avant commande (activation partielle REF_120 dès P0 selon candidat) | Ouvert |
| RSQ-02 | Produit | Responsabilité du fait des produits défectueux (particulièrement critique pour produits à feu ouvert, contact alimentaire, produits d'appui) | Haute | Analyse de risques + notice + avertissements + RC produits avant première vente | Ouvert |
| RSQ-03 | Financier | Capital immobilisé ou perdu au-delà du plafond | Haute | Plafond DEC-0003 (3 000 € TTC) + vetos DEC-0010 + kill criteria DEC-0004 | Actif |
| RSQ-04 | Méthode | Documentation sans vente réelle — dérive vers la méthode-cathédrale | Haute | Règle just-in-time (DM §5.3) + garde-fou méthode (DM §7) + règle Stage Gate (DM §5.1) | Actif |
| RSQ-05 | Fournisseur | Fournisseur non fiable, dérive entre golden sample et production | Moyenne | REF_130 : plans cotés + golden sample contractuel + inspection tierce partie pré-embarquement | Ouvert |
| RSQ-06 | IP | Copie du produit par le fournisseur ou vente parallèle | Moyenne | Accord NNN de droit chinois avant transmission de plans (traité dans REF_130 quand P5 s'active) | Ouvert |
| RSQ-07 | Projet | Dispersion — ATLAS s'ajoute à la charge TEKNEC/HCF | Haute | Priorité TEKNEC > ATLAS (DEC-0001) + rythme à définir explicitement | Actif |
| RSQ-08 | Logistique | Casse/corrosion en transport, litiges dernier km sur produits lourds | Moyenne | Spécification d'emballage export dans le CDC + assurance cargo + protocole réception | Ouvert |
| RSQ-09 | Marque | Indisponibilité du signe commercial choisi | Basse (si traité tôt) | Recherche d'antériorité INPI avant tout actif de marque (AV-10) | Ouvert |
| RSQ-10 | Gouvernance | Perte de contexte entre sessions IA (documents non tenus, conversations non consolidées) | Haute | Règle documentaire (DM §5.2) + JOURNAL_DECISIONS append-only + PAQUET_PASSATION_ATLAS | Actif |
