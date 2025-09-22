---
chapter: 7
section: f
title: Contrôle du Flux
description: JavaScript propose des instructions comme break, continue et les labels pour modifier le comportement normal d’une boucle. Elles permettent d’interrompre, de sauter ou de réorienter l’exécution des itérations.
---

# Contrôle du Flux dans les Boucles

Une boucle suit normalement un déroulement prévisible : initialisation, condition, exécution du bloc, puis passage à l’itération suivante. Cependant, il arrive que l’on veuille interrompre ce cycle ou sauter certaines étapes. JavaScript met à disposition plusieurs instructions permettant de modifier le flux d’exécution à l’intérieur des boucles.



## L’instruction break

`break` met fin immédiatement à l’exécution d’une boucle, même si la condition de poursuite est encore vérifiée.

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    break;
  }
  console.log(i);
}
```

Dans cet exemple, la boucle s’interrompt lorsque `i` atteint 5.
Résultat affiché :

```
0
1
2
3
4
```



## L’instruction continue

`continue` permet de **passer directement à l’itération suivante**, en ignorant les instructions restantes du bloc pour le cycle en cours.

```javascript
for (let i = 0; i < 10; i++) {
  if (i % 2 === 0) {
    continue; // saute les nombres pairs
  }
  console.log(i);
}
```

Résultat affiché :

```
1
3
5
7
9
```



## Les Labels (étiquettes)

Les **labels** offrent la possibilité de donner un nom à une boucle.
Cela permet d’utiliser `break` ou `continue` sur des boucles imbriquées, afin de contrôler plus finement laquelle doit être interrompue ou sautée.

```javascript
outerLoop: for (let i = 0; i < 3; i++) {
  for (let j = 0; j < 3; j++) {
    if (i === j) {
      continue outerLoop;
    }
    console.log(`i=${i}, j=${j}`);
  }
}
```

Résultat affiché :

```
i=0, j=1
i=0, j=2
i=1, j=0
i=1, j=2
i=2, j=0
i=2, j=1
```

Bien que puissants, les labels sont rarement employés en pratique, car ils peuvent nuire à la lisibilité du code. On leur préfère généralement des structures plus claires, voire la réorganisation du programme pour éviter leur utilisation.

---

## À retenir

* `break` arrête totalement une boucle.
* `continue` passe à l’itération suivante en sautant le reste du bloc.
* Les **labels** permettent d’agir sur des boucles imbriquées, mais leur usage reste exceptionnel.

Ces instructions offrent un contrôle précis du déroulement d’une boucle, mais doivent être utilisées avec discernement pour préserver la clarté du code.

---

⬅️ [Chapitre précédent : Itérations Modernes](./e_Iterations.md)

➡️ [Chapitre suivant : Les Fonctions](../08_fonctions/a_Fonctions.md)

