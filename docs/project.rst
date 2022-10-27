Construcción y carga del proyecto
=======================

1. Clonar el repositorio de GitHub de Basicmac y todos sus submódulos.

```bash
git clone --recurse-submodules https://github.com/mkuyper/basicmac.git basicmac
```

2. Crear y activar un entorno virtual con Python dentro de la carpeta basicmac.

```bash
cd basicmac
python3 -m venv venv
source venv/bin/activate
```

3. Instalar los módulos de Python requeridos por las herramientas de compilación y simulación, se pueden instalar usando pip.

```bash
pip install -r basicloader/requirements.txt
pip install -r ./requirements.txt
pip install pyyaml
```

4. Basicmac emplea un gestor de arranque, Basicloader, para cargar e iniciar el firmware real. Este cargador de arranque también aplica cualquier actualización de firmware y verifica la integridad del firmware actual antes de llamar al punto de entrada del firmware. Para crear este cargador usar el siguiente comando:

```bash
cd basicloader
VARIANT=us915 make
```
El resultado del proceso de compilación es un archivo llamado *bootloader.hex*.

5. Conectar la tarjeta al computador mediante USB, verifique que el dispositivo es reconocido como una unidad USB con nombre *DIS\_L072Z*.

6. Después de compilar un proyecto, se puede cargar en un dispositivo. Tenga en cuenta que tanto el cargador de arranque como el firmware deben cargarse, aunque como el cargador de arranque rara vez cambia, generalmente solo se carga una vez. Para cargar el cargador de arranque y el firmware, respectivamente, use los objetivos `make loadbl` y `make load`.

```bash
cd ../projects/ex-join
VARIANT=us915 make loadbl
VARIANT=us915 make load
```