..
   Copyright (C) 2022-2022. Reservados todos los derechos.
   .
   Este archivo está sujeto a los términos y condiciones definidos en el archivo 'LICENCIA', que forma parte de este paquete de código fuente.

¡Bienvenidos!
=============
Esta documentación tiene como finalidad explicar el manejo de `Basic MAC <https://basicmac.io>`_ de manera detallada, haciendo uso de la tarjeta de desarrollo `B-L072Z-LRWAN1 LoRa®/Sigfox™ Discovery Kit <https://www.st.com/en/evaluation-tools/b-l072z-lrwan1.html>`_.


Descripción
-----------

Sub-sección
^^^^^^^^^^

Párrafo
"""""""

Prueba de texto Overline por parts
##################################

Overline para Capitulos
***********************



Basic MAC es una implementación portátil de la especificación LoRaWAN® de LoRa Alliance® en el lenguaje de programación C. Es una bifurcación de la biblioteca LMiC de IBM. Es una bifurcación de la biblioteca LMiC de IBM y admite varias regiones, que se pueden seleccionar en tiempo de compilación y/o ejecución. Puede manejar dispositivos de Clase A, Clase B y Clase C. 

`Basic MAC <https://basicmac.io>` es una implementación portátil de la especificación LoRaWAN® de `LoRa Alliance® <https://lora-alliance.org>` en el lenguaje de programación C. Es una bifurcación de la biblioteca LMiC de IBM y admite múltiples regiones, que se pueden seleccionar en tiempo de compilación y/o ejecución [[1]](https://basicmac.io/). Para la utilización de Basicmac se usará una terminal Linux, los comandos presentados a continuación funcionan para el sistema operativo Ubuntu 20.04, podrían variar si se trabaja desde otra distribución de Linux.

Esta guía tiene por finalidad conectar la tarjeta de desarrollo a un servidor de The Things Network, creando una aplicación y usando la frecuencia us 915 Khz.

.. toctree::
   :maxdepth: 1
   :caption: Contents:

   install
   project
   identity