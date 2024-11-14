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
