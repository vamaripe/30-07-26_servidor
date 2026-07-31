# Taller Práctico: Instalación de Ubuntu Server en Oracle VM VirtualBox


## Integrantes

- Nombre 1 // Mariana Valenzuela Penagos
- Nombre 2 // Maria Jose Rodriguez Oyola

![alt text](image1.png)

Tener descargada la imagen de ubuntu, asignarle un nombre, la OS que sea Linux, la distribución Ubuntu y la version Plucky Puffin 64-bit,no se se le debe dar a instalación desatendida.

![alt text](image2.png)
ahora se configuran los recursos en la vm a partir de los recursos de nuestra pc.

![alt text](image3.png)
![alt text](image4.png)
![alt text](image5.png)

Una vez configurada nuestra vm se debe encender.

![alt text](image6.png)

Seleccionamos el idioma.

![alt text](image7.png)

Elegimos la distribución del teclado.

![alt text](image8.png)

Instalamos Ubuntu completo.

![alt text](image9.png)

Esto se deja tal cual a como está.

![alt text](image10.png)

El proxy se deja vacío.

![alt text](image11.png)

Se deja igual.

![alt text](image12.png)
![alt text](image13.png)

Seleccionamos el disco.
![alt text](image14.png)

Aceptamos.

![alt text](image15.png)

Nos saltamos la actualización.

![alt text](image16.png)

Configuramos nuestras credenciales.

![alt text](image17.png)

Nos saltamos ubuntu pro.
![alt text](image18.png)

Activamos el SHH.
![alt text](image19.png)

![alt text](image20.png)

Aceptamos.
![alt text](image21.png)

Terminamos la instalación y reiniciamos.

![alt text](image22.png)

Le undimos la letra scape y no saldra esto.

![alt text](image23.png)

![alt text](image24.png)

Ponemos el login con el que configuramos el server.

![alt text](image25.png)

y ya podemos empezar a escribir los comandos en nuestra consola.

![alt text](image26.png)

-------------------

# Comandos básicos de Ubuntu Server (VirtualBox)

## Mostrar la información del sistema operativo

```bash
cat /etc/os-release
```
![alt text](image-3.png)

Muestra la distribución de Linux instalada, su versión y otros datos del sistema operativo.

---

## Mostrar información del kernel

```bash
uname -a
```
![alt text](image-4.png)

Muestra información completa del kernel, arquitectura, nombre del equipo y sistema operativo.

---

## Mostrar la versión del kernel

```bash
uname -r
```
![alt text](image-5.png)

Muestra únicamente la versión del kernel de Linux.

---

## Mostrar la arquitectura del procesador

```bash
uname -m
```
![alt text](image-6.png)

Indica la arquitectura del sistema, por ejemplo `x86_64`.

---

## Mostrar el nombre del equipo

```bash
hostname
```
![alt text](image-7.png)

Muestra el nombre del host o computadora.

---

## Mostrar información del equipo

```bash
hostnamectl
```
![alt text](image-8.png)

Presenta información del sistema como hostname, sistema operativo, kernel y arquitectura.

---

## Mostrar el usuario actual

```bash
whoami
```
![alt text](image-9.png)
Indica el nombre del usuario que ha iniciado sesión.

---

## Mostrar el identificador del usuario

```bash
id
```
![alt text](image-10.png)
Muestra el UID, GID y los grupos a los que pertenece el usuario.

---

## Mostrar el directorio actual

```bash
pwd
```
![alt text](image-11.png)

Indica la ruta completa del directorio en el que se encuentra el usuario.

---

## Listar archivos

```bash
ls
```
![alt text](image-12.png)
Muestra los archivos y carpetas del directorio actual.

---

## Listar archivos detalladamente

```bash
ls -la
```
![alt text](image-13.png)

Muestra todos los archivos, incluidos los ocultos, junto con sus permisos, propietario y tamaño.

---

## Mostrar estructura de directorios

```bash
tree
```
(por ahora no e elavorado como tal una extructura)
![alt text](image-14.png)

Muestra la estructura de carpetas en forma de árbol.

> Requiere instalar el paquete `tree`.

---

## Mostrar la fecha y hora

```bash
date
```
![alt text](image-15.png)

Muestra la fecha y hora actual del sistema.

---

## Mostrar el tiempo de actividad

```bash
uptime
```
![alt text](image-16.png)

Indica cuánto tiempo lleva encendido el sistema y la carga del procesador.

---

## Mostrar el uso de memoria

```bash
free -h
```
![alt text](image-17.png)

Muestra el uso de memoria RAM y swap en formato legible.

---

## Mostrar información del procesador

```bash
lscpu
```
![alt text](image-18.png)

Presenta información detallada de la CPU.

---

## Mostrar dispositivos de almacenamiento

```bash
lsblk
```
![alt text](image-19.png)

Lista los discos, particiones y dispositivos de almacenamiento.

---

## Mostrar el espacio en disco

```bash
df -h
```
![alt text](image-20.png)

Muestra el espacio usado y disponible en los sistemas de archivos.

---

## Mostrar sistemas de archivos montados

```bash
mount
```
![alt text](image-21.png)

Lista todos los sistemas de archivos montados.

---

## Mostrar procesos en ejecución

```bash
ps aux
```
![alt text](image-22.png)
Muestra todos los procesos activos del sistema.

---

## Monitor de procesos

```bash
top
```
![alt text](image-23.png)
Muestra en tiempo real el consumo de CPU, memoria y procesos.

---

## Monitor de procesos mejorado

```bash
htop
```
![alt text](image-24.png)

Versión interactiva de `top` con una interfaz más amigable.

> Requiere instalar el paquete `htop`.

---

## Consultar el estado del servicio SSH

```bash
systemctl status ssh
```
![alt text](image-25.png)
Muestra si el servicio SSH está activo y su estado.

---

## Listar los servicios

```bash
systemctl list-units --type=service
```
![alt text](image-26.png)
Lista todos los servicios administrados por `systemd`.

---

## Mostrar direcciones IP

```bash
ip addr
```
![alt text](image-27.png)

Muestra las interfaces de red y sus direcciones IP.

---

## Mostrar rutas de red

```bash
ip route
```
![alt text](image-28.png)

Muestra la tabla de enrutamiento del sistema.

---

## Mostrar la IP del equipo

```bash
hostname -I
```
![alt text](image-29.png)
Muestra las direcciones IP asignadas al equipo.

---

## Probar la conexión a Internet

```bash
ping 8.8.8.8
```
![alt text](image-30.png)
Comprueba la conectividad enviando paquetes al servidor DNS de Google.

---

## Probar la resolución DNS

```bash
ping google.com
```
![alt text](image-31.png)

Comprueba tanto la conexión a Internet como la resolución de nombres DNS.

---

## Mostrar puertos abiertos

```bash
ss -tulnp
```
![alt text](image-32.png)

Lista los puertos TCP y UDP abiertos junto con los procesos asociados.

---

## Mostrar conexiones de red

```bash
netstat -tulnp
```
![alt text](image-33.png)
Muestra los puertos abiertos y conexiones activas.

> Requiere instalar el paquete `net-tools`.

---

## Mostrar la IP pública

```bash
curl ifconfig.me
```
![alt text](image-34.png)

Obtiene la dirección IP pública del equipo desde Internet.

---

## Mostrar variables de entorno

```bash
env
```
![alt text](image-35.png)

Muestra todas las variables de entorno disponibles.

---

## Mostrar historial de comandos

```bash
history
```
![alt text](image-36.png)

Muestra el historial de comandos ejecutados por el usuario.

---

## Crear un directorio

```bash
mkdir practica
```

![alt text](image-37.png)

Crea una carpeta llamada `practica`.

---

## Cambiar de directorio

```bash
cd practica
```
![alt text](image-38.png)

Ingresa al directorio llamado `practica`.

---

## Crear un archivo vacío

```bash
touch archivo.txt
```


Crea un archivo vacío llamado `archivo.txt`.

---

## Editar un archivo

```bash
nano archivo.txt
```
![alt text](image-39.png)

Abre el archivo en el editor de texto Nano.

---

## Mostrar el contenido de un archivo

```bash
cat archivo.txt
```


Muestra el contenido del archivo en la terminal.

---

## Copiar un archivo

```bash
cp archivo.txt copia.txt
```

Copia el archivo con un nuevo nombre.

---

## Renombrar o mover un archivo

```bash
mv copia.txt respaldo.txt
```

Renombra el archivo o lo mueve a otra ubicación.

---

## Eliminar un archivo

```bash
rm respaldo.txt
```

Elimina el archivo indicado.

---

## Eliminar un directorio vacío

```bash
rmdir practica
```

Elimina el directorio si no contiene archivos.

---

## Actualizar la lista de paquetes

```bash
sudo apt update
```
![alt text](image.png)

Actualiza la lista de paquetes disponibles en los repositorios.

---

## Actualizar los paquetes instalados

```bash
sudo apt upgrade
```
![alt text](image-1.png)

Instala las versiones más recientes de los paquetes instalados.

---

## Instalar Net Tools

```bash
sudo apt install net-tools
```

Instala herramientas clásicas de red como `netstat`.

---

## Instalar htop

```bash
sudo apt install htop
```

Instala el monitor de procesos `htop`.

---

## Eliminar paquetes innecesarios

```bash
sudo apt autoremove
```
![alt text](image-2.png)

Elimina paquetes que ya no son utilizados por el sistema.

---

## Reiniciar el sistema

```bash
sudo reboot
```

Reinicia el sistema operativo.

---

## Apagar el sistema

```bash
sudo shutdown now
```

Apaga inmediatamente el sistema.

---

## Mostrar la versión del sistema

```bash
cat /proc/version
```

Muestra información sobre el kernel y el compilador utilizado.

---

## Mostrar información del proceso inicial

```bash
cat /proc/1/cgroup
```

Muestra los grupos de control (cgroups) del proceso con PID 1.

---

## Detectar el entorno de virtualización

```bash
systemd-detect-virt
```

Indica si el sistema se ejecuta en una máquina virtual y cuál es la tecnología utilizada.

---

## Mostrar el modelo del sistema

```bash
sudo dmidecode -s system-product-name
```

Muestra el nombre o modelo del equipo o máquina virtual.

---

## Mostrar el hardware del sistema

```bash
sudo lshw -short
```

Presenta un resumen del hardware instalado.

---

## Buscar información de virtualización

```bash
dmesg | grep -i virtual
```

Busca en los mensajes del kernel información relacionada con la virtualización.