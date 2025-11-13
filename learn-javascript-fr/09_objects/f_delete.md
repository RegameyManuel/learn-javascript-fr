---
chapter: 9
section: f
title: Le mot clé delete
description: L’opérateur `delete` permet de supprimer une propriété d’un objet. Cette opération ne détruit pas l’objet lui-même, mais enlève la clé et la valeur concernées, rendant la propriété inaccessible.
---

# Le mot clé delete

En JavaScript, il est possible de supprimer une propriété d’un objet grâce à l’opérateur `delete`. Lorsqu’il est utilisé, il retire complètement la clé et la valeur correspondante de l’objet. La propriété disparaît, comme si elle n’avait jamais été définie, et ne peut plus être consultée ni énumérée.

Prenons un exemple simple. Si nous créons un objet représentant un adulte et que nous définissons ensuite un objet enfant qui hérite de ses propriétés :

```javascript
let adult = { age: 26 };
let child = Object.create(adult);

child.age = 8;
```

Ici, l’objet `child` possède sa propre propriété `age`, qui masque celle de son prototype `adult`. Si l’on supprime la propriété définie directement dans `child`, alors l’accès à `child.age` se fera à nouveau via le prototype :

```javascript
delete child.age;
console.log(child.age); // 26
```

La suppression libère simplement la place dans l’objet, ce qui fait remonter la recherche vers le prototype. La propriété `age` de `adult` n’a pas été modifiée. On voit donc que `delete` ne touche pas aux objets de la chaîne de prototypes : il agit uniquement sur la clé directement définie sur l’objet.

Il existe toutefois des limitations. Si une propriété est marquée comme non configurable, `delete` ne pourra pas la supprimer. De même, il ne supprime pas l’objet entier. Pour se débarrasser complètement d’une variable et libérer la mémoire, il suffit de lui affecter la valeur `null` ou `undefined`, ce qui rompt la référence avec l’objet.

---

## À retenir

L’opérateur `delete` supprime une propriété d’un objet, mais il ne détruit pas l’objet en lui-même et n’affecte pas la chaîne de prototypes. Lorsqu’une propriété disparaît, JavaScript continue simplement sa recherche dans les prototypes. Si l’on souhaite effacer totalement un objet, il faut retirer la référence en attribuant `null` ou `undefined` à la variable qui le contenait.

---

⬅️ [Chapitre précédent : Prototype](./e_prototype.md)

➡️ [Chapitre suivant : L’énumération](./g_enumeration.md)
