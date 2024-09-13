**Capítulo 6: Estructuras de Datos Avanzadas - Trabajo con Diccionarios y Conjuntos**

En el capítulo anterior, exploramos las estructuras de datos más comunes en Python, como listas y diccionarios. Ahora, vamos a profundizar en dos de las estructuras de datos más útiles para trabajar con conjuntos de datos: los conjuntos y los diccionarios.

**1. Introducción a los Conjuntos**

Un conjunto (set en inglés) es una estructura de datos que almacena elementos únicos y no ordenados. Los conjuntos son muy útiles cuando necesitamos almacenar un grupo de elementos y queremos asegurarnos de que no hay duplicados.

En Python, los conjuntos se crean utilizando la función `set()` o simplemente rodeando una serie de elementos con llaves `{}`. Por ejemplo:
```
mi_conjunto = set([1, 2, 3, 4, 5])
print(mi_conjunto)  # {1, 2, 3, 4, 5}
```
**Operaciones con Conjuntos**

Los conjuntos permiten realizar varias operaciones útiles:

* **Unión**: La unión de dos conjuntos es el conjunto resultante que contiene todos los elementos de ambos conjuntos. Se logra utilizando la función `union()`. Por ejemplo:
```
conjunto1 = set([1, 2, 3])
conjunto2 = set([3, 4, 5])
print(conjunto1.union(conjunto2))  # {1, 2, 3, 4, 5}
```
* **Intersección**: La intersección de dos conjuntos es el conjunto resultante que contiene los elementos comunes a ambos conjuntos. Se logra utilizando la función `intersection()`. Por ejemplo:
```
conjunto1 = set([1, 2, 3])
conjunto2 = set([2, 4, 5])
print(conjunto1.intersection(conjunto2))  # {2}
```
* **Diferencia**: La diferencia entre dos conjuntos es el conjunto resultante que contiene los elementos de uno de los conjuntos que no están en el otro. Se logra utilizando la función `difference()`. Por ejemplo:
```
conjunto1 = set([1, 2, 3])
conjunto2 = set([2, 4, 5])
print(conjunto1.difference(conjunto2))  # {1, 3}
```
* **Diferencia simétrica**: La diferencia simétrica entre dos conjuntos es el conjunto resultante que contiene los elementos que están en uno de los conjuntos pero no en ambos. Se logra utilizando la función `symmetric_difference()`. Por ejemplo:
```
conjunto1 = set([1, 2, 3])
conjunto2 = set([2, 4, 5])
print(conjunto1.symmetric_difference(conjunto2))  # {1, 3, 4, 5}
```
**2. Introducción a los Diccionarios**

Un diccionario (dictionary en inglés) es una estructura de datos que almacena pares clave-valor, donde cada clave es única y se asocia con un valor específico.

En Python, los diccionarios se crean utilizando la función `dict()` o simplemente rodeando una serie de pares clave-valor con llaves `{}`. Por ejemplo:
```
mi_diccionario = dict(nombre='Juan', edad=30)
print(mi_diccionario)  # {'nombre': 'Juan', 'edad': 30}
```
**Operaciones con Diccionarios**

Los diccionarios permiten realizar varias operaciones útiles:

* **Acceso a elementos**: Se puede acceder a los valores de un diccionario utilizando la clave correspondiente. Por ejemplo:
```
mi_diccionario = dict(nombre='Juan', edad=30)
print(mi_diccionario['nombre'])  # 'Juan'
```
* **Modificación de elementos**: Se pueden modificar los valores de un diccionario utilizando la clave correspondiente. Por ejemplo:
```
mi_diccionario = dict(nombre='Juan', edad=30)
mi_diccionario['edad'] = 31
print(mi_diccionario)  # {'nombre': 'Juan', 'edad': 31}
```
* **Iteración sobre los elementos**: Se pueden iterar sobre las claves y valores de un diccionario utilizando las funciones `keys()` y `values()`. Por ejemplo:
```
mi_diccionario = dict(nombre='Juan', edad=30)
for clave, valor in mi_diccionario.items():
    print(f"{clave}: {valor}")
# nombre: Juan
# edad: 30
```
* **Eliminación de elementos**: Se pueden eliminar los elementos de un diccionario utilizando la función `del()`. Por ejemplo:
```
mi_diccionario = dict(nombre='Juan', edad=30)
del mi_diccionario['edad']
print(mi_diccionario)  # {'nombre': 'Juan'}
```
**Ejemplos y Ejercicios**

* **Ejemplo:** Crea un conjunto que almacene los nombres de los miembros de un equipo y otro conjunto que almacene las edades de los mismos. Luego, imprime la unión, intersección y diferencia entre ambos conjuntos.
```
mi_conjunto1 = set(['Juan', 'Maria', 'Pepe'])
mi_conjunto2 = set([30, 25, 35])
print(mi_conjunto1.union(mi_conjunto2))  # {'Juan', 'Maria', 'Pepe', 30, 25, 35}
print(mi_conjunto1.intersection(mi_conjunto2))  # set()
print(mi_conjunto1.difference(mi_conjunto2))  # {'Maria', 'Pepe'}
```
* **Ejercicio:** Crea un diccionario que almacene los nombres y edades de los miembros de un equipo. Luego, imprime la edad del miembro con el nombre 'Juan' y modifica la edad de ese mismo miembro a 31.
```
mi_diccionario = dict(Juan=30, Maria=25, Pepe=35)
print(mi_diccionario['Juan'])  # 30
mi_diccionario['Juan'] = 31
print(mi_diccionario)  # {'Juan': 31, 'Maria': 25, 'Pepe': 35}
```
En resumen, los conjuntos y diccionarios son estructuras de datos muy útiles en Python que permiten almacenar y manipular conjuntos de elementos. Los conjuntos se utilizan para almacenar elementos únicos y realizar operaciones como unión, intersección y diferencia, mientras que los diccionarios se utilizan para almacenar pares clave-valor y acceder a ellos de manera eficiente.

**Próxima Sección:** **Estructuras de datos avanzadas - Trabajando con listas y conjuntos**

Espero que esta sección te haya sido útil. ¡Vamos a profundizar más en las estructuras de datos avanzadas!