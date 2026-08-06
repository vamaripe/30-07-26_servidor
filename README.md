## 4.1 Objetivo general

Adquirir conocimientos básicos sobre el uso de Ubuntu Server mediante diferentes métodos de implementación (Máquina Virtual, WSL y Docker), con el fin de familiarizarse con el entorno Linux y desarrollar las habilidades necesarias para ejecutar, probar y administrar proyectos de software en un sistema operativo diferente a Windows.

## 4.2 Objetivos específicos

* Instalar y configurar Ubuntu Server utilizando una máquina virtual, WSL y contenedores Docker.
* Conocer los comandos básicos de administración y actualización del sistema operativo Ubuntu.
* Comparar las diferentes formas de ejecutar Ubuntu y comprender las características de cada una.
* Desarrollar habilidades en el uso del entorno Linux para la ejecución y administración de aplicaciones.
* Preparar un entorno de trabajo que permita ejecutar y validar proyectos de software tanto en Windows como en Linux, garantizando su funcionamiento en diferentes plataformas.

--------------------------------------------------------------------------

# 5. Descripción del entorno de trabajo

## 5.1 Características del equipo

Las prácticas se realizaron en un computador con las siguientes especificaciones de hardware:

| Componente                       | Característica                                          |
| -------------------------------- | ------------------------------------------------------- |
| **Procesador**                   | Intel® Core™ i7-14700                                   |
| **Núcleos**                      | 20                                                      |
| **Procesadores lógicos (hilos)** | 28                                                      |
| **Velocidad base**               | 2.10 GHz                                                |
| **Velocidad de funcionamiento**  | Entre 2.03 y 2.75 GHz (varía según la carga de trabajo) |
| **Memoria RAM**                  | 16 GB                                                   |
| **Tipo de memoria**              | SODIMM                                                  |
| **Velocidad de la RAM**          | 4800 MT/s                                               |
| **Ranuras de memoria**           | 1 de 2 ocupadas                                         |
| **Almacenamiento**               | SSD NVMe                                                |
| **Tarjeta gráfica**              | Intel® UHD Graphics (integrada)                         |

Durante la ejecución de las prácticas se observó un comportamiento adecuado del equipo:

* El procesador presentó un uso aproximado entre el **3 % y el 4 %**, indicando una carga baja durante las pruebas.
* La memoria RAM registró un consumo cercano al **73 % (11.4 GB de 16 GB)**, suficiente para ejecutar simultáneamente las herramientas utilizadas.
* El disco SSD NVMe mantuvo un uso aproximado del **1 %**, evidenciando un buen rendimiento del almacenamiento.
* La GPU integrada presentó un uso entre el **4 % y el 6 %**, correspondiente a las tareas normales del sistema.

El equipo cuenta con **una ranura de memoria libre**, lo que permitiría ampliar la capacidad de memoria RAM en caso de requerirse un mayor rendimiento para máquinas virtuales, contenedores o proyectos de mayor complejidad.

---

## 5.2 Sistema operativo anfitrión

El entorno de trabajo se desarrolló sobre **Microsoft Windows** como sistema operativo anfitrión. Desde este sistema se implementaron diferentes alternativas para ejecutar **Ubuntu Server**, permitiendo trabajar en un entorno Linux sin necesidad de reemplazar el sistema operativo principal.

Para ello se utilizaron tres métodos diferentes:

* **Máquina Virtual**, para instalar Ubuntu Server como un sistema operativo independiente dentro de Windows.
* **Windows Subsystem for Linux (WSL)**, que permite ejecutar una distribución Linux de forma integrada con Windows.
* **Docker**, mediante un contenedor basado en la imagen oficial de Ubuntu.

Este enfoque permitió conocer distintas formas de utilizar Linux y prepararse para ejecutar y validar futuros proyectos en un entorno diferente a Windows, asegurando su compatibilidad con sistemas operativos basados en Linux.

---

## 5.3 Herramientas utilizadas

Durante el desarrollo de la práctica se emplearon las siguientes herramientas:

| Herramienta                           | Descripción                                                                                                |
| ------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **Microsoft Windows**                 | Sistema operativo anfitrión donde se realizaron todas las pruebas.                                         |
| **Oracle VM VirtualBox**              | Software de virtualización utilizado para crear e instalar una máquina virtual con Ubuntu Server.          |
| **Ubuntu Server (imagen ISO)**        | Sistema operativo Linux utilizado en la máquina virtual.                                                   |
| **Windows Subsystem for Linux (WSL)** | Subsistema de Windows que permite ejecutar Ubuntu de forma nativa sin necesidad de una máquina virtual.    |
| **Docker Desktop**                    | Plataforma de contenedores utilizada para ejecutar Ubuntu en un entorno aislado.                           |
| **Imagen oficial de Ubuntu**          | Imagen descargada desde Docker Hub para crear el contenedor de Ubuntu.                                     |
| **Terminal de Windows (PowerShell)**  | Herramienta utilizada para ejecutar comandos relacionados con Docker, WSL y la administración del sistema. |


---------------------------------------------------------------------------------------------------------------------
# Punto adicional 

## Descripción del entorno de trabajo 
## Comparación de entornos

# Comparación entre VirtualBox (Ubuntu), WSL y Docker

## 11.1 Rendimiento

| Tecnología | Rendimiento |
|------------|-------------|
| **VirtualBox + Ubuntu** | Medio. Ejecuta un sistema operativo completo. |
| **WSL** | Alto. Linux integrado con Windows. |
| **Docker** | Muy alto. Ejecuta aplicaciones en contenedores ligeros. |

---

## 11.2 Consumo de recursos

| Tecnología | Consumo |
|------------|----------|
| **VirtualBox + Ubuntu** | Alto (RAM, CPU y disco). |
| **WSL** | Medio. Usa recursos según la demanda. |
| **Docker** | Bajo. Comparte el sistema operativo. |

---

## 11.3 Facilidad de instalación

| Tecnología | Instalación |
|------------|-------------|
| **VirtualBox + Ubuntu** | Media. Requiere instalar VirtualBox y Ubuntu. |
| **WSL** | Fácil. Se instala con pocos comandos. |
| **Docker** | Media. Requiere instalar Docker y conocer conceptos básicos. |

---

## 11.4 Facilidad de administración

| Tecnología | Administración |
|------------|----------------|
| **VirtualBox + Ubuntu** | Media. Se administran máquinas virtuales. |
| **WSL** | Fácil. Se maneja como una terminal de Linux. |
| **Docker** | Media. Se administran contenedores e imágenes. |

---

## 11.5 Ventajas y desventajas

| Tecnología | Ventajas | Desventajas |
|------------|----------|-------------|
| **VirtualBox + Ubuntu** | Linux completo, buen aislamiento, ideal para aprender. | Alto consumo de recursos y menor rendimiento. |
| **WSL** | Rápido, ligero e integrado con Windows. | Depende de Windows y no incluye escritorio gráfico por defecto. |
| **Docker** | Ligero, portable y rápido para desplegar aplicaciones. | Curva de aprendizaje y no reemplaza un sistema operativo. |

---

## Conclusión

- **VirtualBox + Ubuntu:** Ideal para aprender Linux y virtualización.
- **WSL:** Mejor opción para desarrollar en Windows con herramientas Linux.
- **Docker:** Ideal para ejecutar y desplegar aplicaciones de forma rápida y eficiente.
