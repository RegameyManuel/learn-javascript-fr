---
chapter: 3
section: d
title: Opérateurs avancés
description: Approfondir la manipulation des opérateurs en JavaScript, comprendre leur ordre de priorité et découvrir des opérateurs moins connus.
---

# Opérateurs avancés

Après avoir étudié les opérateurs de base, intéressons-nous à des constructions un peu plus complexes que JavaScript met à notre disposition. Ces opérateurs sont très utiles dans les programmes réels, car ils permettent de gagner en concision et en expressivité.

## L’ordre des opérations

Comme en mathématiques, toutes les opérations ne sont pas évaluées dans l’ordre où elles apparaissent. Chaque opérateur possède une **priorité**, appelée *précédence*.  
Par exemple, la multiplication et la division sont effectuées avant l’addition et la soustraction. Les parenthèses permettent de modifier cet ordre.

```javascript
console.log(2 + 3 * 4);   // 14 (multiplication avant addition)
console.log((2 + 3) * 4); // 20 (parenthèses prioritaires)
```

## L’opérateur de puissance

L’opérateur `**` permet d’élever un nombre à une puissance donnée. C’est une alternative plus lisible à `Math.pow`.

```javascript
console.log(2 ** 3);  // 8
console.log(5 ** 2);  // 25
```

## Incrémentation et décrémentation

Les opérateurs `++` et `--` servent respectivement à augmenter ou diminuer la valeur d’une variable de 1.
Ils peuvent être utilisés **avant** ou **après** la variable, mais l’effet n’est pas exactement le même.

```javascript
let a = 5;
console.log(++a); // 6 (incrémentation avant lecture)
console.log(a++); // 6 (puis la variable passe à 7)
```

Ce comportement est à connaître, même si en pratique on privilégie souvent des formes explicites comme `a = a + 1`.

## Opérateurs d’affectation combinés

JavaScript propose des raccourcis pour combiner une opération et une affectation.

```javascript
let x = 10;
x += 5;  // équivaut à x = x + 5
x -= 3;  // équivaut à x = x - 3
x *= 2;  // équivaut à x = x * 2
x /= 4;  // équivaut à x = x / 4
x %= 3;  // équivaut à x = x % 3
```

Ces opérateurs rendent le code plus concis et améliorent la lisibilité lorsqu’une variable est modifiée par rapport à elle-même.

## L’opérateur nullish coalescing (??)

Introduit plus récemment, l’opérateur `??` permet de fournir une valeur par défaut lorsqu’une variable vaut `null` ou `undefined`.

```javascript
let nom;
console.log(nom ?? "Anonyme"); // "Anonyme"

nom = "Alice";
console.log(nom ?? "Anonyme"); // "Alice"
```

Cet opérateur est particulièrement utile pour éviter les erreurs lorsque certaines valeurs ne sont pas définies.

---

## À retenir

En JavaScript, la **précédence des opérateurs** détermine l’ordre des calculs, mais les parenthèses permettent toujours de clarifier les priorités.
L’opérateur `**` sert aux puissances, tandis que `++` et `--` permettent d’incrémenter ou décrémenter une variable.
Les opérateurs d’affectation combinés (`+=`, `-=`, `*=`, `/=`, `%=`) simplifient l’écriture des mises à jour de variables.
Enfin, l’opérateur `??` est une manière élégante de définir une valeur par défaut en cas de `null` ou `undefined`.

---

⬅️ [Chapitre précédent : Opérateurs de base](./c_Operateurs.md)

➡️ [Chapitre suivant : Exercices](./e_Exercices.md)

