---
chapter: 5
section: g
title: Exercices sur les Conditions
description: Exercices progressifs pour pratiquer la logique conditionnelle en JavaScript avec if, else, switch, comparaisons et opérateurs logiques.
---

# Exercices - Conditions

Ces exercices couvrent l’ensemble du chapitre sur les conditions.  
Ils sont progressifs : commencez par les plus simples et avancez vers les scénarios plus complexes.

---

## Exercice 1 - Première condition

Déclarez une variable `age = 20`.  
Écrivez une condition `if` qui affiche `"Majeur"` si l’âge est supérieur ou égal à 18.

---

## Exercice 2 - If / else

Déclarez une variable `x = 5`.  
Écrivez une condition qui affiche :  

- `"x est supérieur à 10"` si `x > 10`,  
- sinon `"x est inférieur ou égal à 10"`.

---

## Exercice 3 - If / else if / else

Déclarez une variable `country`.  
Si `country === "Espagne"`, affichez `"Ola"`.  
Si `country === "France"`, affichez `"Bonjour"`.  
Si `country === "Allemagne"`, affichez `"Guten Tag"`.  
Sinon, affichez `"Hello"`.

---

## Exercice 4 - Switch

Déclarez une variable `day = "mercredi"`.  
Utilisez un `switch` pour afficher :  

- `"Début de semaine"` si `day === "lundi"`,  
- `"Milieu de semaine"` si `day === "mercredi"`,  
- `"Fin de semaine"` si `day === "vendredi"`,  
- `"Jour non reconnu"` dans les autres cas.

---

## Exercice 5 - Comparaison stricte

Déclarez deux variables :  

```javascript
let a = 5;
let b = "5";
```

Testez les expressions suivantes avec `console.log` :

* `a == b`
* `a === b`
* `a != b`
* `a !== b`

Commentez les résultats.

---

## Exercice 6 - Autres opérateurs de comparaison

Déclarez une variable `temperature = 15`.
Écrivez une condition qui affiche :

* `"Froid"` si la température est inférieure à 10,
* `"Doux"` si elle est comprise entre 10 et 20 inclus,
* `"Chaud"` si elle est strictement supérieure à 20.

---

## Exercice 7 - Opérateurs logiques

Déclarez deux variables :

```javascript
let age = 25;
let country = "France";
```

Écrivez une condition qui affiche `"Accès autorisé"` uniquement si l’âge est supérieur ou égal à 18 **et** si le pays est `"France"`.
Sinon, affichez `"Accès refusé"`.

---

## Exercice 8 - Combinaison avec OR

Déclarez une variable `langue`.
Affichez `"Langue latine"` si `langue` vaut `"français"` **ou** `"espagnol"`.
Sinon, affichez `"Autre langue"`.

---

## Exercice 9 - Opérateur ternaire

Déclarez une variable `note = 14`.
Avec un opérateur ternaire, affectez à une variable `mention` :

* `"Réussi"` si `note >= 10`,
* `"Échec"` sinon.

Affichez `mention`.

---

## Exercice 10 - Challenge final

Écrivez un programme qui :

1. Demande à l’utilisateur son prénom avec `prompt`.
2. Si le prénom est `"Alice"` **ou** `"Bob"`, affiche `"Accès spécial"`.
3. Sinon, si l’utilisateur est en France (`country = "France"`) et majeur (`age >= 18`), affiche `"Accès autorisé"`.
4. Sinon, affiche `"Accès refusé"`.

---

## À retenir

* Les conditions contrôlent l’exécution du code.
* `if`, `else if`, `else` permettent de tester plusieurs cas.
* `switch` rend le code plus lisible quand on compare une même valeur.
* Utilisez `===` et `!==` plutôt que `==` et `!=`.
* Les opérateurs `&&` (ET) et `||` (OU) permettent de combiner les conditions.
* Le ternaire `condition ? valeurSiVrai : valeurSiFaux` simplifie les `if/else` simples.

---

⬅️ [Chapitre précédent : Opérateurs logiques](./f_Conditions.md)

➡️ [Chapitre suivant : Les Tableaux](../06_arrays/a_array.md)
