# 🧠 Fiche Aide Étudiant – Langage C# : Les Fondamentaux

## 📍 Objectif du module

👉 Savoir concevoir une **solution applicative sécurisée** en utilisant les bases du langage **C#** et le framework **.NET**, en appliquant les concepts fondamentaux de la **programmation orientée objet**.

---

## 🧱 1. Les bases du langage C#

### ✅ À savoir :

- **Déclaration de variables et constantes**

  ```csharp
  int age = 25;
  const double PI = 3.14;
  ```

- **Types de données** (principaux) :

  - `int`, `double`, `bool`, `string`, `char`
  - Structures : `DateTime`, `TimeSpan`, etc.

- **Opérations de base**

  ```csharp
  int somme = a + b;
  bool estMajeur = age >= 18;
  ```

- **Structures de contrôle**

  ```csharp
  if (condition) { ... }
  else { ... }

  for (int i = 0; i < 10; i++) { ... }

  while (condition) { ... }

  switch (variable) { case 1: ...; break; }
  ```

---

## 🧰 2. Méthodes

- **Définir une méthode**

  ```csharp
  void DireBonjour(string nom) {
    Console.WriteLine("Bonjour " + nom);
  }
  ```

- **Appeler une méthode**

  ```csharp
  DireBonjour("Alice");
  ```

- **Retourner une valeur**
  ```csharp
  int Addition(int a, int b) {
    return a + b;
  }
  ```

---

## 🧱 3. Programmation Orientée Objet (POO)

### 🧩 Définir une classe

```csharp
class Voiture {
  public string Marque;
  public int Annee;

  public void Klaxonner() {
    Console.WriteLine("Bip bip !");
  }
}
```

### 🧪 Créer un objet

```csharp
Voiture v = new Voiture();
v.Marque = "Renault";
v.Klaxonner();
```

### 🔄 Constructeur

```csharp
public Voiture(string marque, int annee) {
  Marque = marque;
  Annee = annee;
}
```

---

## 🌐 4. Association de classes

Exemple : une **Voiture** contient un **Moteur**

```csharp
class Moteur {
  public int Puissance;
}

class Voiture {
  public Moteur MonMoteur;
}
```

---

## 🧪 5. Interfaces

Une interface définit un **contrat** à respecter :

```csharp
interface IDeplacable {
  void SeDeplacer();
}

class Robot : IDeplacable {
  public void SeDeplacer() {
    Console.WriteLine("Le robot avance.");
  }
}
```

---

## 🧰 6. Bibliothèque .NET

C# repose sur un **écosystème riche** :

- E/S fichiers : `System.IO`
- Dates et heures : `System.DateTime`
- Collections : `List<T>`, `Dictionary<TKey, TValue>`

---

## 💻 7. Visual Studio & Compilation

- Utilise **Visual Studio** (Community Edition gratuite).
- Fichier `.csproj` = projet C#.
- Raccourci build : `Ctrl + Maj + B`
- Exécuter : `Ctrl + F5`

---

## 🛠️ 8. Développement de composants

- Un composant C# = classe réutilisable avec des fonctionnalités bien définies.
- Bonnes pratiques : **encapsulation**, **cohésion**, **réutilisabilité**.

---

## 📌 Méthodologie & Tips

- 💡 **Toujours tester** vos méthodes indépendamment.
- 🔍 **Comprenez vos erreurs de compilation** : elles sont vos alliées !
- 👨‍🔧 **Codez régulièrement** : la pratique est la clé de la maîtrise.
