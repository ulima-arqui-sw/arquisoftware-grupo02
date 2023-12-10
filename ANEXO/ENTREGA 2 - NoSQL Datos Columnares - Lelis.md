# NoSQL - Base de Datos Columnar

## 1. Introducción

### 1.1 Definición de NoSQL
 Se refiere a un tipo de sistema de gestión de bases de datos (DBMS) que difiere significativamente de los sistemas de bases de datos relacionales tradicionales (SQL). La sigla "NoSQL" se interpreta comúnmente como "Not Only SQL," lo que indica que estos sistemas no están limitados al lenguaje de consulta estructurado (SQL) utilizado por las bases de datos relacionales. 

 - Ventajas
   - Esquema flexible
   - Escalabilidad horizontal
   - Alta disponibilidad
   - Alto rendimiento
 - Desafíos
   - Complejidad de modelado

### 1.2 ¿Cuándo se usa NoSQL?

- **Crecimiento Rápido del Volumen de Datos:**
   - Las bases de datos NoSQL son particularmente útiles cuando el volumen de datos experimenta un crecimiento significativo y rápido. Su capacidad para escalar horizontalmente facilita la gestión eficiente de grandes cantidades de datos distribuidos.

- **Necesidades de Proceso no Bien Definidas o Cambiantes:**
   - En situaciones donde las necesidades del proceso no están completamente definidas o son propensas a cambios, NoSQL ofrece flexibilidad con esquemas dinámicos. Esto permite adaptarse fácilmente a modificaciones en la estructura de datos sin la rigidez de los modelos relacionales.

- **Picos de Uso y Variabilidad en la Demanda de Usuarios:**
   - NoSQL se destaca cuando se enfrenta a picos de uso repentinos o variaciones en la demanda de usuarios. Su capacidad para escalar horizontalmente y distribuir la carga de trabajo facilita la gestión de períodos de alta actividad sin sacrificar el rendimiento.

## 2. Tipos de Bases de Datos NoSQL

- ### Documentales
  - Almacenan datos en documentos similares a JSON o BSON. Cada documento puede contener datos anidados y campos variables, ofreciendo flexibilidad para datos semiestructurados o no estructurados. Este enfoque es particularmente útil en situaciones donde la estructura de los datos puede cambiar con el tiempo.
- ### Clave-Valor
  - Almacenan información en pares clave-valor, donde cada clave es única. Esto proporciona un acceso rápido y eficiente a los datos mediante la clave. Estas bases de datos son especialmente adecuadas para operaciones de lectura y escritura simples y son conocidas por su alta velocidad y rendimiento.
- ### Basada en grafos
  - Modelan datos como nodos y las relaciones entre ellos. Este enfoque es eficaz para representar y consultar conexiones complejas entre entidades, siendo especialmente útil en escenarios donde las relaciones son fundamentales.
- ### Columnares
  - Estas bases de datos almacenan datos en columnas en lugar de filas, lo que las hace ideales para consultas analíticas y la gestión eficiente de grandes conjuntos de datos distribuidos. La escalabilidad horizontal es una de las fortalezas clave de este modelo.

## Datos columnares
- Los datos columnares se refieren a un modelo de organización de datos en el cual la información se almacena y recupera en columnas, en contraste con el modelo de filas utilizado en bases de datos relacionales tradicionales. En un sistema de almacenamiento de datos columnar, cada columna se guarda por separado, conteniendo todos los valores para esa columna específica.

  ![Datos columnares](https://blogvisionarios.com/wp-content/uploads/2015/08/image_thumb_3_1FC95E34.png)

## 3. Ejemplos DBMS NoSQL-Datos columnares
- ### HBase
  - Base de datos NoSQL distribuida y escalable, basada en el modelo de datos de Bigtable. Diseñada para manejar grandes volúmenes de datos, utiliza una arquitectura distribuida para proporcionar alta disponibilidad y escalabilidad horizontal. Es especialmente útil para aplicaciones que requieren acceso rápido y aleatorio a grandes conjuntos de datos, como análisis de datos y procesamiento en tiempo real. Integra bien con el ecosistema de Hadoop.
- ### MariaDB
  - Aunque inicialmente se basa en un modelo de base de datos relacional, ha ampliado sus capacidades para abordar necesidades más allá de las bases de datos relacionales tradicionales. A través del motor de almacenamiento ColumnStore, MariaDB proporciona funcionalidades para trabajar con datos columnares, haciendo incursiones en el espacio de las bases de datos NoSQL.
- ### Apache Cassandra
  - Sistema de gestión de bases de datos distribuido y altamente escalable, clasificado dentro de las bases de datos NoSQL. Desarrollado originalmente por Facebook y posteriormente donado a la Apache Software Foundation, Cassandra está diseñado para manejar grandes volúmenes de datos en entornos distribuidos.


## 4. Apache Cassandra en el Teorema CAP

- La relación entre el Teorema CAP y las bases de datos columnares puede observarse en cómo estas bases de datos abordan la consistencia y la disponibilidad. Dado que las bases de datos columnares a menudo se utilizan para consultas analíticas intensivas y manejo eficiente de grandes conjuntos de datos, priorizan la disponibilidad y el rendimiento en lugar de la consistencia inmediata.
  ![CAP](https://gltaboada.github.io/tgdbook/images/TeoremaCAP.jpg)

### 4.1. Características de Apache Cassandra
- Es distribuida
- Escala linealmente
- Es P2P
- Es tolerante a fallos
- Permite replicación
- Usa CQL
- Es Open source
- Consistencia ajustable
## 5. Demo
- En esta demostración, hemos optado por utilizar Docker para simplificar la configuración y ejecución del entorno de Apache Cassandra. Docker nos permite encapsular la aplicación y sus dependencias en contenedores, proporcionando así un entorno consistente y reproducible.
### 5.1. Configuración previa
- Descargar Image
  - `docker pull cassandra`
- Correr contenedor usando imagen
  - `docker run -p 7000:7000 -p 7001:7001 -p 7199:7199 -p 9042:9042 -p 9160:9160 --name cassandra -d cassandra:latest`
- Chequear si contenedor está corriendo
  - `docker ps`
- Entrar al contenedor (sustituir por tu CONTAINER ID)
  - `docker exec -it 1595491161d0 bash`
- Entrar al cqlsh (Cassandra shell)
  - `cqlsh`
### 5.2. Ejecución de Comandos CQL
- Creación de Keyspace
  - `CREATE KEYSPACE practica WITH REPLICATION = { 'class' : 'SimpleStrategy', 'replication_factor' : '1'};`
- Describir Keyspaces
  - `DESC KEYSPACES`
- Usar el Keyspace creado
  - `use practica;`
- Crear tabla
  - ` CREATE TABLE ejercicio_b (
  titulo_curso text,
  creditos_curso int,
  profesor_curso text,
  idE_estudiante int,
  nota_exam text,
  PRIMARY KEY  ( nota_exam, creditos_curso, idE_estudiante  , titulo_curso   ),
  ) WITH CLUSTERING ORDER BY(creditos_curso desc );`
- Insertar registros
  -  `insert into ejercicio_b (creditos_curso, nota_exam, idE_estudiante, titulo_curso,   profesor_curso ) values ( 7,'B',201,'Filología románica','Sara Martínez');
 insert into ejercicio_b (creditos_curso, nota_exam, idE_estudiante, titulo_curso,   profesor_curso ) values ( 7,'B',201,'Griego moderno',	'Daniel Pérez');
 insert into ejercicio_b (creditos_curso, nota_exam, idE_estudiante, titulo_curso,   profesor_curso ) values ( 3,'C',202,'Teorías literarias',	'Juan García');
 insert into ejercicio_b (creditos_curso, nota_exam, idE_estudiante, titulo_curso,   profesor_curso ) values ( 10,'A',203,'Literatura moderna',	'Amalia Sierra');
 insert into ejercicio_b (creditos_curso, nota_exam, idE_estudiante, titulo_curso,   profesor_curso ) values ( 5,'B',203,'Fonética y morfología',	'Miguel Hernández');
 insert into ejercicio_b (creditos_curso, nota_exam, idE_estudiante, titulo_curso,   profesor_curso ) values ( 10,'A',203,'Español moderno',	'Isabel Sanz');`
- Ver tabla
  - `select * from ejercicio_b`

Link video demo: https://drive.google.com/file/d/1ErH4lokSs3vR4iwVUV469_iBmLykpDcg/view?usp=sharing
