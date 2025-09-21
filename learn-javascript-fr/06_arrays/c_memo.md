---
chapter: 6
section: c
title: Mémo – Méthodes des tableaux
description: Fiche de révision rapide des principales méthodes de tableaux en JavaScript.
---

# Mémo – Méthodes des tableaux

## Ajouter / Supprimer
- `push(x)` → ajoute à la fin  
- `pop()` → retire le dernier  
- `unshift(x)` → ajoute au début  
- `shift()` → retire le premier  
- `splice(start, delete, ...items)` → ajoute/supprime/remplace (modifie le tableau)  
- `slice(start, end)` → copie une partie (sans modifier)

## Fusion et conversion
- `concat(arr)` → fusionne  
- `join(sep)` → chaîne avec séparateur  
- `toString()` → convertit en chaîne  

## Parcours
- `forEach(fn)` → exécute une fonction (ne renvoie rien)  
- `map(fn)` → crée un nouveau tableau transformé  
- `filter(fn)` → garde les éléments qui respectent la condition  

## Recherche
- `find(fn)` → premier élément qui correspond  
- `findIndex(fn)` → son index  
- `includes(val)` → contient la valeur ?  
- `indexOf(val)` / `lastIndexOf(val)` → position  

## Réduction
- `reduce(fn, init)` → réduit à une valeur (de gauche à droite)  
- `reduceRight(fn, init)` → réduit de droite à gauche  

## Tri et ordre
- `sort(fn)` → trie (modifie le tableau)  
- `reverse()` → inverse (modifie le tableau)  

## Autres
- `length` → taille du tableau  
- `flat(depth)` → aplatit  
- `flatMap(fn)` → map + flat(1)  
- `fill(val, start, end)` → remplit avec une valeur  
- `copyWithin(target, start, end)` → copie une partie à un autre endroit  
- `keys()` / `values()` / `entries()` → itérateurs

---

## À retenir

- Certaines méthodes **modifient le tableau** (`push`, `pop`, `splice`, `sort`, `reverse`).  
- D’autres **retournent un nouveau tableau** (`slice`, `map`, `filter`, `concat`).  
- `reduce` et `reduceRight` permettent de **combiner** tous les éléments en une seule valeur.  
- `forEach` exécute une fonction, mais ne crée pas de tableau.  

---

⬅️ [Chapitre précédent : Méthodes des tableaux](./b_methodes.md)  
➡️ [Chapitre suivant : Exercices](./d_Exercices.md)
