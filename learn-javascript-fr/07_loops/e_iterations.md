---
chapter: 7
section: e
title: Itérations modernes sur les tableaux
description: Les tableaux en JavaScript proposent des méthodes d’itération intégrées qui facilitent le parcours et la transformation des données. Ces méthodes, plus lisibles et expressives que les boucles classiques, sont devenues incontournables dans la pratique moderne du langage.
---

# Itérations modernes sur les tableaux

Si les boucles traditionnelles (`for`, `while`, `do...while`) restent des outils essentiels, JavaScript met également à disposition des méthodes propres aux tableaux qui permettent d’itérer et de manipuler les données de façon plus concise et expressive. Ces méthodes appartiennent toutes à l’objet **Array** et sont désormais largement privilégiées dans le code moderne.



## forEach()

`forEach()` exécute une fonction donnée pour **chaque élément du tableau**.  
Elle ne retourne pas de valeur mais permet d’effectuer facilement des actions comme l’affichage ou la modification de données.

```javascript
const fruits = ["pomme", "banane", "cerise"];

fruits.forEach(function(fruit) {
  console.log(fruit);
});
```

Résultat :

```
pomme
banane
cerise
```



## map()

`map()` construit un **nouveau tableau** contenant le résultat d’une fonction appliquée à chaque élément.

```javascript
const nombres = [1, 2, 3, 4];
const doubles = nombres.map(x => x * 2);

console.log(doubles); // [2, 4, 6, 8]
```



## filter()

`filter()` retourne un nouveau tableau constitué uniquement des éléments qui satisfont une condition donnée.

```javascript
const nombres = [10, 15, 20, 25, 30];
const pairs = nombres.filter(x => x % 2 === 0);

console.log(pairs); // [10, 20, 30]
```



## reduce()

`reduce()` applique une fonction dite **accumulateur** afin de combiner les éléments du tableau en une seule valeur.

```javascript
const nombres = [1, 2, 3, 4];
const somme = nombres.reduce((acc, x) => acc + x, 0);

console.log(somme); // 10
```



## some() et every()

Ces deux méthodes servent à tester les éléments d’un tableau :

* `some()` retourne `true` si **au moins un élément** satisfait la condition.
* `every()` retourne `true` si **tous les éléments** satisfont la condition.

```javascript
const nombres = [2, 4, 6];

console.log(nombres.some(x => x > 5));   // true
console.log(nombres.every(x => x % 2 === 0)); // true
```



## find() et findIndex()

Enfin, deux méthodes permettent de rechercher un élément précis :

* `find()` retourne le **premier élément** qui correspond à la condition.
* `findIndex()` retourne l’**index** de ce premier élément.

```javascript
const nombres = [5, 12, 8, 130, 44];

console.log(nombres.find(x => x > 10));     // 12
console.log(nombres.findIndex(x => x > 10)); // 1
```

---

## À retenir

Les méthodes modernes d’itération comme `forEach`, `map`, `filter`, `reduce`, `some`, `every`, `find` ou `findIndex` permettent d’écrire du code **plus clair, plus concis et plus expressif** que les boucles classiques.
Elles s’imposent aujourd’hui comme des outils incontournables pour manipuler efficacement les tableaux en JavaScript.

---

⬅️ [Chapitre précédent : La Boucle Do...While](./d_DoWhile.md)

➡️ [Chapitre suivant : Contrôle du Flux](./f_ControleFlux.md)
