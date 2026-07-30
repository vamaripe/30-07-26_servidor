# Taller Práctico: Instalación de Ubuntu Server en Docker


## Integrantes

- Nombre 1 // Mariana Valenzuela Penagos
- Nombre 2 // Maria Jose Rodriguez Oyola


----------------
## PASO 1 — Crear el docker-compose.yml

¿Qué estamos haciendo?
- image: ubuntu:24.04 → Usamos la imagen oficial de Ubuntu.
- container_name: ubuntu-server → El contenedor tendrá ese nombre.
- stdin_open: true → Permite interactuar con la terminal.
- tty: true → Mantiene una terminal interactiva.
- command: /bin/bash → Al iniciar, entraremos a la terminal Bash de Ubuntu.

> docker compose pull

![alt text](image-1.png)

----------------------

## PASO 2 — Descargar la imagen de Ubuntu

> docker images

![alt text](image-2.png)

![alt text](image-8.png)

------------------

## PASO 3 — Crear y levantar el contenedor

>  docker compose up -d

![alt text](image-9.png)
![alt text](image-10.png)

> docker ps

![alt text](image-11.png)

## PASO 4 — Entrar al Ubuntu del contenedor

Para eso ejecutamos :
> docker compose exec ubuntu-server bash

![alt text](image-12.png)

##  ¡Ya estás dentro de Ubuntu ejecutándose en Docker!  :) 

-----------------------
Ahora ejecutamos 

> cat /etc/os-release

- vemos la informacion de ubuntu 

![alt text](image-13.png)


--------------
## PASO 5 — Actualizar Ubuntu

ejecutamos 

> apt update

![alt text](image-14.png)

Cuando termine : se ejecuta 

>  apt upgrade -y

![alt text](image-15.png)

------------------------------------------

## PASO 6 — Instalar un paquete

ejecutamos 

> apt install -y curl

Para demostrar la instalación de paquetes, ejecuta:


![alt text](image-16.png)

Después verifica:

> curl --version
![alt text](image-17.png)

------------------------------------

## PASO 7 — Salir del contenedor

Cuando termines: 
> exit

![alt text](image-18.png)

Puedes comprobar que el contenedor sigue funcionando:

> docker ps
![alt text](image-19.png)
