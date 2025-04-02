# 🧪 TP Final – Partie 1 : Modélise ton RPG orienté objet 🧙‍♂️⚔️

### 🎯 Objectifs pédagogiques

- Identifier et modéliser les éléments essentiels d'un jeu de type RPG
- Définir des classes, propriétés et méthodes pertinentes
- Utiliser les concepts d'encapsulation, d'héritage et d'association
- Préparer la structure d'un programme orienté objet en C#

---

### 📝 Consigne générale

Imagine que tu dois créer un **petit jeu de rôle (RPG) jouable dans le terminal**. Avant d'écrire la moindre ligne de code, tu dois **modéliser ton univers et ses mécaniques principales** en t'appuyant sur la programmation orientée objet.

Tu as **carte blanche sur l'univers** (fantastique, science-fiction, médiéval, absurde...), mais tu dois respecter certaines **contraintes techniques**.

---

### 🧭 Les livrables attendus

1. ✍️ **Une liste des classes que tu comptes créer**
2. 📦 **Les principales propriétés et méthodes pour chaque classe**
3. 🔄 **Les relations entre classes** (héritage, composition, association…)
4. 🧠 **Un mini diagramme de classes** (dessiné à la main ou via un outil en ligne)
5. 💬 Une **courte explication de ton gameplay** (1 paragraphe max)

---

### 💡 Quelques pistes si tu bloques :

Tu n'es pas obligé·e de suivre ces idées, mais elles peuvent t'inspirer :

- Un joueur combat des ennemis dans une arène ou un donjon
- Chaque personnage peut avoir une ou plusieurs armes
- Il existe plusieurs types d'ennemis avec des comportements différents
- Un système d'expérience ou de loot peut enrichir le gameplay
- Les combats peuvent se faire au tour par tour
- Tu peux prévoir un gestionnaire de combat (classe spéciale)

---

### 🧱 Contraintes techniques à respecter

- Tu dois utiliser **au moins 1 relation d'héritage** entre deux classes
- Tu dois prévoir **au moins 1 classe qui utilise une autre classe en composition ou association**
- Prévois des **méthodes simples** pour les actions typiques : attaquer, se défendre, utiliser un objet, etc.
- Prépare ton code pour être **jouable en ligne de commande** (pas d'interface graphique)

---

### 🚀 Bonus (facultatif, pour les plus rapides ou créatifs)

- Utilise une **interface** pour modéliser un comportement partagé (ex : ICombattant ?)
- Ajoute une notion de **carte ou de déplacement**
- Prévois une classe `Inventaire`, ou `Sort`, ou `Potion`...

---

### 🧩 Exemple très simplifié (juste pour t'aider à te projeter)

> Classes : Personnage, Monstre (abstraite), Gobelin, Dragon, Arme, Potion, CombatManager  
> Relations : Personnage possède une Arme ; Gobelin hérite de Monstre ; tous peuvent attaquer()  
> Gameplay : Le joueur affronte une série de monstres, gagne de l'XP, peut utiliser des potions.
