---
chapter: 2
section: e
title: Exercices - Commentaires, Variables, Égalité et Types
description: Exercices progressifs pour mettre en pratique les notions de base de JavaScript (commentaires, variables, opérateurs d’égalité et types de données).
---

# Exercices récapitulatifs

Ces exercices couvrent l’ensemble des notions vues dans ce chapitre. Commence par les plus simples et progresse vers les plus avancés.

---

## Exercice 1 - Les commentaires
Ajoute un **commentaire monoligne** et un **commentaire multiligne** dans le code ci-dessous pour expliquer ce qu’il fait.

```javascript
let message = "Bonjour JavaScript";
console.log(message);
```

---

## Exercice 2 - Variables simples

Déclare trois variables :

* `city` contenant `"Paris"`,
* `year` contenant `2025`,
* `isSunny` contenant `false`.

Affiche leur contenu avec `console.log`.

---

## Exercice 3 - Modification d’une variable

Déclare une variable `score` initialisée à `10`.
Ajoute `5` à ce score puis affiche le nouveau résultat.

---

## Exercice 4 - Égalité

Teste les égalités suivantes et commente le résultat attendu :

```javascript
let a = 5;
let b = "5";

console.log(a == b);   // ?
console.log(a === b);  // ?
```

---

## Exercice 5 - Vérifier le type

Utilise l’opérateur `typeof` pour vérifier le type des valeurs suivantes :

```javascript
let name = "Alice";
let age = 30;
let married = false;
let hobbies = ["cinema", "sport"];
```

---

## Exercice 6 - Objet et propriétés

Crée un objet `car` avec les propriétés suivantes :

* `brand` = `"Toyota"`
* `year` = `2015`
* `electric` = `false`

Affiche chaque propriété avec `console.log`.

---

## Exercice 7 - Mise en pratique

Écris un programme qui :

1. Déclare une variable `temperature` (par exemple `18`).
2. Si la température est supérieure ou égale à `20`, affiche `"Il fait chaud"`.
   Sinon, affiche `"Il fait frais"`.
3. Ajoute un **commentaire** pour expliquer la condition utilisée.

---

## À retenir

* Les **commentaires** aident à comprendre le code.
* Les **variables** stockent des valeurs et peuvent changer.
* L’opérateur `==` compare les valeurs, `===` compare aussi les types.
* L’opérateur `typeof` identifie le type d’une donnée.
* Les **objets** permettent de regrouper plusieurs propriétés.

---

⬅️ [Chapitre précédent : Les Types](./d_Types.md)
➡️ [Chapitre suivant : Les Nombres](../03_numbers/a_Nombres.md)

