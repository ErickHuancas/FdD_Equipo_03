# CAPÍTULO I: INTRODUCCIÓN

## Situación Problemática

---

## Contexto General
El desperdicio de alimentos es una problemática significativa y persistente en los sistemas alimentarios de hoy en día.  En el Perú, existen estudios sobre pérdidas en la agricultura que señalan niveles altos de desperdicio orgánico, especialmente durante la poscosecha; donde las frutas y verduras son las más afectadas por su rápida descomposición y vida útil corta.

Entre los productos más afectados destaca el tomate (Solanum lycopersicum L.), una de las hortalizas de mayor consumo en la dieta diaria peruana. Debido a su alta perecibilidad y elevado contenido de agua, este cultivo presenta una rápida pérdida de calidad durante las etapas de almacenamiento y comercialización, lo que genera importantes pérdidas antes de llegar al consumidor final. Diversos estudios sobre manejo poscosecha señalan que el deterioro del tomate está estrechamente relacionado con condiciones inadecuadas de manipulación, temperatura y tiempo de almacenamiento, factores que incrementan significativamente las pérdidas dentro de la cadena de comercialización (1,2)

A nivel nacional, los informes señalan a la podredumbre como causa principal con un 27% de las pérdidas. Por otro lado, el verdeamiento y la pérdida de agua con un 22% y 14% respectivamente. Asimismo, los golpes mecánicos y la mala clasificación de los tomates cada uno con un 11% de las pérdidas. Por lo tanto, la monitorización de las condiciones ambientales durante la distribución y venta es crítica para mitigar la degradación acelerada del tomate (2).

En este contexto, el desperdicio de tomate en los mercados representa una problemática persistente dentro de la cadena de abastecimiento alimentario, asociada principalmente a deficiencias en el manejo poscosecha, almacenamiento y comercialización, generando impactos económicos para comerciantes y productores, así como una mayor contribución en los niveles de desperdicios de alimentos generados. 

## Contexto en el sector comercial
En el sector retail, las pérdidas de los alimentos perecibles, como el tomate, tiene un impacto significativo en la cadena de suministro y durante la gestión de inventario; proceso que busca conservar la calidad del producto hasta la obtención final del cliente mediante un elevado nivel de gestión en el planeamiento de su logística. Por lo tanto, es necesario mencionar que la vida útil del tomate no está en función únicamente de factores biológicos, sino de las condiciones de almacenamiento en la que se encuentra al establecerse en las cadenas de retail alimentario (3). 

Este comercio minorista de alimentos cuenta con una amplia gama de estrategias para minimizar el desperdicio y evitar que sus productos caduquen antes de ser comprados. Sin embargo, muchos de los mecanismos empleados no permiten un mayor control sobre los alimentos. Dentro de las políticas de inventarios, a menudo se utilizan los sistemas de seguimiento de inventario First-In-First-Out (FIFO), que refiere a la venta de los productos que se adquieren primero, quedando en el inventario los productos que fueron adquiridos recientemente (4). No obstante, un estudio no experimental mediante encuestas en una de las grandes cadenas de retail, evidenció que el nivel de uso y efectividad del sistema FIFO es baja, esto confirma que la gestión de inventarios basada únicamente en un sistema dinámico de almacenaje es insuficiente para productos de alta tasa respiratoria como el tomate. (4) Este mecanismo ignora la variabilidad biológica de cada lote de tomate, es decir que la jaba adquirida recientemente presenta índices de emisión de etileno superiores a los de una jaba antigua.

 Por consiguiente, para apoyar de manera eficiente la cadena de suministro, no solo basta con el uso de una cadena de frío con condiciones de temperaturas óptimas, sino del uso de tecnologías que sean capaces de monitorear el estado fisiológico del tomate; logrando detectar anomalías químicas en lotes específicos que la temperatura no logra revelar y asegurando una toma de decisiones basada en el estado real de degradación del producto. 


---

# Propuesta de solución
En el Perú, especialmente en regiones costeras como Ica, Lima y La Libertad, los supermercados enfrentan pérdidas significativas de tomate debido a condiciones inadecuadas de almacenamiento y exhibición. Factores como temperaturas no controladas, variaciones de humedad y largos tiempos de exposición aceleran el deterioro del producto, reduciendo su vida útil en los puntos de venta. Asimismo, la evaluación de la calidad del tomate se realiza principalmente mediante inspecciones visuales, las cuales son subjetivas y dependen del criterio del personal, lo que limita la detección temprana del deterioro; además, muchos establecimientos no cuentan con sistemas tecnológicos que permitan un monitoreo continuo, objetivo y en tiempo real.

Según un estudio, demostró que la calidad del tomate, evaluada mediante atributos como firmeza, color e índice general de calidad, disminuye rápidamente bajo condiciones ambientales, afectando directamente su aceptación por parte del consumidor. En particular, se ha evidenciado que solo una pequeña proporción de tomates en estado deteriorado mantiene aceptación comercial, lo que resalta la necesidad de implementar sistemas de monitoreo temprano y preciso que permitan evitar pérdidas y rechazos en el punto de venta.(5)

Enfrentados a este problema, es necesario encontrar soluciones tecnológicas que nos permitan monitorear la situación de manera objetiva. Para resolver esto, se propone crear un sistema inteligente llamado FreshTomate. Este sistema utiliza sensores que miden los gases, la temperatura y la humedad, además de técnicas de visión artificial y de inteligencia artificial. Todo esto nos permite monitorear el estado del tomate en tiempo real.

El sistema se aplicará en un momento crítico de la cadena de suministro, específicamente durante la etapa de recepción de mercancía, es decir, antes de que los tomates entren a la cadena de frío. En este lugar, el aparato operará como un filtro de calidad, posibilitando la revisión del estado del producto previo a su almacenamiento en cámaras frigoríficas. Así, se previene que entren productos en malas condiciones que pudieran perjudicar la calidad del lote restante.
Para su funcionamiento, el sistema utiliza un microcontrolador llamado ESP32-CAM. Este microcontrolador permite procesar datos y capturar imágenes del tomate para analizarlo.(6,7) También se utiliza un sensor de gases llamado MQ-135. Este sensor detecta gases como amoníaco y dióxido de carbono que se producen cuando el tomate se descompone.(8) Además, se utiliza un sensor llamado DHT22 para medir la temperatura y la humedad. Estas variables son importantes porque influyen en la maduración del tomate.(9)

Los datos que se recopilan de estos sensores se procesan con una herramienta de aprendizaje automático desarrollada con Edge Impulse. Esta herramienta puede ser entrenada para clasificar el estado del tomate en dos categorías: apto para el consumo y no apto para el consumo. Esta clasificación es rápida y no daña el tomate. Es mejor que los métodos tradicionales.

Además, el sistema dispondrá de una fuente de alimentación con baterías, lo que posibilitará su funcionamiento independiente y hará más fácil su instalación en varios lugares dentro del área de recepción sin la necesidad de tener una conexión eléctrica fija.

En resumen, el sistema permite vigilar las condiciones ambientales y el estado del tomate. Esto nos da alertas antes de que haya problemas y nos ayuda a tomar decisiones. Con tecnologías modernas y fáciles de usar, podemos mejorar la calidad, reducir el desperdicio de comida y gestionar mejor los supermercados. Además, esto se ajusta a la norma ISO 22000, que busca asegurar que los alimentos sean seguros y controlar los riesgos en toda la cadena de suministro del tomate.

---

# Objetivos

## Objetivo general

Diseñar e implementar un sistema ciberfísico inteligente denominado FreshTomate, basado en el uso del microcontrolador ESP32-CAM, sensores ambientales y técnicas de aprendizaje automático, que permita evaluar y monitorear en tiempo real la vida útil del tomate (Solanum lycopersicum L.)

## Objetivos específicos

- Realizar un estudio del estado del arte que permita identificar las tecnologías aplicadas en la detección de la frescura de alimentos, incluyendo sensores de gases, visión artificial e inteligencia artificial.
- Desarrollar el sistema físico mediante la selección e integración de componentes electrónicos, incluyendo sensores de gas, temperatura y humedad, así como el módulo ESP32-CAM para la captura de imágenes.
- Diseñar e implementar un modelo de inteligencia artificial que permita clasificar la frescura del tomate y estimar su vida útil, utilizando técnicas de aprendizaje automático.
- Realizar pruebas de funcionamiento para validar la precisión en la detección de la frescura y el procesamiento de datos provenientes de los sensores y del sistema de visión artificial.
- Evaluar el desempeño del sistema mediante pruebas experimentales, comparando los resultados obtenidos con métodos tradicionales de inspección manual en la detección temprana del deterioro del tomate, en condiciones similares al entorno comercial.


---

## BIBLIOGRAFÍA
- Córdova Peña, Moisés Teodoro, Pinasco Alegre, Renzo Giovanni, Pizarro Chirinos, Giannina Josefina, Quiñones Jara, Teófilo Marcelo, Córdova Peña. laneamiento Estratégico del Tomate en el Perú [Tesis de maestría]. [Surco, Perú]: Pontificia Universidad Católica del Perú; 2016. 
- María Yovani Irigoín Lara. Vida útil de tomate (Solanum lycopersicum L. var. Sheila Victory F1) cosechado en dos estados de madurez y almacenados en diferentes tiempos y temperaturas [Tesis para optar el título profesional de Ingeniero en Industrias Alimentarias]. [Cajamarca, Perú]: Universidad Nacional de Cajamarca; 2024. 
- Salas BDM, David O, Díaz P, Joel D, Lozano V, Vanessa C. GESTIÓN DE   INVENTARIOS PERECIBLES ADAPTADA PARA LAS DECISIONES SOBRE EL SUMINISTRO: ESTUDIO DE CASO DEL PROCESO DE PLANIFICACIÓN DEL ABASTECIMIENTO DE YOGURES EN HIPERMERCADOS TOTTUS.
- Espinoza DRL. Gestión de Inventarios y la merma de productos perecederos en hipermercados Tottus. 2023;115. 
- Aftab RA, Ahmad F, Monish M, Zaidi S. Postharvest quality assessment of tomato during storage: An experimental and ML fusion. J Stored Prod Res. 1 de mayo de 2025;112:102643. doi:10.1016/j.jspr.2025.102643
- Kulkarni SM, Umadi S, R m A, Airani SS, Raikar MM. Grading and Classification of Tomatoes Using ESP32-CAM and Impulse Cloud based IoT Platform for Sustainability. Procedia Comput Sci. 1 de enero de 2025;Seventh International Conference on Recent Trends in Image Processing and Pattern Recognition (RTIP2R-2024)260:938-46. doi:10.1016/j.procs.2025.03.277 
- Santos S. Guía de asignación de pines del ESP32-CAM AI-Thinker: Explicación del uso de los GPIO | Tutoriales de Random Nerd [Internet]. 10 de marzo de 2020 [citado 2 de abril de 2026]. Disponible en: https://randomnerdtutorials.com/esp32-cam-ai-thinker-pinout/
- Tangirbergen A, Tleubekova A, Yergaliuly G, Kurmanbayeva A, Soltabayev B, Soltabayeva A. Real-time detection of potato spoilage by gas sensor array coupled with microbiological analysis. LWT. 1 de enero de 2026;239:118926. doi:10.1016/j.lwt.2025.118926
- K.VENKATARAMANAN, D.PRASANTH, V.SHEEBA, R.KUMARESAN. SMART FOOD SPOILAGE PREDICTION AND ALERT SYSTEM. Int J Nexus Knowl Multidiscip J Online ISSN 3108-0529. 3 de julio de 2025;1(1):62-9. 




