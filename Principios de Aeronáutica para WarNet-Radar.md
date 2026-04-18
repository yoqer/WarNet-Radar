# Principios de Aeronáutica para WarNet-Radar

## 1. Integración en Vehículos Aéreos No Tripulados (UAV)
La integración de un sistema de radar en un UAV, especialmente en un **Aerodirigible WarNet-Air**, requiere considerar factores críticos de aeronáutica. El peso y el balance (W&B) son fundamentales para la estabilidad del vehículo, por lo que el radar debe montarse en la góndola central, cerca del centro de gravedad (CG), para evitar momentos de cabeceo (pitch) o guiñada (yaw) no deseados. Se recomienda el uso de materiales ultraligeros, como la fibra de carbono y plásticos de ingeniería, para la estructura de soporte de los 4 módulos de radar.

## 2. Aerodinámica y Resistencia (Drag)
El radar se aloja en un contenedor aerodinámico (pod) externo para minimizar la resistencia al avance. El algoritmo de vuelo del dirigible se sincroniza con el radar para realizar giros que permitan una detección de apertura sintética (SAR), mejorando la resolución a distancias de hasta 50 km. Esta técnica permite que el movimiento del propio vehículo actúe como una antena virtual de mayor tamaño, aumentando la precisión de la detección sin necesidad de componentes físicos voluminosos.

## 3. Detección y Seguimiento (GNC)
El sistema de Guía, Navegación y Control (GNC) del dirigible utiliza los datos del radar para la evitación de obstáculos y el mantenimiento de posición (loitering). La antena mmWave autodirigible permite mantener el enlace de datos con estaciones de tierra o el Gateway Central T4 mediante radio dirigido. La siguiente tabla resume las especificaciones técnicas clave del radar minimalista:

| Especificación | Valor / Descripción | Aplicación Aeronáutica |
| :--- | :--- | :--- |
| **Frecuencia** | Banda Ka (26.5-40 GHz) | Alta resolución con antenas pequeñas. |
| **Alcance** | 50 km | Detección temprana de vehículos aéreos. |
| **Consumo** | < 10W | Optimizado para alimentación solar. |
| **IA Autodirigida** | Seguimiento en cruz (45°) | Cobertura total con componentes mínimos. |

## 4. Referencias al Manual de Aeronáutica WarNet
Este documento se basa en las investigaciones del repositorio [WarNet-Air](https://github.com/yoqer/WarNet-Air), integrando los principios de **WarNet Fusion** para la fusión de sensores en la navegación autónoma. El algoritmo de vuelo estratosférico permite adaptar la detección a altitudes de hasta 37 km, donde las condiciones atmosféricas son extremas y requieren una alta fiabilidad en los componentes electrónicos y mecánicos del radar.
