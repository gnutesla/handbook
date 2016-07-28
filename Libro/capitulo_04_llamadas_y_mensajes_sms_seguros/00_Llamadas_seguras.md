Llamadas seguras
================

Las llamadas telefónicas hechas a través del sistema normal de telecomunicaciones tienen algunas formas de protección contra la intercepción de terceros, por ejemplo, los teléfonos móviles GSM cifran las llamadas. Sin embargo, no están cifradas de extremo a extremo, y los proveedores de telefonía están cada vez más obligados a dar a los gobiernos y a las instituciones de la ley acceso a sus llamadas. Además, el cifrado utilizado en GSM se ha roto y cualquier persona con interés y un capital suficiente puede comprar el equipo para interceptar llamadas. Un interceptor GSM ([http://en.interceptor.ws/catalog/2087.html](http://en.intercept.ws/catalog/2087.html)) es un dispositivo disponible para la plataforma para grabar conversaciones de teléfono móvil cuando se encuentra en las proximidades de la llamada. Los sistemas centralizados o propietarios como Skype también cifran las llamadas, pero están construidos con puertas traseras para que accedan los servicios secretos y los gobiernos con conocimiento de sus propietarios (en el caso de Skype, Microsoft). Adicionalmente, existe una una amplia clasificación de dispositivos llamados receptores IMSI los cuales pueden recolectar más información acerca de los teléfonos móviles, incluso el contenido de su comunicación.

Sin embargo, existen varias herramientas que usted puede utilizar para asegurar su teléfono usando cifrado punto a punto.

iOS - Instalando Signal
-----------------------

Los creadores de TextSecure proporcionan una herramienta FLOSS llamada Signal. [(https://itunes.apple.com/us/app/signal-private-messenger/id874139669?mt=8](https://itunes,apple.com/us/app/signal-private-messenger/id874139669?mt=8) Signal usa métodos de cifrado similares a SilentCircle pero provee su servicio con herramientas FLOSS. Además, su GUI (interfaz gráfica de usuario) es extremadamente fácil de usar. Signal detectará en forma transparente si usted está hablando con un usuario de Signal y le preguntará si desea establecer una "llamada segura" (con Signal) o una "llamada insegura" (sin cifrado punto a punto).


Android - Instalando RedPhone
-----------------------------

También de los creadores de Signal, existe una herramienta FLOSS llamada RedPhone. [https://play.google.com/store/apps/details?id=org.thoughtcrime.redphone&hi=en](https://play.google.com/store/apps/details?id=org.thoughtcrime.redphone&hl=en) Nuevamente, RedPhone usa métodos de cifrado similares a SilentCircle pero provee sus servicios usando herramientas FLOSS. También en este caso, su GUI detectará en forma transparente si usted está hablando con otros usuarios de Signal o RedPhone y le preguntará si desea establecer una "llamada segura" (con RedPhone) o una "llamada insegura" (sin cifrado punto a punto). Desafortunadamente, RedPhone requiere el framework de Google Play sino no trabajará en dichos teléfonos (Cyanogenmod u otras ROMs similares).
