---
# 📘 `exo1_structure.md`

---

# 🧩 Exercice 1 — Structure et balises de base en HTML5

---

## 🎯 Objectif

Apprendre à construire la **structure complète** d’une page web HTML5 avec les **balises essentielles** :
`<!DOCTYPE>`, `<html>`, `<head>`, `<body>`, `<h1>`, `<p>`, `<ul>`, `<li>`, `<section>`, `<footer>`.

Cet exercice t’apprendra à organiser ton contenu de manière **logique et lisible** — la base de tout site web.

---

## 🌍 Contexte

Tu viens d’être recruté comme **développeur web junior** 🧑‍💻 dans une petite agence digitale à Casablanca.
Ton premier projet est de créer une **page de présentation d’un club de football marocain** 🇲🇦.
Tu dois montrer la structure propre d’un site HTML5.

---

## 🧱 Étapes à suivre

1. Crée un fichier nommé **`index.html`**.

2. Mets la **structure standard HTML5** :

   * `<!DOCTYPE html>`
   * `<html lang="fr">`
   * `<head>` avec `<meta charset="UTF-8">` et `<title>`
   * `<body>` avec le contenu.

3. Dans le `<body>` :

   * Un titre principal `<h1>` avec le nom du club.
   * Un paragraphe `<p>` de description.
   * Une liste `<ul>` de 3 à 5 joueurs.
   * Une section `<section>` avec le **palmarès**.
   * Un pied de page `<footer>` avec ton nom et l’année.

---

## 💡 Astuces

👉 Utilise des **balises sémantiques modernes** : `<header>`, `<main>`, `<footer>`
👉 Ajoute des **emoji** pour rendre le rendu plus vivant : ⚽🇲🇦🏆

---

## ⚽ Exemple attendu

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Raja Club Athletic 🇲🇦</title>
</head>
<body>
  <header>
    <h1>Raja Club Athletic ⚽</h1>
  </header>

  <main>
    <section>
      <h2>Présentation</h2>
      <p>Le Raja est un club de football basé à Casablanca, connu pour son beau jeu et ses supporters passionnés 💚.</p>
    </section>

    <section>
      <h2>Joueurs clés</h2>
      <ul>
        <li>Mohamed Nahiri</li>
        <li>Jamal Harkass</li>
        <li>Ismail Mokadem</li>
      </ul>
    </section>

    <section>
      <h2>Palmarès 🏆</h2>
      <p>Champion du Maroc : 12 fois</p>
      <p>Ligue des Champions CAF : 3 fois</p>
    </section>
  </main>

  <footer>
    <p>© 2025 — Réalisé par [Ton Nom]</p>
  </footer>
</body>
</html>
```

---

## ✅ Critères de réussite

| Compétence                                     | Vérification |
| ---------------------------------------------- | ------------ |
| Structure HTML5 complète                       | ✅            |
| Balises correctement imbriquées                | ✅            |
| Présence de balises sémantiques                | ✅            |
| Code indenté et lisible                        | ✅            |
| Contenu cohérent et contextuel (club marocain) | ✅            |

---

