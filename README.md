# Climatisation LOL — Site web

Site vitrine statique (HTML / CSS / JS, aucun cadre requis) pour Climatisation LOL.
Spécialiste de la réparation et de l'installation de thermopompes et unités de
climatisation résidentielles — Louis-Olivier Lorrain · 514 601-2546.

## Structure

| Fichier | Rôle |
|---|---|
| `index.html` | Le site complet (tout est dans un seul fichier : HTML + CSS + JS) |
| `climatisation-lol.html` | Copie de travail identique (peut être supprimée) |
| `.gitignore` | Fichiers ignorés par Git |

## Développement local

Aucune installation nécessaire. Ouvre simplement `index.html` dans un navigateur.
Pour un aperçu avec petit serveur local :

```bash
# Python (déjà installé sur Mac)
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```

## Pousser une modification

```bash
git add .
git commit -m "Décris ta modification ici"
git push
```

## Déploiement — Hostinger (auto-deploy Git)

1. hPanel → **Avancé → Git**
2. Coller l'URL du dépôt, branche `main`, répertoire cible `public_html`
3. Copier l'**URL de webhook** fournie par Hostinger
4. GitHub → dépôt → **Settings → Webhooks → Add webhook**
   - Payload URL : l'URL de webhook Hostinger
   - Content type : `application/x-www-form-urlencoded`
5. Chaque `git push` sur `main` met le site en ligne automatiquement.

## Déploiement — alternative gratuite (Cloudflare Pages / GitHub Pages)

- **Cloudflare Pages** : connecter le dépôt GitHub, framework « None », build command vide,
  output `/`. Déploiement auto à chaque push, HTTPS + domaine perso inclus.
- **GitHub Pages** : dépôt → Settings → Pages → source `main` / `root`.

## À personnaliser avant mise en ligne

- [ ] Numéro RBQ dans le pied de page (placeholder `0000-0000-00`)
- [ ] Courriel de contact (`info@climatisationlol.ca` — à confirmer)
- [ ] Remplacer les images/vidéo de démo par les vraies photos (page Facebook)
- [ ] Brancher le fil Facebook (plugin officiel gratuit) et les avis Google (curés ou widget)
- [ ] Ajuster la liste des villes desservies si nécessaire

## Intégrations (notes dans le code)

Des commentaires `NOTE INTÉGRATION` dans `index.html` indiquent exactement où
brancher le fil Facebook et les avis Google.
