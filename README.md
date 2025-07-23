╔════════════════════════════════════════════════════════════════════╗
║                        🏛️ EMPORIUM - COMMERCIUM SACRÉ             ║
║                       Alternative libre à Shopify                 ║
║            E-commerce modulaire • React • FastAPI • Docker        ║
╚════════════════════════════════════════════════════════════════════╝

📁 Arborescence du projet
───────────────────────────
EMPORIUM/
├── backend/                   → FastAPI + Pydantic
│   ├── app/
│   │   ├── api/               → Endpoints organisés par domaine
│   │   ├── core/              → Configurations (settings, security)
│   │   ├── db/                → Connexion DB, modèles SQLModel
│   │   ├── schemas/           → Pydantic models
│   │   └── services/          → Logique métier
│   └── main.py                → Entrée FastAPI
│
├── frontend/                  → React + TypeScript + Vite
│   ├── public/                → Statics (favicon, index.html)
│   ├── src/
│   │   ├── assets/            → Images, logos, fractals
│   │   ├── components/        → UI composants réutilisables
│   │   │   ├── ui/            → Boutons, cartes, tableaux
│   │   ├── context/           → Providers (auth, theme)
│   │   ├── hooks/             → Custom hooks
│   │   ├── lib/               → Clients API, fonctions helpers
│   │   ├── pages/             → Pages principales (dashboard, auth)
│   │   ├── routes/            → Définition des routes
│   │   └── main.tsx          → Entrée React
│   └── vite.config.ts         → Config Vite
│
├── docker/
│   ├── Dockerfile.frontend
│   ├── Dockerfile.backend
│   └── docker-compose.yml     → Orchestration globale
│
├── .env.example               → Variables d’environnement
└── README.md                  → Ce fichier

🧠 Fonctionnalités principales
───────────────────────────────
- 🛍️ Gestion produits, coupons, stats, utilisateurs
- ⚙️ Système modulaire : chaque domaine = 1 module (ex. /products, /orders)
- 🧩 API RESTful générée automatiquement (Pydantic ↔ Zod)
- 🧠 AI Tools : ShellGPT, Ollama intégrables
- 🧪 Support formulaires dynamiques JSON (form.config.json ↔ Pydantic)
- 🌐 Déploiement full stack via Docker
- 🔐 Authentification avec cookies + tokens
- 📊 Dashboard analytique

📐 Diagramme fonctionnel global
────────────────────────────────

             ┌───────────────┐
             │ Utilisateur   │
             └──────┬────────┘
                    │
                    ▼
             ┌───────────────┐
             │   Frontend    │  ← React / Vite
             └──────┬────────┘
                    │
                    ▼
             ┌───────────────┐
             │    API        │  ← FastAPI / REST
             └──────┬────────┘
                    │
                    ▼
             ┌───────────────┐
             │    DB         │  ← SQLite / PostgreSQL
             └───────────────┘

📦 Modules du frontend
────────────────────────
- ProductTable.tsx → Liste des produits
- CouponForm.tsx → Création/édition de coupons
- StatCard.tsx → Cartes de statistiques
- AuthProvider.tsx → Gestion du contexte utilisateur
- useAuth.ts → Hook d’authentification
- api.ts → Client Axios

📦 Modules du backend
────────────────────────
- routes/products.py → GET/POST/PUT/DELETE produits
- schemas/product.py → Modèle produit (Pydantic)
- models/product.py → Modèle SQLModel produit
- core/config.py → Variables d’environnement
- main.py → Instance FastAPI
- services/product_service.py → Logique produit

🛠️ Lancement du projet (mode développement)
─────────────────────────────────────────────

1. Crée `.env` à partir de `.env.example`
2. Lancer avec Docker :

```bash
docker-compose up --build
