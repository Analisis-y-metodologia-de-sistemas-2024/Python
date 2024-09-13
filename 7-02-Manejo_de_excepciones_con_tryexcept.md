**Capítulo 5: Manejo de Errores y Excepciones**

**Sección 2: Manejo de Excepciones con Try/Except**

El manejo de errores en Python es una parte fundamental del desarrollo de aplicaciones robustas y seguras. En el capítulo anterior, se presentaron los diferentes tipos de errores que pueden ocurrir en un programa Python. Ahora, vamos a profundizar en cómo manejar estos errores utilizando la estructura `try/except`.

**Introducción**

La estructura `try/except` es una forma de capturar y manejar errores en Python. Esta estructura se compone de dos partes: el bloque `try`, que contiene el código que puede generar un error, y el bloque `except`, que contiene el código que se ejecutará si se produce un error.

**El Bloque Try**

El bloque `try` es donde se coloca el código que puede generar un error. Este código se ejecutará hasta que se produzca un error o hasta que se llegue al final del bloque `try`.

**El Bloque Except**

El bloque `except` es donde se coloca el código que se ejecutará si se produce un error en el bloque `try`. El bloque `except` puede contener un mensaje de error personalizado que se mostrará al usuario.

**Estructura Basic Try/Except**

La estructura básica de un bloque `try/except` es la siguiente:
```
try:
    # Código que puede generar un error
except ExceptionType:
    # Código que se ejecutará si se produce un error
```
Donde `ExceptionType` es el tipo de excepción que se quiere capturar. Por ejemplo, para capturar una excepción `ValueError`, se usaría la siguiente estructura:
```
try:
    x = int("hello")
except ValueError:
    print("Error: no se puede convertir 'hello' a entero")
```
**Capturando Excepciones Personalizadas**

Python permite crear excepciones personalizadas utilizando la clase `Exception`. Para capturar una excepción personalizada, se debe utilizar el nombre de la clase en lugar del tipo de excepción.

Por ejemplo:
```
class MyError(Exception):
    pass

try:
    raise MyError("Ha ocurrido un error")
except MyError as e:
    print(f"Error: {e}")
```
**Capturando Excepciones Genéricas**

A veces, es útil capturar excepciones genéricas como `Exception` o `BaseException`. Esto se puede hacer utilizando el nombre de la clase en lugar del tipo de excepción.

Por ejemplo:
```
try:
    x = int("hello")
except Exception as e:
    print(f"Error: {e}")
```
**Capturando Excepciones Multiple**

Python permite capturar varias excepciones diferentes utilizando una estructura `except` anidada. Por ejemplo:
```
try:
    x = int("hello")
except ValueError:
    print("Error: no se puede convertir 'hello' a entero")
except TypeError:
    print("Error: tipo de dato incorrecto")
```
**Capturando Excepciones en Funciones**

Las funciones también pueden manejar excepciones utilizando la estructura `try/except`. Por ejemplo:
```
def dividir(a, b):
    try:
        resultado = a / b
    except ZeroDivisionError:
        print("Error: no se puede dividir entre cero")
    return resultado

print(dividir(10, 2))  # Output: 5.0
print(dividir(10, 0))  # Output: Error: no se puede dividir entre cero
```
**Conclusión**

En este capítulo, hemos visto cómo manejar errores en Python utilizando la estructura `try/except`. Hemos aprendido a capturar excepciones personalizadas y genéricas, así como también a capturar varias excepciones diferentes. Es importante recordar que el manejo de errores es una parte fundamental del desarrollo de aplicaciones robustas y seguras.

**Ejercicios**

1. Crear un programa que solicite al usuario un número entero y lo divida entre 2. Si el usuario ingresa cero, mostrar un mensaje de error.
2. Crear un programa que solicite al usuario un string y lo convierta a entero. Si el usuario ingresa un valor no numérico, mostrar un mensaje de error.
3. Crear un programa que simule una cuenta bancaria. La cuenta debe tener un saldo inicial de $1000. El programa debe permitir al usuario depositar o retirar dinero. Si el usuario intenta retirar más dinero del saldo disponible, mostrar un mensaje de error.

**Respuestas**

1.
```
try:
    num = int(input("Ingresa un número entero: "))
    resultado = num / 2
except ValueError:
    print("Error: no se puede convertir a entero")
except ZeroDivisionError:
    print("Error: no se puede dividir entre cero")
print(resultado)
```
2.
```
try:
    s = input("Ingresa un string: ")
    num = int(s)
except ValueError:
    print("Error: no se puede convertir a entero")
print(num)
```
3.
```
class CuentaBancaria:
    def __init__(self, saldo_inicial):
        self.saldo = saldo_inicial

    def depositar(self, monto):
        try:
            self.saldo += monto
        except TypeError:
            print("Error: el monto debe ser numérico")

    def retirar(self, monto):
        try:
            if monto > self.saldo:
                raise ValueError("No hay suficiente saldo")
            self.saldo -= monto
        except ValueError as e:
            print(f"Error: {e}")

cuenta = CuentaBancaria(1000)
print(cuenta.saldo)  # Output: 1000
cuenta.depositar(500)
print(cuenta.saldo)  # Output: 1500
cuenta.retirar(2000)  # Output: Error: No hay suficiente saldo
```
Espero que estos ejercicios y respuestas te ayuden a practicar y entender mejor el manejo de excepciones en Python. ¡Buena suerte!