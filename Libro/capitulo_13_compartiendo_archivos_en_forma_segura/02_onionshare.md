# OnionShare

## Introducción

¿Qué es[OnionShare](https://onionshare.org/)? Según las palabras de los propios dueños del proyecto (cita extraída de <https://github.com/micahflee/onionshare/blob/master/README.md>):

> [OnionShare](https://onionshare.org/) le permite a usted compartir archivos de cualquier tamaño segura y anónimamente. Funciona mediante un servidor web, que es accesible mediante un servicio Tor oculto, y genera una URL imposible de adivinar para acceder y descargar los archivos. Esto no requiere que se configure un servidor en algún lugar de Internet o usar algún servicio de terceros para compartir servicios. Usted hospeda el archivo en su propia computadora y usa un servicio oculto de Tor para que esté temporalmente accesible en Internet. El resto de los usuarios solamente necesitan usar el [navegador web de Tor](https://www.torproject.org/download/download-easy.html.en) para descargar su archivo.

## Instalación

Las instrucciones de instalación se encuentran en el sitio web de [OnionShare](https://onionshare.org/).

## Como usar OnionShare

La siguiente es la pantalla de inicio de [OnionShare](https://onionshare.org).

![started OnionShare](onionshare_1.png)

Usted puede compartir tantos archivos y carpetas como quiera. Para añadirlas puede usar el botón correspondiente o arrastrar y soltar las carpetas dentro de la ventana.
Por favor seleccione la opción `Stop sharing automatically`. Esto le asegura que los archivos que usted comparte puedan ser descargados solamente una vez. 

![added files and folders](onionshare_2.png)

Cliqueando el botón `Start Sharing` se lanza un pequeño servidor web en segundo plano. Esto le permite a su amigo descargar el archivo pero solamente a través de la red [Tor](https://torproject.org) porque dicho pequeño servidor es un [servicio Tor oculto](https://tor.eff.org/docs/hidden-services.html.en).
El inicio del servicio oculto puede demorar un poco, por favor, sea paciente.

![preparing to share files](onionshare_3.png)

Una vez que el servicio oculto inicie, copie su url mediante el botón `Copy URL`.
Luego, envíe dicha dirección a su amigo (si es necesario, a través de un canal cifrado).

![sharing files](onionshare_4.png)

Después de recibir la dirección su amigo debe abrirla en su [navegador web Tor](https://www.torproject.org/download/download-easy.html.en). Esta no será accesible desde otros navegadores web.
Su amigo verá un enlace a un archivo comprimido en formato zip y una lista de archivos contenidos en su interior. La descarga se inicia cliqueando el gran botón azul.

![downloading through TorBrowser](onionshare_5.png)

Usted puede ver cuando su amigo descarga los archivos mediante la barra de progreso azul. Una vez que todo ha terminado, [OnionShare](https://onionshare.org) detendrá el intercambio de archivos automáticamente (excepto que haya deseleccionado `Stop sharing automatically`).

![completed download as seen in OnionShare](onionshare_6.png)

Para verificar que [OnionShare](https://onionshare.org) ha detenido efectivamente el intercambio de archivos puede abrir la dirección que le había enviado a su amigo en su propio [navegador Tor](https://www.torproject.org/download/download-easy.html.en). La descarga ya no está disponible.

![trying download through TorBrowser a second time](onionshare_7.png)

