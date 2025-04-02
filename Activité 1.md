# Travaux Pratiques : _Numériser le monde – Explorer les objets du quotidien_

## Partie 1 : Bienvenue dans ObjetLand

---

### Objectifs

- Découvrir les bases de la modélisation en programmation sans écrire de code.
- Apprendre à décrire un objet avec ses caractéristiques et ses actions.
- Comprendre comment les objets peuvent interagir entre eux dans un système.
- Se préparer mentalement à la programmation orientée objet en C#.

---

## 🧭 Mise en situation : Numériser le monde

Imaginez que vous travaillez pour une startup innovante appelée **"ObjetLand Inc."**, dont la mission est de **numériser tous les objets du monde réel** afin de les intégrer dans une simulation numérique. 🌍🔌

Mais pour numériser ces objets, vous devez **les décrire précisément**, comme si vous alliez les faire vivre dans un monde numérique : il faut expliquer **ce qu’ils sont**, **ce qu’ils savent faire** et **comment ils réagissent à leur environnement**.

Vous allez, en équipe, choisir un objet réel ou imaginaire, puis le **décrire comme si vous le donniez à un programmeur** qui devra le recréer virtuellement.

---

## 🧪 Étapes

### 🔹 Étape 1 : Choisissez votre objet

En binôme ou trinôme, choisissez **un objet du quotidien ou totalement inventé**, par exemple :

- Un aspirateur robot
- Une montre connectée
- Un distributeur de bonbons intelligent
- Un dragon de compagnie télécommandé 🐉
- Une théière qui parle…

Il doit être **"actif"**, c’est-à-dire pouvoir **faire des choses** (pas juste une cuillère 😄).

---

### 🔹 Étape 2 : Décrivez votre objet

Sur une fiche ou un support numérique :

#### a. **Description de l’objet**

- Donnez-lui un **nom**
- Imaginez qu’il existe en plusieurs exemplaires : **qu’est-ce qui les différencie ?**  
  _(ex : leur couleur, leur niveau de batterie, leur nom personnalisé...)_

#### b. **Ce que l’objet "sait" sur lui-même**

- Listez ses **caractéristiques** importantes :  
  _(ex : température actuelle, état allumé/éteint, batterie restante, etc.)_

#### c. **Ce que l’objet peut "faire"**

- Décrivez ses **actions** possibles :  
  _(ex : se déplacer, s’allumer, parler, arroser une plante...)_

💡 Ne vous limitez pas à la réalité : soyez créatifs ! Un grille-pain peut devenir lanceur de tartines 😁

---

### 🔹 Étape 3 : Mise en commun et débat d’explorateurs

Chaque groupe **présente son objet** rapidement (2 minutes). Pendant que les autres écoutent, ils doivent réfléchir aux questions suivantes :

- Combien d’objets différents pourrait-on créer à partir de cette description ?
- Si je voulais le reprogrammer, qu’est-ce que je dois absolument connaître ?
- En quoi cet objet ressemble-t-il à d’autres ? Pourrait-on en faire une famille ? (ex : objets connectés)

🤔 Ces questions **vous amènent doucement vers les bases de la pensée orientée objet**, sans qu’on utilise encore ces mots compliqués…

---

### 🔹 Étape 4 : Faites interagir vos objets !

Maintenant que votre objet est bien défini, imaginez qu’il **interagit avec l’objet d’un autre groupe** :

- Que se passe-t-il quand ils se croisent ?
- Comment se parlent-ils ?
- Que déclenche l’un chez l’autre ?

👾 Bonus "Object Battle" :

> Si vos objets devaient **entrer en duel**, quels seraient leurs atouts ? leurs points faibles ?  
> Imaginez une petite "fiche de combat" ou une mise en scène : qui attaque ? qui se protège ? qui se soigne ?

💬 Cela vous aidera à penser aux **relations entre objets**, qui sont essentielles en programmation orientée objet.

---

### 🔹 Étape 5 : Intervention du formateur - “Et maintenant, voyons ce que ça donne en code…”

Le formateur va vous montrer **comment une machine peut comprendre ce que vous venez de faire**.

Sur grand écran, nous allons traduire l’un de vos objets en **langage de programmation C#**.  
Pas de panique : on ne vous demandera pas encore de coder, mais simplement de reconnaître :

- Le nom de l’objet (🔸 classe)
- Ce qu’il sait faire (🔹 méthodes)
- Ses caractéristiques (🔸 propriétés)
- Et comment on crée un exemplaire de cet objet (🧱 instance)

Exemple simple :

```csharp
public class RobotAspirateur
{
    public string Nom;
    public bool EstAllume;

    public void Demarrer() { /* code... */ }
    public void Nettoyer() { /* code... */ }
    public void RetournerBase() { /* code... */ }
}
```

🤯 Et là, magie : vous verrez que **vous avez déjà fait le plus dur**, sans même écrire une ligne de code !

---

## 🎉 Conclusion

👏 Félicitations ! Vous venez de :

- Plonger dans le monde des **objets programmables**.
- Réfléchir comme des **modélisateurs de systèmes numériques**.
- Préparer votre cerveau à **penser comme un développeur orienté objet**.
