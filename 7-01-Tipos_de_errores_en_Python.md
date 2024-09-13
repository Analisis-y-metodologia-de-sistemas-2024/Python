**Capítulo 6: Manejo de Errores y Excepciones**

**Sección 6.1: Tipos de Errores en Python**

En la programación, es común que surjan errores durante el desarrollo o la ejecución del código. En Python, hay diferentes tipos de errores que pueden ocurrir, cada uno con su propio conjunto de características y comportamientos.

**6.1.1: Errores de Sintaxis**

Los errores de sintaxis ocurren cuando el intérprete de Python encuentra un error en la estructura o formato del código. Esto puede incluir palabras reservadas mal utilizadas, falta de paréntesis, o caracteres no válidos.

Ejemplo:
```
if 5 > 3 print("El 5 es mayor que el 3")
```
Este código producirá un error de sintaxis porque falta la palabra clave `:` después del condicional.

**6.1.2: Errores de Semántica**

Los errores semánticos ocurren cuando el intérprete de Python puede analizar correctamente la estructura del código, pero no puede ejecutarlo debido a un problema lógico o significativo. Esto puede incluir variables no declaradas, operaciones que no pueden ser realizadas con los tipos de datos correctos, o intentar acceder a un objeto que no existe.

Ejemplo:
```
x = 5
y = "hola"
print(x + y)
```
Este código producirá un error semántico porque se está tratando de sumar un número (`x`) con una cadena de texto (`y`).

**6.1.3: Errores de Runtime**

Los errores de runtime ocurren cuando el intérprete de Python ha analizado correctamente la estructura del código y puede ejecutarlo, pero surge un error durante la ejecución. Esto puede incluir divisiones por cero, intentar acceder a un índice que no existe en una lista, o lanzar una excepción que no está siendo manejada.

Ejemplo:
```
x = 5
print(x / 0)
```
Este código producirá un error de runtime porque se está tratando de dividir por cero.

**6.1.4: Errores de Tipo**

Los errores de tipo ocurren cuando el intérprete de Python no puede convertir un valor a un tipo de datos esperado. Esto puede incluir intentar sumar un número con una cadena de texto, o intentar acceder a un atributo de un objeto que no existe.

Ejemplo:
```
x = 5
print(x + "hola")
```
Este código producirá un error de tipo porque se está tratando de sumar un número (`x`) con una cadena de texto (`"hola"`).

**6.1.5: Errores de Lógica**

Los errores lógicos ocurren cuando el intérprete de Python puede ejecutar el código correctamente, pero el resultado no es lo que se esperaba. Esto puede incluir bucles infinitos, condicionales que no funcionan como se espera, o variables que no están siendo inicializadas correctamente.

Ejemplo:
```
x = 0
while x < 5:
    print(x)
    x += 1
print("Finalizado")
```
Este código producirá un error lógico porque el bucle `while` se ejecutará infinitamente porque la variable `x` nunca llega a ser mayor que 5.

En resumen, los errores en Python pueden ocurrir por una variedad de razones, desde errores de sintaxis hasta errores lógicos. Es importante entender cada tipo de error y cómo manejarlos para crear software confiable y escalable.

**Sección 6.2: Manejo de Errores en Python**

A continuación, veremos cómo manejar los errores en Python utilizando bloques `try`-`except`. Los bloques `try`-`except` permiten que el código sea ejecutado dentro del bloque `try`, y si se produce un error, el intérprete de Python saltará al bloque `except` correspondiente y ejecutará el código contenido en él.

Ejemplo:
```
try:
    x = 5 / 0
except ZeroDivisionError:
    print("No se puede dividir por cero")
```
En este ejemplo, el intérprete de Python intenta ejecutar la instrucción `x = 5 / 0`, pero produce un error de runtime porque se está tratando de dividir por cero. El intérprete de Python saltará al bloque `except` y ejecutará la instrucción `print("No se puede dividir por cero")`.

**Sección 6.3: Creación de Excepciones Personalizadas**

Además de manejar errores utilizando bloques `try`-`except`, también podemos crear nuestras propias excepciones personalizadas para proporcionar información adicional sobre el error que ha ocurrido.

Ejemplo:
```
class MiExcepcion(Exception):
    pass

try:
    raise MiExcepcion("Ha ocurrido un error")
except MiExcepcion as e:
    print(e)
```
En este ejemplo, creamos una clase `MiExcepcion` que hereda de la clase base `Exception`. Luego, dentro del bloque `try`, lanzamos una instancia de nuestra excepción personalizada utilizando el método `raise`. Finalmente, en el bloque `except`, capturamos la excepción y ejecutamos la instrucción `print(e)`, que imprime el mensaje de error que se proporcionó al lanzar la excepción.

En resumen, en este capítulo hemos explorado los diferentes tipos de errores en Python, incluyendo errores de sintaxis, semántica, runtime, tipo y lógica. También hemos visto cómo manejar errores utilizando bloques `try`-`except`, y cómo crear nuestras propias excepciones personalizadas para proporcionar información adicional sobre el error que ha ocurrido.

**Sección 6.4: Conclusión**

En este capítulo, hemos cubierto los fundamentos del manejo de errores en Python. Hemos visto cómo los errores pueden ocurrir en diferentes formas y cómo podemos manejarlos utilizando bloques `try`-`except`. También hemos explorado la creación de excepciones personalizadas para proporcionar información adicional sobre el error que ha ocurrido.

En el próximo capítulo, exploraremos temas avanzados como la programación orientada a objetos y la manipulación de archivos en Python.