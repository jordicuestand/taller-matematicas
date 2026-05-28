---
layout: post
title: "Estabilidad de soluciones: introducción"
date: 2015-07-09 20:47:16 +0000
math: true
---
{% raw %}

En las aplicaciones prácticas a menudo interesa ya no resolver exactamente una ecuación diferencial sino además saber si la solución obtenida es estable en el sentido de si es poco o muy sensible a los cambios que podamos introducir en las condiciones iniciales, los coeficientes de la ecuación, o simplemente al movernos de un punto $x_0$ a otro punto próximo $x_1$. También puede interesar conocer el comportamiento (continuidad, límites, etc) de la solución de la ecuación incluso en aquellos casos en los que no podemos obtener esa solución de forma explícita.

**Ejemplo 1**: Una de las ecuaciones diferenciales propuestas para predecir el crecimiento y decrecimiento de poblaciones biológicas es la que representa el modelo logístico de la población: $\frac{\operatorname dP}{\operatorname dt}=kP-kP\frac PM$ donde $p(t)$ es la población en función del tiempo, k es la constante de proporcionalidad entre la población y su crecimiento (natalidad), M es la población máxima que puede sostenerse con los recursos existentes, y el término $-kP\frac PM$ es el decrecimiento (mortalidad), que también es proporcional   a la población y al factor p/M. Esta es una ecuación separable que puede integrarse por [descomposición en fracciones simples](http://tallermatematic.eu/wp/?p=138#racionales): $\int\frac{\operatorname dP}{P\left(1-\frac PM\right)}=\int k\operatorname dt\Leftrightarrow\frac P{1-\frac PM}=Ce^{kt}$; para el valor $t=0$ suponemos una población inicial $t_0$, encontramos pues el valor de la constante de integración C: $\frac{P_0}{1-\frac{P_0}M}=C$. Sustituimos en la expresión anterior y operamos para obtener la expresión explícita de la población. $P\left(t\right)=\frac{MP_0e^{kt}}{1-P_0\left(e^{kt}-1\right)}$. Este modelo produce la función P(t) continua y en el límite $t\rightarrow\infty$ tiende al valor M, o sea predice un rápido crecimiento de la población hasta alcanzar el valor máximo.

[![poblacio](/taller-matematicas/assets/images/poblacio.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/07/poblacio.png)
# Ecuaciones de primer orden autónomas

En el ejemplo 1 hemos visto el modelo poblacional logístico, con ecuación $\frac{\operatorname dP}{\operatorname dt}=kP-kP\frac PM$; en el caso general consideramos ecuaciones tales como $\frac{\operatorname dP}{\operatorname dt}=F\left(P\right)$, esto es, ecuaciones de primer orden donde no aparece la variable independiente, denominadas **ecuaciones autónomas**. Supondremos que la función F(y) es diferenciable (y por tanto continua). Para estas ecuaciones $\frac{\operatorname dy}{\operatorname dx}=F\left(y\right)$ si existe una constante c tal que F(c)=0 entonces la ecuación admite la solución y=c.

**Ejemplo 2**: La ecuación diferencial del ejemplo 1 es autónoma, con $F\left(P\right)=kP\left(1-\frac PM\right)$, y el valor P=0  anula F(P), luego la ecuación admite la solución constante P=0. En efecto, esta solución se obtiene tomando la población inicial $P_0=0$. Además hay una segunda raíz para la solución constante P=M, pues $F\left(M\right)=kP\left(1-\frac MM\right)=0$.

En general, a cada raíz c de F(y) le corresponde una solución constante y=c; a los puntos c se les llama **puntos críticos** de la ecuación autónoma. El interés de los puntos críticos es que, cuando variamos las condiciones iniciales, las correspondientes soluciones siempre tienen uno de los dos comportamientos siguientes: o convergen o divergen en cada punto crítico. En el primer caso el punto crítico es **estable**, en el segundo, es **inestable**. En el siguiente gráfico vemos tres soluciones del ejemplo 1: todas convergen para el punto crítico P=M, que es estable,  y divergen para P=0, que es inestable:

$caption id="attachment_1234" align="alignnone" width="488"$[![poblacio2](/taller-matematicas/assets/images/poblacio2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/07/poblacio2.png) Tres soluciones de la ecuación de la población, con distintas poblaciones iniciales; todas convergen para P=M, y divergen para P=0
La estabilidad o inestabilidad de un punto crítico también se relaciona con los cambios en los coeficientes de la ecuación autónoma, además de con las condiciones iniciales; si estudiamos las soluciones de la ecuación de la población, pero con distintos valores del parámetro k, hallamos el mismo comportamiento. Esto es importante para las aplicaciones prácticas, pues a menudo desconocemos el valor real de ciertos parámetros; sabemos entonces que las soluciones convergerán en los puntos estables a la misma solución para cualquier valor inicial y parámetros dados.

**Ejemplo 3**: Supongamos que en realidad ignoramos el valor de la constante k , sólo creemos que estará comprendido en el intervalo [0.1, 0.5]; para un mismo valor inicial de la población pero distintos valores de k, el comportamiento es el mismo cerca del punto crítico estable:

[![poblacio3](/taller-matematicas/assets/images/poblacio3.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/07/poblacio3.png) Soluciones de la ecuación de la población, misma población inicial, distintos coeficientes k
 La forma habitual de estudiar el carácter de los puntos críticos es usar la recta fase de la ecuación autónoma: consiste en observar el signo de la función F(y) a los lados de cada punto crítico; como la derivada y' es igual a F(y), de hecho estamos observando el crecimiento y decrecimiento de la función y alrededor de los puntos críticos: cuando el punto c es estable esperamos que la función y tienda a ese punto c por ambos lados, luego si cuando y<c crece (tendiendo a c), por el otro y>c ha de decrecer (tendiendo también a c). Lo vemos con un ejemplo.

**Ejemplo 4**: La recta fase de la ecuación autónoma de los ejemplos anteriores es:

[![Recta fase de la ecuación de la población, muestra la tendencia a los lados de los puntos críticos ](/taller-matematicas/assets/images/fase.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/07/fase.png) Recta fase de la ecuación de la población, muestra la tendencia a los lados de los puntos críticos
Vemos que la función F(P) se "aleja" del punto crítico P=0, que es un punto inestable, mientras que F(P) se "acerca" al punto P = M, que es estable. Hemos considerado los intervalos P < 0, 0 < P < M, P > M, y en cada uno de ellos hemos estudiado el signo de $F\left(P\right)=kP\left(1-\frac PM\right)$.

# Sistemas de primer orden autónomos

Consideramos los sistemas de dos EDO, con las funciones y(x), z(x), tales que tienen la forma:
$\left.\begin{array}{r}\frac{\operatorname dy}{\operatorname dx}=F\left(y,z\right)\\\frac{\operatorname dz}{\operatorname dx}=G\left(y,z\right)\end{array}\right\}$

o sea que la variable independiente x no aparece. Supondremos que las funciones F, G son diferenciables, y por tanto que para cada punto (y,z) del plano R² existe una solución única y(x), z(x) tal que satisface las condiciones iniciales $y(x_0)=y_0, z(x_0)=z_0$. Estas soluciones son curvas en el plano (y,z) denominadas **trayectorias del sistema**. Entonces, un punto $(y_0,z_0)$ tal que $F(y_0,z_0)=G(y_0,z_0)=0$ se llama **punto crítico del sistema autónomo**. Para cada punto crítico tenemos una solución constante del sistema: $y(x)=y_0, z(x)=z_0$, que es un punto.

**Ejemplo 5**: Consideremos un resorte de constante elástica k, al que fijamos un objeto de masa m; supongamos que hacemos oscilar la masa con el resorte con rozamiento despreciable, resultando un [movimiento armónico simple](https://es.wikipedia.org/wiki/Movimiento_arm%C3%B3nico_simple). Siendo la fuerza del muelle F=-kx, con x: desplazamiento respecto la posición de equilibrio del muelle, la aceleración de la masa m vendrá dada por la 2ª ley de Newton: F = ma = -kx. Recordando que la aceleración es la derivada segunda de la posición, nos resulta una [EDO homogénea de segundo orden](http://tallermatematic.eu/wp/?p=987): mx'' + kx = 0. Por conveniencia suele dividirse toda la ecuación por m: $x''+\omega^2x=0$, donde $\omega=(k/m)^{1/2}$ se denomina pulsación del movimiento. La solución de esta ecuación es $x\left(t\right)=A\cos\left(\omega t\right)+B\sin\left(\omega t\right)$.

Llamando $y$ a la derivada $x'$ (que es la velocidad), resulta que x''=y', entonces podemos escribir la EDO de segundo orden como un sistema de EDO de 1r orden que resulta ser autónomo, ya que la variable independiente tiempo t no aparece:

$\left.\begin{array}{r}x'=y\\y'=-\omega^2x\end{array}\right\}$

Este sistema tiene un único punto crítico en (x, y) = (0, 0). ¿Cuáles son las trayectorias en el espacio (x, y) de las soluciones del sistema (llamado **espacio fase**)? Derivando obtenemos: $x'\left(t\right)=y=-A\omega sin\left(\omega t\right)+B\omega\cos\left(\omega t\right)$, representando los puntos (x, y) variando los parámetros $A, B, \omega$ obtenemos trayectorias elípticas centradas en el origen, que es el punto crítico de la ecuación:

[![centre_estable](/taller-matematicas/assets/images/centre_estable.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/07/centre_estable.png) Trayectorias x(t), y(t) para tres diferentes combinaciones de los parámetros en un oscilador armónico simple; en abscisas tenemos el desplazamiento x, en ordenadas la velocidad y=x'

Un punto crítico como el del ejemplo 5, que está rodeado por trayectorias cerradas, se denomina** centro estable**.
{% endraw %}