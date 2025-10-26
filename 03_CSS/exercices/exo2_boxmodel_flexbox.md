
---

# 🏗️ Exercice 2 : Box Model & Flexbox

## 🎯 Objectifs

* 📦 Comprendre le **Box Model** (contenu, padding, bordure, marge)
* 🧩 Créer des mises en page simples avec **Flexbox**
* ⚖️ Comprendre quand utiliser **Flexbox** et **pas besoin de Grid pour ce cours**

---

## 1️⃣ Différence simple : Flexbox ⚖️

* **Flexbox** → organise les éléments **dans une seule direction** (ligne ou colonne)
  ➡️ idéal pour menus, alignements simples, cartes ou boutons

💡 Astuce :

* Menu horizontal 🟰 **Flexbox**
* Alignement vertical d’éléments 🟰 **Flexbox**

---

## 2️⃣ Le Box Model 📦

Chaque élément HTML est une boîte composée de :

1. **Content** ✏️ → texte ou image à l’intérieur
2. **Padding** 🛋️ → espace **intérieur** entre le contenu et la bordure
3. **Border** 🖤 → contour autour de l’élément
4. **Margin** 🌌 → espace **extérieur** autour de l’élément

**Exemple :**

```html
<div class="box">Boîte CSS</div>
```

```css
.box {
  width: 200px;            /* largeur du contenu */
  padding: 20px;           /* espace intérieur */
  border: 5px solid #3498db; /* bordure bleue */
  margin: 15px;            /* espace extérieur */
  background-color: #ecf0f1; /* couleur de fond */
}
```

💡 Astuce : **Padding + Border + Content = taille totale de la boîte visible**

---

## 3️⃣ Flexbox 🧩

Flexbox permet de **distribuer et aligner les éléments facilement** dans un conteneur.

**Propriétés principales :**

* `display: flex;` → active Flexbox
* `justify-content` → aligne horizontalement (`flex-start`, `center`, `space-between`, `space-around`)
* `align-items` → aligne verticalement (`flex-start`, `center`, `stretch`)
* `flex-wrap` → permet aux éléments de passer à la ligne si besoin

**Exemple :**

```html
<div class="flex-container">
  <div>1️⃣</div>
  <div>2️⃣</div>
  <div>3️⃣</div>
  <div>4️⃣</div>
</div>
```

```css
.flex-container {
  display: flex;                 /* active Flexbox */
  justify-content: space-between;/* espace égal entre les éléments */
  align-items: center;           /* centrage vertical */
  height: 150px;                 /* hauteur du conteneur */
  background-color: #f0f0f0;    /* couleur du conteneur */
  padding: 10px;                 /* espace intérieur */
}
.flex-container div {
  width: 50px;                   /* largeur des éléments */
  height: 50px;                  /* hauteur des éléments */
  background-color: #e67e22;     /* couleur des éléments */
  color: white;                  /* couleur du texte */
  display: flex;                 /* Flexbox interne pour centrer le texte */
  justify-content: center;       /* centrage horizontal du texte */
  align-items: center;           /* centrage vertical du texte */
  border-radius: 5px;            /* coins arrondis */
}
```

💡 Astuce : **Flexbox est très pratique pour créer des cartes ou boutons alignés facilement**

---

## 4️⃣ Exercices ✍️

### Exercice 1 : Box Model 📦

1. Crée une `<div>` avec :

   * largeur 150px
   * padding 20px
   * bordure 3px bleue
   * marge 10px
2. Texte : “Boîte CSS”

### Exercice 2 : Flexbox 🧩

1. Crée un conteneur `flex-container` avec 4 éléments
2. Aligne-les horizontalement avec un **espace égal**
3. Centre verticalement

---

## 5️⃣ Solutions ✅

### Solution Exercice 1 : Box Model 📦

```html
<div class="box">Boîte CSS</div>
```

```css
.box {
  width: 150px;
  padding: 20px;
  border: 3px solid #3498db;
  margin: 10px;
  background-color: #ecf0f1;
}
```

### Solution Exercice 2 : Flexbox 🧩

```html
<div class="flex-container">
  <div>1️⃣</div>
  <div>2️⃣</div>
  <div>3️⃣</div>
  <div>4️⃣</div>
</div>
```

```css
.flex-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 120px;
  background-color: #f0f0f0;
  padding: 10px;
}
.flex-container div {
  width: 40px;
  height: 40px;
  background-color: #e67e22;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 5px;
}
```

---


Veux‑tu que je fasse ça ?
