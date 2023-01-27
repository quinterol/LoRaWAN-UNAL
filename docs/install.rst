..
   Copyright (C) 2022-2022 Alexis. Reservados todos los derechos.
   .
   Este archivo está sujeto a los términos y condiciones definidos en el archivo 'LICENCIA', que forma parte de este paquete de código fuente.

Preparación del entorno
=======================

Para hacer uso de `Basic MAC <https://basicmac.io>`_ es necesario tener instalado en terminal Linux las siguientes librerías, estas se requieren para realizar la compilación del firmware como también su instalación en la placa de desarrollo `B-L072Z-LRWAN1 LoRa®/Sigfox™ Discovery Kit <https://www.st.com/en/evaluation-tools/b-l072z-lrwan1.html>`_.

Requisitos previos
------------------

- Una cadena de herramientas de compilación cruzada adecuada `gcc-arm-none-eabi` y `libnewlib-arm-none-eabi`.

```bash
sudo apt-get update
sudo apt-get install gcc-arm-none-eabi libnewlib-arm-none-eabi
```
- Para distros basadas en Arch 

sudo pacman -Sy arm-none-eabi-gcc arm-none-eabi-newlib

- Un entorno con un intérprete de Python 3.8 o posterior.

```bash
sudo apt-get install python3.8-venv
```

- Una herramienta como OpenOCD para cargar el firmware en el hardware real.
Hay que instalar la verson 1.0.10 en arch

sudo pacman -U https://archive.archlinux.org/packages/o/openocd/openocd-1%3A0.10.0-4-x86_64.pkg.tar.zst

```bash
sudo apt-get -y install openocd
```

- Una herramienta para compilar y administrar una colección de aplicaciones y archivos desde el código fuente.

```bash
sudo apt-get install make
```

- Una herramienta para clonar el repositorio de Basicmac en GitHub.

```bash
sudo apt-get install git
```