**Capítulo 6: Manejo de Errores y Excepciones**

**Sección 5: Creación de Excepciones Personalizadas**

En el capítulo anterior, exploramos cómo manejar errores y excepciones en Python utilizando try/except, clausulas else y finally. También aprendimos a crear nuestras propias excepciones personalizadas para controlar mejor nuestros programas. En esta sección, vamos a profundizar en la creación de excepciones personalizadas y cómo podemos utilizarlas para mejorar la robustez y estabilidad de nuestro código.

**¿Por qué necesitamos crear excepciones personalizadas?**

A menudo, cuando estamos trabajando con un programa, podemos encontrarnos con situaciones específicas que no se cubren con las excepciones predefinidas en Python. Por ejemplo, imagine que estamos desarrollando una aplicación de gestión de libros y queremos manejar errores cuando un usuario intenta eliminar un libro que ya no existe en la base de datos. La excepción `FileNotFoundError` no será suficiente para este caso, porque no se lanza solo por el hecho de que el archivo no existe.

En estos casos, podemos crear nuestras propias excepciones personalizadas para indicar que ha ocurrido un error específico. Esto nos permite manejar errores de manera más precisa y controlada, lo que puede ser muy útil cuando estamos desarrollando aplicaciones complejas.

**Crear una excepción personalizada**

Para crear una excepción personalizada en Python, debemos heredar de la clase `Exception`. Podemos hacerlo utilizando la siguiente sintaxis:
```python
class MiExcepcion(Exception):
    pass
```
La clase `MiExcepcion` es nuestra propia excepción personalizada que podemos lanzar cuando se produzca un error específico.

**Ejemplo: Crear una excepción de libro no encontrado**

Imaginemos que estamos desarrollando la aplicación de gestión de libros mencionada anteriormente. Queremos crear una excepción `BookNotFoundError` que se lance cuando un usuario intenta eliminar un libro que ya no existe en la base de datos.
```python
class BookNotFoundError(Exception):
    def __init__(self, book_title):
        self.book_title = book_title

    def __str__(self):
        return f"El libro '{self.book_title}' no ha sido encontrado"
```
En este ejemplo, hemos definido una clase `BookNotFoundError` que tiene un atributo `book_title` para almacenar el título del libro que se está buscando. El método `__str__` devuelve una cadena que describe el error.

**Lanzar la excepción**

Para lanzar la excepción `BookNotFoundError`, podemos hacerlo utilizando el siguiente código:
```python
def eliminar_libro(book_title):
    # Buscamos el libro en la base de datos
    book = buscar_libro(book_title)
    if book is None:
        raise BookNotFoundError(book_title)

    # Eliminamos el libro
    eliminar_registro(book)
```
En este ejemplo, estamos definiendo una función `eliminar_libro` que intenta eliminar un libro con un título específico. Si el libro no existe en la base de datos, lanzamos la excepción `BookNotFoundError` con el título del libro como argumento.

**Capturar la excepción**

Para capturar la excepción `BookNotFoundError`, podemos utilizar una estructura try/except similar a la siguiente:
```python
try:
    eliminar_libro("El Señor de los Anillos")
except BookNotFoundError as e:
    print(e)
```
En este ejemplo, estamos intentando eliminar el libro "El Señor de los Anillos" utilizando la función `eliminar_libro`. Si se produce un error (es decir, si el libro no existe), la excepción `BookNotFoundError` se captura y se imprime en la consola.

**Ventajas de crear excepciones personalizadas**

Crear excepciones personalizadas tiene varias ventajas. En primer lugar, nos permite manejar errores de manera más precisa y controlada. Esto puede ser muy útil cuando estamos desarrollando aplicaciones complejas que requieren un manejo específico de errores.

En segundo lugar, las excepciones personalizadas pueden ayudar a mejorar la legibilidad y mantenibilidad del código. Cuando se produce un error, podemos utilizar el nombre de la excepción para entender rápidamente qué ha ocurrido y cómo podemos solucionarlo.

Por último, las exceptions personalizadas nos permiten addicionalmente información adicional sobre el error que ha ocurrido. En el ejemplo anterior, estamos proporcionando el título del libro que se está buscando cuando lanzamos la excepción `BookNotFoundError`. Esto puede ser muy útil para debugging y depuración.

**Conclusión**

En esta sección, hemos aprendido cómo crear nuestras propias excepciones personalizadas en Python. Creamos una clase que hereda de la clase `Exception` y definimos métodos y atributos según sea necesario. Lanzamos la excepción cuando se produce un error específico y capturamos la excepción utilizando una estructura try/except.

Las excepciones personalizadas son muy útiles para manejar errores de manera más precisa y controlada, mejorar la legibilidad y mantenibilidad del código y addicionalmente información adicional sobre el error que ha ocurrido. En el siguiente capítulo, vamos a explorar cómo podemos utilizar las excepciones personalizadas en conjunto con otros patrones de diseño para crear aplicaciones más robustas y escalables.

**Ejercicios**

1. Cree una excepción `InvalidUsernameError` que se lance cuando un usuario intenta iniciar sesión con un nombre de usuario inválido.
2. Modifique el ejemplo anterior para que la excepción `BookNotFoundError` tenga un método `__cause__` que devuelve un mensaje más detallado sobre el error.
3. Cree una clase `InvalidPasswordError` que se lance cuando un usuario intenta iniciar sesión con una contraseña inválida.

**Recursos adicionales**

* Documentación oficial de Python: [Excepciones personalizadas](https://docs.python.org/3/tutorial/errors.html#user-defined-exceptions)
* Tutorial en línea: [Creando excepciones personalizadas en Python](https://www.tutorialspoint.com/python/python_user_defined_exceptions.htm)