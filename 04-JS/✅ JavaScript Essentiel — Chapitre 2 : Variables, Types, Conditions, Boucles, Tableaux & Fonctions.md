
---

# 🎓 **Chapitre 1 : Les Bases du JavaScript (Version Complète & Explicative + Schémas)**

---

# 1️⃣ **Déclaration des variables : `var`, `let`, `const`**

## ✔️ À quoi ça sert ?

Les variables servent à **mémoriser des informations** pour pouvoir les réutiliser plus tard.

## ✔️ Différences : `var` vs `let` vs `const`

### 🔹 `var`

* Ancienne manière.
* Portée **globale** ou **fonction** → dangereux.
* Peut être redéclaré.

### 🔹 `let`

* Moderne.
* Portée **bloc { }**.
* Peut changer de valeur mais pas être redéclaré dans le même bloc.

### 🔹 `const`

* Pour les valeurs **qui ne changent pas**.

### 📘 **Schéma de portée**

```
{
   let x = 10     // existe seulement ici
   const y = 20   // existe seulement ici
}
var z = 30        // existe partout dans le script
```

---

# 2️⃣ **Les types de données**

## ✔️ Pourquoi connaître les types ?

Pour vérifier la nature des données manipulées (nombre, texte, liste…), et éviter des bugs.

## ✔️ Types principaux :

| Type      | Exemple       | Description          |
| --------- | ------------- | -------------------- |
| number    | 10, 3.14      | nombres              |
| string    | "Hello"       | texte                |
| boolean   | true/false    | vrai ou faux         |
| array     | [1,2,3]       | liste organisée      |
| object    | {name:"Reda"} | données complexes    |
| null      | null          | vide volontaire      |
| undefined | undefined     | variable non définie |

### 📘 Schéma simple

```
let age = 25       → number
let name = "Reda"  → string
let isOk = true    → boolean
let notes = [12,14,18] → array
let user = {id:1, name:"Yasmine"} → object
```

---

# 3️⃣ **Les conditions (if / else)**

## ✔️ À quoi ça sert ?

À **prendre une décision** dans le programme.

### Exemple :

```
if (age >= 18) {
   console.log("Majeur");
} else {
   console.log("Mineur");
}
```

### 📘 **Schéma du flux**

```
     age >= 18 ?
           |
   ----------------
   |              |
 OUI            NON
   |              |
"Majeur"      "Mineur"
```

---

# 4️⃣ **Switch (choix multiples)**

## ✔️ Pourquoi switch ?

Plus lisible que plusieurs `if…else if…`.

```
switch(niveau) {
   case 1:
      console.log("Débutant");
      break;
   case 2:
      console.log("Intermédiaire");
      break;
   default:
      console.log("Avancé");
}
```

### 📘 Schéma

```
      switch(niveau)
           |
---------------------------------
| Niveau 1 | Niveau 2 | Default |
---------------------------------
```

---

# 5️⃣ **Les boucles (répétition)**

## ✔️ Pourquoi les boucles ?

Pour **répéter une action automatiquement**.

---

## 🔹 **1. Boucle `for`**

→ quand on sait combien de fois répéter.

```
for (let i=0; i<5; i++) {
   console.log(i);
}
```

### Schéma

```
i=0 → i<5 ? → oui → action → i++
i=1 → i<5 ? → oui → action → i++
...
```

---

## 🔹 **2. Boucle `while`**

→ répète TANT QUE la condition est vraie.

```
while(count < 3) {
   console.log("Hello");
   count++;
}
```

### Schéma

```
(condition vraie)
       |
    action
       ↑
       |
   retourner
```

---

## 🔹 **3. Boucle `do…while`**

→ exécute au moins **une fois**.

```
do {
   console.log("Exécuté");
} while(x < 5);
```

### Schéma

```
ACTION
  |
vérifier condition
  |
si vrai → recommence
```

---

## ✔️ Différences rapides

| Boucle   | Exécution min | Usage                       |
| -------- | ------------- | --------------------------- |
| for      | 0             | nombre connu de répétitions |
| while    | 0             | tant que condition vraie    |
| do…while | 1             | au moins une fois           |

---

# 6️⃣ **Les tableaux (Array)**

## ✔️ Pourquoi les tableaux ?

Pour stocker plusieurs valeurs dans une seule variable.

```
let fruits = ["pomme", "banane", "orange"];
```

---

# 🍏 **Fonctions principales pour les tableaux (avec schémas)**

---

## 🔹 1. `push()` — ajouter à la fin

```
let fruits = ["pomme", "banane"];
fruits.push("orange");
```

### Schéma push()

```
[ pomme | banane ]  +  "orange"
          |
          v
[ pomme | banane | orange ]
```

---

## 🔹 2. `pop()` — enlever le dernier

```
fruits.pop();
```

### Schéma pop()

```
[ pomme | banane | orange ]
                      |
                      v (retiré)
[ pomme | banane ]
```

---

## 🔹 3. `shift()` — retirer le premier

```
fruits.shift();
```

### Schéma shift()

```
[ pomme | banane | orange ]
   |
   v (retiré)
[ banane | orange ]
```

---

## 🔹 4. `unshift()` — ajouter au début

```
fruits.unshift("kiwi");
```

### Schéma unshift()

```
"kiwi" + [ banane | orange ]
         |
         v
[ kiwi | banane | orange ]
```

---

# 7️⃣ **Les fonctions**

## ✔️ Pourquoi utiliser une fonction ?

Pour **réutiliser un bloc de code** et éviter la duplication.

---

## 🔹 1. Fonction simple

```
function direBonjour() {
   console.log("Bonjour !");
}
```

---

## 🔹 2. Fonction avec paramètre

```
function salut(nom) {
   console.log("Bonjour " + nom);
}

salut("Reda");
```

### Schéma

```
entrée → nom = "Reda"
       |
   fonction salut
       |
   affiche "Bonjour Reda"
```

---

## 🔹 3. Fonction qui retourne une valeur

```
function addition(a, b) {
   return a + b;
}

let x = addition(2, 3);
```

### Schéma

```
a=2  b=3
  |    |
  v    v
 addition
    |
  return 5
```

---

## 🔹 4. Fonctions fléchées (arrow functions)

```
const carre = (x) => x * x;
```

---


