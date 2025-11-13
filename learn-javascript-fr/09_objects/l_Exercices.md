---
chapter: 9
section: l
title: Exercices
description: Série d’exercices pratiques pour mettre en application les notions d’objets, de propriétés, de mutabilité, de références, de prototypes, de classes et des principes de la programmation orientée objet en JavaScript.
---

# Exercices sur les objets et la POO en JavaScript

Ces exercices permettent de consolider les connaissances acquises dans les sections précédentes, depuis la création d’objets jusqu’aux concepts avancés de classes, d’héritage, de polymorphisme et d’encapsulation.  

---

## Exercice 1 — Création d’objet

Crée un objet représentant un livre avec les propriétés suivantes : `title`, `author`, `year`. Ajoute ensuite une méthode qui retourne une chaîne de caractères du type :  
« *Titre* a été écrit par *Auteur* en *Année* ».

---

## Exercice 2 — Manipulation de propriétés

À partir de l’objet précédent, ajoute une nouvelle propriété `publisher`. Modifie ensuite la valeur de `year` et supprime la propriété `publisher`. Vérifie les changements avec des affichages dans la console.

---

## Exercice 3 — Mutabilité

Explique, à l’aide d’un petit programme, pourquoi deux variables peuvent sembler « partager » le même objet. Montre qu’une modification via une variable se répercute sur l’autre.

---

## Exercice 4 — Références

Crée un objet `car` puis affecte-le à une seconde variable. Modifie une propriété via la première variable et vérifie le résultat sur la seconde. Ajoute ensuite un exemple de copie indépendante avec `Object.assign` ou l’opérateur de déstructuration.

---

## Exercice 5 — Prototype

Crée un objet `person` avec une méthode `introduce`. Crée ensuite un objet `student` avec `Object.create(person)` et donne-lui une propriété spécifique. Montre comment `student` peut utiliser la méthode de son prototype.

---

## Exercice 6 — Delete

Crée un objet `user` avec une propriété `password`. Supprime cette propriété avec `delete` et montre que la valeur n’est plus accessible.

---

## Exercice 7 — Énumération

Crée un objet `inventory` représentant des articles et leurs quantités. Utilise une boucle `for...in` pour afficher toutes les propriétés, puis refais la même chose avec `Object.keys`.

---

## Exercice 8 — Classes

Définis une classe `Rectangle` avec un constructeur prenant largeur et hauteur, et une méthode `area` qui calcule la surface. Crée plusieurs instances et affiche leurs résultats.

---

## Exercice 9 — Héritage

Définis une classe `Animal` avec une méthode `speak`. Crée ensuite deux sous-classes, `Dog` et `Cat`, qui redéfinissent la méthode. Instancie plusieurs objets et montre leur comportement polymorphe.

---

## Exercice 10 — Polymorphisme

Crée une liste d’objets de type `Animal`, `Dog` et `Cat`. Parcours cette liste et appelle la méthode `speak` sur chacun. Observe le résultat et explique le principe de polymorphisme.

---

## Exercice 11 — Encapsulation

Crée une classe `BankAccount` avec une propriété privée `#balance`, des méthodes `deposit`, `withdraw` et `getBalance`. Teste plusieurs scénarios en respectant la logique métier et vérifie que l’accès direct à `#balance` est impossible depuis l’extérieur.

---

## Exercice 12 — Projet de synthèse

Conçois un petit système de gestion de bibliothèque :

- une classe `Book` avec un titre et un auteur,
- une classe `Library` qui contient une collection de livres et des méthodes pour ajouter, supprimer et lister les ouvrages,
- un exemple d’utilisation complet avec plusieurs instances.

---

⬅️ [Chapitre précédent : L’encapsulation](./k_encapsulation.md)

➡️ [Chapitre suivant : Date and Time](../10_date-time/a_date-time.md)
