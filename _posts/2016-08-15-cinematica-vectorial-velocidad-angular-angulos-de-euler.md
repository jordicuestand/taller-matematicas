---
layout: post
title: "Cinemática vectorial: velocidad angular, ángulos de Euler"
date: 2016-08-15 20:26:08 +0000
categories:
  - "Cinemática"
  - "Fí­sica"
  - "Vectores"
tags:
  - "bases móviles"
  - "referencia no inercial"
  - "rotación"
  - "Velocidad angular"
math: true
---
{% raw %}

### Velocidad angular y rotaciones en el espacio

En el artículo [Vectores en Física ](http://tallermatematic.ovh/wp/index.php/2016/08/11/vectores/)explicamos que la velocidad angular es un tipo especial de vector: un vector axial, o pseudovector, y decíamos que estos vectores se diferencian de los vectores "normales" o polares en que se comportan de forma distinta bajo un transformaciones lineales del tipo "reflexión respecto un plano". En el caso de la velocidad angular además podemos decir que, pese a ser una velocidad, no se obtiene derivando un vector respecto al tiempo.

Esto ocurre por que no podemos definir una base para los "vectores rotación", tal como hacemos para los vectores posición, para después descomponer cualquier rotación dada en sus componentes,  derivarlos y obtener velocidades de rotación, y no podemos porque las rotaciones son transformaciones lineales, que además no conmutan entre sí. Esto quiere decir que el orden en que se aplican las rotaciones influye en el resultado.

En el espacio euclídeo, podemos escoger cualesquiera tres direcciones ortogonales, definir sobre cada una un vector unitario, y descomponer, de forma única, cualquier vector v según una combinación lineal de los vectores unitarios:

$\overrightarrow v=v_1\overrightarrow{e_1}+v_2\overrightarrow{e_2}+v_3\overrightarrow{e_3}$

Para hacer lo mismo con las rotaciones, necesitamos una base de rotaciones; podemos pensar que una posibilidad seria escoger rotaciones alrededor de cada eje cartesiano:


Las matrices de cada una de estas rotaciones son, llamando respectivamente $R_x, R_y, R_z$ a las efectuadas sobre los ejes X, Y, Z:

$R_x=\begin{bmatrix}1&amp;0&amp;\\0&amp;\cos\left(\alpha\right)&amp;-\sin\left(\alpha\right)\\0&amp;\sin\left(\alpha\right)&amp;\cos\left(\alpha\right)\end{bmatrix},\;R_y=\begin{bmatrix}cos\left(\alpha\right)&amp;0&amp;sin\left(\alpha\right)\\0&amp;1&amp;0\\-sin\left(\alpha\right)&amp;0&amp;cos\left(\alpha\right)\end{bmatrix},\;R_z=\begin{bmatrix}cos\left(\alpha\right)&amp;-sin\left(\alpha\right)&amp;0\\sin\left(\alpha\right)&amp;1&amp;0\\0&amp;cos\left(\alpha\right)&amp;1\end{bmatrix}$

Esta matrices no son simétricas, y por lo tanto no conmutan entre si; cualquier combinación lineal que hagamos con ellas dará un resultado distinto dependiendo del orden en el que escribamos las matrices, no es que cambien los coeficientes como cuando cambiamos de base, es que la rotación resultante no es la misma:

$\alpha R_1+\beta R_2+\gamma R_3\neq\beta R_2+\gamma R_3+\alpha R_1\neq\gamma R_3+\alpha R_1+\beta R_2$

Siendo toda el Álgebra vectorial que conocemos una [Álgebra conmutativa](https://es.wikipedia.org/wiki/%C3%81lgebra_conmutativa), las rotaciones definidas de este modo no la siguen, y nos obligaría a usar álgebras no conmutativas, demasiadas complicaciones.

Es fácil ver que las rotaciones no conmutan sin necesidad de álgebra; la figura 2 muestra como afectan a una ficha de dominó dos rotaciones, en dos columnas.  En la primera fila vemos la ficha en la posición inicial; en la columna de la izquierda,  segunda fila,  se rota la ficha  un ángulo recto en torno a un eje perpendicular a la pantalla en el sentido inverso  de las agujas del reloj, en la segunda fila se vuelve a rotar la ficha en torno al eje Y vertical, en el sentido del reloj, la posición final muestra el lateral de la ficha.


En la columna de la izquierda, realizamos las dos mismas rotaciones, pero esta vez cambiando el orden. Comparando las posiciones finales, vemos que son distintas.

### Ángulos de Euler

Una forma de descomponer cualquier rotación en el espacio según tres rotaciones elementales, de forma que la suma de las tres determine unívocamente la rotación original, es usar los denominados ángulos de Euler; nosotros aquí los utilizaremos en el contexto de dar la orientación de una base móvil Ref2 respecto a una fija Ref1. Se trata de dar la orientación de una base móvil Ref2 cualquiera en base a tres ángulos, que corresponden a tres rotaciones:

 	- 1a rotación: respecto a un eje fijo cualquiera, aquí tomamos el eje rotulado como X, puede ser cualquier otro. Respecto a este eje X, efectuar una rotación de la base XYZ con un ángulo $\alpha$, resulta la base X'Y'Z':


 	- 2a rotación: respecto a uno de los nuevos ejes desplazados en la 1a rotación, en nuestro ejemplo, el Y' o el Z'; por ejemplo, escogemos el eje Y' para efectuar una rotación de la base con un ángulo $\beta$, resulta la nueva base X''Y''Z'':


 	- 3a rotación: sobre el eje que ha estado afectado sólo por la 2a rotación, en nuestro caso, el eje X'; sobre él, giramos la base un ángulo $\gamma$ para obtener la base X'''Y'''Z''':


Otra forma de resumirlo es: los ejes de la base girada cumplen

 	- un eje está afectado por las rotaciones 1a y 3a, en el ejemplo, es el Y

 	- un segundo eje está afectado sólo por la rotación 2a, es el X

 	- el eje restante está afectado por todas las rotaciones, es el Z.

Tal como los hemos descrito, estas rotaciones tienen la siguiente propiedad, que no demostramos:
**Propiedad 1**: Dada una base móvil con una velocidad angular arbitraria $\overrightarrow\Omega$, siempre podrá expresarse esta velocidad como suma de las derivadas temporales de los tres ángulos de Euler:

$\overrightarrow\Omega=\overset\rightharpoonup\alpha'+\overset\rightharpoonup\beta'+\overset\rightharpoonup\gamma'$

Los pseudovectores $\overset\rightharpoonup\alpha,\;\overset\rightharpoonup\beta,\;\overset\rightharpoonup\gamma$ se definen como es habitual: si giramos en el sentido de las agujas del reloj en sobre un eje, el vector giro estará sobre el eje en sentido positivo, si el sentido de giro es el contrario, estará en sentido negativo. Teniendo esto en cuenta, y observando la figura 5, en la que vemos en rojo las posiciones que ocupan los vectores de rotación de Euler, podemos deducir las componentes del vector $\overrightarrow\Omega$ en la base X'''Y'''Z''':

${\left\{\overset\rightharpoonup\alpha'+\overset\rightharpoonup\beta'+\overset\rightharpoonup\gamma'\right\}}_{X'''Y'''Z'''}=\begin{bmatrix}\gamma'+\alpha'\cos\left(\beta\right)\\\alpha'\sin\left(\beta\right)\sin\left(\gamma\right)+\beta'\cos\left(\gamma\right)\\\alpha'\sin\left(\beta\right)\cos\left(\gamma\right)-\beta'\sin\left(\gamma\right)\end{bmatrix}$.

Este seria el caso más general de composición de tres rotaciones de Euler; a menudo, en las aplicaciones prácticas, sólo necesitaremos uno o dos giros para representar la velocidad angular. Dependerá de la geometría de cada problema cuáles ejes y rotaciones serán los más adecuados.

En general es complicado manejar velocidades y aceleraciones angulares en referencias móviles; no obstante, hay casos especiales que pueden simplificar el problema. Uno a considerar se presenta en la figura 5:


Supongamos que tenemos una referencia móvil Ref2 de la cual tenemos su vector velocidad angular $\Omega$ respecto la referencia fija Ref1 (en la figura es el vector en rojo, representado verticalmente, pero puede tener cualquier dirección), y hay un objeto que está girando con velocidad angular *w* respecto Ref2 en torno a un eje fijo en Ref2; entonces, la velocidad angular del objeto respecto la referencia fija Ref1 es simplemente $\left.\overrightarrow\Omega\right|+\overrightarrow w$ [1] : podemos sumar las velocidades angulares sin recurrir a ángulos de Euler.

**Ejemplo 1**: En este ejemplo, basado en los apuntes de la asignatura de Mecánica de los estudios de Ingenieria Industrial debidos al profesor Joaquim Agulló (ETSEIB - cpda, 1980), estudiamos la cinemática de un punto en una base móvil usando los ángulos de Euler. En la figura 6 vemos un volante que gira en torno al eje aa', el cual está sujeto a una plataforma mediante una articulación de tal forma que el eje aa' puede oscilar en torno al eje bb'. La propia plataforma puede oscilar respecto a un tercer eje cc'. Se pide: a) expresar la velocidad angular del volante en una base móvil adecuada usando ángulos de Euler, b) dar los componentes de la velocidad de un punto P de la periferia del volante en la base móvil del punto anterior.


Primero hay que decidir, atendiendo a la geometría del problema, los ejes fijos y móviles que usaremos; en este caso, parece bastante evidente que los propios ejes aa', bb' y cc' son los más adecuados para describir el movimiento del volante respecto a una referencia fija. De hecho, tomando los ejes moviles aa',  bb' y el tercer eje simplemente el perpendicular al plano bb'-cc', sólo necesitaremos dos ángulos de Euler para describir la rotación de la base móvil pues el eje aa' será directamente el tercer eje. En este caso, podemos ya describir los ángulos de Euler $\alpha, \beta$ de la base XYZ móvil, y los ejes fijos XYZ:


El origen O de las referencias fija y móvil es el mismo: el centro de la plataforma. Encontremos ahora los componentes de las velocidades de las rotaciones de Euler (vectores en rojo en la figura 7) respecto los ejes girados X''Y''Z'', proyectándolos según los ángulos $\alpha, \beta$, esto equivale a decir, encontrar la velocidad angular de la referencia móvil X''Y''Z'', expresada en su propia base, que es, llamando Ref2 a la referencia de ejes X''Y''Z'', y origen O:

${\left\{{\left.{\overrightarrow\Omega}_{Ref2}\right|}_{Ref1}\right\}}_{Ref2}=\begin{bmatrix}\alpha'\cos\left(\beta\right)\\\beta'\\-\alpha'\sin\left(\beta\right)\end{bmatrix}$, [2]

que se interpreta así: velocidad angular de la Ref2, $\overrightarrow\Omega}_{Ref2}$, relativa a la referencia fija Ref1, ${\left.{\overrightarrow\Omega}_{Ref2}\right|}_{Ref1}$, con componentes expresados en la base móvil Ref2, ${\left\{{\left.{\overrightarrow\Omega}_{Ref2}\right|}_{Ref1}\right\}}_{Ref2}$.

Expresemos ahora la velocidad angular del volante respecto Ref1 en la base de Ref2, suponiendo que el volante gira con velocidad angular $\gamma'$ en el sentido contrario a las agujas del reloj respecto del eje aa'. Visto desde la referencia 2 el volante sólo gira en torno al eje fijo (en la Ref2) aa', así pues,

${\left\{{\left.{\overrightarrow\Omega}_V\right|}_{Ref2}\right\}}_{Ref2}=\begin{bmatrix}0\\0\\\gamma'\end{bmatrix}$,

que se interpreta: velocidad angular del volante V, relativa a la referencia móvil Ref2, expresada en a base móvil de la Ref2. Para convertir esta velocidad a la relativa a la referencia fija Ref1 observamos que el volante gira en torno a un eje fijo, el Z'', en la Ref2 con velocidad angular que, expresada en la base de la Ref2, es ${\left\{{\left.\overrightarrow\omega\right|}_{Ref2}\right\}}_{Ref2}=\left(0,0,\gamma'\right)$, y a su vez la Ref2 gira con velocidad angular [2] respecto a la Ref1; aplicando [1], encontramos que:

$\begin{array}{l}{\left\{{\left.\overrightarrow\omega\right|}_{Ref1}\right\}}_{Ref2}={\left\{{\left.{\overrightarrow\Omega}_{Ref2}\right|}_{Ref1}\right\}}_{Ref2}+{\left\{{\left.\overrightarrow\omega\right|}_{Ref2}\right\}}_{Ref2}=\\\begin{bmatrix}\alpha'cos\left(\beta\right)\\\beta'\\-\alpha'sin\left(\beta\right)\end{bmatrix}+\begin{bmatrix}0\\0\\\gamma'\end{bmatrix}=\begin{bmatrix}\alpha'cos\left(\beta\right)\\\beta'\\-\alpha'sin\left(\beta\right)+\gamma'\end{bmatrix}\end{array}$ [3].

Para encontrar la velocidad respecto de la referencia fija Ref1 de un punto P cualquiera de la periferia del disco derivaremos el vector OP, expresado en la base móvil Ref2; para ello usaremos la formula de derivación de vectores expresados en bases móviles respecto de una referencia fija (ver [Cinemática vectorial: sistemas de referencia, vectores posición, velocidad y aceleración](http://tallermatematic.ovh/wp/index.php/2016/08/12/cinematica-vectorial/), ecuación [4]):

$\boxed{{\left\{{\left.\frac{\operatorname d\overset\rightharpoonup u}{\operatorname dt}\right|}_{Ref}\right\}}_{base}={\left\{\frac{\operatorname d\overset\rightharpoonup u}{\operatorname dt}\right\}}_{base}+{\left\{\overset\rightharpoonup\omega{\textstyle\times}{\textstyle\overset\rightharpoonup u}\right\}}_{base}}$ [4],

que para el vector de posición OP será:

${\left\{{\left.\frac{\operatorname d\overrightarrow{OP}}{\operatorname dt}\right|}_{Ref1}\right\}}_{Ref2}={\left\{\frac{\operatorname d\overrightarrow{OP}}{\operatorname dt}\right\}}_{Ref2}+{\left\{\Omega\times\overrightarrow{OP}\right\}}_{Ref2}$ [5]

Las componentes de OP en la base Ref2 serán, considerando el centro O' del disco de radio r, y tomando el ángulo $\gamma$ de giro alrededor del eje Z'', como muestra la figura 9,

$\overrightarrow{OP}=\overrightarrow{OO'}+\overrightarrow{O'P}=\begin{bmatrix}0\\0\\L\end{bmatrix}+\begin{bmatrix}r\cos\left(\gamma\right)\\r\sin\left(\gamma\right)\\0\end{bmatrix}=\begin{bmatrix}rcos\left(\gamma\right)\\rsin\left(\gamma\right)\\L\end{bmatrix}.$ [6]


Aplicamos [5] usando [6] y [2]:

$\begin{array}{l}{\left\{{\left.\frac{\operatorname d\overrightarrow{OP}}{\operatorname dt}\right|}_{Ref1}\right\}}_{Ref2}=\frac d{dt}\begin{bmatrix}rcos\left(\gamma\right)\\rsin\left(\gamma\right)\\L\end{bmatrix}+\begin{bmatrix}\alpha'cos\left(\beta\right)\\\beta'\\-\alpha'sin\left(\beta\right)\end{bmatrix}\times\begin{bmatrix}rcos\left(\gamma\right)\\rsin\left(\gamma\right)\\L\end{bmatrix}=\\\begin{bmatrix}-r\gamma'\sin\left(\gamma\right)\\r\gamma'cos\left(\gamma\right)\\0\end{bmatrix}+\begin{vmatrix}i&amp;j&amp;k\\\alpha'cos\left(\beta\right)&amp;\beta'&amp;-\alpha'sin\left(\beta\right)\\rcos\left(\gamma\right)&amp;rsin\left(\gamma\right)&amp;L\end{vmatrix}=\\\begin{bmatrix}-r\gamma'sin\left(\gamma\right)\\r\gamma'cos\left(\gamma\right)\\0\end{bmatrix}+\begin{bmatrix}\beta'L+\alpha'rsin\left(\beta\right)sin\left(\gamma\right)\\-L\alpha'cos\left(\beta\right)-\alpha'rsin\left(\beta\right)cos\left(\gamma\right)\\\alpha'rcos\left(\beta\right)sin\left(\gamma\right)-\beta'rcos\left(\gamma\right)\end{bmatrix}=\\\begin{bmatrix}\beta'L+\alpha'rsin\left(\beta\right)sin\left(\gamma\right)-r\gamma'sin\left(\gamma\right)\\-L\alpha'cos\left(\beta\right)-\alpha'rsin\left(\beta\right)cos\left(\gamma\right)+r\gamma'cos\left(\gamma\right)\\\alpha'rcos\left(\beta\right)sin\left(\gamma\right)-\beta'rcos\left(\gamma\right)\end{bmatrix}.\\\end{array}$
{% endraw %}