
---

# 🧩 Exercice 3 — Les formulaires HTML5 🧾

---

## 🎯 Objectif

À la fin de cet exercice, tu sauras :
✅ Créer un **formulaire complet** en HTML5.
✅ Comprendre les **différents types de champs** (`text`, `email`, `password`, etc.).
✅ Utiliser les **attributs** pour rendre un formulaire plus clair et interactif.
✅ Mettre en place un **bouton d’envoi** pour récupérer les données saisies.

---

## 💡 1. Introduction : à quoi sert un formulaire ?

Un **formulaire HTML** permet à un utilisateur de **saisir des informations** et de les **envoyer** à un serveur.
C’est le cœur de l’interactivité sur le web 💬 : connexion, inscription, recherche, contact, paiement… tout passe par un formulaire !

---

## 🧱 2. Structure de base d’un formulaire

Voici la structure minimale 👇

```html
<form action="traitement.php" method="POST">
  <label for="nom">Nom :</label>
  <input type="text" id="nom" name="nom">
  <button type="submit">Envoyer</button>
</form>
```

| Élément    | Rôle                                                        |
| ---------- | ----------------------------------------------------------- |
| `<form>`   | Conteneur du formulaire                                     |
| `action`   | Indique la page où les données seront envoyées              |
| `method`   | Mode d’envoi : `GET` (dans l’URL) ou `POST` (plus sécurisé) |
| `<label>`  | Étiquette liée à un champ                                   |
| `<input>`  | Champ de saisie                                             |
| `<button>` | Bouton pour valider ou réinitialiser                        |

---

## ✍️ 3. Les principaux types de champs `<input>`

HTML5 propose de nombreux **types de champs** selon les données à saisir.
Voici les plus utilisés 👇

| Type       | Utilisation                                    | Exemple                                              |
| ---------- | ---------------------------------------------- | ---------------------------------------------------- |
| `text`     | Saisie libre de texte                          | `<input type="text" name="nom">`                     |
| `email`    | Adresse e-mail (avec vérification automatique) | `<input type="email" name="email">`                  |
| `password` | Mot de passe (texte masqué)                    | `<input type="password" name="mdp">`                 |
| `number`   | Nombres uniquement                             | `<input type="number" name="age" min="0" max="100">` |
| `tel`      | Numéro de téléphone                            | `<input type="tel" name="telephone">`                |
| `date`     | Sélection d’une date 📅                        | `<input type="date" name="naissance">`               |
| `color`    | Sélecteur de couleur 🎨                        | `<input type="color" name="couleur">`                |
| `range`    | Curseur numérique (barre de progression)       | `<input type="range" min="0" max="100">`             |
| `file`     | Sélection d’un fichier à envoyer 📂            | `<input type="file" name="cv">`                      |
| `checkbox` | Case à cocher ✅                                | `<input type="checkbox" name="sport">`               |
| `radio`    | Bouton de sélection unique ⚪                   | `<input type="radio" name="sexe" value="homme">`     |

---

## 🧭 4. Exemple simple : formulaire d’inscription 🎓

Voici un exemple complet et clair 👇

```html
<form action="#" method="POST">
  <h2>Formulaire d’inscription 📋</h2>

  <label for="nom">Nom complet :</label><br>
  <input type="text" id="nom" name="nom" placeholder="Entrez votre nom complet"><br><br>

  <label for="email">Adresse e-mail :</label><br>
  <input type="email" id="email" name="email" placeholder="exemple@mail.com"><br><br>

  <label for="mdp">Mot de passe :</label><br>
  <input type="password" id="mdp" name="mdp" placeholder="********"><br><br>

  <label for="naissance">Date de naissance :</label><br>
  <input type="date" id="naissance" name="naissance"><br><br>

  <label>Genre :</label><br>
  <input type="radio" id="homme" name="genre" value="Homme">
  <label for="homme">Homme</label>
  <input type="radio" id="femme" name="genre" value="Femme">
  <label for="femme">Femme</label><br><br>

  <label>Centres d’intérêt :</label><br>
  <input type="checkbox" id="sport" name="interet" value="Sport">
  <label for="sport">⚽ Sport</label>
  <input type="checkbox" id="musique" name="interet" value="Musique">
  <label for="musique">🎵 Musique</label><br><br>

  <label for="ville">Ville :</label><br>
  <select id="ville" name="ville">
    <option value="rabat">Rabat</option>
    <option value="casablanca">Casablanca</option>
    <option value="marrakech">Marrakech</option>
  </select><br><br>

  <button type="submit">✅ Envoyer</button>
  <button type="reset">❌ Réinitialiser</button>
</form>
```

🧠 **Remarques :**

* Les balises `<label>` améliorent l’accessibilité et permettent de cliquer sur le texte pour activer le champ.
* L’attribut `placeholder` affiche un texte d’aide dans le champ.
* Le bouton `reset` efface tout le contenu du formulaire.

---

## 📦 5. Les menus déroulants `<select>` et les zones de texte `<textarea>`

### 🔽 Liste déroulante :

```html
<select name="pays">
  <option value="ma">🇲🇦 Maroc</option>
  <option value="fr">🇫🇷 France</option>
  <option value="es">🇪🇸 Espagne</option>
</select>
```

### 📝 Zone de texte (plusieurs lignes) :

```html
<textarea name="message" rows="4" cols="40" placeholder="Écris ton message ici..."></textarea>
```

---

## 🧩 6. Attributs utiles dans les formulaires

| Attribut      | Description                             | Exemple                                    |
| ------------- | --------------------------------------- | ------------------------------------------ |
| `placeholder` | Indique une aide visuelle dans le champ | `<input placeholder="ex : ton@email.com">` |
| `required`    | Rend le champ obligatoire               | `<input type="email" required>`            |
| `readonly`    | Empêche la modification                 | `<input value="Maroc" readonly>`           |
| `disabled`    | Désactive un champ                      | `<input type="text" disabled>`             |
| `checked`     | Case cochée par défaut                  | `<input type="checkbox" checked>`          |
| `selected`    | Option sélectionnée par défaut          | `<option selected>`                        |

---

## 🧠 7. Bonnes pratiques HTML5 pour les formulaires

✅ Toujours relier chaque champ à un `<label>`
✅ Utiliser `required` pour les champs essentiels
✅ Nommer clairement les champs avec `name`
✅ Grouper les champs similaires (radio, checkbox)
✅ Indenter ton code pour plus de lisibilité
✅ Utiliser des `fieldset` et `legend` pour structurer les grandes parties

---

## 🧪 Exercice pratique : “Formulaire de contact - Support FRMF 🇲🇦⚽”

### 🎯 Objectif :

Créer un **formulaire de contact complet** pour le site de la **Fédération Royale Marocaine de Football**, avec :

* Nom et prénom
* Email
* Sujet (menu déroulant)
* Message (zone de texte)
* Choix du type de demande : “Question”, “Problème”, “Autre”
* Boutons **Envoyer** et **Réinitialiser**

---

### 💡 Indices :

Utilise les balises :

```html
<form>, <label>, <input>, <textarea>, <select>, <option>, <button>, <fieldset>, <legend>
```

---

### 🏁 Résultat attendu :

Un joli formulaire simple, lisible, complet et prêt à être stylisé avec le CSS 🎨

---

💬 **Citation du jour :**

> “Un bon formulaire, c’est comme une bonne conversation : simple, claire et agréable.” 😄

---
