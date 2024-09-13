**Capítulo 5: Entrada/Salida y Manejo de Archivos**

**Manejo de Archivos CSV**

En el mundo de la programación, los archivos CSV (Comma Separated Values) son una forma común de almacenar y intercambiar datos entre diferentes aplicaciones y sistemas. En este capítulo, vamos a profundizar en el manejo de archivos CSV en Python, incluyendo cómo leer, escribir y manipular estos archivos.

**Estructura básica de un archivo CSV**

Un archivo CSV se compone de líneas y columnas separadas por comas (o otros caracteres especificados). Cada línea representa una fila o registro en el archivo, mientras que cada columna representa un campo o atributo del registro. La estructura general de un archivo CSV es la siguiente:
```
campo1,campo2,campo3,...,campon
valor1,valor2,valor3,...,valorn
...
```
Donde `campoX` son los nombres de las columnas y `valorX` son los valores asociados a cada columna.

**Leeendo archivos CSV**

Para leer un archivo CSV en Python, podemos utilizar la función `csv.reader()` del módulo `csv`. Esta función devuelve un objeto iterador que permite recorrer línea por línea el archivo.
```python
import csv

with open('archivo.csv', 'r') as archivo:
    lector = csv.reader(archivo)
    for fila in lector:
        print(fila)
```
En este ejemplo, se abre el archivo `archivo.csv` en modo lectura y se crea un objeto iterador con la función `csv.reader()`. Luego, se itera sobre cada línea del archivo utilizando un bucle `for`, imprimiendo cada fila (o registro) como una lista de valores.

**Escribiendo archivos CSV**

Para escribir un archivo CSV en Python, podemos utilizar la función `csv.writer()` del módulo `csv`. Esta función devuelve un objeto escritor que permite escribir líneas en el archivo.
```python
import csv

with open('archivo.csv', 'w') as archivo:
    escritor = csv.writer(archivo)
    escritor.writerow(['campo1', 'campo2', 'campo3'])  # Escribimos la primera línea (cabecera)
    escritor.writerow(['valor1', 'valor2', 'valor3'])  # Escribimos la segunda línea
    ...
```
En este ejemplo, se abre el archivo `archivo.csv` en modo escritura y se crea un objeto escritor con la función `csv.writer()`. Luego, se escribe la primera línea (cabecera) con los nombres de las columnas utilizando el método `writerow()`, seguida de las líneas de datos.

**Manipulando archivos CSV**

Una vez que tenemos un archivo CSV abierto y leído, podemos manipular sus contenidos utilizando Python. Por ejemplo, podemos agregar o eliminar filas o columnas, cambiar los valores de los campos, etc.
```python
import csv

with open('archivo.csv', 'r') as archivo:
    lector = csv.reader(archivo)
    fila_actual = []
    for fila in lector:
        fila_actual.append(fila)
        if len(fila) > 3:  # Si la fila tiene más de 3 columnas, eliminamos la última columna
            fila_actual[-1] = ''

with open('archivo.csv', 'w') as archivo:
    escritor = csv.writer(archivo)
    for fila in fila_actual:
        escritor.writerow(fila)
```
En este ejemplo, se lee el archivo `archivo.csv` y se itera sobre cada línea. Si la longitud de la fila es mayor a 3, se elimina la última columna. Luego, se escribe el archivo modificado.

**Otras opciones del módulo csv**

Además de las funciones `reader()` y `writer()`, el módulo `csv` ofrece otras opciones para trabajar con archivos CSV:

* **`delimiter`:** permite especificar el carácter que separa los campos en el archivo. Por defecto es la coma (`,`).
* **`quotechar`:** permite especificar el carácter que indica citado o cadena en el archivo. Por defecto es la comilla doble (`"`) o simple (`'`).
* **`escapechar`:** permite especificar el carácter que se utiliza para escapar caracteres especiales en el archivo.
* **`lineterminator`:** permite especificar el carácter que termina una línea en el archivo. Por defecto es la nueva línea (`\n`) o Windows (`\r\n`).

**Conclusión**

En este capítulo, hemos explorado el manejo de archivos CSV en Python utilizando el módulo `csv`. Hemos visto cómo leer y escribir archivos CSV, así como manipular sus contenidos. Con esta información, podremos trabajar con archivos CSV de manera efectiva en nuestros proyectos.

**Ejercicios**

1. Lee un archivo CSV y imprime cada fila.
2. Escriba un archivo CSV con los siguientes datos:
	* Cabecera: `id`, `nombre`, `edad`
	* Registros:
		+ 1, Juan, 25
		+ 2, María, 30
		+ 3, José, 35
3. Modifique el ejercicio anterior para eliminar la columna de edades y agregar una nueva columna llamada `correo`.
4. Lee un archivo CSV y elimine todas las filas que contengan valores nulos.
5. Escriba un archivo CSV con los siguientes datos:
	* Cabecera: `id`, `nombre`, `edad`
	* Registros:
		+ 1, Juan, 25
		+ 2, María, 30
		+ 3, José, 35

**Soluciones**

1. Lee un archivo CSV y imprime cada fila.
```python
import csv

with open('archivo.csv', 'r') as archivo:
    lector = csv.reader(archivo)
    for fila in lector:
        print(fila)
```
2. Escriba un archivo CSV con los siguientes datos:
```python
import csv

with open('archivo.csv', 'w') as archivo:
    escritor = csv.writer(archivo)
    escritor.writerow(['id', 'nombre', 'edad'])  # Cabecera
    escritor.writerow([1, 'Juan', 25])  # Registros
    escritor.writerow([2, 'María', 30])
    escritor.writerow([3, 'José', 35])
```
3. Modifique el ejercicio anterior para eliminar la columna de edades y agregar una nueva columna llamada `correo`.
```python
import csv

with open('archivo.csv', 'w') as archivo:
    escritor = csv.writer(archivo)
    escritor.writerow(['id', 'nombre', 'correo'])  # Cabecera
    escritor.writerow([1, 'Juan', 'juan@example.com'])  # Registros
    escritor.writerow([2, 'María', 'maria@example.com'])
    escritor.writerow([3, 'José', 'jose@example.com'])
```
4. Lee un archivo CSV y elimine todas las filas que contengan valores nulos.
```python
import csv

with open('archivo.csv', 'r') as archivo:
    lector = csv.reader(archivo)
    fila_actual = []
    for fila in lector:
        if '' not in fila:  # Si no hay valores nulos, se añade a la lista de filas
            fila_actual.append(fila)

with open('archivo.csv', 'w') as archivo:
    escritor = csv.writer(archivo)
    for fila in fila_actual:
        escritor.writerow(fila)
```
5. Escriba un archivo CSV con los siguientes datos:
```python
import csv

with open('archivo.csv', 'w') as archivo:
    escritor = csv.writer(archivo)
    escritor.writerow(['id', 'nombre', 'edad'])  # Cabecera
    escritor.writerow([1, 'Juan', 25])  # Registros
    escritor.writerow([2, 'María', 30])
    escritor.writerow([3, 'José', 35])
```
**Recursos**

* [Documentación oficial del módulo csv](https://docs.python.org/3/library/csv.html)
* [Ejemplos de uso del módulo csv](https://docs.python.org/3/tutorial/inputoutput.html#reading-and-writing-csv-files)