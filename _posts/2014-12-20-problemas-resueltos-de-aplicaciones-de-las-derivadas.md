---
layout: post
title: "Problemas resueltos de aplicaciones de las derivadas"
date: 2014-12-20 17:16:35 +0000
categories:
  - "Cálculo en R"
  - "Derivación"
  - "Funciones reales de variable real"
  - "Matemáticas"
tags:
  - "derivada"
  - "función"
math: true
---
{% raw %}

**1.** Comprobar que podemos aplicar el teorema de Rolle a la función $y=x-x^3$ en el intervalo $[-1,0]$, y hallar el valor particular para el que se cumple el teorema.
La función es derivable en todo $\mathbb{R}$. Los valores en los extremos coinciden: $f(-1)=0=f(0)$. Luego existe un $c\in\left$-1,0\right$$ tal que $f'(c)=0$. Para hallarlo simplemente resolvemos la ecuación $f'(x)=0\Leftrightarrow1-3x^2=0\Leftrightarrow x=\pm1/\sqrt3$, el valor $c=-1/\sqrt3$ es el que buscamos.

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)
**2.** Estudiar la existencia de valores máximos y mínimos de la función $\frac{x+1}{x^2+1}$ definida en el intervalo $[-1,0.5]$.

el intervalo $A=[-1,0.5]$ es cerrado y acotado, por tanto es un conjunto compacto (Teorema de Heine-Borel, ver [Cálculo en R -> Tolopologia de R](http://mathseng.blogspot.com.es/2014/02/topologia-de-r.html) ), además la función es contínua en $A$: las fracciones racionales $P(x)/Q(x)$ (cociente de polinomios) son continuas excepto en los puntos donde $Q(x)=0$, en nuestro caso es $x^2+1=0$ que no se cumple para ningun $x$ real. Entonces tenemos una función continua en un conjunto compacto, por el Teorema de Weierstrass (ver [Cálculo en R -> Funciones continuas]({{ site.baseurl }}/2014/09/07/calculo-en-r-funciones-continuas/), teorema 2) ha de tener un máximo y un mínimo absolutos en $A$. Además, la función es derivable (las fracciones racionales lo son). Entonces los máximos y mínimos absolutos o bien son  puntos donde la derivada vale 0, o bien estan en los extremos del intervalo de definición $A$. Calculamos la derivada:

$\begin{array}{l}D\left(\frac{x+1}{x^2+1}\right)=\frac{D\left(x+1\right)\cdot\left(x^2+1\right)-\left(x+1\right)\cdot D\left(x^2+1\right)}{\left(x^2+1\right)^2}=\\\frac{\left(1\right)\cdot\left(x^2+1\right)-\left(x+1\right)\cdot2x}{\left(x^2+1\right)^2}=\frac{x^2+1-2x^2-2x}{\left(x^2+1\right)^2}=\frac{-x^2-2x+1}{\left(x^2+1\right)^2}\end{array}$

Igualando a cero obtenemos:

$\frac{-x^2-2x+1}{\left(x^2+1\right)^2}=0\Rightarrow-x^2-2x+1=0\Rightarrow x=\frac{2\pm\sqrt{4+4}}{-2}=-1\pm\sqrt2$.

De estos dos puntos, solo uno de ellos, $x=-1+\sqrt2$, pertenece al dominio $A$, el otro punto lo descartamos. Para saber si el punto es un máximo/mínimo absoluto, tenemos que compararlo con los valores de la función en los extremos del intervalo $A$:

| **x** 
| **f(x)** 
|  

| $x=-1+\sqrt2$ 
| $1.207$ 
| máximo 

| $-1$ 
| $0$ 
| mínimo 

| $0.5$ 
| $1.2$ 
|  

Tenemos el máximo absoluto (también es un máximo relativo) en $x=-1+\sqrt2$ y el mínimo absoluto en el extremo inferior del intervalo, $x=-1.$

![Los mínimos y máximos locales pueden o no ser absolutos. Aquí, el máximo local es absoluto.](/taller-matematicas/assets/images/exercici2_aplic_derivadas-300x292.png) Los mínimos y máximos locales pueden o no ser absolutos. Aquí, el máximo local es absoluto.

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)

**3.** Calcular el límite $\lim_{x\rightarrow0}\frac{\tan\left(x\right)-\sin\left(x\right)}{x-\sin\left(x\right)}$ usando la regla de l'Hôpital.
$\lim_{x\rightarrow0}\frac{\tan\left(x\right)-\sin\left(x\right)}{x-\sin\left(x\right)}=\frac{0-0}{0-0}=\frac00=?$ el límite es indeterminado, y las funciones del numerador y denominador son derivables en el punto $x=0$, podemos aplicar l'Hôpital:

$\begin{array}{l}\lim_{x\rightarrow0}\frac{\tan\left(x\right)-\sin\left(x\right)}{x-\sin\left(x\right)}=\lim_{x\rightarrow0}\frac{D\left$\tan\left(x\right)-\sin\left(x\right)\right$}{D\left$x-\sin\left(x\right)\right$}=\\\lim_{x\rightarrow0}\frac{{\displaystyle\frac1{\cos^2\left(x\right)}}-\cos\left(x\right)}{1-\cos\left(x\right)}=\frac{{\displaystyle\frac11}-1}{1-1}=\frac00=?\end{array}$

seguimos teniendo una indeterminación del mismo tipo $0/0$, aplicamos de nuevo l'Hôpital:

$\begin{array}{l}\lim_{x\rightarrow0}\frac{{\displaystyle\frac1{\cos^2\left(x\right)}}-\cos\left(x\right)}{1-\cos\left(x\right)}=\lim_{x\rightarrow0}\frac{\displaystyle D\left$\frac1{\cos^2\left(x\right)}-\cos\left(x\right)\right$}{D\left$1-\cos\left(x\right)\right$}=\\\lim_{x\rightarrow0}\frac{\displaystyle\frac{2\sin\left(x\right)}{\cos^3\left(x\right)}+\sin\left(x\right)}{0+\sin\left(x\right)}=\frac{{\displaystyle\frac{2\cdot0}1}+0}{0+0}=\frac00=?\end{array}$

de nuevo tenemos una indeterminación del mismo tipo $0/0$, aplicamos otra vez l'Hôpital:

$\begin{array}{l}\lim_{x\rightarrow0}\frac{\displaystyle\frac{2\sin\left(x\right)}{\cos^3\left(x\right)}+\sin\left(x\right)}{\sin\left(x\right)}=\lim_{x\rightarrow0}\frac{\displaystyle D\left|\frac{2\sin\left(x\right)}{\cos^3\left(x\right)}+\sin\left(x\right)\right|}{D\left$\sin\left(x\right)\right$}=\\\lim_{x\rightarrow0}\frac{\displaystyle\frac{2\cos\left(x\right)\cos^3\left(x\right)+2\sin\left(x\right)\cdot3\cos^2\left(x\right)\sin\left(x\right)}{\cos^6\left(x\right)}+\cos\left(x\right)}{\cos\left(x\right)}=\\\lim_{x\rightarrow0}\frac{2\cos^2\left(x\right)+2\sin\left(x\right)\cdot3\sin\left(x\right)}{\cos^5\left(x\right)}+1=\frac{2+2\cdot0}1+1=3.\end{array}$

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)

**4.** Hallar el radio de la base de un cono con una generatriz de 2 unidades de longitud tal que el volumen del cono sea máximo.

| 

![Radio r, altura h y generatriz s de un cono](/taller-matematicas/assets/images/exercici4_aplic_derivadas-150x150.png) Radio r, altura h y generatriz s de un cono 
| El volumen de un cono de radio $r$ y altura $h$ es $V=\frac13\mathrm{πr}^2\mathrm h$. En el triángulo de la figura, siendo rectángulo, podemos aplicar Pitágoras: $s^2= h^2+r^2$, sustituyendo en la expresión del volumen: $V=\frac13\mathrm{πr}^2\mathrm h=\frac13\mathrm{πr}^2\sqrt{\mathrm s^2-\mathrm r^2}.$ 

Ahora que tenemos la expresión del volumen como una función del radio (dado que la generatriz tiene el valor dado 2), para hallar su máximo derivamos:

$\frac{dV}{dr}=\frac d{dr}\left$\frac13\mathrm{πr}^2\sqrt{\mathrm s^2-\mathrm r^2}\right$=\frac13\mathrm\pi\left(2\mathrm r\sqrt{\mathrm s^2-\mathrm r^2}+\mathrm r^2\frac12\frac{-2\mathrm r}{\sqrt{\mathrm s^2-\mathrm r^2}}\right)$

Los valores mínimos y máximos relativos son aquellos que hacen la derivada igual a cero, sustituyendo el valor dado $s=2$ obtenemos una ecuación con $r$ como incógnita:

$\begin{array}{l}\frac13\mathrm\pi\left(2\mathrm r\sqrt{4-\mathrm r^2}+\mathrm r^2\frac12\frac{-2\mathrm r}{\sqrt{4-\mathrm r^2}}\right)=0\Leftrightarrow\frac13\mathrm{πr}\left(2\sqrt{4-\mathrm r^2}-\frac{2\mathrm r^2}{\sqrt{4-\mathrm r^2}}\right)=0\Leftrightarrow\\\left\{\begin{array}{l}\mathrm r=0.\\2\sqrt{4-\mathrm r^2}-\frac{2\mathrm r^2}{\sqrt{4-\mathrm r^2}}=0\Leftrightarrow\frac{2\left(4-\mathrm r^2\right)-2\mathrm r^2}{\sqrt{4-\mathrm r^2}}=0\Leftrightarrow8-3\mathrm r^2=0\Leftrightarrow\mathrm r=\sqrt{\frac83}.\end{array}\right.\end{array}$

La solución $r=0$ evidentemente nos da el volumen mínimo $V=0$. La segunda solución $r=\sqrt{\frac83}$ es el candidato a máximo; como función de $r$ el volumen $V\left(r\right)\frac13\mathrm{πr}^2\sqrt{\mathrm s^2-\mathrm
r^2}$ está definida en el intervalo $\in\left$0,2\right$$, ya que no es posible tener un radio mayor que 2 si la generatriz es 2 (si $r=2$ tenemos  un cono degenerado: una recta, con volumen nulo); en ese intervalo la función volumen es una función continua, o sea que tenemos una función continua definida en un conjunto compacto, por lo tanto ha de tener mínimo y máximo abolutos. Como en los extremos del intervalo el volumen vale cero, el valor del volumen correspondiente a $r=\sqrt{\frac83}$ ha de ser el máximo, y valdrá $V=\frac13\pi\left(\sqrt{\frac83}\right)^2\sqrt{4-\left(\sqrt{\frac83}\right)^2}=\frac89\pi\sqrt{4-\frac83}=\frac89\pi\sqrt{\frac43}=\frac{16\pi}{9\sqrt3}.$

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)

**5.** Calcular el límite $\lim_{x\rightarrow0^+}\left(\cos\left(3x\right)\right)^{1/x^3}$ aplicando la regla de l'Hôpital.

$\lim_{x\rightarrow0^+}\left(\cos\left(3x\right)\right)^{1/x^3}=\cos\left(0\right)^{1/0}=1^\infty=?$, es una indeterminación que nos piden de resolver por l'Hôpital; para convertirlo a una indeterminación del tipo $0/0$ aplicamos logaritmos:

$L=\lim_{x\rightarrow0^+}\left(\cos\left(3x\right)\right)^{1/x^3}\Leftrightarrow\ln\left(L\right)=\lim_{x\rightarrow0^+}\frac1{x^3}\ln\left(\cos\left(3x\right)\right)$

Aplicamos l'Hôpital:

$\begin{array}{l}\lim_{x\rightarrow0^+}\frac{\ln\left(\cos\left(3x\right)\right)}{x^3}=\frac{\ln\left(1\right)}0=\frac00=\lim_{x\rightarrow0^+}\frac{D\left$\ln\left(\cos\left(3x\right)\right)\right$}{D\left$x^3\right$}=\\\lim_{x\rightarrow0^+}\frac{{\displaystyle\frac1{\cos\left(3x\right)}}\left(-\sin\left(3x\right)\cdot3\right)}{3x^2}=\lim_{x\rightarrow0^+}\frac{-\tan\left(3x\right)}{3x^2}=\frac00=?\end{array}$

Repetimos:

$\lim_{x\rightarrow0^+}\frac{-\tan\left(3x\right)}{x^2}=\lim_{x\rightarrow0^+}\frac{D\left$-\tan\left(3x\right)\right$}{D\left$x^2\right$}=\lim_{x\rightarrow0^+}\frac{-{\displaystyle\frac3{\cos^2\left(3x\right)}}}{x^2}=\frac{-3/1}0=-\infty$
Tenemos que, por las propiedades de los logaritmos, $\ln\left(L\right)=-\infty\Rightarrow L=0.$ Este es un caso un poco "especial", pues para aplicar la regla de l'Hôpital se necesita que el límite $f'(x)/g'(x)$ exista, y en el último paso hemos obtenido un infinito, que en rigor no es un límite, pero debido al uso del logaritmo del límite, el resultado ha sido correcto. Para asegurarnos, podemos estudiar aparte el último límite "sospechoso" por el método de obtener su serie de Taylor en el punto $x=0$, con los primeros términos bastará:

$\begin{array}{l}\tan\left(3x\right)=3x+9x^3+\frac{162x^5}5+O(x^6)\Leftrightarrow\\\frac{\tan\left(3x\right)}{x^2}=\frac3x+9x+\frac{162x^3}5+O(x^4)\end{array}$

Entonces el límite será:

$\lim_{x\rightarrow0^+}\frac{-\tan\left(3x\right)}{x^2}=\lim_{x\rightarrow0^+}-\left$\frac3x+9x+\frac{162x^3}5+O(x^4)\right$=\frac{-3}0-9\cdot0-\frac{162\cdot0}5-0=-\infty$

y llegamos al mismo resultado. De paso hemos visto un ejemplo de como aplicar la fórmula de Taylor en límites indeterminados.

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)**6.** Calcular el límite $\lim_{x\rightarrow0}\frac{\sin\left(x\right)\sin\left(2x\right)}{\left(x-x^2\right)\left(x+x^2\right)}$ aplicando la regla de l'Hôpital.

$\begin{array}{l}\lim_{x\rightarrow0}\frac{\sin\left(x\right)\sin\left(2x\right)}{\left(x+x^2\right)^2}=\frac{0\cdot0}0=?=\lim_{x\rightarrow0}\frac{D\left$\sin\left(x\right)\sin\left(2x\right)\right$}{D\left(x+x^2\right)^2}=\\\lim_{x\rightarrow0}\frac{\cos\left(x\right)\sin\left(2x\right)+\sin\left(x\right)\cos\left(2x\right)\cdot2}{2\left(x+x^2\right)\left(1+2x\right)}=\frac00=?\end{array}$

Vemos que al derivar el numerador se complica rápidamente; podemos ahorrarnos trabajo aplicando la siguiente propiedad de los límites: $\lim_{x\rightarrow a}f\left(x\right)\cdot g\left(x\right)=\lim_{x\rightarrow a}f\left(x\right)\cdot\lim_{x\rightarrow a}g\left(x\right)$. Si lo hacemos así resulta:

$\lim_{x\rightarrow0}\frac{\sin\left(x\right)\sin\left(2x\right)}{\left(x+x^2\right)^2}=\lim_{x\rightarrow0}\frac{\sin\left(x\right)}{x+x^2}\cdot\lim_{x\rightarrow0}\frac{\sin\left(2x\right)}{x+x^2}=\frac00\cdot\frac00$

Aplicamos l'Hôpital a cada límite por separado:

$\begin{array}{l}\lim_{x\rightarrow0}\frac{\sin\left(x\right)}{x+x^2}=\lim_{x\rightarrow0}\frac{D\left$\sin\left(x\right)\right$}{D\left$x+x^2\right$}=\lim_{x\rightarrow0}\frac{\cos\left(x\right)}{1+2x}=\frac11=1;\\\lim_{x\rightarrow0}\frac{\sin\left(2x\right)}{x+x^2}=\lim_{x\rightarrow0}\frac{D\left$\sin\left(2x\right)\right$}{D\left$x+x^2\right$}=\lim_{x\rightarrow0}\frac{2\cos\left(2x\right)}{1+2x}=\frac21=2.\end{array}$

Por tanto el límite pedido es $L=1\cdot2=2$.

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)

** 7.** Hallar el polinomio de Taylor que aproxima a la función $sin(x)$ para $x\in\left(0,1\right)$ con una precisión de al menos $1/500.$

La precisión del polinomio de Taylor viene dada por el término de Lagrange:

$\varepsilon_n(x)=\frac{f^{n+1}(d)}{\left(n+1\right)!}\left(x-c\right)^{n+1}$
Calculamos su valor, para n creciente y $c=0$, hasta que su máximo valor absoluto sea inferior a $1/500$; para ello en cada caso cogemos los valores *d*, *x* que proporcionen el máximo valor para $\varepsilon:$

$\begin{array}{l}\left|\varepsilon_1(x)\right|=\left|\frac{f^{''}(d)}{\left(2\right)!}\left(x-0\right)^2\right|=\left|\frac{-\sin\left(d\right)}2x^2\right|\leq\left|\frac{-\sin\left(1\right)}21^2\right|=0.4207;\\\left|\varepsilon_2(x)\right|=\left|\frac{f^{\left(3\right)}(d)}{\left(3\right)!}\left(x-0\right)^3\right|=\left|\frac{-\cos\left(d\right)}6x^3\right|\leq\left|\frac{-\cos\left(0\right)}61^3\right|=\frac16;\\\left|\varepsilon_3(x)\right|=\left|\frac{f^{\left(4\right)}(d)}{\left(4\right)!}\left(x-0\right)^4\right|=\left|\frac{\sin\left(d\right)}{24}x^4\right|\leq\left|\frac{\sin\left(1\right)}{24}1^4\right|=0.0351;\\\left|\varepsilon_4(x)\right|=\left|\frac{f^{\left(4\right)}(d)}{\left(4\right)!}\left(x-0\right)^4\right|=\left|\frac{\cos\left(d\right)}{120}x^4\right|\leq\left|\frac{\cos\left(0\right)}{120}1^4\right|=\frac1{120};\\\left|\varepsilon_5(x)\right|=\left|\frac{f^{\left(5\right)}(d)}{\left(5\right)!}\left(x-0\right)^5\right|=\left|\frac{-\sin\left(d\right)}{720}x^5\right|\leq\left|\frac{-\sin\left(1\right)}{720}1^5\right|=\frac1{720};\end{array}$

Por tanto el polinomio de Taylor será de grado 4:

$\begin{array}{l}f\left(x\right)=\sin(0)+\frac{\cos\left(0\right)}{1!}x+\frac{-\sin\left(0\right)}{2!}x^2+\frac{-\cos\left(0\right)}{3!}x^3+\frac{\sin\left(0\right)}{4!}x^4\\=x-\frac16x^3+\varepsilon_5\left(x\right)\end{array}.$

Por ejemplo, para $x=0.5$, el polinomio anterior vale $0.5-\frac160.5^3+\varepsilon_5\left(x\right)=\frac{23}{48}\approx0.4792$ mientras que el valor exacto es 0.4794 (redondeado con cuatro decimales), el error absoluto es de |0.4792-0.4794|=0.0002 < 1/500. ![separador2](/taller-matematicas/assets/images/separador2-300x37.png)
{% endraw %}