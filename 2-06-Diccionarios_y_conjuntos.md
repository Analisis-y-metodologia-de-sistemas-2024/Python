**Diccionarios y Conjuntos**

En este capítulo, exploraremos dos conceptos fundamentales en programación: diccionarios y conjuntos. Estos tipos de datos son comunes en muchos lenguajes de programación, incluyendo Python.

**1. Diccionarios (Dictionaries)**

Un diccionario es un tipo de dato que almacena pares de clave-valor. Las claves se utilizan para acceder a los valores asociados. En Python, se pueden crear diccionarios utilizando la función `dict()` o utilizando literales.

**Ejemplo 1: Creación de un diccionario**
```python
mi_diccionario = dict(nombre='Juan', apellido='Pérez', edad=30)
print(mi_diccionario)  # {nombre: 'Juan', apellido: 'Pérez', edad: 30}
```
**Ejemplo 2: Creación de un diccionario utilizando literales**
```python
mi_diccionario = {'nombre': 'Juan', 'apellido': 'Pérez', 'edad': 30}
print(mi_diccionario)  # {nombre: 'Juan', apellido: 'Pérez', edad: 30}
```
**Operaciones con diccionarios**

* **Acceso a valores**: Se pueden acceder a los valores de un diccionario utilizando la clave correspondiente.
```python
mi_diccionario = {'nombre': 'Juan', 'apellido': 'Pérez', 'edad': 30}
print(mi_diccionario['nombre'])  # Juan
```
* **Modificación de valores**: Se pueden modificar los valores de un diccionario utilizando la clave correspondiente.
```python
mi_diccionario = {'nombre': 'Juan', 'apellido': 'Pérez', 'edad': 30}
mi_diccionario['apellido'] = 'González'
print(mi_diccionario)  # {nombre: 'Juan', apellido: 'González', edad: 30}
```
* **Agregación de elementos**: Se pueden agregar nuevos elementos a un diccionario utilizando la función `update()`.
```python
mi_diccionario = {'nombre': 'Juan', 'apellido': 'Pérez', 'edad': 30}
mi_diccionario.update({'ciudad': 'Buenos Aires'})
print(mi_diccionario)  # {nombre: 'Juan', apellido: 'Pérez', edad: 30, ciudad: 'Buenos Aires'}
```
* **Eliminación de elementos**: Se pueden eliminar elementos de un diccionario utilizando la función `pop()` o el método `del`.
```python
mi_diccionario = {'nombre': 'Juan', 'apellido': 'Pérez', 'edad': 30}
mi_diccionario.pop('apellido')
print(mi_diccionario)  # {nombre: 'Juan', edad: 30}
```
**2. Conjuntos (Sets)**

Un conjunto es un tipo de dato que almacena una colección única de elementos. En Python, se pueden crear conjuntos utilizando la función `set()` o utilizando literales.

**Ejemplo 1: Creación de un conjunto**
```python
mi_conjunto = set([1, 2, 3, 4, 5])
print(mi_conjunto)  # {1, 2, 3, 4, 5}
```
**Ejemplo 2: Creación de un conjunto utilizando literales**
```python
mi_conjunto = {1, 2, 3, 4, 5}
print(mi_conjunto)  # {1, 2, 3, 4, 5}
```
**Operaciones con conjuntos**

* **Unión**: Se pueden unir dos conjuntos utilizando la función `union()`.
```python
conjunto1 = set([1, 2, 3])
conjunto2 = set([3, 4, 5])
unido = conjunto1.union(conjunto2)
print(unido)  # {1, 2, 3, 4, 5}
```
* **Intersección**: Se pueden obtener la intersección de dos conjuntos utilizando la función `intersection()`.
```python
conjunto1 = set([1, 2, 3])
conjunto2 = set([3, 4, 5])
interseccion = conjunto1.intersection(conjunto2)
print(interseccion)  # {3}
```
* **Diferencia**: Se pueden obtener la diferencia entre dos conjuntos utilizando la función `difference()`.
```python
conjunto1 = set([1, 2, 3])
conjunto2 = set([3, 4, 5])
diferencia = conjunto1.difference(conjunto2)
print(diferencia)  # {1, 2}
```
* **Diferencia simétrica**: Se pueden obtener la diferencia simétrica entre dos conjuntos utilizando la función `symmetric_difference()`.
```python
conjunto1 = set([1, 2, 3])
conjunto2 = set([3, 4, 5])
diferencia_simetrica = conjunto1.symmetric_difference(conjunto2)
print(diferencia_simetrica)  # {1, 2, 4, 5}
```
**Conclusión**

En este capítulo, hemos explorado los conceptos de diccionarios y conjuntos en Python. Los diccionarios son una forma efectiva de almacenar pares de clave-valor, mientras que los conjuntos son una forma eficiente de almacenar colecciones únicas de elementos. Las operaciones con estos tipos de datos permiten realizar tareas como la unión, intersección y diferencia entre conjuntos, y la modificación de valores en diccionarios.

**Ejercicio**

Crea un programa que lea un archivo de texto y conte las palabras únicas que contiene. Utiliza conjuntos para almacenar las palabras y luego imprime el resultado.

**Solución**
```python
def contar_palabras_archivo(nombre_archivo):
    conjunto_palabras = set()
    with open(nombre_archivo, 'r') as archivo:
        for línea in archivo:
            palabras = línea.split()
            for palabra in palabras:
                conjunto_palabras.add(palabra.lower())
    return len(conjunto_palabras)

nombre_archivo = 'ruta/al/archivo.txt'
print(contar_palabras_archivo(nombre_archivo))
```
Este programa lee un archivo de texto, split las líneas en palabras y agrega cada palabra a un conjunto. Luego, imprime el tamaño del conjunto, que representa el número de palabras únicas en el archivo.