# Gateway Central WarNet-Radar: Centro de Mando Aéreo

## 1. Descripción del Gateway Central
El **Gateway Central WarNet-Radar** es el núcleo de coordinación y control del sistema de vigilancia distribuido. Funciona como un **centro de mando aéreo** que integra información de múltiples subrepositorios (Aire, Tierra, Mar, Espacio) y distribuye comandos de control para optimizar las operaciones de detección y seguimiento.

## 2. Funciones Principales del Gateway

### 2.1. Orquestación de Subrepositorios
El Gateway Central coordina las operaciones de todos los subrepositorios, asignando tareas de vigilancia, priorizando objetivos y distribuyendo recursos de manera óptima.

**Responsabilidades:**
- Recepción de telemetría de los 4 subrepositorios principales
- Fusión de datos de múltiples fuentes
- Priorización de amenazas y objetivos
- Distribución de comandos de control

### 2.2. Comunicación Bidireccional
El Gateway gestiona la comunicación en ambas direcciones: descendente (desde satélites) y ascendente (hacia satélites), garantizando una cobertura global.

**Canales de Comunicación:**
- **Primario:** LoRaWAN de largo alcance (100+ km)
- **Secundario:** Wi-Fi MIMO de alta ganancia (10-50 km)
- **Terciario:** Satelital Iridium SBD (cobertura global)

### 2.3. Procesamiento de Inteligencia
El Gateway integra algoritmos de IA para la fusión de sensores, seguimiento de objetivos y predicción de amenazas.

**Capacidades de IA:**
- Filtro de Kalman para fusión GPS/IMU
- Algoritmos de seguimiento múltiple (JPDAF)
- Clasificación de objetivos mediante redes neuronales
- Predicción de trayectorias

## 3. Arquitectura del Gateway

### 3.1. Componentes Principales
El Gateway Central se compone de los siguientes elementos:

| Componente | Función | Especificación |
| :--- | :--- | :--- |
| **Procesador Central** | Orquestación y control | ESP32-S3 o Jetson Nano |
| **Módulo LoRaWAN** | Comunicación de largo alcance | Semtech SX1262 |
| **Módulo Wi-Fi MIMO** | Comunicación de corto alcance | Dual-band 2.4/5.8 GHz |
| **Módulo Satelital** | Comunicación espacial | Iridium SBD o Starlink |
| **Almacenamiento** | Base de datos de misiones | SD Card / NVMe |
| **Antena mmWave** | Detección de largo alcance | Autodirigible, banda Ka |

### 3.2. Topología de Red
El Gateway Central actúa como un nodo central en una topología de estrella, con los subrepositorios como nodos periféricos:

```
                    ┌─────────────────────┐
                    │  WarNet-Space-Radar │
                    │  (Comunicación Sat) │
                    └──────────┬──────────┘
                               │
                    ┌──────────┴──────────┐
                    │                     │
        ┌───────────▼──────────┐  ┌──────▼──────────┐
        │ WarNet-Air-Radar     │  │ WarNet-Earth-Radar│
        │ (Aerodirigible)      │  │ (Vehículos Terr.)│
        └───────────┬──────────┘  └──────┬──────────┘
                    │                    │
                    └────────┬───────────┘
                             │
                    ┌────────▼────────┐
                    │ WarNet-Radar    │
                    │ (Gateway Central)│
                    └────────┬────────┘
                             │
                    ┌────────▼────────┐
                    │WarNet-Marine-Radar│
                    │ (Dispositivos Mar)│
                    └─────────────────┘
```

## 4. Protocolos de Control

### 4.1. Ciclo de Control del Gateway
El Gateway ejecuta un ciclo de control continuo:

1. **Recepción:** Lectura de mensajes de todos los subrepositorios
2. **Procesamiento:** Fusión de datos y análisis de amenazas
3. **Decisión:** Generación de comandos de control
4. **Transmisión:** Envío de comandos a los subrepositorios
5. **Confirmación:** Verificación de ejecución de comandos

### 4.2. Modos de Operación
El Gateway Central soporta varios modos de operación:

| Modo | Descripción | Latencia | Precisión |
| :--- | :--- | :--- | :--- |
| **VIGILANCIA** | Monitoreo continuo de zona | 1-5 seg | Media |
| **BÚSQUEDA** | Búsqueda activa de objetivo | 5-30 seg | Alta |
| **SEGUIMIENTO** | Seguimiento de objetivo conocido | 0.5-2 seg | Muy Alta |
| **EMERGENCIA** | Respuesta a amenaza inmediata | <500 ms | Crítica |

## 5. Integración con Subrepositorios

### 5.1. WarNet-Air-Radar
El Gateway Central recibe detecciones aéreas y distribuye comandos de búsqueda coordinada. La comunicación es bidireccional, permitiendo que el Gateway ajuste la orientación de la antena mmWave del aerodirigible.

### 5.2. WarNet-Earth-Radar
El Gateway coordina la vigilancia terrestre con la aérea, permitiendo que los vehículos terrestres se posicionen estratégicamente para confirmar detecciones aéreas.

### 5.3. WarNet-Marine-Radar
El Gateway integra datos marinos para vigilancia costera integrada, coordinando la detección de amenazas en la interfaz tierra-mar.

### 5.4. WarNet-Space-Radar
El Gateway utiliza el enlace satelital para comunicación global y para enviar datos consolidados a centros de mando estratégicos.

## 6. Redundancia y Continuidad Operativa
El Gateway Central implementa múltiples niveles de redundancia:

- **Redundancia de Procesador:** Dual-core con failover automático
- **Redundancia de Comunicación:** Múltiples canales (LoRa, Wi-Fi, Satelital)
- **Redundancia de Almacenamiento:** RAID-1 en SD cards
- **Sincronización de Tiempo:** NTP con referencia GPS

## 7. Conclusión
El Gateway Central WarNet-Radar es el corazón del sistema de vigilancia distribuido, permitiendo la coordinación integrada de múltiples plataformas en diferentes dominios operativos. Su arquitectura modular y escalable permite la integración de nuevos subrepositorios y la adaptación a nuevas misiones.
