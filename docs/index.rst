..
   Copyright (C) 2022-2022. Reservados todos los derechos.
   .
   Este archivo está sujeto a los términos y condiciones definidos en el archivo 'LICENCIA', que forma parte de este paquete de código fuente.

¡Bienvenidos!
=============
UNAL-LoRaWAN
------------
Esta documentación tiene como finalidad explicar el manejo de `Basic MAC <https://basicmac.io>`_, haciendo uso de la tarjeta de desarrollo `B-L072Z-LRWAN1 LoRa®/Sigfox™ Discovery Kit <https://www.st.com/en/evaluation-tools/b-l072z-lrwan1.html>`_.


Basic MAC
-----------
`Basic MAC <https://basicmac.io>`_ es una implementación portátil de la especificación LoRaWAN® de `LoRa Alliance® <https://lora-alliance.org>`_ en el lenguaje de programación C. Es una bifurcación de la biblioteca LMiC de IBM y admite múltiples regiones, que se pueden seleccionar en tiempo de compilación y/o ejecución. Puede manejar dispositivos de Clase A, Clase B y Clase C. [#]_

STM32L0 Discovery kit LoRa, Sigfox, low-power wireless
------------------------------------------------------
B-L072Z-LRWAN1
^^^^^^^^^^
El kit de descubrimiento LoRa®/Sigfox™ B-L072Z-LRWAN1 es una herramienta de desarrollo para aprender y desarrollar soluciones basadas en las tecnologías LoRa®, Sigfox™ y FSK/OOK. El kit B-L072Z-LRWAN1 Discovery incluye una interfaz de herramienta de depuración embebida ST-LINK/V2-1, LEDs, pulsadores, antena, conectores Arduino™ Uno V3 y conector USB OTG en formato Micro-B. [#]_

.. [#] Una traducción de `Basic MAC getting started guide <https://basicmac.io/guide/gettingstarted.html>`_. 
.. [#] Una traducción de `Product overview B-L072Z-LRWAN1 <https://www.st.com/en/evaluation-tools/b-l072z-lrwan1.html>`

.. toctree::
   :maxdepth: 1
   :caption: Contenido:

   install
   project
   identity