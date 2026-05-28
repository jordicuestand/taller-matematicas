---
layout: post
title: "Ecuaciones diferenciales ordinarias de 1r orden"
date: 2015-02-22 17:46:06 +0000
categories:
  - "Ecuaciones Diferenciales"
  - "Matemáticas"
tags:
  - "ecuación diferencial ordinaria"
  - "Ecuaciones exactas"
  - "Ecuaciones separables"
  - "envolvente de un haz de curvas"
  - "Funciones homogéneas"
  - "Soluciones singulares"
math: true
---
{% raw %}

- [Ecuaciones separables](#separables)

 	- [Soluciones singulares](#singulares)

 	- [Curva envolvente de un haz de curvas](#envolvente)

 	- [Funciones homogéneas. Aplicación a las ecuaciones diferenciales](#homogeneas)

 	- [Ecuaciones exactas](#exactas)

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
## Ecuaciones separables

Las ecuaciones diferenciales separables son las de la forma $dy / dx = H (x, y)$ donde $H (x, y)$  se puede expresar bien como el cociente $H (x, y) = f (x) / g (y)$  o bien como el producto $H (x, y) = f (x) \text {·} g (y)$.

En el primer caso, $dy / dx = f (x) / g (y) \Rightarrow g (y) dy = f (x) dx \Rightarrow \int g (y) dy = \int f (x) dx + C$, mientras que en el segundo caso $dy/dx=f(x) \text{·}g(y) \Rightarrow g^{-1}(y)dy=f(x)dx \Rightarrow \int g^{-1}(y)dy = \int f(x)dx+C.$

**Ejemplo 1**: Resolver la ecuación diferencial $x^{2}\frac{dy}{dx}=\frac{x^{2}+1}{3y^{2}+1}.$
Tomemos $H(x,y)=\frac{\left(x^{2}+1\right)/x^{2}}{3y^{2}+1}=\frac{f(x)}{g(y)}$ de forma que $\int f(x)dx=\int\frac{x^{2}+1}{x^{2}}dx=x-\frac{1}{x},
\int g(y)dy=\int\left(3y^{2}+1\right)dy=y^{3}+y$ y por tanto la solución vendrá dada de forma implícita por $y^{3}+y=x-\frac{1}{x}+C.$

**Ejemplo 2**: encontrar todas las soluciones de la ecuación $dy/dx=2x\sqrt{y-1}.$

Hagamos $H(x,y) = 2x \sqrt{y-1} = f(x) \text{·}g(y),$ e integremos cada función: $\int f(x)dx=\int2xdx=x^{2};
\int g^{-1}(y)dy=\int\frac{1}{\sqrt{y-1}}dy=2\sqrt{y-1}.$ Las soluciones son $2\sqrt{y-1}=x^{2}+C\Rightarrow y=\left(\frac{x^{2}+C}{2}\right)^{2}+1
.$ Observemos que la función $y (x) = 1$   también es solución de la ecuación, pero no está incluida en la solución general $y = \left ( \frac {x ^ {2} + C} {2} \right) ^ {2} +1,$  es decir que para todo *C* tendremos $y = \left (\frac {x ^ {2} + C} {2} \right) ^ {2} +1 \neq1$. Llamamos a las soluciones no incluidas en la solución general **soluciones singulares** de la ecuación diferencial.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

## Soluciones singulares

En el ejemplo 2 hemos visto que podemos tener soluciones que no están incluidas en la solución general, llamadas soluciones singulares. ¿Cuándo sucederá esto y cómo podemos encontrar esas otras soluciones? Recordemos lo visto en el post [Ecuaciones diferenciales ordinarias: introducción](http://tallermatematic.eu/wp/?p=844), apartado "Haz de curvas y ecuaciones diferenciales de primer orden": la solución general de la ecuación diferencial ordinaria $y'=F(x,y)$ representa un haz de curvas $y=f(C,x)$ tal que cada curva de ese haz cumple la ecuación, o sea que para cada punto $(x,y)$ la pendiente de cualquiera de las curvas $y=f(C,x)$ en ese punto cumple $y'=F(x,y)$.

### Curva envolvente de un haz de curvas y solución singular

$caption id="attachment_868" align="alignnone" width="436"$[![Dos rectas de un haz (azul y rojo) y curva envolvente del haz (verde)](/taller-matematicas/assets/images/Feix_corbes_env1.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/02/Feix_corbes_env1.png) Dos rectas de un haz (azul y rojo) y curva envolvente del haz (verde)
Dado un haz de curvas $F(x,y,C)=0$ se denomina curva envolvente del haz a la curva $f(x,y)$ tal que es tangente a todas las curvas del haz.

**Ejemplo 3**: en la imagen se muestran dos rectas del haz de rectas $y=(1-10/C)*x+(10-C)$, concretamente las dos rectas correspondientes a los valores $C=3$ en rojo y $C=6$ en azul, y la curva envolvente del haz, que es tangente a la primera recta en un punto cercano a $x=1, y=5$ y a la segunda recta cerca de $x=3.5, y=1.5$.

Recordemos que podemos asociar a cualquier haz de curvas $F(x,y,C)=0$ una ecuación diferencial $y'=f(x,y)$ tal que el haz es la solución general de la ecuación: para cada valor de C, tenemos una curva del haz tal que su derivada verifica$y'=f(x,y)$. Pero hemos visto que la curva envolvente es tangente a todas las curvas del haz, o sea que su derivada en cada punto coincide con la derivada de alguna de las curvas del haz; es por esto que la curva envolvente es también solución de la ecuación diferencial del haz.

**Ejemplo 4**. Consideremos el haz de parábolas $4y=(x + C)^2$, todas las curvas son tangentes al eje X en algún punto; en la imagen se representan tres de las curvas del haz, tangentes a $y=0$ en los puntos $x=-3, -2, -1$.

$caption id="attachment_866" align="alignnone" width="502"$[![Haz de parábolas 4y=(x + C)²](/taller-matematicas/assets/images/Feix_corbes_env.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/02/Feix_corbes_env.png) Haz de parábolas 4y=(x + C)²
¿Cuál es la ecuación diferencial del haz de curvas? Derivamos respecto a *x *la ecuación del haz: $4y'=2(x + C)$, y eliminamos la constante *C* usando esta igualdad y la ecuación del haz:

$\left.\begin{array}{r}4y'=2(x+C)\Rightarrow C=2y'-x\\4y=(x\;+\;C)^2\end{array}\right\}\Rightarrow4y=(2y'{)^2=4y'^2}\Rightarrow y=y'^2.$
Observemos que la recta $y=0$, por ser tangente a todas las curvas del haz, tiene la misma derivada que las curvas del haz en cada punto del eje X; por tanto, también verifica la ecuación diferencial del haz. En general: si existe una curva envolvente que es tangente a todas las curvas de un haz, entonces esa curva será una solución singular de la ecuación diferencial del haz.

#### Cálculo de la envolvente de un haz de curvas

Dado un valor cualquiera $x=x_0$, la envolvente tendrá la misma derivada en ese punto que alguna curva del haz, esto es, habrá una constante C, dependiente de $x=x_0$, tal que la derivada de la curva del haz $F(x_0,y,C)=0$ tendrá el mismo valor en ese punto. Prescindimos de $x_0$: en general para cada x tendremos una C(x). Derivemos respecto a x la expresión del haz, teniendo en cuenta que y también depende de x, usando la regla de la cadena y la derivación implícita:

$F(x,y,C)=0\Rightarrow\frac{\operatorname d{F(x,y,C)}}{\operatorname dx}=\frac{\partial F(x,y,C)}{\partial x}+\frac{\partial F(x,y,C)}{\partial y}\frac{\operatorname dy}{\operatorname dx}=\frac{\partial F(x,y,C)}{\partial x}+\frac{\partial F(x,y,C)}{\partial y}y'=0$

Despejamos y' para obtener la derivada en cualquier punto de cualquier curva del haz:

$y'=-\frac{\partial F(x,y,C)}{\partial x}\left(\frac{\partial F(x,y,C)}{\partial y}\right)^{-1}.$

Pasamos ahora a la curva envolvente; en los puntos de contacto $(x,y)$ entre cada curva y la envolventes las derivadas coinciden con las curvas del haz; en cada valor dado x tendremos determinado un C(x), como el valor y(x) también coincide con el del haz, tendremos que en el punto de contacto se cumple $F(x,y,C(x))$. Derivamos de nuevo respecto a x:

$\begin{array}{l}F(x,y,C\left(x\right))=0\Rightarrow\\\frac{\operatorname d{F(x,y,C\left(x\right))}}{\operatorname dx}=\frac{\partial F(x,y,C)}{\partial x}+\frac{\partial F(x,y,C)}{\partial y}\frac{\operatorname dy}{\operatorname dx}+\frac{\partial F(x,y,C)}{\partial C}\frac{\operatorname dC}{\operatorname dx}\\=\frac{\partial F(x,y,C)}{\partial x}+\frac{\partial F(x,y,C)}{\partial y}y'+\frac{\partial F(x,y,C)}{\partial C}C'=0\end{array}.$

Despejamos y':

$y'=\left(\frac{\partial F(x,y,C)}{\partial y}\right)^{-1}\left$\frac{\partial F(x,y,C)}{\partial x}+\frac{\partial F(x,y,C)}{\partial C}C'\right$.$

Las dos expresiones para la derivada y' han de ser iguales:

$y'=\left(\frac{\partial F(x,y,C)}{\partial y}\right)^{-1}\left$\frac{\partial F(x,y,C)}{\partial x}+\frac{\partial F(x,y,C)}{\partial C}C'\right$=\left(\frac{\partial F(x,y,C)}{\partial y}\right)^{-1}\left$\frac{\partial F(x,y,C)}{\partial x}\right$.$

Vemos que ha de ser: $\frac{\partial F(x,y,C)}{\partial C}C'=0,$ que tiene dos soluciones posibles, la trivial $C'=0\Rightarrow C=cte$ y la condición $\frac{\partial F(x,y,C)}{\partial C}=0.$ La primera es una solución sin importancia pues nos dice que la constante C no dependerá
de x (haz de curvas degenerado: todas la curvas son iguales), mientras que la segunda es la condición general que ha de cumplir la envolvente.

**Ejemplo 5**: encontrar la expresión de la curva envolvente del haz de rectas del ejemplo 3, $y=(1-10/C)*x+(10-C).$

Lo expresamos en la forma $F(x,y,C)=y-(1-10/C)\ast x-(10-C)=0$ para derivar respecto a  C e igualar a cero:

$\frac{\partial{F(x,y,C)}}{\partial C}=\frac{-10}{C^2}x+1=0\Rightarrow C=\sqrt{10x}.$

Sustituimos este valor en la expresión del haz para eliminar C y obtener la ecuación de la envolvente:

$F(x,y)=y(1-\frac{10}{\sqrt{10x}})x+(10-\sqrt{10x})=y-10-x+2\sqrt{10x}=0.$

La envolvente es $y=10+x-2\sqrt{10x}.$

**Ejemplo 6**: calcular la envolvente del haz de curvas $4y=(x + C)^2$ del ejemplo 4.

$\begin{array}{l}F(x,y,C)=4y-(x+C)^2=0;\\\frac{\partial F}{\partial C}=2(x+C)=0\Rightarrow C=-x;\\F(x,y)=4y-(x-x)^2=4y=0\Rightarrow\boxed{y=0}.\end{array}$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
## Funciones homogéneas. Aplicación a las ecuaciones diferenciales.

Una función $F(x,y)$ es homogénea de grado n si $F(\lambda x,\lambda y)=\lambda^nF(x,y)$ para todo parámetro $\lambda\neq0.$ Por ejemple, la función $F(x,y)=xy-x^2$ es homogénea de grado 2, pues $F(\lambda x,\lambda y)=\lambda x\lambda y- ( \lambda x)^2=\lambda^2F(x,y).$

En el caso especial de que $F(x,y)$ es homogénea de grado 0 tenemos $F(\lambda x,\lambda y)=F(x,y)$, y nos da un método de resolución de ecuaciones diferenciales $y'=F(x,y)$ en los que la F sea homogénea de grado 0: con el cambio de variable $u=y/x$ se convierten en ecuaciones de variables separadas. En efecto:

$\begin{array}{l}u=y/x\Leftrightarrow y=ux\Rightarrow y'=u'x+u;\\y'=F(x,y)\Leftrightarrow u'x+u=F(x,ux)=F(1,u)\end{array}$

donde hemos usado la x en vez de la $\lambda$ como parámetro de la homogénea. Entonces

$\begin{array}{l}\frac{du}{dx}x+u=F(u)\Leftrightarrow\frac{du}{dx}x=F(u)-u\Leftrightarrow\frac{du}{F(u)-u}=\frac{dx}x\Leftrightarrow\\\int\frac{du}{F(u)-u}=\int\frac{dx}x=\ln\left(x\right)+C\end{array}.$

**Ejemplo 7**: Resolver $y'=\frac y{\sqrt{x^2+y^2}-x}.$

$F(\lambda x,\lambda y)=\frac{\lambda y}{\sqrt{\lambda^2x^2+\lambda^2y^2}-\lambda x}=\frac{\lambda y}{\lambda\left(\sqrt{x^2+y^2}-x\right)}=\frac y{\sqrt{x^2+y^2}-x}$ luego es homogénea de grado 0. Hacemos el cambio $u=y/x$ para conseguir que sea de variables separadas:

$\begin{array}{l}y'=u'x+u=\frac{ux}{\sqrt{x^2+u^2x^2}-x}=\frac u{\sqrt{1+u^2}-1};\\\frac{du}{dx}x=\frac u{\sqrt{1+u^2}-1}-u=\frac{u\left(\sqrt{1+u^2}+1\right)}{1+u^2-1}-u=\frac{\sqrt{1+u^2}+1}u-u=\\\frac{\sqrt{1+u^2}+1-u^2}u;\\\frac{udu}{\sqrt{1+u^2}+1-u^2}=\frac{dx}x\\\end{array}.$

Luego $\int\frac{udu}{\sqrt{1+u^2}+1-u^2}=\int\frac{dx}x=\ln\left(x\right)+C.$ En la primera integral hacemos el cambio de variable $1+u^2=t^2$ que la convierte en:

$\int\frac{udu}{\sqrt{1+u^2}+1-u^2}=\int\frac{t\operatorname dt}{t+1-\left(t^2-1\right)}=\int\frac{t\operatorname dt}{-t^2+t+2},$

que es de tipo racional; descomponemos en fracciones simples:

$\begin{array}{l}\int\frac{t\operatorname dt}{-t^2+t+2}=\int\frac{-1/3}{t+1}+\int\frac{-2/3}{t-2}=-\frac13\ln\left(t+1\right)-\frac23\ln\left(t-2\right)\\=-\frac13\ln\left(\left(t+1\right)\left(t-2\right)^2\right)=\ln\left(\left(t+1\right)\left(t-2\right)^2\right)^{-1/3}\end{array}.$

Igualamos las dos integrales, y deshacemos los cambios para obtener la solución general en forma implícita:

$\begin{array}{l}\ln\left(\left(t+1\right)\left(t-2\right)^2\right)^{-1/3}=\ln\left(x\right)+C\Leftrightarrow\\Cx=\left(\left(t+1\right)\left(t-2\right)^2\right)^{-1/3}=\left(t^3-3t^2+4\right)^{-1/3}\Leftrightarrow\\\frac C{x^3}=\left(u^2+1\right)^{3/2}-3u^2+1\Leftrightarrow\\C=x^3\left$\left(\left(\frac yx\right)^2+1\right)^\frac32-3\left(\frac yx\right)^2+1\right$.\end{array}.$

#### Reducción a homogénea

Las funciones racionales de la forma

$F(x,y)=\frac{ax+by+c}{a'x+b'y+c'}$
sólo son homogéneas de grado 0 cuando $c=c'=0$, no obstante si pensamos en el numerador y denominador de la función como si fueran dos rectas $ax+by+c=0,\;a'x+b'y+c'=0$, podemos probar a encontrar su punto de intersección $(x_0,y_0)$, si existe, entonces el cambio de variable $X = x - x_0, Y = y - y_0$ (que es una traslación de los ejes xy a los ejes XY, tomando como origen de coordenadas el punto $(x_0,y_0)$), convierte la función en homogénea de grado 0.

**Ejemplo 8**:  Resolver $y'=\frac{y-x-1}{x+y-1}.$

Hallamos la intersección de las rectas:

$\left.\begin{array}{r}y-x-1=0\\x+y-1=0\end{array}\right\}y=1,\;x=0$

hacemos el cambio $X=x, Y=y-1$ que transforma la ecuación en:

$y'=\frac{y-x-1}{x+y-1}\Leftrightarrow Y'=\frac{Y-X}{X+Y}$

que contiene una función $f(X,Y)$ homogénea de grado 0; hacemos el cambio $u=Y/X$ para separar las variables:

$\begin{array}{l}u'X+u=\frac{u-1}{1+u}\Leftrightarrow\frac{\operatorname du}{\operatorname dX}X=\frac{u-1}{1+u}-u=\frac{-1-u^2}{1+u}=-\frac{1+u^2}{1+u};\\-\int\frac{1+u}{1+u^2}\operatorname du=\int\frac{\operatorname dX}X=\ln\left(X\right)+C\end{array}.$

Descomponemos la primera integral:

$\begin{array}{l}\int\frac{1+u}{1+u^2}=\int\frac1{1+u^2}+\int\frac u{1+u^2}=\tan^{-1}\left(u\right)+\frac12\int\frac{2u}{1+u^2}=\\\tan^{-1}\left(u\right)+\frac12\ln\left(1+u^2\right)\end{array}.$

Igualamos integrales y deshacemos el cambio:

$\begin{array}{l}-\tan^{-1}\left(u\right)-\frac12\ln\left(1+u^2\right)=\ln\left(X\right)+C=\ln\left(CX\right)\Leftrightarrow\\-\tan^{-1}\left(\frac YX\right)=\ln\left(CX\left(1+\left(\frac YX\right)^2\right)\right);\\\ln\left(Cx\left(1+\left(\frac{y-1}x\right)^2\right)\right)+\tan^{-1}\left(\frac{y-1}x\right)=0.\\\end{array}$

#### Caso especial: las rectas son paralelas

En el caso especial de que las dos rectas no tengan intersección, entonces es que son paralelas, con vectores directores proporcionales: $\frac ba=\frac{b'}{a'}=r$; pero entonces podemos hacer

$F(x,y)=\frac{ax+by+c}{a'x+b'y+c}=\frac{a'rx+b'ry+c}{a'x+b'y+c}=\frac{r\left(a'x+b'y\right)+c}{a'x+b'y+c},$

con el cambio de variable $Y=a'x+b'y$ se convierte en

$\begin{array}{l}F(x,Y)=\frac{rY+c}{Y+c'};\;y=\frac{Y-a'x}{b'}\Rightarrow\frac{\operatorname dy}{\operatorname dx}=\frac1{b'}\left(\frac{\operatorname dY}{\operatorname dx}-a'\right);\\\frac{\operatorname dy}{\operatorname dx}=F(x,y)\Leftrightarrow\frac1{b'}\left(\frac{\operatorname dY}{\operatorname dx}-a'\right)=\frac{rY+c}{Y+c'}\Leftrightarrow\\\frac{\operatorname dY}{\operatorname dx}=b'\frac{rY+c}{Y+c'}+a'\end{array}$

que es de variables separadas.

**Ejemplo 9**: $y'=\frac{x+y+1}{x+y-1}.$

Las rectas $x+y+1=0$ y $x+y-1$ no tienen intersección, son paralelas; hacemos el cambio $Y=x+y, Y'=1+y'$ para obtener:

$\begin{array}{l}Y'-1=\frac{Y+1}{Y-1};\;\frac{\operatorname dY}{\operatorname dx}=\frac{Y+1}{Y-1}+1=\frac{Y+1+Y-1}{Y-1}=\frac{2Y}{Y-1};\\\int\frac{Y-1}{2Y}\operatorname dY=\int\operatorname dx;\\\frac12\int\left(1-\frac1Y\right)\operatorname dY=x+C;\\Y-\ln\left(Y\right)=2x+C;\\x+y-\ln\left(x+y\right)=2x+C;\\y=x+\ln\left(x+y\right)+C.\end{array}$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

## Ecuaciones exactas

Las ecuaciones de la forma $M (x, y) + N (x, y) \frac {dy} {dx} = 0,$ o equivalentemente, $M (x, y) dx + N (x, y) dy = 0$, diremos que son exactas siempre y cuando M y N  sean funciones continuas y
se verifique la condición $\frac {\partial M} {\partial y} = \frac {\partial N} {\partial x}.$

La solución vendrá dada de forma implícita por $F (x, y) = C$ donde $\frac {\partial F} {\partial x} = M, \: \frac {\partial F} {\partial y} = N.$

**Ejemplo 10**: La ecuación $y^{3} dx + 3xy^{2} dy = 0$  es exacta, pues $N = 3xy^{2}, \frac{\partial N} {\partial x} = 3y^{2}, \: M = y^{3}, \: \frac {\partial M} {\partial y} = 3y^{2}.$  Como $\frac {\partial F} {\partial x} = M,$ será $F (x, y) = \int MDX = xy^{3} + C (y)$ y también $F (x, y) = \int Ndy = xy^{3} + C (x);$  igualando las dos expresiones tenemos $F (x, y) = xy^{3},&nbsp;C (x) = C (y) = 0,$ así que la solución general es $xy^{3} = C.$

 

**Ejemplo 11**: Resolver la ecuación diferencial $\left (6xy-y^{3} \right) dx + \left (4y + 3x^{2} -3xy^{2} \right) dy = 0.$

Como $M = 6xy-y^{3},&nbsp;&nbsp;N = 4y + 3x^{2} -3xy^{2},&nbsp;\frac {\partial N} {\partial x} = 6x-3y^{2} = \frac {\partial M} {\partial y},$ la ecuación es exacta. Entonces

$F (x, y) = \int Ndy = 2y^{2} + 3x^{2} y-xy^{3} + C (x),&nbsp;&nbsp; F (x, y) = \int MDX = 3x^{2} y-xy^{3} + C(y),$

y cuando igualamos las dos expresiones obtenemos $C (y) = 2y^{2}.$
{% endraw %}