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

ATRIBUTOS
Código  | Atributo          | Fuente       | Estímulo | Respuesta       | Entorno  | Artefacto    | Medida de Respuesta
--------|-------------------|--------------|-------------|-----------|--------------|------------|----------------------
|ESC-01  | Escalabilidad    | Participantes de la competencia, administradores de la plataforma | Miles de estudiantes en todo el mundo intentan enviar sus soluciones a problemas de programación en un lapso de tiempo muy corto debido a la fecha límite de la competencia. | la plataforma es capaz de escalar de manera efectiva y mantener tiempos de respuesta aceptables para los usuarios, sin experimentar ralentizaciones significativas o tiempos de inactividad. | competencia de programación en línea | Servidores de Aplicación, Balanceadores de Carga |  Tiempo de Respuesta     
| ESC-02 | Escalabilidad  | Administradores de la plataforma, estudiantes participantes.|   aumento en la demanda de competencias futuras por parte de otros departamentos  | la plataforma debe expandirse horizontalmente para admitir un mayor número de competencias y participantes sin degradación en el rendimiento o la disponibilidad   | El éxito de las competencias en un departamento          | Infraestructura de Servidores y Red(Este artefacto incluye tanto el hardware como el software necesarios para alojar y ejecutar la plataforma )          |  Capacidad de Usuarios Concurrentes  
| ESC-03 | Usabilidad  | Nuevo profesor |Intenta crear un nuevo problema o configurar una competencia|La plataforma debe contar con una interfaz de usuario intuitiva y amigable que permita a los profesores, incluso los nuevos, configurar y gestionar problemas y competencias de manera efectiva y sin dificultades innecesarias |Nuevo profesor entra a la plataforma |  Interfaz de Administración de la Plataforma | Número de Errores, Tiempo de Configuración 
| ESC-04 | Usabilidad     | Estudiante nuevo | se registra en la plataforma e intenta explorarla|La plataforma debe proporcionar orientación clara y tutoriales para los estudiantes nuevos|Primera vez entrando a la plataforma|Recursos de Orientación y Tutoriales|Tasa de Abandono, Tiempo para Comenzar a Resolver Problemas    
| ESC-05 | Usabilidad     | Profesor| crear tareas de programación para sus estudiantes |debe proporcionar una interfaz de administración de problemas intuitiva y fácil de usar para permitir que los profesores configuren tareas de programación de manera eficiente y sin dificultades innecesarias|creacion de problemas |Interfaz de Administración de Problemas|Tiempo de Configuración de Tareas,Número de Pasos o Clics,Satisfacción del Profesor  
| ESC-06 | Usabilidad     |Estudiante nuevo| intentar utilizar la plataforma para resolver problemas de práctica|debe proporcionar una interfaz de usuario clara, organizada y fácil de usar para que los estudiantes nuevos puedan encontrar y utilizar las funciones básicas sin dificultades innecesarias|estudiante se registra por primera vez|Interfaz de Usuario|Tiempo de Acceso a Funciones Básicas,Número de Intentos para Realizar una Acción,Tasa de Abandono
| ESC-07 | Disponibilidad |Participantes en la competencia,administradores de la plataforma|la plataforma de juez en línea sufre un tiempo de inactividad no planificado debido a un error de servidor|La plataforma de juez en línea debe mantener una alta disponibilidad para garantizar que las competencias importantes y otras actividades no se vean interrumpidas por tiempos de inactividad inesperados|competencia importante de programación en línea con miles de participantes,|Servidores de la Plataforma|Número de Participantes Afectados,Duración del Tiempo de Inactividad
| ESC-08 | Disponibilidad |Estudiantes participantes, administradores de la plataforma, proveedor de servicios de alojamiento|enviar sus soluciones durante la competencia| debe estar diseñada y configurada de manera que garantice una alta disponibilidad y evite interrupciones o fallas del proveedor de servicios de alojamiento durante competencias y eventos importantes|un grupo de estudiantes de diferentes partes del mundo se está preparando para enviar sus soluciones a un problema importante justo antes de la fecha límite|Servicios de Alojamiento del Proveedor|Tiempo de Disponibilidad,Registro de Interrupciones   
| ESC-09 | Disponibilidad    | personal de mantenimiento del centro de datos| un corte de energía inesperado afecta al centro de datos que aloja la plataforma de juez en línea|La plataforma de juez en línea debe estar diseñada para mantener la disponibilidad incluso en situaciones de interrupción, como cortes de energía, mediante medidas de redundancia y sistemas de respaldo adecuados|Durante una competencia internacional de programación en línea con equipos de todo el mundo|Infraestructura del Centro de Datos|Duración de la Interrupción,Número de Competidores Afectados   
| ESC-10 | Rendimiento    | Programadores participantes|los programadores se enfrentan a problemas altamente complejos que requieren una gran carga computacional para su evaluación|debe estar diseñada y configurada para manejar eficientemente la carga computacional requerida para evaluar soluciones complejas durante competencias, sin ralentizar drásticamente el proceso ni afectar negativamente la calidad de la experiencia de los participantes|Un equipo de programadores participa en una competencia internacional en línea |Sistema de Evaluación de Soluciones|Tiempo de Evaluación, Uso de Recursos del Servidor
| ESC-11 | Rendimiento |Competidores|envía una solución que contiene un error de programación que resulta en un bucle infinito|debe estar diseñada para detectar y manejar adecuadamente situaciones de bucle infinito en las soluciones de los usuarios, evitando así un impacto grave en el rendimiento y retrasos para otros competidores| competencia de programación|Sistema de Evaluación de Soluciones|Tiempo de Ejecución,Recursos Consumidos,Número de Soluciones con Bucle Infinito    
| ESC-12 | Rendimiento |Estudiante|envía una solución que, aunque correcta, contiene un algoritmo ineficiente que requiere mucho tiempo para su evaluación|debe ser capaz de detectar soluciones ineficientes y manejarlas adecuadamente para evitar que afecten negativamente el rendimiento y causen retrasos para otros participantes|competencia en línea de programación|Sistema de Evaluación de Soluciones|Tiempo de Evaluación,Recursos Consumidos,Número de Soluciones Ineficientes 

ESCENARIOS

| Atributo | Escenarios                                       | Requerimiento relacionado |
|----------|-------------------------------------------------|---------------------------|
| RNF01    |                                                 |                           |
| RNF02    |                                                 |                           |
| RNF03    |                                                 |                           |
| RNF04    |                                                 |                           |
| RNF05    |                                                 |                           |
| RNF06    |                                                 |                           |
| RNF07    |                                                 |                           |

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
