**Capítulo 4: Módulos y Paquetes**

**Sección 2: Creación de módulos propios**

En el capítulo anterior, hemos aprendido a importar módulos existentes y a crear nuestros propios módulos. En esta sección, profundizaremos en la creación de módulos propios y exploraremos los diferentes aspectos que deben tenerse en cuenta al crear un módulo propio.

**¿Por qué crear módulos propios?**

Antes de empezar a crear nuestro propio módulo, debemos reflexionar sobre por qué es importante hacerlo. Los módulos propios pueden ser muy útiles cuando se trabaja en proyectos complejos que requieren la creación de funciones y variables específicas para su implementación. Al crear un módulo propio, podemos organizar nuestro código de manera más efectiva, lo que facilita la lectura, la comprensión y el mantenimiento del mismo.

**Estructura de un módulo**

Para crear un módulo propio, debemos seguir una estructura específica. La estructura básica de un módulo es la siguiente:
```python
# mibiblioteca.py

def funcion1():
    # Código para la función 1
    pass

def funcion2():
    # Código para la función 2
    pass

variable_global = "Valor global"
```
En este ejemplo, `mibiblioteca` es el nombre del módulo y `funcion1`, `funcion2` y `variable_global` son los elementos que lo componen. Los elementos de un módulo pueden ser funciones, variables, clases o cualquier otro tipo de elemento que desee incluir en su módulo.

**Creación de un módulo**

Para crear un módulo propio, debemos seguir los siguientes pasos:

1. Creamos un archivo con el nombre del módulo y la extensión `.py` (por ejemplo, `mibiblioteca.py`).
2. Dentro del archivo, definimos las funciones, variables y otros elementos que deseamos incluir en nuestro módulo.
3. Guardamos el archivo en una ubicación específica en nuestro sistema de archivos.

**Uso de un módulo propio**

Una vez creado nuestro módulo, podemos utilizarlo en nuestros programas Python de la siguiente manera:
```python
import mibiblioteca

mibiblioteca.funcion1()
print(mibiblioteca.variable_global)
```
En este ejemplo, estamos importando el módulo `mibiblioteca` y luego llamamos a las funciones `funcion1` y utilizamos la variable `variable_global`.

**Modularización**

La modularización es un concepto importante en programación que se refiere al proceso de dividir un programa en pequeños módulos o componentes para facilitar su mantenimiento, depuración y expansión. En Python, la modularización se logra mediante la creación de módulos propios.

**Ventajas y desventajas**

A continuación, presentamos las ventajas y desventajas de crear módulos propios:

**Ventajas:**

* Facilita la organización del código.
* Permite reutilizar el código en diferentes proyectos.
* Ayuda a reducir la complejidad del programa.
* Facilita la depuración y el mantenimiento.

**Desventajas:**

* Puede ser difícil encontrar el módulo adecuado para un proyecto específico.
* Puede ser necesario crear múltiples módulos para un proyecto grande.
* El uso excesivo de módulos propios puede hacer que el programa sea más complicado de entender y depurar.

**Conclusión**

En esta sección, hemos aprendido a crear módulos propios en Python y hemos explorado los diferentes aspectos que deben tenerse en cuenta al crear un módulo propio. La creación de módulos propios es una herramienta poderosa para la programación en Python que nos permite organizar nuestro código de manera efectiva, reutilizar el código y reducir la complejidad del programa.

**Ejercicio**

Crea un módulo propio que contenga dos funciones: `suma` y `resta`. La función `suma` debe sumar dos números y la función `resta` debe restar dos números. Utiliza el módulo en un programa para probar las funciones.

Solución:
```python
# ejercicios.py

def suma(a, b):
    return a + b

def resta(a, b):
    return a - b
```
```python
import ejercicios

print(ejercicios.suma(2, 3))  # Output: 5
print(ejercicios.resta(4, 1))  # Output: 3
```
**Siguiente sección**

En la próxima sección, profundizaremos en los paquetes y exploraremos cómo crear nuestros propios paquetes para organizar nuestro código de manera efectiva.