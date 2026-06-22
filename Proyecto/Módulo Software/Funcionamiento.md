# Módulo de Software

## Descripción General

El módulo de software constituye el núcleo del sistema, permitiendo la comunicación entre el sistema embebido ESP32-S3-WROOMCAM, el servidor Flask, el modelo de Machine Learning y la interfaz de usuario. Su función principal es procesar las imágenes y datos ambientales adquiridos, estimar la vida útil del tomate y almacenar los resultados obtenidos.

---

# Componentes del Sistema

## Dashboard Web

La interfaz web permite:

- Iniciar una nueva evaluación.
- Visualizar el progreso del proceso.
- Mostrar los resultados de clasificación.
- Consultar el historial de análisis almacenados.

---

## Servidor Flask

El servidor Flask actúa como núcleo del sistema y es responsable de:

- Recibir las solicitudes provenientes del Dashboard.
- Comunicarse con el ESP32-S3-WROOM-CAM mediante HTTP.
- Procesar las imágenes capturadas.
- Ejecutar el modelo de Machine Learning.
- Calcular la vida útil del tomate.
- Almacenar los resultados en una base de datos SQLite.

---

## Sistema Embebido ESP32-CAM

El ESP32-S3-WROOM-CAM se encarga de:

1. Consultar continuamente el estado del servidor.
2. Ejecutar un ciclo de adquisición cuando recibe una orden de inicio.
3. Posicionar el servomotor en tres ángulos diferentes (0°, 90° y 180°).
4. Leer la temperatura mediante el sensor DHT22.
5. Leer la concentración de gases mediante el sensor MQ135.
6. Capturar una imagen de cada cara del tomate.
7. Enviar la información al servidor Flask.

---

## Modelo de Machine Learning

Se emplea una red neuronal convolucional basada en MobileNetV2 entrenada para clasificar tomates en dos categorías:

- Tomate sano.
- Tomate malogrado.

El modelo recibe imágenes RGB de tamaño 224×224 píxeles y genera una probabilidad mediante una función de activación sigmoide.

La clasificación se realiza mediante:

- Probabilidad ≥ 0.5 → Tomate sano.
- Probabilidad < 0.5 → Tomate malogrado.

---

## Estimación de Vida Útil

La vida útil restante se estima considerando tres factores principales:

### Temperatura

Se emplea el modelo Q10, donde un incremento de 10°C aproximadamente duplica la velocidad de deterioro.

### Concentración de gases

El sensor MQ135 proporciona una medida relativa del deterioro mediante la detección de compuestos volátiles emitidos durante el proceso de maduración y descomposición.

### Confianza del modelo

La confianza obtenida por MobileNetV2 permite ajustar la estimación de forma conservadora cuando existen predicciones poco seguras.

---

# Flujo General de Funcionamiento

1. El usuario presiona el botón **"Iniciar Evaluación"** desde el Dashboard.
2. El Dashboard envía una solicitud POST al servidor Flask.
3. Flask genera un identificador único de sesión para asociar las tres caras del tomate.
4. El ESP32-S3-WROOM-CAM consulta periódicamente el estado del servidor mediante GET `/estado`.
5. Al recibir la orden de inicio, comienza el ciclo de adquisición.
6. El servomotor posiciona el tomate en tres orientaciones diferentes (0°, 90° y 180°).
7. En cada posición se registran:

   - Temperatura (DHT22).
   - Concentración de gases (MQ135).
   - Imagen capturada por la cámara.

8. Cada etapa es enviada al servidor Flask mediante HTTP POST.
9. Al completar las tres etapas, el ESP32-CAM notifica la finalización del proceso.
10. Flask procesa las imágenes utilizando MobileNetV2.
11. Se calcula la temperatura promedio y la concentración promedio de gases.
12. Se estima la vida útil restante del tomate.
13. Los resultados se almacenan en SQLite.
14. El Dashboard muestra la clasificación y el historial de evaluaciones.

---

# Comunicación Entre Componentes

## Dashboard → Flask

```text
POST /iniciar
```

Solicita el inicio de una nueva evaluación.

---

## ESP32 → Flask

Consulta periódicamente:

```text
GET /estado
```

para verificar si debe iniciar una nueva adquisición.

---

## Envío de las Etapas

Para cada etapa, el ESP32-S3-WROOM-CAM envía:

### Cabeceras HTTP

```text
X-Session
X-Etapa
X-Temp
X-MQ135
```

### Cuerpo del mensaje (Body)

```text
Imagen JPEG capturada por la ESP32-S3-WROOM-CAM
```

mediante:

```text
POST /etapa
```

---

## Finalización del Proceso

Una vez completadas las tres etapas:

```text
POST /finalizar
```

El servidor Flask procesa toda la información adquirida.

---

# Base de Datos SQLite

La información almacenada incluye:

- Fecha y hora del análisis.
- Identificador de sesión.
- Resultado de clasificación.
- Nivel de confianza.
- Temperatura promedio.
- Concentración promedio de gases.
- Vida útil estimada.
- Rutas de almacenamiento de las imágenes.

---

# Tecnologías Utilizadas

| Componente | Tecnología |
|------------|------------|
| Sistema Embebido | ESP32-S3-WROOM-CAM |
| Servidor | Flask |
| Lenguaje | Python |
| Machine Learning | TensorFlow + MobileNetV2 |
| Procesamiento de Imágenes | Pillow + NumPy |
| Base de Datos | SQLite |
| Comunicación | HTTP |
| Interfaz Gráfica | HTML + CSS + JavaScript |
| Sensor de Temperatura | DHT22 |
| Sensor de Gases | MQ135 |
| Actuador | Servo MG996R |

---

# Conclusión

El módulo de software integra la adquisición de datos, el procesamiento mediante inteligencia artificial, la estimación de vida útil y el almacenamiento de información, permitiendo la clasificación automática del estado del tomate y proporcionando una aproximación de su tiempo de conservación restante.