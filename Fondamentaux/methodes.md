# 🧪 TP 3 : Les Méthodes — Découpe ton code comme un chef 🍳

## Partie 3 : ✂️ "Découpons pour mieux coder !"

**🔍 Objectifs pédagogiques :**

- Comprendre l’utilité des méthodes en programmation
- Savoir déclarer et appeler une méthode
- Utiliser des méthodes avec et sans paramètres
- Retourner des valeurs depuis une méthode (`return`)
- Comprendre la portée (scope) des variables

---

## 🗺️ Scénario

Tu développes une application de suivi de santé pour des aventuriers 🧭. Elle doit calculer des statistiques utiles pour leurs expéditions : calories brûlées, hydratation nécessaire, score d’énergie… Pour éviter un code spaghetti 🍝, tu vas tout organiser grâce aux **méthodes**.

---

## 🔧 Étape 1 – Déclarer ta première méthode

**💡 Mission :**
Crée une méthode nommée `AfficherBienvenue()` qui affiche un message d’accueil dans la console. Appelle-la depuis la méthode `Main`.

**📝 Exemple attendu :**

```csharp
static void AfficherBienvenue()
{
    Console.WriteLine("Bienvenue dans l'application Aventure+ !");
}

static void Main(string[] args)
{
    AfficherBienvenue();
}
```

**📣 À retenir :**

- Le mot-clé `void` signifie que ta méthode **ne retourne rien**.
- L’appel de la méthode se fait simplement avec son nom, suivi de `()`.

---

## 🔄 Étape 2 – Une méthode qui fait un calcul

**💡 Mission :**
Crée une méthode `CalculCalories(int minutes)` qui calcule le nombre de calories brûlées en fonction du temps de marche (10 calories par minute).

Affiche ensuite le résultat depuis `Main`.

**📝 Exemple attendu :**

```csharp
static int CalculCalories(int minutes)
{
    return minutes * 10;
}

static void Main(string[] args)
{
    int calories = CalculCalories(45);
    Console.WriteLine("Calories brûlées : " + calories);
}
```

**💡 Astuce :** Le mot-clé `return` permet de **renvoyer un résultat** depuis ta méthode. La méthode doit alors **préciser le type retourné** (`int`, `double`, `string`...).

---

## 💧 Étape 3 – Méthode avec plusieurs paramètres

**💡 Mission :**
Tu dois évaluer le besoin en eau d’un aventurier :  
Créer une méthode `CalculHydratation(double poids, int duree)` qui renvoie la quantité d’eau nécessaire (en litres), selon la formule :

> `eau = poids (kg) * 0.03 * duree (en heures)`

**📝 À coder :**

```csharp
static double CalculHydratation(double poids, int duree)
{
    return poids * 0.03 * duree;
}
```

**Et dans `Main` :**

```csharp
double eauNecessaire = CalculHydratation(70, 3);
Console.WriteLine("Eau nécessaire : " + eauNecessaire + " L");
```

---

## 📦 Étape 4 – Retourne une phrase complète

**💡 Mission :**
Crée une méthode `CreerRapport(string nom, int calories, double eau)` qui retourne une phrase du type :

> "Bravo Alex ! Tu as brûlé 450 calories et bu 1.5 litres d'eau."

**📝 À coder :**

```csharp
static string CreerRapport(string nom, int calories, double eau)
{
    return "Bravo " + nom + " ! Tu as brûlé " + calories + " calories et bu " + eau + " litres d'eau.";
}
```

**Et dans `Main` :**

```csharp
string rapport = CreerRapport("Alex", 450, 1.5);
Console.WriteLine(rapport);
```

---

## 🧪 Challenge Bonus : Combine les méthodes !

**💡 Mission :**
Reprends tout depuis le début et combine :

- `AfficherBienvenue()`
- `CalculCalories()`
- `CalculHydratation()`
- `CreerRapport()`

Le tout dans un **flux de logique fluide**. Demande même à l’utilisateur son nom, son poids et la durée de l’activité !

**📝 Exemple avancé :**

```csharp
static void Main(string[] args)
{
    AfficherBienvenue();

    Console.Write("Quel est ton prénom ? ");
    string nom = Console.ReadLine();

    Console.Write("Quel est ton poids (kg) ? ");
    double poids = Convert.ToDouble(Console.ReadLine());

    Console.Write("Durée de la marche (en minutes) ? ");
    int duree = Convert.ToInt32(Console.ReadLine());

    int calories = CalculCalories(duree);
    double eau = CalculHydratation(poids, duree / 60); // Conversion en heures

    string rapport = CreerRapport(nom, calories, eau);
    Console.WriteLine(rapport);
}
```

---

## ✅ Livrables attendus

- Fichier `.cs` avec l’ensemble du code
- Chaque méthode bien commentée
- Réponses à ces 2 questions :
  1. Qu’est-ce qui t’a semblé le plus clair dans l’utilisation des méthodes ?
  2. Quelle méthode pourrais-tu améliorer, et comment ?

---

👉 Prêt·e pour la suite ? Prochain TP : les **conditions et boucles en C#** ! Tu vas bientôt créer tes propres objets 🧱🔧
