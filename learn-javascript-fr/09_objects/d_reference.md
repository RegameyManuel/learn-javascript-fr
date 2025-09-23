---
chapter: 9
section: d
title: Les références
description: En JavaScript, les objets ne sont jamais copiés directement. Ce sont les références, c’est-à-dire les liens vers leur emplacement mémoire, qui sont transmises et partagées. Comprendre cette mécanique est essentiel pour éviter des confusions lors de la manipulation d’objets.
---

# Les références

Lorsqu’on manipule un objet en JavaScript, on ne travaille pas sur l’objet lui-même mais sur une référence qui pointe vers l’endroit où cet objet est stocké en mémoire. Cette distinction est capitale : deux variables peuvent très bien désigner le même objet, sans qu’une véritable copie n’ait jamais été effectuée.

Imaginons par exemple un objet défini de façon littérale :

```javascript
let object1 = { foo: "bar" };
```

Si l’on affecte cet objet à une autre variable, la nouvelle variable ne contient pas une copie indépendante, mais bien la même référence :

```javascript
let object2 = object1;
console.log(object1 === object2); // true
```

Les deux variables pointent donc vers un seul et même objet. Modifier une propriété à travers l’une revient automatiquement à modifier ce que l’autre « voit ». C’est un comportement très différent des valeurs primitives, qui, elles, sont copiées et manipulées indépendamment.

Cette logique peut être illustrée de manière imagée. Si l’on considère un objet représentant une pizza, et qu’on assigne cette pizza à deux variables distinctes, les deux renvoient toujours à la même pizza. Si l’une des variables « mange une part », la pizza partagée par l’autre variable sera elle aussi amputée :

```javascript
let myPizza = { slices: 5 };
let yourPizza = myPizza;

myPizza.slices = myPizza.slices - 1;
console.log(yourPizza.slices); // 4
```

Ici, `myPizza` et `yourPizza` partagent la même référence. Il ne s’agit pas de deux pizzas différentes mais bien de la même, vue à travers deux noms.

Il est toutefois possible de créer une copie indépendante d’un objet à l’aide de méthodes comme `Object.assign` ou, plus récemment, l’opérateur de déstructuration (`{ ...objet }`). Dans ce cas, on obtient un nouvel objet distinct, avec son propre emplacement mémoire. Les modifications apportées à l’un ne se répercuteront pas sur l’autre.

---

## À retenir

Les objets ne sont jamais copiés automatiquement en JavaScript. Lorsqu’on les assigne à une variable ou qu’on les transmet à une fonction, c’est toujours leur référence qui circule. Comprendre ce mécanisme permet d’éviter les effets de bord inattendus et explique pourquoi plusieurs variables peuvent sembler « partager » les mêmes données. Pour obtenir de véritables duplications, il faut explicitement créer une copie de l’objet.

---

⬅️ [Chapitre précédent : La mutabilité](./c_mutable.md)

➡️ [Chapitre suivant : Prototype](./e_prototype.md)

