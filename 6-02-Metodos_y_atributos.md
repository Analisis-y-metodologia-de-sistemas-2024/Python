**Capítulo 3: Métodos y Atributos**

En el capítulo anterior, abordamos el tema de clases y objetos, destacando su importancia en la programación orientada a objetos. Ahora, vamos a profundizar en uno de los aspectos más importantes de este paradigma: los métodos y atributos.

**Métodos**

Un método es una función que se encuentra dentro de una clase y puede acceder y modificar los atributos de esa clase. Los métodos se utilizan para definir el comportamiento de un objeto, es decir, lo que puede hacer o qué acciones puede realizar. Hay varios tipos de métodos:

1. **Método constructor**: Es el método que se llama automáticamente cuando se crea un nuevo objeto. Se utiliza para inicializar los atributos del objeto.
2. **Método de instancia**: Es el método que se llama sobre un objeto específico y puede acceder a sus atributos.
3. **Método estático**: Es el método que se llama sin necesidad de crear un objeto y no puede acceder a los atributos de la clase.

En Python, los métodos se definen utilizando la palabra clave `def` seguida del nombre del método y paréntesis para recibir argumentos. Por ejemplo:
```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def saludar(self):
        print(f"Hola, me llamo {self.nombre} y tengo {self.edad} años.")

    @staticmethod
    def saludar_estático():
        print("Hola, soy un método estático.")
```
En este ejemplo, la clase `Persona` tiene un constructor que inicializa los atributos `nombre` y `edad`, un método de instancia `saludar` que imprime un mensaje saludo y un método estático `saludar_estático` que también imprime un mensaje.

**Atributos**

Un atributo es una variable que se encuentra dentro de una clase y se utiliza para almacenar información sobre los objetos de esa clase. Los atributos pueden ser:

1. **Atributo de instancia**: Es el atributo que se encuentra en cada objeto individual y puede variar entre ellos.
2. **Atributo estático**: Es el atributo que se encuentra en la clase y no varía entre objetos.

En Python, los atributos se definen utilizando la sintaxis `self.nombre = valor`. Por ejemplo:
```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def saludar(self):
        print(f"Hola, me llamo {self.nombre} y tengo {self.edad} años.")
```
En este ejemplo, la clase `Persona` tiene dos atributos de instancia: `nombre` y `edad`, que se inicializan en el constructor.

**Relación entre métodos y atributos**

Los métodos y los atributos están estrechamente relacionados en la programación orientada a objetos. Los métodos pueden acceder y modificar los atributos de una clase, lo que les permite realizar acciones específicas. Por ejemplo:
```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def saludar(self):
        print(f"Hola, me llamo {self.nombre} y tengo {self.edad} años.")

p1 = Persona("Juan", 30)
p2 = Persona("Maria", 25)

p1.saludar()  # Imprime "Hola, me llamo Juan y tengo 30 años."
p2.saludar()  # Imprime "Hola, me llamo Maria y tengo 25 años."
```
En este ejemplo, el método `saludar` del objeto `Persona` accede a los atributos `nombre` y `edad` de la clase para imprimir un mensaje saludo.

**Ejemplos prácticos**

Vamos a ver algunos ejemplos prácticos que ilustran la relación entre métodos y atributos:

1. **Caja registradora**: Una caja registradora tiene métodos como "agregar_item" que agrega un producto al carrito de compras, "eliminar_item" que elimina un producto del carrito y "mostrar_carrito" que muestra el contenido del carrito.
2. **Automóvil**: Un automóvil tiene atributos como "marca", "modelo" y "año", y métodos como "arrancar" que arranca el motor, "frenar" que aplica los frenos y "cambiar_velocidad" que cambia la velocidad.
3. **Persona**: Una persona tiene atributos como "nombre", "edad" y "direccion", y métodos como "saludar" que imprime un mensaje saludo, "caminar" que simula el movimiento de caminar y "correr" que simula el movimiento de correr.

En conclusión, los métodos y atributos son fundamentales en la programación orientada a objetos. Los métodos definen el comportamiento de los objetos, mientras que los atributos almacenan información sobre ellos. La relación entre ambos es estrecha, ya que los métodos pueden acceder y modificar los atributos para realizar acciones específicas.

**Ejercicio**

Crea una clase `Vehículo` con los siguientes métodos:

* `arrancar`: arranca el motor del vehículo
* `frenar`: aplica los frenos del vehículo
* `cambiar_velocidad`: cambia la velocidad del vehículo

Y atributos:

* `marca`
* `modelo`
* `año`

Luego, crea dos objetos `Vehículo` y llama a cada método para ver cómo se comportan.

**Solución**

A continuación, te presento una posible solución al ejercicio:
```python
class Vehículo:
    def __init__(self, marca, modelo, año):
        self.marca = marca
        self.modelo = modelo
        self.año = año

    def arrancar(self):
        print(f"El {self.marca} {self.modelo} de {self.año} está arrancando.")

    def frenar(self):
        print("Se están aplicando los frenos del vehículo.")

    def cambiar_velocidad(self, velocidad):
        print(f"La velocidad del vehículo es ahora de {velocidad} km/h.")

# Creación de objetos Vehículo
vehículo1 = Vehículo("Toyota", "Corolla", 2015)
vehículo2 = Vehículo("Ford", "Fiesta", 2018)

# Llamado a métodos
vehículo1.arrancar()  # Imprime "El Toyota Corolla de 2015 está arrancando."
vehículo2.frenar()  # Imprime "Se están aplicando los frenos del vehículo."
vehículo1.cambiar_velocidad(120)  # Imprime "La velocidad del vehículo es ahora de 120 km/h."
```
Espero que esto te haya ayudado a entender mejor el tema de métodos y atributos en la programación orientada a objetos. ¡Si tienes alguna pregunta o necesitas más ayuda, no dudes en preguntar!