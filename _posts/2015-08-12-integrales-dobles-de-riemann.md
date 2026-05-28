---
layout: post
title: "Integrales dobles de Riemann"
date: 2015-08-12 13:00:59 +0000
categories:
  - "Cálculo en varias variables"
  - "Funciones reales de dos variables"
  - "Matemáticas"
tags:
  - "integral de Riemann"
  - "integral doble"
math: true
---
{% raw %}

# Integral de Riemann en dos dimensiones (integral doble)


De la misma forma que en la [integral de Riemann](http://tallermatematic.eu/wp/?p=674) en un intervalo (a,b) para la función $y=f(x)$ de una variable dividíamos la variable independiente x en intervalos de amplitud dx, calculábamos las áreas $dA=y(x)·dx$, sumábamos y pasábamos al límite para obtener la integral $\int_a^bf\left(x\right)\operatorname dx$, cuando tenemos una función real con dos variables independientes $z=f(x,y)$ dividiremos el plano (x,y) en parcelas de dos dimensiones de amplitud dx, dy, sumaremos los productos f(x,y)·dx·dy y pasaremos al límite para obtener la integral doble de f(x,y) en el recinto R: $\int_Rf\left(x,y\right)\operatorname dx\operatorname dy.$

Más en detalle: sea *w* una de las parcelas del plano R; estas parcelas no tienen porque ser rectangulares, pueden tener cualquier forma, como en la siguiente figura:


En cualquier caso, dada una parcela *w*, formaremos el producto $f(x,y)·A_w$ donde $A_w$ simboliza el área de la parcela *w*; ¿qué valor $f(x,y)$ tomaremos? Pues dentro de la región w hay infinitos puntos (x,y)... en la integral de Riemann lo que hacemos es considerar los valores máximo y mínimo de $f(x,y)$ en la parcela w, los denominamos $M_w,  m_w$ respectivamente. Entonces definimos las sumas superior e inferior de Riemann para $f(x,y)$ y para la parcelación efectuada en R, sumando los productos de las áreas de cada parcela por los valores máximo y mínimo, respectivamente, de  $f(x,y)$ en cada parcela:

$S=\sum\nolimits_{i=1}^nM_{w_i}\cdot A_{w_i}\;,\;s=\sum\nolimits_{i=1}^nm_{w_i}\cdot A_{w_i}$

Evidentemente se cumplirá que $S &gt; s$ para cualquier parcelación de R. Si pasamos al límite de particiones infinitesimales, y ese límite existe, diremos que la función de dos variables es integrable en R según Riemann, y se cumplirá:

$\underset{n\rightarrow\infty}{lim}S=\underset{n\rightarrow\infty}{lim}\sum\nolimits_{i=1}^nM_{w_i}\cdot A_{w_i}\;=\int\int_Rf(x,y)\operatorname dw=\underset{n\rightarrow\infty}{lim}\;s=\underset{n\rightarrow\infty}{lim}\sum\nolimits_{i=1}^nm_{w_i}\cdot A_{w_i}$,

o sea que los límites de las sumas inferior y superior coinciden, y definen el valor de la integral doble.  Observad que aparece la diferencial dw en vez de dx o dy; esto se debe a que hemos considerado parcelaciones de R de cualquier tipo, no sólo las rectangulares.

 **Ejemplo1** : integrabilidad de las funciones continuas. Si $f(x,y)$ es una función continua de dos variables, entonces por definición, dado un $\varepsilon&gt;0$ cualquiera, siempre podremos encontrar un entorno circular de radio r centrado en $(x_0,y_0)$ tal que todos los puntos (x,y) dentro del entorno tendrán valores $f(x,y)$ distintos de $f(x_0,y_0)$ en como mucho $\varepsilon$. Por tanto, dentro de ese entorno, el valor máximo M y el mínimo m diferirán en como mucho un múltiplo de $\varepsilon$. Como podemos hacer tender $\varepsilon$ a cero, se sigue que la diferencia $M-m$ tenderá también a cero, y en el límite $\underset{n\rightarrow\infty}{lim}S=\underset{n\rightarrow\infty}{lim}\;s=\int\int_Rf(x,y)\operatorname dw$. Así pues, todas las funciones continuas son integrables según Riemann. Si la función es continua a trozos,  entonces será integrable a trozos.

# Calculo de integrales dobles en recintos rectangulares: integrales reiteradas

En lo que sigue sólo trataremos con regiones R de integración rectangulares; supongamos que dividimos el intervalo a < x < b del eje X en n subintervalos, y el intervalo c < y < d del eje Y en m subintervalos;


tendremos por tanto nm rectángulos, y las sumas de Riemann tendrán la forma:

$S=\sum\nolimits_{i=1}^n\sum\nolimits_{j=1}^mf\left(x_i,y_j\right)\triangle x_i\triangle y_j=\sum\nolimits_{j=1}^m\triangle y_j\sum\nolimits_{i=1}^nf\left(x_i,y_j\right)\triangle x_i$
Sólo consideramos una de las sumas pues ambas son iguales cuando la función es integrable; en la segunda igualdad hemos sumado primero "por filas", esto es, manteniendo constante $y_k$ sumamos para todos los $x_k$, y seguimos obteniendo sumas parciales que totalizamos al final. Pasando al límite sólo para la variable x, vemos que:

$\underset{n\rightarrow\infty}{lim}S=\sum\nolimits_{j=1}^m\triangle y_j\sum\nolimits_{i=1}^nf\left(x_i,y_j\right)\triangle x_i=\sum\nolimits_{j=1}^m\triangle y_j\int_a^bf\left(x,y_j\right)\operatorname dx$

o sea que el sumatorio segun x se transforma en la integral según x; pasando al límite para y:

$\underset{m\rightarrow\infty}{lim}S=\underset{m\rightarrow\infty}{lim}\sum\nolimits_{j=1}^m\triangle y_j\int_a^bf\left(x,y_j\right)\operatorname dx=\int_c^d\operatorname dy\int_a^bf\left(x,y_j\right)\operatorname dx$
Vemos que se puede calcular la integral doble realizando dos integraciones parciales, cada una con una de las variables independientes; a estas integrales se les llama integrales reiteradas.

**Ejemplo 2**: Calcular la integral de z=1-x²-y² en el recinto cuadrado R: {-1 < x, y < 1}. Dividimos el recinto rectangular en n² cuadrados y pasamos al límite $n\rightarrow\infty$ para obtener las integrales reiteradas:

$\int_{-1}^1\operatorname dy\int_{-1}^1\left(1-x^2-y^2\right)\operatorname dx$

Calculamos primero la integral respecto x, considerando y como una constante:

$\int_{-1}^1\left(1-x^2-y^2\right)\operatorname dx=\left$x-\frac{x^3}3-y^2x\right$_{-1}^1=1-\frac13-y^2-\left(-1+\frac13+y^2\right)=\frac43-2y^2$

Calculamos ahora la integral respecto de y: $\int_{-1}^1\left(\frac43-2y^2\right)\operatorname dy=\left$\frac43y-2\frac{y^3}3\right$_{-1}^1=\frac43-\frac23-\left(-\frac43+\frac23\right)=\frac43.$

# Calculo de integrales dobles en recintos no rectangulares

En general podemos integrar en un recinto R delimitado por una curva cerrada C dada de forma implícita por una cierta función f(x,y):


La limitación que se impone para que la integral sea calculable según Riemann es que la curva C sea una [curva de Jordan](http://mathworld.wolfram.com/JordanCurve.html) que son curvas cerradas en las cuales el número de puntos de intersección de la curva con cualquier recta es finito. Para integrar la función f en el interior del recinto delimitado por la curva C, encerramos la curva en un recinto rectangular R y suponemos que la función toma valor cero fuera del interior de la curva. Aplicamos entonces la integral reiterada en el recinto R: para cada valor $y_0$ dado, la recta horizontal $y=y_0$ cortará a la curva en un número de puntos, delimitando unos segmentos $s_1, s_2, ...$; fuera de esos segmentos la integral valdrá cero, y sólo tendremos valores no nulos en los segmentos:

$\int\int_Rf\left(x,y\right)\operatorname dx\operatorname dy=\int_c^d\operatorname
dy\sum\nolimits_{i=1}^n\int_{s_i}f\left(x,y\right)\operatorname dx$

### Caso de recinto R convexo

Cuando el recinto de integración es [convexo](https://es.wikipedia.org/wiki/Convexidad), las rectas que lo cortan lo hacen como máximo en dos puntos, o sea que tendremos para cada $y=y_0$ cada recta horizontal $y=y_0$  definirá un segmento:


Si somos capaces de expresar los valores de los extremos del segmento en función de y, o sea $x_1(y), x_2(y)$, podemos substituirlos en las integrales reiteradas:

$\int\int_Rf\left(x,y\right)\operatorname dx\operatorname dy=\int_c^d\operatorname dy\int_{x_1\left(y\right)}^{x_2\left(y\right)}f\left(x,y\right)\operatorname dx$.

Evidentemente se puede proceder también considerando rectas verticales $x=x_0$ que definen segmentos verticales, e integrar reiteradamente primero respecto de y, luego respecto de x. El orden es indiferente, así que podemos tomar el que sea más evidente o más fácil de expresar. en el siguiente ejemplo los hacemos del segundo modo.
**Ejemplo 3**: Calcular la integral doble de la siguiente función en todo su dominio:

$f\left(x,y\right)=\left\{\begin{array}{l}8xy,\;0&lt;x&lt;y&lt;1\\0\;\text{en otro caso}\end{array}\right.$

El dominio de definición D de la función es el triángulo delimitado por los puntos (0,0), (1,0) y (1,1) en el plano XY:

![](/taller-matematicas/assets/images/integra_area.png)
En la imagen vemos que, fijando un valor x, la variable y varía desde y=0 hasta y=x, ya que el dominio es 0 < y < x < 1. Por tanto el segmento vertical queda definido por $y_1(x)=0, y_2(x)=x$. Lo llevamos a las integrales reiteradas:

$\begin{array}{l}\iint_Df\left(x,y\right)\operatorname dx\operatorname dy=\int_0^1\operatorname dx\int_0^x8xy\operatorname dy=\int_0^1\operatorname dx\left$8x\frac{y^2}2\right$_0^x=\\4\int_0^1x^4\operatorname dx=4\left$\frac{x^4}4\right$_0^1=1.\end{array}$

# Cálculo de volúmenes usando integrales dobles

Al definir la integral doble de Riemann hemos tomado cada parcela *w *de la región R de integración y hemos formado el producto $f(x,y)·A_w$ donde $A_w$ simboliza el área de la parcela *w. *Interpretando f(x,y) como una altura z sobre el plano (x,y), el producto $f(x,y)·A_w$ es el volumen de un "cilindro" de altura z=f(x,y) y base w; en la siguiente figura se representa el cilindro formado por una región R circular y la altura z:


**Ejemplo 4**: Probar que el volumen de un cilindro con base circular y radio r y altura h es $\pi r^2h$ usando una integral doble.

La región R del plano XY es el círculo interior a la circunferencia x²+y²=r²; para la función z=f(x,y) tomamos el valor constante z=h. El volumen del cilindro viene dado por la integral doble $\int\int_Rh\operatorname dx\operatorname dy=h\int\int_R\operatorname dx\operatorname dy.$ Para calcular la integral en el recinto R, usamos integrales reiteradas: tenemos que expresar x en función de y, o viceversa, por ejemplo: $x^2+y^2=r^2\Leftrightarrow x=\pm\sqrt{r^2-y^2}.$ La otra variable, y, cumple $-r\leq y\leq r$. Por tanto las integrales reiteradas son $\int_{-r}^r\operatorname dy\int_{x_2}^{x_1}\operatorname dx$ donde $x_1=\sqrt{r^2-y^2},\;x_2=-\sqrt{r^2-y^2}.$  Calculamos primero la de la variable x:

$\int_{x_2}^{x_1}\operatorname dx\;=x_1-x_2=2\sqrt{r^2-y^2}$

Sustituimos en la integral respecto de y: $2\int_{-r}^r\sqrt{r^2-y^2}\operatorname dy$;  las integral de este tipo se calculan por cambio de variable usando funciones seno o coseno; primero la preparamos:

$\int_{-r}^r\sqrt{r^2-y^2}\operatorname dy=\int_{-r}^rr\sqrt{1-\left(\frac yr\right)^2}\operatorname dy=r\int_{-r}^r\sqrt{1-\left(\frac yr\right)^2}$,

luego hacemos el cambio

$\frac yr=\sin\left(t\right)\Rightarrow\sqrt{1-\left(\frac yr\right)^2}=\cos\left(t\right);\;\frac{\operatorname dy}r=\operatorname d\left(sin\left(t\right)\right)=\cos\left(t\right)\operatorname dt,$

que transforma la integral original en:

$r\int\sqrt{1-\left(\frac yr\right)^2}\operatorname dy=r^2\int\cos^2\left(t\right)\operatorname dt,$

esta integral se hace por partes, resultando $\int\cos^2\left(t\right)\operatorname dt=\sin\left(t\right)\cos\left(t\right)+t.$ Sustituyendo en la integral original y deshaciendo el cambio:

$2\int_{-r}^r\sqrt{r^2-y^2}=2\left$\frac yr\cdot\sqrt{1-\left(\frac yr\right)^2}+\sin^{-1}\left(\frac yr\right)\right$_{-r}^r=2\left$1\cdot0+\frac\pi2-0\right$=\pi$

El volumen es: $V=h\int\int_R\operatorname dx\operatorname dy=\boxed{hr^2\pi}$

**Ejemplo 5**: Calcular el volumen definido por la región R del plano delimitado por las curvas y=x², x=y², y altura dada por la función z=f(x,y)=x²+y².

El volumen que nos piden viene dado por la integral doble $\int\int_R\left(x^2+y^2\right)\operatorname dx\operatorname dy$.

La región R definida por y=x², x²=y está contenida en el cuadrante x>0, y>0, pues sustituyendo x=y² en y=x² obtenemos y=(y²)²=y⁴, luego y⁴-y=0, de donde y(y³-1)=0 que tiene por soluciones y=0, y=1; para y=0 tenemos x=0, para y=1 es x=1. La región es convexa, y se representa en la siguiente figura (aunque no es necesaria la representación gráfica para resolver el problema, siempre ayuda a comprenderlo):


Para un valor $y_0$ dado, la recta $y=y_0$ corta a la región R en dos puntos, con coordenadas $x_1, x_2$ dadas por: 1) intersección con x²=y: $x_1^2=y_0\Leftrightarrow x_1=\sqrt{y_0}$, 2) intersección con y=x²: $x_2=y_0^2$.

Por tanto podemos expresar, dentro de la región R, la variación de x en función de y: el segmento horizontal azul de la figura tiene coordenadas $(y_0^2,y_0),(\sqrt{y_0},y)$, en general, para cualquier y dado en el intervalo [0, 1], la variable x variará entre $y^2$ y $\sqrt{y}$. Podemos pues calcular la integral doble en R usando dos integrales reiteradas:

$\begin{array}{l}\int\int_R\left(x^2+y^2\right)\operatorname dx\operatorname dy=\int_0^1\operatorname dy{\int_{y^2}^\sqrt y}_R\left(x^2+y^2\right)\operatorname dx=\int_0^1\operatorname dy\left$\frac{x^3}3+xy^2\right$_{y^2}^\sqrt y=\\\int_0^1\left(\frac{y^{3/2}}3+y^{5/2}-\frac{y^6}3-y^4\right)\operatorname dy=\left$\frac{y^{5/2}}{{\displaystyle\frac52}\cdot3}+\frac{y^{7/2}}{\displaystyle\frac72}-\frac{y^7}{3\cdot7}-\frac{y^5}5\right$_0^1=\\\frac2{15}+\frac27-\frac1{21}-\frac15=\boxed{\frac6{35}}\end{array}.$

# Cambio de variables en integrales dobles

A menudo la naturaleza del problema presenta una simetría que, bien aprovechada, puede simplificar la resolución. Una forma de aprovechar esa simetría es hacer un cambio de variable; por ejemplo, para una simetría en el plano XY respecto al origen será en general mejor trabajar con coordenadas polares:

$\begin{array}{l}\left.\begin{array}{r}x=\rho cos\left(\theta\right)\\y=\rho sin\left(\theta\right)\end{array}\right\}\\\end{array}$

Para calcular una integral doble en un recinto R del plano XY usando coordenadas polares, tenemos que convertir el elemento de área rectangular $\triangle x\triangle y$ por un elemento de área en las
coordenadas $\rho,\theta$; en la siguiente ilustración vemos que esa área será, aproximadamente, igual al lado $\triangle \rho$ por la longitud del arco; hay dos arcos, si medimos el ángulo $\theta$ en radianes, sus longitudes son $\rho \cdot \triangle \theta$ y $(\rho + \triangle \rho )\cdot \triangle \theta:$


Como para hacer la integral tomamos el límite $\triangle\rho\rightarrow0$, podemos considerar que los dos arcos son iguales, pensando que el radio $\rho$ es el valor medio para el elemento de área,  resulta que el área valdrá $\rho\triangle\theta\triangle\rho$. Entonces al pasar al límite de tenemos la equivalencia:

$\int\int_Rf\left(x,y\right)\operatorname dx\operatorname dy=\int\int_Rf\left(\rho,\theta\right)\rho\operatorname d\theta\operatorname d\rho$

**Ejemplo 6**: Revisemos el ejemplo 4, para el cilindro con base circular podemos usar [coordenadas cilíndricas](https://es.wikipedia.org/wiki/Coordenadas_cil%C3%ADndricas) que toman coordenadas polares para el plano XY dejando la coordenada Z sin cambios; entonces la región R de integración queda muy simple:

$\begin{array}{l}\left.\begin{array}{r}x=\rho cos\left(\theta\right)\\y=\rho sin\left(\theta\right)\end{array}\right\}\Rightarrow x^2+y^2=r^2\Leftrightarrow\rho^2=r^2\Leftrightarrow\rho=r\\\end{array}$

Para la coordenada z no hay cambios: z=h, la altura del cilindro; el volumen será, apllicando integrales reiteradas en las nuevas coordenadas, y teniendo en cuenta que el ángulo $\theta$ varia entre 0 y 2π, y que el radio $\rho$ varia entre 0 y r:

$\begin{array}{l}\int\int_Rh\operatorname dx\operatorname dy=\int\int_Rh\rho\operatorname d\theta\operatorname d\rho=h\int_0^{2\mathrm\pi}\operatorname d\theta\int_0^r\rho\operatorname d\rho=h\int_0^{2\mathrm\pi}\operatorname d\theta\cdot\left$\frac{\rho^2}2\right$_0^r=\\h\int_0^{2\mathrm\pi}\frac{r^2}2\operatorname d\theta=\frac{r^2}2h\int_0^{2\mathrm\pi}\operatorname d\theta=\frac{r^2}2h\left$\theta\right$_0^{2\mathrm\pi}=\boxed{r^2h\pi}\\\end{array}$

Vemos que las integrales se han simplificado mucho respecto a las calculadas en el ejemplo 4.

En general un cambio de variables (x,y) por (u,v) se puede expresar como funciones x=x(u,v), y=y(u,v); por ejemplo, en el caso de coordenadas polares esas funciones son $x=\rho cos\left(\theta\right), y=\rho sin\left(\theta\right)$, con u=r, v=θ. Para expresar el elemento de área dxdy en función de u,v, [diferenciamos](http://mathseng.blogspot.com.es/2012/02/derivadas-parciales.html) las funciones x, y: $\operatorname dx=\frac{\partial x}{\partial u}\operatorname du+\frac{\partial x}{\partial v}\operatorname dv;\;\operatorname dy=\frac{\partial y}{\partial u}\operatorname du+\frac{\partial y}{\partial v}\operatorname dv$, efectuamos el producto, y despreciamos los términos con diferenciales al cuadrado, $du^2, dv^2$, pues recordemos que para integrar pasamos al límite del diferencial de área tendiendo a cero, luego el diferencial al cuadrado tiende a cero mucho más rápidamente, nos queda:

$\operatorname dxdy=\frac{\partial x}{\partial u}\frac{\partial y}{\partial v}+\frac{\partial y}{\partial u}\frac{\partial x}{\partial v}\operatorname du\operatorname dv=\begin{vmatrix}\frac{\partial x}{\partial u}&amp;\frac{\partial x}{\partial v}\\\frac{\partial y}{\partial u}&amp;\frac{\partial y}{\partial v}\end{vmatrix}\operatorname du\operatorname dv$

La matriz de la cual calculamos el determinante es la matriz jacobiana del cambio de variables:

$J=\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}=\begin{pmatrix}\frac{\partial x}{\partial u}&amp;\frac{\partial x}{\partial v}\\\frac{\partial y}{\partial u}&amp;\frac{\partial y}{\partial v}\end{pmatrix}$

Por tanto nos queda la siguiente fórmula de cambio de variables en integrales dobles:

$\iint_Rf\left(x,y\right)\operatorname dx\operatorname dy=\iint_{R'}f\left(u,v\right)\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}\operatorname du\operatorname dv$

donde el recinto R se transforma en el recinto R' al hacer el cambio.

**Ejemplo 7**: calcular el volumen delimitado por la elipse C de ecuación *x²+y²/4 = 1* en el *cuadrante x>0, y>0* *, y el plano P de ecuación cartesiana* x - y + z - 1 = 0*.

En la figura vemos una representación: el plano oblicuo P forma la parte superior de la figura, mientras que la base es una elipse; las intersecciones del plano P con los planos XZ, YZ son las rectas z=1-x, z=y+1 respectivamente, la recta vertical en el plano YZ corresponde a la intersección de la elipse C con el plano x=0:


La región R de integración será el área del plano XY dentro de la elipse, mientras que para la función a integrar tomaremos la altura z sobre el plano XY, dada por la ecuación del plano P: *x - y + z - 1 = 0 => z = -x + y + 1 = f(x, y).  *El volumen será pues:

$V=\iint_R\left(y-x+1\right)\operatorname dx\operatorname dy$

Para simplificar la región R, planteamos el cambio u = x, v = y/2, que convierte a la elipse en un circunferencia de radio 1 de ecuación u² + v² = 1. Calculemos el Jacobiano del cambio: primero expresamos x, y como funciones de u,v: $u=x,\;v=\frac y2\Rightarrow x=u,\;y=2v$, ahora calculamos las derivadas parciales, la matriz* J* , y su determinante:

$J=\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}=\begin{pmatrix}\frac{\partial x}{\partial u}&amp;\frac{\partial x}{\partial v}\\\frac{\partial y}{\partial u}&amp;\frac{\partial y}{\partial v}\end{pmatrix}=\begin{pmatrix}1&amp;0\\0&amp;2\end{pmatrix}$

El determinante vale 2. La función f(x, y) expresada en las nuevas variables es:  $f\left(x,y\right)=y-x+1=2v-u+1=f\left(u,v\right)$, así que la integral que nos da el volumen queda:

$\iint_{R'}f\left(u,v\right)\cdot det(J)\cdot\operatorname du\operatorname dv=\iint_{R'}\left(2v-u+1\right)\cdot2\cdot\operatorname du\operatorname dv=\iint_{R'}\left(4v-2u+2\right)\operatorname du\operatorname dv$

La integral en el recinto circular sabemos que se simplifica mucho tomando coordenadas polares, así que hacemos un segundo cambio: $u=r\cos\left(\theta\right),\;y=r\sin\left(\theta\right)$, la circunferencia de radio 1 en polares se reduce a la ecuación r=1, y el cuadrante x>0, y>0 implica que $0\leq\theta\leq\pi/2$. El Jacobiano del cambio a polares es r:

$\left|J\right|=\left|\frac{\partial\left(u,v\right)}{\partial\left(r,\theta\right)}\right|=\begin{vmatrix}\frac{\partial rcos\left(\theta\right)}{\partial r}&amp;\frac{\partial rcos\left(\theta\right)}{\partial\theta}\\\frac{\partial rsin\left(\theta\right)}{\partial r}&amp;\frac{\partial rsin\left(\theta\right)}{\partial\theta}\end{vmatrix}=\begin{vmatrix}cos\left(\theta\right)&amp;-rsin\left(\theta\right)\\sin\left(\theta\right)&amp;rcos\left(\theta\right)\end{vmatrix}=rcos^2\left(\theta\right)+rsin^2\left(\theta\right)=r$

La función f(u, v) se transforma en $f\left(u,v\right)=2v-u+1=2r\sin\left(\theta\right)-r\cos\left(\theta\right)+1=r\left(2sin\left(\theta\right)-cos\left(\theta\right)\right)+1=f\left(r,\theta\right)$, y la integral se convierte en:

$\iint_{R'}\left(4v-2u+2\right)\operatorname du\operatorname dv=\iint_{R''}\left(r\left(2sin\left(\theta\right)-cos\left(\theta\right)\right)+1\right)\cdot r\cdot\operatorname dr\operatorname d\theta$

donde R'' es la región rectangular $0\leq r\leq1,\;0\leq\theta\leq\pi/2$. Calculamos
las integrales reiteradas:

$\iint_{R''}\left(r\left(2sin\left(\theta\right)-cos\left(\theta\right)\right)+1\right)\cdot r\cdot\operatorname dr\operatorname d\theta=\int_0^{\pi/2}\operatorname d\theta\int_0^1\left$r^2\left(2sin\left(\theta\right)-cos\left(\theta\right)\right)+r\right$\operatorname dr$

La integral respecto de r es:

$\begin{array}{l}\int_0^1\left$r^2\left(2sin\left(\theta\right)-cos\left(\theta\right)\right)+r\right$\operatorname dr=\left$\frac{r^3}3\left(2sin\left(\theta\right)-cos\left(\theta\right)\right)+\frac{r^2}2\right$_0^1=\\\frac{2sin\left(\theta\right)-cos\left(\theta\right)}3+\frac12\end{array}$

y respecto a θ:

$\begin{array}{l}\int_0^{\pi/2}\left(\frac{2sin\left(\theta\right)-cos\left(\theta\right)}3+\frac12\right)\operatorname d\theta=\left$\frac13\left(-2cos\left(\theta\right)-sin\left(\theta\right)\right)+\frac\theta2\right$_0^{\pi/2}=\\\frac13\left(0-\frac13\right)+\frac{\pi/2}2-\left(\frac13\left(-2+0\right)+0\right)=\boxed{\frac\pi4+\frac13}\end{array}.$

---

 
# Ejercicios propuestos

**1.** Calcular $\iint_Rcos^{-1}\left(x^2+y^2\right)\operatorname dx\operatorname dy$ siendo R la región interior delimitada por la la curva $\sqrt{\cos\left(\theta\right)}=\;r$ y el eje X:

[![regio2](/taller-matematicas/assets/images/regio2-300x142.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/08/regio2.png)

**2.** Calcular el volumen cortado en el [paraboloide](https://es.wikipedia.org/wiki/Paraboloide) x² + y² = z por el plano z = 2 + 2x + 2y.

**3**. Calcular el volumen interior a la superficie $x^\frac23+y^\frac23+z^\frac23=a^\frac23$  usando el cambio de variables x = r·cos²(θ), y = r·sin²(θ).
{% endraw %}