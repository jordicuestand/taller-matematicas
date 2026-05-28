---
layout: post
title: "Radio y centro de curvatura de una trayectoria"
date: 2016-09-05 10:05:47 +0000
categories:
  - "Cinemática"
  - "Fí­sica"
tags:
  - "aceleración tangencial"
  - "centro curvatura"
  - "componentes intrínsecas de la aceleración"
  - "radio curvatura"
math: true
---
{% raw %}

### Trayectorias diferenciables: radio y centro de curvatura

Cuando un punto móvil P se mueve en el espacio describe una trayectoria que en el caso más general es una curva; en el caso de que esta curva sea "suave", esto es, sin cambios de trayectoria bruscos, será diferenciable, esto es, podrá aproximarse localmente por una circunferencia (en el caso de un movimiento plano) o una esfera (caso de movimiento en el espacio). En la figura 1 se representa una trayectoria plana con dos puntos no diferenciables (en rojo); se denomina a esta curva diferenciable a trozos, pues podemos distinguir en ella tres secciones en las cuales la curva sí es suave.

$caption id="attachment_150106" align="alignnone" width="458"$![Fig. 1: Trayectoria curva en general](/taller-matematicas/assets/images/Corba_diferenciable.png) Fig. 1: Trayectoria curva, en dos dimensiones, en general[/caption]
Así, en las cercanías del punto móvil P, podemos aproximar la trayectoria por una circunferencia (o esfera) de centro C y radio R, siempre que la curva sea suave en P (figura 2). Llamamos a C al **centro de curvatura de la trayectoria** en P, y a R el **radio de curvatura de la trayectoria** en P.

$caption id="attachment_150107" align="alignnone" width="436"$![Fig. 2: aproximación local en el punto P por una circunferencia](/taller-matematicas/assets/images/Corba_diferenciable2.png) Fig. 2: aproximación local en el punto P por una circunferencia[/caption]
En general, el centro y el radio van variando conforme P se mueve, esto es, C y R son propiedades locales de la trayectoria (figura 3). En el caso particular de movimiento circular evidentemente serán constantes. Otro caso particular es el del movimiento rectilíneo, en el que consideramos que R es infinito y que el centro C está en el infinito.

$caption id="attachment_150108" align="alignnone" width="445"$![Fig. 3: El centro C y radio de curvatura R van variando a medida que el punto describe la trayectoria](/taller-matematicas/assets/images/Corba_diferenciable3.png) Fig. 3: El centro C y radio de curvatura R van variando a medida que el punto describe la trayectoria[/caption]
### Aceleración y curvatura

Siempre que hay un cambio de dirección en una trayectoria de un móvil, ha de existir una aceleración; es por ello que es de esperar que exista alguna relación entre las propiedades puramente geométricas radio y centro de curvatura de la trayectoria en un punto P y el vector aceleración de P.  Sabiendo esa relación, podríamos deducir la geometría de la trayectoria a partir del vector aceleración, o bien calcular la aceleración a partir del conocimiento de la trayectoria.

Consideremos un movimiento Δs del punto P en la trayectoria s (figura 4) suficientemente pequeña para que se pueda considerar que en esa sección la trayectoria sea aproximadamente circular con radio R y centro C.

$caption id="attachment_150109" align="alignnone" width="329"$![Fig. 4: el punto P se mueve hasta otra posición muy próxima P](/taller-matematicas/assets/images/Corba_diferenciable4.png) Fig. 4: el punto P se mueve hasta otra posición muy próxima P' a lo largo de la trayectoria s[/caption]
Consideremos también una referencia fija Ref, con centro en O. El vector velocidad en el punto P se puede expresar como el límite de la velocidad media en el sector Δs:

$\overrightarrow v=\lim_{\triangle t\rightarrow0}\frac{\overrightarrow{OP}'-\overrightarrow{OP}}{\triangle t}=\frac{\operatorname d\overrightarrow{OP}}{\operatorname dt}=\frac{\overrightarrow t\cdot\operatorname ds}{\operatorname dt}=\overrightarrow t\cdot v,$

donde hemos definido el vector $\overrightarrow t$ como un vector  unitario en la dirección del vector velocidad (también llamado versor velocidad), que sabemos que es tangente a la trayectoria s en el punto P, y v es el módulo de la velocidad en el punto, también llamado **celeridad**. Observemos que al hacer el límite la cuerda Δs y el segmento PP' van a coincidir.

Ahora que tenemos la velocidad, obtenemos la aceleración derivando respecto la referencia fija:

$\overrightarrow a=\frac{\operatorname d\overrightarrow v}{\operatorname dt}=\frac{\operatorname d\overrightarrow t}{\operatorname dt}v+\overrightarrow t\cdot\frac{\operatorname dv}{\operatorname dt}=\frac{\operatorname d\overrightarrow t}{\operatorname dt}v+\overrightarrow t\cdot a$; [1]

para obtener la derivada del vector unitario tangente, primero pensamos que a medida que el punto P cambia de dirección, el versor t irá girando, moviéndose en un círculo (esfera en el caso de movimiento en el espacio) de radio 1 (pues es un vector unitario).

$caption id="attachment_150111" align="alignnone" width="218"$![](/taller-matematicas/assets/images/versor_tangent-1.png) Fig. 5: el versor velocidad, tangente a la trayectoria, describe un círculo unitario[/caption]

Si el versor gira un ángulo θ en radianes, siendo el radio la unidad, la longitud de arco valdrá también θ; definiendo el vector unitario n como muestra la figura 5, y llamando t, t' a los versores tangentes, tendremos,

$\overrightarrow t'-\overrightarrow t\approx\theta\cdot\overrightarrow n$

la aproximación será buena si el ángulo θ es pequeño, pues el arco y la cuerda serán casi coincidentes, y en el límite será exacta:

$\operatorname d\overrightarrow t=\operatorname d\theta\cdot\overrightarrow n$,
además, en el límite dθ el vector normal n será perpendicular al versor velocidad t; como éste es a su vez tangente a la trayectoria s, tendremos que el vector n será perpendicular a la trayectoria: es un vector normal unitario a la trayectoria, llamado versor normal. 

$caption id="attachment_150112" align="alignnone" width="300"$![Fig. 6: el versor normal n és perpendicular al versor velocidad, apunta siempre al centro de curvatura de la trayectoria](/taller-matematicas/assets/images/versor-normal-300x177.png) Fig. 6: el versor normal n és perpendicular al versor velocidad, apunta siempre al centro de curvatura de la trayectoria[/caption]

Ahora podemos expresar la derivada temporal del versor velocidad tangencial en función del versor normal:

$\frac{\operatorname d\overrightarrow t}{\operatorname dt}=\frac{\operatorname d\theta\cdot\overrightarrow n}{\operatorname dt}=\frac{\operatorname d\theta}{\operatorname ds}\frac{\operatorname ds}{\operatorname dt}\cdot\overrightarrow n.$ [2]

En la figura 4 vemos que podemos expresar el arco recorrido en función del ángulo girado y del radio de curvatura R: $\nabla s=R\nabla\theta$, que pasado al límite es

$\operatorname ds=R\operatorname d\theta\Leftrightarrow R=\frac{\operatorname ds}{\operatorname d\theta}$ [3]

Usando [3] en [2]:

$\frac{\operatorname d\overrightarrow t}{\operatorname dt}=\frac{\operatorname d\theta}{\operatorname ds}\frac{\operatorname ds}{\operatorname dt}\cdot\overrightarrow n=\frac1Rv\cdot\overrightarrow n$ [4]

Sustituimos [4] en [1] y resulta:

$\boxed{\overrightarrow a=\frac{\operatorname d\overrightarrow t}{\operatorname dt}v+\overrightarrow t\cdot a=\frac{v^2}R\overrightarrow n+\overrightarrow t\cdot a={\overrightarrow a}_n+{\overrightarrow a}_t}$ [5]
que es una generalización de los resultados conocidos del movimiento circular a trayectorias en general, siendo $a_n$ la **aceleración normal** y $a_t$ la **aceleración tangencial**, también llamadas **componentes intrínsecas de la aceleración**. Dado un movimiento con una trayectoria diferenciable la ecuación [5] relaciona el vector aceleración con el radio de curvatura y la celeridad. Para obtener el centro de curvatura C, observamos en la figura 6 que el vector $\overrightarrow{PC}$ será igual a $R \overrightarrow{n}$ [7].

#### Procedimiento general de obtención del radio y centro de curvatura de una trayectoria

Dados los vectores velocidad y aceleración $\overrightarrow{v}, \overrightarrow{a}$, encontramos la celeridad v, el versor tangente $\overrightarrow t=\overrightarrow v/v$, el módulo a de la aceleración, la aceleración tangencial y la normal ${\overrightarrow a}_t=a\cdot\overrightarrow t,\;{\overrightarrow a}_n=\overrightarrow a-{\overrightarrow a}_t$, el módulo de la velocidad normal, $a_n=\left|\left|\;{\overrightarrow a}_n\right|\right|$, e igualamos este valor con v²/R, para obtener el radio: $R=\frac{v^2}{\left|\left|\;{\overrightarrow a}_n\right|\right|}$. Por último, usamos [7] para obtener el centro de curvatura C.

**Ejemplo**: Desde un punto O de la costa observamos un barco situado en P, midiendo la distancia r = 1000m y el ángulo θ = 30⁰ formado por su visual y el eje de dirección Norte-Sur tal como muestra la figura 7, en la que también se incluyen el supuesto centro de curvatura C de la trayectoria del barco. Medimos también, en un instante dado, las velocidades radial y angular, dr/dt = 19m/s, dθ/dt = 0.3 ⁰/s, y las aceleraciones radial y angular, d²r/dt² = 2 m/s², d²θ/dt² = 0.05 ⁰/s². Calcular la posición del centro de curvatura C y el radio de curvatura R de la trayectoria del barco usando la base vectorial móvil {12} de la figura y la referencia móvil que usa estos ejes y el origen P. Este ejemplo está tomado de los apuntes de la asignatura de Mecánica de la Escuela Superior de Ingenieros Industriales, escritos por el catedrático Joaquím Agulló.

$caption id="attachment_150116" align="aligncenter" width="364"$![Fig. 6: Esquema del movimiento de un barco visto desde la costa](/taller-matematicas/assets/images/Agulló_F3_Exemple2.png) Fig. 7: Esquema del movimiento de un barco visto desde la costa[/caption]
Primero de todo necesitamos obtener los vectores velocidad y aceleración en la base móvil {123}, siendo el eje 3 perpendicular al plano definido por {12}; el vector posición de P en esta base es evidentemente (r, 0 , 0). Derivamos este vector expresado en la base móvil respecto a la referencia fija (ver "Derivación de vectores respecto a bases móviles" en el post [Cinemática vectorial: sistemas de referencia, vectores posición, velocidad y aceleración](http://tallermatematic.ovh/wp/index.php/2016/08/12/cinematica-vectorial/)) teniendo en cuenta que la velocidad angular de la base {123} es el vector $\left(0,0,\overset.\theta\right)$, con lo cual:

 
$\begin{array}{l}\begin{array}{l}{\left\{\frac d{dt}\overrightarrow{OP}\right\}}_{Ref\;fija}=\\\frac d{dt}\;\begin{bmatrix}r\\0\\0\end{bmatrix}\;+\;\begin{bmatrix}0\\0\\\overset.\theta\end{bmatrix}\times\begin{bmatrix}r\\0\\0\end{bmatrix}=\begin{bmatrix}\overset.r\\0\\0\end{bmatrix}+\begin{bmatrix}0\\\overset.\theta r\\0\end{bmatrix}=\begin{bmatrix}\overset.r\\\overset.\theta r\\0\end{bmatrix}\end{array}\\\end{array}$

Sustituimos los valores del enunciado, y calculamos la celeridad:

$\overrightarrow v=\begin{bmatrix}\overset.r\\\overset.\theta r\\0\end{bmatrix}=\begin{bmatrix}19\\\left(0.3\frac{2\mathrm\pi}{360}\right)\cdot1000\\0\end{bmatrix}=\begin{bmatrix}19\\5\mathrm\pi/3\\0\end{bmatrix};\;v=\sqrt{19^2+\left(5\mathrm\pi/3\right)^2}\approx20\frac ms.$

Derivamos la velocidad para obtener la aceleración, recordando de volver a aplicar la fórmula de derivación respecto referencias fijas de vectores en bases móviles:

${\left\{\frac d{dt}\overrightarrow v\right\}}_{Ref\;fija}=\frac d{dt}\begin{bmatrix}\overset.r\\r\overset.\theta\\0\end{bmatrix}+\begin{bmatrix}0\\0\\\overset.\theta\end{bmatrix}\times\begin{bmatrix}\overset.r\\r\overset.\theta\\0\end{bmatrix}=\begin{bmatrix}\overset{..}r\\\overset.r\overset.\theta+r\overset{..}\theta\\0\end{bmatrix}+\begin{bmatrix}-r\overset.\theta^2\\\overset.r\overset.\theta\\0\end{bmatrix}=\begin{bmatrix}\overset{..}r-r\overset.\theta^2\\2\overset.r\overset.\theta+r\overset{..}\theta\\0\end{bmatrix}.$

Sustituimos valores:

$\overrightarrow a=\begin{bmatrix}\overset{..}r-r\overset.\theta^2\\2\overset.r\overset.\theta+r\overset{..}\theta\\0\end{bmatrix}=\begin{bmatrix}2\\1\\0\end{bmatrix}\;m/s^2$

La aceleración tangencial será la proyección de la aceleración sobre la dirección del vector velocidad tangente:

${\overrightarrow a}_t=a\cdot\frac{\overrightarrow v}v=\sqrt{4+1}\cdot\frac1{20}\begin{bmatrix}19\\5\mathrm\pi/3\\0\end{bmatrix}\;=\begin{bmatrix}19\sqrt5/20\\\sqrt5\mathrm\pi/60\\0\end{bmatrix}\approx\begin{bmatrix}2\\0.6\\0\end{bmatrix}\;m/s^2$

la aceleración normal la obtenemos restando:

${\overrightarrow a}_n=\overrightarrow a-{\overrightarrow a}_t\approx\begin{bmatrix}2\\1\\0\end{bmatrix}-\begin{bmatrix}2\\0.6\\0\end{bmatrix}\;=\begin{bmatrix}0\\0.4\\0\end{bmatrix}$,

igualamos el módulo de este vector con v²/R, para obtener el radio de curvatura: $0.4=20^2/R\Rightarrow R=1000m.$ El centro de curvatura lo encontramos a partir de la expresión [7]:

$\overrightarrow{PC}=R\overrightarrow n=1000\cdot\begin{bmatrix}0\\1\\0\end{bmatrix}=\begin{bmatrix}0\\1000\\0\end{bmatrix}.$
{% endraw %}