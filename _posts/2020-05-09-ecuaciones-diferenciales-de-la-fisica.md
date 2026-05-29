---
layout: post
title: "Ecuaciones Diferenciales de la Física"
date: 2020-05-09 12:40:33 +0000
categories:
  - "Fí­sica"
  - "Matemáticas"
tags:
  - "campo conservativo"
  - "campo escalar"
  - "campo vectorial"
  - "circulación de un vector"
  - "divergencia"
  - "flujo de un vector"
  - "gradiente"
  - "potencial escalar"
  - "potencial vector"
  - "rotacional"
  - "Teorema de Gauss"
  - "Teorema de Stokes"
math: true
---
{% raw %}

"Las ecuaciones diferenciales son la única forma de presentar las leyes de la Física de forma precisa" - R. Feynman. 

"Entender una ecuación diferencial de la Física es saber repersentar las propiedades de sus soluciones sin necesidad de resolver la ecuación" - Paul A. Dirac.

## Contenidos

- Campos y operadores diferenciales
- Flujo de un campo vectorial. Teorema de Gauss
- Circulación de un vector, teorema de Stokes
- Campos conservativos y potenciales escalares
- Potencial vector
- Ejemplos: Trabajo de una fuerza, campo electrostático, potencial vector electromagnético, Ecuación diferencial de la hidrostática

Los fenómenos naturales más interesantes implican relaciones dinámicas entre magnitudes físicas variables y se expresan mejor con relaciones entre variaciones de esas variables, esto es, con ecuaciones expresan diferencias y relaciones entre esas diferencias: son las ecuaciones diferenciales. Por ejemplo la 2a ley de Newton de la dinámica se expresa en forma de ecuación diferencial como $\overrightarrow F=\frac{\operatorname d\overrightarrow p}{\operatorname dt}$ siendo p el vector impulso, la forma más familiar F = ma es una solución particular de la ecuación diferencial con la condición de que la masa sea constante (en el típico problema del cohete acelerando la masa es variable pues el cohete va quemando combustible).

En las ecuaciones de la Física se manejan frecuentemente variaciones "pequeñas" y variaciones infinitesimales; por ejemplo la variación de la temperatura *T* de un cuerpo con respecto al tiempo es proporcional a la diferencia (T - A) donde *A* es la temperatura del medio ambiente ([ley de enfriamiento de Newton](http://es.wikipedia.org/wiki/Enfriamiento_newtoniano)), para pequeñas variaciones escribimos $\frac{\triangle T}{\triangle t}=k\left(T-A\right)$, interpretando el símbolo $\frac{\triangle}$ como variación (pequeña) de la temperatura; en realidad tal símbolo representa una variación cualquiera de una magnitud, pero en las ecuaciones de la Física lo más frecuente es que represente una variación "pequeña" pues para variaciones grandes muchas veces la ley deja de cumplirse, como es el caso de la ley de enfriamiento de Newton.  En cálculo diferencial se usa la operación "paso al límite" de las diferencias para convertirlas en "infinitesimales", que deben entenderse como un paso al límite:

$\lim_{\triangle t\rightarrow0}\frac{\triangle T}{\triangle t}=\frac{\operatorname dT}{\operatorname dt}$

Para terminar con esta introducción, especifiquemos que se entiende por variación "pequeña": dependerá de la situación en estudio, pero en general será aquella que permita que las hipótesis que realizamos se cumplan. Por ejemplo en el problema del cohete acelerando, si la masa inicial del cohete es de 10⁴kg, el consumo de combustible es de 6kg por hora, y nos preguntamos por la aceleración durante los primeros10 segundos, se consumirán 0.6kg de combustible y la masa del cohete descenderá un 0.006%, podemos considerar como buena aproximación que la masa total se mantiene constante y aplicar la ecuación *F = ma*.

## Campos y operadores diferenciales

Un **campo escalar** es una función *f(x,y,z)* que asigna un número real (un *escalar*) a cada punto del espacio o de una región del espacio. Por ejemplo la temperatura T de una sala con calefacción por radiadores tendrá una temperatura ligeramente variable según el punto en que la midamos, más caliente cerca de los radiadores, y la representamos por el campo escalar *T(x,y,z)*. En los mapas meteorológicos, las *líneas isobaras* representan los puntos que están a la misma presión atmosférica P, que también constituye un campo escalar *P(x,y,z)*, y las *líneas isotermas* representan los puntos de la misma temperatura. En general dado un campo escalar C(x,y,z) las líneas que pasan por los puntos con la misma magnitud C se denominan *curvas de nivel*. Si "andamos" por encima de una curva de nivel L cualquiera, la magnitud C se mantiene constante, su variación es cero: $\triangle C_L=0$, por el contrario si nos alejamos de una curva de nivel perpendicularmente a ella, la variación de la magnitud C será la máxima posible siempre que el desplazamiento sea pequeño, pues para mantener la variación máxima deberíamos movernos por una trayectoria $\Gamma$ tal que fuera perpendicular en cada uno de sus puntos a la curva de nivel en ese punto. No nos detendremos en las demostraciones matemáticas de estas propiedades ni de otras que saldrán a menos que nos aporten comprensión física de las leyes. En la figura 1 simplificamos el modelo pasando de tres a dos dimensiones, z = f(x,y): vemos tres curvas de nivel en el plano (x,y) correspondientes a tres valores distintos de z, tenemos también tres movimientos entre curvas de nivel, la que proporciona mayor variación con menor desplazamiento es la trayectoria C perpendicular a la curva de nivel. 

![](/taller-matematicas/assets/images/gradient.png)Fig. 1: curvas de nivel en el plano (X,Y) correspondientes a tres valores de Z=f(X,Y); el movimiento A mantiene el valor de la función Z pues se mueve por encima de una curva de nivel, el movimiento B introduce una variación de una unidad pues pasa de la curva de nivel Z=2 a la Z=3, finalmente el movimiento C al ser perpendicular a la curva de nivel será la distancia más corta entre las curvas consecutivas, y por tanto la que aporta más variación de Z con mínimo desplazamiento.

Pasando al límite de desplazamiento infinitesimal, la ratio entre variación del campo C(x,y,z) y la de variación de la posición coincide por definición con la de derivadas parciales del campo escalar C:

$\lim_{\triangle x\rightarrow0}\frac{\triangle C}{\triangle x}=\frac{\partial C}{\partial x},\;\lim_{\triangle y\rightarrow0}\frac{\triangle C}{\triangle y}=\frac{\partial C}{\partial y},\;\lim_{\triangle z\rightarrow0}\frac{\triangle C}{\triangle z}=\frac{\partial C}{\partial z}$

Si agrupamos las tres derivadas parciales como si fueran un vector (cualquiera tres cantidades puestas en línea como si fueran un vector en general no lo serán, deben de transformarse adecuadamente bajo cambios de coordenadas, ver [Vectores en Física](http://tallermatematic.ovh/wp/2016/08/11/vectores/)) obtenemos el denominado **gradiente del campo escalar**:

$Grad\;C=\left(\frac{\partial C}{\partial x},\frac{\partial C}{\partial y},\frac{\partial C}{\partial z}\right)$ [1]

que resulta que sí es un vector "de verdad": el **vector gradiente**. Resulta que para un pequeño desplazamiento $\left(\triangle x,\triangle y,\triangle z\right)$ la variación de C es igual, aproximadamente, a 

$\frac{\partial C}{\partial x}\triangle x+\frac{\partial C}{\partial y}\triangle y+\frac{\partial C}{\partial z}\triangle z=\overrightarrow{Grad}(C)\cdot\overrightarrow r$

que es el producto escalar del vector gradiente por el vector desplazamiento; si este último es paralelo al gradiente, el producto escalar toma su valor máximo, y si es perpendicular, vale cero, en correspondencia a lo que hemos dicho de los movimientos siguiendo lineas de nivel: "el vector gradiente del campo C en cada punto es paralelo a la línea de nivel por ese punto".

Dado que la operación "derivada parcial del campo" es una operación lineal (la derivada de la suma de campos es la suma de derivadas) se puede definir un operador diferencial lineal, el operador gradiente, como sigue:

$\nabla C=\overrightarrow{Grad}(C)=\left(\frac{\partial C}{\partial x},\frac{\partial C}{\partial y},\frac{\partial C}{\partial z}\right)$

válido para cualquier campo escalar C; podemos incluso obviar ese campo cualquiera C y "desnudar" el operador gradiente:

$\nabla=\overrightarrow{Grad}=\left(\frac\partial{\partial x},\frac\partial{\partial y},\frac\partial{\partial z}\right)$

Entendiendo que ese operador no es un vector, sino que al operar sobre  un campo escalar cualquiera nos resulta un vector, el vector gradiente de ese campo. Aunque el operador no sea un vector, podemos realizar operaciones vectoriales con él como si lo fuera, por ejemplo, el producto escalar de dos gradientes:

$\nabla\cdot\nabla=\overrightarrow{Grad}\cdot\overrightarrow{Grad}=\left(\frac\partial{\partial x},\frac\partial{\partial y},\frac\partial{\partial z}\right)\cdot\left(\frac\partial{\partial x},\frac\partial{\partial y},\frac\partial{\partial z}\right)=\frac{\partial^2}{\partial x^2}+\frac{\partial^2}{\partial y^2}+\frac{\partial^2}{\partial z^2}$

resulta como era de esperar un operador escalar que además es muy importante en Física. el [operador Laplaciano](https://es.wikipedia.org/wiki/Operador_laplaciano):

 $\bigtriangleup=\nabla\cdot\nabla=\nabla^2\frac{\partial^2}{\partial x^2}+\frac{\partial^2}{\partial y^2}+\frac{\partial^2}{\partial z^2}$ [2]

Consideremos ahora un **campo vectorial**, que es una función **F**(x,y,z) que asigna a cada punto del espacio un vector, seria un ejemplo el campo de velocidades del aire en la atmósfera. Si realizamos el producto escalar del operador gradiente con el vector de campo **F** obtenemos el denominado** rotacional** de **F**: 

$\overrightarrow{Rot}\left(\overrightarrow F\right)=\nabla\times\overrightarrow F=\left(\frac{\partial F_z}{\partial y}-\frac{\partial F_y}{\partial z},\frac{\partial F_x}{\partial z}-\frac{\partial F_z}{\partial x},\frac{\partial F_y}{\partial x}-\frac{\partial F_x}{\partial y}\right)$ [3]

que es obviamente un vector; observemos que si invertimos el orden del producto vectorial, **F** x **Grad**, no obtenemos un vector sino un operador diferencial: aplicar el gradiente a un camo escalar, y al vector gradiente resultante lo multiplicamos vectorialmente por el campo **F**. 

Hemos visto que el operador gradiente está relacionado con las direcciones de máxima variación de un campo escalar, y no hay gran misterio en ello, al ser perpendicular a las líneas de nivel y por tanto seguir la dirección de variación más rápida. Pero además veremos que tiene otras aplicaciones fundamentales para la Física, al estar también relacionado con la cantidad de flujo de una magnitud a través de superfícies y volúmenes (como el calor, la radiación, un líquido, etc).

## Flujo de un campo vectorial. Teorema de Gauss

Para fijar ideas imaginemos que el campo escalar de la figura 1 nos da las temperaturas T(x,y) en una superficie, y las curvas de nivel son curvas isotermas; como tenemos temperaturas distintas, habrá flujo de calor desde las zonas más calientes a las más frías: el flujo tiene una dirección y un sentido contrario al gradiente de temperatura, podemos pues definir el vector flujo de calor ***q ***asignándole una magnitud igual al incremento de calor por unidad de longitud, $\frac{\Delta Q}{\Delta s}$, y sentido inverso al vector gradiente de temperatura, $\nabla T$, (ver figura 2) esto es:

$\overrightarrow{q}=\frac{\Delta Q}{\Delta s}\;\frac{\nabla T}{\left|\nabla T\right|}=\frac{\Delta Q}{\Delta s}\widehat{e}$

![](/taller-matematicas/assets/images/Camp-T.png)Fig. 2: El flujo de calor ΔQ por unidad de longitud a través de un pequeño segmento Δs, ΔQ/Δs, define el módulo del vector flujo de calor** q** de dirección igual al gradiente de temperatura pero con sentido contrario.

![](/taller-matematicas/assets/images/gradient-angle.png)Fig. 3: elemento de superficie formando un ángulo con el gradiente de temperatura

En el caso de un campo T(x,y,z) en el espacio, el flujo de calor lo tomamos a través de la unidad de superficie. En la figura 2 para T(x,y) hemos tomado Δs sobre una curva de nivel T = constante y si T depende de x,y,z hubiéramos tomado Δs sobre una *superficie de nivel* (región del espacio tal que T es constante), pero podemos considerar un Δs cualquiera formando un ángulo con el gradiente (figura 3), llamando **n** al vector unitario normal al elemento Δs obtenemos el flujo de calor a través de Δs con el producto escalar **q**·**n**.  

Si consideramos que el elemento Δs es infinitesimal, *ds*, y recubrimos con tales elementos una superficie S, el flujo total de calor a través de esa superficie será $\Phi=\int_S\overrightarrow{q}\cdot\widehat n\cdot\operatorname ds$, y el vector **q** juega el papel en esa integral de *vector de densidad de flujo*. Cuando la superfície S es cerrada, encierra en su interior un volumen V, y el flujo total de calor a través de S nos da la variación de energía térmica en el volumen V; en estas condiciones es de aplicación un teorema de cálculo diferencial: *el teorema de Gauss*,

$\Phi=\oint_S\overrightarrow v\cdot\widehat n\cdot\operatorname ds=\int_V\triangle\overrightarrow v\cdot dV$ [4]

que leemos así: *el flujo total de un vector **v** a través de una superficie cerrada es igual a la divergencia del vector integrada sobre el volumen V limitado por S*. Hemos usado un vector v cualquiera porque el teorema es cierto para cualquier campo vectorial **v**(x,y,z), y en particular para el vector flujo de calor **q**. 

## Circulación de un vector, teorema de Stokes

![](/taller-matematicas/assets/images/circulacio.png)Fig. 4: circulación de **v** a lo largo de C

Consideremos ahora un campo vectorial v(x,y,z) y una curva cerrada C suave (sin aristas, y por tanto diferenciable), en la figura 4 tomamos es una elipse pero puede ser cualquier curva suave; escojamos un sentido de recorrido de la curva y dividamos C en segmentos infinitesimales ds, en cada uno de ellos, situados en un punto (x,y,z) de C, tendremos un valor del vector v. Si definimos el vector d**s** como el de módulo ds y dirección la de la tangente a la curva en ese punto, podemos multiplicar escalarmente los vectores d**s** y **v** en cada punto, y sumar los productos a lo largo de toda la curva C, o sea integrar, para obtener la *circulación del vector **v** a lo largo de C*. 

$\Phi=\oint_C\overrightarrow v\cdot\operatorname d\overrightarrow s$ [5]

![](/taller-matematicas/assets/images/circulacio-quadrat.png)Fig. 5: camino C cerrado, cuadrado, para el cálculo de la circulación

Consideremos el caso particular de que C es un cuadrado "pequeño" que encierra una superficie Δs (figura 5) y tiene lados Δx, Δy. Recorramos C en la dirección marcada por las flechas, en sentido contrario a las agujas del reloj (es el sentido estándard) y calculemos la circulación de un vector $\overrightarrow v=\left(v_x,v_y\right)$ obteniendo el producto **v**·Δ**s** en cada arista del cuadrado, teniendo en cuenta que en cada arista la dirección de Δ**s** es constante. El que sea pequeño el cuadrado significa que sus dimensiones Δx, Δy no son infinitesimales, de forma que los valores de **v** son distintos en cada arista, pero al mismo tiempo seran válidas las aproximaciones 

$\overrightarrow v\left(3\right)\approx\overrightarrow v\left(1\right)+\frac{\partial\overrightarrow v\left(1\right)}{\partial y}\triangle y,\;\overrightarrow v\left(2\right)\approx\overrightarrow v\left(4\right)+\frac{\partial\overrightarrow v\left(4\right)}{\partial x}\triangle x$

que provienen del desarrollo en serie de Taylor de la función v(x,y) truncada hasta el término de primer orden (aproximación lineal).

Lado 1: $\overrightarrow v\left(1\right)\cdot\Delta s_1=\left(v_x\left(1\right),v_y\left(1\right)\right)\cdot\triangle x\cdot(1,0)=v_x\left(1\right)\triangle x$

Lado 2: $\overrightarrow v\left(2\right)\cdot\Delta s_2=\left(v_x\left(2\right),v_y\left(2\right)\right)\cdot\triangle y\cdot(0,1)=v_y\left(2\right)\triangle y$

Lado 3: $\overrightarrow v\left(3\right)\cdot\Delta s_3=\left(v_x\left(3\right),v_y\left(3\right)\right)\cdot\triangle x\cdot(-1,0)=-v_x\left(3\right)\triangle x$

Lado 4: $\overrightarrow v\left(4\right)\cdot\Delta s_2=\left(v_x\left(4\right),v_y\left(4\right)\right)\cdot\triangle y\cdot(0,-1)=-v_y\left(4\right)\triangle y$

Sumando todo nos queda $\Phi=\left(v_x\left(1\right)-v_x\left(3\right)\right)\triangle x+\left(v_y\left(2\right)-v_y\left(4\right)\right)\triangle y$,, aplicamos la aproximación de primer orden de Taylor:

$\Phi=\left(v_x-v_x-\frac{\partial v}{\partial y}\triangle y\right)\triangle x+\left(v_y+\frac{\partial v}{\partial x}\triangle x-v_y\right)\triangle y=\left(\frac{\partial v}{\partial x}-\frac{\partial v}{\partial y}\right)\triangle x\triangle y$

que podemos expresar como operador:

![](/taller-matematicas/assets/images/rotacional-2-2.png)

Si hubiéramos desarrollado la circulación en tres dimensiones (x,y,z) la expresión seria

![](/taller-matematicas/assets/images/circulacio-quadrat-3D.png)

El determinante al desarrollarlo coincide con el rotacional del vector:

$Rot\left(\overrightarrow v\right)=\nabla\times\overrightarrow v=\left(\frac{\partial v_z}{\partial y}-\frac{\partial v_y}{\partial z},\frac{\partial v_x}{\partial z}-\frac{\partial v_z}{\partial x},\frac{\partial v_y}{\partial x}-\frac{\partial v_x}{\partial y}\right)$

Por tanto para tres dimensiones se cumple que *la circulación de un vector a lo largo de un cuadrado elemental C es igual al producto del rotacional del vector por el ár*ea del cuadrado: $\Phi=\sum_i\overrightarrow{v_i}\cdot\operatorname d\overrightarrow{s_i}=\nabla\times\overrightarrow v\operatorname ds$ [6].

Si imaginamos un cuadrado formado por n cuadrados pequeños, y miramos la circulación por todos ellos, observaremos que los lados que coinciden anulan la circulación entre sí (figura 6).

![](/taller-matematicas/assets/images/sumacirculacio.png)Fig.6: unión de caminos elementales y circulación en cada uno

 Por ello si en cada cuadrado elemental se cumple la ecuación [6], también se cumplirá para el cuadrado mayor. Para una superficie S cualquiera delimitada por una curva C cerrada podemos imaginar que la recubrimos con cuadrados elementales, de forma que la circulación total por C es también la suma de circulaciones elementales, que expresamos como integral, en la ecuación conocida como **Teorema de Stokes**: *la circulación de un vector a lo largo de un camino cerrado C es igual a la integral sobre la superficie S contenida por del rotacional del vector:*

$\Phi=\oint_C\overrightarrow v\cdot\operatorname d\overrightarrow s=\int_S\nabla\times\overrightarrow v\operatorname ds$ [7].

La deducción anterior no es rigurosa, lo que nos interesa es ver la relación entre el operador rotacional y la circulación de un vector por un camino cerrado. 

## Campos conservativos y potenciales escalares

Una propiedad importante de los operadores es que el rotacional de un gradiente es siempre cero: $Rot\left(\overrightarrow{Grad}\right)=\nabla\times\nabla=0$ que puede verse como la consecuencia de que el producto vectorial de un vector por sí mismo es cero. Segun el teorema de Stokes [7] la circulación sobre una curva cerrada C de un vector gradiente habrá de ser también cero: $\int_S\nabla\times\nabla q\operatorname ds=0=\oint_C\overrightarrow{q}\cdot\operatorname d\overrightarrow s=\Phi$. Nos podemos preguntar que tipos de campos vectoriales proporcionan una circulación nula por cualquier camino cerrado C, tal como sucede con los vectores gradientes. El cálculo diferencial nos asegura que *todo campo vectorial con circulación nula para cualquier camino cerrado C es el vector gradiente de un campo escalar al que llamamos **** potencial* escalar** (o simplemente potencial).  El campo vectorial que es un gradiente de un potencial y por tanto tiene rotacional nulo y circulación nula se llama **campo conservativo**. 

![](/taller-matematicas/assets/images/camp-vector-gravetat.png)Fig. 7: dos caminos para ir del punto A al B en un campo gravitatorio

**Ejemplo 1**: **Trabajo de una fuerza**.  El trabajo realizado por una fuerza **F** actuando sobre una masa m a lo largo de una trayectoria C toma la misma forma que la circulación del vector fuerza a lo largo de C: $W=\int_C\overrightarrow F\cdot\operatorname d\overrightarrow s$ [8]; si la curva C no es cerrada, el trabajo no tiene por que ser nulo, pero ¿que sucede si C es un ciclo que empieza y acaba en el mismo punto? En el caso del campo vectorial gravitatorio **g**=(0,0,-g) si la fuerza **F** trabaja *contra* ese campo, sólo efectuará trabajo no nulo la componente vertical de **F**, y será un trabajo igual a *menos* el trabajo del campo gravitatorio. En la figura 7 vemos dos caminos distintos para ir desde el punto A al B en un campo gravitatorio; descomponiendo la integral [8] en suma de integrales para cada tramo 1234567, los tramos horizontales 1357 al ser perpendiculares a la gravedad no aportan trabajo, y los verticales 246 al ser paralelos a la gravedad aportan $W=-\int_{tramo\;i}m\left(0,0,-g\right)\cdot\operatorname d\overrightarrow s=-mg\int_{tramo\;i}\operatorname d\overrightarrow s=-mg\cdot altura\;tramo\;i$ sumando todos los tramos nos queda el trabajo total *W = *-mgh siendo h la diferencia de altura entre A y B. Evidentemente por el camino alternativo 11'2' encontramos lo mismo: *el trabajo efectuado por el campo gravitatorio entre dos puntos sólo depende de la diferencia de altura entre los puntos y no del camino recorrido*.  Por tanto si ejercemos la fuerza **F** en un ciclo cerrado que empieza y acaba en el mismo punto A, el trabajo deberá de ser nulo, y por definición la circulación de **F** también: *el campo gravitatorio es un campo conservativo* y el vector fuerza gravitatoria será igual al gradiente de un potencial: $\overrightarrow F=(0,0,-g)=\nabla\psi$, además, el rotacional del campo gravitatorio ha de ser nulo. El potencial gravitatorio resulta ser $\psi\left(x,y,z\right)=-mgz$. 

**Ejemplo** **2**: **campo electrostático**. El campo electrostático **E** generado por un conjunto de cargas estáticas es también conservativo, verificando **Rot** x **E** = **0**;  y existe un **potencial electrostático** A(x,y,z) tal que **E** = **Grad**(A). En cambio si las cargas estan en movimiento el campo E deja de ser conservativo, y se cumple una de las **ecuaciones de Maxwell** del electromagnetismo, $Rot\left(\overrightarrow E\right)=-\frac{\partial\overrightarrow B}{\partial t}$ siendo B el campo magnético generado por las cargas en movimiento; además la circulación del campo **E** en torno a un bucle cerrado no será nula. 

## Potencial vector

Hemos visto que si el rotacional de un campo vectorial **v** es cero, entonces ese campo es igual a gradiente de algun campo escalar A que denominamos el potencial escalar de **v**. La idea provenia del hecho de que **Rot** (**Grad** A) = 0 para cualquier campo escalar A. Por otro lado la divergencia del rotacional también es siempre cero, $\nabla\cdot\overset\rightharpoonup\nabla\times\overrightarrow v=0$, intuitivamente vemos que el producto vectorial de **∇** por **v** es un vector perpendicular a ámbos, y por tanto su producto escalar por **∇** ha de ser nulo. Nos preguntamos si es un resultado general el que si la divergencia de un vector **v** es nula, entonces ese vector es el rotacional de otro vector **w**, la respuesta es afirmativa, y llamamos al vector **w** el **potencial vector** de **v**. 

Si **∇**·**v** = 0, entonces existe un **w** tal que **v** = **∇** X **w**. 

**Ejemplo 3**: **potencial vector electromagnético**. El campo magnético **B** verifica la ecuación de Maxwell **∇**·**B** = 0, luego existe un potencial vector **A** tal que **B** = **Rot** (**A**) denominado [potencial vectorial electromagnético](https://es.wikipedia.org/wiki/Potencial_vectorial_electromagn%C3%A9tico).  

**Ejemplo 4: Ecuación diferencial de la hidrostática**. La hidroestática estudia las leyes físicas de los fluidos en equilibrio estático; consideremos el interior de un fluido en el que hay unas presiones variables que pueden representarse mediante un campo escalar p(x,y,z), e imaginemos un elemento de volumen de lados ∇x, ∇y, ∇z y volumen ∇x∇y∇z = ∇V, sometido a presiones externas en sus caras (figura 8). 

![](/taller-matematicas/assets/images/element-fluid-estàtic.png)Fig. 8: elemento de volumen de fluido sometido a presión

La presión dado que el elemento es pequeño podemos considerar que es la misma para cada cara y aplicada en el centro, pero ligeramente diferente entre caras; así, segun el eje X de coordenadas, y dadas la presiones de sentido contrario p, p', podemos expresar la segunda en función de la primera por $p'=p+\frac{\partial p}{\partial x}\triangle x$. Nos fijamos ahora en las fuerzas generadas por las presiones p y p' que son, respectivamente F = p·∇x∇y y F' = p'·∇x∇y, la suma de fuerzas en la dirección X será F - F', que es:

$F-F'=p\triangle y\triangle z-\left(p+\frac{\partial p}{\partial x}\triangle x\right)\triangle y\triangle z=-\frac{\partial p}{\partial x}\triangle x\triangle y\triangle z=-\frac{\partial p}{\partial x}\triangle V$,

pero en las direcciones Y y Z tendremos expresiones similares, pues la presión se ejerce en todas las caras del elemento de volumen. El vector fuerza que actúa sobre el volumen será, teniendo en cuenta sus tres componentes,

$\overrightarrow F=\left(-\frac{\partial p}{\partial x}\triangle V,-\frac{\partial p}{\partial y}\triangle V,-\frac{\partial p}{\partial z}\triangle V\right)-=\left(\frac{\partial p}{\partial x},\frac{\partial p}{\partial y},\frac{\partial p}{\partial z}\right)\triangle V=-\nabla p\cdot\triangle V$. [9]

Consideremos que además de la presión actuan sobre el fluido otras fuerzas conservativas, como la gravedad, que representamos en conjunto por un potencial  φ(x,y,z) que para simplificar las expresiones suponderemos que es un potencial por unidad de masa (se obtiene dividiendo el potencial por la masa); observemos que la fuerza [9] dividida por el volumen V se convierte en una fuerza por unidad de volumen y vale $\overrightarrow{F_v}=-\nabla p$, y por otro lado multiplicando el potencial por unidad de masa por la densidad del fluido ρ obtendremos el potencial por unidad de volumen, así pues la fuerza total por unidad de volumen la podemos expresar por $\sum_{}F=-\nabla p-\rho\nabla\varphi$. Esta fuerza ha de ser cero si el fluido está en equilibrio, al espresarlo tenemos la ecuación diferencial de la hidrostática en condiciones de presión y de fuerzas conservativas:

$\nabla p+\rho\nabla\varphi=0$ [10],

y viene expresada en función de gradientes de campos escalares. Veamos ahora como los operadores diferenciales nos ayudan a ver las soluciones de tal ecuación; si aplicamos el operador rotacional a toda la expresión, recordando que es un operador lineal, que el rotaconal de un gradiente es cero, y que el rotacional del vector nulo es también cero, obtenemos:

$Rot\left(\nabla p+\rho\nabla\varphi\right)=Rot\left(0\right)\Rightarrow Rot\left(\nabla p\right)+Rot\left(\rho\nabla\varphi\right)=0\Rightarrow Rot\left(\rho\nabla\varphi\right)=0$.

En general, para densidades variables segun la posición (x,y,z), esta última ecuación no se cumple, por ejemplo en los gases sometidos a presión y fuerzas conservativas en general, siendo los gases fácilmente compresibles las densidades variarán de forma que habrá movimiento del gas, no habrá equilibrio estático. En el caso de un líquido, mucho más difícil de comprimir, si consideramos que tiene un densidad constante entonces podemos sacarlo fuera del operador rotacional y entonces la condición de equilibrio se cumple siempre: $Rot\left(\rho\nabla\varphi\right)=0\Rightarrow\rho\cdot Rot\left(\nabla\varphi\right)=0\Rightarrow\rho\cdot0=0$. En este caso la condición [10] implica la igualdad entre gradientes $\nabla p=-\rho\nabla\varphi$ que se cumplirá siempre que $p+\rho\varphi=\;$ *constante* que es la *ecuación de equilibrio del fluido para densidad constante*.
{% endraw %}