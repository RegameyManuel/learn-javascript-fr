---
chapter: 10
section: a
title: Date et temps
description: L’objet `Date` permet de manipuler les dates et le temps en JavaScript. Il fournit de nombreuses méthodes pour consulter, modifier et afficher les informations temporelles, en tenant compte du fuseau horaire du système.
---

# Date et temps

JavaScript propose un objet intégré, appelé `Date`, qui sert à représenter des moments dans le temps. Cet objet permet aussi bien de créer une date que de la manipuler ou de l’afficher sous différents formats. Lorsqu’on utilise un objet `Date`, le langage s’appuie sur le fuseau horaire du système ou du navigateur pour déterminer la représentation textuelle par défaut.

La manière la plus simple de créer un objet date est d’écrire :

```javascript
let now = new Date();
```

Dans ce cas, `now` contient la date et l’heure courantes. Mais il est aussi possible de fournir des paramètres au constructeur pour définir un moment précis. Par exemple :

```javascript
let christmas = new Date(2025, 11, 25);
```

Ici, la date correspond au 25 décembre 2025. Attention toutefois : les mois sont numérotés de 0 à 11, janvier valant 0 et décembre 11. Si l’on dépasse ces valeurs, JavaScript ajuste automatiquement l’année suivante ou précédente.

On peut également utiliser une chaîne de caractères ou encore un nombre représentant le nombre de millisecondes écoulées depuis le 1er janvier 1970 (l’« époque Unix »). Ces différentes syntaxes donnent une grande souplesse pour instancier des objets `Date`.

Une fois la date créée, de nombreuses méthodes permettent de consulter ou de modifier ses valeurs. Par exemple, `getFullYear()` retourne l’année complète, `getMonth()` donne le mois (de 0 à 11), `getDate()` fournit le jour du mois et `getDay()` indique le jour de la semaine (de 0 pour dimanche à 6 pour samedi). Pour les heures, minutes et secondes, on dispose de `getHours()`, `getMinutes()` et `getSeconds()`. Chacune de ces méthodes possède également une version UTC, comme `getUTCFullYear()` ou `getUTCHours()`, qui se basent sur le temps universel plutôt que sur le fuseau local.

Il est tout aussi possible de modifier les valeurs avec des méthodes équivalentes commençant par `set`. Ainsi, `setFullYear(2030)` change l’année, `setMonth(0)` fixe le mois à janvier, et `setDate(1)` définit le premier jour du mois. Ces méthodes permettent de recalculer dynamiquement des moments précis.

Enfin, l’objet `Date` offre plusieurs moyens de transformer une date en texte. La méthode `toString()` fournit une représentation générique, tandis que `toDateString()` affiche uniquement la partie calendrier et `toTimeString()` se limite à l’heure. Pour des usages plus universels, on privilégiera `toISOString()`, qui renvoie la date au format ISO standard, ou encore `toLocaleDateString()` et `toLocaleTimeString()`, qui adaptent la présentation en fonction de la langue et des conventions locales.

---

## Méthodes et propriétés de l’objet `Date`

| Nom                    | Description                                                                                   |
| ---------------------- | --------------------------------------------------------------------------------------------- |
| `constructor`          | Renvoie la fonction qui a créé le prototype de l’objet Date                                   |
| `getDate()`            | Renvoie le jour (1-31) du mois en cours                                                       |
| `getDay()`             | Renvoie le jour (0-6) de la semaine                                                           |
| `getFullYear()`        | Renvoie l’année sur 4 chiffres                                                                |
| `getHours()`           | Renvoie l’heure (0-23)                                                                        |
| `getMilliseconds()`    | Renvoie les millisecondes (0-999)                                                             |
| `getMinutes()`         | Renvoie les minutes (0-59)                                                                    |
| `getMonth()`           | Renvoie le mois (0-11)                                                                        |
| `getSeconds()`         | Renvoie les secondes (0-59)                                                                   |
| `getTime()`            | Renvoie le nombre de millisecondes depuis le 1er janvier 1970                                 |
| `getTimezoneOffset()`  | Renvoie l’écart en minutes avec le fuseau horaire UTC                                         |
| `getUTCDate()`         | Renvoie le jour (1-31) du mois en UTC                                                         |
| `getUTCDay()`          | Renvoie le jour (0-6) de la semaine en UTC                                                    |
| `getUTCFullYear()`     | Renvoie l’année sur 4 chiffres en UTC                                                         |
| `getUTCHours()`        | Renvoie l’heure (0-23) en UTC                                                                 |
| `getUTCMilliseconds()` | Renvoie les millisecondes (0-999) en UTC                                                      |
| `getUTCMinutes()`      | Renvoie les minutes (0-59) en UTC                                                             |
| `getUTCMonth()`        | Renvoie le mois (0-11) en UTC                                                                 |
| `getUTCSeconds()`      | Renvoie les secondes (0-59) en UTC                                                            |
| `now()`                | Renvoie le nombre de millisecondes écoulées depuis le 1er janvier 1970                        |
| `parse()`              | Transforme une date sous forme de chaîne en millisecondes écoulées depuis le 1er janvier 1970 |
| `prototype`            | Permet d’ajouter des propriétés ou méthodes au prototype de `Date`                            |
| `setDate()`            | Définit le jour du mois                                                                       |
| `setFullYear()`        | Définit l’année                                                                               |
| `setHours()`           | Définit l’heure                                                                               |
| `setMilliseconds()`    | Définit les millisecondes                                                                     |
| `setMinutes()`         | Définit les minutes                                                                           |
| `setMonth()`           | Définit le mois                                                                               |
| `setSeconds()`         | Définit les secondes                                                                          |
| `setTime()`            | Définit la date complète à partir d’un nombre de millisecondes                                |
| `setUTCDate()`         | Définit le jour du mois en UTC                                                                |
| `setUTCFullYear()`     | Définit l’année en UTC                                                                        |
| `setUTCHours()`        | Définit l’heure en UTC                                                                        |
| `setUTCMilliseconds()` | Définit les millisecondes en UTC                                                              |
| `setUTCMinutes()`      | Définit les minutes en UTC                                                                    |
| `setUTCMonth()`        | Définit le mois en UTC                                                                        |
| `setUTCSeconds()`      | Définit les secondes en UTC                                                                   |
| `toDateString()`       | Renvoie la date sous forme lisible                                                            |
| `toISOString()`        | Renvoie la date au format ISO                                                                 |
| `toJSON()`             | Renvoie la date au format JSON                                                                |
| `toLocaleDateString()` | Renvoie la date formatée selon la locale                                                      |
| `toLocaleTimeString()` | Renvoie l’heure formatée selon la locale                                                      |
| `toLocaleString()`     | Renvoie la date et l’heure formatées selon la locale                                          |
| `toString()`           | Renvoie une chaîne représentant l’objet Date                                                  |
| `toTimeString()`       | Renvoie uniquement la partie temps sous forme lisible                                         |
| `toUTCString()`        | Renvoie la date au format UTC                                                                 |
| `toTemporalInstant()`  | Convertit en `Temporal.Instant` (précision nanosecondes, UTC)                                 |
| `valueOf()`            | Renvoie la valeur primitive de l’objet Date                                                   |

---

## À retenir

L’objet `Date` est la solution native de JavaScript pour travailler avec les dates et les heures. On peut l’instancier avec la date courante, un moment précis ou un nombre de millisecondes depuis 1970. Il dispose d’un riche ensemble de méthodes pour lire ou modifier les valeurs, ainsi que pour produire des représentations textuelles adaptées à différents contextes. Le tableau ci-dessus constitue une référence utile pour se repérer parmi ces nombreuses possibilités.

---

⬅️ [Chapitre précédent : …](../09_objets/l_Exercices.md)

➡️ [Chapitre suivant : …](./b_Exercices.md)

