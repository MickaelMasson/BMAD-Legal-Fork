---
title: "Charte de Rédaction Juridique (Legal Design)"
---

Ce projet adhère aux principes du [Legal Design](https://law.stanford.edu/legal-design-lab/) et du [Langage Clair](https://www.modernisation.gouv.fr/bonnes-pratiques/le-langage-clair) pour structurer le contenu juridique.

## Règles Fondamentales (Droit Français)

| Règle | Spécification |
|------|---------------|
| **Termes Définis** | Tout terme commençant par une Majuscule (ex: le "Client") renvoie à l'Article Définitions. |
| **Numérotation** | Structure décimale stricte (1.1, 1.1.1) pour faciliter les renvois. |
| **Voix Active** | Privilégier "Le Client paiera" plutôt que "Le paiement devra être effectué par le Client". |
| **Phrases Courtes** | Une idée = Une phrase. Maximum 3 lignes par paragraphe. |
| **Listes** | Utiliser des listes à puces pour les conditions cumulatives (ET) ou alternatives (OU). |
| **Code Civil** | Citer l'article de loi en commentaire si la clause est d'ordre public. |

## Admonitions (Notes d'Intention)

L'IA utilise ces blocs pour communiquer avec l'avocat humain sans polluer le texte du contrat.

```md
:::tip[Stratégie]
Pourquoi nous avons choisi cette formulation (ex: pro-prestataire).
:::

:::note[Contexte]
Faits spécifiques du client (ex: secteur bancaire nécessitant un audit).
:::

:::caution[Risque Juridique]
Alerte sur une clause potentiellement abusive ou nécessitant une négo.
:::

:::danger[Bloquant]
Point de non-conformité majeure (ex: illégal en droit français).
:::
Structure des "Epics" (Articles)
Chaque section du contrat (Epic) doit suivre ce format dans le dossier de travail :

Plaintext

1. Titre de l'Article (ex: Article 5 - Propriété Intellectuelle)
2. Intention (Note pour l'avocat : "On cède tout sauf le noyau")
3. Liste des Stipulations (User Stories)
4. Texte de la Clause (Le "Livrable")
5. Références Croisées (Renvois vers Article "Prix" ou "Résiliation")
Conventions de Nommage des Fichiers
Markdown

LEAD-Project/
├── _lead-config/                  # Configuration du Cabinet
├── _contract-drafts/
│   ├── 00-Term-Sheet.md           # Les points clés négociés
│   ├── 01-Definitions.md          # Glossaire global
│   └── 05-IP-Rights.md            # Article spécifique
└── ...
Structure des Tableaux de Suivi
Phases de Rédaction :

Markdown

| Phase | Nom | Action |
|-------|------|--------------|
| 1 | Stratégie | Term Sheet & Structure (Architecte) |
| 2 | Rédaction | Rédaction des clauses (Drafter) |
| 3 | Contradictoire | Simulation d'opposition (Party Mode) |
| 4 | Finalisation | Revue Avocat Humain |
Commandes de l'Agent :

Markdown

| Commande | Agent | But |
|---------|-------|---------|
| `*structure-init` | Senior Partner | Créer le squelette du contrat |
| `*draft-clause` | Drafter | Rédiger un article spécifique |
| `*audit-clause` | Opposing Counsel | Chercher les failles |
Checklist Qualité (QA)
Avant de valider une section :

[ ] Les Termes Définis sont-ils utilisés correctement ?

[ ] Y a-t-il des renvois orphelins (ex: voir article X qui n'existe pas) ?

[ ] La clause survit-elle à la résiliation (ex: Confidentialité) ?

[ ] La juridiction compétente est-elle rappelée en cas de doute ?
