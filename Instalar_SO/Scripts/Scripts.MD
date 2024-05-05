# Aplicar Script a VirtualBox para Instalar MacOS

Este repositorio contiene un script y las instrucciones necesarias para aplicarlo en VirtualBox con el fin de facilitar la instalación de MacOS en una máquina virtual.

## Instrucciones

1. Cierra VirtualBox si está abierto.
2. Abre CMD como administrador.
3. Copia el siguiente código según el procesador de tu sistema (Intel o AMD).

### Código para Procesadores Intel:
cd "C:\Program Files\Oracle\VirtualBox\"
VBoxManage.exe modifyvm "nombre maquina virtual" –-cpuidset 00000001 000106e5 00100800 0098e3fd bfebfbff
VBoxManage setextradata "nombre maquina virtual" VBoxInternal/Devices/efi/0/Config/DmiSystemProduct “MacBookPro15,1”
VBoxManage setextradata "nombre maquina virtual" "VBoxInternal/Devices/efi/0/Config/DmiBoardProduct" "Mac-551B86E5744E2388"
VBoxManage setextradata "nombre maquina virtual" "VBoxInternal/Devices/smc/0/Config/DeviceKey" "ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc"
VBoxManage setextradata "nombre maquina virtual" "VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC" 1

### Código para Procesadores AMD:
cd "C:\Program Files\Oracle\VirtualBox\"
VBoxManage.exe modifyvm "nombre maquina virtual" –-cpuidset 00000001 000106e5 00100800 0098e3fd bfebfbff
VBoxManage setextradata "nombre maquina virtual" VBoxInternal/Devices/efi/0/Config/DmiSystemProduct “MacBookPro15,1”
VBoxManage setextradata "nombre maquina virtual" "VBoxInternal/Devices/efi/0/Config/DmiBoardProduct" "Mac-551B86E5744E2388"
VBoxManage setextradata "nombre maquina virtual" "VBoxInternal/Devices/smc/0/Config/DeviceKey" "ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc"
VBoxManage setextradata "nombre maquina virtual" "VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC" 1
VBoxManage modifyvm "nombre maquina virtual" --cpu-profile "Intel Core i7-6700K"

4. Reemplaza "nombre maquina virtual" por el nombre de tu máquina virtual en VirtualBox.
5. Ejecuta el código en CMD para aplicar la configuración necesaria.
