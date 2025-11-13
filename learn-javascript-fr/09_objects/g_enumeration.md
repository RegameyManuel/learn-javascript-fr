---
chapter: 9
section: g
title: L'énumération
description: L’énumération consiste à parcourir les propriétés d’un objet afin d’exécuter des instructions sur chacune d’elles. C’est une manière de découvrir et de manipuler dynamiquement le contenu des objets en JavaScript.
---

# L’énumération

En JavaScript, il est fréquent de vouloir examiner toutes les propriétés d’un objet afin d’agir sur chacune d’elles. Ce processus est appelé énumération. Grâce à lui, on peut parcourir l’ensemble des clés d’un objet et utiliser leurs valeurs de manière dynamique, sans connaître à l’avance la structure précise de cet objet.

La méthode la plus ancienne pour énumérer consiste à utiliser une boucle `for...in`. Cette boucle passe en revue toutes les propriétés énumérables de l’objet, y compris celles héritées de son prototype. À chaque itération, la variable choisie représente le nom d’une propriété, ce qui permet d’accéder à sa valeur en l’utilisant comme clé.

Prenons un exemple simple :

```javascript
let fruit = {
  apple: 2,
  orange: 5,
  pear: 1
};

let sentence = "I have ";

for (let kind in fruit) {
  let quantity = fruit[kind];
  sentence += quantity + " " + kind + (quantity === 1 ? "" : "s") + ", ";
}

sentence = sentence.substr(0, sentence.length - 2) + ".";
console.log(sentence); // I have 2 apples, 5 oranges, 1 pear.
```

Ici, la boucle permet de construire une phrase en parcourant chaque propriété de l’objet `fruit`. La syntaxe reste simple, mais elle inclut également les propriétés héritées, ce qui peut parfois amener des résultats inattendus si l’on n’y prend pas garde.

Une autre approche, plus moderne et souvent plus sûre, consiste à utiliser la méthode `Object.keys`. Celle-ci retourne un tableau contenant uniquement les noms des propriétés que l’objet possède directement, sans inclure celles héritées. On peut alors parcourir ce tableau avec une boucle ou une méthode comme `forEach`.

```javascript
let object = { foo: "bar", baz: "qux" };

Object.keys(object).forEach(function(property) {
  console.log(property + ": " + object[property]);
});
// Affiche :
// foo: bar
// baz: qux
```

Cette méthode donne un contrôle plus précis, car elle se limite aux propriétés propres à l’objet, sans aller chercher dans la chaîne de prototypes.

---

## À retenir

L’énumération permet de parcourir dynamiquement les propriétés d’un objet. La boucle `for...in` parcourt toutes les propriétés énumérables, y compris celles héritées, tandis que `Object.keys` ne retient que celles définies directement dans l’objet. Ces techniques offrent des moyens souples et puissants de travailler avec des structures de données dont on ne connaît pas à l’avance la forme exacte.

---

⬅️ [Chapitre précédent : Le mot clé delete](./f_delete.md)

➡️ [Chapitre suivant : Classes](./h_class.md)
