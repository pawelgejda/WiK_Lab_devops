# HopeLink (1.5%) — static website

HopeLink is a static landing page for a 1.5% tax donation campaign.
This repository is designed to be **public and safe**: no secrets, no `.env` committed.

## Features
- Static website (HTML/CSS/JS)
- Dockerized with Nginx
- Docker Compose for local run
- CI: Docker image build on every push/PR
- CD: publish Docker image to GHCR on push to `main`

## Requirements
- Docker
- Docker Compose

## Run locally (Docker)
Start:
bash
docker compose up --build

Open:
http://localhost:8080

Stop:
docker compose down

Alternative local run (optional)
If you just want a quick local preview without Docker:
python3 -m http.server 8080

Open: http://localhost:8080


## CI/CD
CI: builds Docker image for every Pull Request and push to main.
CD: builds and publishes Docker image to GitHub Container Registry (GHCR) on push to main:
ghcr.io/<owner>/<repo>/hopelink:latest


## Security
No .env is required
.env is ignored by git to prevent accidental leaks
No secrets are stored in the repository


## Author
Pawel G