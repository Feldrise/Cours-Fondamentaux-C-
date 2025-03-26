# 🧪 TP 4 : Conditions & Boucles — Le cerveau de ton programme 🧠🔁

## Partie 4 : 🤖 "Et si ? Et tant que ? Et pour chaque…"

**🔍 Objectifs pédagogiques :**

- Maîtriser les structures conditionnelles `if`, `else if`, `else`, `switch`
- Utiliser les boucles `while`, `for`, `foreach` pour répéter des actions
- Comprendre l’importance des structures de contrôle dans la logique applicative
- Savoir manipuler une collection (`tableaux`, `List`) avec des boucles

---

## 🗺️ Scénario

Tu développes un mini assistant virtuel de **survie en milieu hostile** 🌲🔥🐻. Il doit s’adapter à la météo, prévoir des alertes et gérer un inventaire (sac à dos). Il faudra penser à tout : analyser, répéter, réagir.

---

## 🧭 Étape 1 – Décider avec `if / else`

**💡 Mission :**
Tu veux afficher un message différent selon la température extérieure :

- Moins de 0° → "Attention : risques de gel ! 🥶"
- Entre 0° et 25° → "Température idéale pour explorer 🌤️"
- Plus de 25° → "Hydrate-toi ! Il fait chaud ☀️"

**📝 À coder :**

```csharp
int temperature = 18;

if (temperature < 0)
{
    Console.WriteLine("Attention : risques de gel ! 🥶");
}
else if (temperature <= 25)
{
    Console.WriteLine("Température idéale pour explorer 🌤️");
}
else
{
    Console.WriteLine("Hydrate-toi ! Il fait chaud ☀️");
}
```

---

## 🎒 Étape 2 – Liste des objets : `foreach` au rapport

**💡 Mission :**
Tu as un sac à dos contenant plusieurs objets. Tu veux tous les afficher proprement.

**📝 À coder :**

```csharp
string[] sacADos = { "Couteau", "Lampe", "Boussole", "Barres énergétiques" };

foreach (string objet in sacADos)
{
    Console.WriteLine("- " + objet);
}
```

**💬 Pause Réflexion :**

> Quelle différence avec une boucle `for` classique ? Dans quel cas `foreach` est-elle plus pratique ?

---

## 🕵️ Étape 3 – Analyser du texte avec une boucle `for`

**💡 Mission :**
Tu veux analyser une chaîne de caractères (`string`) pour compter combien de fois la lettre `e` apparaît dans un message.

**📝 Exemple attendu :**

```csharp
string message = "Explorer demande de l’endurance et de l’équipement.";
int compteurE = 0;

for (int i = 0; i < message.Length; i++)
{
    if (message[i] == 'e' || message[i] == 'E')
    {
        compteurE++;
    }
}

Console.WriteLine("Nombre de lettres 'e' : " + compteurE);
```

---

## 🔁 Étape 4 – Boucle `while` pour survivre

**💡 Mission :**
Tu dois simuler une réserve d’eau. Tant qu’elle est au-dessus de zéro, tu peux continuer ta randonnée. Tu bois 0.5L à chaque étape.

**📝 À coder :**

```csharp
double eau = 2.5;
int etapes = 0;

while (eau > 0)
{
    eau -= 0.5;
    etapes++;
    Console.WriteLine("Étape " + etapes + " : encore " + eau + " L d’eau.");
}
Console.WriteLine("Plus d'eau ! Demi-tour 🚨");
```

---

## 🎯 Étape 5 – Bonus avec `switch`

**💡 Mission :**
Tu veux afficher une action selon la météo du jour (ex : "pluie", "soleil", "neige", etc.).

**📝 Exemple :**

```csharp
string meteo = "neige";

switch (meteo.ToLower())
{
    case "pluie":
        Console.WriteLine("Pense au poncho de survie 🌧️");
        break;
    case "soleil":
        Console.WriteLine("N'oublie pas ta casquette 🧢");
        break;
    case "neige":
        Console.WriteLine("Equipe-toi de raquettes ❄️");
        break;
    default:
        Console.WriteLine("Conditions inconnues... prudence !");
        break;
}
```

---

## 🧪 Challenge Bonus : mini jeu interactif

**💡 Mission :**
Demande à l’utilisateur une commande (type : `"manger"`, `"dormir"`, `"explorer"`) et affiche une réponse adaptée. Continue tant qu’il ne tape pas `"quitter"`.

**📝 Squelette proposé :**

```csharp
string commande = "";

while (commande != "quitter")
{
    Console.Write("Que veux-tu faire ? ");
    commande = Console.ReadLine();

    switch (commande)
    {
        case "manger":
            Console.WriteLine("Tu manges une ration de survie.");
            break;
        case "dormir":
            Console.WriteLine("Tu installes une tente et te reposes.");
            break;
        case "explorer":
            Console.WriteLine("Tu pars en expédition vers le nord.");
            break;
        case "quitter":
            Console.WriteLine("Fermeture du journal de bord.");
            break;
        default:
            Console.WriteLine("Commande inconnue.");
            break;
    }
}
```

---

## ✅ Livrables attendus

- Code complet dans un fichier `.cs`
- Chaque boucle et condition commentée
- Réponses à ces 2 questions :
  1. Quelle structure de contrôle préfères-tu, et pourquoi ?
  2. Quelle situation réelle pourrais-tu modéliser avec une boucle `while` ?
