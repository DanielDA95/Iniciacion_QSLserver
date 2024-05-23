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
***
- Lenguaje de programacion para la creacion de las basess de datos es el **TRANSACT-SQL ó (T-SQL).**
  ## Codigos para usar
  *Sentencias*
  1. SELECT (lista de seleccion):
* `SELECT @@VERSION` --Version del servidor. 
* `select @@SERVERNAME` --nombre del servidor
* `select SUSER_NAME()` --Inicio de sesion Esto es una FUNCION DE SQL. 
* `select USER_NAME()`--Usuario en la base de datos.
* `select * from sys.sysdatabases` --Busqueda de bases de datos en el sistema.
* 
  2. From (table source):
  
  3. WHERE
  4. GROUP BY
  5. ORDER BY

     
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
y esta el esquema (schema) dbo que no tiene nada que ver con lo de arriba. Lo podemos usar en la busqueda de archivos dentro del SSMS



## Clausulas.

- where: siempre va antes de group byb
- group by

- having: va despues de group by

- https://learn.microsoft.com/es-es/sql/t-sql/functions/datepart-transact-sql?view=sql-server-ver16

***
## Requisitos para relacionar tablas. 

+ Todas las tablas deben tener algun dato en común para poder relacionarse entre si. O tener una base intermedia donde se tenegan datos de alguna de las otras tablas. 
+ Una de las tablas que intervienen en la relacion deben terner valores unicos y debe estar siempre rellena y no puede tener valores nulos NULL
+ para que QSL sepa que tiene una columna con valores unicos debe estar definda como PRIMARY KEY o clave principal y no admite nulos
+ En cada tabla solamente puede haber UNA clave principal, pero no tiene porque estar formada por 1 sola columna, puede tener varias columnas.

**Diagrama de base de datos**


## Crear base de datos.
Para crear la base de datos se necesita por lo menos el nombre, que va a terner la base de datos. 

`CREATE DATABASE ......(Nombre de la BD que queremos)

**Para modificar una ya creada**

` Alter DATABASE ..... ` //Nombre de base de datos
` MODIFY FILE ( NAME = 'ACADEMIA', ` -- Nombre de archivo
               ` SIZE = 13, `               
             `   FILEGROWTH = 25) `

**Para crear una vista** Seria tipo de una consulta que se hace en una tabla, o BD. Y sirve como un atajo para ver una consulta que necesitariamos ver más frecuentemente

`Create view Clientes_Trapagaran`

`AS`

`SELECT ...`

`FROM ...`

`WHERE ....`

**Para modificar una vista**
`Alter view Clientes_Trapagaran`

`AS`

`SELECT ....`

`FROM .....`

`WHERE ....`
