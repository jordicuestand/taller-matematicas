---
layout: post
title: "Examen-1 resuelto de Cálculo"
date: 2016-10-16 08:58:44 +0000
categories:
  - "Cálculo en R"
  - "Derivación"
  - "Funciones reales de variable real"
  - "Integración"
  - "Matemáticas"
  - "Métodos numéricos"
tags:
  - "análisis matemático"
  - "Cálculo"
  - "problemas resueltos de cálculo"
math: true
---
{% raw %}

**1.** Estudiar la continuidad o en su caso, discontinuidad, en x=1, de la función real:

$f\left(x\right)=\left\{\begin{array}{l}\sin\left(\mathrm\pi x\right)\right),\;x\leq1\\\frac{x-1}{x+1},\;x&gt;1\end{array}\right.$

Solución: Para que sea continua en el punto, ha de cumplir la condición de que el límite en ese punto coincida con el valor de la función en el punto:

$\underset{x\rightarrow1}{lim}f\left(x\right)=f\left(1\right)=\sin\left(\mathrm\pi\right)=-1$

El límite en x = 1 hay que calcularlo según las dos ramas de la función (límites laterales), ya que precisamente en ese punto se bifurca la función; límite por la derecha,

$\underset{x\rightarrow1^+}{lim}\frac{x-1}{x+1}=\frac{0^+}{2^+}=0$

límite por la izquierda,

$\underset{x\rightarrow1^-}{lim}\sin\left(\mathrm{πx}\right)=\sin\left(\mathrm\pi\right)=-1$

Vemos que los límites laterales no coinciden, luego no existe el límite en el punto x=1, y por tanto la función no puede ser continua. Además, al no coincidir los límites laterales, en x=1 hay una discontinuidad de salto (o no evitable), pero los dos límites son finitos, así pues el salto es finito: es una discontinuidad de 1a especie.

**2.** Dada la función $1-\frac1{x^2+2}$ realizar 5 iteraciones del método del punto fijo tomando como punto inicial x=0.

Solución: El método del punto fijo genera una sucesión de valores a partir de un valor inicial: {x_0, x_1=f(x_0), x_2=f(x_1), ...}, que converge a un punto x tal que f(x) = x. En nuestro caso esta sucesión es:

$\begin{array}{l}x_1=f\left(0\right)=1-\frac1{0^2+2}=\frac12;\\x_2=f\left(\frac12\right)=1-\frac1{\left(\frac12\right)^2+2}=1-\frac1{\displaystyle\frac94}=\frac59;\\x_3=f\left(\frac59\right)=1-\frac1{\left(\frac59\right)^2+2}=\frac{106}{187}\approx0.5668;\\x_4=f\left(\frac{106}{187}\right)=1-\frac1{\left(\frac{106}{187}\right)^2+2}\approx0.5692;\\x_5=f\left(0.5692\right)=1-\frac1{\left(\frac{106}{187}\right)^2+2}=0.5697\end{array}$

Vemos que un punto fijo de esta función está cerca de  x=0.5692 pues para este valor el punto y su imagen por f prácticamente coinciden: $f\left(0.5692\right)=0.5697$

**3.** Calcular $\int_0^1\frac{3x}{\left(3x^2+1\right)^2}\operatorname dx$

Solución: Primero calculamos la integral indefinida; es del tipo inmediato $\int\frac{f'\left(x\right)}{\left[f\left(x\right)\right]^n}=\frac{\left[f\left(x\right)\right]^{n+1}}{n+1},\;n&gt;1$, pues la derivada del denominador, sin tener en cuenta la potencia, es casi igual al numerador, excepto por un factor constante que podemos añadir:

$\int\frac{3x}{\left(3x^2+1\right)^2}\operatorname dx=\frac12\int\frac{6x}{\left(3x^2+1\right)^2}\operatorname dx=\frac12\frac{\left(3x^2+1\right)^3}3$

Ahora aplicamos la regla de Barrow para calcular la integral definida:

$\frac16\left[\left(3x^2+1\right)^3\right]_0^1=\frac16\left[4^3-1^3\right]=\frac{21}2.$

**4.** Calcular los puntos extremos de la función $f\left(x\right)=\frac{1-x^2}{x-3}$ en el intervalo [-1, 1].

Solución: Para encontrar los posibles extremos relativos calculamos la derivada de la función y la igualamos a cero:

$\begin{array}{l}f'\left(x\right)=\frac{D\left(1-x^2\right)\cdot\left(x-3\right)-\left(1-x^2\right)D\left(x-3\right)}{\left(x-3\right)^2}=\frac{-2x\left(x-3\right)-\left(1-x^2\right)}{\left(x-3\right)^2}=\\\frac{-2x^2+6x-1+x^2}{\left(x-3\right)^2}=\frac{-x^2+6x-1}{\left(x-3\right)^2}=0;\\x=\frac{-6\pm\sqrt{36-4\left(-1\right)\left(-1\right)}}{-2}=\frac{-6\pm\sqrt{32}}{-2}=3\pm\sqrt8\approx\left\{\begin{array}{l}5.3\\0.17\end{array}\right.\end{array}$

Tenemos dos posibles puntos extremos relativos, pero sólo uno de ellos cae en el intervalo [-1, 1], el punto x=0.17; para ver si es máximo o mínimo local, calculamos la derivada segunda y sustituimos:

$\begin{array}{l}f'\left(x\right)=\frac{-x^2+6x-1}{\left(x-3\right)^2}\Rightarrow f''\left(x\right)=\frac{\left(-2x+6\right)\left(x-3\right)^2-2\left(x-3\right)\left(-x^2+6x-1\right)}{\left(x-3\right)^4};\\f''(0.17)=\frac{45.28}{64.14}&gt;0\end{array}$

como el signo es positivo, tenemos un mínimo relativo. Pasamos a estudiar los extremos absolutos: estudiamos los valores de la función en los extremos del intervalo [-1, 1]:  f(-1) = 0, f(1) = 0. Los comparamos con el valor de la función en el mínimo relativo, que es f(0.17) = -0.3. Como la función es continua en el intervalo [-1, 1], concluimos que en ese intervalo toma sus valores máximos en x = -1, x = 1, y su valor mínimo en x=0.17.

[![examen1](/taller-matematicas/assets/images/examen1.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/12/examen1.png)

 

** 5.** Dada la función de dos variables

$f\left(x,y\right)=\left\{\begin{array}{l}\frac{x^3}{x^2+y^2},\;\left(x,y\right)\neq\left(0,0\right)\\0,\;\left(x,y\right)=\left(0,0\right)\end{array}\right.$

Calcular sus derivadas parciales en (0, 0)  y estudiar su diferenciabilidad en el origen.

Solución: En el punto (0, 0) la función se bifurca en dos ramas, así que no podemos usar las fórmulas de derivación usuales, hay que aplicar la definición de derivada parcial:

$\frac{\partial f}{\partial x}=\underset{h\rightarrow0}{lim}\frac{f\left(x+h,y\right)-f\left(x,y\right)}h;\;\frac{\partial f}{\partial y}=\underset{h\rightarrow0}{lim}\frac{f\left(x,y+h\right)-f\left(x,y\right)}h$

Las aplicamos a la función dada en el punto (0, 0):

$\begin{array}{l}\frac{\partial f}{\partial x}=\underset{h\rightarrow0}{lim}\frac{\frac{\left(x+h\right)^3}{\left(x+h\right)^2+y^2}-0}h=\underset{h\rightarrow0}{lim}\frac{\left(x+h\right)^3}{h\left(x+h\right)^2+hy^2}\xrightarrow{}\frac{x^3}0=\infty\\\end{array}$

La derivada parcial según x en (0, 0) no existe; vamos por la otra derivada parcial:

$\begin{array}{l}\frac{\partial f}{\partial y}=\underset{h\rightarrow0}{lim}\frac{\frac{\left(x\right)^3}{\left(x\right)^2+\left(y+h\right)^2}-0}h=\underset{h\rightarrow0}{lim}\frac{x^3}{x^2+y^2+h^2+2yh}\xrightarrow{}\frac{x^3}{x^2+y^2}\\\end{array}$
vemos que según la dirección y sí tenemos derivada en el origen. Vamos a ver si es diferenciable: no puede serlo, pues las funciones diferenciables tienen derivadas parciales en cualquier dirección, esto es, no solo han de existir las derivadas parciales, sino que además se exige que existan las derivadas direccionales en cualquier dirección. Si la función hubiera tenido derivadas parciales, entonces tendríamos que haber comprobado si también tenía derivadas direccionales. Otra posibilidad para ver que es diferenciable, es probar que tiene derivadas parciales que además sean continuas.
{% endraw %}