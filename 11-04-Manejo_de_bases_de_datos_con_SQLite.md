**Capítulo 7: Temas Avanzados - Manejo de bases de datos con SQLite**

La gestión de bases de datos es un aspecto fundamental en la programación, ya que permite almacenar y recuperar información de manera efectiva y eficiente. En este capítulo, vamos a profundizar en el manejo de bases de datos con SQLite, una herramienta popular y fácil de usar para desarrolladores.

**¿Qué es SQLite?**

SQLite es una base de datos relacional completamente en código abierto que se almacena en un solo archivo. Es compatible con la mayoría de los lenguajes de programación, incluyendo Python. Aunque no es tan potente como otras bases de datos relacionales como MySQL o PostgreSQL, SQLite es muy fácil de usar y se presta a ser utilizada en aplicaciones pequeñas y medianas.

**Instalación de SQLite**

Para empezar a trabajar con SQLite en Python, debemos instalar la biblioteca sqlite3. En los sistemas operativos Unix-like (como Linux o macOS), podemos hacerlo mediante el comando:

```
pip install pysqlite3
```

En Windows, podemos instalarla mediante el instalador de pip.

**Creación de una base de datos**

Para crear una base de datos en SQLite, podemos utilizar la función `connect()` de la biblioteca sqlite3. Esta función devuelve un objeto que representa la conexión a la base de datos:

```python
import sqlite3

conexion = sqlite3.connect("mi_base_de_datos.db")
cursor = conexion.cursor()
```

En este ejemplo, estamos creando una base de datos llamada "mi_base_de_datos.db" y estableciendo un cursor (un objeto que nos permite ejecutar consultas SQL) para interactuar con la base de datos.

**Creación de tablas**

Una vez conectados a la base de datos, podemos crear tablas utilizando el método `execute()` del cursor:

```python
cursor.execute("""
    CREATE TABLE personas (
        id INTEGER PRIMARY KEY,
        nombre TEXT NOT NULL,
        apellido TEXT NOT NULL,
        edad INTEGER NOT NULL
    );
""")
```

En este ejemplo, estamos creando una tabla llamada "personas" con cuatro columnas: "id", "nombre", "apellido" y "edad". La columna "id" es la clave principal de la tabla.

**Inserción de datos**

Para insertar datos en la base de datos, podemos utilizar el método `execute()` del cursor:

```python
cursor.execute("""
    INSERT INTO personas (nombre, apellido, edad)
    VALUES ('Juan', 'Pérez', 30);
""")
```

En este ejemplo, estamos insertando un registro en la tabla "personas" con los valores "Juan", "Pérez" y 30 para las columnas "nombre", "apellido" y "edad", respectivamente.

**Recuperación de datos**

Para recuperar datos de la base de datos, podemos utilizar el método `fetchall()` del cursor:

```python
cursor.execute("SELECT * FROM personas;")
personas = cursor.fetchall()
print(personas)
```

En este ejemplo, estamos seleccionando todos los registros de la tabla "personas" y almacenándolos en una variable llamada "personas". Luego, estamos imprimiendo los valores de cada registro.

**Actualización de datos**

Para actualizar datos en la base de datos, podemos utilizar el método `execute()` del cursor:

```python
cursor.execute("""
    UPDATE personas
    SET nombre = 'Maria'
    WHERE id = 1;
""")
```

En este ejemplo, estamos actualizando el valor de la columna "nombre" para el registro con id=1 en la tabla "personas" a "Maria".

**Eliminación de datos**

Para eliminar datos de la base de datos, podemos utilizar el método `execute()` del cursor:

```python
cursor.execute("DELETE FROM personas WHERE id = 1;")
```

En este ejemplo, estamos eliminando el registro con id=1 en la tabla "personas".

**Conclusión**

En este capítulo, hemos aprendido a crear una base de datos con SQLite en Python y a realizar operaciones básicas como insertar, recuperar, actualizar y eliminar registros. SQLite es una herramienta muy útil para desarrolladores, ya que permite trabajar con bases de datos sin necesidad de instalar un servidor de base de datos aparte.

**Ejercicios**

1. Cree una base de datos llamada "mi_base_de_datos.db" y cree una tabla llamada "libros" con las columnas "id", "titulo", "autor" y "fecha_publicación".
2. Inserte varios registros en la tabla "libros".
3. Recupere todos los registros de la tabla "libros" y muestre los resultados.
4. Actualice el título de un libro existente en la tabla "libros".
5. Elimine un registro de la tabla "libros".

**Resolución de ejercicios**

Puedes encontrar la respuesta a cada ejercicio en el apéndice de este capítulo.

**Apéndice**

### Ejercicio 1: Creación de base de datos y tabla

```python
import sqlite3

conexion = sqlite3.connect("mi_base_de_datos.db")
cursor = conexion.cursor()

cursor.execute("""
    CREATE TABLE libros (
        id INTEGER PRIMARY KEY,
        titulo TEXT NOT NULL,
        autor TEXT NOT NULL,
        fecha_publicacion DATE NOT NULL
    );
""")
```

### Ejercicio 2: Insertar registros en la tabla "libros"

```python
cursor.execute("""
    INSERT INTO libros (titulo, autor, fecha_publicacion)
    VALUES ('El Aleph', 'Jorge Luis Borges', '1949-03-31');
""")

cursor.execute("""
    INSERT INTO libros (titulo, autor, fecha_publicacion)
    VALUES ('1984', 'George Orwell', '1949-06-08');
""")

cursor.execute("""
    INSERT INTO libros (titulo, autor, fecha_publicación)
    VALUES ('La Sombra del Viento', 'Carlos Ruiz Zafón', '2001-05-28');
""")
```

### Ejercicio 3: Recuperar todos los registros de la tabla "libros"

```python
cursor.execute("SELECT * FROM libros;")
libros = cursor.fetchall()
print(libros)
```

### Ejercicio 4: Actualizar el título de un libro existente en la tabla "libros"

```python
cursor.execute("""
    UPDATE libros
    SET titulo = 'El Aleph - Edición Especial'
    WHERE id = 1;
""")
```

### Ejercicio 5: Eliminar un registro de la tabla "libros"

```python
cursor.execute("DELETE FROM libros WHERE id = 2;")
```

Espero que este capítulo te haya ayudado a entender mejor el manejo de bases de datos con SQLite en Python. En el próximo capítulo, exploraremos temas más avanzados como la concurrencia y la programación asíncrona.