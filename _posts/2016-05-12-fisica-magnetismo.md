---
layout: post
title: "Física -> Magnetismo"
date: 2016-05-12 00:19:16 +0000
categories:
  - "Electricidad y Magnetismo"
  - "Fí­sica"
tags:
  - "Campo magnético"
  - "inducción magnética"
  - "magnetismo"
  - "producto vectorial"
math: true
---
{% raw %}

### Magnetismo

![Fig. 1: Magnetita (By Rob Lavinsky, iRocks.com – CC-BY-SA-3.0, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=10139390)](/taller-matematicas/assets/images/470px-Magnetite-118736-294x300.jpg) Fig. 1: Magnetita (By Rob Lavinsky, iRocks.com – CC-BY-SA-3.0, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=10139390)
Antiguamente ya se conocía la propiedad de la [magnetita](https://es.wikipedia.org/wiki/Magnetita) o piedra imán para atraer el hierro, y se utilizó en la primeras brújulas para navegación marítima. También se había observado que la atracción tenía una dirección y también un sentido: la aguja de la brújula se orienta siempre en la misma dirección y sentido.

El primero que dio una explicación al fenómeno de la brújula fue el investigador Willliam Gilbert hacia 1600 en su obra "[De Magnete](https://es.wikipedia.org/wiki/De_magnete)", en la que postula que toda la Tierra es un imán gigante que actúa sobre cualquier brújula, orientándola.

Coulomb experimentó con imanes hasta encontrar, empíricamente, la ley a la que obedecía la fuerza experimentada entre imanes, encontrando que era idéntica  a la [ley de Coulomb para la electrostática](https://es.wikipedia.org/wiki/Ley_de_Coulomb), $F=K·q·q'/d^2$, sustituyendo las cargas eléctricas q, q' por "cargas magnéticas" m, m', i la constante K toma un valor distinto dependiendo de las unidades que tomemos (Coulomb consideró K=1). Ello parecía indicar que había alguna relación entre electrostática y magnetismo, pero no fue hasta 1820 que [Oersted](https://es.wikipedia.org/wiki/Hans_Christian_%C3%98rsted) observó que una aguja imantada colocada cerca de una corriente eléctrica era afectada, como si hubiera un imán cerca; al comunicar su descubrimiento, [Ampère](https://es.wikipedia.org/wiki/Andr%C3%A9-Marie_Amp%C3%A8re) propone que el magnetismo observado es creado por el movimiento de cargas eléctricas (o sea, por la corriente eléctrica); en el caso de los materiales magnéticos, como la magnetita, propone que deben haber corrientes eléctricas permanentes en esos materiales. Además postula que no existen las "cargas magnéticas", sólo las eléctricas.

### Campo magnético creado por inducción

En Física un "campo" es una magnitud física, como por ejemplo la fuerza o la velocidad, que está distribuida en el espacio según alguna ley. Por ejemplo, las velocidades de un fluido en una corriente de una tubería definen un campo de velocidades.

Un conjunto de corrientes eléctricas producirán magnetismo a su alrededor, por lo que diremos que las corrientes inducen un campo magnético. Si consideramos que cualquier carga eléctrica en movimiento produce efectos magnéticos, también sucederá que quedará afectada por el campo magnético inducido. Así pues, si por esa región del espacio en la que hay un campo magnético de inducción pasa una pequeña carga eléctrica q con velocidad v, experimentará una fuerza F debida al campo magnético B. Experimentalmente se encuentra que la fuerza es siempre perpendicular a *v*, pero su magnitud depende de la dirección de *v*: hay una dirección en la que la fuerza es máxima, en las demás es inferior, y en la dirección perpendicular a la de fuerza máxima, la fuerza se anula.

![Fig. 2: la fuerza de inducción magnética sobre una carga en movimiento siempre es perpendicular a la velocidad de la carga](/taller-matematicas/assets/images/força-induccio.png) Fig. 2: la fuerza de inducción magnética sobre una carga en movimiento siempre es perpendicular a la velocidad de la carga, su módulo depende de la dirección de la velocidad.
Matemáticamente esta relación entre los vectores **v**, **F** y sus direcciones se puede expresar diciendo que existe un vector **B** campo magnético, tal que:

$boldsymbol F=qcdotboldsymbol vwedgeboldsymbol B$ [1]

donde "^" representa el [producto vectorial](https://es.wikipedia.org/wiki/Producto_vectorial) de los vectores.

[![Producto Vectorial según el angulo entre vectores](https://upload.wikimedia.org/wikipedia/commons/0/0d/Producto_Vectorial_seg%C3%BAn_el_angulo_entre_vectores.gif)](https://commons.wikimedia.org/wiki/File%3AProducto_Vectorial_seg%C3%BAn_el_angulo_entre_vectores.gif) Fig. 3: El producto vectorial de los vectores a, b siempre es otro vector perpendicular a los dos, pero no en el mismo plano que los contiene. Además, el módulo del producto es variable entre un valor máximo y cero. Fuente: https://es.wikipedia.org/wiki/Producto_vectorial
Tal como "funciona" el producto vectorial, si el campo **B** resulta ser paralelo a la velocidad **v**, la fuerza resultante vale cero, y si **B** y **v** son perpendiculares, entonces **F** toma su valor máximo. El producto a x b es perpendicular al plano que contiene a los vectores a, b.

Concretamente, la magnitud de **F** viene dada por

$F=qvB·sinleft(alpharight)$

donde $alpha$ es el ángulo que forman el campo **B** y la velocidad **v**.
Como consecuencia de esta fuerza la carga móvil *q* variará su trayectoria, girando, pero sin perder velocidad, pues la fuerza es siempre perpendicular a la velocidad; entonces la carga describirá una trayectoria curva en el campo, esta curva dependerá de como varía B en el espacio. En el caso más simple, si suponemos que B es constante en todo el espacio, la fuerza también será constante, y cuando la carga "entre" en el campo, describirá una trayectoria circular, con una aceleración normal $a_n=F/m=v^2/R$, siendo m la masa de la partícula y R el radio del círculo. Si además el campo B es perpendicular a v tendremos fuerza máxima F=qvB, sustituyendo tenemos $qvB/m=v²/R$ y por tanto el radio de giro es $R=frac{qB}{mv}$.

![Fig. 4: la carga q con velocidad v curva su trayectoria al entrar en una región con campo magnético perpendicular al plano (aquí B se saldría de la pantalla apuntando hacia nosotros)](/taller-matematicas/assets/images/curvatura-camp-magnetic.png) Fig. 4: la carga q con velocidad v curva su trayectoria al entrar en una región con campo magnético perpendicular al plano (aquí B se saldría de la pantalla apuntando hacia nosotros)
### Ecuación de Laplace para la fuerza magnética ejercida sobre un elemento de corriente

![Fig. 4: sección de un conductor recorrido por una corriente de electrones](/taller-matematicas/assets/images/element_corrent-300x146.png) Fig. 4: sección de un conductor recorrido por una corriente de electrones
Pensemos en un cable eléctrico recorrido por una corriente de intensidad *I*; en su interior se desplazan cargas eléctricas: electrones, de los que tomaremos su velocidad media como *v*. Si nos fijamos en una pequeña sección longitudinal del cable de longitud *dL, *si el cable tiene una área transversal S, entonces el número de electrones en la sección de longitud dL y área S será proporcional al producto S·dL que es un volumen (superficie x longitud). Por otro lado la intensidad de corriente I es proporcional al producto S·v, sección recta x velocidad media, y vale

$I=frac{triangle q}{triangle t}=frac{eNSvtriangle t}{triangle t}=eNSv$

siendo N la densidad de electrones por m³, y e la carga del electrón.

Supongamos ahora que el cable está situado en una región del espacio en el que hay un campo magnético **B**. Entonces en cada una de las cargas en movimiento actuará una fuerza dada por la ecuación [1]. La fuerza total ejercida sobre el elemento de cable será la suma de fuerzas sobre cada electrón, un total de NSdL:

$boxed{mathbf dmathbf F}=operatorname dqcdotboldsymbol vwedgeboldsymbol B=left(eNSoperatorname dLright)cdotboldsymbol vwedgeboldsymbol B=left(eNSvright)cdotboldsymbol dboldsymbol Lwedgeboldsymbol B=boxed{mathbf Iboldsymbolcdotmathbf dmathbf Lboldsymbolwedgemathbf B}$ [2]

Aquí la "*d*" significa "**diferencial**" y la "*L*" longitud: en Física la diferencial de una magnitud es una fracción muy pequeña de ella, y tiene relación con la diferencial y la derivada de una función, conceptos de análisis matemático, ver por ejemplo [Uso de diferenciales en Física](http://tallermatematic.eu/wp2/index.php/2016/05/10/uso-de-diferenciales-en-fisica/). Hemos definido el vector **dL** como el vector que tiene la dirección de **v** y la longitud dL, de esta forma en el sustituimos el vector velocidad por  el módulo de la velocidad.

### Fuerza ejercida por un campo magnético B sobre la corriente I que circula por una espira cerrada

![Fig.5: Espira rectangular de lado d por la que circula una corriente I, sometida a un campo magnético B](/taller-matematicas/assets/images/espira-campo-B.png) Fig.5: Espira rectangular de lado d por la que circula una corriente I, sometida a un campo magnético B
En la figura 5 vemos un circuito cerrado cuadrado de lado d por el que circula una corriente continua I; el circuito está en una región del espacio en el que hay un campo magnético B uniforme, que forma un cierto ángulo con la normal al plano del circuito. En estas condiciones, cada elemento diferencial del circuito estará sometido a una fuerza diferencial dada por la ecuación de Laplace [2]. En cada lado del rectángulo, la fuerza diferencial tendrá el mismo sentido y dirección, por lo que la suma total de fuerzas, en cada lado, será un vector fuerza resultante, dibujado en rojo en la figura 5, y que por simetría se aplicará en el punto medio de cada lado. En los lados superior e inferior las fuerzas resultantes  tienen sentidos opuestos, por lo que anulan entre sí, pero en los laterales las resultantes aunque son iguales en módulo, $IBdsinleft(alpharight)$ no son opuestas, están giradas un ángulo, por lo que forman un par de fuerzas de valor  $IBd^2sinleft(alpharight)$. Si definimos el vector momento magnético de la espira por $boldsymbol M=IBScdotboldsymbol n$, donde A=d² es el area de la espira y n es el vector unitario normal a la espira, entonces el par de fuerzas resultante se expresa como $boldsymbol Pboldsymbol=boldsymbol Mboldsymboltimesboldsymbol B$, el producto vectorial del momento magnético de la espira por el campo magnético. Este par tenderá a hacer girar la espira, alineando los vectores **M** y **B** (al estar paralelos su producto vectorial será cero). Usando [2] y cálculo integral, puede mostrarse que este resultado se cumple para espiras de cualquier forma, incluso circulares u ovaladas. (Fernandez-Pujal, 1973)

### Ley de Ampère

 
### Bibliografia

 	- Julián Fernandez y Marcos Pujal: Iniciación a la Física, volumen II, 1973
{% endraw %}