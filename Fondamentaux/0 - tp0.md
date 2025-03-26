# 🧪 TP 0 : Premiers pas avec .NET et Visual Studio

## Partie 0 : 🧰 "Allume ton moteur, on décolle avec .NET 🚀"

**🔍 Objectifs pédagogiques :**

- Installer et utiliser Visual Studio pour développer en C#
- Comprendre l’organisation d’un projet .NET
- Écrire son premier programme en C#
- Utiliser les méthodes de base de la classe `System.Console`
- Compiler, exécuter et corriger une application console

---

## 🗺️ Scénario

Bienvenue au Centre d’Entraînement pour Développeur·se·s en Herbe ! 🌱  
Avant de devenir un Jedi du code, il te faut apprendre à manier ton sabre : Visual Studio, .NET et le terminal.

Dans ce TP, tu vas :

- Créer ton premier projet C#
- Lancer ton tout premier programme
- Manipuler les premières **méthodes de la classe `Console`**

---

## 🧭 Étape 1 – Crée ton premier projet C# dans Visual Studio

**💡 Mission :**

1. Ouvre **Visual Studio 2022** ou plus récent.
2. Clique sur : `Créer un nouveau projet`.
3. Choisis **Application console (.NET Core ou .NET 6/7)**.
4. Appelle ton projet : `TP0_PremiersPas`.
5. Clique sur **Créer**.

**📝 Résultat attendu :** Un fichier `Program.cs` contenant du code ressemblant à ça :

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Hello, world!");
    }
}
```

> 💬 Ici, `Console.WriteLine()` est une **méthode de la classe Console**. Elle permet d'afficher du texte dans la console.

---

## 🎉 Étape 2 – Teste les méthodes de base de `Console`

**💡 Mission :**
Découvre les méthodes les plus utilisées pour interagir avec l'utilisateur et afficher des résultats dans la console.

### 🔹 `Console.WriteLine()` : affiche du texte avec retour à la ligne

### 🔹 `Console.Write()` : affiche du texte sans retour à la ligne

### 🔹 `Console.ReadLine()` : lit une ligne saisie par l’utilisateur

### 🔹 `Console.Clear()` : efface tout le contenu de la console

### 🔹 `Console.ReadKey()` : attend une touche du clavier

**📝 À coder :**

```csharp
Console.WriteLine("Bienvenue, jeune explorateur !");
Console.Write("Quel est ton prénom ? ");

string prenom = Console.ReadLine();

Console.WriteLine("Enchanté, " + prenom + " !");
Console.WriteLine("Appuie sur une touche pour continuer...");
Console.ReadKey();
```

---

## 🧼 Étape 3 – Nettoyer la console, puis afficher un message personnalisé

**💡 Mission :**
Utilise `Console.Clear()` pour vider la console après une saisie utilisateur, puis afficher un message de bienvenue dynamique.

**📝 Exemple attendu :**

```csharp
Console.Write("Quel est ton plat préféré ? ");
string plat = Console.ReadLine();

Console.Clear();

Console.WriteLine("🍽️ Mise en route du simulateur de préparation de " + plat + "...");
```

---

## 🔁 Étape 4 – Crée une interaction simple

**💡 Mission :**
Demande à l’utilisateur :

- Son prénom
- Son activité préférée
- Une durée (en minutes)

Puis affiche une petite phrase finale en combinant les trois informations.

**📝 Exemple attendu :**

```csharp
Console.Write("Ton prénom : ");
string nom = Console.ReadLine();

Console.Write("Ton activité préférée : ");
string activite = Console.ReadLine();

Console.Write("Pendant combien de minutes pratiques-tu cette activité ? ");
string duree = Console.ReadLine();

Console.WriteLine("Super " + nom + " ! Tu fais du " + activite + " pendant " + duree + " minutes. 🏆");
```

---

## 🎯 Challenge Bonus : Crée un journal météo interactif

**💡 Mission :**
Demande à l’utilisateur :

- La ville
- La température actuelle
- Son humeur

Et affiche un résumé du type :

> "À Nantes, il fait 17°C aujourd’hui. Tu es de bonne humeur 😄 !"

---

## ✅ Livrables attendus

- Fichier `Program.cs` complet
- Chaque méthode utilisée avec un petit commentaire
- Réponses à ces 2 questions :
  1. Quelle méthode `Console` as-tu trouvé la plus intuitive ?
  2. Qu’aimerais-tu ajouter comme interaction ?

---

## 🔧 En résumé : Tu as appris...

- À créer un projet console C# (.NET)
- À exécuter un programme avec Visual Studio
- À utiliser les méthodes essentielles de `Console`
- À afficher, lire, et manipuler du texte de manière interactive
