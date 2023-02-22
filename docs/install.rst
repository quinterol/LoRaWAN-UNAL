..
   Copyright (C) 2022-2022 Alexis. Reservados todos los derechos.
   .
   Este archivo está sujeto a los términos y condiciones definidos en el archivo 'LICENCIA', que forma parte de este paquete de código fuente.

Preparación del entorno
=======================

Para hacer uso de `Basic MAC <https://basicmac.io>`_ es necesario tener instalado en terminal Linux las siguientes librerías, estas se requieren para realizar la compilación del firmware como también su instalación en la placa de desarrollo `B-L072Z-LRWAN1 LoRa®/Sigfox™ Discovery Kit <https://www.st.com/en/evaluation-tools/b-l072z-lrwan1.html>`_.

La guía explicara los preparativos en dos de las principales distribuciones de Linux, `Ubuntu <https://ubuntu.com/>`_ y `Arch Linux <https://archlinux.org/>`_

Requisitos previos
------------------

-  Es necesario instalar un compilador para arm, para ello usamos el paquete `GCC, the GNU Compiler Collection <https://gcc.gnu.org/>`_ y su variante para arm la cual es una cadena de herramientas de compilación cruzada.

En ubuntu para instalar se puede instalar directamente con el gestor de paquetes apt.::
   
   sudo apt update && sudo apt-get install gcc-arm-none-eabi libnewlib-arm-none-eabi

En Arch Linux y sus derivadas se usa el gestor de pacman. ::

   sudo pacman -Sy arm-none-eabi-gcc arm-none-eabi-newlib

- Un entorno con un intérprete de Python 3.8, para ello vamos a usar entornos virtuales y un control de versiones en python.

En ubuntu se instalan las siguientes librerías.::

   sudo apt-get install python3 python-tk python3-tk tk-dev python3.8-venv

En Arch Linux ::
   
   sudo pacman -Sy pyenv tk python

- OpenOCD como herramienta para instalar en el hardware real, es necesario usar la version 1.0.10 del 01/Nov/2020

En ubuntu (aun por verificar como se instala esa verison exactamente) ::

   sudo apt-get -y install openocd

En Arch Linux ::

   sudo pacman -U https://archive.archlinux.org/packages/o/openocd/openocd-1%3A0.10.0-4-x86_64.pkg.tar.zst

``Nota: Editar el archivo /etc/pacman.conf y agregar la linea IgnorePkg = openocd``mas información sobre pacman `aquí <https://wiki.archlinux.org/title/pacman#Skip_package_from_being_upgraded>`_.

- make y git para compilar y administrar una colección de aplicaciones y archivos desde el código fuente.

En Ubuntu ::

   sudo apt-get install make git

En Arch Linux ::
   
   sudo pacman -Sy make git
