# Zara

A Django project with Nginx in front of Gunicorn for local or containerized deployment.

## Local Docker setup

1. Make sure your `.env` file contains the required Django variables.
2. Run the project:

```bash
docker compose up --build
```

3. Open the app in the browser at http://localhost

Nginx serves the Django app on port 80 and proxies requests to Gunicorn running inside the `app` container.
Static files are served directly from `staticfiles/`.

## Files added for Nginx support

- `docker-compose.yml`
- `Dockerfile`
- `nginx/default.conf`
- `staticfiles/.gitkeep`

## Useful commands

```bash
docker compose up --build
docker compose down
docker compose logs -f app
docker compose logs -f nginx
```
