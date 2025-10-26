
```
03_CSS/exercices/exo1_couleurs_polices.md
```

---

# 📝 Exercice 1 : Couleurs, polices et textes

## 🎯 Objectifs

* Appliquer des couleurs à différents éléments
* Modifier les polices et tailles de texte
* Aligner le texte correctement
* Utiliser les classes pour styliser des éléments spécifiques

---

## 1️⃣ Exercice 1 : Couleur et taille du titre

**HTML fourni :**

```html
<h1 class="titre">Bienvenue sur mon site 🎨</h1>
```

**Instructions :**

1. Dans `style.css`, change la couleur du titre en **orange** (#e67e22).
2. Augmente la taille du texte à **40px**.
3. Centre le titre horizontalement.

---

## 2️⃣ Exercice 2 : Paragraphe stylé

**HTML fourni :**

```html
<p class="important">Apprenons le CSS avec plaisir ! 🌟</p>
```

**Instructions :**

1. Change la couleur du texte en **bleu foncé** (#2980b9).
2. Mets le texte en **gras** et **italique**.
3. Aligne le texte au **centre**.

---

## 3️⃣ Exercice 3 : Fond et corps de page

**HTML fourni :**

```html
<body>
  <h1 class="titre">Mon site coloré</h1>
  <p class="important">Test de couleurs et polices</p>
</body>
```

**Instructions :**

1. Ajoute un fond gris clair (`#f0f0f0`) à la page entière.
2. Change la police du corps de la page en **Verdana, sans-serif**.
3. Vérifie que tes modifications s’appliquent correctement aux éléments existants.

---

## 💡 Conseils

* Chaque règle CSS doit cibler le bon sélecteur (`h1`, `.important`, `body`)
* Toujours utiliser un fichier **externe** `style.css` et le lier via `<link>`
* Teste tes changements dans un navigateur pour voir le résultat 🎯

---

## ✅ Solutions (`solutions/exo1_couleurs_polices.css`)

```css
body {
  background-color: #f0f0f0;
  font-family: "Verdana", sans-serif;
}

h1.titre {
  color: #e67e22;
  font-size: 40px;
  text-align: center;
}

p.important {
  color: #2980b9;
  font-weight: bold;
  font-style: italic;
  text-align: center;
}
```

---


