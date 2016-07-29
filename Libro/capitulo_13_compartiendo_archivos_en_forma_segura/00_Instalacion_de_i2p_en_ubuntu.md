Instalación de I2P on Ubuntu Lucid Lynx (y posteriores) y sus derivados como Linux Mint & Trisquel
============================

 1. Abra una terminal y escriba:
    
 `sudo apt-add-repository ppa:i2p-maintainers/i2p`
 
 Este comando agregará el PPA a /etc/apt/sources.list.d y descargará la clave gpg con la cual se ha firmado el repositorio. La clave GPG se asegura de que los paquetes no se han alterado desde que fue construido.

 2. Notifique a su administrador de paquetes del nuevo PPA ingresando

 `sudo apt-get update`

 Este comando recuperará la lista más reciente de software de cada repositorio que está habilitado en el sistema, incluyendo el PPA I2P que se ha añadido con el comando anterior.
 
 3. Ahora está listo para instalar I2P

 `sudo apt-get install i2p`
 
 4. Su explorador debería abrir con la consola del router I2P local, para navegar por dominios I2P tiene que configurar su navegador para usar el proxy I2P. También puede ver el estado de conexión en el lado izquierdo de la consola del router. Si su estado es **Network: Firewalled** su conexión va a ser bastante lenta. La primera vez que inicie I2P puede tardar algunos minutos para integrarse en la red y encontrar pares adicionales para optimizar su integración, por lo que por favor sea paciente.

En el menú Tools, seleccione Options para abrir el panel de configuración de Firefox. Haga click en el icono con la etiqueta Advanced, haga clic en la ficha Network. En la sección Connections, haga clic en el botón Settings. Verá una ventana como la siguiente:

![I2P](i2p_1.jpg)

En la ventana de Connection Settings, haga click en el círculo cercano a Manual proxy configuration, luego ingrese 127.0.0.1, port 4444 en el campo HTTP Proxy. Ingrese 127.0.0.1, port 4445 en el campo SSL Proxy. Asegúrese de ingresar localhost y 127.0.0.1 en la casilla de "No Proxy for".

![I2P](i2p_1.jpg)

Para más información y cómo configurar proxies para otros navegadores consulte [https://www.i2p2.de/htproxyports.htm](https://www.i2p2.de/htproxyports.htm)

Instrucciones para Debian Lenny y posteriores
=============================================
Para más información visita esta página [https://www.i2p2.de/debian.html](https://www.i2p2.de/debian-html)


Empezando con I2P
=================
Usando estos paquetes I2P el router I2P puede iniciar de alguna de las siguientes formas:

* "on demand" usando el script i2prouter. Simplemente ejecute "i2prouter start" en un terminal. (Nota: ¡no use sudo ni lo ejecute como root!)
* como un servicio que se ejecuta automáticamente cuando inicia su sistema, aún antes de loguearse. El servicio puede ser habilitado con "dpkg-reconfigure i2p" como root o mediante sudo. Esta es la manera recomendada.


