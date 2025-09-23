---
chapter: 11
section: b
title: Exercices sur JSON
description: Série d’exercices pratiques pour manipuler le format JSON en JavaScript : conversion, parsing, stockage et échange de données.
---

# Exercices sur JSON

Ces exercices permettent de pratiquer la manipulation du format JSON en JavaScript, notamment la conversion d’objets en chaînes, l’analyse de données JSON, et l’utilisation de ce format pour stocker ou transmettre des informations.

---

## Exercice 1 — Conversion simple
Crée un objet représentant un utilisateur avec un nom, un âge et une ville. Convertis-le en JSON à l’aide de `JSON.stringify` et affiche le résultat.

---

## Exercice 2 — Retour à l’objet
Reprends la chaîne JSON produite dans l’exercice précédent. Utilise `JSON.parse` pour retrouver l’objet JavaScript original et affiche ses propriétés une par une.

---

## Exercice 3 — Tableaux en JSON
Crée un tableau d’objets représentant plusieurs livres (titre, auteur, année). Convertis ce tableau en JSON et vérifie la structure obtenue.

---

## Exercice 4 — JSON et `null`
Crée un objet contenant une propriété `status` avec la valeur `null`. Convertis-le en JSON puis réanalyse-le avec `JSON.parse`. Vérifie que la valeur est correctement préservée.

---

## Exercice 5 — Types non supportés
Crée un objet contenant une fonction et une date. Convertis-le en JSON. Observe ce qui est produit et explique pourquoi.

---

## Exercice 6 — Stockage local
Crée un objet représentant les préférences d’un utilisateur (langue, thème clair/sombre). Convertis-le en JSON et simule son stockage dans `localStorage` avec `localStorage.setItem("prefs", json)`. Récupère ensuite ces préférences avec `localStorage.getItem` et `JSON.parse`.

---

## Exercice 7 — API simulée
Imagine qu’un serveur renvoie la chaîne JSON suivante :
```json
{ "temperature": 21, "humidity": 55, "city": "Paris" }
```

Analyse cette chaîne avec `JSON.parse` et affiche les valeurs de chaque propriété dans la console.

---

## Exercice 8 — Formatage

Crée un objet puis convertis-le en JSON avec `JSON.stringify`. Utilise les paramètres supplémentaires de `stringify` pour afficher la chaîne avec une indentation de 2 espaces, afin de la rendre plus lisible.

---

## Exercice 9 — Modification après parsing

Analyse un objet JSON représentant un produit (nom, prix, stock). Modifie son prix en JavaScript, puis reconvertis l’objet en JSON pour obtenir la nouvelle version.

---

## Exercice 10 — Projet de synthèse

Crée un petit programme qui gère une liste de tâches :

* ajoute plusieurs tâches dans un tableau d’objets,
* convertis la liste en JSON,
* stocke-la dans `localStorage`,
* récupère-la ensuite et affiche chaque tâche dans la console.

---

⬅️ [Chapitre précédent : JSON](./a_json.md)

➡️ [Chapitre suivant : …](../12_error-handling/a_Error.md)
