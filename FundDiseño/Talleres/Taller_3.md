# CAPÍTULO I: INTRODUCCIÓN

## Situación Problemática

---

## Contexto General



## Contexto en el sector comercial

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



