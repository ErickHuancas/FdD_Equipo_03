# Descripción de Versiones y Mejoras del Hardware y Carcasa
## Proyecto: Sistema Inteligente para el Monitoreo y Clasificación de Tomate Fresco

Este documento detalla la evolución del diseño de la carcasa (CAD en Onshape), la integración de los componentes electrónicos, el sistema mecánico y de alimentación a través de sus tres versiones de desarrollo hasta consolidar el prototipo final funcional.

---

## 📐 Versión 1.0 - Diseño Inicial del Sistema

### Descripción General
Se desarrolló el primer prototipo digital de una carcasa destinada al monitoreo de las condiciones ambientales para la conservación de tomate fresco. El diseño fue realizado en **Onshape** considerando la integración de sensores y módulos electrónicos necesarios para la adquisición de datos y captura de imágenes.

### Componentes Integrados
* **ESP32:** Utilizado como unidad principal de procesamiento.
* **ESP32-CAM:** Dedicado exclusivamente para la captura y procesamiento de imágenes.
* **Sensor DHT22:** Para la medición precisa de temperatura y humedad ambiental.
* **Sensor MQ-135:** Para el monitoreo de la calidad del aire y detección de gases de descomposición.

### Características Implementadas
* Diseño geométrico de la carcasa principal.
* Modelado tridimensional de la tapa frontal y tapa trasera.
* Soportes internos dedicados para el anclaje de módulos electrónicos.
* Apertura y dimensionamiento específico para la óptica de la cámara ESP32-CAM.
* Rejillas de ventilación pasiva para la correcta circulación del aire hacia los sensores.
* Sistema de fijación y cierre mediante tornillos mecánicos.
* Base estructural sólida para el soporte general del sistema.

### Objetivos Alcanzados
* Definición de la estructura física y ergonomía base del dispositivo.
* Integración preliminar y espacial de los componentes electrónicos dentro del espacio tridimensional.
* Verificación dimensional del espacio disponible para el ensamblaje manual.
* Generación del primer prototipo CAD completamente funcional.

---

## ⚙️ Versión 2.0 - Integración de Alimentación, Iluminación y Sistema Mecánico

### Descripción General
Se realizaron mejoras sustanciales enfocadas en la autonomía eléctrica mediante alimentación externa, la homogenización de la iluminación para las técnicas de visión artificial y la incorporación de un mecanismo de accionamiento físico para automatizar el proceso de clasificación de los tomates.

### Mejoras Implementadas
* **Alimentación Externa:** Incorporación de un adaptador de corriente para la conexión directa a la red eléctrica.
* **Iluminación Controlada:** Integración de un sistema de iluminación mediante LED para estandarizar las capturas de imágenes de la cámara.
* **Optimización Térmica:** Adición de rejillas laterales de ventilación para mejorar el flujo de aire interno.
* **Distribución Espacial:** Rediseño y optimización de la ubicación interna de los componentes para evitar interferencias.
* **Soporte Electrónico:** Implementación de una baquelita perforada para el montaje, soldadura y organización rígida de los componentes electrónicos.

### Cambios de Componentes
* 🔴 *Se retiró* el ESP32 clásico utilizado inicialmente como controlador principal.
* 🟢 *Se incorporó* un servomotor para el accionamiento mecánico y desvío en la clasificación.
* 🔄 *Se unificó* el control en la placa **ESP32-S3-WROOM-1 CAM** para el procesamiento general, captura de imágenes y control de periféricos.

### Beneficios Obtenidos
* Mejor calidad y repetibilidad en la iluminación para los modelos de visión artificial.
* Mayor funcionalidad mecánica e interactividad automatizada mediante el servomotor.
* Mejor organización de los cables y de las conexiones eléctricas internas.
* Mayor facilidad para tareas de mantenimiento, desmontaje y montaje.
* Mejor disipación térmica activa/pasiva gracias a las nuevas rejillas de ventilación.

---

## 🏆 Versión 3.0 y Final - Prototipo Final Funcional

### Descripción General
Se desarrolló la versión definitiva y de producción del sistema, incorporando mejoras críticas de portabilidad en campo, flexibilidad en la alimentación, robustez en la protección del cableado, ergonomía de apertura rápida y control de encendido manual.

### Mejoras Implementadas
* **Portabilidad:** Integración de una Power Bank como fuente de alimentación portátil para pruebas en entornos agrícolas reales.
* **Conectividad Estándar:** Incorporación de conexión e interfaz mediante cable micro USB.
* **Control de Energía:** Adición de un interruptor físico ON/OFF para el control de encendido y apagado general del dispositivo.
* **Protección de Entrada:** Implementación de un prensaestopa para proteger, sellar y asegurar el paso del cableado de alimentación hacia el interior de la carcasa, evitando tirones mecánicos.
* **Sistema de Cierre Magnético:** Incorporación de imanes de neodimio de 10 mm para sustituir los tornillos en el sistema de cierre de la tapa.
* **Brazos de Desacople:** Diseño e impresión de brazos de apertura que permiten separar fácilmente la tapa venciendo la fuerza de atracción magnética de los imanes de neodimio.
* **Optimización de Potencia:** Redistribución balanceada de las líneas de energía interna.
* **Gestión de Cableado (*Cable Management*):** Organización final del cableado interno, mejorando la integración de las borneras y eliminando cruces de cables.
* **Interconexión Modular:** Inclusión de cables tipo macho y hembra para facilitar el intercambio rápido de módulos averiados.

### Componentes Incorporados (Lista Definitiva de Materiales)
1.  Power Bank (Alimentación portátil)
2.  Interruptor ON/OFF
3.  Prensaestopa plástico de seguridad
4.  Borneras de conexión atornillables
5.  Baquelita perforada de soporte
6.  Arnés de cables macho y hembra
7.  Servomotor de clasificación
8.  Sistema de iluminación LED integrado
9.  Imanes de neodimio de 10 mm (x4)
10. Brazos de apertura rápida para desacople magnético

### Beneficios Obtenidos
* **Máxima Autonomía:** Portabilidad completa para realizar pruebas directamente en los centros de acopio o invernaderos.
* **Robustez Mecánica:** Protección mecánica del cableado de entrada mediante el prensaestopa contra esfuerzos externos.
* **Acceso Rápido:** Cierre hermético y seguro de la carcasa sin necesidad de herramientas o tornillos adicionales.
* **Mantenimiento Eficiente:** Apertura rápida en segundos para inspección de componentes internos o calibración de sensores.
* **Seguridad Operacional:** Mejor experiencia de uso y seguridad eléctrica gracias al sistema de encendido independiente (Switch ON/OFF).
* **Validación Académica:** Diseño optimizado estéticamente y estructuralmente para pruebas finales y sustentaciones técnicas de alto nivel.