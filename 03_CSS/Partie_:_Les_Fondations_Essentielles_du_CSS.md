
# 1️⃣ Partie 1 : Les Fondations Essentielles du CSS

**Objectif :** Savoir cibler des éléments, appliquer des styles de base, et comprendre que chaque élément HTML est une **boîte** que l’on peut manipuler.

---

## 💻 Chapitre 1.1 : Installation et Ciblage

### 1. Les Bases : Connecter CSS à HTML

CSS applique le style au HTML. Il existe **trois méthodes** pour connecter CSS à HTML :

#### A. CSS en ligne (Inline) 🛑

Style directement dans la balise HTML :

```html
<p style="color: blue;">Texte bleu</p>
```

**Limite :** Très peu pratique si beaucoup d’éléments à styliser.

#### B. CSS interne 🟡

Dans le `<head>` avec `<style>` :

```html
<head>
    <style>
        p { color: red; }
    </style>
</head>
<body>
    <p>Texte rouge</p>
</body>
```

#### C. CSS externe ✅

Séparer le CSS dans un fichier `style.css` :

```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

**Avantages :** Organisation, réutilisation et maintenance facile.

---

### 2. Cibler : Maîtriser les Sélecteurs

| Type    | Syntaxe      | Exemple                                                | Usage                |
| ------- | ------------ | ------------------------------------------------------ | -------------------- |
| Élément | `p`          | `p { color: red; }`                                    | Tous les paragraphes |
| Classe  | `.intro`     | `<p class="intro">` → `.intro { font-size: 18px; }`    | Groupe d’éléments    |
| ID      | `#principal` | `<div id="principal">` → `#principal { color: blue; }` | Élément unique       |

> **Astuce :** Favorisez **les classes** pour plus de flexibilité.

---

### 3. Priorité : Cascade et Spécificité

Si plusieurs règles ciblent le même élément, **la cascade** et **la spécificité** déterminent laquelle l’emporte.

**Exemple :**

```css
p { color: green; }          /* élément = poids 1 */
.texte { color: red; }       /* classe = poids 10 */
#principal { color: blue; }  /* ID = poids 100 */
```

```html
<p id="principal" class="texte">Bonjour</p>
```

**Résultat :** Bleu, car l’ID a le plus haut poids.

---

## 📦 Chapitre 1.2 : Le Modèle de Boîte (Box Model)

Chaque élément HTML est une **boîte rectangulaire** avec 4 parties : **contenu, padding, border, margin**.

### 1. Schéma du Modèle de Boîte

```
+---------------------------+
|         Margin            |
|  +---------------------+  |
|  |      Border         |  |
|  |  +---------------+  |  |
|  |  |   Padding     |  |  |
|  |  |  +---------+  |  |  |
|  |  |  | Content |  |  |  |
|  |  |  +---------+  |  |  |
|  |  +---------------+  |  |
|  +---------------------+  |
+---------------------------+
```

**Exemple pratique :**

```css
.bouton {
    background-color: orange;
    padding: 10px;     /* espace intérieur */
    border: 2px solid black;
    margin: 20px;      /* espace extérieur */
}
```

---

### 2. `box-sizing: border-box;` ✅

Inclut **padding et border** dans les dimensions définies :

```css
* {
    box-sizing: border-box;
}
```

Sans `border-box`, `width` + `padding` + `border` dépassera la largeur définie.

---

### 3️⃣ Types d’affichage : `display`

La propriété `display` détermine comment un élément HTML est placé et comment il interagit avec les autres éléments.

#### 3.1 block – Bloc 🟦

**Description :**

* Occupe toute la largeur disponible.
* Commence sur une nouvelle ligne.
* Peut avoir `width`, `height`, `padding`, `margin`.

**Exemple HTML :**

```html
<div>Je suis un block</div>
<h1>Titre principal</h1>
<p>Paragraphe de texte.</p>
```

**Exemple CSS :**

```css
div {
    width: 300px;
    height: 100px;
    background-color: #f39c12;
    margin: 10px auto;
    padding: 20px;
}
```

**Schéma ASCII :**

```
[###############]   <-- L'élément prend toute la largeur disponible
[###############]   <-- Les autres éléments block apparaissent sur une nouvelle ligne
```

**Astuce :** Parfait pour sections, titres, conteneurs.

---

#### 3.2 inline – En ligne 🟩

**Description :**

* Occupe juste l’espace nécessaire.
* Reste sur la même ligne que d’autres éléments inline.
* `width` et `height` ne fonctionnent pas.

**Exemple HTML :**

```html
<span>Mot 1</span>
<span>Mot 2</span>
<a href="#">Lien</a>
```

**Exemple CSS :**

```css
span {
    color: red;
    font-weight: bold;
}
```

**Schéma ASCII :**

```
[Mot1][Mot2][Lien]  <-- Tous sur la même ligne
```

**Astuce :** Parfait pour les mots, liens ou phrases à l’intérieur d’un texte.

---

#### 3.3 inline-block – En ligne mais bloc 🟧

**Description :**

* Se comporte comme `inline` (reste sur la même ligne).
* Accepte `width`, `height`, `padding`, `margin` comme un `block`.

**Exemple HTML :**

```html
<div class="menu">Accueil</div>
<div class="menu">Services</div>
<div class="menu">Contact</div>
```

**Exemple CSS :**

```css
.menu {
    display: inline-block;
    width: 100px;
    height: 50px;
    line-height: 50px;
    text-align: center;
    background-color: #3498db;
    color: white;
    margin: 5px;
    border-radius: 5px;
}
```

**Schéma ASCII :**

```
[Accueil] [Services] [Contact]  <-- Tous sur la même ligne
```

**Astuce :** Très utilisé pour les menus horizontaux ou boutons alignés côte à côte.

---

### 4. Résumé visuel simple

```
Block      : [##########] 
             [##########]  <-- nouvelle ligne

Inline     : [##][##][##]  <-- même ligne

Inline-block: [###][###][###]  <-- même ligne + peut définir width/height
```

**Exemples typiques :**

* Block → sections, div, h1, p
* Inline → texte, liens, span, a
* Inline-block → boutons, menus horizontaux, cartes alignées

---

## 🎨 Chapitre 1.3 : Styles de Contenu et Visuels

### 1. Typographie 🖋️

#### `text-align` – Alignement du texte

* **left** – Aligné à gauche (par défaut)
* **right** – Aligné à droite
* **center** – Centré horizontalement
* **justify** – Justifié sur toute la largeur du conteneur

**Exemples HTML + CSS :**

```html
<h1 class="center">Titre centré</h1>
<p class="left">Texte aligné à gauche</p>
<p class="right">Texte aligné à droite</p>
<p class="justify">Texte justifié sur toute la largeur du conteneur.</p>
```

```css
.center  { text-align: center; }
.left    { text-align: left; }
.right   { text-align: right; }
.justify { text-align: justify; }
```

**Schéma ASCII :**

```
Left     : Texte aligné à gauche
Right    :          Texte aligné à droite
Center   :        Titre centré
Justify  : |Texte justifié sur toute la largeur du conteneur|
```

> ✅ Astuce : Utilisez `justify` pour les paragraphes longs et `center` pour les titres ou messages importants.

---

### 2. Couleurs 🌈

Formats : `Hex`, `RGB`, `RGBA`, `HSL`, `HSLA`.

```css
body { background-color: #f0f0f0; }
div { background-color: rgba(52,152,219,0.8); color: white; padding: 10px; }
```

---

### 3. Images de fond 🖼️

```css
section {
    width: 300px; height: 200px;
    background-image: url('bg.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}
```

---

### 4. Ombres ✨

```css
div {
    box-shadow: 5px 5px 15px gray;
}

h1 {
    text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
}
```

---

### 5. Exemple complet HTML + CSS

**HTML :**

```html
<h1>Bonjour CSS ! 🎨</h1>
<p class="intro">Apprenons la mise en forme et les couleurs.</p>
<div class="box">Je suis une boîte stylée 📦</div>
```

**CSS :**

```css
* { box-sizing: border-box; }

body {
    font-family: Verdana;
    background-color: #f0f0f0;
    text-align: center;
}

h1 {
    font-size: 36px;
    color: #d35400;
    text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
}

p.intro {
    font-size: 18px;
    font-style: italic;
    text-align: justify;
    color: #2980b9;
    margin: 20px;
}

div.box {
    width: 200px;
    padding: 20px;
    border: 3px solid black;
    margin: 30px auto;
    background-color: rgba(52,152,219,0.8);
    box-shadow: 5px 5px 15px gray;
}
```

