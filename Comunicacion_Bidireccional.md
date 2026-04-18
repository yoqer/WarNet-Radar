# Comunicación Bidireccional Tierra-Espacio en WarNet-Radar

## 1. Introducción al Sistema de Comunicación
El **Gateway Central WarNet-Radar** actúa como el hub de comunicación bidireccional entre plataformas terrestres, marinas, aéreas y espaciales. Este sistema permite la coordinación en tiempo real de operaciones de detección y vigilancia en múltiples dominios, integrando señales desde fuentes espaciales (satélites, constelaciones) hasta sistemas terrestres localizados.

## 2. Arquitectura de Comunicación Bidireccional

### 2.1. Enlace Descendente (Downlink): Espacio → Tierra
El enlace descendente transmite datos desde satélites y sistemas espaciales hacia el Gateway Central. Esta comunicación proporciona información de largo alcance, cobertura global y redundancia en la comunicación.

**Características Principales:**
- Frecuencia: Banda L (1.5-1.7 GHz) para Iridium, banda S (2-4 GHz) para Starlink
- Latencia: 100-500 ms (satélites geoestacionarios), 20-50 ms (órbita baja)
- Ancho de banda: 2.4 kbps (Iridium) a 100 Mbps (Starlink)
- Redundancia: Múltiples satélites en constelación

### 2.2. Enlace Ascendente (Uplink): Tierra → Espacio
El enlace ascendente transmite comandos y datos desde el Gateway Central hacia los sistemas espaciales. Esta comunicación es crítica para el control remoto y la coordinación estratégica.

**Características Principales:**
- Frecuencia: Banda L (1.6-1.7 GHz) para Iridium, banda S (2-4 GHz) para Starlink
- Potencia: 5-10W (satélites de órbita baja), 100-500W (geoestacionarios)
- Modulación: QPSK, 16-QAM (según disponibilidad)
- Tasa de datos: 1.2-9.6 kbps (Iridium), hasta 100 Mbps (Starlink)

## 3. Protocolos de Comunicación

### 3.1. Formato de Mensaje Estándar
Todos los mensajes en el sistema WarNet-Radar siguen un formato JSON estandarizado para garantizar la interoperabilidad entre subrepositorios:

```json
{
  "header": {
    "timestamp": "2026-03-13T14:30:00Z",
    "source": "WarNet-Air-Radar",
    "destination": "WarNet-Radar-Gateway",
    "message_id": "MSG-2026-001234",
    "priority": "HIGH"
  },
  "payload": {
    "type": "DETECTION",
    "data": {
      "target": "Aircraft",
      "latitude": 40.7128,
      "longitude": -74.0060,
      "altitude": 8500,
      "range": 45.2,
      "bearing": 123.5,
      "velocity": 450,
      "confidence": 0.95
    }
  },
  "signature": "SHA256_HASH"
}
```

### 3.2. Tipos de Mensajes
El sistema define varios tipos de mensajes para diferentes operaciones:

| Tipo de Mensaje | Origen | Destino | Descripción |
| :--- | :--- | :--- | :--- |
| **DETECTION** | Subrepositorios | Gateway Central | Reporte de detección de objetivo. |
| **COMMAND** | Gateway Central | Subrepositorios | Comando de control o cambio de modo. |
| **TELEMETRY** | Subrepositorios | Gateway Central | Datos de estado y salud del sistema. |
| **ALERT** | Subrepositorios | Gateway Central | Alerta de amenaza o anomalía. |
| **HEARTBEAT** | Subrepositorios | Gateway Central | Confirmación de conectividad. |
| **SYNC** | Gateway Central | Subrepositorios | Sincronización de tiempo y estado. |

## 4. Flujo de Comunicación Integrada

### 4.1. Escenario de Vigilancia Aérea Integrada
Un ejemplo de flujo completo de comunicación bidireccional:

1. **Detección Inicial:** El WarNet-Air-Radar detecta un objetivo a 50 km.
2. **Reporte al Gateway:** Envía un mensaje DETECTION al Gateway Central WarNet-Radar.
3. **Distribución de Inteligencia:** El Gateway distribuye la información a WarNet-Earth-Radar y WarNet-Marine-Radar.
4. **Búsqueda Coordinada:** Los subrepositorios terrestres y marinos buscan confirmación del objetivo.
5. **Consolidación de Datos:** El Gateway centraliza los datos de múltiples fuentes.
6. **Transmisión Espacial:** El WarNet-Space-Radar transmite la información consolidada a satélites para vigilancia global.
7. **Comandos de Control:** El Gateway envía comandos COMMAND a los subrepositorios para ajustar la búsqueda.

### 4.2. Redundancia y Failover
El sistema implementa múltiples caminos de comunicación para garantizar la continuidad operativa:

- **Enlace Primario:** LoRaWAN de largo alcance (100+ km)
- **Enlace Secundario:** Wi-Fi MIMO de alta ganancia (10-50 km)
- **Enlace Terciario:** Comunicación satelital Iridium (cobertura global)

## 5. Seguridad y Encriptación
Todos los mensajes se encriptan utilizando **AES-256** para garantizar la confidencialidad. Se implementa autenticación basada en certificados X.509 para verificar la identidad de los nodos.

## 6. Latencia y Sincronización
La sincronización de tiempo es crítica para la correlación de datos entre subrepositorios. El sistema utiliza **NTP (Network Time Protocol)** con referencias de GPS para mantener una precisión de ±100 ms.

## 7. Conclusión
La arquitectura de comunicación bidireccional de WarNet-Radar permite una vigilancia integrada y coordinada en múltiples dominios. La flexibilidad del sistema permite la adaptación a nuevos subrepositorios y la integración de tecnologías emergentes de comunicación satelital.
