---
layout: post
title: "Cálculo en R -> Funciones continuas - > Problemas resueltos"
date: 2014-09-13 09:26:50 +0000
categories:
  - "Cálculo en R"
  - "Funciones continuas"
  - "Funciones reales de variable real"
  - "Matemáticas"
tags:
  - "asíntota"
  - "conjunto acotado"
  - "conjunto cerrado"
  - "Continuidad"
  - "continuidad a trozos"
  - "continuidad uniforme"
  - "dominio"
  - "función creciente"
  - "funciones"
  - "supremo"
  - "Teorema de Weierstrass"
math: true
---
{% raw %}

**1.** Consideramos las funciones que cumplen la igualdad $f\left(\alpha x\right)=\alpha f\left(x\right)$ para cualquier $\alpha\in\mathbb{R}.$ Encontrar la forma explícita de todas las funciones de ese tipo. ¿Son uniformemente continuas en $\mathbb{R}.$?

Consideremos dos puntos $x_1, x_2=\alpha x_1$. Se cumple:

$\frac{y_2}{x_2}=\frac{f\left(x_2\right)}{x_2}=\frac{f\left(\alpha x_1\right)}{\alpha x_1}=\frac{\alpha f\left(x_1\right)}{\alpha x_1}=\frac{\alpha y_1}{\alpha x_1}=\frac{y_1}{x_1}.$

Como $\alpha$ puede ser cualquier valor, la igualdad anterior es cierta para todos los valores $x_1,y_1,x_2,y_2$, y la razón $y/x$ es una constante: $\frac yx=C\Leftrightarrow\boxed{y=Cx}.$ Ésta es la forma general de las funciones que buscábamos.

Es fácil ver ahora que son uniformemente continuas:

$f\left(x\right)=Cx\Rightarrow\left|y_1-y_2\right|\leq R\Leftrightarrow\left|Cx_1-Cx_2\right|\leq R\Leftrightarrow\left|C\right|\cdot\left|x_1-x_2\right|\leq R\Leftrightarrow\left|x_1-x_2\right|\leq\frac R{\left|C\right|}.$

Tomando $r=\frac R{\left|C\right|}$ se cumple la condición de continuidad uniforme: dado un $R$ cualquiera, si se cumple $\left|y_1-y_2\right|\leq R$ entonces existe un $r$ tal que $\left|x_1-x_2\right|\leq r$ (ver, si es necesario, la [teoría de continuidad]({{ site.baseurl }}/2014/09/07/calculo-en-r-funciones-continuas/)).

---

**2.** Estudiar la continuidad de la función dada por:
$\left\{\begin{array}{l}\sqrt{x^2-1}\;\text{si }x\in\left(-\infty,-1\right),\\x^2+2x+1\;\text{si }x\in\left$-1,10\right$,\\\frac{121}{10}x\;\text{si }x\in\left(10,+\infty\right).\end{array}\right.$

La primera expresión de la función, $\sqrt{x^2-1}\;\text{si }x\in\left(-\infty,-1\right),$ es la composición de dos funciones:

$f(x)=\sqrt{x^2-1}\;=f_1(x)\circ f_2(x),\;f_1(x)=\sqrt x,\;f_2(x)=x^2-1.$
Ambas funciones $f_1, f_2$ son continuas, luego su composición también lo es. No obstante, la función $f_1(x)=\sqrt x$ sólo está definida para $x\geq0$, por tanto la función compuesta también estará definida sólo en $x^2-1\geq0\Rightarrow\left|x\right|\geq1$, que es compatible con el intervalo de definición dado, $x\in\left(-\infty,-1\right), $ hasta aquí tenemos continuidad.

La siguiente expresión es un polinomio de segundo grado, que es continuo en todo el dominio. La última expresión también lo es. Ahora queda estudiar los puntos de enlace entre las tres expresiones, donde tendremos que aplicar la definición de continuidad:

**Definición 1**: Si $f:A\subset\mathbb{R}\rightarrow\mathbb{R}$ y el punto $a$ pertenece al conjunto de puntos de acumulación de $A$, $a\in\text{Acum}\left(A\right)$, diremos que $f$ es continua en $a$ si existe el límite $L=\lim_{x\rightarrow a}f\left(x\right)\neq\pm\infty$ y además se cumple que $L=f(a)$. 

Para el punto $x=-1$, donde pasamos de la expresión 1 a la 2, hacemos los límites laterales:

$\begin{array}{l}\lim_{x\rightarrow-1^-}f(x)=\sqrt{-1^2-1}=0;\\\lim_{x\rightarrow-1^+}f(x)=-1^2+2(-1)+1=0;\\\end{array}$

Puesto que coinciden entre sí en el valor $L=-1$, y además $f(-1)=-1=L$. la función es continua en $x=-1$. Para el otro punto de transición, $x=10$, procedemos igual:

$\begin{array}{l}\lim_{x\rightarrow10^-}f(x)=10^2+2(10)+1=121;\\\lim_{x\rightarrow-1^+}f(x)=\frac{121}{10}10=121;\\\end{array}$

los límites laterales coinciden, luego el límite en $x=10$ toma el valor 121, que es el mismo que f(10), y la función es continua en ese punto. En conclusión, $f(x)$ es continua en todo su dominio.

---

**3.** Estudiar la continuidad de  $f(x)=\frac{\sqrt{1+2x}-\sqrt{1+55x}}{x+\sqrt{x+1}}.$

La función será continua en todo punto $a$ en que $\lim_{x\rightarrow a}f\left(x\right)=f\left(a\right);$ como es una función irracional (por la presencia de raíces), será continua en todo su dominio. Además, como la expresión de la función tiene un cociente, también tendremos en cuenta el dominio de las funciones racionales:

 	- funciones del tipo $f\left(x\right)=\frac{g(x)}{h(x)}$: tienen dominio $\mathbb{R}-\left\{x:\;g(x)=0\right\}$

 	- funciones del tipo $f\left(x\right)=\sqrt[n]x$ con $n$ par: tienen dominio $\mathbb{R}-\left\{x:\;g(x)&lt;0\right\}$

Lo aplicamos; primero el cociente:

$\begin{array}{l}x+\sqrt{x+1}=0\Rightarrow x=-\sqrt{x+1}\Rightarrow x^2=x+1\Rightarrow x^2-x-1=0\Rightarrow\\x=\frac{1\pm\sqrt{1+4}}2=\left\{\begin{array}{l}\frac{1+\sqrt5}2\\\frac{1-\sqrt5}2\end{array}\right.\end{array}$

Siempre que elevamos una expresión al cuadrado, se genera una solución que no lo es de la ecuación original; comprobamos las dos obtenidas:

$\begin{array}{l}x=\frac{1+\sqrt5}2\Rightarrow x+\sqrt{x+1}\approx3.236\neq0;\\x=\frac{1-\sqrt5}2\Rightarrow x+\sqrt{x+1}=0.\end{array}$

La solución "buena" es por tanto $x=\frac{1-\sqrt5}2.$ Ahora estudiamos el dominio de las funciones irracionales:

$\frac{\sqrt{1+2x}-\sqrt{1+55x}}{x+\sqrt{x+1}}\rightarrow\left\{\begin{array}{l}1+2x\geq0\Rightarrow x\geq\frac{-1}2\\1+55x\geq0\Rightarrow x\geq\frac{-1}{55}\\x+1\geq0\Rightarrow x\geq-1.\end{array}\right.$

Para encontrar el dominio de $f(x)$ imponemos todas las condiciones simultáneamente:

$Dom\;f\left(x\right)=\left\{x\neq\frac{1-\sqrt5}2\right\}\;\text{y }\left\{x\geq\frac{-1}{55}\right\}\;\text{y }\left\{x\geq\frac{-1}2\right\}\;\text{y }\left\{x\geq-1\right\}$

Imponer varias restricciones, como es el caso, equivale a encontrar la intersección de todas ellas: sustituimos algunas expresiones por sus valores calculados aproximados, para poder compararlas:

$\begin{array}{l}\left\{x\neq-0.618\right\}\cap\left\{x\geq-0.0\overset\frown{18}\right\}\cap\left\{x\geq\frac{-1}2\right\}\cap\left\{x\geq-1\right\}=\\\left\{x\geq-0.0\overset\frown{18}\right\}\end{array}$

La última condición implica todas las demás. Nos queda por tanto $Dom\;f\left(x\right)=\left\{x:\;x\geq\frac{-1}{55}\right\}$ y la función es continua en ese dominio.

---

**4.** Demostrar que la ecuación $x^5+4x^3-2x+2=0$ tiene al menos una solución real.
Definimos la función $f\left(x\right)=x^5+4x^3-2x+2$ que es continua en todo $\mathbb{R}$ por ser un polinomio. Buscamos algunos puntos para encontrar un cambio de signo en la función:

$\begin{array}{c}\begin{array}{ccccc}\left.x\right|&amp;-2&amp;-1&amp;0&amp;1\\\left.f\left(x\right)\right|&amp;-58&amp;-1&amp;2&amp;5\end{array}\end{array}$

Vemos que hay un cambio de signo entre $x=-1$ y $x=0$, por el Teorema de Bolzano ha de existir al menos un $c\in\left(-1,0\right)$ tal que $f(c)=0.$

---

**5**. ¿Existe alguna función continua tal que no alcance (no tome valores en) su supremo ni si ínfimo? Si es así, ¿contradice el Teorema de Weierstrass de funciones continuas?

Hay infinitas funciones como las que nos piden: las funciones con asíntotas horizontales no alcanzan nunca ciertos valores. Por ejemplo, la función:

![f(x)= 1+exp(x) si x=0](/taller-matematicas/assets/images/ni_suprem_ni_infim.png) f(x)= 1+exp(x) si x<0, 1èxp(-x) si x>=0

$f\left(x\right)=\left\{\begin{array}{l}1+e^x\;\text{si }x&lt;0\\1+e^{-x}\;\text{si }x\geq0\end{array}\right.$

es continua en todos sitios, tiene una asíntota horizontal en $y=1$ y ademas está acotada; en efecto:

$\lim_{x\rightarrow0^-}f\left(x\right)=1+e^0=2=\lim_{x\rightarrow0^+}f\left(x\right)=1+e^{-0}=f(0).$ luego es continua.

$\begin{array}{l}{\text{Máx}}_{x&lt;0}1+e^x=2;\;{\text{Mín}}_{x&lt;0}1+e^x=1;\\{\text{Máx}}_{x\geq0}1+e^{-x}=2;\;{\text{Mín}}_{x\geq0}1+e^{-x}=1;\end{array}$

Luego está acotada superiormente por 2 e inferiormente por 1.

$\lim_{x\rightarrow\infty}f\left(x\right)=1+e^{-\infty}=1;\;\lim_{x\rightarrow-\infty}f\left(x\right)=1+e^{-\infty}=1,$

luego
$y=1$ es una asíntota horizontal.
Observemos que $1&lt;f\left(x\right)\leq2$ así que la función no alcanza nunca su valor ínfimo (la mayor de las cotas inferiores). En cambio si que alcanza su valor supremo $y=2$ en $x=0$. Necesitamos una función con dos asíntotas horizontales distintas, por ejemplo:

![Función con dos asíntotas horizontales](/taller-matematicas/assets/images/ni_suprem_ni_infim2.png) Función con dos asíntotas horizontales

$\left\{\begin{array}{l}\frac{5x^2-1}{x^2}\;\text{si }x&lt;-1\\\frac{7-x}2\;\text{si }-1\leq x\leq1\\\frac{2x^2+1}{x^2}\;\text{si }x&gt;1\end{array}\right.$
El lector puede comprobar, por el mismo método del ejemplo anterior, que esta función tiene una asíntota a la derecha  $y=2$, otra asíntota a la izquierda $y=5$ y que es continua en todos los puntos. En este caso la función no alcanza ni su supremo $y=5$ ni su ínfimo $y=2$. Esto no contradice el teorema de Weierstrass (recordemos que nos dice que toda función continua en un compacto alcanza su valor máximo y su mínimo) puesto que el dominio de definición debería ser un compacto (un conjunto cerrado y acotado), mientras que para esta función el dominio es todo $\mathbb{R}$, que no es cerrado ni acotado.

En cambio, si limitamos el dominio de esta forma:

$\left\{\begin{array}{l}\frac{5x^2-1}{x^2}\;\text{si}-2\leq x&lt;-1\\\frac{7-x}2\;\text{si}-1\leq x\leq1\\\frac{2x^2+1}{x^2}\;\text{si}1&lt;x\leq2\end{array}\right.$

entonces el dominio de definición es el conjunto cerrado y acotado $[-2, 2]$, el Teorema de Weierstrass es aplicable, y la función alcanza su mínimo en $x=2$ y su máximo en $x=-2$.

---

 **6.** ¿Es posible que la composición de dos funciones que no sean ambas continuas, pueda ser continua? Dar algún ejemplo.

Una de las propiedades de las funciones continuas es:
$f,g$ funciones continuas $\begin{array}{c}\Rightarrow\\\nLeftarrow\end{array}f\circ g,\;g\circ f$ continuas

o sea que, si $f,g$ son continuas, seguro que $f\circ g,\;g\circ f$ también lo son, en cambio si $f$ o $g$ no son continuas, no podemos concluir nada. Por tanto sí es posible que la composición de dos funciones que no sean ambas continuas, pueda ser continua.

Como ejemplo veamos las funciones valor absoluto $f\left(x\right)=\left|x\right|$ y la función siguiente:

$g\left(x\right)=\left\{\begin{array}{l}1\;\text{si }x&lt;0\\-1\;\text{si }x\geq0\end{array}\right.$

Esta segunda función es claramente discontinua en $x=0$, pero en cambio veamos que pasa con $f\circ g:$

$f\circ g\left(x\right)=\left\{\begin{array}{l}f\left(1\right)\;\text{si }x&lt;0\\f\left(-1\right)\;\text{si }x\geq0\end{array}\right.=\left\{\begin{array}{l}1\;\text{si }x&lt;0\\1\;\text{si }x\geq0\end{array}\right.$

O sea que $h=f\circ g$ es la función constante $h(x)=1$, que es continua.

---

**7.** Estudiar la continuidad de la función:

$f\left(x\right)=\left\{\begin{array}{l}x\;\text{ si }x\;\text{ es racional}\\1-x\;\text{ si }x\;\text{ es irracional}\end{array}\right.$

Necesitamos recordar la siguiente propiedad de los números reales y racionales:

Entre dos números reales cualesquiera, existen infinitos números reales (racionales e irracionales). En particular, entre dos números racionales cualesquiera, existen infinitos números reales (racionales e irracionales). 
Entonces, dado un racional cualquiera $a\in\mathbb{Q}$, si intentamos calcular el límite $\lim_{x\rightarrow a\in\mathbb{Q}}f\left(x\right)$, nos encontramos con problemas, pues tenemos que aplicar las dos definiciones de la función, no importa lo cerca que nos aproximemos al punto $a$. Más precisamente, si aplicamos la definición de límite, dado un $\delta&gt;0$, no existe un $\varepsilon&gt;0$ tal que, si $\left|x-a\right|&lt;\varepsilon$ entonces $\left|f\left(x\right)-f\left(a\right)\right|&lt;\delta$, pues en el intervalo centrado en *a* $\left(a-x,\;a+x\right)$ con $\left|a-x\right|&lt;\varepsilon$ existen infinitos racionales e infinitos irracionales, y no todos ellos estarán dentro del intervalo $\left(f\left(a\right)-\delta,\;f\left(a\right)+\delta\right).$ Hay una excepción: si vemos la gráfica de la función nos daremos cuenta.

![Función discontinua en todos los puntos, excepto en x=1/2](/taller-matematicas/assets/images/discontinua_tot_punt.png) Función discontinua en todos los puntos, excepto en x=1/2
Las dos rectas contienen infinitos puntos, pero no todos: la de pendiente positiva contiene los racionales, la otra los irracionales.  Vemos pues que dado cualquier $x=a$, por ejemplo, $a=1$, en cualquier entorno de ese punto hay infinitas imágenes en las dos rectas, cuando nos acercamos al punto $a$ la función va oscilando entre las dos rectas. Pero en el punto $x=1/2$ se cruzan ambas . En ese punto:

$\lim_{x\rightarrow1/2}f\left(x\right)=\left\{\begin{array}{l}\frac12\;\text{si }x\;\text{es racional}\\1-\frac12\;=\frac12\;\text{si }x\;\text{es irracional}\end{array}\right.$

Entonces el límite existe y vale $1/2$, que además coincide con el valor de la función en $x=1$, con lo cual podemos afirmar que $f(x)$ es continua en $x=1$ y discontinua en cualquier otro punto.

---

**8.** Supongamos que $f(x)$ es continua en todo $\mathbb{R}$, y que $f(x)=0$ para todo $x$ racional. Probar que $f(x)$ ha de ser la función nula $f(x)=0$ para todo $\mathbb{R}$.

Definimos $f$ como sigue:

$f\left(x\right)=\left\{\begin{array}{l}0\;\;\;\;\;\text{si }x\;\text{esracional}\\g\left(x\right)\;\text{si }x\;\text{esirracional}\end{array}\right.$
donde $g(x)$ es desconocida. Nos piden que demostremos que $g(x)=0$. Siguiendo el razonamiento del ejercicio anterior, dado un racional cualquiera $a\in\mathbb{Q}$, si intentamos calcular el límite $\lim_{x\rightarrow a\in\mathbb{Q}}f\left(x\right)$, nos encontramos con problemas, pues tenemos que aplicar las dos definiciones de la función, no importa lo cerca que nos aproximemos al punto $a$. Entonces, la única forma de que la función sea continua en todos los puntos es que tomen el mismo valor en las dos ramas de la función, esto es, que $g(x)=0$.

---

**9.** Sea la función continua $f(x)$ definida en el intervalo cerrado $[a,b]$. Definimos la función $g(x)$ de la siguiente forma: $g(a)=f(a)$, y para valores distintos de $a$, definimos $g\left(x_0\right)=\text{Max }\left\{f\left(x\right)\left|x\in\left$a,x_0\right$\right.\right\}$. Estudiar la continuidad de $g(x)$.
En primer lugar nos damos cuenta de que la función $g(x)$ tiene sentido, está bien definida, esto es, para cada valor $x$ existe la imagen $g(x)$; en efecto, como $f(x)$ es continua, alcanzará su valor máximo en todo intervalo cerrado (Teorema de Weierstrass). Al definir $g(y)$ com el valor máximo de $f(x)$ en el intervalo cerrado $[a,x]$, aseguramos que ese máximo existe.

En segundo lugar, es fácil ver que $g(x)$ es una función creciente: a medida que aumentamos los valores de $x$, el máximo de $f(x)$ en el intervalo  $[a,x]$ no puede disminuir por definición: o bien no aumenta, o bien encontramos un nuevo máximo mayor que el anterior.

Además, siendo $f$ continua, al movernos de un valor $x$ a otro próximo $x+\varepsilon$ las imágenes no pueden variar "demasiado", esto es, la variación estará acotada, y también los valores máximos de $f$  han de estarlo; por ello, dado un $\delta&gt;0$, siempre podremos encontrar un $\varepsilon&gt;0$ tal que si $\left|x_1-x_2\right|&lt;\varepsilon$ entonces la variación en los máximos en los intervalos $$a,x_1$$ y $$a,x_2$$ no será mayor que $\varepsilon$: la función $g$ es continua.

Como ejemplo concreto, consideremos $f(x)=\sin\left(x\right)$ en $\left$0,2\pi\right$$, y representemos $f,g$:

![Función f(x)=Sin(x) (azul), y función g(x) (verde)](/taller-matematicas/assets/images/Apostol_4_19.png) Función f(x)=Sin(x) (azul), y función g(x) (verde)

Vemos que $g(x)$ coincide con $f(x)$ en $\left$0,\pi/2\right$$ hasta que $f(x)$ alcanza su valor máximo absoluto en $x=\pi/2$, a partir de ahí $g(x)$ queda constante.

---

 

**10.** Estudiar la continuidad de la función

$\left\{\begin{array}{l}\frac2x,\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;x\leq-2\\\frac1{x+2},\;\;\;\;\;\;\;-2&lt;x\leq1\\\frac{x-1}{x^2-5x+4},\;x&gt;1,\;x\neq4\\2,\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;x=4\end{array}\right.$
$2/x$ es continua para todo $x\ne0$, como esta rama de la función está definida para $x\leq-2$, esta primera rama es continua.

Igualmente, $\frac1{x+2}$ es continua excepto en $x=-2$, que no pertenece al dominio de esta rama: $-2&lt;x\leq1.$

$\frac{x-1}{x^2-5x+4}$ es continua excepto en los puntos que cumplen $x^2-5x+4=0,$ que son $x=1,\;x=4,$ que tampoco pertenecen al dominio de esta tercera rama de la función.

Así pues, la función es continua en cada rama de su definición; falta comprobar los puntos de unión de cada rama; en esos puntos, como tenemos una definición "doble" de la función (el punto está en la intersección de dos ramas) hay que calcular los límites laterales.

En $x=-2$ tenemos:

$\begin{array}{l}\lim_{x\rightarrow-2^-}f\left(x\right)=\frac2{-2}=-1;\\\lim_{x\rightarrow-2^+}f\left(x\right)=\frac1{-2^++2}=\frac1{0^+}=+\infty\end{array}$

El límite no existe, y $f(x)$ no es continua en $x=-2$. Para el siguiente punto,  $x=1$ tenemos:

$\begin{array}{l}\lim_{x\rightarrow1^-}f\left(x\right)=\frac1{1+2}=\frac13;\\\lim_{x\rightarrow1^+}f\left(x\right)=\frac{1^+-1}{1^+-5^++4}=\frac{0^+}{0^{}}=?\end{array}$

Para resolver la indeterminación del segundo límite simplificamos la fracción:

$\lim_{x\rightarrow1^+}\frac{x-1}{x^2-5x+4}=\lim_{x\rightarrow1^+}\frac{x-1}{\left(x-4\right)\left(x-1\right)}=\lim_{x\rightarrow1^+}\frac1{x-4}=\frac1{-3}$

Como no coinciden los límites laterales, no existe el límite, y la función es discontinua en $x=1$. Para $x=4$ los límites laterales  izquierda no existen, por ejemplo, por la izquierda: $\lim_{x\rightarrow4^-}f\left(x\right)=\lim_{x\rightarrow4^-}\frac1{x-4}=\frac1{0^-}=-\infty, $ y la función tampoco es continua en ese punto.

En resumen, $f(x)$ es continua en todo $\mathbb{R}$ excepto en $x=-2,\;1,\;4.$

![a_trossos](/taller-matematicas/assets/images/a_trossos.png)

---

**11**. Una función lineal f(x) se define por los siguientes valores de la función:
      

| **x** 
| 
2

 
| 
6

 
| 
50

 
| 
n

 

| **f(x)** 
| 
-1

 
| 
-13

 
| 
m

 
| 
-100

 

 

Encontrar los valores m, n.

Solución: las funciones lineales tienen la forma f(x) = Ax + B. Con los datos de la tabla podemos encontrar A, B. Planteamos dos ecuaciones, usando las parejas de valores (x, f(x)) de la tabla (2, -1) y (6, -13):

$\begin{array}{l}-1\;=\;2A\;+\;B\\-13\;=\;6A\;+\;B\end{array}$

Este es un sistema lineal de dos ecuaciones con dos incógnitas; restamos las dos ecuaciones (método de reducción) para eliminar la B, que està en las dos, para ello, cambiamos todos los signos de la primera ecuación y sumamos ámbas:

$\begin{array}{l}\begin{array}{l}1\;=\;-2A\;-\;B\\\underline{-13\;=\;6A\;+\;B}\end{array}\\-12=4A\Leftrightarrow A=-12/4=-3\\\end{array}$

Luego B = -1 -2A = -1 +6 = 5. Ya tenemos que f(x) = -3x + 5.

Ahora es inmediato encontrar m, n:

m = f(50) = -3·50 + 5 = **-145,**

-100 = f(n) = -3·n + 5 → n = (-100 – 5) / -3 = -105/-3 = **35**.

---
{% endraw %}