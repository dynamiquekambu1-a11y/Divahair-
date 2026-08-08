# Divahair — Site vitrine

Site vitrine multi-pages pour le salon **Divahair**, 132 Church Street, Pietermaritzburg CBD.

## 📁 Structure du projet

```
divahair-site/
├── index.html        # Page d'accueil
├── services.html      # Services & tarifs
├── gallery.html        # Galerie photos
├── reviews.html         # Avis clients
├── contact.html          # Contact & réservation
├── style.css               # Feuille de style partagée
├── script.js                 # Menu mobile (burger)
└── images/
    ├── gallery-1.jpg    # Photos de la galerie (à remplacer)
    ├── gallery-2.jpg
    ├── gallery-3.jpg
    ├── gallery-4.jpg
    └── gallery-5.jpg
```

## 🚀 Publier le site avec GitHub Pages

1. Crée un nouveau dépôt sur GitHub (ex : `divahair-site`).
2. Ajoute tous les fichiers de ce dossier à la racine du dépôt (garde la structure telle quelle, notamment le dossier `images/`).
3. Pousse le code :
   ```bash
   git init
   git add .
   git commit -m "Site Divahair"
   git branch -M main
   git remote add origin https://github.com/TON-COMPTE/divahair-site.git
   git push -u origin main
   ```
4. Dans le dépôt GitHub → **Settings** → **Pages** → Source : sélectionne la branche `main` et le dossier `/ (root)`.
5. Le site sera en ligne à une adresse du type :
   `https://TON-COMPTE.github.io/divahair-site/`

## 🌐 Publier sur Render (site statique — pas de requirements.txt)

Ce site est en HTML/CSS pur, donc **aucun `requirements.txt` ni backend Python n'est nécessaire**. Sur Render, choisis bien le type **"Static Site"** (et non "Web Service") :

1. Pousse d'abord ce dossier complet sur un dépôt GitHub (racine du dépôt, dossier `images/` inclus).
2. Sur [render.com](https://render.com), clique sur **New +** → **Static Site**.
3. Connecte ton compte GitHub et sélectionne le dépôt.
4. Render détecte automatiquement le fichier `render.yaml` inclus ici — les champs **Build Command** (vide) et **Publish Directory** (`./`) se remplissent seuls. Sinon, remplis-les manuellement :
   - Build Command : *(laisser vide)*
   - Publish Directory : `.`
5. Clique sur **Create Static Site**. Render déploie en 1-2 minutes et donne une URL du type `divahair-site.onrender.com`.

⚠️ Si Render affiche un formulaire "Web Service" avec Python/Node/Docker, c'est le mauvais type — reviens en arrière et choisis bien **"Static Site"**.

## ✏️ Personnalisation rapide

- **Photos** : remplace `images/gallery-1.jpg` à `gallery-5.jpg` par tes vraies photos (garde les mêmes noms de fichiers, ou modifie les `src` dans `gallery.html`).
- **Prix** : modifie les montants dans `services.html` (recherche `<div class="tag-price">`).
- **Avis clients** : modifie les textes dans `reviews.html`.
- **Coordonnées** : téléphone, email, adresse et horaires sont dans le pied de page (`footer`) de chaque fichier `.html`, ainsi que dans `contact.html`.
- **Formulaire de contact** : actuellement visuel uniquement. Pour qu'il envoie vraiment des emails, connecte-le à un service comme [Formspree](https://formspree.io) ou [EmailJS](https://www.emailjs.com/) (gratuit pour un usage simple).

## 🎨 Palette & typographie

- Couleurs : bleu roi `#0F3D91`, bleu vif `#1E88E5`, blanc, doré `#E8B94B`
- Polices : **Baloo 2** (titres) + **Nunito** (texte courant) — via Google Fonts
