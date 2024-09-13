**Capítulo 7: Temas Avanzados**

**Sección 3: Testing en Python (unittest, pytest)**

En el mundo de la programación, es fundamental asegurarse de que nuestro código funciona correctamente y sin errores. Esto se logra mediante pruebas, también conocidas como testing. En este capítulo, vamos a profundizar en los conceptos básicos de testing en Python, utilizando las bibliotecas unittest y pytest.

**¿Por qué necesitamos testing?**

Antes de empezar a desarrollar un proyecto, debemos plantearnos qué queremos lograr con él. ¿Qué características debe tener nuestro programa para ser considerado completo? ¿Cuáles son los requisitos funcionales y no funcionales que debe cumplir? Una vez que tengamos una idea clara de lo que queremos lograr, podemos empezar a diseñar y desarrollar nuestro proyecto.

Sin embargo, durante el desarrollo, es fácil olvidarnos de algunos aspectos importantes. Podríamos escribir código que funcione correctamente en un entorno determinado, pero no sea compatible con otros entornos o no tenga en cuenta ciertos casos específicos. Esto puede llevar a errores y problemas difíciles de solventar.

Esa es donde entra el testing. El testing nos permite comprobar que nuestro código funciona correctamente y sin errores, antes de lanzarlo al mercado o antes de pasar a la etapa de pruebas alpha o beta. De esta manera, podemos asegurarnos de que nuestro programa cumpla con los requisitos establecidos y sea compatible con diferentes entornos.

**Introducción a unittest**

La biblioteca unittest es una de las más populares para testing en Python. Fue incluida por defecto en la versión 2.1 de Python y se ha convertido en una herramienta fundamental para cualquier desarrollador Python.

La idea básica detrás de unittest es crear clases que representen nuestras pruebas. Cada clase debe tener métodos iniciados con el nombre test_, que contienen las pruebas que queremos ejecutar. Por ejemplo:
```python
import unittest

class PruebaSimple(unittest.TestCase):
    def test_suma(self):
        self.assertEqual(2 + 2, 4)

    def test_restas(self):
        self.assertEqual(5 - 3, 2)
```
En este ejemplo, creamos una clase llamada PruebaSimple que contiene dos métodos: test_suma y test_restas. Estos métodos contienen las pruebas que queremos ejecutar.

Para ejecutar nuestras pruebas, podemos utilizar la función unittest.main(). Esta función busca todas las clases que contengan métodos iniciados con el nombre test_ y los ejecuta.
```python
if __name__ == '__main__':
    unittest.main()
```
**Introducción a pytest**

Pytest es otra biblioteca popular para testing en Python. Fue creada como una alternativa más rápida y flexible que unittest, pero sigue siendo compatible con ella.

La idea básica detrás de pytest es crear archivos de pruebas que contienen funciones o métodos que representan nuestras pruebas. Por ejemplo:
```python
import pytest

def suma(a, b):
    return a + b

@pytest.mark.parametrize("a, b, expected", [
    (2, 2, 4),
    (5, 3, 8)
])
def test_suma(a, b, expected):
    assert suma(a, b) == expected
```
En este ejemplo, creamos una función llamada suma que devuelve la suma de dos números. Luego, creamos un archivo de pruebas que contiene una función llamada test_suma que utiliza la marca pytest para especificar los casos de prueba que queremos ejecutar.

Para ejecutar nuestras pruebas, podemos utilizar la función pytest. Esta función busca todos los archivos de pruebas que contienen funciones o métodos marcados con la marca pytest y los ejecuta.
```python
pytest -v test_suma.py
```
**Ventajas y desventajas de unittest y pytest**

Ambas bibliotecas tienen sus ventajas y desventajas.

Unittest es una biblioteca más antigua y tiene una mayor compatibilidad con versiones anteriores de Python. Sin embargo, puede ser un poco más complicada de usar que pytest, especialmente para desarrolladores que no están familiarizados con el testing en general.

Pytest, por otro lado, es más rápida y flexible que unittest. Permite utilizar marcas para especificar los casos de prueba y tiene una mayor capacidad para manejar errores y excepciones. Sin embargo, puede requerir un poco más de configuración que unittest.

**Ejemplos prácticos**

Vamos a crear un ejemplo práctico utilizando unittest y pytest.

Supongamos que queremos crear un programa que calcula la superficie de un triángulo. El programa debe tomar como entrada los lados del triángulo y devolver la superficie como salida.

Primero, creamos el programa:
```python
def triangulo(a, b, c):
    s = (a + b + c) / 2
    return math.sqrt(s * (s - a) * (s - b) * (s - c))
```
Luego, creamos un archivo de pruebas utilizando unittest:
```python
import unittest
import math

class PruebaTriangulo(unittest.TestCase):
    def test_triangulo(self):
        self.assertAlmostEqual(triangulo(3, 4, 5), 6.0)

if __name__ == '__main__':
    unittest.main()
```
Y creamos otro archivo de pruebas utilizando pytest:
```python
import pytest
import math

def triangulo(a, b, c):
    s = (a + b + c) / 2
    return math.sqrt(s * (s - a) * (s - b) * (s - c))

@pytest.mark.parametrize("a, b, c, expected", [
    (3, 4, 5, 6.0),
    (1, 2, 3, 3.0)
])
def test_triangulo(a, b, c, expected):
    assert math.isclose(triangulo(a, b, c), expected)
```
**Conclusión**

En este capítulo, hemos visto los conceptos básicos de testing en Python utilizando las bibliotecas unittest y pytest. Hemos aprendido cómo crear clases y archivos de pruebas que contienen métodos y funciones que representan nuestras pruebas.

Hemos visto también algunas ventajas y desventajas de cada biblioteca y hemos creado ejemplos prácticos para ilustrar cómo utilizarlas en nuestros proyectos.

Recuerda que el testing es una parte fundamental del desarrollo de software y que tanto unittest como pytest son herramientas muy útiles para asegurarse de que nuestro código funciona correctamente.