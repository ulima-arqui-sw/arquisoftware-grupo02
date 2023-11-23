# Patron Pub - Sub

## Conceptos generales 

### Definicion del patrón 
El patrón Pub/Sub es un modelo de mensajería en el que los componentes de un sistema se comunican entre sí sin estar directamente acoplados. En lugar de quer los componentes se comuniquen directamente unos con otros, lo hacen a través de un intermediario llamada "Canal" o "topic". Este intermediarío maneja la distribución de los mensajes. 

### Definiciones generales sobre el patrón
* **Publicador**: es la entidad que envía mensajes. No necesita conocer quienes son los suscriptores ni cómo se manejan los mensjaes después de ser publicados. 

* **Canal o Tema**: Es el medio a través del cual se distribuyen los mensajes. Los publicadores envían sus mensajes al canal, y los suscriptores reciben mensajes del canala. Los canales pueden ser específicos para ciertos tipos de mensajes. 

* **Suscriptor**: Es la entidad que expresa interés en recibir mensajes de un canal específico. Se suscribe a un canal para recibir notificaciones sobre eventos o datos de interés.

* **Mensaje**:  La unidad de información que se envía a través del canal. Puede contener cualquier tipo de datos relevante para el sistema.

## Escenarios de uso 

* **Comercio electrónico**: Sistema de correo eletrónico donde se necesite notificar a los clientes sobre cambios en el estado de sus pedidos.
* **Juegos en tiempo real**: Juegos en linea com movimientos, cambios del entorno, tc. Se publican en un canal y los clientes se suscriben para recibir actualizaciones en tiempo real.  

## Vídeo
