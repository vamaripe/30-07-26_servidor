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
