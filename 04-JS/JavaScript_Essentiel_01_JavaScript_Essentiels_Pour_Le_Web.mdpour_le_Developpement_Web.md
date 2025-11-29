

# 🌟 JavaScript Essentiel Pour Le Web

*(Le guide parfait après HTML & CSS)*

Bienvenue dans le module JavaScript Essentiel !
Tu viens de maîtriser **HTML** (la structure) et **CSS** (le style).
Maintenant, tu vas apprendre le **cerveau de tes pages web : JavaScript**.

Grâce à JavaScript, tu peux rendre ton site :

✔ interactif
✔ dynamique
✔ intelligent
✔ réactif aux actions de l’utilisateur

C’est l’étape obligatoire avant d’aller vers :

🔥 Les fonctions avancées
🔥 L’OOP (programmation orientée objet)
🔥 Le backend (PHP, Node.js…)

---

# 🔰 0. Les Mots Essentiels à Comprendre Avant Tout

## 1️⃣ Qu’est-ce qu’un “nom d’élément” ?

C’est juste le *nom que toi, développeur, tu donnes à un élément HTML* quand tu le sélectionnes en JavaScript.

HTML :

```html
<h2 id="titre">Bonjour</h2>
```

JS :

```js
const titre = document.getElementById("titre");
```

➡️ `titre` est seulement un **nom choisi par toi**
➡️ Il représente cet élément dans ton code
Tu aurais pu l’appeler `bonjour`, `text`, ou même `banane` 🍌

---

## 2️⃣ `classList` – Les classes d’un élément 🎨

Permet d’ajouter, retirer ou basculer des classes CSS.

```js
titre.classList.add("active");
titre.classList.remove("rouge");
titre.classList.toggle("visible");
```

➡️ `toggle()` = *si la classe existe → on la retire | sinon → on l’ajoute*

C’est **l’outil le plus utilisé** pour les interactions modernes.

---

## 3️⃣ `addEventListener()` – Réagir à une action de l’utilisateur 🎛️

“Quand il se passe quelque chose → fais une action.”

```js
bouton.addEventListener("click", () => {
    console.log("Tu as cliqué !");
});
```

Les événements importants :

* `"click"` → quand on clique
* `"input"` → quand on écrit
* `"submit"` → formulaire envoyé
* `"mouseover"` → souris dessus
* `"keydown"` → touche du clavier

---

## 4️⃣ `const` et `let` – Les variables modernes (2025)

### ✔ `const`

Variable **qui ne change pas**
→ Utilisée dans 80% des cas

```js
const titre = document.querySelector("h2");
```

### ✔ `let`

Variable **qui peut changer**

```js
let compteur = 0;
compteur++;
```

### ❌ Pourquoi on N’utilise plus `var` ?

Parce que :

* Problèmes de portée (dangereux)
* Peut être redéclaré sans prévenir
* S’échappe des blocs
* Comportement imprévisible

➡️ **En 2025 : on utilise CONST et LET.**

---

# 🧠 1. Sélectionner des Éléments (DOM)

Le JavaScript doit d’abord **attraper un élément HTML** pour agir dessus.

## ✔ `getElementById("id")`

Le plus simple, rapide, précis.

```js
const titre = document.getElementById("titre");
```

---

## ✔ `querySelector("sélecteur CSS")`

Le plus utilisé.
Accepte `.class`, `#id`, `div p`, `.menu li:last-child`…

```js
const bouton = document.querySelector(".btn");
```

---

## ✔ `querySelectorAll("sélecteur")`

Sélectionne **plusieurs éléments**.

```js
const items = document.querySelectorAll(".item");
```

---

# 🎨 2. Modifier des Éléments HTML

## ✔ Modifier le texte

```js
titre.textContent = "Nouveau texte";
```

## ✔ Modifier le contenu HTML

```js
titre.innerHTML = "<b>Texte en gras</b>";
```

## ✔ Modifier le style

```js
titre.style.color = "blue";
```

## ✔ Modifier les classes

```js
titre.classList.add("active");
titre.classList.toggle("red");
titre.classList.remove("hidden");
```

## ✔ Modifier un attribut

```js
img.src = "photo.png";
```

---

# 🎛️ 3. Les Événements (actions de l’utilisateur)

Structure :

```js
element.addEventListener("click", () => {
    // action
});
```

Les événements les plus utilisés :

* `"click"`
* `"input"`
* `"submit"`
* `"mouseover"`
* `"keydown"`
* `"change"`

---

# 🧠 4. Les Fonctions – Le cerveau du code

## Forme classique :

```js
function direBonjour() {
    console.log("Bonjour !");
}
```

## Forme moderne (recommandée) :

```js
const direBonjour = () => {
    console.log("Bonjour !");
};
```

## Appeler une fonction :

```js
direBonjour();
```

---

# 🌟 EXEMPLES COMPLETS (à copier/coller)

---

# ⭐ Exemple 1 : Changer un texte + couleur

## 🧩 HTML

```html
<h2 id="titre">Bonjour !</h2>
<button id="btn">Changer</button>

<script src="script.js" defer></script>
```

## 🎨 CSS

```css
.red {
  color: red;
}
```

## ⚡ JavaScript

```js
const titre = document.getElementById("titre");
const btn = document.getElementById("btn");

btn.addEventListener("click", () => {
  titre.textContent = "Tu as cliqué 🎉";
  titre.classList.toggle("red");
});
```

---

# ⭐ Exemple 2 : Afficher / masquer un texte

## 🧩 HTML

```html
<p id="txt">Je suis visible.</p>
<button id="toggle">Afficher / Masquer</button>

<script src="script.js" defer></script>
```

## 🎨 CSS

```css
.hide {
  display: none;
}
```

## ⚡ JavaScript

```js
const txt = document.querySelector("#txt");
const btn = document.querySelector("#toggle");

btn.addEventListener("click", () => {
  txt.classList.toggle("hide");
});
```

---

# ⭐ Exemple 3 : Compteur (+1)

## 🧩 HTML

```html
<div id="count">0</div>
<button id="plus">+</button>

<script src="script.js" defer></script>
```

## ⚡ JavaScript

```js
let number = 0;

const count = document.getElementById("count");
const plus = document.getElementById("plus");

plus.addEventListener("click", () => {
  number++;
  count.textContent = number;
});
```

---

# ⭐ Exemple 4 : Menu Burger 🍔

## 🧩 HTML

```html
<div id="burger">☰</div>
<ul id="menu">
  <li>Accueil</li>
  <li>Contact</li>
  <li>Services</li>
</ul>

<script src="script.js" defer></script>
```

## 🎨 CSS

```css
#menu {
  display: none;
}

#menu.show {
  display: block;
}

#burger {
  cursor: pointer;
  font-size: 2rem;
}
```

## ⚡ JavaScript

```js
const burger = document.querySelector("#burger");
const menu = document.querySelector("#menu");

burger.addEventListener("click", () => {
  menu.classList.toggle("show");
});
```

---

# 🎉 Résumé Final

Tu sais maintenant :

✔ Ce que signifie “nom d’un élément”
✔ Ce qu’est `classList`
✔ Ce qu’est un event listener
✔ À quoi servent `const` et `let`
✔ Pourquoi `var` est mort en 2025
✔ Comment sélectionner des éléments
✔ Comment les modifier
✔ Comment les faire réagir
✔ Comment écrire des fonctions
✔ Comment faire des mini-interactions utiles

🎯 **Tu as toutes les bases pour commencer :**
➡️ Les fonctions avancées
➡️ L’OOP JavaScript
➡️ Le backend (PHP)

---
