---
layout: post
title: "Física -> Electricidad y Magnetismo -> Corriente alterna"
date: 2017-02-07 11:08:09 +0000
categories:
  - "Electricidad y Magnetismo"
tags:
  - "corriente alterna"
  - "corriente eléctrica"
  - "factor de potencia"
  - "frecuencia de resonancia"
  - "Fresnel"
  - "impedancia"
  - "intensidad eficaz"
  - "reactancia"
  - "reactancia capacitiva"
  - "reactancia inductiva"
  - "RLC"
  - "tensión eficaz"
  - "valor eficaz"
math: true
---
{% raw %}

En los orígenes de la industria eléctrica se descubrió que el transporte de la electricidad es más económico cuando se usa corriente alterna en vez de continua, y desde entonces las instalaciones de potencia cambian la polaridad de la corriente con una frecuencia de 50 ciclos por segundo, o 50 Hertz (en Europa), mientras que en las transmisiones por ondas electromagnéticas se usan frecuencias de millones de Hertz. Este artículo trata sobre cálculo de parámetros de circuitos simples en corriente alterna.

### Corriente alterna

Es toda corriente eléctrica cuya intensidad es una función periódica del tiempo y con un sentido de circulación que se invierte también periódicamente. En Análisis Matemático se demuestra que estas funciones periódicas se pueden descomponer en serie de funciones sinusoidales de la forma $A_i\sin\left(\omega_it\right)$, con unas frecuencias que son múltiplos de la más baja; por tanto, toda corriente alterna en general (abreviadamente c.a.) se puede considerar igual a la superposición de corrientes alternas sinusoidales; por ello, basta con estudiar éste último tipo de c.a.

### Circuito RLC serie con corriente alterna


En la figura 1 vemos un tramo de circuito con una resistencia R, una inductancia L y un condensador C conectados en serie; supongamos que es recorrido por una c.a. de intensidad $i=I\sin\left(\omega t\right)$, y que en un instante t circula de izquierda a derecha, provocando una caída de tensión $V_A-V_B=iR$ en la resistencia, otra caída $V_B-V_C=L·i'$ en la inductancia, siendo i' la derivada respecto del tiempo de la intensidad i, y por último una caída $BV_c-V_D=q/C$ en el condensador, siendo q su carga y C su capacidad. En un instante dt la corriente lleva al condensador una carga dq = i·dt, por tanto la carga total es $q=\int i\cdot\operatorname dt$. La caída total de tensión en el tramo RLC es la suma:

$\triangle V=Ri+L\frac{\operatorname di}{\operatorname dt}+\frac1C\int i\cdot\operatorname dt$ [1]

Como la intensidad es una función sinusoidal, y las derivadas e integrales de funciones sinusoidales también son sinusoidales, la caída de tensión será a su vez una función sinusoidal tal como

$\triangle V=V_0\sin\left(\omega+\varphi\right)$


Sustituyendo en [1]:

$V_0\sin\left(\omega+\varphi\right)=V_A-V_D=Ri+L\frac{\operatorname di}{\operatorname dt}+\frac1C\int i\operatorname dt$

Esta es una ecuación que matemáticamente parece complicada; en el siguiente apartado vemos los instrumentos para operarla fácilmente, usando sólo geometría elemental.

### Representación del potencial periódico mediante los vectores de Fresnel

Al derivar e integrar la intensidad sinusoidal el resultado tiene un desfase respecto la original; en efecto:

$\frac{\operatorname d\;}{\operatorname dt}A\sin\left(\omega t\right)=A\omega\cos\left(\omega t\right)=A\omega\sin\left(\omega t+\frac{\mathrm\pi}2\right)$

Propiedad 1: La derivada temporal de la función sinusoidal es también sinusoidal con la misma pulsación $\omega$, con amplitud modificada por el factor $\omega$, y con una fase adelantada en $\frac{\mathrm\pi}2$.

Obviamente para la integral tendremos un resultado como este:

Propiedad 2: La integral temporal de la función sinusoidal es también sinusoidal con la misma pulsación $\omega$, con amplitud modificada por el factor $1/\omega$, y con una fase retrasada en $\frac{\mathrm\pi}2$.

Un movimiento oscilatorio simple de pulsación $\omega$ y amplitud A puede representarse por un vector de módulo constante igual a la amplitud A, que efectúa un movimiento circular uniforme con velocidad angular constante $\omega$, es la denominada representación de Fresnel de la oscilación. Entonces, como tanto la intensidad i(t) como su derivada e integral tienen la misma pulsación, si las representamos con vectores de Fresnel girarán con la misma velocidad angular, con módulos distintos, y con un desfase de $\frac{\mathrm\pi}2$ entre ellos; la suma [1] se podrá obtener como suma de los tres vectores.


 En la figura 3 se representan las diferencias de potencial: la $V_A-V_B$ debido a la resistencia R tiene por módulo RI, y lo representamos sobre el eje X; a continuación, la $V_B-V_C$ debida a la inductancia L tiene por módulo $L\omegaI$ y forma un ángulo de 90⁰ en el sentido contrario a las agujas del reloj con el vector $V_A-V_B$ (propiedad 1); por último, la $V_C-V_D$ debida al condensador tiene por módulo $I(C\omega)^{-1}$ y forma un ángulo de -90⁰ con el vector $V_A-V_B$ (propiedad 2). La suma vectorial de estos tres vectores se representa en azul, y nos da la diferencia de potencial del tramo completo del circuito, $V_A-V_D$. Llamando $\theta$ al ángulo del vector $V_A-V_D$, es evidente que

$\tan\left(\theta\right)=\frac{L\omega I_0-I_0C^{-1}\omega^{-1}}{RI_0}\Rightarrow\theta=\tan^{-1}\left(\frac{L\omega I_0-{\displaystyle\frac1{C\omega}}}R\right)$ [2]

Por otro lado, aplicando el teorema de Pitágoras al triángulo ABE, y llamando V a la diferencia de potencial $V_A-V_D$, obtenemos:

$V^2=I_0^2R^2+I_0^2\left(L\omega-\frac1{C\omega}\right)^2\Rightarrow I_0=\frac V{\sqrt{R^2+\left(L\omega-\frac1{C\omega}\right)^2}}$ [3]

Las ecuaciones [2] y [3] relacionan la intensidad y la diferencia de potencial en un circuito RLC de corriente alterna.

### Impedancia y reactancia

 La ecuación [3] podemos expresarla en forma compacta: I = V / Z, donde Z es la **impedancia** del circuito,

$Z=\sqrt{R^2+\left(L\omega-\frac1{C\omega}\right)^2}$ [4]

De esta forma, la relación entre intensidad y tensión queda parecida a la ley de Ohm de corriente continua, I = V / R, sustituyendo la resistencia R por la impedancia Z, la cual es también una medida de a oposición del circuito al paso de corriente, y también se mide en Ohms.

De forma parecida, podemos simplificar la ecuación [2],

$\theta=\tan^{-1}\left(\frac{L\omega I_0-{\displaystyle\frac1{C\omega}}}R\right)=\tan^{-1}\left(\frac XR\right)$

hemos definido la **reactancia** del circuito, X:

$X=L\omega I_0-\frac1{C\omega}$ [5]

que puede ser positiva o negativa; en los casos particulares de circuitos RC (sin inductancia) se dice que tenemos una **reactancia capacitiva**, que será negativa, y en circuitos RL (sin capacitancia) una **reactancia inductiva**, que será positiva.

Mirando la figura 3 veremos que, cuando la reactancia sea positiva, la intensidad, que está sobre el eje X, estará retrasada un ángulo $\theta$ respecto la tensión V (la línea azul resultante), mientras que para reactancias negativas será al contrario, la intensidad irá avanzada respecto la tensión.

Usando la reactancia, la ecuación [4] queda aún más compacta:

$Z=\sqrt{R^2+X)^2}$ [5]

**Ejemplo 1**: Tenemos en serie una resistencia R, una bobina y un condensador. La bobina tiene resistencia despreciable y un coeficiente de autoinducción de 25mH. El condensador tiene una capacidad de 50μF. Sabiendo que la tensión instantánea es V = 120·sen(400t) y que la intensidad está adelantada 60⁰ respecto a la tensión, calcular el valor de R, la caída de tensión en la resistencia y el diagrama de Fresnel de tensiones.

El esquema del circuito es semejante al de la figura 1, y el diagrama de tensiones será como el de la figura 3. Con los datos que tenemos podemos calcular la reactancia del circuito:

$X=L\omega-\frac1{C\omega}=25\cdot10^{-3}\cdot400-\frac1{50\cdot10^{-6}\cdot400}=-40\Omega$

Vemos que la reactancia es negativa, mirando la figura 3 deducimos que el ángulo entre intensidad y tensión ha de ser negativo, e igual a -60⁰. Usando la ecuación [2], en la cual el numerador es igual a la reactancia X:

$\tan\left(-60⁰\right)=\frac XR=\frac{-40}R\Rightarrow R=\frac{40}{\tan\left(60⁰\right)}=\frac{40}{\sqrt3}\Omega$.

La caída de tensión en la resistencia viene dada por la ley de Ohm V = IR, que es una función sinusoidal:

$V=R\cdot I=\frac{40}{\sqrt3}\frac{3\sqrt3}2\sin\left(400t\right)=60\sin\left(400t\right)$.

Teniendo en cuenta el ángulo negativo, el diagrama de Fresnel del circuito tiene este aspecto:


![separador2](/taller-matematicas/assets/images/separador2.png)

### Valor eficaz de una corriente alterna

Siendo las tensiones e intensidades variables con el tiempo, a menudo interesa conocer su valor medio, más que su valor instantáneo. Para una función periódica en general y(t) de período T, su valor medio en ese intervalo de tiempo se define como

$\overline y=\sqrt{\int_0^Ty^2\left(t\right)\operatorname dt}$

Para el caso particular de una función sinusoidal,

$\overline y=\sqrt{\int_0^T\left$Y_0\sin\left(\omega t+\varphi\right)\right$^2\operatorname dt}$

Esta integral se resuelve fácilmente teniendo en cuenta la condición de periodicidad $y\left(t+T\right)=y\left(t\right)$ (que se puede expresar como $\omega T=2\pi$) y usando identidades trigonométricas, resulta:

$\overline y=\sqrt{\int_0^T\left$Y_0\sin\left(\omega t+\varphi\right)\right$^2\operatorname dt}=\frac{Y_0}{\sqrt2}$

A este valor medio de la función periódica se le conoce por **valor eficaz**; aplicado al caso de corriente alterna, tenemos la **tensión eficaz** $\frac{I_0}{\sqrt2}$ y la **intensidad eficaz** $\frac{V_0}{\sqrt2}$.

**Ejemplo 2**: En el ejemplo 1, la tensión eficaz entre los extremos de la resistencia vale $60/\sqrt2=42.43V$

### Resonancia eléctrica

En un circuito de c.a. decimos que hay resonancia eléctrica cuando no hay desfase entre la intensidad y la tensión; en un circuito RLC para que ello ocurra la reactancia ha de valer cero, o sea que
$L\omega=\frac1{C\omega}\Leftrightarrow\omega^2=\frac1{LC}$

A esta pulsación se la llama pulsación de resonancia, y a su frecuencia asociada, **frecuencia de resonancia** (del circuito RLC):
$f=\frac\omega{2\mathrm\pi}=\frac1{2\mathrm\pi\sqrt{LC}}$ [6]

El diagrama de Fresnel de un circuito RLC en resonancia tiene este aspecto:


Vemos que las variaciones de tensión en la inducción y el condensador tienen el mismo valor, pero con signos contrarios. Con ello, la variación en todo el circuito es la misma que en la resistencia, y las tensiones en la inducción y el con-


densador no tienen efectos externos al circuito, son valores internos. Ahora bien, podría darse el caso de que estas tensiones internas fueran grandes, incluso mucho mayores que la tensión externa aplicada (la que medimos en los extremos AD del circuito), apareciendo *sobretensiones* en los componentes L y C que hay que tener en cuenta en los aislamientos del circuito. Este hecho se puede aprovechar para diseñar *amplificadores de tensión*, en el que un circuito RLC produce internamente altas tensiones a partir de una tensión aplicada menor; una inductancia sometida a altas tensiones variables se comporta como un generador de ondas electromagnéticas: una antena emisora.

### Potencia, corriente activa y reactiva

La energía disipada en un circuito de corriente continua durante un período de tiempo t es W = VIt; en el caso de un circuito en c.a. nos interesa conocer la energía disipada en un período de oscilación T:

$W=\int_0^Tv\left(t\right)i\left(t\right)\operatorname dt$

Sustituyendo en esta expresión los valores v, i por las funciones sinusoidales,

$W=\int_0^TV_0I_0\sin\left(\omega t\right)\sin\left(\omega t+\theta\right)\operatorname dt$

donde $\theta$ es el desfase entre intensidad y corriente. Usando identidades trigonométricas, y la condición de periodicidad $\omega T=2\pi$ llegamos a

$W=\int_0^TV_0I_0\sin\left(\omega t\right)\sin\left(\omega t+\theta\right)\operatorname dt=\frac{V_0I_0}2T\cos\left(\theta\right)$

y la potencia media por período será el trabajo anterior dividido por el tiempo T:

$P=\frac WT=\frac{V_0I_0}2\cos\left(\theta\right)=\frac{V_0}{\sqrt2}\frac{I_0}{\sqrt2}\cos\left(\theta\right)=VI\cos\left(\theta\right)$ [7]

donde se han utilizado las definiciones de tensión e intensidad eficaces, I, V; a la cantidad $\cos\left(\theta\right)$ se la llama [**factor de potencia**](https://es.wikipedia.org/wiki/Factor_de_potencia) del circuito considerado:

La potencia media disipada por período en un circuito c.a. es igual al producto de la intensidad y tensión eficaz por el factor de potencia del circuito.

El vector de corriente i(t) formalmente se puede descomponer en dos componentes: una paralela al vector v(t) y otra perpendicular a él; imaginemos que el circuito es atravesado por esas dos corrientes superpuestas, una en concordancia de fase con la tensión, llamada **corriente activa**, la otra a 90⁰ de desfase, llamada **corriente reactiva**. Como el ángulo entre i(t) y v(t) es $\theta$, de la ecuación [7] deducimos que

$P=VI\cos\left(\theta\right)=VI_a$ [8]

o sea que la potencia consumida se debe a la intensidad activa $I_a$, la que está en fase con la tensión; esto puede verse como la consecuencia del hecho de que la potencia se consume sólo en las resistencias del circuito, la corriente activa es la que consume energía, mientras que las inductancias y condensadores (los ideales, que tienen resistencias internas despreciables) no consumen energía. Entonces la corriente reactiva no consume energía. Cuando en un circuito sólo tenemos resistencias, toda la corriente será activa; a medida que vamos conectando elementos capacitivos e inductivos, la intensidad y la tensión se van desfasando y aparece la corriente reactiva. Para una potencia P y una tensión eficaz V dadas, la ecuación [8] nos dice que como menor es el factor de potencia, mayor habrá de ser la intensidad: entonces, si tenemos una instalación de 220V con un factor de potencia bajo, las intensidades de corriente que necesitaremos para consumir una potencia dada fija será mayor que para un factor de potencia alto, es por tanto importante mantener todo lo alto posible el factor de potencia para disminuir la intensidad (altas intensidades calientan más los componentes y se pierde energía por disipación). el factor de potencia es un elemento clave en el diseño de componentes eléctricos y en la optimización de instalaciones.
{% endraw %}