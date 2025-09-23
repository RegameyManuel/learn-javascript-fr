---
chapter: 9
section: a
title: Les objets
description: Un objet est un type de données composé qui permet de stocker et d’organiser plusieurs valeurs sous forme de paires clé-valeur. Il s’agit d’une structure de données fondamentale en JavaScript, largement utilisée pour représenter des données complexes et des entités structurées.
---

# Les objets

En JavaScript, un objet est une entité qui regroupe des informations sous la forme de paires appelées « propriétés ». Chaque propriété associe un nom (ou clé) à une valeur. C’est une manière de décrire et d’organiser des données de façon structurée, bien plus riche que les simples types primitifs tels que les nombres, les chaînes de caractères ou les valeurs booléennes.

Une différence importante entre les objets et les types primitifs réside dans leur comportement vis-à-vis des modifications. Les valeurs primitives, comme un nombre ou une chaîne, sont immuables : chaque fois qu’on leur attribue une nouvelle valeur, une nouvelle référence est créée. Les objets, au contraire, sont mutables : lorsqu’on modifie l’une de leurs propriétés, c’est toujours le même objet qui est concerné, seule son « interne » évolue.

La création d’objets en JavaScript peut se faire de plusieurs manières. La plus directe consiste à utiliser la notation littérale, c’est-à-dire simplement une paire d’accolades. Par exemple :

```javascript
let personne = {};
```

Ici, on obtient un objet vide prêt à accueillir des propriétés. Cette méthode est considérée comme la plus simple et la plus courante.

Il est également possible de créer un objet avec le constructeur intégré `Object`. Cela revient à écrire :

```javascript
let personne = new Object();
```

Cette syntaxe est moins utilisée dans la pratique, mais elle illustre bien le fait qu’en JavaScript les objets reposent sur une logique orientée objet.

Enfin, JavaScript propose la méthode `Object.create`. Elle permet de créer un nouvel objet en indiquant explicitement quel prototype il doit utiliser comme base :

```javascript
let personne = Object.create(proto);
```

Avec cette approche, l’objet nouvellement créé hérite directement des propriétés définies dans l’objet prototype passé en paramètre. Cela ouvre la voie à une gestion fine de l’héritage par prototype, concept essentiel du langage.

---

## À retenir

Les objets sont au cœur de JavaScript. Ils permettent de regrouper des informations et de représenter des entités complexes à travers des propriétés. Contrairement aux valeurs primitives qui sont immuables, les objets sont mutables et se manipulent toujours par référence. Leur création peut se faire de manière littérale, via le constructeur `Object`, ou encore par la méthode `Object.create` qui met en avant le rôle des prototypes.

---

⬅️ [Chapitre précédent : …](../08_autre_section/derniere_page.md)

➡️ [Chapitre suivant : Les propriétés](./b_properties.md)

