---
chapter: 9
section: k
title: L’encapsulation
description: L’encapsulation consiste à regrouper les données et les comportements qui leur sont liés dans une même entité, tout en contrôlant l’accès à certains éléments internes. En JavaScript, elle s’exprime par la gestion des propriétés publiques et privées.
---

# L’encapsulation

L’encapsulation est l’un des grands principes de la programmation orientée objet. Elle consiste à protéger l’intégrité d’un objet en rendant certaines de ses données inaccessibles directement depuis l’extérieur. L’idée est simple : un objet doit exposer uniquement ce qui est nécessaire à son utilisation, tout en dissimulant les détails internes qui ne concernent pas le reste du programme.

En JavaScript, les objets et les classes permettent de mettre en œuvre ce principe. Les propriétés et les méthodes que l’on définit dans une classe sont, par défaut, accessibles depuis l’extérieur. Toutefois, depuis les versions récentes du langage, il est possible de créer des champs véritablement privés en les déclarant avec le préfixe `#`.

Prenons un exemple avec une classe qui gère un compte bancaire :

```javascript
class BankAccount {
  #balance;

  constructor(initialBalance) {
    this.#balance = initialBalance;
  }

  deposit(amount) {
    this.#balance += amount;
  }

  withdraw(amount) {
    if (amount <= this.#balance) {
      this.#balance -= amount;
    } else {
      console.log("Fonds insuffisants");
    }
  }

  getBalance() {
    return this.#balance;
  }
}

let account = new BankAccount(100);
account.deposit(50);
console.log(account.getBalance()); // 150
```

Ici, la propriété `#balance` est privée. Elle ne peut pas être consultée ou modifiée directement depuis l’extérieur de la classe. On est obligé de passer par les méthodes `deposit`, `withdraw` ou `getBalance`. Cela garantit que l’état du compte reste cohérent et qu’il ne peut pas être altéré de manière imprévisible.

Avant l’introduction de cette syntaxe, les développeurs avaient recours à des conventions (comme préfixer une propriété par `_`) ou à des fermetures (*closures*) pour simuler un accès privé. Ces techniques restent valides, mais l’utilisation des champs privés rend aujourd’hui l’encapsulation plus claire et plus naturelle.

L’encapsulation permet donc de séparer ce qui relève de l’interface publique d’un objet (ce que les autres parties du programme sont censées utiliser) et ce qui relève de son implémentation interne (qui doit rester dissimulée). Cette séparation rend le code plus sûr, plus robuste et plus facile à maintenir.

---

## À retenir

L’encapsulation regroupe les données et les comportements dans une même entité tout en protégeant l’accès à certains éléments internes. En JavaScript, elle s’exprime aujourd’hui à travers les champs privés (`#propriété`) et les méthodes publiques. Ce principe permet de contrôler la manière dont un objet est utilisé et d’éviter des modifications non souhaitées de son état interne.

---

⬅️ [Chapitre précédent : Le polymorphisme](./j_polymorphism.md)

➡️ [Chapitre suivant : Exercices](./l_Exercices.md)
