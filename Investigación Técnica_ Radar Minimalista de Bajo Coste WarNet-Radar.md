# Investigación Técnica: Radar Minimalista de Bajo Coste WarNet-Radar

## 1. Introducción y Objetivos
La presente investigación se centra en el desarrollo de un sistema de radar **minimalista y funcional**, diseñado específicamente para reducir drásticamente los costes, volúmenes y necesidades energéticas de los sistemas convencionales. Este radar está orientado a su integración en el **Aerodirigible WarNet-Air**, con una capacidad de detección de vehículos aéreos a distancias de hasta **50 km**. El objetivo principal es lograr un sistema ultra-eficiente que utilice los componentes mínimos necesarios, manteniendo una funcionalidad robusta para plataformas de volumen reducido.

## 2. Arquitectura del Sistema y Configuración de Módulos
El diseño arquitectónico se fundamenta en una configuración de **4 amplificadores** y **4 módulos** de radar, optimizando el uso de componentes comerciales (COTS) y procesamiento mediante Inteligencia Artificial. La disposición de los sensores se realiza en una estructura en cruz, lo que permite la detección vertical y horizontal simultánea. Para cubrir los puntos ciegos inherentes a esta configuración, el sistema realiza un movimiento de rotación de 45° sobre su propio eje, logrando una cobertura omnidireccional con el mínimo de sensores.

### 2.1. Antena mmWave Autodirigible
El sistema emplea una antena de ondas milimétricas (**mmWave**) que opera en la banda Ka (26.5-40 GHz) o W (76-81 GHz). Esta antena es autodirigible y está controlada por un sistema de IA que le permite apuntar hacia objetivos detectados o realizar barridos de largo alcance. La optimización de la antena permite la detección de objetos con una sección transversal de radar (RCS) pequeña a distancias de hasta 50 km, lo que resulta fundamental para la vigilancia aérea.

## 3. Inteligencia Artificial y Control de Posición
La IA integrada, que puede ejecutarse en procesadores como el **ESP32-S3** o el **Jetson Nano**, gestiona la autodirección de la posición de la antena y los sensores según la telemetría del vehículo. Esta inteligencia se encarga de la fusión de datos de los 4 sensores para eliminar falsos positivos y de implementar algoritmos de seguimiento en radio dirigido para mantener el contacto con los vehículos detectados.

## 4. Estudio de Componentes y Análisis de Costes
Para lograr un sistema de bajo coste, se proponen componentes de referencia que equilibran el rendimiento técnico con la accesibilidad económica. La siguiente tabla detalla los componentes principales y sus funciones dentro del sistema:

| Componente | Modelo de Referencia | Función Principal | Coste Estimado (USD) |
| :--- | :--- | :--- | :--- |
| **Módulo Radar mmWave** | TI IWR6843 / AWR1843 | Sensor principal FMCW para detección y rango. | $100 - $150 |
| **Amplificador Banda Ka** | PE15A63021 / TGA4517 | Amplificación de señal para maximizar el alcance. | $50 - $200 |
| **Micro-Servos de Precisión** | Dynamixel XL330 | Orientación activa de la antena y sensores. | $30 - $50 |
| **Procesador de IA** | ESP32-S3 / Jetson Nano | Control del sistema y procesamiento de señales. | $15 - $100 |
| **Antena MIMO** | Custom mmWave Array | Emisión y recepción de ondas milimétricas. | $50 - $150 |

El coste total estimado del sistema se sitúa por debajo de los **$1,000 USD**, lo que representa una fracción del coste de los sistemas comerciales equivalentes, que suelen superar los $20,000 USD.

## 5. Aplicación en el Aerodirigible WarNet-Air
El radar se integra en la góndola del dirigible, aprovechando su capacidad de **loitering** (mantenimiento de posición) para realizar barridos circulares. El dirigible puede realizar maniobras de giro sincronizadas con el radar para ampliar la apertura sintética (SAR) y mejorar la resolución de la detección a larga distancia. Además, el sistema ultra-eficiente permite su alimentación mediante los paneles solares y la pila de combustible del dirigible, garantizando una autonomía prolongada.

## 6. Conclusión
El enfoque de **WarNet-Radar** demuestra que es posible construir un sistema de detección de largo alcance con componentes mínimos y alta inteligencia. La reducción de la precisión extrema se compensa con la ubicuidad y el bajo coste, permitiendo el despliegue de redes de radares distribuidos en múltiples plataformas autónomas.
