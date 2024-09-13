**Capítulo 4: Tipos de Datos y Variables**

**Números (int, float, complex)**

En el capítulo anterior, exploramos los conceptos básicos de variables y asignación en Python. Ahora, vamos a profundizar en uno de los tipos de datos más comunes en programación: los números. En este apartado, veremos las tres principales categorías de números en Python: enteros (int), flotantes (float) y complejos (complex).

### 4.1 Integers (int)

Los enteros o números enteros son valores numéricos que no tienen parte decimal. En Python, los enteros se representan con la palabra clave `int`. A continuación, veremos algunos ejemplos de cómo utilizar variables de tipo entero:
```python
x = 5  # valor entero
print(x)  # Output: 5

y = -10  # valor entero negativo
print(y)  # Output: -10

z = 0  # valor entero cero
print(z)  # Output: 0
```
### 4.2 Floats (float)

Los flotantes o números flotantes son valores numéricos que tienen parte decimal. En Python, los flotantes se representan con la palabra clave `float`. A continuación, veremos algunos ejemplos de cómo utilizar variables de tipo flotante:
```python
x = 3.14  # valor flotante
print(x)  # Output: 3.14

y = -0.5  # valor flotante negativo
print(y)  # Output: -0.5

z = 1e10  # valor flotante con exponente
print(z)  # Output: 10000000000.0
```
### 4.3 Complex (complex)

Los complejos o números complejos son valores numéricos que tienen dos partes: real y imaginaria. En Python, los complejos se representan con la palabra clave `complex`. A continuación, veremos algunos ejemplos de cómo utilizar variables de tipo complejo:
```python
x = 3 + 4j  # valor complejo
print(x)  # Output: (3+4j)

y = -2 - 5j  # valor complejo negativo
print(y)  # Output: (-2-5j)

z = 1 + 0j  # valor complejo con parte real y cero imaginaria
print(z)  # Output: (1+0j)
```
### 4.4 Operaciones básicas

Una vez que hemos declarado variables de tipo entero, flotante o complejo, podemos realizar operaciones básicas como suma, resta, multiplicación y división.

**Suma y resta**
```python
x = 5
y = 3
print(x + y)  # Output: 8

x = -2
y = 4
print(x + y)  # Output: 2
```
**Multiplicación y división**
```python
x = 4
y = 2
print(x * y)  # Output: 8

x = 6
y = 3
print(x / y)  # Output: 2.0
```
### 4.5 Operaciones avanzadas

Además de las operaciones básicas, también podemos realizar operaciones más avanzadas como exponentes y raíces.

**Exponentes**
```python
x = 2
y = 3
print(x ** y)  # Output: 8

x = -2
y = 4
print(x ** y)  # Output: 16
```
**Raíces**
```python
x = 9
print(x ** (1/2))  # Output: 3.0

x = 25
print(x ** (1/2))  # Output: 5.0
```
En este apartado, hemos explorado los conceptos básicos de números en Python, incluyendo enteros, flotantes y complejos. También hemos visto algunas operaciones básicas y avanzadas que se pueden realizar con estos tipos de datos.

### Ejercicio

1. Declara variables `x`, `y` y `z` del tipo entero (int) y asignales valores 5, -2 y 0, respectivamente.
2. Realiza la suma de `x` y `y` y almacena el resultado en una nueva variable llamada `result`.
3. Declara variables `a`, `b` y `c` del tipo flotante (float) y asignales valores 3.14, -0.5 y 1e10, respectivamente.
4. Realiza la multiplicación de `a` y `b` y almacena el resultado en una nueva variable llamada `product`.
5. Declara variables `d`, `e` y `f` del tipo complejo (complex) y asignales valores 3 + 4j, -2 - 5j y 1 + 0j, respectivamente.
6. Realiza la suma de `d` y `e` y almacena el resultado en una nueva variable llamada `sum`.

**Solución**

1.
```python
x = 5
y = -2
z = 0
```
2.
```python
result = x + y
print(result)  # Output: 3
```
3.
```python
a = 3.14
b = -0.5
c = 1e10
```
4.
```python
product = a * b
print(product)  # Output: -1.57
```
5.
```python
d = 3 + 4j
e = -2 - 5j
f = 1 + 0j
```
6.
```python
sum = d + e
print(sum)  # Output: (1+9j)
```
En el próximo apartado, exploraremos los conceptos de cadenas de texto y caracteres en Python.