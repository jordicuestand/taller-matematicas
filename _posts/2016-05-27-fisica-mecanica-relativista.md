---
layout: post
title: "Física -> Mecánica relativista"
date: 2016-05-27 10:58:21 +0000
categories:
  - "Fí­sica"
  - "Mecánica"
  - "Mecánica relativista"
tags:
  - "Relatividad especial"
  - "sistemas inerciales"
  - "velocidad límite"
math: true
---
{% raw %}

En este artículo nos introducimos en la **cinemática y dinámica relativistas** a partir de ejemplos, buscando la máxima comprensión en detrimento del rigor, para exposiciones rigurosas podemos acudir a la bibliografía.

### La relación entre masa y energía, $E=mc^2$

Según la mecánica cuántica, un fotón de frecuencia *f* tiene una energía asociada $E=hf$, donde *h* es la [constante de Planck](https://es.wikipedia.org/wiki/Constante_de_Planck); por otro lado, De Broglie propuso que toda partícula de masa *m* en movimiento con velocidad *v*, y cantidad de movimiento $p=mv$, tenía asociada una "onda de materia" de longitud de onda $\lambda=\frac hp$ ([dualidad onda-partícula](https://es.wikipedia.org/wiki/Dualidad_onda_corp%C3%BAsculo)). Teniendo en cuenta que la relación entre longitud de onda, frecuencia y velocidad de la luz es $\lambda f=c$, operamos y obtenemos $E=hf=h\frac c\lambda=h\frac c{h/p}=cp$.

Entonces un haz de luz conteniendo un número muy elevado de fotones transportará una cantidad de movimiento $p=E/C$, donde E es la energía del haz; incluso sin tener masa, pues la luz es inmaterial, posee una cantidad de movimiento, por lo que cuando "choque" (más usualmente se dice que incide sobre ...) con un objeto material, por la ley de la conservación de movimiento, transferirá una parte de p al cuerpo material, de la misma forma que cuando chocan dos cuerpos materiales. es la denominada "[presión de radiación](https://es.wikipedia.org/wiki/Presi%C3%B3n_de_radiaci%C3%B3n)". Todo esto es consecuencia de la Física cuántica básica, desarrollada a principios del siglo XX. En vez de luz, podemos llegar a la misma conclusión pensando en cualquier [radiación](https://es.wikipedia.org/wiki/Radiaci%C3%B3n). Dado que la radiación, en sí inmaterial (caso de la radiación electromagnética) es emitida y absorbida por la materia, nos encontramos que materia y energía radiante pueden "chocar" e intercambiar energía.

**Ejemplo 1**: Emisión de radiación dentro de una caja aislada.


Imaginemos una caja aislada, en reposo, de masa M, dentro de la cual hemos hecho el vacío, que contiene un material radiactivo (fig.1, parte superior); en un momento dado (t = 0) el material emite una haz de radiación de energía E, el cual viaja por el interior de la caja hasta llegar al otro extremo donde es reabsorbida por la pared de la caja. Al emitirse la radiación, se genera una cantidad de movimiento $p=E/c$; siendo el sistema aislado, la cantidad de movimiento total se conserva, así que la caja deberá adquirir una cantidad de movimiento igual e opuesta $-p=-E/c$, pero para la caja $p=Mv$ luego $-E/c=mv\Rightarrow v=-\fracE{mc}$, la caja retrocede con esta velocidad. Despues de un tiempo *t*, se habrá desplazado una distancia $x=vt=\frac E{mc}t$.

Cuando la radiación alcance el otro extremo, habrá transcurrido un tiempo que será, aproximadamente, $t=L/c$; estamos suponiendo que $x&lt;&lt;L$ pues de hecho la radiación ha de recorrer la distancia $L-x$. Entonces tenemos que el desplazamiento *x* es igual a $x=\frac E{mc}t\approx\frac E{mc}\frac Lc=\frac{EL}{mc^2}$ [1], que efectivamente ha de ser despreciable respecto a L pues tenemos el valor *c*² en el denominador, siendo *c* = 3·10⁹ m/s.

Pero observando el sistema "desde fuera", está aislado, no actúa nada sobre él, así que no si fuerzas que actúen no puede moverse en absoluto ... *x* debería ser exactamente cero,  ¿tenemos una contradicción?  Afinando un poco más el argumento, lo que no puede moverse en un sistema aislado es su centro de masas; la caja de masa *M* se ha movido una distancia *x* a la izquierda, pero al mismo tiempo se ha emitido una masa *m* (la masa asociada a la radiación) a la derecha una distancia aproximadamente igual a L. Para que el centro de gravedad del sistema caja-radiación no se mueva, ha de cumplirse $mL=Mx$, sustituyendo el valor del desplazamiento x obtenemos:

$mL=Mx\Leftrightarrow mL=M\frac{EL}{Mc^2}=\frac{EL}{c^2}\Leftrightarrow\boxed{E=mc^2}$ [2]

Hemos obtenido la famosa ecuación de Einstein que relaciona masa con energía, en este caso relaciona la masa *m* inercial de la radiación con su energía, pues masa material hemos supuesto que no tiene. También se puede ver como la afirmación de que toda energía radiante lleva asociada una masa inercial.

### Energía cinética relativista

Si [2] implica que toda energía radiante tiene una masa inercial asociada, nos podemos preguntar si, dado un cuerpo material de masa en reposo *M*, al comunicarle energía cinética al cuerpo, podemos asociarle a esa energía cinética una masa inercial *m*, con lo cual la masa total del cuerpo en movimiento será $M + m$, habrá aumentado. Dado que hemos visto que la materia y la energía radiante pueden "chocar" e intercambiar energía y momento, esta suposición de asignar masa inercial a la energía ya no radiante sino cinética parece fundamentada.

De la dinámica clásica sabemos que el incremento de energía cinética $\triangle E$ al trabajo producido: $\triangle E=F\cdot x=W$, para el caso de masa variable, la expresión a usar para la fuerza es $F=\frac{\operatorname dp}{\operatorname dt}$. Tomando una fuerza *F* que actúa en un pequeño intervalo *dx*, obtenemos $\operatorname dE=\operatorname dW=\frac{\operatorname dp}{\operatorname dt}\operatorname dx=\operatorname dp\frac{\operatorname dx}{\operatorname dt}=vc\dot\operatorname dp$ [3].

Por otro lado, en Física clásica no relativista la cantidad de movimiento es $p=mv$, luego la masa cumple $m=p/v$. Si sustituimos esta masa en la expresión [2] obtenemos $E=mc^2=\frac pvc^2$ [4].

Multipliquemos las ecuaciones [3] y [4]:

 $E\operatorname dE=c^2p\operatorname dp$

integrando llegamos a $E^2=c^2p^2+E_0^2$. Pero usando [4] resulta que $cp=Ev/c$, sustituyendo:

$E^2=\left(\frac{Ev}c\right)^2+E_0^2\Leftrightarrow E^2\left(1-\frac{v^2}{c^2}\right)=E_0^2\Leftrightarrow\boxed{E=\frac{E_0}{sqrt{1-\frac{v^2}{c^2}}}}$ [5]

que es la expresión de la energía total de un cuerpo en movimiento, siendo $E_0$ la energía en reposo, cuando *v* = 0.

### Masa relativista

Suponiendo que la ecuación E=mc² nos da la energía total de la partícula tanto si está en reposo como si está en movimiento, el incremento de energía ha de ser debido al incremento relativista de la masa inercial $\triangle E=\triangle\left(mc^2\right)=c^2\triangle\left(m\right)$, pues c es una constante; entonces:

$mc^2=\frac{m_0c^2}{\sqrt{1-\frac{v^2}{c^2}}}\Leftrightarrow m=\frac{m_0}{\sqrt{1-\frac{v^2}{c^2}}}$ [6]

expresión que nos permite calcular la masa inercial total de un cuerpo en movimiento.

### Velocidad límite

Si en la expresión de la energía [5], o equivalentemente, en el de la masa [6], hacemos que la velocidad del cuerpo se acerce a la velocidad de la luz c, obtenemos valores infinitos:

$\underset{v\rightarrow c}{\lim}m=\underset{v\rightarrow c}{\lim}\frac{m_0}{\sqrt{1-\frac{v^2}{c^2}}}=\frac{m_0}{\sqrt{1-1}}=+\infty$

Con una masa inercial tendiendo a infinita, la fuerza necesaria para acelerarla tenderá también a infinito, sin llegar nunca al límite *v = c*. Por tanto los desarrollos anteriores nos llevan a afirmar que *c* es el límite superior absoluto de la velocidad, no superable por nada, y sólo alcanzable por la energía con masa "material" en reposo nula.

### Transformación de velocidades entre sistemas de referencia


En la figura tenemos el conocido esquema que muestra dos sistemas de referencia inerciales: el *LAB* que representa el del laboratorio, que suponemos estático, y el *Ref*, con una velocidad u relativa al laboratorio. Hay un móvil en la posición *x'* que se mueve con una velocidad *v'* respecto a *Ref*. En la referencia *LAB* la posición es *x* y la velocidad *v*. En estas condiciones se cumple:

$v=\frac{v'+u}{1+v'u/c^2}; v'=\frac{v-u}{1-vu/c^2}$

Al usar estas fórmulas han de tenerse en cuenta los signos de *v, v', u* a partir de la representación de la figura.

**Ejemplo: **dos cuerpos se acercan el uno al otro con una velocidad relativa entre ellos de 0.89c. Un observador exterior los ve moverse uno hacia el otro a la misma velocidad; hallar esta velocidad.


En la figura representamos la situación: desde el punto de vista del laboratorio estático los dos móviles se mueven a la misma velocidad u, desde el punto de vista de uno de los móviles (referencia *Ref*) el otro móvil se acerca a una velocidad 0.89c.  Comparando este esquema con el de transformación de velocidades, identificamos variables: *u*: velocidad en la ref. *LAB* de la referencia Ref (el móvil de la izquierda), *v*: velocidad del móvil de la derecha respecto a *LAB*, que cumple v = -u, *v'*: velocidad del móvil de la derecha respecto a *Ref* (móvil de la izquierda) que cumple $v'=-0.89c$. Aplicamos la ley de transformación de velocidades para obtener *u, *y operamos:

$-0.89c=\frac{-u-u}{1-{\displaystyle\frac{-u-u}{c^2}}}=\frac{-2u}{c^2+u^2}c^2\Rightarrow-0.89u^2+2cu-0.89c^2=0\Rightarrow\\u=\frac{-1\pm\sqrt{1-0.89^2}}{-0.89}c=\left\{\begin{array}{l}\boxed{0.61c}\\12.88c\end{array}\right.$

De las dos soluciones descartamos la que da un resultado mayor que c por imposible físicamente, nos queda: $u\approx0.61c$.

Como comprobación, si encontramos la velocidad relativa v'  a una referencia que se mueve a velocidad u=0.61c, sabiendo que el móbil se mueve a velocidad v=-0.61c respecto del sistema LAB, encontramos:

$v'=\frac{0.61c-(-0.61c)}{1-0.61c\cdot(-0.61c)/c^2}=\frac{2\cdot0.61c}{1+0.61^2}=0.89c$

que es la velocidad dada en el enunciado.
{% endraw %}