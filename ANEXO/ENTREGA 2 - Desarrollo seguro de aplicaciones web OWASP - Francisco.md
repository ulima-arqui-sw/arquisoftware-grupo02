# Desarrollo seguro de aplicaciones con OWASP

* Enlace a la web -> [(OWASP)](https://owasp.org)

## Acerca de
Son las siglas de Open Web Application Security Project. Actualmente, es una de las comunidades más importantes a nivel de seguridad que existen a nivel global, cuyo objetivo primordial es concientizar, educar y promover las mejores prácticas de seguridad en las aplicaciones web, para protegerlas de ciberamenazas.

Entre las principales característcas que ofrece la "red" de OWASP, se encuentra:
* Recursos OWASP, entre los que se hallan guías y herramientas, permitiendo a cualquier organización mejorar a nivel de seguridad, y sin costo alguno, pues estos recursos son gratuitos.
* Una comunidad llena de expertos provenientes de todas partes del mundo, que trabaja y apoya con dedicación para la detección y mitigación de riesgos y amenazas de seguridad.
* Promueve la seguridad de aplicaciones web de manera proactiva, buscando mentalizar a los desarrolladores a abordar las amenazas antes de que se conviertan en problemas reales.

## Proyectos OWASP
### 1. OWASP Top 10
Este es un documento que brinda una guía de manera detallada en relación a la seguridad en aplicaciones web. Constantemente, OWASP publica una lista de las 10 vulnerabilidades más recurrentes en aplicaciones web.

Para el 2021, la lista de vulnerabilidades más importantes identificadas por OWASP es la siguiente:
* A1: Pérdida de acceso
* A2: Fallas criptográficas
* A3: Inyección
* A4: Diseño inseguro (nuevo)
* A5: Configuración de seguridad incorrecta
* A6: Componentes vulnerables y desactualizados
* A7: Fallas de identificación y autenticación
* A8: Fallas en el software y en la integridad de los datos (nuevo)
* A9: Fallas en el registro y monitoreo
* A10: Falsificación de solicitudes del lado del servidor

Esta lista, como se mencionó, cambia a medida que surjan amenazas importantes, y que estas se vuelvan recurrentes. Para el 2017, la lista era la siguiente:

<img src="https://www.arsys.es/blog/file/uploads/2022/06/OWASPgraph-1536x780.jpg" alt="2017top10" width="600">

### 2. OWASP Web Security Testing Guide
Es un framework que se encarga de brindar una serie de recursos de testeo para aplicaciones y servicios web. Incluyre las mejores prácticas, que han sido empleadas por organizaciones y pentesters en todo el mundo. La versión más actual de la guía es la 5.0.

A diferencia de la Top 10, esta guía no se centra en los tecnicismos al momento de desarrollar un software, y tampoco en realizar pruebas a las funcionalidades de este. Simplemente se enfoca en definir a los actores, amenazas, factores de riesgo, prevalencia de las vulnerabilidades y la explotabilidad.

#### Framework de testing OWASP
<img src="https://thehackerway.files.wordpress.com/2021/02/typical_sdlc_testing_workflow.gif" alt="intermediario" width="600">

### 3. OWASP ZAP
La Zed Attack Proxy (ZAP), es una herramienta gratuita de tipo "proxy de intermediario", enfocada al pentesting de aplicaciones web mediante el escaneo de vulnerabilidades.

Es considerada como proxy de intermediario debido a que se ubica entre el navegador del tester y el app web que se va a testear, con el objetivo de interceptar los mensajes enviados entre estos dos, realizar ciertas modificaciones, de ser necesario, y enviarlos de nuevo al destino.

<img src="https://kajabi-storefronts-production.kajabi-cdn.com/kajabi-storefronts-production/blogs/2147492532/images/5ocLZAERQz2YWRAokBky_guardar1.png" alt="intermediario" width="600">

#### Ventajas:
* Es multiplataforma, pudiendo funcionar tanto en Linux como en Mac, además de, obviamente, sistemas Windows.
* Genera informes, que pueden ser guardados de manera local.
* De fácil uso, que incluso puede ser utilizada por personas aspirantes al pentesting o gente principiante.
* 100% gratuita.

#### Funcionalidades
Entre sus funcionalidades principales, se encuentran:
* Gestión de contextos
* Marketplace de extensiones
* Manipulación de peticiones con Requester
* Verificación de controles de acceso
* Scripts de tipo Zest
* API Rest

Se empleará esta herramienta para realizar una demostración de análisis de vulnerabilidades.
## Demo - OWASP ZAP
Video de demostración de la herramienta OWASP ZAP, para el análisis de vulnerabilidades de la web de ULITORNEOS, desarrollada por nosotros, el grupo 2.
Hay que tener en cuenta que debe tener instalado la versión de Java específica para la versión de ZAP descargada.
* ZAP 2.12.0 and later requires a minimum of Java 11
* ZAP 2.7.0 and later requires a minimum of Java 8
* ZAP 2.0.0 and later requires a minimum of Java 7
* Previous versions of ZAP also support Java 6, the last of those being 1.4.1

Para la demo, se descargó ZAP versión 2.14.0 [(Enlace)](https://www.zaproxy.org/download/), por lo cual, la versión de Java  requerida es la 11.

<img src="https://upload.wikimedia.org/wikipedia/commons/b/b0/OWASP-ZAP.png" alt="intermediario" width="600">

* Enlace al video de la demo -> [(OWASP | Análisis de vulnerabilidades con ZAP)](https://youtu.be/S-lb4YSl9Ds)