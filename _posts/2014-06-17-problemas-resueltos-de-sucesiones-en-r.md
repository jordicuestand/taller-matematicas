---
layout: post
title: "Problemas resueltos de sucesiones en R"
date: 2014-06-17 11:24:26 +0000
categories:
  - "Matemáticas"
  - "Sucesiones"
tags:
  - "límite indeterminado"
  - "punto de acumulación"
  - "serie de Leibniz"
  - "sucesión convergente"
  - "sucesión de Cauchy"
  - "sucesión acotada"
  - "sucesión monótona"
math: true
---
{% raw %}

[Cálculo en R](http://mathseng.blogspot.com.es/p/blog-page.html) -> [Sucesiones](http://mathseng.blogspot.com.es/2014/06/sucesiones-en-r.html) -> problemas resueltos

---

**1.** Calcular los siguientes límites.

**a)** $L = lim_n\frac{3n^2+2}{5n-1}$

Aplicando la regla de los límites de fracciones polinómicas, L = +∞, pues el numerador tiene mayor grado que el denominador.
**b)** $L=lim_n\frac{2n^3-5n-2}{-n^3-n^2+2n1+1}$

Siendo los grados de numerador y denominador iguales, el límite es el cociente de los factores de mayor grado,  $L =\frac{2}{-1} = -2$

**c) **$L=lim_n\frac{2n^2-5n-2}{-n^3-n^2+2n1+1}$

$L = 0$, pues el numerador tiene menor grado que el denominador.

**d)** $L=lim_n\frac{\sqrt{n^{2\;}+3}\;-\;\sqrt[{}]{n^2+5}}{\sqrt{n^{2\;}+3}\;+\;\sqrt[{}]{n^2+5}}$

Tenemos $L=lim_n\frac{\infty\;-\;\infty}{\infty\;+\;\infty}=\frac?\infty$, el límite del numerador es uno de los casos de indeterminación. Observamos que el "grado" del numerador y del denominador es $\sqrt{n^{2\;}}=n$. Por ello, para eliminar la indeterminación probemos a dividir por n:

$L=lim_n\frac{\left(\sqrt{n^{2\;}+3}\;-\;\sqrt[{}]{n^2+5}\right)/n}{\left(\sqrt{n^{2\;}+3}\;+\;\sqrt[{}]{n^2+5}\right)/n\;}=\frac{\sqrt{1+3/n^2}\;-\;\sqrt[{}]{1+5/n^2}}{\sqrt{1+3/n^2}\;+\;\sqrt[{}]{1+5/n^2}}$

Cuando n → ∞ resulta $L = L=\frac{\sqrt{1+0}-\sqrt{1+0}}{\sqrt{1+0}+\sqrt{1+0}}=\frac{1-1}{1+1}=0$

**e) **$L=\lim_n\left(\sqrt{n^2+1}-\sqrt n\right)$

El límite es indeterminado del tipo +∞ -∞. Para deshacer la indeterminación, convertimos el término general en una expresión racional, multiplicando y dividiendo por el conjugado:

$L=\lim_n\left(\sqrt{n^2+1}-\sqrt n\right)\frac{\sqrt{n^2+1}+\sqrt n}{\sqrt{n^2+1}+\sqrt n}$

$L=\lim_n\frac{\left(n^2+1\right)-\left(n\right)}{\sqrt{n^2+1}+\sqrt n}$

De esta forma aprovechamos el hecho de que $\left(a+b\right)\left(a-b\right)=a^2-b^2$ para eliminar los radicandos del numerador. Pero el límite sigue siendo indeterminado:

$L=\lim_n\frac{\left(n^2+1\right)-\left(n\right)}{\sqrt{n^2+1}+\sqrt n}=\frac{\infty-\infty}{\infty+\infty}=\frac?\infty$

Para deshacer la indeterminación dividimos todo per n elevado al mayor grado de los términos: n²

$L=\lim_n\frac{\left(n^2+1-n\right)/n^2}{\left(\sqrt{n^2+1}+\sqrt n\right)/n^2}=\lim_n\frac{1+1/n^2-1/n}{\sqrt{1/n^{2\;}+1/n^4}+\sqrt{1/n^3}}=\frac{1+0-0}{0+0+0}=\frac10$

Recordando las propiedades de los límites infinitos, concluimos L = +∞

---

**2**. Calcular $L=\lim_n\frac{n!}{n^n}$

$L=\lim_n\frac{n!}{n^n}=\lim_n\frac{n\cdot\left(n-1\right)\cdot\left(n-2\right)\cdot\dots\cdot2\cdot1}{n\cdot n\cdot n\dots n\cdot n}=\frac\infty\infty=?$

Observemos que $\frac{n!}{n^n}&gt;0$ para todo n, y que $\left(x_n\right)=\left\lbrace1,\frac12,\frac6{27},\dots \right\rbrace$ es decreciente y acotada, por lo que ha de ser convergente (no demostraremos estas afirmaciones, y que no nos lo piden explícitamente en el enunciado).

Si comparamos $\left(x_n\right)$ con la sucesión $\left(y_n\right)$ de términos $\left(y_n\right)=\left(\frac{n^{n-1}}{n^n}\right)=\frac{n\cdot n\dots n\cdot1}{n\cdot n\dots n\cdot n}=\frac1n$  vemos que se cumple, para todo n:

$0\leq\frac{n\cdot\left(n-1\right)\cdot\left(n-2\right)\cdot\dots\cdot2\cdot1}{n\cdot n\cdot n\dots n\cdot n}\leq\frac{n\cdot n\dots n\cdot1}{n\cdot n\dots n\cdot n}=\frac1n\Rightarrow0\leq\left(x_n\right)\leq\left(y_n\right)$

Pero \((y_n)\to 0\), con lo que tenemos que $0\leq\underset{}{\lim\left(x_n\right)\leq0\Rightarrow\lim\left(x_n\right)=0.}$

---

**3**. Mediante la definición de límite basada en puntos de acumulación, comprobar que la sucesión $\left(a_n\right)=\left(\frac{n-3}{2n}\right)$  es convergente.

El teŕmino general es del tipo fracción racional polinómica, aplicando el criterio de convergéncia adecuado concluimos inmediatamente que $\lim_{}\left(a_n\right)=\frac12$.

Para demostrar que es convergente con límite $\frac12$ hemos de ver que $x=\frac12$ es un punto de acumulación del conjunto $\left\lbrace-1,\frac-14,0,\frac18,\dots \right\rbrace$, que equivale a decir que siempre podemos encontrar elementos de la sucesión $x_n$ a medida que nos acercamos a distancias progresivamente menores r del punto x = 1/2:

![recta](/taller-matematicas/assets/images/recta.png) xn está situado a una distancia menor que r del  punto  x=1/2

 

Planteamos pues $x_n &gt; 1/2 - r$ (ver figura), o sea:

$\frac{n-3}{2n}&gt;\frac12-r\Leftrightarrow n-1&gt;n-2rn\Leftrightarrow-1&gt;2rn\Leftrightarrow1&lt;2rn\Leftrightarrow n&gt;\frac1{2r}$

Para todo $n&gt;\frac1{2r}$ los valores $x_n$ quedan más cerca de x=1/2 que el valor r, sea cual sea r, por lo que x=1/2 es punto de acumulación, y también el límite de la sucesión.

---

 

**4**. Mediante la definición clásica de límite basada en entornos, probar que la sucesión definida por $a_n=1$ si n es impar, $\frac1n$ en otro caso, no es convergente.

Los primeros términos de la sucesión son $\left\lbrace1,\frac12,1,\frac14,1,\frac16,\dots \right\rbrace$. Vemos que la sucesión no es monótona. Procedemos por reducción al absurdo: supongamos que el límite es $x$.
Entonces, para todo $r&gt;0$ existirá un $m\in\mathbb{N}$ tal que $x_n\in\beta\left(x,r\right)$ siempre que $n\geq m$,  equivalentemente, tendremos $x_n\in\left(x-r,x+r\right)$, que implica $x-r\leq x_n\leq x+r$. 
Entonces tendremos, simultaneamente,

\[
\begin{cases}
x-r \leq \dfrac{1}{n} \leq x+r, & n \text{ par},\\[6pt]
x-r \leq 1 \leq x+r, & n \text{ impar}.
\end{cases}
\]

De la segunda desigualdad, sumando $-x-1$ obtenemos $-1-r&lt;-x&lt;r-1\Leftrightarrow1+r&gt;x&gt;1-r$, que ha de ser cierto para cualquier $r&gt;0$, lo cual nos lleva a concluir que $x=1$. Sustituimos este valor de $x$ en la primera desigualdad para obtener $1-r&lt;\frac1n&lt;1+r$. pero para $n$ suficientemente grande, tenemos que $\frac1n$ tiende a $0$, entonces para valores de $r$ pequeños la desigualdad es imposible. En conclusión no existe el límite de la sucesión.

---

 

 

**5**. Mediante las propiedades de las sucesiones de Cauchy, probar que la sucesión definida por $a_n=1$ si n es impar, $\frac1n$ en otro caso, no es convergente.

En las sucesiones de Cauchy, la distancia entre los términos posteriores a uno dado puede hacerse tan pequeña como se quiera, esto es, para cualquier valor $r&gt;0$, existirá un $m\in\mathbb{N}$ tal que para cualquiera valores $n, p&gt;m$ se cumplirá $\left|x_n-x_p\right|&lt;r$. ¿Es esto cierto para la sucesión del enunciado?

Supongamos que $n&gt;m$ es par y que $p&gt;m$ es impar; podemos suponerlo por que la propiedad anterior que define la sucesión de Cauchy ha de cumplirse para cualesquiera términos posteriores a uno dado. 
Entonces \(\left|x_n-x_p\right|=\left|\frac{1}{n}-1\right|=1-\frac{1}{n}\), pero este valor aumenta con \(n\), acercándose a \(1\) cuando \(n\) es muy grande; por tanto, no podemos hacerlo menor que un \(r\) dado para valores grandes de \(n\).. En conclusión, la sucesión no es de Cauchy, y tampoco puede ser convergente.

---

 

**6.** Clasificar (¿acotada? ¿creciente? ¿decreciente? ¿monótona? ¿convergente?) la sucesión de término general:

\[
(a_n)=
\begin{cases}
\dfrac{n+1}{n} \xrightarrow[n\to\infty]{} 1,\\[6pt]
1-\dfrac{1}{2n} \xrightarrow[n\to\infty]{} 1-0=1.
\end{cases}
\]

Escribamos los primeros términos de la sucesión:

$\left(a_n\right)=\left\lbrace\frac12,\frac32,\frac56,\frac54,\frac9{10},\frac76,\frac{13}{14},\frac98,\dots \right\rbrace$

Vemos que a medida que avanzamos no hay un orden estricto, a veces aumentan los valores, a veces decrecen: no es una sucesión ni creciente ni decreciente, y por tanto tampoco es monótona. Para ver si es convergente consideremos cómo se comporta la diferencia entre dos términos cualesquiera $\left(a_p\right),\left(a_q\right),\;p,q&gt;m\in\mathbb{N}$ cuando avanzamos en la sucesión; como tenemos dos términos generales, dependiendo de si $p, q$ son pares o impares, tendremos que distinguir cada caso por separado. Suponemos que $q&gt;p$.

Tanto $p$ como $q$ son pares:

$\frac{q+1}q-\frac{p+1}p=\left(1+\frac1q\right)-\left(1+\frac1p\right)=\frac1q-\frac1p\xrightarrow[\infty]{}\frac1\infty-\frac1\infty=0.$.

Tanto $p$ como $q$ son impares:

$\left(1-\frac1{2q}\right)-\left(1-\frac1{2p}\right)=\frac1{2p}-\frac1{2q}\xrightarrow[\infty]{}\frac1\infty-\frac1\infty=0.$

$p$ es par, $q$ es impar:

$\left(1-\frac1{2q}\right)-\left(1+\frac1p\right)=\frac1p-\frac1{2q}\xrightarrow[\infty]{}\frac1\infty-\frac1\infty=0.$

El caso restante $p$ es impar, $q$ es par es análogo y lo dejamos para el lector. Vemos que en todos los casos la diferencia entre términos sucesivos cualesquiera se hace más y más pequeña conforme avanzamos en la sucesión, por tanto podremos hacer que sea menor que cualquier $r&gt;0$ dado siempre que $p, q &gt; m$ para cierto $m$ que dependerá de $r$, en otras palabras, la sucesión es de Cauchy, y por tanto convergente.

Si queremos calcular el límite, que ahora sabemos que existe, lo hacemos para ambas expresiones:

$\left(a_n\right)=\left\lbrace\begin{array}{l}\frac{n+1}n\xrightarrow[\infty]{}1\\1-\frac1{2n}\xrightarrow[\infty]{}1-0=1\end{array}\right.$

Vemos que en cualquier caso la sucesión se acerca progresivamente a 1, que es el límite de la sucesión.

---

**7.** Clasificar la sucesión de números racionales $\left(a_n\right)=1-\frac13+\frac15-\dots+\left(-1\right)^{n+1}\frac1{2n-1}=\sum_{i=1}^n\left(-1\right)^{i+1}\frac1{2i-1}$  teniendo en cuenta que sólo contiene números racionales, esto es, $\left(a_n\right)\in\mathbb{Q}$

Escribamos los primeros términos de la sucesión:

 	- n=1) 1

 	- n=2) 1 - 1/3 = 2/3

 	- n=3) 1 - 1/3 + 1/5 = 2/3 + 1/5 = 13/15

 	- n=4) 1 - 1/3 + 1/5 - 1/7 = 76/105

Vemos que  a veces aumentan los valores, a veces decrecen: no es una sucesión ni creciente ni decreciente, y por tanto tampoco es monótona. Para ver si es una sucesión de Cauchy calculamos la diferencia entre dos términos cualesquiera:

$\left(a_p\right)-\left(a_q\right)=\left(1-\frac13+\frac15-\dots+\left(-1\right)^{p+1}\frac1{2p-1}\right)-\left(1-\frac13+\frac15-\dots+\left(-1\right)^{q+1}\frac1{2q-1}\right)$

$\left(a_p\right)-\left(a_q\right)=\left(-1\right)^{p+1}\frac1{2p-1}-\left(-1\right)^{q+1}\frac1{2q-1}$

Como solo nos interesa el valor absoluto de la diferencia, ignoramos los signos:

\[
\left|a_p-a_q\right|
=
\left|\frac{1}{2p-1}-\frac{1}{2q-1}\right|
\xrightarrow[p,q\to\infty]{}
\left|\frac{1}{\infty}-\frac{1}{\infty}\right|
=0.
\]

Por tanto la sucesión es de Cauchy, no obstante, ahora no implica que sea convergente, pues la implicación Cauchy $\Rightarrow$ convergente sólo es válida para sucesiones de números reales, y esta sucesión es de números racionales. De hecho, esta sucesión se conoce como [serie de Leibniz](http://es.wikipedia.org/wiki/Serie_de_Leibniz) y se puede probar que converge a $\mathrm\pi/4$, que es un número irracional, por lo tanto la sucesión no converge a ningún número racional: es divergente.

![separador2](/taller-matematicas/assets/images/separador2.png)
# Bibliografia

 

Sucesiones y series infinitas (Curso programado de Cálculo C.E.M.). Un libro antiguo e injustamente olvidado, en mi opinión. El Curso programado sigue la didáctica [constructivista](https://es.wikipedia.org/wiki/Constructivismo_%28pedagog%C3%ADa%29), introduciendo cada concepto con ejemplos, de forma que el alumno va construyendo su conocimiento en vez de simplemente memorizarlo.
{% endraw %}