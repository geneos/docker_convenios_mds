## Generar imagen docker desde los repositorios del proyecto MDS

## Utilizar imagen compilado con docker-compose

Clonar el repositorio `git clone https://github.com/geneos/docker_convenios_mds.git`

## 1. Preparar el entorno, esta tarea debe realizarse cuando se ejecuta por primera vez

Ejecutar `docker-compose up` y detener con `Ctrl + c` cuando termine de generar la estructura de volumenes

Aplicar la migracion en la base de datos `docker-compose run --rm backend ./manage.py migrate`

Crear un usuario `docker-compose run --rm backend ./manage.py createsuperuser`

## 2. Comandos para iniciar o detener el docker

Ejecutar el docker con el comando `docker-compose up -d`

Detener el docker con el comando `docker-compose down`

Eliminar los volumenes persistente `docker-compose down -v`

Esta tarea elimina todos los datos en el disco y para volver a ejecutar se debe repetir el paso 1.

## 3. URL para ingresar al frontend / backend

Ingresar al backend `http://mds-backend.localhost/admin`

Ingresar al frontend `http://mds.localhost/`
