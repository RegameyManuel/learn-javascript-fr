---
chapter: 7
section: g
title: Exercices sur les Boucles
description: Exercices pratiques pour consolider l’apprentissage des boucles en JavaScript. Ils couvrent les boucles for, while, do...while, for...in, for...of, ainsi que les méthodes modernes d’itération et le contrôle du flux.
---

# Exercices sur les Boucles

Les boucles constituent un outil essentiel du langage JavaScript. Pour bien les maîtriser, rien ne vaut la pratique. Les exercices suivants te permettront d’explorer leurs différentes formes et de comprendre leurs usages concrets.

## Exercice 1 : Les bases de la boucle for

Écris un programme qui affiche les nombres de 1 à 10 à l’aide d’une boucle `for`.  
Puis modifie-le pour n’afficher que les nombres pairs.

## Exercice 2 : Compter avec while

Utilise une boucle `while` pour afficher les multiples de 3 inférieurs à 30.  
Attention à ne pas tomber dans une boucle infinie !

## Exercice 3 : Au moins une fois avec do...while

Écris un programme qui demande à l’utilisateur un nombre grâce à `prompt()`.  
La boucle doit se répéter **tant que le nombre est inférieur à 10**, mais elle doit s’exécuter au moins une fois, même si l’utilisateur entre directement une valeur supérieure.

## Exercice 4 : Parcourir un objet

Déclare un objet représentant une personne avec son prénom, son nom et son âge.  
Parcours ses propriétés à l’aide d’une boucle `for...in` pour afficher toutes les valeurs dans la console.

## Exercice 5 : Les lettres d’un mot

Écris une boucle `for...of` qui parcourt la chaîne `"JavaScript"` et affiche chaque caractère sur une nouvelle ligne.

## Exercice 6 : forEach et map

Crée un tableau de nombres `[2, 4, 6, 8]`.  

- Avec `forEach`, affiche chaque nombre multiplié par 3.  
- Avec `map`, construis un nouveau tableau contenant les carrés de ces nombres.

## Exercice 7 : filter et reduce

À partir du tableau `[5, 12, 18, 7, 3, 25]` :  

- Utilise `filter()` pour obtenir uniquement les nombres supérieurs à 10.  
- Utilise `reduce()` pour calculer la somme des valeurs filtrées.

## Exercice 8 : break et continue

Écris une boucle `for` qui parcourt les nombres de 1 à 20.  

- Si le nombre est divisible par 7, la boucle doit s’arrêter (`break`).  
- Si le nombre est pair, il ne doit pas être affiché (`continue`).

## Exercice 9 : Tables de multiplication en HTML

Crée un programme qui génère automatiquement une **table de multiplication** de 1 à 10 à l’intérieur d’un tableau HTML.

Le rendu attendu dans la page doit ressembler à ceci :

| ×      | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  |
| ------ | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **1**  | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  |
| **2**  | 2   | 4   | 6   | 8   | 10  | 12  | 14  | 16  | 18  | 20  |
| **3**  | 3   | 6   | 9   | 12  | 15  | 18  | 21  | 24  | 27  | 30  |
| ...    | …   | …   | …   | …   | …   | …   | …   | …   | …   | …   |
| **10** | 10  | 20  | 30  | 40  | 50  | 60  | 70  | 80  | 90  | 100 |

### Indications

1. Utilise une boucle `for` extérieure pour générer chaque **ligne** (`<tr>`).  
2. À l’intérieur, une boucle `for` intérieure générera chaque **colonne** (`<td>`).  
3. Affiche le tableau dans le `body` grâce à `document.write()` ou, mieux encore, en créant dynamiquement des éléments avec `document.createElement()`.

## Exercice 10 : Challenge final

Crée un tableau de prénoms.  
Ton programme doit :  

1. Utiliser `map()` pour transformer tous les prénoms en majuscules.  
2. Utiliser `filter()` pour ne garder que ceux qui contiennent la lettre `"A"`.  
3. Utiliser une boucle `for...of` pour afficher les résultats restants un par un.

---

## À retenir

Ces exercices illustrent la richesse des boucles en JavaScript.  
Elles permettent non seulement de répéter des instructions, mais aussi de manipuler des données de façon expressive et efficace.  
La pratique régulière te donnera les bons réflexes pour choisir la forme la plus adaptée selon le problème rencontré.

---

⬅️ [Chapitre précédent : Contrôle du Flux](./f_controls.md)  

➡️ [Chapitre suivant : Les Fonctions](../08_fonctions/a_Fonctions.md)
