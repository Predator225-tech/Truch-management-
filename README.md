# Transport Mada

Plateforme de gestion de transport routier de marchandises à Madagascar.

## Phase 0 — initialisation

### Prérequis

- Docker et Docker Compose
- Pour lancer hors Docker : Java 21, Maven 3.9+, Node.js 20+

### Démarrage avec Docker

```bash
cp .env.example .env
# Modifiez POSTGRES_PASSWORD dans .env pour votre environnement.
docker compose up --build
```

Le frontend est disponible sur <http://localhost:5173>, l’API sur <http://localhost:8080/api/health> et Swagger sur <http://localhost:8080/swagger-ui.html>. Le frontend affiche l’état de santé de l’API.

### Démarrage local

L’endpoint de santé n’utilise pas encore la base de données.

```bash
cd backend && mvn spring-boot:run
```

Dans un autre terminal :

```bash
cd frontend && npm install && npm run dev
```

Pour les vérifications : `cd backend && mvn test` et `cd frontend && npm install && npm test && npm run build`.

Le profil Spring `dev` est actif par défaut. Utilisez `SPRING_PROFILES_ACTIVE=prod` pour le profil de production. Les paramètres modifiables sont documentés dans `.env.example`.
# Truch-management-
