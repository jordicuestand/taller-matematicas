---
layout: post
title: "Funciones integrables: integral de Riemann"
date: 2015-01-04 11:00:21 +0000
categories:
  - "Cálculo en R"
  - "Matemáticas"
tags:
  - "función primitiva"
  - "integrabilidad"
  - "integral de Riemann"
  - "integral definida"
  - "integral indefinida"
  - "Regla de Barrow"
  - "sumas de Riemann"
  - "teorema fundamental del cálculo"
math: true
---
{% raw %}

## Introducción: el problema del cálculo del área y sus aplicaciones

[caption id="attachment_675" align="alignnone" width="414"][![Àrea de la región comprendida entre un intervalo de x y la gráfica f(x)](/taller-matematicas/assets/images/area.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/area.png) Àrea de la región comprendida entre un intervalo de x y la gráfica f(x)[/caption]
Consideremos el siguiente problema: dada una función cualquiera $y=f(x)$ y un intervalo $[a,b]$, calcular el área de la región delimitada por ese intervalo, la gráfica de $f(x)$ y las rectas verticales $x=a, x=b$. En la ilustración, la función es $y=Ln(x)$, el intervalo es $[2,4]$ y la región se representa con fondo rayado.

***Definición 1**: llamamos integral definida de $f(x)$ en el intervalo $[a,b]$, o simplemente integral definida de $f(x)$ en $[a,b]$, al valor del área delimitada por$[a,b]$, la gráfica de $f(x)$ y las rectas verticales $x=a, x=b$, y la representaremos por $\int_a^bf(x)\operatorname{d}x.$*

En esta definición suponemos que el concepto de área está bien definido y es conocido, aunque realmente no es nada fácil definirla formalmente. Para nuestros propósitos, será suficiente con establecer que el área de un rectángulo de lados $a,b$ es $ab$.

Las aplicaciones de la integral, además de al cálculo de áreas de figuras curvas, son variadas:

 	- Si la función $v(t)$ representa la velocidad de un objeto, entonces su integral en un intervalo de tiempo nos dará el espacio recorrido en ese intervalo de tiempo.

 	- Si expresamos la potencia de un motor como función del tiempo $P(t)$, entonces su integral en un intervalo de tiempo nos dará el trabajo realizado por el motor en ese tiempo.

 	- Si tenemos una función que exprese la velocidad de una reacción química como por ejemplo $A+B\rightarrow C+D$, entonces su integral en un intervalo de tiempo nos da la cantidad de productos $C, D$ obtenidos en ese tiempo.

 	- Para calcular la probabilidad de un suceso dada por una variable numérica real, tendremos que calcular la integral de la función de probabilidad de la variable.

## Integral de Riemann

Se han propuesto diversos métodos de cálculo de integrales; el más usado en el nivel de estos apuntes (Matemáticas para la Ingeniería) es el de Riemann, basado en aproximar el área de la región por una sucesión de rectángulos. Lo vemos con un ejemplo.

**Ejemplo 1**: Usar la integral de Riemann para calcular $\int_1^3x^2dx.$

El método consiste en dividir el intervalo $[1,3]$ en n subintervalos contiguos, en principio no tienen porque ser del mismo tamaño, pero los cogeremos iguales en longitud. La longitud total del intervalo es 3-1=2, como lo dividimos en n subintervalos, cada uno tendrá una longitud de $\triangle x=2/n.$ Los intervalos seran

$\left(a,a+\triangle x\right),\left(a+\triangle x,a+2\triangle x\right),\dots\left(a+\left(n-1\right)\triangle x,a+n\triangle x\right)$

o sea en nuestro caso:

$\left(1,3\right)=\left(1,1+\frac2n\right)\cup\left(1+\frac2n,1+2\frac2n\right)\cup\left(1+2\frac2n,1+3\frac2n\right)\cup\dots\cup\left(1+\left(n-1\right)\frac2n,1+n\frac2n\right)$

Ahora formamos n rectángulos que tienen como base cada uno de los subintervalos anteriores y como altura $f(a+k·\triangle x)$ con $k=1,2,\dots,n$, por ejemplo, para $n=2$ rectángulos tendríamos:

[caption id="attachment_677" align="alignnone" width="189"][![Aproximación al área por rectángulos](/taller-matematicas/assets/images/area_sup-189x300.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/area_sup.png) Aproximación al área por rectángulos, tomando el extremo superior de cada intervalo: suma superior de Riemann[/caption]

Para los 2 rectángulos de la figura, la base sería$\triangle x=2/n=2/2=1$ y la suma de las áreas seria 1·4 + 1·9 = 13. En general, para n rectángulos, el área será

$\begin{array}{l}S_n=f\left(a+\triangle x\right)\triangle x+f\left(a+2\triangle x\right)\triangle x+\dots+f\left(a+n\triangle x\right)\triangle x\\=\triangle x{\textstyle\sum_{k=1}^n}f\left(a+k\triangle x\right)\end{array}$
Esta es una primera aproximación al área de la región debajo de la gráfica. Intuitivamente se ve que, a mayor número de rectángulos, menor error de aproximación. Para minimizar el error, pasamos al límite:

$\int_a^bf\left(x\right)\operatorname{d}x=\lim_{n\rightarrow\infty}S_n=\lim_{n\rightarrow\infty}\triangle x{\textstyle\sum_{k=1}^n}f\left(a+k\triangle x\right)=\lim_{n\rightarrow\infty}\frac{b-a}n{\textstyle\sum_{k=1}^n}f\left(a+k\triangle x\right)$

En nuestro ejemplo la suma de áreas de los rectańgulos es:

$\begin{array}{l}S_n=\overset n{\underset{k=1}\sum}\left(1+k\frac2n\right)^2=\frac2n\sum_{k=1}^n\left(\frac{n+2k}n\right)^2=\frac2n\sum_{k=1}^n\frac1{n^2}\left(n+2k\right)^2\\=\frac2{n^3}\left[\sum_{k=1}^nn^2+\sum_{k=1}^n4k^2+\sum_{k=1}^n4kn\right]=\frac2{n^3}\left[n\cdot n^2+4\sum_{k=1}^nk^2+\overset n{\underset{k=1}{4n\sum}}k\right].\end{array}$

Necesitamos ahora, para seguir, dos fórmulas de sumas parciales de series, que damos sin demostración:

$\begin{array}{l}1+2+3+\dots+n=\sum_{k=1}^nk=\frac{n\left(n+1\right)}2;\\1^2+2^2+3^2+\dots+n^2=\sum_{k=1}^nk^2=\frac{n\left(n+1\right)\left(2n+1\right)}6.\end{array}$

Usando estas fórmulas en la expresión del área total:

$\begin{array}{l}S_n=\frac2{n^3}\left[n\cdot n^2+4\sum_{k=1}^nk^2+\overset n{\underset{k=1}{4n\sum}}k\right]\\=\frac2{n^3}\left[n^3+4\frac{n\left(n+1\right)\left(2n+1\right)}6+4n\frac{n\left(n+1\right)}2\right]\end{array}$

Pasamos al límite, ignorando en la expresión anterior las potencias inferiores a $n^3$, que son despreciables cuando n tiende a infinito:

$\begin{array}{l}\lim_{n\rightarrow\infty}S_n=\lim_{n\rightarrow\infty}\frac2{n^3}\left[n^3+4\frac{n\left(n+1\right)\left(2n+1\right)}6+4n\frac{n\left(n+1\right)}2\right]\\=\lim_{n\rightarrow\infty}\frac{2n^3+{\displaystyle\frac{16}6}n^3+4n^3}{n^3}=2+\frac{16}6+4=\boxed{\frac{26}3}.\end{array}$

Por tanto, concluimos que $\int_1^3x^2\operatorname{d}x=\frac{26}3.$

**Sumas de Riemann superior e inferior**
En el ejemplo anterior, al calcular la altura del rectángulo $y=f(x)$ correspondiente al intervalo $\left(a+\left(k-1\right)\triangle x,a+k\triangle x\right)$ hemos tomado el extremo superior del intervalo, $x=a+k\triangle x$. La suma $S_n$ obtenida se llama suma superior de Riemann y la denotamos por $S_n$. Si tomamos el extremo inferior del intervalo, $x=a+\left(k-1\right)\triangle x$, la suma resultante se llama suma inferior de Riemann y la denotamos por $s_n$, su expresión en general es:

$\begin{array}{l}s_n=f\left(a\right)\triangle x+f\left(a+\triangle x\right)\triangle x+\dots+f\left(a+\left(n-1\right)\triangle x\right)\triangle x\\=\triangle x{\textstyle\sum_{k=0}^{n-1}}f\left(a+k\triangle x\right)\end{array}$

[caption id="attachment_681" align="alignnone" width="230"][![Aproximación al área tomando los extremos inferiores del intervalo](/taller-matematicas/assets/images/area_inf-230x300.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/area_inf.png) Aproximación al área tomando los extremos inferiores del intervalo: suma inferior de Riemann[/caption]

La pregunta que viene a la cabeza de forma natural es: ¿dará el mismo resultado que con la primera elección? En general, no. En este momento es cuando definimos realmente la integral de Riemann:
***Definición 2**: Sea una función $f(x)$ y un intervalo $(a,b)$ incluido en el dominio de la función. Si los límites de las umas de Riemann superior e inferior $\lim_{n\rightarrow\infty}S_n$ $y \lim_{n\rightarrow\infty}s_n$ existen y son iguales, decimos que la función es Riemann-integrable en $(a,b)$, y que $\lim_{n\rightarrow\infty}S_n=\lim_{n\rightarrow\infty}s_n=\int_a^bf\left(x\right)\operatorname{d}x.$*

¿Qué funciones serán Riemann-integrables? El siguiente teorema lo aclara:
**Teorema 1**: *integrabilidad según Riemann*

 	- *Si la función $f(x)$
es continua en el intervalo $(a,b)$, entonces es integrable en $(a,b)$*

 	- *Si la función $f(x)$ es acotada en el intervalo $(a,b)$ y continua excepto en un conjunto finito de puntos, entonces es integrable en $(a,b)$*

 	- *Si la función $f(x)$ es  acotada, y creciente o  decreciente en el intervalo $(a,b)$, entonces es integrable en $(a,b)$*

Todas las funciones usuales del cálculo, como las exponenciales, trigonométricas o polinómicas, son Riemann-integrables. Incluso algunas funciones más "exóticas" también lo son:

**Ejemplo 2**: Definimos la función escalonada siguiente

[caption id="attachment_682" align="alignnone" width="358"][![Función escalonada con infinitos puntos de discontinuidad](/taller-matematicas/assets/images/area2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/area2.png) Función escalonada con infinitos puntos de discontinuidad[/caption]

Sea el conjunto infinito de intervalos $\left(\frac12,\frac23\right),\left(\frac23,\frac34\right),\dots,\left(\frac n{n+1},\frac{n+1}{n+2}\right),\dots$, todos contenidos en $[0,1]$; para cada intervalo $\left(\frac n{n+1},\frac{n+1}{n+2}\right)$ definimos:

$f\left(x\right)=\left\{\begin{array}{l}1-\frac n{n+1}\;\text{si }x\in\left(\frac n{n+1},\frac{n+1}{n+2}\right),\;n=1,2,\dots\;\\0\;\text{en otro caso}\end{array}\right.$,

o sea:

$f\left(x\right)=\left\{\begin{array}{l}0\;\text{si }x\in\left(0,\frac12\right)\\1-\frac12\;\text{si }x\in\left(\frac12,\frac23\right)\\1-\frac23\;\text{si }x\in\left(\frac23,\frac34\right)\\\vdots\end{array}\right.$
Esta función no es continua, y tiene un número infinito de discontinuidades, una en cada intervalo; pero es acotada y creciente en el intervalo de definición $[0,1]$, luego es Riemann-integrable. Al ser una función escalonada es fácil obtener la suma de Riemann: la longitud del intervalo n-ésimo y la suma es :

$\begin{array}{l}\triangle x_n=\frac{n+1}{n+2}-\frac n{n+1}=\frac{\left(n+1\right)^2-n\left(n+2\right)}{\left(n+1\right)\left(n+2\right)}=\frac1{\left(n+1\right)\left(n+2\right)};\\f\left(x_n\right)=1-\frac n{n+1}=\frac1{n+1}\\S_n=\sum_{k=1}^n\frac1{k+1}\frac1{\left(k+1\right)\left(k+2\right)}=\sum_{k=1}^n\frac1{\left(k+1\right)^2\left(k+2\right)}=\frac1{12}+\frac2{36}+\dots\end{array}$

Pasando al límite:

$\lim_{n\rightarrow\infty}S_n=\lim_{n\rightarrow\infty}\sum_{k=1}^n\frac1{\left(k+1\right)^2\left(k+2\right)}\approx0.345$

la suma infinita la hemos obtenido con hoja de cálculo, sumando los 100 primeros términos.

**Ejemplo 3**: la función $y=1/x$ no es Riemann-integrable en $[0,1]$ ya que en $x=0$ ni es continua ni es acotada.

## Propiedades de la integral

 	- Linealidad: $\int_a^b\left(Af\pm Bg\right)\operatorname{d}x=A\int_a^bf\operatorname{d}x+B\int_a^bg\operatorname{d}x.$ Ejemplo: $\int_a^b\left(3x^3-4e^x\right)\operatorname{d}x=3\int_a^bx^3\operatorname{d}x-4\int_a^be^x\operatorname{d}x$

 	- Orden: si $f\left(x\right)\leq g\left(x\right)\Rightarrow\int_a^bf\operatorname{d}x\leq\int_a^bg\operatorname{d}x$. Ejemplo: $x^2&gt;\ln\left(x\right)\Rightarrow\int_a^bx^2\operatorname{d}x&gt;\int_a^b\ln\left(x\right)\operatorname{d}x$

 	- Partición del intervalo de integración: si $\left(a,b\right)=\left(a,m\right)\cup\left(m,b\right)x\Rightarrow\int_a^bf\operatorname{d}x=\int_a^mf\operatorname{d}x+\int_m^bf\operatorname{d}x.$ Ejemplo: $\left(-1,1\right)=\left(-1,0\right)\cup\left(0,1\right)\Rightarrow\int_{-1}^1f\operatorname{d}x=\int_{-1}^0f\operatorname{d}x+\int_{0m}^1f\operatorname{d}x$

 	- No conservación del producto: $\int_a^bf\cdot g\operatorname{d}x\neq\left(\int_a^bf\operatorname{d}x\right)\cdot\left(\int_a^bg\operatorname{d}x\right),$ en general. Ejemplo: $\int_0^\mathrm\pi x\cdot\sin\left(x\right)\operatorname{d}x\neq\left(\int_0^\mathrm\pi x\operatorname{d}x\right)\cdot\left(\int\sin\left(x\right)\operatorname{d}x\right),$ la primera integral vale $\pi$, las otras valen 2 y 5 respectivamente.

 	- Cambio de signo: si $\int_a^bf\operatorname{d}x=I\Leftrightarrow\int_a^b-f\operatorname{d}x=-I.$ Si calculamos áreas habrá que tener en cuenta que debemos tomar los valores absolutos. Ejemplo: el área delimitada por $f(x)=sin(x)$ entre $(0,2\mathrm\pi)$ no puede calcularse como $\int_0^{2\mathrm\pi}\sin\left(x\right)\operatorname{d}x$ ya que esta integral vale cero, debido a que la función $sin(x)$ cambia de signo periódicamente. El valor real del área será $A=\int_0^{2\mathrm\pi}\left|\sin\left(x\right)\right|\operatorname{d}x,$ o bien $A=\int_0^\mathrm\pi\left|\sin\left(x\right)\right|\operatorname{d}x+\left|\int_\mathrm\pi^{2\mathrm\pi}\sin\left(x\right)\operatorname{d}x\right|=2+2=4.$

 	- El área de un punto es nula: Para cualquier función $f(x)$ y cualquier punto $a$ se cumple $\int_a^af\operatorname{d}x=0$, equivale al área de una región delimitada por el intervalo $(a,a)$ de longitud nula. Como consecuencia, la integral de $f(x)$ en el intervalo abierto $(a,b)$ es la misma que en el intervalo cerrado $[a,b]$.

[caption id="attachment_691" align="alignnone" width="243"][![Para calcular áreas hemos de tener en cuenta los cambios de signo de la función](/taller-matematicas/assets/images/area3.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/area3.png) Para calcular áreas hemos de tener en cuenta los cambios de signo de la función[/caption]
##  Relación entre derivación e integración

La derivada de un función está relacionada con su variación local, así como con el problema de encontrar la recta tangente , mientras que la integral la hemos presentado como la solución al cálculo de áreas. en principio no parece haber ninguna relación, no obstante la hay:

***Teorema 2**: sea la función Riemann-integrable $f(x)$ y definamos la función $F(x)$ de la siguiente forma: $F(x)=\int_a^xf\operatorname{d}x$, donde $a, x$ son puntos dentro del dominio de $f(x).$ Entonces se cumple que $\frac{\operatorname{d}{F(x)}}{\operatorname{d}x}=F'(x)=f(x).$*

**Ejemplo 4**: la función $F(x)=\int_0^xf\left(x\right)\operatorname{d}x=\int_0^xx\operatorname{d}x$ nos da, para cada valor x, el área del triángulo rectángulo de base = altura = x, que sabemos es $A=\frac12x^2.$ Entonces $F(x)=\frac12x^2$, derivando, $F'(x)=x=f(x)$ como afirma el teorema.

[caption id="attachment_694" align="alignnone" width="300"][![Areas de los triángulos rectángulos de lado y altura iguales a x](/taller-matematicas/assets/images/area4-300x282.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/area4.png) Áreas de los triángulos rectángulos de lado y altura iguales. Para x=1 tenemos el triángulo de lados 1 y área 1/2, para x=2 el área es 2·2/2 = 1, etc. En general el área correspondiente al valor x será x²/2=F(x).[/caption]

También lo podemos ver aplicando la definición de derivada: el incremento relativo de área al pasar del valor x al valor x+h es:

$\frac{F(x+h)-F(x)}h=\frac{{\displaystyle\frac{(x+h)^2}2}-{\displaystyle\frac{x^2}2}}h=\frac{h^2+2xh}{2h}=\frac{h+2x}2$

Pasando al límite obtenemos la derivada de F:

$\lim_{h\rightarrow0}\frac{F(x+h)-F(x)}h=F'(x)=\lim_{h\rightarrow0}\frac{h+2x}2=x=f(x)$
## Integral indefinida. Función primitiva. Regla de Barrow

***Definición 3**: Sea la función integrable $f(x)$ y la función $F(x)$ derivable, tales que F'(x)=f(x). Entonces decimos que $F(x)$ es una **función primitiva** de $f(x)$, y la denotamos por $F(x)=\int f(x).$ Esta última integral, sin límites de integración, se llama **integral indefinida** de $f(x)$.*

**Ejemplo 5**: siguiendo con el ejemplo anterior, una función primitiva de $f(x)=x$ es $F(x)=x^2/2$. Pero también lo será $F_1(x)=x^2/2+1$, pues $F_1'(x)=F'(x)=x$. En general, cualquier función $F(x)=x^2/2+C$ con $Ck\in\mathbb{R}$ es una función primitiva de $f(x)=x.$ Hay pues infinitas funciones primitivas. Para el cálculo de áreas podemos tomar $C=0$, y en otras aplicaciones de la integral el valor de C dependerá del enunciado.

**Teorema 3** (primer *teorema fundamental del cálculo*): Si * $f(x)$ es integrable en $<em>\left[a,b\right]</em>$ y es continua en $x_0\in\left[a,b\right],$ entonces su función primitiva $F(x)$ es derivable en $x_0$ y se cumple
que $F'(x_0)=f(x_0)$.*

***Teorema 4** (segundo teorema fundamental del cálculo, o **Regla de Barrow**): Sea la función integrable $f(x)$ y una cualquiera de sus funciones primitiva $F(x)$. Entonces se cumple que $\int_a^bf\operatorname{d}x=F(b)-F(a).$*

Estos teoremas nos permiten relacionar la derivada, la función primitiva y la integral, pues:

$\begin{array}{l}\int_a^bf\operatorname{d}x=F(b)-F(a)\Leftrightarrow F'(b)=\lim_{a\rightarrow b}\frac{F(b)-F(a)}{b-a}=\lim_{a\rightarrow b}\frac1{b-a}\int_a^bf\operatorname{d}x\\=\frac1{b-a}\frac{f(b)}{b-a}=f(x)\end{array},$

ya que en la integral de Riemann que hemos explicado, $\lim_{a\rightarrow b}\int_a^bf\operatorname{d}x$ es el área de un rectángulo infinitesimal de base $b-a$ y altura $f(b)$, que es $(b-a)·f(b)$.

Además, en los casos prácticos de cálculo de integrales, lo que se hace es obtener la primitiva F de la función para después, aplicando la regla de Barrow, obtener la integral, ya que el cálculo directo usando las sumas de Riemann puede ser complicado y largo. Las técnicas de obtención de la función primitiva F se ven en el artículo [Cálculo de integrales](http://tallermatematic.eu/wp/?p=138). Ejemplos de aplicación de las integrales se verán en el artículo Problemas resueltos de aplicaciones de las integrales.

**Ejemplo 6**: siguiendo con el ejemplo anterior, una función primitiva de $f(x)=x$ es $F(x)=x^2/2$. Por tanto, $\int_0^2x\operatorname{d}x=F(2)-F(0)=\frac{2^2}2-\frac{0^2}2=2.$

***Teorema 4**: Las funciones primitivas tienen las siguientes propiedades:*

*1. La función primitiva (si existe) es siempre continua *

*2. La igualdad $F'(x)=f(x)$ se cumple en todos los puntos en los que $f(x)$ sea continua; en otros puntos no tiene porque cumplirse. Por tanto, una función puede ser integrable, podremos calcular su integral indefinida $I(x)=\int f\left(x\right)$, pero esta función $I(x)$ no tiene porque ser igual a su función primitiva en todos los puntos.*

*3. Si la función $f(x)$ es acotada e integrable (pero no necesariamente continua), existirá su  integral indefinida $I(x)$, pero puede existir o no su función primitiva $P(x)$; caso de que exista, el segundo teorema fundamental del cálculo asegura que $I(x)=P(x).$*

*4. Una función no integrable $f$ no tiene integral indefinida, pero en cambio sí puede tener función primitiva tal que $F'=f$, por tanto en este caso no podremos obtener $F$ haciendo la integral de $f.$*

**Ejemplo 7**: La función escalonada del ejemplo 2 es discontinua, acotada e integrable. ¿Existirá su integral indefinida? ¿Y su función primitiva?

Podemos calcular su integral indefinida $I\left(x_0\right)=\int_0^{x_0}f\left(x\right)$ dividiendo el intervalo de integración en subintervalos coincidentes con los escalones de la función y sumando todas la integrales; el último subintervalo será el que contendrá al valor $x_0$; esto es, $x_0\in\left(\frac n{n+1},\frac{n+1}{n+2}\right)\Leftrightarrow\frac n{n+1}\leq x_0&lt;\frac{n+1}{n+2},$ por tanto se cumplirá que $x_0&lt;\frac{n+1}{n+2}\Leftrightarrow\left(n+2\right)x_0&lt;n+1\Leftrightarrow n\left(x-1\right)+2x_0&lt;1\Leftrightarrow n&lt;\frac{1-2x_0}{x_0-1},$ como $n$ ha de ser un entero, recordando la definición de la [función parte entera](http://es.wikipedia.org/wiki/Funciones_de_parte_entera#Funci.C3.B3n_piso.2Fsuelo.2Fparte_entera) $E(x)$, resulta $n=E\left(\frac{1-2x_0}{x_0-1}\right).$ Por ejemplo, para $x_0=0.8$, será $n=E\left(\frac{1-2\cdot0.8}{0.8-1}\right)=E\left(4.\overset\frown6\right)=4,$ luego cogeríamos hasta el cuarto intervalo. En general:

$\begin{array}{l}I\left(x_0\right)=\int_0^{x_0}f\left(x\right)=\int_0^{1/2}f\left(x\right)+\int_{1/2}^{2/3}f\left(x\right)+\dots+\int_{n/\left(n+1\right)}^{x_0}f\left(x\right)\\=0+\frac12\left(\frac23-\frac12\right)+\dots+\frac1{n+1}\left(x_0-\frac n{n+1}\right)\\=\sum_{k=1}^{n-1}\left[\frac1{k+1}\frac1{\left(k+1\right)\left(k+2\right)}\right]+\frac1{n+1}\left(x_0-\frac n{n+1}\right)\end{array},$

con $n(x)=E\left(\frac{1-2x_0}{x_0-1}\right)$ que también es función de x. Entonces la integral indefinida  $\begin{array}{l}I\left(x\right)=\sum_{k=1}^{n-1}\left[\frac1{k+1}\frac1{\left(k+1\right)\left(k+2\right)}\right]+\frac1{n+1}\left(x-\frac n{n+1}\right)\end{array}$ existe, pero es claramente discontinua, porque la función parte entera $n(x)=E\left(\frac{1-2x_0}{x_0-1}\right)$ lo es, entonces por la propiedad 1 del teorema 4 la función primitiva, si existe, en este caso no puede ser igual a la integral indefinida. En general, las funciones escalonadas no tienen función primitiva.

**Ejemplo 8**: La función $f(x)$ definida en el intervalo cerrado $[0,2]$:

$f\left(x\right)=\left\{\begin{array}{l}x^2\;\text{si }0\leq x&lt;1\\2x\;\text{si }1\leq x\leq2\end{array}\right$

es discontinua en el punto $x=1:$

[![Exemple8_integral_Riemann_b](/taller-matematicas/assets/images/Exemple8_integral_Riemann_b-300x201.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/Exemple8_integral_Riemann_b.png)

Si calculamos su integral indefinida, tendremos que hacerlo por subintervalos: para $x_0&lt;1$ será $\int_0^{x_0}f\left(x\right)=\int_0^{x_0}x^2=\frac13x_0^2,$ mientras que para $1\leqx_0\leq2$ será $\int_0^{x_0}f\left(x\right)=\int_0^1x^2+\int_1^{x_0}2x=\frac13+\left[x^2\right]_1^{x_0}=\frac13+x_0^2-1,$ o sea que:

$I\left(x_0\right)=\int_0^{x_0}f\left(x\right)=\left\{\begin{array}{l}\frac13x_0^3\;\text{si }0\leq x&lt;1\\\frac13+x_0^2-1\;\text{si }1\leq x\leq2\end{array}\right.$

Esta función es continua: se deja como ejercicio comprobar que $\lim_{x_0\rightarrow1^-}I\left(x_0\right)=\lim_{x_0\rightarrow1^+}I\left(x_0\right)=I(1)=\frac13,$ su gráfica es:

[![Exemple8_integral_Riemann](/taller-matematicas/assets/images/Exemple8_integral_Riemann-300x197.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/Exemple8_integral_Riemann.png)

Pero a pesar de ser continua, $I(x)$ no es derivable en el punto $x=1$ (observar en la gráfica anterior el cambio brusco de pendiente en ese punto), se puede comprobar aplicando la definición de derivada en ese punto: $I'(1)=\lim_{x\rightarrow1}\frac{I\left(x\right)-I(1)}{x-1},$ al hacer los límites laterales $\lim_{x\rightarrow1^-}$ y $\lim_{x\rightarrow1^+}$ no coinciden (ejercicio para el lector), luego no existe la derivada en $x=1$.

Entonces, la función primitiva $F(x)$ no está definida para $x=1$, y se cumple que $F(x)=I(x)$ y que $F'(x)=f(x)$ para todo $x\in\left[0,2\right]$ excepto en $x=1.$
{% endraw %}