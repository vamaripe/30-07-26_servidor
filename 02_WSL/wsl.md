# Comandos básicos de Ubuntu en WSL

## Mostrar la información del sistema operativo

```bash
cat /etc/os-release
```

Muestra la distribución de Linux instalada, su versión y otros datos del sistema operativo.

![alt text](image.png)
---

## Mostrar información del kernel

```bash
uname -a
```

Muestra información completa del kernel, arquitectura, nombre del equipo y sistema operativo.

![alt text](image-1.png)

---

## Mostrar la versión del kernel

```bash
uname -r
```

Muestra únicamente la versión del kernel de Linux.

![alt text](image-2.png)

---

## Mostrar la arquitectura del procesador

```bash
uname -m
```

Indica la arquitectura del sistema, por ejemplo `x86_64`.

![alt text](image-3.png)

---

## Mostrar el nombre del equipo

```bash
hostname
```

Muestra el nombre del host o computadora.

![alt text](image-4.png)

---

## Mostrar información del equipo

```bash
hostnamectl
```

Presenta información del sistema como hostname, sistema operativo, kernel y arquitectura.

![alt text](image-5.png)

> Requiere que **systemd** esté habilitado en WSL.

---

## Mostrar el usuario actual

```bash
whoami
```

Indica el nombre del usuario que ha iniciado sesión.

![alt text](image-6.png)

---

## Mostrar el identificador del usuario

```bash
id
```

Muestra el UID, GID y los grupos a los que pertenece el usuario.

![alt text](image-7.png)

---

## Mostrar el directorio actual

```bash
pwd
```

Indica la ruta completa del directorio en el que se encuentra el usuario.

![alt text](image-8.png)

---

## Listar archivos

```bash
ls
```

Muestra los archivos y carpetas del directorio actual.

![alt text](image-9.png)

---

## Listar archivos detalladamente

```bash
ls -la
```

Muestra todos los archivos, incluidos los ocultos, junto con sus permisos, propietario y tamaño.

![alt text](image-10.png)

---

## Mostrar estructura de directorios

```bash
tree
```

Muestra la estructura de carpetas en forma de árbol.

![alt text](image-11.png)

> Requiere instalar el paquete `tree`.

---

## Mostrar la fecha y hora

```bash
date
```

Muestra la fecha y hora actual del sistema.

![alt text](image-12.png)

---

## Mostrar el tiempo de actividad

```bash
uptime
```

Indica cuánto tiempo lleva iniciada la sesión de WSL y la carga del sistema.

![alt text](image-13.png)

---

## Mostrar el uso de memoria

```bash
free -h
```

Muestra el uso de memoria RAM y swap en formato legible.

![alt text](image-14.png)

---

## Mostrar información del procesador

```bash
lscpu
```

Presenta información detallada de la CPU.

![alt text](image-15.png)
![alt text](image-16.png)

---

## Mostrar dispositivos de almacenamiento

```bash
lsblk
```

Lista los discos y particiones visibles desde WSL.

![alt text](image-17.png)

> Puede mostrar información limitada debido a la integración con Windows.

---

## Mostrar el espacio en disco

```bash
df -h
```

Muestra el espacio usado y disponible en los sistemas de archivos montados.

![alt text](image-18.png)

---

## Mostrar sistemas de archivos montados

```bash
mount
```

Lista todos los sistemas de archivos montados, incluidos los de Windows.

![alt text](image-19.png)
![alt text](image-20.png)
---

## Mostrar procesos en ejecución

```bash
ps aux
```

Muestra todos los procesos activos de la distribución Linux.

![alt text](image-21.png)

---

## Monitor de procesos

```bash
top
```

Muestra en tiempo real el consumo de CPU, memoria y procesos.

![alt text](image-22.png)

---

## Monitor de procesos mejorado

```bash
htop
```

Versión interactiva de `top` con una interfaz más amigable.

![alt text](image-60.png)

> Requiere instalar el paquete `htop`.

---

## Consultar el estado del servicio SSH

```bash
systemctl status ssh
```

Muestra si el servicio SSH está activo y su estado.

![alt text](image-24.png)

> Requiere que **systemd** esté habilitado.

---

## Listar los servicios

```bash
systemctl list-units --type=service
```

Lista los servicios administrados por `systemd`.

![alt text](image-25.png)

> Requiere que **systemd** esté habilitado.

---

## Mostrar direcciones IP

```bash
ip addr
```

Muestra las interfaces de red y sus direcciones IP.

![alt text](image-26.png)
---

## Mostrar rutas de red

```bash
ip route
```

Muestra la tabla de enrutamiento del sistema.

![alt text](image-27.png)
---

## Mostrar la IP del equipo

```bash
hostname -I
```

Muestra las direcciones IP asignadas a WSL.

![alt text](image-28.png)
---

## Probar la conexión a Internet

```bash
ping 8.8.8.8
```

Comprueba la conectividad enviando paquetes al servidor DNS de Google.

![alt text](image-29.png)

---

## Probar la resolución DNS

```bash
ping google.com
```

Comprueba tanto la conexión a Internet como la resolución de nombres DNS.

![alt text](image-30.png)
---

## Mostrar puertos abiertos

```bash
ss -tulnp
```

Lista los puertos TCP y UDP abiertos junto con los procesos asociados.

![alt text](image-31.png)

---

## Mostrar conexiones de red

```bash
netstat -tulnp
```

Muestra los puertos abiertos y conexiones activas.

![alt text](image-32.png)

> Requiere instalar el paquete `net-tools`.

---

## Mostrar la IP pública

```bash
curl ifconfig.me
```

Obtiene la dirección IP pública del equipo desde Internet.

![alt text](image-33.png)

---

## Mostrar variables de entorno

```bash
env
```

Muestra todas las variables de entorno disponibles.

![alt text](image-34.png)

![alt text](image-35.png)
---

## Mostrar historial de comandos

```bash
history
```

Muestra el historial de comandos ejecutados por el usuario.

![alt text](image-36.png)

---

## Crear un directorio

```bash
mkdir practica
```

Crea una carpeta llamada `practica`.

![alt text](image-37.png)

---

## Cambiar de directorio

```bash
cd practica
```

Ingresa al directorio llamado `practica`.

![alt text](image-38.png)

---

## Crear un archivo vacío

```bash
touch archivo.txt
```

Crea un archivo vacío llamado `archivo.txt`.

![alt text](image-39.png)

---

## Editar un archivo

```bash
nano archivo.txt
```

Abre el archivo en el editor de texto Nano.

![alt text](image-41.png)

![alt text](image-40.png)

---

## Mostrar el contenido de un archivo

```bash
cat archivo.txt
```

Muestra el contenido del archivo en la terminal.

![alt text](image-42.png)

---

## Copiar un archivo

```bash
cp archivo.txt copia.txt
```

Copia el archivo con un nuevo nombre.

![alt text](image-43.png)
---

## Renombrar o mover un archivo

```bash
mv copia.txt respaldo.txt
```

Renombra el archivo o lo mueve a otra ubicación.

![alt text](image-44.png)
---

## Eliminar un archivo

```bash
rm respaldo.txt
```

Elimina el archivo indicado.

![alt text](image-45.png)
---

## Eliminar un directorio vacío

```bash
rmdir practica
```

Elimina el directorio si no contiene archivos.

![alt text](image-46.png)

---

## Actualizar la lista de paquetes

```bash
sudo apt update
```

Actualiza la lista de paquetes disponibles en los repositorios.

![alt text](image-47.png)

---

## Actualizar los paquetes instalados

```bash
sudo apt upgrade
```

Instala las versiones más recientes de los paquetes instalados.

![alt text](image-48.png)

---

## Instalar Net Tools

```bash
sudo apt install net-tools
```

Instala herramientas clásicas de red como `netstat`.

![alt text](image-49.png)

---

## Instalar htop

```bash
sudo apt install htop
```

Instala el monitor de procesos `htop`.

![alt text](image-50.png)

---

## Eliminar paquetes innecesarios

```bash
sudo apt autoremove
```

Elimina paquetes que ya no son utilizados por el sistema.

![alt text](image-51.png)
---

## Reiniciar WSL

```bash
sudo reboot
```

Reinicia la distribución de Ubuntu si **systemd** está habilitado; de lo contrario, puede no funcionar como en una instalación tradicional.

![alt text](image-52.png)
---

## Apagar WSL

```bash
sudo shutdown now
```

Apaga la distribución de Ubuntu si **systemd** está habilitado.

![alt text](image-53.png)

---

## Mostrar la versión del sistema

```bash
cat /proc/version
```

Muestra información sobre el kernel utilizado por WSL y el compilador empleado.

![alt text](image-54.png)

---

## Mostrar información del proceso inicial

```bash
cat /proc/1/cgroup
```

Muestra los grupos de control (cgroups) del proceso con PID 1.

![alt text](image-55.png)

---

## Detectar el entorno de virtualización

```bash
systemd-detect-virt
```

Indica que el sistema se está ejecutando sobre WSL u otro entorno virtualizado.

![alt text](image-56.png)

---

## Abrir el Explorador de Windows

```bash
explorer.exe .
```

Abre el directorio actual de WSL en el Explorador de archivos de Windows.

![alt text](image-57.png)

---

## Ejecutar un comando de Windows

```bash
cmd.exe /c dir
```

Ejecuta el comando `dir` de Windows desde la terminal de WSL.

![alt text](image-58.png)
---

## Buscar información de virtualización

```bash
dmesg | grep -i virtual
```

Busca en los mensajes del kernel información relacionada con la virtualización.

![alt text](image-59.png)