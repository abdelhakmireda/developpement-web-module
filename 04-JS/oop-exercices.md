
Voici **une série d’exercices OOP complets et progressifs** pour **maîtriser l’Orienté Objet (OOP)**, avec **encapsulation, héritage, polymorphisme et abstraction**.
Je te conseille de les faire **dans l’ordre** et **sans regarder la solution au début**.

---

## 🟢 EXERCICE 1 – Encapsulation (Bases)

### Objectif

Comprendre **private / public**, **getters / setters**, et la protection des données.

### Énoncé

Créer une classe `CompteBancaire` avec :

* attributs **privés** :

  * `titulaire`
  * `solde`
* méthodes publiques :

  * `deposer(montant)`
  * `retirer(montant)`
  * `getSolde()`
  * `getTitulaire()`

### Règles

* Le solde ne doit **jamais être négatif**
* Impossible de modifier `solde` directement

👉 **Test** :
Créer un compte, déposer 1000, retirer 300, afficher le solde.

---

## 🟢 EXERCICE 2 – Encapsulation + Validation

### Objectif

Sécuriser les données via setters.

### Énoncé

Créer une classe `Utilisateur` :

* `nom` (string)
* `email` (string)
* `age` (int)

### Règles

* âge ≥ 18
* email doit contenir `@`
* utiliser **setters avec validation**

👉 **Test** :
Créer un utilisateur invalide → afficher une erreur.

---

## 🟡 EXERCICE 3 – Héritage

### Objectif

Réutilisation du code.

### Énoncé

Créer une classe `Personne` :

* `nom`
* `prenom`
* `sePresenter()`

Créer une classe `Etudiant` qui **hérite** de `Personne` :

* `niveau`
* `sePresenter()` personnalisé

👉 **Test** :
Créer une personne et un étudiant.

---

## 🟡 EXERCICE 4 – Polymorphisme

### Objectif

Même méthode, comportements différents.

### Énoncé

Créer une classe `Animal` avec :

* méthode `crier()`

Créer :

* `Chien` → "Je aboie"
* `Chat` → "Je miaule"

👉 **Test** :
Mettre les animaux dans un tableau et appeler `crier()`.

---

## 🟠 EXERCICE 5 – Abstraction

### Objectif

Forcer l’implémentation.

### Énoncé

Créer une classe abstraite `Forme` :

* méthode abstraite `calculerSurface()`

Créer :

* `Rectangle`
* `Cercle`

👉 **Test** :
Calculer les surfaces.

---

## 🔴 EXERCICE 6 – OOP COMPLET (PROJET MINI)

### 🎯 Projet : **Système de Gestion d’École**

### Classes à créer

1️⃣ `Personne` (abstraite)

* nom
* email
* méthode `sePresenter()`

2️⃣ `Etudiant`

* niveau
* notes[]
* calculerMoyenne()

3️⃣ `Professeur`

* specialite
* salaire

4️⃣ `Ecole`

* listePersonnes
* ajouterPersonne()
* afficherTout()

### Concepts obligatoires

✅ Encapsulation
✅ Héritage
✅ Polymorphisme
✅ Abstraction

---

## 💡 Conseils pour bien maîtriser OOP

* Toujours penser : **qui possède quoi ?**
* Les attributs = **private**
* Les actions = **public**
* Une classe = **une responsabilité**

---


