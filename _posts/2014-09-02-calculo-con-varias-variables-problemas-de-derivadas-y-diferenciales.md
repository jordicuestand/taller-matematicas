---
layout: post
title: "Cálculo con varias variables -> Problemas de derivadas y diferenciales"
date: 2014-09-02 05:32:12 +0000
categories:
  - "Cálculo en varias variables"
  - "Derivabilidad de funciones de varias variables"
  - "Funciones reales de dos variables"
  - "Matemáticas"
tags:
  - "derivada parcial"
  - "diferencial"
math: true
---
{% raw %}

**1.** Dada la función $f(x,y,z)=3x+y+z^2$, y las funciones $g(u,v)=uv, h(u,v)=sin(u)+3, k(u,v)=exp(u)$, calcular el gradiente de la función $f(g(u,v),h(u,v),k(u,v))$ en el punto $(u,v)=(1,0)$.

Lo haremos de dos formas: una más corta pero menos rigurosa, otra más larga pero rigurosa.

Primera forma de hacerlo: sustituimos las definiciones de las funciones g, h, k de dos variables en la función f  de tres variables para obtener una nueva función compuesta de dos variables:

$\begin{array}{l}f(g(u,v),h(u,v),k(u,v))=3g(u,v)+h(u,v)+\left(k(u,v)\right)^2=\\3\cdot uv+(\sin(u)+3)+\left(e^u\right)^2=3uv+\sin\left(u\right)+3+e^{2u}.\end{array}$

Es como si la "x" pasara a ser la función g(u,v), la "y" pasara a ser h(u,v) y la "z" pasara a ser la función k(u,v). El resultado es una nueva función $F(u,v)=3uv+\sin\left(u\right)+3+e^{2u}.$ El gradiente de esta función es:

$\nabla F(u,v)=\begin{bmatrix}\frac{\partial F}{\partial u}\\\frac{\partial F}{\partial v}\end{bmatrix}=\begin{bmatrix}3v+\cos\left(u\right)+2e^{2u}\\3u\end{bmatrix}.$

Para el punto $(u,v)=(1,0)$ el gradiente vale:

${\begin{bmatrix}3v+\cos\left(u\right)+2e^{2u}\\3u\end{bmatrix}}_{\left(1,0\right)}=\begin{bmatrix}\cos\left(1\right)+2e^2\\3\end{bmatrix}.$

Segunda forma de hacerlo: aplicando la definición de la regla de la cadena para la derivada de la función compuesta, $D\left(f\circ g\right)\left(x,y\right)=\left(Df\circ g\left(x,y\right)\right)\cdot Dg\left(x,y\right).$ ¿Cuáles son las funciones que componemos en este problema? Veamos, tenemos:

$f:\mathbb{R}^3\rightarrow\mathbb{R},\;g,h,k:\mathbb{R}^2\rightarrow\mathbb{R},\;f(g,h,k):\mathbb{R}^2\rightarrow\mathbb{R},$

la composición resultante es:

$\begin{array}{l}\mathbb{R}^2\;\;\longrightarrow\;\;\mathbb{R}^3\;\;\longrightarrow\;\;\mathbb{R}\\(u,v)\rightarrow\left(x,y,z\right)\rightarrow f\left(x,y,z\right)\end{array},$

definimos pues la función $F(u,v)=\left(g(u,v),h(u,v),k(u,v\right),\;F:\mathbb{R}^2\rightarrow\mathbb{R}^3,$ y nos queda la composición $f\circ F\left(u,v\right):\mathbb{R}^3\rightarrow\mathbb{R}.$ Obtenemos el gradiente de esta composición aplicando la regla de la cadena:

$D\left(f\circ F\right)\left(u,v\right)=\left(Df\circ F\left(u,v\right)\right)\cdot DF\left(u,v\right)$

$Df=\begin{bmatrix}\frac{\operatorname{d}f}{\operatorname{d}x}\\\frac{\operatorname{d}f}{\operatorname{d}y}\\\frac{\operatorname{d}f}{\operatorname{d}z}\end{bmatrix}=\begin{bmatrix}3\\1\\2z\end{bmatrix};$

$Df\circ F\left(u,v\right)=\begin{bmatrix}3\\1\\2z\end{bmatrix}\circ\begin{bmatrix}uv\\\sin\left(u\right)+3\\e^u\end{bmatrix}=\begin{bmatrix}3\\1\\2e^u\end{bmatrix};$

$DF(u,v)=\begin{bmatrix}\frac{\operatorname{d}F}{\operatorname{d}u}\\\frac{\operatorname{d}F}{\operatorname{d}v}\end{bmatrix}=\begin{bmatrix}v&amp;\cos\left(u\right)&amp;e^u\\u&amp;0&amp;0\end{bmatrix}.$

Nos queda pues:

$D\left(f\circ F\right)\left(u,v\right)=\begin{bmatrix}v&amp;\cos\left(u\right)&amp;e^u\\u&amp;0&amp;0\end{bmatrix}\cdot\begin{bmatrix}3\\1\\2e^u\end{bmatrix}=\begin{bmatrix}3v+\cos\left(u\right)+2e^{2u}\\3u\end{bmatrix}.$

En el punto $(u,v)=(1,0)$ el gradiente vale:

$D\left(f\circ F\right)\left(1,0\right)=\begin{bmatrix}3\cdot0+\cos\left(1\right)+2e^{2\cdot1}\\3\cdot1\end{bmatrix}=\begin{bmatrix}\cos\left(1\right)+2e^2\\3\end{bmatrix},$

el mismo resultado que con el primer método.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
 **2.** Estudiar la continuidad y derivabilidad en el origen de la función de dos variables dada por:

$f(x,y)=\left\{\begin{array}{l}\frac{x^3\sin\left(x+y\right)}{x^2+y^2},\;(x,y)\neq(0,0)\\0,\;\;(x,y)=(0,0)\end{array}\right.$

La diferenciabilidad en un punto implica la continuidad, pero en el enunciado nos preguntan sobre la derivabilidad, que es un concepto distinto: la derivada en una función de varias variables siempre ha de calcularse a lo largo de una recta: es la derivada direccional; la recta viene dada por un vector director unitario $u$, y la el valor de la derivada direccional de $f(v)$, siendo $v$ un vector, viene dada por

Definición 1: $\frac{\partial f\left(\overset\rightharpoonup v\right)}{\partial\overset\rightharpoonup u}=\lim_{h\rightarrow0}\frac{f\left(\overset\rightharpoonup v+h\overset\rightharpoonup u\right)-f\left(\overset\rightharpoonup v\right)}h.$

En el caso particular de que las rectas sean los ejes de coordenadas entonces estamos calculando las derivadas parciales de la función; por ejemplo, según el eje x será, para el caso de una función de dos variables:

Definición 2: $\frac{\partial f\left(\overset\rightharpoonup v\right)}{\partial\left(1,0\right)}=\frac{\partial f\left(x,y\right)}{\partial x}=\lim_{h\rightarrow0}\frac{f\left(x+h,y\right)-f\left(x,y\right)}h$

La diferenciabilidad es más "exigente" que la derivabilidad, en el sentido de que si la función es diferenciable entonces seguro que es derivable, però la afirmación contraria no es cierta:

diferenciabilidad $\begin{array}{l}\Rightarrow\\\nLeftarrow\end{array}$ derivabilidad

Como consecuencia de todo esto, la función puede ser derivable pero no continua ni diferenciable, o puede ser continua pero no derivable. Tendremos que estudiar la continuidad y la derivabilidad independientemente.

Continuidad en el origen

Definimos la curva general  en coordenadas polares $x=r\cos\left(\theta\right),\;y=r\sin\left(\theta\right),\;r\geq0,\;0\leq\theta\leq2\mathrm\pi$, y hallamos el límite para $r\rightarrow0$, esto es, nos acercamos al origen haciendo que este parámetro $r$ tienda a cero. Primero hallamos la expresión de la función en coordenadas polares:

$\begin{array}{l}x=r\cos\left(\theta\right),\;y=r\sin\left(\theta\right)\Rightarrow f\left(x,y\right)=\frac{\left(r\cos\left(\theta\right)\right)^3\sin\left(r\cos\left(\theta\right)+r\sin\left(\theta\right)\right)}{\left(r\cos\left(\theta\right)\right)^2+\left(r\sin\left(\theta\right)\right)^2}\\=\frac{r^3\cos^3\left(\theta\right)\cdot\sin\left(r\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)}{r^2\left(\cos^2\left(\theta\right)+\sin^2\left(\theta\right)\right)}=\frac{r^{}\cos^3\left(\theta\right)\cdot\sin\left(r\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)}{\left(1\right)}\\=r\cdot\cos^3\left(\theta\right)\cdot\sin\left(r\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)\end{array},$

ahora pasamos al límite:

$\begin{array}{l}\lim_{r\rightarrow0}r\cdot\cos^3\left(\theta\right)\cdot\sin\left(r\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)=\left\{0\cdot\cos^3\left(\theta\right)\right\}\cdot\left\{\sin\left(0\cdot\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)\right\}\\=\left\{0\right\}\cdot\left\{\sin\left(0\right)\right\}=0\end{array},$

debido a que $\cos\left(\theta\right),\;\sin\left(\theta\right)$ tienen sus valores acotados en el intervalo $[-1,1]$ y al multiplicar por un valor $r\rightarrow0$ el resultado también tiende a cero. En conclusión, $\lim_{\left(x,y\right)\rightarrow\left(0,0\right)}f\left(x,y\right)=0.$ Como el valor exacto de $f\left(0,0\right)$ es también cero (según la definición de la función dada en el enunciado), vemos que coinciden $f\left(0,0\right)=\lim_{\left(x,y\right)\rightarrow\left(0,0\right)}f\left(x,y\right),$ y por tanto $f(x,y)$ es continua en el origen.

Derivabilidad en el origen

Para estudiar la existencia de derivadas direccionales en un punto $(x,y)$ según cualquier dirección $(u,v)$ se puede aplicar directamente la definición 1 para el origen de coordenadas:

$\frac{\partial f\left(0,0\right)}{\partial\overset\rightharpoonup u}=\lim_{h\rightarrow0}\frac{f\left(\left(0,0\right)+h\overset\rightharpoonup u\right)-f\left(0,0\right)}h=\lim_{h\rightarrow0}\frac{f\left(h\overset\rightharpoonup u\right)-0}h,$

sustituyendo en la expresión de la función:

$\lim_{h\rightarrow0}\frac{\left(\frac{h^3u_x^3\sin\left(hu_x+hu_y\right)}{h^2u_x^2+h^2u_y^2}\right)}h=\lim_{h\rightarrow0}\frac{h{\displaystyle\frac{u_x^3\sin\left(hu_x+hu_y\right)}{u_x^2+u_y^2}}}h$

simplificando y recordando que el vector de dirección $u$ es unitario, nunca puede tomar valores nulos:

$\lim_{h\rightarrow0}\frac{u_x^3\sin\left(h\left(u_x+u_y\right)\right)}{u_x^2+u_y^2}\rightarrow\frac{u_x^3\sin\left(0\right)}{u_x^2+u_y^2}=0$. [1]

Así pues la función es derivable en el origen, y su derivada direccional en el origen, para cualquier dirección, es cero.  La gràfica en 3D obtenida con [WolframAlpha](http://www.wolframalpha.com/) es:

[![3DPlot_Exer2_derivadas_n_var](/taller-matematicas/assets/images/3DPlot_Exer2_derivadas_n_var.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/09/3DPlot_Exer2_derivadas_n_var.png)

Ya que estamos, estudiemos también la diferenciabilidad de esta función; una condición suficiente es:

Criterio de diferenciabilidad: Si la función de dos variables $f(x,y)$ tiene derivadas parciales y al menos una de ellas es continua, entonces la función es diferenciable.

Calculemos la derivada parcial respecto x:

$D_xf\left(x,y\right)=\frac{3x^2\sin\left(x+y\right)\cdot\cos\left(x+y\right)\cdot\left(x^2+y^2\right)-x^3\sin\left(x+y\right)\cdot2x}{\left(x^2+y^2\right)^2}.$

Es una función continua salvo, quizás, en el origen $x=y=0,$ donde tenemos que usar la definición de derivada parcial, pero de hecho no es necesario calcularla, pues antes ya habíamos obtenido la derivada direccional en el orígen (ecuación [1]), que vale cero para cualquier dirección, y la derivada parcial según x resulta de tomar el vector $u=(1,0)$.

Para ver si $D_xf(x,y)$ es continua en el origen tenemos que ver que $\lim_{\left(x,y\right)\rightarrow\left(0,0\right)}D_xf\left(x,y\right)=D_xf\left(0,0\right)=0.$ Simplificamos:

$D_xf\left(x,y\right)=x^2\frac{3\cdot\cos\left(x+y\right)\cdot\left(x^2+y^2\right)-2x^2}{\left(x^2+y^2\right)^2}\sin\left(x+y\right)$

pasamos a coordenadas polares:

$\begin{array}{l}D_xf\left(r,\theta\right)=r^2\cos^2\left(\theta\right)\frac{3\cos\left(r\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)\cdot r^2-2r^2\cos^2\left(\theta\right)}{r^4}\sin\left(r\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)\\=\cos^2\left(\theta\right)\cdot\left$3\cos\left(r\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)-2\cos^2\left(\theta\right)\right$\cdot\sin\left(r\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)\end{array}$

Pasamos al límite $\lim_{r\rightarrow0}$ para obtener:

$\begin{array}{l}\lim_{r\rightarrow0}\cos^2\left(\theta\right)\cdot\left$3\cos\left(r\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)-2\cos^2\left(\theta\right)\right$\cdot\sin\left(r\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)\\=\cos^2\left(\theta\right)\left$3\cos\left(0\right)-2\cos^2\left(\theta\right)\right$\cdot\sin\left(0\right)\\=\cos^2\left(\theta\right)\left$3-2\cos^2\left(\theta\right)\right$\cdot0=0\end{array}$

que no depende del ángulo $\theta$, luego el límite existe y vale cero, y la función derivada parcial respecto a x es continua. Por el criterio de diferenciabilidad, la función es diferenciable.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
{% endraw %}