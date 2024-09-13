**Capítulo 10: Temas Avanzados - Expresiones Regulares**

En el capítulo anterior, hemos abordado brevemente el tema de las expresiones regulares (regex) y su aplicación en Python. En este capítulo, profundizaremos en todos los aspectos de este tema, cubriendo temas como la creación de patrones, la búsqueda de matches, la extracción de información y la utilización de grupos capturadores.

**Creación de Patrones**

Las expresiones regulares se componen de una serie de caracteres especiales que permiten definir patrones para buscar en cadenas de texto. Los patrones se crean utilizando un lenguaje especial que combina letras, números y símbolos especiales para describir el patrón deseado.

En Python, los patrones se definen utilizando la clase `re` (regular expression) que se encuentra en el módulo `re`. La forma más común de definir un patrón es mediante una cadena de texto que contiene las secuencias y símbolos especiales necesarios para describir el patrón.

Por ejemplo, para crear un patrón que busque la cadena "hello" con exactitud, podemos utilizar la siguiente expresión regular:
```
import re
patron = re.compile("hello")
```
La función `re.compile()` se utiliza para compilar el patrón y crear una instancia de la clase `Pattern` que se puede utilizar para buscar matches en cadenas de texto.

**Búsqueda de Matches**

Una vez definido el patrón, podemos utilizar la función `search()` o `match()` para buscar matches en una cadena de texto. La función `search()` busca el primer match desde el principio de la cadena, mientras que la función `match()` busca un match exacto al principio de la cadena.

Por ejemplo, supongamos que queremos encontrar la cadena "hello" en un texto:
```
import re
texto = "Hola mundo, esto es un mensaje con la palabra hello"
patron = re.compile("hello")
match = patron.search(texto)
if match:
    print(match.group())  # Imprime "hello"
```
La función `search()` devuelve el objeto `Match` que contiene la posición y el contenido del match. Podemos utilizar el método `group()` para obtener el texto del match.

**Extracción de Información**

Las expresiones regulares también permiten extrar información de una cadena de texto mediante grupos capturadores. Un grupo capturador es un conjunto de caracteres que se encierra entre paréntesis () y que se puede utilizar para extraer información de la cadena.

Por ejemplo, supongamos que queremos extraer el nombre y la dirección de una persona desde un texto:
```
import re
texto = "John Doe, 123 Main St, Anytown, USA"
patron = re.compile(r"(\w+)\s+(\w+),\s+(\d+(?:\.\d+)?)\s+(\w+)")
match = patron.match(texto)
if match:
    nombre = match.group(1)  # Imprime "John"
    apellido = match.group(2)  # Imprime "Doe"
    direccion = match.group(3)  # Imprime "123"
    ciudad = match.group(4)  # Imprime "Anytown"
    print(f"Nombre: {nombre} Apellido: {apellido} Dirección: {direccion}, {ciudad}")
```
En este ejemplo, el patrón utiliza grupos capturadores para extraer el nombre, apellido, dirección y ciudad de la cadena. Los grupos se identifican por su número (1, 2, 3, etc.) y se pueden utilizar para obtener el texto del grupo.

**Utilización de Grupos Capturadores**

Los grupos capturadores también permiten utilizar subpatrones dentro de un patrón más grande. Por ejemplo, supongamos que queremos encontrar todas las palabras que contengan la letra "o" en un texto:
```
import re
texto = "Este es un texto con varias palabras"
patron = re.compile(r"\b\w*o\w*\b")
matches = patron.findall(texto)
print(matches)  # Imprime ["Este", "un", "varias"]
```
En este ejemplo, el patrón utiliza un grupo capturador (\w*) para capturar la parte de la palabra que contiene la letra "o". La función `findall()` devuelve una lista de todos los matches encontrados en la cadena.

**Utilización de Símbolos Especiales**

Las expresiones regulares también utilizan símbolos especiales que tienen significados específicos. Algunos de los símbolos más comunes son:

* `.` : representa un carácter arbitrario
* `^` : representa el inicio de la cadena
* `$` : representa el final de la cadena
* `\w` : representa una letra o número (igual que [a-zA-Z0-9])
* `\W` : representa cualquier caracter que no sea una letra o número (igual que [^a-zA-Z0-9])
* `\d` : representa un dígito (igual que [0-9])
* `\D` : representa cualquier caracter que no sea un dígito (igual que [^0-9])

Por ejemplo, para crear un patrón que busque números enteros entre 1 y 100, podemos utilizar la siguiente expresión regular:
```
import re
patron = re.compile(r"\b\d{1,3}\b")
matches = patron.findall("Este es un texto con los números 10, 20, 30, 40, 50, 60, 70, 80 y 90")
print(matches)  # Imprime ["10", "20", "30", "40", "50", "60", "70", "80", "90"]
```
En este ejemplo, el patrón utiliza los símbolos especiales `\b` para representar los límites de palabra y `\d{1,3}` para representar un número entre 1 y 3 dígitos.

**Conclusión**

Las expresiones regulares son una herramienta poderosa para buscar y extraer información de cadenas de texto en Python. Al entender cómo se crean patrones y cómo se utilizan los grupos capturadores, podemos desarrollar aplicaciones más avanzadas que pueden manejar grandes cantidades de datos.

En el próximo capítulo, abordaremos otro tema importante: la gestión de errores y excepciones en Python.