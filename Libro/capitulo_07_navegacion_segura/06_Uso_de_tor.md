Uso de Tor
==========

Tor es un sistema pensado para facilitar el anonimato online, y está compuesto por un software cliente y una red de servidores los cuales pueden ocultar información acerca de la localización de los usuarios y otros factores que podrían identificarlos. Imagine un mensaje envuelto en muchas capas de protección: cada servidor tiene que quitar una capa, con lo que inmediatamente elimina la información del remitente del servidor anterior. 

Si Alice desea visitar el sitio web de Bob en forma directa, lo representamos de la siguiente forma:

	Alicia -> Bob

Esto está bien, y Alicia y Bob podrán usar cifrado punto a punto para asegurarse la privacidad, la integridad y la autenticidad de sus comunicaciones. Sin embargo, si Alice no quiere que Bob sepa que ella está visitando su sitio web o no quiere que Eva (una hipotética espía, del lado de Alicia o del de Bob en la conexión) sepa que ella y Bob están comunicándose, se deben establecer algunos pasos extra.

Alicia debe entablar una conexión cifrada con un nodo de entrada de la red Tor, aquí se establecerá una conexión TLS y el nodo de entrada le permitirá a Alicia establecer una comunicación a través de él. Una vez establecida dicha conexión TLS, se repite este proceso con un nodo de repetición, y entre éste y un nodo de salida. En este punto, Alicia cifrará sus datos 3 veces, primero a través del nodo de salida, luego a través del nodo repetidor y finalmente a través del nodo de entrada. La ruta establecida en la red luce de la siguiente manera:

	Alicia -> Nodo de entrada -> Nodo repetidor -> Nodo de salida -> Bob

Cuando el nodo de entrada recibe los datos de Alicia estos están aún cifrados por el nodo repetidor y el nodo de salida. El nodo de entrada conoce su procedencia (Alicia) pero no su destino final (Bob) ni su contenido. El nodo repetidor recibe los datos del nodo de entrada y los trasmite al nodo de salida. Los datos aún están cifrados por el nodo de salida, y no conoce el origen (Alicia) ni el destino (Bob). Cuando el nodo de salida recibe los datos del nodo repetidor, se remueve la última capa de cifrado: el nodo de salida puede ver los datos y el destino (Bob) pero no conoce su origen (Alicia).

Esta aproximación por capas da su nombre a Tor (The Onion Router, el enrutador cebolla), cada capa conoce la capa en contacto con ella, y significa que nadie en la cadena excepto Alicia conoce la ruta completa que los datos están siguiendo; sin embargo, Alicia, Bob y el nodo de salida son capaces de leer el contenido del mensaje, por eso el cifrado punto a punto es requerido para asegurar la privacidad, la integridad y la autenticidad de las comunicaciones a través de la red Tor.

El uso de este sistema hace que sea más difícil de rastrear el tráfico de Internet del usuario, que incluye visitas a sitios web, publicaciones en línea, mensajes instantáneos y otras formas de comunicación. Su objetivo es proteger la libertad personal de los usuarios, la privacidad y capacidad de hacer negocios confidenciales, al mantener sus actividades en Internet a salvo del monitoreo. Tor es software libre y la red es de uso gratuito.

Como todas las redes actuales de anonimato de baja latencia, Tor no puede y no trata de protegerlo contra la vigilancia del tráfico en los extremos de la red, es decir, el tráfico que entra y sale de la red. Mientras que Tor proporciona protección contra el análisis de tráfico, no puede evitar la confirmación del tráfico (también llamada correlación de extremo a extremo)

Precaución: Como Tor no lo hace, y por diseño, no puede, cifrar el tráfico entre un nodo de salida y el servidor de destino, cualquier nodo de salida está en disposición de capturar cualquier tráfico que pasa a través de él, que no utilice cifrado de extremo a extremo, tal como TLS. (Si el cartero es corrupto, podría abrir el sobre y leer el contenido). Si bien esto puede o no violar el anonimato de la fuente, si los usuarios de Tor no cifran la comunicación de extremo a extremo ellos puede estar sujeto a un riesgo adicional de la interceptación de datos por parte de terceros. Resumiendo: la ubicación del usuario permanece oculta, sin embargo, en algunos casos el contenido es vulnerable al análisis a través del cual también se puede obtener información sobre el usuario.

Uso del paquete Tor para navegadores
------------------------------------

El paquete Tor para navegadores le permite usar Tor en Windows, OSX o GNU/Linux sin necesidad de configurar al navegador web. Aún mejor, también es una aplicación portable que se puede ejecutar desde una unidad flash USB, lo que le permite llevarlo a cualquier PC sin necesidad de instalarlo en el disco rígido de cada computadora.

Descarga del paquete Tor para navegadores
-----------------------------------------

Puede descargarlo desde el sitio web de torproject.org ([https://www.torproject.org](https://www.torproject.org)).

Si su país restringe el acceso al sitio web de tor, tipee "tor mirrors" en su motor de búsqueda web favorito: el resultado probablemente incluya algunas direcciones alternativas para descargarlo.

Por favor, siga las instrucciones del sito web del proyecto Tor acerca de cómo instalarlo.

Precaución: cuando usted descarga el paquete Tor (en sus versiones completa o dividida), debería verificar las firmas de los archivos, especialmente si lo está descargando desde un sitio espejo. Este paso le asegura que los archivos no han sido falsificados. Para aprender más acerca de archivos de firma y cómo revisarlos, consulte [https://www.torproject.org/docs/verifying-signatures](https://www.torproject.org/docs/verifying-signatures)


Ejecutando un repetidor o un puente
-----------------------------------

Tor es una red de voluntarios que ejecutan repetidores y puentes. Si desea ayudar al crecimiento de la red Tor contribuyendo con ancho de banda y ciclos extra de CPU, considere ejecutar un repetidor. Además, al correr un repetidor puede mejorar su anonimato ya que un atacante no puede distinguir entre el tráfico originado por usted o por el repetidor. Consulte [https://www.torproject.org/docs/faq.html.en#BetterAnonymity](https://www.torproject.org/docs/faq.html.en#BetterAnonymity) para obtener más detalles.

Sin embargo, si usted corre un repetidor, su dirección IP será listada en Internet como un repetidor Tor. Los clientes Tor dependen de esta lista, provista por los servidores del directorio de Tor, para poder establecer los circuitos. Si desea contribuir con Tor, pero no desea correr un repetidor público, considere ejecutar un puente. Ya que los repetidores Tor son públicos, algunos ISP bloquean el acceso a la red Tor bloqueando *todos los repetidores.*  Los puentes Tor, sin embargo, no están listados y además, son más difíciles de hallar.

La meta de Tor es proteger el anonimato en Internet, pero algunas veces se usa con fines ilegales. Como operador de un repetidor, consulte [https://www.torproject.org/eff/tor-legal-faq.html](https://www.torproject.org/eff/tor-legal-faq.html), escrito por la Electronic Frontier Foundation (EFF). La EFF es una organización sin fines de lucro de EE.UU. cuya misión es "proteger sus derechos digitales." En otros países, deberían buscar asesoramiento de organizaciones similares. Sin embargo, los riesgos legales pueden ser minimizados corriendo un repetidor que no sea de salida o un puente.

Si desea configurar su computadora para correr un repetidor o un puente, visite el [https://www.torproject.org/docs/tor-doc-relay.html.en](https://www.torproject.org/docs/tor-doc-relay.html.en) para obtener instrucciones.
