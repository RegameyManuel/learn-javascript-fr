---
chapter: 4
section: b
title: Création de chaînes
description: Découvrir comment créer des chaînes de caractères en JavaScript et utiliser les littéraux de gabarit introduits avec ES6.
---

# Création de chaînes

Les chaînes de caractères peuvent être définies par du texte entouré par des guillemets simples ou doubles :

```javascript
// Avec des guillemets simples
let str = 'Notre belle chaîne';

// Avec des guillemets doubles
let otherStr = "Une autre chaîne";
```

Les chaînes supportent l’Unicode, ce qui permet d’utiliser des caractères provenant de quasiment toutes les langues :

```javascript
let unicodeStr = "中文 español English हिन्दी العربية русский 日本語 한국어";
console.log(unicodeStr);
```

Il est également possible d’utiliser le constructeur `String` :

```javascript
const stringObject = new String("Je suis une chaîne");
```

Cependant, il est déconseillé de créer des chaînes avec `new String`, car cela crée un **objet** au lieu d’une valeur primitive `string`. Cela peut entraîner de la confusion.
La bonne pratique est de préférer les littéraux de chaînes (`"..."` ou `'...'`).


## Littéraux de gabarits

Depuis ES6, JavaScript introduit une nouvelle syntaxe : les **littéraux de gabarits**.
Ce sont des chaînes entourées de backticks (`` ` ``), qui permettent d’inclure des expressions directement à l’intérieur grâce à la syntaxe `${expression}`.

```javascript
const name = "John";
const message = `Hello, ${name}!`;
console.log(message); // Hello, John!
```

Les littéraux de gabarits permettent aussi d’écrire sur plusieurs lignes et d’inclure des calculs ou expressions :

```javascript
const age = 25;
const intro = `Mon nom est ${name}
et j'ai ${age} ans.`;

console.log(intro);
```


---

## À retenir

* Une chaîne peut être créée avec `'...'` ou `"..."`.
* Il est déconseillé d’utiliser `new String()` pour créer une chaîne.
* Les **littéraux de gabarits** (`` `...` ``) facilitent l’interpolation de variables et l’écriture sur plusieurs lignes.

---

⬅️ [Chapitre précédent : Chaînes de caractères](./a_Chaines.md)

➡️ [Chapitre suivant : Remplacement de chaînes](./c_Remplacement.md)

