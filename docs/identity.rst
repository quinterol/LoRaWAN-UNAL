Personalización
=======================

El HAL para STM32 almacena información de personalización como EUI y claves para el funcionamiento de LoRaWAN en EEPROM. Si no se encuentra información de personalización válida en la EEPROM, la HAL creará un dispositivo EUI a partir de los registros de ID únicos de la MCU's y utilizará una clave de prueba y un EUI de unión fijos [[1]](https://basicmac.io/guide/gettingstarted.html):

- Device EUI: `FF-FF-FF-AA-xx-xx-xx-xx`
- Join EUI: `FF-FF-FF-BB-00-00-00-00`
- Device Key: `404142434445464748494A4B4C4D4E4F`

Los valores de Join EUI y Device Key son los mismos para todas las tarjetas, solo el Device EUI es único para cada tarjeta. Para ver el Device EUI utilizado por la tarjeta de desarrollo, se deben seguir los siguientes pasos:

1. Abrir una nueva terminal o salir del directorio anterior.
2. En el B-L072Z-LRWAN1, el firmware imprime información de depuración en el UART que está conectado a través de ST-LINK a la computadora host. En Linux, este dispositivo suele aparecer como `/dev/ttyACM0`. Ejecutar el siguiente comando para lanzar el terminal serial minicom de la tarjeta:

```bash
sudo minicom -D /dev/ttyACM0 -b 2000000
```

3. Presionar los dos botones de reset de la tarjeta al tiempo. En la terminal se visualizara la salida de depuración. En esta se muestra el Device EUI como se muestra en la siguiente imagen.

![minicom](./img/minicom.png)

# Conexión a The Things Network (TTN)

1. Entrar a la sección de aplicaciones de la pagina de The Things Network, a traves del link: https://nam1.cloud.thethings.network/console/applications

2. Crear un nueva aplicación presionando el botón de *add application* y dandole un nombre y un ID.

3. Ir a la pestaña de *End devices* y crear un nuevo dispositivo en *add end device*, como se muestra en la siguiente imagen.

![registro 3](./img/Registro_3.png)

4. Registrar manualmente el dispositivo como se muestra en la siguiente imagen.

![registro 1](./img/Registro_1.png)

5. Ingresar los datos de Device EUI, Join EUI y Device Key como se muestra en la siguiente imagen. Estos datos fueron dados en la sección anterior, recordar que el Device EUI es único de la tarjeta y se obtuvo en el paso 3 de la sección de Personalizaron. Por ultimo, presionar el botón de *Register end device*.

![registro 2](./img/Registro_2.png)

Una vez terminados estos pasos, ya se podrán visualizar los datos enviados por la tarjeta a TTN desde la pestaña *Live data* de la aplicación creada, siempre y cuando se tenga cobertura de un Gateway conectado a la red de TTN.


# Referencias

[[1] M. Kuyper. Basicmac, Getting Started, 2020](https://basicmac.io/guide/index.html)

[[2] ST. UM2115, User manual. Discovery kit for LoRaWAN™, Sigfox™, and LPWAN protocols with STM32L0](https://www.st.com/resource/en/user_manual/dm00329995-discovery-kit-for-lorawan-sigfox-and-lpwan-protocols-with-stm32l0-stmicroelectronics.pdf)

[[3] A crash course in LoRaWAN®, 2021](https://twaclaw.github.io/presentation_lora_lorawan/index.html)