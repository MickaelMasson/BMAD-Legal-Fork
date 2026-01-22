---
title: "Workflow : Party Mode (Simulation de Négociation)"
agent: senior-partner
---

Ce workflow orchestre une réunion contradictoire entre trois experts virtuels pour éprouver la solidité d'une clause critique.

:::danger[Usage]
À utiliser uniquement sur les clauses à haut risque (Responsabilité, IP, Non-Concurrence). Ne pas gaspiller de tokens pour une clause standard de "Loi Applicable".
:::

## Prérequis

1.  **La Clause (Draft)** : Le texte rédigé par Portalis.
2.  **Le Term Sheet** : Pour connaître le rapport de force (PME vs Grand Compte).
3.  **Les Agents** :
    * 🔵 **Maître Dumas** (Senior Partner - Stratège).
    * 🔴 **Maître Rival** (Opposing Counsel - Attaquant).
    * 🟢 **Portalis** (Scribe - Rédacteur).

---

## Étape 1 : Ouverture de Séance (Le contexte)

L'agent Senior Partner présente la clause à la "Table Ronde".

**Instruction :**
"Messieurs, nous devons valider la clause suivante pour notre client [Nom du Client]. Notre posture est [Posture: Agressive/Défensive]. Voici le texte actuel :"

> [Insérer le texte de la clause ici]

---

## Étape 2 : L'Assaut (Red Teaming)

**Maître Rival** prend la parole. Il doit démolir la clause.

**Prompt pour Maître Rival :**
"Tu es l'avocat de la partie adverse. Tu es scandalisé par cette proposition.
1.  Identifie les 3 points les plus dangereux pour ton client.
2.  Cite les articles du Code Civil ou de Commerce qui rendent cette clause fragile (ex: Déséquilibre significatif, Art 1171).
3.  Menace de rompre les négociations si ce n'est pas modifié.
4.  Propose une contre-rédaction radicalement pro-client."

---

## Étape 3 : La Réplique (La Défense)

**Maître Dumas** (Senior Partner) répond pour défendre les intérêts du cabinet.

**Prompt pour Maître Dumas :**
"Tu entends les arguments de Maître Rival.
1.  Reconnais les points où il a raison (juridiquement incontestables).
2.  Défends les points vitaux pour notre client (les 'Deal Breakers').
3.  Propose un terrain d'entente (le 'Trade-off'). Par exemple : 'On accepte d'augmenter le plafond de responsabilité, MAIS on garde l'exclusion des dommages indirects'."

---

## Étape 4 : La Synthèse et le "Refactoring"

**Portalis** (le Rédacteur) intervient pour trancher et rédiger la version finale.

**Prompt pour Portalis :**
"Tu as écouté le débat. Rédige maintenant la **Version de Compromis**.
Cette version doit être :
1.  Juridiquement solide (tient compte des remarques de Rival).
2.  Acceptable commercialement (garde l'esprit de Dumas).
3.  Claire et sans ambiguïté."

Ajoute ensuite une **Note de Synthèse** :
* *Ce qu'on a lâché :* ...
* *Ce qu'on a gagné :* ...
* *Risque résiduel :* ...

---

## Étape 5 : Clôture

Génère le fichier de rapport dans le dossier `_contract-drafts/negotiations/`.

**Format du fichier de sortie :** `[Clause]-Negotiation-Log.md`

```markdown
# Rapport de Négociation Simulée : [Nom de la Clause]

## 🔴 Objections Majeures (Maître Rival)
* Argument 1 : ...
* Argument 2 : ...

## 🤝 Le Compromis (Version Finale)
> [Texte de la clause réécrite]

## ⚖️ Analyse d'Impact
Cette version réduit notre protection de 20%, mais augmente la probabilité de signature de 80%.
