# Projet Kongo — Site statique

Ce dépôt contient un site statique (fichiers HTML/CSS). Ci-dessous les étapes pour héberger et protéger votre site.

## 1) Préparer le dépôt local
- Vérifiez que tous les fichiers du site sont dans le dossier du projet (ex: `accueil.html`, `presentation.html`, ...).
- Le dépôt contient déjà `.gitignore`.

Pour initialiser / committer localement :

```
git init
git add .
git commit -m "Initial commit: site files"
```

## 2) Créer le dépôt GitHub et pousser
1. Sur GitHub, créez un nouveau repository.
2. Pour garder le code privé (empêche l'accès public au code source) : cochez **Private** lors de la création.
3. Ensuite, exécutez :

```
git remote add origin https://github.com/VOTRE_UTILISATEUR/NOM_REPO.git
git branch -M main
git push -u origin main
```

> Remarque : si vous n'avez pas configuré d'authentification, créez un Personal Access Token (PAT) et utilisez-le comme mot de passe lors du `git push`.

## 3) Hébergement et protection d'accès
Options sécurisées pour rendre l'accès au site restreint :

- Option A — Garder le repo GitHub **privé** : le code source est protégé. Si vous voulez un site accessible uniquement par des personnes précises, donnez-leur accès au dépôt (collaborateurs). Note : GitHub Pages rend le site public si activé pour un repo public.

- Option B — Déployer sur un service qui supporte la protection d'accès (recommandé si vous voulez un site public derrière une authentification) :
  - Netlify : possibilité d'ajouter authentification via Netlify Identity ou via des règles/proxy (ou Netlify Business pour mot de passe natif). 
  - Vercel : offre des protections par mot de passe au niveau des déploiements (plans payants). 
  - Cloudflare Access : protège n'importe quel site (grâce à un domaine et Cloudflare) et permet d'exiger une connexion GitHub/Google.

Je peux vous guider pas-à-pas pour choisir et configurer l'une de ces options.

## 4) Si vous voulez un lien protégé maintenant
Je ne peux pas créer le dépôt GitHub ou déployer sur Netlify/Vercel sans vos identifiants ou autorisation d'accès (token). Dites-moi :

- Préférez-vous que je :
  1. Crée le dépôt GitHub à votre place (vous devez me fournir un PAT avec permissions repo), ou
  2. Vous fournisse les commandes et instructions pas-à-pas pour que vous le fassiez (plus sûr), ou
  3. Déploie sur Netlify/Vercel/Cloudflare (je vous guide pour créer un compte et me donner temporairement l'accès si vous voulez que je le fasse).

## 5) Bonnes pratiques pour éviter le vol de contenu
- Gardez le repo privé pour protéger le code source.
- Ne mettez jamais de secrets (mot de passe, clés) dans des fichiers du dépôt ; utilisez `.env` et variables d'environnement sur la plateforme d'hébergement.
- Si vous devez restreindre l'accès au site public, utilisez une couche d'authentification côté serveur (Netlify/Vercel/Cloudflare Access), pas un simple script JavaScript côté client (peu sécurisé).

---

Si vous voulez, je peux maintenant :

- initialiser le commit local (je l'effectue ici),
- puis vous montrer exactement les commandes pour créer le repo GitHub privé et pousser le code, ou
- créer et pousser le repo pour vous si vous fournissez un PAT.

Dites-moi quelle option vous préférez.