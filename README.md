# 🏛️ COMMERCIUM — Plateforme E-commerce Sacrée & Modulaire

> Alternative libre, vivante et spirituellement alignée à Shopify.  
> Conçu pour les **artisans**, **thérapeutes**, **enseignants** et **créateurs du nouveau monde**.  
> Un projet issu du **SOCLE CODEX SACRÉ** 🌐✨

---

## 📐 Vision

**COMMERCIUM** est une plateforme open-source complète de e-commerce, modulaire, souveraine et pilotée par l’IA.  
Elle s’articule autour de trois pôles sacrés :

- **EMPORIUM** — le cœur e-commerce (frontend & backend)
- **INSTITUUM** — système ERP (gestion produit, commande, stock, clients)
- **ARCHÉTYPES** — assistants IA intégrés et vivants (Ollama, ShellGPT, etc.)

---

## 🧱 Architecture


COMMERCIUM/
├── EMPORIUM/                 # Frontend React (UI, dashboard vendeur)
│   ├── components/           # Composants UI réutilisables
│   ├── pages/                # Pages principales (produits, commandes, etc.)
│   └── form.config.json/     # Configuration des formulaires dynamiques
│
├── BACKEND/                  # Backend FastAPI (API REST + AI)
│   ├── models/               # Modèles Pydantic/SQLModel
│   ├── routes/               # Routes API auto-générées
│   └── scripts/              # Générateurs & synchronisation AI
│
├── ARCHETYPES/               # Agents IA (Ollama, ShellGPT, Watchers)
│   └── samdan.sh             # Watcher silencieux (SAMDĀN)
│
├── docker-compose.yml        # Déploiement unifié
├── sacred-run-all.sh         # Script d’installation et synchronisation sacrée
└── README.md                 # Ce fichier
