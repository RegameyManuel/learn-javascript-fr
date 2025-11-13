---
chapter: 14
section: b
title: Exercices sur les expressions régulières
description: Série d’exercices pratiques pour s’initier et se perfectionner dans l’utilisation des regex en JavaScript.
---

# Exercices sur les expressions régulières

Ces exercices permettent de mettre en pratique les concepts abordés dans le chapitre précédent : création de regex, utilisation des modificateurs, métacaractères, ensembles de caractères et méthodes comme `test` ou `exec`.

---

## Exercice 1 — Première correspondance

Crée une regex qui vérifie si une chaîne contient le mot « JavaScript ». Teste-la sur plusieurs phrases avec `test()`.

---

## Exercice 2 — Recherche insensible à la casse

Écris une regex qui reconnaît le mot « chat » quel que soit son cas (`Chat`, `CHAT`, `cHaT`). Vérifie-la sur plusieurs exemples.

---

## Exercice 3 — Recherche globale

À l’aide du modificateur `g`, trouve toutes les occurrences de la lettre « e » dans la phrase :  
`"Les expressions régulières sont puissantes"`. Utilise `exec` ou `match`.

---

## Exercice 4 — Validation d’un nombre

Écris une regex qui vérifie si une chaîne contient uniquement des chiffres. Teste-la avec `"12345"` (valide) et `"12a45"` (non valide).

---

## Exercice 5 — Validation d’un mot de passe

Écris une regex qui exige :  

- au moins une majuscule,  
- au moins une minuscule,  
- au moins un chiffre,  
- et une longueur minimale de 8 caractères.  

Teste-la sur plusieurs exemples de mots de passe.

---

## Exercice 6 — Extraction d’emails

À partir de la phrase :  
`"Contactez-nous à info@example.com ou support@test.org"`,  
écris une regex pour extraire toutes les adresses e-mail.

---

## Exercice 7 — Numéros de téléphone

Écris une regex qui reconnaît des numéros au format français simple : `06 12 34 56 78` ou `0612345678`. Teste-la sur différents cas.

---

## Exercice 8 — Début et fin de mot

Écris une regex qui reconnaît les mots commençant par « pro ». Teste-la sur la phrase :  
`"programmation, projet, amateur, productif"`.

---

## Exercice 9 — Remplacement

Dans la phrase :  
`"J’aime le JavaScript et le javascript me plaît"`,  
utilise une regex avec `replace` pour uniformiser et remplacer tous les cas par « JavaScript ».

---

## Exercice 10 — Projet de synthèse

Crée un mini-validateur de formulaire avec des regex :  

- une regex pour l’adresse e-mail,  
- une regex pour le mot de passe (comme à l’exercice 5),  
- une regex pour un code postal français (5 chiffres).  
  Écris un petit script qui teste ces trois champs et affiche s’ils sont valides ou non.

---

⬅️ [Chapitre précédent : Expressions régulières](./a_regular-expression.md)

<!-- ➡️ [Chapitre suivant : …](./c_autre_section.md) -->
