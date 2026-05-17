# Electroencefalografía
## Introducción
La electroencefalografía (EEG) es una técnica no invasiba utiizada para registrar la actividad eléctrica cerebral mediante electrodos colocados sobre el cuero cabelludo. Estas señales reflejan principalmente la actividad sincrónica de poblaciones neuronales corticales y son ampliamente utilizadas en aplicaciones clínicas, investigación neurocientífica e interfaces cerebro-computadora [1].

Las señales EEG poseen amplitudes relativamente pequeñas, usualmente del orden de microvoltios, y se distribuyen en distintas bandas de frecuencia. Entre las principales se encuentran las bandas delta (0.5–4 Hz), theta (4–8 Hz), alfa (8–13 Hz) y beta (13–30 Hz), cada una relacionada con diferentes estados funcionales del cerebro [2], [4]. Por ejemplo, el ritmo alfa suele incrementarse durante estados de relajación con ojos cerrados, mientras que la actividad beta se asocia a estados de atención y procesamiento cognitivo [2].

La adquisición de señales EEG presenta múltiples desafíos debido a la susceptibilidad de la señal frente a diversas fuentes de ruido y artefactos. Entre los principales problemas se encuentran las interferencias de la red eléctrica, movimientos musculares, actividad ocular y desplazamientos de los electrodos [3].

En el presente laboratorio se empleó el sistema BITalino (r)evolution para la adquisición de señales EEG en diferentes condiciones experimentales, incluyendo estados basales, tareas cognitivas y generación controlada de artefactos. Además, se aplicaron técnicas básicas de procesamiento digital para identificar cambios en las bandas de frecuencia y evaluar la influencia de diferentes condiciones fisiológicas sobre la actividad cerebral.



## Discusión: 
1. ¿Qué banda de frecuencia predomina al cerrar los ojos?

Al cerrar los ojos en un estado de reposo despierto, la banda de frecuencia que predomina de forma inmediata es el ritmo alfa, el cual oscila en el rango de 8 a 13 Hz [4].Este fenómeno se debe a la atenuación de la entrada de estímulos visuales hacia la corteza cerebral, lo que induce una sincronización masiva y rítmica de las poblaciones neuronales tálamocorticales [4]. Cuando se mantienen los ojos abiertos, la señal se desincroniza y pasa  a frecuencias más altas y de menor amplitud; sin embargo, al quitar el ingreso de luz y fijación ocular, aparece este patrón  sinusoidal característicor, el cuál es bservable nítidamente en las regiones posteriores y frontales del cuero cabelludo [4], [6].

2. ¿Qué filtro es imprescindible para EEG y por qué?

Debido a que las señales de EEG se miden en el orden de los microvoltios ) y poseen un ancho de banda biológico muy bajo, son altamente vulnerables a la contaminación externa. Por ello, el uso de dos etapas de filtrado digital es  imprescindible [5].
Entre los filtros más importantes, tenemos:

Filtro Pasabanda (ej. 0.8 a 48 Hz): Es crucial para eliminar la deriva de la línea base (frecuencias menores a 0.5 Hz) inducida por el sudor, la respiración del sujeto a prueba o sutiles movimientos de los cables que alteran el potencial detectado por el electrodo en contacto con la superficie cutánea. Asimismo, limita las frecuencias altas para evitar el solapamiento (aliasing) y atenuar el ruido electromiográfico (EMG) de los músculos faciales [5].

Filtro Notch o Rechaza-banda (60 Hz): Dado que los cables del sistema actúan como antenas que absorben la radiación electromagnética de las luces y equipos del laboratorio, la señal cruda suele quedar completamente enmascarada por el ruido de la red eléctrica comercial (60 Hz en Perú). El filtro Notch remueve esta onda  específica de forma selectiva sin destruir los componentes fisiológicos adyacentes de la señal cerebral [5].

3. ¿Puedes modular conscientemente tu señal EEG? Da un ejemplo.
Sí, es totalmente posible modular la actividad eléctrica cerebral de manera voluntaria y consciente mediante el control de los estados de atención, la ejecución de tareas cognitivas o la imaginación motora [6].
Ejemplo práctico: En el desarrollo de Interfaces Cerebro-Computador (BCI), los usuarios pueden controlar dispositivos externos aprendiendo a modular conscientemente sus ritmos sensorio-motores (como el ritmo alfa). Al imaginar el movimiento de la mano derecha (sin llegar a ejecutarlo físicamente) se produce una disminución localizada de la amplitud de la señal en el hemisferio contralateral; al detener la imaginación motora, el ritmo regresa a su amplitud normal [6]. Este mismo principio de modulación conscientes se evidencia cuando pasas de un estado de relajación a resolver un cálculo aritmético mental complejo, suprimiendo las ondas alfa y aumentando las ondas beta (13-30 Hz) debido a la carga ejecutiva frontal [4].

4. ¿Se observan diferencias entre Fp1 y Fp2? ¿Por qué podrían ocurrir?

Sí se evidencia una diferencia entre Fp1 y Fp2 en amplitud y niveles de ruido. Estas diferencias ocurren por dos razones.

Factores Técnicos e Instrumentales: La causa más común de variación no fisiológica es la asimetría en la impedancia de los electrodos. Pequeñas diferencias en la preparación de la piel con alcohol, la cantidad de gel conductor aplicado o la presión mecánica ejercida por el BITalino alteran la resistencia de contacto. Además, los artefactos electrooculares causados por parpadeos o micro-movimientos de los ojos no siempre se acoplan de forma simétrica en la musculatura frontal, afectando un canal más que al otro [5], [7].

Asimetría Fisiológica: Desde la perspectiva neurofisiológica, los lóbulos frontales no se activan de manera idéntica. Existe una marcada especialización hemisférica donde el polo frontal izquierdo (Fp1) muestra una mayor tasa de activación ante estímulos que involucran lógica verbal, procesamiento analítico secuencial y aproximación conductual, mientras que el polo frontal derecho (Fp2) correlaciona con el procesamiento visoespacial, la atención global y la regulación de emociones ligadas al retiro o la inhibición [4].



## Referencias
[1] PElectroencephalography S. Sanei and J. A. Chambers, EEG Signal Processing and Machine Learning, 2nd ed. Hoboken, NJ, USA: Wiley, 2021.

[2] EEG artifact removal S. K. Gonuguntla, K. R. R. Reddy, and P. K. Bora, “A review on removal of artifacts from EEG signals,” Journal of Neuroscience Methods, vol. 347, 2021.

[3] PLUX Biosignals PLUX Biosignals, “BITalino (r)evolution User Manual,” 2021. [Online]. Available: PLUX Biosignals Official Website

4] E. Niedermeyer and F. L. da Silva, Electroencephalography: Basic Principles, Clinical Applications, and Related Fields, 5th ed. Philadelphia, PA: Lippincott Williams & Wilkins, 2005.

[5] J. G. Webster, Medical Instrumentation: Application and Design, 4th ed. Hoboken, NJ: John Wiley & Sons, 2009.

[6] J. R. Wolpaw, N. Birbaumer, D. J. McFarland, G. Pfurtscheller, and T. M. Vaughan, "Brain-computer interfaces for communication and control," Clinical Neurophysiology, vol. 113, no. 6, pp. 767–791, Jun. 2002.

[7] T. Radüntz, J. Scouten, O. Hochmuth, and B. Meffert, "EEG artifact elimination by extraction of source components using independent component analysis," IEEE Transactions on Biomedical Engineering, vol. 54, no. 1, pp. 31–37, Jan. 2007.
