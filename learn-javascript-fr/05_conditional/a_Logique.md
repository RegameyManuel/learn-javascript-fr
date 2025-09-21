---
chapter: 5
section: a
title: Logique conditionnelle
description: Introduction à la logique conditionnelle en JavaScript et rôle central des tests dans le contrôle du flux d’un programme.
---

# Logique conditionnelle

Une **condition** est un test qui détermine si une partie de code doit s’exécuter ou non. 
Les conditions sont au cœur de tous les langages de programmation, car elles permettent de contrôler le déroulement du programme en fonction de la validité de certaines données.

## Pourquoi utiliser des conditions ?

Les conditions permettent avant tout de rendre un programme **robuste et prévisible**. 
Si vous faites aveuglément confiance aux données reçues (par exemple les saisies d’un utilisateur), vos programmes risquent d’échouer ou de se comporter de manière imprévisible. 
À l’inverse, si vous mettez en place des tests systématiques, votre code gagne en fiabilité. 
Cette approche est souvent appelée **programmation défensive**.

## Un code en arbre

Les conditions permettent aussi de créer des structures de code en forme d’**arbre**.  
En fonction des résultats des tests, l’exécution peut emprunter différentes branches.  
C’est ce qui se passe, par exemple, lorsqu’un formulaire en ligne affiche un message différent selon les informations entrées par l’utilisateur.

## Exemple simple

```javascript
let age = 20;

if (age >= 18) {
  console.log("Accès autorisé");
} else {
  console.log("Accès refusé");
}
```

Dans cet exemple, deux branches sont possibles :

* si la condition `age >= 18` est vraie, on exécute le premier bloc,
* sinon, on passe au bloc `else`.

---

## À retenir

* Une **condition** est un test qui renvoie vrai ou faux.
* Les conditions permettent de contrôler l’exécution du code.
* Elles sont indispensables pour rendre un programme fiable et réactif.

---

⬅️ [Chapitre précédent : Exercices](../04_strings/f_Exercices.md)

➡️ [Chapitre suivant : If](./b_if.md)
