# Site développeur DrinkAware

Ce dossier sert à héberger le site développeur pour **AdMob** et **Google Play**. Il doit être poussé dans un **nouveau dépôt GitHub** séparé, puis activé en GitHub Pages.

## Contenu

- **app-ads.txt** : requis par AdMob pour valider l’application
- **index.html** : page d’accueil minimale du site

## Étapes à suivre

### 1. Créer un nouveau dépôt sur GitHub

1. Va sur [github.com/new](https://github.com/new)
2. **Repository name** : par ex. `drinkaware-website` ou `drinkaware-app` (sans espace, minuscules)
3. **Public**, sans README, sans .gitignore
4. Clique sur **Create repository**

### 2. Pousser le contenu de ce dossier

Dans un terminal, depuis ton projet SobrietyTracker :

```bash
cd developer-website
git init
git add app-ads.txt index.html README.md
git commit -m "Site développeur DrinkAware + app-ads.txt"
git branch -M main
git remote add origin https://github.com/darchevert/drinkaware-website.git
git push -u origin main
```

### 3. Activer GitHub Pages

1. Dans le dépôt sur GitHub : **Settings** → **Pages**
2. **Source** : **Deploy from a branch**
3. **Branch** : `main` → **/ (root)** → **Save**
4. Attends 1–2 minutes. L’URL du site sera :

   **https://darchevert.github.io/drinkaware-website/**

### 4. Vérifier app-ads.txt

Ouvre dans le navigateur :

**https://darchevert.github.io/drinkaware-website/app-ads.txt**

Tu dois voir la ligne :

```
google.com, pub-5218071664586608, DIRECT, f08c47fec0942fa0
```

### 5. Renseigner l’URL dans Google Play Console

1. [Google Play Console](https://play.google.com/console) → ton app **DrinkAware**
2. **Présence sur le Play Store** → **Fiche de présentation de l’application**
3. Champ **Site Web du développeur** :  
   **https://darchevert.github.io/drinkaware-website**  
   (sans `/app-ads.txt`, sans slash final)
4. Enregistre

### 6. Relancer la validation AdMob

1. AdMob → **Valider l’application** pour DrinkAware (Android)
2. Clique sur **Rechercher des mises à jour**
3. La validation peut prendre quelques minutes

---

**Important :** L’URL du site développeur (Play Console et AdMob) doit être exactement : **https://darchevert.github.io/drinkaware-website**
