**Capítulo 6: Manejo de Errores y Excepciones**

**Sección 2: Cláusulas Else y Finally**

En el capítulo anterior, hemos aprendido a manejar errores y excepciones utilizando la estructura `try`/`except`. Sin embargo, hay momentos en los que queremos ejecutar código adicional después de detectar una excepción o cuando no se produce ninguna. En este sentido, entra en juego las cláusulas `else` y `finally`.

**Cláusula Else**

La cláusula `else` se utiliza para especificar qué código se va a ejecutar cuando no se produce cualquier tipo de excepción dentro del bloque `try`. Esto es útil cuando deseamos realizar una acción específica después de que el código dentro del bloque `try` se ha ejecutado correctamente.

Veamos un ejemplo:
```python
import math

def division(a, b):
    try:
        resultado = a / b
    except ZeroDivisionError:
        print("No se puede dividir entre cero")
    else:
        print(f"El resultado es {resultado}")

division(10, 2)  # Imprime "El resultado es 5.0"
division(10, 0)  # Imprime "No se puede dividir entre cero"
```
En este ejemplo, cuando se llama a la función `division` con argumentos válidos (10 y 2), el código dentro del bloque `try` se ejecuta correctamente y el resultado se imprime. Sin embargo, cuando se llama a la función con un argumento inválido (0 como segundo argumento), se produce una excepción de tipo `ZeroDivisionError` y se ejecuta el bloque `except`. La cláusula `else` no se activa en este caso porque se ha producido una excepción. Si no se hubiera producido ninguna excepción, la cláusula `else` se habría ejecutado.

**Cláusula Finally**

La cláusula `finally` se utiliza para especificar qué código se va a ejecutar siempre, sea que se produzca una excepción o no. Esto es útil cuando deseamos liberar recursos, como archivos abiertos o conexiones a bases de datos, en cualquier caso.

Veamos un ejemplo:
```python
import os

def abrir_archivo(nombre_archivo):
    try:
        archivo = open(nombre_archivo, 'r')
        print("Archivo abierto correctamente")
    except FileNotFoundError:
        print(f"El archivo {nombre_archivo} no existe")
    finally:
        if hasattr(archivo, 'close'):
            archivo.close()
            print("Archivo cerrado")

abrir_archivo('prueba.txt')  # Imprime "Archivo abierto correctamente", luego "Archivo cerrado"
```
En este ejemplo, la función `abrir_archivo` intenta abrir un archivo. Si el archivo no existe, se produce una excepción de tipo `FileNotFoundError`. La cláusula `finally` se ejecuta en cualquier caso, ya sea que se produzca una excepción o no. En este caso, cerramos el archivo utilizando el método `close()` si este existe (por ejemplo, si el archivo se abrió correctamente). Esto garantiza que el archivo se cierre siempre, sea que se produzca una excepción o no.

**Ejemplos prácticos**

Veamos algunos ejemplos prácticos de cómo utilizar las cláusulas `else` y `finally` para manejar errores y excepciones en Python:

* ** Manejo de archivos**: cuando trabajamos con archivos, es común que se produzcan errores de lectura o escritura. En este caso, podemos utilizar la cláusula `except` para manejar errores específicos, como errores de archivo no encontrado o errores de permiso. La cláusula `finally` se puede utilizar para asegurarnos de que el archivo se cierre siempre, sea que se produzca una excepción o no.
* **Conexiones a bases de datos**: cuando trabajamos con bases de datos, es común que se produzcan errores de conexión o consultas. En este caso, podemos utilizar la cláusula `except` para manejar errores específicos, como errores de conexión o errores de consulta. La cláusula `finally` se puede utilizar para asegurarnos de que la conexión se cierre siempre, sea que se produzca una excepción o no.
* **Operaciones críticas**: cuando estamos realizando operaciones críticas, como transacciones financieras o envío de correos electrónicos, es importante asegurarnos de que se produzcan los cambios en el sistema solo si todo sale bien. En este caso, podemos utilizar la cláusula `try`/`except` para manejar errores y la cláusula `finally` para asegurarnos de que se produzcan los cambios en el sistema solo si todo sale bien.

En resumen, las cláusulas `else` y `finally` son herramientas poderosas para manejar errores y excepciones en Python. La cláusula `else` se utiliza para especificar qué código se va a ejecutar cuando no se produce cualquier tipo de excepción dentro del bloque `try`, mientras que la cláusula `finally` se utiliza para especificar qué código se va a ejecutar siempre, sea que se produzca una excepción o no. Al combinar estas cláusulas con la estructura `try`/`except`, podemos crear programas más robustos y resistentes a errores.

**Ejercicio**

* Escriba un programa que lea un archivo de texto y muestre su contenido en pantalla. Utilice una cláusula `try`/`except` para manejar errores de lectura del archivo y una cláusula `finally` para asegurarse de que el archivo se cierre siempre, sea que se produzca una excepción o no.
* Escriba un programa que realice una transacción financiera (por ejemplo, depositar dinero en una cuenta bancaria). Utilice una cláusula `try`/`except` para manejar errores de conexión a la base de datos y una cláusula `finally` para asegurarse de que se produzcan los cambios en la cuenta bancaria solo si todo sale bien.
* Escriba un programa que envíe correos electrónicos a varios destinatarios. Utilice una cláusula `try`/`except` para manejar errores de conexión al servidor de correo electrónico y una cláusula `finally` para asegurarse de que se produzcan los cambios en la base de datos solo si todo sale bien.

**Conclusión**

En este capítulo, hemos profundizado en las cláusulas `else` y `finally` en el manejo de errores y excepciones en Python. Hemos visto cómo utilizar estas cláusulas para especificar qué código se va a ejecutar cuando no se produce cualquier tipo de excepción dentro del bloque `try`, o siempre, sea que se produzca una excepción o no. Al combinar estas cláusulas con la estructura `try`/`except`, podemos crear programas más robustos y resistentes a errores. En el siguiente capítulo, veremos cómo utilizar las funciones de depuración para diagnosticar y solucionar problemas en nuestros programas.