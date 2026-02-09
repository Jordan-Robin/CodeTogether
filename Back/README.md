# CodeTogether - Backend

API REST construite avec Symfony et API Platform.

## 🚀 Installation

### Avec Docker (recommandé)

```sh
docker-compose up -d
```

L'API sera accessible sur `https://localhost:5001/api`

### Configuration

Les variables d'environnement sont définies dans :

- `.env` - Configuration par défaut
- `.env.test` - Configuration pour les tests

## 📋 Commandes utiles

### Base de données

```sh
# Exécuter les migrations
docker-compose exec api symfony console doctrine:migrations:migrate

# Charger les fixtures
docker-compose exec api symfony console doctrine:fixtures:load
```

### Tests

```sh
# Lancer les tests PHPUnit
docker-compose exec api ./vendor/bin/phpunit

# Analyse statique avec PHPStan
docker-compose exec api ./vendor/bin/phpstan analyse
```

### Qualité de code

```sh
# PHP CS Fixer
docker-compose exec api ./vendor/bin/php-cs-fixer fix
```

## 🗂️ Structure du projet

```
Back/
├── config/          # Configuration Symfony
├── migrations/      # Migrations Doctrine
├── public/          # Point d'entrée web
├── src/
│   ├── DataFixtures/  # Fixtures de test
│   ├── Entity/        # Entités Doctrine
│   └── Repository/    # Repositories
├── tests/           # Tests PHPUnit
└── docker/          # Configuration Docker
```

## 🔐 Authentification

L'API utilise JWT pour l'authentification :

- `POST /api/register` - Inscription
- `POST /api/auth` - Connexion (retourne un token JWT)

## 📊 Entités principales

| Entité            | Description                                         |
| ----------------- | --------------------------------------------------- |
| `User`            | Utilisateur avec email et mot de passe              |
| `Profile`         | Profil utilisateur (pseudo, liens, description)     |
| `Speciality`      | Spécialités disponibles (Front-end, Back-end, etc.) |
| `SpecialityLevel` | Niveau de compétence par spécialité                 |
| `Technology`      | Technologies disponibles                            |
| `TechnologyLevel` | Niveau de compétence par technologie                |

## 🐳 Docker

Le projet utilise un Dockerfile multi-stage avec :

- **base** : Image PHP Alpine avec extensions nécessaires
- **development** : Inclut Xdebug et outils de développement

Port exposé : `5001`
