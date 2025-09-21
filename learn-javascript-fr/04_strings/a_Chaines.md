---
chapter: 4
section: a
title: Chaînes de caractères
description: Introduction aux chaînes de caractères en JavaScript et à leur rôle central dans la manipulation de texte.
---

# Chaînes de caractères

Une **chaîne de caractères** (ou *string*) est une suite de caractères représentant du texte.  
En JavaScript, les chaînes font partie des types de données fondamentaux et sont utilisées partout : affichage de messages, saisie utilisateur, manipulation de données textuelles, etc.


## Définition d’une chaîne

On peut créer une chaîne en entourant du texte avec des guillemets simples ou doubles :  

```javascript
let str1 = "Bonjour";
let str2 = 'Salut';
```

Les deux formes sont équivalentes. Le choix dépend surtout de vos préférences et de la cohérence du projet.


## Les chaînes comme objets

En JavaScript, les chaînes sont des **valeurs primitives** de type `string`.
Il est aussi possible de créer une chaîne via le constructeur `String` :

```javascript
let strObj = new String("Bonjour");
```

Mais cette approche est déconseillée, car `strObj` n’est pas une primitive mais un **objet**, ce qui peut produire des résultats inattendus lors de comparaisons.


---

## À retenir

* Une chaîne est une valeur de type `string` utilisée pour manipuler du texte.
* On peut la définir avec `'...'` ou `"..."`.
* L’utilisation de `new String()` crée un objet et doit être évitée.

---

⬅️ [Chapitre précédent : Opérateurs Avancés](../03_numbers/e_Exercices.md)

➡️ [Chapitre suivant : Création de chaînes](./b_Creation.md)

