**Listas y Tuplas**

En el capítulo anterior, hemos abordado los conceptos fundamentales de variables y asignación en Python. En este capítulo, nos enfocaremos en uno de los tipos de datos más versátiles y útiles que ofrece Python: las listas y tuplas.

**Definición y Creación**

Una lista es un tipo de dato que puede contener cero o más elementos, cada uno de ellos identificado por un índice numérico. Las listas se crean utilizando la función `list()` o encerrando los elementos entre corchetes `[]`. Por ejemplo:
```python
mi_lista = [1, 2, 3, 4, 5]
otra_lista = list("hola mundo")
```
Una tupla, por otro lado, es similar a una lista pero con una diferencia fundamental: las tuplas son inmutables, lo que significa que no se pueden modificar después de su creación. Las tuples se crean utilizando la función `tuple()` o encerrando los elementos entre paréntesis `()`. Por ejemplo:
```python
mi_tupla = (1, 2, 3, 4, 5)
otra_tupla = tuple("hola mundo")
```
**Acceso y Modificación**

Para acceder a un elemento de una lista o tupla, se utiliza el índice numérico correspondiente. Por ejemplo:
```python
mi_lista[0]  # Accede al primer elemento de la lista
mi_tupla[1]  # Accede al segundo elemento de la tupla
```
Para modificar un elemento de una lista, se utiliza el índice numérico y el operador de asignación `=`. Por ejemplo:
```python
mi_lista[0] = 10  # Modifica el primer elemento de la lista
```
Sin embargo, no se puede modificar un elemento de una tupla ya que es inmutable.

**Longitud y Rango**

La longitud de una lista o tupla se puede determinar utilizando la función `len()`. Por ejemplo:
```python
print(len(mi_lista))  # Imprime el número de elementos en la lista
print(len(mi_tupla))  # Imprime el número de elementos en la tupla
```
El rango de una lista o tupla se puede determinar utilizando la función `range()`. Por ejemplo:
```python
for i in range(len(mi_lista)):
    print(mi_lista[i])  # Imprime cada elemento de la lista
```
**Operaciones**

Las listas y tuplas pueden ser utilizadas para realizar operaciones básicas como concatenación, slicing y búsqueda.

* Concatenación: se puede concatenar dos listas o tuplas utilizando el operador `+`. Por ejemplo:
```python
mi_lista1 = [1, 2, 3]
mi_lista2 = [4, 5, 6]
mi_lista_concatenada = mi_lista1 + mi_lista2
print(mi_lista_concatenada)  # [1, 2, 3, 4, 5, 6]
```
* Slicing: se puede extraer un rango de elementos de una lista o tupla utilizando el operador `[]`. Por ejemplo:
```python
mi_lista = [1, 2, 3, 4, 5]
print(mi_lista[1:3])  # [2, 3]
```
* Búsqueda: se puede buscar un elemento en una lista o tupla utilizando la función `in`. Por ejemplo:
```python
mi_lista = [1, 2, 3, 4, 5]
if 3 in mi_lista:
    print("El elemento 3 está en la lista")
```
**Conversiones**

Las listas y tuplas pueden ser convertidas entre sí utilizando las funciones `list()` y `tuple()`. Por ejemplo:
```python
mi_tupla = (1, 2, 3)
mi_lista = list(mi_tupla)
print(mi_lista)  # [1, 2, 3]

mi_lista = [1, 2, 3]
mi_tupla = tuple(mi_lista)
print(mi_tupla)  # (1, 2, 3)
```
**Ejemplos y Uso**

A continuación, se presentan algunos ejemplos de cómo utilizar listas y tuplas en Python:

* Listas:
```python
# Crear una lista vacía
mi_lista_vacia = []

# Agregar elementos a la lista
mi_lista_vacia.append(1)
mi_lista_vacia.append(2)
print(mi_lista_vacia)  # [1, 2]

# Modificar un elemento de la lista
mi_lista_vacia[0] = 10
print(mi_lista_vacia)  # [10, 2]
```
* Tuplas:
```python
# Crear una tupla vacía
mi_tupla_vacia = ()

# Agregar elementos a la tupla
mi_tupla_vacia += (1,)
mi_tupla_vacia += (2,)
print(mi_tupla_vacia)  # (1, 2)

# Intentar modificar un elemento de la tupla
try:
    mi_tupla_vacia[0] = 10
except TypeError:
    print("No se puede modificar una tupla")
```
En resumen, las listas y tuplas son dos tipos de datos fundamentales en Python que ofrecen una gran flexibilidad y versatilidad. Las listas pueden ser modificadas mientras que las tuplas son inmutables. Aprendiendo a utilizar estas estructuras de datos, podemos crear programas más eficientes y efectivos.

**Ejercicios**

1. Crear una lista vacía y agregar 5 elementos.
2. Modificar el primer elemento de la lista.
3. Crear una tupla con 3 elementos y mostrar su longitud.
4. Concatenar dos listas.
5. Extraer un rango de elementos de una lista utilizando slicing.
6. Buscar un elemento en una lista utilizando la función `in`.
7. Convertir una lista a tupla y viceversa.

**Conclusión**

En este capítulo, hemos explorado los conceptos fundamentales de listas y tuplas en Python. Aprendimos cómo crear, acceder y modificar elementos en estas estructuras de datos, así como realizar operaciones básicas como concatenación, slicing y búsqueda. Con la práctica y el uso de ejercicios, podemos mejorar nuestras habilidades y crear programas más efectivos utilizando listas y tuplas. En el próximo capítulo, exploraremos otros tipos de datos y variables en Python.