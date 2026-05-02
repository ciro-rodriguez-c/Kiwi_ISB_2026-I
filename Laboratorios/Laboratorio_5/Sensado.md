## Introducción

En este laboratorio se realizó la adquisición y análisis de señales ECG bajo diferentes condiciones fisiológicas, con el objetivo de evaluar cómo varía la actividad cardíaca frente a cambios en la respiración y la actividad física. Se registraron señales en estado basal, durante ciclos controlados de respiración (incluyendo hiperventilación e hipoventilación), y posterior a la realización de ejercicio físico (en nuestro caso, burpees).
Adicionalmente, se analizaron la primera, segunda y tercera derivada de la señal ECG (I, II y III), con el fin de resaltar características relevantes de la señal. Este enfoque permite una mejor identificación de patrones fisiológicos en la dinámica cardíaca.

---

## Análisis de resultados
### Señal basal

Los resultados muestran que el filtrado aplicado logra limpiar la señal EKG y conservar sus componentes principales. En los tres registros se identifican complejos QRS claros y una concentración de energía principalmente en bajas frecuencias, lo cual es coherente con una señal electrocardiográfica en condición basal.

Además, es importante considerar que la señal fue registrada en una persona sentada, relajada, sin actividad física previa y medida mediante un sistema BITalino. Por ello, se esperaba observar una señal relativamente estable, con un ritmo cardíaco sin grandes variaciones bruscas asociadas al esfuerzo físico. En este contexto, D1 presenta menor amplitud y menor energía, mientras que D2 y D3 muestran picos QRS más pronunciados y mayor potencia en el rango aproximado de 5 a 20 Hz. D3 parece ser el registro más regular visualmente, mientras que D2 muestra mayor variabilidad y algunos picos más intensos.

### Ciclo de inhalacion-contencion-exhalacion

Los resultados muestran que las señales EKG registradas durante hiperventilación conservan complejos QRS identificables después del filtrado, pero presentan mayor variabilidad que una señal basal. Esto es esperable porque, durante la hiperventilación, la respiración se vuelve más rápida y profunda, generando movimiento torácico, cambios en la línea base y posibles alteraciones en el contacto de los electrodos del BITalino.

Entre los tres registros, HV D2_1 presenta una señal relativamente clara con artefactos puntuales, HV D2_2 muestra la mayor variabilidad y una fuerte presencia de componentes de baja frecuencia, mientras que HV D2_3 tiene una señal más estable y con complejos QRS bien definidos. En conjunto, los resultados reflejan una condición respiratoria activa, diferente al reposo basal.

### Segunda señal basal

Los resultados de la segunda señal basal muestran un comportamiento coherente con una medición EKG en reposo. En los tres registros se identifican complejos QRS claros, repetitivos y relativamente regulares, con mayor concentración de energía en frecuencias bajas y medias. Esto confirma que el filtrado aplicado permitió conservar las componentes principales del EKG y mejorar su visualización.
En comparación con la primera señal basal, esta segunda medición mantiene un patrón similar de reposo, aunque en algunos registros, especialmente Basal2 D2 y Basal2 D3, los complejos QRS se observan más altos y definidos. Esta diferencia no necesariamente indica un cambio fisiológico importante, sino que puede deberse a una mejor colocación de los electrodos, menor movimiento corporal o mejor contacto piel-electrodo durante la medición.

Al compararla con los archivos de hiperventilación (HV), la segunda señal basal presenta menor variabilidad y una línea base más estable. En HV se observó mayor irregularidad y más componentes de baja frecuencia, probablemente asociadas a la respiración forzada y al movimiento torácico. Por ello, esta segunda señal basal puede considerarse una referencia adicional de reposo para contrastar los cambios producidos por la hiperventilación y otras condiciones experimentales.


### Actividad física (Burpees)

Los resultados muestran que las señales EKG registradas después de realizar burpees presentan una respuesta compatible con actividad física intensa: mayor frecuencia de complejos QRS, mayor amplitud en algunos registros y mayor contenido frecuencial en comparación con una condición basal de reposo. Esto es esperable porque, luego del ejercicio, el sistema cardiovascular incrementa su actividad para responder a la mayor demanda de oxígeno del cuerpo.

En los tres registros se observa que el filtrado aplicado permitió mejorar la visualización de la señal y conservar los componentes principales del EKG. Burpees D1 muestra una señal clara y con frecuencias dominantes identificables alrededor de 2.5, 5, 10 y 16 Hz. Burpees D2 presenta mayor variabilidad y posibles artefactos, mientras que Burpees D3 muestra picos QRS bastante marcados y regulares. En conjunto, los resultados reflejan adecuadamente una señal cardíaca posterior al ejercicio, medida con BITalino, donde la persona ya no se encontraba en reposo sino bajo los efectos fisiológicos de una actividad física previa.

### Contención de respiración

La señal obtenida durante el test de mantener la respiración tiene sentido, ya que durante la mayor parte del registro se observan complejos QRS claros, repetitivos y relativamente estables. Esto indica que el EKG se mantuvo interpretable y que el filtrado aplicado permitió conservar las componentes principales de la señal cardíaca.

A diferencia de la hiperventilación, donde había mayor variabilidad por el movimiento torácico y la respiración forzada, en esta prueba la línea base parece más estable porque la persona redujo temporalmente el movimiento respiratorio. Sin embargo, hacia el final del registro se observa una zona más irregular, lo cual podría deberse al esfuerzo de seguir conteniendo la respiración, al reinicio de la respiración o a pequeños movimientos que afectaron el contacto de los electrodos.

En conjunto, el resultado es coherente con una prueba de apnea breve o retención de aire: la señal mantiene una estructura cardíaca clara, pero presenta cambios finales compatibles con la incomodidad fisiológica o el retorno de la respiración. Para fortalecer el análisis, sería recomendable identificar exactamente el inicio y final de la retención, y calcular la frecuencia cardíaca antes, durante y después del test.


---
## Homeguide
### Q1. What are the most typical types of noise sources affecting ECG?

Los tipos más comunes de ruido que afectan una señal ECG son la **interferencia de la red eléctrica**, la **deriva de la línea base**, el **ruido muscular o electromiográfico**, los **artefactos por movimiento**, el **mal contacto de los electrodos** y el **ruido propio del sistema de adquisición**. Estos ruidos son importantes porque pueden distorsionar la morfología del ECG y dificultar la detección correcta de los complejos cardíacos, especialmente el complejo QRS [1]–[3].

* **Interferencia de la red eléctrica:**  
  Proviene de la corriente eléctrica del ambiente. En Perú, la red eléctrica trabaja normalmente a **60 Hz**, por lo que esta interferencia puede aparecer alrededor de esa frecuencia. Puede generarse por cables, equipos eléctricos cercanos o una mala conexión a tierra [1].

* **Ruido por movimiento del paciente:**  
  Ocurre cuando el paciente se mueve durante el registro. Esto puede modificar el contacto entre los electrodos y la piel, generando cambios bruscos, desplazamientos de la línea base o distorsiones en la señal ECG [2], [3].

* **Ruido por mal contacto de los electrodos:**  
  Se produce cuando los electrodos no están bien colocados, la piel no fue preparada adecuadamente o hay sudor, vello o grasa. Esto cambia la impedancia piel-electrodo y puede causar una señal inestable o con artefactos [2], [3].

* **Interferencia muscular o electromiográfica:**  
  Aparece cuando los músculos del paciente se contraen, por ejemplo, si está tenso, temblando o hablando. Esta actividad eléctrica muscular puede mezclarse con la señal cardíaca y producir ruido de mayor frecuencia [1]–[3].

* **Deriva de la línea base:**  
  Es una variación lenta de la señal ECG. Generalmente se debe a la respiración, movimientos del cuerpo o cambios en la impedancia entre la piel y el electrodo [1], [2].

* **Ruido del equipo o ruido electrónico interno:**  
  Puede originarse en los componentes del sistema de adquisición, como amplificadores, cables, sensores o conversores analógico-digitales. Aunque suele ser menor, también puede afectar la calidad de la señal ECG [1]–[3].

### Q2. Why does the change of the positioning of the sensors (lead I-III) change the ECG signal components? How do the components change?

Cambiar la posición de los sensores en las derivaciones **I, II y III** cambia los componentes de la señal ECG porque cada derivación registra la actividad eléctrica del corazón desde una dirección distinta. Las derivaciones I, II y III son derivaciones bipolares de las extremidades, es decir, miden diferencias de potencial eléctrico entre dos electrodos ubicados en distintas posiciones del cuerpo [4]–[6].

El corazón genera señales eléctricas durante la despolarización y repolarización. Sin embargo, cada derivación no registra toda la actividad eléctrica de la misma forma, sino la **proyección del vector eléctrico cardíaco** sobre el eje de esa derivación. Por eso, al cambiar de una derivación a otra, también cambia la forma en que se observan las ondas P, QRS y T [6], [7].

Generalmente, la derivación II suele mostrar una señal más clara y de mayor amplitud porque su dirección se parece más al eje eléctrico normal del corazón durante la despolarización ventricular. Además, si la actividad eléctrica se dirige hacia el electrodo positivo, la onda se observa positiva; si se aleja, se observa negativa; y si el vector eléctrico va casi perpendicular al eje de la derivación, la amplitud registrada disminuye [4]–[8].

| Componente | ¿Cómo puede cambiar? |
|---|---|
| Onda P | Puede verse más grande, más pequeña o menos clara. |
| Complejo QRS | Puede aumentar o disminuir su amplitud, o incluso verse más negativo. |
| Onda T | Puede cambiar su tamaño o su polaridad. |
| Línea base | Puede variar si cambia el contacto del electrodo o hay movimiento. |

En conclusión, las derivaciones **I, II y III** registran la misma actividad cardíaca, pero desde diferentes puntos de vista. Por eso, al cambiar la posición de los sensores, cambian principalmente la **amplitud**, la **polaridad** y la **forma** de las ondas **P**, **QRS** y **T**.

### Q3. Describe if there are major differences in the signal when acquiring the signal from different body locations (e.g., wrist / collarbone/ chest). What could be the cause? Did you expect such changes in the signal? Store a signal segment of each to visualize the differences
Las señales capturadas en el pecho muestran amplitudes mucho más altas en comparación con las obtenidas en la muñeca o extremidades. Esto se debe a que los electrodos están físicamente más cerca de la fuente de activación eléctrica cardíaca. Respecto a la calidad de la señal, la relación señal-ruido es superior en la clavícula y el pecho. La muñeca presenta una alta susceptibilidad a los artefactos por movimiento y una mayor resistencia eléctrica debido al trayecto que la señal debe recorrer a través de diversos tejidos.
La causa fundamental para esta diferencia es la distancia respecto al corazón y el fenómeno del conductor de volumen. Conforme la señal eléctrica se propaga por el cuerpo, atraviesa capas de piel, músculo y hueso que actúan atenuando la amplitud. Estos cambios son esperados puesto que el vector eléctrico del corazón se proyecta con mayor intensidad en las derivaciones cercanas al torso, y la proximidad física reduce la cantidad de ruido captado durante la trayectoria.

### Q4. The cardiac and the respiratory systems are well interconnected as is well known. Do you expect that different types of breathing (e.g. faster, deeper) to influence the ECG signals? Show screenshots of ECG signals in different respiratory circumstances and described the variations if there are any.
En las señales correspondientes a la hiperventilación, se observa que la respiración rápida y profunda altera significativamente los intervalos R-R. Este fenómeno se conoce como "Arritmia Sinusal Respiratoria". Durante la fase de inhalación, la frecuencia cardíaca tiende a aumentar, lo que resulta en intervalos R-R más cortos. Por el contrario, durante la exhalación, la frecuencia disminuye y los intervalos se alargan. Adicionalmente, el movimiento mecánico del tórax durante la respiración profunda introduce un balanceo en la línea base (baseline wander) debido a las variaciones en la impedancia entre el electrodo y la piel.
### Q5. In Home-Guide #1 you have seen that different amounts of force produced in the muscle generated signals with different amplitudes. How does movement influence your ECG signal?
Las señales orrespondientes a la actividad de burpees muestran una interferencia de alta frecuencia muy marcada. Esto ocurre porque los músculos esqueléticos involucrados en el movimiento generan sus propios potenciales de acción eléctricos (electromiografía o EMG). Esta actividad muscular se superpone al ECG, creando un ruido que puede ocultar componentes clave como la onda P o la onda T. Para corregir esto, el procesamiento digital utiliza un filtro de banda de 1 a 45 Hz. Al eliminar las frecuencias por encima de 45 Hz se descarta el ruido muscular, mientras que el corte inferior a 1 Hz estabiliza la línea base que se ve afectada por el movimiento de los cables y el cuerpo.
### Q6. To the best of your knowledge, how can you detect bradycardia and tachycardia in the ECG signal?
Para determinar estas condiciones en la señal, se realiza el cálculo de la frecuencia cardíaca mediante la identificación de los picos R siguiendo este procedimiento:

1. Detección de picos R: Se localizan los tiempos exactos de dos ondas R consecutivas, denominadas R1 y R2.
2. Cálculo del intervalo R-R: Se obtiene la diferencia temporal entre ambos puntos.
   
$$\Delta T = R2 - R1$$

3. Obtención de la frecuencia cardíaca: Se aplica la fórmula para convertir el tiempo a latidos por minuto (BPM).

$$\text{FC (BPM)} = \frac{60}{\Delta T}$$

Criterios de detección aplicados:
Se identifica taquicardia cuando la frecuencia cardíaca es superior a 100 BPM de forma sostenida. Se identifica bradicardia si la frecuencia es inferior a 60 BPM, situación que suele presentarse en los datos en estado basal si el sujeto se encuentra en reposo absoluto o posee un alto nivel de entrenamiento físico.

---
## Bibliografía

[1] S. M. Qaisar, L. Fesquet, and M. Renaudin, “Baseline wander and power-line interference elimination of ECG signals using efficient signal-piloted filtering,” *Healthcare Technology Letters*, vol. 7, no. 4, pp. 114–118, 2020. Disponible en: https://pmc.ncbi.nlm.nih.gov/articles/PMC7494370/

[2] H. Li, X. Wang, L. Chen, and E. Sejdić, “An Automatic Method to Reduce Baseline Wander and Motion Artifacts in Ambulatory ECG,” *Sensors*, vol. 21, no. 24, 2021. Disponible en: https://pmc.ncbi.nlm.nih.gov/articles/PMC8708403/

[3] F. A. Ghaleb, M. B. Kamat, M. N. M. Saad, and A. R. M. Sidek, “Two-stage motion artefact reduction algorithm for electrocardiogram using weighted adaptive noise cancelling and recursive Hampel filter,” *PLOS ONE*, vol. 13, no. 11, 2018. Disponible en: https://pmc.ncbi.nlm.nih.gov/articles/PMC6245678/

[4] Y. Sattar and L. Chhabra, “Electrocardiogram,” *StatPearls*, National Library of Medicine, 2023. Disponible en: https://www.ncbi.nlm.nih.gov/books/NBK549803/

[5] J. R. Hampton and D. Adlam, “Conquering the ECG,” *Cardiology Explained*, National Library of Medicine. Disponible en: https://www.ncbi.nlm.nih.gov/books/NBK2214/

[6] B. E. Jin, A. W. Wulff, and J. S. Wakai, “A simple device to illustrate the Einthoven triangle,” *Advances in Physiology Education*, vol. 37, no. 4, pp. 341–345, 2013. Disponible en: https://pmc.ncbi.nlm.nih.gov/articles/PMC3776430/

[7] G. D. Gargiulo *et al*., “On the Einthoven Triangle: A Critical Analysis of the Single Rotating Dipole Hypothesis,” *Sensors*, vol. 18, no. 7, 2018. Disponible en: https://pmc.ncbi.nlm.nih.gov/articles/PMC6068749/

[8] M. AlGhatrif and J. Lindsay, “A brief review: history to understand fundamentals of electrocardiography,” *Journal of Community Hospital Internal Medicine Perspectives*, vol. 2, no. 1, 2012. Disponible en: https://pmc.ncbi.nlm.nih.gov/articles/PMC3714093/
