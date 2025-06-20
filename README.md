# TP 352 Dockerisé

##  Table des matières
- [Pré-requis](#pré-requis)
- [Installation](#installation)
- [Lancement de l'application](#lancement-de-lapplication)
- [Tests](#tests)
- [URLs locales](#urls-locales)
- [Structure du projet](#structure-du-projet)

## 🔧 Pré-requis

Assurez-vous d'avoir installé les outils suivants sur votre machine :
- [Docker](https://www.docker.com/) - Plateforme de conteneurisation
- [Docker Compose](https://docs.docker.com/compose/) - Outil d'orchestration multi-conteneurs
- [Git](https://git-scm.com/) - Système de contrôle de version

##  Installation

### Clonage du projet
```bash
git clone https://github.com/sandjonyves/tp_gl_groupe7-back_front.git
cd tp_gl_groupe7-back_front
```

##  Lancement de l'application

### Avec Docker Compose (recommandé)
```bash
docker compose up --build
```

Cette commande va :
- Construire les images Docker pour le frontend et le backend
- Démarrer tous les services nécessaires
- Configurer la communication entre les conteneurs

### Arrêt de l'application
```bash
docker compose down
```

##  Tests

### Tests Backend
```bash
# Naviguer vers le dossier backend
cd backend

# Tests unitaires
npm run test:unit

# Tests d'intégration
npm run test:integration
```

### Tests Frontend
```bash
# Naviguer vers le dossier frontend
cd frontend

# Tests end-to-end
npm run test:e2e
```

##  URLs locales

Une fois l'application lancée, vous pouvez accéder aux services suivants :

- **Frontend** : [http://localhost:3000](http://localhost:3000)
- **Backend API** : [http://localhost:3001](http://localhost:3001)

##  Structure du projet

```
tp_gl_groupe7-back_front/
├── .github/           # CI/CD
├── backend/           # API Backend
├── frontend/          # Interface utilisateur
├── docker-compose.yml # Configuration Docker Compose
└── README.md         # Documentation du projet
```

## 📝 Notes

- Assurez-vous que les ports 3000 et 3001 ne sont pas utilisés par d'autres applications
- Le projet utilise Docker Compose pour orchestrer les services frontend et backend
- Les tests doivent être exécutés dans leurs répertoires respectifs (backend/frontend)