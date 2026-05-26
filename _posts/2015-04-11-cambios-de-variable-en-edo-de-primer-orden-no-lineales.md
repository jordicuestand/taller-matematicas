---
layout: post
title: "EDOs de primer orden no lineales, cambios de variable"
date: 2015-04-11 07:32:30 +0000
categories:
  - "Ecuaciones Diferenciales"
  - "Matemáticas"
tags:
  - "ecuación de Bernouilli"
  - "ecuación de Clairaut"
  - "ecuación de Lagrange"
  - "ecuación de Ricatti"
  - "ecuacíón diferencial no lineal"
math: true
---

**Introducción**
En este post vemos algunos métodos de cambio de variable para resolver ecuaciones diferenciales ordinarias no lineales; en general estas ecuaciones son difíciles de resolver, y muchas veces de hecho no existe una solución analítica, esto es, una función $y=f(x)$ explícita, que sea un polinomio, una función trigonométrica, exponencial, etc. o una combinación de las anteriores, por lo que hay que resolver la ecuación con métodos numéricos. Sólo en algunos casos especiales podemos obtener la solución analítica; incluso en estos casos, puede pasar que no podamos dar la el haz de curvas solución en forma explícita $y=f(C,x)$, sino en forma paramétrica $\phi\left(x,y,p,C\right)=0.$

¿Comentarios, preguntas? visitad [https://www.facebook.com/tallermatematic](https://www.facebook.com/tallermatematic).

 	- [Ecuaciones sin la y en la que se puede despejar* y*'](#sin_la_y)

 	- [Ecuaciones en las que se puede despejar *y*](#despejar_y)

 	- [Ecuaciones en las que se puede despejar *x*](#despejar_x)

 	- [Ecuaciones de Bernoulli, Ricatti, Lagrange y Clairaut](#bernoulli)

[*](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

## 

## Ecuaciones sin la *y* en la que se puede despejar* y*'

Este es el único caso en el que no aparece un cambio de variable, en principio: cuando la ecuación diferencial no contiene la función *y*,  $F(x,y',y'^2, ...,y^n) = 0$, y además puede ponerse en forma de un polinomio en *y'* tal como

$A_0+A_1y'+A_2y'^2+...+A_ny'^n=0$,

podemos intentar encontrar las raíces del polinomio, $y'_1=F_1(x,y), y'_2=F_2(x,y), ...,y'_n=F_n(x,y)$, y entonces plantear las *n* ecuaciones lineales $y'=F_1(x,y), y'=F_2(x,y), ...,y'=F_n(x,y)$.

**Ejemplo 1**: La ecuación $2y'^2-y'+x=0$ es un polinomio de segundo grado en y', que puede resolverse fácilmente:

$y'=\frac{1\pm\left(1-8x\right)^{1/2}}4$

tenemos dos ecuaciones separables:

$\begin{array}{l}\frac{\operatorname dy}{\operatorname dx}=\frac{1+\left(1-8x\right)^{1/2}}4\Rightarrow\int\operatorname dy=\int\frac{1+\left(1-8x\right)^{1/2}}4\operatorname dx\Rightarrow\\y=\int\frac14\operatorname dx+\frac14\frac1{-8}\int-8\left(1-8x\right)^{1/2}\operatorname dx=\frac14\left[x-\frac1{12}\left(1-8x\right)^{3/2}\right]+C\end{array}$

la otra ecuación es idéntica salvo en un signo, y resulta $y=\frac14\left[x+\frac1{12}\left(1-8x\right)^{3/2}\right]+C.$ Cada solución tiene su propio haz de curvas; en la figura se representa una curva de cada solución, para $C=0$.

[caption id="attachment_914" align="alignnone" width="465"][![Dos soluciones de 2y](/assets/images/no_lineal_ordinaria.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/03/no_lineal_ordinaria.png) Dos soluciones de 2y'² - y' + x = 0[/caption]

[![separador2](/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
## Ecuaciones en la que se puede despejar *y*

En este caso de la ecuación $F(x,y,y') = 0$ podemos despejar y, resultando $y=F(x,y')$. Se puede intentar la sustitución $y'=p$ que convierte la ecuación en $y=F(x,p)$; derivando respecto de x obtenemos $y'=p=F_x+F_p·p'$ donde la notación $F_x, F_p$ denotan las derivadas parciales de* F* respecto de *x,* p*. Despejando p' obtenemos $p'=\frac{p-F_x}{F_p}=\varphi\left(x,p\right)$ que es la misma ecuación diferencial pero con respecto a $p(x)$, con la derivada p' despejada, que puede ser más fácil de resolver.

**Ejemplo 2**: La ecuación $x^2y'^2-y=0$ permite despejar tanto y' como y; si despejamos y, con la sustitución $y'=p$, obtenemos $x^2p^2=y$, derivando respecto de x:

$\begin{array}{l}2xp^2+2x^2p\cdot p'=y'=p\Rightarrow2px\left(p+xp'\right)=p\Rightarrow2x\left(p+xp'\right)=1\Rightarrow\\p+xp'=\frac1{2x}\Rightarrow p'+\frac1xp=\frac1{2x^2}\end{array}$

que es una [ecuación diferencial lineal](http://tallermatematic.eu/wp/?p=897); la lineal homogénea es $p'+\frac1xp=0$, de variables separables:

$\begin{array}{l}p'+\frac1xp=0\Rightarrow\frac{\operatorname dp}{\operatorname dx}=-\frac1xp\Rightarrow\int\frac{\operatorname dp}p=-\int\frac{\operatorname dx}x\Rightarrow\\\ln\left(p\right)=-\ln\left(x\right)+C\Rightarrow p_h=\frac Cx\end{array}.$

La notación $p_h$ significa "solución de la ecuación homogénea" Para encontrar una solución particular de la ecuación completa, utilizamos el método de variación de constantes: $p=\frac{C\left(x\right)}x$; derivamos y sustituimos en la ecuación lineal:

$\begin{array}{l}\begin{array}{l}p'=\frac{C'\left(x\right)\cdot x-C\left(x\right)\cdot1}{x^2}=C'\left(x\right)\frac1x-C\left(x\right)\frac1{x^2};\\p'+\frac1xp=\frac1{2x^2}\Rightarrow\left[C'\left(x\right)\frac1x-C\left(x\right)\frac1{x^2}\right]+\frac1xC\left(x\right)\cdot\frac1x=\frac1{2x^2}\Rightarrow\end{array}\\C'\left(x\right)\frac1x=\frac1{2x^2}\Rightarrow\frac{\operatorname dC}{\operatorname dx}=\frac1{2x}\Rightarrow\int\operatorname dC=\int\frac1{2x}\operatorname dx=\frac12\int\frac1x\operatorname dx\Rightarrow\\C\left(x\right)=\frac12\ln\left(x\right).\end{array}$

La solución particular es pues $p=\frac{C\left(x\right)}x,\;C\left(x\right)=\frac12\ln\left(x\right)\;\Rightarrow p=\frac{\ln\left(x\right)}{2x}$ y la solución general se obtiene combinando la solución de la homogénea y la solución particular:

$p=C\frac1x+\frac{\ln\left(x\right)}{2x}$

Esta igualdad relaciona el parámetro p con la variable independiente x; añadiendo la igualdad $x^2p^2=y$ obtenemos la expresión del haz de curvas solución en paramétricas:

$\left\{\begin{array}{l}p=C\frac1x+\frac{\ln\left(x\right)}{2x}\\x^2p^2=y\end{array}\right.$

Tal como vienen dadas estas ecuaciones, para determinar los puntos $(x,y)$ de las curvas solución, damos valores a la variable independiente x, a continuación hallamos $p(x)$ con la primera ecuación, y por último hallamos $y(x,p)$ con la segunda ecuación:

[caption id="attachment_940" align="alignnone" width="739"][*](http://tallermatematic.eu/wp/wp-content/uploads/2015/04/parametricas.png) Algunos puntos (x,y) obtenidos de las ecuaciones paramétricas[/caption]

[![separador2](/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
## Ecuaciones en la que se puede despejar x*

Si no podemos despejar y pero sí la x, tendremos $x=F(y,y')$, la sustitución $y'=p$ convierte la ecuación en $x=F(y,p)$, per ahora consideraremos que p no es función de x, sino de y'; evidentemente, como y' es a su vez función de x, p también ha de ser función de x, pero lo será de forma implícita: $p(y)=p\left(y\left(x\right)\right)$.  Derivando  respecto de x toda la expresión$x=F(y,p)$ con la regla de la cadena y teniendo en cuenta las funciones implícitas y, p, obtenemos:

$\begin{array}{l}\frac{\operatorname dx}{\operatorname dx}=\frac{\partial F(y,p)}{\partial y}\cdot\frac{\operatorname dy}{\operatorname dx}+\frac{\partial F(y,p)}{\partial p}\cdot\frac{\operatorname dp}{\operatorname dy}\cdot\frac{\operatorname dy}{\operatorname dx}\Leftrightarrow\\1=F_y\cdot y'+F_p\cdot p'\cdot y'\\\end{array}$

donde la notación $F_x, F_p$ denotan las derivadas parciales de* F* respecto de *x,* *p*. Observar como al derivar $F(y,p)$ respecto de x realmente lo hacemos respecto de las variables y, p, pero siendo éstas últimas a su vez funciones de x, y respectivamente,  multiplicamos por sus derivadas respecto a x, y; por último, en el término $\frac{\partial F}{\partial p}F(y,p)\cdot\frac{\operatorname dp}{\operatorname
dy}\cdot\frac{\operatorname dy}{\operatorname dx}$ aparece tambien la derivada de y respecto de x. Esto no es más que la regla de la cadena de las derivadas:

$\frac{\operatorname d{}}{\operatorname dx}f\left(g\left(h\left(x\right)\right)\right)=\frac{\operatorname df\left(g\left(h\left(x\right)\right)\right)}{\operatorname dx}\cdot\frac{\operatorname dg\left(h\left(x\right)\right)}{\operatorname dx}\cdot\frac{\operatorname dh\left(x\right)}{\operatorname dx}$

Despejamos ahora p'  de la expresión derivada :

#### $\begin{array}{l}p'=\frac{\operatorname dp}{\operatorname dy}=\frac{1-F_y\cdot p}{F_p\cdot p}\\\end{array}$

que es una ecuación diferencial en p', con p' despejada y en la que falta la p, o sea el primer caso de este post.

**Ejemplo 3**: Sea la ecuación diferencial ordinaria no lineal $y'y=x$. Aplicando el cambio $y'=p$ la ecuación se convierte en $py=x$; derivando respecto x obtenemos:

$\frac{\operatorname dp}{\operatorname dy}\frac{\operatorname dy}{\operatorname dx}y+p\frac{\operatorname dy}{\operatorname dx}=\frac{\operatorname dx}{\operatorname dx}\Rightarrow p'py+p^2=1\Rightarrow p'=\frac{1-p^2}{py}$

que es separable: $\frac{\operatorname dp}{\operatorname dy}=\frac{1-p^2}{py}\Rightarrow\int\frac p{1-p^2}\operatorname dp=\int\frac1y\operatorname dy$, la primera integral es del tipo $\int\frac{f'\left(x\right)}{f(x)}=\ln\left(f\left(x\right)\right)$, la segunda es inmediata:

$\begin{array}{l}\int\frac p{1-p^2}\operatorname dp=-\frac12\int\frac{-2p}{1-p^2}\operatorname dp=-\frac12\ln\left(1-p^2\right);\\\int\frac1y\operatorname dy=\ln\left(y\right);\\\int\frac p{1-p^2}\operatorname dp=\int\frac1y\operatorname dy\Rightarrow-\frac12\ln\left(1-p^2\right)=\ln\left(y\right)+C\Rightarrow\\\ln\left(y\cdot\left(1-p^2\right)^{1/2}\right)=C\Rightarrow y\cdot\left(1-p^2\right)^{1/2}=C\Rightarrow\boxed{y=\frac C{\sqrt{1-p^2}}}\\\end{array}$

que junto con la igualdad $x=py$ nos da el haz de curvas solución en coordenadas paramétricas $\phi\left(x,y,p\right).$

**NOTA**: la ecuación de este último ejemplo es de variables separables y por tanto puede resolverse directamente:

$y'y=x\Leftrightarrow\int y\operatorname dy=\int x\operatorname dx\Rightarrow\frac{y^2}2=\frac{x^2}2+C\Rightarrow y^2-x^2=C.$

Además, en este caso podemos resolver explícitamente las ecuaciones paramétricas, obteniendo el mismo resultado:

$\begin{array}{l}\left.\begin{array}{r}y=\frac C{\sqrt{1-p^2}}\\x=py\end{array}\right\}\Rightarrow p=\frac xy\Rightarrow y=\frac C{\sqrt{1-{\displaystyle\frac{x^2}{y^2}}}}=\frac{Cy}{\sqrt{y^2-x^2}}\Rightarrow\\1=\frac C{\sqrt{y^2-x^2}}\Rightarrow\sqrt{y^2-x^2}\;=C.\end{array},$

pero en general, esto no será posible, y tendremos que dejar la solución en paramétricas, como veremos en el siguiente ejemplo.

**Ejemplo 4**: La ecuación $4y=x^2+(y')^2$ es del tipo "se puede despejar y"; probemos el cambio $y'=p$ que la transforma en $4y=x^2+p^2$. Derivando respecto de x: $4p=2x+2pp'$, que es del tipo $p'=F(x,p)$ con F homogénea de grado 0 (ver [Funciones homogéneas. Aplicación a las ecuaciones diferenciales](http://tallermatematic.eu/wp/?p=855#homogeneas)):

$\begin{array}{l}4p=2x+2pp'\Rightarrow p'=\frac{2p-x}p=F(x,p);\\F(\lambda x,\lambda p)=\frac{2\lambda p-\lambda x}{\lambda p}=\frac{2p-x}p=F(x,p)\end{array},$

con el cambio de variable $u=p/x$ se convierte en una ecuación de variables separadas:

$\begin{array}{l}u=p/x\Rightarrow u'=\frac{p'x-p}{x^2}\Rightarrow p'=\frac{x^2u'+p}x=\frac{x^2u'+ux}x=xu'+u;\\p'=\frac{2p-x}p\Leftrightarrow xu'+u=\frac{2ux-x}{ux}=\frac{2u-1}u\Rightarrow xu'=\frac{2u-1-u^2}u\Rightarrow\\\frac{\operatorname du}{\operatorname dx}=\frac{2u-1-u^2}{xu}\Rightarrow\int\frac u{2u-1-u^2}\operatorname du=\int\frac1x\operatorname dx\\\\\end{array}$

La primera integral es del tipo racional:

$\frac u{2u-1-u^2}=\frac u{-\left(u-1\right)^2}=-\frac A{u-1}-\frac B{\left(u-1\right)^2}=-\frac{A\left(u-1\right)+B}{\left(u-1\right)^2}$

sustituyendo el valor $u=1$ llegamos a $B=1$ y luego a $A=1$, por tanto:

$\int\frac u{2u-1-u^2}\operatorname du=-\int\frac1{u-1}\operatorname du-\int\frac1{\left(u-1\right)^2}\operatorname du=-\ln\left(u-1\right)+\frac1{u-1}$

Entonces:

$\begin{array}{l}\int\frac u{2u-1-u^2}\operatorname du=\int\frac1x\operatorname dx\Leftrightarrow-\ln\left(u-1\right)+\frac1{u-1}=\ln\left(x\right)+C\Rightarrow\\\ln\left(Cx\right)+\ln\left(u-1\right)=\frac1{u-1}\Rightarrow\ln\left(Cx\left(u-1\right)\right)=\frac1{u-1}\Rightarrow\\Cx=\frac{e^\frac1{u-1}}{u-1}.\end{array}$

Si deshacemos el cambio $u=p/x$ obtenemos:

$\begin{array}{l}Cx=\frac{e^\frac1{u-1}}{u-1}=\frac1{{\displaystyle\frac px}-1}exp\left(\frac1{\frac px-1}\right)=\frac x{p-x}exp\left(\frac x{p-x}\right)\Rightarrow\\\phi\left(x,p\right)=\frac1{p-x}exp\left(\frac x{p-x}\right)=C\end{array}$

que junto con la condición $y=(x^2+p^2)/4$ nos da el haz de curvas solución dependiente del parámetro p. Pero vemos que la función $\phi\left(x,p\right)$ no permite despejar x, por lo que es de difícil manejo; mejor en este caso dejar las ecuaciones paramétricas en función del parámetro u:

$\left.\begin{array}{r}x=C\frac{e^\frac1{u-1}}{u-1}\\y=\frac{x^2+\left(xu\right)^2}4=x^2\frac{1+u^2}4\end{array}\right\}$

[![separador2](/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

## Ecuaciones de Bernoulli, Ricatti, Lagrange y Clairaut

#### Ecuación de Bernoulli

Son de la forma $y'+X(x)y=F(x)\cdot y^n$ y pueden reducirse a lineales con el cambio de variable $v(x)=y^{1-n}$ siempre que n no sea ni 0 ni 1; si $n = 0$ entonces la ecuación es lineal.

**Ejemplo 5**: La ecuación $dy/dx-3y/2x=2x/y$ és de Bernoulli, con $P(x)=3/2x, Q(x)=2x,  n=-1$. El cambio $v=y^{2}$ transforma la ecuación:

$y=v^{1/2}\Rightarrow y'=\frac1{2v^{1/2}}\frac{\operatorname dv}{\operatorname dx}\Rightarrow\frac1{2v^{1/2}}v'-\frac{3v^{1/2}}{2x}=\frac{2x}{v^{1/2}}$

Multipliquemos todo por $2v^{1/2}$ para obtener $v'-\frac3xv=4x$ que és lineal. Resolvemos esta ecuación usando la fórmula general (ver el post [Ecuaciones diferenciales lineales de 1r orden](http://tallermatematic.eu/wp/?p=897)):

$y=e^{-\int X\left(x\right)\operatorname dx}\cdot\left[C+\int F(x)\cdot e^{\int X\left(x\right)\operatorname dx}\operatorname dx\right]$

en nuestro caso es:

$\begin{array}{l}\begin{array}{l}X(x)=-\frac3x,\;F(x)=4x\;\Rightarrow\int X\left(x\right)\operatorname dx=\int-\frac3x\operatorname dx=-3\ln\left(x\right),\\\int F(x)\cdot e^{\int X\left(x\right)\operatorname dx}=\int4x\cdot e^{-3\ln\left(x\right)}=\int4x\cdot x^{-3}=-4x^{-1},\\v(x)=e^{-\int X\left(x\right)\operatorname dx}\cdot\left[C+\int F(x)\cdot e^{\int X\left(x\right)\operatorname dx}\operatorname dx\right]=\end{array}\\e^{3\ln\left(x\right)}\cdot\left[C-4x^{-1}\right]=Cx^3-4x^2\end{array}$

deshacemos el cambio $v=y^{2}$ para obtener $y(x)=\pm\sqrt{Cx^3-4x^2}=\boxed{\pm x\sqrt{Cx-4}}.$
**Ejemplo 6**:  La ecuación $x\left(dy/dx\right)+6y=3xy^{4/3}$ no és separable, ni lineal, ni homogénea ni exacta, pero dividiéndola por x resulta $dy/dx+6y/x=3y^{4/3}$, que es una ecuación de Bernoulli con $n=4/3, P(x)=1/x,\: Q(x)=3$, aplicando el cambio  $v=y^{1-4/3}=y^{-1/3}$ se transformarà en lineal.

#### Ecuación de Ricatti

Son de la forma $dy/dx=P(x)y^2+Q(x)y+R(x)$; en el caso particular de que conozcamos una de sus soluciones particulares $y_p$ entonces el cambio $y=y_p+1/v$ la convertirá en lineal.

**Ejemplo 7**: La ecuación $y'+y^2=1+x^2$ es de Ricatti; sabiendo que una solución particular es $y=x$, aplicamos el cambio $y=x+1/v$, derivamos y sustituimos:

$\begin{array}{l}y=x+\frac1v\Rightarrow y'=1-\frac1{v^2}v';\\y'+y^2=1+x^2\Leftrightarrow1-\frac1{v^2}v'+\left(x+\frac1v\right)^2=1+x^2\Rightarrow\\1-\frac1{v^2}v'+x^2+\frac1{v^2}+2x\frac1v=1+x^2\Rightarrow
\v'-2xv=1\end{array}$

esta última ecuación es lineal en $v'$.

#### Ecuación de Lagrange

Son un caso particular de las ecuaciones en las que se pueden despejar $y$, tienen la forma $y=xF(y')+G(y')$. Se resuelven como hemos visto, con el cambio $y'=p$ que las transforma en lineales en p, siempre que se cumpla $p-F(p)\neq0$, condición que no se cumple en las ecuaciones de la forma $y=xy'+G(y')$, denominadas ecuaciones de Clairaut.

#### Ecuación de Clairaut

Tienen la forma $y=xy'+G(y')$ y su haz de curvas integral es directamente $y=Cx+G(x)$, fácil de comprobar derivando y sustituyendo en la ecuación.