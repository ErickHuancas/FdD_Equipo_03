# Equipo 03 - Fundamentos de Diseño
### Carrera de Ingeniería Informática, Industrial  y Ambiental
**Universidad Peruana Cayetano Heredia**

---

## 🌍 Descripción del Equipo  
Somos el **Equipo 03** del curso **Fundamentos de Diseño 2026-1**, conformado por estudiantes de la carrera de Ingeniería Informática, Industrial y Ambiental.  
Nuestro objetivo es aplicar la metodología de diseño para generar soluciones innovadoras con impacto social, tecnológico y ambiental.  

---

## 📌 Descripción

El equipo 03 desarrollará FreshTomato, un dispositivo tecnológico inteligente que clasifica tomates según su frescura y tiempo de vida útil utilizando ESP32-CAM, machine learning.

El objetivo principal de este proyecto es reducir perdidas en mercados, contribuyendo al cumplimiento de los ODS 2 (Hambre Cero), 11 (Ciudades Sostenibles), 12 (Producción y Consumo Responsable) y 13 (Acción por el Clima).

---

## ⚠️ Problemática en el Perú

En la costa peruana, especialmente en las principales zonas productoras como Ica, Lima y La Libertad, la cadena postcosecha del tomate enfrenta diversas dificultades documentadas por la industria y la academia:

1. **Pérdidas por maduración acelerada y reducción de vida útil**
   
   El tomate es una fruta climatérica que continúa su proceso de maduración después de la cosecha. Las temperaturas elevadas durante el almacenamiento y               transporte aceleran este proceso, reduciendo drásticamente su vida útil.

2. **Deterioro por almacenamiento inadecuado y exposición a condiciones variables**

   La exposición del tomate a temperaturas inadecuadas y a la luz acelera su maduración y favorece el desarrollo de daños fisiológicos:
      - Temperaturas superiores a 25°C: Aumentan la tasa respiratoria y aceleran la pérdida de calidad, provocando ablandamiento rápido y mayor susceptibilidada            daños mecánicos .
      - Temperaturas bajas (menores a 10°C): Pueden causar daño por frío (chilling injury), manifestándose como manchas superficiales, maduración irregular y               pérdida de sabor .
      - Humedad relativa baja (<85%): Acelera la pérdida de agua, provocando arrugamiento y pérdida de peso .



4. **Falta de herramientas accesibles para la evaluación de calidad**

   Actualmente, la evaluación de la calidad postcosecha del tomate se realiza mediante métodos subjetivos (presión manual u observación del color externo) o          destructivos (corte del fruto para verificar su estado interno). Los dispositivos comerciales existentes tienen costos elevados, lo que dificulta su               implementación en contextos rurales o de pequeña escala.

6. **Impacto ambiental por residuos**

    El desperdicio de Tomates genera un impacto negativo en el medio ambiente:
      - Los residuos orgánicos producen gases contaminantes durante su descomposición.
      - Se incrementa la cantidad de residuos sólidos en los mercados.
      - Se contribuye al cambio climático debido a la emisión de gases de efecto invernadero.

---

## 🍅 FreshTomato – Detector de Madurez y Factores Ambientales
### 💡 Propuesta de solución

Este proyecto tiene como objetivo desarrollar un sistema inteligente que detecte la frescura del tomate. Para ello, se emplean sensores de gases, temperatura y humedad, junto con visión artificial e inteligencia artificial.

La solución propuesta evalúa el estado interno del tomate sin dañarla, mediante el análisis de gases emitidos y características visuales externas.

A diferencia de los métodos tradicionales basados en inspección manual, esta propuesta permite una clasificación objetiva del producto. Además, estima el tiempo de vida útil restante, proporcionando información clave para la toma de decisiones.

### ¿Qué hace el dispositivo?

| Paso | Función |
|------|---------|
| 1 | Captura una imagen del tomate con ESP32-CAM |
| 2 | Mide gases de descomposición con sensor MQ-135 |
| 3 | Registra temperatura y humedad con DHT22 |
| 4 | Clasifica la palta como **APTA** o **NO APTA** (Machine Learning con Edge Impulse) |
| 5 | Estima los *días de vida útil restantes* (1-10 días según temperatura y gas) |
| 6 | Muestra el resultado en pantalla OLED o una pagina web |
| 7 | Envía una alerta al usuario con el estado y recomendación |

### 🎯 Población objetivo

Centros de acopio, plantas de distribución y empresas agroindustriales que manejan grandes volúmenes de tomate en etapa postcosecha, y que requieren optimizar los procesos de selección, clasificación y rotación de inventario para reducir pérdidas y mejorar la eficiencia logística.


Nos interesa trabajar en los siguientes **Objetivos de Desarrollo Sostenible (ODS):**
  
## 🌾 ODS 2: Hambre Cero

Este ODS busca la eliminación del hambre y garantizar que todas las personas tengan acceso a alimentos suficientes y nutritivos.

Nuestro grupo promueve el acceso equitativo a una alimentación sana, nutritiva y suficiente durante todo el año.

En el Perú, la inseguridad alimentaria es uno de los principales desafíos. Más de la mitad de la población se encuentra en riesgo, especialmente los niños y niñas, quienes no logran acceder a una alimentación adecuada.

Según la FAO (Organización de las Naciones Unidas para la Alimentación y la Agricultura), en 2024 el 51,7% de la población se encuentra en situación de inseguridad alimentaria moderada, lo que equivale a aproximadamente 17,6 millones de personas. Este dato posiciona al Perú como uno de los países con mayor prevalencia de inseguridad alimentaria en América del Sur.

La inseguridad alimentaria impacta directamente en el desarrollo infantil. Según el INEI (Instituto Nacional de Estadística e Informática), el 43,1% de los niños de 6 a 35 meses en Perú sufre anemia, lo que afecta su desarrollo físico y cognitivo.

Frente a esta problemática, existen iniciativas como World Vision, que promueve dietas balanceadas, estrategias multisectoriales y políticas públicas para combatir la anemia.

A nivel tecnológico, destacan:
- Plantix, desarrollada por PEAT GmbH, que utiliza inteligencia artificial para detectar enfermedades en cultivos.
- Crop Analytica, que emplea sistemas IoT para monitorear cultivos en tiempo real.
- Infarm, que implementa agricultura urbana con sensores en granjas verticales, reduciendo el uso de agua hasta en un 90–95%.


## 🏙️ ODS 11: Ciudades y Comunidades Sostenibles

Según el World Air Quality Report 2022, Perú se encuentra entre los países con mayor contaminación del aire en Latinoamérica.

Uno de los factores contribuyentes es la emisión de gases de efecto invernadero generados por la pérdida de alimentos. Cerca de 12,8 millones de toneladas de alimentos se desperdician al año, de los cuales más del 50% termina en botaderos.

Esto provoca la liberación de metano, un gas altamente contaminante, y aumenta la incidencia de enfermedades respiratorias en las zonas cercanas.

El ODS 11 busca el desarrollo de ciudades sostenibles, inclusivas y seguras, donde se garantice una buena calidad de vida sin comprometer el medio ambiente.

Ejemplos de soluciones:
- En California, el Laboratorio Nacional Lawrence Berkeley desarrolló sistemas para capturar metano en rellenos sanitarios y transformarlo en energía.
- Estudiantes de la Universidad de Alicante crearon un biosensor que detecta la frescura de alimentos, reduciendo el desperdicio.

## ♻️ ODS 12: Producción y Consumo Responsable

Este ODS promueve un modelo de consumo y producción sostenible, fundamental para las generaciones presentes y futuras.

Nuestro grupo promueve abordar la tercera meta que involucra este ODS que es poder reducir a la mitad el desperdicio de alimentos de alimentos per cápita en zonas rurales del Perú.

En el Perú:
- Se desperdician 12.8 millones de toneladas de alimentos al año (47.6% del total).
- Cada persona desperdicia en promedio 67.34 kg de alimentos al año.

Mientras tanto, más de 17 millones de peruanos viven en situación de inseguridad alimentaria.

Como señaló el Banco de Alimentos del Perú, una mejor gestión permitiría alimentar a millones de personas.

Ejemplos de soluciones:
- Too Good To Go, aplicación que permite comprar alimentos no vendidos a menor precio.
- Sistemas IoT para detectar la descomposición temprana de alimentos.

## 🌍 ODS 13: Acción por el Clima

Según el Ministerio del Ambiente, el Perú solo genera alrededor del 0.4% de los gases de efecto invernadero a nivel mundial. Sin embargo, es considerado el tercer país más vulnerable frente al cambio climático. Esta vulnerabilidad se refleja en distintos desastres naturales que afectan directamente a la población. Entre los años 2008 y 2019, aproximadamente 656,000 personas se vieron obligadas a abandonar sus hogares, perdiendo no solo sus viviendas, sino también sus medios de sustento.

Frente a esta situación, el ODS 13 tiene como propósito principal tomar medidas urgentes para combatir el cambio climático y reducir sus impactos. Nuestro proyecto aborda específicamente la meta 13.1, que busca fortalecer la resiliencia y la capacidad de adaptación a los riesgos climáticos, contribuyendo a reducir el desperdicio de alimentos y, con ello, las emisiones de metano generadas por residuos orgánicos en vertederos.

Algunos ejemplos de proyectos que contribuyen a este objetivo son:

- El Copernicus Programme, impulsado por la Unión Europea, que utiliza satélites y sensores para observar la Tierra en tiempo real y proporcionar datos abiertos sobre el medio ambiente.

- En El Salvador, se desarrolló un sistema IoT de bajo costo que permite monitorear la calidad del aire y acceder a información sobre la contaminación desde cualquier dispositivo con conexión a internet.

---


## 📚 Fuentes

Alicante, N. U. de. (2024). NANOBIOPOL (Grupo de investigación de Análisis de Polímeros y Nanomateriales)

CH4 Pathways. (s/f). Captura del gas de rellenos sanitarios

Coca Pimentel, V. (2023, septiembre 23). Contaminación del aire en Perú: El 58% proviene del parque automotor.

Comex.Perú. (2022, febrero 11). Solo aprovechamos el 1% de residuos orgánicos e inorgánicos que generamos.

Dirección de Estudios Económicos & Dirección General de Políticas Agrarias. (2022). Pérdidas y desperdicios de alimentos en el Perú. 

MINAM. (2024, mayo 16). Más de 148 500 toneladas de residuos sólidos municipales son valorizados en el país.

Visión Mundial Perú. (2024, 10 de diciembre). Inseguridad alimentaria en Perú.

AgroPerú Informa. (2025, septiembre 23). Pérdida y desperdicio de alimentos: un reto que exige innovación y colaboración.

La República. (2021, marzo 20). En el Perú, la mitad de los alimentos termina en la basura, según estudio.

IoT M2M Council. (2021, marzo 17). Infarm launches new vertical farming centres. Hasib, A., & Sarkar Akib, A. S. M. A. (2026).

An IoT-based smart plant monitoring and irrigation system with real-time environmental sensing, automated alerts, and cloud analytics. arXiv.

---

## 📸 Fotografía del Equipo  
<p align="center">
<img width="1408" height="768" alt="imagen_alumnos_IA" src="/Recursos/Imágenes/equipo.jpeg"/>
  <em>Figura 1. Fotografía del equipo 03</em>
</p>

---

## 👥 Integrantes del Equipo  

| Foto | Nombre | Rol | Intereses |
|------|--------|-----|-----------|
| <img src="/Recursos/Imágenes/erick.jpeg" width="90"/> | **Erick Huancas Bereche** erick.huancas@upch.pe| Líder del equipo | Innovación social, sostenibilidad, liderazgo, emprendedor |
| <img src="/Recursos/Imágenes/Rose.jpeg" width="90"/> | **Rose Suazo Davila** rose.suazo@upch.pe | Responsable de investigación | Gestión ambiental, desarrollo comunitario, investigación cientifica |
| <img src="/Recursos/Imágenes/Miguel.jpeg" width="90"/> | **Miguel Ruiz Trelles** miguel.ruiz@upch.pe | Diseñador/a | Diseño de prototipos, creatividad aplicada, impacto ambiental |
| <img src="/Recursos/Imágenes/Paloma.jpeg" width="90"/> | **Paloma Velasquez Saforas** paloma.velasquez@upch.pe | Encargado/a de documentación | Comunicación científica, redacción técnica, investigación |
| <img src="/Recursos/Imágenes/Jeremy.jpeg" width="90"/> | **Jeremy Mendez Ponce De Leon** jeremy.mendez@upch.pe | Programador/a - Modelador/a | Programación, análisis de datos, simulación |

---

## 📌 Resumen Final  
Este README resume quiénes somos, qué nos motiva y en qué ODS queremos enfocar nuestro trabajo durante el curso.  
