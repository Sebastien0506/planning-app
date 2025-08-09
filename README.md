# Planning App

Application de gestion de planning avec **Django** (backend), **Angular** (frontend) et **Traefik** (reverse proxy).

## Fonctionnalités
- Gestion des utilisateurs avec rôles (admin / employé)
- Création et modification de plannings
- Consultation du planning par les employés
- Déploiement automatisé via GitHub Actions (CI/CD)

---

##  Technologies utilisées
- **Backend** : [Django](https://www.djangoproject.com/) + Django REST Framework
- **Frontend** : [Angular](https://angular.io/)
- **Proxy** : [Traefik](https://traefik.io/) (SSL + routage)
- **Base de données** : PostgreSQL
- **Orchestration** : Docker / Docker Compose
- **CI/CD** : GitHub Actions

---

## Installation en local

### Pré-requis
- Docker
- Git

### Étapes
```bash
# 1. Cloner le projet avec les sous-modules
git clone --recurse-submodules https://github.com/Sebastien0506/planning-app.git

# 2. Aller dans le dossier du projet
cd planning-app

# 3. Créer le fichier .env pour le backend
echo "SECRET_KEY=ma_clef_django" > planningBack/.env

# 4. Lancer les services
docker compose up -d --build

# 5. Appliquer les migrations Django
docker compose exec planningBackend python manage.py migrate --noinput