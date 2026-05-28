---
layout: post
title: "Cinemática vectorial: sistemas de referencia, vectores posición, velocidad y aceleración"
date: 2016-08-12 09:56:41 +0000
categories:
  - "Cinemática"
  - "Vectores"
tags:
  - "aceleración de Coriolis"
  - "aceleración fictícia"
  - "bases móviles"
  - "cinemática"
  - "fuerza fictícia"
  - "mecánica vectorial"
  - "sistemas de referencia"
  - "sistemas inerciales"
  - "sistemas no inerciales"
  - "vecor posición"
  - "vector aceleración"
  - "vector velocidad"
math: true
---
{% raw %}

La **Cinemática** se ocupa de describir matemáticamente el movimiento de los cuerpos materiales, en este artículo sólo trataremos *cuerpos de dimensiones puntuales,* y en este caso simple la descripción del movimiento se basa en los conceptos de posición, velocidad y aceleración. La **Cinemática Vectorial**, parte de la **Mecánica Vectorial**, usa la matemática de los vectores, el Álgebra vectorial y el Cálculo diferencial vectorial, para describir y calcular posiciones, velocidades y aceleraciones.

El movimiento es siempre relativo a quién lo describe; el pasajero de un tren de alta velocidad describirá el movimiento dentro del tren de forma distinta a un observador que ve pasar el tren y mira en su interior. Es por esto que se necesita decidir un [**sistema de referencia**](https://es.wikipedia.org/wiki/Sistema_de_referencia) antes de calcular nada. En Mecánica Vectorial, escoger un sistema de referencia equivale a escoger un punto O origen de coordenadas, y una [base vectorial del espacio](https://es.wikipedia.org/wiki/Base_(%C3%A1lgebra)), que serán dos o tres vectores (dependiendo de si el espacio que consideramos es plano o tridimensional) *unitarios* (de módulo igual  la unidad) y perpendiculares entre sí (*ortogonales*), en el caso del espacio tridimensional, además escogemos una [orientación de la base](https://es.wikipedia.org/wiki/Orientaci%C3%B3n_(geometr%C3%ADa)).

## **Referencias y vector posición**

La cinemática del punto usa el concepto de [espacio euclídeo](https://es.wikipedia.org/wiki/Espacio_eucl%C3%ADdeo) para representar el espacio físico real: para definir un marco de referencia euclídeo debemos dar un **origen de coordenadas** O y una **base**, que para el espacio tridimensional es un conjunto de tres vectores ortogonales unitarios $e_1,e_2,e_3$ (también llamados *ortonormales*).


Cualquier punto P en el espacio tendrá asociado un **vector de posición** OP, que se expresará según una combinación lineal de los vectores de la base; esto significa que, dados dos sistemas de referencia con el mismo origen O pero distintas bases, los vectores de posición de un mismo punto del espacio P serán distintos en cada referencia. También, dos referencias con la misma base pero distintos orígenes O, O' darán, para un mismo punto del espacio, diferentes vectores de posición.

**Ejemplo 1**: En el sistema de referencia Ref1, el vector posición OP de un punto tiene por coordenadas (0, 2, 2); otro sistema de referencia Ref2 tiene los ejes paralelos a Ref1, y la misma base, pero su origen O' tiene coordenadas en Ref1 (0, 0, -2). Determinar el vector posición O'P en la referencia Ref2.


En la figura 2 vemos la geometría del problema; el vector O'P forma un triángulo con los vectores OP, OO'. Usando las propiedades de los vectores, O'P = O'O + OP; el vector O'O es el inverso de OO', el cual a su vez es el vector posición de O' respecto a O, que es un dato del problema: O'O = -OO' = - (0, 0, -2) = (0, 0, 2). Nos queda:

O'P = O'O + OP = (0, 0, 2) + (0, 2, 2) = (0, 2, 4).

**Ejemplo 2**: Cuando dos referencias Ref1, Ref2 difieren en sus bases, puede determinarse el vector posición en una referencia conociendo el de la otra usando la **matriz de cambio de base** [S]; se cumple, para un vector cualquiera u:

${\left\{\overset\rightharpoonup u\right\}}_{Ref1}=\left$S\right${\left\{\overset\rightharpoonup u\right\}}_{Ref2}$ [1]

donde la matriz [S]  tiene por columnas los componentes de la base de Ref2 en la base de Ref1. Por ejemplo, sea la base de Ref1 la habitual (1,0,0), (0,1,0), (0,0,1), y la base de Ref2 expresada según la base de Ref1, $\left(1/\sqrt2,1/\sqrt2,0\right),\;\left(1/\sqrt2,-1/\sqrt2,0\right),\;(0,0,1)$. La matriz de cambio de base es

$\left$S\right$=\begin{bmatrix}1/\sqrt2&amp;1/\sqrt2&amp;0\\1/\sqrt2&amp;-1/\sqrt2&amp;0\\0&amp;0&amp;1\end{bmatrix}$

Si el punto P tiene coordenadas (1,1,1) en Ref2, entonces en Ref1 serán

$\left$S\right$\cdot\left(1,1,1\right)=\begin{bmatrix}1/\sqrt2&amp;1/\sqrt2&amp;0\\1/\sqrt2&amp;-1/\sqrt2&amp;0\\0&amp;0&amp;1\end{bmatrix}\cdot\begin{bmatrix}1\\1\\1\end{bmatrix}=\begin{bmatrix}2/\sqrt2\\0\\1\end{bmatrix}$.

## Referencias móviles, y referencias galileanas

Se da el caso de que puede haber movimiento entre referencias: diremos que son **referencias móviles**; en el caso especial de que el movimiento sea rectilíneo uniforme, diremos que son *referencias galileanas*, también denominadas ***sistemas* de *referencia inerciales***. Un espacio euclídeo descrito por referencias galileanas representa un espacio físico homogeneo (todos los puntos tienen las mismas propiedades) e isótropo (en todas las direcciones posibles el espacio tiene las mismas propiedades), y un tiempo uniforme (transcurre al mismo ritmo en todo el espacio). Las [leyes de Newton](https://es.wikipedia.org/wiki/Leyes_de_Newton) fueron enunciadas, y sólo se cumplen en, sistemas de referencia inerciales.

Si la referencia móvil tiene aceleración (no describe un movimiento rectilíneo uniforme), decimos que es una **referencia no galileana**, o equivalentemente,  una **referencia no inercial**. En estas referencias no se cumplen las leyes de Newton.

Dado que, en la práctica, se dan muchos casos de movimientos complicados, que son composición de diversos movimientos, y dan lugar a ecuaciones y expresiones también complicadas, es muy útil expresar esos movimientos según vectores usando una base móvil, que "acompañe" al cuerpo móvil, para simplificar las expresiones. Pero hemos dicho que una base móvil con aceleración, no es un sistema de referencia inercial, y por tanto en ella no se cumplen las leyes de Newton. Para resolver este punto, se recurre al "truco" de encontrar los vectores posición, velocidad y aceleración respecto a una base fija inercial, en la que se cumplen las leyes de Newton, pero expresando las componentes de los vectores en una base móvil adecuada para simplificar las expresiones. Dado que la velocidad es la derivada de la función posición, y la aceleración es a su vez la derivada de la velocidad, lo que acabamos de decir implica que tenemos que saber derivar un vector que está expresado en una base que es móvil (no inercial, en general), respecto a otra base que es fija (más exactamente, inercial).

## Vector velocidad

El vector velocidad de un punto P relativo a la referencia Ref se define por la expresión

${\overset\rightharpoonup v}_{Ref}\left(P\right)={\left.\frac{\operatorname d\overset\rightharpoonup{OP}}{\operatorname dt}\right|}_{Ref}=\underset{\triangle t\rightarrow0}{lim}\frac{\overset\rightharpoonup{OP}\left(t+\triangle t\right)-\overset\rightharpoonup{OP}\left(t\right)}{\triangle t}$
Es importante notar que la derivada se define también respecto a la referencia; si la referencia no es fija sino que se está moviendo, la derivada tendrá que tener en cuenta la variación creada por este movimiento. Pensemos que, un punto fijo en una referencia Ref1, se verá como móvil en otra referencia Ref2 que se está moviendo respecto a Ref1.

## Derivación de vectores respecto a bases móviles

Supongamos que tenemos un vector cualquiera *u* expresado respecto a una base móvil. Para calcular su derivada respecto a una referencia fija:

${\left.\frac{\operatorname d\overset\rightharpoonup u}{\operatorname dt}\right|}_{Ref}={\textstyle\sum_{i=1}^3}\frac{\operatorname du_i}{\operatorname dt}\cdot{\overset\rightharpoonup e}_i+{\textstyle\sum_{i=1}^3}u_i\cdot{\left.\frac{\operatorname d{\overset\rightharpoonup e}_i}{\operatorname dt}\right|}_{Ref}$ [2]

donde las $e_i$ son los vectores de la base móvil, $u_i$ las componentes del vector u en la base móvil.  Damos ahora la siguiente propiedad algebraica, que no demostramos:

**Propiedad 1**: *la derivada temporal de una base móvil respecto a una referencia fija puede expresarse mediante el producto vectorial de la velocidad angular de la base por cada uno de los vectores de la base*.

${\left.\frac{\operatorname d\overset\rightharpoonup{e_i}}{\operatorname dt}\right|}_{Ref}=\overset\rightharpoonup\omega\times\overset\rightharpoonup{e_i}$ [3]

Usando [3] en [2] obtenemos

$\begin{array}{l}{\left.\frac{\operatorname d\overset\rightharpoonup u}{\operatorname dt}\right|}_{Ref}={\textstyle\sum_{i=1}^3}\frac{\operatorname du_i}{\operatorname dt}\cdot{\overset\rightharpoonup e}_i+{\textstyle\sum_{i=1}^3}u_i\cdot\overset\rightharpoonup\omega\times\overset\rightharpoonup{e_i}=\\{\textstyle\sum_{i=1}^3}{\textstyle\frac{\operatorname du_i}{\operatorname dt}}{\textstyle\cdot}{\textstyle\overset\rightharpoonup e}{\textstyle+}{\textstyle\overset\rightharpoonup\omega}{\textstyle\times}{\textstyle\sum_{i=1}^3}{\textstyle u}{\textstyle{}_i}{\textstyle\cdot}{\textstyle\overset\rightharpoonup{e_i}}{\textstyle=}{\textstyle\;}{\textstyle\sum_{i=1}^3}{\textstyle\frac{\operatorname du_i}{\operatorname dt}}{\textstyle\cdot}{\textstyle\overset\rightharpoonup e}{\textstyle+}{\textstyle\overset\rightharpoonup\omega}{\textstyle\times}{\textstyle\overset\rightharpoonup u}\end{array}$

Podemos resumir este resultado así:

$\boxed{{\left\{{\left.\frac{\operatorname d\overset\rightharpoonup u}{\operatorname dt}\right|}_{Ref}\right\}}_{base}={\left\{\frac{\operatorname d\overset\rightharpoonup u}{\operatorname dt}\right\}}_{base}+{\left\{\overset\rightharpoonup\omega{\textstyle\times}{\textstyle\overset\rightharpoonup u}\right\}}_{base}}$ [4],

que se expresará como propiedad así:

**Propiedad 2**: *La derivada temporal respecto de una referencia fija de un vector u expresado en una base móvil es igual a la derivada temporal respecto a la base móvil más el producto vectorial de la velocidad angular de la base móvil (respecto la referencia fija) por el vector u*.

**Ejemplo 2**: Un disco de radio R está girando respecto nuestro sistema de referencia fijo con una velocidad angular Ω. Encima del disco, a una distancia r del centro, una partícula P se está moviendo a velocidad constante y siguiendo una línea paralela al diámetro del disco, como muestra la figura 3; en el instante t = 0 ocupaba la posición O'. Definimos la referencia Ref1 como la fija, y la Ref2 con origen en O', un eje que sigue la trayectoria del punto, y el otro eje perpendicular al anterior; esta Ref2 vista desde la Ref1 gira con el disco, como se ve en la figura 3. Notar que, al no tener movimiento rectilíneo uniforme, Ref2 no es galileana. Hallar el vector velocidad de P respecto la Ref1 en (a) la base de Ref2, (b) la base de Ref1.

  ![](/taller-matematicas/assets/images/velocitat-base-mòbil3.png)

Fig. 3: referencias fijas y móviles
 La velocidad de P respecto la Ref1 viene dada por la derivada del vector OP respecto a Ref1; queremos expresar este vector en la base de la Ref2, que es móvil. Para ello, usamos la expresión [4], siendo el vector $\overrightarrow u=\overrightarrow{OP}$. El vector OP cumple OP = OO' + O'P, tenemos que expresar estos vectores en la base móvil de la Ref2:

$\begin{array}{l}{\left\{\overrightarrow{OP}\right\}}_{Ref2}={\left\{\overrightarrow{OO'}\right\}}_{Ref2}+{\left\{\overrightarrow{O'P}\right\}}_{Ref2}=\\\begin{bmatrix}0\\r\\0\end{bmatrix}+\begin{bmatrix}vt\\0\\0\end{bmatrix}=\begin{bmatrix}vt\\r\\0\end{bmatrix}\end{array}$

El vector velocidad angular de Ref2, expresado en la base de Ref2, es

${\left\{\Omega\right\}}_{Ref2}=\begin{bmatrix}0\\0\\\omega\end{bmatrix}$

ya que los ejes Z son paralelos en Ref1 y Ref2. Aplicamos [4]:

$\begin{array}{l}{\left\{{\left.\frac{\operatorname d\overset\rightharpoonup u}{\operatorname dt}\right|}_{Ref}\right\}}_{base}={\left\{\frac{\operatorname d\overset\rightharpoonup u}{\operatorname dt}\right\}}_{base}+{\left\{\overset\rightharpoonup\omega{\textstyle\times}{\textstyle\overset\rightharpoonup u}\right\}}_{base}=\\\frac d{dt}\begin{bmatrix}vt\\r\\0\end{bmatrix}+\begin{bmatrix}0\\0\\\omega\end{bmatrix}\times\begin{bmatrix}vt\\r\\0\end{bmatrix}=\begin{bmatrix}v\\0\\0\end{bmatrix}+\begin{vmatrix}i&amp;j&amp;k\\0&amp;0&amp;\omega\\vt&amp;r&amp;0\end{vmatrix}=\begin{bmatrix}v\\0\\0\end{bmatrix}+\begin{bmatrix}-r\omega\\\omega vt\\0\end{bmatrix}=\begin{bmatrix}v-r\omega\\\omega vt\\0\end{bmatrix}\end{array}.$ [5]

Para pasar este vector velocidad de la base de Ref2 a la de Ref1, usamos la matriz de cambio de base S, que recordemos que cumple ${\left\{u\right\}}_{Ref1}=\left$S\right$\cdot{\left\{u\right\}}_{Ref2}$, donde S es la matriz que tiene por columnas los vectores de la base Ref2 expresados según la base Ref1:

$\left$S\right$=\begin{bmatrix}\sin\left(\theta\right)&amp;\cos\left(\theta\right)&amp;0\\-\cos\left(\theta\right)&amp;\sin\left(\theta\right)&amp;0\\0&amp;0&amp;1\end{bmatrix}$ [6]

donde $\theta$ es el ángulo formado por los ejes de Ref2 y Ref1, que será igual a la velocidad angular por el tiempo: $\theta=\omega t$. Los coeficientes de la matriz S los deducimos de la geometría del problema:


Aplicamos el cambio de base:

${\left\{\overrightarrow v\left(P\right)\right\}}_{Ref1}=\left$S\right$\cdot{\left\{\overrightarrow v\left(P\right)\right\}}_{Ref2}=\begin{bmatrix}\sin\left(\theta\right)&amp;\cos\left(\theta\right)&amp;0\\-\cos\left(\theta\right)&amp;\sin\left(\theta\right)&amp;0\\0&amp;0&amp;1\end{bmatrix}\begin{bmatrix}v-r\omega\\\omega vt\\0\end{bmatrix}=\begin{bmatrix}\left(v-r\omega\right)\cdot sin\left(\omega t\right)+\omega vt\cdot cos\left(\omega t\right)\\-\left(v-r\omega\right)\cdot cos\left(\omega t\right)+\omega vt\cdot sin\left(\omega t\right)\\0\end{bmatrix}$ [7].

Comparando [5] con [7] vemos que el último tiene una expresión bastante más complicada, aunque hay que recordar que ambas expresiones son el mismo vector velocidad del punto P respecto Ref1, sólo que expresadas en bases distintas. Es por esto que puede ser conveniente trabajar con bases móviles, para simplificar las expresiones.  En la figura 5 vemos las gráficas de las componentes del vector velocidad [7] respecto al tiempo; son oscilantes con módulo creciente, ya que a medida que P se mueve hacia la periferia del disco, su distancia al centro de giro O aumenta, y por tanto también su velocidad lineal respecto Ref1 (respecto Ref2 es constante). Los picos de velocidad respecto a cada eje corresponden a ceros en el otro eje perpendicular.


**Ejemplo 3**: Consideramos el mismo disco del ejemplo 2, pero ahora el punto se está moviendo a lo largo de un radio.


En la referencia móvil Ref2, que está girando con el disco, la posición O'P es simplemente (0, r(t), 0), y el vector OP expresado en la base móvil será el mismo, {OP}ref2 = {O'P}ref2, ya que O y O' coinciden. La velocidad de P respecto la referencia fija Ref1 expresada en función de la base de Ref2 es:

$\begin{array}{l}{\left\{{\left.\frac{\operatorname d\overset\rightharpoonup{OP}}{\operatorname dt}\right|}_{Ref}\right\}}_{base}={\left\{\frac{\operatorname d\overset\rightharpoonup{OP}}{\operatorname dt}\right\}}_{base}+{\left\{\overset\rightharpoonup\omega{\textstyle\times}{\textstyle\overset\rightharpoonup{OP}}\right\}}_{base}=\\\frac d{dt}\begin{bmatrix}0\\r(t)\\0\end{bmatrix}+\begin{bmatrix}0\\0\\\omega\end{bmatrix}\times\begin{bmatrix}0\\r(t)\\0\end{bmatrix}=\begin{bmatrix}0\\r'(t)\\0\end{bmatrix}+\begin{vmatrix}i&amp;j&amp;k\\0&amp;0&amp;\omega\\0&amp;r(t)&amp;0\end{vmatrix}=\begin{bmatrix}0\\r'(t)\\0\end{bmatrix}+\begin{bmatrix}-r(t)\omega\\0\\0\end{bmatrix}=\begin{bmatrix}-r(t)\omega\\r'(t)\\0\end{bmatrix}\end{array}$

La componente $-r(t)\omega$ es perpendicular a la trayectoria de P, siendo la velocidad tangencial que sabemos del movimiento circular, la componente r'(t) es simplemente la derivada respecto al tiempo de la función r(t), con el sgnificado de velocidad en sentido radial.

## Vectores aceleración, aceleración centrípeta y de Coriolis

El vector aceleración de un punto P relativo a la referencia Ref se define por la expresión

${\overrightarrow a}_{Ref}\left(P\right)={\left.\frac{\operatorname d{\overrightarrow v}_{Ref}\left(P\right)}{\operatorname dt}\right|}_{Ref}=\underset{t\rightarrow0}{lim}\frac{{\overrightarrow v}_{Ref}\left(t+\triangle t\right)-{\overrightarrow v}_{Ref}\left(t\right)}{\triangle t}$ [8]
Es importante destacar que, al derivar respecto al tiempo el vector velocidad de un punto respecto a una referencia Ref, la derivada ha de realizarse respecto a la misma referencia Ref para que el resultado sea una aceleración, de lo contrario, ¡el vector obtenido puede no tener significado físico!

Además, la derivada nos da la variación instantánea, respecto a la referencia, del vector velocidad, que puede ser en módulo, en dirección, en sentido, o en una combinación de las tres. Por tanto, si una velocidad es nula en un momento dado, o bien tiene un módulo constante, no implica que su derivada sea nula.

**Ejemplo 4**: Calcular la aceleración de P del ejemplo 3 respecto a la referencia fija Ref1 en las coordenadas móviles de Ref2, considerando que la velocidad de rotación del disco es variable (el disco está acelerando).

Aplicamos la definición [8]

${\overrightarrow a}_{Ref}\left(P\right)={\left.\frac{\operatorname d{\overrightarrow v}_{Ref}\left(P\right)}{\operatorname dt}\right|}_{Ref}=\frac d{dt}{\begin{bmatrix}v-r\omega\\\omega vt\\0\end{bmatrix}}_{Ref}$

El vector velocidad viene dado según la base móvil Ref2, pero derivamos respecto a la base fija Ref1, por tanto usamos la expresión [4], abreviamos las derivadas respecto al tiempo usando apóstrofes: r' significa dr/dt, r'' significa d²r/dt², etc:

$\begin{array}{l}{\overrightarrow a}_{Ref}\left(P\right)=\frac d{dt}{\begin{bmatrix}-r(t)\omega\\r'(t)\\0\end{bmatrix}}_{Ref}=\frac d{dt}\begin{bmatrix}-r(t)\omega\\r'(t)\\0\end{bmatrix}+\overrightarrow\Omega\times\begin{bmatrix}-r(t)\omega\\r'(t)\\0\end{bmatrix}=\\\begin{bmatrix}-r'(t)\omega+r(t)\omega'\\r''(t)\\0\end{bmatrix}+\begin{bmatrix}i&amp;j&amp;k\\0&amp;0&amp;\omega\\-r(t)\omega&amp;r'(t)&amp;0\end{bmatrix}=\begin{bmatrix}-r'\omega+r\omega'-\omega r'\\r''(t)-\omega^2r\\0\end{bmatrix}=\\\begin{bmatrix}r\omega'-2\omega r'\\r''(t)-\omega^2r\\0\end{bmatrix}\end{array}$.

Tenemos aceleración en dos direcciones perpendiculares: ll componente $r''-r\omega^2$ da cuenta de la aceleración del punto P según r''(t) y además aparece una aceleración adicional, que tiene la misma dirección que el movimiento de P pero sentido contrario, y es la denominada [**aceleración centrípeta**, ](https://es.wikipedia.org/wiki/Aceleraci%C3%B3n_centr%C3%ADpeta)que sería la única componente que tendríamos si el punto P tuviera velocidad constante o nula respecto el disco.

Como P además se mueve respecto al disco, aparece un componente adicional de aceleración perpendicular al movimiento de P. En el caso particular de que el disco gire con velocidad angular constante, $\omega'=0$, este término perpendicular se reduce a $-2\omega r'$: esta aceleración tangencial se conoce como **aceleración de Coriolis**.

**Ejemplo 5**: calcular la aceleración del punto P del ejemplo 2 respecto a la referencia fija Ref1.

El vector velocidad viene dado según la base móvil Ref2, pero derivamos respecto a la base fija Ref1, por tanto usamos la expresión [4]:

$\begin{array}{l}{\overrightarrow a}_{Ref}\left(P\right)=\frac d{dt}{\begin{bmatrix}v-r\omega\\\omega vt\\0\end{bmatrix}}_{Ref}=\frac d{dt}\begin{bmatrix}v-r\omega\\\omega vt\\0\end{bmatrix}+\overrightarrow\Omega\times\begin{bmatrix}v-r\omega\\\omega vt\\0\end{bmatrix}=\\\begin{bmatrix}0\\\omega v\\0\end{bmatrix}+\begin{bmatrix}0\\0\\\omega\end{bmatrix}\times\begin{bmatrix}v-r\omega\\\omega vt\\0\end{bmatrix}=\begin{bmatrix}0\\\omega v\\0\end{bmatrix}+\begin{bmatrix}i&amp;j&amp;k\\0&amp;0&amp;\omega\\v-r\omega&amp;\omega vt&amp;0\end{bmatrix}=\\\begin{bmatrix}0\\\omega v\\0\end{bmatrix}+\begin{bmatrix}-\omega^2vt\\\omega\left(v-r\omega\right)\\0\end{bmatrix}=\begin{bmatrix}-\omega^2vt\\-r\omega^2\\0\end{bmatrix}\end{array}$

###### Sobre las aceleraciones y fuerzas "ficticias", o "pseudofuerzas"

Es una costumbre generalizada llamar ficticias a las aceleraciones que hemos visto que "aparecen" en el cálculo, al derivar vectores expresados en bases no inerciales respecto de bases inerciales, como la aceleración centrípeta o la de Coriolis; el motivo de rebajar estas aceleraciones, que de hecho existen, al rango de "ficticias", es por que, según nos dicen, no hay ningún agente que las provoque, "nadie hace fuerza" para provocar esas aceleraciones. Dado que la 2ª ley de Newton, *F = ma*, relaciona aceleración con fuerza, se sigue que a cada aceleración ficticia le podemos asociar una fuerza ficticia, o "pseudofuerza". Por ejemplo es esa (pseudo)fuerza centrífuga que, cuando vamos en un coche que coge una curva a gran velocidad, nos presiona contra la puerta que tenemos al lado.

Para mi humilde opinión, esta forma de discriminación entre aceleraciones confunde más que ayuda a comprender la realidad física. Todas las aceleraciones son reales, no existen las ficticias.

Las aceleraciones lo que son es cambios temporales de la velocidad: siempre que el vector velocidad cambie, hay una aceleración. En el caso de un sistema de referencia no inercial, es el propio espacio que tomamos como referencia el que está cambiando las velocidades, que recordemos, son relativas al sistema de referencia, y por tanto, por definición, hay aceleraciones. Estas aceleraciones son las responsables de, por ejemplo, variar la velocidad para que el móvil efectúe un movimiento circular (por tanto no rectilíneo uniforme)

Esto se ve muy bien en la teoría de la Relatividad General y su [principio de equivalencia: ](https://es.wikipedia.org/wiki/Principio_de_equivalencia)  la presencia de masa deforma el espacio circundante, que deja de ser euclídeo, por tanto cualquier sistema de referencia que lo represente será no inercial (recordemos que los inerciales se relacionan con espacios euclídeos), y aparecen aceleraciones vinculadas a  la referencia no inercia, en este caso especial, la aceleración no inercial es la gravedad.  De hecho, la gravedad no es una fuerza, sino una aceleración. El peso es la fuerza que contrarresta la aceleración de la gravedad, que nos sostiene en equilibrio; por eso en la [caída libre](https://es.wikipedia.org/wiki/Ca%C3%ADda_libre) no se experimenta peso alguno, hay sensación de ingravidez. Una explicación de este hecho, muy sencilla, a nivel divulgativo, es esta: [Espacio-tiempo curvo para todos los públicos](http://matfisfil.blogspot.com/2014/11/espacio-tiempo-curvo-para-todos-los.html).

Entonces, hay una aceleraciones producidas directamente por fuerzas aplicadas, y hay otras producidas por el espacio de referencia no inercial; en este último caso, también pueden existir fuerzas reales vinculadas: en el caso del coche que toma la curva, la fuerza que hace el asiento, el cinturón de seguridad, y quizás la puerta, sobre nosotros, es la que genera la aceleración centrípeta necesaria para que nuestra masa tome la curva; si soltamos el cinturón y abrimos la puerta, salimos despedidos hacia fuera del coche, en dirección tangencial a la curva, debido a que en ausencia de fuerzas nuestra masa vuelve a la referencia inercial sin aceleración: a la trayectoria recta. En cambio, la fuerza centrífuga si podría llamarse una pseudo-fuerza, pero creo que es más apropiado no llamarla de ningún modo, pues simplemente no existe: no hay ninguna fuerza que nos empuje fuera del coche en la curva, al contrario, hay una única fuerza real, la centrípeta, que nos obliga a tomar la curva.

![separador2](/taller-matematicas/assets/images/separador2-300x38.png)
{% endraw %}