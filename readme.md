# Arquitectura de Software Grupo 02
## Integrantes
* Javier Enrique Olazábal Silva [(Itsjavito)](https://github.com/ItsJavito)
* Lelis Raquel Atencia Mondragón [(atencia22)](https://github.com/atencia22)
* Angel Cuya Sanchez [(galadto)](https://github.com/galadto)
* Francisco Diaz Delgado [(fmdd00)](https://github.com/fmdd00)
## Tema de proyecto (Juez en línea)
Para el trabajo en grupo hemos definido utilizar como tema de trabajo la arquitectura de un software como lo es un juez online, como lo es BOCA, Codeforces, UVA, etc.

## 1. Caso de Negocio
### 1.1. Generalidades
Ulitorneos es una plataforma virtual con sede en Lima. Se dedica a ofrecer una experiencia de competencia en línea, similar a un "online judge", que permite a los participantes involucrarse en torneos de programación y desafíos similares. Su enfoque se encuentra en la virtualidad, lo que significa que opera en un entorno completamente en línea, lo que facilita la participación desde cualquier ubicación geográfica.

### 1.2. Modelo de Negocio
#### 1.2.1. Descripción
El modelo de negocio de la empresa se centra principalmente en generar ingresos a través de suscripciones premium, ofreciendo a los usuarios una versión mejorada y más completa de su plataforma o servicio a cambio de una tarifa periódica. El tipo de negocio sería B2B. Los usuarios serían las instituciones que quieran llevar a cabo los torneos.
#### 1.2.2. Objetivos del Negocio
- Desarrollar una plataforma funcional y atractiva que ofrezca la experiencia de competencia en línea.
- Probar la plataforma con un grupo inicial de usuarios para identificar posibles problemas y realizar mejoras.
- Concentrar esfuerzos en atraer los primeros usuarios y construir una base de usuarios sólida.
#### 1.2.3. Business Model Canvas

##### Segmentos de Clientes:
- Instituciones que quieran tener torneos de programación.

##### Propuesta de Valor:
- Experiencia de competencia en línea.
- Adaptabilidad para que la plataforma se adecúe a las necesidades de la institución.
- Acceso a una plataforma virtual desde cualquier ubicación.

##### Canales:
- Plataforma en línea (sitio web).
- Publicidad en línea.
- Redes sociales.
- Alianzas con instituciones educativas.

##### Relaciones con los Clientes:
- Soporte en línea.
- Comunidad en línea (foros, redes sociales).

##### Fuentes de Ingresos:
- Suscripciones premium (ingresos recurrentes).

##### Recursos Clave:
- Plataforma en línea.
- Tecnología de competencia en línea.

##### Actividades Clave:
- Desarrollo y mantenimiento de la plataforma.
- Consultoría a institución que quiera organizar el torneo.
- Marketing y promoción en línea.

##### Asociaciones Clave:
- Alianzas con instituciones educativas.
- Colaboraciones con empresas de tecnología.

##### Estructura de Costos:
- Desarrollo y mantenimiento de la plataforma.
- Costos de personal.
- Publicidad y marketing en línea.

### 1.3. Estructura del Equipo
El equipo detrás de Ulitorneos está compuesto por cuatro miembros clave. Javier lidera el proyecto, y junto a Angelo, Francisco y Lelis, todos ellos desempeñan roles de desarrollo en el proyecto. Dado el tamaño reducido del equipo, no se han establecido divisiones por áreas funcionales o departamentos. La fuerza del equipo radica en su experiencia preprofesional en desarrollo de software, con competencias que abarcan lenguajes como Python, JavaScript, SQL, y más.

### 1.4. Listado de Stakeholders
En cuanto a los stakeholders, en este momento no hay inversores o accionistas involucrados en Ulitorneo, ya que el proyecto se desarrolla como parte de un curso académico y no tiene fines lucrativos. Los clientes potenciales incluyen instituciones que deseen organizar hackathons y programadores interesados en participar en competencias. Las partes interesadas más destacadas son los propios desarrolladores (Javier, Angelo, Francisco y Lelis) y el profesor del curso (José Caballero), quienes tienen un interés significativo en que el proyecto sea exitoso, dada su dedicación al desarrollo del mismo como parte de su formación académica.

## 2. Requerimientos del Sistema

### 2.1. Requerimientos Funcionales
#### US01: Registro de usuario
Como usuario, quiero poder crear una cuenta nueva, con un correo (revisar esto), usuario y una contraseña, para acceder a la plataforma.
#### US02: Inicio de sesión
Como usuario, quiero poder ingresar al sistema con los datos de usuario que registré, para poder acceder a las funciones de la plataforma.
#### US03: Modificar datos personales
Como usuario, quiero poder modificar mi nombre de usuario, contraseña y el país, para tener mis datos siempre actualizados.
#### US04: Cerrar sesión
Como usuario, quiero poder cerrar mi sesión del sistema, para dar por culminado mi trabajo.
#### US05: Visualizar problemas
Como usuario, quiero poder visualizar el nombre y la descripción de los problemas que puedo resolver, para estar conocer los detalles de estos.
#### US06: Subir solución
Como usuario, quiero seleccionar un problema y subir los archivos de código fuente, para presentar una solución.
#### US07: Visualización del tiempo del concurso
Como usuario, quiero poder ver el tiempo restante del concurso, para poder organizarme de la mejor manera.
#### US08: Visualizar resultados
Como usuario, quiero poder visualizar la información de los problemas y las respectivas soluciones que presenté, así como el tiempo que tomé, el lenguage utilizado, y la respuesta por parte del juez, para seguir el récord de mis soluciones presentadas.
#### US09: Visualizar puntajes globales
Como usuario, quiero poder ver los puntajes a nivel global de otros usuarios que han presentado sus soluciones, con datos como el nombre de usuario, el país, el instituto, los problemas que ha resuelto y el puntaje total, para hacer un seguimiento del progreso de otros usuarios.

-----
### US10: Registrar nuevo concurso 
Como Usuario, quiero poder crear mi concurso de programación con la cantidad de participantes, el tiempo del concurso, las fechas límites del concurso y las características como los títulos, descripciones, etc. 

### US11: Subir problemas al concurso creado 
Como usuario, debería poder subir los problemas para el concurso que he creado junto a sus casos de prueba y los límites que este necesita. 

### US12: Modificar el concurso 
Como usuario, debería poder modificar una vez creado el concurso creado, tanto como el título, la cantidad de participantes, las fechas, lo límites, etc. 

### US13: Modificar los problemas del concurso
Como usuario, debería poder modificar los problemas creados junto a los límites y las características del problema. 

---
<!-- #### // Requerimientos por evaluar: Existen otras funcionalidades nuestras plataformas modelo ofrecen y que se necesitan evaluar para su implementación en la nuestra. Como usuario del sistema, existen opciones realizar clarificaciones respecto a un problema, ver tastks y realizar backups. Como administrador del sistema, se pueden crear y modificar los datos de competencias, ver logs, reportes, los usuarios en una competencia, entre otros. // -->

### 2.2. Flujo de Interacción con la Plataforma Ulitorneos: (Flujo principal)

1. El usuario accede a la página de inicio de Ulitorneos.
2. El usuario hace clic en "Registro de Usuario" (US01) para crear una cuenta nueva.
3. El usuario completa el formulario de registro, proporcionando su correo electrónico, nombre de usuario y contraseña.
4. Después de completar el registro, el usuario inicia sesión en la plataforma haciendo clic en "Inicio de Sesión" (US02) y proporciona sus credenciales recién creadas.
5. Una vez dentro de la plataforma, el usuario puede acceder a su perfil y seleccionar la opción "Modificar Datos Personales" (US03) para actualizar su nombre de usuario, contraseña y país.
6. Cuando el usuario haya terminado de usar la plataforma, puede hacer clic en "Cerrar Sesión" (US04) para salir de su cuenta.
7. Para resolver problemas, el usuario puede acceder a la sección "Visualizar Problemas" (US05) y ver una lista de problemas disponibles con sus nombres y descripciones.
8. El usuario elige un problema específico y hace clic en "Subir Solución" (US06) para cargar sus archivos de código fuente y presentar una solución.
9. Mientras participa en un concurso, el usuario puede ver el tiempo restante del concurso en la sección "Visualización del Tiempo del Concurso" (US07).
10. El usuario puede ver los resultados de sus soluciones en la sección "Visualizar Resultados" (US08), donde se muestra información como el tiempo tomado, el lenguaje utilizado y la respuesta del juez.
11. Además, el usuario puede explorar los puntajes globales de otros participantes en la sección "Visualizar Puntajes Globales" (US09), donde se proporcionan datos como el nombre de usuario, país, instituto y puntaje total.

### 2.3. Requerimientos de Atributos de Calidad (Escenarios)

A continuación, se presenta una tabla que resume los atributos de calidad, sus descripciones y los escenarios asociados:

| Atributo | Descripción | Escenario |
|--------------------------|---------------------------|-------------------------|
| Precisión               | Evaluar soluciones de manera precisa.              | Un estudiante envía una solución y la plataforma informa incorrectamente que es incorrecta cuando en realidad es correcta. |
| Confiabilidad          | Funcionar sin interrupciones significativas.       | Un grupo de estudiantes está en una competencia y la plataforma experimenta tiempos de inactividad frecuentes. |
| Escalabilidad          | Manejar una carga creciente sin degradación del rendimiento. | En una competencia importante, la plataforma enfrenta un aumento significativo en el número de usuarios. |
| Retroalimentación Detallada | Proporcionar retroalimentación detallada sobre las soluciones. | Después de enviar una solución, la plataforma ofrece información vaga sobre por qué falló sin identificar específicamente los casos de prueba. |
| Seguridad              | Proteger la integridad de los datos y prevenir intentos de trampas. | Un usuario malintencionado intenta obtener acceso no autorizado o distribuir contenido malicioso. |
| Usabilidad             | Ofrecer una interfaz de usuario intuitiva y fácil de usar. | Un profesor encuentra la interfaz de administración confusa y difícil de navegar. |
| Rendimiento            | Proporcionar respuestas rápidas y tiempos de ejecución eficientes. | La plataforma tarda mucho tiempo en evaluar una solución, causando tiempos de espera frustrantes. |
| Flexibilidad           | Permitir la configuración y personalización de problemas y competencias. | Un instructor desea personalizar los criterios de evaluación, pero la plataforma no permite configuración personalizada. |
| Documentación y Soporte | Ofrecer documentación clara y soporte adecuado.    | Un estudiante nuevo no puede encontrar documentación o tutoriales claros. |
| Mantenimiento          | Mantenerse actualizada y recibir mejoras periódicas. | La plataforma no ha recibido actualizaciones ni correcciones de errores durante un período prolongado. |
| Integración            | Integrarse con otros sistemas y herramientas.      | Un centro educativo desea integrar la plataforma con su sistema de gestión de aprendizaje (LMS). |

### 2.4. Restricciones

- Tecnologías Propias: Nosotros desarrollamos todas las tecnologías internamente, incluyendo el marco de trabajo y las políticas de seguridad.

- Idioma de Desarrollo: El sistema se desarrollará utilizando un único lenguaje de programación, que es Python.

- Base de Datos Relacional: Utilizaremos una base de datos relacional para almacenar datos críticos del usuario y resultados de competencias.

- Servidores Propios: Todos los servidores y recursos de la plataforma estarán ubicados en nuestro centro de datos, no utilizaremos servicios de nube externos.

- Política de Seguridad Rigurosa: Implementaremos una política de seguridad rigurosa que incluye autenticación de dos factores y cifrado de datos en reposo y en tránsito.

## 3. Decisiones a Nivel de Arquitectura

### 3.1. Asignación de Responsabilidades

### 3.2. Modelo de Coordinación

### 3.3. Modelo de Datos

### 3.4. Mapeo entre Elementos de Arquitectura

### 3.5. Elección de Tecnología ….

## 4. Tácticas

### 4.1. Disponibilidad

### 4.2. Mantenibilidad

### 4.3. Interoperabilidad

### 4.4. Rendimiento

### 4.5. Seguridad …

## 5. Anexo: Tópicos en Arquitectura de Software (Por alumno)

### 5.1. Tema / Alumno

### 5.2. Desarrollo Conceptual

### 5.3. Consideraciones Técnicas

#### 5.3.1. Instalación / Configuración de Servicio

#### 5.3.2. Primeros pasos

### 5.4. Demo

#### 5.4.1. Escenario práctico

#### 5.4.2. Pasos para la demo

#### 5.4.3. Resultados

## 6. Referencias
