---
chapter: 9
section: i
title: L’héritage
description: L’héritage permet de créer de nouvelles classes qui réutilisent, étendent ou redéfinissent les fonctionnalités d’autres classes. En JavaScript, il s’exprime grâce au mot-clé `extends` et repose toujours sur la chaîne de prototypes.
---

# L’héritage

L’héritage est un principe central de la programmation orientée objet. Il permet à une classe d’hériter des propriétés et des méthodes d’une autre classe, afin de les réutiliser ou de les spécialiser. En JavaScript, ce mécanisme repose toujours sur la chaîne de prototypes, mais la syntaxe introduite par ES6 le rend bien plus lisible grâce au mot-clé `extends`.

Lorsqu’une classe hérite d’une autre, elle devient une sous-classe. Elle dispose immédiatement des fonctionnalités de la classe parente, tout en pouvant ajouter ses propres propriétés et méthodes, ou redéfinir celles qu’elle a reçues. Ce fonctionnement favorise la réutilisation de code et permet de structurer des hiérarchies logiques d’objets.

Voici un exemple simple. Imaginons une classe `Animal` définissant un comportement générique :

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    return this.name + " fait un bruit.";
  }
}
```

Une classe `Dog` peut hériter de `Animal` et redéfinir la méthode `speak` :

```javascript
class Dog extends Animal {
  speak() {
    return this.name + " aboie.";
  }
}

let rex = new Dog("Rex");
console.log(rex.speak()); // "Rex aboie."
```

Dans cet exemple, `Dog` reprend le constructeur de `Animal` pour initialiser son nom, mais elle fournit une version spécialisée de la méthode `speak`. Ce mécanisme est appelé redéfinition (ou overriding). Si la méthode n’avait pas été redéfinie, l’objet `rex` aurait utilisé directement la version héritée de `Animal`.

Le mot-clé `super` joue un rôle important lorsqu’une sous-classe a besoin d’appeler le constructeur ou une méthode de sa classe parente. Dans un constructeur, `super` doit être utilisé avant d’accéder à `this`, afin d’initialiser correctement l’objet hérité :

```javascript
class Cat extends Animal {
  constructor(name, color) {
    super(name);
    this.color = color;
  }

  speak() {
    return super.speak() + " Mais en réalité, " + this.name + " miaule.";
  }
}

let felix = new Cat("Félix", "noir");
console.log(felix.speak()); 
// "Félix fait un bruit. Mais en réalité, Félix miaule."
```

Ici, `super.speak()` invoque la version de la méthode définie dans la classe `Animal`, avant d’y ajouter un comportement spécifique. L’héritage permet donc de combiner la généralité d’une classe de base avec la spécialisation de classes dérivées.

---

## À retenir

L’héritage en JavaScript s’exprime grâce au mot-clé `extends`, qui relie une sous-classe à une classe parente. Ce mécanisme repose toujours sur la chaîne de prototypes mais rend le code plus clair et plus structuré. Le mot-clé `super` permet d’appeler les constructeurs ou méthodes du parent. Grâce à l’héritage, il est possible de créer des hiérarchies d’objets qui partagent un comportement commun tout en permettant des spécialisations.

---

⬅️ [Chapitre précédent : Les classes](./h_class.md)

➡️ [Chapitre suivant : Le polymorphisme](./j_polymorphism.md)

