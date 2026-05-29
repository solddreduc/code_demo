# code_demo

Projet Python exécuté dans Docker (dev container ou Compose).

## Structure

```
├── docker/              # Dockerfile
├── docker-compose.yml   # Service de développement
├── .devcontainer/       # Configuration Cursor / VS Code
├── src/                 # Code Python
└── requirements.txt     # Dépendances pip
```

## Dev container (recommandé)

Dans Cursor ou VS Code : **Reopen in Container** (palette de commandes). Le workspace est monté dans `/workspace` ; le terminal et l’exécution Python tournent dans le conteneur.

## Docker Compose (sans IDE)

```bash
docker compose up -d --build
docker compose exec dev python src/main.py
docker compose down
```