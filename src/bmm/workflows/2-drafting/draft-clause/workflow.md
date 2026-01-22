---
title: "Workflow : Rédaction de Clause (Drafting)"
agent: drafter
---

Ce workflow guide le Rédacteur (Drafter) pour transformer une "User Story" juridique (une stipulation) en un texte contractuel formel et exécutoire.

:::tip[Règle d'Or]
Ne jamais inventer de terme défini. Si tu dois parler du "Client", vérifie d'abord comment il est nommé dans le fichier `Definitions.md` (ex: "le Client", "l'Abonné", "le Licencié").
:::

## Prérequis

1.  **Le Fichier Définitions** : Le glossaire du projet (Article 1).
2.  **La Story** : L'instruction précise (ex: "Paiement à 30 jours fin de mois").
3.  **La Posture** : Définie par le Senior Partner (ex: "Agressif sur la protection de l'IP").

---

## Étape 1 : Analyse de la Demande

Avant d'écrire, analyse le contexte légal de la clause demandée.

**Checklist d'analyse :**
1.  **Catégorie :** Est-ce une obligation de moyens (best effort) ou de résultat ?
2.  **Sanction :** Que se passe-t-il si cette clause n'est pas respectée ? (Résiliation ? Pénalité ?). Si la Story ne le dit pas, propose une sanction standard.
3.  **Terminologie :** Scanne le fichier `Definitions.md` pour charger les variables en mémoire.

---

## Étape 2 : Rédaction (The Draft)

Rédige le texte de la clause en suivant les standards du "Legal Design".

**Règles de syntaxe :**
* **Clarté :** Sujet + Verbe + Complément. Évite les phrases à rallonge.
* **Précision :** Remplace "dans les meilleurs délais" par une durée chiffrée (ex: "sous 5 jours ouvrés").
* **Structure :** Si la clause a plus de 2 conditions, utilise une liste à puces.

*Exemple de structure :*
> **ARTICLE X. TITRE**
>
> X.1. Principe général.
> X.2. Exception ou condition spécifique.
> X.3. Sanction en cas de non-respect.

---

## Étape 3 : Annotation d'Intention (Pour l'Avocat Humain)

C'est l'étape critique de la méthode LEAD. Ajoute un bloc de commentaire après la clause pour expliquer ta rédaction.

**Format attendu :**

```md
:::note[Intention du Rédacteur]
* **Source :** Inspiré de l'article 1231-5 du Code Civil (Clause pénale).
* **Choix Stratégique :** J'ai ajouté une mise en demeure préalable obligatoire pour protéger le Prestataire contre une résiliation surprise.
* **Point d'Attention :** Le délai de 3 jours est court, l'avocat adverse risque de demander 15 jours.
:::

---

## Étape 4 : Auto-Correction (Linting Juridique)
Relis ta propre clause et vérifie les "Bad Smells" (les erreurs de débutant).

Checklist de fin :

[ ] Ai-je utilisé "Nous" ou "Je" ? (Interdit -> utiliser "le Prestataire").

[ ] Ai-je laissé des [Crochets] non remplis ?

[ ] La clause est-elle contradictoire avec le Term Sheet (ex: prix différent) ?

[ ] Les renvois d'articles (Article X) sont-ils corrects ?

## Étape 5 : Génération du Fichier
Sauvegarde la clause dans le dossier de travail.

Nom du fichier : _contract-drafts/clauses/[Numero]-[NomDeLaClause].md

---
