**🧪 CPS Lab10 - Pruebas Unitarias con JUnit 5 y Log4J**
Proyecto desarrollado como parte del Laboratorio N°10 del curso Construcción y Pruebas de Software en Tecsup.
📋 Descripción
Aplicación Java standalone que implementa pruebas unitarias usando JUnit 5 y registro de eventos con Log4J, aplicados sobre una calculadora básica.
🛠️ Tecnologías utilizadas

Java 17
JUnit 5 (5.8.1)
Log4J (2.14.1)
Maven

📁 Estructura del proyecto
cps_lab10/
├── src/
│   ├── main/java/pe/edu/tecsup/lab10/
│   │   └── Calculator.java        # Clase con operaciones matemáticas
│   └── test/java/pe/edu/tecsup/
│       └── CalculatorTest.java    # Pruebas unitarias
└── pom.xml
🔢 Clase Calculator
Implementa 4 operaciones matemáticas básicas:
javapublic int add(int i, int j)   // Suma
public int sub(int i, int j)   // Resta
public int mul(int i, int j)   // Multiplicación
public int div(int i, int j)   // División

**🧪 Pruebas implementadas**
Parte 1 - JUnit 5 básico
PruebaOperaciónEntradaResultado esperadoadd()Suma4 + 37sub()Resta4 - 31mul()Multiplicación4 * 312div()División6 / 32
Parte 2 - JUnit 5 + Log4J
Se agregaron las siguientes anotaciones para controlar el ciclo de vida de las pruebas:
AnotaciónMétodoDescripción@BeforeAllinitAll()Se ejecuta una vez al inicio@AfterAllfinishAll()Se ejecuta una vez al final@BeforeEachbeforeTest()Se ejecuta antes de cada prueba@AfterEachafterTest()Se ejecuta después de cada prueba
Trazas generadas por Log4J
INFO - initAll()....!
INFO - beforeTest()....!
INFO - testAdd()....!
INFO - afterTest()....!
INFO - beforeTest()....!
INFO - testDiv()....!
INFO - afterTest()....!
INFO - beforeTest()....!
INFO - testMul()....!
INFO - afterTest()....!
INFO - beforeTest()....!
INFO - testSub()....!
INFO - afterTest()....!
INFO - finishAll()....!
▶️ Cómo ejecutar las pruebas
Desde IntelliJ

Clic derecho sobre CalculatorTest.java
Selecciona Run 'CalculatorTest'

Desde consola
bashmvn test
✅ Resultados
4 tests passed en 31 ms ✅
📌 Observaciones

JUnit 5 valida automáticamente los resultados mediante assertEquals, marcando la prueba como fallida si el valor actual no coincide con el esperado.
Log4J permite visualizar el orden exacto de ejecución de cada prueba, facilitando la depuración y el seguimiento del ciclo de vida de los tests.

👩‍💻 Autor
Elienai Ramos
Curso: Construcción y Pruebas de Software
Semana 10 — 2026
