# Coding Dojo — Dev Augmenté (Frontend)

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
git switch skeleton/react
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
