# Filtros Digitales para Señales Biomédicas: EEG, ECG, EMG
## Filtro Butterworth
El filtro Butterworth es un filtro digital del tipo IIR (Infinite Impulse Response) ampliamente utilizado en el procesamiento de señales biomédicas debido a su respuesta en frecuencia suave y su banda pasante maximálmente plana, es decir sin presencia de oscilaciones fuertes (ripple). Es importante recalcar que el principal atributo como ya se mencionó es la estabilidad de la banda de paso, sin embargo este filtro presenta un desfase considerable que debe tratarse con cuidado dependiendo de las señales analizadas [2].
### Importancia
Como ya se mencionó, este filtro toma relevancia en el ámbito biomédico porque preserva amplitudes con una fidelidad muy aceptable, es simple de diseñar, tiene bajo costo computacional y es eficiente [1].
Es versátil para implementar como tipo de filtro pasa-bajos, pasa-altos, pasa-banda o rechaza-banda.
### Tipo de ruido que elimina y sus frecuencias
Las frecuencias atenuadas por el filtro Butterworth dependen del rango fisiológico esperado de la señal biomédica analizada [3]. En ECG, por ejemplo, suele preservarse el contenido entre 0.5 Hz y 40 Hz, mientras que componentes inferiores pueden asociarse a variaciones lentas de línea base y componentes superiores a ruido muscular o electrónico. De manera similar, en EEG y EMG se seleccionan distintas bandas de frecuencia según las características fisiológicas de cada señal [4]. 
### Referencias
[1] M. S. Hossain et al., “Wearable Device-Based Heart Rate Variability Analysis Using Butterworth Filtering Techniques,” *Sensors*, vol. 25, no. 22, 2025. [Online]. Available: https://www.mdpi.com/1424-8220/25/22/7091

[2] J. M. Smith and P. A. Lewicki, “Linear Phase FIR Digital Filters for Biological Signal Processing,” *IEEE Transactions on Biomedical Engineering*, 1986. [Online]. Available: https://pubmed.ncbi.nlm.nih.gov/3721526/

[3] A. T. Sehgal et al., “Noise Reduction and Signal Processing Techniques for ECG Signals,” *Sensors*, vol. 20, no. 21, 2020. [Online]. Available: https://www.mdpi.com/1424-8220/20/21/6318

[4] Y. Luo et al., “Butterworth Low-Pass Filter Applications in Physiological Signal Processing,” *Sensors*, vol. 20, no. 24, 2020. [Online]. Available: https://www.mdpi.com/1424-8220/20/24/7343
