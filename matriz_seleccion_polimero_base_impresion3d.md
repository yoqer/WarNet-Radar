# Matriz de selección del polímero base para impresión 3D y recubrimiento funcional civil

> **Alcance**
>
> Esta matriz está pensada para aplicaciones **civiles**: carcasas técnicas, paneles de apantallamiento EMC, útiles antiestáticos, prototipos funcionales y piezas que después recibirán un **recubrimiento funcional**. No está pensada para optimización militar ni para evasión de radares.

---

## 1. Criterios de selección

La elección del polímero base no depende solo del material, sino también de la **tecnología de impresión**. La literatura y las guías técnicas coinciden en que cada proceso impone requisitos distintos:

- **FDM/FFF** necesita termoplásticos con reología y comportamiento térmico adecuados para extrusión y adhesión entre capas. [Springer Link](https://link.springer.com/article/10.1186/s42252-021-00020-6)
- **SLA/DLP/LCD** requiere resinas fotocurables de baja viscosidad y curado rápido bajo luz. [Springer Link](https://link.springer.com/article/10.1186/s42252-021-00020-6)
- **SLS/MJF** trabaja con polvos termoplásticos y destaca en piezas funcionales, isotropía y geometrías complejas sin soportes. [Formlabs](https://formlabs.com/blog/fdm-vs-sla-vs-sls-how-to-choose-the-right-3d-printing-technology/) [PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC8470301/)
- **DIW/pasta** exige formulaciones reofluidificantes o con esfuerzo de fluencia para mantener forma tras deposición. [Springer Link](https://link.springer.com/article/10.1186/s42252-021-00020-6)

---

## 2. Regla rápida de decisión

- Si priorizas **coste bajo y facilidad** → **FDM/FFF**.
- Si priorizas **superficie, precisión y estanqueidad** → **SLA/DLP**.
- Si priorizas **pieza funcional robusta, sin soportes y con buena repetibilidad** → **SLS/MJF**. [Formlabs](https://formlabs.com/blog/fdm-vs-sla-vs-sls-how-to-choose-the-right-3d-printing-technology/)

Para una pieza que luego llevará un recubrimiento funcional, normalmente conviene priorizar:

1. **estabilidad dimensional**,
2. **adhesión superficial**,
3. **baja absorción de humedad**,
4. **resistencia química/temperatura**,
5. **acabado superficial compatible con coating**.

---

## 3. Matriz maestra por tecnología y polímero base

| Tecnología | Polímero / familia | Ventajas principales | Riesgos / límites | Mejor uso como sustrato para recubrimiento funcional | Valoración global |
|---|---|---|---|---|---|
| FDM/FFF | **PLA** | Muy fácil de imprimir, barato, buena precisión visual | Frágil, baja resistencia térmica, peor durabilidad | Solo prototipos rápidos y validación geométrica | **Baja** |
| FDM/FFF | **PETG** | Equilibrado, buena resistencia química y humedad, fácil de imprimir | Menor rigidez térmica que PC/PA, acabado menos técnico | Carcasas, cajas, prototipos funcionales de coste medio | **Alta** |
| FDM/FFF | **ABS** | Más tenaz y térmicamente mejor que PLA, buen postproceso | Deformación, vapores, peor estabilidad UV | Piezas funcionales de interior y utillaje | **Media-Alta** |
| FDM/FFF | **ASA** | Similar a ABS pero mejor UV y mejor acabado superficial | Requiere cámara y control térmico | Carcasas expuestas, exterior, envolventes técnicas | **Alta** |
| FDM/FFF | **PA / Nylon** | Muy buena resistencia mecánica e impacto | Absorbe humedad, impresión más delicada | Piezas de ingeniería y soportes exigentes | **Alta** si controlas humedad |
| FDM/FFF | **TPU** | Flexible, resistente a impacto y abrasión | Difícil de imprimir y de recubrir uniformemente | Juntas, insertos, amortiguación, protección blanda | **Media** |
| FDM/FFF | **PC** | Muy fuerte, buena resistencia térmica | Exigente de imprimir, sensible a UV en algunos casos | Carcasas técnicas de alto rendimiento | **Alta** |
| FDM/FFF | **PEI / ULTEM / PEKK / PEEK** | Muy alta temperatura, química y rigidez | Muy alto coste, impresoras industriales | Aplicaciones extremas, aero/industrial avanzada | **Muy alta** |
| SLA/DLP | **Standard resin** | Muy buen detalle y acabado | Más frágil, menos robusta a largo plazo | Maquetas funcionales, ajuste, validación de geometría | **Media** |
| SLA/DLP | **Tough / Durable** | Mejor resistencia a impacto/fatiga, piezas funcionales finas | Sigue siendo termoestable, sensibilidad ambiental según formulación | Carcasas finas, clips, prototipos de uso | **Alta** |
| SLA/DLP | **Rigid** | Alta rigidez y estabilidad | Más frágil que Tough | Componentes de precisión y fijación | **Alta** |
| SLA/DLP | **Flexible / Elastic** | Deformación elástica, tacto gomoso | Menor estabilidad dimensional, coating más delicado | Sellos, grips, protección blanda | **Media** |
| SLA/DLP | **High Temp** | Buena resistencia térmica | Menor tenacidad | Herramentales ligeros, piezas cerca de calor | **Alta** |
| SLA/DLP | **ESD / FR / biocompatible** | Función especializada | Coste mayor, propiedades específicas a validar | Electrónica, seguridad, médico | **Muy alta** si el caso lo exige |
| SLS / MJF | **PA12** | El estándar funcional: precisión, detalle, robustez, baja humedad relativa comparado con otras PA | Superficie más porosa/rugosa que SLA | Excelente base para paneles, carcasas, series cortas | **Muy alta** |
| SLS / MJF | **PA11** | Más dúctil e impact-resistant, bio-based | Algo menos rígido/estable que PA12 en ciertos casos | Snap-fits, piezas sometidas a golpe/fatiga | **Muy alta** |
| SLS / MJF | **PP** | Baja absorción de humedad, buena resistencia química, soldable | Menor rigidez que PA12 | Depósitos, fluidos, carcasas químicamente expuestas | **Alta** |
| SLS / MJF | **TPU / TPE** | Flexible y durable | Menor estabilidad geométrica que PA12/PA11 | Amortiguación, sellado, impacto | **Alta** para piezas blandas |
| SLS / MJF | **PA12 con vidrio / cargados** | Alta rigidez y estabilidad dimensional | Más fragilidad relativa, posproceso menos amable | Utillaje, soportes, geometrías estables | **Muy alta** |
| SLS industrial | **PAEK / PEKK / PEEK** | Máximo nivel térmico y químico | Coste y acceso muy altos | Entornos severos, industrial avanzado | **Muy alta** |
| DIW / pasta | **Siliconas, uretanos, resinas cargadas, mezclas personalizadas** | Máxima libertad de formulación | Desarrollo complejo de reología y curado | I+D, recubrimientos funcionales, tintas | **Variable** |

Fuentes base para esta matriz: [Hubs](https://www.hubs.com/knowledge-base/fdm-3d-printing-materials-compared/) [Formlabs](https://formlabs.com/blog/fdm-vs-sla-vs-sls-how-to-choose-the-right-3d-printing-technology/) [HP](https://www.hp.com/us-en/printers/3d-printers/materials.html) [EOS](https://www.eos.info/polymer-solutions/polymer-materials) [Stratasys](https://www.stratasys.com/en/materials/materials-catalog/fdm-materials/) [PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC8470301/)

---

## 4. Matriz práctica por tipo de impresora

### 4.1 Impresoras FDM/FFF de escritorio

| Prioridad | Mejor opción | Segunda opción | Evitar si el recubrimiento es crítico |
|---|---|---|---|
| Facilidad y bajo coste | **PETG** | PLA | TPU blando, Nylon sin secado |
| Exterior / UV | **ASA** | PETG | ABS si habrá intemperie |
| Resistencia mecánica general | **PC** o **PA** | ASA | PLA |
| Prototipo rápido de concepto | **PLA** | PETG | PC/PA si no hace falta |
| Base para coating técnico civil | **PETG** | ASA / PC | PLA salvo pruebas rápidas |

**Lectura práctica:** en FDM de escritorio, **PETG** suele ser la mejor puerta de entrada si quieres algo imprimible, razonablemente estable y compatible con un recubrimiento posterior. **ASA** gana si habrá exposición UV o exterior. **PC** gana si la impresora está bien cerrada y controlada. [Hubs](https://www.hubs.com/knowledge-base/fdm-3d-printing-materials-compared/)

### 4.2 Impresoras FDM industriales

| Caso de uso | Opción recomendada | Justificación |
|---|---|---|
| Carcasa técnica exigente | **PC** | Durabilidad y temperatura superiores |
| Exterior + intemperie | **ASA** | Resistencia UV y buen acabado |
| Rigidez alta y bajo peso | **Nylon 12CF** | Alta rigidez específica | 
| Alta temperatura / química | **ULTEM 1010 / 9085** | Rendimiento extremo |
| Electrónica sensible | **ABS-ESD / PC-ESD** | Disipación electrostática |

Stratasys posiciona precisamente ASA, PC, Nylon 12CF y ULTEM como familias FDM industriales de referencia para piezas funcionales y utillaje. [Stratasys](https://www.stratasys.com/en/materials/materials-catalog/fdm-materials/)

### 4.3 Impresoras SLA / DLP / LCD de resina

| Objetivo | Familia de resina base | Cuándo elegirla |
|---|---|---|
| Máximo detalle visual | **Standard** | Maquetas, estética, validación fina |
| Prototipo funcional resistente | **Tough / Durable** | Clips, tapas, carcasas finas |
| Alta rigidez dimensional | **Rigid** | Piezas de precisión, soportes |
| Flexibilidad | **Flexible / Elastic** | Sellos, grips, piezas blandas |
| Calor | **High Temp** | Proximidad a fuentes térmicas |
| Electrónica / ESD | **ESD** | Bandejas, útiles, alojamientos de PCB |
| Seguridad / fuego | **Flame Retardant** | Aplicaciones reguladas |
| Sanitario | **Biocompatible** | Dental, guías, contacto indirecto permitido |

Las guías de Formlabs y la comparación FDM/SLA/SLS sitúan SLA como mejor opción cuando necesitas **acabado superficial, tolerancias, estanqueidad e isotropía**. [Formlabs](https://formlabs.com/blog/fdm-vs-sla-vs-sls-how-to-choose-the-right-3d-printing-technology/) [formlabs.com](https://formlabs.com/compare/materials/)

**Recomendación práctica para coating:** si buscas una superficie muy uniforme para aplicar recubrimiento fino, las mejores candidatas suelen ser **Tough/Durable** o **Rigid**, no las standard más frágiles.

### 4.4 Impresoras SLS / MJF de polvo polimérico

| Objetivo | Mejor material base | Alternativa | Comentario |
|---|---|---|---|
| Uso general funcional | **PA12** | PA11 | El estándar más equilibrado |
| Impacto y ductilidad | **PA11** | TPU | Mejor para fatiga y snap-fits |
| Química / humedad baja | **PP** | PA12 | Muy útil en fluidos y ambientes húmedos |
| Flexibilidad | **TPU** | TPE | Ideal para piezas blandas |
| Máxima estabilidad dimensional | **PA12 GB** | cargados equivalentes | Muy útil para utillaje |

HP sitúa **PA12** como su material funcional todoterreno; **PA11** como la versión más dúctil; **PP** para resistencia química y baja humedad; **TPU** para elasticidad; y **PA12 GB** para rigidez/estabilidad dimensional. [HP](https://www.hp.com/us-en/printers/3d-printers/materials.html)

EOS, por su parte, refuerza el posicionamiento de **PA11, PA12, TPU** y materiales de altas prestaciones como **PAEK** para aplicaciones industriales avanzadas. [EOS](https://www.eos.info/polymer-solutions/polymer-materials)

---

## 5. Recomendación específica si el objetivo es aplicar un recubrimiento funcional civil

### Mejor elección por tecnología

| Tecnología disponible | Mejor sustrato base recomendado | Motivo |
|---|---|---|
| Solo FDM doméstica | **PETG** | equilibrio entre facilidad, humedad y funcionalidad |
| FDM cerrada / semindustrial | **ASA** o **PC** | mejor durabilidad, calor y acabado técnico |
| SLA profesional | **Tough/Durable** o **Rigid** | superficie excelente y buena estabilidad |
| SLS/MJF | **PA12** | mejor equilibrio global para pieza funcional recubierta |
| SLS/MJF con impacto/flexión | **PA11** | más ductilidad |
| Piezas blandas | **TPU** | absorción, sellado, flexibilidad |

### Ranking general de “mejor base para recubrimiento”

1. **PA12 (SLS/MJF)**
2. **PA11 (SLS/MJF)**
3. **Rigid o Tough resin (SLA)**
4. **ASA (FDM)**
5. **PC (FDM industrial o bien controlada)**
6. **PETG (FDM escritorio/semipro)**
7. **TPU** solo cuando la flexibilidad es requisito
8. **PLA** solo para pruebas de concepto

---

## 6. Elección según escenario real

### Escenario A — Tengo una impresora FDM de escritorio

Elige **PETG** si quieres la ruta más equilibrada. Pasa a **ASA** si la pieza verá exterior o radiación UV. Sube a **PC** si necesitas más temperatura y tu impresora realmente puede controlarlo. [Hubs](https://www.hubs.com/knowledge-base/fdm-3d-printing-materials-compared/)

### Escenario B — Tengo una impresora de resina

Elige **Tough/Durable** para piezas funcionales o **Rigid** para piezas dimensionalmente críticas. Si el interés principal es el acabado superficial antes del coating, SLA es excelente. [Formlabs](https://formlabs.com/blog/fdm-vs-sla-vs-sls-how-to-choose-the-right-3d-printing-technology/) [formlabs.com](https://formlabs.com/compare/materials/)

### Escenario C — Puedo mandar fabricar en SLS o MJF

Elige **PA12** como apuesta segura. Si la pieza necesita más deformación sin rotura, elige **PA11**. Si debe resistir químicos y humedad con menor absorción, valora **PP**. [HP](https://www.hp.com/us-en/printers/3d-printers/materials.html) [EOS](https://www.eos.info/polymer-solutions/polymer-materials)

---

## 7. Mi recomendación final resumida

Si tu objetivo es desarrollar una pieza impresa para luego aplicarle un recubrimiento funcional civil, mi recomendación por orden práctico sería:

- **PA12 (SLS/MJF)** si tienes acceso a servicio o máquina industrial.
- **ASA** si imprimes en FDM y la pieza debe ser técnica y estable al exterior.
- **PETG** si estás en FDM de escritorio y quieres minimizar problemas.
- **Tough/Rigid resin** si tu prioridad es acabado superficial y precisión antes del coating.

---

## 8. Enlaces activos

- [Springer Link – 3D printing of graphene-based polymeric nanocomposites for smart materials](https://link.springer.com/article/10.1186/s42252-021-00020-6)
- [Formlabs – FDM vs SLA vs SLS](https://formlabs.com/blog/fdm-vs-sla-vs-sls-how-to-choose-the-right-3d-printing-technology/)
- [Formlabs – Materials comparison](https://formlabs.com/compare/materials/)
- [PMC – Review of polymer 3D printing processes](https://pmc.ncbi.nlm.nih.gov/articles/PMC8470301/)
- [Hubs – FDM materials compared](https://www.hubs.com/knowledge-base/fdm-3d-printing-materials-compared/)
- [HP – 3D printing materials portfolio](https://www.hp.com/us-en/printers/3d-printers/materials.html)
- [EOS – Polymer materials](https://www.eos.info/polymer-solutions/polymer-materials)
- [Stratasys – FDM materials catalog](https://www.stratasys.com/en/materials/materials-catalog/fdm-materials/)
