# Reporte de Evolución y Mejoras del Diseño Esquemático
## Proyecto: Sistema de Monitoreo Agrícola "FreshTomato"

Este documento presenta de forma técnica y detallada la evolución del diseño electrónico del proyecto **FreshTomato**, detallando el histórico de las cuatro (4) versiones del esquemático hasta consolidar una solución final estable, eficiente y protegida contra ruidos eléctricos y conflictos de hardware.

---

## 📊 Cuadro Comparativo de Versiones

| Parámetro / Componente | Versión 1.0 (Inicial) | Versión 2.0 (Transición) | Versión 3.0 (Corrección) | Versión Final (Estabilizada) |
| :--- | :--- | :--- | :--- | :--- |
| **Microcontroladores** | 2 placas (ESP32 DevKit + ESP32-CAM) | 1 placa (ESP32-S3-WROOM-1 CAM) | 1 placa (ESP32-S3-WROOM-1 CAM) | 1 placa (ESP32-S3-WROOM-1 CAM) |
| **Actuador (Servo)** | No incluido | MG996R (Conectado a salida Stepdown) | MG996R (Conectado a salida Stepdown) | MG996R (Línea de 7.2V directa + Switch) |
| **Alimentación General** | Fuentes separadas no reguladas | Stepdown de 7V a 5V general | Stepdown de 7V a 5V general | **Fuentes Independientes (USB + Cargador 5V/2A + 7.2V)** |
| **Manejo de Pines (CAM)** | Sin restricciones (No integrados) | **Conflicto Crítico** (Pines de la cámara ocupados) | **Corregido** (Reasignación a pines libres) | **Optimizado** con protección en la señal del Servo |
| **Filtrado MQ135** | Sin capacitor de desacoplo | Sin capacitor de desacoplo | Sin capacitor de desacoplo | **Capacitor Electrolítico de 100 µF** |
| **Protección Lógica** | No incluida | No incluida | No incluida | **Divisores resistivos** para entradas analógicas/lógicas |

---

## 🔍 Análisis Detallado de la Evolución del Circuito

### 🔴 Versión 1.0: Arquitectura Duplicada (Inicial)
La primera aproximación del proyecto dependía de dos procesadores independientes para segmentar las tareas:
* **Componentes:** Un ESP32 clásico (para la lectura de sensores) y un ESP32-CAM (únicamente dedicado al procesamiento de imágenes).
* **Limitaciones:** El circuito no incluía servomotor. Carecía de filtros de desacoplo en la línea del sensor de gas MQ135, lo que provocaba lecturas altamente inestables debido al ruido térmico del calentador interno del sensor. La comunicación entre ambos microcontroladores complejizaba innecesariamente el código y aumentaba el consumo energético.

### 🟠 Versión 2.0: Unificación de Hardware y Errores de Conmutación
Con el fin de optimizar costos y espacio, se migró a un único procesador potente y se introdujo fuerza mecánica:
* **Mejoras:** Se reemplazaron las dos placas por un único **ESP32-S3-WROOM-1 CAM**. Se integró el servomotor de alto torque (MG996R) y un regulador conmutado *Stepdown* para reducir el voltaje de las baterías de 7V a 5V.
* **Errores Críticos Identificados:** 1.  **Conflicto de Pines CSI:** Se asignaron las líneas de control del servo (`GPIO6`), el DHT22 (`GPIO4`) y el MQ135 (`GPIO1`) a pines que la cámara utiliza internamente para el bus de datos y bus de control SCCB. Esto corruptora las capturas de imagen y reseteaba el procesador.
    2.  **Cortes de Tierra:** El interruptor general se ubicó interrumpiendo la línea de masa (`GND`), dejando el circuito flotante.

### 🟡 Versión 3.0: Corrección de Matriz de Pines
Esta versión se enfocó exclusivamente en resolver la interacción de hardware a nivel de software y distribución de pistas:
* **Mejoras:** Se realizó un mapeo profundo de la hoja de datos del ESP32-S3 CAM. Se liberaron por completo los pines internos de la cámara y se reubicaron las señales del Servo, DHT22 y MQ135 hacia GPIOs libres (como `GPIO8`, `GPIO9`, etc.). El interruptor fue movido a la línea positiva antes de la regulación.

### 🟢 Versión Final: Independencia de Potencia y Estabilidad Señal-Ruido
La versión definitiva del esquemático soluciona los problemas de caídas de tensión y picos de corriente aislando los caminos eléctricos por su naturaleza de consumo:

1.  **Aislamiento de la Etapa de Potencia del Servomotor:** * El servomotor MG996R demanda corrientes pico elevadas al romper la inercia. Se conectó de forma directa a la línea del portabaterías de **7.2V** (aprovechando su rango máximo de operación).
    * Se le integró un **Switch dedicado** en el positivo para cortar su energía cuando no esté operando, erradicando el consumo parásito y previniendo sobrecalentamientos.
2.  **Filtrado Eléctrico para el Sensor MQ135:**
    * El MQ135 posee una resistencia calefactora que genera picos cíclicos de demanda. Para mitigar las fluctuaciones en las lecturas analógicas, se energizó mediante un **cargador externo dedicado de 5V a 2 Amperios**.
    * Se colocó un **capacitor electrolítico de 100 µF** en paralelo entre `VCC` y `GND` del sensor, absorbiendo los rizos de corriente y estabilizando los voltajes de lectura.
3.  **Alimentación Lógica Limpia:**
    * El **ESP32-S3-WROOM-1 CAM** y el sensor **DHT22** se alimentan mediante el bus USB conectado a una laptop, garantizando una fuente conmutada limpia, ideal para el procesamiento de la IA y el envío de datos.
4.  **Adaptación de Niveles con Divisores Resistivos:**
    * Se incluyeron **divisores resistivos** calculados en las salidas de las señales analógicas/lógicas para adecuar los voltajes al rango seguro de tolerancia del ADC del ESP32-S3 ($0	ext{ V} - 3.3	ext{ V}$), protegiendo las compuertas lógicas contra degradación por sobrevoltaje.

---

## 🎯 Conclusión del Proceso de Ingeniería
El diseño final abandonó la regulación única con *Stepdown* general debido a que los tirones del servomotor y el ruido del calefactor del MQ135 degradaban la estabilidad del ESP32-S3. La arquitectura final de **Fuentes Distribuidas** (Batería 7.2V para motor + Cargador 5V/2A para sensor de gas + USB para lógica) asegura un funcionamiento continuo de 24/7 sin reinicios imprevistos, lecturas analógicas confiables y una captura de video nítida.