---
chapter: 9
section: j
title: Le polymorphisme
description: Le polymorphisme désigne la capacité d’objets différents à répondre à un même message, souvent par des comportements adaptés. En JavaScript, il se manifeste principalement à travers la redéfinition des méthodes dans une hiérarchie de classes.
---

# Le polymorphisme

Le polymorphisme est une notion fondamentale de la programmation orientée objet. Il désigne la capacité de plusieurs objets à partager la même interface tout en proposant des comportements différents. Autrement dit, une même méthode peut être appelée sur des instances de classes différentes, chacune donnant une réponse adaptée à sa propre nature.

En JavaScript, le polymorphisme se traduit le plus souvent par la redéfinition de méthodes dans des sous-classes. Grâce à l’héritage, une classe fille peut conserver la signature d’une méthode définie dans la classe parente, mais lui donner une implémentation spécifique. Le code qui utilise ces objets n’a pas besoin de savoir à quelle sous-classe ils appartiennent : il appelle simplement la méthode, et c’est l’objet lui-même qui détermine le comportement.

Prenons un exemple simple. Imaginons une classe de base `Animal` avec une méthode `speak` :

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

On peut ensuite créer plusieurs sous-classes spécialisées :

```javascript
class Dog extends Animal {
  speak() {
    return this.name + " aboie.";
  }
}

class Cat extends Animal {
  speak() {
    return this.name + " miaule.";
  }
}
```

Si l’on crée une liste d’animaux et qu’on leur demande de « parler », chacun réagit à sa manière :

```javascript
let animals = [new Dog("Rex"), new Cat("Félix")];

animals.forEach(animal => {
  console.log(animal.speak());
});
// "Rex aboie."
// "Félix miaule."
```

Le même appel `animal.speak()` déclenche des comportements différents selon la classe de l’objet. C’est là toute la force du polymorphisme : il permet d’écrire du code générique, capable de manipuler des objets variés sans se soucier de leurs différences internes.

Le polymorphisme peut également s’exprimer au travers d’interfaces implicites, car JavaScript est un langage souple. Tant que des objets possèdent une méthode donnée, ils peuvent être utilisés de manière interchangeable, même sans lien d’héritage. On parle alors parfois de *duck typing* : « si ça marche comme un canard et que ça cancane comme un canard, alors c’est un canard ».

---

## À retenir

Le polymorphisme permet d’invoquer une même méthode sur des objets différents, chaque objet apportant sa propre implémentation. En JavaScript, cela se manifeste à travers la redéfinition des méthodes dans les sous-classes, mais aussi par le caractère flexible du langage qui accepte toute structure possédant la méthode attendue. C’est un outil puissant pour écrire du code générique, clair et extensible.

---

⬅️ [Chapitre précédent : L’héritage](./i_inheritance.md)

➡️ [Chapitre suivant : L’encapsulation](./k_encapsulation.md)
