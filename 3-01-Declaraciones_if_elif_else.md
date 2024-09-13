**Capítulo 5: Control de Flujo**

**Declaraciones if, elif, else**

En el mundo de la programación, el control de flujo es una de las características más importantes y versátiles que podemos encontrar en los lenguajes de programación. En este capítulo, vamos a profundizar en uno de los elementos fundamentales del control de flujo: las declaraciones if, elif y else.

**¿Qué son las declaraciones if, elif y else?**

Las declaraciones if, elif y else se utilizan para crear decisiones condicionales en un programa. Estas estructuras permiten al programador evaluar una condición y ejecutar diferentes bloques de código según sea verdadera o falsa.

**La sentencia if**

La sentencia if es la más básica y fundamental de las tres. Su estructura es la siguiente:
```
if condición:
    # Código a ejecutar si la condición es verdadera
```
Donde `condición` es una expresión booleana que se evalúa como verdadera o falsa. Si la condición es verdadera, el código dentro del bloque indentado se ejecutará.

Ejemplo:
```
x = 5
if x > 10:
    print("El valor de x es mayor que 10")
```
En este ejemplo, la condición `x > 10` se evalúa como falsa porque el valor de `x` es 5. Por lo tanto, no se ejecutará el código dentro del bloque indentado.

**La sentencia elif**

La sentencia elif (short for "else if") se utiliza para agregar más condiciones a la sentencia if. Su estructura es la siguiente:
```
if condición1:
    # Código a ejecutar si la condición1 es verdadera
elif condición2:
    # Código a ejecutar si la condición1 es falsa y la condición2 es verdadera
```
Donde `condición1` y `condición2` son expresiones booleanas que se evalúan como verdadera o falsa. Si la condición1 es verdadera, el código dentro del bloque indentado se ejecutará. Si no, se evalúa la condición2.

Ejemplo:
```
x = 5
if x > 10:
    print("El valor de x es mayor que 10")
elif x == 5:
    print("El valor de x es igual a 5")
```
En este ejemplo, la condición `x > 10` se evalúa como falsa. Luego, se evalúa la condición `x == 5`, que es verdadera. Por lo tanto, se ejecutará el código dentro del bloque indentado correspondiente.

**La sentencia else**

La sentencia else se utiliza para especificar un bloque de código que se ejecutará cuando todas las condiciones anteriores sean falsas. Su estructura es la siguiente:
```
if condición1:
    # Código a ejecutar si la condición1 es verdadera
elif condición2:
    # Código a ejecutar si la condición1 es falsa y la condición2 es verdadera
else:
    # Código a ejecutar si todas las condiciones son falsas
```
Donde `condición1` y `condición2` son expresiones booleanas que se evalúan como verdadera o falsa. Si ninguna de las condiciones es verdadera, el código dentro del bloque indentado correspondiente se ejecutará.

Ejemplo:
```
x = 0
if x > 10:
    print("El valor de x es mayor que 10")
elif x == 5:
    print("El valor de x es igual a 5")
else:
    print("El valor de x es menor o igual a 0")
```
En este ejemplo, las condiciones `x > 10` y `x == 5` son falsas. Por lo tanto, se ejecutará el código dentro del bloque indentado correspondiente al else.

**Ejemplos prácticos**

A continuación, presentaremos algunos ejemplos prácticos que demuestran la utilidad de las declaraciones if, elif y else:

* Ejemplo 1: Verificar si un número es positivo, negativo o cero.
```
x = int(input("Ingrese un número: "))
if x > 0:
    print("El número es positivo")
elif x < 0:
    print("El número es negativo")
else:
    print("El número es cero")
```
* Ejemplo 2: Verificar si una persona es mayor o menor de edad.
```
edad = int(input("Ingrese su edad: "))
if edad >= 18:
    print("La persona es mayor de edad")
elif edad < 18 and edad > 0:
    print("La persona es menor de edad")
else:
    print("La edad ingresada no es válida")
```
* Ejemplo 3: Verificar si un carácter es una vocal o consonante.
```
caracter = input("Ingrese un carácter: ")
if caracter in "aeiou":
    print("El carácter es una vocal")
elif caracter.isalpha():
    print("El carácter es una consonante")
else:
    print("El carácter no es alfabético")
```
**Conclusión**

En este capítulo, hemos profundizado en las declaraciones if, elif y else y su utilidad en el control de flujo en Python. Hemos visto cómo estas estructuras permiten evaluar condiciones y ejecutar diferentes bloques de código según sea verdadera o falsa.

A continuación, en el próximo capítulo, vamos a abordar los temas de bucles (for y while) y loops condicionales (while y until). Estos elementos nos permitirán crear programas más complejos y versátiles.