# Adquisición y procesamiento de señales EMG para la cuantificación del temblor neuromuscular en mano y antebrazo tras el consumo de bebidas energéticas

## INTRODUCCIÓN

En la actualidad el consumo de bebidas energéticas por parte de la población joven en el Perú ha determinado un crecimiento anual estimado de hasta un 7,1 % durante al menos unos 9 años [1]. Los estudios estadísticos del 2025 afirman que el 60% de los jóvenes (media de 18 años) consume o ha consumido bebidas energéticas por fines académicos o deportivos [2].

Las consecuencias médicas si bien no son relevantes y notorias inicialmente, tienden a agravarse cuando el consumo es constante y desinformado.

Para entender el proceso fisiológico es necesario aclarar que la mayoría de bebidas de esta categoría el ingrediente principal es la cafeína, de la cual nos basaremos para explicar el mecanismo de acción en el sistema nervioso de las bebidas energéticas. Para un efecto mucho más completo y real es necesario tener en cuenta el resto de componentes de las bebidas y cómo interactúan entre sí cuando son ingeridas. En síntesis, la cafeína posee una estructura molecular muy similar a la adenosina, la cual nos permite sentir cansancio, es por esto que “suprimimos” esa sensación. Tras este evento de reemplazar a la adenosina surgen eventos en cascada que produce finalmente la liberación de dopamina, glutamato y por consecuencia, adrenalina. Ese desencadenante provoca el aumento de la tasa cardiaca y la presión arterial, también fasciculaciones musculares.

El objetivo principal entonces es caracterizar y cuantificar señales EMG para un análisis posterior e identificar qué factores fisiológicos están relacionados con los episodios de temblor neuromuscular debido al consumo de bebidas energéticas.

---
## OBJETIVOS DEL PROYECTO

Objetivo General:

Desarrollar y validar un algoritmo de procesamiento y análisis de señales de electromiografía de superficie (EMG´s) para la caracterización y cuantificación objetiva del temblor neuromuscular en la mano y el antebrazo, permitiendo identificar los factores fisiológicos e índices de inestabilidad motora asociados al consumo de bebidas energéticas en jóvenes.

Objetivos Específicos:

    1) Desarrollar e implementar algoritmos de filtrado adaptativo y procesamiento digital de señales para la eliminación efectiva de ruido electromagnético y artefactos de movimiento en la banda de bajas frecuencias (4-15           Hz).

    2) Implementar métodos de análisis espectral, específicamente la Densidad Espectral de Potencia (PSD), para la extracción de características biomarcadoras que permitan la correcta detección y clasificación del temblor            neuromuscular.

    3) Estructurar un protocolo de evaluación comparativo (mediciones antes y después del consumo de bebidas energéticas) para segmentar, limpiar y analizar los datos de forma estandarizada.

    4) Generar un índice cuantitativo preciso que correlacione de manera objetiva los cambios en la actividad muscular y el grado de inestabilidad motora fina con la ingesta de las sustancias estimulantes.

---
## PROBLEMÁTICA A ABORDAR

Diversos estudios indican que estas bebidas representan una parte importante del consumo de cafeína en la población joven, lo que hace que estén más expuestos a sus efectos en el cuerpo [3],[4]. Sin embargo, el problema radica no solo en la cafeína, sino en cómo se consume. Muchas veces se toman de manera rápida, en grandes cantidades o sin considerar otras fuentes de cafeína en el día, como café o gaseosas.

Desde el punto de vista de la salud, se ha reportado que el consumo de bebidas energéticas está asociado a efectos como insomnio, nerviosismo y temblores en las manos. Un metaanálisis con más de 96,000 personas mostró que quienes consumen estas bebidas tienen  mayor probabilidad de presentar estos síntomas en comparación con los no consumistas [5]. Además, la cantidad de cafeína puede variar bastante entre productos, pudiendo ir desde 50 hasta más de 500 mg por envase, lo que hace más difícil que las personas controlen cuánto consumen realmente [6].

A pesar de esto, muchas personas no son completamente conscientes de cómo estas bebidas afectan su cuerpo. Sí pueden notar “estar más nerviosos” o que les tiemblan las manos, pero estos efectos suelen quedarse en una percepción superficial y no se llegan a medir de forma objetiva.

La relevancia de este problema aumenta al considerar que el temblor puede comprometer actividades cotidianas que requieren precisión. Esto es especialmente importante en estudiantes y profesionales, donde el control de la mano es clave para un buen desempeño. Estudios han demostrado que la cafeína puede incrementar significativamente el temblor en tareas de precisión, afectando el rendimiento motor fino. En este sentido, el antebrazo tiene un rol importante, ya que contiene los músculos responsables del control de los movimientos finos de la mano y los dedos [7]. Debido a esta alta demanda de control motor, es posible que los efectos de la hiperexcitación neuromuscular, como el temblor inducido por estimulantes, se manifiesten mayormente en esta región.

A pesar de su importancia en el área clínica, la cuantificación del temblor inducido por sustancias estimulantes enfrenta varios desafíos técnicos críticos, concretamente en el procesamiento de señales de electromiografía de superficie o sEMG. La señal sEMG es inherentemente estocástica (evolución temporal incierta), lo que complica la estimación robusta de la potencia en bandas de frecuencia específicas y altera el comportamiento espectral esperado ante la hiperexcitabilidad de las unidades motoras [8].

Un obstáculo metodológico principal es la interferencia de los artefactos de movimiento en el mismo rango de las frecuencias bajas (4-15 Hz) propias del temblor neuromuscular. Esto complica la tarea de diferenciar entre el movimiento voluntario y los temblores involuntarios si no se utilizan algoritmos de filtrado adaptativo [9, 10].

Además, la implementación de sistemas de adquisición de bajo costo aumenta la susceptibilidad al ruido electromagnético y degrada la pureza de la señal, limitando la fiabilidad del análisis de Densidad Espectral de Potencia o PSD para la extracción de características biomarcadoras [13,14 ].

Finalmente, la falta de protocolos de procesamiento digital estandarizados para la segmentación y limpieza de datos genera una brecha tecnológica que impide generar un índice cuantitativo preciso que correlacione la dosis de estimulantes con el grado de inestabilidad motora en el antebrazo [11, 12].

---

## PROPUESTA DE SOLUCIÓN

### Desarrollo de un dispositivo portátil de electromiografía (EMGs) para cuantificación objetiva del temblor

Se propone el diseño de un dispositivo wearable de bajo costo, ubicado en el antebrazo, capaz de adquirir señales de electromiografía de superficie (sEMG) para registrar la actividad muscular asociada al temblor neuromuscular.

A diferencia de las soluciones existentes reportadas, donde solo se realiza la adquisición de señal, el sistema busca integrar una etapa de procesamiento digital (para filtración de ruidos y artefactos), el análisis espectral de la señal y la extracción de características relevantes.

La evaluación se realizará mediante un protocolo comparativo antes y después del consumo de bebidas energéticas, con el objetivo de correlacionar los cambios en la actividad muscular con la ingesta de bebidas energéticas.

Para los fines del curso, el enfoque principal se centrará en el desarrollo y validación del algoritmo de procesamiento y análisis de la señal sEMG, priorizando la detección y clasificación del temblor. La implementación de hardware se considerará a nivel conceptual o como plataforma de adquisición, sin profundizar en su optimización.

---

## PLAN DE ACTIVIDADES

![Fiigura 1](images/imagen_2026-04-05_204949903.png)

---

## REFERENCIAS

[1] Informes de Expertos, "Mercado de Bebidas Energizantes en Perú: Por Producto (Bebidas, Tragos, Mezcladores); Por Envase (Latas, Botellas); Por Canal de Distribución (On-Trade, Off Trade); Dinámica del Mercado (2026-2035) y Panorama Competitivo," Abr. 2026.

[2] "Moda o riesgo: el 60% de los jóvenes consume bebidas energéticas," Salud con lupa, 2024.

[3] S. Breda, K. Whiting, J. Encarnação, J. Norberg, J. Jones, M. Reinap, y J. Jewell, “Consumo de bebidas energéticas en Europa: una revisión de los riesgos, los efectos adversos para la salud y las opciones políticas para responder,” Frontiers in Public Health, vol. 2, 2014.

[4] EFSA, “Opinión científica sobre la seguridad de la cafeína,” Revista EFSA, 2015.

[5] S. Visram, G. Cheetham, J. Riby, J. Crossley, y A. Lake, “Consumption of energy drinks by children and young people: A rapid review examining evidence of physical effects and consumer attitudes,” BMJ Open, vol. 6, no. 10, 2016.

[6] S. M. Al-Hadithy, J. G. Gikas, y P. Mahapatra, “Effect of energy drinks on microsurgical hand tremor,” Surgical Neurology International, vol. 4, 2013.

[7] R. S. Levangie y C. C. Norkin, Estructura y función de las articulaciones: un análisis integral, 5ª ed., F.A. Davis, 2011.

[8] Deuschl, G., et al. (2019). "How to do an electrophysiological study of tremor." Clinical Neurophysiology Practice. [DOI: 10.1016/j.cnp.2019.06.002]

[9] Kahathuduwa, C. N., et al. (2016). "Task-specific kinetic finger tremor affects the performance of carrom players." Journal of Sports Sciences. [DOI: 10.1080/02640414.2015.1078487]

[10] Rissanen, S. (2011). "Surface electromyography and kinematic measurements in Parkinson's disease: analysis methods for differential diagnosis and quantification of treatment." University of Eastern Finland.

[11]  Li, Y., et al. (2024). "Characteristics of Post-Exercise lower limb muscle tremor among speed skaters." Sensors. [DOI: 10.3390/s25144301]

[12]  Smith, J. (2021). "Analysis of Electromyographic Effects of Peripheral Sensory Stimulation on Essential Tremor." BYU ScholarsArchive.
