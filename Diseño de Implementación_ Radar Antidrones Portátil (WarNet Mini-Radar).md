# Diseño de Implementación: Radar Antidrones Portátil (WarNet Mini-Radar)

## 1. Concepto y Arquitectura del Sistema
El **WarNet Mini-Radar** es una unidad de detección táctica portátil diseñada para integrarse en el ecosistema **WarNet Air**. Actúa como un nodo sensor avanzado que proporciona datos de detección local a la **App Comander** y se sincroniza con el **Gateway Central** del Aerodirigible para una conciencia situacional global.

### Arquitectura de Integración
- **Nodo Local (Mini-Radar):** Ejecuta detección y clasificación por IA en el borde (Edge AI).
- **Gateway Central (Aerodirigible):** Actúa como servidor de mando y control (C2), agregando datos de múltiples mini-radares.
- **App Comander:** Interfaz de usuario para visualización de amenazas, control de alertas y gestión de contramedidas.

---

## 2. Especificaciones Técnicas y Piezas (BOM)

### A. Sensores de Radar (FMCW de Onda Milimétrica)
Para detectar objetivos pequeños (drones Clase 1) a corta distancia con alta precisión:
- **Sensor Principal:** **uRAD 77GHz** o **OmniPreSense OPS243-C**.
  - **Rango:** 0.1m - 100m+ (optimizado para proximidad).
  - **Funciones:** Medición de distancia, velocidad, ángulo y dirección.
  - **Interfaz:** USB/UART para conexión directa al procesador de IA.

### B. Unidad de Procesamiento e IA Local
- **Procesador:** **NVIDIA Jetson Nano** o **Google Coral Dev Board**.
  - **IA Local:** Modelo **YOLOv9-Tiny** optimizado para detección de drones en tiempo real.
  - **Función:** Clasificación de objetivos (Dron vs Ave vs Ruido) y seguimiento de trayectorias.

### C. Comunicaciones y Red
- **Módulo de Radio:** **LoRaWAN** o **WiFi 6 de largo alcance** (para conexión con el Aerodirigible).
- **Protocolos:** 
  - **MQTT:** Para el envío de telemetría y alertas ligeras al Gateway.
  - **MAVLink:** Para la coordinación de navegación y estados del sistema.
  - **Protobuf:** Para la serialización eficiente de datos de radar.

### D. Alimentación y Carcasa
- **Batería:** LiPo de alta densidad (10,000 mAh) para 4-6 horas de autonomía.
- **Carcasa:** Diseño tipo mochila con chasis de aluminio ligero y polímero resistente a impactos.
- **Peso Total:** < 2.5 kg.

---

## 3. Lógica de la IA Local y Funciones
1. **Filtro de Ruido:** Algoritmos de procesamiento de señal para eliminar "clutter" (lluvia, vegetación).
2. **Clasificación Automática:** Identificación de la firma radar (RCS) para distinguir tipos de drones.
3. **Alerta Temprana:** Notificación instantánea a la App Comander mediante vibración y alertas visuales en el mapa táctico.
4. **Coordinación WarNet:** Si un mini-radar detecta una amenaza, el Gateway del Aerodirigible puede reorientar otros sensores o drones interceptores automáticamente.

---

## 4. Requisitos de Implementación
- **Software:** Linux (Ubuntu para Jetson), Python 3.11, OpenCV, TensorRT.
- **Integración:** API REST/Websockets para la comunicación con la App Comander.
- **Seguridad:** Encriptación AES-256 en todos los enlaces de datos.

---

## 5. Conclusión del Diseño
Este radar mini portátil cierra la brecha entre la detección estratégica y la protección táctica inmediata. Su integración con el **WarNet Air** permite que cada soldado sea un nodo sensor inteligente, coordinado por el **Comander** desde el aire.
