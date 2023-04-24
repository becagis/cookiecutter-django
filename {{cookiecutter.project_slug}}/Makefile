# DEV
up:
	docker-compose up -d

down:
	docker-compose down

build:
	docker-compose build

pull:
	docker-compose pull

migrate:
	docker-compose run --rm django python manage.py migrate

createsuperuser:
	docker-compose run --rm django python manage.py createsuperuser

py-shell:
	docker-compose run --rm django python manage.py shell

logs:
	docker-compose logs --follow

# PROD
up-prod:
	docker-compose -f production.yml up -d

down-prod:
	docker-compose -f production.yml down

build-prod:
	docker-compose -f production.yml build

# GENERAL
merge-envs:
	python3 merge_production_dotenvs_in_dotenv.py

backup:
	docker-compose exec postgres backup

move-backup-c2h:
	docker cp $(docker-compose ps -q postgres):/backups ./backups