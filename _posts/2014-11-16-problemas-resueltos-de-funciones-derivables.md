---
layout: post
title: "Problemas resueltos de funciones derivables"
date: 2014-11-16 11:58:10 +0000
categories:
  - "Derivación"
  - "Funciones reales de variable real"
  - "Matemáticas"
tags:
  - "derivabilidad"
  - "derivadas"
  - "recta tangente"
  - "regla de la cadena"
math: true
---
{% raw %}

**1.** Derivar $y=\sqrt{\sqrt{\sqrt x.}}$
La forma más simple de derivar esta función será, primero simplificar su expresión: utilizamos la notación de raíz en forma de potencia: $y=\sqrt{\sqrt{\sqrt x}}=\left(\left(x^\frac12\right)^\frac12\right)^\frac12=x^{\frac12\cdot\frac12\cdot\frac12}=x^\frac18$. Ahora usamos la derivada del monomio $(Ax^n)'=Anx^{n-1}$, que en este caso será $y'=\frac18x^{\frac18-1}=\frac18x^\frac78=\frac18\sqrt[8]{x^7}.$

Otra forma, más larga pero buena para practicar con la regla de la cadena, es: primero expresamos la función como una composición:

$y=\sqrt{\sqrt{\sqrt x}}=\sqrt x\circ\sqrt x\circ\sqrt x=f(x)\circ g(x)\circ h(x)$,

y a continuación derivamos por la regla de la cadena, de izquierda a derecha:

$\begin{array}{l}D\left(\sqrt x\circ\sqrt x\circ\sqrt x\right)=D\left(\sqrt x\right)\circ\sqrt x\circ\sqrt x\cdot D\left(\sqrt x\right)\circ\sqrt x\cdot D\left(\sqrt x\right)=\\\frac1{2\sqrt x}\circ\sqrt x\circ\sqrt x\cdot\frac1{2\sqrt x}\circ\sqrt x\cdot\frac1{2\sqrt x}=\\\frac1{2\sqrt{\sqrt{\sqrt x}}}\cdot\frac1{2\sqrt{\sqrt x}}\cdot\frac1{2\sqrt x}\end{array}$

Para simplificar esta expresión, usamos exponentes:

$\begin{array}{l}\frac1{2\sqrt{\sqrt{\sqrt x}}}\cdot\frac1{2\sqrt{\sqrt x}}\cdot\frac1{2\sqrt x}=\frac12x^{-\frac12\frac12\frac12}\cdot\frac12x^{-\frac12\frac12}\frac12x^{-\frac12}=\\\frac18x^{-\frac18-\frac14-\frac12}=\frac18x^{-\frac18-\frac28-\frac48}=\frac18x^{-\frac78}=\frac1{8\sqrt[8]{x^7}}.\end{array}$

![separador2](/taller-matematicas/assets/images/separador2.png)

**2.** Derivar $f(x)=\sqrt{\ln\left(x\right)}$.

Expresemos la función como composición: $f(x)=\sqrt{\ln\left(x\right)}=\sqrt x\circ\ln\left(x\right)$. Aplicamos la regla de la cadena:

$\begin{array}{l}f'(x)=\left(\sqrt x\circ\ln\left(x\right)\right)'=\left(\sqrt x\right)'\circ\ln\left(x\right)\cdot\left(\ln\left(x\right)\right)'=\\\frac1{2\sqrt x}\circ\ln\left(x\right)\cdot\frac1x=\frac1{2\sqrt{\ln\left(x\right)}}\cdot\frac1x=\frac1{2x\sqrt{\ln\left(x\right)}}.\end{array}$

![separador2](/taller-matematicas/assets/images/separador2.png)

**3.** Derivar $f(x)=e^{x^2+\sin\left(x^3+1\right)}$.

Expresemos la función como composición: $f(x)=e^{x^2+\sin\left(x^3+1\right)}=e^x\circ\left(x^2+\sin\left(x^3+1\right)\right)$. Aplicamos la regla de la cadena:

$\begin{array}{l}f'(x)=e^x\circ\left(x^2+\sin\left(x^3+1\right)\right)=\left(e^x\right)'\circ\left(x^2+\sin\left(x^3+1\right)\right)\cdot\left(x^2+\sin\left(x^3+1\right)\right)'=\\e^x\circ\left(x^2+\sin\left(x^3+1\right)\right)\cdot\left(2x+\left(\sin\left(x^3+1\right)\right)'\right);\end{array}$

Aplicamos de nuevo la regla de la cadena para derivar la función seno:

$\begin{array}{l}\left(\sin\left(x^3+1\right)\right)=\sin\left(x\right)\circ\left(x^3+1\right);\\\left(\sin\left(x^3+1\right)\right)'=\left(\sin\left(x\right)\right)'\circ\left(x^3+1\right)\cdot\left(x^3+1\right)'=\cos\left(x\right)\circ\left(x^3+1\right)\cdot\left(3x^2\right)=\\3x^2\cos\left(x^3+1\right).\end{array}$

Sustituimos en la expresión de $f'(x)$ para obtener:

$\begin{array}{l}y'=e^x\circ\left(x^2+\sin\left(x^3+1\right)\right)\cdot\left(2x+3x^2\cos\left(x^3+1\right)\right)=\\\left(2x+3x^2\cos\left(x^3+1\right)\right)\cdot e^{\left(x^2+\sin\left(x^3+1\right)\right)}.\end{array}.$

![separador2](/taller-matematicas/assets/images/separador2.png)

**4. **Derivar $y=\tan^{-1}\left(\sin\left(x\right)\right).$

Expresemos la función como composición: $y=\tan^{-1}\left(\sin\left(x\right)\right)=\tan^{-1}\left(x\right)\circ\left(\sin\left(x\right)\right);$ aplicamos la regla de la cadena:

$\begin{array}{l}y'=\left(\tan^{-1}\left(x\right)\right)'\circ\left(\sin\left(x\right)\right)\cdot\left(\sin\left(x\right)\right)'=\\\frac1{1+x^2}\circ\left(\sin\left(x\right)\right)\cdot\cos\left(x\right)=\frac{\cos\left(x\right)}{1+\sin^2\left(x\right)}.\end{array}$

![separador2](/taller-matematicas/assets/images/separador2.png)

**5.** Hallar la recta tangente a la gráfica de la función $f(x)=\sqrt{1+x^2}$ en los puntos $x=0$, $x=1$.
La recta $y=mx+b$ es tangente a la gráfica de la función $f(x)$ en el punto $(x_0,f(x_0))$ si la pendiente $m$ cumple que $m=f'(x_0)$ y ademaś la recta pasa por el punto $(x_0,f(x_0))$. Para la primera condición hemos de calcular $f'(x)$:

$\begin{array}{l}f'(x)=\left(\sqrt{1+x^2}\right)'=\left(\sqrt x\circ\left(1+x^2\right)\right)'=\left(\sqrt x\right)'\circ\left(1+x^2\right)\cdot\left(1+x^2\right)'=\\\frac{2x}{2\sqrt{1+x^2}}\end{array}$

En el punto $x_0=0$ la derivada vale $f'(0)=0=m$. La segunda condición es que la recta $y=mx+b=0·x+b=b$ pase por el punto $(0,f(0)=(0,1)$, o sea que $y=b=1$. La recta tangente para $x_0=0$ es $y=1$.

En el punto $x_1=0$ la derivada vale $f'(1)=\frac1{\sqrt2}=m$. La segunda condición es que la recta $y=mx+b=\frac1{\sqrt2}·x+b=b$ pase por el punto $(1,f(1)=(1,\sqrt2)$, o sea que $\sqrt2=\frac1{\sqrt2}\cdot1+b\Rightarrow b=\sqrt2-\frac1{\sqrt2}=\frac2{\sqrt2}-\frac1{\sqrt2}=\frac1{\sqrt2}.$. La recta tangente para $x_0=1$ es $y=1$.

![recta_tangent_4](/taller-matematicas/assets/images/recta_tangent_4.png)

 ![separador2](/taller-matematicas/assets/images/separador2.png)

**6.** Calcular la derivada en todos los puntos donde exista de la función dada por:

$f(x)=\left\{\begin{array}{l}\frac12x-\frac12\;\text{si }x\leq1\\-\sqrt{\left|x\right|}\;\text{si }-1&lt;x\leq0\\\sqrt x\;\text{si }0&lt;x\leq1\\\frac12x+\frac12\;\text{si }x&gt;1\end{array}\right.$
Primero estudiamos la derivabilidad de cada rama de la función; en una segunda fase estudiaremos la derivabilidad en los puntos de bifurcación entre las ramas.

Derivabilidad de cada rama de la función.

$f(x)=\frac12x-\frac12$ es derivable en todo el dominio, y su derivada vale $f'(x)=\frac12$.

$f(x)=-\sqrt{\left|x\right|}=\left(-\sqrt x\right)\circ\left|x\right|$ es una composición de funciones, la primera es derivable en todo $x\geq0$ y la segunda es derivable en todo $\mathbb{R}$ excepto en $x=0$: para verlo  hacemos las derivadas laterales en ese punto:

$\begin{array}{l}\lim_{h\rightarrow0}\frac{f(0^++h)-f(0^+)}h=\frac{\left|0^++h\right|-\left|0^+\right|}h=\frac{0^++h-0^+}h=\frac hh=1;\\\lim_{h\rightarrow0}\frac{f(0^-+h)-f(0^-)}h=\frac{\left|0^-+h\right|-\left|0^-\right|}h=\frac{-\left(0^-+h\right)-(-0^-)}h=\frac{-h}h=-1\end{array}$

Los límites no coincicen, luego no existe la derivada de la función $\left|x\right|$ en $x=0$. Entonces tenemos que la composición $\left(-\sqrt x\right)\circ\left|x\right|:\mathbb{R}_0^+\rightarrow\mathbb{R}_0^-$ es derivable en el dominio de definición de esta rama de la función, excepto en el punto $x=0$. Recordatorio: $\mathbb{R}_0^+$ significa todos los reales positivos incluido el 0.

La derivada vale:

$\left(-\sqrt{\left|x\right|}\right)'=\left(-\sqrt x\circ\left|x\right|\right)'=\left(-\sqrt x\right)'\circ\left|x\right|\cdot\left|x\right|'=\frac{-1}{2\sqrt x}\circ\left|x\right|\cdot\left|x\right|'$

En el intervalo $-1&lt;x&lt;0$ tenemos que $\left|x\right|=-x$, luego:

$\frac{-1}{2\sqrt x}\circ\left|x\right|\cdot\left|x\right|'=\frac{-1}{2\sqrt{\left|x\right|}}\cdot(-1)=\frac1{2\sqrt{\left|x\right|}}$

El punto $x=0$ lo estudiamos en la segunda parte del problema. Para la siguiente rama de la función tenemos $f(x)=\sqrt x$ que es derivable en su dominio, con derivada $\left(\sqrt x\right)'=\frac1{2\sqrt x}$. Para la última rama, $f(x)\frac12x-\frac12$, la derivada vale $\left(\frac12x-\frac12\right)'=\frac12.$

Estudiamos ahora los puntos de salto entre ramas.

En estos puntos la definición de la función cambia bruscamente, y no podemos usar las tablas de derivadas, tenemos que usar la definición de derivada, y además haciendo los límites laterales, sólo si coinciden ambos podemos asegurar que existe la derivada en el punto.

**$x=-1$**

Por la izquierda: $\begin{array}{l}\lim_{h\rightarrow0}\frac{f(x^-+h)-f(x^-)}h=\lim_{h\rightarrow0}\frac{\left({\displaystyle\frac12}\left(x^-+h\right)-{\displaystyle\frac12}\right)-\left({\displaystyle\frac12}x^--{\displaystyle\frac12}\right)}h=\\\lim_{h\rightarrow0}\frac{\displaystyle\frac12}h=\frac12\end{array}$

Por la derecha: $\begin{array}{l}\lim_{h\rightarrow0}\frac{f(x^++h)-f(x^+)}h=\lim_{h\rightarrow0}\frac{\left(-\sqrt{\left|x^++h\right|}\right)-\left(-\sqrt{\left|x^+\right|}\right)}h=\\\lim_{h\rightarrow0}\frac{\left(-\sqrt{\left|-1^++h\right|}\right)-\left(-\sqrt{\left|-1^+\right|}\right)}h=\lim_{h\rightarrow0}\frac{\left(-\sqrt{1^--h}\right)+1^+}h=\frac{-1+1}0=?\end{array}$

Observemos que hemos hecho $\sqrt{\left|-1^++h\right|}=\left(-\sqrt{1^--h}\right)$ pues el valor absoluto de un número negativo se obtiene cambiándole el signo, y al hacerlo, si el valor negativo estaba a la derecha de 1, al canviar el signo pasará a estar a la izquierda.

Para resolver la indeterminación, és útil trabajar con la definición alternativa de derivada en el punto $x=x_0$, que es:

$x=x_0+h\Rightarrow f'(x_0)=\lim_{h\rightarrow0}\frac{f\left(x_0+h\right)-f\left(x_0\right)}h=\lim_{x\rightarrow x_0}\frac{f\left(x\right)-f\left(x_0\right)}{x-x_0}$

Reintentamos el límite por la derecha:

$f'(-1^+)=\lim_{x\rightarrow-1^+}\frac{f\left(x\right)-f\left(-1^+\right)}{x-\left(-1^+\right)}=\lim_{x\rightarrow-1^+}\frac{-\sqrt{\left|x\right|}-\left(-1^-\right)}{x+1^-}=\frac{-1+1}{-1+1}=\frac00$

Tenemos indeterminación de nuevo. Multiplicamos por el conjugado:

$\begin{array}{l}\lim_{x\rightarrow-1^+}\frac{-\sqrt{-x}+1}{x+1^-}\frac{\sqrt{-x}+1}{\sqrt{-x}+1}=\lim_{x\rightarrow-1^+}\frac{x+1}{\left(x+1^-\right)\left(\sqrt{-x}+1\right)}=\\\lim_{x\rightarrow-1^+}\frac1{\sqrt{-x}+1}=\frac12\end{array}$

Los dos límites laterales coinciden: la derivada en el punto -1 es $\frac12$

**$x=0$**

Límite por la izquierda:

$\begin{array}{l}f'(0^-)=\lim_{x\rightarrow0^-}\frac{f\left(x\right)-f\left(0^-\right)}{x-0^-}=\lim_{x\rightarrow0^-}\frac{-\sqrt{\left|x\right|}-\left(-\sqrt{\left|0^-\right|}\right)}{x-0^-}=\\\lim_{x\rightarrow0^-}\frac{-\sqrt{-x}}x=\lim_{x\rightarrow0^-}\frac{-\sqrt{-x}}x\frac{\sqrt{-x}}{\sqrt{-x}}=\lim_{x\rightarrow0^-}\frac x{x\sqrt{-x}}=\lim_{x\rightarrow0^-}\frac1{\sqrt{-x}}=+\infty\end{array}$

Como es divergente, no es necesario hacer el límite por la derecha: la función no es derivable en $x=0$.

**$x=1$**

Límite por la izquierda:

$\begin{array}{l}f'(1^-)=\lim_{x\rightarrow1^-}\frac{f\left(x\right)-f\left(1^-\right)}{x-1^-}=\lim_{x\rightarrow1^-}\frac{\sqrt x-\sqrt{1^-}}{x-1^-}=\lim_{x\rightarrow1^-}\frac{\sqrt x-\sqrt{1^-}}{x-1^-}\frac{\sqrt x+\sqrt{1^-}}{\sqrt x+\sqrt{1^-}}=\\\lim_{x\rightarrow1^-}\frac{x-1^-}{\left(x-1^-\right)\left(\sqrt x+\sqrt{1^-}\right)}=\lim_{x\rightarrow1^-}\frac1{\left(\sqrt x+\sqrt{1^-}\right)}=\frac12\\\end{array}$

Límite por la derecha:

$\begin{array}{l}f'(1^+)=\lim_{x\rightarrow1^+}\frac{f\left(x\right)-f\left(1^+\right)}{x-1^+}=\lim_{x\rightarrow1^+}\frac{\left({\displaystyle\frac12}x+{\displaystyle\frac12}\right)-1^+}{x-1^+}=\lim_{x\rightarrow1^+}\frac{\frac12x-\left(\frac12\right)^-}{x-1^+}=\\\lim_{x\rightarrow1^+}\frac12\frac{x-1^-}{x-1^+}=\frac12\end{array}$

Coinciden, y la función es derivable en $x=1$. Podemos dar la derivada de la función completa:

$f'(x)=\left\{\begin{array}{l}\frac12\;\text{si}x\leq1\\\frac1{2\sqrt{\left|x\right|}}\;\text{ si }-1&lt;x&lt;0\\\text{no existe para }x=0\\\frac1{2\sqrt x}\;\text{ si }0&lt;x\leq1\\\frac12\;\text{ si }x&gt;1\end{array}\right.$

Gráfica de la función $f(x)$, observemos que en $x=0$ la gràfica queda vertical, y por tanto la derivada toma valor infinito:

![Exercici_derivades](/taller-matematicas/assets/images/Exercici_derivades.png)

![separador2](/taller-matematicas/assets/images/separador2.png)

**7.** Verificar si la recta $y=-x$ es tangente a la gráfica de la función $f(x)=x^3-6x^2+8x$ en algún punto, o bien es secante, o bien es tangente en un punto y secante en otro punto.

La pendiente de la recta $y=-x$ es $m=-1$; si es una recta tangente a la gráfica de $f(x)$ entonces la derivada $f'(x)$ debe tomar el valor -1 en algún punto $x_0$. Derivamos e igualamos:

$f'(x)=3x^2-12x+8=-1\Rightarrow x=\frac{12\pm\sqrt{12^2-4\cdot3\cdot9}}6=\frac{12\pm6}6=\left\{\begin{array}{l}3\\1\end{array}\right.$

Para estos dos valores, sustituimos en la ecuación de la recta para obtener los puntos $(x,y)$ de la recta; si ésta fuera recta tangente, entonces alguno de esos puntos debería pertenecer también a la gráfica de $f(x)$:

$x_0=3\Rightarrow y=-3\;\text{en la recta; }y=3^3-6\cdot3^2+8\cdot3=-3\;\text{en la función;}$ coinciden, luego la recta es tangente a $f(x)$ en el punto.

$x_0=1\Rightarrow y=-1\;\text{en la recta; }y=1^3-6\cdot1^2+8\cdot1=3\;\text{en la función;}$ no coinciden, luego la recta no es tangente a $f(x)$ en el punto.

Para estudiar si la recta es secante a $f(x)$ planteamos el sistema de ecuaciones:

$\begin{array}{l}\left.\begin{array}{r}y=f(x)=x^3-6x^2+8x\\y=-x\end{array}\right\}\Rightarrow-x=x^3-6x^2+8x\Rightarrow x^2-6x+8=-1\Rightarrow\\x=\frac{-6\pm\sqrt{36-4\cdot(-1)\cdot(-9)}}{-2}=3\pm0=3.\end{array}$

Obtenemos de nuevo el punto $x=3$ que ya hemos obtenido como punto de contacto entre la recta tangente y la función. Pero además tenenemos otra solución a la ecuación:

$-x=x^3-6x^2+8x\Rightarrow x^3-6x^2+9x=0\Rightarrow x\left(x^2-6x+9\right)=0$

y es evidente que $x=0$ tambien es solución. Así pues, la recta dada es tangente a la función $f(x)$ en el punto $x=3$ y secante en el punto $x=0$. La gráfica de ámbas es:

![recta_tangent_5](/taller-matematicas/assets/images/recta_tangent_5.png)

![separador2](/taller-matematicas/assets/images/separador2.png)

**8.** Calcular la derivada de la función $y=x^{x^x}.$

Aplicamos logaritmos:

$Ln\left(y\right)=Ln\left(x^{x^x}\right)=Ln\left(x^{\left(x^x\right)}\right)=x^xLn\left(x\right)$

Observar que seria incorrecto
$Ln\left(x^{x^x}\right)=Ln\left(x^x\right)^x=xLn\left(x^x\right)$ pues $x^{x^x}\neq\left(x^x\right)^x$ sino que es $x^{x^x}=x^{\left(x^x\right)}.$ Ahora aplicamos la regla de la derivada del producto:

$D\left$Ln\left(y\right)\right$=D\left$x^xLn\left(x\right)\right$=D\left$x^x\right$\cdot Ln\left(x\right)+x^x\cdot D\left$Ln\left(x\right)\right$$

La derivada de $x^x$ la hacemos aparte, aplicando de nuevo logaritmos:

$\begin{array}{l}y=x^x\Leftrightarrow\ln\left(y\right)=\ln\left(x^x\right)=x\cdot\ln\left(x\right);\\D\left$\ln\left(y\right)\right$=D\left$x\cdot\ln\left(x\right)\right$=Dx\cdot\ln\left(x\right)+x\cdot D\left$\ln\left(x\right)\right$=1\cdot\ln\left(x\right)+x\cdot\frac1x=\ln\left(x\right)+1.\end{array}$

Como $D\left$Ln\left(y\right)\right$=\frac1yDy$ (por la regla de la cadena), tenemos que: $\frac{Dy}y=\ln\left(x\right)+1\Leftrightarrow Dy=y\left$\ln\left(x\right)+1\right$=x^x\left$\ln\left(x\right)+1\right$.$

 Ahora sustituimos en la derivada original:

$\begin{array}{l}\frac1yDy=x^x\left$\ln\left(x\right)+1\right$\cdot Ln\left(x\right)+x^x\cdot\frac1x\Leftrightarrow\\Dy=y\cdot x^x\left$Ln^2\left(x\right)+Ln\left(x\right)+\frac1x\right$=x^{x^x}\cdot x^x\left$Ln^2\left(x\right)+Ln\left(x\right)+\frac1x\right$.\end{array}$

![separador2](/taller-matematicas/assets/images/separador2.png)

**9.** La posición en el tiempo de un punto material que se está moviendo en el plano $(x,y)$ viene dada en función del tiempo por $x(t)= sin(t), y(t)=sin(2t)$. Si consideramos la trayectoria como una función $y=f(x)$, calcular la  derivada $y'(x)$.

La trayectoria viene dada en función del paràmetro tiempo en vez de venir en forma explícita $y=f(x)$; en ocasiones es más cómodo hacerlo así, pues la forma explícita puede ser difícil de expresar. La gráfica de la trayectoria es un lazo:

![parametriques](/taller-matematicas/assets/images/parametriques-300x180.png)
Para calcular la derivada $y'(x)$ usaremos la notación diferencial de la derivada:

$y'(x)=\frac{\operatorname{d}y}{\operatorname{d}x}=\frac{\operatorname{d}y}{\operatorname{d}t}\cdot\frac{\operatorname{d}t}{\operatorname{d}x}$

Observar cómo hemos utilizado las diferenciales para expresar la derivada con respecto a x en función de las derivadas respecto  a t.

$\begin{array}{l}\frac{\operatorname{d}y}{\operatorname{d}t}=D\sin\left(t\right)\circ2t=\cos\left(t\right)\circ2t\cdot D\left(2t\right)=2\cos\left(2t\right).\\\frac{\operatorname{d}t}{\operatorname{d}x}=\left(\frac{\operatorname{d}x}{\operatorname{d}t}\right)^{-1}=\left$D\sin\left(t\right)\right$^{-1}=\frac1{\cos\left(t\right)}.\end{array}$

Nos queda que $\begin{array}{l}\frac{\operatorname{d}y}{\operatorname{d}x}=2\cos\left(2t\right)\cdot\frac1{\cos\left(t\right)}=2\frac{\cos\left(2t\right)}{\cos\left(t\right)}.\\\end{array}$ La gráfica de la derivada presenta asíntotas verticales, correspondientes a los puntos del eje x donde el lazo tiene tangente vertical:

![derivada_parametriques1](/taller-matematicas/assets/images/derivada_parametriques1.png)
![separador2](/taller-matematicas/assets/images/separador2.png)

**10.** Dada la función

$f(x)=\left\{\begin{array}{l}e^{-\frac1{x^2}}\;\text{si }x\neq0\\0\;\text{si }x=0\end{array}\right.$

demostrar que es una función continua, que su derivada de cualquier orden $f^n$ también es contínua y que $f^n(0)=0$ para todo $n=1,2,...$.

Para ver si es continua, estudiamos su comportamiento cerca de el único punto dudoso, $x=0$, calculando el límite:

$\lim_{x\rightarrow0}f(x)=\lim_{x\rightarrow0}e^{-\frac1{x^2}}=\lim_{x\rightarrow0}\frac1{e^\frac1{x^2}}\rightarrow\frac1{e^{+\infty}}=0.$

Como el límite en $x=0$ coincide con $f(0)$ la función es contínua.

Para obtener la derivada, si $x\neq0$ derivamos su expresión:

$\begin{array}{l}D\left$e^{-\frac1{x^2}}\right$=D\left$e^x\circ\frac{-1}{x^2}\right$=D\left$e^x\right$\circ\frac{-1}{x^2}\cdot D\left$\frac{-1}{x^2}\right$=\\e^x\circ\frac{-1}{x^2}\cdot D\left$-x^{-2}\right$=e^{-\frac1{x^2}}\cdot\frac2{x^3}\end{array}$

Esta expresión es válida para $x\neq0$. Para $x=0$ usamos la definición de derivada:

$\lim_{x\rightarrow0\;}\frac{f(x)-f(0)}{x-0}=\lim_{x\rightarrow0\;}\frac{e^{-{\displaystyle\frac1{x^2}}}-0}x=\lim_{x\rightarrow0\;}\frac1{xe^{\displaystyle\frac1{x^2}}}\rightarrow\frac1{0\cdot e^\infty}\rightarrow\frac1\infty=0,$

debido a que $\lim_{x\rightarrow0\;}x\cdot e^\frac1x=0$ pues la función exponencial es de orden superior a cualquier potencia de x.

Así pues,

$f'(x)=\left\{\begin{array}{l}e^{-\frac1{x^2}}\cdot\frac2{x^3}\;\text{, x≠0}\\0\;\text{, x=0}\end{array}\right.$

Para la derivada segunda en $x=0$, haciendo el límite:

$f''(0)=\lim_{x\rightarrow0\;}\frac{f'(x)-f'(0)}{x-0}=\lim_{x\rightarrow0\;}\frac{{\displaystyle\frac2{x^3}}e^{-{\displaystyle\frac1{x^2}}}-0}x=\lim_{x\rightarrow0\;}\frac2{x^4e^{\displaystyle\frac1{x^2}}}\rightarrow\frac2{0\cdot e^\infty}\rightarrow\frac1\infty=0,$

 y en general para la derivada n-èsima tendremos

$f^n(0)=\lim_{x\rightarrow0}\frac2{x^ke^{\displaystyle\frac1{x^2}}}\rightarrow0.$
{% endraw %}