**Sintaxis Básica y Estilo de Codificación (PEP 8)**

En este capítulo, vamos a profundizar en la sintaxis básica del lenguaje Python y en los estilos de codificación recomendados por la comunidad de desarrolladores.

**Sintaxis Básica**

La sintaxis básica de Python se basa en la indentación, es decir, el uso de espacios para indicar la jerarquía de los elementos en el código. La indentación se utiliza para separar las sentencias y bloques de código, lo que facilita la lectura y escritura del código.

Las sentencias en Python son similares a las de otros lenguajes de programación, como la declaración de variables, la asignación de valores y la ejecución de condicionales. Sin embargo, Python tiene algunas características únicas que lo diferencian de otros lenguajes.

**Tipos de Variables**

En Python, los tipos de variables se determinan automáticamente en función del valor que se les asigna. Por ejemplo:

```
x = 5  # x es un entero
y = "Hola"  # y es una cadena de texto
z = [1, 2, 3]  # z es una lista
```

**Operadores**

Python tiene varios operadores que se utilizan para realizar operaciones aritméticas, lógicas y comparativas. Algunos ejemplos son:

```
a = 5 + 3  # suma
b = a * 2  # multiplicación
c = a > 5  # condición
```

**Condicionales**

Las sentencias condicionales en Python se utilizan para ejecutar un bloque de código si se cumple una condición. La estructura general es la siguiente:

```
if condición:
    bloque_de_código
```

Por ejemplo:

```
x = 5
if x > 10:
    print("x es mayor que 10")
else:
    print("x no es mayor que 10")
```

**Bucles**

Los bucles en Python se utilizan para repetir un bloque de código varias veces. La estructura general es la siguiente:

```
for variable in iterable:
    bloque_de_código
```

Por ejemplo:

```
frutas = ["manzana", "banana", "plátano"]
for fruta in frutas:
    print(fruta)
```

**Funciones**

Las funciones en Python se utilizan para agrupar un conjunto de instrucciones que se pueden ejecutar varias veces con diferentes parámetros. La estructura general es la siguiente:

```
def nombre_de_la_función(par1, par2):
    bloque_de_código
    return valor_devuelto
```

Por ejemplo:

```
def saludar(nombre):
    print("Hola " + nombre)
saludar("Juan")
```

**Estilo de Codificación (PEP 8)**

El estilo de codificación en Python se basa en las normas definidas por la PEP 8, que es un documento publicado por la comunidad de desarrolladores de Python. La PEP 8 proporciona recomendaciones para el estilo de codificación, incluyendo la indentación, los espacios y la nomenclatura.

**Indentación**

La indentación se utiliza en Python para separar las sentencias y bloques de código. La indentación se debe realizar utilizando cuatro espacios, no tabuladores.

```
if condición:
    bloque_de_código  # indentado con cuatro espacios
```

**Espacios**

Los espacios se utilizan para separar los símbolos en el código. Se recomienda utilizar un espacio después de los operadores y antes y después de los paréntesis.

```
a = 5 + (3 * 2)  # espacio después del operador
```

**Nomenclatura**

La nomenclatura se refiere a la forma en que se nombran las variables, funciones y clases. Se recomienda utilizar nombres descriptivos y consistentes.

```
def calcular_area_del_triángulo(base, altura):
    return (base * altura) / 2
```

**Conclusión**

En este capítulo, hemos visto la sintaxis básica de Python y los estilos de codificación recomendados por la PEP 8. La indentación, los espacios y la nomenclatura son fundamentales para escribir código legible y fácil de mantener.

Esperamos que esta información te haya sido útil para empezar a explorar el mundo de la programación en Python. En el siguiente capítulo, vamos a profundizar en temas más avanzados como las funciones, los módulos y las clases.