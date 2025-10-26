
# 🌍 Cours 01 — Introduction au Web

---

## 🎯 Objectif général

Avant d’apprendre à coder, il faut **comprendre le terrain de jeu : le Web**.
Ce cours va t’aider à savoir :

* Ce qu’est **Internet** et ce qu’est **le Web** (ce n’est pas la même chose 🧐).
* Comment fonctionne **le protocole HTTP** entre ton ordinateur et un serveur.
* Les **types de Web** (Web 1.0, 2.0, 3.0).
* Les **technologies fondamentales** : HTML, CSS, JavaScript.
* Et pourquoi ces langages sont **indispensables** aujourd’hui.

---

## 🌐 1. Internet et le Web : deux notions différentes

Beaucoup de gens pensent qu’**Internet = Web**, mais ce n’est pas vrai.
En réalité :

* **Internet** 🌎 est un **réseau mondial** d’ordinateurs et de serveurs connectés entre eux.
  C’est “l’infrastructure” (les câbles, les routeurs, les serveurs).

* **Le Web (World Wide Web)** 💻 est **un service** qui fonctionne **sur Internet**.
  Il permet d’accéder à des **pages**, des **images**, des **vidéos**, etc., grâce à un **navigateur** (Chrome, Firefox, Edge…).

🧠 **Petit exemple concret :**
Quand tu envoies un message sur **WhatsApp**, tu utilises Internet,
mais quand tu consultes **un site web**, tu utilises **le Web**.

📖 **Analogie simple :**

> Internet, c’est une **autoroute** 🛣️
> Le Web, ce sont les **voitures** 🚗 qui circulent dessus.

---

## 🕰️ 2. L’évolution du Web — du Web 1.0 au Web 3.0

Le Web a beaucoup évolué depuis sa création par **Tim Berners-Lee (1991)**.

| Type de Web    | Période            | Description                                                                               | Exemple                                                  |
| -------------- | ------------------ | ----------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| **Web 1.0** 🌍 | 1990 – 2004        | Web **statique** : on pouvait seulement lire les pages. Aucun échange avec l’utilisateur. | Les premiers sites d’informations ou les pages vitrines. |
| **Web 2.0** 🤝 | 2004 – 2020        | Web **social et interactif** : les utilisateurs peuvent créer, commenter, partager.       | Facebook, YouTube, Wikipédia.                            |
| **Web 3.0** 🧠 | 2020 – aujourd’hui | Web **intelligent et décentralisé** : IA, blockchain, personnalisation.                   | ChatGPT, applications Web3, NFTs.                        |

💬 **Exemple marocain :**

* Web 1.0 → un site statique présentant la ville de Marrakech.
* Web 2.0 → un site touristique où les utilisateurs laissent des avis ✍️.
* Web 3.0 → une application qui recommande des destinations selon ton profil.

---

## ⚙️ 3. Comment fonctionne le Web ?

Le Web fonctionne grâce à une **communication entre deux acteurs principaux** :
le **client (navigateur)** et le **serveur (hébergeur du site)**.

### 🔁 Le modèle client–serveur

1. Tu tapes une adresse (ex : `https://www.frmf.ma`) dans ton navigateur.
2. Le navigateur (le **client**) envoie une **requête HTTP** au **serveur**.
3. Le serveur reçoit cette requête, trouve la page demandée et renvoie une **réponse HTTP** contenant du code HTML, CSS et JS.
4. Le navigateur lit ce code et affiche la page à l’écran.

---

### 🧩 Schéma du fonctionnement

```
Utilisateur 👩‍💻
    │
    ▼
Navigateur Web 🌐 (Client)
    │   Requête HTTP ➡️
    ▼
Serveur Web 🖥️
    │   Réponse HTTP ⬅️
    ▼
Affichage de la page HTML/CSS/JS 🎨
```

🧠 **En résumé :**

* Le **client** demande → le **serveur** répond.
* Ce dialogue se fait grâce au **protocole HTTP**.

---

## 🚦 4. Le protocole HTTP expliqué simplement

**HTTP** signifie **HyperText Transfer Protocol**.
C’est le **langage de communication du Web** — il définit **comment un navigateur et un serveur échangent des informations**.

### 💬 Exemple simple

Tu veux visiter le site de la Fédération Royale Marocaine de Football :

```
1️⃣ Tu tapes : https://www.frmf.ma
2️⃣ Ton navigateur envoie une requête : 
   "Donne-moi la page d’accueil (index.html)"
3️⃣ Le serveur répond : 
   "Voici ton fichier HTML + ton CSS + ton JS"
4️⃣ Le navigateur affiche le site.
```

---

### 📊 Schéma du protocole HTTP

```
[ 👩‍💻 Toi (Client) ]
        |
        | Requête HTTP (GET)
        v
[ 🌐 Serveur Web ]
        |
        | Réponse HTTP (HTML + CSS + JS)
        v
[ 🖥️ Page affichée dans ton navigateur ]
```

---

### 🧾 Exemple d’une requête HTTP

```
GET /index.html HTTP/1.1
Host: www.frmf.ma
User-Agent: Chrome/124.0
Accept-Language: fr-MA
```

➡️ Cela signifie :

> “Bonjour serveur, je suis Chrome, je veux le fichier `index.html` de ton site.”

### 🧾 Exemple d’une réponse HTTP

```
HTTP/1.1 200 OK
Content-Type: text/html; charset=UTF-8
Content-Length: 1540
```

➡️ Cela signifie :

> “D’accord client, voici ton fichier HTML demandé 👇”

---

## 📈 5. Le Web en chiffres (2025)

Quelques données impressionnantes :

* 🌍 Environ **2 milliards de sites web** existent dans le monde.
* 💻 Plus de **90 % des sites utilisent HTML, CSS et JavaScript**.
* 📱 Environ **75 % du trafic web mondial** vient des smartphones.
* 👨‍💻 Chaque année, plus de **1,8 million d’applications web** sont créées.
* 🇲🇦 Au Maroc, plus de **80 % des entreprises** ont aujourd’hui un site ou une application web.

🧠 **Ce que cela signifie :**
HTML, CSS et JS sont les **langages universels du Web**.
Aucun site ne peut exister sans eux !

---

## 🧱 6. Les 3 langages essentiels du Web

| Langage          | Rôle                     | Exemple                         |
| ---------------- | ------------------------ | ------------------------------- |
| **HTML** 🏗️     | Structure la page        | `<h1>Bienvenue sur le Web</h1>` |
| **CSS** 🎨       | Met en forme la page     | `h1 { color: red; }`            |
| **JavaScript** ⚡ | Rend la page interactive | `alert("Salam Maroc !")`        |

💬 **Exemple concret :**
Quand tu visites une page sur les **Lions de l’Atlas 🦁🇲🇦** :

* le **HTML** affiche le titre et les paragraphes,
* le **CSS** ajoute les couleurs du drapeau,
* le **JavaScript** permet de cliquer sur un bouton “Voir les joueurs”.

---

## 🧠 7. Navigateur et rendu des pages

Le navigateur (Chrome, Firefox, Safari, Edge...)
est le **logiciel qui interprète et affiche** le code reçu.

Il contient :

* un **moteur de rendu** (pour HTML et CSS),
* un **moteur JavaScript**,
* et des **outils développeurs** (F12) pour observer et corriger ton code.

💡 **Astuce pour tes étudiants :**

> Fais un clic droit → “Inspecter” sur n’importe quel site,
> et tu verras le code HTML, CSS et JS en direct 👀.

---

## 🔢 8. Les types de fichiers du Web

| Type de fichier | Extension              | Description                |
| --------------- | ---------------------- | -------------------------- |
| Page web        | `.html`                | Contenu structurel         |
| Style           | `.css`                 | Apparence du site          |
| Script          | `.js`                  | Interactions et animations |
| Image           | `.jpg`, `.png`, `.svg` | Médias                     |
| Données         | `.json`, `.xml`        | Échanges de données        |
| Vidéos / Docs   | `.mp4`, `.pdf`         | Contenus additionnels      |

---

## 🚀 9. Le cycle de création d’un site web

1. **Idée et maquette** 🎨
2. **Structure avec HTML** 🧱
3. **Design avec CSS** 💅
4. **Interactivité avec JavaScript** ⚡
5. **Mise en ligne (hébergement)** 🌍
6. **Maintenance et mises à jour** 🔁

💬 Exemple :
Créer un mini-site sur ton **club marocain préféré** :

* Page HTML → les joueurs et les matchs.
* CSS → couleurs du club.
* JS → bouton “Voir le prochain match”.

---

## 📚 10. À retenir

* Le Web repose sur la communication **client ↔ serveur** via **HTTP**.
* Il existe **3 générations du Web** :

  * Web 1.0 → statique
  * Web 2.0 → social
  * Web 3.0 → intelligent
* Plus de **90 %** des sites utilisent **HTML, CSS, JS**.
* Ces langages sont **indispensables** pour tout développeur web 🌍.
* Le Maroc est aujourd’hui un acteur croissant du numérique et du développement web 🇲🇦.

---

> 💬 *“Comprendre le Web, c’est comprendre comment le monde communique aujourd’hui.”*

---

