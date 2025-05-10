
---


# 🧮 Calculatrice JavaScript Simple

Bienvenue dans ce projet de **calculatrice basique** construite avec **HTML**, **CSS** et **JavaScript**. Ce projet montre comment créer une interface simple pour effectuer des opérations mathématiques de base (+, −, ×, ÷).

---

## 📄 Structure du fichier HTML

### 🧠 En-tête du document

```html
<!DOCTYPE html>
````

🔧 Indique que ce fichier utilise **HTML5**.

```html
<html>
```

🌐 Ouvre la balise principale du document HTML.

```html
<head>
  <title>Simple Calculator</title>
```

🧩 Le titre de l’onglet du navigateur : *Simple Calculator*.

---

## 🎨 Style CSS intégré

```html
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
    padding: 20px;
  }
```

🖋️ Le corps de la page utilise la police **Arial**, centre le texte, et applique une marge intérieure de `20px`.

```css
  #display {
    width: 200px;
    height: 40px;
    font-size: 20px;
    margin-bottom: 10px;
    border: 1px solid #333;
    padding: 10px;
    background: #f0f0f0;
    display: inline-block;
  }
```

📺 Le `div` d’affichage :

* Taille : 200x40px
* Texte en **20px**
* Bordure grise
* Fond clair
* Comportement en ligne pour aligner les éléments

```css
  .btn {
    padding: 10px 20px;
    margin: 5px;
    font-size: 18px;
    cursor: pointer;
  }
</style>
```

🖲️ Style des boutons :

* Espacement intérieur (padding)
* Marge extérieure
* Texte en 18px
* Curseur en forme de **main** lors du survol

---

## 🧱 Corps de la page

```html
<body>
  <h2>🧮 Basic JS Calculator</h2>
  <div id="display"></div>
  <br />
```

🖥️ Titre de la page et zone d’affichage (`display`) des opérations.

---

### 🧮 Les boutons de chiffres et d’opérations

```html
<button class="btn" onclick="append('1')">1</button>
...
<button class="btn" onclick="append('+')">+</button>
...
<button class="btn" onclick="clearDisplay()">C</button>
<button class="btn" onclick="calculate()">=</button>
```

📌 Chaque bouton :

* Utilise une classe CSS `btn`
* Appelle une fonction JavaScript lorsqu’on clique dessus

  * `append()` pour ajouter un chiffre ou un symbole
  * `clearDisplay()` pour réinitialiser l’écran
  * `calculate()` pour exécuter le calcul

---

## ⚙️ Script JavaScript

```html
<script>
  function append(value) {
    document.getElementById("display").innerHTML += value;
  }
```

🧩 La fonction `append()` ajoute le chiffre ou symbole au contenu du `display`.

```javascript
  function clearDisplay() {
    document.getElementById("display").innerHTML = "";
  }
```

🧼 La fonction `clearDisplay()` vide complètement l’écran.

```javascript
  function calculate() {
    let display = document.getElementById("display");
    display.innerHTML = eval(display.innerHTML) || "Error";
  }
</script>
```

🧠 La fonction `calculate()` :

* Utilise la fonction **`eval()`** pour évaluer l’expression mathématique saisie
* Si le calcul échoue, affiche **"Error"**

⚠️ **Attention : `eval()` peut poser des risques de sécurité si des entrées non sécurisées sont utilisées.**

---

## ✅ Fonctionnalités

* 📱 Interface simple
* ➕➖✖️➗ Opérations de base
* 🔄 Réinitialisation
* 🟰 Résultat immédiat

---

## 💡 Améliorations possibles

* ✅ Remplacer `eval()` par un **parser** sécurisé
* 💅 Ajouter un design responsive (adapté aux mobiles)
* 🔢 Ajouter des touches clavier

---

## 🚀 Aperçu

Une calculatrice web simple et élégante pour apprendre les bases de la manipulation DOM et des événements en JavaScript.

---

## 🧠 Technologies utilisées

* HTML5 🧾
* CSS3 🎨
* JavaScript 🧠

---


---

