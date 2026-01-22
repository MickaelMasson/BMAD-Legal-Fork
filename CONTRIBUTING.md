# Contribuer à LEAD Method (Legal Engineering)

Merci de vouloir contribuer ! Nous croyons en **l'Amplification Juridique, pas au Remplacement**. Notre but est de coupler la rigueur du Droit avec la puissance d'analyse de l'IA pour créer des contrats "Zéro Défaut".

💬 **Discord** : [Rejoindre la communauté](https://discord.gg/gk8jAdXWmj) (Lien à mettre à jour si tu en crées un) pour discuter clause, jurisprudence et prompt engineering.

---

## ⚖️ Notre Philosophie : "Code is Law"

LEAD renforce la collaboration Humain-IA à travers des workflows de rédaction structurés. Chaque contribution doit répondre à la question : **"Est-ce que cela rend le contrat plus sûr, plus clair et juridiquement plus solide ?"**

**✅ Ce que nous recherchons :**
- Des "Patterns" de clauses robustes (ex: Clause limitative de responsabilité validée par jurisprudence).
- Des Personas d'agents améliorés (ex: un "Avocat Adverse" plus agressif).
- Des modules spécifiques (ex: Module RGPD, Module Droit du Travail).
- Une meilleure gestion du contexte juridique (références croisées).

**❌ Ce qui est refusé :**
- Les solutions 100% automatisées sans validation humaine ("Human-in-the-loop" obligatoire).
- Le "Légalese" inutile (jargon complexe quand le langage clair suffit).
- Les hallucinations juridiques (références à des articles de loi inexistants ou abrogés).

---

## Signaler des "Bugs" Juridiques

**TOUT signalement de faille ou demande de modèle doit passer par les Issues GitHub.**

### Avant de créer une Issue

1. **Recherche** : Vérifiez si la clause ou le problème a déjà été discuté.
2. **Contexte** : Précisez toujours la juridiction visée (par défaut : **Droit Français**).

### Bug Reports (Failles Juridiques)

Si vous trouvez une faille dans un template ou un prompt, utilisez le template de bug et incluez :
- La clause incriminée.
- La raison juridique de la faille (ex: "Contraire à l'article 1170 du Code civil").
- Une proposition de correction (le "Patch").

### Feature Requests (Nouveaux Contrats)

Pour proposer un nouveau type de contrat (ex: "CGV E-commerce"), expliquez :
- L'objectif du document.
- Les parties prenantes (ex: Vendeur Pro / Acheteur Consommateur).
- Les points de friction habituels.

---

## Standards de Rédaction (Legal Engineering)

⚠️ **Règles d'Or pour les Prompts et les Agents :**

| Règle | Description |
| :--- | :--- |
| **Primauté du Droit** | Toute rédaction doit se conformer au Droit Français (sauf mention contraire). Citer les articles du Code Civil/Commerce est encouragé. |
| **Atomicité** | Une "User Story" = Une Clause unique. Ne mélangez pas "Paiement" et "Livraison". |
| **Intention** | Chaque clause générée doit être accompagnée d'un commentaire expliquant *l'intention* (le "Pourquoi") pour faciliter la relecture par l'avocat. |
| **Clarté** | Privilégier le style "Legal Design" : phrases courtes, voix active. |

---

## Guidelines pour les Pull Requests (PR)

### Branche Cible
Soumettez vos PR sur la branche `main`.

### Taille de la PR
- **Idéal** : 1 Article complet ou 1 Agent spécifique.
- **Maximum** : Ne refondez pas tout le Code Civil en une fois.

### Description de la PR (Template)

```markdown
## Quoi
[1-2 phrases décrivant l'ajout : ex: "Ajout du module Propriété Intellectuelle SaaS"]

## Pourquoi
[Pourquoi c'est nécessaire : ex: "Le module actuel ne couvrait pas la cession des droits futurs"]

## Comment (Preuve juridique)
- [Référence à l'article L.111-1 du CPI]
- [Inspiré de la jurisprudence X vs Y]

## Test (Simulacre)
[J'ai testé cette clause avec l'agent "Avocat Adverse", elle a résisté aux arguments sur la nullité]
