---
chapter: 13
section: a
title: Modules
description: Les modules permettent d’organiser le code en parties séparées, réutilisables et faciles à maintenir. Ils introduisent les directives `import` et `export` pour partager ou utiliser des fonctionnalités entre fichiers.
---

# Modules

Lorsqu’une application grandit, le code source a tendance à devenir de plus en plus complexe et difficile à maintenir. Si l’on regroupe toutes les fonctionnalités dans un seul fichier, il devient vite pénible de s’y retrouver, et les risques d’erreurs ou de comportements inattendus augmentent. Pour éviter cela, JavaScript propose un mécanisme de **modules**.  

Un module est un fichier qui encapsule une partie du code : il déclare ce qu’il rend disponible aux autres fichiers et peut lui-même importer des fonctionnalités définies ailleurs. On peut ainsi diviser une application en morceaux logiques, faciles à comprendre et à réutiliser.  

Historiquement, plusieurs systèmes de modules ont vu le jour :  

- **AMD** (Asynchronous Module Definition), utilisé notamment par *require.js*.  
- **CommonJS**, adopté par Node.js.  
- **UMD** (Universal Module Definition), qui cherche à être compatible avec les deux précédents.  

Aujourd’hui, la norme moderne repose sur deux mots-clés : `export` et `import`.  

## Exporter et importer des fonctions

Un module peut désigner certaines de ses fonctions ou variables comme accessibles depuis l’extérieur grâce à `export`. Un autre fichier peut ensuite les utiliser en les important avec `import`.  

Prenons un exemple simple. On crée un fichier `sayHi.js` qui exporte une fonction :

```javascript
// sayHi.js
export const sayHi = (user) => {
  alert(`Bonjour, ${user}!`);
};
```

Dans un autre fichier, `main.js`, on peut importer cette fonction et l’utiliser :

```javascript
// main.js
import { sayHi } from "./sayHi.js";

sayHi("Kelvin"); // Bonjour, Kelvin!
```

Ici, le fichier `sayHi.js` déclare ce qu’il rend disponible, et `main.js` choisit ce qu’il souhaite importer.

## Export nommé et export par défaut

Il existe deux façons d’exporter : **nommée** et **par défaut**.

Un export nommé permet d’indiquer précisément quelles constantes ou fonctions doivent être accessibles. On peut le faire directement à la déclaration ou à la fin du fichier :

```javascript
//  person.js
export const name = "Kelvin";
export const age = 30;

// ou bien
const name = "Kelvin";
const age = 30;
export { name, age };
```

Un export par défaut, en revanche, signale qu’un module fournit une seule valeur principale. Par exemple :

```javascript
//  message.js
const message = (name, age) => {
  return `${name} is ${age} years old.`;
};
export default message;
```

Lorsqu’on importe, la syntaxe change légèrement :

```javascript
import { name, age } from "./person.js"; // import d’exports nommés
import message from "./message.js";      // import d’un export par défaut
```

Il n’est pas possible d’avoir plusieurs exports par défaut dans un même fichier, mais on peut combiner un export par défaut et des exports nommés.

## Attention aux dépendances circulaires

Un point de vigilance concerne la **dépendance circulaire** : c’est une situation où un module A dépend d’un module B, alors que B dépend lui-même de A (directement ou indirectement). Ces boucles rendent le code difficile à exécuter correctement et doivent être évitées par une bonne conception.

---

## À retenir

Les modules sont une manière d’organiser son code en fichiers autonomes, réutilisables et mieux structurés.

* `export` permet de désigner ce qui est rendu public par un module.
* `import` permet de réutiliser ce qui a été exporté ailleurs.
* Il existe deux formes d’export : nommé (plusieurs par fichier) et par défaut (un seul par fichier).
* Une bonne organisation modulaire réduit la complexité et facilite la maintenance.

---

⬅️ [Chapitre précédent : …](../12_autre_chapitre/l_exercices.md)

➡️ [Chapitre suivant : …](./b_autre_section.md)
