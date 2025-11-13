---
chapter: 6
section: b
title: Référence des méthodes de tableaux
description: Référence détaillée des principales méthodes de tableaux en JavaScript, avec explications, mutation ou non, valeur de retour et exemples approfondis.
---

# Référence des méthodes de tableaux

Ce document présente les méthodes et la propriété les plus utilisées pour manipuler les tableaux en JavaScript.  
Pour chaque entrée : **ce que ça fait**, **si le tableau est modifié (mutation)**, **ce qui est renvoyé**, et **des exemples**.

## Ajouter / Supprimer

### `push(...items)`

**Ajoute** un ou plusieurs éléments **à la fin**.  
**Mutation :** oui. **Retour :** nouvelle longueur.

```javascript
const fruits = ["pomme", "banane"];
const len = fruits.push("orange", "kiwi");
console.log(fruits); // ["pomme","banane","orange","kiwi"]
console.log(len);    // 4
```

### `pop()`

**Retire** le **dernier** élément.
**Mutation :** oui. **Retour :** l’élément retiré (ou `undefined` si vide).

```javascript
const nums = [1, 2, 3];
const last = nums.pop();
console.log(last); // 3
console.log(nums); // [1, 2]
```

### `unshift(...items)`

**Ajoute** un ou plusieurs éléments **au début**.
**Mutation :** oui. **Retour :** nouvelle longueur.

```javascript
const a = [2, 3];
a.unshift(0, 1);
console.log(a); // [0,1,2,3]
```

### `shift()`

**Retire** le **premier** élément.
**Mutation :** oui. **Retour :** l’élément retiré (ou `undefined`).

```javascript
const a = ["x","y","z"];
const first = a.shift();
console.log(first); // "x"
console.log(a);     // ["y","z"]
```

### `splice(start, deleteCount, ...items)`

**Ajoute**, **remplace** ou **supprime** des éléments **dans** le tableau.
**Mutation :** oui. **Retour :** tableau des éléments supprimés.

* `start` peut être négatif (compte depuis la fin).
* `deleteCount` omis ⇒ supprime jusqu’à la fin.

```javascript
const a = [1,2,3,4,5];
// supprimer 2 éléments à partir de l’index 1
const removed = a.splice(1, 2);
console.log(removed); // [2,3]
console.log(a);       // [1,4,5]

// remplacer à partir de l’index 1 par "A","B"
a.splice(1, 1, "A", "B");
console.log(a); // [1,"A","B",5]
```

### `slice(begin, end)`

**Copie** une portion du tableau **sans** le modifier.
**Mutation :** non. **Retour :** **nouveau** tableau.

* Indices négatifs acceptés.
* `end` exclusif.

```javascript
const a = [0,1,2,3,4];
console.log(a.slice(1, 3));   // [1,2]
console.log(a.slice(-2));     // [3,4]
console.log(a);               // [0,1,2,3,4] (inchangé)
```

## Fusion et conversion

### `concat(...arraysOrValues)`

**Fusionne** tableaux/valeurs et **retourne un nouveau tableau**.
**Mutation :** non. **Retour :** nouveau tableau.

```javascript
const a = [1,2];
const b = [3,4];
const c = a.concat(b, 5);
console.log(c); // [1,2,3,4,5]
console.log(a); // [1,2] (inchangé)
```

### `join(separator = ",")`

Crée une **chaîne** avec les éléments séparés par `separator`.
**Mutation :** non. **Retour :** chaîne.

```javascript
const a = ["a","b","c"];
console.log(a.join("-")); // "a-b-c"
console.log(a.join());    // "a,b,c" (séparateur par défaut)
```

### `toString()`

Convertit le tableau en **chaîne** (équivalent à `join(",")`).
**Mutation :** non. **Retour :** chaîne.

```javascript
console.log([1,2,[3]].toString()); // "1,2,3"
```

## Parcours

### `forEach(callback, thisArg?)`

Exécute `callback` **pour chaque élément**.
**Mutation :** non (mais vous pouvez modifier les éléments si vous y accédez).
**Retour :** `undefined`.

> À privilégier pour les **effets de bord** (log, DOM, etc.). N’utilisez pas `forEach` pour produire un nouveau tableau (utilisez `map`).

```javascript
const a = [1,2,3];
a.forEach((x, i) => console.log(i, x));
```

### `map(callback, thisArg?)`

**Transforme** chaque élément et **retourne un nouveau tableau**.
**Mutation :** non. **Retour :** nouveau tableau.

```javascript
const a = [1,2,3];
const doubled = a.map(x => x * 2);
console.log(doubled); // [2,4,6]
console.log(a);       // [1,2,3]
```

### `filter(callback, thisArg?)`

**Sélectionne** les éléments qui satisfont la condition.
**Mutation :** non. **Retour :** nouveau tableau filtré.

```javascript
const a = [1,2,3,4,5];
const evens = a.filter(x => x % 2 === 0);
console.log(evens); // [2,4]
```

## Recherche

### `find(callback, thisArg?)`

Retourne le **premier élément** qui satisfait la condition (ou `undefined`).
**Mutation :** non.

```javascript
const a = [{id:1},{id:2},{id:3}];
const found = a.find(o => o.id === 2);
console.log(found); // {id:2}
```

### `findIndex(callback, thisArg?)`

Retourne l’**index** du premier élément qui satisfait la condition (ou `-1`).
**Mutation :** non.

```javascript
const a = [10, 20, 30];
console.log(a.findIndex(x => x > 15)); // 1
```

### `includes(value, fromIndex = 0)`

Vérifie si la valeur est présente (`true`/`false`).
**Mutation :** non.
**Détail important :** `includes` utilise la comparaison **SameValueZero** ⇒ il trouve aussi `NaN`.

```javascript
console.log([1,2,NaN].includes(NaN)); // true
```

### `indexOf(value, fromIndex = 0)` / `lastIndexOf(value, fromIndex?)`

Renvoient l’**index** de la première/dernière occurrence (ou `-1`).
**Mutation :** non.
**Détail :** comparaison **stricte** (`===`) ⇒ ne trouve **pas** `NaN`.

```javascript
const a = [1,2,1,2];
console.log(a.indexOf(2));      // 1
console.log(a.lastIndexOf(2));  // 3
console.log([NaN].indexOf(NaN)); // -1 (contrairement à includes)
```

## Réduction

### `reduce(callback, initialValue?)`

Combine les éléments pour produire **une seule valeur**.
**Mutation :** non. **Retour :** valeur accumulée.
**Important :** fournissez **toujours** `initialValue` pour éviter des pièges avec tableaux vides.

```javascript
const a = [1,2,3,4];
const sum = a.reduce((acc, x) => acc + x, 0);
console.log(sum); // 10

// Exemple avancé : regrouper par parité
const grouped = [1,2,3,4,5].reduce((acc, x) => {
  const key = x % 2 === 0 ? "even" : "odd";
  (acc[key] ??= []).push(x);
  return acc;
}, {});
console.log(grouped); // { odd:[1,3,5], even:[2,4] }
```

### `reduceRight(callback, initialValue?)`

Comme `reduce`, mais de **droite à gauche**.

```javascript
const a = ["a","b","c"];
const joined = a.reduceRight((acc, x) => acc + x, "");
console.log(joined); // "cba"
```

## Tri et ordre

### `sort(compareFn?)`

Trie **en place** (mutation) et **retourne le tableau trié**.
Sans `compareFn`, tri **lexicographique** (piège pour les nombres).
Pour des nombres, fournissez un comparateur.

```javascript
const nums = [10,2,30];
nums.sort();                 // ["10","2","30"] → [10,2,30] (ordre lexicographique)
nums.sort((a,b) => a - b);   // [2,10,30]

// Tri d’objets
const users = [{n:"Zoé"},{n:"Émile"},{n:"Alice"}];
users.sort((a,b) => a.n.localeCompare(b.n, "fr"));
console.log(users.map(u => u.n)); // ["Alice","Émile","Zoé"]
```

**Mutation :** oui. **Retour :** le **même** tableau (trié).

### `reverse()`

Inverse l’ordre **en place**.
**Mutation :** oui. **Retour :** le **même** tableau.

```javascript
const a = [1,2,3];
a.reverse();
console.log(a); // [3,2,1]
```

## Autres

### `length` (propriété)

Taille du tableau. Peut être **modifiée** pour tronquer/étendre (créant des “trous”).

```javascript
const a = [1,2,3,4];
console.log(a.length); // 4
a.length = 2;
console.log(a);        // [1,2]
a.length = 5;
console.log(a);        // [1,2, <3 trous>]
```

### `flat(depth = 1)`

Aplati un tableau de tableaux.
**Mutation :** non. **Retour :** nouveau tableau.

```javascript
const a = [1, [2, [3, 4]]];
console.log(a.flat());     // [1, 2, [3, 4]]
console.log(a.flat(2));    // [1, 2, 3, 4]
```

### `flatMap(callback, thisArg?)`

Équivaut à `array.map(...).flat(1)` en **un seul passage**.
**Mutation :** non. **Retour :** nouveau tableau.

```javascript
const words = ["salut", "les amis"];
const chars = words.flatMap(w => w.split(""));
// ["s","a","l","u","t"," ","l","e","s"," ","a","m","i","s"]
```

### `fill(value, start = 0, end = length)`

Remplit une section du tableau avec `value`.
**Mutation :** oui. **Retour :** le **même** tableau.

```javascript
const a = [1,2,3,4,5];
a.fill(0, 1, 4);
console.log(a); // [1,0,0,0,5]
```

### `copyWithin(target, start = 0, end = length)`

Copie une **portion** du tableau **dans lui-même** (sans changer la taille).
**Mutation :** oui. **Retour :** le **même** tableau.

```javascript
const a = [1,2,3,4,5];
// copie les éléments [3,4] (index 2..4) à partir de l’index 0
a.copyWithin(0, 2, 4);
console.log(a); // [3,4,3,4,5]
```

### `keys()` / `values()` / `entries()`

Renvoient des **itérateurs** sur les **indices**, **valeurs**, ou **paires \[index, valeur]**.
Utile avec `for...of` ou l’opérateur de décomposition.

```javascript
const a = ["x","y"];
for (const i of a.keys()) console.log(i);       // 0, 1
for (const v of a.values()) console.log(v);     // "x","y"
for (const [i, v] of a.entries()) console.log(i, v); // 0 "x" / 1 "y"

// convertir en tableau
console.log([...a.entries()]); // [[0,"x"], [1,"y"]]
```

---

## À retenir

* **Mutation vs non-mutation** : `splice`, `sort`, `reverse`, `fill`, `copyWithin`, `push/pop/shift/unshift` **modifient** le tableau.
  `slice`, `concat`, `map`, `filter`, `flat`, `flatMap` **créent** de nouveaux tableaux.
* **Recherche** : `includes` trouve aussi `NaN`, `indexOf` non.
* **Tri** : fournissez un **comparateur** pour trier correctement des nombres ou tenir compte de la locale (`localeCompare`).
* **Réduction** : passez toujours un **accumulateur initial** à `reduce`/`reduceRight`.
* **length** peut être modifiée (tronque/étend), avec effet direct sur le contenu.

---

⬅️ [Chapitre précédent : Méthodes des tableaux](./a_array.md)

➡️ [Chapitre suivant : Memo](./c_memo.md)
