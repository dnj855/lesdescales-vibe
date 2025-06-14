# 🎲 Site Vitrine de l'Association Les Dés'Calés

Bienvenue dans le dépôt du site officiel de l'association Les Dés'Calés !  
Ce site présente l'association, ses événements, sa galerie photo, et son festival annuel.

---

## 🧱 Stack technique

Ce projet est basé sur une architecture **moderne, performante et gratuite** :

| Partie          | Technologie utilisée                       | Rôle principal                               |
| --------------- | ------------------------------------------ | -------------------------------------------- |
| Frontend        | [Next.js](https://nextjs.org)              | Affichage du site, navigation, SEO           |
| Backend (CMS)   | [Strapi](https://strapi.io) (headless CMS) | Gestion des contenus (événements, images...) |
| Base de données | SQLite intégrée à Strapi                   | Stockage local simple                        |
| Hébergement     | Vercel + Render                            | Déploiement gratuit et automatisé            |

---

## 🗂️ Organisation du projet

```
lesdescales-vibe/
├── frontend/       # Application Next.js (le site web public)
├── backend/        # Application Strapi (CMS pour la gestion de contenu)
├── .gitignore
└── README.md
```

### ➤ `/frontend`

Contient le **site web visible par les visiteurs** :

- Pages dynamiques (accueil, événements, festival…)
- Composants d'affichage
- Connexion API à Strapi

### ➤ `/backend`

Contient le **CMS Strapi** (interface d’administration) :

- Collections configurées : événements, galeries, éditions de festivals
- Rôles et permissions des utilisateurs
- Médias uploadés (images)

---

## 🛠️ Installation locale (développeur)

> Pré-requis : Node.js ≥ 18, Git, Yarn ou npm

```bash
# Clone du repo
git clone https://github.com/votre-org/association-site.git
cd association-site

# Lancer Strapi (backend)
cd backend
npm install
npm run develop
# Interface admin disponible sur http://localhost:1337/admin

# Dans un autre terminal : lancer le frontend
cd ../frontend
pnpm install
pnpm run dev
# Site web accessible sur http://localhost:3000
```

> Pensez à créer un fichier `.env.local` dans `frontend/` avec :  
> `NEXT_PUBLIC_STRAPI_API_URL=http://localhost:1337/api`

## 🚀 Déploiement (automatisé)

### Frontend (Next.js)

- Hébergé sur [Vercel](https://vercel.com)
- Mise à jour automatique à chaque push Git

### Backend (Strapi)

- Hébergé sur [Render](https://render.com)
- Accès sécurisé, base de données incluse

### Webhook (optionnel)

- Déclenchement automatique du rebuild du frontend à chaque mise à jour de contenu

---

## ✉️ Contact / formulaire

Le formulaire de contact fonctionne via **FormSubmit** (sans backend)  
Les messages sont envoyés par email à l'association.

---

## 📸 Gestion des médias

- Les images sont uploadées directement depuis Strapi
- Le site les optimise automatiquement via Next.js (`next/image`)

---

## 🧩 Licence

Projet libre, open-source, sous licence MIT.  
Crée avec ❤️ pour promouvoir les jeux de société !
