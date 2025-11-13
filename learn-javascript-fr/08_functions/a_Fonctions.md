---
chapter: 8
section: a
title: Les Fonctions
description: Les fonctions sont des blocs de code réutilisables qui exécutent une tâche spécifique. Elles acceptent des valeurs d’entrée appelées arguments et renvoient un résultat. Indispensables en programmation, elles permettent de structurer et d’organiser efficacement un programme.
---

# Les Fonctions

Parmi toutes les notions de la programmation, les fonctions occupent une place centrale. Elles permettent de regrouper un ensemble d’instructions sous un nom unique, de les exécuter à volonté et de les réutiliser dans différents contextes. À l’image des fonctions mathématiques, elles prennent des **valeurs d’entrée** (appelées *arguments*) et produisent généralement une **valeur de sortie**.

Définir une fonction, c’est donc décrire une opération que l’on pourra ensuite invoquer dans le reste du programme. Une fois définie, elle peut être appelée à tout moment, ce qui en fait un outil incontournable pour éviter la répétition de code.

## Déclaration et expression de fonction

Il existe deux manières principales de créer une fonction en JavaScript.

La première est la **déclaration de fonction**. Elle consiste à introduire un nom de fonction, suivi de ses arguments et de son corps :

```javascript
function double(x) {
  return 2 * x;
}
```

Une particularité de la déclaration de fonction est qu’elle peut être invoquée même avant sa définition, car le moteur JavaScript les enregistre dès le début de l’exécution.

La seconde méthode est l’**expression de fonction**. Ici, la fonction est affectée à une variable, ce qui en fait une valeur manipulable comme n’importe quelle autre donnée :

```javascript
let double = function(x) {
  return 2 * x;
};
```

Dans ce cas, la fonction ne peut pas être utilisée avant sa définition, exactement comme une variable classique. Si le nom est omis, on parle alors de **fonction anonyme**.

## Fonctions comme valeurs

En JavaScript, les fonctions sont de véritables valeurs. Elles peuvent être stockées dans des variables, passées en argument à d’autres fonctions, ou encore renvoyées comme résultat.
Ce comportement particulier permet de définir des fonctions dites **callbacks**, qui sont exécutées par une autre fonction à un moment précis :

```javascript
function saluer(nom, action) {
  console.log("Bonjour " + nom);
  action();
}

saluer("Alice", function() {
  console.log("Bienvenue dans le programme !");
});
```

Ici, la fonction anonyme fournie comme deuxième argument sera exécutée après l’affichage du message de salutation.

## Les fonctions fléchées

Depuis les versions modernes de JavaScript, on peut aussi écrire des **fonctions fléchées** (*arrow functions*), qui constituent une forme plus compacte :

```javascript
const double = (x) => 2 * x;
```

Cette écriture est particulièrement appréciée pour sa concision. Cependant, elle diffère des fonctions traditionnelles sur certains points importants : une fonction fléchée n’a pas ses propres valeurs pour `this`, `arguments` ou `super`, et elle ne peut pas être utilisée comme constructeur. Cela la rend pratique pour les petites opérations, mais moins adaptée dans certains cas.

---

## À retenir

Les fonctions permettent de structurer et de réutiliser le code.
On peut les définir sous forme de **déclaration** ou d’**expression**, leur donner un nom ou non, et même les écrire de manière plus concise grâce aux **fonctions fléchées**. En tant que valeurs, elles peuvent être transmises à d’autres fonctions, ce qui ouvre la voie à des concepts avancés comme les **callbacks**.

---

⬅️ [Chapitre précédent : Contrôle du Flux](../07_loops/g_Exercices.md)

➡️ [Chapitre suivant : Les Paramètres](./b_higher-order.md)
