**Estructuras de Datos Avanzadas: Pilas y Colas**

En el capítulo anterior, abordamos los conceptos básicos de pilas y colas en Python. En este capítulo, profundizaremos en los aspectos más avanzados de estas estructuras de datos, explorando sus aplicaciones prácticas y optimizaciones para su uso efectivo.

**Definición y Concepto**

Una pila (stack) es una estructura de datos que sigue el principio de "LIFO" (Last In, First Out), lo que significa que el último elemento agregado a la pila es el primero en ser eliminado. En otras palabras, cuando se agrega un elemento a una pila, se coloca en el tope de la pila, y cuando se elimina un elemento, se extrae del tope de la pila.

Por otro lado, una cola (queue) es una estructura de datos que sigue el principio de "FIFO" (First In, First Out), lo que significa que el primer elemento agregado a la cola es el primero en ser eliminado. En otras palabras, cuando se agrega un elemento a una cola, se coloca al final de la cola, y cuando se elimina un elemento, se extrae del principio de la cola.

**Implementación en Python**

En Python, podemos implementar pilas y colas utilizando listas o clases personalizadas. A continuación, veremos ejemplos de cómo hacerlo:

**Pila**
```python
class Pila:
    def __init__(self):
        self.elementos = []

    def push(self, elemento):
        self.elementos.append(elemento)

    def pop(self):
        if not self.elementos:
            raise ValueError("La pila está vacía")
        return self.elementos.pop()

    def tamaño(self):
        return len(self.elementos)
```
**Cola**
```python
class Cola:
    def __init__(self):
        self.elementos = []

    def enqueue(self, elemento):
        self.elementos.append(elemento)

    def dequeue(self):
        if not self.elementos:
            raise ValueError("La cola está vacía")
        return self.elementos.pop(0)

    def tamaño(self):
        return len(self.elementos)
```
**Ejemplos y Aplicaciones**

A continuación, veremos algunos ejemplos y aplicaciones prácticas de pilas y colas:

**Ejemplo 1: Evaluador de expresiones**
```python
pila = Pila()

def evaluar_expresion(expresion):
    for caracter in expresion:
        if caracter == '(':
            pila.push(caracter)
        elif caracter == ')':
            if not pila.tamaño():
                raise ValueError("La expresión no está bien formada")
            pila.pop()
    return pila.tamaño() > 0

print(evaluar_expresion("(2+3)*4"))  # True
print(evaluar_expresion("((2+3)*4)"))  # False
```
En este ejemplo, utilizamos una pila para evaluar la expresión matemática. La idea es que cada vez que se encuentra un paréntesis izquierdo, se agrega a la pila, y cuando se encuentra un paréntesis derecho, se elimina de la pila. Al final, si la pila no está vacía, significa que hay paréntesis abiertos sin cerrar, por lo que la expresión no está bien formada.

**Ejemplo 2: Servidor de cola**
```python
cola = Cola()

def procesar_mensaje(mensaje):
    cola.enqueue(mensaje)
    while cola.tamaño() > 0:
        mensaje = cola.dequeue()
        print(f"Procesando mensaje {mensaje}")

procesar_mensaje("Hola")
procesar_mensaje("Mundo")
procesar_mensaje("!")
```
En este ejemplo, utilizamos una cola para procesar mensajes. La idea es que cada vez que se recibe un nuevo mensaje, se agrega a la cola, y luego se procesa los mensajes en orden de llegada.

**Optimización**

A continuación, veremos algunas formas de optimizar el uso de pilas y colas:

**Pila**
```python
class Pila:
    def __init__(self):
        self.elementos = []

    def push(self, elemento):
        if not isinstance(elemento, type(self.elementos[0])):
            raise TypeError("Todos los elementos deben ser del mismo tipo")
        self.elementos.append(elemento)

    def pop(self):
        if not self.elementos:
            raise ValueError("La pila está vacía")
        return self.elementos.pop()

    def tamaño(self):
        return len(self.elementos)
```
En este ejemplo, agregamos una comprobación para asegurarnos de que todos los elementos en la pila sean del mismo tipo.

**Cola**
```python
class Cola:
    def __init__(self):
        self.elementos = []

    def enqueue(self, elemento):
        if not isinstance(elemento, type(self.elementos[0])):
            raise TypeError("Todos los elementos deben ser del mismo tipo")
        self.elementos.append(elemento)

    def dequeue(self):
        if not self.elementos:
            raise ValueError("La cola está vacía")
        return self.elementos.pop(0)

    def tamaño(self):
        return len(self.elementos)
```
En este ejemplo, también agregamos una comprobación para asegurarnos de que todos los elementos en la cola sean del mismo tipo.

**Conclusiones**

En conclusión, pilas y colas son estructuras de datos fundamentales en programación, y su comprensión es crucial para desarrollar aplicaciones efectivas. En este capítulo, hemos profundizado en los conceptos básicos de pilas y colas, y hemos explorado formas de implementarlas en Python utilizando listas o clases personalizadas. También hemos visto ejemplos prácticos de cómo utilizar pilas y colas para resolver problemas complejos. Al final, hemos agregado algunas formas de optimizar el uso de estas estructuras de datos.

**Ejercicio**

1. Implementa una pila que utilice un objeto `llamada` con los atributos `nombre`, `apellido` y `edad`.
2. Crea una cola que utilice un objeto `Mensaje` con los atributos `texto` y `prioridad`.
3. Desarrolla un programa que simule un sistema de gestión de tareas, utilizando una cola para almacenar las tareas y una pila para almacenar las prioridades.
4. Implementa un método `ordenar` que ordena la pila por prioridad.

**Siguiente Capítulo**

En el próximo capítulo, exploraremos otros tipos de estructuras de datos avanzados, como árboles y grafos. Estas estructuras de datos son fundamentales para resolver problemas complejos en programación y pueden ser utilizadas en una variedad de aplicaciones prácticas.

**Resumen**

En este capítulo, hemos abordado los conceptos básicos de pilas y colas en Python, incluyendo su implementación utilizando listas o clases personalizadas. También hemos explorado ejemplos prácticos de cómo utilizar pilas y colas para resolver problemas complejos y hemos agregado algunas formas de optimizar el uso de estas estructuras de datos. En el próximo capítulo, exploraremos otros tipos de estructuras de datos avanzados.