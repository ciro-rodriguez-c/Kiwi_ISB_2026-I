                                                                                     El Filtro de Wavelet:

El Filtro de Wavelet permite un análisis de tiempo-frecuencia. Esto es vital para señales como el EKG o el EEG, que son no estacionarias (sus características cambian con el tiempo).
Importancia
El Filtro de Wavelet es fundamental en el procesamiento de bioseñales porque permite un análisis tiempo-frecuencia simultáneo. Este método es ideal para el EKG y EEG, cuyas características cambian dinámicamente en el tiempo.
Su relevancia radica en el uso de una "Wavelet Madre": una plantilla matemática que se correlaciona con la morfología real de la señal (como el complejo QRS). Esto permite aplicar la Transformada Wavelet Discreta (DWT) para descomponer la señal, filtrar el ruido mediante umbralización (Hard o Soft Thresholding) y reconstruirla sin deformar los componentes diagnósticos esenciales que los filtros tradicionales suelen suavizar en exceso [1], [2], [5].




<img width="538" height="535" alt="imagen" src="https://github.com/user-attachments/assets/4a7e0334-d480-439f-bd46-cb23bdb1702c" />



                         Proceso transformada de Wavelet. [5]





Tipo de ruido que elimina y sus frecuencias
Este filtro es una herramienta versátil que actúa sobre diversos tipos de contaminación sin comprometer las bandas de interés clínico:
•	En EKG: Elimina eficazmente la deriva de línea de base (ruido de baja frecuencia provocado por la respiración y movimiento del torso) y el ruido de alta frecuencia, preservando la integridad del intervalo ST y la onda P [4].
•	En EEG: Es altamente selectivo para suprimir artefactos oculares (parpadeos) y ruido muscular (EMG). Su precisión permite limpiar la señal sin afectar las frecuencias rápidas de las bandas Gamma o Beta, cruciales para el análisis neurofisiológico [3].

Referencias Bibliográficas (Formato IEEE):


[1] D. L. Donoho, "De-noising by soft-thresholding," IEEE Transactions on Information Theory, vol. 41, no. 3, pp. 613-627, May 1995, doi: 10.1109/18.382009.


[2] P. S. Addison, "Wavelet transforms in biomedical engineering," Annals of Biomedical Engineering, vol. 30, no. 1, pp. 115-128, Jan. 2002.


[3] M. Balamareeswaran and D. Ebenezer, "Denoising of EEG signals using Discrete Wavelet Transform Based Scalar Quantization," Biomedical and Pharmacology Journal, vol. 8, no. 1, pp. 235-242, 2015.


[4] M. K. Stiles, D. Clifton, N. R. Grubb, J. N. Watson, and P. S. Addison, “Wavelet‐Based Analysis of Heart‐Rate‐Dependent ECG Features,” Annals of Noninvasive Electrocardiology, vol. 9, no. 4, pp. 316–322, Oct. 2004, doi: https://doi.org/10.1111/j.1542-474x.2004.94566.x.


‌ [5] “Transformada Wavelet – acervo para el mejoramiento del aprendizaje de alumnos de ingeniería, en Inteligencia Artificial.” https://virtual.cuautitlan.unam.mx/intar/?page_id=1108
‌



