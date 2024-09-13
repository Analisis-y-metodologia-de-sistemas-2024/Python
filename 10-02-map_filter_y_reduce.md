**Capítulo 9: Programación Funcional en Python - Map, Filter y Reduce**

En el capítulo anterior, exploramos las funciones de orden superior en Python, destacando su capacidad para manipular colecciones de datos de manera efectiva. En este capítulo, vamos a profundizar en tres de las funciones más poderosas de Python: `map`, `filter` y `reduce`. Estas funciones son fundamentales en la programación funcional y nos permiten realizar operaciones complejas sobre nuestras colecciones de datos.

**Map**

La función `map` es una de las funciones más versátiles de Python. Recibe dos parámetros: una función y un iterable (como una lista, tupla o cadena). La función se aplica a cada elemento del iterable y devuelve un nuevo iterable con los resultados.

Por ejemplo, supongamos que tenemos una lista de números y queremos multiplicar cada número por 2:
```python
numbers = [1, 2, 3, 4, 5]
double_numbers = list(map(lambda x: x * 2, numbers))
print(double_numbers)  # [2, 4, 6, 8, 10]
```
En este ejemplo, la función `lambda` se aplica a cada elemento de la lista `numbers`, multiplicando cada número por 2. El resultado es un nuevo iterable que contiene los números doblados.

La función `map` también puede ser utilizada con funciones más complejas. Por ejemplo, supongamos que queremos convertir una lista de cadenas en mayúsculas:
```python
strings = ['hello', 'world', 'python']
uppercase_strings = list(map(str.upper, strings))
print(uppercase_strings)  # ['HELLO', 'WORLD', 'PYTHON']
```
En este ejemplo, la función `str.upper` se aplica a cada cadena de la lista y devuelve un nuevo iterable con las cadenas en mayúsculas.

**Filter**

La función `filter` es similar a `map`, pero en lugar de aplicar una función a cada elemento del iterable, filtra los elementos que cumplen con cierta condición. La función recibe dos parámetros: una función y un iterable.

Por ejemplo, supongamos que tenemos una lista de números y queremos obtener solo los números pares:
```python
numbers = [1, 2, 3, 4, 5]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)  # [2, 4]
```
En este ejemplo, la función `lambda` se aplica a cada elemento de la lista y devuelve `True` si el número es par. La función `filter` devuelve un nuevo iterable que contiene solo los números pares.

La función `filter` también puede ser utilizada con funciones más complejas. Por ejemplo, supongamos que queremos obtener solo las cadenas de una lista que contienen la palabra "python":
```python
strings = ['hello', 'world', 'python is awesome', 'learning python']
python_strings = list(filter(lambda s: 'python' in s.lower(), strings))
print(python_strings)  # ['python is awesome', 'learning python']
```
En este ejemplo, la función `lambda` se aplica a cada cadena de la lista y devuelve `True` si contiene la palabra "python" (ignorando mayúsculas). La función `filter` devuelve un nuevo iterable que contiene solo las cadenas que contienen la palabra "python".

**Reduce**

La función `reduce` es una de las funciones más poderosas de Python. Recibe tres parámetros: una función, un iterable y un valor inicial (opcional). La función se aplica a cada elemento del iterable y al resultado anterior, devolviendo el resultado final.

Por ejemplo, supongamos que queremos sumar todos los números de una lista:
```python
numbers = [1, 2, 3, 4, 5]
sum_numbers = reduce(lambda x, y: x + y, numbers)
print(sum_numbers)  # 15
```
En este ejemplo, la función `lambda` se aplica a cada elemento de la lista y al resultado anterior, sumando todos los números.

La función `reduce` también puede ser utilizada con funciones más complejas. Por ejemplo, supongamos que queremos concatenar todas las cadenas de una lista:
```python
strings = ['hello', 'world', 'python']
concatenated_strings = reduce(lambda x, y: x + y, strings)
print(concatenated_strings)  # 'helloworldpython'
```
En este ejemplo, la función `lambda` se aplica a cada cadena de la lista y al resultado anterior, concatenando todas las cadenas.

**Conclusión**

En este capítulo, hemos explorado las funciones `map`, `filter` y `reduce` en Python. Estas funciones son fundamentales en la programación funcional y nos permiten realizar operaciones complejas sobre nuestras colecciones de datos. A través de ejemplos prácticos, hemos visto cómo estas funciones pueden ser utilizadas para manipular datos de manera efectiva.

En el próximo capítulo, vamos a profundizar en otros temas de programación funcional en Python, como lambda functions y closures.