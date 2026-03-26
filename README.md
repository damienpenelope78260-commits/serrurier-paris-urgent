# Serrurier Paris Urgent — Site MVP

## Stack
- HTML/CSS statique (aucun framework)
- Formspree pour la capture de leads
- Vercel pour l'hébergement (gratuit)

## Fichiers
- index.html — page principale
- merci.html — page de confirmation après soumission du formulaire
- politique-confidentialite.html — RGPD
- mentions-legales.html — mentions légales
- vercel.json — config Vercel

## Déploiement sur Vercel

### Étape 1 — Créer un compte Formspree
1. Aller sur https://formspree.io
2. Créer un compte gratuit
3. Créer un nouveau formulaire → copier l'ID (ex: xrgvopqb)
4. Dans index.html, remplacer : https://formspree.io/f/VOTRE_ID_FORMSPREE
   par : https://formspree.io/f/xrgvopqb (ou ton ID réel)

### Étape 2 — Déployer sur Vercel
Option A (recommandée) — Via GitHub :
1. Créer un repo GitHub (ex: serrurier-paris-urgent)
2. Pousser ces fichiers dans le repo
3. Connecter le repo à Vercel (vercel.com → New Project → Import Git Repo)
4. Cliquer Deploy

Option B — Via Vercel CLI :
```bash
npm i -g vercel
vercel login
vercel --prod
```

### Étape 3 — Configurer le domaine custom
1. Acheter serrurier-paris-urgent.fr sur OVH ou Namecheap (~10-15€/an)
2. Dans Vercel → Settings → Domains → ajouter serrurier-paris-urgent.fr
3. Configurer les DNS chez le registrar :
   - Type A → 76.76.21.21
   - OU CNAME www → cname.vercel-dns.com

### Étape 4 — Remplir les informations manquantes
Dans mentions-legales.html :
- Remplacer [NOM / SOCIÉTÉ À COMPLÉTER] par ton nom ou ta société
- Remplacer [ADRESSE À COMPLÉTER] par ton adresse

Dans index.html :
- Remplacer +33100000000 par le vrai numéro du serrurier artisan

## Leads reçus
- Les leads arrivent par email via Formspree
- Configurer un Google Sheets webhook si besoin de suivi centralisé

## Modèle économique
- Location du site à un artisan serrurier : 300-400€/mois
- L'artisan reçoit tous les leads directement
