**Capítulo 5: Control de Flujo**

**5.1 Bucles While**

En el capítulo anterior, hemos aprendido a utilizar los bucles `for` para iterar sobre elementos en una lista o secuencia. Sin embargo, a veces necesitamos repetir un bloque de código mientras se cumpla cierta condición. En este caso, podemos utilizar los bucles `while`.

Un bucle `while` es una estructura de control de flujo que permite ejecutar un conjunto de instrucciones tantas veces como sea necesario, mientras se cumpla una condición específica.

**Estructura básica**

La estructura básica de un bucle `while` en Python es la siguiente:
```
while condición:
    # código a ejecutar
```
Donde `condición` es la expresión booleana que se evalúa en cada iteración. Si la condición es verdadera, el código dentro del bucle se ejecuta; si no lo es, el bucle termina.

**Ejemplo**

Veamos un ejemplo sencillo de cómo utilizar un bucle `while` para contar desde 0 hasta 5:
```
i = 0
while i <= 5:
    print(i)
    i += 1
```
En este ejemplo, la variable `i` se inicializa en 0. La condición del bucle es `i <= 5`, que significa "mientras `i` sea menor o igual a 5". En cada iteración, el código imprime el valor actual de `i` y luego incrementa su valor en 1.

**Ejemplo con input**

Pero ¿qué pasaría si queremos pedir al usuario que ingrese un número y luego contamos hasta ese número? Podríamos utilizar un bucle `while` para lograr esto:
```
num = int(input("Ingresá un número: "))
i = 0
while i <= num:
    print(i)
    i += 1
```
En este ejemplo, el usuario ingresa un número y luego se ejecuta el bucle `while`. La condición es `i <= num`, que significa "mientras `i` sea menor o igual al número ingresado". En cada iteración, el código imprime el valor actual de `i` y luego incrementa su valor en 1.

**Uso de variables**

Otro aspecto importante a considerar cuando trabajamos con bucles `while` es la gestión de variables. Por ejemplo, si queremos utilizar una variable para almacenar el valor de una iteración, debemos asegurarnos de que esta variable esté dentro del alcance del bucle.

**Ejemplo**

Veamos un ejemplo de cómo utilizar una variable dentro de un bucle `while`:
```
i = 0
suma = 0
while i <= 5:
    suma += i
    print(suma)
    i += 1
```
En este ejemplo, la variable `suma` se inicializa en 0 y se utiliza para almacenar la suma de los valores impares. En cada iteración, el código calcula la suma de los valores impares hasta ese momento y luego imprime el resultado.

**Ejemplo con arrays**

Finalmente, podemos utilizar bucles `while` para trabajar con arrays o listas en Python. Por ejemplo, si queremos imprimir todos los elementos de un array, podemos utilizar un bucle `while`:
```
mi_array = [1, 2, 3, 4, 5]
i = 0
while i < len(mi_array):
    print(mi_array[i])
    i += 1
```
En este ejemplo, el bucle `while` se utiliza para iterar sobre los elementos del array `mi_array`. En cada iteración, el código imprime el elemento actual y luego incrementa la variable `i`.

**Conclusión**

En conclusión, los bucles `while` son una herramienta poderosa en Python que nos permite ejecutar un conjunto de instrucciones tantas veces como sea necesario, mientras se cumpla una condición específica. Aprender a utilizar estos bucles correctamente es fundamental para cualquier desarrollador de software.

**Ejercicios**

1. Escribir un programa que pida al usuario que ingrese un número y luego conte hasta ese número utilizando un bucle `while`.
2. Escribir un programa que calcule la suma de todos los números impares entre 0 y 10 utilizando un bucle `while`.
3. Escribir un programa que imprima todos los elementos de un array utilizando un bucle `while`.

**Respuestas**

1.
```
num = int(input("Ingresá un número: "))
i = 0
while i <= num:
    print(i)
    i += 1
```
2.
```
suma = 0
i = 0
while i < 11:
    if i % 2 != 0:
        suma += i
    i += 1
print(suma)
```
3.
```
mi_array = [1, 2, 3, 4, 5]
i = 0
while i < len(mi_array):
    print(mi_array[i])
    i += 1
```