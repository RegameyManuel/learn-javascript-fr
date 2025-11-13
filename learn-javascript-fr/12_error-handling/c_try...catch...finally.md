---
chapter: 12
section: c
title: try...catch...finally
description: Le bloc `try...catch...finally` permet de gérer les erreurs tout en garantissant qu’un morceau de code sera exécuté dans tous les cas, qu’une erreur survienne ou non.
---

# try...catch...finally

Le bloc `try...catch` permet déjà d’intercepter des erreurs et d’éviter que le programme ne s’arrête brutalement. Mais il existe un mécanisme supplémentaire qui renforce encore cette logique : le mot-clé `finally`.  

Un bloc `finally` contient du code qui sera exécuté dans **tous les cas** : que le code du `try` réussisse sans problème ou qu’il échoue et passe dans le `catch`. Cela permet, par exemple, d’assurer la libération de ressources, la fermeture d’une connexion ou l’affichage d’un message final, peu importe le scénario.  

Voici la syntaxe générale :

```javascript
try {
  // Code à exécuter
} catch (err) {
  // Gestion des erreurs
} finally {
  // Code toujours exécuté
}
```

Prenons un petit exemple :

```javascript
try {
  alert("Bloc try exécuté");
} catch (err) {
  alert("Bloc catch exécuté");
} finally {
  alert("Bloc finally exécuté");
}
```

Dans ce cas précis, aucun problème ne survient dans le `try`, donc `catch` est ignoré. Mais le `finally` est tout de même exécuté, garantissant que certaines actions se déroulent toujours.

---

## Exemple pratique

Le `finally` prend tout son sens lorsqu’il s’agit d’assurer un nettoyage ou une étape de conclusion.

```javascript
function divideNumbers(a, b) {
  try {
    if (b === 0) {
      throw new Error("Impossible de diviser par zéro");
    }
    return a / b;
  } catch (error) {
    console.error("Une erreur est survenue :", error.message);
  } finally {
    console.log("Fin de l’exécution de la fonction");
  }
}

let result = divideNumbers(10, 2);  // Affiche : 5 puis "Fin de l’exécution de la fonction"
let result2 = divideNumbers(10, 0); // Affiche : "Une erreur est survenue : Impossible de diviser par zéro" puis "Fin de l’exécution de la fonction"
```

Dans les deux cas, le message « Fin de l’exécution de la fonction » s’affiche, preuve que le bloc `finally` est inévitablement exécuté, qu’il y ait eu une erreur ou non.

---

## À retenir

Le bloc `try...catch...finally` offre un outil puissant pour combiner la gestion des erreurs et l’exécution garantie d’un code de conclusion.

* Le `try` contient le code principal.
* Le `catch` s’exécute seulement si une erreur survient.
* Le `finally` s’exécute toujours, qu’il y ait une erreur ou non.

C’est le moyen le plus sûr de garantir que certaines actions, comme la fermeture d’un fichier ou la libération d’une ressource, se produisent dans tous les cas.

---

⬅️ [Chapitre précédent : try...catch](./b_try...-catch.md)

➡️ [Chapitre suivant : La gestion des erreurs asynchrones](./d_async_errorhandling.md)
