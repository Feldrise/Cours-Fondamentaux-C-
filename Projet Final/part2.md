# 🧪 TP Final – Partie 2 : Implémentation de ton RPG en C#

### 🎯 Objectifs pédagogiques

- Instancier des objets en C#
- Utiliser l'héritage, les classes abstraites ou interfaces
- Implémenter une boucle de jeu interactive
- Afficher des informations dans le terminal
- Gérer un jeu en tour par tour pour plusieurs joueurs

---

### 📝 Consigne générale

Tu vas commencer l'**implémentation de ton RPG** en te concentrant sur :

- La **création des personnages et de leurs objets**
- La **boucle de jeu principale** (gestion des tours)
- Les **actions possibles à chaque tour**

Tu dois rester en **ligne de commande** (pas d'interface graphique). Soigne l'affichage, c'est ce qui rendra ton jeu vivant !

---

### 🧑‍🤝‍🧑 Déroulement attendu au lancement du jeu

Voici un **exemple de rendu console** au début du jeu :

```
Bienvenue dans le RPG Terminal Quest ! 🎮

Nombre de joueurs : 2

>>> Joueur 1, choisis ton personnage :
1. Guerrier (force, attaque lourde)
2. Mage (magie, attaque à distance)
3. Voleur (vitesse, esquive)
> 2

Nom de ton personnage : Gandalf

>>> Choisis ton arme :
1. Bâton magique (Dégâts : 15)
2. Tome du feu (Dégâts : 12 + brûlure)
> 1

>>> Joueur 2, choisis ton personnage :
...
```

Une fois tous les joueurs prêts, la **boucle de combat** démarre :

```
--- Tour 1 ---
Gandalf (PV: 100) vs Ragnar (PV: 120)

>>> Gandalf, choisis ton action :
1. Attaquer
2. Utiliser un objet
3. Défendre
> 1

💥 Gandalf attaque Ragnar avec Bâton magique ! Dégâts : 15
Ragnar perd 15 PV.

>>> Ragnar, choisis ton action :
...
```

---

### 🔁 Squelette de la boucle de jeu (à compléter)

```csharp
while (!jeuTermine)
{
    foreach (var joueur in listeDesJoueurs)
    {
        Console.WriteLine($"\n--- {joueur.Nom} (PV: {joueur.PointsDeVie}) ---");
        Console.WriteLine("1. Attaquer");
        Console.WriteLine("2. Utiliser un objet");
        Console.WriteLine("3. Défendre");
        Console.Write("> ");
        string choix = Console.ReadLine();

        switch (choix)
        {
            case "1":
                joueur.Attaquer(joueurCible); // à définir
                break;
            case "2":
                joueur.UtiliserObjet(); // facultatif
                break;
            case "3":
                joueur.SeDefendre(); // à définir
                break;
            default:
                Console.WriteLine("Choix invalide.");
                break;
        }

        // Vérification des points de vie...
        if (joueurCible.PointsDeVie <= 0)
        {
            Console.WriteLine($"{joueurCible.Nom} est KO !");
            jeuTermine = true;
            break;
        }
    }
}
```

---

### 📦 Contraintes techniques

- Utiliser l'**héritage** : chaque type de personnage (Guerrier, Mage, etc.) doit hériter d'une classe `Personnage`
- Utiliser des **objets composés** (`Arme`, `Pouvoir`, etc.)
- Implémenter des **méthodes polymorphes** : `Attaquer()`, `SeDefendre()`, etc.
- Structurer le jeu pour **gérer plusieurs joueurs et plusieurs tours**

---

### 🔍 Conseils

- Gère bien les **entrées clavier** pour éviter les crashs (TryParse, switch)
- Crée une méthode `InitialiserJeu()` pour organiser les étapes de création des joueurs
- Utilise des `List<Personnage>` pour gérer les tours
- Commence simple, puis enrichis ton jeu avec des effets secondaires, un inventaire, des sorts...
