---
chapter: 9
section: h
title: Les classes
description: Introduites avec ES6, les classes offrent une syntaxe plus claire et familière pour créer des objets et gérer l’héritage en JavaScript. Elles reposent toujours sur le mécanisme de prototypes, mais simplifient son usage.
---

# Les classes

Depuis 2015 (ES6), JavaScript propose une syntaxe de classes. Cette nouveauté ne change pas le fonctionnement fondamental du langage, qui reste basé sur l’héritage par prototypes, mais elle rend la création et la structuration d’objets beaucoup plus lisibles. La syntaxe des classes se rapproche de celle que l’on retrouve dans d’autres langages orientés objet, comme Java ou C#, ce qui facilite l’apprentissage et la compréhension.

Une classe est une sorte de modèle qui permet de créer plusieurs objets partageant la même structure et les mêmes comportements. On définit ses propriétés et ses méthodes directement dans la déclaration de la classe. Lorsqu’on instancie cette classe à l’aide du mot-clé `new`, on obtient un nouvel objet construit à partir de ce modèle.

Voici un exemple simple :

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    return "Bonjour, je m’appelle " + this.name;
  }
}

let alice = new Person("Alice", 30);
console.log(alice.greet()); // "Bonjour, je m’appelle Alice"
```

Le constructeur est une fonction spéciale appelée automatiquement lors de la création de l’objet. C’est là que l’on initialise les propriétés de chaque instance. Les méthodes définies dans la classe ne sont pas recopiées pour chaque objet : elles sont en réalité stockées dans le prototype de la classe, ce qui permet de mutualiser leur usage.

L’héritage entre classes s’exprime grâce au mot-clé `extends`. Une classe peut hériter des propriétés et méthodes d’une autre, et enrichir ou modifier ce comportement. Le mot-clé `super` permet d’appeler le constructeur ou les méthodes de la classe parente.

```javascript
class Student extends Person {
  constructor(name, age, level) {
    super(name, age);
    this.level = level;
  }

  greet() {
    return super.greet() + " et je suis en niveau " + this.level;
  }
}

let bob = new Student("Bob", 22, "Master");
console.log(bob.greet()); 
// "Bonjour, je m’appelle Bob et je suis en niveau Master"
```

Grâce à cette syntaxe, JavaScript offre un cadre plus clair pour exprimer des notions classiques de la programmation orientée objet comme l’héritage, la redéfinition de méthodes ou la réutilisation de code. Pourtant, sous cette apparence, tout repose toujours sur la mécanique des prototypes.

---

## À retenir

Les classes ne modifient pas le cœur de JavaScript mais simplifient la manière d’écrire du code orienté objet. Elles permettent de définir des modèles réutilisables pour créer des objets, de structurer le code autour de constructeurs et de méthodes, et de mettre en place de l’héritage de manière claire et lisible. Elles sont devenues la norme pour écrire du code moderne en JavaScript.

---

⬅️ [Chapitre précédent : L’énumération](./g_enumeration.md)

➡️ [Chapitre suivant : L’héritage](./i_inheritance.md)
