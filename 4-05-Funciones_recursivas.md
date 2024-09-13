**Capítulo 5: Funciones**

**5.1 Introducción a las funciones recursivas**

En el capítulo anterior, hemos explorado los conceptos básicos de las funciones en Python. Sin embargo, hay un tipo especial de función que se llama "función recursiva" y es fundamental entender cómo funciona para aprovechar al máximo sus ventajas.

**¿Qué son las funciones recursivas?**

Una función recursiva es una función que llama a sí misma durante su ejecución. Esto puede parecer confuso al principio, pero no hay nada de malo en que una función llame a otra versión de ella mismo. De hecho, esto es precisamente lo que permite a las funciones recursivas resolver problemas complejos de manera eficiente.

**Ejemplo básico: Factorial**

Un ejemplo clásico de función recursiva es el cálculo del factorial de un número natural. El factorial de un número n se define como el producto de todos los números enteros positivos menores que o igual a n:

n! = 1 × 2 × 3 × ... × n

Podemos implementar esta función utilizando una llamada recurrente:
```python
def factorial(n):
    if n == 0:  # base case
        return 1
    else:
        return n * factorial(n-1)  # recursive call
```
La función `factorial` toma un número natural `n` como argumento y devuelve su factorial. La base case es cuando `n` es igual a cero, en el que caso simplemente se devuelve uno. De lo contrario, la función llama a sí misma con `n-1` como argumento y multiplica el resultado por `n`.

**Análisis de la función recursiva**

La función `factorial` tiene una estructura básica:

1. **Base case**: La base case es cuando se puede resolver el problema sin necesidad de más llamadas a la función.
2. **Recursive call**: La función llama a sí misma con un argumento diferente, que en este caso es `n-1`.
3. **Recomposición del resultado**: El resultado de la llamada recurrente se multiplica por `n` para obtener el resultado final.

**Ventajas y desventajas de las funciones recursivas**

Las funciones recursivas tienen varias ventajas:

* Permite resolver problemas complejos de manera eficiente.
* Es fácil implementar algoritmos que requieren una estructura recursiva natural.
* Puede ser más legible y mantenerse en forma que código no recursivo.

Sin embargo, también hay algunas desventajas:

* Pueden tener un consumo de memoria alto si se llama a la función demasiadas veces.
* Pueden ser lentas si el problema es muy complejo o si se hace una llamada recursiva excesiva.
* No es tan fácil depurar y encontrar errores en funciones recursivas.

**Ejemplos adicionales**

A continuación, te presento algunos ejemplos más de funciones recursivas:

* **Fibonacci sequence**: La secuencia de Fibonacci es una sucesión de números naturales donde cada término es la suma de los dos términos anteriores. Podemos implementar esta función utilizando una llamada recurrente:
```python
def fibonacci(n):
    if n == 0:  # base case
        return 0
    elif n == 1:  # base case
        return 1
    else:
        return fibonacci(n-1) + fibonacci(n-2)
```
* **Binary search**: La búsqueda binaria es un algoritmo para encontrar un elemento en una lista ordenada. Podemos implementar esta función utilizando una llamada recurrente:
```python
def binary_search(arr, target):
    if len(arr) == 0:  # base case
        return -1
    else:
        mid = len(arr) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            return binary_search(arr[mid+1:], target)
        else:
            return binary_search(arr[:mid], target)
```
**Conclusión**

En este capítulo, hemos explorado el tema de las funciones recursivas en Python. Las funciones recursivas son una herramienta poderosa para resolver problemas complejos y pueden ser utilizadas para implementar algoritmos eficientes. Sin embargo, es importante tener en cuenta las ventajas y desventajas de estas funciones y utilizarlas con moderación.

**Ejercicios**

1. Implemente la función `factorial` utilizando una estructura for en lugar de una llamada recurrente.
2. Modifique el ejemplo de la secuencia de Fibonacci para que devuelva el término `n` en lugar de la suma de los dos términos anteriores.
3. Implemente la búsqueda binaria utilizando una llamada recurrente y compárela con la implementación no recursiva.

**Recursos adicionales**

* [Python documentation: Recursion](https://docs.python.org/3/tutorial/recursion.html)
* [Wikipedia: Recursion (computer science)](https://en.wikipedia.org/wiki/Recursion_(computer_science))

Espero que este capítulo te haya proporcionado una buena comprensión de las funciones recursivas en Python. En el próximo capítulo, exploraremos otros temas importantes como la programación orientada a objetos y los módulos.