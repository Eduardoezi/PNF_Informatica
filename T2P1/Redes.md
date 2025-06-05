# Fundamentos Básicos de Redes

Las redes son la columna vertebral de la comunicación digital hoy en día, permitiendo que la información viaje por todo el mundo. Entender sus fundamentos es crucial en nuestro día a día, dado que estamos rodeados de sistemas interconectados.

## Concepto de Redes

En esencia, una red es un conjunto de dispositivos interconectados que comparten recursos e intercambian información. Piensa en tu casa: tienes tu teléfono, tu computadora, tu televisor inteligente, y todos ellos pueden conectarse a internet a través de tu router. Esa es una red doméstica. A una escala mucho mayor, internet es una red global masiva. Elementos Clave de una Red Para que la comunicación funcione en una red, deben existir ciertos elementos:

- **Emisor:** Es el origen del mensaje, el dispositivo o persona que inicia la comunicación. Por ejemplo, cuando envías un correo electrónico, tú eres el emisor.

- **Mensaje:** Es la información que se va a transmitir. Puede ser texto, imágenes, video, audio, etc.

- **Medio:** Es el canal físico a través del cual viaja el mensaje. Los medios pueden ser
cables, ondas de radio, fibra óptica, etc.

- **Receptor:** Es el destino del mensaje, el dispositivo o persona que lo recibe. Siguiendo el ejemplo anterior, la persona que recibe tu correo electrónico es el receptor. Medios de Comunicación Los medios de comunicación en redes se dividen en dos categorías principales:

### **Medios Alámbricos (Guiados):** Estos medios utilizan un conducto físico para guiar la señal. Algunos ejemplos incluyen

- **Cables de par trenzado:** Comunes en redes Ethernet para conectar
computadoras y routers.
- **Cables coaxiales:** Utilizados tradicionalmente para televisión por cable e internet de banda ancha.
- **Fibra óptica:** Transmite datos usando pulsos de luz, ofreciendo velocidades mucho mayores y distancias más largas, ideal para infraestructuras de internet.

### **Medios Inalámbricos (No Guiados):** Estos medios transmiten datos a través del aire mediante ondas electromagnéticas, sin necesidad de un conductor físico. Ejemplos comunes son

- **Wi-Fi:** Permite la conexión inalámbrica de dispositivos a una red local.
- **Bluetooth:** Usado para conexiones de corto alcance entre dispositivos, como auriculares y teléfonos.
- **Ondas de radio:** Utilizadas en tecnologías como 4G, 5G y comunicación satelital.

## Transmisión de Datos

La transmisión de datos se refiere a cómo la información viaja de un punto a otro.

- **Unidades de Transmisión:** Los datos se miden en bits (la unidad más pequeña de información, un 0 o un 1). Grupos de bits forman bytes (8 bits), y las velocidades de transmisión se expresan comúnmente en bits por segundo (bps), kilobits por segundo (Kbps), megabits por segundo (Mbps), etc.

### **Formas de Transmisión:**

  ○ Transmisión Serie: Los bits se envían uno tras otro por un único canal. Es más lenta, pero requiere menos cables y es más común para la comunicación a largas distancias (por ejemplo, puertos USB, Ethernet).

  ○ Transmisión Paralelo: Múltiples bits se envían simultáneamente a través de varios canales paralelos. Es más rápida para distancias cortas, pero requiere más cables y es más propensa a errores por desincronización (por ejemplo, algunas impresoras antiguas).

### Modos de Transmisión de Datos: Los modos de transmisión definen la dirección y el flujo de la comunicación entre dos dispositivos

- Simplex: La comunicación ocurre en una sola dirección, de forma unidireccional. Un ejemplo clásico es la transmisión de radio o televisión, donde la señal solo va del emisor a los receptores.
- Half-Duplex (Semi-dúplex): La comunicación puede ocurrir en ambas direcciones, pero no simultáneamente. Los dispositivos deben turnarse para enviar y recibir. Un buen ejemplo es un walkie-talkie, donde solo una persona puede hablar a la vez.
- Full-Duplex (Dúplex completo): La comunicación puede ocurrir en ambas direcciones simultáneamente. Tanto el emisor como el receptor pueden enviar y recibir datos al mismo tiempo. Las llamadas telefónicas y la mayoría de las conexiones a internet son ejemplos de comunicación full-duplex.

### Dirección IP, Estructura, Clases y Máscara de Red

La Dirección IP (Protocolo de Internet) es un identificador numérico único asignado a cada dispositivo conectado a una red que utiliza el Protocolo de Internet para la comunicación. Es como la dirección postal de tu casa en el mundo digital, permitiendo que los paquetes de datos
lleguen a su destino correcto.

#### Estructura de la Dirección IP (IPv4)

Las direcciones IPv4 (la versión más común actualmente) constan de 32 bits, que se representan como cuatro números decimales separados por puntos, cada número variando de 0 a 255. A cada uno de estos números se le conoce como octeto. Por ejemplo: 192.168.1.10.
Cada dirección IP se divide en dos partes:

- Parte de Red (Network ID): Identifica la red a la que pertenece el dispositivo. Todos los dispositivos en la misma red comparten el mismo ID de red.

- Parte de Host (Host ID): Identifica un dispositivo específico dentro de esa red.

#### **Clases de Direcciones IP**

Originalmente, las direcciones IP se dividieron en clases para organizar y asignar rangos de direcciones. Aunque hoy en día se usa más el enrutamiento sin clases (CIDR), entender las clases básicas es fundamental:

- Clase A: Las direcciones comienzan con un número entre 1 y 126. El primer octeto define la red, y los tres octetos restantes definen los hosts. Diseñada para redes muy grandes.

  - Rango: 1.0.0.0 a 126.255.255.255

- Clase B: Las direcciones comienzan con un número entre 128 y 191. Los dos primeros
octetos definen la red, y los dos restantes definen los hosts. Diseñada para redes de
tamaño mediano a grande.

  - Rango: 128.0.0.0 a 191.255.255.255

- Clase C: Las direcciones comienzan con un número entre 192 y 223. Los tres primeros octetos definen la red, y el último octeto define los hosts. Diseñada para redes pequeñas.

  - Rango: 192.0.0.0 a 223.255.255.255

- Clase D: (224.0.0.0 a 239.255.255.255): Utilizadas para multicast, donde un paquete es enviado a un grupo de dispositivos simultáneamente.

- Clase E: (240.0.0.0 a 255.255.255.255): Reservadas para investigación y desarrollo.

#### Máscara de Red (Subnet Mask)

La máscara de red es un número de 32 bits que se utiliza junto con la dirección IP para determinar qué parte de la dirección IP corresponde al ID de red y cuál corresponde al ID de host. Se representa de la misma manera que una dirección IP (por ejemplo, 255.255.255.0).

En la máscara de red, los bits que están a 1 (unos) indican la parte de la dirección IP que es el ID de red, y los bits que están a 0 (ceros) indican la parte que es el ID de host.
**Por ejemplo:**

- Si tienes una dirección IP 192.168.1.10 y una máscara de red 255.255.255.0:
  - La máscara 255.255.255.0 en binario es 11111111.11111111.11111111.00000000.
  - Esto significa que los primeros tres octetos de la dirección IP (192.168.1) son la
parte de la red, y el último octeto (10) es la parte del host.

La máscara de red permite a los dispositivos determinar si un paquete de datos está destinado a un dispositivo dentro de su propia red local o si debe enviarse a través de un router a otra red.

Comprender estos fundamentos es el primer paso para dominar el fascinante mundo de las redes informáticas.

## Líneas de Comunicación

Las líneas de comunicación son los canales físicos o lógicos a través de los cuales la información viaja de un punto a otro. Su objetivo principal es facilitar el intercambio de datos entre dispositivos, permitiendo la comunicación efectiva en redes y sistemas. Sus funciones incluyen

- Transmisión de datos: Mover la información de origen a destino.
- Sincronización: Asegurar que el emisor y el receptor estén en el mismo "ritmo" para interpretar correctamente los datos.
- Control de flujo: Regular la cantidad de datos transmitidos para evitar la saturación del receptor.
- Detección y corrección de errores: Identificar y, en lo posible, reparar los errores que puedan ocurrir durante la transmisión.

- ### Se clasifican de varias formas

  - Conmutadas: Establecen una conexión temporal entre dos puntos solo cuando es necesario (ej. una llamada telefónica tradicional).
  - Dedicadas: Mantienen una conexión permanente y exclusiva entre dos puntos (ej. una línea arrendada entre dos sucursales).
  - Punto a punto: Conectan directamente dos dispositivos o nodos.
  - Multipunto: Permiten que un dispositivo se comunique con varios otros simultáneamente a través de un mismo canal compartido.
  - Digitales: Transmiten información en formato digital (bits), lo que ofrece mayor velocidad, eficiencia y resistencia al ruido en comparación con las analógicas.

## Medios de Conexión de Redes

Los medios de conexión de redes son los soportes físicos por los cuales se transmiten los datos en una red. Su objetivo es proporcionar la infraestructura necesaria para que la información fluya entre los diferentes componentes de la red. Sus funciones incluyen

- Transporte de señales: Conducir las señales eléctricas, ópticas o electromagnéticas que representan los datos.
- Interconexión de dispositivos: Enlazar computadoras, servidores, impresoras y otros dispositivos de red.
- Determinación del ancho de banda: Influir en la velocidad máxima a la que los datos pueden ser transmitidos.

### Tipos de Medios: Los principales tipos de medios utilizados en las redes

- Cobre:
  - Cables de par trenzado (Twisted Pair): Son los más comunes. Consisten en pares de hilos de cobre trenzados para reducir la interferencia electromagnética.
  - UTP (Unshielded Twisted Pair - Par Trenzado No Apantallado): No tienen un blindaje adicional. Son económicos y ampliamente usados en redes locales.

  - STP (Shielded Twisted Pair - Par Trenzado Apantallado): Incorporan un blindaje metálico alrededor de los pares trenzados o individualmente, ofreciendo mayor protección contra el ruido e interferencia, pero son más costosos y rígidos.

  - Fibra Óptica: Transmite datos mediante pulsos de luz a través de finos hilos de vidrio o plástico. Ofrece velocidades extremadamente altas, gran ancho de banda y es inmune a la interferencia lectromagnética, ideal para largas distancias y entornos de alta demanda.

    - Conectores: Para interconectar los cables a los dispositivos de red, se utilizan conectores específicos

      - Jack: Generalmente se refiere a los conectores hembra en dispositivos de red, como los puertos Ethernet en computadoras o switches, donde se inserta el conector RJ45.
      - RJ45 (Registered Jack 45): Es el conector más común para cables de red Ethernet de par trenzado. Tiene 8 pines y se utiliza para conectar dispositivos como computadoras, routers, switches y módems.
  - Implementación del Cableado con RJ45: Directos y cruzados El cableado de red con conectores RJ45 sigue estándares para asegurar la compatibilidad y el correcto funcionamiento. Los más comunes son los estándares EIA/TIA 568A y 568B, que especifican el orden de los hilos dentro del conector.

    - Cable Directo (Straight-Through): Se utiliza para conectar dispositivos de diferente tipo (ej. una computadora a un switch o router). En un cable directo, ambos extremos del cable (ambos conectores RJ45) están cableados con el mismo estándar (o 568A en ambos lados, o 568B en ambos lados). El orden de los colores de los hilos es idéntico en ambos extremos.
      - Estándar EIA/TIA 568B (más común):
        1. Blanco/Naranja
        2. Naranja
        3. Blanco/Verde
        4. Azul
        5. Blanco/Azul
        6. Verde
        7. Blanco/Marrón
        8. Marrón

    - Cable Cruzado (Crossover): Se utiliza para conectar dispositivos del mismo tipo (ej. dos computadoras directamente, o dos switches). En un cable cruzado, un extremo está cableado con el estándar 568A y el otro extremo con el estándar 568B. Esto "cruza" los hilos de transmisión y recepción, permitiendo que un dispositivo transmita y el otro reciba correctamente.

      - Extremo 1 (568A):
        1. Blanco/Verde
        2. Verde
        3. Blanco/Naranja
        4. Azul
        5. Blanco/Azul
        6. Naranja
        7. Blanco/Marrón
        8. Marrón
      - Extremo 2 (568B):
        1. Blanco/Naranja
        2. Naranja
        3. Blanco/Verde
        4. Azul
        5. Blanco/Azul
        6. Verde
        7. Blanco/Marrón
        8. Marrón

- Inalámbrica: Utiliza ondas de radio, microondas o infrarrojos para la transmisión de datos sin necesidad de cables. Proporciona flexibilidad y movilidad, pero puede ser susceptible a interferencias y tener un alcance limitado dependiendo de la tecnología.

### Especificaciones de Cables: Las especificaciones de los cables de red son cruciales para el rendimiento y la fiabilidad de la comunicación

- Velocidad: Es la capacidad del cable para transmitir datos en un determinado período, generalmente medida en megabits por segundo (Mbps) o gigabits por segundo (Gbps). La velocidad soportada depende de la categoría del cable (ej. Cat 5e, Cat 6, Cat 6a, Cat 7), su construcción y la tecnología de red utilizada.

  - Problemas Inherentes:
    - Ruidos (Noise): Son señales eléctricas no deseadas que pueden interferir con la señal de datos, distorsionándola y causando errores. Pueden ser generados por motores, líneas eléctricas o dispositivos electrónicos cercanos.
    - Atenuación (Attenuation): Es la pérdida de fuerza de la señal a medida que viaja a través del cable. Cuanto mayor es la distancia, mayor es la atenuación, lo que puede limitar el alcance efectivo del cable.
    - Diafonía (Crosstalk): Es la interferencia causada por las señales de un par de hilos adyacentes en un cable de par trenzado que se "filtran" a otro par. Reduce la integridad de la señal y es mitigada eficazmente por el trenzado de los hilos y el blindaje (en cables STP).
