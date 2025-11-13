---
chapter: 12
section: d
title: La gestion des erreurs asynchrones
description: Les erreurs dans le code asynchrone sont plus difficiles à gérer, car elles ne se produisent pas immédiatement. JavaScript propose plusieurs techniques, comme les promesses et `async/await`, pour les intercepter et réagir correctement.
---

# La gestion des erreurs asynchrones

Dans le cas du code synchrone, une erreur se produit au moment même où l’instruction est exécutée. Le bloc `try...catch` suffit alors pour l’intercepter. Mais les choses se compliquent avec le code asynchrone : les erreurs n’apparaissent pas forcément au moment du déclenchement, mais plus tard, quand une opération différée se termine.  

Prenons un exemple courant : une requête vers un serveur. On envoie la demande maintenant, mais la réponse n’arrivera que dans quelques instants. Si cette réponse contient une erreur, elle se produit en dehors du flot d’exécution immédiat. Il faut donc des mécanismes spécifiques pour les capturer.

## Les promesses et `.catch()`

En JavaScript moderne, une grande partie du code asynchrone repose sur les promesses. Lorsqu’une promesse échoue, elle se « rejette » avec une erreur. Pour la gérer, il suffit d’ajouter un `.catch()` à la chaîne.  

```javascript
fetch("https://api.example.com/data")
  .then(response => {
    if (!response.ok) {
      throw new Error(`Erreur HTTP ! statut : ${response.status}`);
    }
    return response.json();
  })
  .then(data => {
    console.log("Données reçues :", data);
  })
  .catch(error => {
    console.error("Erreur lors de la récupération :", error);
  });
```

Dans cet exemple, si le serveur renvoie un code d’erreur, le rejet de la promesse sera capturé par le `.catch()`, qui affiche alors un message approprié.

## La syntaxe `async/await` et `try...catch`

La syntaxe `async/await` rend le code asynchrone plus lisible, en lui donnant l’apparence d’un code synchrone. Elle permet également d’utiliser `try...catch` pour intercepter les erreurs.

```javascript
async function fetchData(url) {
  try {
    let response = await fetch(url);
    if (!response.ok) {
      throw new Error(`Erreur HTTP ! statut : ${response.status}`);
    }
    let data = await response.json();
    return data;
  } catch (error) {
    console.error("Erreur lors de la récupération :", error);
  }
}
```

Ici, si une erreur survient pendant l’appel ou la conversion en JSON, elle est interceptée par le bloc `catch`. Le flux d’exécution reste donc maîtrisé.

## Bonnes pratiques

Gérer les erreurs asynchrones demande quelques habitudes supplémentaires :

* **Toujours prévoir un traitement d’erreur** : ne laissez pas une promesse sans `.catch()`.
* **Offrir un comportement de secours** : quand une opération échoue, on peut renvoyer des données par défaut ou un message compréhensible pour l’utilisateur.
* **Consigner les erreurs** : en plus de les afficher, il est souvent utile de les enregistrer dans un service de suivi pour comprendre ce qui se passe en production.
* **Éviter les échecs silencieux** : ne jamais ignorer une erreur sans la gérer ou au minimum l’afficher.
* **Centraliser la gestion** : dans les applications complexes, il peut être judicieux de regrouper le traitement des erreurs pour garder une cohérence.

---

## À retenir

Les erreurs asynchrones ne peuvent pas être interceptées par un simple `try...catch` appliqué au code synchrone. Elles apparaissent plus tard, une fois l’opération terminée. Pour les gérer, JavaScript propose deux approches principales :

* utiliser le `.catch()` des promesses,
* ou bien combiner `async/await` avec `try...catch`.

Une gestion attentive et cohérente des erreurs asynchrones est essentielle pour construire des applications robustes et fiables.

---

⬅️ [Chapitre précédent : try...catch...finally](./c_try...catch...finally.md)

➡️ [Chapitre suivant : …](./e_Exercices.md)
