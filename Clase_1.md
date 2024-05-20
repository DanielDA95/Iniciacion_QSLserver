# Que es una base de datos?
- Para que sirve?
***
- Organizacion de los datos dentro de la base de datos, tablas... Tener una base de datos con la minima cantidad de datos repetidos y hacer los datos lo mas dividido posible. 
- Estructura de tablas. Filas y columnas 
**CursoQSL => cntr = Curso**
- Bases de datos relacionales.???? Conjuntos de una o mas tablas, estructuradas en registros.
  ***
- Almacenamiento de las bases de datos de sql server se guardan en dos archivos. Ej. archivo 1.MDF (Archivo principal)-- Archvivo_2.LDF (Registro de transacciones). Podria existir otro tipo de extension que es NDF, y son los archivos secundarios.
- Archivos de copia de seguridad, con nombre de extension .BAK
  
- SISTEMA GESTOR DE BASES DE DATOS (SGBD), Gestionar grandes cantidades de infoformacion.
***
- Metodos para ingresar a las bases de datos, Inicios de sesion son de dos formas, windows o QSL. Modo mixto
- Inicio de sesion con SQL se llama S A. SA = Inicio como administrador del servidor. Para ingresar a las bases de datos se deben asignar usuarios y contraseñas a cada base de datos.

- Lenguaje de programacion para la creacion de las basess de datos es el **TRANSACT-SQL ó (T-SQL).**

***
Cuando se escribe codigo, cuando se selecciona una VARIABLE, las que tienen doble @ son variables globales del sistema. 
comentarios en los codigos se realizan con 2 guiones (--) de una sola linea. 
Para comentarios de varias lineas se tiene que poner /* */
Las funciones siempre llevan parentesis.  *Ejemplo:* `SELECT USER_NAME()`

***Bases de datos del sistema.***
La base de datos master, es la base de datos principal en SQL_Server. 
Base de datos Msdb, almacena las tareas correspondientes a las tareas programadas o trabajos y pueden ser de cualquier tipo, por ejemplo una copia de seguridad programada. 
Base de datos TempDB, Se crea cuando se reinicia el servidor.
Base de datos model, es la que utilizamos como plantilla cuando creamos bases de datos nuevas.

***
Que es un DBO (dbo)
Hay uno dbo que es el usuario administrador de la base de datos - 
y esta el esquema (schema) dbo que no tiene nada que ver con lo de arriba. 

