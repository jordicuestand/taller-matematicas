---
layout: post
title: "Física -> Electricidad -> Circuitos CC"
date: 2016-05-06 11:10:11 +0000
categories:
  - "Electricidad y Magnetismo"
  - "Fí­sica"
tags:
  - "circuito CC"
  - "fcem"
  - "fem"
  - "generador paralelo"
  - "generador serie"
  - "Kirchoff"
  - "potencial"
  - "red CC"
  - "resistencia paralelo"
  - "resistencia serie"
math: true
---
{% raw %}

### Generador eléctrico, f.e.m.

Las cargas eléctricas siempre se mueven desde la zona de más potencial eléctrico *V* hacia la de menor potencial (eléctrico); un símil fácil de recordar es el de comparar la corriente de cargas con una corriente de agua, que también se mueve desde las zonas más elevadas(con mayor energía potencial gravitatoria) hacia las más bajas (con menor energía potencial gravitatoria).

$caption id="attachment_1589" align="alignnone" width="255"$![Diferencia de energía potencial y sentido de la corriente](/taller-matematicas/assets/images/desnivell.png) Fig. 1:Diferencia de energía potencial y sentido de la corriente[/caption]
En un circuito cerrado, para que haya circulación continua tendremos que volver a dar potencial a las cargas (o al agua) que la han perdido al "bajar" el desnivel; en el caso de una corriente de agua usaríamos una bomba para volver a subirla al nivel, en el caso de cargas usaremos un generador eléctrico:

$caption id="attachment_1590" align="alignnone" width="380"$![Fig.2: Circuito cerrado, el Generador G devuelve la energía potencial perdida en el recorrido](/taller-matematicas/assets/images/circuit-simple.png) Fig.2: Circuito cerrado, el Generador G devuelve la energía potencial perdida en el recorrido, aunque al tener una resistencia interna, parte de su fuerza electromotriz E se pierde según la ley de Ohm  V=Ir[/caption]
Las características del generador son: su **fuerza electromotriz** *E* (**f.e.m.**) que és el potencial que es capaz de restituir a la corriente que lo atraviesa, y su **resistencia interna** *r* que produce una disminución de su f.e.m. efectiva que puede calcularse según la **ley de Ohm**: $V = I·r$. Así, la diferencia de potencial en el circuito de la figura 2 cumple $V_A-V_B=E-rI$. El símbolo utilizado para el generador en los diagramas eléctricos es ![generador electric](/taller-matematicas/assets/images/generador-electric.png) con el polo negativo indicando la entrada donde tenemos potencial menor, y el polo positivo la salida con el potencial aumentado en *+E*. También suelen usarse como generadores de corriente pilas o asociaciones de pilas, con los símbolos ![pila](/taller-matematicas/assets/images/pila.png) o bien ![piles](/taller-matematicas/assets/images/piles.png).

**Fuerza contralectromotriz (f.c.e.m.)**
Aparte de las resistencias, las cuales convierten la energía eléctrica en calor, hay otros elementos que convierten la energía eléctrica en otras formas de energía; el efecto que tienen sobre el potencial es reducirlo. Se suelen representar de igual modo que los generadores de corriente pero con los polos invertidos, para representar que en vez de aumentar el potencial, lo reducen. O sea: si la corriente atraviesa un elemento en el sentido de más potencial a menos el elemento disminuye el potencial en una cantidad E, que se denomina **fuerza contraelectromotriz** *E* (**f.c.e.m.**), y si lo atraviesa en el sentido de menos a más, entonces actúa como fuerza electromotriz.

$caption id="attachment_1597" align="alignnone" width="300"$![Fig. 3: E1 actúa como f.e.m., E2 actúa como f.c.e.m.](/taller-matematicas/assets/images/fcem-300x98.png) Fig. 3: E1 actúa como f.e.m., E2 actúa como f.c.e.m.[/caption]
Por ejemplo, en la figura 3, si la intensidad va de izquierda a derecha, entonces el primer elemento actúa como f.e.m. y el segundo como f.c.e.m., así que la diferencia de potencial entre los puntos A y B es $V_B-V_A=E_1-E_2$.

### Circuitos de corriente continua

En un circuito de corriente continua (CC) suelen haber diversos componentes distribuidos: resistencias, f.e.m., f.c.e.m.,  y condensadores, como en la figura 4.

$caption id="attachment_1600" align="alignnone" width="300"$![](/taller-matematicas/assets/images/circuit-simpleCC-300x164.png) Fig. 4: Circuito simple completo en CC[/caption]
Las baterías V1 y V2 aportaran una fem E1, E2 respectivamente. Supongamos que la corriente circula en el sentido ABCDEA, entonces aplicando la ley de Ohm sucesivamente a cada tramo:

$V_A-V_B=IR_1+E_2$

$V_B-V_C=IR_2$

$V_C-V_D=IR_4$

$V_D-V_E=-E_1$

$V_E-V_A=0$

En la última igualdad hemos supuesto que el condensador está totalmente cargado; sumando todas las ecuaciones anteriores, nos queda

$0=IR_1+E_2+IR_2+IR_4-E_1Rightarrow-E_1+E_2+Ileft(R_1+R_2+R_4right)=0$,

que equivale a decir que:

*si fijamos un sentido arbitrario a la corriente, considerando positivas las fem que vayan en esa dirección y negativas a las que no, llamando R a la suma de todas las resistencias y E a la suma de todas las fem (teniendo en cuenta sus signos positivos o negativos), entonces se cumplirá* $I=E/R$ [1] que es la **ley de Ohm para un circuito**.

#### Asociaciones de resistencias

$caption id="attachment_1604" align="alignnone" width="461"$![Asociaciones de resistencias](/taller-matematicas/assets/images/asoc_resistencies.png) Fig. 5: Asociaciones de resistencias[/caption]
En la figura 5 vemos, a la izquierda. dos **resistencias en serie** (por ambas circula la misma intensidad de corriente) y a la derecha, tres **resistencias en paralelo** (la diferencia de tensión entre sus extremos es la misma, la intensidad es distinta).

Para las resistencias en serie se cumple que la diferencia de potencial cuando la corriente I atraviesa las dos será $V=IR_1+IR_2=I(R_1+R_2)=IR$ donde hemos definido la resistencia equivalente R como la suma de resistencias.

Para las resistencias en paralelo definamos la **conductancia** G como el inverso de la resistencia, $G=1/R$, con lo que la ley de Ohm, se expresa $V=I/G$ o equivalentemente $I=VG$; entonces como en los extremos de cada rama tenemos la misma diferencia de potencial V, aplicando la ley de Ohm en las tres tenemos que $I_1=VG_1, I_2=VG_2, I_3=VG_3$, sumando las tres ecuaciones, $I_1+I_2+I_3=V(G_1+G_2+G_3)$, pero la suma de las intensidades de las tres ramas es igual a la intensidad total que entra (y que sale)  $I_1+I_2+I_3=I$, o sea que $I=V(G_1+G_2+G_3)$. Si definimos la conductancia equivalente $G=G_1+G_2+G_3$ entonces se cumple que $begin{array}{l}I=VG=frac VR=Vleft(G_1+G_2+G_3right)=Vleft(frac1{R_1}+frac1{R_2}+frac1{R_3}right)Rightarrow\boxed{frac1R=frac1{R_1}+frac1{R_2}+frac1{R_3}}end{array}$. Resumiendo:

*La resistencia equivalente R a un conjunto de n resistencias en serie $R_i$ es la suma de todas ellas, $R={textstylesum_1^n}R_i$; La resistencia equivalente R a un conjunto de n resistencias en paralelo $R_i$ verifica $frac1R={textstylesum_1^n}frac1{R_i}$.*

**Ejemplo 1: circuito con asociaciones de resistencias.**

$caption id="attachment_1608" align="alignnone" width="419"$![asoc_resistencies_exemple](/taller-matematicas/assets/images/asoc_resistencies_exemple.png) Fig. 6: circuito con asociaciones de resistencias[/caption]
En el circuito de la figura 6 se nos pregunta por las intensidades I, I1, I2 e I3. Evidentemente $I=I1+I2+I3$. Para aplicar la ley de Ohm $V=IR$ y calcular cada intensidad en cada tramo del circuito necesitamos saber los potenciales V y las resistencias. Entre los puntos A y B está claro que V=5 (proporcionados por la única f.e.m. E); pero no sabemos cual es la tensión en la entrada de las resistencias en paralelo, pues no sabemos que vale I. El que vamos a hacer es calcular la resistencia equivalente de todo el circuito, y así podemos hallar I.

 	- Resistencia equivalente en el tramo I2: están en serie, luego $R_{eq}I2=R3+R5=2$

 	- Resistencia equivalente a las resistencias en paralelo:

$frac1{R_{eq.p.}}=frac1{R_2}+frac1{R_{eq}I2}+frac1{R_4}=frac11+frac12+frac11=frac52Rightarrow R_{eq.p.}=frac25$

3. Resistencia equivalente a todo el circuito: están en serie, luego las sumamos: $R=1+frac25=frac75$

Ahora calculamos $I = V/R = 5frac57=frac{25}7$

La variación de tensión debida a la resistencia R1 es $V=frac{25}7·1=frac{25}7$; entonces la diferencia de potencial entre la entrada y la salida de las resistencias en paralelo será $5-frac{25}7=frac{10}7$. Para el tramo I1, aplicamos Ohm: $I1=V/R2=frac{10}7/1=frac{10}7$. Para el tramo I3, lo mismo, $I3=V/R2=frac{10}7/1=frac{10}7$. Para el tramo I2 aplicamos que $I=I1+I2+I3Leftrightarrow I=I-I1-I3=frac{25}7-frac{10}7-frac{10}7=frac57$.

![separador2](/taller-matematicas/assets/images/separador2.png)
#### Asociaciones de generadores

También podemos encontrarnos con circuitos en los que hayan asociaciones de generadores (fig. 6).

$caption id="attachment_1607" align="alignnone" width="300"$![Fig. 6: Asociaciones en paralelo y en serie de generadores](/taller-matematicas/assets/images/asoc_generadors-300x200.png) Fig. 6: Asociaciones en paralelo y en serie de generadores[/caption]
En la figura 6, a la izquierda tenemos tres **generadores dispuestos en paralelo**; consideraremos el caso más simple en el que los tres son iguales: todos tienen f.e.m. *e* y resistencia interna *r*, y por cada uno circulará una intensidad de corriente I. Como los tres están conectados a un mismo punto, la intensidad total en ese punto será la suma de intensidades, 3I; por otro lado, las tres resistencias internas *r* están en paralelo, así que la resistencia equivalente cumple $1/R = 1/r + 1/r + 1/r = 3/r$, por tanto $R=r/3$. Si imaginamos un generador equivalente a los tres, tendrá una intensidad de corriente 3I con una resistencia interna de *r/3*; su f.e.m. la obtenemos aplicando Ohm: $E=I_{eq}R=3Icdot r/3=Ir=e$, vemos que es la misma de los generadores en serie, en resumen:

*la asociación de n generadores en paralelo todos iguales con f.e.m. E y resistencia interna r equivale a un único generador de f.e.m. E y resistencia interna r/n.*

La asociación de la derecha, en la figura 6, representa dos **generadores en serie**, V2, V5, con f.e.m. E1 y E2 y resistencias internas r1, r2; por ambos circula la misma corriente I, con lo que el generador equivalente tendrá f.e.m. E1 + E2 y resistencia interna r1 + r2.

**Ejemplo 2: circuito con asociación de generadores y de resistencias**

$caption id="attachment_1616" align="alignnone" width="231"$![Fig. 7: asociaciones de generadores y resistencias](/taller-matematicas/assets/images/asoc_generadors_exemple.png) Fig. 7: asociaciones de generadores y resistencias[/caption]
En la figura 7, supongamos que E1=E2=6V, con resistencias internas r=1, y que E3=3V con resistencia interna r=1/3, las resistencias R1, R2 y R3 valen 2 Ohm. E1 y E2 equivalen a un generador de E12=6V y resistencia interna r=1/2; la asociación de este generador con E3 es en serie, luego la f.e.m. total será E = E12 + E3 = 6 + 3 = 9V, y la resistencia interna total es 1/2 + 1/3 = 5/6. En cuanto a las resistencias en paralelo R2 y R3, equivalen a una resistencia 1/R23 = 1/R2 + 1/R3 = 1/2 + 1/2 = 1, por tanto R23 = 1; por último, esta resistencia se suma a la R1, resultando la resistencia equivalente R = R23 + R1 = 1 + 2 = 2 Ohm. Nos queda un circuito equivalente a un generador E = 9V, r = 5/6 y R = 2, por el que circulará una corriente I = E / (R + r) = 9 / (2 + 5/6) = 54/17.

![separador2](/taller-matematicas/assets/images/separador2.png)
### Redes en CC: leyes de Kirchoff

Cuando combinamos las conexiones entre elementos de forma que aparecen puntos en los cuales se cruzan más de dos conexiones, diremos que tenemos una **red eléctrica**; los puntos de cruce se llaman **nodos de la red**.

**Ejemplo 3**: consideramos la siguiente red

$caption id="attachment_1586" align="alignnone" width="433"$![Fig. 1: red eléctrica con dos circuitos.](/taller-matematicas/assets/images/CircuitCCP47.png) Fig. 8: red eléctrica con dos circuitos.[/caption]
Esta red consta de dos circuitos simples que comparten un hilo, y vemos que hay dos nodos en los que se cruzan tres hilos conectores, el nodo inferior tiene una conexión a tierra, indicando que está a potencial eléctrico cero. Aplicando la ley de Ohm reiteradamente a cada tramo de la red podemos obtener las intensidades en todo punto. Pero se puede sistematizar este procedimiento aplicando dos leyes debidas a [Gustav Robert Kirchoff:](https://es.wikipedia.org/wiki/Gustav_Kirchhoff)

*1ª ley de Kirchoff: la suma algebraica de intensidades en cada nudo es igual a cero;*

*2ª ley de Kirchoff: en cada circuito simple de la red se cumplirá la ley de Ohm para un circuito, ecuación [1], teniendo en cuenta que, fijado un sentido de recorrido escogido libremente, se consideraran positivas las intensidades y f.e.m. en ese sentido, y negativas en caso contrario.
*

Vamos a aplicar estas leyes al circuito de la figura 8; para ello, damos nombres a las intensidades que circulan por cada tramo de cada circuito de la red, y direcciones arbitrarias, teniendo en cuenta que en el hilo conector compartido por los dos circuitos  la intensidad será distinta:

![](/taller-matematicas/assets/images/Kirchoff1b.png)

La 1ª ley de Kirchoff aplicada al nudo superior, considerando que la intensidad que entra en el nudo B tiene signo positivo y la que sale negativo, da: I_1-I_2-I_3=0. En el nudo E no es necesario aplicar la ley, por motivos algebraicos (dependencia lineal de las ecuaciones) sólo hay que aplicarla a n-1 nodos de la red, en este caso esta red tiene sólo n = 2 nodos.

Para aplicar la 2ª ley, la de Ohm para un circuito simple completo, $sum_{}E=Isum_{}R$, fijamos el sentido del recorrido como el de las agujas del reloj; aplicada al circuito simple de la izquierda (a los circuitos simples en redes se les denomina **mallas de la red**) nos da el recorrido ABEFA y la ecuación V1 - V2 = I1·(R1 + R5) + I·R2.

La 2ª ley aplicada a la malla de la derecha recorrida en el sentido de las agujas del reloj nos da otra ecuación:

V2 + V3 = I3·(R3 + R4) - I2·R2

Tenemos un total de 3 ecuaciones con tres incógnitas; sustituimos los valores dados: I1-I2-I3=0; -16 = I1·3 + I2·2; 40 = I3·10 - I2·2. Escribiéndolo en forma estándar:

$begin{array}{l}I_1-I_2-I_3=0\;3I_1;+;2I_2;=-16\;;;-2I_2+10I_3=40end{array}$

Resolviendo este sistema, con calculadora o bine on-line con [http://matrixcalc.org/es/slu.html ](http://matrixcalc.org/es/slu.html)o con [wolfram ... ](http://www.wolframalpha.com/)

$caption id="attachment_1620" align="alignnone" width="474"$![Resolviendo on-line el sistema lineal con Wolfram Alpha, llamamos x=I1, y=I2, z=I3](/taller-matematicas/assets/images/wolfram_sistema_lineal.png) Resolviendo on-line el sistema lineal con Wolfram Alpha, llamamos x=I1, y=I2, z=I3[/caption]

Las intensidades son pues  I1 = -2 (por tanto circula en sentido inverso al que hemos supuesto), I2 = -5 (misma observación) e I3 = 3.
Encontremos ahora los potenciales en los puntos A, B, C y D. Como $V_E=0$  y el punto F está al mismo potencial que E, nos fijamos en el tramo AF; la intensidad que circula en ese tramo es I1=-2 (por tanto circula en sentido A->F), aplicando la ley de Ohm a este tramo obtenemos:

![tram_Ohm](/taller-matematicas/assets/images/tram_Ohm.png)

$V_F-V_A=E-IR=-8-2cdot1=-10Rightarrow V_A=V_F+10=0+10=10.$

observemos que hemos tomado I1 = 2, pues hemos considerado que su dirección es la correcta, de A hacia F, y que el generador actúa como f.c.e.m. con signo negativo pues I1 la atraviesa de + a -

 

Para el punto B partimos del potencial en A: $V_B-V_A=I_1R_1=2cdot2=4Rightarrow V_B=V_A+4=14V$.

Para el punto C, partimos de B: $V_B-V_C=I_3R_3=6Rightarrow V_c=V_B-6=8V$

Finalmente para el punto D sumamos los 16V de la f.e.m. V3, resulta $V_D=V_C+16=24V$.

![separador2](/taller-matematicas/assets/images/separador2.png)

 

 

Los circuitos de este post han sido dibujados con la herramienta on-line easyeda.com
{% endraw %}