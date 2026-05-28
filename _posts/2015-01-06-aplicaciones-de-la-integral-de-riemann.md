---
layout: post
title: "Aplicaciones de la integral de Riemann"
date: 2015-01-06 20:15:43 +0000
categories:
  - "Cálculo en R"
  - "Funciones reales de variable real"
  - "Integración"
  - "Matemáticas"
tags:
  - "integral"
  - "integral de Riemann"
math: true
---
{% raw %}

De entre las muchas aplicaciones de la integral (cálculo de áreas y volúmenes, de longitudes de curvas, desarrollos en serie de Fourier, transformadas integrales, ecuaciones integrales, etc.) sólo veremos aquí unas pocas, ajustadas al nivel de estos apuntes: primer curso de ingeniería. Concretamente se tratan:

 	- [Cálculo de áreas planas](#areas)

 	- [Cálculo de la longitud de curvas](#longitud)

 	- [Integrales impropias](#impropias)

 	- [Integrales de Euler: funciones Gamma  y Beta](#Euler)

 	- [Teorema del valor medio: forma integral](#medio)

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

## Cálculo de áreas planas

Si calculamos áreas habrá que tener en cuenta que debemos tomar los valores absolutos. Ejemplo: el área delimitada por $f(x)=sin(x)$ entre $(0,2\mathrm\pi)$ no puede calcularse como $\int_0^{2\mathrm\pi}\sin\left(x\right)\operatorname{d}x$ ya que esta integral vale cero, debido a que la función $sin(x)$ cambia de signo periódicamente.

[![Para calcular áreas hemos de tener en cuenta los cambios de signo de la función](/taller-matematicas/assets/images/area3.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/area3.png)

El valor real del área será $A=\int_0^{2\mathrm\pi}\left|\sin\left(x\right)\right|\operatorname{d}x,$ o bien $A=\int_0^\mathrm\pi\sin\left(x\right)\operatorname{d}x+\int_\mathrm\pi^{2\mathrm\pi}-\sin\left(x\right)\operatorname{d}x=2+2=4.$

Para hallar el área en una región entre dos gráficas de funciones $y=f(x), y=g(x)$, hallamos el valor absoluto de la diferencia :

$\int_a^b\left|\left(f-g\right)\right|\operatorname{d}x=\left\{\begin{array}{l}\int_a^b\left(f-g\right)\operatorname{d}x\;\text{si }f\geq g\;\text{en }\left(a,b\right)\\\int_a^b\left(g-f\right)\operatorname{d}x\;\text{si }g\geq f\;\text{en }\left(a,b\right)\end{array}\right.$

En ocasiones, el valor absoluto en el intervalo de integración $(a,b)$ habrá de calcularse por subintervalos, como en el siguiente ejemplo.
**Ejemplo 1**: calcular el área $A$ de la región comprendida entre las gráficas de las funciones $y=\sin(x), y=\cos(x+1)$ y el intervalo $x\in\left(1,4\right).$

[![Cálculo del área comprendida entre las gráficas de dos funciones](/taller-matematicas/assets/images/area5.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/area5.png) Cálculo del área comprendida entre las gráficas de dos funciones
$\begin{array}{l}A=\int_1^4\left|\left(\sin\left(x\right)-\cos\left(x+1\right)\right)\right|\operatorname{d}x=\begin{array}{l}\int_1^{x_0}\left(\sin\left(x\right)-\cos\left(x+1\right)\right)\operatorname{d}x+\end{array}\int_{x_0}^4\left(\cos\left(x+1\right)-\sin\left(x\right)\right)\end{array},$

donde $x_0$ es el punto de intersección de las dos gráficas, situado dentro del intervalo de integración $(1,4)$; en ese punto, se invierte la diferencia de funciones. Integrando: $\int\left(\sin\left(x\right)-\cos\left(x+1\right)\right)=-\cos\left(x\right)-\sin\left(x+1\right). $ Entonces:

$\begin{array}{l}A=\left$-\cos\left(x\right)-\sin\left(x+1\right)\right$_1^{x_0}+\left$\cos\left(x\right)+\sin\left(x+1\right)\right$_{x_0}^4\\=\left$-\cos\left(x_0\right)-\sin\left(x_0+1\right)+\cos\left(1\right)+\sin\left(2\right)\right$+\left$\cos\left(4\right)+\sin\left(5\right)-\cos\left(x_0\right)-\sin\left(x_0+1\right)\right$\\=-2\cos\left(x_0\right)-2\sin\left(x_0+1\right)+\cos\left(1\right)+\sin\left(2\right)+\cos\left(4\right)+\sin\left(5\right)\\=-2\cos\left(x_0\right)-2\sin\left(x_0+1\right)-0.1630.\end{array}$

Para hallar el punto $x_0$ planteamos la ecuación $\sin\left(x\right)=\cos\left(x+1\right); $ usando la fórmula de la suma de ángulos: $\cos\left(x+1\right)=\cos\left(x\right)\cos(1)-\sin\left(x\right)\sin\left(1\right)$, obtenemos:

$\begin{array}{l}\sin\left(x\right)=\cos\left(x\right)\cos(1)-\sin\left(x\right)\sin\left(1\right)\Leftrightarrow\\\sin\left(x\right)\left$1+\sin\left(1\right)\right$=\cos\left(x\right)\cos(1)\Leftrightarrow\\\tan\left(x\right)=\frac{\cos(1)}{1+\sin\left(1\right)}\Leftrightarrow x=\tan^{-1}\left(\frac{\cos(1)}{1+\sin\left(1\right)}\right)\approx0.285\end{array}.$

El conjunto completo de soluciones de la ecuación se encuentra sumando $k\pi$, o sea: $x=0.285+k\mathrm\pi,\;\mathrm k=0,1,2,\dots.$ De todas estas soluciones, la única que cae dentro del intervalo de integración $(1,4)$ es $x=0.285+\mathrm\pi\approx3.427$, este es el valor $x_0$ buscado. Sustituimos: $A=-2\cos\left(3.427\right)-2\sin\left(4.427\right)-0.1630=\boxed{3.675}.$

## [![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

## Cálculo de la longitud de curvas

Dada una función derivable $y=f(x)$ y con derivada continua, queremos calcular la longitud del trazado $s$ de su gráfica entre dos puntos $(a,b)$. Procediendo como hicimos con las áreas en la [integral de Riemann](http://tallermatematic.eu/wp/?p=674), dividimos el intervalo en n subintervalos; para cada uno de ellos, aproximamos el segmento de arco $\triangle s$ por la hipotenusa del triángulo de lados $\triangle x,\;\triangle y:$

$caption id="attachment_717" align="alignnone" width="427"$[![Aproximación a la longitud de un arco de curva](/taller-matematicas/assets/images/longitud_arc.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/longitud_arc.png) Aproximación a la longitud de un arco de curva

$\triangle s=\sqrt{\left(\triangle x\right)^2+\;\left(\triangle y\right)^2}.$

Operando:

$\begin{array}{l}\triangle s=\sqrt{\left(\triangle x\right)^2+\;\left(\triangle y\right)^2}=\sqrt{\left(\left(\triangle x\right)^2+\;\left(\triangle y\right)^2\right)\frac{\left(\triangle x\right)^2}{\left(\triangle x\right)^2}}\\=\sqrt{1+\frac{\;\left(\triangle y\right)^2}{\left(\triangle x\right)^2}}\triangle x\end{array}.$

La longitud total del arco será aproximadamente la suma de los n segmentos de arco: $s\approx\sum_{k=0}^n\triangle s_k=\sum_{k=0}^n\sqrt{1+\frac{\;\left(\triangle y_k\right)^2}{\left(\triangle x_k\right)^2}}\triangle x_k.$ Pasando al límite: $s=\lim_{n\rightarrow\infty}\sum_{k=0}^n\sqrt{1+\frac{\;\left(\triangle y_k\right)^2}{\left(\triangle x_k\right)^2}}\triangle x_k,$  cada intervalo tendrá una longitud $\triangle x_k\rightarrow0.$ Recordando que $\lim_{\triangle x\rightarrow0}\frac{\triangle x}{\triangle y}=y'(x)$ obtenemos

$s=\lim_{n\rightarrow\infty}\sum_{k=0}^n\sqrt{1+\left(y'\left(x_k\right)\right)^2}\triangle x_k=\int_a^b\sqrt{1+\left(y'\left(x\right)\right)^2}\operatorname{d}x.$

En el último paso igualamos el límite de la suma a una integral de Riemann, pues hemos supuesto que la derivada es continua, y por tanto $\sqrt{1+\left(y'\left(x\right)\right)^2}$ también será continua, e integrable.
**Ejemplo 2**: cuando un cable flexible se tiende entre dos extremos, toma la forma conocida como curva catenaria, cuya expresión analítica es $y=a·\cosh(x/a),$ donde $a$ es la distancia entre el origen de coordenadas y la curva (o sea la altura mínima de la catenaria respecto al suelo):

| 

[![Catenaria. Licencia Creative Commons](/taller-matematicas/assets/images/catenaria.jpg)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/catenaria.jpg) [Catenaria](http://www.flickr.com/photos/diegobe/226041902/sizes/o/). [Licencia Creative Commons.](https://creativecommons.org/licenses/by-sa/2.0/) 
| 

[![Curva catenaria (en negro) y parábola (en rojo)](/taller-matematicas/assets/images/catenaria-300x113.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/catenaria.png) Curva catenaria (en negro) y parábola (en rojo) 

Hallar la longitud de cable tendida entre dos postes sabiendo que la altura mínima es de 6 metros, y que la distancia entre postes es de 15 metros.

$\begin{array}{l}y'=D_x\left$a\cdot \cosh\left(\frac xa\right)\right$=\sinh\left(\frac xa\right)\Leftrightarrow\\\sqrt{1+\left(y'\left(x\right)\right)^2}=\sqrt{1+\left(\sinh\left(\frac xa\right)\right)^2}=\sqrt{\cosh^2\left(\frac xa\right)}=\cosh\left(\frac xa\right).\end{array}$

La longitud del arco viene dada por

$s=\int_{-15/2}^{15/2}\cosh\left(\frac x6\right)\operatorname{d}x=6\left$\sinh\left(\frac x6\right)\right$_{-15/2}^{15/2}=19.2$

## [![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

## Integrales impropias

En las aplicaciones prácticas a menudo encontramos integrales definidas en intervalos que no son del tipo $(a,b)$, o bien que toman valores infinitos en algún punto (no estan acotadas en el intervalo de integración). Por ejemplo, la [transformada de Laplace](http://tallermatematic.eu/wp/?p=1075) muy usada en [teoría de circuitos](https://es.wikipedia.org/wiki/Transformada_de_Laplace_en_circuitos) se basa en una integral impropia. La definición dada de [integral de Riemann](http://tallermatematic.eu/wp/?p=674) no puede usarse con este tipo de funciones e intervalos, pero puede generalizarse para cubrir dos casos:

***Definición 1**: Si el dominio de integración $(a,b)$ contiene puntos donde $f(c)=\pm\infty,\;c\in\left(a,b\right),$ denominamos a $\int_a^bf\operatorname{d}x$ **integral impropia de segunda especie**.*

***Definición 2**: Si el dominio de integración es una semirrecta $(-\infty,b)$ o $(a,\infty)$ denominamos a $\int_a^bf\operatorname{d}x$ **integral impropia de primera especie**.*

**Ejemplo 3**: La integral $\int_0^1\frac1{1-x}\operatorname{d}x$ es impropia de segunda especie, pues $\lim_{x\rightarrow1}\frac1{1-x}=\pm\infty.$

#### **Cálculo de integrales impropias de segunda especie**

Supongamos que $\lim_{x\rightarrow b}f\left(x\right)=\infty.$ Definimos:

$L=\int_a^bf\operatorname{d}x=\lim_{\varepsilon\rightarrow0}\int_a^{b-\varepsilon}f\operatorname{d}x.$

 	-  Si este límite L existe y es finito, diremos que la integral de segunda especie es convergente. De forma similar, si $\lim_{x\rightarrow a}f\left(x\right)=\infty$ definimos $\int_a^bf\operatorname{d}x=\lim_{\varepsilon\rightarrow0}\int_{a+\varepsilon}^bf\operatorname{d}x,$ que puede existir o no.

 	- En el caso de que $f(x)$ tenga un número finito de puntos $c_1,c_2,\dots,c_n\in\left(a,b\right)$ tales que $\lim_{x\rightarrow c_i}f\left(x\right)=\infty$ para todos ellos, entonces aplicamos la propiedad de la partición del intervalo de integración: $\int_a^bf\operatorname{d}x=\int_a^{c_1}f\operatorname{d}x+\int_{c_1}^{c_2}f\operatorname{d}x+\dots+\int_{c_{n-1}}^{c_n}f\operatorname{d}x+\int_{c_n}^bf\operatorname{d}x.$

 	- Por último, si $f(x)$ toma valores infinitos en ambos extremos del intervalo de integración, entonces escogemos un punto $c\in\left(a,b\right)$ arbitrario tal que $f(c)\neq0$ y aplicamos $\int_a^bf\operatorname{d}x=\int_a^cf\operatorname{d}x+\int_c^bf\operatorname{d}x=\lim_{\varepsilon\rightarrow0}\int_{a+\varepsilon}^cf\operatorname{d}x+\lim_{\varepsilon\rightarrow0}\int_c^{b-\varepsilon}f\operatorname{d}x.$

**Ejemplo 4**: La integral impropia de segunda especie $\int_0^1\frac1{1-x}\operatorname{d}x$ se calcula como

$\begin{array}{l}\int_0^1\frac1{1-x}\operatorname{d}x=\lim_{\varepsilon\rightarrow0}\int_0^{1-\varepsilon}\frac1{1-x}\operatorname{d}x=\lim_{\varepsilon\rightarrow0}\left$-\ln\left(1-x\right)\right$_0^{1-\varepsilon}=\\\lim_{\varepsilon\rightarrow0}-\ln\left(\varepsilon\right)+\ln\left(1\right)=\lim_{\varepsilon\rightarrow0}\ln\left(\frac1\varepsilon\right)=\infty\end{array},$

vemos que no es convergente.

#### Criterio de convergencia de **integrales impropias de segunda especie**

***Proposición 1**:*

*$\int_a^b\frac1{\left(b-x\right)^n}\operatorname{d}x\;\text{es }\left\{\begin{array}{l}\text{convergente para }n&lt;1\\\text{divergente para }n\geq1\end{array}\right.$*

***Proposición 2**:*

*$\int_a^b\frac1{\left(x-a\right)^n}\operatorname{d}x\;\text{es }\left\{\begin{array}{l}\text{convergente para }n&lt;1\\\text{divergente para }n\geq1\end{array}\right.$*

Estas integrales sirven para estudiar la convergencia de otras más generales, comparándolas.
**Ejemplo 5**: La integral $I=\int_1^2\frac1{x\sqrt[3]{x^2-4x+4}}$  es impropia de 2ª especie  pues en $x=2$ el denominador vale cero y la función toma valores no acotados. Sabiendo que $x=2$ es una raíz de $x^2-4x+4,$ dividimos este polinomio por $(x-2)$ para simplificarlo; resulta $x^2-4x+4=\left(x-2\right)^2\Leftrightarrow\int_1^2\frac1{x\sqrt[3]{x^2-4x+4}}=\int_1^2\frac1{x\left(x-2\right)^{2/3}}.$ Usamos ahora la proposición 2:

$\int_1^2\frac1{x\left(x-2\right)^{2/3}}&lt;\int_1^2\frac1{\left(x-2\right)^{2/3}}=\int_1^2\frac1{\left(2-x\right)^{2/3}}=\int_a^b\frac1{\left(x-b\right)^n},$

pues $(a-b)^2=(b-a)^2\Leftrightarrow\sqrt[3]{(a-b)^2}=\sqrt[3]{(b-a)^2};$ la última integral es convergente, pues $n=2/3&lt;1$, luego $I$ también es convergente. Calcular esta integral no es inmediato: haciendo el cambio de variable $x-2=t^3$ el integrando se simplifica: $\frac1{x\left(x-2\right)^{2/3}}\operatorname{d}x=\frac1{\left(t^3+2\right)t^2}3t^2\operatorname{d}t=3\frac1{t^3+2}.$ Los límites de integración también quedan afectados por el cambio de variable:

$\begin{array}{l}x=1\Leftrightarrow t=\sqrt[3]{1-2}=\sqrt[3]{-1}=-1;\;\\x=2\Leftrightarrow t=\sqrt[3]{2-2}=0.\end{array}$

La integral queda $3\int_{-1}^0\frac1{t^3+2}\operatorname{d}t\approx1.77,$ omitimos el cálculo de esta última integral (en los ejemplos de [Problemas resueltos de integrales indefinidas](http://tallermatematic.eu/wp/?p=172) se resuelven integrales parecidas). Observad que, con el cambio de variable, la integral ha dejado de ser impropia.

**Cálculo de integrales impropias de primera especie**

Definimos: $\int_a^\infty f=\lim_{b\rightarrow\infty}\int_a^bf,\;\int_{-\infty}^bf=\lim_{a\rightarrow-\infty}\int_a^bf.$ Si estos límites existen decimos que la integral converge.
**Ejemplo 6**: $\int_0^\infty e^{-x}=\lim_{b\rightarrow\infty}\int_0^be^{-x}=\lim_{b\rightarrow\infty}\left$-e^{-x}\right$_0^b=\lim_{b\rightarrow\infty}\left$-e^{-b}+1\right$=1.$

#### Criterio de convergencia de **integrales impropias de primera especie**

***Proposición 3**: las integrales impropias de primera especie $\int_a^\infty\frac1{x^n},\int_{-\infty}^b\frac1{x^n}$ son convergentes si y sólo si $n&gt;1.$*

**Ejemplo 7**: $\int_1^\infty\frac1{\sqrt[3]{x^2}}=\int_1^\infty\frac1{x^{2/3}}$ es divergente, pues $2/3&lt;1$.

## [![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

## Integrales de Euler: funciones $\Gamma\;\text{ y }\;\beta$

***Definición 3**: La **función Gamma** se
define como $\Gamma\left(x\right)=\int_0^\infty t^{x-1}e^{-t}\operatorname{d}t$ para $x&gt;0$. *

Esta integral impropia es convergente para $x&gt;0$, pero no puede resolverse analíticamente, o sea, no existe la función primitiva $F(t)$ tal que $F'(t)=t^{x-1}e^{-t}.$ En cambio, tiene numerosas aplicaciones prácticas, una de ellas es la de generalizar la función factorial,  que sólo está definida para enteros, $n!=n·(n-1)·\dots·2·1$, a números reales.

**Proposición 4**: La función Gamma tiene las siguientes propiedades

1) $\Gamma\left(x+1\right)=x!$ si $x$ es un entero positivo

2) $\Gamma\left(x+1\right)=x\Gamma\left(x\right)$ para todo $x&gt;0$

3) Utilizando repetidamente la segunda propiedad se deduce la siguiente expresión: $\Gamma\left(x\right)=\left(x-1\right)\left(x-2\right)\dots\left(x-n\right)\Gamma\left(1+r\right),$ donde $n$ verifica que $n+1$ es el mayor entero menor que $x$, y $0\leq r\le1$. Con esta expresión, conociendo los valores de $\Gamma\left(x\right)$ en el intervalo $[1,2)$, podemos calcular \Gamma\left(x\right) para cualquier $x$:

 

| **x** 
| 1 
| 1.1 
| 1.2 
| 1.3 
| 1.4 
| 1.5 
| 1.6 
| 1.7 
| 1.8 
| 1.9 

|  **$\Gamma\left(x\right)$** 
| 1.000 
| 0.951 
| 0.918 
| 0.897 
| 0.887 
| 0.886 
| 0.894 
| 0.909 
| 0.931 
| 0.962 

**Ejemplo 8**: Calculemos $\Gamma\left(3.1\right),$ el mayor entero $n+1$ menor que 3.1 es 2, luego $n=2$ y los términos del desarrollo son  $\Gamma\left(3.1\right)=\left(3.1-1\right)\left(3.1-2\right)\Gamma\left(3.1-2\right)=2.1\cdot1.1\cdot\Gamma\left(1.1\right)=2.1\cdot1.1\cdot0.951=2.197.$

** Definición 5**: Dados $p, q&gt;0$, definimos la **función Beta(p,q)**: $\beta\left(p,q\right)=\int_0^1x^{p-1}\left(1-x\right)^{q-1}.$ Su utilidad viene dada por sus propiedades.
**Proposición 5**: La función Beta tiene las siguientes propiedades

1. $\beta\left(p,q\right)=\frac{\Gamma\left(p\right)\Gamma\left(q\right)}{\Gamma\left(p+q\right)}$

2. $\beta\left(p,q\right)=\beta\left(q,p\right)$

3. $\beta\left(p,q\right)=2\int_0^{\pi/2}\left(\sin\left(x\right)\right)^{2p-1}\left(\cos\left(x\right)\right)^{2q-1}\operatorname{d}x$

La primera propiedad es útil para resolver ciertas integrales exponenciales que suelen presentarse en Cálculo de probabilidades y Estadística, mientras que la tercera es útil para resolver ciertas integrales trigonométricas.
**Ejemplo 9**: Calcular $\int_0^{\pi/2}\left(\sin\left(x\right)\right)^{25}\left(\cos\left(x\right)\right)^{30}\operatorname{d}x.$ Usando la propiedad 3: $25=2p-1\Leftrightarrow p=13;\;30=2q-1\Leftrightarrow q=31/2,$ entonces: $\int_0^{\pi/2}\left(\sin\left(x\right)\right)^{25}\left(\cos\left(x\right)\right)^{30}\operatorname{d}x=\frac122\int_0^{\pi/2}\left(\sin\left(x\right)\right)^{2p-1}\left(\cos\left(x\right)\right)^{2q-1}=\frac12\beta\left(13,15.5\right).$ Usemos ahora la propiedad 1: $\frac12\beta\left(13,15.5\right)=\frac{\Gamma\left(13\right)\Gamma\left(15.5\right)}{\Gamma\left(13+15.5\right)}.$ Calculamos cada uno de estos valores por separado:

$\begin{array}{l}\Gamma\left(13\right)=12!\\\Gamma\left(15.5\right)=14.5\cdot13.5\cdot\dots\cdot2.5\cdot\Gamma\left(1.5\right)\\\Gamma\left(13+15.5\right)=\Gamma\left(28.5\right)=27.5\cdot26.5\cdot\dots\cdot2.5\cdot\Gamma\left(1.5\right)\\\end{array},$

por tanto:

$\begin{array}{l}\int_0^{\pi/2}\left(\sin\left(x\right)\right)^{25}\left(\cos\left(x\right)\right)^{30}\operatorname{d}x=\frac{\Gamma\left(13\right)\Gamma\left(15.5\right)}{\Gamma\left(13+15.5\right)}=\\\frac{\left(12!\right)\left(14.5\cdot13.5\cdot\dots\cdot2.5\cdot\Gamma\left(1.5\right)\right)}{27.5\cdot26.5\cdot\dots\cdot2.5\cdot\Gamma\left(1.5\right)}=\frac{12!}{27.5\cdot26.5\cdot\dots\cdot15.5}\approx2.7961\cdot10^{-9}\end{array}.$

El último resultado se ha obtenido con una hoja de cálculo.

**Ejemplo 10**: Calcular $\int_0^\infty e^{-x^2}\operatorname{d}x.$ Es una integral impropia que, además, no tiene solución analítica (no existe ninguna función conocida que sea su primitiva). Comparando con $\Gamma\left(p\right)=\int_0^\infty t^{p-1}e^{-x}\operatorname{d}x,$ podemos ver que, si hacemos el cambio de variable $x^2=t,\;2x\operatorname{d}x=\operatorname{d}t,\;\operatorname{d}x=\frac{\operatorname{d}t}{2x}=\frac{\operatorname{d}t}{2\sqrt t}=\frac12t^{-1/2}\operatorname{d}t,$ entonces la integral nos queda: $\int_0^\infty\frac12t^{-1/2}e^{-t}\operatorname{d}x=\frac12\Gamma\left(\frac12\right).$

Usando la propiedad 1 de la función Beta: $\beta\left(\frac12,\frac12\right)=\frac{\Gamma\left(\frac12\right)\cdot\Gamma\left(\frac12\right)}{\Gamma\left(\frac12+\frac12\right)}=\frac{\left$\Gamma\left(\frac12\right)\right$^2}{\Gamma\left(1\right)}=\left$\Gamma\left(\frac12\right)\right$^2.$

Ahora recordamos la propiedad 3:

$\beta\left(\frac12,\frac12\right)=2\int_0^{\pi/2}\left(\sin\left(x\right)\right)^{2\frac12-1}\left(\cos\left(x\right)\right)^{2\frac12-1}\operatorname{d}x\;=2\int_0^{\pi/2}1\operatorname{d}x=2\frac{\mathrm\pi}2=\mathrm\pi$

Nos queda: $\beta\left(\frac12,\frac12\right)=\mathrm\pi=\left$\Gamma\left(\frac12\right)\right$^2\Leftrightarrow\Gamma\left(\frac12\right)=\sqrt{\mathrm\pi}$ y la integral pedida es: $\int_0^\infty e^{-x^2}\operatorname{d}x=\frac12\Gamma\left(\frac12\right)=\frac12\sqrt{\mathrm\pi}.$

## [![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)Teorema del valor medio: forma integral

En el post [Aplicaciones de las derivadas -> Teoremas de valores intermedios](http://tallermatematic.eu/wp/?p=547#intermedios) se vieron  algunos teoremas relativos a la relación entre derivadas y  valores de la función en un intervalo. Vemos ahora la relación entre integración y valores de la función en un intervalo.

***Definición 6**: Si $f(x)$ es integrable en $[a,b]$, el **valor medio promedio de la función** en ese intervalo es $\frac1{b-a}\int_a^bf\left(x\right).$*

**Ejemplo 11**: Calculemos el valor promedio de $f(x)=\cos\left(x\right)$ en $[0,2\pi/2]$, que es:

$\frac1{\mathrm\pi-0}\int_0^{\mathrm\pi/2}\cos\left(x\right)=\frac1{\mathrm\pi/2}\left$\sin\left(x\right)\right$_0^{\mathrm\pi/2}=\frac1{\mathrm\pi/2}\left(\sin\left(\mathrm\pi/2\right)-\sin\left(0\right)\right)=\frac2{\mathrm\pi}\approx0.6366.$

El valor promedio integral es una generalización a funciones integrables del concepto de media aritmética, de hecho el valor medio integral es el promedio de todos los infinitos valores $f(x)$ correspondientes al intervalo $[a,b]$:

**Ejemplo 12**: Calcular el promedio de 10 valores de $f(x)=\cos\left(x\right)$ tomados en el intervalo $[0,2\pi/2]$ y compararlo con el resultado del ejemplo 9.

Con una hoja de cálculo formamos la siguiente tabla de valores:

[![taula_valors_sinus](/taller-matematicas/assets/images/taula_valors_sinus.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/taula_valors_sinus.png)
Los valores de x se han obtenido mediante
$x_k=\frac k9\frac{\mathrm\pi}2,\;k=0,1,\cdots,9\Leftrightarrow x_k=\left\{0,\frac19\frac{\mathrm\pi}2,\cdots,\frac89\frac{\mathrm\pi}2,\frac99\frac{\mathrm\pi}2\right\}.$ La suma de la fila $sin(x)$ es 6.22, y el promedio de los valores es 6.22/10 = 0.62; comparando con el ejemplo anterior, hay una diferencia de una centésima. Aumentando el número $n$ de valores de la tabla, la diferencia disminuiría, y en el límite $n\rightarrow\infty$ no habría diferencia.

***Teorema del valor medio integral**: Si $f(x)$ es continua en $[a,b]$, entonces existirá un punto intermedio $c\in\left$a,b\right$$ tal que $f\left(c\right)=\frac1{b-a}\int_a^bf.$*

**Ejemplo 13**: En un estudio el salario de los ingenieros industriales en función de su edad ha resultado ser, aproximadamente, $salario=-10000+12000\cdot edad^{3/7}$ en el intervalo de edades $[22,60].$ Calcular el salario medio y a que edad se percibe ese salario.

[![exemple11_aplic_integral](/taller-matematicas/assets/images/exemple11_aplic_integral.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/exemple11_aplic_integral.png)

Calculamos el valor medio, llamando $x$ a la variable independiente tiempo, e $y$ a la variable dependiente salario:

$\begin{array}{l}\overline y=\frac1{60-22}\int_{22}^{60}\left(-10000+12000\cdot x^{3/7}\right)=\frac1{38}\left$-10^4x+\frac{1.2\cdot10^4}{10/7}x^{10/7}\right$_{22}^{60}\\=\frac1{38}\left(-60\cdot10^4+0.84\cdot10^4\cdot60^{10/7}+22\cdot10^4-0.84\cdot10^4\cdot22^{10/7}\right)\\=\frac{10^4}{38}183.9=4.8\cdot10^4\end{array}.$

Como la función es continua, según el teorema del valor medio existe un punto $c\in\left$a,b\right$$ tal que $f(c)=4.8\cdot10^4$, lo planteamos:

$\begin{array}{l}f\left(x\right)=-10000+12000\cdot x^{3/7}=4.8\cdot10^4\Leftrightarrow\\x=\left(\frac{4.8\cdot10^4+10^4}{1.2\cdot10^4}\right)^{7/3}=\left(\frac{4.8+1}{1.2}\right)^{7/3}=40.13\\\end{array},$

a la edad de 40 años se està cobrando el salario medio segun este estudio.

# [![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)Bilbliografía

 

**Análisis Matemático** - Un clásico, y uno de los mejores libros de Cálculo diferencial e integral, de nivel medio. Toda una referencia como libro de teoría.

 

**Problemas resueltos de cálculo** - Antiguo, económico y eficaz libro de problemas
{% endraw %}