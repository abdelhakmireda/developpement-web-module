
# 🎬 Partie 3️⃣ : Bonus — Animations & Nouveautés CSS Modernes

**Objectif :**
Apporter de la vie à vos pages web avec des animations fluides, des transitions élégantes et découvrir les nouvelles fonctionnalités du CSS moderne.

---

## ✨ Chapitre 3.1 : Transitions CSS — le mouvement simple

### 1. Qu’est-ce qu’une transition ?

Une **transition** permet d’animer le changement progressif d’une propriété CSS (par exemple, la couleur ou la taille) lorsqu’un événement se produit (comme un hover).

### Exemple CSS :

```css
button {
    background-color: #3498db;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    transition: background-color 0.3s ease, transform 0.2s ease;
}

button:hover {
    background-color: #2ecc71;
    transform: scale(1.1);
}
```

**Résultat :** le bouton change de couleur et grandit en douceur lorsqu’on passe la souris dessus.

⚡ **Astuce :** Utilise `transition: all 0.3s ease-in-out;` pour animer plusieurs propriétés en même temps.

---

## 🎥 Chapitre 3.2 : Animations avec `@keyframes`

### 1. Définir une animation

`@keyframes` permet de définir une séquence d’étapes de mouvement.

### Exemple CSS :

```css
@keyframes slideIn {
    from { transform: translateX(-100%); opacity: 0; }
    to { transform: translateX(0); opacity: 1; }
}

.box {
    width: 200px;
    height: 100px;
    background: #e74c3c;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    animation: slideIn 1s ease-out;
}
```

**Résultat :** l’élément glisse depuis la gauche et apparaît progressivement.

🧩 **Astuce :** Tu peux répéter une animation avec `animation-iteration-count: infinite;` ou la faire alterner avec `animation-direction: alternate;`.

---

## 🌈 Chapitre 3.3 : Transformations & Effets 3D

### 1. Rotation et échelle

```css
.square {
    width: 100px;
    height: 100px;
    background-color: #9b59b6;
    transition: transform 0.5s;
}

.square:hover {
    transform: rotate(45deg) scale(1.2);
}
```

### 2. Perspective 3D

```css
.card {
    width: 150px;
    height: 200px;
    background-color: #3498db;
    color: white;
    transform: rotateY(20deg);
    transform-style: preserve-3d;
}
```

💡 **Astuce :** Combine `transform` et `transition` pour créer des effets de cartes qui se retournent ou flottent.

---

## 🧪 Chapitre 3.4 : Les Nouveautés CSS à Connaître (2024+)

| Fonctionnalité          | Description                                                           | Exemple                                          |
| ----------------------- | --------------------------------------------------------------------- | ------------------------------------------------ |
| 🧭 `:has()`             | Sélecteur “parent intelligent” (détection d’un enfant)                | `div:has(img:hover)`                             |
| 🧩 `@layer`             | Organisation du code CSS par couches (priorités claires)              | `@layer base, theme, components;`                |
| 🎚️ `container queries` | Mise en page adaptative selon la taille du conteneur, pas du viewport | `@container (min-width: 400px)`                  |
| 🌒 `color-mix()`        | Mélange de couleurs directement en CSS                                | `background: color-mix(in srgb, red 50%, blue);` |
| 🌫️ `backdrop-filter`   | Effet de flou sur les éléments en arrière-plan                        | `backdrop-filter: blur(10px);`                   |

⚡ **Astuce :** Ces nouveautés rendent CSS plus puissant que jamais — elles permettent de créer des designs dynamiques sans JavaScript.

---

## 🚀 Chapitre 3.5 : Exemple Complet — Carte Animée

### HTML :

```html
<div class="card">
  <h2>Frontend Power 💪</h2>
  <p>CSS moderne et fluide</p>
</div>
```

### CSS :

```css
.card {
  width: 250px;
  height: 150px;
  background: linear-gradient(135deg, #3498db, #9b59b6);
  color: white;
  border-radius: 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  transition: transform 0.4s ease, box-shadow 0.4s ease;
}

.card:hover {
  transform: translateY(-10px) scale(1.05);
  box-shadow: 0 10px 20px rgba(0,0,0,0.3);
}
```

🎨 **Résultat :** une carte qui s’élève et s’agrandit avec un effet d’ombre fluide.

---

## 🧭 Chapitre 3.6 : Pour Aller Plus Loin

* 🔗 [https://developer.mozilla.org/fr/docs/Web/CSS](https://developer.mozilla.org/fr/docs/Web/CSS)
* 🎨 [https://css-tricks.com/](https://css-tricks.com/)
* 🧠 [https://web.dev/learn/css/](https://web.dev/learn/css/)

---

Souhaites-tu que je te fasse une **mise en page Markdown complète et stylée (avec couleurs, emoji et sections bien séparées)** prête à copier dans ton cours ou GitHub ?
