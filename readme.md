# 🌐 E-Arena Championship 2025

Un site web vitrine moderne présentant la compétition e-sport inter-équipes **E-Arena Championship 2025**.  
L’événement regroupe plusieurs jeux majeurs tels que **Valorant**, **League of Legends** et **Counter-Strike 2**, avec un **prize pool de 25 000 €**.

---

## 🧭 Structure du site

Le site est composé de **trois pages principales** :

### 1. `index.html` – Accueil

Page d’introduction à l’événement :

- Présentation du championnat et de ses jeux phares.
- Liens rapides vers les pages _Équipes & Règles_ et _Contact_.
- Section _Highlights_ (dates, jeux, prize pool).
- Galerie de logos des sponsors (Adidas, Coca-Cola, Fifa, Puma, Spotify).
- Design responsive et décorations SVG dynamiques pour un effet futuriste.

### 2. `teams.html` – Équipes & Règles

Page dédiée à la compétition et à ses participants :

- Liste détaillée des **équipes participantes** avec leurs jeux et palmarès.
- Section **Règlement du tournoi** (BO3, fair-play, anti-triche, etc.).
- Conseils stratégiques pour les joueurs (communication, map control, etc.).
- Tableau **Top Rankings** affichant les scores historiques.
- Encadré _Sponsor officiel_ invitant les marques à collaborer.

### 3. `contact.html` – Contact & Recrutement

Page de contact avec formulaire interactif :

- Formulaire de contact complet (nom, email, sujet, message).
- Informations de contact : e-mail, téléphone, adresse, réseaux sociaux.
- Sections additionnelles :
  - **Partenariats**
  - **Media Kit**
  - **FAQ** (exemples de questions fréquentes).

---

## 🛠️ Technologies utilisées

- **HTML5** pour la structure du contenu.
- **CSS3** (fichier `mystyle.css`) pour la mise en forme et le responsive design.
- **Balises sémantiques et ARIA** pour l’accessibilité.
- **Images adaptatives (`<picture>`)** pour la compatibilité mobile.
- **SVG** pour les illustrations vectorielles légères et dynamiques.

---

## 📁 Arborescence du projet

# 🧩 Difficultés rencontrées et solutions

### 1. Compréhension de la balise Open Graph

- **Problème :** J’ai eu des difficultés à comprendre l’Open Graph présent dans les balises meta à l’intérieur du `<head>`.
- **Solution :** L’Open Graph permet d’afficher un aperçu (titre, image, description) de votre site web lorsqu’il est partagé sur les réseaux sociaux comme Facebook ou X (Twitter).
- **Référence :** [https://ahrefs.com/blog/open-graph-meta-tags/](https://ahrefs.com/blog/open-graph-meta-tags/)

---

### 2. Propriété CSS `background-attachment`

- **Problème :** J’ai eu du mal à faire la différence entre les valeurs `fixed`, `local` et `scroll`.
- **Solution :**
  - `fixed` : l’image d’arrière-plan reste fixe lors du défilement.
  - `local` : l’image défile en fonction de l’élément et du conteneur racine.
  - `scroll` : l’image défile uniquement avec la page principale (le root). Si le conteneur a un comportement de défilement interne, l’image restera fixe à l’intérieur.
- **Référence :** [https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment](https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment)

---

### 3. Choisir la bonne image selon le type d’appareil

- **Problème :** J’ai eu des difficultés à choisir la bonne image selon le type ou la taille d’écran de l’appareil.
- **Solution :**  
  Il faut utiliser la balise `<picture>` avec plusieurs balises `<source>`, et placer la balise `<img>` en dernier.  
  Chaque balise `<source>` doit contenir :
  - `srcset` → le lien de l’image
  - `media` → la condition d’affichage (par exemple, afficher cette image si la largeur est inférieure à 444px)
  ```html
  <picture>
    <source srcset="small.jpg" media="(max-width: 444px)" />
    <source srcset="large.jpg" media="(min-width: 445px)" />
    <img src="default.jpg" alt="exemple" />
  </picture>
  ```
