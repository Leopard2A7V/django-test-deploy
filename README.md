# Create new .venv

- Windows: python -m venv .venv
- Bash: python3 -m venv .venv

# Activate .venv

- Windows: .venv\Scripts\Activate.ps1
- Bash: source .venv\Scripts\activate

# Deactivate .venv

- terminal: deactivate

# Create requirements.txt for Docker

- terminal: pip freeze > requirements.txt
<hr/>

# DOCKER REQUIRED

# First Start

docker-compose up -d --build

# Migrate Data

docker-compose exec web python manage.py migrate

# Create SU

docker-compose exec web python manage.py createsuperuser

# Migration

docker-compose exec web python manage.py makemigrations

# Turn on Server

docker-compose up

# Turn down Server

docker-compose down
