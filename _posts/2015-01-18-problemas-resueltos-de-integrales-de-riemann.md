---
layout: post
title: "Problemas resueltos de integrales de Riemann"
date: 2015-01-18 11:33:49 +0000
math: true
---
{% raw %}

**1.** Calcular la derivada de la función $f\left(x\right)=\int_1^{x^2-2}t^2\operatorname{d}t.$

Definimos la función $g\left(x\right)=\int_1^xt^2\operatorname{d}t,$ entonces podemos expresar $f(x)$ como una composición de funciones: $g\left(x^2+2\right)=g\left(x\right)\circ\left(x^2+2\right)=\int_1^{x^2+2}t^2\operatorname{d}t=f\left(x\right).$ Derivamos esta expresión usando la regla de la cadena:

$\begin{array}{l}D_x\left$g\left(x\right)\circ\left(x^2+2\right)\right$=\left(D_xg\left(x\right)\right)\circ\left(x^2+2\right)+g\left(x\right)\circ D\left(x^2+2\right)\\=\left(D_x\int_1^xt^2\operatorname{d}t\right)\circ\left(x^2+2\right)\cdot D\left(x^2+2\right)\\=x^2\circ\left(x^2+2\right)\cdot\left(2x\right)=\\=2x\left(x^2+2\right)^2.\end{array}$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

 

**2.** Sea $f(t)$ una función continua, y $g\left(x\right)=\int_0^xx^2f\left(t\right)\operatorname{d}t.$ Calcular $g'(x).$

En la integral $\int_0^xx^2f\left(t\right)\operatorname{d}t$ la variable de integración es "t" y no "x", luego "x" actúa como una constante en la integral, y podemos escribirla como $\int_0^xx^2f\left(t\right)\operatorname{d}t=x^2\int_0^xf\left(t\right)\operatorname{d}t.$ Derivamos respecto a "x":

$\begin{array}{l}D_x\left$x^2\int_0^xf\left(t\right)\operatorname{d}t\right$=D_x\left$x^2\right$\cdot\int_0^xf\left(t\right)\operatorname{d}t+x^2\cdot D_x\left$\int_0^xf\left(t\right)\operatorname{d}t\right$\\=2x\cdot\int_0^xf\left(t\right)\operatorname{d}t+x^2\cdot f\left(x\right).\end{array}$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)**3.** Calcular el área de la región delimitada por la gráfica de $y=x-x^3$, el eje de abscisas, y el intervalo $x\in\left$-1,1\right$.$

El área que nos piden viene dada por $A=\int_{-1}^1\left|x-x^3\right|\operatorname{d}x;$ para obtener el valor absoluto habrá que tener en cuenta el signo de $f(x)$ en el intervalo. Para ello:

a) encontramos si hay raíces de $y=x-x^3=0$ en el intervalo:

$x-x^3=0\Leftrightarrow x\left(1-x^2\right)=0\Leftrightarrow\left\{\begin{array}{l}x=0\\1-x^2\Leftrightarrow x=\pm1\end{array}\right.$

b) verificamos el signo en los subintervalos $[-1,0],[0,1]:$

en $[-1,0]$ tenemos que $\left|x^3\right|&lt;left|x\right|$, y $x&lt;0$, luego $f(x)&lt;0$

en $[0,1]$ tenemos que $\left|x^3\right|&lt;left|x\right|$, y $x&gt;0$, luego $f(x)&gt;0$

Por tanto:

$\begin{array}{l}A=\int_{-1}^1\left|x-x^3\right|\operatorname{d}x=\int_{-1}^0-\left(x-x^3\right)\operatorname{d}x+\int_0^1\left(x-x^3\right)\operatorname{d}x\\=-\left$\frac{x^2}2-\frac{x^4}4\right$_{-1}^0+\left$\frac{x^2}2-\frac{x^4}4\right$_0^1\\=-\left(-\frac12+\frac14\right)+\left(\frac12-\frac14\right)=1-2\frac14=\frac12.\end{array}.$

[![exer3_integral_Riemann](/taller-matematicas/assets/images/exer3_integral_Riemann-300x185.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/exer3_integral_Riemann.png)[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)**4.** Usando el teorema del valor medio integral, dar una aproximación al valor del área de la región comprendida entre la gráfica de $y=1/Ln(x)$, el eje de abscisas y el intervalo $x\in\left$2,3\right$.$

El área es $A=\int_2^3\left|\frac1{\ln\left(x\right)}\right|\operatorname{d}x,$ como la función es positiva para $x&gt;1$, el valor absoluto puede ignorarse; pero por otro lado no existe la expresión analítica de la primitiva $\int\frac1{\ln\left(x\right)}.$

[![exer4_integral_Riemann](/taller-matematicas/assets/images/exer4_integral_Riemann.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/exer4_integral_Riemann.png)

El teorema del valor medio integral nos dice que si la función es integrable (y lo es pues es continua en el intervalo dado), entonces existe un punto $c\in\left$2,3\right$$  tal que $f(c)=\frac1{3-2}\int_2^3\frac1{\ln\left(x\right)}\operatorname{d}x\Leftrightarrow\int_2^3\frac1{\ln\left(x\right)}\operatorname{d}x=f(c).$ Podemos aproximar este valor tomando algunos valores $y=f(x)$ y promediándolos; tomando 10 valores equidistantes en el intervalo $\left$2,3\right$$ obtenemos:

 

| **x** 
| 2,00 
| 2,11 
| 2,22 
| 2,33 
| 2,44 
| 2,56 
| 2,67 
| 2,78 
| 2,89 
| 3,00 

| **1/ln(x)** 
| 1,44 
| 1,34 
| 1,25 
| 1,18 
| 1,12 
| 1,07 
| 1,02 
| 0,98 
| 0,94 
| 0,91 

El promedio de los valores $1/ln(x)$ es $11.25/10=1.125$, tomamos este valor: $f(c)\approx1.125\Leftrightarrow A=\int_2^3\frac1{\ln\left(x\right)}\operatorname{d}x\approx1.125.$ El valor obtenido mediante algoritmos de cálculo numérico es 1.11842, el error cometido en nuestra aproximación es del orden de centésimas.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)**5.** Calcular el área de la región delimitada por la gráfica de la elipse $\left(\frac x3\right)^2+\left(\frac y2\right)^2=1$ y la región  $x&gt;2.$

Tenemos que encontrar el intervalo de integración, que no viene dado en este enunciado; para ello encontramos la intersección de dos àreas: la del interior de la elipse, $\left(\frac x3\right)^2+\left(\frac y2\right)^2&lt;1,$ y la dada $x&gt;2.$ La ecuación de la elipse que nos dan es la centrada en el origen de ejes $a,b$ tal como $\left(\frac xa\right)^2+\left(\frac yb\right)^2=1,$ esto significa que $a=3,b=2$ y que $-3&lt;x&lt;3.$ Imponiendo además que $x&gt;2$ nos queda el intervalo de integración $(2,3):$

$caption id="attachment_763" align="alignnone" width="300"$[![Àrea de la región delimitada por la elipse y la región x>2](/taller-matematicas/assets/images/area_elipse-300x247.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/area_elipse.png) Àrea de la región delimitada por la elipse y la región x>2[/caption]

Hay de hecho dos sub-regiones en el intervalo $(2,3)$ que se corresponden con dos funciones:

$\begin{array}{l}\left(\frac x3\right)^2+\left(\frac y2\right)^2=1\Leftrightarrow y=\pm2\sqrt{1-\left(\frac x3\right)^2};\\y_1=+2\sqrt{1-\left(\frac x3\right)^2},y_2=-2\sqrt{1-\left(\frac x3\right)^2,}\end{array}$

entonces el área total será la suma de las dos sub-regiones:

$\begin{array}{l}A=\int_2^3\left|y_1\right|+\int_2^3\left|y_2\right|=\int_2^32\sqrt{1-\left(\frac x3\right)^2}+\int_2^32\sqrt{1-\left(\frac x3\right)^2}\\=2\int_2^32\sqrt{1-\left(\frac x3\right)^2}=4\int_2^3\frac{\sqrt{9-x^2}}3=\frac43\int_2^3\sqrt{9-x^2}\end{array}.$

La función primitiva (integral indefinida) la hacemos aparte:

$\begin{array}{l}\begin{array}{l}I=\int\sqrt{9-x^2}=\int\sqrt{9-9\left(\frac x3\right)^2}=3\int\sqrt{1-\left(\frac x3\right)^2};\\\frac x3=\sin\left(t\right);1-\left(\frac x3\right)^2=\cos^2\left(t\right);\frac{\operatorname{d}x}3=\cos\left(t\right)\operatorname{d}t\Rightarrow\end{array}\\I=3\int\cos\left(t\right)\cdot3\cos\left(t\right)\operatorname{d}t=9\int\cos^2\left(t\right)\operatorname{d}t\end{array}$

Usamos el método de integración por partes: $\begin{array}{l}I=\int\cos^2\left(t\right)\operatorname{d}t=\sin(t)\cos(t)+\int\sin^2(t)\operatorname{d}t\\\left\{u=\cos(t);\;dv=\cos(t)\operatorname{d}t;\operatorname{d}u=-\sin(t)\operatorname{d}t;v=\sin(t)\right\}\\I=\sin(t)\cos(t)+\int\left(1-\cos^2(t)\operatorname{d}t\right)=t-I\Leftrightarrow\\I=\frac12\left(t+\sin(t)\cos(t)\right)=\frac12\left(t+\sin(t)\sqrt{1-\sin^2(t)}\right)\end{array}.$

Deshaciendo el cambio $t=\sin(t)$ y aplicando los límites de integración:

$\begin{array}{l}\left$\frac92\left(\sin^{-1}\left(\frac x3\right)+\left(\frac x3\right)\sqrt{1-\left(\frac x3\right)^2}\right)\right$_2^3=\\\frac92\left$\sin^{-1}\left(1\right)+0-\sin^{-1}\left(\frac23\right)-\left(\frac23\right)\frac{\sqrt5}3\right$=\end{array}$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)**6.** Sea una función $f(x)$ continua y definamos $F(x)=\int_0^tf(t)\operatorname{d}t$. Valorar si son ciertas o falsas las siguientes proposiciones, dando algún ejemplo o contraejemplo en cada caso.

*P1) Si $f$ es creciente para $x&gt;0$ entonces $F$ también es creciente para $x&gt;0$ *

*P2) Si $f$ es no negativa para $x&gt;0$ entonces $F$ es creciente para $x&gt;0$*

*P3) Si $f$ es no negativa para $x&gt;0$ entonces $F$es no negativa para $x&gt;0$*

Proposición 1: Por el primer *teorema fundamental del cálculo* (ver por ejemplo [Funciones integrables](http://tallermatematic.eu/wp/?p=674) -> Teorema 3) tenemos que $F(x)=\int_0^tf(t)\operatorname{d}t\Leftrightarrow F'(x)=f(x),$ así pues, la derivada de $F(x)$ es $f(x)$. La primera proposición dice que si la derivada es creciente, la función también los será; bien, si la derivada es creciente significa que la tangente a $F(x)$ en cada punto tiene una pendiente creciente con $x$, pero para saber si $F(x)$ es creciente hemos de fijarnos en el signo de la derivada, que no sabemos. En principio pues no tiene porqué ser cierto. Como contraejemplo que contradice la proposición, podemos pensar en una derivada $f(x)$ creciente pero con valores  negativos: sea $f(x)=-1/(x+1),$ que para $x\in\left(0,\infty\right)$ es siempre negativa, y en el límite $x\rightarrow\infty$ vale cero (queda como ejercicio comprobar que es creciente para todo $x&gt;0$); como la derivada es siempre negativa, la función $F(x)$ debe de ser decreciente, en efecto,  $F(x)=\int_0^x-\frac1{t+1}\operatorname{d}t=-\left$\ln\left(t+1\right)\right$_0^x=-\ln\left(x+1\right),$ que es estrictamente decreciente:

$caption id="attachment_782" align="alignnone" width="464"$[![Exer6_problemes_integrals](/taller-matematicas/assets/images/Exer6_problemes_integrals.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/Exer6_problemes_integrals.png) Función decreciente (azul) con derivada creciente (rojo)[/caption]

Proposición 2: Si la derivada $f(x)$ es positiva, entonces la función primitiva $F(x)$ es creciente; esto es una consecuencia de las propiedades de la derivada: ver por ejemplo [Aplicaciones de las derivadas](http://tallermatematic.eu/wp/?p=547) -> Teorema 3 del incremento finito -> Aplicación práctica: crecimiento y decrecimiento). La proposición es verdadera.

Proposición 3: Si la derivada $f(x)$ es positiva, no sabemos nada acerca del signo de la función primitiva $F(x)$; podemos imaginar un contraejemplo en que la función $F(x)$ es creciente (luego su derivada es positiva) pero toma valores negativos: $F(x)=x^2-4,\;F'(x)=f(x)=2x$ cumple la condición, ya que $F(x)&lt;0$ para $0&lt;x&lt;2$ pero $f(x)=2x&gt;0$ para $x&gt;0$. La proposición es pues falsa.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
 **7**. Calcular: (a) $I=\int_0^2\ln\left(x\right)\operatorname{d}x,$ (b) el área de la región delimitada por el intervalo $x\in(0,2)$ y la gráfica de la función $f(x)=ln\left(x\right).$

Para encontrar una primitiva para la función logaritmo, hacemos el cambio de variable $x=e^t$, con lo cual:

$\int\ln\left(x\right)\operatorname{d}x=\int\ln\left(e^t\right)\operatorname{d}\left(e^t\right)=\int te^t\operatorname{d}$

Ahora integramos por partes:

$\begin{array}{l}\operatorname{d}v=e^t\operatorname{d}t\Rightarrow v=e^t;u=t\Rightarrow\operatorname{d}u=\operatorname{d}t;\\\int te^t\operatorname{d}t=te^t-\int e^t\operatorname{d}t=e^t\left(t-1\right);\end{array}$

Deshacemos el cambio:

$\begin{array}{l}x=e^t\Rightarrow t=\ln\left(x\right);\\e^t\left(t-1\right)=e^{\ln\left(x\right)}\left(\ln\left(x\right)-1\right)=x\left(\ln\left(x\right)-1\right).\end{array}$

Cuando aplicamos los límites de integración obtenemos una indeterminación: $I=\int_0^2\ln\left(x\right)\operatorname{d}x=\left$x\left(\ln\left(x\right)-1\right)\right$_0^2=2\left(\ln\left(2\right)-1\right)-0\left(\ln\left(0\right)-1\right),$ pues la función $\ln\left(x\right)$ no està definida en $x=0$, o equivalentemente, $\lim_{x\rightarrow0}\ln\left(x\right)=-\infty:$ la integral es impropia de segunda especie (ver [aplicaciones de la integral ->integrales impropias](http://tallermatematic.eu/wp/?p=706#impropias)). La calculamos siguiendo el método estándar:

$\begin{array}{l}I=\lim_{\varepsilon\rightarrow0}\int_\varepsilon^2\ln\left(x\right)\operatorname{d}x=\lim_{\varepsilon\rightarrow0}\left$x\left(\ln\left(x\right)-1\right)\right$_0^\varepsilon=2\left(\ln\left(2\right)-1\right)-\lim_{\varepsilon\rightarrow0}\varepsilon\left(\ln\left(\varepsilon\right)-1\right);\\\lim_{\varepsilon\rightarrow0}\varepsilon\left(\ln\left(\varepsilon\right)-1\right)=\lim_{\varepsilon\rightarrow0}\left(\varepsilon\ln\left(\varepsilon\right)-\varepsilon\right)=\lim_{\varepsilon\rightarrow0}\varepsilon\ln\left(\varepsilon\right)=0\cdot\left(-\infty\right)=?\\\end{array}$

La indeterminación puede resolverse por L'Hôpital:

$\begin{array}{l}\\\lim_{\varepsilon\rightarrow0}\varepsilon\ln\left(\varepsilon\right)=\lim_{\varepsilon\rightarrow0}\frac{\ln\left(\varepsilon\right)}{1/\varepsilon}=-\frac\infty\infty\\=\lim_{\varepsilon\rightarrow0}\frac{D_\varepsilon\left(\ln\left(\varepsilon\right)\right)}{D_\varepsilon\left(1/\varepsilon\right)}=\lim_{\varepsilon\rightarrow0}\;\frac{1/\varepsilon}{-1/\varepsilon^2}=\lim_{\varepsilon\rightarrow0}-\varepsilon=0.\\\end{array}$

Por tanto nos queda la respuesta al apartado a: $I=2\left(\ln\left(2\right)-1\right)-0\approx-0.6137.$

En el apartado b nos piden un área, que será: $A=\int_0^2\left|\ln\left(x\right)\right|\operatorname{d}x.$ En el intervalo $(0,2)$ la función logaritmo tiene una raíz en $x=1$, toma valores negativos en $(0,1)$ y positivos en $(1,2)$, luego:

$\begin{array}{l}A=\int_0^2\left|\ln\left(x\right)\right|\operatorname{d}x=-\int_0^1\ln\left(x\right)\operatorname{d}x+\int_1^2\ln\left(x\right)\operatorname{d}x\\=-\left$1\left(\ln\left(1\right)-1\right)\right$+\left$2\left(\ln\left(2\right)-1\right)-1\left(\ln\left(1\right)-1\right)\right$\\=2\left(\ln\left(2\right)-1\right)-2\left(\ln\left(1\right)-1\right)=2\left(\ln\left(2\right)-\ln\left(1\right)\right)=2\ln\left(2\right)=1.3863\end{array}$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
{% endraw %}