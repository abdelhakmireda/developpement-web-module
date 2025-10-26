
---

# 🎨 Cours CSS — Partie 1 : Bases et mise en forme du texte

## 🎯 Objectifs de la partie

À la fin de cette section, tu sauras :

* Comprendre le rôle du CSS dans le Web
* Appliquer des couleurs et des polices à ton site 🌈
* Modifier la taille, le style et l’alignement du texte 🖋️
* Créer des styles simples pour tes pages HTML

---

## 🌐 1. Qu’est-ce que le CSS ?

CSS signifie **Cascading Style Sheets** (Feuilles de style en cascade).
💡 Il sert à **styliser** le contenu HTML : couleurs, tailles, marges, alignements, animations, etc.

### Exemple simple :

HTML :

```html
<p>Bonjour le Maroc 🇲🇦 !</p>
```

CSS :

```css
p {
  color: red;       /* Couleur du texte */
  font-size: 20px;  /* Taille du texte */
  font-family: Arial, sans-serif; /* Police du texte */
}
```

Résultat :
Le paragraphe devient **rouge**, taille 20px, avec la police Arial 🖌️

---

## 🎨 2. Sélecteurs CSS

Les **sélecteurs** permettent de dire au CSS **quelle partie du HTML** il doit styliser.

| Sélecteur | Exemple HTML                     | CSS                                 | Description                               |
| --------- | -------------------------------- | ----------------------------------- | ----------------------------------------- |
| Élément   | `<p>Texte</p>`                   | `p { color: blue; }`                | Style tous les `<p>`                      |
| ID        | `<p id="intro">Texte</p>`        | `#intro { font-size: 18px; }`       | Style l’élément avec un ID unique         |
| Classe    | `<p class="important">Texte</p>` | `.important { font-weight: bold; }` | Style tous les éléments avec cette classe |

💡 Bon réflexe : **ID = unique, classe = réutilisable**

---

## 🌈 3. Couleurs CSS

CSS propose plusieurs façons de définir les couleurs :

### 1️⃣ Noms de couleur

```css
h1 {
  color: green; /* Vert */
}
```

### 2️⃣ Code hexadécimal

```css
p {
  color: #ff0000; /* Rouge */
}
```

### 3️⃣ RGB

```css
p {
  color: rgb(0, 128, 255); /* Bleu clair */
}
```

### 4️⃣ RGBA (avec transparence)

```css
p {
  color: rgba(255, 0, 0, 0.5); /* Rouge semi-transparent */
}
```

---

## 🖋️ 4. Polices et texte

### 1️⃣ Police du texte

```css
body {
  font-family: "Arial", sans-serif;
}
```

### 2️⃣ Taille du texte

```css
h1 {
  font-size: 36px;
}
```

### 3️⃣ Style du texte

```css
p {
  font-style: italic;     /* Italique */
  font-weight: bold;      /* Gras */
  text-decoration: underline; /* Souligné */
}
```

### 4️⃣ Alignement

```css
p {
  text-align: center; /* gauche / center / right / justify */
}
```

---

## 📦 5. Exemple complet

HTML :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Exemple CSS</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Bonjour le Maroc 🇲🇦</h1>
  <p class="important">Apprenons le CSS avec plaisir ! 🎨</p>
</body>
</html>
```

CSS (`style.css`) :

```css
body {
  font-family: "Verdana", sans-serif;
  background-color: #f0f0f0; /* Gris clair */
}

h1 {
  color: #d35400; /* Orange */
  text-align: center;
}

p.important {
  color: #2980b9; /* Bleu */
  font-size: 18px;
  font-weight: bold;
  text-align: center;
}
```

Résultat :

* Fond gris clair
* Titre orange centré
* Paragraphe bleu gras centré

---

## 💡 6. Bonnes pratiques CSS

✅ Utiliser un fichier externe `style.css`
✅ Noms de classes explicites `.important`, `.header`
✅ Indenter pour la lisibilité
✅ Commenter son code

```css
/* Couleur du titre principal */
h1 { color: #d35400; }
```

---

