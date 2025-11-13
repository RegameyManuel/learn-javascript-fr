---
chapter: 8
section: c
title: Les Paramètres
description: Les paramètres permettent de transmettre des valeurs à une fonction. Ils peuvent avoir des valeurs par défaut, être récupérés de manière flexible grâce à l’opérateur rest, et même être déstructurés pour plus de lisibilité.
---

# Les Paramètres

Lorsqu’une fonction est définie, elle peut recevoir des informations extérieures nécessaires à son exécution. Ces informations sont appelées **paramètres** dans la déclaration de la fonction, et **arguments** lorsqu’on les fournit lors de l’appel.  

Par exemple, si l’on souhaite écrire une fonction qui salue un utilisateur, on peut définir un paramètre `nom` qui sera remplacé par la valeur fournie au moment de l’appel :

```javascript
function saluer(nom) {
  console.log("Bonjour " + nom);
}

saluer("Alice"); // Bonjour Alice
saluer("Bob");   // Bonjour Bob
```

Ici, `nom` est le paramètre de la fonction, tandis que `"Alice"` et `"Bob"` sont les arguments transmis.

## Valeurs par défaut

En JavaScript, il est possible d’assigner une valeur par défaut à un paramètre. Cette valeur sera utilisée si aucun argument n’est fourni :

```javascript
function saluer(nom = "inconnu") {
  console.log("Bonjour " + nom);
}

saluer(); // Bonjour inconnu
saluer("Claire"); // Bonjour Claire
```

Cela évite de devoir vérifier systématiquement si un argument a été passé ou non.

## Paramètres variables et opérateur rest

Certaines fonctions doivent pouvoir accepter un nombre indéfini d’arguments.

Historiquement, JavaScript proposait l’objet spécial `arguments`, mais il est désormais préférable d’utiliser l’opérateur **rest** (`...`), qui rassemble tous les arguments restants dans un tableau :

```javascript
function somme(...nombres) {
  return nombres.reduce((acc, n) => acc + n, 0);
}

console.log(somme(1, 2, 3, 4)); // 10
console.log(somme(7, 8));       // 15
```

Ainsi, la fonction `somme` peut traiter autant de valeurs qu’on le souhaite.

## Passage par valeur et par référence

Il est important de comprendre comment les arguments sont transmis :

* Les **types primitifs** (nombres, chaînes, booléens) sont passés **par valeur**. La fonction reçoit une copie, et toute modification n’affecte pas la variable originale.
* Les **objets** et **tableaux**, en revanche, sont passés **par référence**. Si la fonction modifie ces données, les changements sont visibles en dehors de la fonction.

```javascript
function modifier(tab) {
  tab.push(99);
}

let nombres = [1, 2, 3];
modifier(nombres);

console.log(nombres); // [1, 2, 3, 99]
```

## Déstructuration des paramètres

Les fonctions modernes peuvent déstructurer directement des objets ou des tableaux dans leurs paramètres. Cela rend le code plus lisible lorsqu’une fonction reçoit plusieurs propriétés.

Exemple avec un objet :

```javascript
function afficherProfil({prenom, nom}) {
  console.log(prenom + " " + nom);
}

afficherProfil({prenom: "Alice", nom: "Durand"}); // Alice Durand
```

Exemple avec un tableau :

```javascript
function afficherCoordonnees([x, y]) {
  console.log("x=" + x + ", y=" + y);
}

afficherCoordonnees([10, 20]); // x=10, y=20
```

## Bonnes pratiques

Il est conseillé d’utiliser des paramètres nommés (sous forme d’objet) lorsque la fonction doit gérer plusieurs options, surtout si certaines sont facultatives.
Les valeurs par défaut, quant à elles, permettent de simplifier le code et d’éviter les erreurs liées aux arguments manquants.

---

## À retenir

Les paramètres permettent aux fonctions de recevoir des valeurs et d’agir en conséquence.
Ils peuvent être simples, avoir des valeurs par défaut, être regroupés grâce à l’opérateur rest, ou encore être déstructurés pour plus de clarté. Comprendre leur fonctionnement est essentiel pour écrire des fonctions souples, lisibles et robustes.

---

⬅️ [Chapitre précédent : Fonctions d’ordre supérieur](./b_higher-order.md)

➡️ [Chapitre suivant : Les Portées](./d_Portee.md)
