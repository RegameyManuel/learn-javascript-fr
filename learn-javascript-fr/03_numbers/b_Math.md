---
chapter: 3
section: b
title: Math
description: L'objet Math permet d'effectuer des opérations mathématiques en JavaScript. C'est un objet statique qui ne possède pas de constructeur. Cela signifie qu'il est possible d'utiliser les méthodes de l'objet Math sans l'instancier au préalable.
---

# Math

L’objet `Math` est intégré à JavaScript et sert à effectuer des opérations mathématiques. C’est un objet **statique** : cela signifie qu’il n’est pas nécessaire de créer une instance avec `new`. Toutes ses propriétés et méthodes sont accessibles directement par son nom. On écrit par exemple `Math.propriété` ou `Math.méthode(argument)`.

## Les constantes de Math

Certaines propriétés de `Math` fournissent des constantes numériques utiles.  

```javascript
console.log(Math.E);      // nombre d'Euler ≈ 2.718
console.log(Math.PI);     // nombre π ≈ 3.14159
console.log(Math.SQRT2);  // racine carrée de 2
console.log(Math.SQRT1_2);// racine carrée de 1/2
console.log(Math.LN2);    // logarithme naturel de 2
console.log(Math.LN10);   // logarithme naturel de 10
console.log(Math.LOG2E);  // log base 2 de e
console.log(Math.LOG10E); // log base 10 de e
```

Ces constantes évitent de réécrire manuellement des valeurs approximatives et garantissent la précision des calculs.

## Les méthodes de base

En plus des constantes, `Math` propose de nombreuses méthodes pour manipuler les nombres. Voici quelques exemples fondamentaux :

```javascript
console.log(Math.pow(8, 2));   // 64 (puissance)
console.log(Math.round(4.6));  // 5 (arrondi au plus proche)
console.log(Math.ceil(4.2));   // 5 (arrondi vers le haut)
console.log(Math.floor(4.9));  // 4 (arrondi vers le bas)
console.log(Math.trunc(4.9));  // 4 (partie entière)
console.log(Math.sign(-4));    // -1 (signe négatif)
console.log(Math.sqrt(64));    // 8 (racine carrée)
console.log(Math.abs(-4.7));   // 4.7 (valeur absolue)
```

Ces méthodes sont parmi les plus utilisées au quotidien. Elles couvrent déjà une large partie des besoins courants en développement web.

## Fonctions trigonométriques

JavaScript gère également les fonctions trigonométriques. Il faut noter que toutes les valeurs sont exprimées en **radians**, et non en degrés. Pour convertir des degrés en radians, on multiplie par `Math.PI / 180`.

```javascript
console.log(Math.sin(90 * Math.PI / 180)); // 1 (sinus de 90°)
console.log(Math.cos(0 * Math.PI / 180));  // 1 (cosinus de 0°)
```

Ces fonctions sont utiles notamment pour des animations, de la géométrie ou de la manipulation de graphiques.

## Minimum, maximum et aléatoire

L’objet `Math` permet aussi de déterminer rapidement une valeur minimale ou maximale dans une série de nombres, ainsi que de générer des valeurs aléatoires.

```javascript
console.log(Math.min(0, 150, 30, 20, -8, -200)); // -200
console.log(Math.max(0, 150, 30, 20, -8, -200)); // 150

console.log(Math.random()); // nombre pseudo-aléatoire entre 0 et 1
```

Il faut retenir que `Math.random()` retourne toujours un nombre compris entre 0 inclus et 1 exclus. Pour obtenir un nombre dans une autre plage, on multiplie et ajuste le résultat.

Exemple :

```javascript
// Nombre entier aléatoire entre 1 et 10
let alea = Math.floor(Math.random() * 10) + 1;
console.log(alea);
```

## Autres méthodes disponibles

L’objet `Math` contient encore bien d’autres méthodes : exponentielles (`Math.exp`), logarithmes (`Math.log`, `Math.log2`, `Math.log10`), racine cubique (`Math.cbrt`), fonctions hyperboliques (`Math.sinh`, `Math.cosh`, etc.).

Il n’est pas nécessaire de toutes les retenir immédiatement. L’important est de connaître les plus fréquentes et de savoir que les autres existent pour pouvoir les retrouver dans la documentation officielle.


---

## À retenir

En JavaScript, l’objet `Math` fournit à la fois des **constantes** (`Math.PI`, `Math.E`, etc.) et des **méthodes** (`Math.sqrt`, `Math.round`, `Math.random`, etc.) pour effectuer des calculs.
C’est un objet **statique** : on l’utilise directement sans créer d’instance.
Il couvre les besoins courants en arrondis, puissances, trigonométrie et génération de nombres aléatoires.

---

⬅️ [Chapitre précédent : Nombres](./a_Nombres.md)

➡️ [Chapitre suivant : Opérateurs de base](./c_Operateurs.md)
