# ✨ TP Final – Partie Bonus : Enrichis ton RPG !

### 🎯 Objectifs pédagogiques

- Approfondir l'utilisation des **interfaces** et **comportements polymorphes**
- Ajouter des mécaniques de jeu avancées : objets, inventaire, effets spéciaux
- Structurer un code plus **modulaire et maintenable**
- Apprendre à équilibrer un gameplay de façon logique

---

### 🎁 Objectifs bonus (à choisir librement)

Chaque défi est indépendant. Tu peux en faire un, deux, ou plus !

---

#### 🧪 Bonus 1 – Les objets utilisables

> Ajoute des objets (potion de soin, pierre de rage, etc.) que le joueur peut utiliser pendant son tour.

**Contraintes** :

- Crée une interface `IUtilisable` avec une méthode `Utiliser(Personnage cible)`
- Crée une classe `PotionDeSoin`, `PierreDeForce`, etc.
- Le joueur peut choisir d'“utiliser un objet” lors de son tour

```csharp
interface IUtilisable
{
    void Utiliser(Personnage cible);
}
```

---

#### 🎒 Bonus 2 – L'inventaire

> Permets aux personnages d'avoir un inventaire d'objets (objets utilisables ou non).

**Pistes techniques** :

- Ajoute une `List<IUtilisable>` dans ta classe `Personnage`
- Affiche l'inventaire dans la console quand on choisit "Utiliser un objet"
- Gère les objets à usage unique ou infini

---

#### 🧙 Bonus 3 – Des effets spéciaux

> Implémente des **effets temporaires ou passifs** (brûlure, poison, bouclier magique…).

**Exemples** :

- Poison : le joueur perd 5 PV pendant 3 tours
- Bouclier : réduit les dégâts reçus pendant 1 tour

**Conseils** :

- Crée une classe `Effet` avec une durée, un type, un effet à appliquer
- Chaque personnage a une `List<EffetActif>`
- À chaque tour, tu appliques les effets actifs

---

#### 🧠 Bonus 4 – Une IA simple

> Ajoute un personnage contrôlé par l'ordinateur 🤖

**Idée** :

- Crée une classe `Bot` qui hérite de `Personnage`
- Implémente une méthode `ChoisirAction()` aléatoire ou logique

---

#### 🗺️ Bonus 5 – Une carte ou arène

> Imagine une mini-carte en ASCII avec des déplacements case par case.

```
[ ] [M] [ ] [P]
[P] = Personnage, [M] = Monstre
```

- Chaque joueur peut se déplacer ou attaquer en fonction de sa position
- Tu peux utiliser une `char[,]` ou une `List<List<char>>` pour modéliser ta grille

---

### 🏆 Challenge ultime (facultatif) – Un système de sauvegarde

> Propose une méthode pour **sauvegarder puis recharger une partie** (niveau avancé).

- Sauvegarde dans un fichier texte ou JSON (avec `System.Text.Json`)
- Lecture à la reprise pour restaurer les objets, PV, inventaire…
