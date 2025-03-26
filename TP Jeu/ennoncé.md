# 🧪 TP Final – Mini-Jeu Console : **"Devine le Nombre !"**

## 🎮 Concept du jeu

Le joueur doit deviner un nombre secret choisi aléatoirement par l’ordinateur. À chaque tentative, le programme l’informe s’il est trop haut, trop bas, ou correct. Le joueur a un nombre limité d’essais selon la difficulté choisie.

Tu vas implémenter plusieurs **fonctionnalités progressives**, structurées autour des notions clés vues dans les TP précédents.

---

## 🎯 Objectifs pédagogiques

- Structurer une application console avec des **méthodes**
- Utiliser les **types** de données appropriés (`int`, `string`, `bool`)
- Contrôler le **flux d’exécution** avec des **conditions** et des **boucles**
- Prendre en main des **valeurs aléatoires** (`Random`)
- Mettre en place un **système de niveaux de difficulté**

---

# 🎮 Partie 1 : Lancement du jeu

## 🔧 Étape 1 – Démarrage et message de bienvenue

**💡 Mission :**
Crée une méthode `AfficherBienvenue()` qui :

- Affiche un titre du jeu
- Explique brièvement les règles

**📝 Exemple d’output :**

```
============================
     DEVINE LE NOMBRE !
============================

Le but ? Deviner le nombre secret.
À chaque essai, je te dirai si c’est trop haut ou trop bas.
Bonne chance ! 🍀
```

---

# 🧱 Partie 2 : Choix de la difficulté

## 🎚️ Étape 2 – Proposer trois niveaux

| Difficulté | Plage de valeurs | Tentatives |
| ---------- | ---------------- | ---------- |
| Facile     | 1 à 20           | 10         |
| Moyen      | 1 à 50           | 7          |
| Difficile  | 1 à 100          | 5          |

**💡 Mission :**
Crée une méthode `ChoisirDifficulte()` qui retourne un objet ou une structure avec :

- `min`
- `max`
- `tentativesMax`

**💬 Exemple d’output attendu :**

```
Choisis ta difficulté (facile, moyen, difficile) : difficile
> Très bien ! Tu dois deviner un nombre entre 1 et 100. Tu as 5 essais.
```

---

# 🔄 Partie 3 : La boucle de jeu

## 🕹️ Étape 3 – Deviner le nombre

1. Génère un nombre aléatoire (`Random`)
2. Boucle tant que le joueur a des essais restants :
   - Demande un nombre
   - Compare avec le nombre secret
   - Affiche un indice
3. Si c’est gagné, félicite-le !
4. Sinon, affiche le nombre correct à la fin

**📌 Méthodes suggérées :**

- `DemanderNombre(int min, int max)` → `int`
- `ComparerNombre(int secret, int tentative)` → `string` ("trop haut", "trop bas", "bravo")

---

## 🔢 Exemple d’output (niveau moyen) :

```
Essai 1/7 – Entre un nombre entre 1 et 50 : 25
Trop bas !

Essai 2/7 – Ton choix : 40
Trop haut...

Essai 3/7 – Ton choix : 33
Bravo ! Tu as deviné le nombre secret en 3 essais ! 🎉
```

Ou, en cas d’échec :

```
Tu as épuisé tous tes essais. 😢 Le nombre secret était : 42.
```

---

# 🧪 Partie 4 : Bonus & amélioration

## 💡 Défis bonus

### 🔁 Rejouer ?

À la fin de la partie, proposer de rejouer (`o/n`) :

```csharp
bool Rejouer()
{
    Console.Write("Veux-tu rejouer ? (o/n) : ");
    return Console.ReadLine().ToLower() == "o";
}
```

### 🧠 Système de score

Attribuer des points en fonction du niveau de difficulté + nombre d’essais utilisés :

- **Facile** : 1 point
- **Moyen** : 2 points
- **Difficile** : 3 points
- Bonus si trouvé en 1 seul coup : +5 pts

Affiche un résumé à la fin.

---

# ✅ Livrables attendus

- Un fichier `Program.cs` structuré avec :
  - Au moins 3 méthodes : `AfficherBienvenue()`, `ChoisirDifficulte()`, `LancerPartie()`
  - Bonne utilisation des `if`, `while`, `switch` ou `for`
  - Lecture d’entrée utilisateur (`Console.ReadLine()`)
  - Affichages dynamiques (`Console.WriteLine()`)

---

## 🧠 En synthèse, ce TP mobilise :

| Notions C#                       | Appliquées ? |
| -------------------------------- | ------------ |
| Variables & constantes           | ✅           |
| Types (`int`, `string`, `bool`)  | ✅           |
| Méthodes                         | ✅           |
| Conditions `if`, `else`          | ✅           |
| Boucles `while`, `for`           | ✅           |
| Lecture/écriture console         | ✅           |
| Génération de nombres aléatoires | ✅           |
