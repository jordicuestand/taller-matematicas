---
layout: post
title: "Física -> Mecánica ->Choques: teoria y ejemplos"
date: 2016-04-23 08:45:44 +0000
categories:
  - "Fí­sica"
  - "Mecánica"
tags:
  - "cantidad movimiento"
  - "choque elástico"
  - "choque inelástico"
  - "choques"
  - "energía cinética"
  - "mecánica"
math: true
---
{% raw %}

- [Física](http://tallermatematic.ovh/wp/?page_id=333) -> Mecánica -> Choques: teoria y ejemplos

 	- Relacionado con: [Problemas de Mecánica](http://tallermatematic.ovh/wp/?page_id=337)

### Cantidad de movimiento

![Newtons_cradle_animation_book](/taller-matematicas/assets/images/Newtons_cradle_animation_book.gif) Fig.1: Péndulo de Newton. Fuente: De DemonDeLuxe (Dominique Toussaint) - Trabajo propio, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=1031903
En el [péndulo de Newton](https://es.wikipedia.org/wiki/P%C3%A9ndulo_de_Newton) tenemos un buen ejemplo experimental que nos servirá de punto de partida para entender el concepto de impulso (o cantidad de movimiento) y su aplicación a la Física de los choques. Separamos una de las bolas de su posición inicial, y la dejamos caer, al chocar con las demás, se detiene completamente, y en cambio la última bola de la filera sale despedida, iniciando un ciclo de vaivén. Si separamos dos bolas, entonces se produce el mismo efecto pero con las dos.

Newton definió: "*la cantidad de movimiento es la medida del mismo, surgida de la velocidad y la cantidad de materia conjuntamente; en un cuerpo con cantidad de materia doble e igual velocidad la cantidad de movimiento será doble, y para un cuerpo con el doble de masa y el doble de velocidad, la cantidad será cuádruple*". Matemáticamente esta afirmación significa que la cantidad de movimiento *p* será proporcional al producto de la masa del cuerpo *m*, por su velocidad *v*:

$p=m·v$

Cuando elevamos una de las bolas del péndulo, todas ellas de la misma masa *m*, hasta una altura h y la dejamos caer, la aceleración gravitatoria la acelerará progresivamente, de forma que cuando alcance en su caída las bolas en reposo, tendrá una cierta velocidad *v*, y por tanto tendrá una cantidad de movimiento *p = mv*. Sucede que esta cantidad de movimiento no se pierde en el choque, sino que se transmite:

La cantidad de movimiento no se pierde en los choques

Pasemos ahora a estudiar la Física del choque.

### Física del choque: el choque elástico

En el péndulo de Newton de la ilustración las bolas son metálicas, rígidas, no hay deformación (o es despreciable) de las bolas cuando chocan entre sí. En este caso de rigidez absoluta toda la energía que transporta la bola en movimiento se transmite íntegramente sin pérdidas: decimos que el choque es **perfectamente elástico**. ¿De qué energía estamos hablando? Pues hay muchos tipos de energía: elástica, potencial, elèctrica, térmica ... hablamos de la energía cinética:

$E_c=frac{1}{2}mv^2$

La energía cinética no se pierde en los choques perfectamente elásticos

Cuando la bola que hemos levantado, supongamos la de la izquierda, y dejado caer, choca con la primera bola estática de la hilera su velocidad pasa a ser cero, ya que en el choque elástico hemos dicho que la energía cinética se transfiere íntegramente; usando la conservación de la energía cinética y la de la cantidad de movimiento veremos que esto es así. Supongamos que las velocidades después del choque de las dos bolas son distintas, y planteamos:

 	- Energía cinética bola de la izquierda momento choque = suma de energías cinéticas de las dos bolas después del choque

 	- Cantidad de movimiento bola de la izquierda momento choque = suma de cantidades de movimiento de las dos bolas después del choque

Usando ecuaciones [1]:

$begin{array}{l}mv=mv_1+mv_2\frac12mv^2=frac12mv_1^2+frac12mv_2^2end{array}$

Eliminando los factores comunes las reducimos a:

$begin{array}{l}v=v_1+v_2\v^2=v_1^2+v_2^2end{array}$

Sustituyendo la 1ª ecuación en la segunda y operando:

$left(v_1+v_2right)^2=v_1^2+v_2^2Rightarrow v_1^2+v_2^2+2v_1v_2=v_1^2+v_2^2Rightarrow2v_1v_2=0$

Del último resultado deducimos que al menos una de las dos velocidades ha de ser cero, las dos imposible, pues entonces la energía cinética y la cantidad de movimiento serían también cero. Pero $v_2$ no puede ser cero, pues en ese caso $v_1$ no lo sería, lo cual significa que la bola inicial seguiría moviéndose ... ¡a través de la siguiente, que no se movería! Así pues solo nos queda que $v_1=0, v_2&gt;0$. Además, como $mv=mv_1+mv_2=m·0+mv_2$ entonces ha de ser $v=v_2$: toda la velocidad se transmite a la segunda bola.

Como la segunda bola está en contacto con las otras, no puede moverse libremente; el conjunto de bolas en reposo se comporta como si fueran un único objeto rígido que transfiere la energía hasta la última bola, a la derecha, que sí está libre para moverse, adquiere toda la energía cinética y sale despedida a la misma velocidad $v$ que tenía la primera bola.

### Choque inelástico

Si no tenemos esa rigidez perfecta que mantiene la energía cinética constante, las bolas se deformaran al chocar entre sí, y parte de la energía cinética inicial se disipará; supongamos por ejemplo que tenemos un péndulo de Newton con bolas de goma blanda. ¿Qué parte de la energía cinética se perderá en la deformación de cada bola? Dependerá de la elasticidad del material, por poner un ejemplo supongamos que en la colisión de dos bolas de goma se pierde un 10% de la energía cinética. Además, al chocar las dos bolas, se deforman ambas. Para el caso de sólo dos bolas las ecuaciones [1] teniendo en cuenta la pérdida del 10%+10% de energía son:

$begin{array}{l}mv=mv_1+mv_2\frac12mv^2=frac12mv_1^2+frac12mv_2^2+0.2cdotfrac12mv^2end{array}$

Resolviendo el sistema para $v_2$ resultan dos soluciones posibles:

$v_2=left{begin{array}{l}vleft(frac12+frac{sqrt{15}}{10}right)\vleft(frac12-frac{sqrt{15}}{10}right)end{array}right.$

una es positiva y la otra negativa, indicando movimiento en sentido contrario al original; para $v_1$ se obtienen soluciones simétricas:

$left{begin{array}{l}v_2=vleft(frac12+frac{sqrt{15}}{10}right),;v_1=;vleft(frac12-frac{sqrt{15}}{10}right)\v_2=vleft(frac12-frac{sqrt{15}}{10}right),;;v_1=vleft(frac12+frac{sqrt{15}}{10}right)end{array}right.$

Obviamente la solución aceptable físicamente es $v_1&lt;0$ (retroceso, la bola original rebota a la izquierda) y $v_2&gt;0$ la segunda bola se mueve a la derecha.

El caso extremo es cuando los objetos son capaces de quedar "enganchados" cuando chocan, moviéndose ambos a la misma velocidad; en este caso, denominado choque perfectamente inelástico, las ecuaciones [1] son:

 $begin{array}{l}mv=mv'+mv'\frac12mv^2=frac12mv'^2+frac12mv'^2+triangle Eend{array}$

donde $triangle E$ es la pérdida de energia debido al choque. De la primera ecuación deducimos $v'=v/2$, que al llevarla a la segunda ecuación nos da $frac14mv^2=triangle E$, que es la mitad de la energía cinética inicial, antes del choque, que tenía la bola; esto no es cierto en general: depende de las masas de los cuerpos que chocan.

### Choques en el plano

Hasta ahora las velocidades de los cuerpos que chocan se han considerado que eran en una dimensión, vemos a continuación la Física de los choques de cuerpos que se mueven en dos dimensiones; las velocidades seran ahora vectores en el plano $overrightarrow v$, así como la cantidad de movimiento $overrightarrow p$. Además se presentan complicaciones adicionales: hay que considerar el punto de contacto entre los cuerpos que chocan pues afecta  a la dirección en la que se ven desviados.

![](http://www.educaplus.org/momentolineal/recursos/esquema_choque.png) Fig.2: Choque de dos bolas cuando no estan alineadas por sus centros. Fuente: www.educaplus.org
Al nivel de estos apuntes, no entraremos en detalle en estas desviaciones, seran un dato que nos proporcionan en el problema.

**Ejemplo 1: choque perfectamente elástico de dos bolas de billar**

En el choque elástico de la figura 2 supongamos que *v1*=3m/s, y que después del choque observamos que el ángulo α es de 30 grados; además, la masa de la bola 1 es de 100 gramos, y la masa de la bola 2, 70 gramos. Queremos determinar el resto de parámetros del choque: ángulo β y velocidades *v1f*, *v2f*.  Planteamos las ecuaciones [1] adaptadas a dos dimensiones: según el eje X y según el eje Y:

![xoc en 2D](/taller-matematicas/assets/images/xoc-en-2D.png) Fig.3: Ejes cartesianos en el choque en dos dimensiones
Según el eje X:

$begin{array}{l}m_1v_1=m_1v_{1f}cosleft(alpharight)+m_2v_{2f}cosleft(betaright)\frac12m_1v_1^2=frac12m_1v_{1f}^2+frac12mv_{2f}^2end{array}$

Observemos que la energía cinética no se descompone según los ejes, no es una magnitud vectorial. Añadimos la ecuación que falta, la del eje Y:

$begin{array}{l}begin{array}{l}m_1v_1=m_1v_{1f}cosleft(alpharight)+m_2v_{2f}cosleft(betaright)\frac12m_1v_1^2=frac12m_1v_{1f}^2+frac12mv_{2f}^2end{array}\0=m_1v_{1f}sinleft(alpharight)+m_2v_{2f}sinleft(betaright)end{array}$

En la última ecuación la velocidad inicial es cero porque v1 tenía dirección horizontal, con componente Y nula. Resolvemos este sistema de 3 ecuaciones con las incógnitas v1f, v2f y el ángulo β. Primero sustituimos valores:

$begin{array}{l}begin{array}{l}0.1cdot3=0.1cdot v_{1f}cosleft(30right)+0.07cdot v_{2f}cosleft(betaright)\frac120.1cdot3^2=frac120.1cdot v_{1f}^2+frac120.07cdot v_{2f}^2end{array}\0=0.1cdot v_{1f}sinleft(30right)+0.07cdot v_{2f}sinleft(betaright)end{array}$

Calculamos:

$begin{array}{l}begin{array}{l}0.3=0.1cdot v_{1f}frac{sqrt3}2+0.07cdot v_{2f}cosleft(betaright)\frac9{20}=frac1{20}v_{1f}^2+frac7{200}v_{2f}^2end{array}\0=frac{10}{20}cdot v_{1f}+frac7{200}cdot v_{2f}sinleft(betaright)end{array}$

No es un sistema inmediato de resolver, es no lineal de tres incógnitas, una de ellas la β viene dada de forma indirecta por las funciones seno y coseno; en los ejercicios elementales de choques suelen darse simplificaciones adicionales, por ejemplo se suponen las masas iguales y/o se da la velocidad final de una de las bolas. Supongamos que sabemos que la velocidad final de la bola 1 es v1f = 1.9 m/s. Entonces:

$begin{array}{l}begin{array}{l}0.3=0.1cdot1.9frac{sqrt3}2+0.07cdot v_{2f}cosleft(betaright)\frac9{20}=frac1{20}1.9^2+frac7{200}v_{2f}^2end{array}\0=frac{10}{20}cdot1.9+frac7{200}cdot v_{2f}sinleft(betaright)end{array}$

De la segunda ecuación encontramos $frac9{20}=frac1{20}1.9^2+frac7{200}v_{2f}^2Rightarrow v_{2f}^{}=sqrt{left(frac9{20}-frac{1.9^2}{20}right)frac{200}7}=frac{sqrt{770}}{10}approx2.8$.

Para encontrar la β tenemos dos ecuaciones, lo más exacto será combinarlas: de una encontramos $frac{-190}{196}=sinleft(betaright)$, de la otra resulta $frac{0.3-0.1cdot1.9frac{sqrt3}2}{0.07cdot2.8}=cosleft(betaright)=0.69$, dividimos las dos para obtener $tanleft(betaright)=frac{sinleft(betaright)}{cosleft(betaright)}=frac{-190}{196}div0.69=-1.4Rightarrowbeta=tan^{-1}left(-1.4right)=-54^o$.

**Ejemplo 2: Péndulo balístico**

![De Algarabia - Trabajo propio, Dominio público, https://commons.wikimedia.org/w/index.php?curid=7705870](/taller-matematicas/assets/images/pendulo_balistico.jpg) Fig. 4: Péndulo balístico. Fuente: De Algarabia - Trabajo propio, Dominio público,https://commons.wikimedia.org/w/index.php?curid=7705870
Un proyectil de masa *m* se incrusta a una velocidad *v* en un bloque de masa *M* que se mantiene colgado por dos hilos de longitud l; supondremos que el tiempo que tarda en penetrar en el bloque es muy corto, tanto que no da tiempo a que el bloque oscile mientras el proyectil penetra.

Este es un ejemplo típico de choque inelástico, pues los objetos que chocan no se consideran perfectamente rígidos, no hay un rebote perfecto, al contrario, el bloque es penetrado por el proyectil. Pero aún se conserva la cantidad de movimiento; llamemos v' a la velocidad del bloque (que contiene dentro el proyectil) inmediatamente después del impacto, entonces: $mv=(m+M)v'$, de donde $v'=vm/(m+M)$.

¿Cuánta energía se ha perdido en el choque inelástico? La diferencia de energía cinética:

$begin{array}{l}triangle E=frac12left(m+Mright)v'^2-frac12mv^2=frac12left(m+Mright)left(frac{vm}{(m+M)}right)^2-frac12mv^2=\frac12mv^2left[frac m{(m+M)}-1right]end{array}$

Si nos preguntan a que altura máxima llegará el bloque después del impacto, es fácil contestar usando la conservación de la energía mecánica (cinética + potencial gravitatoria):

$frac12mv^2=left(m+Mright)ghRightarrow h=frac{mv^2}{2left(m+Mright)g}$

Veamos un ejemplo concreto: tenemos un proyectil de 50gr a una velocidad de 500km/h que se incrusta en un bloque de madera de 10kg; después del impacto la velocidad del bloque será $v'=500·0,05/(0.05+10)=2.5$ km/h, equivalente a 0.7 m/s, la pérdida de energía será

$0.05frac{139^2}2left(frac{0.05^{}}{(0.05+10)}-1right)=-481J$

### Centro de masas, segunda ley de Newton y conservación de la cantidad de movimiento

Para entender mejor el principio de conservación de la cantidad de movimiento en los choques es muy útil el concepto de [centro de masas](https://es.wikipedia.org/wiki/Centro_de_masas).

![Centro de masas de dos objetos](/taller-matematicas/assets/images/centre_mases.png) Fig. 5: Centro de masas de dos objetos
 Si tenemos dos objetos en el plano con masas *m* y *M*, su **centro de masas** CM es un "punto virtual" situado entre ambos con masa *m + M* y coordenadas

$x_{cm}=frac{mx_m+Mx_M}{m+M},;y_{cm}=frac{my_m+My_M}{m+M}$

Supongamos que los dos objetos de la figura 5 se están moviendo con velocidades distintas $v_m, v_M$, incluso chocando uno contra el otro y cambiando de velocidades; ¿cómo se moverá su centro de masas? Por la segunda ley de Newton, la velocidad del CM ha de ser constante: la misma en todo instante, incluso si chocan ambos objetos, ya que no hay fuerzas exteriores actuando. Supongamos que en un momento dado las velocidades son constantes e iguales a $v_m, v_M$, entonces la velocidad según X del CM es:

$begin{array}{l}v_{xCM}=frac{triangle x_{CM}}{triangle t}=frac1{triangle t}triangleleft(frac{mx_m+Mx_M}{m+M}right)=frac1{triangle t}frac{mtriangle x_m+Mtriangle x_M}{m+M}=frac{mtriangle x_m/triangle t+Mtriangle x_M/triangle t}{m+M}=\frac{mv_{xm}+Mv_{xM}}{m+M}end{array}$

que seguirá siendo la misma incluso si ambos cuerpos chocan;  la expresión de la velocidad según Y es similar. En lo que sigue pensaremos en un choque en una dimensión. Supongamos que chocan de forma inelástica, quedando "enganchados" y moviéndose a la misma velocidad *V*. Como ahora los objetos están unidos, el centro de masas coincide con ellos (suponemos que los objetos son puntuales); en efecto, si después del choque llamamos x a la posición conjunta de los dos objetos enganchados, y calculamos la posición del CM:

$x_{CM}=frac{mx_m+Mx_M}{m+M}=frac{mx+Mx}{m+M}=frac{xleft(m+Mright)}{m+M}=x$

La velocidad del centro de masas después del choque será (m + M)V, pero el centro de masas se mueve a velocidad constante, así que:

$frac{mv_m+Mv_M}{m+M}=VRightarrowboxed{mv_m+Mv_M=left(m+Mright)V}$

que es la ley de conservación de la cantidad de movimiento en el choque inelástico, que hemos deducido de la 2a ley de Newton usando el concepto de centro de masas.

Si el choque es elástico, usando la constancia de la velocidad del CM llegamos también a la ley de conservación de la cantidad de movimiento:

$V_{CM}=frac{mv_{1m}+Mv_{1M}}{m+M}=frac{mv_{2m}+Mv_{2M}}{m+M}Rightarrowboxed{mv_{1m}+Mv_{1M}=mv_{2m}+Mv_{2M}}$

### ¿La cantidad de movimiento se conserva en todos los choques?

Pues depende: hemos visto que sí siempre que no actúen fuerzas exteriores a los objetos que chocan. Cuando consideramos que los choques son tan rápidos que prácticamente son instantáneos, incluso habiendo fuerzas exteriores actuando, como por ejemplo rozamientos, se seguirá cumpliendo el principio de conservación, pues en un tiempo virtualmente igual a cero "no da tiempo" a que las fuerzas exteriores tengan ningún efecto. En cambio si consideramos que el choque es rápido  pero no instantáneo, y además hay fuerzas externas actuando, entonces no se conservará la cantidad de movimiento.

**Ejemplo 3: choque inelástico no instantáneo.**

![Choque entre dos vehículos](/taller-matematicas/assets/images/xoc_vehicles-300x111.png) Fig. 6: Choque entre dos vehículos
Este ejemplo está basado en un caso real, encontrado como consulta en un foro de tráfico. Una furgoneta de reparto, de masa 2000Kg, está parada en un semáforo cuando es embestida por detrás por un coche de masa 900Kg moviéndose a una velocidad v = 30m/s.  En el choque la carrocería del coche se deforma, y como reacción acelera a la furgoneta durante 5 centésimas de segundo, después de ese tiempo los dos vehículos quedan unidos moviéndose a la misma velocidad. La furgoneta vió como se acercaba por detrás el coche, así que pisó a fondo los frenos para evitar en lo posible el pasar el semáforo en rojo, como consecuencia del empujón recibido, y quizá provocar otro accidente en cadena. El coeficiente de fricción entre los neumáticos del camión y el asfalto es de $mu=0.6$. Queremos saber cuantos metros más allá del semáforo en rojo recorrerán los vehículos, así como si se conserva la cantidad de movimiento en este choque.

Solución:  Si la cantidad de movimiento se conservara, seria fácil encontrar la velocidad inmediatamente después del choque:

$mv+Mcdot0=left(m+Mright)v_fRightarrow v_f=vfrac m{m+M}=30frac{900}{2900}=9.3;m/s$

La energía cinética perdida en el choque inelástico sería:

$triangle E_c=frac12left(M+mright)v_f^2-frac12mv^2=frac122900cdot9.3^2-frac12900cdot30^2=-279310;J$

Pero el choque no es instantáneo, hay un tiempo de aceleración de 0.05s, durante el cual hay una fuerza constante de rozamiento actuando, que vale $F_r=mu Mg=0.6cdot2000cdot9.8=11760N$; esta fuerza produce una aceleración negativa de $a_r=F_r/(M+m)=mu Mg/(M+m)=0.6cdot9.8cdot2000/2900;=;4.1m/s^2$, observad que la fuerza se aplica al conjunto furgoneta + coche, pues ya están en contacto. Es una buena aproximación considerar que hay dos aceleraciones independientes actuando: la que el coche proporciona a la furgoneta, y la que el rozamiento resta. La primera la calculamos a partir de la velocidad final después del choque inelástico sin rozamiento: a = v / t = 9.3 / 0.05 = 186 m/s²; la aceleración neta resultante será a = 186- 4.1 = 181.9 m/s², y la velocidad después del choque será v = at = 181.9·0.05 = 9.1 m/s. Vemos que hay una pequeña diferencia de velocidad después del choque de sólo 9.3 - 9.1 = 0.2 m/s si consideramos el rozamiento, esto es, un 0.2·100/9.3 = 2.2% de diferencia relativa. La pérdida de cantidad de movimiento en este choque es $triangle p=2900cdot9.1;-900cdot30;=;-610$, en términos relativos también representa un 2.2% de pérdida.

Es pues una buena aproximación, en la mayoría de casos reales, considerar que el choque es instantáneo y la cantidad de movimiento se conserva.

La distancia recorrida después del choque por la furgoneta y el coche podemos encontrarla por cinemática, pues es un movimiento uniformemente decelerado; la aceleración es la causada per la fuerza de rozamiento, y detiene el conjunto que iba a una velocidad inicial de 9.3 m/s en un tiempo t: $v=v_0+atRightarrow t=left(v-v_0right)/a=left(0-9.3right)/(-11760/2900)=2.3s$. Con este tiempo, encontramos la distancia recorrida:

$x=v_0t+frac12at^2=9.3cdot2.3-0.5cdotleft(11760/2900right)cdot2.3^2=10.7m$

### Percusiones en cuerpos rígidos, rotaciones

Cuando aplicamos una fuerza F en un punto durante un tiempo suficientemente corto para despreciar el desplazamiento del punto decimos que hemos aplicado una **percusión** al punto. Al producto de la fuerza por el intervalo de tiempo se le denomina impulso de la percusión, y lo denotamos con la letra P mayúscula: $P=Ftriangle t$.

Dado que $F=ma$, se sigue que $P=matriangle t=mtriangle v=triangle p$ (estamos suponiendo que la masa es constante), así que el impulso aplicado a un punto de masa *m* es igual al incremento de su cantidad de movimiento.

Si aplicamos una percusión a un cuerpo rígido que no sea un punto, sino que tenga una extensión, por lo general produciremos no sólo un desplazamiento del cuerpo, sino también una rotación.

Consideraremos para este estudio un ejemplo:

**Ejemplo 4**: **bola de billar golpeada con un taco** (fig. 7).

![Bola de billar golpeada en un punto con un taco](/taller-matematicas/assets/images/percusio.png) Fig. 7: Bola de billar golpeada en un punto con un taco
Supondremos que le aplicamos un impulso P en un punto situado una altura h por encima del centro de la bola, que por ser homogénea, será también su centro de masas CM. El radio de la bola será R, y el punto de contacto con la mesa es O.

 
Al golpear la bola siguiendo una línea que no pasa por el CM, estamos aplicando un [momento de fuerza](https://es.wikipedia.org/wiki/Momento_de_fuerza) M a la bola respecto de su centro, de valor $M=F·h$; el valor de la fuerza será $F=P/triangle t$. Como reacción (ley de acción-reacción de Newton) a esta fuerza, aparecerá una fuerza de rozamiento $F_r$ del suelo sobre la bola aplicada en el punto O, que no estudiaremos en detalle; si comentaremos que supondremos que $F=F_r$ con lo cual la resultante de las fuerzas será nula y no tendremos desplazamiento horizontal, que en el caso de la bola significa que ésta no deslizará, sino que rodará sin deslizamiento. Nos proponemos calcular la velocidad angular de rotación de la bola a partir del impulso P, de la masa m de la bola y de la geometría del problema. Para ello hacemos un repaso rápido de dinámica de rotaciones.

**Dinámica de rotaciones**

Tenemos las siguientes "equivalencias" entre magnitudes dinámicas del movimiento lineal y del circular:

| **Movimiento lineal** 
| **Movimiento circular** 

| Fuerza, masa, aceleración: $F=ma$ 
| Momento, momento de inercia, aceleración angular: $M=Ialpha$ 

| Cantidad de movimiento, masa, velocidad: $p=mv$ 
| Momento cinético, momento de inercia, velocidad angular: $L=Iomega$ 

| Energía cinética lineal, masa, velocidad: $E_c=0.5mv^2$ 
| Energía cinética angular, momento de inercia, velocidad angular, masa: $E_c=0.5Iomega^2$ 

| Velocidad, aceleración, tiempo. $v=at$ 
| Velocidad angular, aceleración angular, tiempo. $omega=alphat$ 

 

Volvamos a la bola de billar: al aplicar la percusión $P=Ftriangle t$ generamos un momento M que verifica $triangle L=M·triangle t$, pero $L=Iomega$, así que $triangle L=I·triangle omega$, y como la velocidad de rotación inicial era cero, resulta que

$omega=frac{triangle L}I=frac{ph}I$

El momento de inercia I de una esfera de radio R y masa m respecto a su centro es $I=frac25·m.R^2$, así que la velocidad de rotación de la bola de billar es:

$omega=frac{ph}{frac25mR^2}=frac52frac{ph}{mR^2}$

Tomemos los siguientes **datos**: radio de la bola R = 0.1m, masa = 0.1 Kg, h=0.05m, fuerza aplicada F=10N, tiempo de percusión t=0.05s. Sustituyendo:

$omega=frac52frac{10cdot0.05cdot0.05}{0.1cdot0.1^2}=62.5;rad/s$
{% endraw %}