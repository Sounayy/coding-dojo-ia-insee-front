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

---

## Exercices suivants (à ne pas faire avant d'avoir fait les premiers exercices sur l'implémentation initale de la todo list)
> **Prérequis** : ne commencer ces exercices qu'après avoir terminé l'implémentation de la todo list (exercices 1 et 2 du dojo). Ils supposent que la persistance localStorage est en place et fonctionnelle.

<details>
<summary>SPOILERS</summary>

### Recherche & filtrage

Filtrer la liste des todos en mémoire, sans requête réseau.

- Ajouter une barre de recherche textuelle qui filtre les todos par leur libellé (recherche en temps réel, avec **debounce** pour éviter de recalculer à chaque frappe)
- Ajouter un sélecteur de statut (Tous / À faire / Terminés) qui filtre la liste affichée
- Refléter l'état des filtres dans l'**URL** (query params) pour que la vue survive au refresh
- Gérer l'état vide : message explicite quand aucun todo ne correspond aux filtres

### Labels/Tags

Étendre le modèle de données localStorage pour y ajouter une entité liée.

- Créer une structure `labels` séparée dans le localStorage (nom + couleur), avec une UI pour les **créer et supprimer**
- Étendre le modèle `todo` pour qu'il stocke une liste d'IDs de labels
- Dans le formulaire d'ajout/édition d'un todo, permettre de **sélectionner plusieurs labels**
- Afficher les labels d'un todo sous forme de **badges colorés** dans la liste
- Ajouter un **filtre par label** combinable avec le filtre statut de l'exercice précédent

</details>
