**Cadenas de Texto (str)**

En el capítulo anterior, hemos abordado las variables y la asignación, así como también los números enteros, flotantes y complejos en Python. Ahora, vamos a profundizar en uno de los tipos de datos más comunes y versátiles: las cadenas de texto.

**Definición**

Una cadena de texto (str) es un tipo de dato que almacena una secuencia de caracteres, como letras, dígitos o símbolos. En Python, las cadenas de texto se representan con la palabra clave `str`.

**Creación de Cadena de Texto**

Hay varias formas de crear una cadena de texto en Python:

1. **Usando comillas**: Puedes crear una cadena de texto simplemente entre comillas:
```
mi_cadena = "Hola, mundo!"
print(mi_cadena)  # Output: Hola, mundo!
```

2. **Usando triple comillas**: Si deseas crear una cadena de texto que contenga saltos de línea o caracteres especiales, puedes utilizar triple comillas (`"""` o `'''`):
```
mi_cadena = """Este es un ejemplo
de una cadena de texto con saltos de línea"""
print(mi_cadena)
# Output:
# Este es un ejemplo
# de una cadena de texto con saltos de línea
```

3. **Usando la función `str()`**: Puedes convertir cualquier objeto a una cadena de texto utilizando la función `str()`:
```
mi_numero = 42
mi_cadena = str(mi_numero)
print(mi_cadena)  # Output: 42
```

**Operaciones con Cadena de Texto**

Las cadenas de texto en Python admiten varias operaciones:

1. **Concatenación**: Puedes concatenar dos o más cadenas de texto utilizando el símbolo `+`:
```
cadena1 = "Hola, "
cadena2 = "mundo!"
mi_cadena = cadena1 + cadena2
print(mi_cadena)  # Output: Hola, mundo!
```

2. **Repetición**: Puedes repetir una cadena de texto utilizando el operador `*`:
```
mi_cadena = "Hola" * 3
print(mi_cadena)  # Output: HolaHolaHola
```

3. **Índices y slicing**: Puedes acceder a un carácter o una parte de la cadena de texto utilizando índices y slicing:
```
mi_cadena = "Hola, mundo!"
print(mi_cadena[0])  # Output: H
print(mi_cadena[1:5])  # Output: ola,
```

4. **Métodos**: Las cadenas de texto en Python admiten varios métodos para realizar operaciones como convertir a mayúsculas o minúsculas, reemplazar caracteres, etc.:
```
mi_cadena = "Hola, mundo!"
print(mi_cadena.upper())  # Output: HOLA, MUNDO!
print(mi_cadena.replace("mundo", "planeta"))  # Output: Hola, planeta!
```

**Ejercicios**

1. Crea una cadena de texto que contenga tu nombre y apellido.
2. Utiliza la función `str()` para convertir un número entero a una cadena de texto.
3. Concatena dos cadenas de texto utilizando el símbolo `+`.
4. Repite una cadena de texto utilizando el operador `*`.
5. Accede a un carácter o una parte de la cadena de texto utilizando índices y slicing.

**Conclusión**

En este capítulo, hemos explorado las cadenas de texto (str) en Python, incluyendo su creación, operaciones básicas y métodos más avanzados. Las cadenas de texto son un tipo de dato fundamental en cualquier programa y es importante entender cómo se trabajan con ellas para crear aplicaciones eficaces.

**Siguiente Capítulo**

En el próximo capítulo, vamos a abordar los tipos de datos booleanos (bool) y la lógica condicional en Python.