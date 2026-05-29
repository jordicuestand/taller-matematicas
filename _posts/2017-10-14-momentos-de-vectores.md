---
layout: post
title: "Momentos de vectores"
date: 2017-10-14 10:19:34 +0000
categories:
  - "Fí­sica"
  - "Vectores"
tags:
  - "Eje central"
  - "momento mínimo"
  - "par vectorial"
  - "Reducción de sistemas de vectores"
  - "Trinomio invariante"
  - "Varignon"
  - "vector deslizante"
math: true
---
{% raw %}

### Introducción

En el artículo [Vectores en Física ](http://tallermatematic.ovh/wp/index.php/2016/08/11/vectores/)se habló de algunas propiedades geométricas de los vectores (la invariancia respecto de transformaciones de coordenadas) que son importantes para representar magnitudes físicas como la fuerza o la velocidad angular. En este artículo vemos el concepto teórico de momento de un vector respecto a un punto o a una recta, que físicamente tiene importancia para calcular el efecto que un vector ejerce respecto a ese punto o recta; un ejemplo práctico es la antigua [ley de la palanca](https://es.wikipedia.org/wiki/Palanca) de Arquímedes, que nos muestra cómo varía el efecto de una fuerza con el punto de aplicación: la fuerza P, más alejada del punto de apoyo, ejerce una acción de giro igual a la fuerza mayor R que está más cerca; esa "acción de giro" se materializa usando el concepto de momento de cada fuerza respecto al punto de apoyo.

![](/taller-matematicas/assets/images/moments0.png) Fig. 1: Ley de la palanca (By Dnu72 (Own work) [GFDL (http://www.gnu.org/copyleft/fdl.html) or CC BY-SA 4.0-3.0-2.5-2.0-1.0 (https://creativecommons.org/licenses/by-sa/4.0-3.0-2.5-2.0-1.0)], via Wikimedia Commons)Otro ejemplo lo vemos en la siguiente figura, en la que se representa la sección de un rodillo situado en un plano horizontal, al que hemos atado una cuerda r también horizontal en su parte superior.

![](/taller-matematicas/assets/images/moments.png) Fig. 2: un cilindro sujeto a una fuerza tangente efectuada tirando de una cuerda, el efecto de giro no depende del punto exacto de aplicación de la fuerza

Si ahora aplicamos una fuerza a lo largo de la cuerda, digamos $F_1$ o $F_2$, el efecto será que el rodillo adquirirá una velocidad angular w, que no dependerá más de la magnitud de la fuerza: fuerzas de magnitud igual producirán la misma velocidad angular, independientemente del punto de aplicación de la fuerza (círculos en azul). Físicamente, diremos que la rotación del cilindro es causada por el momento de la fuerza aplicada, y ese momento depende de la magnitud y de la dirección de la fuerza, pero no de su posición a lo largo de la recta r.

Cuando en una situación física encontramos vectores que se comportan de este modo, causando el mismo efecto independientemente de si movemos su punto de aplicación a lo largo de una recta, decimos que *los vectores son deslizantes*. Tiene pues sentido estudiar los momentos ya no de fuerzas, sino de vectores deslizantes en general.
### Momento de un vector respecto a un punto

Si un vector ***v*** tiene su origen (o está aplicado en) en punto P, el momento **m** de **v** con respecto a otro punto O se define por:

$\boldsymbol m=\left(P-O\right)\times\boldsymbol v$ [1]

donde la expresión (P-O) simboliza la diferencia de las coordenadas de los dos puntos, y el producto $\times$ representa el producto vectorial.

![](/taller-matematicas/assets/images/moments1.png) Fig. 3: momento m del vector v, aplicado en P, respecto del punto O

Recordemos que (P-O) puede verse como el vector **OP** con orígen en O y extremo en P; además, recordando las propiedades del producto vectorial, el vector momento **m** será perpendicular al plano formado por los vectores **v** y **OP**, y será un pseudovector, o vector polar (ver  [Vectores en Física](http://tallermatematic.ovh/wp/index.php/2016/08/11/vectores/)), su módulo valdrá el doble del área del triángulo formado por los vectores **v** y **OP**, o analíticamente,

$\left|\mathbf m\right|=\left|\left(\mathbf P\boldsymbol-\mathbf O\right)\boldsymbol\times\mathbf v\right|=\left|\left(\mathbf P\boldsymbol-\mathbf O\right)\right|\cdot\left|\boldsymbol v\right|\cdot\sin\left(\alpha\right)$

siendo $\alpha$ el ángulo formado por los vectores **v** y **OP**.

**Ejemplo 1**: en el caso de la palanca (figura 1) llamamos O al punto de apoyo, y los puntos P, R de aplicación de las fuerzas **P **y **R** estan situados a una distancia Bp y Br respectivamente, además, los vectores **OP** y **OR** son perpendiculares a las fuerzas **P **y **R **y todos estos vectores están en un mismo plano que llamamos XY (son coplanarios). En estas condiciones, si aplicamos la definición para calcular el moment total respecto a O:

$\begin{array}{l}\boldsymbol m(\boldsymbol P)=\boldsymbol O\boldsymbol P\times\boldsymbol P=\begin{vmatrix}\widehat i&amp;\widehat j&amp;\widehat k\\B_P&amp;0&amp;0\\0&amp;-P&amp;0\end{vmatrix}=-\widehat kPB_P;\\\boldsymbol m(R)=\boldsymbol O\boldsymbol R\times\boldsymbol R=\begin{vmatrix}\widehat i&amp;\widehat j&amp;\widehat k\\-B_R&amp;0&amp;0\\0&amp;-R&amp;0\end{vmatrix}=\widehat kRB_R\end{array}$

Luego la suma de momentos es $-\widehat k\left(RB_R-PB_P\right)$, un vector en la dirección del versor $\widehat k$, que "sale" de la pantalla. En la condición de equilibrio el momento debe de ser cero, para ello debe de cumplirse que $PB_P=RB_R$, expresión que coincide con la ley de la palanca.

![](/taller-matematicas/assets/images/separador2.png)
### Propiedades del vector momento

Una primera propiedad es que el vector momento es un pseudovector (o vector axial) debido a que se obtiene del producto vectorial de dos vectores polares (ver por ejemplo V[ectores en Física](http://tallermatematic.ovh/wp/index.php/2016/08/11/vectores/)).

Si el vector **v** lo desplazamos a lo largo de su recta soporte r hasta aplicarlo en otro punto P' (figura 2), geométricamente el nuevo triángulo formado por **OP**' - **v** tendrá la misma área que el **OP** - **v** , pues la base **v** es la misma y la altura h (obtenida trazando la perpendicular a la recta r pasando por O) de los dos triángulos es la misma. Además, el plano que contiene al vector **v** y a **OP** es el mismo que contiene a **v** y a **OP**' (es el plano definido por el punto O y la recta r), por tanto vemos que:
Propiedad 1: El momento m de un vector v respecto a un punto O no depende del punto de aplicación del vector, siempre que esté sobre la recta r que contiene al vector.
![](/taller-matematicas/assets/images/moments2.png) Fig. 4: el momento m de un vector v respecto un punto fijo O no depende del punto de aplicación P, P', etc

Por tanto los vectores en lo que respecta a su momento respecto a un punto fijo O se comportan como vectores deslizantes. En cambio si variamos del punto O al O', entonces si obtenemos un cambio en el vector momento **m**: podemos verlo planteando P - O' = (P - O) + (O - O') y sustituyendo en la expresión del momento **m**':

$\begin{array}{l}\boldsymbol m\boldsymbol'=\left(P-O'\right)\times\boldsymbol v=\left$\left(P-O\right)+\left(O-O'\right)\right$\times\boldsymbol v\Rightarrow\\\boldsymbol m\boldsymbol'=\left(P-O\right)\times\boldsymbol v+\left(O-O'\right)\times\boldsymbol v\Rightarrow\\\boxed{\mathbf m\boldsymbol'\boldsymbol=\mathbf m\boldsymbol+\left(\mathbf O\boldsymbol-\mathbf O\boldsymbol'\right)\boldsymbol\times\mathbf v}\;\lbrack2\rbrack\end{array}$

Viendo al producto $\left(\mathrm O-\mathrm O'\right)\boldsymbol\times\mathbf v$ como el momento de v estando aplicado en O con respecto a O' (comparar con la definición [1]), podemos expresarlo en palabras:
Propiedad 2: El momento de un vector aplicado en P respecto a un punto O' es igual al momento de ese vector aplicado en P respecto a otro punto O más el momento respecto a O' del vector aplicado en el punto O.
Otra propiedad del vector momento es el denominado teorema de Varignon:
Propiedad 3 (Varignon): El momento total respecto a un punto O cualquiera de un conjunto de vectores concurrentes en un punto P es igual al momento de la suma del conjunto de vectores respecto a ese punto O.
### **Cálculo vectorial con vectores deslizantes**

Las operaciones con vectores las realizamos usando un sistema de coordenadas y los componentes de los vectores respecto a ese sistema; así, el vector **PQ** con origen en el punto P y extremo en el punto Q, al restar las coordenadas Q - P obtenemos un vector v con origen en el origen de coordenadas, no en el punto P. Si deslizamos el vector **PQ** a lo largo de su recta soporte, pasando a estar en los puntos P', Q', el nuevo vector **P'Q'** tendrá las mismas coordenadas Q'-P' coincidentes con **v**. Dos vectores de la misma magnitud y direcciones paralelas se dice que son *equipolentes*; así pues, cuando trabajemos con las coordenadas de vectores deslizantes, realmente estaremos trabajando con las coordenadas de vectores equipolentes con origen en el origen de coordenadas, pero los  momentos que calculemos los supondremos aplicados en los puntos dados.

![](/taller-matematicas/assets/images/moments_equipolencia.png) Fig. 5: vector equipolente a un vector deslizante

**Ejemplo 1**: obtener el momento respecto al punto O(0,0) de los vectores v, w, ambos aplicados en el punto P(1,1), y con los extremos en Q(2,2) y R(2,3) respectivamente.

![](/taller-matematicas/assets/images/moments3.png) Fig. 6: momento de dos vectores concurrentes respecto a un punto O

Las coordenadas son en dos dimensiones, pero el momento, calculado según la definición [1] es un vector perpendicular al plano que contiene los vectores **v**, **w** y el punto O; "ampliamos" pues nuestra referencia con una tercera coordenada que "saldrá" del plano de la pantalla hacia nuestro rostro (regla de la mano derecha):

O(0, 0, 0), P(1, 1, 0), **OP** = P - O = (1, 1, 0);

El vector **PQ** = (2, 2, 0) - (1, 1, 0) = (1, 1, 0) es paralelo a **v** con el mismo módulo y origen en (0,0, 0) (**v** y **PQ** son *vectores equipolentes*), por tanto el producto $\boldsymbol OP\times\boldsymbol v$  es el mismo que el producto $\boldsymbol OP\timesPQ$, que calculamos usando determinantes:

$\boldsymbol OP\times \boldsymbol PQ=\begin{vmatrix}i&amp;j&amp;k\\1&amp;1&amp;0\\1&amp;1&amp;0\end{vmatrix}=\left(0,0,0\right)$

obviamente el momento es cero, pues **OP** y v estan sobre la misma recta; procedemos igual con **w**: tomamos en su lugar el vector **PR**  = R-P = (0, 1, 0) y obtenemos el producto vectorial $\boldsymbol OP \times \boldsymbol PR$:

$\boldsymbol OP\times \boldsymbol PR=\begin{vmatrix}i&amp;j&amp;k\\1&amp;1&amp;0\\0&amp;1&amp;0\end{vmatrix}=\left(0,0,-1\right)$

este vector momento "entra" verticalmente en la pantalla. El momento total de los dos vectores es la suma de sus momentos. Como v, w son concurrentes, también podemos llegar al mismo resultado aplicando la propiedad 3: sumamos los dos vectores y calculamos el momento de la suma: sustituimos v + w por los vectores que parten de O: (1, 1, 0) + (0, 1, 0) = (1, 2, 0), calculamos el momento:

$OP\times PQ=\begin{vmatrix}i&amp;j&amp;k\\1&amp;2&amp;0\\0&amp;1&amp;0\end{vmatrix}=\left(0,0,-1\right)$

![](/taller-matematicas/assets/images/separador2.png)
### Momento de un vector respecto a un eje

En los apartados que siguen, se estudian las propiedades de los momentos y de los sistemas de momentos respecto a rectas (ejes); los resultados nos serviran para reducir conjuntos de vectores a un conjunto mínimo equivalente a efectos del momento resultante. También nos interesará encontrar los puntos respecto a los cuales el momento resultante de un sistema de vectores resulta ser mínimo, la cual cosa permitirá resolver problemas de equilibrio.

![](/taller-matematicas/assets/images/moments4.png) Fig. 7: momentos de un vector v respecto a los puntos situados en un eje E

Imaginemos un eje E, esto es, una recta sobre la que hemos definido un vector unitario u para definir un sentido, y sobre el eje dos puntos distintos O, O'. Nos preguntamos por los momentos **m**, **m**' de un vector cualquiera v respecto a esos puntos. Recordemos la igualdad [2]:

$\mathbf m\boldsymbol'\boldsymbol=\mathbf m\boldsymbol+\left(\mathbf O\boldsymbol-\mathbf O\boldsymbol'\right)\boldsymbol\times\mathbf v$

Multiplicando escalarmente los dos lados de esta igualdad por el vector unitario **u**:

$\mathbf m\boldsymbol'\boldsymbol\cdot\boldsymbol u\boldsymbol=\mathbf m\boldsymbol\cdot\mathbf u\boldsymbol+\left(\mathbf O\boldsymbol-\mathbf O\boldsymbol'\right)\boldsymbol\times\mathbf v\boldsymbol\cdot\mathbf u$

El vector $\left(\mathbf O\boldsymbol-\mathbf O\boldsymbol'\right)\boldsymbol\times\mathbf v$ es perpendicular al plano que contiene a **u** y **v**, por tanto el producto escalar es cero, nos queda pues

$\mathbf m\boldsymbol'\boldsymbol\cdot\boldsymbol u\boldsymbol=\mathbf m\boldsymbol\cdot\mathbf u$

Recordando la interpretación geométrica del producto escalar, tenemos que la proyección sobre el eje E del momento del vector **v** respecto a cualquier punto del eje E es constante; a este valor, que es un escalar, se le llama momento del vector **v** respecto al eje E.

En particular, el momento de un vector respecto a un eje paralelo al vector será nulo, pues el vector y el eje serán coplanarios, y el momento será perpendicular a ese plano, luego el producto escalar del vector u con el momento será cero, siendo perpendiculares.

Entonces para un vector v cualquiera, podemos descomponerlo en suma de dos vectores, uno paralelo al eje E y otro perpendicular; el primero tendrá momento respecto al eje nulo, por tanto vemos que:
Propiedad 4: el momento respecto al eje E de un vector v será igual al momento respecto al eje E del vector proyección ortogonal de v respecto a un plano perpendicular a E.
**Ejemplo 2**: obtener el momento respecto a los ejes Y, Z del vector w, aplicado en el punto P(1,1), y con extremo en R(2,3).

El vector u para el eje Y es u(0, 1, 0), y para calcular el momento de w respecto al eje Y nos vale cualquier punto O sobre el eje, por ejemplo, el (0, 0, 0) que ya hemos obtenido en el ejemplo 1, siendo m = (0, 0, -1); el producto escalar es m·u = (0, 0, -1)·(0, 1, 0) = 0, resultado esperado, pues el momento m es perpendicular al plano que contiene el eje Y. Para el momento respecto del eje Z tomamos u(0, 0, 1), entonces m·u = (0, 0, -1)·(0, 0, 1) = -1.

![](/taller-matematicas/assets/images/separador2.png)
### Momento resultante de un sistema de fuerzas

Si tenemos un conjunto de vectores $v_1,v_2,...,v_n$ podemos calcular sus momentos $m_1,m_2,..._m_n$ respecto a un único punto fijo O; si consideramos otro punto O', aplicando [2] a cada vector y sumando:

$\begin{array}{l}m'_i=m_i+\left(O-O'\right)\times v_i\Rightarrow\\\sum_{}m'_i=\sum_{}m_i+\left(O-O'\right)\times\sum_{}v_i\end{array}$

Llamando **M** y **M**' al momento suma, y **R** al vector suma (llamado *resultante del sistema de vectores*), nos queda:

$\boldsymbol M'=\boldsymbol M+\left(O-O'\right)\times\sum_{}{\boldsymbol v}_i=\boldsymbol M+\left(O-O'\right)\times\boldsymbol R$ [3]
Propiedad 5: El momento resultante respecto a O' es la suma del momento resultante respecto a O y el momento respecto a O' del vector  resultante del sistema aplicado en O.
En el caso especial de que la resultante sea nula, R = 0, vemos que debe de ser M = M': *para sistemas de vectores con resultante nula el momento del sistema es independiente del punto que se tome. Un sistema de vectores con resultante nula pero con momento total distinto de cero se llama un par vectorial*. En el caso particular de vectores fuerza, será un *par de fuerzas*.

Otro caso especial es cuando el vector OO' es paralelo a la resultante R, pues entonces el producto vectorial de [3] es cero, y el  momento respecto a O es igual al momento respecto a O':
Propiedad 6: El momento resultante de un sistema de vectores es el mismo para cualquier punto situado en una recta paralela a la resultante del sistema.
**Trinomio invariante**

Si multiplicamos la expresión [3] por la resultante R (producto escalar) obtenemos:

$\boldsymbol M'\cdot\boldsymbol R=\boldsymbol M\boldsymbol\cdot\boldsymbol R+\cancel{\left(\mathbf O\boldsymbol-\mathbf O\boldsymbol'\right)\boldsymbol\times\mathbf R\boldsymbol\cdot\mathbf R}=\boldsymbol M\boldsymbol\cdot\boldsymbol R$

luego *el producto escalar del momento resultante por la resultante $\boldsymbolM\cdot\boldsymbolR$ es invariante*, no depende del punto escogido para el cálculo de los momentos. Cuando se expresa en función de las componentes x, y, z en la forma $T=M_xR_x+M_yR_y+M_zR_z$ se llama *trinomio invariante*. Para un sistema de un sólo vector T siempre vale cero, pues el vector es perpendicular a su momento.
### **Eje central de momentos**

**Momento mínimo**

El que la expresión $\boldsymbol M'\cdot\boldsymbol R=\boldsymbol M\boldsymbol\cdot\boldsymbol R=\left|M\right|\cdot\left|R\right|\cdot\cos\left(\overset{\boldsymbol\hat{}}{\mathbf M\mathbf R}\right)$ sea invariante para cualquier punto de cálculo del momento, implica que si en un cierto punto O el momento resultante es paralelo a la resultante R, entonces para ese punto $\cos\left(\overset{\boldsymbol\hat{}}{\mathbf M\mathbf R}\right)=1$, y comparando con otro punto O' con momento no paralelo a R, será $\left|M'\right|\cdot\left|R\right|\cdot cos\left(\widehat{\mathrm{MR}}\right)=\left|M\right|\cdot\left|R\right|$,  como $cos\left(\widehat{\mathrm{MR}}\right)$ es en módulo menor que uno (estamos suponiendo que R y M no estan en la misma dirección) , se deduce que $\left|M'\right|\cdot\left|R\right|&gt;\left|M\right|\cdot\left|R\right|$para M paralelo a R, que significa que *el momento resultante M respecto a puntos O en los cuales M es paralelo a la resultante R es el momento mínimo posible*.

**Lugar geométrico de puntos que generan el mínimo momento**

La pregunta siguiente que nos hacemos es: ¿cuáles son esos puntos en los cuales el momento resultante M del sistema es paralelo a la resultante R, y por tanto el momento M es el mínimo posible?

Fijémonos en que si existieran dos puntos O, O' con esa propiedad, tendríamos que sus momentos M, M' son iguales, y por [3], que

$\boldsymbol M'=\boldsymbol M+\left(O-O'\right)\times\boldsymbol R=\boldsymbol M\Rightarrow\left(O-O'\right)\times\boldsymbol R=0$

por tanto **OO'** sería un vector paralelo a la resultante R; esto valdría para cualquier punto que proporcionara un momento paralelo a R:
El lugar geométrico de los puntos respecto a los cuales los momentos de un sistema de vectores C son paralelos a la resultante R, es una recta también paralela a R, denominada *eje central de momentos del sistema*.
**Caracterización del eje central de momentos**

Encontremos ahora las condiciones que ha de cumplir un punto O' del eje central.  Sea O el origen de coordenadas, y O' el punto de intersección de la perpendicular al eje central que pasa por O (figura 8).

![](/taller-matematicas/assets/images/moments5.png) Fig. 8: situación para la deducción de las ecuaciones del eje central

El  momento M' serà paralelo a la resultante R y al eje central; si aplicamos [3], multiplicando vectorialmente toda la expresión por la izquierda por la resultante R obtenemos:

$\boldsymbol R\times\boldsymbol M'=\boldsymbol R\times\boldsymbol M+R\times\left(O-O'\right)\times\boldsymbol R$

Como R y M' son paralelos, el producto del primer miembro es nulo. Para el doble producto vectorial aplicamos la propiedad **A** x (**B** x **C**) = **B** · (**A**·**C**) - **C** · (**A**·**B**), y resulta:

$\begin{array}{l}\mathbf0=\boldsymbol R\times\boldsymbol M+\left(O-O'\right)\cdot\left(\mathbf R\boldsymbol\cdot\mathbf R\right)-\boldsymbol R\boldsymbol\cdot\left(\cancel{\left(\mathbf O\boldsymbol-\mathbf O\boldsymbol'\right)\boldsymbol\cdot\mathbf R}\right)\Rightarrow\\0=\boldsymbol R\times\boldsymbol M+\left(O-O'\right)\cdot R^2\Leftrightarrow\\\left(O'-O\right)=\boldsymbol O\boldsymbol O\boldsymbol'=\frac1{R^2}\boldsymbol R\times\boldsymbol M\end{array}$ [4]

El producto escalar (O-O')·**R** es nulo porque OO' es perpendicular a **R**. La expresión [4] es el vector de posición de un punto O' del eje central, en función de la resultante **R** y del momento respecto al orígen de coordenadas **M**.  Ele eje central es la recta paralela a R que pasa por el punto O', quedando así totalmente determinada.

**Ejemplo 3**: dado el sistema de  vectores deslizantes v(1, 2, 3) aplicado en P(1, 1, 1) y w(0, 1, -1) aplicado en Q(0, 0, 1),  obtener la ecuación de su eje central de momentos, así como el momento mínimo del sistema.

Utilizamos vectores los equipolentes  **v**' = v - P = (0, 1, 2) y **w**' = w - Q = (0, 1, -2), obtenemos la resultante **R** = **v**' + **w**' = (0, 2, 0) y seguidamente el momento resultante respecto al origen de coordenadas:

**M**(v') = (P - O) x **v**' = [(1, 1, 1) - (0, 0, 0)] x (0, 1, 2) = (1, 1, 1) x (0, 1, 2) = (1, -2, 1);

**M**(w') = (Q - O) x **v**' = [(0, 0, 1) - (0, 0, 0)] x (0, 1, -2) = (0, 0, 1) x (0, 1, -2) = (-1, 0, 0);

**M** = **M**(v') + **M**(w') = (0, -2, 1), el módulo de M es √5.

Calculamos ahora el punto O' del eje central:

R = |(0, 2, 0)| = 2; **R** x **M** = (0, 2, 0) x (0, -2, 1) = (2, 0, 0), por tanto las coordenadas de O' son (1, 0, 0); el eje central pasa por O' y es paralelo a **R**(0, 2, 0), sus ecuaciones paramétricas son (x, y, z) = (1, 0, 0) + t·(0, 2, 0) -> x = 1, y = t, z = 0. El momento del sistema respecto del eje central, **M**',  puede obtenerse usando el valor del trinomio invariante y el hecho de que es paralelo a R:

condición trinomio invariante: M'·R = M·R = (0, -2, 1)·(0, 2, 0)= -4

es paralelo a R: M' = t·(0, 2, 0)

Luego M'·R = t·(0, 2, 0)·(0, 2, 0) = 4t, igualando al trinomio invariante, 4t = -4 -> t = -1, el momento M' es (0, -2, 0). Observemos que el módulo de M' es 2, que es menor que el módulo de M, como esperábamos, ya que M' es el momento mínimo.

![](/taller-matematicas/assets/images/separador2.png)
### Reducción de sistemas de vectores deslizantes

**Sistemas de vectores equivalentes**

Consideramos que dos sistemas de vectores deslizantes son equivalentes si ambos tiene la misma resultante R y el mismo momento resultante M respecto a un punto fijo O. De hecho, aplicando la identidad [3], el momento resultante será también idéntico para cualquier punto del espacio; en efecto, llamando $M_1, R_1, M_2,R_2$ a los momentos y resultantes del sistema 1 y 2, se cumple:

$\begin{array}{l}M_1'=M_1+\left(O-O'\right)\times R_1,\\M_2'=M_2+\left(O-O'\right)\times R_{1;}\\M_1=M_2=M,\;R_1=R_2=R\Rightarrow\\M_1'=M_{}+\left(O-O'\right)\times R_{}=M_2'\end{array}$

**Operaciones para obtener un sistema equivalente**

Las siguientes transformaciones, aplicadas a un sistema de vectores deslizantes, proporcionan otro sistema equivalente:

 	- Decomposición de un vector en varios concurrentes

 	- Composición de vectores concurrentes en uno solo

 	- Sumar o restar dos vectores situados en una misma línea

Respecto a la obtención de un sistema equivalente que sea más simple, tenemos el siguiente teorema:
**Teorema**: todo sistema de vectores deslizantes puede reducirse a otro que contenga como máximo sólo dos vectores.
Veamos como: si R es la resultante y M el momento resultante respecto a O, un sistema equivalente será el constituido por un vector equipolente a R que pase por O (por tanto de momento nulo) más un par (dos vectores opuestos v, w con resultante nula, uno de ellos, digamos el v, pasando por O) cuyo momento sea M; si sumamos el vector v con R, obtenemos un sistema de sólo dos vectores, (v+R) y w, equivalente al sistema inicial.

 **Ejemplo 4**:  Sea el sistema de vectores  deslizantes a(1,2,3), b(-1,0,1), c(0, 2, 0), con puntos de aplicación p(0,0,0), q(0, 1,0) y r(0,0,1) respectivamente, y sea el punto O(-1, 2, 1). Encontrar un sistema equivalente de sólo dos vectores.

Primero hallamos las coordenadas de los vectores equipolentes aplicados en el origen:

a' = (1,2,3) - (0,0,0) = (1,2,3); b' = (-1,0,1) - (0, 1,0) = (-1,-1,1); c' = (0, 2, 0) - (0,0,1) = (0, 2, 0).

La resultante será la suma R = a' + b' + c' = (0, 3, 4); el momento resultante respecto a O lo calculamos para cada vector según la definición. recordando de utilizar los vectores equipolentes a', b', c' para los vectores (P-O) y los vectores originales a, b, c para el producto vectorial:

$\begin{array}{l}M_a=\left$(0,0,0)-\left(-1,2,1\right)\right$\times\left(1,2,3\right)=\left(-4,-4,4\right);\\M_b=\left$(0,1,0)-\left(-1,2,1\right)\right$\times\left(-1,-1,1\right)=\left(-2,0,-2\right);\\M_c=\left$(0,0,1)-\left(-1,2,1\right)\right$\times\left(0,2,0\right)=\left(0,0,2\right);\\M=M_a+M_b+M_c=\left(-6,-4,4\right).\end{array}$

Un sistema equivalente a {a, b, c} aplicados a los puntos p, q, r respecto al punto O será el formado por el vector R aplicado en O más un par de vectores v, w con momento M, estando v aplicado en O.

Como la resultante del par (v,w) ha de ser nula, los vectores equipolentes v', w' situados en el origen de coordenadas han de cumplir v' + w' = 0. Llamando x, y, z a las componentes de v:

$v'=\left(x,y,z\right)-\left(-1,2,1\right)=\left(x-1,y-2,z-1\right)\Rightarrow w'=\left(1-x,2-y,1-z\right)$

Como el momento de v respecto a O es nulo, ha de ser que el momento de w respecto a O sea igual a M. Lo planteamos así:

$M=\left(-6,-4,4\right)=(S-O)\times w'\left(0,0,1\right)$

Detallando las coordenadas, y llamando al punto S(s,t,u):

$\begin{array}{l}\begin{array}{l}M=\left(-6,-4,4\right)=(s+1,t-2,u-1)\times\left(1-x,2-y,1-z\right)\Rightarrow\\\begin{vmatrix}i&amp;j&amp;k\\s+1&amp;t-2&amp;u-1\\1-x&amp;2-y&amp;1-z\end{vmatrix}=\left(-6,-4,4\right)\end{array}\\\end{array}$

Resulta un sistema  de ecuaciones:

$\left.\begin{array}{r}\left(t-2\right)\left(1-z\right)-\left(u-1\right)\left(2-y\right)=-6\\-\left(s+1\right)\left(1-z\right)+\left(u-1\right)\left(1-x\right)=-4\\\left(s+1\right)\left(2-y\right)-\left(t-2\right)\left(1-x\right)=4\end{array}\right\}$

Tenemos 6 incógnitas, las coordenadas del punto S y las del vector w, y sólo tres ecuaciones; esto significa que tenemos tres grados de libertad al escoger el par, aunque no todas las combinaciones son posibles, pues algunas de ellas pueden conducirnos a sistemas incompatibles. Una posible elección es la que sigue (se definen  algunos parámetros y de ellos se deducen los otros):

$\begin{array}{l}t=2;\;s=2;\Rightarrow y=\frac23,\;u=\frac{11}2;\\\;x=z\Rightarrow x=-\frac{11}6=z\\\\\end{array}$

Los vectores del par resultan:

$v'=\left(-\frac{11}6,\frac23,-\frac{11}6\right),\;w'=\left(1+\frac{11}6,2-\frac23,1+\frac{11}6\right)=\left(\frac{17}6,\frac43,\frac{17}6\right)$

y estan aplicados en los puntos O(-1, 2, 1) y S(2,2,11/2). Junto con el vector R'= (0, 3, 4) aplicado también en O, constituyen un sistema equivalente al inicial. Sumamos ahora R' y v' (ámbos aplicados al mismo punto O) para obtener R''= (0, 3, 4) + (-11/6, 2/3, -11/6) = (-11/6, 11/6, -11/6) = (11/6)·(-1, 1, -1), vector aplicado en O. Hemos reducido el sistema original a sólo dos vectores:

 	- $R''=\frac{11}6\left(-1,1,-1\right)$ aplicado en O(-1, 2, 1)

 	- vector equipolente $w'=\left(\frac{17}6,\frac43,\frac{17}6\right)$ aplicado en S(2,2,11/2)

![](/taller-matematicas/assets/images/separador2.png)
{% endraw %}