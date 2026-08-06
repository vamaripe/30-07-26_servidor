## 4.1 Objetivo general

Adquirir conocimientos básicos sobre el uso de Ubuntu Server mediante diferentes métodos de implementación (Máquina Virtual, WSL y Docker), con el fin de familiarizarse con el entorno Linux y desarrollar las habilidades necesarias para ejecutar, probar y administrar proyectos de software en un sistema operativo diferente a Windows.

## 4.2 Objetivos específicos

* Instalar y configurar Ubuntu Server utilizando una máquina virtual, WSL y contenedores Docker.
* Conocer los comandos básicos de administración y actualización del sistema operativo Ubuntu.
* Comparar las diferentes formas de ejecutar Ubuntu y comprender las características de cada una.
* Desarrollar habilidades en el uso del entorno Linux para la ejecución y administración de aplicaciones.
* Preparar un entorno de trabajo que permita ejecutar y validar proyectos de software tanto en Windows como en Linux, garantizando su funcionamiento en diferentes plataformas.

--------------------------------------------------------------------------
# Punto adicional 

## Descripción del entorno de trabajo 
## Comparación de entornos
# Comparación entre VirtualBox (Ubuntu), WSL y Docker

## 11.1 Rendimiento

| Tecnología | Descripción |
|------------|-------------|
| **VirtualBox + Ubuntu** | El rendimiento es **medio**, ya que ejecuta un sistema operativo completo sobre Windows mediante virtualización. Esto genera una pequeña pérdida de rendimiento debido a la capa adicional de hardware virtual. |
| **WSL (Windows Subsystem for Linux)** | El rendimiento es **alto**, especialmente con WSL 2, ya que utiliza un kernel de Linux optimizado y se integra directamente con Windows. Es mucho más rápido que una máquina virtual tradicional para tareas de desarrollo. |
| **Docker** | El rendimiento es **muy alto**, porque los contenedores comparten el kernel del sistema operativo y únicamente ejecutan los procesos necesarios de la aplicación, sin iniciar un sistema operativo completo. |

---

## 11.2 Consumo de recursos

| Tecnología | Descripción |
|------------|-------------|
| **VirtualBox + Ubuntu** | Tiene un **alto consumo** de recursos. Es necesario asignar previamente memoria RAM, procesadores y espacio en disco para la máquina virtual. |
| **WSL** | Presenta un **consumo medio** de recursos. Solo utiliza memoria y CPU cuando está en ejecución y administra los recursos de manera dinámica. |
| **Docker** | Tiene un **bajo consumo** de recursos, ya que los contenedores son ligeros y comparten el sistema operativo anfitrión. |

---

## 11.3 Facilidad de instalación

| Tecnología | Descripción |
|------------|-------------|
| **VirtualBox + Ubuntu** | La instalación es de **dificultad media**. Se debe instalar VirtualBox, descargar la imagen ISO de Ubuntu y realizar la instalación completa del sistema operativo. |
| **WSL** | La instalación es **muy sencilla**, ya que puede realizarse mediante un solo comando en Windows o desde Microsoft Store. |
| **Docker** | La instalación es de **dificultad media**. Es necesario instalar Docker Desktop (en Windows) o Docker Engine (en Linux) y comprender conceptos básicos como imágenes y contenedores. |

---

## 11.4 Facilidad de administración

| Tecnología | Descripción |
|------------|-------------|
| **VirtualBox + Ubuntu** | La administración es de **dificultad media**, ya que se deben gestionar máquinas virtuales, recursos asignados, instantáneas (snapshots) y actualizaciones del sistema operativo. |
| **WSL** | Su administración es **sencilla**, debido a que funciona como una distribución de Linux integrada en Windows, requiriendo muy poca configuración adicional. |
| **Docker** | Su administración es **media-alta**. Aunque automatiza el despliegue mediante Dockerfile y Docker Compose, requiere aprender conceptos relacionados con imágenes, redes y volúmenes. |

---

## 11.5 Ventajas y desventajas

### VirtualBox + Ubuntu

#### Ventajas

- Permite ejecutar un sistema operativo Linux completo.
- Excelente para aprender administración de sistemas Linux.
- Gran aislamiento entre el sistema anfitrión y el invitado.
- Permite probar diferentes distribuciones y sistemas operativos.

#### Desventajas

- Alto consumo de memoria RAM y CPU.
- Requiere mayor espacio de almacenamiento.
- El inicio del sistema operativo es más lento.
- El rendimiento es inferior al de ejecutar Linux directamente.

---

### WSL (Windows Subsystem for Linux)

#### Ventajas

- Excelente integración con Windows.
- Alto rendimiento para tareas de desarrollo.
- Bajo consumo de recursos.
- Compatible con herramientas como Git, Python, Node.js, Java y Docker.

#### Desventajas

- No ofrece un entorno gráfico completo por defecto.
- Algunas funciones relacionadas con hardware pueden estar limitadas.
- Depende de Windows para funcionar.

---

### Docker

#### Ventajas

- Muy bajo consumo de recursos.
- Inicio de aplicaciones en pocos segundos.
- Permite crear entornos reproducibles y portables.
- Facilita el desarrollo, pruebas y despliegue de aplicaciones.
- Es ampliamente utilizado en entornos empresariales y DevOps.

#### Desventajas

- Tiene una curva de aprendizaje inicial.
- No reemplaza un sistema operativo completo.
- La administración de redes, volúmenes y persistencia puede ser compleja para usuarios principiantes.

---

# Conclusión

Cada tecnología tiene un propósito diferente:

- **VirtualBox + Ubuntu** es la mejor opción para aprender Linux de manera completa o cuando se necesita un sistema operativo totalmente aislado.
- **WSL** está orientado a desarrolladores que trabajan en Windows y desean utilizar herramientas de Linux con un excelente rendimiento y bajo consumo de recursos.
- **Docker** está diseñado para ejecutar aplicaciones en contenedores ligeros, facilitando el desarrollo, las pruebas y el despliegue de software de forma consistente.

En entornos profesionales es muy común utilizar **WSL junto con Docker**, ya que WSL proporciona el entorno Linux y Docker permite ejecutar aplicaciones y servicios en contenedores de manera eficiente.
