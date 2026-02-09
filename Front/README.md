# CodeTogether - Frontend

Application Vue.js 3 avec TypeScript et Vite.

## 🚀 Installation

```sh
npm install
```

## 📋 Commandes disponibles

### Développement

```sh
npm run dev
```

L'application sera accessible sur `http://localhost:5173`

### Production

```sh
npm run build
npm run preview
```

### Tests

```sh
# Tests de composants (headless)
npm run test:unit

# Tests de composants (avec interface)
npm run test:unit:dev

# Tests E2E (headless)
npm run test:e2e

# Tests E2E (avec interface)
npm run test:e2e:dev
```

### Qualité de code

```sh
# Linting
npm run lint

# Vérification TypeScript
npm run type-check
```

## 🗂️ Structure du projet

```
Front/
├── cypress/           # Tests Cypress (E2E et composants)
├── public/            # Assets statiques
└── src/
    ├── assets/
    │   └── styles/    # SCSS global et helpers
    ├── components/
    │   ├── form/      # Composants de formulaire
    │   ├── loader/    # Loaders
    │   ├── structure/ # Layout (Header, Submenu)
    │   └── svg/       # Icônes et logos SVG
    ├── entities/      # Types TypeScript
    ├── helpers/       # Utilitaires
    ├── router/        # Configuration Vue Router
    └── views/         # Pages de l'application
```

## 🎨 Système de design

### Couleurs (définies dans `main.scss`)

| Variable     | Couleur   | Usage              |
| ------------ | --------- | ------------------ |
| `$primary`   | `#58b9ff` | Couleur principale |
| `$secondary` | `#ffbf1d` | Couleur secondaire |
| `$light`     | `#fefefe` | Texte clair        |
| `$dark`      | `#1c1b20` | Fond sombre        |

### Classes utilitaires

- **Display** : `.f`, `.f-col`, `.a-cent`, `.j-betw`
- **Spacing** : `.mb-32`, `.ml-16`, `.p-32-64`
- **Background** : `.bg-dark`, `.bg-primary`, `.br-50`

## 📄 Pages

| Route         | Composant      | Description        |
| ------------- | -------------- | ------------------ |
| `/`           | `HomeView`     | Page d'accueil     |
| `/login`      | `LoginView`    | Connexion          |
| `/register`   | `RegisterView` | Inscription        |
| `/my-profile` | `MyProfile`    | Profil utilisateur |

## 🔧 Configuration IDE

Recommandé : [VSCode](https://code.visualstudio.com/) avec :

- [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar)
- [TypeScript Vue Plugin](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin)

> ⚠️ Désactiver Vetur si installé
