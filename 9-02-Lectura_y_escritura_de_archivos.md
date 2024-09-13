**Lectura y Escritura de Archivos**

En el capítulo anterior, hemos abordado la entrada y salida estándar en Python, donde aprendimos a utilizar los métodos `input()` y `print()` para interactuar con el usuario y mostrar información en la pantalla. Sin embargo, hay situaciones en las que necesitamos acceder a archivos de texto o otros formatos de datos almacenados en un dispositivo de almacenamiento externo. En este sentido, es fundamental entender cómo leer y escribir archivos en Python.

**Tipos de Archivos**

Antes de empezar a hablar sobre la lectura y escritura de archivos, es importante distinguir entre los diferentes tipos de archivos que podemos encontrar:

* **Archivos de texto**: Son archivos que contienen información almacenada en formato de texto. Estos archivos pueden ser editados con cualquier editor de texto y pueden ser leídos y escritos utilizando métodos específicos.
* **Archivos binarios**: Son archivos que contienen datos en un formato no legible para el hombre, como imágenes, audio o video. Estos archivos requieren métodos especializados para leer y escribir.

**Lectura de Archivos**

Para leer un archivo en Python, utilizamos la función `open()` del módulo `built-in` que proporciona acceso a los archivos del sistema de archivos. La sintaxis general para abrir un archivo es la siguiente:

```python
archivo = open('ruta/al/archivo.txt', 'modo')
```

Donde `'ruta/al/archivo.txt'` es el nombre y ruta del archivo que deseamos leer, y `'modo'` es el modo en que deseamos abrir el archivo. Los modos más comunes son:

* **'r'**: Lectura (modo predeterminado)
* **'w'**: Escritura (sobreescribe el contenido del archivo si ya existe)
* **'a'**: Anexión (agrega contenido al final del archivo)

Una vez que tenemos el archivo abierto, podemos leer su contenido utilizando métodos como `read()`, `readline()` o `readlines()`.

* **`read(size=-1)`**: Lee el contenido del archivo hasta un tamaño determinado (`size`) o hasta el final del archivo (si `size` es -1).
* **`readline(size=-1)`**: Lee una línea completa del archivo. Si no se especifica un tamaño, lee la línea completa.
* **`readlines()`**: Lee todas las líneas del archivo y devuelve una lista de strings.

Por ejemplo, para leer el contenido completo de un archivo llamado `archivo.txt`, podemos utilizar el método `read()`:

```python
archivo = open('archivo.txt', 'r')
contenido = archivo.read()
print(contenido)
archivo.close()
```

O, si queremos leer las líneas del archivo de manera individual, podemos utilizar el método `readlines()`:

```python
archivo = open('archivo.txt', 'r')
líneas = archivo.readlines()
for línea in líneas:
    print(línea.strip())
archivo.close()
```

**Escritura de Archivos**

Para escribir en un archivo en Python, también utilizamos la función `open()` del módulo `built-in`. La sintaxis general para abrir un archivo en modo de escritura es la siguiente:

```python
archivo = open('ruta/al/archivo.txt', 'w')
```

Una vez que tenemos el archivo abierto, podemos escribir contenido utilizando métodos como `write()` o `writelines()`.

* **`write(string)`**: Escribe un string en el archivo.
* **`writelines(seqs)`**: Escribe una lista de strings en el archivo, separados por nuevos saltos de línea.

Por ejemplo, para escribir un mensaje en un archivo llamado `mensaje.txt`, podemos utilizar el método `write()`:

```python
archivo = open('mensaje.txt', 'w')
mensaje = 'Hola mundo!'
archivo.write(mensaje)
archivo.close()
```

O, si queremos escribir varias líneas de texto en el archivo, podemos utilizar el método `writelines()`:

```python
archivo = open('mensaje.txt', 'w')
líneas = ['Esto es un mensaje', 'Escribo varias líneas']
archivo.writelines(líneas)
archivo.close()
```

**Anexión de Archivos**

Para anexar contenido a un archivo en Python, podemos utilizar el modo `'a'` cuando abrimos el archivo:

```python
archivo = open('archivo.txt', 'a')
mensaje = 'Esta es una nueva línea'
archivo.write(mensaje)
archivo.close()
```

**Cierre de Archivos**

Es importante cerrar los archivos después de utilizarlos para evitar problemas de acceso concurrente y asegurar la integridad del contenido. En Python, podemos cerrar un archivo utilizando el método `close()`:

```python
archivo = open('archivo.txt', 'r')
contenido = archivo.read()
print(contenido)
archivo.close()  # Cerramos el archivo después de leer su contenido
```

**Error Handling**

Al trabajar con archivos, es importante manejar errores y excepciones para evitar problemas y garantizar la estabilidad del programa. En Python, podemos utilizar bloques `try`-`except` para capturar y manejar errores:

```python
try:
    archivo = open('archivo.txt', 'r')
    contenido = archivo.read()
    print(contenido)
except FileNotFoundError:
    print('El archivo no existe')
except IOError:
    print('Error al leer el archivo')
finally:
    if 'archivo' in locals():
        archivo.close()  # Cerramos el archivo si se abrió correctamente
```

En conclusión, la lectura y escritura de archivos es una habilidad fundamental en programación y Python ofrece varias formas de hacerlo. Al entender cómo abrir, leer y escribir archivos en modo de texto o binario, podemos crear programas más poderosos y escalables que interactúan con el sistema de archivos del sistema operativo.