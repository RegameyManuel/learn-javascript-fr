---
chapter: 12
section: b
title: try...catch
description: Le bloc `try...catch` permet d’intercepter les erreurs d’exécution afin d’éviter que le programme ne s’arrête brutalement. On peut ainsi réagir de manière contrôlée et offrir une meilleure expérience à l’utilisateur.
---

# try...catch

Dans un programme, il arrive qu’une erreur apparaisse à l’exécution : une variable mal nommée, un calcul impossible, ou encore une ressource manquante. Si rien n’est prévu, le script s’interrompt immédiatement. Pour éviter ce comportement brutal, JavaScript propose le bloc `try...catch`.  

L’idée est simple : on place le code susceptible de poser problème dans une partie `try`. Si tout se passe bien, l’exécution continue normalement. Mais si une erreur survient, l’exécution de `try` s’arrête immédiatement et le programme bascule dans la partie `catch`. C’est là que l’on peut définir la réaction à adopter : afficher un message, ignorer l’erreur, ou encore déclencher un traitement de secours.

Voici un premier exemple :

```javascript
try {
  alert("Bienvenue dans notre programme");
  asdk; // Erreur : cette variable n’existe pas
} catch (err) {
  console.log("Une erreur est survenue");
}
```

Dans cet extrait, l’appel à `asdk` provoque une erreur. Grâce au `try...catch`, le script ne s’arrête pas complètement. Le bloc `catch` intercepte l’erreur et affiche un message dans la console.

Le bloc `catch` reçoit automatiquement un objet représentant l’erreur. Cet objet possède notamment deux propriétés utiles :

* `name`, qui indique le type d’erreur (par exemple `ReferenceError`),
* `message`, qui donne des détails sur ce qui s’est passé.

Il est aussi possible de créer et déclencher ses propres erreurs grâce au mot-clé `throw`. Cela permet, par exemple, d’imposer certaines règles dans le programme et de signaler explicitement lorsqu’elles ne sont pas respectées.

```javascript
function divide(a, b) {
  if (b === 0) {
    throw new Error("Impossible de diviser par zéro");
  }
  return a / b;
}

try {
  console.log(divide(10, 0));
} catch (err) {
  console.error(err.message);
}
```

Ici, la fonction déclenche volontairement une erreur si l’on tente de diviser par zéro. Le `try...catch` permet alors de récupérer cette erreur et d’afficher un message compréhensible.

---

## Limites

Il faut garder à l’esprit que `try...catch` n’intercepte que les erreurs d’exécution, c’est-à-dire lorsque le code est effectivement lancé. Les erreurs de syntaxe (comme un mot-clé mal écrit) empêchent le script de s’exécuter et ne peuvent pas être capturées par ce mécanisme. De plus, il fonctionne uniquement pour du code **synchrone**. Pour gérer les erreurs dans du code asynchrone, il faut utiliser les promesses (`.catch()`) ou la syntaxe `async/await`, ce qui sera abordé plus loin.

---

## À retenir

Le bloc `try...catch` permet de rendre un programme plus robuste. Il intercepte les erreurs qui surviennent pendant l’exécution, empêche l’arrêt brutal du script et donne au développeur la possibilité de réagir de manière contrôlée. C’est l’outil de base de la gestion des erreurs en JavaScript, sur lequel viennent ensuite se greffer d’autres techniques pour les cas plus avancés, comme l’asynchrone.

---

⬅️ [Chapitre précédent : La gestion des erreurs](./a_Error.md)

➡️ [Chapitre suivant : try...catch...finally](./c_try...catch...finally.md)
