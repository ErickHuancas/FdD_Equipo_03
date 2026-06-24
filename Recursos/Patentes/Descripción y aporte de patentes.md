# Cuadros Técnicos de las Patentes del Proyecto

Este documento presenta los cuadros técnicos de las patentes identificadas para el proyecto.

---

## Cuadro Técnico de la Patente 01

| Componente | Detalle |
| :--- | :--- |
| **Título** | Método y dispositivo para detectar la madurez de frutas y verduras |
| **Título Original** | Method and device for detecting maturity of fruits and vegetables |
| **Código** | `CN114659918A` |
| **Enlace de consulta** | [Espacenet - CN114659918A](https://worldwide.espacenet.com/patent/search/family/082037969/publication/CN114659918A?q=detect%20maturity) |
| **Descripción / Resumen** | Este dispositivo permite detectar la madurez de frutas y verduras y está compuesto por una base que integra un detector en la parte superior derecha y una caja fija en la parte superior izquierda. Dentro de esta caja se ubican lámparas de iluminación en la parte frontal y posterior, así como una cubierta articulada que incorpora un sensor de color. Además, en su interior se encuentra un sensor de grado de azúcar. Para su funcionamiento, utiliza el sensor de color, el sensor de grado de azúcar y un medidor de dureza para registrar las características de madurez, las cuales son procesadas mediante un procesador y un módulo de comparación, apoyados por un módulo de selección y un módulo de análisis de madurez. Finalmente, el controlador de visualización muestra los resultados de la detección junto con el grado de madurez, lo que facilita su evaluación y mejora la precisión en comparación con equipos convencionales. |
| **Aporte** | El aporte principal de la presente patente radica en su modelo de procesamiento de datos, donde un procesador centraliza las lecturas de los sensores para posteriormente analizarlas a través del módulo de madurez con Machine Learning. Este flujo robustece el marco lógico del proyecto, proveyendo una base analítica sólida para entrenar y refinar los algoritmos de Machine Learning encargados de predecir con precisión la vida útil del tomate en entornos comerciales. |

---

## Cuadro Técnico de la Patente 02

| Componente | Detalle |
| :--- | :--- |
| **Título** | Dispositivo para el reconocimiento de un alimento y para la determinación de su grado de frescura |
| **Título Original** | Device for the recognition of a food and for the determination of the degree of freshness thereof |
| **Código** | `WO2024201242A1` |
| **Enlace de consulta** | [Google Patents - WO2024201242A1](https://patents.google.com/patent/WO2024201242A1/en) |
| **Descripción / Resumen** | Este dispositivo está diseñado para el reconocimiento de un alimento y la determinación de su grado de frescura, y está configurado para insertarse al menos parcialmente dentro de un recipiente que contiene dicho alimento. Comprende una carcasa externa con una cavidad interna que se comunica con el exterior mediante una abertura, la cual puede cerrarse herméticamente mediante un elemento de cierre. En el interior de la cavidad se dispone al menos un detector de gases, configurado para generar una señal indicativa de la concentración de gases. El dispositivo incluye además una unidad de procesamiento y control en comunicación con el detector de gases, capaz de generar, a partir de dicha señal, información sobre el tipo de alimento presente en el recipiente y su grado de frescura. Para su funcionamiento, puede operar en una configuración de ajuste o calibración, en la que la cavidad permanece aislada del entorno externo, y en una configuración de detección, en la que la cavidad se encuentra en comunicación con el interior del recipiente, permitiendo analizar los gases presentes. |
| **Aporte** | Esta patente aporta al proyecto al introducir el uso de sensores de gases como una alternativa no destructiva para evaluar la frescura de los alimentos. Además, proporciona una referencia sobre la integración de sistemas de detección y procesamiento capaces de analizar los gases emitidos durante el deterioro del producto, permitiendo determinar su estado de conservación. Estos conceptos constituyen una base importante para el desarrollo de tecnologías automatizadas orientadas al monitoreo y control de la calidad de productos agrícolas. |

---

## Cuadro Técnico de la Patente 03

| Componente | Detalle |
| :--- | :--- |
| **Título** | Sensor de Frescura del producto |
| **Título Original** | Produce freshness sensor |
| **Código** | `US11408820B` |
| **Enlace de consulta** | [Google Patents - US11408820B1](https://patents.google.com/patent/US11408820B1/en) |
| **Descripción / Resumen** | Este dispositivo consiste en un sensor de frescura para productos agrícolas, diseñado para ser de bajo costo y desechable, lo que permite su uso a lo largo del sistema de distribución. El sensor es fijado directamente al producto por el productor y monitorea parámetros que afectan su frescura, como el color y la composición química. Está compuesto por uno o más emisores, un sensor de temperatura, un microprocesador y un transceptor, todos montados en una placa de circuito impreso, permitiendo el monitoreo continuo del producto durante su recorrido. Asimismo, se establece una línea base inicial al momento de fijar el sensor, registrándose el tiempo de inicio y las mediciones iniciales; posteriormente, la información en tiempo real es procesada para proporcionar análisis y datos relevantes. |
| **Aporte** | Esta patente aporta al proyecto al introducir un sistema de monitoreo continuo de la frescura de productos agrícolas mediante sensores integrados de temperatura, emisores ópticos, microprocesadores y comunicación inalámbrica. Además, proporciona una referencia sobre la obtención de mediciones en tiempo real y el establecimiento de una línea base inicial para comparar los cambios que experimenta el producto durante su almacenamiento y distribución. Estos conceptos permiten comprender cómo variables como la temperatura, el color y la composición del alimento pueden utilizarse para determinar su estado de madurez y conservación, constituyendo una base importante para el desarrollo de tecnologías inteligentes orientadas al control de calidad y estimación de la vida útil de productos agrícolas. |

---

## Cuadro Técnico de la Patente 04

| Componente | Detalle |
| :--- | :--- |
| **Título** | Dispositivo de calibración para sensor de dióxido de carbono |
| **Título Original** | Calibration Device for Carbon Dioxide Sensor |
| **Código** | `US7174766B2` |
| **Enlace de consulta** | [Google Patents - US7174766B2](https://patents.google.com/patent/US7174766B2/e) |
| **Descripción / Resumen** | La patente describe un sensor de dióxido de carbono (CO2) autocalibrable diseñado para solucionar la pérdida de sensibilidad y el desfase que sufren estos equipos a lo largo de su vida útil debido a contaminantes ambientales. El dispositivo integra, dentro de una misma carcasa, un detector de CO2 (que puede ser electroquímico o infrarrojo) y un generador interno de gas de referencia. Este generador consta de un elemento calefactor en contacto térmico con un material sólido capaz de liberar gas (típicamente un carbonato del Grupo 2, como carbonato de magnesio o de calcio). Cuando el procesador del sistema activa el calentador a una temperatura y tiempo predeterminados, el sólido se descompone térmicamente liberando una cantidad exacta y conocida de CO2 de referencia. El detector mide este gas liberado y, si detecta desviaciones frente al valor teórico, el procesador ajusta automáticamente los parámetros de calibración del sensor sin necesidad de mantenimiento externo o inyección manual de gases. |
| **Aporte** | Esta patente aporta al proyecto al presentar un sistema de monitoreo continuo de la frescura de productos agrícolas mediante la integración de sensores, emisores ópticos, un microprocesador y comunicación inalámbrica. Además, introduce el uso de una línea base inicial para registrar las condiciones del producto y comparar los cambios que experimenta durante su almacenamiento y distribución. Estos conceptos permiten realizar un seguimiento en tiempo real de parámetros relacionados con la calidad del alimento, proporcionando una base para el desarrollo de sistemas inteligentes orientados a la evaluación del estado de conservación y la estimación de la vida útil de productos agrícolas. |