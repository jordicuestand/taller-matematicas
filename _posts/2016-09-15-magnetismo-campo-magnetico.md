---
layout: post
title: "Magnetismo: campo magnético"
date: 2016-09-15 09:56:01 +0000
categories:
  - "Electricidad y Magnetismo"
  - "Fí­sica"
tags:
  - "Campo magnético"
  - "magnetismo"
  - "producto vectorial"
  - "Relatividad especial"
math: true
---
{% raw %}

## Magnetismo

$caption id="attachment_1625" align="alignleft" width="199"$![ Magnetita (By Rob Lavinsky, iRocks.com – CC-BY-SA-3.0, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=10139390)](/taller-matematicas/assets/images/470px-Magnetite-118736-294x300.jpg) Magnetita (By Rob Lavinsky, iRocks.com – CC-BY-SA-3.0, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=10139390)
Se conoce la piedra imán,la [magnetita](https://es.wikipedia.org/wiki/Magnetita), desde la antigüedad, y se aprovechó para [las primeras brújulas](https://es.wikipedia.org/wiki/Br%C3%BAjula#Historia_de_la_br.C3.BAjula) usadas en navegación. Gilbert (1600) establece que los imanes tienen [polos magnéticos](https://es.wikipedia.org/wiki/Im%C3%A1n#Polos_magn.C3.A9ticos),  y postula que el planeta Tierra es un enorme imán que actúa sobre la magnetita, orientándola según el eje de la Tierra Norte-Sur. Cavendish y Coulomb inician la experimentación y descripción matemática del magnetismo, y descubren que la fuerza magnética $F_m$ tiene una expresión similar a la electrostática $F_e$, sustituyendo las cargas eléctricas por "masas magnéticas":

$F_e=K\frac{q_1q_2}{d^2},\;F_m=\frac{m_1m_2}{d^2}$

Viendo las dos leyes, parecía haber una relación entre electricidad y magnetismo no intuida hasta entonces; [Oersted](https://es.wikipedia.org/wiki/Hans_Christian_%C3%98rsted) descubrió que una aguja imantada cerca de una corriente eléctrica recibía una fuerza, igual que si se ponía cerca de un imán.

[Ampère](https://es.wikipedia.org/wiki/Andr%C3%A9-Marie_Amp%C3%A8re) impulsa el nuevo campo de conocimiento deduciendo que el magnetismo se relaciona con las cargas eléctricas en movimiento, poniendo las bases de la [Electrodinámica](https://es.wikipedia.org/wiki/Electrodin%C3%A1mica); deduce también que si una corriente se comporta como un imán, entonces dos corrientes próximas se ejercerán efectos magnéticos como si fueran dos imanes, y propone, correctamente, que quizás los imanes permanentes tienen corrientes eléctricas en su interior, que son las que provocan su magnetismo, y que las "masas magnéticas" de Coulomb no existen, sólo existen las cargas eléctricas y sus efectos. Inventa el [solenoide,](https://es.wikipedia.org/wiki/Solenoide) el primer [electroimán](https://es.wikipedia.org/wiki/Electroim%C3%A1n), y el [galvanómetro](https://es.wikipedia.org/wiki/Galvan%C3%B3metro).

## Origen relativista de las fuerzas magnéticas

No deduciremos el origen del magnetismo a partir de la Relatividad especial, pero daremos una idea de por donde va. Imaginemos una carga libre positiva moviéndose a velocidad constante *v* de forma paralela a un conductor por la que circula una corriente eléctrica; esta corriente de hecho es un movimiento de los electrones del conductor, quedando fijas las cargas positivas .  Para simplificar, supondremos que la velocidad de los electrones es también *v*. Siendo dos sistemas de cargas en movimiento, deberán experimentar fuerzas magnéticas. Dado que el número de cargas positivas y negativas en el conductor está compensado, la carga libre no experimentará fuerza eléctrica alguna.

$caption id="attachment_150131" align="alignnone" width="504"$![Fig. 1: carga en movimiento paralelo a una corriente eléctrica en un conductor](/taller-matematicas/assets/images/magnetisme1.png) Fig. 1: carga en movimiento paralelo a una corriente eléctrica en un conductor. Fuente: [http://galileo.phys.virginia.edu/](http://galileo.phys.virginia.edu/)

Cambiemos ahora al sistema de referencia que se mueve con la carga libre; desde esta referencia las cargas negativas del conductor están fijas y las que se  mueven son las positivas, en sentido contrario:

$caption id="attachment_150132" align="alignnone" width="491"$![Fig. 2: la misma situación de la figura 1 vista desde el sistema de referencia de la partícula libre](/taller-matematicas/assets/images/magnetisme2.png) Fig. 2: la misma situación de la figura 1 vista desde el sistema de referencia de la partícula libre
Ahora bien, siendo ésta referencia móvil respecto a la de la figura 1, debemos aplicar las transformaciones de Lorentz relativistas para tener una imagen real de lo que sucede; concretamente, si aplicamos la [contracción de Lorentz](https://es.wikipedia.org/wiki/Contracci%C3%B3n_de_Lorentz) (disminución de las distancias en la dirección del movimiento) obtenemos que las distancias entre las cargas positivas se verán como menores desde la referencia de la carga libre, algo así como:

$caption id="attachment_150133" align="alignnone" width="491"$![Fig. 3: vista de las cargas móviles aplicando la contracción de Lorentz](/taller-matematicas/assets/images/magnetisme3.png) Fig. 3: vista de las cargas móviles aplicando la contracción de Lorentz
Ahora las cargas en el conductor no están compensadas: hay más densidad de carga positiva que negativa, y en consecuencia la partícula libre experimentará un campo eléctrico, una fuerza, inducida por la velocidad relativa de las cargas positivas del conductor. Esta fuerza será perpendicular a la velocidad que la genera:

$caption id="attachment_150137" align="alignnone" width="509"$![Fig. 6: fuerza debida a la desigual densidad de cargas negativa y positiva](/taller-matematicas/assets/images/magnetisme6.png) Fig. 6: fuerza debida a la desigual densidad de cargas negativa y positiva
Esta fuerza, vista desde la referencia 1 en reposo, es la denominada fuerza magnética. Decir que la contracción mostrada en las figuras está muy exagerada pues en los casos reales las velocidades de las cargas son muchísimo más pequeñas que la velocidad de la luz, y la contracción relativista es casi despreciable. No obstante, incluso esa pequeña contracción a nivel microscópico (electrones del material) ejerce una fuerza apreciable a nivel macroscópico pues el número de electrones portadores de la electricidad es muy elevado. Estos detalles no se trataran aquí, el sitio adecuado seria un articulo sobre electricidad y magnetismo en la materia.

Así pues, el magnetismo es una de las pruebas, y de las más "cercanas" que tenemos, de los efectos predichos por la Relatividad de Einstein.

### Vector campo magnético

Si reflejamos la vista de la figura 1, como si la viéramos en un espejo, ¿qué dirección tomará la fuerza magnética? La situación la vemos en la figura 7:

$caption id="attachment_150161" align="alignnone" width="504"$![Fig. 7: hilo conductor recorrido por una corriente y carga en movimiento, y su reflejo](/taller-matematicas/assets/images/magnetisme10-2.png) Fig. 7: hilo conductor recorrido por una corriente y carga en movimiento, y su reflejo respecto un plano perpendicular a la corriente I
El espejo invierte el sentido de los vectores velocidad e intensidad de corriente, pero el vector fuerza no se modifica; esto es porque el sentido de la fuerza sólo cambia si la velocidad de la carga no es la misma que la de la corriente, ya que entonces la contracción de Lorentz afectaría  a las cargas positivas y negativas del conductor justo al revés, haciendo que la densidad de negativas fuera mayor que la de positivas.

En el siglo XIX cuando se estudiaba el magnetismo los investigadores no tenían todavía la teoría de la Relatividad, pero ya encontraron este comportamiento extraño en sus experimentos. Este comportamiento anómalo del vector fuerza no se da en otros campos de la Física. En el artículo [vectores en Física](http://tallermatematic.ovh/wp/index.php/2016/08/11/vectores/) se explicó que hay dos tipos de vectores: los polares, que bajo una reflexión como la de la figura 7 cambian como lo hacen la velocidad y la intensidad de corriente, y los pseudovectores, que se modifican de otra forma. Parecería entonces que la fuerza magnética no es un vector polar, pero esto es difícilmente aceptable, ya que los vectores fuerza se comportan como vectores polares en todas las situaciones. ¿Cómo solucionamos este comportamiento anómalo del vector fuerza en este caso?  Recordando la propiedad del producto vectorial *[vector] x [pseudovector] = [vector] * se planteó *vector velocidad de la carga x pseudovector campo magnético = vector fuerza*.  O sea, definimos de forma indirecta el pseudovector **campo magnético B** como aquel que cumple

$\overrightarrow F=q\cdot\overrightarrow v\times\overrightarrow B$ [1]

Con esta definición, el vector fuerza sigue siendo un vector polar, como en el resto de la Física.

![la fuerza de inducción magnética sobre una carga en movimiento siempre es perpendicular a la velocidad de la carga](/taller-matematicas/assets/images/força-induccio.png) Fig. 8; la fuerza inducida por el campo  magnético sobre una carga en movimiento siempre es perpendicular a la velocidad de la carga, su módulo depende del ángulo que forma con el vector campo magnético B

 

[![Producto Vectorial según el angulo entre vectores](https://upload.wikimedia.org/wikipedia/commons/0/0d/Producto_Vectorial_seg%C3%BAn_el_angulo_entre_vectores.gif)](https://commons.wikimedia.org/wiki/File%3AProducto_Vectorial_seg%C3%BAn_el_angulo_entre_vectores.gif) Fig. 9: El producto vectorial de los vectores a, b siempre es otro vector perpendicular a los dos, pero no en el mismo plano que los contiene. Además, el módulo del producto es variable entre un valor máximo y cero. Fuente: https://es.wikipedia.org/wiki/Producto_vectorialTal como "funciona" el producto vectorial, si el campo **B** resulta ser paralelo a la velocidad **v**, la fuerza resultante vale cero, y si **B** y **v** son perpendiculares, entonces **F** toma su valor máximo. El producto *a x b* de dos vectores es perpendicular al plano que contiene a los vectores a, b.

El módulo de **F** viene dada por

 
$F=qvB· \sin \left(\alpha \right)$ [2]

donde $\alpha$ es el ángulo que forman el campo **B** y la velocidad **v**.
Como consecuencia de esta fuerza la carga móvil *q* variará su trayectoria, girando, pero sin perder velocidad, pues la fuerza es siempre perpendicular a la velocidad; entonces la carga describirá una trayectoria curva en el campo, esta curva dependerá de como varía B en el espacio. En el caso más simple, si suponemos que B es constante en todo el espacio, la fuerza también será constante, y cuando la carga "entre" en el campo, describirá una trayectoria circular, con una aceleración normal $a_n=F/m=v^2/R$, siendo m la masa de la partícula y R el radio del círculo. Si además el campo B es perpendicular a v tendremos fuerza máxima F=qvB, sustituyendo tenemos $qvB/m=v²/R$ y por tanto el radio de giro es $R=\frac{qB}{mv}$.

$caption id="attachment_1628" align="alignnone" width="328"$![Fig. 4: la carga q con velocidad v curva su trayectoria al entrar en una región con campo magnético perpendicular al plano (aquí B se saldría de la pantalla apuntando hacia nosotros)](/taller-matematicas/assets/images/curvatura-camp-magnetic.png) Fig. 10: la carga q con velocidad v curva su trayectoria al entrar en una región con campo magnético perpendicular al plano (aquí B se saldría de la pantalla apuntando hacia nosotros)
Si en vez de una corriente tenemos un conjunto de corrientes con diversas intensidades, cada una de ellas creará un campo de inducción magnética; puede demostrarse que el campo magnético conjunto será la suma de cada uno de los generados por cada corriente.

$caption id="attachment_150134" align="alignnone" width="433"$![Fig. 4: Campo magnético B creado por un sistema de corrientes y fuerza ejercida sobre una carga q con velocidad v](/taller-matematicas/assets/images/magnetisme4.png) Fig. 11: Campo magnético B creado por un sistema de corrientes y fuerza ejercida sobre una carga q con velocidad v
**Ejemplo 1**: En la figura 4 el campo magnético en cada punto del espacio próximo al origen de coordenadas puede considerarse uniforme y viene dado por B= (0, 5, 0) Tesla; la partícula de carga q = 1C tiene una velocidad v = (-3, 2, 0) m/s. Calcular el vector fuerza F ejercido sobre la partícula. Si la partícula tiene una masa de 100 gramos, describir su movimiento.

Aplicando [1]:

$\overrightarrow F=q\overrightarrow v\times\overrightarrow B=1\cdot\begin{bmatrix}-3\\2\\0\end{bmatrix}\times\begin{bmatrix}0\\5\\0\end{bmatrix}=\begin{vmatrix}i&amp;j&amp;k\\-3&amp;2&amp;0\\0&amp;5&amp;0\end{vmatrix}=\begin{bmatrix}0\\0\\-15\end{bmatrix}.$

La fuerza perpendicular a la velocidad actúa como una fuerza centrípeta, produciendo una aceleración normal $a = F/m$ perpendicular a la velocidad: la partícula gira con velocidad conatante, y como la fuerza también lo es, el movimiento será circular uniforme; dado que la aceleración normal en un movimiento  circular vale a = v²/R, siendo R el radio del círculo descrito, tendremos que F/m = v² / R, por tanto $R\;=\;mv²/F=0.1\cdot\left(\sqrt{3^2+2^2+0}\right)^2/15=9\cdot10^{-2}m$, la partícula gira con un radio de 9cm.

Una vez definido el pseudovector campo magnético, necesitamos saber calcularlo en situaciones diversas; como suele suceder en Física, sólo podremos hacerlo en casos simples, resultando bastante complicado en los casos más generales.

## Fuerza ejercida por un campo magnético sobre una corriente eléctrica

$caption id="attachment_150138" align="alignnone" width="397"$![Fig. 7: elemento de corriente ](/taller-matematicas/assets/images/magnetisme7.png) Fig. 5: elemento de corriente
Imaginemos una corriente rectilínea de portadores negativos de carga, todos ellos con la misma velocidad, y consideremos una pequeña porción de longitud *dx*. Definamos $\rho$ como la densidad de portadores de carga por unidad de volumen (un dato que depende del material conductor) y *S* como la sección recta del conductor. En la sección considerada tendremos* *$dn = \rho·S·dx$ portadores de carga (escribimos *dn* para indicar que es el número de cargas dentro de la pequeña sección dx). Si ahora aplicamos un campo magnético uniforme y constante B, cada una de las n cargas en movimiento experimentará una fuerza  dada por [1],  y la fuerza total sobre la sección del conductor será n veces esa fuerza:

$\operatorname d\overrightarrow F=\left(q\overrightarrow v\times\overrightarrow B\right)\cdot\operatorname dn=\left(q\overrightarrow v\times\overrightarrow B\right)\cdot\rho S\operatorname dx=q\rho S\operatorname dx\cdot\left(\overrightarrow v\times\overrightarrow B\right)$

Siendo la velocidad constante, podemos definir un vector unitario u en su dirección y sacar la celeridad fuera del producto vectorial:

$\operatorname d\overrightarrow F=q\rho Sv\operatorname dx\cdot\left(\overrightarrow u\times\overrightarrow B\right)$

Por definición, $q\rho Sv$ es la intensidad de la corriente, I, luego

$\operatorname d\overrightarrow F=I\operatorname dx\cdot\left(\overrightarrow u\times\overrightarrow B\right)$

Definiendo el vector dl = u·dx, denominado elemento de corriente, obtenemos la fórmula de Laplace para la fuerza ejercida sobre un elemento de corriente por un campo magnético:

$\operatorname d\overrightarrow F=I\cdot\left(\operatorname d\overrightarrow l\times\overrightarrow B\right)$[3]

Dado que hemos trabajado con elementos diferenciales, que hemos supuesto rectilíneos, se puede aplicar [3] para encontrar la fuerza ejercida sobre corrientes en circuitos que no sean rectílineos pero si describan curvas "suaves" (diferenciables), integrando sobre la trayectoria L que recorre la corriente:

$\overrightarrow F=\int_L\operatorname d\overrightarrow F=\int_LI\cdot\left(\operatorname d\overrightarrow l\times\overrightarrow B\right)$ [4].

**Ejemplo 2:** Fuerza ejercida por un campo magnético sobre una corriente que recorre una espira rectangular.

![Fig. 6: corriente que recorre una espira en un campo magnético](/taller-matematicas/assets/images/magnetisme8.png) Fig. 6: corriente que recorre una espira en un campo magnético
Una espira rectangular, de lados *a, b*, es recorrida por una corriente de intensidad I, y está situada en un campo magnético uniforme B que forma un ángulo θ con la recta normal al plano de la espira, como muestra la figura 6. Hallar la fuerza total ejercida sobre la espira.

Consideramos primero el segmento superior de la espira, y los descomponemos en elementos diferenciales de corriente *dl*; cada uno de ellos estará sometido a una fuerza dada por [3]; el producto vectorial $\operatorname d\overrightarrow l\times\overrightarrow B$ nos indica que la fuerza dF estarà dirigida verticalmente hacia arriba (la dirección de giro desde dl hacia B es contraria a las agujas del reloj). Si nos fijamos ahora en el segmento inferior, obtenemos el mismo valor, sólo que aquí la fuerza estará dirigida hacia abajo; luego las fuerzas en los segmentos inferior y superior son iguales en valor pero de sentido contrario: se anulan entre sí.

Vamos por el segmento vertical izquierdo; el módulo del vector fuerza, dado por [3], teniendo en cuenta que el vector B está en el plano perpendicula al segmento, será

$\left|\operatorname d\overrightarrow F\right|=I\cdot\left|\left(\operatorname d\overrightarrow l\times\overrightarrow B\right)\right|=I\cdot\operatorname dl\cdot B$

A lo largo de todo el segmento vertical izquierdo, cada elemento de corriente estará sometido a esa misma fuerza constante, al integrarlas todas:

$\int_L\left|\operatorname d\overrightarrow F\right|=\int_LI\cdot\operatorname dl\cdot B=IB\int_L\operatorname dl=IBa$

donde a es la longitud del segmento; para el segmento vertical derecho obtenemos el mismo valor, pero en sentido contrario, sólo que ahora no se anulará con el segmento izquierdo, pues ambas fuerza resultantes no están aplicadas sobre la misma línea de acción:

![Fig. 8: fuerzas sobre la espira. Las verticales se anulan, las horizontales no están sobre la misma recta](/taller-matematicas/assets/images/magnetisme9.png) Fig. 8: fuerzas sobre la espira. Las verticales se anulan, las horizontales no están sobre la misma recta
En la figura podemos ver que la distancia *d* entre las líneas de aplicación de las fuerzas de los segmentos verticales es igual a $b \sin\left(\theta\right)$; tenemos pues dos fuerzas de igual valor, sentido contrario, y diferente línea de acción, aplicadas sobre un objeto: constituyen un [par de fuerzas](https://es.wikipedia.org/wiki/Par_de_fuerzas), que ejercerán un momento angular que provocará un giro  de la espira (movimiento circular acelerado); el momento resultante será $M=F\cdot d=IBa\cdot d=IBab\sin\left(\theta\right)$.

Usando cálculo integral, puede mostrarse que este resultado se cumple para espiras de cualquier forma, incluso circulares u ovaladas. (Fernandez-Pujal, 1973)

## Campo magnético inducido por una corriente rectilínea

Hemos visto que una corriente eléctrica de intensidad I crea un campo magnético. En el caso ideal simple de que la corriente sea rectilínea "indefinida" (hilo conductor muy largo en comparación al espacio que estamos estudiando) por consideraciones de simetría tendremos que la magnitud de B sólo puede depender de la distancia r al conductor. Lo mismo puede decirse de la fuerza F resultante, dada por la expresión [2]. Además, vimos que esta fuerza puede deducirse por aplicación de la relatividad restringida, y vimos que será perpendicular al conductor (figura 6). Siendo además que esta fuerza F es a su vez perpendicular al campo B, encontramos que los vectores F, B han de ser como los de la figura 9.

![Fig. 9: campo magnético y fuerza resultante inducida por una corriente rectilínea](/taller-matematicas/assets/images/magnetisme10.png) Fig. 9: campo magnético y fuerza resultante inducida por una corriente rectilínea: F es radial, y B es tangencial.
Vectorialmente podemos expresar este resultado con la siguiente expresión, conocida como ley de [Biot-Savart](https://es.wikipedia.org/wiki/Ley_de_Biot-Savart):

$\overrightarrow B=K\cdot\frac{\overrightarrow l\times\overrightarrow r}{r^3}$[5]

donde $\overrightarrow l$ es el vector intensidad de corriente, que tiene por módulo la intensidad de corriente I y por dirección la del hilo conductor, el vector $\overrightarrow r$ es el vector radial, que apunta al punto P donde queremos obtener el campo B, y es perpendicular al hilo conductor, y la constante K depende del medio, en el sistema internacional  y en el vacío vale 10⁻⁷

 **Ejemplo 3**: A lo largo de un hilo conductor muy largo, alineado en la dirección del vector unitario $(1,0,0)$ circula una corriente de 1A; calcular el campo magnético en el punto P(1, 1, 1). Si colocamos en ese punto una carga q = 0.1C, ¿que fuerza se ejercerá sobre ella?

Aplicamos [5]; necesitamos antes obtener el vector radial de P, que en este caso será simplemente (0, 1, 1). Entonces:

$\overrightarrow B=K\cdot\frac{\overrightarrow l\times\overrightarrow r}{r^3}=\frac K{2^{3/2}}\begin{bmatrix}1\\0\\0\end{bmatrix}\times\begin{bmatrix}1\\1\\1\end{bmatrix}=\frac K{2^{3/2}}\begin{vmatrix}i&amp;j&amp;k\\1&amp;0&amp;0\\1&amp;1&amp;1\end{vmatrix}=\frac K{2^{3/2}}\begin{bmatrix}0\\-1\\1\end{bmatrix}$

La fuerza ejercida sobre la carga viene dada por [2], y será cero, pues la velocidad de la carga es cero: sólo se ejerce fuerza magnética sobre cargas en movimiento.

## 

### Bibliografía

 	- Julián Fernández - Marcos Pujal: Iniciación a la Física

 	- E. M. Purcell: Electricidad y Magnetismo

 	- Feynmann: Física, volumen 3, Electromagnetismo y materia
{% endraw %}