Mensajería segura
=================

Los SMS son mensajes cortos enviados entre teléfonos móviles. El texto se envía sin cifrar y pueden ser leídos y almacenados por los proveedores de telefonía móvil y otras partes que tienen acceso a la infraestructura de la red a la que está conectado. Para evitar que sus mensajes sean interceptados usted tiene que utilizar cifrado punto a punto en sus mensajes de texto.

Android
-------
 * **TextSecure** - WhisperSystems provee un sistema de cifrado de SMS para Android llamado TextSecure, basado en la criptografía de clave pública que asegura que los mensajes se cifren desde la conexión y que también se almacenen en una base de datos cifrada en el dispositivo, sin embargo, para asegurar el cifrado de la conexión, ambas partes deben usar la aplicación, Es [Open Source](https://github.com/WhisperSystems/TextSecure/) y está disponible a través de [PlayStore](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms&hl=en)

La tecnología detrás del cifrado (llamada //axolotl//) extiende el protocolo OTR para que el mensaje pueda ser cifrado y enviado aunque no estén online todas las partes intervinientes en la comunicación.

