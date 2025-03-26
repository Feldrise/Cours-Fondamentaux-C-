# 🧪 TP 2 : Types de données — Bien choisir ses outils 🛠️

## Partie 2 : 🧠 "Le bon type pour la bonne info"

**🔍 Objectifs pédagogiques :**

- Identifier les types de données primitifs (`int`, `double`, `decimal`, `float`, `string`)
- Manipuler les opérations entre différents types
- Comprendre et pratiquer le transtypage
- Utiliser la concaténation de chaînes de caractères

---

## 🗺️ Scénario

Tu travailles sur un outil de gestion d’un festival de musique 🎶. Entre les billets vendus, les distances à parcourir pour chaque scène, les notes laissées par les spectateurs, et les noms des artistes, tu vas devoir manier les **types de données** comme un·e pro.

---

## 🎯 Étape 1 – Les entiers : quand ça compte tout rond

**💡 Mission :**
Déclare une variable pour chacun des éléments suivants :

- `nombreBilletsVendus` : un nombre entier (ex: 1325)
- `nombreScenes` : nombre de scènes (ex: 7)

Et effectue une addition pour connaître le total de **postes à gérer** (1 par scène + 1 par 200 billets vendus).

**📝 Exemple attendu :**

```csharp
int nombreBilletsVendus = 1325;
int nombreScenes = 7;

int nombrePostes = nombreScenes + (nombreBilletsVendus / 200);
```

---

## 💸 Étape 2 – Les décimaux : les chiffres qui comptent... vraiment !

**💡 Mission :**
Tu dois enregistrer :

- une distance (`float`) entre deux scènes : 450.75 mètres
- une note moyenne (`double`) donnée par les visiteurs : 4.67231
- un coût de location (`decimal`) d’un stand : 349.90 €

⚠️ N’oublie pas les suffixes (`F`, `D`, `M`) pour indiquer le type des nombres flottants.

**📝 À coder :**

```csharp
float distanceEntreScenes = 450.75F;
double noteMoyenne = 4.67231;
decimal coutLocation = 349.90M;
```

**💬 Pause Quiz :**

> 🎯 Quel type utiliser pour de l’argent : `float`, `double` ou `decimal` ? Et pourquoi ?

---

## 🔁 Étape 3 – Et si on mélangeait les types ?

**💡 Mission :**
Teste les cas suivants :

1. Effectue `10 / 3` en tant qu'entiers et observe le résultat.
2. Refais le calcul mais en forçant l’un des deux opérandes à être un `double`.
3. Que se passe-t-il si tu essaies de stocker le résultat d’un `double` dans un `int` ?

**📝 À coder :**

```csharp
int a = 10;
int b = 3;

int resultatEntier = a / b; // -> 3
double resultatDecimal = (double)a / b; // -> 3.3333...
int erreurDeType = (int)(a / (double)b); // forçage (cast)
```

**⚠️ Attention :** le transtypage doit être explicite pour éviter les erreurs de compilation ou les pertes de données non voulues.

---

## 💬 Étape 4 – Manipule le texte comme un pro 🎤

**💡 Mission :**
Tu gères une liste d’artistes. Crée des chaînes de caractères avec leurs noms, puis :

- Concatène-les dans une seule phrase lisible
- Ajoute un compteur de participations
- Crée une phrase du type :  
  `"L'artiste Queen a participé 4 fois au festival."`

**📝 Exemple attendu :**

```csharp
string artiste1 = "Queen";
string artiste2 = "Daft Punk";

string phrase = "Artistes en tête d’affiche : " + artiste1 + " et " + artiste2;

int participations = 4;
string recap = "L'artiste " + artiste1 + " a participé " + participations + " fois au festival.";

Console.WriteLine(phrase);
Console.WriteLine(recap);
```

**💬 Réflexion :**

> 💡 Que se passe-t-il si tu concatènes un `string` avec un `int` ? Est-ce que le compilateur râle ?

---

## 🧪 Challenge Bonus : Devine le type !

**💡 Mission :**
Testes ces lignes de code et indique ce que le compilateur va en déduire. Explique le comportement dans un commentaire.

```csharp
var moyenne = 18.5;
var nom = "FestivalZik";
var compteur;

compteur = 5; // Est-ce que ça compile ? Pourquoi ?
```

---

## ✅ Livrables attendus

- Ton fichier `.cs` avec tous les exemples codés
- Réponses aux quiz et commentaires de réflexion
- Optionnel : une fonction qui retourne un résumé du festival sous forme de texte, en combinant plusieurs types

---

👉 Bravo, tu commences à manipuler les types comme un vrai développeur C#!  
Prochaine étape ? 🧱 Apprendre à créer tes propres méthodes pour mieux structurer ton code.
