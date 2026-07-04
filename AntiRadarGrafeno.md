Estudio técnico, basado en fuentes abiertas, sobre qué se sabe públicamente de ese material portugués, 
cómo encajaría en impresión 3D desde la ciencia de materiales, qué patentes y papers existen, 
y cómo se compara a alto nivel con soluciones públicas relacionadas con el [F-35](https://www.lockheedmartin.com/en-us/products/f-35.html).  



## 1) Qué dice realmente el artículo sobre [GTechPlasma](http://www.gtechplasma.com/) y el material

La noticia que enlazas procede en esencia de [Euronews](https://www.euronews.com/next/2026/06/30/from-lab-to-sky-portuguese-graphene-that-hides-jets-and-drones-may-transform-defence): el proyecto lo lidera [GTechPlasma](http://www.gtechplasma.com/), una spin-off del Instituto de Plasmas e Fusão Nuclear del [Instituto Superior Técnico](https://tecnico.ulisboa.pt/), y la industrialización la llevaría [Plasmaphene](https://plasmaphene.com/), en Vila Viçosa. La empresa afirma que su sistema de plasma produce grafeno “personalizado” a partir de precursores como alcohol etílico o metano, y que el material actual sale como un polvo negro muy ligero con intención de evolucionar hacia recubrimientos y pinturas aplicables sobre superficies. La afirmación de “hacer casi invisibles” drones o reducir la firma radar de un F-16 a la de un pájaro aparece en las fuentes como una estimación de la empresa, no como un resultado independiente publicado con protocolo abierto de medida de RCS. [Euronews](https://www.euronews.com/next/2026/06/30/from-lab-to-sky-portuguese-graphene-that-hides-jets-and-drones-may-transform-defence) [Innovation News Network](https://www.innovationnewsnetwork.com/portugal-developing-graphene-materials-for-stealth-technology/71158/)

Un dato industrial relevante es que, según esas fuentes, sus equipos ya producen 40 mg/min de grafeno de alta calidad y ya habrían suministrado 260 g de material absorbente de radar a un fabricante portugués de drones. Eso sugiere que, al menos hoy, el formato de salida es un feedstock funcional en polvo, no una pieza final ni un filamento comercial para FDM listo para enchufar a una impresora. [Euronews](https://www.euronews.com/next/2026/06/30/from-lab-to-sky-portuguese-graphene-that-hides-jets-and-drones-may-transform-defence)



## 2) Qué se sabe públicamente de la composición y la plataforma de síntesis

La familia de patentes más alineada con esa noticia no describe una “pintura furtiva final” cerrada, sino una plataforma de síntesis por plasma para fabricar grafeno y otras nanoestructuras 2D. La patente [EP3455389B1](https://patents.google.com/patent/EP3455389B1/pt) (“Process for fabrication of graphene using plasma technology”) cita como inventores a Elena Tatarova, Júlio Henriques, Luís Lemos Alves y Bruno Soares Gonçalves; el cesionario es la [Universidade de Lisboa](https://www.ulisboa.pt/). 
Publica gases inertes como helio, neón, argón, criptón o xenón, y precursores gaseosos como metano, etileno o acetileno; también precursores líquidos como etanol, propanol, butanol o metanol. [Google Patents](https://patents.google.com/patent/EP3455389B1/pt)

La patente hermana [WO2017196198A2](https://patents.google.com/patent/WO2017196198A2/pt) amplía la arquitectura del sistema: reactor de plasma de microondas con una zona de lanzamiento de onda superficial, una zona transitoria de formación de plasma y una zona de nucleación; además contempla enfriamiento externo y radiación IR/UV para controlar gradientes espaciales de temperatura y velocidad del flujo. En abierto, esto es importante porque te dice dónde está la “ventaja”: no tanto en una receta química trivial, sino en el control fino del crecimiento y dopado del material a escala atómica. [Google Patents](https://patents.google.com/patent/WO2017196198A2/pt)

En composición funcional, la propia patente no se limita al grafeno puro. También menciona derivados como N-grafeno y F-grafeno, además de germaneno y nitruro de boro hexagonal. Ese punto encaja muy bien con un paper posterior del mismo ecosistema, “[Plasma-Driven Tuning of Dielectric Permittivity in Graphene](https://pubmed.ncbi.nlm.nih.gov/38533978/)”, donde el grupo reporta láminas de grafeno dopadas con nitrógeno con permitividad ajustable entre 1 y 40 GHz, incluyendo valores subunitarios e incluso negativos en banda Ka (30–40 GHz), asociándolo a excitaciones plasmónicas superficiales 2D de baja energía. Traducido a ingeniería: el interés no sería solo “meter grafeno”, sino usar grafeno dopado y estructuralmente controlado para modular respuesta electromagnética. [PubMed](https://pubmed.ncbi.nlm.nih.gov/38533978/)



## 3) Qué ofrece la empresa y cómo encaja [Plasmaphene](https://plasmaphene.com/)

La página histórica de [GTechPlasma](http://www.ipfn.tecnico.ulisboa.pt/gtechplasma/index.html) se presenta como productora de materiales basados en grafeno “de alta calidad, personalizados y con propiedades mejoradas” mediante una tecnología de plasma versátil, coste-efectiva y ambientalmente favorable. Es decir: venden plataforma de material, no solo un único producto final. [IPFN/GTechPlasma](http://www.ipfn.tecnico.ulisboa.pt/gtechplasma/index.html)

[Plasmaphene](https://plasmaphene.com/) se posiciona precisamente donde tú estás preguntando: industrializar grafeno y derivados para que fabricantes mejoren productos sin cambiar sus líneas de producción. En su web destacan aplicaciones en coatings & paints, polymers & rubbers y surface engineering. Eso refuerza la lectura técnica de que el camino más realista de adopción no es imprimir “grafeno puro”, sino integrarlo como aditivo funcional en polímeros, cauchos, resinas o recubrimientos. [Plasmaphene](https://plasmaphene.com/)



## 4) Cómo combinarlo con impresión 3D sin entrar en usos furtivos

Si nos ceñimos a ciencia de materiales y fabricación aditiva civil, este tipo de grafeno encaja mejor en **dos rutas**. La primera es la ruta “bulk”: convertir el polvo en masterbatch o compuesto imprimible con un polímero base. La segunda es la ruta “post-proceso”: imprimir la geometría con un polímero adecuado y luego aplicar un recubrimiento funcional sobre la pieza. Dado que el artículo dice que el material hoy se obtiene como polvo y que la empresa quiere evolucionar a pinturas/recubrimientos, la segunda ruta parece la más madura a corto plazo; la primera exige resolver dispersión, reología y repetibilidad de procesado. [Euronews](https://www.euronews.com/next/2026/06/30/from-lab-to-sky-portuguese-graphene-that-hides-jets-and-drones-may-transform-defence) [Plasmaphene](https://plasmaphene.com/)

La revisión abierta de [Springer](https://link.springer.com/article/10.1186/s42252-021-00020-6) sobre impresión 3D de nanocompuestos poliméricos con grafeno resume bien el estado del arte: las técnicas más usadas son FDM, DIW, SLS y SLA; los rellenos más comunes son grafeno, GO, rGO y nanoplaquetas de grafeno; y el problema central casi siempre es el mismo, la dispersión homogénea del nanorrelleno sin destruir la procesabilidad. La revisión también remarca tres rutas de preparación: mezcla en solución, mezcla en fundido e in-situ polymerization. [Springer Link](https://link.springer.com/article/10.1186/s42252-021-00020-6)

Eso significa que, para una integración seria en impresión 3D, el cuello de botella no es “tener grafeno”, sino responder cuatro preguntas de ingeniería:

1) con qué matriz lo mezclas,
2) cómo evitas aglomerados,
3)  cómo mantienes una viscosidad o fluidez imprimible,
    4) y cómo aseguras que la mejora funcional compense la pérdida potencial de adhesión entre capas, ductilidad o consistencia dimensional. [Springer Link](https://link.springer.com/article/10.1186/s42252-021-00020-6)



## 5) Qué matrices y procesos tendrían más sentido

Para FDM/FFF, las matrices más naturales son termoplásticos procesables en filamento o pellet: TPU si buscas flexibilidad y absorción de vibración, PA12/PA6 si te importa resistencia térmica y mecánica, y en menor medida PLA/PETG para prototipos funcionales rápidos. Para DIW, la ventaja es mayor libertad reológica: puedes formular pastas o tintas cargadas, pero necesitas que el sistema sea pseudoplástico y mantenga forma tras deposición. Para SLA/DLP, el reto es todavía más duro porque el relleno puede afectar la fotopolimerización y la penetración óptica. Esta lectura no sale del artículo de prensa, sino del consenso técnico de la revisión sobre grafeno en AM. [Springer Link](https://link.springer.com/article/10.1186/s42252-021-00020-6)

Mi conclusión técnica es que, si el material portugués llega al mercado en forma de polvo funcional o de pintura, su primer encaje realista en impresión 3D civil no será un “filamento milagroso”, sino una de estas dos opciones: un compuesto con baja o moderada fracción de grafeno para dotar de conductividad/apantallamiento/robustez superficial a una matriz polimérica, o un sistema híbrido en el que la pieza se imprime para obtener geometría y luego se recubre para aportar la función electromagnética. Esa separación entre “geometría” y “función EM” es, industrialmente, mucho más robusta. [Plasmaphene](https://plasmaphene.com/) [Springer Link](https://link.springer.com/article/10.1186/s42252-021-00020-6)



## 6) Lo más importante: en absorción EM la geometría importa tanto como el material

Un error común es pensar que basta con subir el porcentaje de carga conductiva. La literatura abierta sobre absorbedores impresos en 3D muestra que la **arquitectura** es tan importante como la composición. El artículo de [MDPI](https://www.mdpi.com/2073-4360/14/22/4960) sobre TPU con polvo de hierro carbonílico impresos en 3D muestra que estructuras tipo panal y, sobre todo, piramidales mejoran la absorción al adaptar mejor la impedancia y favorecer múltiples reflexiones internas; en ese trabajo, la geometría piramidal fue la más eficaz y amplió muchísimo la banda de absorción. [MDPI](https://www.mdpi.com/2073-4360/14/22/4960)

La lección trasladable a tu pregunta no es “usa tal porcentaje y tal forma para esconder drones” —eso no te lo voy a dar—, sino esta: si el objetivo civil es apantallamiento EM, compatibilidad EMC o paneles absorbentes para laboratorio, una pieza impresa con geometría gradiente o celular y luego funcionalizada con grafeno puede ser más sensata que intentar que toda la masa del polímero sea hipercargada de nanorrelleno. Menos peso, mejor procesado y más libertad de diseño. [MDPI](https://www.mdpi.com/2073-4360/14/22/4960) [Springer Link](https://link.springer.com/article/10.1186/s42252-021-00020-6)



## 7) Comparativa de alto nivel con soluciones públicas relacionadas con el [F-35](https://www.lockheedmartin.com/en-us/products/f-35.html)

No hay composición pública completa y verificable del material furtivo real del F-35; además, la propia noticia subraya que ese tipo de material no se exporta. Por tanto, una comparación honesta solo puede hacerse contra **fuentes públicas indirectas**: patentes abiertas y descripciones generales, no contra la formulación real de producción del F-35. [Euronews](https://www.euronews.com/next/2026/06/30/from-lab-to-sky-portuguese-graphene-that-hides-jets-and-drones-may-transform-defence)

| Sistema público comparable | Fase activa principal | Formato | Filosofía de fabricación | Lo que aporta |
|---|---|---|---|---|
| [GTechPlasma / patentes EP3455389B1 y WO2017196198A2](https://patents.google.com/patent/EP3455389B1/pt) | Grafeno y derivados, incluido N-grafeno | Polvo / flakes / feedstock para formulación | Síntesis por plasma de microondas y control atómico del material | Plataforma de material ajustable desde el origen |
| [Lockheed Martin – US20100271253A1](https://patents.google.com/patent/US20100271253A1/en) | CNT sobre fibras dentro de una matriz | Compuesto estructural multicapa | Integrar control de firma en la propia estructura, no solo como pintura | Gradiente de CNT para reducir reflexión y disipar energía |
| [Leonardo – WO2019167009A1](https://patents.google.com/patent/WO2019167009A1/en) | Nanoplaquetas de grafeno | Laminado multicapa aeronáutico | Fibras no conductoras rociadas con GNP + infusión de resina | Bloque reflector + bloque absorbedor + bloque adaptador de impedancia |

La comparación clave es esta: el enfoque portugués parece empezar “desde el material”, es decir, controlar la síntesis del grafeno/dopado; la patente pública de Lockheed se centra en integrar CNT en fibras estructurales con gradientes; y la de Leonardo describe un laminado con nanoplaquetas de grafeno dentro de un apilado aeronáutico clásico. Si lo miras desde fabricación aditiva, el enfoque portugués sería el más transferible a compuestos imprimibles o recubrimientos funcionales; el de Lockheed está más pegado a compuestos estructurales avanzados; y el de Leonardo encaja mejor con paneles/laminados compuestos que con impresión 3D pura. [Google Patents](https://patents.google.com/patent/US20100271253A1/en) [Google Patents](https://patents.google.com/patent/WO2019167009A1/en) [Google Patents](https://patents.google.com/patent/EP3455389B1/pt)



## 8) Qué puede inferirse de la “composición” del F-35 desde fuentes públicas

La mejor fuente pública que encontré para comparación técnica no es una ficha del F-35, sino la patente de [Lockheed Martin US20100271253A1](https://patents.google.com/patent/US20100271253A1/en). Ahí se describe un compuesto absorbente basado en tres elementos: fibras de soporte, nanotubos de carbono y una matriz polimérica o equivalente; la idea es crear una jerarquía en profundidad, con densidad baja de CNT hacia el exterior para facilitar acoplamiento con la onda incidente y densidades mayores hacia dentro para disipación/absorción. No es una “pintura negra mágica”; es una lógica de diseño electromagnético integrada en un material compuesto. [Google Patents](https://patents.google.com/patent/US20100271253A1/en)

Eso encaja con una tendencia general de stealth moderno: pasar de recubrimientos superficiales frágiles a materiales y subestructuras multifuncionales. En otras palabras, incluso aunque el artículo periodístico hable de “pinturas y coatings”, el benchmark tecnológico alto no está solo en la pintura, sino en sistemas donde estructura, impedancia, pérdidas dieléctricas/magnéticas y durabilidad trabajan juntos. [Google Patents](https://patents.google.com/patent/US20100271253A1/en) [Google Patents](https://patents.google.com/patent/WO2019167009A1/en)



## 9) Mi valoración técnica: ¿vale la pena para impresión 3D?

Sí, pero no por la promesa periodística de “invisibilidad”. Vale la pena si lo miras como una familia de materiales avanzados para: apantallamiento electromagnético, piezas conductivas ligeras, sensores, superficies antiestáticas, refuerzo de recubrimientos, durabilidad y, potencialmente, absorbedores EM civiles. En esas aplicaciones, el valor real del grafeno controlado por plasma estaría en combinar conductividad, baja densidad, posibilidad de dopado y ajuste fino de propiedades dieléctricas. [PubMed](https://pubmed.ncbi.nlm.nih.gov/38533978/) [Plasmaphene](https://plasmaphene.com/)

Donde yo sería prudente es en tres frentes. Primero, escalado: pasar de gramos a producción industrial repetible con especificación cerrada no es trivial. Segundo, procesabilidad: un polvo excelente puede comportarse fatal en extrusión o en resina si no está bien funcionalizado/disperso. Tercero, verificación: no he visto en abierto una campaña independiente completa de caracterización de la formulación final del “material furtivo” portugués aplicada a piezas reales. [Euronews](https://www.euronews.com/next/2026/06/30/from-lab-to-sky-portuguese-graphene-that-hides-jets-and-drones-may-transform-defence) [Springer Link](https://link.springer.com/article/10.1186/s42252-021-00020-6)


---


## 10) Enlaces clave de creación, patentes, papers y documentación abierta

Te dejo los mejores enlaces útiles que he encontrado en abierto:

**Proyecto y empresas**
- [Artículo base en Euronews](https://www.euronews.com/next/2026/06/30/from-lab-to-sky-portuguese-graphene-that-hides-jets-and-drones-may-transform-defence)
- [Resumen adicional en Innovation News Network](https://www.innovationnewsnetwork.com/portugal-developing-graphene-materials-for-stealth-technology/71158/)
- [GTechPlasma / descripción histórica](http://www.ipfn.tecnico.ulisboa.pt/gtechplasma/index.html)
- [Plasmaphene](https://plasmaphene.com/)

**Patentes del ecosistema portugués**
- [EP3455389B1 – Process for fabrication of graphene using plasma technology](https://patents.google.com/patent/EP3455389B1/pt)
- [PDF oficial de EP3455389B1](https://patentimages.storage.googleapis.com/c2/a0/e8/e2e7a68dcb19e0/EP3455389B1.pdf)
- [WO2017196198A2 – Process, reactor and system for fabrication of freestanding two-dimensional nanostructures using plasma technology](https://patents.google.com/patent/WO2017196198A2/pt)
- [PDF oficial de WO2017196198A2](https://patentimages.storage.googleapis.com/b5/16/f3/450785d8accf61/WO2017196198A2.pdf)

**Papers relacionados**
- [Plasma-Driven Tuning of Dielectric Permittivity in Graphene – PubMed](https://pubmed.ncbi.nlm.nih.gov/38533978/)
- [Microwave Plasma-Driven Synthesis of Graphene and N-Graphene at a Gram Scale – MDPI landing](https://www.mdpi.com/2227-9717/13/1/196)
- [Research portal ULisboa del paper anterior](https://researchportal.ulisboa.pt/en/publications/microwave-plasma-driven-synthesis-of-graphene-and-n-graphene-at-a/)
- [Revisión abierta sobre impresión 3D de nanocompuestos con grafeno](https://link.springer.com/article/10.1186/s42252-021-00020-6)
- [Artículo abierto sobre absorbedores EM impresos en 3D TPU/CIP](https://www.mdpi.com/2073-4360/14/22/4960)

**Comparables públicos de stealth**
- [US20100271253A1 – CNT-based signature control material (Lockheed Martin)](https://patents.google.com/patent/US20100271253A1/en)
- [WO2019167009A1 – Multilayer radar-absorbing laminate with graphene nanoplatelets (Leonardo)](https://patents.google.com/patent/WO2019167009A1/en)


____________________________________________________________________


•Matriz de viabilidad para impresión 3D civil**, comparando PLA, PA12, TPU, resina y recubrimiento post-impresión con pros, contras y nivel de madurez.
