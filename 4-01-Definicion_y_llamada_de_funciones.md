**Capítulo 5: Funciones**

**Sección 1: Definición y Llamada de Funciones**

En el mundo de la programación, las funciones son bloques de código que realizan una tarea específica y se pueden reutilizar en diferentes partes del programa. En este capítulo, vamos a profundizar en los conceptos fundamentales de definición y llamada de funciones en Python.

**Definición de Funciones**

Una función en Python se define utilizando la palabra clave `def`, seguida del nombre de la función y paréntesis que contiene los argumentos. El cuerpo de la función es el bloque de código que se ejecutará cuando se llame a la función.

Sintaxis:
```
def nombre_funcion(argumento1, argumento2, ...):
    # Código a ejecutar
```
Por ejemplo, podemos definir una función que calcula la suma de dos números:
```python
def sumar(a, b):
    return a + b
```
**Llamada de Funciones**

Para llamar a una función, simplemente se escribe el nombre de la función seguido de los argumentos entre paréntesis. Los argumentos se pasan por valor o por referencia, dependiendo del tipo de dato y de cómo se defina la función.

Sintaxis:
```
nombre_funcion(argumento1, argumento2, ...)
```
Volviendo al ejemplo anterior, podemos llamar a la función `sumar` con los números 2 y 3 como argumentos:
```python
resultado = sumar(2, 3)
print(resultado)  # Imprime 5
```
**Argumentos y Parámetros**

Los argumentos son los valores que se pasan a una función cuando se la llama. Los parámetros, por otro lado, son los nombres que se utilizan en la definición de la función para referirse a los argumentos.

En el ejemplo anterior, `a` y `b` son los parámetros de la función `sumar`, y 2 y 3 son los argumentos que se pasan a la función cuando se la llama.

**Tipos de Argumentos**

Los argumentos pueden ser pasados por valor o por referencia. Los argumentos pasados por valor son copias de los valores originales, mientras que los argumentos pasados por referencia son referencias directas a los valores originales.

En Python, todos los argumentos se pasan por valor por defecto, excepto los argumentos que se definen como `*args` o `**kwargs`, que se pasan por referencia.

**Ejemplos**

Vamos a ver algunos ejemplos para ilustrar cómo funcionan los argumentos y parámetros en Python:

* Ejemplo 1: Argumentos pasados por valor
```python
def multiplicar(a, b):
    return a * b

resultado = multiplicar(2, 3)
print(resultado)  # Imprime 6
```
* Ejemplo 2: Argumentos pasados por referencia (usando `*args`)
```python
def concatenar(*args):
    resultado = ''
    for arg in args:
        resultado += str(arg)
    return resultado

resultado = concatenar('Hola', ' ', 'mundo')
print(resultado)  # Imprime "Hola mundo"
```
* Ejemplo 3: Argumentos pasados por referencia (usando `**kwargs`)
```python
def calcular_area(**kwargs):
    area = 0
    if 'largo' in kwargs and 'ancho' in kwargs:
        area = kwargs['largo'] * kwargs['ancho']
    return area

area = calcular_area(largo=3, ancho=4)
print(area)  # Imprime 12
```
**Retorno de Valores**

Las funciones en Python pueden devolver un valor utilizando la palabra clave `return`. El valor devuelto se puede asignar a una variable o utilizarlo en el código.

Sintaxis:
```
return valor_devuelto
```
Ejemplo:
```python
def cuadrado(a):
    return a * a

resultado = cuadrado(4)
print(resultado)  # Imprime 16
```
**Conclusión**

En esta sección, hemos aprendido cómo definir y llamar a funciones en Python. Vimos también los conceptos de argumentos y parámetros, tipos de argumentos y retorno de valores. Estos conceptos son fundamentales para crear programas eficientes y escalables.

En la próxima sección, vamos a profundizar en otros aspectos de las funciones en Python, como el uso de lambda functions y funciones recursivas.