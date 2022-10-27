..
   Copyright (C) 2022-2022 Alexis. Reservados todos los derechos.
   .
   Este archivo está sujeto a los términos y condiciones definidos en el archivo 'LICENCIA', que forma parte de este paquete de código fuente.

Preparación del entorno
=======================

Para iniciar en la compilación y creación de firmware personalizado haciendo uso de esta librería es necesario, disponer de las siguientes dependencias.

# Requisitos previos
Las herramientas necesarias para construir y trabajar con Basicmac se muestran a continuación:
- Una cadena de herramientas de compilación cruzada adecuada `gcc-arm-none-eabi` y `libnewlib-arm-none-eabi`.

```bash
sudo apt-get update
sudo apt-get install gcc-arm-none-eabi
sudo apt-get install libnewlib-arm-none-eabi
```

- Un entorno con un intérprete de Python 3.8 o posterior.

```bash
sudo apt-get install python3.8-venv
```

- Una herramienta como OpenOCD para cargar el firmware en el hardware real.

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