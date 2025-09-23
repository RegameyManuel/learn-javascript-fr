---
chapter: 9
section: c
title: La mutabilité
description: La mutabilité désigne la capacité d’un objet à être modifié après sa création, contrairement à l’immutabilité qui implique qu’un changement produit une nouvelle valeur sans altérer l’original. Cette distinction est essentielle en JavaScript pour comprendre la différence entre objets et valeurs primitives.
---

# La mutabilité

En JavaScript, il est fondamental de distinguer les types de données immuables des types mutables. Les valeurs primitives, comme les nombres, les chaînes de caractères ou les booléens, appartiennent à la première catégorie. Elles ne peuvent pas être modifiées une fois créées. Chaque réaffectation entraîne en réalité la création d’une nouvelle valeur en mémoire, la variable pointant désormais vers cette nouvelle référence.

Prenons l’exemple suivant :

```javascript
let myPrimitive = "première valeur";
myPrimitive = "autre valeur";
```

La variable `myPrimitive` ne contient plus la première chaîne mais une autre. L’ancienne valeur existe toujours quelque part en mémoire, mais elle n’est plus accessible par cette variable. On dit donc que les chaînes sont immuables.

Les objets, en revanche, sont mutables. Cela signifie qu’une fois créés, ils peuvent évoluer en conservant la même identité. Si l’on crée un objet et que l’on modifie l’une de ses propriétés, l’objet demeure le même, mais son contenu change.

```javascript
let myObject = { key: "première valeur" };
myObject.key = "autre valeur";
```

Dans cet exemple, l’objet `myObject` reste le même, mais sa propriété `key` a été réécrite. C’est cette souplesse qui rend les objets si puissants en JavaScript, car ils peuvent être enrichis ou modifiés au fil de l’exécution du programme.

Il est également possible d’ajouter de nouvelles propriétés à la volée ou d’en supprimer certaines. La syntaxe reste très simple :

```javascript
let object = {};
object.foo = "bar";        // Ajout d’une propriété
object["baz"] = "qux";     // Ajout avec notation par crochets
object.foo = "quux";       // Modification de la propriété existante
delete object.baz;         // Suppression d’une propriété
```

Ces opérations illustrent parfaitement la mutabilité des objets : leur état interne peut être continuellement adapté aux besoins du programme, contrairement aux valeurs primitives qui restent figées.

---

## À retenir

La mutabilité est une caractéristique clé des objets en JavaScript. Alors que les valeurs primitives sont immuables et créent une nouvelle référence lorsqu’elles changent, les objets conservent leur identité et autorisent l’ajout, la suppression ou la modification de propriétés. Cette distinction explique pourquoi les objets sont si largement utilisés pour représenter des structures complexes et dynamiques.

---

⬅️ [Chapitre précédent : Les propriétés](./b_properties.md)

➡️ [Chapitre suivant : Les références](./d_reference.md)
