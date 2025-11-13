---
chapter: 11
section: a
title: JSON
description: Le JSON (JavaScript Object Notation) est un format léger d’échange de données, largement utilisé pour transmettre et stocker des informations dans le développement web.
---

# JSON

Le **JSON** (JavaScript Object Notation) est un format textuel simple et universel pour représenter des données. Conçu à l’origine à partir de la syntaxe des objets JavaScript, il s’est imposé comme un standard pour l’échange d’informations entre systèmes et plateformes, notamment dans le développement web. Son principal atout est d’être lisible aussi bien par des humains que par des machines, tout en restant léger.

En JavaScript, il est très facile de convertir un objet en JSON, puis de faire l’opération inverse. Par exemple :

```javascript
// Un objet JavaScript
let myObj = { name: "Ryan", age: 30, city: "Austin" };

// Conversion en JSON
let myJSON = JSON.stringify(myObj);
console.log(myJSON);
// Résultat : '{"name":"Ryan","age":30,"city":"Austin"}'

// Conversion inverse en objet JavaScript
let originalJSON = JSON.parse(myJSON);
console.log(originalJSON);
// Résultat : { name: 'Ryan', age: 30, city: 'Austin' }
```

Deux méthodes principales sont disponibles sur l’objet `JSON` :

| Méthode       | Description                                                          |
| ------------- | -------------------------------------------------------------------- |
| `parse()`     | Analyse une chaîne JSON et retourne l’objet JavaScript correspondant |
| `stringify()` | Convertit un objet JavaScript en une chaîne au format JSON           |

Le JSON prend en charge un ensemble limité mais suffisant de types de données :

* des chaînes de caractères,
* des nombres,
* des tableaux,
* des booléens,
* l’objet (c’est-à-dire une collection clé-valeur),
* et la valeur spéciale `null`.

En revanche, certains éléments courants en JavaScript ne sont pas pris en charge. C’est le cas des fonctions, des dates ou de la valeur `undefined`. Ces données doivent être transformées ou représentées autrement avant de pouvoir être intégrées dans un document JSON.

Grâce à sa simplicité et à sa compatibilité avec la plupart des langages, JSON est devenu incontournable dans les échanges de données sur le web : on le retrouve dans les API, le stockage local des navigateurs, ou encore les fichiers de configuration.

---

## À retenir

Le JSON est un format textuel standard qui permet de représenter des données de manière légère et universelle. En JavaScript, on utilise `JSON.stringify` pour convertir un objet en JSON et `JSON.parse` pour faire l’inverse. Ce format accepte les types simples comme les chaînes, les nombres, les tableaux, les booléens, les objets et `null`, mais il ne prend pas en charge les fonctions, les dates ou `undefined`.

---

⬅️ [Chapitre précédent : Date et temps](../10_date-time/b_Exercices.md)

➡️ [Chapitre suivant : Exercices](./b_Exercices.md)
