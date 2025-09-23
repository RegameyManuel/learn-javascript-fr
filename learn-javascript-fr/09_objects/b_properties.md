---
chapter: 9
section: b
title: Les propriétés
description: Une propriété est une paire clé-valeur associée à un objet. Elle permet de représenter des caractéristiques, des attributs ou des fonctionnalités et constitue l’unité de base de la structure d’un objet en JavaScript.
---

# Les propriétés

Un objet se compose de propriétés. Chaque propriété associe un nom à une valeur, un peu comme une étiquette collée sur une boîte contenant un contenu précis. Le nom de la propriété est toujours interprété comme une chaîne de caractères, même si on l’écrit autrement dans le code. La valeur, quant à elle, peut être de n’importe quel type : un nombre, une chaîne, un autre objet, voire une fonction.

Prenons un exemple simple. Si l’on souhaite décrire le langage JavaScript, on peut créer un objet avec plusieurs propriétés :

```javascript
let language = {
  name: "JavaScript",
  isSupportedByBrowsers: true,
  createdIn: 1995,
  author: {
    firstName: "Brendan",
    lastName: "Eich"
  },
  getAuthorFullName: function () {
    return this.author.firstName + " " + this.author.lastName;
  }
};
```

Dans ce cas, l’objet `language` regroupe des informations variées : son nom, l’année de création, le fait qu’il soit supporté par les navigateurs, mais aussi un objet imbriqué représentant l’auteur. On peut même y stocker une fonction comme valeur d’une propriété, ce qui permet d’associer des comportements en plus des simples données.

L’accès à une propriété peut se faire de deux manières. La plus courante consiste à utiliser la notation par point :

```javascript
let nom = language.name;
```

Ici, la variable `nom` contient la chaîne `"JavaScript"`. L’autre manière consiste à employer la notation entre crochets :

```javascript
let nom = language["name"];
```

Les deux approches mènent au même résultat. La deuxième est utile lorsque le nom de la propriété est calculé dynamiquement ou qu’il contient des caractères spéciaux, mais elle est généralement moins lisible.

Si l’on tente d’accéder à une propriété qui n’existe pas encore, JavaScript renverra simplement la valeur `undefined`. Il est tout aussi simple d’ajouter une nouvelle propriété à un objet déjà existant :

```javascript
language.newProperty = "Nouvelle valeur";
```

À partir de ce moment, `language` possède une propriété supplémentaire. Si la propriété existait déjà, sa valeur aurait été remplacée. La notation entre crochets fonctionne également, avec le même effet :

```javascript
language["newProperty"] = "Valeur modifiée";
```

---

## À retenir

Les propriétés sont la brique fondamentale des objets en JavaScript. Elles associent un nom à une valeur, qui peut être de n’importe quel type, y compris une fonction. Elles s’ajoutent, se modifient et s’accèdent très simplement, soit par la notation pointée, soit par les crochets. C’est grâce aux propriétés que les objets deviennent de véritables structures capables de représenter aussi bien des données que des comportements.

---

⬅️ [Chapitre précédent : Les objets](./a_Objets.md)

➡️ [Chapitre suivant : La mutabilité](./c_mutable.md)

