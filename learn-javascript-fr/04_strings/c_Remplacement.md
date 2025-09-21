---
chapter: 4
section: c
title: Remplacement dans les chaînes
description: Apprendre à remplacer des parties d’une chaîne de caractères avec JavaScript en utilisant la méthode replace().
---

# Remplacement dans les chaînes

Il est fréquent de devoir modifier une chaîne en remplaçant un mot ou un caractère par un autre.  
En JavaScript, cette opération se fait à l’aide de la méthode **`replace()`**.


## La méthode replace()

La méthode `replace()` prend deux arguments :  
1. la **valeur à remplacer** (ou une expression régulière),  
2. la **nouvelle valeur** à insérer.  

Exemple simple :

```javascript
let text = "Bonjour monde";
let newText = text.replace("monde", "JavaScript");
console.log(newText); // Bonjour JavaScript
```


## Utilisation avec des expressions régulières

La méthode `replace()` fonctionne aussi avec les expressions régulières, ce qui permet de remplacer plusieurs occurrences à la fois.

```javascript
let phrase = "Chat, chat et encore chat.";
let newPhrase = phrase.replace(/chat/gi, "chien");
console.log(newPhrase); // Chien, chien et encore chien.
```

Dans cet exemple :

* `g` signifie *global* (remplace toutes les occurrences),
* `i` signifie *insensible à la casse* (remplace `chat`, `Chat`, etc.).


## Exercice

1. Déclarez une variable `message` avec la valeur `"Je suis triste"`.
2. Utilisez `replace()` pour remplacer `"triste"` par `"heureux"`.
3. Affichez le nouveau message.


### Solution attendue

```javascript
let message = "Je suis triste";
let newMessage = message.replace("triste", "heureux");
console.log(newMessage); // Je suis heureux
```

---

## À retenir

* La méthode `replace()` permet de remplacer une partie d’une chaîne.
* Elle accepte une **valeur simple** ou une **expression régulière**.
* Avec les regex, on peut remplacer toutes les occurrences (`g`) et ignorer la casse (`i`).

---

⬅️ [Chapitre précédent : Création de chaînes](./b_Creation.md)

➡️ [Chapitre suivant : Longueur des chaînes](./d_Longueur.md)
