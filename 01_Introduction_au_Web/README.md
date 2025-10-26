
## 📁 `01_Introduction_au_Web/README.md`

```markdown
# 🌍 Introduction au Web

## 🎯 Objectifs d’apprentissage
À la fin de cette section, tu seras capable de :
- Expliquer le fonctionnement général du **Web**.
- Décrire la différence entre **Internet** et **le Web**.
- Comprendre les rôles du **client**, du **serveur** et des **navigateurs**.
- Connaître les **technologies de base** du web moderne (HTML, CSS, JS).

---

## 🌐 1. Internet vs Web

| Concept | Définition |
|----------|-------------|
| **Internet** | Un réseau mondial d’ordinateurs connectés. C’est l’infrastructure. |
| **Web (World Wide Web)** | Un service d’Internet qui permet d’échanger et de consulter des pages à travers des **navigateurs**. |

🧠 **Analogie :**  
Internet est une autoroute 🛣️  
Le Web, ce sont les voitures 🚗 qui circulent dessus.  

---

## ⚙️ 2. Comment fonctionne le Web ?

Le Web repose sur un **modèle client-serveur**.

1. Tu entres une adresse (URL) dans ton navigateur.  
2. Le **navigateur (client)** envoie une **requête HTTP** vers un **serveur**.  
3. Le **serveur** renvoie une **réponse** : une page HTML.  
4. Le **navigateur** interprète ce code et l’affiche à l’écran.  

### 🧩 Schéma simplifié

```

[ Navigateur (Client) ] ⇄ [ Serveur ]
↓                    ↑
Requête HTTP       Réponse HTML

```

---

## 🧱 3. Les trois langages fondamentaux du web

| Langage | Rôle | Exemple |
|----------|------|----------|
| **HTML** 🏗️ | Structure la page | `<h1>Bonjour</h1>` |
| **CSS** 🎨 | Met en forme la page | `h1 { color: red; }` |
| **JavaScript** ⚡ | Rend la page interactive | `alert('Salut !')` |

---

## 🌍 4. Le navigateur

Un **navigateur web** est un logiciel qui interprète et affiche le code HTML, CSS et JavaScript.  
Exemples :  
🦊 Firefox, 🌐 Chrome, 🧭 Safari, 🪟 Edge.

### ⚙️ Fonctionnement interne :
- **Moteur de rendu (Render Engine)** → interprète HTML et CSS.  
- **Moteur JavaScript (JS Engine)** → exécute le code JS.  
- **Outils développeurs** (F12) → permettent d’explorer et corriger le code.

---

## 🔤 5. Les langages côté client et côté serveur

| Type | Exemples | Exécuté où ? |
|------|-----------|--------------|
| **Côté client** | HTML, CSS, JS | Dans le navigateur |
| **Côté serveur** | PHP, Node.js, Python, Java | Sur le serveur avant l’envoi de la page |

---

## 🧩 6. Les fichiers du Web

| Type de fichier | Extension | Rôle |
|-----------------|------------|------|
| **Page web** | `.html` | Contenu de la page |
| **Feuille de style** | `.css` | Apparence |
| **Script** | `.js` | Interaction |
| **Image** | `.png`, `.jpg`, `.svg` | Illustrations |
| **Document** | `.pdf`, `.json`, etc. | Ressources complémentaires |

---

## 🧭 7. Les protocoles

### 🔹 HTTP / HTTPS
- **HTTP (HyperText Transfer Protocol)** : le protocole qui fait circuler les pages web.
- **HTTPS** : version sécurisée (avec chiffrement SSL/TLS 🔒).

### 🔹 Autres protocoles utiles
| Protocole | Utilité |
|------------|----------|
| **FTP** | Transfert de fichiers entre ordinateurs |
| **SMTP / IMAP** | Pour les e-mails |
| **WebSocket** | Communication en temps réel |

---

## 🧩 8. Les URLs (Uniform Resource Locator)

Une URL est l’adresse unique d’une ressource sur le Web.

**Exemple :**
```

[https://www.exemple.com/blog/article.html](https://www.exemple.com/blog/article.html)

```

**Détails :**
| Partie | Signification |
|--------|----------------|
| `https` | Protocole |
| `www.exemple.com` | Nom de domaine |
| `/blog/article.html` | Chemin vers le fichier |

---

## 🚀 9. Le cycle de création d’un site web

1. Conception et maquettes 🎨  
2. Création du contenu HTML 🏗️  
3. Mise en forme avec CSS 💅  
4. Ajout d’interactivité (JS) ⚡  
5. Hébergement et déploiement 🌍  
6. Maintenance et évolution 🔁  

---

## 🧠 10. À retenir

- Le **Web** repose sur un échange entre **client** et **serveur**.
- Les **langages fondamentaux** du front-end sont **HTML, CSS, JS**.
- Le **navigateur** traduit ces langages pour afficher une page.
- Le **développement web** mêle logique, design et interaction.

---

> 💬 _“Comprendre le web, c’est comprendre le terrain sur lequel tu construis tes applications.”_
```


