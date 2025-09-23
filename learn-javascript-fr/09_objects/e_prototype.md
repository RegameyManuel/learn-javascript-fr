---
chapter: 9
section: e
title: Prototype
description: Le prototype est un mécanisme central de JavaScript. Chaque objet peut hériter de propriétés et de méthodes à travers une chaîne de prototypes, ce qui constitue le système d’héritage propre au langage.
---

# Prototype

En JavaScript, chaque objet possède un lien particulier appelé prototype. Ce prototype est lui-même un objet, dont les propriétés et les méthodes peuvent être partagées avec d’autres objets. C’est ce mécanisme qui constitue l’héritage en JavaScript, non pas sous la forme de classes traditionnelles comme en Java ou en C#, mais à travers une chaîne dynamique reliant plusieurs objets entre eux.

Lorsqu’on tente d’accéder à une propriété sur un objet, l’interpréteur commence par chercher cette propriété directement dans l’objet. Si elle n’existe pas, il poursuit sa recherche dans le prototype de cet objet, puis dans le prototype du prototype, et ainsi de suite, jusqu’à atteindre `Object.prototype`, qui est l’ancêtre commun de tous les objets. Cette suite d’objets liés entre eux est appelée la chaîne de prototypes.

Prenons un exemple simple. Si l’on définit un objet avec une seule propriété :

```javascript
let adult = { age: 26 };
```

On peut bien sûr accéder à la valeur `age`, mais si l’on appelle une méthode comme `toString`, qui n’a pas été définie dans `adult`, JavaScript va automatiquement se tourner vers le prototype. Par défaut, ce prototype est `Object.prototype`, qui fournit déjà toute une série de méthodes standards, comme `toString` ou `hasOwnProperty`. Ainsi, même si `adult` ne déclare pas directement ces méthodes, elles sont disponibles grâce au prototype.

Il est possible de personnaliser cet héritage. Par exemple, on peut surcharger la méthode `toString` en la redéfinissant directement dans l’objet :

```javascript
adult.toString = function () {
  return "J’ai " + this.age + " ans";
};
```

Dès lors, c’est cette version personnalisée qui sera utilisée, l’interpréteur donnant toujours la priorité aux propriétés définies directement dans l’objet avant de consulter ses prototypes.

On peut également créer un objet en spécifiant explicitement son prototype grâce à la méthode `Object.create`. Si l’on écrit :

```javascript
let child = Object.create(adult);
child.age = 8;
```

L’objet `child` hérite du prototype `adult`. Cela signifie qu’il a accès aux propriétés et méthodes définies dans `adult`, tout en conservant la possibilité de définir ou de redéfinir ses propres valeurs. Ici, `child` possède sa propre propriété `age`, mais il peut aussi utiliser la méthode `toString` définie dans `adult`. Si cette méthode n’existait pas, JavaScript aurait continué la recherche dans `Object.prototype`.

Ce système rend la chaîne de prototypes extrêmement flexible. Chaque objet peut hériter d’un autre, tout en restant libre de redéfinir ce dont il a besoin. C’est ce mécanisme qui fonde la programmation orientée objet en JavaScript, bien avant l’introduction de la syntaxe moderne `class`.

---

## À retenir

Le prototype est la clé de voûte du modèle objet en JavaScript. Chaque objet peut hériter de propriétés et de méthodes à travers une chaîne de prototypes qui remonte jusqu’à `Object.prototype`. Lorsqu’une propriété est recherchée, l’interpréteur explore cette chaîne jusqu’à la trouver. Ce système permet de partager du code entre objets et d’organiser efficacement la réutilisation des fonctionnalités.

---

⬅️ [Chapitre précédent : Les références](./d_reference.md)

➡️ [Chapitre suivant : Le mot clé delete](./f_delete.md)
