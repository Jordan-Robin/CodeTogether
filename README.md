# CodeTogether

CodeTogether est une application web full-stack permettant aux développeurs de collaborer sur des projets. Elle est composée d'un backend Symfony (API Platform) et d'un frontend Vue.js.

## 🏗️ Architecture

```
CodeTogether/
├── Back/          # API Symfony avec API Platform
├── Front/         # Application Vue.js 3
└── .github/       # Workflows CI/CD
```

## 🚀 Démarrage rapide

### Prérequis

- Docker et Docker Compose
- Node.js (v18+)
- npm

### Lancer le projet complet

1. **Backend** (depuis `Back/`)

   ```sh
   docker-compose up -d
   ```

2. **Frontend** (depuis `Front/`)
   ```sh
   npm install
   npm run dev
   ```

## 📚 Documentation

- [Documentation Backend](Back/README.md)
- [Documentation Frontend](Front/README.md)

## 🛠️ Stack technique

| Composant    | Technologies                                  |
| ------------ | --------------------------------------------- |
| **Backend**  | PHP 8, Symfony, API Platform, PostgreSQL, JWT |
| **Frontend** | Vue.js 3, TypeScript, Vite, Cypress           |
| **DevOps**   | Docker, GitHub Actions                        |

## 📝 Licence

Ce projet est sous licence privée.
