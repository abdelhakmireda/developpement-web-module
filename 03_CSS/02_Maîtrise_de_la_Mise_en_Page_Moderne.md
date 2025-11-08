
# 2️⃣ Partie 2 : Maîtrise de la Mise en Page Moderne

**Objectif :** Organiser et aligner n’importe quel contenu dans l’espace en utilisant Flexbox et CSS Grid, tout en comprenant les principes de base du positionnement, de la dimension et des axes.

---

## 🗺️ Chapitre 2.1 : Organisation Traditionnelle et Positionnement

### 1. Dimensions : width, height, min/max et overflow 📐

* **width / height** : définissent la largeur et la hauteur d’un élément.
* **min-width / max-width** : assurent que l’élément ne devienne jamais trop petit ou trop grand.
* **overflow** : contrôle comment le contenu dépasse de sa boîte. Options :

  * `visible` : le contenu dépasse librement (par défaut)
  * `hidden` : le contenu dépassant est caché
  * `scroll` : barre de défilement toujours présente
  * `auto` : barre de défilement si nécessaire

**Exemple CSS :**

```css
div.box {
    width: 300px;       /* largeur fixe */
    max-width: 80%;     /* jamais plus large que 80% de son parent */
    height: 150px;      /* hauteur fixe */
    min-height: 100px;  /* jamais plus petit que 100px */
    overflow: auto;     /* barre de scroll si contenu dépasse */
    background-color: #ecf0f1;
    padding: 10px;
}
```

**Schéma ASCII :**

```
+------------------------+
| Contenu qui peut scroll |
+------------------------+
```

> ⚡ Astuce : Utilise `max-width` pour créer des éléments **responsive**.

---

### 2. Position : relative, absolute, fixed, sticky 📍

Permet de **placer les éléments exactement où tu veux**.

| Position | Description                                               | Exemple pratique                     |
| -------- | --------------------------------------------------------- | ------------------------------------ |
| relative | Déplace l’élément **par rapport à sa position normale**   | Tooltip décalé d’un parent           |
| absolute | Déplace l’élément **par rapport à son parent positionné** | Menu déroulant, pop-up               |
| fixed    | Éléments **fixes par rapport à la fenêtre**               | Barre de navigation sticky           |
| sticky   | Mix entre relative et fixed                               | Header qui devient fixe après scroll |

**Exemple CSS :**

```css
div.relative { position: relative; top: 10px; left: 20px; background: #f39c12; }
div.absolute { position: absolute; top: 50px; left: 100px; background: #2ecc71; }
div.fixed { position: fixed; top: 0; width: 100%; background: #3498db; color: white; }
div.sticky { position: sticky; top: 0; background: #f1c40f; }
```

**Schéma ASCII :**

```
Normal flow:   [Box1]
               [Box2]

Relative:      [Box1] ← décalé de 10px vers le bas
Absolute:      [Box1] ← positionné par rapport au parent
Fixed:         [Box1] ← reste visible sur la fenêtre
Sticky:        [Box1] ← devient fixe après scroll
```

---

### 3. Profondeur avec z-index 🏔️

* Permet de gérer **l’empilement des éléments**.
* Plus le `z-index` est grand, plus l’élément est **au-dessus**.

```css
div.bg { z-index: 1; background: lightgray; position: relative; }
div.fg { z-index: 10; background: orange; position: relative; }
```

**Schéma ASCII :**

```
[fg]  <-- devant
[bg]  <-- derrière
```

> ⚡ Astuce : Toujours ajouter `position: relative` ou `absolute` avant d’utiliser `z-index`.

---

## 🔄 Chapitre 2.2 : Le Layout 1D (Flexbox)

Flexbox est utilisé pour **aligner les éléments sur une seule dimension** : une ligne ou une colonne.

### 1. Activation et axes ⚙️

```css
.container {
    display: flex;       /* active Flexbox */
    flex-direction: row; /* par défaut : ligne horizontale */
}
```

* **Main axis** : l’axe principal (horizontal par défaut).
* **Cross axis** : axe perpendiculaire (vertical par défaut).

**Schéma ASCII :**

```
Main axis → [Item1][Item2][Item3]
Cross axis ↓
```

---

### 2. Alignement : justify-content et align-items 🎯

| Propriété       | Effet                                                                                                             |
| --------------- | ----------------------------------------------------------------------------------------------------------------- |
| justify-content | Aligne les éléments **sur l’axe principal** (`flex-start`, `center`, `flex-end`, `space-between`, `space-around`) |
| align-items     | Aligne les éléments **sur l’axe perpendiculaire** (`flex-start`, `center`, `flex-end`, `stretch`)                 |

**Exemple CSS :**

```css
.container {
    display: flex;
    justify-content: space-around; /* espace égal entre les éléments */
    align-items: center;           /* centre verticalement */
    height: 150px;
    background-color: #ecf0f1;
}
.item {
    width: 50px;
    height: 50px;
    background-color: #e74c3c;
}
```

**Schéma ASCII :**

```
[Item1]    [Item2]    [Item3]
```

---

### 3. Flex-grow, flex-shrink et flex 🔧

* **flex-grow** : l’élément peut **grandir** pour remplir l’espace.
* **flex-shrink** : l’élément peut **rétrécir** si l’espace est limité.
* **flex** : raccourci pour `flex-grow flex-shrink flex-basis`.

```css
.item1 { flex: 1; }    /* prend 1 part de l’espace */
.item2 { flex: 2; }    /* prend 2 parts de l’espace */
.item3 { flex: 1; }    /* prend 1 part de l’espace */
```

**Schéma ASCII :**

```
[Item1][Item2][Item3] <-- largeur proportionnelle à flex
```

---

### 4. Exemple complet Flexbox 💡

**HTML :**

```html
<div class="container">
    <div class="item1">1️⃣</div>
    <div class="item2">2️⃣</div>
    <div class="item3">3️⃣</div>
</div>
```

**CSS :**

```css
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100px;
    background-color: #ecf0f1;
}
.item1 { flex: 1; background-color: #e74c3c; }
.item2 { flex: 2; background-color: #2ecc71; }
.item3 { flex: 1; background-color: #3498db; }
```

**Résultat :** les blocs ont une largeur proportionnelle à leur valeur `flex`.

---

## 🧱 Chapitre 2.3 : Le Layout 2D (CSS Grid)

CSS Grid permet de créer **des mises en page sur deux dimensions** : lignes et colonnes.

### 1. Activation et colonnes/lignes ⚡

```css
.container {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;  /* colonnes proportionnelles */
    grid-template-rows: 100px 200px;     /* lignes fixes */
    gap: 10px;                           /* espace entre les cellules */
}
```

**Schéma ASCII :**

```
+--------+--------+--------+
| Cell1  | Cell2  | Cell3  |
+--------+--------+--------+
| Cell4  | Cell5  | Cell6  |
+--------+--------+--------+
```

---

### 2. grid-template-areas : visualisation simplifiée 🖼️

```css
.container {
    display: grid;
    grid-template-areas:
        "header header header"
        "menu main sidebar"
        "footer footer footer";
    gap: 10px;
}
.header { grid-area: header; background: #3498db; color: white; text-align: center; }
.menu { grid-area: menu; background: #2ecc71; color: white; text-align: center; }
.main { grid-area: main; background: #e74c3c; color: white; text-align: center; }
.sidebar { grid-area: sidebar; background: #f1c40f; color: black; text-align: center; }
.footer { grid-area: footer; background: #9b59b6; color: white; text-align: center; }
```

**Schéma ASCII :**

```
[ Header ][ Header ][ Header ]
[ Menu   ][ Main   ][Sidebar ]
[ Footer ][ Footer ][ Footer ]
```

---

### 3. Exemple HTML complet Grid 🌟

```html
<div class="container">
    <div class="header">Header</div>
    <div class="menu">Menu</div>
    <div class="main">Main</div>
    <div class="sidebar">Sidebar</div>
    <div class="footer">Footer</div>
</div>
```

> ✅ Astuce : CSS Grid est parfait pour **les layouts de site web complets**, les tableaux complexes ou les galeries.

---

### 4. Résumé visuel simple 📊

| Layout  | Description            | Schéma ASCII                 |
| ------- | ---------------------- | ---------------------------- |
| Flexbox | 1D : ligne ou colonne  | [Item1][Item2][Item3]        |
| Grid    | 2D : lignes + colonnes | [C1][C2][C3]<br>[C4][C5][C6] |

---

