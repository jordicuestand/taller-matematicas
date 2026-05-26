---
layout: post
title: "Problemas resueltos de derivadas de funciones reales"
date: 2014-08-21 20:06:55 +0000
math: true
---
{% raw %}

**1.** Calcular la derivada de $f(x)=\sqrt{\sqrt x}.$

Usamos la regla derivación $f(x)=x^n\Rightarrow f'(x)=nx^{n-1}$, válida para todo $n$ distinto de -1. Para ello, expresamos las raíces como poténcias:

$\sqrt[n]{x^m}=x^\frac mn\Rightarrow\sqrt{\sqrt x}=\sqrt{x^\frac12}=\left(x^\frac12\right)^\frac12=x^\frac14.$

Luego:

$f'(x)=\frac{\operatorname{d}{}}{\operatorname{d}x}x^\frac14=\frac14x^{\frac14-1}=\frac14x^\frac{-3}4=\frac1{4x^{\displaystyle\frac34}}=\frac1{4\sqrt[4]{x^3}}.$

---

 

**2.** Calcular la derivada de $f(x)=e^{x+\cos\left(x^2-1\right)}.$

Usamos la derivada de la función exponencial:

$\frac{\operatorname{d}{}}{\operatorname{d}x}e^{f(x)}=f'(x)\cdot e^{f(x)}\Rightarrow\frac{\operatorname{d}{}}{\operatorname{d}x}e^{x+\cos\left(x^2-1\right)}=\frac{\operatorname{d}{}}{\operatorname{d}x}\left(x+\cos\left(x^2-1\right)\right)\cdot e^{x+\cos\left(x^2-1\right)}.$

Aparte, derivamos la función exponente, aplicando la regla de la cadena:

$\frac{\operatorname{d}{}}{\operatorname{d}x}\left(x+\cos\left(x^2-1\right)\right)=1-\sin\left(x^2-1\right)\cdot\left(2x\right).$

Resultado final:

$f'(x)=2x\left(1-\sin\left(x^2-1\right)\right)\cdot e^{x+\cos\left(x^2-1\right)}.$

---

** 3.** Obtener la recta tangente a la gráfica de la función $f(x)=\sqrt{x^2-1}$ en el punto $(\sqrt{2},1).$
La recta tangente a $f(x)$ en el punto $x_0$ tiene la ecuación $y=mx+c$ donde $m=f'(x_0)$ y ademas ha de cumplirse que $f(x_0)=mx_0+c$. Derivemos la función para obtener la pendiente de la recta tangente:

$f'(x)=\frac{2x}{2\sqrt{x^2-1}},\;f'(\sqrt2)=\frac{\sqrt2}{\sqrt{2-1}}=\sqrt2.$

Imponemos la condición $f(x_0)=mx_0+c$:

$f(\sqrt2)=\sqrt{2-1}\;=1=\sqrt2\cdot\sqrt2+c\Leftrightarrow c=-1.$

La recta tangente es pues: $y=\sqrt2x-1.$ En la imagen vemos la gráfica de $f(x)$, con dominio $\left|x\right|\geq1$, y en rojo la recta tangente por el punto $(\sqrt{2},1).$

[caption id="attachment_257" align="alignnone" width="633"][![y=(x²-1)^0.5 y su recta tangente en (2^0.5, 1), en rojo](/assets/images/Exer3_Derivades.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/Exer3_Derivades.png) y=(x²-1)^0.5 y su recta tangente en (2^0.5, 1), en rojo[/caption]

---

 

**4.  **Calcular las distancias mínima y máxima desde el centro de coordenadas a la elipse $4x^2+y^2-2y-3=0.$

Queremos los valores extremos de la distancia entre el origen $(0,0)$ y la elipse; la distancia entre dos puntos cualquiera del plano $P, Q$ con coordenadas $P=\left(P_x,P_y\right),Q=\left(Q_x,Q_y\right)$ viene dada (en un espacio Euclídeo) por $d(P,Q)=\sqrt{\left(P_x^2-Q_x^2\right)+\left(P_y^2-Q_x^2\right)}$; en el caso de que $Q$ es el origen $(0,0)$, entonces la distancia es simplemente $\sqrt{x^2+y^2}$. Esta es la función de la que queremos encontrar los valores extremos, sujeta a la condición de que $(x,y)$ pertenezca a la elipse:

Extremos de: $f\left(x,y\right)=\sqrt{x^2+y^2},\;\text{sujeta a: }4x^2+y^2-2y-3=0.$
Podemos aplicar dos métodos: a) multiplicadores de Lagrange, b) pasar la ecuación de la elipse a forma explícita $y=f(x)$, sustituir en la función distancia $d(x,y(x))=d(x)$ y derivar para encontrar los extremos.  Usaremos éste último método; operando:

$\begin{array}{l}4x^2+y^2-2y-3=0=0\Leftrightarrow y^2-2y+\left(4x^2-3\right)=0\Rightarrow\\y\left(x\right)=\frac{2\pm\sqrt{4-4\cdot\left(4x^2-3\right)}}2=1\pm\sqrt{1-4x^2+3}=1\pm2\sqrt{-x^2+1}.\end{array}$

Observemos que de hecho tenemos dos funciones, debido al signo $\pm$, debido a que la elipse, que es una curva cerrada, no puede representarse por una función: para cada valor de x tenemos dos valores de y, así pues, necesitamos dos funciones.

 

[caption id="attachment_243" align="aligncenter" width="297"][![Una curva cerrada; a cada valor x le corresponden dos valores y](/assets/images/elipse.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/elipse.png) Una curva cerrada; a cada valor x le corresponden dos valores y[/caption]
Sustituimos la expresión de $y(x)$ en la función $d^2(x,y)$:

$\begin{array}{l}\begin{array}{l}y\left(x\right)=1\pm2\sqrt{-x^2+1}\Rightarrow\\d^2\left(x,y\right)=d^2\left(x\right)=x^2+\left(1\pm2\sqrt{-x^2+1}\right)^2=x^2+1+4\left(-x^2+1\right)\pm4\sqrt{-x^2+1}=\end{array}\\-3x^2+5\pm4\sqrt{-x^2+1}.\end{array}$

En vez de derivar la función $d(x)$, trabajaremos con la función distancia al cuadrado $d^2(x)$, pues será más fácil de derivar, y los valores extremos son los mismos (una función positiva $f(x)$ siempre tiene los mismos puntos extremos $x$ que la función $f^2(x)$):

$\begin{array}{l}\frac{\operatorname{d}{}}{\operatorname{d}x}\left(-3x^2+5\pm4\sqrt{-x^2+1}\right)=-6x\pm4\frac{-2x}{2\sqrt{-x^2+1}}=-6x\pm\frac{4x}{\sqrt{-x^2+1}}=0\Rightarrow\\-6x\sqrt{-x^2+1}\pm4x=0\Rightarrow x\left(-6\sqrt{-x^2+1}\pm4\right)=0\Rightarrow\\\left\{\begin{array}{l}\boxed{x=0}\\-6\sqrt{-x^2+1}=0\pm4\Rightarrow\sqrt{-x^2+1}=\pm\frac23.\end{array}\right.\end{array}$

La solución de $\sqrt{-x^2+1}=-\frac23$ no existe, pues la raíz siempre devolverá un número no negativo; nos quedamos pues con las soluciones $x=0$ y $\sqrt{-x^2+1}=\frac23\Rightarrow x=\sqrt{1-\frac49}=\sqrt{\frac59}=\frac{\sqrt5}3.$
Para ver si estos valores son máximos o mínimos absolutos bastará con sustituirlos en la función $d(x)$ y compararlos, no es necesario calcular la derivada segunda y estudiar su signo, ¿por qué? La función  $d(x)$ está definida en el dominio $[-1,1]$, y es acotada en ese dominio, además es contínua, por lo que seguro que tiene un máximo y un mínimo absoluto, que puede estar dentro del intervalo $(-1,1)$ o bien en los extremos $x=-1, x=1$. Comprobemos estos valores:

$\begin{array}{l}d^2\left(\frac{\sqrt5}3\right)=-3\left(\frac{\sqrt5}3\right)^2+5+4\sqrt{-\left(\frac{\sqrt5}3\right)^2+1}=\frac{10}3+\frac8{\sqrt5}\approx6.9,\\d^2(0)=9,\\d^2(-1)=-3+5=2,\\d^2(1)=-3+5=2.\end{array}$

Vemos que en $x=0$ tenemos la distancia máxima $d^2(0)=9\Rightarrow d=3$ y en $x=\frac{\sqrt5}3\right)$ la distancia mínima $d^2\left(\frac{\sqrt5}3\right)=\frac{10}3+\frac8{\sqrt5}\Rightarrow d\approx2.6.$ En la imagen siguiente vemos la gráfica de la elipse.

[caption id="attachment_254" align="alignnone" width="226"][![Elipse 4x²+y²-2y-3=0](/assets/images/elipse1.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/elipse1.png) Elipse 4x²+y²-2y-3=0 (gráfica realizada con WolframAlpha)[/caption]

---

**5.** Supongamos que la función $f(x)$ es derivable con derivada $f'(x)$ continua, y que $f(0)=0, f'(0)=1$. Si definimos la función $g(x)$:

$g(x)=\left\{\begin{array}{l}xf(x)\;\text{si }x\neq0\\0\;\text{si }x=0,\end{array}\right.$

calcular la función derivada de  $g(x)$. ¿Es continua $g'(x)$?
Cuando $x\neq0$ la función $g(x)$ coincide con la función $xf(x)$, así pues: $g'(x)=f(x)+xf'(x)$ cuando $x\neq0$. Para $x=0$ no podemos usar las reglas de derivación habituales, pues en las proximidades de $x=0$ la función $g(x)$ cambia su expresión; en este caso tenemos que aplicar la definición de derivada:

$g'(0)=\lim_{h\rightarrow0}\frac{g(0+h)-g(0)}h=\lim_{h\rightarrow0}\frac{xf(h)-0}h=\lim_{h\rightarrow0}\frac{0\cdot f(h)}h=0\cdot\lim_{h\rightarrow0}\frac{f(h)}h.$

Como $f(x)$ es derivable en $x=0$, y ademas $f(0)=0, f'(0)=1$, se cumple que:

$f'(0)=\lim_{h\rightarrow0}\frac{f(0+h)-f(0)}h=\lim_{h\rightarrow0}\frac{f(h)-0}h=\lim_{h\rightarrow0}\frac{f(h)}h=1\Rightarrow\\g'(0)=0\cdot\lim_{h\rightarrow0}\frac{f(h)}h=0\cdot1=0.$

En conclusión:

$g'(x)=\left\{\begin{array}{l}f(x)+xf'(x),\;\text{si }x\neq0\\0,\;\text{si }x=0.\end{array}\right.$

Para ver si $g'(x)$ es continua, estudiamos primero el caso $x$ distinto de cero: siendo la función $f$ derivable, se sigue que ha de ser contínua; también sabemos que $f'(x)$ es continua, luego el producto $x·f'(x)$ es también continuo por ser producto de funciones continuas. Así pues, $g'(x)$ es continua siempre que $x$ sea distinto de cero.

En el caso $x=0$, aplicamos la definición de continuidad: $g'(x)$ es continua en 0 si se cumple $\lim_{x\rightarrow0}g'(x)=g'(0)=0:$

$\lim_{x\rightarrow0}g'(x)=\lim_{x\rightarrow0}\left(f(x)+xf'(x)\right)=\lim_{x\rightarrow0}f(x)+\lim_{x\rightarrow0}xf'(x)=0+0\cdot f'(0)=0\cdot1=0,$

ya que por ser $f(x)$ y $f'(x)$ continuas, se cumple $\lim_{x\rightarrow0}f(x)=f(0)=0,\lim_{x\rightarrow0}f'(x)=f'(0)=1$ ; como $g'(0)=0$, concluimos que la función derivada $g'(x)$ es continua en todos los puntos.

---

**6.** Sean las funciones $f(x)=x^2+1, g(x)=x^3-2x^2$. Calcular los valores que toma la función compuesta $h=f\circ g$ y su derivada $h'(x)$ en el punto $x=1$.

Tenemos $h(x)=\left(f\circ g\right)(x)=f\left(g\left(x\right)\right)$, y aplicando la regla de la cadena:

$h'(x)=\left(f\circ g\right)'(x)=f'\left(g\left(x\right)\right)\cdot g'(x).$

Con estos resultados ya podemos responder:

$\begin{array}{l}g(1)=1^3-2\cdot1^2=-1,\\h(1)=f\left(g(1)\right)=f(-1)=\boxed2,\\f'(x)=2x\Rightarrow f'\left(g(1)\right)=f'(-1)=-2,\\g'(x)=3x^2-4x\Rightarrow g'(1)=-1,\\h'(x)=f'(g(1))\cdot g'(1)=-2\cdot(-1)=\boxed2.\end{array}$

Alternativamente, podríamos haber obtenido la expresión de la función $h(x)$ y derivarla para obtener el mismo resultado:

$\begin{array}{l}h(x)=\left(x^2+1\right)\circ\left(x^3-2x^2\right)=\left(x^3-2x^2\right)^2+1\Rightarrow\\h'(x)=2\left(x^3-2x^2\right)\left(3x^2-4x\right),\\h(1)=\left(1^3-2\cdot1^2\right)^2+1=2,\\h'(1)=2\left(1^3-2\cdot1^2\right)\left(3\cdot1^2-4\cdot1\right)=2\cdot(-1)=-2.\end{array}$

---

**7.** Dada la función

$\begin{array}{l}f(x)=\left\{\begin{array}{c}x-1,\;\text{si }x\leq0\\\frac1x,\;\text{si }0&lt;x\leq1\\e^{x-1},\;\text{si }1&lt;x\end{array}\right.\\\\\\\end{array}$

Estudiar su derivabilidad, y calcular, donde exista, la función derivada.

La función no es continua en $x=0$, pues:

$\lim_{x\rightarrow0^+}f(x)=\lim_{x\rightarrow0^+}\frac1x=+\infty$

así que no puede ser derivable en $x=0$ (recordemos que derivable $\begin{array}{c}\Rightarrow\\\nLeftarrow\end{array}$ continua).

En $x=1$ si es continua, pues $\lim_{x\rightarrow1^-}f(x)=\frac11=1=\lim_{x\rightarrow1^+}f(x)=e^{1-1}=e^0,$ por tanto podemos tener derivada en $x=1$; para comprobarlo, necesitamos aplicar la definición de derivada en un punto:

$f'(1)=\lim_{x=1,\;h\rightarrow0}\frac{f\left(x+h\right)-f\left(x\right)}h=\lim_{h\rightarrow0}\frac{f\left(1+h\right)-f\left(1\right)}h,$
pero hemos de ser cuidadosos en este punto: el valor de $f(1+h)$ depende de por dónde nos acercamos a $x=1$: si nos acercamos por la izquierda toma el valor $1/(1+h)$, si nos acercamos por la derecha entonces el valor es $e^{1-1+h}$; por esta razón hemos de calcular los límites laterales, y solo si coinciden ambos podremos asegurar que existe el límite. Estos límites laterales, cuando calculamos derivadas, se llaman derivadas laterales:

$\begin{array}{l}f'(1^-)=\lim_{x=1,\;h\rightarrow0^-}\frac{f\left(x+h\right)-f\left(x\right)}h=\lim_{\;h\rightarrow0^-}\frac{f\left(1+h\right)-f\left(1\right)}h=\\\lim_{\;h\rightarrow0^-}\frac{{\displaystyle\frac1{1+h}}-1}h=\lim_{\;h\rightarrow0^-}\frac{1-1-h}{\left(1+h\right)h}=\lim_{\;h\rightarrow0^-}\frac{-1}{1+h}=-1.\end{array}$

$\begin{array}{l}\begin{array}{l}f'(1^+)=\lim_{x=1,\;h\rightarrow0^+}\frac{f(x+h)-f(x)}h=\lim_{h\rightarrow0^+}\frac{f(1+h)-f(1)}h=\lim_{h\rightarrow0^+}\frac{e^{1-1+h}-1}h=\\\lim_{h\rightarrow0^+}\frac{e^h-1}h=\frac00=?.\end{array}\\\end{array}$

Nos encontramos con un límite indeterminado del tipo $0/0$, aplicamos la regla de L'Hôpital, aplicable con cocientes de funciones derivables:

$L=\lim_{x\rightarrow a}\frac{f(x)}{g(x)}=\frac00=?\Leftrightarrow L=\lim_{x\rightarrow a}\frac{f'(x)}{g'(x)}$

Nos da:

$L=\lim_{h\rightarrow0}\frac{e^h-1}h=\lim_{h\rightarrow0}\frac{{\displaystyle\frac{\operatorname{d}{}}{\operatorname{d}h}}\left(e^h-1\right)}{\frac{\operatorname{d}{}}{\operatorname{d}h}h}=\lim_{h\rightarrow0}\frac{e^h}1=\frac11=1.$

Observamos que no coinciden las derivadas laterales, por consiguiente no existe la derivada en el punto $x=1$. Podemos ya escribir la función derivada $f'(x)$ en todos los puntos:

$f'(x)=\left\{\begin{array}{l}1,\;x&lt;0\\\text{no existe en }x=0\\\frac{-1}{x^2},0&lt;x&lt;1\\\text{no existe en }x=1\\e^{x-1},\;x&gt;1\end{array}\right.$

En la siguiente ilustración vemos la gráfica de la función $f(x)$. En el punto $x=1$ la función es continua, pero presenta un "pico" que hace que la tangente a la curva en ese punto esté indefinida, luego no hay derivada.

[![Exer7_Derivades](/assets/images/Exer7_Derivades.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/Exer7_Derivades.png)

La gráfica de la función derivada muestra discontinuidades en los puntos donde no está definida:

[![Exer7b_Derivades](/assets/images/Exer7b_Derivades.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/Exer7b_Derivades.png)

---
{% endraw %}