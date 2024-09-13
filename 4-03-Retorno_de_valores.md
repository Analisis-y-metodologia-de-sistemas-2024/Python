**Retorno de Valores**

En el capítulo anterior, vimos cómo las funciones pueden recibir argumentos y parámetros para realizar operaciones y obtener resultados. Sin embargo, en este apartado, nos enfocaremos en uno de los aspectos más importantes de las funciones: su capacidad para regresar valores.

**Qué son los Valores de Retorno**

Los valores de retorno son los resultados que una función devuelve después de ser ejecutada. Estos valores pueden ser utilizados por el código que llama a la función, permitiendo obtener información valiosa y procesarla según sea necesario.

En Python, las funciones pueden regresar varios tipos de valores, incluyendo:

* Números enteros o flotantes
* Cadena de texto
* Booleanos (verdadero o falso)
* Listas o conjuntos de elementos
* Diccionarios
* Null o None

**Cómo Regresar Valores**

Existen varias formas de regresar valores desde una función en Python. A continuación, se presentan algunas de las más comunes:

1. **Return**: La palabra clave `return` es utilizada para regresar un valor desde una función. Por ejemplo:
```python
def sumar(a, b):
    resultado = a + b
    return resultado

print(sumar(2, 3))  # Imprime 5
```
En este ejemplo, la función `sumar` recibe dos argumentos `a` y `b`, los suma y regresa el resultado utilizando la palabra clave `return`.

2. **Return con Argumentos**: Puedes regresar múltiples valores utilizando una lista o tupla. Por ejemplo:
```python
def dividir(a, b):
    if b == 0:
        return "Error: División entre cero"
    else:
        resultado = a / b
        return resultado

print(dividir(4, 2))  # Imprime 2.0
print(dividir(4, 0))  # Imprime "Error: División entre cero"
```
En este ejemplo, la función `dividir` regresa un mensaje de error si se intenta dividir entre cero, y el resultado de la división en caso contrario.

3. **Return con Diccionarios**: Puedes regresar diccionarios utilizando la palabra clave `return`. Por ejemplo:
```python
def obtener_datos(nombre, edad):
    datos = {"nombre": nombre, "edad": edad}
    return datos

print(obtener_datos("Juan", 30))  # Imprime {'nombre': 'Juan', 'edad': 30}
```
En este ejemplo, la función `obtener_datos` regresa un diccionario con los valores de `nombre` y `edad`.

**Uso de Valores de Retorno**

Los valores de retorno son fundamentales en programación, ya que permiten compartir información entre diferentes partes del código. A continuación, se presentan algunos ejemplos de cómo utilizar valores de retorno:

1. **Asignar Valores**: Puedes asignar el valor regresado por una función a una variable. Por ejemplo:
```python
def get_name():
    return "Juan"

nombre = get_name()
print(nombre)  # Imprime "Juan"
```
En este ejemplo, la función `get_name` regresa el nombre "Juan", que se asigna a la variable `nombre`.

2. **Manipular Valores**: Puedes manipular los valores regresados por una función utilizando operaciones aritméticas o lógicas. Por ejemplo:
```python
def get_area(largo, ancho):
    return largo * ancho

area = get_area(4, 5)
print(area)  # Imprime 20
```
En este ejemplo, la función `get_area` regresa el área de un rectángulo, que se utiliza para asignar un valor a la variable `area`.

3. **Imprimir Valores**: Puedes imprimir los valores regresados por una función utilizando la función `print`. Por ejemplo:
```python
def get_message():
    return "Bienvenido al sistema"

print(get_message())  # Imprime "Bienvenido al sistema"
```
En este ejemplo, la función `get_message` regresa un mensaje, que se imprime utilizando la función `print`.

**Conclusión**

En conclusión, los valores de retorno son una característica fundamental de las funciones en Python. Permiten compartir información entre diferentes partes del código y permiten manipular y procesar datos de manera efectiva. En este apartado, vimos cómo regresar valores desde una función utilizando la palabra clave `return` y cómo utilizar los valores regresados para asignar variables, manipular datos o imprimir mensajes.

En el próximo capítulo, exploraremos otro tema importante en programación: estructuras de control de flujo. Aprenderemos a utilizar sentencias `if`, `else` y `while` para dirigir el flujo del programa y realizar operaciones condicionales y repetidas.