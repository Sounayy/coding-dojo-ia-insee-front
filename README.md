# Coding Dojo — Dev Augmenté (Frontend)

Exercice support pour la formation **Dev Augmenté**. L'objectif est de refaire le même exercice plusieurs fois en faisant varier la stratégie de prompting, et d'observer ce qui change dans le code produit par l'IA.

## Exercice : Todo list

Construire une todo list côté frontend, avec persistance locale.

### Spécification fonctionnelle

- Afficher la liste des tâches.
- Ajouter une tâche via un champ texte + un bouton.
- Cocher / décocher une tâche (statut « fait » / « à faire »).
- Supprimer une tâche.
- Persister les tâches dans le `localStorage` du navigateur (elles survivent au refresh de la page).

### Contraintes

Aucune contrainte d'architecture, de découpage ou de bibliothèque. C'est l'IA qui propose en fonction du prompt — c'est précisément ce qu'on observe.

## Démarrage

### React (chemin par défaut)

Un squelette React + Vite (TypeScript) est déjà installé sur la branche `skeleton/react`.

```bash
git checkout skeleton/react
npm install
npm run dev
```

### Autre framework

Si tu veux faire l'exercice en Vue, Svelte, Angular, Solid, ou autre : reste sur `main`, et initialise toi-même le projet à la racine. Quelques commandes à titre indicatif :

```bash
# Vue
npm create vue@latest .

# Svelte
npm create svelte@latest .

# Angular
npx @angular/cli new . --defaults
```

La spécification ci-dessus reste rigoureusement la même.

## Protocole du dojo

L'idée est de refaire l'exercice **plusieurs fois**, en faisant varier à chaque itération la stratégie de prompting. Quelques variantes typiques à essayer :

1. **Yolo** — un prompt très court et flou.
2. **Prompt structuré** — contexte, contraintes, format de sortie, critères de qualité explicités.
3. **Avec rules** — un fichier `CLAUDE.md` (ou équivalent) qui pose les conventions, et un prompt court derrière.
4. **Avec skills** — un skill (Claude Code) qui encode les bonnes pratiques, invoqué depuis le prompt.

> **Aucun prompt n'est fourni** : l'écriture des prompts fait partie de l'exercice. C'est la matière du dojo.

### Workflow Git suggéré

Pour ne pas mélanger les itérations et pouvoir comparer après coup :

```bash
# Repartir du squelette propre pour chaque variante
git checkout -b run/yolo skeleton/react
# (faire l'exercice avec la variante "yolo", commit le résultat)

git checkout -b run/structured skeleton/react
# (refaire avec la variante "prompt structuré")

# etc.
```

## Critères d'observation

Pendant et après chaque itération, regarder :

- Structure du code généré (découpage, fichiers, responsabilités).
- Séparation des responsabilités (UI / état / persistance).
- Qualité du nommage et lisibilité.
- Gestion d'erreurs et cas limites (ex. tâche vide, doublons).
- Accessibilité (labels, focus, clavier).
- Présence de tests, qualité des tests.
- Temps passé jusqu'à un résultat fonctionnel.

Confronter les résultats entre variantes : qu'est-ce que le prompt mieux construit a apporté ? Qu'est-ce que les rules / skills ont changé ?
