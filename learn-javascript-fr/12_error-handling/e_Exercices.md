---
chapter: 12
section: e
title: Exercices sur la gestion des erreurs
description: Série d’exercices pratiques pour manipuler `try...catch`, `try...catch...finally` et la gestion des erreurs asynchrones en JavaScript.
---

# Exercices sur la gestion des erreurs

Ces exercices permettent de mettre en application les notions vues dans ce chapitre : interception d’erreurs synchrones, exécution garantie avec `finally`, et gestion des erreurs dans du code asynchrone avec promesses ou `async/await`.

---

## Exercice 1 — Erreur simple
Écris un code qui tente d’afficher une variable non définie dans un bloc `try`. Intercepte l’erreur dans le `catch` et affiche un message personnalisé.

---

## Exercice 2 — Division par zéro
Crée une fonction `divide(a, b)` qui lève une erreur si `b` vaut zéro. Utilise `throw` pour générer l’erreur et `try...catch` pour la gérer proprement.

---

## Exercice 3 — Nettoyage garanti
Écris une fonction qui ouvre une ressource fictive (par exemple affiche « Ressource ouverte ») puis lève une erreur volontaire. Assure-toi que la ressource est toujours « fermée » grâce à un bloc `finally`.

---

## Exercice 4 — Lecture de tableau
Crée une fonction qui tente d’accéder à un élément d’un tableau. Si l’indice est invalide (trop grand ou négatif), lève une erreur et gère-la avec `try...catch`.

---

## Exercice 5 — Promesse rejetée
Écris une promesse qui se rejette avec une erreur après deux secondes. Utilise `.catch()` pour intercepter et afficher le message d’erreur.

---

## Exercice 6 — async/await
Écris une fonction `fetchData()` simulant une requête asynchrone avec `setTimeout`. Si l’URL donnée n’est pas `"ok"`, la fonction lève une erreur. Gère l’erreur avec `try...catch` dans une fonction marquée `async`.

---

## Exercice 7 — Message utilisateur
Écris un code qui tente de convertir une chaîne JSON invalide avec `JSON.parse`. Utilise `try...catch` pour afficher un message clair destiné à l’utilisateur (« Le format des données est incorrect »).

---

## Exercice 8 — Centralisation
Écris une fonction `handleError(error)` qui se charge d’afficher toutes les erreurs de manière uniforme. Utilise-la dans au moins deux blocs `catch` différents.

---

## Exercice 9 — Fallback
Crée une fonction `getUserData()` qui simule une requête serveur. En cas d’échec, elle doit renvoyer un objet par défaut (par exemple `{ name: "Inconnu" }`). Utilise `async/await` et `try...catch`.

---

## Exercice 10 — Projet de synthèse
Construis un petit programme qui :  
1. lit un nombre fourni par l’utilisateur,  
2. tente de diviser 100 par ce nombre,  
3. gère le cas d’une saisie invalide ou d’un zéro avec `throw` et `try...catch`,  
4. affiche toujours « Programme terminé » grâce à un `finally`.  

---

⬅️ [Chapitre précédent : La gestion des erreurs asynchrones](./d_async_errorhandling.md)

➡️ [Chapitre suivant : …](../13_modules/a_modules.md)

