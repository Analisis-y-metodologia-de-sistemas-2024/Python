**Capítulo 6: Control de Flujo**

**Sección 1.2: Bucles For**

En el capítulo anterior, hemos explorado las declaraciones `if`, `elif` y `else`, que nos permiten tomar decisiones dentro de un programa. En este sentido, los bucles son una herramienta fundamental para repetir ciertas acciones dentro de nuestro código.

**Introducción a los Bucles For**

Un bucle `for` es una estructura de control de flujo que permite iterar sobre una secuencia de valores, como una lista, un tupla o un conjunto. Esto se logra mediante la utilización de una variable que toma el valor de cada elemento en la secuencia y se repite para procesarlo.

En Python, los bucles `for` se escriben de manera similar a otros lenguajes de programación. La sintaxis básica es la siguiente:
```python
for variable in iterable:
    # Código a ejecutar
```
Donde `variable` es el nombre que asignamos a la variable que va a tomar el valor de cada elemento en la secuencia, y `iterable` es la secuencia misma.

**Ejemplo Básico**

Supongamos que queremos imprimir los números del 1 al 5:
```python
for i in range(1, 6):
    print(i)
```
Al ejecutar este código, se imprime cada número desde el 1 hasta el 5. La variable `i` toma el valor de cada elemento en la secuencia y se repite para imprimirlo.

**Iterar sobre una Lista**

Una de las formas más comunes de utilizar los bucles `for` es iterar sobre una lista. Por ejemplo, supongamos que tenemos una lista de nombres:
```python
nombres = ["Juan", "María", "Pepe", "Luis"]
```
Podemos iterar sobre esta lista para imprimir cada nombre utilizando el siguiente código:
```python
for nombre in nombres:
    print(nombre)
```
Al ejecutar este código, se imprime cada nombre en la lista.

**Iterar sobre un Rango**

Otra forma común de utilizar los bucles `for` es iterar sobre un rango de números. Por ejemplo, supongamos que queremos imprimir los números pares desde el 2 hasta el 10:
```python
for i in range(2, 11, 2):
    print(i)
```
En este caso, la función `range()` devuelve una secuencia de números que comienza en el 2, termina en el 10 y aumenta en 2 cada vez. La variable `i` toma el valor de cada elemento en esta secuencia y se repite para imprimirlo.

**Iterar sobre un Diccionario**

Los bucles `for` también podemos utilizarlos para iterar sobre los elementos de un diccionario. Por ejemplo, supongamos que tenemos un diccionario que contiene nombres y edades:
```python
personas = {"Juan": 25, "María": 30, "Pepe": 35}
```
Podemos iterar sobre este diccionario para imprimir cada nombre y edad utilizando el siguiente código:
```python
for nombre, edad in personas.items():
    print(f"{nombre} tiene {edad} años")
```
Al ejecutar este código, se imprime cada nombre y edad en el diccionario.

**Iterar sobre un Conjunto**

Los bucles `for` también podemos utilizarlos para iterar sobre los elementos de un conjunto. Por ejemplo, supongamos que tenemos un conjunto de números:
```python
numeros = {1, 2, 3, 4, 5}
```
Podemos iterar sobre este conjunto para imprimir cada número utilizando el siguiente código:
```python
for numero in numeros:
    print(numero)
```
Al ejecutar este código, se imprime cada número en el conjunto.

**Ejercicios**

1. Escriba un bucle `for` que itere sobre una lista de colores y imprima cada color.
2. Escriba un bucle `for` que itere sobre un rango de números del 10 al 20 y sume los valores impares.
3. Escriba un bucle `for` que itere sobre un diccionario que contiene nombres y edades, y imprima cada nombre y edad.

**Conclusión**

En este capítulo, hemos explorado en profundidad los bucles `for` en Python. Vimos cómo se pueden utilizar para iterar sobre secuencias de valores, como listas, tuplas o conjuntos, y cómo se pueden aplicar a diferentes tipos de datos. Esperamos que hayas aprendido a utilizar los bucles `for` con confianza y estés listo para seguir adelante en tu aventura de programación en Python.

**Siguiente Capítulo**

En el próximo capítulo, exploraremos los bucles `while`, que nos permiten iterar sobre un condicional hasta que se cumpla una cierta condición. ¡Vamos a profundizar más en el control de flujo y aprender a crear programas más complejos!