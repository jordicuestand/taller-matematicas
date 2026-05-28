---
layout: post
title: "Teoría cinética de los gases"
date: 2020-08-05 16:15:56 +0000
categories:
  - "Fí­sica"
  - "Termodinámica"
tags:
  - "constante de Boltzmann"
  - "presión"
  - "principio de Maxwell"
  - "recorrido libre medio"
math: true
---
{% raw %}

La teoría cinética de los gases, originaria del siglo XIX, es un modelo de la realidad que utiliza la mecánica de Newton, algunos conceptos de la Estadística, y la teoría molecular de la materia, para explicar el porqué de las propiedades macroscópicas observadas de los gases, como la presión, la temperatura o la conducción del calor.

Su hipótesis base es la siguiente: un gas está formado por un gran número de moléculas que se mueven de forma caótica (en todas direcciones, y cambiando a menudo de dirección) que chocan de forma elástica (se conserva la energía cinética) entre sí y con las paredes del recipiente que contiene al gas. A partir de esta imagen, se deducen la propiedades y comportamientos observados en el gas.

**Ejemplo 1**: en una caja de un litro que contiene gas hidrógeno a temperatura ambiente y presión atmosférica hay 0.09 gr de masa, N = 4·10²² moléculas, cada molécula ocupa un volumen de $V=4^{-27}m^{3}$, ocupando un volumen total molecular NV = 1.7·10⁻⁴m³ = 1.7·10⁻¹ litros, o sea un 17% del volumen total, el resto del volumen, 83%, está vacío. Cada molécula se mueve a una velocidad media de 1838 m/s, unos 2km por segundo. Vemos que el número de moléculas es muy elevado, que ocupan poco espacio del total disponible, y que se mueven muy rápido, a esa velocidad sólo tardan 5 cienmilésimas de segundo en ir de un lado al otro de la caja que contiene al gas.

### Presión de un gas confinado

$caption id="attachment_150765" align="alignnone" width="279"$![](/taller-matematicas/assets/images/teoria_cinetica1.png) Fig. 1: moléculas de un gas en movimiento aleatorio[/caption]
Consideremos un gas confinado en un recipiente de forma cualquiera y  de volumen *V*; habrán moléculas moviéndose en cualquier dirección. Fijamos una de las direcciones, a la que llamamos X, y pensamos en moléculas que, en un instante dado, se mueven en esa dirección;  las velocidades de esas moléculas en la dirección X pueden ser de módulos distintos *v* , y cambian continuamente. Nos acercamos a una de las paredes del recipiente, que supondremos plana y de superficie S (si no es plana, siempre podemos considerar una pequeña parte de la pared, y despreciar la curvatura), y consideramos una pequeña distancia d de la pared, dada por *d = v·dt*, la distancia recorrida por una molécula en un diferencial de tiempo, suficientemente pequeña para suponer que en ese espacio la molécula no chocará con otras.

$caption id="attachment_150768" align="alignright" width="125"$![](/taller-matematicas/assets/images/teoria_cinetica2.png) Fig.2: moléculas moviéndose en la dirección X dentro de un pequeño volumen d·S[/caption]
Pensemos ahora en todas las moléculas que en un instante t se mueven en la dirección X y llamemos *N* a su número. Las que ocupan el volumen *dV =  S·d = S-v·dt*, serán *(N/V) · dV*. ya que *N/V* son las moléculas que se mueven en dirección X por unidad de volumen. Las que no se muevan estrictamente en esa dirección pero tengan una componente de velocidad no nula según X también las contaremos, sólo no entran en el cómputo las velocidades ortogonales a X.

Como todas las direcciones y sentidos son *igualmente probables*, en la dirección X la mitad se moverán en el sentido positivo y la otra mitad en el sentido negativo, por tanto  el numero de moléculas que se mueven hacia la pared del recipiente y están dentro del volumen considerado será:

$\operatorname dN_X=\frac12\left(\frac NV\right)\left(Sv\operatorname dt\right)\;\;\;\lbrack1\rbrack,$

Veremos más tarde que la distancia que recorren las moléculas entre choques sucesivos es grande comparada con su tamaño (denominada *recorrido libre medio*), por tanto esta aproximación de considerar que, en la distancia *d* no chocaran entre sí, es aceptable.

Nos fijamos ahora en *los choques elásticos de las moléculas contra la pared*, la cual tiene una masa enorme en comparación con las moléculas, por ello, supondremos que la pared no cambia su velocidad tras el choque. La conservación del impulso en el choque implica que, para cada molécula, se conserva todo el impulso sólo que la velocidad cambia de sentido:

$\operatorname dp=m\cdot\triangle v=m\left(v-\left(-v\right)\right)=2mv$.

La variación total de impulso para todas las moléculas que chocan en la dirección X será el producto de la variación de cada molécula por la expresión [1]:

$\operatorname dp_X=\left(2mv\right)\cdot\frac12\frac NVSv\operatorname dt=\frac{mv^2NS}V\operatorname dt\;\;\;\lbrack2\rbrack$

En la mecánica de Newton, la variación del impulso con el tiempo es una fuerza, F = dp/dt, o bien F·dt = dp; aplicándolo a [2] y sumando para todos los módulos de velocidades v posibles en la dirección X:

$F\cancel{\operatorname dt}=\operatorname dp_X=\frac{mS}V\left(\sum_vv^2N_v\right)\cancel{\operatorname dt}\;\;\;\lbrack2b\rbrack$,

dónde hemos llamado $N_v$ al número de moléculas que tienen una velocidad de módulo v en la dirección X, es necesario distinguirlo, pues estamos sumando para todas las posibles velocidades *v*. y además hemos eliminado el término dt. Tenemos pues la presión P = F/S ejercida por los choques moleculares sobre la pared:

$P=F/S=\frac mV\left(\sum_vv^2N_v\right)\;\;\lbrack3\rbrack$

Debido a que será imposible en la práctica obtener la suma indicada para cada molécula, trabajamos con los valores medios: definimos la* velocidad cuadrática media según la dirección X*:

$\overline{v_x^2}=\frac{\left(\sum_vv^2N_v\right)}{N_T}\;\;\lbrack4\rbrack$.

que no es más que la media ponderada de velocidades al cuadrado: cada velocidad cuadrática v² posible va ponderada por su número $N_v$, sumadas todas, y dividimos el total por el número total de moleculas del gas $N_T$. La presión [3] la expresamos en función de [4]:

$P=\frac{mN}V\overline{v_x^2}\;\;\lbrack5\rbrack$

Consideremos ahora una dirección cualquiera y una velocidad v en esa dirección; se descompondrá según los ejes coordenados en $v=\left(v_x,v_y,v_z\right)$, y su módulo al cuadrado será igual a $v^2=v_x^2+v_y^2+v_z^2$, y de la misma forma encontramos el valor medio del cuadrado de la velocidad, $\overline {v^2}=\overline{v_x^2}+\overline{v_y^2}+\overline{v_z^2}$. Como los tres ejes, X, Y, Z, son equivalentes en un movimiento al azar, para cada uno de ellos la velocidad cuadrática media será la misma, y en particular podemos escribir $\overline {v^2}=3\cdot\overline{v_x^2}$. Entonces, la expresión [5] podemos expresarla en función de la velocidad cuadrática general:

$P=\frac13\frac{mN_T}V\overline{v_{}^2}\;\;\lbrack6\rbrack$

Observamos ahora que $N_T·m$ es la masa total del gas (masa de cada molécula por número total de moléculas), y por tanto $N_T·m/V$ es la densidad del gas, que denominamos $\rho$. Por ello, expresamos [6] así:

$P=\frac13\rho\overline{v_{}^2}\;\;\lbrack7\rbrack$

que literalmente nos dice *la presión de un gas contra las paredes del recipiente que lo contiene es proporcional a la densidad del gas y a la velocidad cuadrática media de sus moléculas*. También podemos expresar [6] de esta otra forma:

$PV=\frac13mN\overline{v_{}^2}\;\;\lbrack8\rbrack$

que nos recuerda a la ecuación de estado de los gases perfectos, *PV = nRT*.

**Ejemplo 2**: El gas hidrógeno tiene una densidad de 0.09 g/l = 0.09 Kg/m³ a temperatura ambiente y presión atmosférica (1 atm = 101325 Pa), aplicando [7] podemos encontrar la velocidad cuadrática media de la molécula de hidrógeno:

$P=\frac13\rho\overline{v^2}\Rightarrow\overline{v^2}=\frac{3P}\rho=\frac{3\cdot101325}{0.09}\frac{N/m^2}{kg/m^3}=3.38\cdot10^6\frac{N\cdot m}{kg}$

Recordando que [Newton = kg·m/s²] vemos que [Newton·m/kg] = [kg·m²/s²·kg] = [m²/s²]. La velocidad media molecular será $\overline v=\sqrt{3.38\cdot10^6}=1837\;m/s$, una velocidad muy elevada, del orden de 2Km por segundo.

### Energía cinética interna

La energía cinética total interna del gas es la suma de las moleculares:

$E_c=\sum_i\frac12mv_i^2=\frac12m\sum_i{\textstyle v_i}{\textstyle{}^2}$

Usando la definición de velocidad cuadrática media, ${\textstyle\overline{v^2}}{\textstyle=}\frac1{N_T}\sum_i{\textstyle v_i}{\textstyle{}^2}$, y la expresión [8]:

$E_c=\frac12m\overline{v^2}\cdot N_T=\frac123PV\Rightarrow PV=\frac23E_c\;\;\;[9]$

En el modelo que estamos usando de moléculas vistas como masas puntuales, *el producto presión·volumen es proporcional a la energía cinética total de las moléculas*.

### Gases perfectos monoatómicos

Comparando [9] con la ecuación de estado de los gases perfectos PV = nRT, podemos aventurar que la temperatura T debe de estar relacionada con la energía cinética total; consideremos un mol de gas perfecto (n = 1), y recordemos que la constante universal de los gases, R, tiene dimensiones [Joules / Kelvin], o sea que relaciona energía con temperatura. Por otra parte, la capacidad calorífica a volumen constante de un gas compuesto de moléculas monoatómicas es igual a $c_V=3R/2\;\;\;[10]$; recordando el primer principio de la termodinámica, $Q=W+\triangle E$, tomando W = 0 (un proceso de calentamiento del gas sin trabajo), y identificando la energía interna del gas con su energía cinética total (no tenemos otras formas de energía en este modelo), tenemos que $Q=\triangle E_C=c_V\triangle T$.Usando [10] y simplificando:

$\cancel\triangle E_C=c_V\cancel\triangle T\Rightarrow E_C=c_VT=\frac{3R}2T$

Usando ahora [9]:

$\frac32PV=\frac{3R}2T\Rightarrow\boxed{PV=RT}$

hemos obtenido la ecuación de estado de los gases perfectos monoatómicos.

### La constante de Boltzmann

En la ecuación [8] cuando consideramos un mol de gas implica que el número total de moléculas $N_T$ es igual al [número de Avogadro](https://es.wikipedia.org/wiki/Constante_de_Avogadro): $PV=\frac13mN_A\overline{v_{}^2}\;$. Definamos la *energía cinética media molecular* a partir de la velocidad cuadrática media:

$\overline{E_c}=\frac12m\overline{v^2}$

Entonces:

$PV=\frac13N_Am\overline{v_{}^2}\;=\frac13N_A\cdot2\cdot\overline{E_c}=\frac23N_A\overline{E_c}$

pero por la ecuación [7], *PV = RT*, deducimos:

$RT=\frac23N_A\overline{E_c}\Rightarrow\boxed{\overline{E_c}=\frac32\left(\frac R{N_A}\right)T=\frac32kT}\;\;\;\lbrack10\rbrack$

donde $k=R/N_A$ es la[ constante de Boltzmann](https://es.wikipedia.org/wiki/Constante_de_Boltzmann), relacionando directamente energía cinética con temperatura.

**Ejemplo 3**: Para el gas hidrógeno a P = 1atm y V = 1m³, obtenemos una energía cinética media molecular de:

$PV=101325\cdot1=\frac236\cdot10^{23}\cdot\overline{E_C}\Rightarrow\overline{E_C}=\frac{3\cdot101325}{2\cdot6\cdot10^{23}}=2.5\cdot10^{-19}J$

### Principio de Maxwell de equipartición de la energía

En [10] y anteriores estamos relacionando exclusivamente la energía interna del gas con las velocidades moleculares, o sea con la energía cinética; como las direcciones X, Y, Z son equivalentes, podemos descomponer la participación de las velocidades en la energía cinética en tres componentes del mismo valor; usando [10]:

$\left.\begin{array}{r}\overline{E_c}={\overline{E_c}}_X+{\overline{E_c}}_Y+{\overline{E_c}}_Z\\{\overline{E_c}}_X={\overline{E_c}}_Y={\overline{E_c}}_Z\end{array}\right\}\Rightarrow{\overline{E_c}}_X=\frac13\overline{E_c}=\frac12kT$

Llamando *grado de libertad* a cada dirección independiente de la velocidad (y de la energía), diremos que el gas monoatómico tiene tres grados de libertad (ejes X, Y, Z) y que cada grado de libertad contribuye con el valor $\frac12kT$ a la energía interna del gas.

En moléculas poliatómicas, cuando aumentamos su energía además de la energía cinética hay otras energías mecánicas que participan: la energía de rotación de la molécula, proporcional al momento de inercia y al cuadrado de la velocidad angular, $\frac12I\omega^2$, y la energía elástica, proporcional a la constante elástica y al cuadrado de la elongación, $\frac12Ax^2$. Diremos que el gas poliatómico tiene más grados de libertad que el monoatómico.

El principio de equipartición enuncia que *cada contribución a la energía total del gas, debida a cada grado de libertad, participa en la energía total interna en la misma medida,  $\frac12kT$*. Así pues, en un gas poliatómico con 5 grados de libertad (tres de movimiento, más uno de rotación y uno de vibración elástica), la energia total en función de la temperatura vendrá dada por

$E=\frac52kT\;\;\;\lbrack11\rbrack$

En general, si el gas admite L grados de libertad, la relación entre su energía interna y su temperatura será $E=\frac L2kT$, en particular, ese gas aumentará menos su energía cinética, a una temperatura T dada, que un gas monoatómico; como hemos visto que la energía cinética del gas es proporcional a la temperatura, deducimos que dada una transferencia de calor Q, *los gases poliatómicos aumentaran menos de temperatura que los monotaómicos*. Otra forma de decir lo mismo es que *el coeficiente calorífico de un gas poliatómico es mayor que el de un gas monoatómico*; de hecho puede demostrarse que $c_V=\frac L2R$.
{% endraw %}