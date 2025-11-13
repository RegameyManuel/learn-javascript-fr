---
chapter: 7
section: b
title: La Boucle For
description: La boucle for est une structure de contrôle utilisée pour exécuter un bloc de code plusieurs fois, que ce soit pour un nombre d’itérations fixé ou sur un intervalle défini. C’est une instruction polyvalente, couramment employée pour parcourir des tableaux, des chaînes de caractères et d’autres objets itérables.
---

# La Boucle For

Parmi les différentes formes de boucles offertes par JavaScript, la boucle **for** est sans doute la plus connue et la plus utilisée. Elle est particulièrement adaptée lorsqu’on connaît à l’avance le nombre d’itérations à effectuer, ou lorsqu’on souhaite parcourir une structure de données de manière systématique.

La syntaxe générale d’une boucle for se présente ainsi :

```javascript
for (initialisation; condition; miseAJour) {
  // instructions à exécuter
}
```

Trois éléments la composent :

* **l’initialisation**, exécutée une seule fois au début, permet de définir la variable de contrôle ;
* **la condition**, testée avant chaque itération, détermine si la boucle doit continuer ;
* **la mise à jour**, effectuée à la fin de chaque passage, modifie la variable de contrôle pour préparer l’itération suivante.

Par exemple, pour exécuter un bloc d’instructions dix fois :

```javascript
for (let i = 0; i < 10; i++) {
  console.log("Itération numéro " + i);
}
```

Ici, la variable `i` commence à 0. Tant que `i` est strictement inférieur à 10, le bloc s’exécute, puis `i` est incrémentée de 1. La boucle se répète ainsi jusqu’à ce que la condition devienne fausse.

## Parcourir des objets et des tableaux

La boucle for dispose de variantes qui facilitent l’itération sur des collections.

### for...in

`for...in` permet de parcourir les **clés** d’un objet ou les indices d’un tableau.

```javascript
const personne = {prenom:"John", nom:"Doe", age:25};
let infos = "";

for (let cle in personne) {
  infos += personne[cle];
}

console.log(infos); // "JohnDoe25"
```

Dans le cas d’un tableau, `for...in` parcourt les indices :

```javascript
const nombres = [45, 4, 9, 16, 25];
let txt = "";

for (let i in nombres) {
  txt += nombres[i];
}

console.log(txt); // "45491625"
```

### for...of

`for...of` introduit une manière plus intuitive de parcourir directement les **valeurs** d’un objet itérable (tableaux, chaînes de caractères, ensembles, cartes, etc.).

```javascript
let langage = "JavaScript";
let resultat = "";

for (let caractere of langage) {
  resultat += caractere;
}

console.log(resultat); // "JavaScript"
```

---

## À retenir

La boucle **for** est une structure extrêmement polyvalente :
elle permet de répéter un bloc d’instructions un nombre déterminé de fois, de parcourir efficacement les tableaux et d’itérer sur les objets grâce à ses variantes `for...in` et `for...of`.

Elle constitue l’un des outils les plus pratiques et les plus utilisés du langage JavaScript.

---

⬅️ [Chapitre précédent : Les Boucles](./a_Boucles.md)

➡️ [Chapitre suivant : La Boucle While](./c_While.md)
