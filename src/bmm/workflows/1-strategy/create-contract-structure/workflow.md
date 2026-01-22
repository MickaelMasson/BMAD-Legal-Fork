---
title: "Workflow : Création de la Structure du Contrat"
agent: senior-partner
---

Ce workflow guide l'Architecte Juridique (Senior Partner) pour transformer un besoin commercial (Term Sheet) en un plan de rédaction structuré (Liste des Articles).

:::tip[Objectif]
Ne pas rédiger de clauses maintenant. L'objectif est de définir **l'Arborescence** du contrat et la **Stratégie** (Offensive vs Défensive).
:::

## Prérequis

1.  **Term Sheet** : Un document résumant le deal (Prix, Durée, Objet).
2.  **Identité des Parties** : Qui contracte ? (PME vs Grande Groupe = Rapport de force différent).
3.  **Legal Stack** : Confirmation de la juridiction (France) et du type de droit (Commercial, Travail, etc.).

---

## Étape 1 : Qualification et Stratégie

Analyse les documents d'entrée pour déterminer la nature juridique de l'opération.

**Actions :**
1.  Identifier le type de contrat principal (Licence SaaS, Prestation de Service, Vente, NDA).
2.  Identifier le **Niveau de Risque** (Faible < 10k€ | Moyen | Critique > 100k€ ou Données sensibles).
3.  Définir la **Posture de Rédaction** :
    * *Pro-Prestataire* (Standard) : Limiter les responsabilités, protéger l'IP.
    * *Équilibré* (Fair) : Pour faciliter une signature rapide.
    * *Pro-Client* (Si imposé) : Accepter de fortes garanties (à éviter si possible).

:::note[Output attendu]
Une section "Stratégie" en tête du document de structure, définissant le ton du contrat.
:::

---

## Étape 2 : Découpage Modulaire (Architecture)

Définis la structure du document. En *Legal Engineering*, nous préférons la modularité (Contrat Cadre + Annexes) aux documents monolithiques.

**Actions :**
1.  Créer la liste des **Articles** (Epics).
2.  Séparer le Juridique pur (CGV) de l'Opérationnel (SLA, Description technique).
3.  Identifier les **Annexes** nécessaires (ex: "Annexe 1 : DPA/RGPD", "Annexe 2 : Grille Tarifaire").

**Liste standard des Epics à considérer :**
* Définitions (Le "Dictionnaire")
* Objet et Périmètre
* Obligations des Parties
* Conditions Financières
* Propriété Intellectuelle (IP)
* Confidentialité
* Responsabilité et Assurances
* Durée et Résiliation
* Dispositions Diverses (Droit applicable, Force Majeure)

---

## Étape 3 : Spécification des Clauses (User Stories)

Pour chaque Article (Epic), liste les points clés à couvrir, sans rédiger le texte.

*Exemple pour l'Epic "Paiement" :*
* [ ] Story : Paiement à 30 jours date de facture.
* [ ] Story : Pénalités de retard (3x taux légal).
* [ ] Story : Clause de déchéance du terme en cas de non-paiement.

---

## Étape 4 : Analyse de Conformité (Compliance Check)

Vérifie que la structure respecte les contraintes d'Ordre Public (lois impératives).

**Points de contrôle :**
* **RGPD :** Si traitement de données, l'article "Données Personnelles" est obligatoire.
* **Prix :** L'article Prix est-il déterminable (Art. 1163 Code Civil) ?
* **Déséquilibre :** Y a-t-il des clauses purement léonines qui risquent la nullité ?

---

## Étape 5 : Génération du Plan

Génère le fichier de sortie `00-Contract-Structure.md` dans le dossier `_contract-drafts/`.

**Format du livrable :**

```markdown
# Structure du Contrat : [Nom du Projet]

## Stratégie
* **Type :** Contrat SaaS B2B
* **Posture :** Pro-Prestataire (Limitation forte)
* **Risque :** Moyen (Données CRM)

## Plan de Rédaction (Backlog)

### Epic 1 : Objet
* Story 1.1 : Droit d'usage non-exclusif...

### Epic 2 : Conditions Financières
* Story 2.1 : Acompte 30%...

:::caution[Validation] Ne passe pas à la rédaction (Agent Drafter) tant que ce plan n'est pas validé par l'humain. Une erreur de structure coûte cher à corriger plus tard. :::
