**Capítulo 5: Decoradores**

En el capítulo anterior, hemos explorado las funciones de orden superior y cómo pueden ser utilizadas para crear funciones más poderosas y versátiles en Python. En este capítulo, nos enfocaremos en los decoradores, una herramienta fundamental en la programación funcional que permite modificar o ampliar el comportamiento de funciones existentes.

**¿Qué son los decoradores?**

Un decorador es una función que se aplica a otra función para modificar o extender su comportamiento. En otras palabras, un decorador es una función que "adorna" a otra función, por lo que se llama "decorador". Los decoradores se utilizan comúnmente para lograr varios objetivos, como:

* Registrar el tiempo de ejecución de una función
* Implementar autenticación o autorización en funciones
* Agregar funcionalidades adicionales a una función sin modificar su código original
* Proporcionar un punto de extensión para otras partes del programa

**Estructura de los decoradores**

Los decoradores se estructuran como funciones que toman otra función como parámetro y devuelven otra función. La sintaxis general de un decorador es la siguiente:
```python
@decorator_name
def function_to_decorate():
    pass
```
La notación `@` indica que el decorador `decorator_name` se aplica a la función `function_to_decorate`. Cuando se aplica un decorador, Python llama a la función decoradora y pasa como parámetro la función original. La función decoradora puede modificar o ampliar la función original de varias maneras.

**Ejemplo básico**

Vamos a crear un decorador que registre el tiempo de ejecución de una función:
```python
import time

def timer_decorator(func):
    def wrapper():
        start_time = time.time()
        func()
        end_time = time.time()
        print(f"Tiempo de ejecución: {end_time - start_time} segundos")
    return wrapper

@timer_decorator
def example_function():
    time.sleep(2)
    print("Ejecutando ejemplo")

example_function()
```
En este ejemplo, el decorador `timer_decorator` toma la función `example_function` como parámetro y devuelve una nueva función `wrapper`. La función `wrapper` llama a la función original `example_function`, registra el tiempo de inicio y fin de ejecución, y imprime el resultado.

**Ejemplos más avanzados**

A continuación, vamos a ver algunos ejemplos más avanzados de decoradores:
```python
# Ejemplo 1: Decorador para implementar autenticación
def authenticated_decorator(func):
    def wrapper(*args, **kwargs):
        if not authenticate():
            print("Acceso denegado")
            return
        func(*args, **kwargs)
    return wrapper

@authenticated_decorator
def sensitive_function():
    print("Ejecutando función sensibles")

# Ejemplo 2: Decorador para agregar funcionalidades adicionales
def logging_decorator(func):
    def wrapper(*args, **kwargs):
        print(f"Ejecutando {func.__name__}")
        result = func(*args, **kwargs)
        print(f"Resultado de {func.__name__}: {result}")
        return result
    return wrapper

@logging_decorator
def example_function():
    return "Hola, mundo!"

# Ejemplo 3: Decorador para crear un singleton
def singleton_decorator(func):
    instances = {}
    def wrapper(*args, **kwargs):
        if func not in instances:
            instances[func] = func()
        return instances[func]
    return wrapper

@singleton_decorator
def create_singleton():
    return "Instancia única"

print(create_singleton())  # Imprime "Instancia única"
print(create_singleton())  # Imprime "Instancia única" (no crea una nueva instancia)
```
En estos ejemplos, los decoradores se utilizan para implementar autenticación, agregar funcionalidades adicionales y crear un singleton.

**Conclusión**

Los decoradores son una herramienta poderosa en la programación funcional que permiten modificar o ampliar el comportamiento de funciones existentes. A través de ejemplos prácticos, hemos visto cómo los decoradores pueden ser utilizados para registrar el tiempo de ejecución de una función, implementar autenticación o autorización, agregar funcionalidades adicionales y crear un singleton.

En el siguiente capítulo, exploraremos otros aspectos de la programación funcional en Python, como las closures y las higher-order functions.