# Proyecto: Fundamentos de Programación Orientada a Objetos (POO) en Python

---

## 📋 DATOS DEL ESTUDIANTE

| Campo | Información |
|-------|-------------|
| **Autor** | Eduardo Zambrano |
| **Fecha** | 20 de febrero de 2026 |
| **Materia** | Programación Orientada a Objetos |
| **Profesor** | Nelson Castro |

---

## 📖 DESCRIPCIÓN GENERAL

Este repositorio contiene una colección de notebooks de Colaboratory que demuestran de manera práctica los **4 pilares fundamentales de la Programación Orientada a Objetos (POO)** utilizando Python.

Cada pilar está implementado en un notebook independiente con ejemplos interactivos, comentarios explicativos y demostraciones visuales que facilitan la comprensión de conceptos abstractos.


## 🎯 OBJETIVOS DEL PROYECTO

- Demostrar comprensión práctica de los pilares de POO
- Implementar ejemplos funcionales y comentados
- Preparar respuestas para las preguntas clave del profesor
- Documentar el proceso de aprendizaje y análisis personal



## 🧱 ESTRUCTURA DEL PROYECTO

📦 Fundamentos-POO-Python

- ├── 📓 Pilar 1 - Clases Objetos.ipynb.
- ├── 📓 Pilar 2 - Abstraccion Encapsulamiento.ipynb.
- ├── 📓 Pilar 3 - Herencia y Polimorfismo.ipynb.
- ├── 📓 Pilar 4 - Clases Abstractas.ipynb.
- └── 📄 README.md.

---
## 🧩 PILAR 1: CLASES Y OBJETOS
### 📁 Código: [`Pilar 1 - Clases Objetos`](Pilar_1_-_Clases_Objetos.ipynb)

### 🎮 Ejemplo Implementado: **Sistema de Estudiantes**
- Clase `Estudiante` con atributos: nombre, edad, carrera, nota
- Cálculo automático de resultado (aprobado/reprobado) según nota ≥ 65
- Lista estática que almacena todos los estudiantes creados

#### 🔍 Análisis Personal

**¿Qué entendí sobre la diferencia entre clase (estática) y objetos (en memoria)?**

La **clase** es como un "molde" o "plantilla" que define la estructura y comportamiento que tendrán los objetos. Existe **una sola vez en memoria** y contiene:
- La definición de atributos
- Los métodos (comportamientos)
- Las variables de clase (como `estudiante`)

Los **objetos** son las **instancias concretas** creadas a partir de ese molde. Cada objeto:
- Ocupa su **propio espacio en memoria** (ID único)
- Tiene sus **propios valores** para los atributos
- Puede comportarse de manera independiente

❓ Respuesta a Preguntas Clave

P: "Si tuvieras que crear 1,000 registros, ¿qué parte de tu código se mantiene estática y qué parte cambia en memoria?"

R:

    PARTE ESTÁTICA (1 sola vez en memoria):
        La definición de la clase Estudiante
        Todos los métodos (__init__, mostrar_info, presentarse)
        La variable de clase estudiantes (la lista que los contiene)
        Las constantes NOTA_MAXIMA y PORCENTAJE_APROBACION

    PARTE VARIABLE (1,000 copias en memoria):
        Los atributos de instancia de cada estudiante (nombre, edad, carrera, nota, resultado)
        Cada objeto ocupa su propio espacio con sus valores específicos

P: "¿Por qué definiste estos atributos aquí y no fuera del constructor?"

R: Los atributos como nombre, edad, carrera y nota se definen dentro del __init__ porque son atributos de instancia, lo que significa que:

    Deben inicializarse en el momento de creación del objeto
    Cada objeto necesita sus propios valores (no son compartidos)
    El constructor garantiza que todos los objetos tengan la misma estructura pero con valores diferentes
    Si los definiera fuera del constructor, serían atributos de clase (compartidos por todos los objetos), lo cual no tendría sentido porque cada estudiante debe tener su propio nombre y nota.

## 🧩 PILAR 2: ABSTRACCIÓN Y ENCAPSULAMIENTO
### 📁 Código: [`Pilar 2 - Abstraccion Encapsulamiento`](Pilar_2_-_Abstraccion_Encapsulamiento.ipynb)

### 🏦 Ejemplo Implementado: Cajero Automático
    Clase CuentaBancaria con atributos público, protegido y privado
    Getters y setters con @property para controlar acceso
    Validaciones en operaciones de depósito y retiro

#### 🔍 Análisis Personal

¿Por qué usé _variable y @property?

En Python, el encapsulamiento funciona por convención más que por imposición:

    Esto "_variable" (El guión bajo + el nombre de la variable): Indica "atributo protegido". Es una convención (un acuerdo) que le dice a otros programadores: "Esto es para uso interno, no lo modifiques directamente". Técnicamente se puede acceder, pero es mala práctica.

    Esto "__variable" (el doble guión bajo + el nombre de la variable): Activa el "name mangling" de Python. El intérprete renombra internamente la variable a _Clase__variable, haciéndola más difícil de acceder accidentalmente.

    @property: Permite crear getters y setters que parecen atributos pero tienen lógica de control. Ventajas:
        Validar datos antes de asignarlos (ej: saldo no negativo)
        Formatear la salida (ej: mostrar $1,000.00 en lugar de 1000.0)
        Mantener una interfaz limpia mientras se oculta la complejidad

❓ Respuesta a Preguntas Clave

P: "Veo que usaste _variable o __variable. ¿Qué intentas proteger y qué pasaría si un usuario de tu código cambia ese valor directamente desde fuera?"

R:
Con _saldo intento proteger que no se modifique el saldo sin pasar por las validaciones. Si un usuario hace cuenta._saldo = -500:

    ✅ Técnicamente funcionará (Python lo permite)
    ❌ Pero rompe la lógica de negocio (saldos negativos no deberían existir)
    ❌ Se saltaría las validaciones que protegen la integridad de los datos

Con __numero_cuenta es más estricto: si alguien intenta cuenta.__numero_cuenta, obtendrá un AttributeError porque Python ofuscó el nombre. Aunque aún se puede acceder con cuenta._CuentaBancaria__numero_cuenta, la doble barra indica "esto es realmente privado, no deberías tocarlo".

P: "¿Qué ventaja te da usar un decorador en lugar de acceder al atributo directamente?"

R: Usar @property me da control total sobre cómo se accede y modifica el atributo:

    Validación: El setter puede rechazar valores inválidos
    Formato: El getter puede mostrar los datos de manera más amigable
    Mantenibilidad: Si en el futuro necesito cambiar cómo se calcula el saldo, solo modifico el getter/setter, sin afectar el resto del código
    Consistencia: Garantizo que todas las modificaciones pasen por las mismas reglas de negocio

## 🧩 PILAR 3: HERENCIA Y POLIMORFISMO
### 📁 Código: [`Pilar 3 - Herencia y Polimorfismo`](`Pilar_3_-_Herencia_y_Polimorfismo.ipynb`)

### 💼 Ejemplo Implementado: Sistema de Nómina
    Clase "padre": Empleado
    Clases "hijas": EmpleadoTiempoCompleto, EmpleadoPorHoras, EmpleadoComision, EmpleadoRemoto
    Función polimórfica procesar_nomina() que funciona con cualquier tipo

#### 🔍 Análisis Personal

Herencia: Permite que las clases hijas reutilicen el código de la clase padre, evitando duplicación. Cada hija hereda los atributos y métodos base, pero puede:

    Añadir sus propios atributos específicos
    Sobrescribir métodos para cambiar su comportamiento

Polimorfismo: La capacidad de que objetos de diferentes clases respondan al mismo mensaje de formas distintas. En el código, la función procesar_nomina() recibe una lista de Empleado, pero cada uno ejecuta su propia versión de calcular_salario().
❓ Respuesta a Preguntas Clave

P: "Si mañana tengo que agregar un nuevo tipo de empleado, ¿tengo que reescribir tus funciones o tu código está listo para recibirlo?"

R: El código está listo para recibir nuevos tipos sin modificar lo existente (principio Abierto/Cerrado). Para agregar EmpleadoRemoto:

    Creé la nueva clase heredando de Empleado
    Implementé sus métodos específicos (calcular_salario, tipo_empleado)
    No toqué la función procesar_nomina() - sigue funcionando igual

Esto es posible gracias al polimorfismo: la función solo necesita saber que los objetos son Empleado y pueden responder a calcular_salario().

P: "Explícame cómo Python sabe qué método ejecutar aquí."

R: Python utiliza "Dynamic Dispatch" o "Late Binding". Cuando se ejecuta empleado.calcular_salario():

    Python mira el tipo real del objeto (no el tipo declarado)
    Busca el método en la clase del objeto
    Si lo encuentra, lo ejecuta; si no, busca en la clase padre

Esto sucede en tiempo de ejecución, no en compilación. Por eso aunque todos están en una lista de Empleado, cada uno ejecuta su versión específica.

## 🧩 PILAR 4: CLASES ABSTRACTAS
### 📁 Código: [`Pilar 4 - Clases Abstractas`](`Pilar_4_-_Clases_Abstractas.ipynb`)
### 🎮 Ejemplo Implementado: Videojuego de Personajes

    Clase abstracta Personaje con métodos @abstractmethod
    Clases concretas: Guerrero, Mago, Arquero (completas)
    Clases incompletas: Curandero, Demihumano (causan error)
    Demostración interactiva de errores en tiempo real

### 🔍 Análisis Personal

Una clase abstracta es como un contrato que dice: "Todo personaje en mi juego DEBE poder atacar y defender". Pero no dice cómo deben hacerlo, eso lo decide cada clase hija.

Características clave:

    No se puede instanciar directamente
    Define métodos abstractos que las hijas deben implementar
    Puede tener métodos concretos que todas las hijas comparten

❓ Respuesta a Preguntas Clave

P: "¿Por qué decidiste que esta clase fuera abstracta? ¿Qué pasaría si intento instanciarla?"

R: Hice Personaje abstracta porque:

    Garantiza que todos los personajes tengan ataque y defensa
    Obliga a los programadores a implementar estos métodos
    Evita crear personajes "incompletos" que romperían el juego

Si intento instanciar Personaje directamente:
python

p = Personaje("Test")  # ❌ TypeError!

Python lanza: TypeError: Can't instantiate abstract class Personaje with abstract methods atacar, defender

P: "Muéstrame el 'contrato' que obligas a cumplir a las clases hijas."

R: El contrato está definido por los métodos abstractos:
python

class Personaje(ABC):
    @abstractmethod
    def atacar(self):
        pass  # Las hijas deciden cómo
    
    @abstractmethod
    def defender(self, dano):
        pass  # Las hijas deciden cómo

Cualquier clase que herede de Personaje DEBE implementar estos dos métodos. Si no lo hace:
python

class Curandero(Personaje):
    def __init__(self, nombre):
        super().__init__(nombre)
    # ❌ FALTA atacar() y defender()
    
c = Curandero("Pedro")  # ❌ TypeError!

## 🛠️ TECNOLOGÍAS UTILIZADAS
Tecnología	Versión	Uso:
Python	3.9+	Lenguaje de programación principal
Colaboratory Notebook	6.4+	Entorno interactivo para ejecutar el código
GitHub	-	Control de versiones y alojamiento del repositorio
Markdown	-	Formato del README y documentación

## 📦 INSTALACIÓN Y USO
Requisitos previos

    Python 3.9 o superior
    Colaboratory Notebook

### Pasos para ejecutar

   1. Clonar el repositorio

bash

git clone https://github.com/tuusuario/Fundamentos-POO-Python.git
cd Fundamentos-POO-Python

    Instalar dependencias (si es necesario)

       - Pilar 1 - Clases Objetos.ipynb
       - Pilar 2 - Abstraccion Encapsulamiento.ipynb
       - Pilar 3 - Herencia Polimorfismo.ipynb
       - Pilar 4 - Clases Abstractas.ipynb

# 📊 CONCLUSIONES PERSONALES

Este proyecto me permitió comprender en profundidad los fundamentos de la POO:

  -  Clases y Objetos: Entendí la diferencia entre el molde (clase) y las instancias (objetos) en memoria.
  -  Abstracción/Encapsulamiento: Aprendí a proteger los datos y exponer solo lo necesario mediante getters/setters.
  -  Herencia/Polimorfismo: Descubrí cómo escribir código extensible que funciona con nuevos tipos sin modificaciones.
  -  Clases Abstractas: Comprendí la importancia de definir contratos que garanticen comportamientos mínimos.

La implementación práctica, especialmente el videojuego de personajes, hizo que conceptos abstractos fueran tangibles y divertidos de aprender.

### 📚 REFERENCIAS

   - Python Documentation - Classes
   - Real Python - Object - Oriented Programming in Python
   - PEP 8 – Style Guide for Python Code
   - Python abc module

#### **📬 CONTACTO**
  **Autor**:  Eduardo Zambrano
  **GitHub**: @Eduardoezi
  **Correo**: [eezambranois@gmail.com]

⭐ Si este proyecto te fue útil, ¡no olvides darle una estrella en GitHub! ⭐


