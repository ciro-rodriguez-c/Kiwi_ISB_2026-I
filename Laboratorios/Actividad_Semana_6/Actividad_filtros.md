# Filtros Digitales para Señales Biomédicas: EEG, ECG, EMG

## Filtro de Wavelet:

El Filtro de Wavelet permite un análisis de tiempo-frecuencia. Esto es vital para señales como el EKG o el EEG, que son no estacionarias (sus características cambian con el tiempo).

### Importancia:


El Filtro de Wavelet es fundamental en el procesamiento de bioseñales porque permite un análisis tiempo-frecuencia simultáneo. Este método es ideal para el EKG y EEG, cuyas características cambian dinámicamente en el tiempo.
Su relevancia radica en el uso de una "Wavelet Madre": una plantilla matemática que se correlaciona con la morfología real de la señal (como el complejo QRS). Esto permite aplicar la Transformada Wavelet Discreta (DWT) para descomponer la señal, filtrar el ruido mediante umbralización (Hard o Soft Thresholding) y reconstruirla sin deformar los componentes diagnósticos esenciales que los filtros tradicionales suelen suavizar en exceso [1], [2], [5].




<img width="538" height="535" alt="imagen" src="https://github.com/user-attachments/assets/4a7e0334-d480-439f-bd46-cb23bdb1702c" />


**Figura 1.** Proceso transformada de Wavelet. [5] 

                     

### Tipo de ruido que elimina y sus frecuencias:


Este filtro es una herramienta versátil que actúa sobre diversos tipos de contaminación sin comprometer las bandas de interés clínico:
•	En EKG: Elimina eficazmente la deriva de línea de base (ruido de baja frecuencia provocado por la respiración y movimiento del torso) y el ruido de alta frecuencia, preservando la integridad del intervalo ST y la onda P [4].
•	En EEG: Es altamente selectivo para suprimir artefactos oculares (parpadeos) y ruido muscular (EMG). Su precisión permite limpiar la señal sin afectar las frecuencias rápidas de las bandas Gamma o Beta, cruciales para el análisis neurofisiológico [3].


## Filtro Chebyshev

### Importancia

El filtro Chebyshev es un filtro digital de tipo IIR utilizado en el procesamiento de señales biomédicas como EMG, EKG/ECG y EEG. Su principal ventaja es que permite una transición rápida entre la banda de frecuencias que se desea conservar y la banda que se desea eliminar. Por eso, puede ser útil cuando se necesita atenuar ruidos específicos sin afectar demasiado la señal principal. Sin embargo, también tiene una limitación: puede generar ondulaciones o *ripples* en la banda de paso o en la banda de rechazo, según el tipo de filtro utilizado [6].

Existen dos tipos principales de filtros Chebyshev. El tipo I presenta ondulaciones en la banda de paso, mientras que el tipo II las presenta en la banda de rechazo. En señales biomédicas, este filtro puede configurarse como pasaaltas, pasabajas, pasabanda o notch, dependiendo del ruido que se quiera reducir [6].

![Filtro Chebyshev tipo I y tipo II](https://www.elprocus.com/wp-content/uploads/2015/07/Types-of-Chebyshev-Filter.jpg)

**Figura 2.** Filtro Chebyshev tipo I y tipo II. [12] 

### Tipo de ruido que elimina y sus frecuencias

En señales EKG/ECG, el filtro Chebyshev puede emplearse para eliminar la deriva de línea base, el ruido de alta frecuencia y la interferencia de red eléctrica. La deriva de línea base aparece en frecuencias muy bajas, generalmente menores a 0.5 Hz, y puede deberse a la respiración, movimiento del paciente o cambios en el contacto electrodo-piel. Para reducirla, se puede usar un filtro pasaaltas con frecuencia de corte cercana a 0.5 Hz [6]. También se puede aplicar un filtro pasabajas para eliminar frecuencias superiores a 100 Hz, ya que la información útil del ECG suele encontrarse aproximadamente entre 0.5 Hz y 100 Hz [6]. Además, para la interferencia eléctrica de 50 Hz o 60 Hz, se puede usar un filtro notch centrado en esa frecuencia [6], [8].

En señales EMG, el filtro Chebyshev puede ayudar a reducir artefactos de movimiento, ruido de línea eléctrica y ruido de alta frecuencia. Los artefactos de movimiento afectan principalmente las bajas frecuencias, por lo que suele usarse un filtro pasaaltas alrededor de 20 Hz [7]. La interferencia eléctrica aparece en 50 Hz o 60 Hz, dependiendo del país, y puede reducirse con un filtro notch [8]. Además, como la señal sEMG útil puede extenderse hasta aproximadamente 400 Hz, se puede usar un filtro pasabajas entre 400 Hz y 450 Hz para eliminar componentes de alta frecuencia no deseadas [7].

En señales EEG, el filtro Chebyshev puede utilizarse para limpiar la señal antes de analizar las bandas cerebrales. Las bandas típicas del EEG son delta, de 0.5 a 4 Hz; theta, de 4 a 7 Hz; alfa, de 8 a 12 Hz; y beta, de 13 a 30 Hz [11]. En este caso, un filtro pasaaltas puede reducir la deriva lenta menor a 0.5 o 1 Hz, mientras que un filtro notch puede atenuar la interferencia eléctrica de 50 Hz o 60 Hz [9]. Además, el EEG puede contaminarse con actividad muscular, la cual puede aparecer aproximadamente entre 20 Hz y 300 Hz, por lo que el filtrado debe aplicarse con cuidado para no confundir ruido muscular con actividad cerebral real [10].

En conclusión, el filtro Chebyshev es útil para procesar señales EMG, EKG/ECG y EEG porque permite eliminar ruidos según su frecuencia. Puede reducir deriva de línea base, interferencia eléctrica, artefactos de movimiento y ruido de alta frecuencia. Sin embargo, debe diseñarse correctamente, ya que un mal filtrado puede alterar la forma original de la señal biomédica y afectar su interpretación.

## Filtro Butterworth

El filtro Butterworth es un filtro digital del tipo IIR (Infinite Impulse Response) ampliamente utilizado en el procesamiento de señales biomédicas debido a su respuesta en frecuencia suave y su banda pasante maximálmente plana, es decir sin presencia de oscilaciones fuertes (ripple). Es importante recalcar que el principal atributo como ya se mencionó es la estabilidad de la banda de paso, sin embargo este filtro presenta un desfase considerable que debe tratarse con cuidado dependiendo de las señales analizadas [14].

### Importancia

Como ya se mencionó, este filtro toma relevancia en el ámbito biomédico porque preserva amplitudes con una fidelidad muy aceptable, es simple de diseñar, tiene bajo costo computacional y es eficiente [13].
Es versátil para implementar como tipo de filtro pasa-bajos, pasa-altos, pasa-banda o rechaza-banda.

### Tipo de ruido que elimina y sus frecuencias

Las frecuencias atenuadas por el filtro Butterworth dependen del rango fisiológico esperado de la señal biomédica analizada [15]. En ECG, por ejemplo, suele preservarse el contenido entre 0.5 Hz y 40 Hz, mientras que componentes inferiores pueden asociarse a variaciones lentas de línea base y componentes superiores a ruido muscular o electrónico. De manera similar, en EEG y EMG se seleccionan distintas bandas de frecuencia según las características fisiológicas de cada señal [16]. 


## Referencias Bibliográficas (Formato IEEE):


[1] D. L. Donoho, "De-noising by soft-thresholding," IEEE Transactions on Information Theory, vol. 41, no. 3, pp. 613-627, May 1995, doi: 10.1109/18.382009.

[2] P. S. Addison, "Wavelet transforms in biomedical engineering," Annals of Biomedical Engineering, vol. 30, no. 1, pp. 115-128, Jan. 2002.

[3] M. Balamareeswaran and D. Ebenezer, "Denoising of EEG signals using Discrete Wavelet Transform Based Scalar Quantization," Biomedical and Pharmacology Journal, vol. 8, no. 1, pp. 235-242, 2015.

[4] M. K. Stiles, D. Clifton, N. R. Grubb, J. N. Watson, and P. S. Addison, “Wavelet‐Based Analysis of Heart‐Rate‐Dependent ECG Features,” Annals of Noninvasive Electrocardiology, vol. 9, no. 4, pp. 316–322, Oct. 2004, doi: https://doi.org/10.1111/j.1542-474x.2004.94566.x.

[5] “Transformada Wavelet – acervo para el mejoramiento del aprendizaje de alumnos de ingeniería, en Inteligencia Artificial.” https://virtual.cuautitlan.unam.mx/intar/?page_id=1108

[6] M. S. Chavan, R. A. Agarwal, and M. D. Uplane, “Comparative Study of Chebyshev I and Chebyshev II Filter used For Noise Reduction in ECG Signal,” *International Journal of Circuits, Systems and Signal Processing*, vol. 2, no. 1, pp. 1–17, 2008. [En línea]. Disponible en: https://www.naun.org/main/NAUN/circuitssystemssignal/cssp-60.pdf

[7] C. J. De Luca, L. D. Gilmore, M. Kuznetsov, and S. H. Roy, “Filtering the surface EMG signal: Movement artifact and baseline noise contamination,” *Journal of Biomechanics*, vol. 43, no. 8, pp. 1573–1579, 2010, doi: 10.1016/j.jbiomech.2010.01.027. [En línea]. Disponible en: https://www.bu.edu/nmrc/files/2010/06/103.pdf

[8] J. Chen, Y. Sun, S. Sun, and Z. Yao, “Reducing Power Line Interference from sEMG Signals Based on Synchrosqueezed Wavelet Transform,” *Sensors*, vol. 23, no. 11, Art. no. 5182, 2023, doi: 10.3390/s23115182. [En línea]. Disponible en: https://www.mdpi.com/1424-8220/23/11/5182

[9] A. de Cheveigné and I. Nelken, “Filters: When, Why, and How (Not) to Use Them,” *Neuron*, vol. 102, no. 2, pp. 280–293, 2019, doi: 10.1016/j.neuron.2019.02.039. [En línea]. Disponible en: https://discovery.ucl.ac.uk/id/eprint/10067236/1/filtering_190205.pdf

[10] S. D. Muthukumaraswamy, “High-frequency brain activity and muscle artifacts in MEG/EEG: a review and recommendations,” *Frontiers in Human Neuroscience*, vol. 7, Art. no. 138, 2013, doi: 10.3389/fnhum.2013.00138. [En línea]. Disponible en: https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2013.00138/full

[11] C. S. Nayak and A. C. Anilkumar, “Normal EEG Waveforms,” *StatPearls*, Treasure Island, FL: StatPearls Publishing, 2025. [En línea]. Disponible en: https://www.ncbi.nlm.nih.gov/books/NBK539805/

[12] T. Agarwal, “Different Types of Analog Filters with Explanation,” ElProCus - Electronic Projects for Engineering Students, July 16, 2015. https://www.elprocus.com/types-of-analog-filters/.
‌
[13] M. S. Hossain et al., “Wearable Device-Based Heart Rate Variability Analysis Using Butterworth Filtering Techniques,” *Sensors*, vol. 25, no. 22, 2025. [Online]. Available: https://www.mdpi.com/1424-8220/25/22/7091

[14] J. M. Smith and P. A. Lewicki, “Linear Phase FIR Digital Filters for Biological Signal Processing,” *IEEE Transactions on Biomedical Engineering*, 1986. [Online]. Available: https://pubmed.ncbi.nlm.nih.gov/3721526/

[15] A. T. Sehgal et al., “Noise Reduction and Signal Processing Techniques for ECG Signals,” *Sensors*, vol. 20, no. 21, 2020. [Online]. Available: https://www.mdpi.com/1424-8220/20/21/6318

[16] Y. Luo et al., “Butterworth Low-Pass Filter Applications in Physiological Signal Processing,” *Sensors*, vol. 20, no. 24, 2020. [Online]. Available: https://www.mdpi.com/1424-8220/20/24/7343


