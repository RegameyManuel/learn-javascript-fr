---
chapter: 12
section: a
title: La gestion des erreurs
description: Dans un programme, des erreurs surviennent inévitablement (fautes de code, saisies incorrectes, ou événements imprévisibles). Plutôt que de laisser le programme s’arrêter brutalement, il est possible de gérer ces erreurs pour assurer un fonctionnement plus robuste et offrir une meilleure expérience à l’utilisateur.
---

# La gestion des erreurs

Les erreurs font partie intégrante du développement logiciel. Un bon programme n’est pas seulement celui qui fonctionne en conditions idéales, mais aussi celui qui sait quoi faire quand les choses tournent mal. En JavaScript, gérer les erreurs permet d’éviter que tout le script ne s’arrête brutalement, et d’offrir une réponse adaptée aux situations imprévues.

## Pourquoi gérer les erreurs ?

Un programme qui gère correctement ses erreurs est plus solide et plus agréable à utiliser. Cela permet d’abord de **reprendre en douceur** lorsqu’un problème survient, au lieu de planter sans prévenir. C’est aussi une question d’**expérience utilisateur** : un message clair aide l’utilisateur à comprendre ce qui se passe, au lieu d’afficher un écran vide ou une erreur incompréhensible.  

Pour le développeur, une gestion efficace facilite le **débogage**. Les erreurs signalées au bon endroit permettent de repérer rapidement la cause du problème. Enfin, c’est une garantie de **fiabilité** : un code qui gère ses erreurs réduit les risques de blocage complet et inspire confiance.

## Les différents types d’erreurs

En JavaScript, on distingue plusieurs familles d’erreurs :  

- Les **erreurs de syntaxe**, qui surviennent lorsque le code est mal écrit et ne peut même pas être exécuté.  
- Les **erreurs d’exécution**, qui apparaissent pendant que le programme tourne, par exemple lorsqu’on essaie d’utiliser une variable qui n’existe pas.  
- Les **erreurs de logique**, plus subtiles, quand le code s’exécute sans bloquer mais ne produit pas le résultat attendu.  

## Exemples d’usage

La gestion des erreurs se rencontre dans de nombreuses situations courantes : une requête réseau qui échoue, une saisie utilisateur incorrecte, ou encore un problème rencontré dans une bibliothèque externe. Dans tous ces cas, mieux vaut prévoir une réaction adaptée qu’un arrêt brutal.

## Avantages d’une bonne gestion des erreurs

En résumé, gérer les erreurs correctement permet d’éviter l’interruption totale du programme, de donner des informations utiles pour comprendre le problème, et de maintenir une expérience fluide pour l’utilisateur. Cela contribue directement à la qualité et à la fiabilité du code.

## Bonnes pratiques

Quelques principes aident à tirer le meilleur de la gestion des erreurs. Il est recommandé d’utiliser des types d’erreurs précis quand c’est possible, de consigner les erreurs pour pouvoir les analyser, de donner des messages clairs et compréhensibles aux utilisateurs, et de traiter les erreurs au plus près de leur origine pour limiter leur propagation.

## Le bloc try...catch

L’une des techniques les plus répandues consiste à entourer un morceau de code d’un bloc `try...catch`. L’idée est simple : on essaie d’exécuter du code dans la partie `try`. Si tout se passe bien, on continue normalement. Si une erreur survient, l’exécution est interrompue et on passe dans le bloc `catch`, où l’on peut réagir sans que tout le script s’arrête.  

Ce mécanisme est détaillé dans les sections suivantes :  

- [try...catch](./b_try...-catch.md)  
- [try...catch...finally](./c_try...catch...finally.md)  

## Les erreurs asynchrones

Avec du code asynchrone, la situation se complique un peu. Les erreurs ne se produisent pas forcément au moment où le code est lancé, mais plus tard, par exemple lorsqu’une réponse arrive d’un serveur. Dans ces cas, la gestion des erreurs doit être prévue dans les rappels (*callbacks*), les promesses (*promises*) ou via `async/await`. Ces techniques sont expliquées en détail dans la suite du chapitre :  

- [La gestion asynchrone des erreurs](./d_async_errorhandling.md)

---

## À retenir

La gestion des erreurs est indispensable pour rendre un programme robuste et agréable à utiliser. Elle permet d’anticiper les imprévus, d’éviter les blocages, d’aider au débogage et de donner une meilleure expérience aux utilisateurs. En JavaScript, le bloc `try...catch` constitue l’outil de base pour intercepter et traiter ces erreurs, tandis que les opérations asynchrones nécessitent des techniques adaptées comme les promesses ou `async/await`.  

---

⬅️ [Chapitre précédent : JSON](../11_json/b_Exercices.md)

➡️ [Chapitre suivant : try...catch](./b_try...-catch.md)
