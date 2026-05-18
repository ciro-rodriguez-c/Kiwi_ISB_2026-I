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

## Metodología

### Adquisición de la señal EEG

Para la adquisición de las señales EEG se utilizó un sistema BITalino (r)evolution Board Kit BLE/BT junto con el software OpenSignals, el cual permitió visualizar y guardar las señales obtenidas. La frecuencia de muestreo utilizada fue de 1000 Hz, suficiente para analizar las bandas de frecuencia presentes en señales EEG.  

Se colocaron electrodos Ag/AgCl siguiendo el sistema internacional 10-20, específicamente en las posiciones Fp1 y Fp2, mientras que la referencia se colocó en la mastoide derecha. Antes de colocar los electrodos, se limpió la piel para reducir la impedancia y mejorar la calidad de la señal registrada.  

### Protocolo experimental

El registro EEG se realizó bajo diferentes condiciones con el objetivo de observar cambios en la actividad cerebral y la aparición de artefactos.

Primero se tomó una línea basal en reposo, procurando evitar movimientos faciales y oculares. Luego, el participante realizó distintas actividades, como mantener los ojos abiertos fijando la vista en un punto, generar artefactos mediante parpadeo y movimientos de masticación, y finalmente actividades libres como responder preguntas y escuchar música relajante o estimulante.

Durante toda la adquisición se intentó mantener un ambiente con la menor cantidad posible de interferencias y movimientos para obtener señales más limpias.

---
## Resultados

### Señal basal 1
<img width="1553" height="525" alt="imagen" src="https://github.com/CzairoX/Kiwi_ISB_2026-I/blob/main/Laboratorios/Laboratorio_7/Datos/basal1.png" />
                                                                          
                                                                              
                                                            Fig1. Señal basal 1
### Señal basal 2
<img width="1553" height="525" alt="imagen" src="https://github.com/CzairoX/Kiwi_ISB_2026-I/blob/main/Laboratorios/Laboratorio_7/Datos/basal2.png" />
                                                                          
                                                                              
                                                            Fig2. Señal basal 2

### Señal basal 3
<img width="1553" height="525" alt="imagen" src="https://github.com/CzairoX/Kiwi_ISB_2026-I/blob/main/Laboratorios/Laboratorio_7/Datos/basal3.png" />
                                                                          
                                                                              
                                                            Fig3. Señal basal 3
### Ojos fijos en un punto
<img width="1553" height="525" alt="imagen" src="https://github.com/CzairoX/Kiwi_ISB_2026-I/blob/main/Laboratorios/Laboratorio_7/Datos/ojofijopunto.png" />
                                                                          
                                                                              
                                                      Fig4. Ojos fijos en un punto
### Pregunta fácil
<img width="1553" height="525" alt="imagen" src="https://github.com/CzairoX/Kiwi_ISB_2026-I/blob/main/Laboratorios/Laboratorio_7/Datos/librepreguntafacil.png" />
                                                                          
                                                                              
                                                      Fig5. Pregunta fácil
### Pregunta difícil
<img width="1553" height="525" alt="imagen" src="https://github.com/CzairoX/Kiwi_ISB_2026-I/blob/main/Laboratorios/Laboratorio_7/Datos/librepreguntadificil.png" />
                                                                          
                                                                              
                                                      Fig6. Pregunta difícil
### Artefactos
<img width="1553" height="525" alt="imagen" src="https://github.com/CzairoX/Kiwi_ISB_2026-I/blob/main/Laboratorios/Laboratorio_7/Datos/artefactos.png" />
                                
                                                                              
                                                        Fig7. Artefactos
                                                                       
---

## Análisis de resultados
### Señal basal 1

Los resultados de la señal basal 1 muestran un registro relativamente estable en ambos canales, Fp1 y Fp2. En la señal cruda se observa una actividad de baja amplitud, sin grandes cambios bruscos durante la mayor parte del tiempo. Esto es coherente con una condición basal, donde la persona probablemente se encontraba en reposo y sin realizar una tarea cognitiva o física específica.

Después del filtrado de 0.8 a 48 Hz con notch de 60 Hz, la señal se observa más limpia y con menor interferencia de ruido eléctrico. En Fp1, la amplitud se mantiene más baja y estable, aunque aparece un pico aislado cerca de la parte final del registro. En Fp2, la señal presenta mayor amplitud y más variabilidad que Fp1, lo que puede deberse a diferencias en el contacto del electrodo, actividad muscular cercana o pequeñas variaciones de movimiento.

En conjunto, la señal basal 1 puede considerarse una referencia inicial de reposo. Aunque no está completamente libre de ruido, conserva un patrón relativamente uniforme, especialmente en comparación con las señales de artefactos o con las tareas cognitivas.

### Señal basal 2

La señal basal 2 también presenta un comportamiento compatible con una condición de reposo. En la señal cruda se observa una amplitud moderada, con algunos picos aislados durante el registro, especialmente hacia la parte media y final. Esto indica que, aunque la persona estaba en condición basal, pudieron existir pequeños movimientos, parpadeos o cambios en el contacto de los electrodos.

Luego del filtrado, la señal mejora visualmente porque se atenúan componentes de ruido y se conserva principalmente la actividad dentro del rango de interés. En Fp1, la señal filtrada mantiene una amplitud baja a moderada, con algunos picos puntuales. En Fp2, se observan picos más notorios y mayor variabilidad, lo que sugiere que este canal fue más sensible a interferencias o a actividad no cerebral.

Comparada con la basal 1, la basal 2 presenta más eventos transitorios, especialmente en Fp2. Sin embargo, sigue siendo una señal útil como referencia de reposo, ya que la mayor parte del registro mantiene una estructura estable.

### Señal basal 3

La señal basal 3 muestra mayor variabilidad que las señales basales anteriores. En Fp1 se observan picos fuertes al inicio y al final del registro, mientras que en la parte central la señal se mantiene más estable. Esto puede interpretarse como presencia de artefactos al comenzar o finalizar la medición, posiblemente por movimiento, ajuste de electrodos o cambio de postura.

En Fp2, la señal cruda y filtrada presenta amplitudes más elevadas, sobre todo al inicio y al final. El filtrado conserva estos cambios porque probablemente no corresponden solo a ruido de alta frecuencia, sino a variaciones fuertes dentro del rango que el filtro permite pasar. Por eso, aunque el filtrado mejora la señal, no elimina completamente los artefactos de gran amplitud.

En general, basal 3 puede utilizarse como señal de reposo, pero con precaución. La zona central del registro parece más confiable, mientras que los extremos presentan alteraciones importantes que podrían afectar el análisis si se consideran sin segmentar la señal.


### Ojos fijos en un punto

La señal de ojos fijos en un punto presenta un comportamiento relativamente estable durante casi todo el registro, especialmente en comparación con las señales de artefactos. Esto tiene sentido, porque al mantener la mirada fija se espera reducir movimientos oculares amplios y disminuir parte de la variabilidad asociada al parpadeo o al desplazamiento de los ojos.

En Fp1, la señal cruda muestra una amplitud moderada y bastante constante, aunque hacia el final aparece una zona con mayor actividad y picos más intensos. En la señal filtrada, esta tendencia se mantiene: la mayor parte del registro es estable, pero al final aparece una alteración más marcada. Esto podría deberse a fatiga visual, parpadeo, movimiento ocular o cambio de atención.

En Fp2, se observa un patrón similar, aunque con mayor amplitud. La señal filtrada conserva una actividad más intensa hacia el final, lo que sugiere que el evento no fue únicamente ruido eléctrico, sino posiblemente un artefacto fisiológico o de movimiento.

En conjunto, esta señal es coherente con una prueba de fijación visual. La mayor parte del registro parece controlada, pero el tramo final debería analizarse con cuidado porque presenta una alteración evidente.

### Pregunta fácil

Durante la señal de pregunta fácil se observa mayor variabilidad que en las señales basales. Esto puede estar relacionado con la activación cognitiva generada por responder o pensar en una pregunta, aunque también pueden influir artefactos por movimiento facial, tensión muscular o cambios en la mirada.

En Fp1, la señal cruda presenta un aumento notable de amplitud entre los 5 y 9 segundos aproximadamente, y luego otra zona de alta amplitud hacia el final del registro. Después del filtrado, estos eventos siguen apareciendo, aunque con una forma más limpia. Esto indica que no eran solo interferencia de 60 Hz, sino componentes presentes dentro del rango permitido por el filtro.

En Fp2, la señal muestra picos más marcados que Fp1, especialmente al inicio de la tarea y hacia el final. Esto sugiere que Fp2 fue más sensible a variaciones durante la actividad, posiblemente por mayor ruido muscular o diferencias en la ubicación/contacto del electrodo.

En general, la pregunta fácil genera una señal más activa que la basal. Sin embargo, no todo el aumento de amplitud puede atribuirse directamente a actividad cerebral, porque también hay presencia de artefactos evidentes.

### Pregunta difícil

La señal de pregunta difícil muestra una actividad más irregular y con picos de mayor amplitud, especialmente entre los 14 y 20 segundos aproximadamente. Esto puede estar relacionado con una mayor demanda cognitiva, ya que una pregunta difícil puede generar mayor concentración, tensión o esfuerzo mental. Sin embargo, también es importante considerar que los canales frontales Fp1 y Fp2 son muy sensibles a parpadeos, movimientos oculares y actividad muscular facial.

En Fp1, la señal cruda presenta una zona muy marcada en la parte media, con oscilaciones amplias y picos positivos y negativos. En la señal filtrada, estos eventos se mantienen, aunque con menor ruido. Esto indica que la alteración tiene componentes dentro del rango de análisis y no fue eliminada completamente por el filtro.

En Fp2, también se observa mayor variabilidad, con picos fuertes durante la misma zona temporal y algunos eventos adicionales hacia la parte final. En comparación con la pregunta fácil, la pregunta difícil parece mostrar una respuesta más intensa en algunos tramos, aunque también con más artefactos.

En conjunto, los resultados son coherentes con una tarea de mayor exigencia mental, pero el análisis debe ser cuidadoso porque parte de la señal puede estar contaminada por movimientos oculares, parpadeos o tensión muscular.

### Artefactos

La señal de artefactos es la que presenta mayor irregularidad visual. En ambos canales se observan picos bruscos, cambios rápidos de amplitud y eventos repetitivos que no parecen corresponder a una señal EEG estable. Esto confirma que la medición contiene alteraciones importantes producidas probablemente por movimiento, parpadeo, tensión muscular, mala conexión o manipulación de los electrodos.

En Fp1, la señal cruda muestra múltiples picos positivos y negativos distribuidos a lo largo del registro. Después del filtrado, la señal mejora parcialmente, pero los artefactos siguen presentes porque muchos de ellos tienen componentes dentro del rango de 0.8 a 48 Hz. Por eso, el filtro no puede eliminarlos completamente.

En Fp2, la presencia de artefactos es aún más evidente. Se observan picos muy altos y repetitivos, algunos cercanos al límite de amplitud del gráfico. Esto indica que el canal estuvo bastante contaminado durante la medición.

En conjunto, esta señal sirve como referencia para identificar cómo se ven los artefactos en comparación con las señales basales o de tareas. También demuestra que el filtrado ayuda a reducir ruido eléctrico, pero no reemplaza una buena adquisición ni elimina por completo movimientos o interferencias fisiológicas.


---


### Procesamiento de la señal

Las señales obtenidas fueron exportadas en archivos .txt para ser procesadas posteriormente en MATLAB. Se aplicó un filtro pasabanda en el rango aproximado de 0.8 a 48 Hz, correspondiente al rango de frecuencias de interés para señales EEG.  

Después del filtrado, se realizó un análisis espectral usando la densidad espectral de potencia (PSD) mediante el método de Welch, con el fin de identificar las bandas cerebrales δ, θ, α y β en las diferentes condiciones evaluadas. También se analizaron los artefactos producidos por parpadeo y movimientos musculares.

## Conclusiones 

El desarrollo de este laboratorio permitió comprender la importancia del procesamiento y filtrado de señales biomédicas para la identificación de información relevante dentro de registros fisiológicos reales. El análisis se logró gracias a un proceso de filtrado que permitió reducir componentes no deseados como ruido eléctrico, movimientos musculares y artefactos externos. Posteriormente revisando la descomposición espectral en el dominio de la frecuencia es posible distinguir por lo menos las señales predominantes conocidas (δ, θ, α y β), además de observar la presencia de artefactos producidos tanto voluntaria (movimientos puntuales realizados solo en ciertas mediciones) como involuntariamente (parpadeo, movimiento ocular, movimiento de músculos faciales).
Las diferencias observadas entre respuestas a preguntas simples y complejas sugieren cambios en la actividad registrada, lo cual resalta la relación entre procesos cognitivos y señales fisiológicas.
Se puede resaltar como principal idea de la experiencia de laboratorio que, las respuestas cognitivas generan modificaciones medibles en ciertas bandas espectrales.

## Referencias
[1] PElectroencephalography S. Sanei and J. A. Chambers, EEG Signal Processing and Machine Learning, 2nd ed. Hoboken, NJ, USA: Wiley, 2021.

[2] EEG artifact removal S. K. Gonuguntla, K. R. R. Reddy, and P. K. Bora, “A review on removal of artifacts from EEG signals,” Journal of Neuroscience Methods, vol. 347, 2021.

[3] PLUX Biosignals PLUX Biosignals, “BITalino (r)evolution User Manual,” 2021. [Online]. Available: PLUX Biosignals Official Website

4] E. Niedermeyer and F. L. da Silva, Electroencephalography: Basic Principles, Clinical Applications, and Related Fields, 5th ed. Philadelphia, PA: Lippincott Williams & Wilkins, 2005.

[5] J. G. Webster, Medical Instrumentation: Application and Design, 4th ed. Hoboken, NJ: John Wiley & Sons, 2009.

[6] J. R. Wolpaw, N. Birbaumer, D. J. McFarland, G. Pfurtscheller, and T. M. Vaughan, "Brain-computer interfaces for communication and control," Clinical Neurophysiology, vol. 113, no. 6, pp. 767–791, Jun. 2002.

[7] T. Radüntz, J. Scouten, O. Hochmuth, and B. Meffert, "EEG artifact elimination by extraction of source components using independent component analysis," IEEE Transactions on Biomedical Engineering, vol. 54, no. 1, pp. 31–37, Jan. 2007.
