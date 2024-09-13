**Capítulo 5: Módulos y Paquetes**

**Módulos de la Biblioteca Estándar**

En el capítulo anterior, hemos aprendido cómo importar módulos propios y crear nuestros propios módulos en Python. También vimos cómo los paquetes se utilizan para organizar y distribuir código en forma de colecciones de módulos. En este capítulo, vamos a profundizar en los módulos de la biblioteca estándar que vienen incluidos con Python.

**¿Qué son los Módulos de la Biblioteca Estándar?**

Los módulos de la biblioteca estándar son una colección de módulos predefinidos que vienen incluidos con Python. Estos módulos proporcionan funcionalidades básicas y comunes para programación, como manejo de archivos, manejo de redes, manipulación de cadenas, entre otras.

**Ejemplos de Módulos de la Biblioteca Estándar**

A continuación, te presento algunos ejemplos de módulos de la biblioteca estándar que vienen incluidos con Python:

* **math**: Este módulo proporciona funciones matemáticas básicas como potencias, raíces, logaritmos, entre otras.
* **statistics**: Este módulo proporciona funciones para realizar análisis estadísticos comunes como media, moda, desviación estándar, entre otras.
* **time**: Este módulo proporciona funciones para trabajar con fechas y horarios, como obtener la hora actual, convertir entre formatos de fecha, etc.
* **random**: Este módulo proporciona funciones para generar números aleatorios, como números enteros o flotantes.
* **re**: Este módulo proporciona funciones para trabajar con expresiones regulares, como buscar patrones en cadenas.

**Cómo Utilizar los Módulos de la Biblioteca Estándar**

Para utilizar un módulo de la biblioteca estándar, debes importarlo utilizando la instrucción `import`. Por ejemplo, para importar el módulo `math`, puedes escribir:
```python
import math
```
Una vez que hayas importado el módulo, puedes utilizar sus funciones y variables como si fueran parte de tu propio código. Por ejemplo, para calcular la raíz cuadrada de un número utilizando el módulo `math`, puedes escribir:
```python
import math
x = 9
y = math.sqrt(x)
print(y)  # Imprime 3.0
```
**Ventajas y Desventajas de los Módulos de la Biblioteca Estándar**

Los módulos de la biblioteca estándar tienen varias ventajas:

* **Conveniencia**: Los módulos de la biblioteca estándar proporcionan funcionalidades comunes que pueden ahorrarte tiempo y esfuerzo al desarrollar tu propio código.
* **Estabilidad**: Los módulos de la biblioteca estándar están estabilizados y bien probados, lo que reduce el riesgo de errores y problemas en tu código.
* **Compatibilidad**: Los módulos de la biblioteca estándar son compatibles con todas las versiones de Python.

Sin embargo, también tienen algunas desventajas:

* **Dependencia**: Los módulos de la biblioteca estándar pueden ser dependientes de otros módulos o bibliotecas, lo que puede hacer que tu código sea más complicado y difícil de mantener.
* **Limitaciones**: Los módulos de la biblioteca estándar tienen limitaciones en cuanto a las funcionalidades que ofrecen, lo que puede requerir que crees tus propios módulos o utilices otros módulos externos.

**Ejemplos de Uso de los Módulos de la Biblioteca Estándar**

A continuación, te presento algunos ejemplos de uso de los módulos de la biblioteca estándar:

* **Ejemplo 1: Utilizando el módulo `math` para calcular la raíz cuadrada**
```python
import math

x = 9
y = math.sqrt(x)
print(y)  # Imprime 3.0
```
* **Ejemplo 2: Utilizando el módulo `time` para obtener la hora actual**
```python
import time

hora_actual = time.strftime("%H:%M:%S")
print(hora_actual)  # Imprime la hora actual en formato HH:MM:SS
```
* **Ejemplo 3: Utilizando el módulo `random` para generar un número aleatorio**
```python
import random

numero_aleatorio = random.randint(1, 100)
print(numero_aleatorio)  # Imprime un número aleatorio entre 1 y 100
```
**Conclusión**

En este capítulo, hemos aprendido sobre los módulos de la biblioteca estándar que vienen incluidos con Python. Estos módulos proporcionan funcionalidades básicas y comunes para programación, como manejo de archivos, manejo de redes, manipulación de cadenas, entre otras. Aprender a utilizar estos módulos puede ahorrarte tiempo y esfuerzo al desarrollar tu propio código y puede ayudarte a crear aplicaciones más complejas y robustas.

**Ejercicios**

1. Importa el módulo `math` y utiliza la función `sin()` para calcular el seno de un ángulo en grados.
2. Importa el módulo `time` y utiliza la función `strftime()` para obtener la fecha actual en formato ISO 8601.
3. Importa el módulo `random` y utiliza la función `choice()` para seleccionar un elemento aleatorio de una lista.

**Preguntas**

1. ¿Qué es un módulo de la biblioteca estándar?
2. ¿Cómo se importan los módulos de la biblioteca estándar?
3. ¿Qué ventajas y desventajas tiene utilizar los módulos de la biblioteca estándar?