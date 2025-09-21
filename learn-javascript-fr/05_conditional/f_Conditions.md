---
chapter: 5
section: f
title: Opérateurs logiques
description: Apprendre à combiner plusieurs conditions en JavaScript avec les opérateurs logiques AND (&&) et OR (||).
---

# Opérateurs logiques

Il est souvent nécessaire de tester plusieurs conditions en même temps.  
Pour cela, JavaScript propose deux opérateurs logiques :  

- **`&&`** (*AND*) : toutes les conditions doivent être vraies,  
- **`||`** (*OR*) : au moins une des conditions doit être vraie.  


## Exemple avec AND (&&)

Imaginons que vous vouliez tester si une valeur `x` est comprise entre 10 et 20.  
On combine alors deux sous-conditions avec `&&` :

```javascript
if (x > 10 && x < 20) {
  console.log("x est compris entre 10 et 20");
}
```

Ici, les deux comparaisons doivent être vraies pour que le bloc soit exécuté.


## Exemple avec OR (||)

Si vous voulez vous assurer que la variable `country` est égale à `"Angleterre"` ou `"Allemagne"`, vous pouvez écrire :

```javascript
if (country === "Angleterre" || country === "Allemagne") {
  console.log("Le pays est reconnu");
}
```

Le bloc s’exécute si **au moins une** des conditions est remplie.


## Priorité avec les parenthèses

Comme pour les opérations mathématiques, on peut utiliser des parenthèses pour définir l’ordre d’évaluation.

Exemple :

```javascript
if ((name === "John" || name === "Jennifer") && country === "France") {
  console.log("Nom et pays valides");
}
```

Dans ce cas, la vérification du `name` est effectuée en premier, puis combinée avec la condition sur `country`.

---

## À retenir

* `&&` signifie *ET* logique : toutes les conditions doivent être vraies.
* `||` signifie *OU* logique : au moins une condition doit être vraie.
* Les parenthèses permettent de clarifier et prioriser les conditions.

---

⬅️ [Chapitre précédent : Comparaison](./e_Comparaison.md)

➡️ [Chapitre suivant : Exercices](./g_Exercices.md)

