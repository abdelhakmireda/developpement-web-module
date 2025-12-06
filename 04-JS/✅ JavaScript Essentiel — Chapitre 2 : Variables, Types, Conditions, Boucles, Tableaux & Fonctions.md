
---

# 🌟 **Cours JavaScript Essentiel – Chapitre Complet Avec Schématisations**

Bienvenue dans ce module qui te donne **toutes les bases solides** de JavaScript avant d’aller vers l’OOP et les projets avancés.

---

# 🔰 **1. Les Variables : let, const, var**

## 📌 Schéma comparatif

```
----------------------------------------------
|                VARIABLES JS                |
----------------------------------------------
| var   | Ancien, dangereux, à éviter        |
| let   | Modifiable, respecte les blocs     |
| const | Non modifiable, utilisé en 1er     |
----------------------------------------------
```

## 📌 Portée des variables (scope)

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

## 📌 Exemple d’objet

```
user
 ├─ nom: "Reda"
 └─ age: 24
```

---

# 🔀 **3. Les Conditions**

## 📌 Schéma du if / else

```
       condition ?
       /       \
   vrai         faux
    |            |
  bloc A       bloc B
```

### Exemple :

```js
if (age >= 18) {
    console.log("Majeur");
} else {
    console.log("Mineur");
}
```

---

# 🔁 **4. switch – Pour plusieurs cas**

## 📌 Schéma

```
switch (x)
     |
     ├─ case 1 → action
     ├─ case 2 → action
     └─ default → si aucun cas trouvé
```

---

# 🔄 **5. Les Boucles**

## ✔ 5.1 Boucle for – “Je sais combien de fois je répète”

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

## ✔ 5.2 Boucle while – “Je répète tant que la condition est vraie”

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

## ✔ 5.3 Boucle do…while – “Je fais AU MOINS une fois”

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

## 🧠 **Différences entre les boucles**

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

## 📌 Représentation d'un tableau

```
fruits = ["🍎", "🍌", "🍊"]
index      0       1      2
```

---

## ✔ push() — ajoute à la fin

```
AVANT : ["🍎", "🍌"]
push("🍓")
APRÈS : ["🍎", "🍌", "🍓"]
```

```js
fruits.push("🍓");
```

---

## ✔ pop() — retire la fin

```
AVANT : ["🍎", "🍌", "🍓"]
pop()
APRÈS : ["🍎", "🍌"]
```

---

## ✔ unshift() — ajoute au début

```
AVANT : ["🍌", "🍊"]
unshift("🍎")
APRÈS : ["🍎", "🍌", "🍊"]
```

---

## ✔ shift() — retire le début

```
AVANT : ["🍎", "🍌", "🍊"]
shift()
APRÈS : ["🍌", "🍊"]
```

---

## ✔ map() — transforme les éléments

```
[10,20,30] 
   ↓  ↓  ↓
[20,40,60] (multiplié par 2)
```

---

## ✔ forEach() — parcourt chaque élément

```
["🍎","🍌","🍓"]
    ↓    ↓    ↓
 afficher chaque élément
```

---

## 🧠 Résumé des principales fonctions d’Array

```
push()    → ajoute à la fin
pop()     → enlève la fin
shift()   → enlève le début
unshift() → ajoute au début
length    → taille du tableau
forEach() → parcourir
map()     → transformer
```

---

# 🧩 **7. Les Fonctions — Types + Schémas**

## ✔ Fonction classique

```
function nom() {
    code
}
```

---

## ✔ Fonction fléchée (moderne)

```
const nom = () => { code }
```

---

## ✔ Fonction avec paramètres

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

---

## ✔ Fonction avec return

```
fonction
   |
   └── return → renvoie une valeur
```

---
