# Arquitectura de Software Grupo 02
## Integrantes
* Javier Enrique Olazábal Silva [(Itsjavito)](https://github.com/ItsJavito)
* Lelis Raquel Atencia Mondragón [(atencia22)](https://github.com/atencia22)
* Angel Cuya Sanchez
* Francisco Diaz Delgado 
## Tema de proyecto (Juez en línea)
Para el trabajo en grupo hemos definido utilizar como tema de trabajo la arquitectura de un software como lo es un juez online, como lo es BOCA, Codeforces, UVA, etc.

## 1. Caso de Negocio
### 1.1. Generalidades
Ulitorneos es una plataforma virtual con sede en Lima. Se dedica a ofrecer una experiencia de competencia en línea, similar a un "online judge", que permite a los participantes involucrarse en torneos de programación y desafíos similares. Su enfoque se encuentra en la virtualidad, lo que significa que opera en un entorno completamente en línea, lo que facilita la participación desde cualquier ubicación geográfica.
### 1.2. Modelo de Negocio
El núcleo del modelo de negocio de Ulitorneos es proporcionar una plataforma que permita la organización de torneos tipo hackathon y la interacción en tiempo real entre jueces y participantes. Su público objetivo abarca instituciones que deseen organizar competencias de programación, como hackathons, así como programadores de todos los niveles que estén interesados en participar en estos eventos. Actualmente, la plataforma no genera ingresos, ya que se encuentra en sus primeras etapas de desarrollo, y los gastos se limitan principalmente al mantenimiento del servidor y el uso de herramientas en la nube.
### 1.3. Estructura del Equipo
El equipo detrás de Ulitorneos está compuesto por cuatro miembros clave. Javier lidera el proyecto, y junto a Angelo, Francisco y Lelis, todos ellos desempeñan roles de desarrollo en el proyecto. Dado el tamaño reducido del equipo, no se han establecido divisiones por áreas funcionales o departamentos. La fuerza del equipo radica en su experiencia preprofesional en desarrollo de software, con competencias que abarcan lenguajes como Python, JavaScript, SQL, y más.
### 1.4. Listado de Stakeholders
En cuanto a los stakeholders, en este momento no hay inversores o accionistas involucrados en Ulitorneo, ya que el proyecto se desarrolla como parte de un curso académico y no tiene fines lucrativos. Los clientes potenciales incluyen instituciones que deseen organizar hackathons y programadores interesados en participar en competencias. Las partes interesadas más destacadas son los propios desarrolladores (Javier, Angelo, Francisco y Lelis) y el profesor del curso (José Caballero), quienes tienen un interés significativo en que el proyecto sea exitoso, dada su dedicación al desarrollo del mismo como parte de su formación académica.
## 2. Requerimientos del Sistema

### 2.1. Requerimientos Funcionales
#### US01: Registro de usuario
Como usuario, quiero poder crear una cuenta nueva, con un correo (revisar), usuario y una contraseña, para acceder a la plataforma.
#### US02: Inicio de sesión
Como usuario, quiero poder ingresar al sistema con los datos de usuario que registré, para poder acceder a las funciones de la plataforma.
#### US03: Modificar datos personales
Como usuario, quiero poder modificar mi nombre de usuario, contraseña y el país, para tener mis datos siempre actualizados.
#### US04: Cerrar sesión
Como usuario, quiero poder cerrar mi sesión del sistema, para dar por culminado mi trabajo.
#### US05: Visualizar problemas
Como usuario, quiero poder visualizar el nombre y la descripción de los problemas que puedo resolver, para estar conocer los detalles de estos.
#### US06: Subir solución
Como usuario, quiero seleccionar un problema y subir los archivos de sódigo fuente, para presentar una solución.
#### US07: Visualización del tiempo del concurso
Como usuario, quiero poder ver el tiempo restante del concurso, para poder organizarme de la mejor manera.
#### US08: Visualizar resultados
Como usuario, quiero poder visualizar la información de los problemas y las respectivas soluciones que presenté, así como el tiempo que tomé, el lenguage utilizado, y la respuesta por parte del juez, para seguir el récord de mis soluciones presentadas.
#### US09: Visualizar puntajes globales
Como usuario, quiero poder ver los puntajes a nivel global de otros usuarios que han presentado sus soluciones, con datos como el nombre de usuario, el país, el instituto, los problemas que ha resuelto y el puntaje total, para hacer un seguimiento del progreso de otros usuarios.
### 2.2. Requerimientos de Atributos de Calidad (Escenarios)
Precisión: La plataforma debe ser precisa en la evaluación de las soluciones de los usuarios. Debe ser capaz de determinar con precisión si una solución es correcta o incorrecta y proporcionar retroalimentación precisa sobre los casos de prueba que fallaron. 
ESCENARIO: Imagine que un estudiante ha enviado una solución a un problema de programación en la plataforma. La plataforma debe ser capaz de determinar de manera precisa si la solución es correcta o incorrecta según las pruebas establecidas. Si la plataforma informa incorrectamente que una solución es incorrecta cuando en realidad es correcta, esto sería un problema de precisión.


Confiabilidad: La plataforma debe estar disponible y funcionar de manera confiable en todo momento. Los usuarios deben poder acceder a ella sin interrupciones significativas. ESCENARIO: Suponga que un grupo de estudiantes está participando en una competencia de programación en línea y, durante la competencia, la plataforma se cae o experimenta tiempos de inactividad frecuentes. Esto interrumpiría la competencia y afectaría la experiencia de los usuarios debido a la falta de confiabilidad.


Escalabilidad: Debe ser capaz de manejar una carga creciente de usuarios y soluciones sin degradación del rendimiento. Esto es especialmente importante en competencias en línea que pueden atraer a miles de participantes.
ESCENARIO: En una competencia importante, la plataforma enfrenta un aumento significativo en el número de usuarios que intentan enviar soluciones al mismo tiempo. Si la plataforma no es capaz de manejar esta carga adicional y se vuelve lenta o inaccesible, esto muestra una falta de escalabilidad.


Retroalimentación Detallada: Debe proporcionar retroalimentación detallada sobre las soluciones de los usuarios, incluyendo información sobre los casos de prueba que fallaron y sugerencias para la corrección.
ESCENARIO: Después de que un estudiante envía una solución, la plataforma le proporciona información vaga sobre por qué su solución falló sin identificar específicamente los casos de prueba que no pasaron. Esto dificulta que el estudiante comprenda y corrija su error, lo que refleja una falta de retroalimentación detallada.


Seguridad: La plataforma debe ser segura para proteger la integridad de los problemas, las soluciones y los datos de los usuarios. Esto incluye la prevención de intentos de trampas y protección contra vulnerabilidades de seguridad.
ESCENARIO: Un usuario malintencionado intenta utilizar la plataforma para obtener acceso no autorizado a problemas o soluciones de otros usuarios o para distribuir contenido malicioso. La plataforma debe ser capaz de prevenir estos intentos y proteger la seguridad de los datos.


Usabilidad: La plataforma debe ser fácil de usar para los usuarios, tanto para aquellos que envían soluciones como para aquellos que crean y administran problemas. La interfaz de usuario debe ser intuitiva.
ESCENARIO: Un profesor que desea crear un nuevo problema en la plataforma encuentra la interfaz de administración confusa y difícil de navegar. La plataforma debería tener una interfaz de usuario intuitiva y fácil de usar tanto para profesores como para estudiantes.


Rendimiento: Debe proporcionar respuestas rápidas y tiempos de ejecución eficientes al evaluar las soluciones de los usuarios. Los tiempos de espera prolongados pueden ser frustrantes para los participantes. 
ESCENARIO: Cuando un estudiante envía una solución, la plataforma tarda mucho tiempo en evaluarla, lo que provoca que los estudiantes experimenten tiempos de espera frustrantes. El rendimiento deficiente de la plataforma afecta negativamente la experiencia del usuario.


Flexibilidad: Debe ser flexible y permitir la configuración y personalización de problemas y competencias. Los administradores deben poder definir sus propios problemas y reglas.
ESCENARIO: Un instructor desea personalizar los criterios de evaluación para un problema específico, pero la plataforma no permite una configuración personalizada. La falta de flexibilidad en la plataforma limita la capacidad de los instructores para adaptarse a sus necesidades específicas.


Documentación y Soporte: Debe ofrecer documentación clara y soporte adecuado para los usuarios, incluyendo tutoriales, ejemplos y una base de conocimientos.
ESCENARIO: Un estudiante nuevo en la plataforma no puede encontrar documentación o tutoriales claros sobre cómo enviar soluciones. La falta de documentación y soporte dificulta que los usuarios comprendan cómo utilizar la plataforma eficazmente.


Mantenimiento: La plataforma debe mantenerse actualizada y recibir mejoras periódicas para corregir errores, agregar nuevas características y mantenerse al día con las mejores prácticas de seguridad. 
ESCENARIO: La plataforma no ha recibido actualizaciones ni correcciones de errores durante un período prolongado. Esto puede llevar a problemas de seguridad no resueltos y a una falta de nuevas características que podrían mejorar la experiencia del usuario.


Escalabilidad: Debe ser capaz de manejar un aumento en el número de usuarios y problemas sin perder su rendimiento.
ESCENARIO: Durante una competencia importante, la plataforma maneja un gran aumento en el número de usuarios y problemas sin problemas. La capacidad de la plataforma para adaptarse a la creciente carga de trabajo muestra su escalabilidad.


Integración: La plataforma debe ser capaz de integrarse con otros sistemas y herramientas, como sistemas de gestión de aprendizaje, sistemas de seguimiento de competencias y sistemas de autenticación.
ESCENARIO: Un centro educativo utiliza un sistema de gestión de aprendizaje (LMS) y desea integrar la plataforma de juez en línea con su LMS para un acceso más fácil. La plataforma debe ser capaz de integrarse de manera efectiva con el LMS para proporcionar una experiencia de usuario fluida.


### 2.3. Restricciones

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
