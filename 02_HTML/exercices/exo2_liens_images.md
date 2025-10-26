
---

# 🧩 Exercice 2 — Liens, images et contenus multimédias 🌐

---

## 🎯 Objectif

Apprendre à insérer des **liens hypertextes**, des **images** et des **éléments multimédias** (comme les vidéos) dans une page web.
Tu vas comprendre comment rendre un site **vivant, navigable et illustré** — indispensable pour tout site moderne 🌍

---

## 🧭 Introduction

HTML permet non seulement d’écrire du texte, mais aussi de **lier** des pages entre elles et d’y **insérer des médias** : images, vidéos, sons, etc.

Ces éléments rendent une page plus agréable, plus claire et plus interactive pour les utilisateurs 📱💻

---

## 🔗 1. Les liens hypertextes `<a>`

Le lien est l’âme du web : c’est ce qui relie toutes les pages entre elles 🌐

**Syntaxe de base :**

```html
<a href="URL">Texte cliquable</a>
```

### 🧩 Exemple simple :

```html
<a href="https://www.frmf.ma">Site officiel de la FRMF</a>
```

💡 **Attributs utiles :**

| Attribut          | Rôle                                | Exemple                                  |
| ----------------- | ----------------------------------- | ---------------------------------------- |
| `href`            | Lien à ouvrir                       | `<a href="https://...">`                 |
| `target="_blank"` | Ouvre le lien dans un nouvel onglet | `<a href="..." target="_blank">`         |
| `title`           | Texte affiché au survol             | `<a href="..." title="Visitez le site">` |

---

## 🖼️ 2. Les images `<img>`

Les images permettent d’illustrer ton contenu 📸

**Syntaxe de base :**

```html
<img src="chemin/vers/image.jpg" alt="Description de l’image">
```

💬 Exemple :

```html
<img src="images/maroc.png" alt="Drapeau du Maroc" width="150">
```

🧠 **Règles importantes :**

* Toujours ajouter un **attribut `alt`** (utile pour l’accessibilité).
* Spécifie la **taille** avec `width` ou `height`.
* Le navigateur **ne ferme pas** la balise `<img>` (c’est une balise **orpheline / void**).

---

## 📸 3. Liens + images

On peut transformer une **image en lien cliquable** 🔗🖼️

**Exemple :**

```html
<a href="https://fr.wikipedia.org/wiki/Marrakech" target="_blank">
  <img src="images/marrakech.jpg" alt="Marrakech" width="300">
</a>
```

👉 Quand on clique sur l’image, on est redirigé vers la page Wikipédia de Marrakech.

---

## 🎥 4. Intégrer une vidéo YouTube (balise `<iframe>`)

HTML permet aussi d’afficher du contenu externe, comme une **vidéo YouTube**, à l’aide de la balise `<iframe>`.

**Exemple :**

```html
<iframe width="560" height="315"
  src="https://www.youtube.com/embed/qzvQvYljh7Q"
  title="Maroc vu du ciel"
  frameborder="0"
  allowfullscreen>
</iframe>
```

💡 *Astuce :*
Sur YouTube, clique sur **Partager → Intégrer → Copier le code HTML** pour obtenir ton `<iframe>` automatiquement.

---

## 🧱 5. Balises de présentation utiles

| Balise | Rôle                            | Exemple                     |
| ------ | ------------------------------- | --------------------------- |
| `<hr>` | Ligne horizontale de séparation | `<hr>`                      |
| `<br>` | Saut de ligne                   | `<p>Bonjour<br>Maroc !</p>` |

⚠️ Ces balises sont aussi **orphelines** : elles ne se ferment pas !

---

## 🧪 Exercice pratique : “Tourisme au Maroc 🇲🇦”

### 📘 Consigne :

Crée une page web nommée `tourisme.html` contenant :

1. Un titre principal `<h1>` → *“Découvre le Maroc 🇲🇦”*
2. Un paragraphe d’introduction décrivant le Maroc.
3. Une **section avec trois villes marocaines** :

   * Pour chaque ville :

     * une image `<img>` avec le drapeau ou un monument,
     * un lien `<a>` vers Wikipédia ou un site touristique.
4. Une **ligne de séparation** `<hr>` entre les sections.
5. Une **vidéo YouTube intégrée** sur le tourisme marocain.

---

### 💡 Balises recommandées :

```html
<h1>, <p>, <a>, <img>, <hr>, <iframe>
```

---

### ⚽ Exemple (simplifié) :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Tourisme au Maroc 🇲🇦</title>
</head>
<body>
  <h1>Découvre le Maroc 🌍</h1>
  <p>Explore la beauté du Maroc à travers ses villes les plus emblématiques.</p>

  <hr>

  <h2>Villes à visiter 🏙️</h2>

  <a href="https://fr.wikipedia.org/wiki/Marrakech" target="_blank">
    <img src="images/marrakech.jpg" alt="Marrakech" width="250">
  </a>

  <a href="https://fr.wikipedia.org/wiki/Chefchaouen" target="_blank">
    <img src="images/chefchaouen.jpg" alt="Chefchaouen" width="250">
  </a>

  <a href="https://fr.wikipedia.org/wiki/Agadir" target="_blank">
    <img src="images/agadir.jpg" alt="Agadir" width="250">
  </a>

  <hr>

  <h2>Vidéo : Le Maroc vu du ciel 🎥</h2>
  <iframe width="560" height="315"
          src="https://www.youtube.com/embed/qzvQvYljh7Q"
          title="Maroc vidéo"
          frameborder="0"
          allowfullscreen></iframe>

</body>
</html>
```

---

## ✅ Critères de réussite

| Compétence                             | Vérification |
| -------------------------------------- | ------------ |
| Liens cliquables fonctionnels          | ✅            |
| Images affichées avec texte alternatif | ✅            |
| Ligne horizontale bien utilisée        | ✅            |
| Vidéo intégrée via `<iframe>`          | ✅            |
| Code indenté et lisible                | ✅            |

---

💬 **Astuce bonus :**
Tu peux créer un dossier `/images` pour ranger tes photos et un dossier `/pages` pour tes autres fichiers HTML.
Cela t’aide à garder ton projet bien organisé 📁

---

