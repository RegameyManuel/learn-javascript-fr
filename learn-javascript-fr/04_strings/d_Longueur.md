---
chapter: 4
section: d
title: Longueur d’une chaîne
description: Comprendre comment obtenir la longueur d’une chaîne de caractères en JavaScript grâce à la propriété length.
---

# Longueur d’une chaîne

En JavaScript, chaque chaîne de caractères possède une propriété intégrée appelée **`length`**.  
Cette propriété retourne le nombre total de caractères contenus dans la chaîne, y compris les espaces et les symboles.

## Exemple simple

```javascript
let text = "Bonjour";
console.log(text.length); // 7
```

Dans cet exemple, le résultat est `7` car le mot `"Bonjour"` contient exactement 7 caractères.

## Les espaces comptent aussi

La propriété `length` prend en compte tous les caractères, y compris les espaces :

```javascript
let phrase = "Hello World";
console.log(phrase.length); // 11
```

Le résultat est `11` car `"Hello World"` contient 10 lettres + 1 espace.

## Exercice

1. Déclarez une variable `message` contenant la valeur `"JavaScript"`.
2. Utilisez la propriété `length` pour afficher le nombre de caractères.
3. Testez ensuite avec la chaîne `"Hello World!"` et observez la différence.

### Solution attendue

```javascript
let message = "JavaScript";
console.log(message.length); // 10

let otherMessage = "Hello World!";
console.log(otherMessage.length); // 12
```

---

## À retenir

* La propriété `length` retourne le nombre de caractères d’une chaîne.
* Elle inclut les **espaces**, les **caractères spéciaux** et la **ponctuation**.

---

⬅️ [Chapitre précédent : Remplacement de chaînes](./c_Remplacement.md)

➡️ [Chapitre suivant : Concaténation de chaînes](./e_Concatenation.md)
