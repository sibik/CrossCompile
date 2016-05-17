Espacio de Kernel
===
Tarea 1 Compilación cruzada del kernel de linux
---

+ Descargamos el Toolchain

`git clone https://github.com/raspberrypi/tools`

+ Agregamos al $PATH ~/Documentos/apuntesClaseDiplo/modKernel/tareaCrossCompilation/tools-master/arm-bcm2708/gcc-linaro-arm-linux-gnueabihf-raspbian/bin/

con: 
`export PATH=$PATH:~/Documentos/apuntesClaseDiplo/modKernel/tareaCrossCompilation/tools-master/arm-bcm2708/gcc-linaro-arm-linux-gnueabihf-raspbian/bin`

+ Instalamos gcc-arm-linux-gnueabihf con:

`apt-get install gcc-arm-linux-gnueabihf`

+ Verificamos la instalacion con:

`arm-linux-gnueabihf-gcc --version`

+ Descargamos el fuente del kernel

$ git clone --depth=1 https://github.com/raspberrypi/linux

+ Dentro del directorio descargado ejecutamos los siguientes comandos:

`cd linux
KERNEL=kernel
make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- bcmrpi_defconfig

apt-get install gcc-arm-linux-gnueabihf

make ARCH=arm CROSS_COMPILE=/arm-linux-gnueabihf- zImage modules dtbs -j2 `

Usamos -j2 para que se usen los 2 nucleos de nuestro host.

+ Aproximadamente le tomo 30 minutos completar la tarea.

Mesografía
<https://www.raspberrypi.org/documentation/linux/kernel/building.md>

