---
layout: post
title: "Problemas de distribuciones de probabilidad continua"
date: 2015-05-27 16:10:23 +0000
categories:
  - "Estadística"
  - "Probabilidades"
tags:
  - "densidad de probabilidad"
  - "distribución de probabilidad"
math: true
---
{% raw %}

**P1)** Tenemos una distribución de probabilidad continua bidimensional (X,Y) con función de densidad:

$f\left(x,y\right)=\left\{\begin{array}{l}8xy,\;0&lt;x&lt;y&lt;1\\0\;\text{en otro caso}\end{array}\right.$

 	- Comprobar que la probabilidad total vale 1

 	- Calcular las densidades de probabilidad marginales $f_x(x), f_y(y)$. ¿Son independientes las variables X, Y?

 	- Calcular la media de X y la media de Y

 	- Hallar la probabilidad condicionada P( X>0.8 | Y < 0.4)

 	- Calcular la covariancia de las dos variables

 	- Calcular la correlación lineal de las dos variables

**Resolución:**
**1. Comprobar que la probabilidad total vale 1**

El dominio de definición D de la función de densidad es el triángulo delimitado por los puntos (0,0), (1,0) y (1,1) en el plano XY:

$caption id="attachment_1097" align="alignnone" width="555"$[![integra_area](/taller-matematicas/assets/images/integra_area.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/05/integra_area.png) Fig. 1: variación de Y en el dominio D: 0 < Y < X > 1

Para encontrar la probabilidad en todo el dominio calculamos la integral doble

$\iint_Df\left(x,y\right)\operatorname dx\operatorname dy$

La integral doble en el recinto la calculamos con integrales reiteradas, despejando una de las variables en función de la otra; en la imagen vemos que, fijando un valor x, la variable y varía desde y=0 hasta y=x, ya que el dominio es 0 < y < x < 1. Entonces tenemos:

$\begin{array}{l}\iint_Df\left(x,y\right)\operatorname dx\operatorname dy=\int_0^1\operatorname dx\int_0^x8xy\operatorname dy=\int_0^1\operatorname dx\left$8x\frac{y^2}2\right$_0^x=\\4\int_0^1x^4\operatorname dx=4\left$\frac{x^4}4\right$_0^1=1.\end{array}$

Efectivamente la probabilidad total es 1.
**2. Calcular las densidades de probabilidad marginales $f_x(x), f_y(y)$. ¿Son independientes las variables X, Y?**

Las densidades de probabilidad marginales:

$f_x\left(x\right)=\int f\left(x,y\right)\operatorname dy,\;f_y\left(y\right)=\int f\left(x,y\right)\operatorname dx$

representan las probabilidades de las variables X e Y por separado. Para la marginal de x integramos respecto a y,  los límites de integración para la variable y son (0,x), puede visualizarse en el gràfico de la figura 1: la línea vertical simboliza la variación de y dado un x cualquiera, desde altura cero hasta alcanzar la recta y=x:

$f_x\left(x\right)=\int_0^x8xy\operatorname dy=8x\left$\frac{y^2}2\right$_0^x=4x^3$

Para la marginal de y integramos respecto de x; los límites de integración los visualizamos ahora con una línia horizontal situada dentro del dominio D, desde el valor mínimo x=y sobre la recta hasta el valor máximo x=1:

$caption id="attachment_1106" align="alignnone" width="548"$[![area2](/taller-matematicas/assets/images/area2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/05/area2.png) Fig. 2: variación de X en el dominio D: 0 < y < x < 1

Por tanto la integral es:

$f_y\left(y\right)=\int_y^18xy\operatorname dx=8y\left$\frac{x^2}2\right$_y^1=4y\left(1-y^2\right)$

Como comprobación no necesaria pero instructiva, integrando cada función de densidad marginal, debe de dar 1 (suma de probabilidades):

$\begin{array}{l}\int_0^1f_y\left(y\right)\operatorname dy=\int_0^14y\left(1-y^2\right)\operatorname dy=4\left$\frac{y^2}2-\frac{y^4}4\right$_0^1=4\left(\frac12-\frac14\right)=1;\\\int_0^1f_x\left(x\right)\operatorname dx=\int_0^14x^3\operatorname dx=4\left$\frac{x^4}4\right$_0^1=1\end{array}$

Las variables X, Y no son independientes; si lo fueran , el producto de densidades marginales debería coincidir con la densidad de probabilidad conjunta:
$f\left(x,y\right)=f_x\left(x\right)\cdot f_y\left(y\right)\;\Leftrightarrow X,\;Y\;\text{independientes}$

cosa que no se cumple: $8xy\neq4x^3\cdot4y\left(1-y^2\right)\;\Rightarrow X,\;Y\;\text{dependientes}.$

 
**3. Calcular la media de X y la media de Y**

Cuando tenemos una distribución bidimensional y queremos calcular las medias de las variables, usamos las distribuciones marginales: $\mu_x=\int xf_x\left(x\right)\operatorname dx,\;\mu_y=\int yf_y\left(y\right)\operatorname dy$. o sea:

$\mu_x=\int_0^1x\cdot4x^3\operatorname dx=4\left$\frac{x^5}5\right$_0^1=\frac45,\;\mu_y=\int_0^1y\cdot4y\left(1-y^2\right)\operatorname dx=4\left$\frac{y^3}3-\frac{y^5}5\right$_0^1=\frac8{15}$

 
**4. Hallar la probabilidad condicionada P( X>0.8 | Y < 0.4).**

La probabilidad condicionada P( X>0.8 | Y < 0.4) es, por definición:

$P(\;X&gt;0.8\;\vert\;Y\;&lt;\;0.4)=\frac{P(\;X&gt;0.8\;\cap\;Y\;&lt;\;0.4)}{P(\;Y\;&lt;\;0.4)}$

El conjunto $X&gt;0.8\;\cap\;Y\;&lt;\;0.4$, teniendo en cuenta el dominio de definición $0&lt;x&lt;y&lt;1$, es un rectángulo:

[![area](/taller-matematicas/assets/images/area-300x165.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/05/area.png)

Entonces la probabilidad de la intersección es:

$\begin{array}{l}\begin{array}{l}P\left(X&gt;0.8\;\cap\;Y\;&lt;\;0.4\right)=\int_{0.8}^1\operatorname dx\int_0^{0.4}8xy\operatorname dy=8\int_{0.8}^1x\operatorname dx\left$\frac{y^2}2\right$_0^{0.4}=\end{array}\\4\cdot0.4^2\int_{0.8}^1x\operatorname dx=\frac{16}{25}\left$\frac{x^2}2\right$_{0.8}^1=\frac8{25}\left(1-0.8^2\right)=\frac{72}{625}\end{array}$

La probabilidad que falta es:

$P\left(Y\;&lt;\;0.4\right)=\int_0^{0.4}f_Y\left(y\right)\operatorname dy$

donde $f_Y$ es la densidad marginal de la variable Y:

$P\left(Y\;&lt;\;0.4\right)=\int_0^{0.4}4y\left(1-y^2\right)\operatorname dy=4\left$\frac{y^2}2-\frac{y^4}4\right$_0^{0.4}=0.2944$

Resultado: $P\left(X&gt;0.8\;\vert\;Y\;&lt;\;0.4\right)=\frac{\frac{72}{625}}{0.2944}\approx0.3913$
**5. Calcular la covariancia de las dos variables**

Usamos la formula $cov\left(X,Y\right)=\int_D\left(x-\mu_x\right)\left(y-\mu_y\right)f\left(x,y\right)\operatorname dx\operatorname dy$ sustituyendo:

$\begin{array}{l}cov\left(X,Y\right)=\int_D\left(x-\frac45\right)\left(y-\frac8{15}\right)8xy\operatorname dx\operatorname dy=\\8\int_0^1x\left(x-\frac45\right)\operatorname dx\int_0^xy\left(y-\frac8{15}\right)\operatorname dy=\\8\int_0^1x\left(x-\frac45\right)\left(\frac{x^3}3-\frac{4x^2}{15}\right)\operatorname dx=\frac4{225}\end{array}$

Si las variables hubieran sido independientes, entonces no seria necesario efectuar este cálculo, pues *la covariancia de dos variables independientes es cero*.
**6. Calcular la correlación lineal de las dos variables**

La correlación viene dada por el coeficiente de correlación de Pearson:  $r_{xy}=\frac{cov\left(X,Y\right)}{\sigma_x\sigma_y}$. Primero calculamos las varianzas de cada variable:

Para x:

$\begin{array}{l}\sigma_x^2=\int_0^1\left(x-\mu_x\right)^2f_x\left(x\right)\operatorname dx=E\left(X^2\right)-E^2\left(X\right)=\int_0^1x^2f_x\left(x\right)\operatorname dx-\left(\frac45\right)^2=\\\int_0^1x^2\cdot4x^3\operatorname dx-\frac{16}{25}=4\frac16-\frac{16}{25}=\frac2{75}\end{array}$

para y:

$\begin{array}{l}\sigma_y^2=\int_0^1\left(y-\mu_y\right)^2f_y\left(x\right)\operatorname dx=E\left(Y^2\right)-E^2\left(Y\right)=\int_0^1y^2f_y\left(y\right)\operatorname dy-\left(\frac8{15}\right)^2=\\\int_0^1y\cdot4y\left(1-y^2\right)\operatorname dx-\frac{64}{225}=\frac8{15}-\frac{64}{225}=\frac{56}{225}\end{array}$

Sustituimos:

$r_{xy}=\frac{\displaystyle\frac4{225}}{\sqrt{\displaystyle\frac2{75}}\sqrt{\displaystyle\frac{56}{225}}}=\frac1{\sqrt{21}}\approx0.22$

Esta es una correlación positiva ("al aumentar X, aumenta también Y") pero baja, debido a que la relación entre X, Y no es lineal.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

**P2)** **Función de densidad conjunta**. Sea la función de densidad conjunta $f(x,y)=\left\{\begin{array}{l}xy\;\text{si }0&lt;x&lt;1,\;0&lt;y&lt;1\\0\;\text{si no}\end{array}\right.$.

(a) Hallar las funciones de densidad marginales, (b) justificar si las variables X, Y son independientes, (c) calcular la covarianza de X, Y.

La marginal de x es:

$f_x\left(x\right)=\int_{-\infty}^\infty f(x,y)\operatorname dy=\left\{\begin{array}{l}\int_0^1xy\operatorname dy=x\left$\frac{y^2}2\right$_0^1=x\frac12\\\int_{-\infty}^00\operatorname dy+\int_1^\infty0\operatorname dy=0\end{array}\right.$

La marginal de y es:

$f_y\left(y\right)=\int_{-\infty}^\infty f(x,y)\operatorname dx=\left\{\begin{array}{l}\int_0^1xy\operatorname dx=y\left$\frac{x^2}2\right$_0^1=y\frac12\;\text{si }0&lt;y&lt;1\\\int_{-\infty}^00\operatorname dx+\int_1^\infty0\operatorname dx=0\end{array}\right.$

Si las variables X, Y son independientes, entonces el producto de densidades marginales ha de ser igual a la densidad conjunta, pero en este caso no se cumple:

$f_x\left(x\right)\cdot f_y\left(y\right)=\left\{\begin{array}{l}x\frac12y\frac12=xy\frac14\;\text{si }0&lt;y&lt;1\\0\cdot0=0\end{array}\right.$

La covarianza es: $Cov\left(X,Y\right)=\int_{-\infty}^\infty\operatorname dx\int_{-\infty}^\infty\operatorname dy\cdot\left(x-\mu_x\right)\left(y-\mu_y\right)f\left(x,y\right)$, donde $\mu_x,\mu_y$ son los valores medios marginales, que calculamos aparte:

$\begin{array}{l}\mu_x=\int_0^1x\cdot f_x(x)\operatorname dx=\int_0^1x\frac12x\operatorname dx=\left$\frac{x^3}6\right$_0^1=\frac16;\\\mu_y=\int_0^1y\cdot f_y(y)\operatorname dy=\int_0^1y\frac12y\operatorname dy=\left$\frac{y^3}6\right$_0^1=\frac16;\end{array}$

Sustituyendo:

$\begin{array}{l}Cov\left(X,Y\right)=\int_0^1\operatorname dx\int_0^1\operatorname dy\cdot\left(x-\frac16\right)\left(y-\frac16\right)xy=\\\int_0^1\operatorname dx\int_0^1\operatorname dy\cdot\left(x^2y^2-\frac16x^2y-\frac16xy^2+\frac1{36}xy\right)=\\\int_0^1\operatorname dx\left(x^2\frac13-\frac16x^2\frac12-\frac16x\frac13+\frac1{36}x\frac12\right)=\\\frac13\left(\frac13-\frac1{12}\right)+\frac12\left(-\frac1{18}+\frac1{72}\right)=\frac1{16}\end{array}$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

**P3).** **Probabilidad condicionada en funciones de densidad de probabilidad**. Una variable aleatoria continua X tiene por función de densidad $f(x)=kx(1-x)$ siempre que $0&lt;x&lt;1$, valiendo cero en caso contrario. Calcular la probabilidad condicionada $P(X&gt;1/3 | X&gt;1/4)$. ¿Cuál es su varianza?

Por definición, $P(X&gt;\frac13\vert X&gt;\frac14)=\frac{P\left(\left(X&gt;\frac13\right)\cap\left(X&gt;\frac14\right)\right)}{P\left(X&gt;\frac14\right)}=\frac{P\left(X&gt;\frac13\right)}{P\left(X&gt;\frac14\right)}$, ya que $\left(X&gt;\frac13\right)\Rightarrow\left(X&gt;\frac14\right).$ Para calcular las probabilidades usamos la función de densidad:

$\begin{array}{l}P\left(X&gt;\frac13\right)=\int_\frac13^1kx(1-x)\operatorname dx=k\left$\frac{x^2}2-\frac{x^3}3\right$_\frac13^1=k\frac{10}{81};\\P\left(X&gt;\frac14\right)=\int_\frac14^1kx(1-x)\operatorname dx=k\left$\frac{x^2}2-\frac{x^3}3\right$_\frac14^1=k\frac9{64};\end{array},$

luego:

$P(X&gt;\frac13\vert X&gt;\frac14)=\frac{P\left(X&gt;\frac13\right)}{P\left(X&gt;\frac14\right)}=\frac{k\frac10{81}}{k\frac9{64}}=\frac{640}{729}$

Para calcular la varianza usamos la igualdad $Var\left(X\right)=\int\left(x-\mu_x\right)^2f\left(x\right)\operatorname dx$; calculamos primero el valor medio de X:

$\mu_x=\int xf\left(x\right)\operatorname dx=\int_0^0x\cdot kx(1-x)=k\left$\frac{x^3}3-\frac{x^4}4\right$_0^1=k\left(\frac13-\frac14\right)=\frac k{12}$

Para determinar el valor de k usamos la condición de normalización de la función de densidad de probabilidad:

$\int f\left(x\right)\operatorname dx=1\Rightarrow\int_0^1kx(1-x)=k\left$\frac{x^2}2-\frac{x^3}3\right$_0^1=k\left(\frac12-\frac13\right)=\frac k6\Leftrightarrow k=6$

Ya podemos calcular la varianza:

$\begin{array}{l}Var\left(X\right)=\int\left(x-\mu_x\right)^2f\left(x\right)\operatorname dx=\int_0^1\left(x-\frac12\right)^2\cdot6x(1-x)\operatorname dx=\\6\int_0^1\left(-x^4+2x^3-\frac{5x^2}4+\frac x4\right)\operatorname dx=6\left$-\frac{x^5}5+2\frac{x^4}4-\frac54\frac{x^3}3+\frac14\frac{x^2}2\right$_0^1=\\\frac1{120}\end{array}$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

**P4).** **Función de densidad conjunta**. Una variable aleatoria continua X tiene por función de densidad:

$f(x)=\left\{\begin{array}{l}e^{1-x}\;\text{si }x\geq1\\0\;\text{si }x&lt;1\end{array}\right.$
En un experimento aleatorio con esa variable, tomamos dos medidas independientes entre sí, $x_1, x_2$; si consideramos una nueva variable aleatoria bidimensional Z formada por los valores anteriores, ¿cuál será su función de densidad de probabilidad? Definimos el estadístico T(z) = mínimo {$x_1, x_2$}; calcular la probabilidad P(T > t) para cualquier valor t real. ¿Cuál es la función de densidad de probabilidad de T(z)?

Siendo los valores $x_1, x_2$ independientes entre sí, la densidad de probabilidad conjunta del valor $(x_1, x_2)$ será el producto de densidades; llamemos $z=(x,y)$ por comodidad, entonces:

$f(x,y)=\left\{\begin{array}{l}e^{1-x}e^{1-y}\;\text{si }x,y\geq1\\0\;\text{si }x&lt;1\;\text{o }y&lt;1\end{array}\right.$

Calculemos ahora P(T > t):

$\begin{array}{l}T&gt;t\Leftrightarrow min\left\{x,y\right\}&gt;t\Rightarrow\left(x&gt;t\right)\cap\left(y&gt;t\right);\\P\left(T&gt;t\right)=P\left(\left(x&gt;t\right)\cap\left(y&gt;t\right)\right)=P\left(x&gt;t\right)\cdot P\left(y&gt;t\right)\end{array}$

Usando la función de densidad:

$P\left(x&gt;t\right)=\int_t^\infty e^{1-x}\operatorname dx=e\left$-e^{-x}\right$_t^\infty=e\left(0+e^{-t}\right)=e^{1-t}$

siempre que $t\geq1$, y cero en otro caso; para la $P\left(y&gt;t\right)$ obtenemos el mismo valor, por tanto: $P\left(T&gt;t\right)=e^{1-t}\cdot e^{1-t}=e^{2-2t}.$

Por definición de la función de distribución $F(t)$ tenemos que $F(t)=P(T&lt;t)=1-P(T&gt;t)=1-e^{2-2t}.$ Pero la derivada de la función de distribución es la función de densidad, así que:

$f\left(t\right)=\frac{\operatorname d{}}{\operatorname dt}F(t)=\frac{\operatorname d{}}{\operatorname dt}\left(1-e^{2-2t}\right)=2e^{2-2t}.$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
{% endraw %}