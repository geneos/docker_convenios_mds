# Generar imagen docker desde los repositorios del proyecto MDS

## Crear imagen del frontend

### `docker build -t ferjavrec/mds-frontend:1.0 .`

## Crear imagen del backend

### `docker build -t ferjavrec/mds-backend:1.0 .`

## Utilizar imagen compilado con docker-compose

Ejecutar `docker-compose up` y detener con `Ctrl + c` cuando termine de generar la estructura de volumenes

Aplicar la migracion en la base de datos `docker-compose run --rm backend ./manage.py migrate`

Crear un super usuario `docker-compose run --rm backend ./manage.py createsuperuser`

Ejecutar el docker con el comando `docker-compose up -d`

Detener el docker con el comando `docker-compose down`

## Ingresar al backend `127.0.0.1:8000/admin`

## Ingresar al frontend `127.0.0.1`
