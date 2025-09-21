---
chapter: 3
section: e
title: Exercices - Nombres, Math et Opérateurs
description: Exercices progressifs pour pratiquer la manipulation des nombres, l’utilisation de l’objet Math et les opérateurs arithmétiques en JavaScript.
---

# Exercices récapitulatifs

Ces exercices permettent de consolider les notions vues dans ce chapitre : **nombres en JavaScript, l’objet Math, les opérateurs de base et les opérateurs avancés**.  
Ils sont organisés du plus simple au plus complexe.

---

## Exercice 1 - Les nombres
1. Crée deux variables `a = 0.1` et `b = 0.2`. Additionne-les et affiche le résultat. Explique pourquoi ce n’est pas exactement `0.3`.  
2. Déclare un nombre en binaire (`0b1011`) et affiche sa valeur en décimal.  
3. Affiche `Number.MAX_SAFE_INTEGER` puis ajoute `1` et `2`. Observe le résultat.

---

## Exercice 2 - L’objet Math
1. Utilise `Math.PI` pour calculer la circonférence d’un cercle de rayon `5`.  
   Formule : `2 * π * r`.  
2. Calcule la racine carrée de `144` avec `Math.sqrt`.  
3. Génére un nombre aléatoire compris entre 1 et 10 inclus.

---

## Exercice 3 - Opérateurs de base
1. Calcule et affiche le reste de la division de `123` par `10`.  
2. Additionne un nombre et une chaîne de caractères pour constater la concaténation.  
3. Divise `0` par `0` et observe le résultat.  
4. Convertis la chaîne `"256"` en nombre puis ajoute `10`.

---

## Exercice 4 - Opérateurs avancés
1. Évalue `2 + 3 * 4 ** 2` puis compare avec `(2 + 3) * 4 ** 2`.  
2. Déclare une variable `n = 10`.  
   - Incrémente-la deux fois.  
   - Décrémente-la une fois.  
   - Affiche sa valeur à chaque étape.  
3. Utilise un opérateur d’affectation combiné pour multiplier une variable `x = 7` par `3`.  
4. Teste l’opérateur `??` avec une variable `let nom;` puis avec `let nom = "Alice";`.

---

## Exercice 5 - Mini-problème global
Écris un petit programme qui :  
1. Déclare une variable `rayon = 10`.  
2. Calcule l’aire du cercle correspondant (π × r²).  
3. Si l’aire est supérieure à 200, affiche `"Grand cercle"`, sinon `"Petit cercle"`.  
4. Ajoute un commentaire expliquant ton raisonnement.

---

## À retenir

- Les nombres en JavaScript sont des **flottants 64 bits** avec une précision limitée.  
- L’objet `Math` propose des **constantes** (`PI`, `E`) et des **méthodes** (`sqrt`, `random`, etc.).  
- Les opérateurs arithmétiques permettent des calculs simples, mais attention à la **coercition de type** avec `+`.  
- Les opérateurs avancés (`**`, `++`, `+=`, `??`) rendent le code plus concis et expressif.  

---

⬅️ [Chapitre précédent : Opérateurs avancés](./d_Avances.md)

➡️ [Chapitre suivant : Chaînes de caractères](../04_strings/a_Chaines.md)