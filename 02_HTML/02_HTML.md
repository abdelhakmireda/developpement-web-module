
# 🏗️ Cours : HTML5 — Structure et bases du Web

---

## 🎯 Objectifs du chapitre

À la fin de ce cours, tu sauras :

* Créer une **page web complète** en HTML5.
* Comprendre la **structure standard d’un document HTML**.
* Utiliser les **balises sémantiques** modernes.
* Faire la différence entre **balises orphelines (void)** et **balises avec contenu**.
* Suivre les **bonnes pratiques HTML5** pour coder proprement.

---

## 🌐 1. Qu’est-ce que le HTML ?

**HTML** signifie **HyperText Markup Language**.
C’est le **langage de structure** d’une page web.

> 💬 Il ne sert pas à “programmer”, mais à **organiser** et **décrire** le contenu d’une page.

Chaque élément du HTML est une **balise** :

```html
<p>Ceci est un paragraphe.</p>
```

Les balises indiquent **le rôle du contenu** au navigateur.

---

## 🧱 2. Structure d’une page HTML5

Voici la structure de base d’un fichier HTML moderne :

```html
<!DOCTYPE html>
<html lang="fr">
  <head>
    <meta charset="UTF-8">
    <title>Page d’exemple</title>
  </head>
  <body>
    <h1>Bienvenue sur ma première page HTML5</h1>
    <p>Ceci est un texte d’exemple.</p>
  </body>
</html>
```

### 🧩 Décomposition :

| Élément           | Rôle                                                        |
| ----------------- | ----------------------------------------------------------- |
| `<!DOCTYPE html>` | Indique au navigateur que c’est un document HTML5           |
| `<html>`          | Conteneur racine du document                                |
| `<head>`          | Contient les métadonnées (titre, encodage, liens CSS, etc.) |
| `<body>`          | Contient le contenu visible par l’utilisateur               |

---

## 📄 3. Le rôle des balises

### 🔹 Balises ouvrantes et fermantes

La plupart des balises ont une ouverture `<balise>` et une fermeture `</balise>` :

```html
<p>Je suis un paragraphe</p>
```

### 🔹 Balises **orphelines** (ou **void elements**)

Certaines balises **n’ont pas de contenu**, donc **pas de balise fermante**.
Elles se suffisent à elles-mêmes 👇

| Balise    | Rôle                     | Exemple                                      |
| --------- | ------------------------ | -------------------------------------------- |
| `<img>`   | Afficher une image       | `<img src="lion.png" alt="Lion de l’Atlas">` |
| `<br>`    | Saut de ligne            | `<p>Bonjour<br>Maroc !</p>`                  |
| `<hr>`    | Ligne de séparation      | `<hr>`                                       |
| `<meta>`  | Informations sur la page | `<meta charset="UTF-8">`                     |
| `<input>` | Champ de formulaire      | `<input type="text">`                        |

> ⚠️ Ces balises **ne se ferment pas** (`</img>` ❌).

---

## ⚙️ 4. Comment fonctionne le HTML dans le Web ?

Imaginons que tu crées une page “**Équipe nationale du Maroc 🇲🇦**” :

Quand tu ouvres le fichier `index.html`, le **navigateur lit** le code HTML et **affiche** le contenu visuel.

### ⚽ Exemple :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Équipe du Maroc</title>
</head>
<body>
  <h1>Les Lions de l’Atlas 🦁🇲🇦</h1>
  <p>L’équipe nationale de football du Maroc, l’une des meilleures d’Afrique.</p>
  <img src="maroc.png" alt="Drapeau du Maroc" width="150">
  <ul>
    <li>Achraf Hakimi</li>
    <li>Yassine Bounou</li>
    <li>Sofyan Amrabat</li>
  </ul>
</body>
</html>
```

Le navigateur affichera :

* Un **titre** 🦁
* Un **paragraphe descriptif**
* Une **image** du drapeau 🇲🇦
* Une **liste** des joueurs

> 🧠 Ce code est lisible par les humains **et** par les machines (navigateurs, robots de recherche, lecteurs vocaux...).

---

## 🧩 5. Les balises de texte

| Balise          | Description                     | Exemple                                       |
| --------------- | ------------------------------- | --------------------------------------------- |
| `<h1>` → `<h6>` | Titres hiérarchiques            | `<h1>Titre principal</h1>`                    |
| `<p>`           | Paragraphe                      | `<p>Un texte</p>`                             |
| `<strong>`      | Texte important (gras)          | `<strong>Attention</strong>`                  |
| `<em>`          | Texte mis en emphase (italique) | `<em>Mot en valeur</em>`                      |
| `<a>`           | Lien hypertexte                 | `<a href="https://www.frmf.ma">Site FRMF</a>` |
| `<img>`         | Image                           | `<img src="lion.png" alt="Lion">`             |
| `<br>`          | Retour à la ligne               | `<br>`                                        |

---

## 📦 6. Les balises de structure sémantique (HTML5)

Le HTML5 a introduit de **nouvelles balises sémantiques**,
pour donner **du sens** au contenu (meilleure accessibilité et SEO 🧭).

| Balise      | Rôle                                           | Exemple                    |
| ----------- | ---------------------------------------------- | -------------------------- |
| `<header>`  | En-tête de page                                | Logo, titre                |
| `<nav>`     | Navigation                                     | Liens vers d’autres pages  |
| `<main>`    | Contenu principal                              | Articles, sections         |
| `<section>` | Partie thématique du contenu                   | Section "Actualités"       |
| `<article>` | Contenu indépendant (ex : un post, un article) | Un article de blog         |
| `<aside>`   | Contenu secondaire                             | Publicité, infos latérales |
| `<footer>`  | Pied de page                                   | Copyright, contact         |

### 🧭 Exemple structuré :

```html
<body>
  <header>
    <h1>Les Lions de l’Atlas 🦁</h1>
    <nav>
      <a href="#joueurs">Joueurs</a> |
      <a href="#palmares">Palmarès</a>
    </nav>
  </header>

  <main>
    <section id="joueurs">
      <h2>Nos Stars 🇲🇦</h2>
      <p>Achraf Hakimi, Yassine Bounou, Sofyan Amrabat...</p>
    </section>

    <section id="palmares">
      <h2>Palmarès 🏆</h2>
      <p>Vainqueur CAN 1976, demi-finaliste Coupe du Monde 2022 ⚽</p>
    </section>
  </main>

  <footer>
    <p>© 2025 Fédération Royale Marocaine de Football</p>
  </footer>
</body>
```

---

## 📄 7. Les attributs HTML

Les **attributs** apportent des **informations supplémentaires** à une balise.
Ils sont toujours écrits dans la balise ouvrante.

### Exemple :

```html
<img src="maroc.png" alt="Drapeau du Maroc" width="150">
```

| Attribut       | Description                                       |
| -------------- | ------------------------------------------------- |
| `src`          | Chemin vers l’image                               |
| `alt`          | Texte alternatif (important pour l’accessibilité) |
| `width`        | Largeur de l’image                                |
| `id` / `class` | Identifiants pour le CSS ou JS                    |

> 🧠 Bon réflexe : toujours ajouter un attribut `alt` pour les images.

---

## ⚙️ 8. Les commentaires

Les **commentaires** ne s’affichent pas à l’écran, mais servent à documenter ton code :

```html
<!-- Ceci est un commentaire -->
```

---

## 🧩 9. L’arborescence d’un projet HTML

```
mon_site/
│
├── index.html
├── style.css
└── images/
    ├── maroc.png
    └── logo.png
```

> 💡 Le fichier `index.html` est **toujours** le point d’entrée du site.

---

## 🌍 10. Schéma visuel du protocole HTTP

```
[ 🧑‍💻 Étudiant ]
      │
      ▼
[ Navigateur (Client) ]
      │  Envoie une requête HTTP ➡️
      ▼
[ Serveur Web ]
      │  Renvoie une réponse (HTML, CSS, JS) ⬅️
      ▼
[ Affichage de la page dans le navigateur 🖥️ ]
```

**Exemple concret :**

Tu ouvres dans ton navigateur :
`https://www.frmf.ma`

👉 Le navigateur envoie une requête **HTTP GET** au serveur de la FRMF.
👉 Le serveur répond avec la page HTML du site officiel.
👉 Ton navigateur l’affiche : le site de la Fédération Royale Marocaine de Football 🇲🇦⚽

---

## 🧠 11. Bonnes pratiques HTML5

✅ Toujours utiliser un `<!DOCTYPE html>`

✅ Indiquer la langue (`<html lang="fr">`)

✅ Fermer correctement les balises

✅ Indenter ton code pour qu’il soit lisible

✅ Utiliser les **balises sémantiques** plutôt que des `<div>` anonymes

✅ Décrire les images avec `alt`

✅ Ne jamais abuser des `<br>` pour faire de la mise en page (utilise le CSS)


---

## 🏁 Conclusion

Le **HTML5** est la **base de tout site web** 🌐
Il te permet d’organiser le contenu et de donner un sens à chaque partie de ta page.

👉 Dans le prochain chapitre, tu apprendras à **styliser tes pages avec le CSS** 🎨
pour transformer une structure brute en **site moderne et esthétique**.

---

