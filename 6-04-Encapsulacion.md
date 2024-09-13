**Capítulo 5: Programación Orientada a Objetos - Encapsulación**

La encapsulación es una de las características más importantes de la programación orientada a objetos (POO). En este capítulo, profundizaremos en el tema de la encapsulación y cómo se aplica en Python.

**¿Qué es la encapsulación?**

La encapsulación consiste en envolver los atributos y métodos de una clase dentro de un contenedor llamado objeto. De esta forma, se ocultan los detalles internos de la clase y solo se exponen métodos y propiedades específicos para interactuar con ella.

**Ventajas de la encapsulación**

La encapsulación tiene varias ventajas importantes:

* **Seguridad**: al ocultar los detalles internos de una clase, se reduce el riesgo de modificación accidental o malintencionada.
* **Organización**: la encapsulación ayuda a organizar el código en bloques lógicos y faciles de entender.
* **Reutilización**: las clases encapsuladas pueden ser reutilizadas sin afectar el resto del programa.

**Ejemplo de encapsulación en Python**

Vamos a crear un ejemplo simple de una clase que representa un Banco:
```python
class Banco:
    def __init__(self, nombre, ciudad):
        self.__nombre = nombre
        self.__ciudad = ciudad
        self.__clientes = []

    def agregar_cliente(self, cliente):
        self.__clientes.append(cliente)

    def mostrar_clientes(self):
        for cliente in self.__clientes:
            print(cliente.nombre)

# Creamos un objeto Banco
banco = Banco("Banco Nacional", "Ciudad Autónoma de Buenos Aires")

# Agregamos clientes al banco
banco.agregar_cliente(Clientes("Juan Pérez"))
banco.agregar_cliente(Clientes("María Gómez"))

# Mostramos los clientes del banco
banco.mostrar_clientes()
```
En este ejemplo, la clase `Banco` tiene tres atributos: `nombre`, `ciudad` y `clientes`. Estos atributos están encapsulados utilizando el símbolo de doble guion bajo (`__`) al principio del nombre. Esto indica que estos atributos son privados y solo se pueden acceder a través de métodos específicos.

El método `agregar_cliente` agrega un cliente al banco, mientras que el método `mostrar_clientes` muestra la lista de clientes del banco. Estos métodos están diseñados para interactuar con los objetos del banco sin necesidad de acceso directo a sus atributos privados.

**Acceso a los atributos encapsulados**

Aunque los atributos privados están encapsulados, podemos crear métodos públicos que permitan acceder y modificarlos. Por ejemplo:
```python
class Banco:
    # ...

    def get_nombre(self):
        return self.__nombre

    def set_nombre(self, nombre):
        self.__nombre = nombre

banco = Banco("Banco Nacional", "Ciudad Autónoma de Buenos Aires")
print(banco.get_nombre())  # Imprime "Banco Nacional"
banco.set_nombre("Banco Internacional")
print(banco.get_nombre())  # Imprime "Banco Internacional"
```
En este ejemplo, creamos dos métodos públicos: `get_nombre` y `set_nombre`. El método `get_nombre` devuelve el valor del atributo privado `nombre`, mientras que el método `set_nombre` permite modificarlo.

**Best Practices**

Al trabajar con encapsulación en Python, es importante tener en cuenta las siguientes best practices:

* **Utiliza atributos privados**: utiliza el símbolo de doble guion bajo (`__`) al principio del nombre de los atributos para indicar que son privados.
* **Crea métodos públicos**: crea métodos públicos que permitan acceder y modificar los atributos encapsulados.
* **Evita acceso directo**: evita acceder directamente a los atributos encapsulados, utilizando en su lugar métodos públicos para interactuar con ellos.

**Conclusión**

En este capítulo, hemos visto cómo la encapsulación es una característica fundamental de la programación orientada a objetos (POO). Al envolver los atributos y métodos de una clase dentro de un contenedor llamado objeto, se puede reducir el riesgo de modificación accidental o malintencionada, organizar el código en bloques lógicos y faciles de entender, y reutilizar las clases sin afectar el resto del programa.

Esperamos que este capítulo te haya ayudado a comprender mejor la encapsulación y cómo se aplica en Python. En el próximo capítulo, exploraremos otro tema importante de la POO: polimorfismo.