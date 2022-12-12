# Raspberry-Pi-configuracion-y-VNC-viewer
Instalación de sistema operativo de Raspberry Pi en el dispositivo y la instalación del VNC Viewer para comunicación visualización de  Raspberry Pi

##Sistema operativo de Raspberry Pi 4
![]()
* Se requiere instalar un sistema operativo al dispositivo, este se descarga mediante una aplicación de que obtine desde la pagina oficial de [Raspberry](https://www.raspberrypi.com/software/), esta app puede ser descargada en Windows.
* Conectar a la computadora la tajeta micro SD.
* Abrir la app de Raspberry
* Aparecerá un asistente de instalación del sistema operativo (Paspberry Pi Image), la configuración se escoge:
  * Sistema operativo de 32 bits 
  * Habilitar SSH
  * Asignar nombre a la Raspberry.
  * Asignar nombre de usuario.
  * Asignar contraseña de usuario.
  * Agregar los datos de WiFi **nombre de Red y contraseña de red**
* Cargar el sistema operativo( dar clic en Write) a una tarjeta Micro SD, que se pasara al dispositivo raspberry Pi 4.

## Iniciar la Raspberry Pi 4
Una vez que la tarjeta Micro SD tenga el sistema operativo se tiene que pasar a montar en la Raspberry Pi apagada.

Se tienen dos opciones para acceder a la Raspberry Pi: 
+ Hardware
+ Virtual

Al usar Hardware no se requiere la conexión por SSH ni VNC.

### Acceso por hardware a la Raspberry Pi 4.
Al dispositivo se le conectan los perifericos.
  * Pantalla HDMI
  * Tecaldo USB
  * Mouse USB
  
### Acceso Virtual a la Raspberry Pi 4.
Al no contar con pantalla disponible, se puede acceder via remota desde otra computadora, esta debe tener instalado SSH y VNC.
+ En algun buscador de IP de dipositivos conectados a la red  de WiFi se busca la **IP de la Raspberry Pi**, Tambien se puede visualizar la iP desde la pagina de configuración del modem.
+ Desde terminal de comando en Ubuntu se conecta por SSH a Raspberry Pi, usando el comendo de ssh nombre de **[raspberry pi]@IP**

      ssh pi@192.168.x.x

+ En este punto podemos acceder a la configuración del dispositivo Raspberry Pi 4.
      
      sudo raspi-config

+ Aárece la ventana de configuación y activamos el protocolo de VNC en la opcion de:
  * Interface Options.
    * VNC.
+ Ademas configuramos la resolucion de pantall VNC, dentro de la misma ventana de onfiguracion de Raspberry Pi.
  * Display Options.
    * VNC Resolution.
      * 1280 x 720.

De esta forma se comunicará la Raspberry con la computadora, pero aun falta poder visualizar la pantalla de la Raspberry, para esto usamos VNC Viewer.

## VNC Viewer.
Instalar VNC Viewer desde la pagina ofical (https://www.realvnc.com/es/connect/download/viewer/), cuidando de descargar para Linux Ubuntu Debian

Una vez instalada se abre el software VNC Viewer.

Ejecutamos con cuenta gratuita.

Usamos la IP de Raspberry para crear una conexión, Cada que se usa se debe actualizar la IP de la Raspberry Pi en esta conexion.
