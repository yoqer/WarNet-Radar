# Estructura de Subrepositorios WarNet-Radar

## Descripción General
El proyecto **WarNet-Radar** funciona como un **Gateway Central en el aire**, coordinando la comunicación bidireccional entre múltiples subrepositorios especializados. Esta estructura permite el desarrollo distribuido de sistemas de detección para diferentes dominios operativos.

## Subrepositorios Especializados

### 1. WarNet-Air-Radar
**Repositorio:** [github.com/yoqer/WarNet-Air-Radar](https://github.com/yoqer/WarNet-Air-Radar)
**Dominio:** Aire (Aerodirigibles, Drones, UAVs Estratosféricos)

Este subrepositorios contiene la investigación y desarrollo de sistemas de radar para plataformas aéreas. Incluye algoritmos de detección optimizados para altitudes estratosféricas (hasta 37 km) y comunicación de largo alcance con el Gateway Central WarNet-Radar.

**Características Principales:**
- Radar minimalista de 4 módulos y 4 amplificadores
- Antena mmWave autodirigible (banda Ka, 26.5-40 GHz)
- Detección a 50 km de vehículos aéreos
- Integración con el Aerodirigible WarNet-Air

**Referencias Cruzadas:**
- Recibe comandos de control desde WarNet-Radar (Gateway Central)
- Envía telemetría y datos de detección a WarNet-Radar
- Coordina con WarNet-Earth-Radar para vigilancia terrestre integrada

---

### 2. WarNet-Earth-Radar
**Repositorio:** [github.com/yoqer/WarNet-Earth-Radar](https://github.com/yoqer/WarNet-Earth-Radar)
**Dominio:** Tierra (Vehículos Terrestres, Robótica, Estaciones Fijas)

Este subrepositorios desarrolla sistemas de radar para plataformas terrestres, incluyendo vehículos autónomos y estaciones de vigilancia. La integración con el Gateway Central permite la coordinación de detecciones entre sistemas aéreos y terrestres.

**Características Principales:**
- Radares de corto a medio alcance (10-30 km)
- Integración con WarNet-Robot para vigilancia distribuida
- Comunicación bidireccional con el Gateway Central
- Algoritmos de fusión de sensores

**Referencias Cruzadas:**
- Recibe información de vigilancia aérea desde WarNet-Air-Radar
- Envía alertas de amenazas terrestres al Gateway Central
- Coordina con WarNet-Marine-Radar en zonas costeras

---

### 3. WarNet-Marine-Radar
**Repositorio:** [github.com/yoqer/WarNet-Marine-Radar](https://github.com/yoqer/WarNet-Marine-Radar)
**Dominio:** Mar (Dispositivos Marítimos de Superficie y Submarinos)

Este subrepositorios contiene la investigación de sistemas de radar para entornos marinos, incluyendo detección de superficie y sistemas submarinos. La comunicación con el Gateway Central permite la vigilancia integrada de zonas costeras y oceánicas.

**Características Principales:**
- Radares de detección de superficie marina (20-100 km)
- Sistemas de comunicación submarina
- Integración con boyas y plataformas flotantes
- Algoritmos de compensación de movimiento marino

**Referencias Cruzadas:**
- Recibe comandos de vigilancia desde el Gateway Central
- Envía datos de tráfico marítimo y amenazas submarinas
- Coordina con WarNet-Space-Radar para vigilancia orbital

---

### 4. WarNet-Space-Radar
**Repositorio:** [github.com/yoqer/WarNet-Space-Radar](https://github.com/yoqer/WarNet-Space-Radar)
**Dominio:** Espacio (Satélites, Monitorización Orbital, Comunicaciones de Largo Alcance)

Este subrepositorios desarrolla sistemas de comunicación y detección para aplicaciones espaciales. Actúa como el enlace de largo alcance del Gateway Central, permitiendo la comunicación con satélites y sistemas de monitorización orbital.

**Características Principales:**
- Comunicación satelital (Iridium, Starlink, constelaciones propias)
- Monitorización de órbitas y trayectorias
- Enlace de datos de largo alcance (>1000 km)
- Integración con sistemas de navegación GNSS

**Referencias Cruzadas:**
- Proporciona enlace de comunicación de largo alcance al Gateway Central
- Recibe datos consolidados de todos los subrepositorios
- Permite la comunicación global y coordinación estratégica

---

## Flujo de Comunicación Bidireccional

```
┌─────────────────────────────────────────────────────────────┐
│                   WarNet-Radar (Gateway Central)             │
│                    (Centro de Mando Aéreo)                   │
└─────────────────────────────────────────────────────────────┘
         ↑                    ↑                    ↑
         │                    │                    │
    Comandos              Comandos             Comandos
    Control               Control              Control
         │                    │                    │
         ↓                    ↓                    ↓
┌──────────────────┐ ┌──────────────────┐ ┌──────────────────┐
│ WarNet-Air-Radar │ │WarNet-Earth-Radar│ │WarNet-Marine-Radar│
│   (Aerodirigible)│ │  (Vehículos Terr.)│ │  (Dispositivos Mar)│
└──────────────────┘ └──────────────────┘ └──────────────────┘
         ↑                    ↑                    ↑
         │                    │                    │
    Telemetría           Telemetría            Telemetría
    Detecciones          Detecciones           Detecciones
         │                    │                    │
         └────────────────────┴────────────────────┘
                        ↓
              ┌──────────────────────┐
              │ WarNet-Space-Radar   │
              │ (Comunicación Espacial)│
              └──────────────────────┘
                        ↑
                        │
              Enlace de Largo Alcance
              (Satelital/Iridium)
```

## Protocolo de Comunicación
Todos los subrepositorios utilizan un protocolo de comunicación estandarizado basado en JSON para garantizar la interoperabilidad. El Gateway Central (WarNet-Radar) actúa como el orquestador central, recibiendo datos de todos los subrepositorios y distribuyendo comandos de control.

## Integración y Despliegue
Para integrar un nuevo subrepositorios o realizar modificaciones, consulta la documentación de cada repositorio específico. El Gateway Central mantiene una lista actualizada de versiones compatibles y proporciona herramientas de validación para asegurar la interoperabilidad.
