---
chapter: 8
section: h
title: Exercices sur les Fonctions
description: Une série d’exercices pratiques pour mettre en application les notions de fonctions en JavaScript (paramètres, fonctions d’ordre supérieur, fonctions fléchées, closures et récursion).
---

# Exercices sur les Fonctions

Les fonctions sont au cœur de JavaScript. Les exercices suivants permettent d’en explorer les différents aspects, du plus simple au plus avancé.

## Exercice 1 : Fonction simple

Écris une fonction `saluer` qui prend un nom en paramètre et affiche :  

```
Bonjour, \[nom] !
```

## Exercice 2 : Valeurs par défaut

Modifie la fonction `saluer` pour qu’elle affiche « Bonjour, invité ! » si aucun argument n’est fourni.

## Exercice 3 : Somme de plusieurs nombres

Écris une fonction `somme` qui peut additionner un nombre quelconque d’arguments en utilisant l’opérateur **rest** (`...`).

Exemple attendu :

```javascript
somme(1, 2, 3, 4); // 10
```

## Exercice 4 : Passage par référence

Écris une fonction `ajouterElement` qui prend un tableau et un nombre, puis ajoute ce nombre au tableau.
Teste la fonction et vérifie que le tableau original a bien été modifié.

## Exercice 5 : Déstructuration

Écris une fonction `afficherUtilisateur` qui prend un objet avec les propriétés `prenom` et `age`, et affiche une phrase du type :

```
Alice a 30 ans
```

## Exercice 6 : Fonction d’ordre supérieur

Crée une fonction `appliquerOperation` qui prend une fonction `operation` et un tableau de nombres, et qui retourne un nouveau tableau avec l’opération appliquée à chaque élément.
Teste avec une fonction `double` et une fonction `carre`.

## Exercice 7 : Fonction fléchée

Réécris la fonction `carre` en utilisant la syntaxe des fonctions fléchées.

## Exercice 8 : Closure simple

Crée une fonction `creerCompteur` qui retourne une fonction permettant d’incrémenter et de mémoriser un compteur.
Exemple attendu :

```javascript
let compteur = creerCompteur();
console.log(compteur()); // 1
console.log(compteur()); // 2
console.log(compteur()); // 3
```

## Exercice 9 : Variables privées avec closure

Écris une fonction `creerBanque` qui simule un compte bancaire avec trois méthodes :

* `deposer(montant)`
* `retirer(montant)`
* `consulter()`

La variable `solde` ne doit pas être accessible directement depuis l’extérieur.

## Exercice 10 : Fonction récursive

Écris une fonction récursive `factorielle(n)` qui calcule la factorielle d’un nombre entier positif.
Exemple attendu :

```
factorielle(5); // 120
```

## Exercice 11 : Parcours récursif

Écris une fonction récursive `afficherArborescence` qui affiche les propriétés d’un objet imbriqué (par exemple un profil utilisateur avec des informations de contact et d’adresse).

---

## À retenir

Ces exercices couvrent les principales notions liées aux fonctions :

* définition et paramètres,
* fonctions d’ordre supérieur,
* fonctions fléchées,
* closures,
* récursion.

La pratique régulière de ces concepts est essentielle pour acquérir des réflexes solides en JavaScript.

---

⬅️ [Chapitre précédent : Les Fonctions récursives](./g_Recursives.md)

➡️ [Chapitre suivant : Les Objets](../09_objects/a_Objets.md)
