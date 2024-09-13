**Capítulo 3: Funciones**

**Alcance de Variables y Funciones Lambda**

En el capítulo anterior, vimos cómo definir y llamar a funciones en Python. También exploramos los conceptos de argumentos y parámetros, así como el retorno de valores. Ahora, profundizaremos en dos temas clave: alcance de variables y funciones lambda.

**Alcance de Variables**

En Python, las variables tienen un alcance que se refiere al ámbito dentro del cual la variable es accesible. En otras palabras, el alcance de una variable determina dónde puede ser utilizada o modificada en el código.

Python utiliza dos tipos de alcance para las variables:

1. **Alcance local**: Las variables definidas dentro de una función tienen alcance local y solo son accesibles dentro de esa función. Cuando la función se llama, crea un ámbito temporal que contiene las variables locales. Cuando la función termina, el ámbito se elimina y las variables locales desaparecen.
2. **Alcance global**: Las variables definidas fuera de una función tienen alcance global y pueden ser accedidas desde cualquier lugar del código.

A continuación, veremos un ejemplo que ilustra la diferencia entre alcance local y global:
```python
x = 10  # variable global

def suma(y):
    z = y + x  # variable local
    return z

print(suma(5))  # imprime 15
print(x)  # imprime 10
```
En este ejemplo, la variable `x` es una variable global definida fuera de la función `suma`. La variable `z` es una variable local definida dentro de la función `suma`. Aunque ambas variables se llaman "x" y "z", tienen alcance diferente. La variable `x` global puede ser accedida desde cualquier lugar del código, mientras que la variable `z` local solo está disponible dentro de la función `suma`.

**Funciones Lambda**

Las funciones lambda son una forma concisa de definir pequeñas funciones anónimas. Se utilizan comúnmente cuando se necesita una función única y breve que se use una sola vez.

La sintaxis para definir una función lambda es la siguiente:
```python
lambda arguments: expression
```
Donde `arguments` es una lista de parámetros separados por comas, y `expression` es el cuerpo de la función.

A continuación, veremos un ejemplo que ilustra cómo se utiliza una función lambda:
```python
suma = lambda x, y: x + y
print(suma(2, 3))  # imprime 5
```
En este ejemplo, definimos una función lambda llamada `suma` que toma dos argumentos `x` y `y`. La función lambda devuelve la suma de ambos argumentos. Luego, llamamos a la función lambda con los argumentos `2` y `3`, y el resultado es `5`.

**Ventajas y Desventajas de las Funciones Lambda**

Las funciones lambda tienen algunas ventajas y desventajas que debemos considerar:

Ventajas:

* **Concisión**: Las funciones lambda son muy concisas y pueden ser utilizadas en lugares donde no se puede definir una función normal.
* **Facilidad de uso**: Las funciones lambda son fáciles de utilizar y no requieren la definición de un nombre para la función.

Desventajas:

* **Limitaciones**: Las funciones lambda tienen algunas limitaciones. No pueden contener sentencias `return`, ni declarar variables o funciones internas.
* **Dificultad de depuración**: Debido a su concisión, las funciones lambda pueden ser difíciles de depurar cuando algo sale mal.

**Ejemplos de Uso de Funciones Lambda**

A continuación, veremos algunos ejemplos que ilustran cómo se utilizan las funciones lambda en diferentes contextos:

* **Filter**: La función `filter` utiliza una función lambda para filtrar un conjunto de elementos.
```python
numbers = [1, 2, 3, 4, 5]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)  # imprime [2, 4]
```
* **Map**: La función `map` utiliza una función lambda para aplicar un operador a un conjunto de elementos.
```python
numbers = [1, 2, 3, 4, 5]
squared_numbers = list(map(lambda x: x**2, numbers))
print(squared_numbers)  # imprime [1, 4, 9, 16, 25]
```
* **Reduce**: La función `reduce` utiliza una función lambda para reducir un conjunto de elementos a un valor único.
```python
numbers = [1, 2, 3, 4, 5]
sum_numbers = reduce(lambda x, y: x + y, numbers)
print(sum_numbers)  # imprime 15
```
En conclusión, las funciones lambda son una herramienta útil en Python que permite definir pequeñas funciones anónimas. Aunque tienen algunas limitaciones, se utilizan comúnmente en contextos donde se necesitan funciones breves y concisas.

**Ejercicio**

Definir una función lambda que tome un número como argumento y devuelva el cuadrado de ese número.

Solución:
```python
cuadrado = lambda x: x ** 2
print(cuadrado(4))  # imprime 16
```
**Conclusiones**

En este capítulo, hemos profundizado en dos temas clave relacionados con las funciones en Python: alcance de variables y funciones lambda. Vimos cómo las variables tienen un alcance que determina dónde pueden ser utilizadas o modificadas en el código, y cómo las funciones lambda son una forma concisa de definir pequeñas funciones anónimas.

Esperamos que este capítulo te haya sido útil para entender mejor los conceptos de alcance de variables y funciones lambda en Python. En el próximo capítulo, exploraremos otros temas relacionados con las funciones, como la recursión y el uso de funciones como objetos.