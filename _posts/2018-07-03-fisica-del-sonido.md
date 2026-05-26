---
layout: post
title: "Física del sonido"
date: 2018-07-03 20:17:14 +0000
categories:
  - "Acústica"
  - "Fí­sica"
tags:
  - "absorción del sonido"
  - "Acústica de salas"
  - "coeficiente de absorción medio"
  - "coeficiente de absorción sonora"
  - "Efecto Doppler"
  - "fórmula de Sabine"
  - "Intensidad del sonido"
  - "recorrido libre medio"
  - "velocidad del sonido"
math: true
---
{% raw %}

En anteriores artículos de la categoría "Acústica" hemos sobre todo realizado una descripción de las características del sonido y de la música, un tipo especial de sonido. En este  artículo tratamos los detalles desde un punto de vista más matemático.
### Intensidad del sonido

El sonido es una *onda elástica de presión*, la intensidad que percibimos en el sonido es proporcional al cuadrado de de la amplitud de la vibración (esto es así para el movimiento ondulatorio en general). También podemos expresar la intensidad en función de la variación máxima de presión del aire originada por el sonido al propagarse, como vamos a ver a continuación.

La presión del aire, cuando propaga el sonido, es variable en cada punto, y por tanto el volumen que ocupa una cantidad fija de aire también varia con la presión.

[caption id="attachment_150645" align="aligncenter" width="485"]![](/assets/images/ona-longitudinal.png) Fig. 1: Onda longitudinal de presión: desplazamientos instantáneos[/caption]

Imaginemos (figura 1) un volumen de aire dentro de un pequeño cilindro de área *S* y longitud *dx*, situado inicialmente entre las posiciones *x*, *x + dx*, con volumen *V = S·dx*,  que es atravesado por la onda de expansión (el sonido) en la dirección de el eje X; decimos que sea pequeño para aproximar el frente de onda a una onda plana, cuando en realidad es esférica. El cilindro se desplazará y ensanchará sólo en la dirección X (la base *S* es transversal a X, y la onda es longitudinal según X) de forma que las posiciones de los extremos serán *(x + dy)* y *(x + dx + dy)*, donde llamamos y a la elongación de la onda, que recordemos es longitudinal y por tanto paralela al eje X.

El el nuevo volumen será* S(dx + dy)*, luego el incremento de volumen es *dV = S·dy*. Luego:
$\frac{\operatorname dV}V=\frac{S\operatorname dy}{Sdx}=\frac{\operatorname dy}{\operatorname dx}$ [1]

No confundamos la variable *y* con la dimensión vertical del eje de ordenadas: aquí *y* representa la elongación de la onda longitudinal en la dirección horizontal.

Por otro lado, la velocidad de propagación de una onda longitudinal en un medio elástico sólo depende de su densidad $\rho$ y del denominado [módulo de compresibilidad](https://es.wikipedia.org/wiki/M%C3%B3dulo_de_compresibilidad) $\chi=-V\frac{\triangle p}{\triangle V}$ [2], donde p es la presión, según la igualdad:
$v=\sqrt{\frac\chi\rho}$ [3]

Combinando las expresiones [1] y [2], e identificando las variaciones finitas $\triangle$ con las diferenciales:
$\chi=-\cancel{\operatorname dV}\frac{\operatorname dx}{\operatorname dy}\frac{\operatorname dp}{\cancel{\operatorname dV}}=-\operatorname dp\frac{\operatorname dx}{\operatorname dy}$

Sustituimos en la expresión de la velocidad [3]:
$v=\sqrt{-\operatorname dp\frac{\operatorname dx}{\rho\operatorname dy}}\Rightarrow-\operatorname dp=v^2\rho\frac{\operatorname dy}{\operatorname dx}$ [4]

Supongamos ahora que el sonido es un movimiento ondulatorio armónico (por tanto, es un sonido musical simple, puro) con elongación dada por
$y=A\sin\omega\left(t-\frac xv\right)$ [5]

Derivamos respecto x manteniendo t constante:
$\frac{\operatorname dy}{\operatorname dx}=-\frac Av\omega\cos\left(t-\frac xv\right)$

Sustituimos el valor de dy/dx en [4]:
$\operatorname dp=Av\rho\omega\cos\omega\left(t-\frac xv\right)=\widehat A\cos\omega\left(t-\frac xv\right)$ [6]

que nos dice que *la variación de presión debida al sonido se propaga como una onda de presión*, con amplitud $\widehat A$ y que, comparada con la onda de elongación [5], *está adelantada en fase 90⁰* (ya que depende de la función coseno en vez de la seno).

El valor máximo de la sobrepresión es $\operatorname dp_{MAX}=Av\rho\omega$; en general, la intensidad de una onda (energía que atraviesa la unidad de superficie normalmente a ella en la unidad de tiempo) es $I=\frac12A^2\rho\omega^2v$, de donde deducimos, usando [6]:
$\frac{\operatorname d{p^2}_{MAX}}I=\frac{A^2v^2\rho^2\omega^2}{\frac12A^2\rho\omega^2v}=2v\rho\Rightarrow\boxed{I=\frac{\operatorname d{p^2}_{MAX}}{2v\rho}}$

*La intensidad del sonido es proporcional al cuadrado de la sobrepresión  máxima asociada a la onda de presión*.
### Cálculo de la velocidad del sonido en el medio ambiente

En el aire y en condiciones normales, las variaciones de presión son muy rápidas, y se puede considerar que no da tiempo al intercambio de calor (un gas al ser comprimido se calienta y al ser expandido se enfría), en términos termodinámicos, son *variaciones de presión adiabáticas*. Supongamos que el aire se comporta aproximadamente como un gas perfecto, cumpliendo la* ecuación de los gases ideales en expansión adiabática*, $pV^\gamma=cte$ [7], donde $\gamma$ es el *coeficiente adiabático*. Diferenciando: $\operatorname dp\cdot V^\gamma+\gamma V^{\gamma-1}\cdot\operatorname dV=0\Rightarrow\operatorname dp\cdot V+\gamma\operatorname dV=0$, de donde $\operatorname dp=-\gamma p\frac{\operatorname dV}V$. Sustituyendo en la expresión [2]:
$\operatorname dp=-\gamma p\frac{\operatorname dV}V,\;\chi=-V\frac{-\gamma p\frac{\operatorname dV}V}{\operatorname dV}=\gamma p$

Sustituyendo en la velocidad [3]:
$v=\sqrt{\frac\chi\rho}=\sqrt{\frac{\gamma p}\rho}$ [8]

Para el aire es $\gamma=1.4$; además, a 0⁰ grados Celsius y presión p = 1atm = 1.013·10⁵ N/m², la densidad del aire es ρ = 1.293  kg/m³, sustituyendo en [8] obtenemos
$v=\sqrt{\frac{1.4\cdot1.013\cdot10^5}{1.293}}=331$

Vemos que con consideraciones teóricas obtenemos un valor muy de acuerdo con las mediciones experimentales. Nos damos cuenta, además, de que la velocidad del sonido en el aire dependerá de la temperatura, pues con ella variará la presión atmosférica. Usando la ecuación de los gases perfectos pV = nRT, para eliminar la presión *p* de la ecuación [8] se obtiene (T en grados Kelvin):
$v=\sqrt{\frac{\gamma RT}M}$ [9]

En la figura 2 vemos la variación de v según la temperatura obtenida aplicando [9] para un rango de [0, 30] grados centígrados, es prácticamente lineal, variando unos 0,6 m/s por cada grado.

[caption id="attachment_150649" align="aligncenter" width="630"]![](/assets/images/vel_so_temp.png) Fig. 2: Variación de la velocidad del sonido con la temperatura[/caption]
### Efecto Doppler

Cuando oímos un tren que se acerca con el silbato actuando, nos parece que el sonido es más agudo que si el tren se aleja de nosotros. El mismo efecto se observó con la luz, su frecuencia parece más alta cuando el foco emisor se acerca a nosotros que cuando se aleja, si la luz es visible, en el primer caso vemos la luz "más azul" (corrimiento al azul) y en el segundo, "más roja" (corrimiento al rojo). Veamos la expresión exacta que nos da el corrimiento en frecuencia.

[caption id="attachment_150659" align="alignnone" width="360"]![](/assets/images/Doppler.png) Fig. 3: foco de sonido y receptor en movimiento mutuo. Efecto Doppler.[/caption]

En la figura 3 representamos la situación: un observador O se mueve hacia la derecha con velocidad v y un foco de luz se mueve en dirección contraria con velocidad u (todo con respecto a un sistema de referencia que suponemos fijo); los frentes de onda se suponen planos (realmente son esféricos). La velocidad del sonido relativa al foco es w, y la absoluta (respecto al suelo) será u + w, mientras que la velocidad relativa al observador O será u + w - v (estamos suponiendo que las velocidades son mucho menores que la de la luz, y por ellos despreciando los efectos relativistas).

La frecuencia percibida del sonido es el número de ondas que llegan al receptor por segundo; en el caso de observador y foco en reposo, esa frecuencia será ν, y está relacionada con la velocidad w de la onda y su longitud λ por la relación w = λ·ν, de donde ν = w/ λ.  Cuando el foco de sonido se mueve, el número de ondas por segundo que  llegan a un receptor no será el mismo, y se percibirá una frecuencia ν' distinta. La onda de sonido en sí no cambia: su longitud de onda, su amplitud, su forma, no cambian, sólo que su velocidad relativa al observador sí lo hace (figura 4).

[caption id="attachment_150660" align="alignnone" width="300"]![](/assets/images/ona_lambda-300x191.png) Fig. 4: onda sinusoidal, se desplaza a velocidad w relativa a una referencia fija[/caption]

Desde el punto de vista del foco, que se mueve en la misma dirección que los frentes de onda y con velocidad u, se emiten ν ondas por segundo, y se "ven" los frentes de onda alejándose del foco a velocidad (w - u), por ello el foco verá una longitud de onda de λ = (w - u) / ν.

Veamos ahora el punto de vista del observador O, que se mueve a velocidad v acercándose al foco, y por tanto verá moverse a los frentes de onda a velocidad (v + w). Razonando de la misma forma que para el foco, verá una longitud de onda λ = (v + w ) / ν'. Igualando las dos expresiones para λ:
$\lambda=\frac{w-u}\nu=\frac{w+v}{\nu'}$

que nos proporciona la relación buscada entre frecuencia emitida f y frecuencia observada f'. Por ejemplo, si el silbato de un tren emite un sonido de frecuencia f = 440 Hz (440 ondas por segundo), estamos parados respecto al suelo (luego v = 0) y el tren se acerca hacia nosotros a velocidad u = 30 m/s, la frecuencia percibida será:
$\frac{331-30}{440}=\frac{331+0}{f'}\Rightarrow f'=484 m/s$

donde hemos tomado para la velocidad del sonido w = 331 m/s. Cuando el tren llega a nuestra posición para empezar a alejarse de nosotros, tendremos una velocidad  u = -30 m/s, luego:
$\frac{331-(-30)}{440}=\frac{331+0}{f'}\Rightarrow f'=403 m/s$

Vemos que se aprecian claramente variaciones de frecuencia de aproximadamente un 9% del valor real, en más o en menos.
### Acústica de salas

Para terminar con este breve paseo por la física del sonido, vemos la física del acondicionamiento de salas para escuchar música.

Cuando en una sala un emisor emite un sonido breve (una nota musical o una sílaba si es un orador), la onda sonora se expande por la sala, reflejándose en las paredes, suelo y techo. A un oyente que esté en el otro extremo le llegará el sonido primero por el camino directo más corto, pero un instante más tarde recibirá las ondas reflejadas, con menor intensidad. Las reflejadas siguen expandiéndose por la sala y se vuelven a reflejar una y otra vez, llegando cada vez más atenuadas al oyente, hasta que son demasiado débiles para ser percibidas. Decimos que hay **reverberación en la sala** para resumir este fenómeno de estar oyendo el sonido directo y reflejado. La reverberación refuerza el sonido: si salimos al aire libre se oirá menos. Tiene también un grave inconveniente: si se emiten más notas o sílabas, puede pasar que se mezclen en nuestro oído varias notas: las que llegan de forma directa y las anteriores que todavía están reverberando, las notas "se pisan" unas a otras.

En las iglesias antiguas se tenia en cuenta esto: la reverberación es grande allí, ayudando a que se oiga bien en el otro extremo, pero obliga a hablar lentamente, para dar tiempo a que se disipen las palabras anteriores. El **tiempo de reverberación de una sala** se define como el tiempo que tarda en hacerse inaudible el sonido reflejado. más exactamente, se define como es tiempo después del cual la intensidad del sonido es la millonésima parte. Se intuye que el tiempo de reverberación óptimo depende de la finalidad de la sala: para conferencias estará cerca de un segundo, para un concierto de rock será inferior y para un concierto de órgano será mayor.

Para ajustar la reverberación de una sala podemos usar materiales más o menos absorbentes del sonido en las paredes; en cada reflexión se pierde una parte de la energía: el **coeficiente de absorción sonora** α es la fracción de energía absorbida: si I es la energía incidente,  I' es la reflejada, entonces se cumple *I' = I·(1-α)*. Para α cercano a 1, el sonido es absorbido totalmente por la superficie. En la [página del portal de Acústica y Sonido](http://acusticaysonido.com/?p=148) encontraremos más detalles del coeficiente α y una tabla de valores para distintos materiales. Sucede que α no es constante para cada material, sino que depende de la frecuencia del sonido; algunos valores típicos son 0.02 para paredes de hormigón, 0.08 para el yeso, o 0.80 para el poliuretano, a una frecuencia de 1 KHz. Para ajustar la reverberación podemos poner o quitar superficies con α cercano a 1: alfombras, cortinas gruesas, etc. Incluso la ropa que llevan puesta los espectadores influye en la reverberación: una sala repleta de gente en verano con poca ropa reverbera más que en invierno con más ropa.

Puede demostrarse, haciendo un estudio estadístico de todas las múltiples reflexiones en las diversas superficies, que la intensidad del sonido decrece exponencialmente con el tiempo, y que el tiempo de reverberación de la sala viene dado aproximadamente por la **fórmula de Sabine**:
$T=0.16\frac V{S\overline\alpha}$

donde S es la superficie total de las paredes, V el volumen de la sala, y $\overline\alpha$ es el **coeficiente de absorción medio** de la sala, calculado promediando todos las superficies de la sala:
$\overline\alpha=\frac{{\overline\alpha}_1S_1+{\overline\alpha}_2S_2+\dots}{S_1+S_1+\dots}$

Se puede tener en cuenta también la absorción del sonido por el aire: en salas grandes el recorrido del sonido entre reflexiones será también mayor, y el efecto será más notable, especialmente a frecuencias altas. Se puede demostrar que el **recorrido libre medio** L, que se define como la media de los tramos recorridos entre reflexiones sucesivas, vale
$L=\frac{4V}S$

Podemos pues complementar el coeficiente de absorción α con un término adicional que tenga en cuenta la absorción por el aire, que a su vez depende del recorrido libre medio:
$\alpha'=\overline\alpha+kL$

donde k es una constante que depende de las condiciones físicas del aire (temperatura, humedad, presión ...).

**Ejemplo práctico**

*Una habitación destinada a audición musical tiene un tiempo de reverberación de 1s. Se pone un tabique hecho del mismo material que las paredes, de forma que la superficie total S de la habitación aumenta un 20%, evidentemente el volumen V no varia. Calcular el nuevo tiempo de reverberación*.

Antes de poner el tabique teníamos, por la formula de Sabine,

$T=0.16\frac V{S\overline\alpha}=1$

Con el tabique será

$T'=0.16\frac V{1.2S\overline\alpha}$

dividiendo la 1a por la 2a:

$\frac T{T'}=1.2\Rightarrow T'=\frac T{1.2}=\frac{\displaystyle1}{\displaystyle1.2}=\frac56\approx0.8s$
{% endraw %}