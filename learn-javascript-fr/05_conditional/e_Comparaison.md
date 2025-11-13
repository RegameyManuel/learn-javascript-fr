---
chapter: 5
section: e
title: Comparaison
description: Découvrir les opérateurs de comparaison en JavaScript, comprendre la différence entre égalité simple et stricte, et introduire l’opérateur ternaire.
---

# Comparaison

Concentrons-nous sur la partie conditionnelle :

```javascript
if (country === "France") {
    ...
}
```

La partie conditionnelle (ou la condition) est représentée par la variable `country` suivie par les trois signes égal (`===`). Cet opérateur d'égalité stricte teste si la variable `country` possède à la fois la valeur attendue (`France`) et le type requis (`String`).

Bien sûr, il est possible de réaliser la condition suivante avec l'opérateur d'égalité à deux signes égal (`==`). Dans ce cas, on occultera le test du type de la variable. Ainsi, la condition `if (x == 5)` retournera `true` aussi bien pour `var x = 5;` que pour `var x = "5";`. Dans le premier cas `x` est du type `Number` et dans le second du type `String`.

Vous en conviendrez, cela change beaucoup de choses et peut créer des comportements indésirables. Pour prévenir ce genre de problème, il est recommandé d’utiliser en priorité la comparaison stricte (`===` et `!==`) plutôt que la comparaison faible (`==` et `!=`).

## Autres tests conditionnels fréquents

* `x > a` : x est strictement supérieur à a ?
* `x < a` : x est strictement inférieur à a ?
* `x <= a` : x est inférieur ou égal à a ?
* `x >= a` : x est supérieur ou égal à a ?
* `x != a` : x est différent de a ?
* `x` : est-ce que x existe ?

## Comparaison logique - opérateur ternaire

Pour éviter une écriture trop répétitive des blocs `if/else`, on peut utiliser la syntaxe du **ternaire**.
En substance, il s’agit d’écrire un `if/else` simple de manière plus concise.

```javascript
let topper = marks > 85 ? "YES" : "NO";
```

Dans l’exemple ci-dessus :

* `?` est l’opérateur conditionnel,
* l’opérande gauche (`marks > 85`) est la condition à tester,
* si la condition est `true`, la valeur `"YES"` est assignée à `topper`,
* sinon, la valeur `"NO"` est assignée.

Les deux cas possibles sont séparés par le signe `:`.

---

## À retenir

* L’opérateur `===` compare à la fois la valeur et le type ; il est recommandé par rapport à `==`.
* Les opérateurs `>`, `<`, `<=`, `>=`, `!=` permettent d’évaluer différentes relations entre valeurs.
* L’opérateur ternaire `condition ? valeurSiVrai : valeurSiFaux` est une forme raccourcie d’un `if/else` simple.

---

⬅️ [Chapitre précédent : Switch](./d_switch.md)

➡️ [Chapitre suivant : Conditions multiples](./f_Conditions.md)
