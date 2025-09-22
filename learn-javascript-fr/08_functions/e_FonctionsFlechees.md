---
chapter: 8
section: e
title: Les Fonctions fléchées
description: Les fonctions fléchées, introduites avec ES6, offrent une syntaxe plus concise pour définir des fonctions. Elles présentent néanmoins certaines particularités, notamment concernant la gestion de `this`.
---

# Les Fonctions fléchées

Depuis l’évolution du langage avec ES6, JavaScript propose une nouvelle manière d’écrire des fonctions : les **fonctions fléchées** (*arrow functions*). Leur nom vient du symbole `=>` qui les caractérise. Elles apportent une syntaxe plus courte et sont particulièrement adaptées aux fonctions courtes et aux callbacks.



## Syntaxe de base

La forme la plus simple consiste à écrire :

```javascript
const double = (x) => x * 2;

console.log(double(4)); // 8
```

Ici, la fonction prend un paramètre `x` et renvoie directement `x * 2`.
Il n’est pas nécessaire d’écrire le mot-clé `function`, ni même `return` lorsque l’instruction est réduite à une seule expression.



## Différences avec les fonctions classiques

Malgré leur concision, les fonctions fléchées ont un comportement différent des fonctions classiques sur plusieurs points importants :

* Elles **n’ont pas leur propre `this`** : elles conservent la valeur de `this` du contexte dans lequel elles sont créées.
* Elles n’ont pas non plus leurs propres `arguments` ou `super`.
* Elles ne peuvent pas être utilisées comme **constructeurs** (avec `new`).

Cela les rend pratiques pour certaines situations, mais inadaptées à d’autres.



## Exemple avec `this`

L’une des différences les plus marquantes se voit avec l’utilisation de `this` :

```javascript
function Compteur() {
  this.valeur = 0;

  setInterval(function() {
    this.valeur++;
    console.log(this.valeur);
  }, 1000);
}

new Compteur(); // Erreur : this ne désigne pas l'objet Compteur
```

Dans ce cas, la fonction anonyme utilisée dans `setInterval` définit son propre `this`, qui n’est pas l’objet `Compteur`.

Avec une fonction fléchée, le problème disparaît :

```javascript
function Compteur() {
  this.valeur = 0;

  setInterval(() => {
    this.valeur++;
    console.log(this.valeur);
  }, 1000);
}

new Compteur(); // Affiche 1, 2, 3...
```

Ici, la fonction fléchée reprend le `this` du contexte de création, ce qui correspond bien à l’objet `Compteur`.



## Cas d’utilisation courants

Les fonctions fléchées sont très utiles pour :

* écrire des callbacks dans des méthodes comme `map`, `filter`, `reduce`, etc.
* simplifier l’écriture de petites fonctions utilitaires.
* éviter les pièges liés à la gestion de `this` dans les fonctions classiques.

Exemple avec `map` :

```javascript
const nombres = [1, 2, 3, 4];
const doubles = nombres.map(n => n * 2);

console.log(doubles); // [2, 4, 6, 8]
```

---

## À retenir

Les **fonctions fléchées** sont une syntaxe moderne, concise et pratique.
Elles simplifient l’écriture des fonctions courtes et des callbacks, tout en évitant certains problèmes liés à `this`.
Cependant, elles ne remplacent pas totalement les fonctions classiques, car elles ne possèdent pas leur propre `this`, `arguments` ou `super`, et ne peuvent pas servir de constructeurs.

---

⬅️ [Chapitre précédent : Les Portées](./d_Portes.md)

➡️ [Chapitre suivant : Les Closures](./f_Closures.md)
