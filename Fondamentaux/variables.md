# 🧪 TP 1 : Variables & Constantes — La base de tout programmeur 🧠

## Partie 1 : 📦 "Petites boîtes, grands pouvoirs !"

**🔍 Objectifs pédagogiques :**

- Comprendre ce qu’est une variable et une constante en C#
- Savoir les déclarer et les nommer correctement
- Manipuler les types `int`, `double`, `string` et `const`
- Effectuer des opérations arithmétiques de base avec des variables

---

## 🗺️ Scénario

Tu es assistant(e) d’un·e développeur·se freelance qui gère les finances d’un petit food-truck écoresponsable 🌮🚚. Ta mission ? Écrire en C# un petit programme pour suivre son budget, ses économies, et... quelques statistiques rigolotes sur les prénoms des clients. 🧾📊

---

## 🧩 Étape 1 – Déclare tes premières variables

**💡 Mission :**
Déclare trois variables avec leur valeur initiale :

- `budgetCourses` : un montant entier (en €) alloué aux courses, exemple `450`
- `epargne` : montant en épargne, exemple `950`
- `nomClientVedette` : prénom du client du jour, exemple `"Amandine"`

**📝 Exemple attendu :**

```csharp
int budgetCourses = 450;
int epargne = 950;
string nomClientVedette = "Amandine";
```

**⚠️ Astuce :** Pense à bien **nommer** tes variables ! En C#, on utilise la _camelCase_ pour les variables. Par exemple : `nombreDeChurros`.

---

## 🔁 Étape 2 – Change le contenu des boîtes

**💡 Mission :**
Modifie les valeurs de tes variables à l’aide d’opérateurs :

- Le food-truck ajoute 100€ à son épargne après un super marché.
- Il dépense 70€ en fruits bio, à retirer du `budgetCourses`.
- Il change de client vedette : `"Loïc"`

**📝 À coder :**

```csharp
epargne += 100;
budgetCourses -= 70;
nomClientVedette = "Loïc";
```

**💬 Pause Quiz :**

> ✨ Qu’est-ce que fait la ligne `epargne += 100;` exactement ?  
> a) Elle multiplie l’épargne par 100  
> b) Elle remplace l’épargne par 100  
> c) Elle ajoute 100 à l’épargne actuelle

---

## 📊 Étape 3 – Fais quelques calculs simples

**💡 Mission :**
Effectue ces opérations pour aider à planifier :

1. Calcule combien de jours il faudra pour atteindre **5000€ d’épargne** si on ajoute **250€/jour**
2. Calcule le **budget journalier** si on répartit le `budgetCourses` actuel sur **7 jours**

**📝 Exemple attendu :**

```csharp
int joursRestants = (5000 - epargne) / 250;
double budgetParJour = budgetCourses / 7.0;
```

**💬 Remarque :** Pourquoi 7.0 et pas 7 ? Parce que le résultat peut contenir des centimes ! 💸

---

## 🔒 Étape 4 – Ne jamais changer... certaines valeurs

**💡 Mission :**
Déclare deux **constantes** :

- Le nombre de jours dans une semaine : `7`
- Le nom du food-truck : `"GreenTacos"`

Et montre qu’on ne peut **pas** les modifier. 😬

**📝 Exemple attendu :**

```csharp
const int joursSemaine = 7;
const string nomFoodTruck = "GreenTacos";

// joursSemaine = 8;  ❌ Erreur !
```

**💬 Pause Réflexion :**

> 🧠 Pourquoi est-il préférable de déclarer des constantes dans ton code, selon toi ?

---

## 🎯 Challenge Bonus : Détection de voyelles

**💡 Mission :**
Déclare une nouvelle variable `string` qui contient un mot de ton choix. Parcours chaque caractère de ce mot pour **compter les voyelles**.

**Indice :** utilise une boucle `foreach` et une condition `if`.

**📝 Exemple de squelette :**

```csharp
string mot = "Churros";
int nombreVoyelles = 0;

foreach (char c in mot.ToLower())
{
    if ("aeiouy".Contains(c))
    {
        nombreVoyelles++;
    }
}
Console.WriteLine("Il y a " + nombreVoyelles + " voyelles.");
```

---

## ✅ Livrables attendus

- Ton fichier `.cs` avec tous les exemples ci-dessus
- Réponses aux questions (Quiz & Réflexion)
- Un petit mot dans un commentaire : **Qu’as-tu trouvé facile ? Qu’est-ce qui t’a surpris ?**

---

👉 Prêt·e à passer à la suite ? Dans le prochain TP, tu vas découvrir **les types de données** plus en détail, et comment choisir le bon type selon le contexte. 🧠💡
