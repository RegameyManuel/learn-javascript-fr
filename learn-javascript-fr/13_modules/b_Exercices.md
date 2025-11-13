---
chapter: 13
section: b
title: Exercices sur les modules
description: Série d’exercices pratiques pour apprendre à organiser du code en modules JavaScript avec `import` et `export`.
---

# Exercices sur les modules

Ces exercices permettent de mettre en pratique les notions vues dans le chapitre sur les modules : création, exportation et importation de fonctions, variables ou valeurs par défaut. L’objectif est de comprendre comment structurer un projet en plusieurs fichiers clairs et réutilisables.

---

## Exercice 1 — Premier module

Crée un fichier `mathUtils.js` qui exporte une fonction `add(a, b)` renvoyant la somme des deux nombres.  
Dans un fichier `main.js`, importe cette fonction et teste-la avec quelques additions.

---

## Exercice 2 — Plusieurs exports nommés

Dans un fichier `greetings.js`, définis deux fonctions :  

- `sayHello(name)` qui renvoie « Bonjour, *nom* »,  
- `sayGoodbye(name)` qui renvoie « Au revoir, *nom* ».  
  Exporte-les toutes les deux et importe-les dans `main.js` pour afficher les messages correspondants.

---

## Exercice 3 — Export par défaut

Crée un fichier `square.js` contenant une fonction par défaut `square(x)` qui retourne le carré de son argument.  
Dans `main.js`, importe cette fonction et utilise-la pour afficher le carré de plusieurs nombres.

---

## Exercice 4 — Mélange d’exports

Dans un fichier `person.js`, définis une constante `species = "Homo sapiens"` et une fonction `introduce(name, age)` qui affiche une présentation.  
Exporte `species` comme export nommé et `introduce` comme export par défaut.  
Teste dans `main.js` les deux formes d’import.

---

## Exercice 5 — Organisation d’un projet

Imagine une mini-application qui gère des produits :  

- un fichier `product.js` qui exporte une fonction `createProduct(name, price)`,  
- un fichier `cart.js` qui exporte une fonction `addToCart(cart, product)` et une fonction `getTotal(cart)`,  
- un fichier `main.js` qui crée quelques produits et calcule le total du panier.  

---

## Exercice 6 — Renommer un import

Dans un fichier `math.js`, exporte une fonction `multiply(a, b)`.  
Dans `main.js`, importe-la mais en la renommant en `times`. Vérifie que tu peux bien appeler `times(3, 4)` pour obtenir 12.

---

## Exercice 7 — Dépendances circulaires

Crée deux fichiers `a.js` et `b.js`. Dans chacun, importe quelque chose de l’autre et affiche un message. Observe le comportement dans la console. Explique pourquoi il est préférable d’éviter les dépendances circulaires.

---

## Exercice 8 — Regrouper les exports

Crée un fichier `utils.js` qui exporte trois fonctions simples : `double(x)`, `triple(x)` et `quadruple(x)`.  
Dans `main.js`, importe-les toutes en une seule fois avec la syntaxe `import * as utils from "./utils.js"` et appelle `utils.double(4)`, `utils.triple(4)`, `utils.quadruple(4)`.

---

## Exercice 9 — Export d’objets

Dans `config.js`, exporte un objet `settings` contenant une langue (`fr`) et un thème (`dark`).  
Dans `main.js`, importe cet objet et affiche ses propriétés.

---

## Exercice 10 — Projet de synthèse

Construis une mini-application modulaire :  

- un fichier `user.js` qui exporte une fonction pour créer un utilisateur,  
- un fichier `auth.js` qui exporte une fonction `login(user, password)`,  
- un fichier `main.js` qui crée un utilisateur et tente une connexion.  

Organise les fichiers avec des exports nommés et par défaut selon les besoins.

---

⬅️ [Chapitre précédent : Modules](./a_modules.md)

➡️ [Chapitre suivant : Expression Régulières](../14_regular-expression/a_regular-expression.md)
