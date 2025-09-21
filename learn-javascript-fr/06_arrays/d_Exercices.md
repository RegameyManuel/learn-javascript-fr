---
chapter: 6
section: d
title: Exercices sur les tableaux
description: Exercices progressifs pour pratiquer la création, la manipulation et l’utilisation des méthodes des tableaux en JavaScript.
---

# Exercices – Tableaux

Ces exercices couvrent la création de tableaux, leur manipulation avec les méthodes principales, et la compréhension des différences entre méthodes mutables et immuables.



## Exercice 1 – Création simple
Crée un tableau `fruits` contenant `"pomme"`, `"banane"` et `"orange"`.  
Affiche sa longueur avec `console.log`.



## Exercice 2 – Ajout et suppression
1. Ajoute `"kiwi"` à la fin du tableau `fruits`.  
2. Supprime le premier élément.  
3. Affiche le tableau après chaque étape.



## Exercice 3 – Fusion et conversion
1. Crée un tableau `legumes = ["carotte","tomate"]`.  
2. Fusionne `fruits` et `legumes` dans un nouveau tableau `courses`.  
3. Transforme `courses` en une chaîne séparée par des tirets (`-`).  



## Exercice 4 – Parcours et transformation
1. Crée un tableau `nombres = [1,2,3,4,5]`.  
2. Utilise `forEach` pour afficher chaque nombre multiplié par 2.  
3. Utilise `map` pour créer un nouveau tableau `carres` contenant le carré de chaque nombre.



## Exercice 5 – Filtrage et recherche
1. À partir de `nombres`, crée un tableau `pairs` contenant uniquement les nombres pairs.  
2. Utilise `find` pour récupérer le premier nombre supérieur à 3.  
3. Vérifie si le tableau contient le nombre `4` avec `includes`.



## Exercice 6 – Réduction
Écris un programme qui calcule :  
1. La somme des éléments du tableau `[10, 20, 30, 40]`.  
2. Le produit des mêmes éléments.  
Astuce : utilise `reduce`.



## Exercice 7 – Tri et ordre
1. Crée un tableau `notes = [12, 5, 18, 9, 15]`.  
2. Trie les notes dans l’ordre croissant.  
3. Trie ensuite dans l’ordre décroissant.  
4. Inverse l’ordre avec `reverse`.



## Exercice 8 – Méthodes avancées
1. Crée un tableau `phrase = ["bonjour", "le", "monde"]`.  
2. Utilise `flatMap` pour obtenir un tableau de **lettres individuelles**.  
3. Crée un tableau `[1, 2, 3, 4, 5]` et remplis tous les éléments avec `0` à partir de l’index `2`.



## Exercice 9 – Cas pratique
Un tableau `panier = ["pomme","banane","pomme","orange","banane","pomme"]`.  
1. Calcule combien de fois chaque fruit apparaît (résultat attendu : `{ pomme: 3, banane: 2, orange: 1 }`).  
2. Utilise `reduce` pour y parvenir.

---

## À retenir

- Les tableaux se manipulent avec des méthodes qui **mutent** (ex: `push`, `pop`, `splice`, `sort`) ou qui créent un **nouveau tableau** (ex: `slice`, `map`, `filter`, `concat`).  
- Les méthodes de recherche (`find`, `includes`, `indexOf`) sont essentielles pour tester la présence d’éléments.  
- `reduce` permet de transformer un tableau entier en une seule valeur (somme, produit, objet, etc.).  
- Un bon usage combiné de `map`, `filter` et `reduce` rend le code concis et puissant.

---

⬅️ [Chapitre précédent : Mémo](./c_memo.md)

➡️ [Chapitre suivant : Les Boucles](../07_loops/a_Boucles.md)
