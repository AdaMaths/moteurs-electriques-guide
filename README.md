# MotoGuide — Tout comprendre sur les moteurs électriques

Site web didactique, en français, dédié aux maintenanciers et étudiants pour comprendre
les moteurs synchrones, asynchrones triphasés et monophasés : constitution, fonctionnement,
pannes, bobinage, couplage étoile/triangle, formules et quiz.

Site statique en un seul fichier (`index.html`), sans dépendance ni build : HTML/CSS/JS
pur, mobile-first. Il suffit de l'ouvrir dans un navigateur ou de l'héberger tel quel.

## 🚀 Aperçu local

Ouvrez simplement `index.html` dans un navigateur, ou lancez un petit serveur local
(utile pour que les polices Google Fonts et le comportement se rechargent bien) :

```bash
python3 -m http.server 8000
# puis ouvrez http://localhost:8000
```

## 📦 Structure du dépôt

```
moteurs-electriques-guide/
├── index.html          # Le site complet (HTML + CSS + JS intégrés)
├── README.md
└── .gitignore
```

## 🐙 Héberger sur GitHub

1. Créez un nouveau dépôt sur GitHub, par exemple `moteurs-electriques-guide`
   (public, sans README ni licence pré-cochés puisque ce dossier les contient déjà).
2. Dans PyCharm : **VCS → Create Git Repository…** sur ce dossier, puis
   **Git → Add** pour ajouter tous les fichiers.
3. Premier commit et envoi vers GitHub :

   ```bash
   git init
   git add .
   git commit -m "Site MotoGuide - moteurs électriques"
   git branch -M main
   git remote add origin https://github.com/AdaMaths/moteurs-electriques-guide.git
   git push -u origin main
   ```

   (Dans PyCharm, ces mêmes actions sont accessibles via le menu **Git** en haut à
   droite : *Commit*, puis *Push*, après avoir renseigné le dépôt distant dans
   **Git → Manage Remotes**.)

## 🌍 Déployer avec GitHub Pages (gratuit)

1. Sur GitHub, ouvrez le dépôt → **Settings** → **Pages** (menu de gauche).
2. Sous **Build and deployment**, choisissez **Source : Deploy from a branch**.
3. Sélectionnez la branche **main** et le dossier **/ (root)**, puis **Save**.
4. Après 1 à 2 minutes, le site est en ligne à l'adresse :

   ```
   https://AdaMaths.github.io/moteurs-electriques-guide/
   ```

Chaque nouveau `git push` sur `main` republie automatiquement le site.

## ✏️ Modifier le contenu

Tout est dans `index.html` :
- Les styles sont dans la balise `<style>` en tête de fichier (variables CSS en haut :
  `--navy`, `--blue`, `--copper`, etc.).
- Le contenu de chaque section est dans les balises `<section id="...">`.
- La navigation, la recherche et le quiz sont pilotés par le `<script>` en bas de fichier
  (tableaux `navData`, `searchIndex`, `quizData`).

---
© 2026 Adama GUEYE. Tous droits réservés.
Portfolio professionnel — Physique Numérique & Maintenance Électromécanique.
adama.gueye.3304@gmail.com · github.com/AdaMaths
