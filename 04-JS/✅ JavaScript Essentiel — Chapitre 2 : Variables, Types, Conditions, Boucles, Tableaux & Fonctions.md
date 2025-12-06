
---

# 🔰 **1. Les Variables : `let`, `const`, `var`**

## 📌 Introduction

Les variables sont **comme des boîtes où l’on range des informations** : nombres, textes, objets… que l’on pourra réutiliser dans le programme.

## 📌 Intérêt

* Permettent de **mémoriser des données**.
* Permettent de **réutiliser et modifier ces données** facilement.
* Comprendre leur portée évite les **bugs liés à l’utilisation dans différents blocs de code**.

## 📌 Différences

```
----------------------------------------------
|                VARIABLES JS                |
----------------------------------------------
| var   | Ancien, dangereux, à éviter        |
| let   | Modifiable, respecte les blocs     |
| const | Non modifiable, utilisé en 1er     |
----------------------------------------------
```

### Portée (scope)

```
global
│
├── { bloc }
│      ├── let     ✔ existe seulement ici
│      ├── const   ✔ existe seulement ici
│      └── var     ❌ sort du bloc ! (dangereux)
```

---

# 🔢 **2. Les Types en JavaScript**

## 📌 Introduction

Les types définissent **la nature des données** : nombre, texte, vrai/faux, liste…
Connaître les types permet d’**éviter des erreurs de calcul ou d’affichage**.

## 📌 Intérêt

* Vérifier les données avant de les manipuler.
* Choisir la bonne action selon le type de donnée.
* Préparer la transition vers des structures plus complexes (objets, tableaux…).

## 📌 Tableau des types

```
-------------------------
|       TYPES JS        |
-------------------------
| number  → 10, 3.14    |
| string  → "texte"     |
| boolean → true/false  |
| array   → [1,2,3]     |
| object  → {clé: val}  |
| null    → vide voulu  |
| undefined → pas défini|
-------------------------
```

### Exemple d’objet

```
user
 ├─ nom: "Reda"
 └─ age: 24
```

---

# 🔀 **3. Les Conditions (`if / else`)**

## 📌 Introduction

Les conditions permettent **au programme de prendre des décisions** selon les valeurs des variables.

## 📌 Intérêt

* Contrôler le flux du programme.
* Exécuter du code uniquement si certaines conditions sont remplies.
* Base de toutes les décisions en programmation.

### Schéma

```
       condition ?
       /       \
   vrai         faux
    |            |
  bloc A       bloc B
```

### Exemple

```js
if (age >= 18) {
    console.log("Majeur");
} else {
    console.log("Mineur");
}
```

---

# 🔁 **4. Switch – Choix multiples**

## 📌 Introduction

Switch est une alternative aux multiples `if…else if…`, plus lisible pour **plusieurs cas possibles**.

## 📌 Intérêt

* Lire facilement les multiples cas.
* Réduire les erreurs et simplifier le code.

### Schéma

```
switch (x)
     |
     ├─ case 1 → action
     ├─ case 2 → action
     └─ default → si aucun cas trouvé
```

---

# 🔄 **5. Les Boucles**

## 📌 Introduction

Les boucles permettent **de répéter automatiquement une action** plusieurs fois.

## 📌 Intérêt

* Éviter de réécrire plusieurs fois le même code.
* Traiter des listes ou séries de données efficacement.
* Base pour les tableaux, les objets, et la programmation dynamique.

---

### ✔ 5.1 Boucle `for`

**Quand l’utiliser ?** Quand on sait combien de fois on doit répéter.

```
INITIALISATION → CONDITION → ACTION → i++
       ↑_________________________________↓
```

```js
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

---

### ✔ 5.2 Boucle `while`

**Quand l’utiliser ?** Quand on répète **tant que la condition est vraie**.

```
     CONDITION ?
       |
      oui → exécute → retourne à condition
       |
      non → stop
```

```js
while (x < 5) {
   x++;
}
```

---

### ✔ 5.3 Boucle `do…while`

**Quand l’utiliser ?** Quand on veut **exécuter au moins une fois**, puis répéter si la condition est vraie.

```
exécute une fois →
vérifie condition →
si vrai → recommence
```

```js
do {
   console.log("Hello");
} while (x < 5);
```

---

### 🧠 Différences rapides

```
-------------------------------------------------------------
| Boucle     | Quand l'utiliser ?                           |
-------------------------------------------------------------
| for        | Nombre d’itérations connu                    |
| while      | Répéter tant que la condition est vraie      |
| do…while   | Faire au moins une fois                      |
-------------------------------------------------------------
```

---

# 📦 **6. Les Tableaux (Array) + Méthodes Essentielles**

## 📌 Introduction

Un tableau est **une liste de valeurs** que l’on peut manipuler facilement.
Chaque valeur a un **index**, permettant de l’identifier.

## 📌 Intérêt

* Stocker plusieurs données sous une seule variable.
* Faire des opérations sur toutes les valeurs rapidement.

### Représentation d'un tableau

```
fruits = ["🍎", "🍌", "🍊"]
index      0       1      2
```

---

### Méthodes importantes

#### ✔ push() — ajoute à la fin

```
AVANT : ["🍎", "🍌"]
push("🍓")
APRÈS : ["🍎", "🍌", "🍓"]
```

#### ✔ pop() — retire la fin

```
AVANT : ["🍎", "🍌", "🍓"]
pop()
APRÈS : ["🍎", "🍌"]
```

#### ✔ unshift() — ajoute au début

```
AVANT : ["🍌", "🍊"]
unshift("🍎")
APRÈS : ["🍎", "🍌", "🍊"]
```

#### ✔ shift() — retire le début

```
AVANT : ["🍎", "🍌", "🍊"]
shift()
APRÈS : ["🍌", "🍊"]
```

#### ✔ map() — transforme les éléments

```
[10,20,30] 
   ↓  ↓  ↓
[20,40,60] (multiplié par 2)
```

#### ✔ forEach() — parcourt chaque élément

```
["🍎","🍌","🍓"]
    ↓    ↓    ↓
 afficher chaque élément
```

---

# 🧩 **7. Les Fonctions**

## 📌 Introduction

Une fonction est **un bloc de code réutilisable**, qui peut recevoir des données (paramètres) et renvoyer un résultat.

## 📌 Intérêt

* Évite la duplication de code.
* Rend le programme **modulaire et lisible**.
* Base pour les projets plus complexes et l’OOP.

---

### Types de fonctions

#### ✔ Fonction classique

```
function nom() {
    code
}
```

#### ✔ Fonction fléchée (moderne)

```
const nom = () => { code }
```

#### ✔ Fonction avec paramètres

```
ENTRÉES → [x, y]
   |
   ↓
 FONCTION
   |
   ↓
 SORTIE → résultat
```

```js
const addition = (a, b) => {
    return a + b;
};
```

#### ✔ Fonction avec return

```
fonction
   |
   └── return → renvoie une valeur
```

---
