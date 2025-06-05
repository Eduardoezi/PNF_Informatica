# Unidad 1

Integrales
Definicines:- Integrales. - Derivadas. - Antiderivada.
Tipos de integral.
Metodos de Integracion
Reglas básicas de integración

## Resumiéndolo en conceptos clave:

✅ La derivada nos dice cómo cambia una función en cada punto. Representa la pendiente de la tangente en ese punto.

✅ La integral (o antiderivada) nos permite reconstruir la función original a partir de su tasa de cambio. También se usa para calcular el área bajo la curva.

✅ El Teorema Fundamental del Cálculo establece que la integración y la derivación son procesos inversos. Si tomas una función, la derivada te da su tasa de cambio, y la integral te devuelve la función original.

## Tipos de Integrales

### Integrales Indefinidas

- No tienen límites de integración.
- Se expresan con una constante de integración CC.
  - Ejemplo:
    - ∫(2x+3) dx=x2+3x+C\int (2x + 3) \, dx = x^2 + 3x + C

### Integrales Definidas

- Tienen límites de integración aa y bb.
- Dan un valor numérico, no una función.
- Se resuelven con el Teorema Fundamental del Cálculo.
  - Ejemplo:
    -∫14(x2) dx\int_{1}^{4} (x^2) \, dx

### Integrales Impropias

- Si el intervalo es infinito (por ejemplo, de x=1x = 1 a x=∞x = \infty).
- O si hay una discontinuidad en el integrando.
- Se evalúan con límites matemáticos.
  - Ejemplo:
    - ∫1∞1x dx\int_{1}^{\infty} \frac{1}{x} \, dx

### Integrales de Línea

- Se evalúan sobre una curva en el espacio.
- Se usan en física y ingeniería para calcular trabajo, energía, etc.
  - Ejemplo:
    - ∫Cf(x,y) ds\int_{C} f(x,y) \, ds

### Integrales de Superficie

- Se calculan sobre una superficie en el espacio en lugar de una línea.
- Útiles en electromagnetismo, flujos de fluidos, etc.
  - Ejemplo:
    - ∬Sf(x,y,z) dS\iint_{S} f(x,y,z) \, dS

### Integrales Múltiples

- Se evalúan en varias dimensiones.
- Integral doble: Para áreas en 2D.
- Integral triple: Para volúmenes en 3D.
  - Ejemplo:
    - ∫02∫03(x+y) dx dy\int_{0}^{2} \int_{0}^{3} (x+y) \, dx \, dy

### Integrales Trigonométricas

- Contienen funciones trigonométricas como sen(x), cos(x).
- Se resuelven con identidades trigonométricas o sustituciones.
  - Ejemplo:
    - ∫sin⁡xcos⁡x dx\int \sin x \cos x \, dx

**Cada tipo tiene su propia estrategia de solución, dependiendo de lo que necesites calcular.**

## Metodos de Integracion

### 🔹 1. Sustitución o Cambio de Variable

- 📌 Definición: Este método transforma una integral difícil en una más sencilla al introducir una nueva variable uu para reemplazar parte del integrando.

- 📌 Reglas fundamentales:
  - Escoger una parte del integrando para sustituir con uu.
  - Derivar uu para encontrar dudu.
  - Expresar la integral completamente en términos de uu y resolverla.
  - Volver a la variable original al final.

- 📌 Tipos de sustitución:
  - ✔ Sustitución simple: Cuando el integrando contiene una función compuesta, como (x2+1)5(x^2 + 1)^5.
  - ✔ Sustitución trigonométrica: Cuando hay raíces o expresiones como 1−x2\sqrt{1 - x^2}.
  - ✔ Sustitución logarítmica: Cuando hay expresiones como 1x\frac{1}{x}.

### 🔹 2. Integración por Partes

- 📌 Definición: Se usa cuando la integral involucra un producto de funciones y no se puede resolver directamente. Se basa en la fórmula:

∫u dv=uv−∫v du\int u \, dv = uv - \int v \, du

- 📌 Reglas fundamentales:

  - Elegir uu y dvdv correctamente (normalmente uu es la función más fácil de derivar).
  - Derivar uu para obtener dudu.
  - Integrar dvdv para obtener vv.
  - Aplicar la fórmula y resolver la integral restante.

- 📌 Tipos de integración por partes:
  - ✔ Funciones algebraicas y exponenciales: Como xexx e^x.
  - ✔ Funciones algebraicas y logarítmicas: Como xln⁡xx \ln x.
  - ✔ Funciones trigonométricas: Como xcos⁡xx \cos x.

### 🔹 3. Integrales Racionales

- 📌 Definición: Son integrales donde el integrando es un cociente de polinomios. Se resuelven descomponiendo la expresión en fracciones parciales o utilizando sustitución adecuada.

- 📌 Reglas fundamentales:
  - Si el denominador es factorizable, se usa fracciones parciales.
  - Si el denominador es irreducible, se usa completar cuadrado o sustituciones trigonométricas.
  - Si el grado del numerador es mayor o igual al denominador, se usa división polinómica antes de integrar.

- 📌 Tipos de integrales racionales:
  - ✔ Con raíces simples en el denominador → Se pueden resolver con fracciones parciales.
  - ✔ Con raíces cuadráticas irreducibles → Se usa completar cuadrado o sustitución trigonométrica.
  - ✔ Propias e impropias → Dependen de la relación entre numerador y denominador.

### Reglas Basicas de Integración
  
#### 🔹 1. Regla de la Potencia

- 📌 Definición: Se usa para integrar expresiones de la forma xnx^n, donde nn es un número real distinto de −1-1.

- 📌 Fórmula:
  - ∫xn dx=xn+1n+1+C,n≠−1\int x^n \,dx = \frac{x^{n+1}}{n+1} + C, \quad n \neq -1
- 📌 Características:
  - ✔ Aplica a funciones de potencia, como x3x^3, x1/2x^{1/2}, etc.
  - ✔ Se suma 1 al exponente y se divide por el nuevo exponente.
  - ✔ No es válida para x−1x^{-1} (que requiere la regla del logaritmo).

- 📌 Consideraciones: 
  - ❗Si n=−1n = -1, no se puede aplicar esta regla, y en su lugar se usa:
  - ∫1x dx=ln⁡∣x∣+C\int \frac{1}{x} \,dx = \ln |x| + C
    - 📌 Ejemplo:
    - ∫x4 dx=x55+C\int x^4 \,dx = \frac{x^5}{5} + C

#### 🔹 2. Regla de la Suma y Diferencia

- 📌 Definición: Permite separar integrales que contienen suma o resta de funciones y resolver cada término por separado.

- 📌 Fórmula:

  - ∫(f(x)±g(x)) dx=∫f(x) dx±∫g(x) dx\int (f(x) \pm g(x)) \, dx = \int f(x) \,dx \pm \int g(x) \,dx
- 📌 Características:
  - ✔ Se aplica cuando hay varios términos sumándose o restándose.
  - ✔ Se integran cada uno por separado y luego se combinan los resultados.

- 📌 Consideraciones: ❗ No se puede distribuir la integral en el caso de un producto de funciones (para eso se usa integración por partes).

  - 📌 Ejemplo:
    - ∫(x2+3x−5) dx=x33+3x22−5x+C\int (x^2 + 3x - 5) \,dx = \frac{x^3}{3} + \frac{3x^2}{2} - 5x + C

#### 🔹 3. Regla de la Constante

- 📌 Definición: Si una constante kk multiplica a una función, se puede sacar fuera de la integral y multiplicar al resultado final.

- 📌 Fórmula:

  - ∫kf(x) dx=k∫f(x) dx\int k f(x) \, dx = k \int f(x) \,dx
- 📌 Características: ✔ Facilita el cálculo sacando la constante antes de integrar. ✔ No cambia la estructura de la función, solo simplifica el proceso.
  - 📌 Ejemplo:
    - ∫7x2 dx=7∫x2 dx=7×x33=7x33+C\int 7x^2 \,dx = 7 \int x^2 \,dx = 7 \times \frac{x^3}{3} = \frac{7x^3}{3} + C

#### 🔹 4. Regla para la Integral de una Constante

- 📌 Definición: Si el integrando es solo una constante kk sin xx, el resultado será esa constante multiplicada por la variable independiente.

- 📌 Fórmula:
  - ∫k dx=kx+C\int k \,dx = kx + C
    - 📌 Ejemplo:
      - ∫5 dx=5x+C\int 5 \,dx = 5x + C

#### 🔹 5. Regla para la Integral de exe^x

- 📌 Definición: La función exponencial exe^x se mantiene igual al integrar.

- 📌 Fórmula:
  - ∫ex dx=ex+C\int e^x \,dx = e^x + C
- 📌 Consideraciones:
  - ❗ Si el exponente es más complejo, se usa sustitución.
    - 📌 Ejemplo:
      - ∫e3x dx=13e3x+C\int e^{3x} \,dx = \frac{1}{3} e^{3x} + C

#### 🔹 6. Regla para la Integral en Integrales Definidas

- 📌 Definición: En una integral definida, si usamos sustitución, los límites de integración también deben cambiar.
- 📌 Fórmula:
  - ∫abf(x) dx\int_{a}^{b} f(x) \, dx
  - Si usamos u=g(x)u = g(x), los nuevos límites serán u(a)u(a) y u(b)u(b).
    - 📌 Ejemplo: Si queremos integrar:
      - ∫14(2x) dx\int_1^4 (2x) \, dx
      - Usamos u=x2u = x^2, entonces los límites cambian:
      - Cuando x=1x = 1, u=12=1u = 1^2 = 1.
      - Cuando x=4x = 4, u=42=16u = 4^2 = 16.
      - La nueva integral será:
      - ∫1162 du\int_{1}^{16} 2 \, du

### 📌 Resumen visual de reglas básicas

|Regla               |Fórmula                  |Cuándo usarla       |
|--------------------|-------------------------|--------------------|
|📌 Potencia            |∫xn dx=xn+1n+1+C\int x^n \,dx = \frac{x^{n+1}}{n+1} + C|Siempre que xx tenga un exponente|
|📌 Suma y diferencia|∫(f±g) dx=∫f dx±∫g dx\int (f \pm g) \,dx = \int f \,dx \pm \int g \,dx|Cuando haya términos sumándose/restándose|
|📌 Constante multiplicando|∫kf(x) dx=k∫f(x) dx\int k f(x) \, dx = k \int f(x) \,dx|Para simplificar cuando hay constantes|
|📌 Integral de una constante|∫k dx=kx+C\int k \,dx = kx + C|Cuando el integrando es solo un número|
|📌 Exponencial    |exe^x, ∫ex dx=ex+C\int e^x \,dx = e^x + C|Cuando la función tiene exe^x|
|📌 Integrales definidas|Cambiar límites si hay sustitución|En integrales con límites a,ba, b|
