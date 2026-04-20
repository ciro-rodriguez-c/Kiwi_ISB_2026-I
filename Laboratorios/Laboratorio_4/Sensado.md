# Laboratorio 4

---

## Fotos de la experiencia
### Foto de la conexión de la experiencias 1 (Tensión de puño)
![Experiencia 1](images/imagen_2026-04-18_154251315.png)
### Foto de la conexión de la experiencia 2 (Tobillo)
![Experiencia 2](images/imagen_2026-04-18_154337904.png)
---

## Ploteo de las señales
### Experiencia 1

### Experiencia 2


---

## Resumen y explicaciones
### Experiencia 1

En esta experiencia se registró una señal electromiográfica (EMG) del antebrazo mientras se realizaba la acción de cerrar el puño de forma repetida. La señal fue adquirida mediante el sistema BITalino y visualizada en el software OpenSignals.

Al observar la gráfica, se puede notar que la señal presenta variaciones constantes en su amplitud a lo largo del tiempo. En los momentos donde el músculo está en reposo, la señal se mantiene relativamente estable alrededor de un valor medio. Sin embargo, cuando se realiza la contracción del puño, aparecen picos de mayor amplitud, lo que indica un incremento en la actividad muscular.

Este comportamiento se explica porque la señal EMG representa la actividad eléctrica generada por las fibras musculares. Cuando el músculo se contrae, se activan más unidades motoras, lo que produce señales eléctricas más intensas y, por lo tanto, picos más altos en la gráfica.

Además, la señal presenta un patrón repetitivo de aumento y disminución de amplitud, lo cual coincide con la acción de contraer y relajar el puño varias veces durante la medición. También se observa que la señal es irregular y algo “ruidosa”, lo cual es normal en este tipo de registros, ya que se trata de la suma de múltiples señales musculares y posibles interferencias.

En conclusión, la señal obtenida refleja adecuadamente la actividad muscular del antebrazo durante la tensión del puño, mostrando una clara relación entre el nivel de esfuerzo realizado y la amplitud de la señal registrada.

### Experiencia 2

En esta experiencia se registró la señal EMG mientras se realizaba el movimiento del tobillo de forma repetida. A diferencia de la experiencia anterior, aquí la gráfica muestra picos mucho más marcados y separados entre sí, lo que hace más fácil identificar cada movimiento.

Cuando el tobillo estaba en reposo, la señal se mantenía bastante estable alrededor de un valor medio. Pero cada vez que se realizaba el movimiento (flexión o extensión), aparecían picos altos bien definidos. Esto indica que el músculo se activaba de forma más clara y puntual en cada repetición.

Algo que llama la atención es que los picos pareciesen ser más “ordenados” y espaciados en el tiempo, lo que sugiere que el movimiento fue más rítmico. Es decir, no fue una contracción continua como en el puño, sino más bien acciones separadas, una por una.

También se puede notar que la señal baja nuevamente después de cada pico, lo que corresponde al momento en que el músculo vuelve a relajarse. Este patrón se repite varias veces, mostrando claramente el ciclo de activación y descanso del músculo.

En general, la señal refleja bien el comportamiento del músculo del tobillo durante el movimiento: cada acción genera un pico claro en la gráfica, y entre cada una hay un periodo de reposo. Esto permite diferenciar fácilmente cuándo el músculo está activo y cuándo no.

---

## Código
```py
# Import OpenSignalsReader
from opensignalsreader import OpenSignalsReader
acq1 = OpenSignalsReader('opensignals_Tobillo-Adr.txt', show=True, raw=True)
acq2 = OpenSignalsReader('opensignals_Tension-Punno.txt', show=True, raw=True)
```
