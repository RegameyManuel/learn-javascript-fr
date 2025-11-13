---
chapter: 1
section: b
title: Typographie et conventions
description: Comprendre l’importance de la typographie, des espaces et des conventions dans l’écriture du code JavaScript.
---

# Typographie et conventions

Lorsque vous **apprenez à programmer**, il est essentiel de développer une certaine rigueur dans l’écriture. Comme pour un texte en français ou en anglais, la **typographie** et les **conventions d’écriture** jouent un rôle important dans la lisibilité du code.

En JavaScript (comme dans la plupart des langages), les **espaces**, les **sauts de ligne** et l’**indentation** facilitent la lecture et la compréhension.  
Un code bien structuré sera plus simple à corriger, à partager et à améliorer.

## Lire et écrire activement

Vous ne pouvez pas vous contenter de **lire rapidement** les exemples présentés.  
Il est essentiel de pratiquer une **lecture active** :

1. **Exécutez** le code donné dans les exemples.  
2. **Modifiez-le** pour voir comment il réagit.  
3. **Observez** les résultats.  

C’est ainsi que vous développerez une véritable compréhension du langage.

## Exemple

Prenons un exemple simple :

```javascript
console.log("Bonjour le monde !");
```

Cela sera probablement votre premier programme en **JS** (**javascript**), si vous avez vos bases en **HTML5** vous savez déjà que vous devrez intégrer ce **script** dans une page html. 
Le mot-clé `console.log` permet d’**afficher un texte** dans la console (vous pouvez ouvrir la console de votre navigateur à l'aide de la touche `F12`).
Ici, le texte `"Bonjour le monde !"` sera affiché à l’écran.

```javascript
// Résultat attendu :
Bonjour le monde !
```

## Mémo : Fonctions d’interaction en JavaScript

Pour vos premiers programmes, vous utiliserez souvent ces fonctions simples qui permettent **d’afficher des informations** ou **d’interagir avec l’utilisateur**.

### `console.log()`

Affiche un message dans la console du navigateur (accessible avec `F12`).  
C’est l’outil principal pour tester et déboguer vos programmes.

```javascript
console.log("Bonjour !");
```

Résultat (dans la console) :

```javascript
Bonjour !
```

### `alert()`

Affiche une **boîte de dialogue** avec un message.
L’utilisateur doit cliquer sur **OK** pour continuer.

```javascript
alert("Bienvenue dans mon programme !");
```

### `prompt()`

Affiche une boîte de dialogue avec un champ de saisie.
Permet de **demander une valeur** à l’utilisateur. La valeur saisie est retournée sous forme de **chaîne de caractères**.

```javascript
let nom = prompt("Quel est ton nom ?");
console.log("Bonjour " + nom);
```

### `confirm()`

Affiche une boîte de dialogue avec deux choix : **OK** et **Annuler**.
Renvoie `true` si l’utilisateur clique sur OK, `false` sinon.

```javascript
let reponse = confirm("Veux-tu continuer ?");
console.log(reponse);
```

-
---

## À retenir

Un langage de programmation n’est pas seulement fait pour être lu, mais surtout pour être **pratiqué**. 

- La **typographie** et les **conventions** rendent le code lisible et compréhensible.  
- Testez systématiquement les **exemples de code** que vous rencontrez.
- Écrivez toujours votre **propre version** du code pour vous l’approprier.
- `console.log()` → écrire dans la console (débogage).
- `alert()` → afficher un message bloquant.
- `prompt()` → demander une saisie à l’utilisateur.
- `confirm()` → poser une question fermée (OK/Annuler).

Ces fonctions sont très pratiques pour les **premiers pas** en JavaScript, mais dans un projet sérieux, elles sont souvent remplacées par des interactions plus avancées (formulaires, DOM, etc.).

---

⬅️ [Chapitre précédent : JavaScript](./a_JavaScript.md)

➡️ [Chapitre suivant : Les Commentaires](../02_basics/a_Commentaires.md)