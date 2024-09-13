**Capítulo 6: Módulo functools**

El módulo `functools` es una parte fundamental del lenguaje Python que nos permite trabajar con funciones de manera más eficiente y flexible. En este capítulo, exploraremos en profundidad los aspectos más importantes del módulo `functools`, destacando sus características y aplicaciones prácticas.

**Introducción**

El módulo `functools` fue introducido en Python 2.5 como una herramienta para trabajar con funciones de manera más eficiente. Inicialmente, se enfocó en proporcionar funcionalidades para el manejo de funciones anónimas y closures, pero con el tiempo, su función ha evolucionado para abarcar un rango más amplio de funcionalidades.

**Funciones curry**

Una de las características más interesantes del módulo `functools` es la capacidad de crear funciones curry. Una función curry es una función que toma varios argumentos y devuelve otra función que toma los restantes argumentos. Esto nos permite crear funciones con comportamientos más flexibles y personalizables.

Por ejemplo, podemos utilizar la función `partial` para crear una función curry:
```python
from functools import partial

def suma(a, b):
    return a + b

suma_dos = partial(suma, 2)
print(suma_dos(3))  # Output: 5
```
En este ejemplo, creamos una función `suma` que toma dos argumentos y devuelve la suma de ellos. Luego, utilizamos la función `partial` para crear una nueva función `suma_dos` que tiene el primer argumento fijo en 2. Finalmente, llamamos a `suma_dos` con el segundo argumento 3 y obtenemos el resultado 5.

**Funciones reduce**

Otra característica importante del módulo `functools` es la capacidad de crear funciones reducir. Una función reducir toma una lista o iterable y devuelve un valor único que resulta de aplicar una función a cada elemento de la lista.

Por ejemplo, podemos utilizar la función `reduce` para calcular la suma de los elementos de una lista:
```python
from functools import reduce

def suma(a, b):
    return a + b

numeros = [1, 2, 3, 4, 5]
resultado = reduce(suma, numeros)
print(resultado)  # Output: 15
```
En este ejemplo, creamos una función `suma` que toma dos argumentos y devuelve la suma de ellos. Luego, utilizamos la función `reduce` para aplicar esta función a cada elemento de la lista `numeros`. Finalmente, obtenemos el resultado 15 que es la suma de todos los elementos de la lista.

**Funciones lru_cache**

Una característica interesante del módulo `functools` es la capacidad de crear funciones con caché. Una función con caché almacena en memoria los resultados de las llamadas anteriores para evitar re-ejecutarlas en el futuro.

Por ejemplo, podemos utilizar la función `lru_cache` para crear una función que calcula la factorial de un número:
```python
from functools import lru_cache

@lru_cache(maxsize=128)
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n-1)

print(factorial(5))  # Output: 120
```
En este ejemplo, creamos una función `factorial` que calcula la factorial de un número. Luego, utilizamos la función `lru_cache` para crear una versión cachée de esta función. La función `lru_cache` almacena en memoria los resultados de las llamadas anteriores para evitar re-ejecutarlas en el futuro.

**Funciones wraps**

Otra característica importante del módulo `functools` es la capacidad de crear funciones wrappers. Una función wrapper es una función que envuelve otra función y puede realizar operaciones adicionales antes o después de llamar a la función original.

Por ejemplo, podemos utilizar la función `wraps` para crear una función wrapper que registra el tiempo de ejecución de una función:
```python
from functools import wraps

def timer(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        print(f"Tiempo de ejecución: {end_time - start_time} segundos")
        return result
    return wrapper

@timer
def suma(a, b):
    return a + b

print(suma(2, 3))  # Output: 5
```
En este ejemplo, creamos una función `suma` que toma dos argumentos y devuelve la suma de ellos. Luego, utilizamos la función `wraps` para crear una función wrapper `timer` que registra el tiempo de ejecución de la función original. Finalmente, llamamos a la función `suma` con los argumentos 2 y 3 y obtenemos el resultado 5.

**Conclusión**

En este capítulo, hemos explorado los aspectos más importantes del módulo `functools` de Python. Hemos visto cómo crear funciones curry, reducir, cachear y wrapper con esta biblioteca. Estas características nos permiten trabajar con funciones de manera más eficiente y flexible, lo que es fundamental para la programación funcional en Python.

**Ejercicios**

1. Crea una función curry que tome dos argumentos y devuelva la suma de ellos.
2. Utiliza la función `reduce` para calcular la multiplicación de los elementos de una lista.
3. Crea una función cachée que calcule la factorial de un número.
4. Utiliza la función `wraps` para crear una función wrapper que registra el tiempo de ejecución de una función.

**Soluciones**

1. ```python
    from functools import partial

    def suma(a, b):
        return a + b

    suma_dos = partial(suma, 2)
    print(suma_dos(3))  # Output: 5
   ```
2. ```python
    from functools import reduce

    def multiplicar(a, b):
        return a * b

    numeros = [1, 2, 3, 4, 5]
    resultado = reduce(multiplicar, numeros)
    print(resultado)  # Output: 120
   ```
3. ```python
    from functools import lru_cache

    @lru_cache(maxsize=128)
    def factorial(n):
        if n == 0 or n == 1:
            return 1
        else:
            return n * factorial(n-1)

    print(factorial(5))  # Output: 120
   ```
4. ```python
    from functools import wraps

    def timer(func):
        @wraps(func)
        def wrapper(*args, **kwargs):
            start_time = time.time()
            result = func(*args, **kwargs)
            end_time = time.time()
            print(f"Tiempo de ejecución: {end_time - start_time} segundos")
            return result
        return wrapper

    @timer
    def suma(a, b):
        return a + b

    print(suma(2, 3))  # Output: 5
   ```

Esperamos que esta sección te haya sido útil para entender mejor el módulo `functools` y cómo utilizar sus características para crear funciones más eficientes y flexibles. ¡Buen provecho!