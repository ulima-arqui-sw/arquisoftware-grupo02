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
- Ofrecer un entorno de creacion de concursos mas el compilador de juez, asi como el uso de datos para marketing.
- Contactar a programadores destacadas en base a logros en la plataforma
#### 1.2.3. Business Model Canvas

##### Segmentos de Clientes:
- Universidades
- Empresas de reclutamiento de desarrolladores con empresas 
- Instituciones que quieran tener torneos de programación.

##### Propuesta de Valor:
- Experiencia de competencia en línea.
- Adaptabilidad para que la plataforma se adecúe a las necesidades de la institución en el aspecto de "look an feel"
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
- Suscripciones premium para los concursantes(ingresos recurrentes).

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

|           Rol            |     Encargado     |                   Descripción                  |
|--------------------------|-------------------|----------------------------------------------|
|         Cliente          | Organizaciones | La institución organizadora que utiliza la plataforma para crear y gestionar hackathons. Son responsables de configurar competencias, establecer reglas y proporcionar desafíos a los participantes. |
|         Usuario          | Organizaciones y participantes | Los participantes en los hackathons, que pueden ser estudiantes de programación o programadores experimentados. Utilizan la plataforma para competir, enviar sus soluciones y recibir retroalimentación sobre sus códigos. |
|    Gestor de negocio     | Javier Olazabal | Encargado de la gestión estratégica y operativa de la plataforma. Definen las estrategias de crecimiento, colaboraciones y acuerdos comerciales con las instituciones organizadoras. Aseguran que la plataforma satisfaga las necesidades de los clientes. |
| Arquitecto de software   | Lelis Atencia| Diseña la estructura de la plataforma, incluyendo la arquitectura técnica y la infraestructura necesaria para soportar la carga de trabajo. Toma decisiones técnicas clave para garantizar la escalabilidad y la eficiencia. |
| Implementador e integrador| Francisco Diaz | Responsable de desarrollar, implementar y mantener las características técnicas de la plataforma. Codifican las funcionalidades requeridas, integran sistemas externos y aseguran que todo funcione correctamente. |
| Responsable de mantenimiento| Angel Cuya | Encargado de mantener y actualizar la plataforma en funcionamiento. Esto implica la solución de problemas técnicos, la aplicación de actualizaciones de seguridad y el monitoreo constante para garantizar el rendimiento y la disponibilidad. |
|         Performance Checker         | Javier Olazabal | Supervisa y gestiona la evaluación de los códigos enviados por los participantes. Realiza pruebas de compilación y ejecución para verificar la precisión y eficiencia de las soluciones. Contribuye a la imparcialidad y calidad de la plataforma al garantizar una evaluación precisa de los outcomes de los participantes. |


## 2. Requerimientos del Sistema

### 2.1. Requerimientos Funcionales
#### US01: Registro de usuario
Como usuario, quiero poder crear una cuenta nueva, con un correo (revisar esto), usuario y una contraseña, para acceder a la plataforma. También poder crear la cuenta utilzando los servicios de google para mayor facilidad. 
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




Atributo         | Código  | Entorno                                           | Fuente                                                         | Estímulo                                                                                                                  | Artefacto                                              | Respuesta                                                                                                          | Medida de Respuesta
-----------------|---------|--------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|---------------------
Escalabilidad    | ESC-01  | Proceso de envío de soluciones | Participantes | Miles de envíos en un periodo corto | Infraestructura de servidores | Activación automática de servidores adicionales | El servidor se activa en 15 segundos.
Escalabilidad    | ESC-02  | Proceso de compilación | Gestor de Proyecto | Solicitud de escalamiento vertical | Servidor | Ampliación de capacidad de almacenamiento del servidor | La plataforma aumenta su capacidad de almacenamiento en 40%.
Usabilidad       | ESC-03  | Proceso de creación de retos de programación | Encargado de crear retos | Intento de crear un nuevo reto | Interfaz de administración de la plataforma  | La plataforma cuenta con una interfaz de usuario intuitiva y amigable. | El tiempo promedio para configurar un problema es 5 minutos o menos.
Usabilidad       | ESC-04  | Proceso de navegacion web             | Estudiante nuevo                                              | Se registra en la plataforma e intenta explorarla                                                                      | Recursos de Orientación y Tutoriales                 | Se proporciona una orientación clara y tutoriales para los estudiantes nuevos                                | Tasa de Abandono (TA) menor al 20 %
Usabilidad       | ESC-05  | Creación de problemas                               | Profesor                                                       | Crear tareas de programación para sus estudiantes                                                                       | Interfaz de Administración de Problemas                | La interfaz de administración de problemas es intuitiva y fácil de usar | Tiempo de Configuración de Tareas maximo de 4 minutos
Usabilidad       | ESC-06  | Proceso de navegacion web           | Estudiante nuevo                                              | Resolver problemas de práctica                                                      | Interfaz de Usuario                                  | Tener una interfaz de usuario clara, organizada y fácil de usar | Tiempo de Acceso a Funciones Básicas max de 5 minutos, TA menor al 20%
Disponibilidad   | ESC-07  | Proceso de Recuperacion por caidas | Participantes en la competencia, administradores | Uno de los servidores de la plataformas se cae | Servidores de la Plataforma | La plataforma no debe verse interrumpida por tiempos de inactividad inesperados | Duración del Tiempo de Inactividad menor de 1 minuto
Disponibilidad   | ESC-08  | Proceso de envios de soluciones| Participantes, administradores, proveedor de servicios de alojamiento | Enviar sus soluciones masivas durante la competencia | Servicios de Alojamiento del Proveedor                  | Garantizar una alta disponibilidad y evitar fallas del proveedor de servicios | Tiempo de Disponibilidad, Registro de Interrupciones max de 2
Disponibilidad   | ESC-09  | Proceso de gestion de cortes de energia | Personal de mantenimiento del centro de datos | corte de energia en el centro de datos de la plataforma | Infraestructura del Centro de Datos                  | Medidas de redundancia y sistemas de respaldo adecuados | Duración de la Interrupción max de 1 min
Rendimiento      | ESC-10  | Proceso de evalucion de problemas | Programadores participantes                                     | Envio de soluciones altamente complejos | Sistema de Evaluación de Soluciones                    | Manejar eficientemente la carga computacional de soluciones complejas | Tiempo de Evaluación max de 1 min
Rendimiento      | ESC-11  | Proceso de evalucion de problemas     | Competidores                                                    |solución que contiene un bucle Infinito | Sistema de Evaluación de Soluciones | Manejar situaciones de bucle infinito en las soluciones de los usuarios| Tiempo de Ejecución max de 1 min, Recursos Consumidos, Número de Soluciones con Bucle Infinito
Rendimiento      | ESC-12  | Proceso de evalucion de problemas | Estudiante                                                      |solución correcta pero optimizado    | Sistema de Evaluación de Soluciones                    |Detectar soluciones ineficientes para evitar que afecten negativamente el rendimiento  | Recursos Consumidos, Número de Soluciones Ineficientes
|Seguridad|ESC-13|Plataforma en funcionamiento|Usuario|Transacción errada|Escáner de seguridad|Sistema realiza escaneos regulares para identificar vulnerabilidades|Número de vulnerabilidades identificadas
|Seguridad|ESC-14|Plataforma en funcionamiento|Usuario|Intento de ciberataque|Módulo de acceso a datos|Sistema impide el acceso no autorizado a datos confidenciales|Número de intentos bloqueados
|Seguridad|ESC-15|Proceso de autenticaicón|Usuario|Inicio de sesión fallido|Módulo de autenticación|Sistema detecta y bloquea intentos de inicio de sesión fallidos|Número de intentos bloqueados
|Mantenibilidad|ESC-16|Plataforma despleagada|Usuario|Notificación de error|Código fuente|Equipo de desarrollo puede localizar y corregir errores fácilmente|Tiempo promedio de corrección de errores
|Mantenibilidad|ESC-13|Mantenimiento de plataforma|Gestor de proyecto|Solicitud de nueva funcionalidad|Código fuente|Nuevas características se pueden implementar sin perjudicar al sistema|Tiempo promedio para implementar nuevas características
|Mantenibilidad|ESC-16|Proceso de QA a módulo|Conformance checker|Notificación de error|Suite de pruebas automatizadas|Suite de pruebas ayuda a identificar problemas rápidamente|Porcentaje de cobertura de pruebas automatizadas
|Interoperabilidad|ESC-17|Proceso de inicio de sesión|Usuario|Intento de inicio de sesión|Módulo de autenticaición|Usuarios pueden iniciar sesión utilizando cuentas existentes en otras plataformas|Número de sistemas admitidos
|Interoperabilidad|ESC-18|Desarrollo de plataforma|Empresa dueña del IDE|IDE utilizado deja de ser open source|IDE|Integración con IDEs|Número de IDEs compatibles


ESCENARIOS


| Escenarios                                       | Requerimiento funcional relacionado |
|--------------------------------------------------|---------------------------|
| ESC-1                                                 |                           |
| ESC-2                                                 |                           |
| ESC-3                                                 |                           |
| ESC-4                                                 |                           |
| ESC-5                                                 |                           |
| ESC-6                                                 |                           |
| ESC-7                                                 |                           |
| ESC-8                                                 |                           |
| ESC-9                                                 |                           |
| ESC-10                                                 |                           |
| ESC-11                                                 |                           |
| ESC-12                                                 |                           |
| ESC-13                                                 |                           |
| ESC-14                                                 |                           |
| ESC-15                                                 |                           |
| ESC-16                                                 |                           |
| ESC-17                                                 |                           |







### 2.4. Restricciones

- Tecnologías Propias: Nosotros desarrollamos todas las tecnologías internamente, incluyendo el marco de trabajo y las políticas de seguridad.

- Idioma de Desarrollo: El sistema se desarrollará utilizando un único lenguaje de programación, que es Python.

- Base de Datos Relacional: Utilizaremos una base de datos relacional para almacenar datos críticos del usuario y resultados de competencias.

- Servidores Propios: Todos los servidores y recursos de la plataforma estarán desplegados en la nube.

- Política de Seguridad Rigurosa: Implementaremos una política de seguridad rigurosa que incluye autenticación de dos factores y cifrado de datos en reposo y en tránsito.

## 3. Decisiones a Nivel de Arquitectura
En esta sección se va especificar los módulos de 
### 3.1. Asignación de Responsabilidades

### 3.2. Modelo de Coordinación

### 3.3. Modelo de Datos

### 3.4. Mapeo entre Elementos de Arquitectura

### 3.5. Elección de Tecnología ….

## 4. Tácticas




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
