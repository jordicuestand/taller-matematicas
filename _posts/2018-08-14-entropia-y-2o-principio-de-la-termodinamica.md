---
layout: post
title: "Entropía y 2º principio de la termodinámica"
date: 2018-08-14 16:44:27 +0000
categories:
  - "Fí­sica"
  - "Termodinámica"
math: true
---
{% raw %}

Se observa que el calor Q fluye de forma natural desde las fuentes térmicas de más temperatura a las de menos, pero al revés no sucede, excepto si lo forzamos gastando un trabajo W. El 1r principio de la termodinámica establece un balance entre el calor entregado a un sistema, el trabajo realizado por el sistema y su incremento de energía interna, Q = W + ΔE, pero no dice nada del sentido de la transferencia de calor, nada prohíbe que fluya de menos a más temperatura. Se necesita un criterio adicional al 1r principio que regule el sentido de las transferencias de calor, y ese será el 2º principio.

Lo que se explica a continuación sigue el siguiente esquema: 1) exploramos la relación calor transferido/temperatura, Q/T,  en un ciclo reversible, 2) visitaremos brevemente el análisis matemático recordando las nociones de *campos vectoriales conservativos*, *circulación de un vector* en el campo y *potencial* del campo, 3) usaremos esos conceptos matemáticos y la relación Q/T de un ciclo para definir la función de estado *entropía S*, y a continuación 4) veremos las propiedades más importantes de S y sus aplicaciones prácticas en los cambios de estado termodinámicos.
### Relación entre calor transferido y temperatura en un ciclo de Carnot

En [Trabajo, calor y primer principio de la Termodinámica](http://tallermatematic.ovh/wp/index.php/2018/07/31/trabajo-calor-1r-principio-de-la-termodinamica/) se estudian los *ciclos de Carnot*, que son sucesiones continuas de cambios de estado *reversibles* (en cada instante el sistema está siempre en equilibrio termodinámico) y  *cíclicos* (estado final igual al estado inicial) formados por dos transformaciones isotermas (temperatura T = cte) y dos adiabáticas (calor transferido Q = 0). En la figura 1 vemos en un diagrama Presión-Volumen las isotermas (transformaciones desde 1 a 2 y de 3 a 4) y las adiabáticas 2->3 y 4->1.

[caption id="attachment_150685" align="alignnone" width="268"]![](/assets/images/Carnot-1.png) Fig.1: ciclo de Carnot representado en el diagrama Presión-Volumen[/caption]

Aplicando la relación PV = cte para las isotermas y $PV^\gamma$ para las adiabáticas del ciclo de Carnot:

$\begin{array}{l}P_1V_1=P_2V_2\\P_2V_2^\gamma=P_3V_3^\gamma\\P_3V_3=P_4V_4\\P_4V_4^\gamma=P_1V_1^\gamma\end{array}$

si las multiplicamos todas entre sí y eliminamos términos repetidos, nos queda

${V_2}V_4=V_3V_1$ [1]

Supongamos ahora que el sistema usado en el ciclo es un gas ideal, entonces la ecuación de estado es PV = nRT, y además el trabajo generado en las isotermas será (para detalles ver [Trabajo, calor y primer principio de la Termodinámica](http://tallermatematic.ovh/wp/index.php/2018/07/31/trabajo-calor-1r-principio-de-la-termodinamica/)) $W_{12}=nRT\ln\left(\frac{V_2}{V_1}\right),\;W_{34}=nRT'\ln\left(\frac{V_4}{V_3}\right)$. Dividiendo la primera por la segunda y aplicando [1]:

$\frac{W_{12}}{\;W_{34}}=\frac{T\ln\left({\displaystyle\frac{V_2}{V_1}}\right)}{T'\ln\left(\frac{V_4}{V_3}\right)}=\frac{T\ln\left({\displaystyle\frac{V_2}{V_1}}\right)}{-T'\ln\left(\frac{V_3}{V_4}\right)}=-\frac T{T'}$.

Tengamos ahora en cuenta que, pr el 1r principio, $Q = W_{12},\;Q'=W_{34}$, así que nos queda la relación
$\frac Q{Q'}=-\frac T{T'}\Leftrightarrow\boxed{\frac QT+\frac{Q'}{T'}=0}$ [2]

que relaciona de forma simple los calores transferidos con las temperaturas a las que se transfieren. En particular, si prescindimos de los signos (valores absolutos) implica que si T > T' entonces |Q| > |Q'|: se transfiere más calor del foco térmico que está a más temperatura; la diferencia |Q| - |Q'| es igual al trabajo realizado por el ciclo, y si fuera T = T', entonces |Q| = |Q'| y el trabajo W seria nulo. Pero el trabajo es igual al área encerrada en el diagrama PV por el ciclo, y un trabajo nulo implica que no hay área, luego no se puede recorrer un ciclo manteniendo la temperatura constante en todo él, ha de haber una diferencia de temperatura.
### Relación entre calor transferido y temperatura en un ciclo reversible

Generalicemos ahora el resultado del apartado anterior al caso de ciclos reversibles cualesquiera, que representamos en la figura 2.

[caption id="attachment_150706" align="alignnone" width="270"]![](/assets/images/recubriment_Carnot.png) Fig.2: ciclo reversible cualquiera, parcialmente recubierto por ciclos de Carnot[/caption]

Hemos añadido algunos ciclos de Carnot (recordemos, isoterma seguida de adiabática seguida de isoterma seguida de adiabática) tales que recubren parcialmente el área del ciclo C, representado en el diagrama PV por una elipse, pero puede ser cualquier figura (con alguna restricción geométrica que no enunciaremos); los ciclos de Carnot tienen las curvas adiabáticas muy pequeñas, de forma que se van ajustando más o menos a la curva C, mientras que las isotermas son más largas y recorren de lado a lado el interior de C, Podemos imaginarnos que dibujamos más ciclos Carnot hasta recubrir en su totalidad toda el área C. Además, observando la figura 1, como cada ciclo de Carnot está adyacente a otro ciclo, podemos pensar que el calor cedido Q' por cada ciclo es igual al absorbido Q por el siguiente, pero no son exactamente iguales, pues cada ciclo de Carnot tampoco coincide exactamente con su contiguo (fig. 3), de forma que el calor cedido Q' por el i-èsimo ciclo de Carnot no es exactamente igual al absorbido por el (i+1): $\textstyle Q'_i=Q_{i+1}+\triangle Q_{i,i+1}$, hay una diferencia.

[caption id="attachment_150707" align="alignnone" width="206"]![](/assets/images/superposicio-cicles-carnot.png) Fig.3: detalle de dos ciclos contiguos de Carnot  del recubrimiento de un ciclo C[/caption]

Además, para cada ciclo de Carnot se cumplirá [2]: $\frac{Q_i}{T'_i}+\frac{Q_i'}{T_i'}=0$, y la suma anterior extendida a todos los n ciclos también dará cero:

$\sum_i\left(\frac{Q_i}T+\frac{Q'_i}{T_i'}\right)=0$ [3]

Llevando al límite para $n\rightarrow\infty$ ciclos de Carnot, C quedará recubierto de forma que $\triangle Q_i\rightarrow\operatorname dQ$, las adiabáticas de cada ciclo de Carnot tenderán a coincidir con el elemento diferencial de longitud *d**l*** de la curva C, y la suma [3] pasará a ser una integral extendida a todo el contorno C:
$\oint_{C,rev}\frac{\operatorname dQ}T=0$ [4]

donde hemos dejado de distinguir calor absorbido Q del emitido Q' y simplemente tenemos un dQ transferido (en más o en menos), y la temperatura T es una variable que toma valores distintos en cada punto de C; también hemos puesto el subíndice *rev* para indicar que el ciclo se recorre de forma reversible. A continuación hacemos una breve incursión por el análisis matemático, que nos da herramientas potentes para manejar las integrales [4].
### Circulación y potencial de un campo conservativo

Un *campo vectorial* es una función que asigna a cada punto P un vector **v**(P), como por ejemplo el campo eléctrico, o la asignación a cada punto del espacio (x, y, z) del interior de un gas de una magnitudes (P, V, T) entendidas como un vector en un espacio vectorial. Imaginemos un camino cualquiera (una trayectoria entre dos puntos A, B)  en el espacio a través de una curva C; para cada uno de sus puntos P, existirá un vector campo v(P), y un elemento diferencial d**l** que será tangente a la curva en P:

[caption id="attachment_150708" align="alignnone" width="379"]![](/assets/images/circulacio-vector.png) Fig.4: curva C, elemento diferencial dl tangente a C en P, y vector campo v(P) en P[/caption]

Denominamos *circulación del campo v(P) entre los puntos A, B a lo largo de la curva C* a la suma de los productos escalares **v**(P)·d**l** extendida a todos los puntos P entre A y B:
$Circ_C\left(\overrightarrow v,A,B\right)={\int_A^B}_C\overrightarrow v\operatorname d\overrightarrow l$ [5]

En el caso de que C sea un *camino cerrado*, escribimos la integral así:
$Circ_C\left(\overrightarrow v\right)=\oint_C\overrightarrow v\operatorname d\overrightarrow l$[6]

Hay un tipo especial de campos vectoriales que en Física son de gran interés, son los denominados *campos conservativos*, en los que se cumple la condición siguiente para todo camino cerrado C:
$Circ_C\left(\overrightarrow v\right)=\oint_C\overrightarrow v\operatorname d\overrightarrow l=0$ [7]

Se llaman "conservativos" pues, por las propiedades de las integrales (ver figura 5):

$\oint_C\overrightarrow v\operatorname d\overrightarrow l=\int_{PQR}\overrightarrow v\operatorname d\overrightarrow l+\int_{RSP}\overrightarrow v\operatorname d\overrightarrow l=0\Rightarrow\int_{PQR}\overrightarrow v\operatorname d\overrightarrow l=-\int_{RSP}\overrightarrow v\operatorname d\overrightarrow l$,

además, invirtiendo el sentido de integración,

$\int_{RSP}\overrightarrow v\operatorname d\overrightarrow l=\int_{PSR}-\overrightarrow v\operatorname d\overrightarrow l$

y por tanto:

$\int_{PQR}\overrightarrow v\operatorname d\overrightarrow l=\int_{PSR}\overrightarrow v\operatorname d\overrightarrow l$,

que nos dice que *el valor de la circulación de un campo conservativo sólo depende de los puntos inicial P y final R, y no del camino concreto recorrido entre esos dos puntos*. [7']

[caption id="attachment_150709" align="alignnone" width="284"]![](/assets/images/ostres.png) Fig.5: un camino cerrado C y algunos de sus puntos, P, Q, R, S[/caption]

Debido a esta propiedad de conservar el valor de la circulación entre dos puntos independientemente del camino recorrido, en los campos conservativos se puede la magnitud *diferencia de potencial* $V_{PR}$ como
$V_{PR}=\int_{PR}\overrightarrow v\operatorname d\overrightarrow l$ [8]

para cualquier trayectoria entre los puntos P y R. Tomando un punto cualquiera O como referencia, el *potencial* en otro punto P se define como $V_P=V_{PO}=V_P-V_O$.

Los potenciales tiene gran interés en física; así por ejemplo, un campo vectorial eléctrico es conservativo, y por tanto se puede definir un potencial eléctrico en cada punto del campo, además, la corriente eléctrica solo fluye en el sentido de más potencial a menos potencial.
### Entropía

Por analogía, siguiendo el apartado anterior y comparando con el resultado [4] obtenido para la relación Q/T en un ciclo reversible, podemos igualar dQ/T al producto escalar de un cierto campo vectorial **v** por el elemento diferencial de longitud del camino C; siendo nula la integral para todo C reversible y cerrado, concluimos que ese campo **v** es conservativo, luego admite un potencial que se calculará según [8], que en el caso termodinámico será
$S_{AB}=S_A-S_B=\int_{AB_{REV}}\frac{\operatorname dQ}T$ [9]

A la cantidad $S_A$ la llamamos ***entropía del estado*** A, y seria el potencial del campo en ese punto; de hecho no nos interesa el campo en sí, que sólo es instrumental, sino el potencial, la entropía. Para cada estado (P, V, T) queda definido una entropía (resultado [7']) , de forma que podemos decir que* la entropía es una función de estado*: dos estados distintos tienen entropía distinta.

Observar que en la integral [9] entre los estados A, B hemos incluido el subíndice *REV* para indicar que *la transformación A->B que se use para el cálculo ha de ser reversible*. [9a]

**Propiedades inmediatas de la entropía S**

 	- Como S es función de estado, la variación de entropía de un sistema que evoluciona siguiendo un ciclo cerrado cualquiera, tanto si es reversible como si es irreversible, es nula.

 	- Como S es función de estado, en una transformación de un sistema desde el estado A hasta el B, la variación de entropía será la misma tanto si se hace de forma reversible como si se hace de forma irreversible.

### Transformaciones internas reversibles de sistemas aislados

A continuación aplicaremos la entropía como herramienta para comprender mejor qué sucede en las transformaciones de los denominados  sistemas aislados, que son aquellos que no reciben ni entregan calor ni trabajo, siendo todas sus transformaciones internas. Imaginemos un sistema así, como por ejemplo un recipiente con aislamiento térmico en el que hemos introducido un líquido A a temperatura $T_1$ superior a la $T_2$  del aire que contiene el resto del volumen B del recipiente, y acto seguido lo cerramos. Como hay una diferencia de temperatura interna, habrá un flujo de calor Q (fig. 6)

[caption id="attachment_150714" align="alignnone" width="252"]![](/assets/images/sistema-tancat.png) Fig.6: Sistema aislado del exterior, con una transferencia interna de calor Q[/caption]

Llamando $Q_A$ al calor absorbido por A, y $Q_B$ al absorbido por B, en general en un sistema aislado en el que no se intercambia calor con el exterior, $Q_A+Q_B=0$. Por el 1r principio de la termodinámica, Q = W + ΔE, siendo W = 0, tendremos también ΔE = 0, o sea $\triangle E_A+\triangle E_B=0$.

Supongamos que el intercambio de calor es reversible: implica que la diferencia de temperatura entre A y B es tan pequeña que en ningún momento ni A ni B salen de los estados de equilibrio, supondremos T = T'; entonces los incrementos diferenciales de entropía (reversible) de cada subsistema A, B son, aplicando [9]:

$\operatorname dS_A=\frac{\operatorname dQ_A}T,\;\operatorname dS_B=\frac{\operatorname dQ_B}T$,

pero ha de ser $\operatorname dQ_A=-\operatorname dQ_B$ al ser reversible, y la variación de entropía total es:

$\operatorname dS=\operatorname dS_A+\operatorname dS_B=\frac{\operatorname dQ_A}T+\frac{\operatorname dQ_B}T=0$,

que puede enunciarse así:
en un sistema aislado que evoluciona reversiblemente, la variación de entropía interna es nula.
En los sistemas reales no podremos en general hacer una suposición tan fuerte, veamos que sucede.
### Segundo principio de la termodinámica

En toda transformación irreversible de un sistema aislado, la entropía aumentará.
En las transformaciones reales, que no podemos suponer que mantienen constantemente el equilibrio, *incluso si ocurren en un sistema aislado que no transfiere ni recibe calor ni trabajo* de su entorno, producen un aumento de la entropía del sistema. En particular este principio se relaciona con el hecho observado que mencionamos al principio, que el calor Q fluye de forma natural desde las fuentes térmicas de más temperatura a las de menos, pero al revés no.

Podemos ver una justificación (que  no una demostración) considerando el caso de un gas ideal que evoluciona  de forma irreversible (ver el diagrama PV en la fig. 7) desde el estado A, definido por $(P_A, V_A, T_A)$ hasta el estado B $(P_B, V_B, T_B)$, de más presión temperatura y volumen; para saber el cambio de entropía entre esos dos estados consideramos la transformación alternativa A->B'->B: la primera parte A->B' es reversible adiabática, la segunda parte B'->B es reversible isotérmica. La variación de entropía será
$S_{AB}=S_{AB'}+S_{B'A}=0+\frac Q{T_B}$

pues en una adiabática reversible no varía S. El signo de la ΔS depende pues del calor Q absorbido o emitido en la transformación isoterma B'B; por el 1r principio, Q = W + ΔE = Q, pues ΔE en el gas ideal depende exclusivamente de la temperatura, así pues el signo de Q será igual al del trabajo: positivo si el gas realiza trabajo,

[caption id="attachment_150720" align="alignnone" width="387"]![](/assets/images/irreversible.png) Fig. 7: transformación irreversible y camino reversible alternativo[/caption]

El recorrido completo A-B'-B produce un trabajo W > 0. Por el primer principio, Q = W + ΔE, siendo Q el calor absorbido total, pero sólo en la isoterma, ya que en la adiabática Q = 0,  y ΔE la variación de energía interna total, pero sólo en la adiabática, ya que en los gases perfectos ΔE depende exclusivamente de la temperatura). La variación de entropía total será
$S_{AB}=S_{AB'}+S_{B'A}=0+\frac Q{T_B}$,

ya que A-B' es adiabática reversible, luego $Q_{AB'} = 0$ y no hay variación de entropía.  Para calcular $Q_{B'B}$ aplicamos el 1r principio, Q = W + ΔE, siendo:
$W_{B'A}=\int_{B'}^BP\operatorname dV=nrT\ln\left(\frac{V_B}{V_{B'}}\right)&gt;0$

y ΔE = 0 pues T es constante, luego $Q_{B'B}&gt;0$ y la variación de entropía total S es positiva: aumenta.

El 2º principio afirma que en una transformación irreversible S aumentará incluso si no hay transferencia de calor Q, seria el caso de un proceso adiabático irreversible; llamemos ΔS' a este aumento sin transferencia de calor, si a este proceso la añadiéramos además una transferencia de calor, tendríamos además un ΔS'' debido ese calor Q, por ello, en general podemos decir que el ΔS de toda transformación irreversible puede descomponerse en dos factores:
*ΔS = ΔS' + ΔS'' (entropía intrínseca irreversible + debida a Q)* [10]

*Procesos isoentrópicos* son aquellos procesos en los que la entropía S no varia. S es función de estado, y eso significa que cada estado ha de tener un valor de S fijado, pero al mismo tiempo podemos tener varios estados que tengan la misma entropía; un proceso que se mueva entre esos estados será isoentrópico. Un sistema aislado que se transforma irreversiblemente no puede ser isoentrópico, pero si es reversible seguro que lo será.
### Diagramas TS

Representan los estados y su evolución usando como coordenadas la temperatura y la entropía. En la figura 8 vemos un ciclo de Carnot para un gas perfecto en el diagrama TS, se ven como rectángulos: las líneas horizontales son las isotermas, en las que se transfiere calor y por tanto hay variación de entropía, las líneas verticales son las adiabáticas con Q = 0, la entropía no varía pero la temperatura sí. Como en el diagrama PV, el área interior al ciclo en el TS equivale al valor de trabajo realizado por el ciclo; en efecto, $\operatorname dW=P\operatorname dV$, y además $\operatorname dS=\frac{\operatorname dQ}T\Rightarrow T\operatorname dS=\operatorname dQ=\operatorname dE+\operatorname dW$. Integrando y recordando que la energía interna no varia en un ciclo: $\oint T\operatorname dS=\cancel{\oint\operatorname dE}+\oint\operatorname dW\Rightarrow W=\oint T\operatorname dS$

[caption id="attachment_150742" align="alignnone" width="371"]![](/assets/images/diagrama-TS-Carnot.png) Fig.8: un ciclo de Carnot visto en el diagrama TS[/caption]

 
### Máquina térmica perpetua

Se llama así a una máquina (térmica en estos apuntes) teórica con una eficiencia del 100% de forma que se puede invertir todo el trabajo que genera en producir calor para retroalimentarla y que siga funcionando de forma autónoma y perpetua, o sea que no necesita una fuente térmica externa (fig. 8), tal máquina tendría dos partes, una que se encarga de transformar todo el calor Q en trabajo w, y otra que transforma todo el trabajo W de nuevo en calor Q, sin pérdidas).  Se desarrollaron [diversos intentos de construirla](https://es.wikipedia.org/wiki/M%C3%B3vil_perpetuo#Intentos_de_m%C3%B3vil_perpetuo), todos fallidos.

[caption id="attachment_150726" align="alignnone" width="304"]![](/assets/images/maquina-perpetua.png) Fig.8: esquema de una máquina térmica perpetua, que constituye un sistema aislado que se retroalimenta[/caption]

Veamos que según el 2º principio es imposible tal máquina; en efecto, por ser S una función de estado, su variación es cero en todo ciclo tanto reversible como no reversible, pero una máquina autónoma y perpetua que no interacciona con nada (ni tiene fuentes térmicas ni intercambia trabajo con el exterior) es por definición un sistema aislado, y el 2º principio afirma que todo sistema aislado que evoluciona de forma irreversible ha de aumentar su entropía: llegamos a una contradicción, luego no existe tal máquina térmica perpetua.
### Teorema de Carnot

[caption id="attachment_150727" align="alignleft" width="246"]![](/assets/images/TeoremaCarnot-246x300.png) Fig.9: esquema para demostrar el teorema de Carnot con dos máquinas de Carnot conectadas entre sí[/caption]

Dice así:
el rendimiento de una máquina térmica cualquiera sólo depende de las temperaturas extremas T, T' con las que trabaja.
Equivalentemente, dos máquinas térmicas que trabajen entre las mismas temperaturas extremas tendrán el mismo rendimiento.

Consideremos dos máquinas A y B acopladas que trabajan entre los mismos focos térmicos T > T', en el esquema de la fig. 9 vemos las transferencias de calor y trabajo; el acoplamiento consiste en que el trabajo suministrado por la máquina A se utiliza para hacer funcionar la máquina B, que actúa en modo inverso, o sea como bomba de calor, extrayéndolo del foco frío e inyectándolo en el foco caliente. Ajustemos ambas máquinas de tal forma que $Q_A=Q_B$ y $Q'_A=Q'_B$; esto equivale a modificar sus ciclos hasta que las áreas interiores sean iguales, pues por el 1r principio para cada máquina Q - Q' = W (fig. 10).

[caption id="" align="alignnone" width="634"]![](/assets/images/igual-W.png) Fig.10: dos ciclos entre distintas isotermas y adiabáticas, ajustados para tener la misma área W[/caption]

 

Entonces será W = W', además, $W = Q_A-Q'_A$ y $W'=Q_B-Q'_B$ luego $ Q_A-Q'_A=Q_B-Q'_B$. Recordemos que los rendimientos de las máquinas son $r_A=W/Q_A,r_B=W'/Q_B$ o sea  $r_A=W/Q_A,r_B=W/Q_B$ , y vamos a suponer que A tiene más rendimiento que B, $r_A &gt; r_B$, que implica $W/Q_A&gt;W/Q_B$, que equivale a $Q_A&lt;Q_B$: la máquina A toma menos calor de la fuente caliente que el calor devuelt por B.

[caption id="attachment_150730" align="alignnone" width="300"]![](/assets/images/TeoremaCarnot2-300x238.png) Fig.11: combinación de máquinas térmicas equivalente a una que viola el 2º principio[/caption]

Entonces, podemos prescindir de la fuente térmica T acoplando las máquinas como muestra la figura 11; el conjunto A+B toma un calor $Q'_B-Q'_A$  de un foco T' y devuelve un calor neto $Q_B-Q_A&gt;0$, obviamente este calor podría pasarse a una tercera máquina C que produciria un trabajo neto  W'' con lo cual el sistema completo A+B+C (linea de trazos en la figura 11) produciria un trabajo neto W''' con un único foco térmico: tendríamos una máquina térmica perpetua en contradicción con el 2º principio.

[caption id="attachment_150731" align="alignleft" width="276"]![](/assets/images/TeoremaCarnot3-276x300.png) Fig.12: con rendimentos iguales, la combinación propuesta equivale a una máquina nula que no transfiere calor ni trabajo y por tanto no vulnera ningún principio[/caption]

 

La contradicción se deshace si consideramos que los rendimientos de A y B son iguales, en este caso la máquina A + B simplemente no hace nada (figura 12) pues extrae y devuelve la misma cantidad de calor de los focos T y T' sin aportar nada de trabajo.

 
### Rendimiento de máquinas reales irreversibles

Consideremos de nuevo una máquina térmica M operando entre dos fuentes T > T' pero de forma irreversible; el conjunto máquina + fuentes térmicas será un sistema aislado, con transformaciones internas irreversibles, luego por el 2º principio su entropía $S_{total}$ debe aumentar, y será igual al incremento de entropía de la máquina M más los incrementos de entropía de las fuentes térmicas: $\triangle S_{total}=\triangle S_M+\triangle S_T+\triangle S_{T'}$. Pero la entropía $S_M$ se mantiene constante en toda transformación cíclica, por ser S función de estado, luego $\triangle S_{total}=\triangle S_T+\triangle S_{T'}&gt;0$. Para calcular estas entropías consideremos una cesión de calor muy lenta, infinitesimal, dQ, de cada una de las fuentes; teniendo en cuenta que peramenecen a temperatura constante, y tomando la definición de entropía, obtenemos:
$\operatorname dS_T=\frac{\operatorname dQ}T,\;\operatorname dS_T'=\frac{\operatorname dQ'}{T'}\Rightarrow\triangle S_T=\int\frac{\operatorname dQ}T=\frac QT,\;\triangle S_{T'}=\int\frac{\operatorname dQ'}{T'}=\frac{Q'}{T'}$

luego deducimos que
$\frac QT+\frac{Q'}{T'}&gt;0\Leftrightarrow\left|\frac{\displaystyle Q}{\displaystyle T}\right|\neq\left|\frac{\displaystyle Q'}{\displaystyle T'}\right|$

Comparando con la expresión [3] vemos que en general,
$\frac QT+\frac{Q'}{T'}\geqslant0$

siendo válida la igualdad para procesos reversibles y la desigualdad estricta para los irreversibles. Recordemos ahora la expresión [10] y la aplicamos a un ciclo irreversible; para todo ciclo es *ΔS = 0, *luego*ΔS' + ΔS'' = 0,* siendo ΔS' debida a la irreversibilidad y ΔS'' debida al intercambio de calor Q, esta última será igual a $\frac QT+\frac{Q'}{T'}$, luego:
$\frac QT+\frac{Q'}{T'}+\triangle S''=0$,

despejando Q':
$Q'=-T'\left(\triangle S''+\frac QT\right)$,

como en un ciclo ha de ser W = Q + Q' nos queda:

$W=Q-T'\left(\triangle S''+\frac QT\right)=Q\left(1-\frac{T'}T\right)-T'\triangle S''$,

entonces el rendimiento del ciclo irreversible será R = W/Q:
$R=\left(\frac{T-T'}T\right)-\frac{T'\triangle S''}Q=r-\frac{T'\triangle S''}Q$

donde r es el rendimiento de un ciclo de Carnot (reversible por tanto), vemos que el rendimiento irreversible R es siempre menor que el reversible r: los rendimientos de las máquinas reales son inferiores a los de las máquinas ideales reversibles.
{% endraw %}