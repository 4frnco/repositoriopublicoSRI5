DNS - Docker Compose

1. Creación de Ficheros de Configuración

Primero, crea los directorios y archivos necesarios para la configuración del servicio DNS con Docker:

franco@ubuntu:~$ mkdir bind9-docker
franco@ubuntu:~$ mkdir -p named/etc/bind
franco@ubuntu:~$ mkdir -p named/var/cache/bind
franco@ubuntu:~$ mkdir -p named/var/lib/bind
franco@ubuntu:~$ mkdir -p named/var/log
franco@ubuntu:~$ mkdir -p named/var/run
franco@ubuntu:~$ touch docker-compose.yml
franco@ubuntu:~$ touch README.md
