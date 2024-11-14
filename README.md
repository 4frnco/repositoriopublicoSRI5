# Configuración de BIND9 con Docker

## Creación de Ficheros de Configuración

Primero, crea los directorios y archivos necesarios para la configuración del servicio DNS con Docker:

```
mkdir bind9-docker
mkdir -p named/etc/bind
mkdir -p named/var/cache/bind
mkdir -p named/var/lib/bind
mkdir -p named/var/log
mkdir -p named/var/run
touch docker-compose.yml
touch README.md
```

## Contenido del Fichero `docker-compose.yml`

A continuación, edita el archivo `docker-compose.yml` con el siguiente contenido:

```
version: '3.8'
services:
  bind9:
    image: internetsystemsconsortium/bind9:9.18
    container_name: bind9
    ports:
      - "53:53/tcp"
      - "53:53/udp"
    volumes:
      - ./named.conf.options:/etc/bind/named.conf.options
      - ./zones:/etc/bind/zones
      - ./logs:/var/log/bind
    restart: unless-stopped
```
## Levantar el Contenedor con Docker Compose

Para iniciar el contenedor con el servicio DNS BIND9, ejecuta el siguiente comando:

```
docker-compose up -d
```

Esto levantará el contenedor en segundo plano.


