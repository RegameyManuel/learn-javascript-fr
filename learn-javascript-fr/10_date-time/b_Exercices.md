---
chapter: 10
section: b
title: Exercices sur les dates et le temps
description: Série d’exercices pratiques pour manipuler l’objet `Date` en JavaScript (création, lecture, modification, comparaison et formatage).
---

# Exercices sur les dates et le temps

Ces exercices permettent de mettre en application les notions vues sur l’objet `Date` : création d’instances, consultation et modification des valeurs, comparaison de moments, formatage et calculs temporels.

---

## Exercice 1 — Date courante

Crée un objet `Date` contenant la date et l’heure actuelles, puis affiche-le dans la console avec `toString()` et `toLocaleString()` pour comparer les formats.

---

## Exercice 2 — Date précise

Crée un objet `Date` représentant le 14 juillet 2025 à midi. Vérifie que les valeurs de jour, mois et année correspondent à ce que tu attends avec `getDate()`, `getMonth()` et `getFullYear()`.

---

## Exercice 3 — Calcul d’âge

Écris une fonction qui prend une année de naissance en paramètre et qui retourne l’âge de la personne à la date du jour. Utilise `getFullYear()` sur la date courante.

---

## Exercice 4 — Différence entre deux dates

Crée deux objets `Date` représentant le 1er janvier 2025 et le 1er janvier 2026. Calcule le nombre de jours écoulés entre ces deux dates. Indice : utilise `getTime()` pour obtenir la valeur en millisecondes.

---

## Exercice 5 — Manipulation d’horaires

Crée une date correspondant au 1er mars 2025 à 8h30.  

- Modifie-la pour qu’elle corresponde au 1er mars 2025 à 15h45 en utilisant `setHours` et `setMinutes`.  
- Affiche ensuite l’heure finale avec `toTimeString()`.

---

## Exercice 6 — Fuseau horaire

Crée une date correspondant à l’instant présent.  
Affiche la différence avec UTC en utilisant `getTimezoneOffset()`. Indique si ton fuseau horaire est en avance ou en retard par rapport à l’heure universelle.

---

## Exercice 7 — Formatage localisé

Crée un objet `Date` et affiche-le au format français (`fr-FR`) et au format anglais (`en-US`) à l’aide de `toLocaleDateString` et `toLocaleTimeString`.

---

## Exercice 8 — ISO et JSON

Crée un objet `Date` et affiche le résultat de `toISOString()` et de `toJSON()`. Compare les deux sorties et explique en quoi elles se ressemblent ou se distinguent.

---

## Exercice 9 — Minuteur simple

Écris une fonction qui prend une durée en secondes et qui calcule la date et l’heure de fin en ajoutant cette durée à la date courante. Affiche le résultat.

---

## Exercice 10 — Projet de synthèse

Conçois un petit programme qui affiche la date du jour, l’heure actuelle, l’heure dans une semaine et le nombre de jours restants avant la fin de l’année. Utilise les différentes méthodes vues (`getDate`, `getMonth`, `setDate`, `getTime`, etc.).

---

⬅️ [Chapitre précédent : Date et temps](./a_date-time.md)

➡️ [Chapitre suivant : JSON](../11_json/a_json.md)
