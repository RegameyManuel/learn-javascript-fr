---
chapter: 3
section: c
title: Opérateurs de base
description: Comprendre les opérateurs arithmétiques en JavaScript, leurs particularités et leurs pièges fréquents.
---

# Opérateurs de base

En programmation, un **opérateur** est un symbole qui indique à l’ordinateur d’effectuer une opération sur une ou plusieurs valeurs.  
En JavaScript, les opérateurs de base permettent de réaliser des calculs arithmétiques simples comme l’addition, la soustraction, la multiplication et la division. Ces opérateurs fonctionnent de manière intuitive pour qui connaît déjà les mathématiques de base.

## Les opérations arithmétiques

Les quatre opérations fondamentales sont représentées par les symboles `+`, `-`, `*` et `/`.  

```javascript
console.log(10 + 5); // 15
console.log(10 - 5); // 5
console.log(10 * 5); // 50
console.log(10 / 5); // 2
```

Chaque opérateur applique l’opération attendue : addition, soustraction, multiplication ou division. Il est possible d’utiliser des nombres entiers comme des décimaux, puisque JavaScript ne distingue pas entre les deux.

## L’opérateur de modulo

Un autre opérateur très utile est le **modulo** (`%`). Il donne le reste d’une division entière.

```javascript
console.log(10 % 3); // 1
console.log(12 % 4); // 0
```

Le modulo est particulièrement employé pour vérifier si un nombre est pair ou impair, ou encore pour répéter des motifs dans une boucle.

## Attention à l’opérateur +

En JavaScript, l’opérateur `+` a une particularité : il sert à la fois à additionner des nombres et à concaténer des chaînes de caractères.

```javascript
console.log(10 + 5);       // 15
console.log("10" + "5");   // "105"
console.log(10 + "5");     // "105"
```

Dans le dernier exemple, l’opérande numérique est converti automatiquement en chaîne. Ce comportement, appelé **coercition de type**, peut provoquer des erreurs subtiles. C’est pourquoi il est recommandé d’être attentif au type des valeurs manipulées.

## NaN et Infinity

Certains calculs donnent lieu à des résultats particuliers :

```javascript
console.log(0 / 0);   // NaN
console.log(1 / 0);   // Infinity
console.log(-1 / 0);  // -Infinity
```

`NaN` (*Not a Number*) indique qu’une opération n’a pas de sens (comme diviser zéro par zéro).
`Infinity` et `-Infinity` représentent respectivement l’infini positif et négatif.

Ces résultats appartiennent malgré tout au type `number`.

## Conversion de chaînes en nombres

Lorsqu’une donnée est stockée sous forme de chaîne, on peut la convertir en nombre grâce à `parseInt`, `parseFloat` ou `Number()`.

```javascript
console.log(parseInt("42"));     // 42
console.log(parseFloat("3.14")); // 3.14
console.log(Number("123"));      // 123
```

Ces conversions sont indispensables lorsqu’on manipule des données saisies par un utilisateur ou provenant de fichiers externes.


---

## À retenir

Les opérateurs arithmétiques de base (`+`, `-`, `*`, `/`) fonctionnent comme en mathématiques.
Le **modulo** (`%`) permet d’obtenir le reste d’une division.
L’opérateur `+` est particulier car il sert aussi à concaténer des chaînes.
Certains calculs renvoient des valeurs spéciales comme `NaN` ou `Infinity`.
Enfin, il est possible de convertir des chaînes en nombres avec `parseInt`, `parseFloat` ou `Number()`.

---

⬅️ [Chapitre précédent : Math](./b_Math.md)
➡️ [Chapitre suivant : Opérateurs avancés](./d_Avances.md)
