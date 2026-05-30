---
layout: post
title: "Problemas resueltos de series numéricas"
date: 2014-12-24 11:09:37 +0000
categories:
  - "Cálculo en R"
  - "Matemáticas"
  - "series"
tags:
  - "series numéricas"
math: true
---
{% raw %}

La teoría (con ejemplos) correspondiente la encontrareis aquí: [Series de números reales](http://tallermatematic.ovh/wp/index.php/2015/07/25/series-de-numeros-reales/).

**1.** Estudiar la convergéncia de la serie $\sum_{n=1}^\infty\frac{n^n}{n!}$
Al tener el término general $\frac{n^n}{n!}$ exponentes y factoriales, parece una buena idea probar con el criterio del cociente (también conocido por criterio d'Alembert), ya que suele simplificarse. Probemos:

$\begin{array}{l}\lim_{n\rightarrow\infty}\frac{a_{n+1}}{a_n}=\lim_{n\rightarrow\infty}\frac{\left(n+1\right)^{n+1}/\left(n+1\right)!}{n^n/n!}=\lim_{n\rightarrow\infty}\frac{\left(n+1\right)^{n+1}}{n^n}\frac{n!}{\left(n+1\right)!}=\\\lim_{n\rightarrow\infty}\frac{\left(n+1\right)^{n+1}}{n^n}\frac1{n+1}=\lim_{n\rightarrow\infty}\frac{\left(n+1\right)^n}{n^n}=\lim_{n\rightarrow\infty}\left(\frac{n+1}n\right)^n=\\\lim_{n\rightarrow\infty}\left(1+\frac1n\right)^n=e.\end{array}$

Segun el criterio del cociente, el límite debería ser como mucho 1 para que la serie fuera convergente, por tanto esta serie es divergente. De hecho, podeímos hacerlo usando el criterio más general de convergencia de una serie: es necesario (no suficiente) para la convergencia que el término $a_n$ tienda a cero, cosa que no sucede:

$\lim_{n\rightarrow\infty}\frac{n^n}{n!}=\lim_{n\rightarrow\infty}\frac{n\cdot n\cdot n\dots\cdot n}{n\cdot\left(n-1\right)\left(n-2\right)\dots2\cdot1}=\lim_{n\rightarrow\infty}1\cdot\frac n{n-1}\cdot\frac n{n-2}\dots\frac n2n$

en esta producto todos los términos iniciales son mayores o iguales a 1, y los últimos tienden a $\infty$, luego el producto también tiende a $\infty$ y la serie es divergente.

![separador2](/taller-matematicas/assets/images/separador2-150x50.png)

 

**2. **Estudiar la convergéncia de la serie** **$\sum_{n=1}^\infty\sin^n\left(\frac{n\mathrm\pi}{\mathrm{nπ}+2}\right)$

También aquí tenemos exponentes que pueden simplificarse usando el criterio del cociente, probemos:

$\begin{array}{l}\lim_{n\rightarrow\infty}\frac{\sin^{n+1}\left(\frac{\left(n+1\right)\mathrm\pi}{\left(n+1\right)\pi+2}\right)}{\sin^n\left(\frac{n\mathrm\pi}{\mathrm{nπ}+2}\right)}=\lim_{n\rightarrow\infty}\left$\frac{\sin\left(\frac{\left(n+1\right)\mathrm\pi}{\left(n+1\right)\pi+2}\right)}{\sin\left(\frac{n\mathrm\pi}{\mathrm{nπ}+2}\right)}\right$^n\sin\left(\frac{\left(n+1\right)\mathrm\pi}{\left(n+1\right)\pi+2}\right)=\\\left$\frac{\sin\left(1\right)}{\sin\left(1\right)}\right$^n\sin\left(1\right)=1^\infty\cdot\sin\left(1\right)=?\end{array}$

Obtenemos una indeterminación del tipo $e$, que en este caso no es inmediato por la presencia de la función seno. Probemos con el criterio de la raíz:
$\lim_{n\rightarrow\infty}\sqrt[n]{\left|\sin^n\left(\frac{n\mathrm\pi}{\mathrm{nπ}+2}\right)\right|}=\lim_{n\rightarrow\infty}\left|\sin\left(\frac{n\mathrm\pi}{\mathrm{nπ}+2}\right)\right|=\left|\sin\left(1\right)\right|&lt;1$

La serie es convergente. La suma, obtenida con hoja de cálculo, es 3.541 con un error de $10^-4$.

![separador2](/taller-matematicas/assets/images/separador2-150x50.png)

 

**3. **Estudiar la convergéncia de la serie** **$\sum_{n=1}^\infty\frac{3n^2+1}{\left(2n+1\right)n^2}$

El término general tiende a cero: $\lim_{n\rightarrow\infty}\frac{3n^2+1}{\left(2n+1\right)n^2}=\lim_{n\rightarrow\infty}\frac{O\left(n^2\right)}{O\left(n^3\right)}=0$, y puede ser convergente. Aplicando el criterio del cociente:

$\begin{array}{l}\lim_{n\rightarrow\infty}\frac{\left(3\left(n+1\right)^2+1\right)/\left(\left(2\left(n+1\right)+1\right)\left(n+1\right)^2\right)}{\left(3n^2+1\right)/\left(2n+1\right)n^2}=\\\lim_{n\rightarrow\infty}\frac{\left(3\left(n+1\right)^2+1\right)n^2\left(2n+1\right)}{\left(3n^2+1\right)\left(2\left(n+1\right)+1\right)\left(n+1\right)^2}=\lim_{n\rightarrow\infty}\frac{O\left(6n^5\right)}{O\left(6n^5\right)}=1\end{array}$

El criterio no decide. Probemos el criterio de comparación con la serie $\sum_{n=1}^\infty\frac1{n^p}$, que sabemos que es convergente para $p&gt;1$. La serie es de términos positivos, planteamos el límite del cociente

$\lim_{n\rightarrow\infty}\frac{3n^2+1}{\left(2n+1\right)n^2}:\frac1{n^p}=\lim_{n\rightarrow\infty}\frac{3n^{p+2}+n^p}{\left(2n+1\right)n^2}=\lim_{n\rightarrow\infty}\frac{O\left(3n^{p+2}\right)}{O\left(2n^3\right)}$

Para que este límite exista, ha de ser $p+2\leq3\Leftrightarrow p\leq1$ pero para que $\sum_{n=1}^\infty\frac1{n^p}$ converja ha de ser $p&gt;1$ luego la serie $\sum_{n=1}^\infty\frac{3n^2+1}{\left(2n+1\right)n^2}$ es divergente.

**NOTA**: vemos que puede existir una serie $\sum_{k=0}^\infty a_n$ basada en una sucesión $a_n$ cuyos términos tienden a cero y no obstante la serie es divergente (su suma es infinita). El hecho de que el criterio del cociente no decida, indica que es decrecimiento de los términos se va ralentizando, ya que en el límite $\lim_{n\rightarrow\infty}\frac{a_{n+1}}{a_n}=1$, los términos "sucesivos" (en el límite infinito  no hay de hecho sucesivos) son iguales. Es el caso de la serie armónica $\sum_{k=1}^\infty\frac1k$, cuyo término general tiende a cero, pero es divergente.

![separador2](/taller-matematicas/assets/images/separador2-150x50.png)

**4.** Estudiar la convergencia de la serie $\sum_{n=0}^\infty\left(\sqrt[3]{n^3-3}-\sqrt{n^2+4}\right)$

La dificultad de este problema está en que restamos dos raíces de distinto grado: el límite es indeterminado del tipo $\infty-\infty$ y no podemos racionalizar. Una forma de simplificar este tipo de expresiones es usando [series de Taylor](/taller-matematicas/2014/12/13/aplicaciones-de-las-derivadas/#taylor), en este caso, usando los desarrollos de Taylor en el punto $x=1$ para $\sqrt x$ y para $\sqrt[3]x$ que son:

$\begin{array}{l}\sqrt[3]x=1+\frac{x-1}3-\frac19\left(x-1\right)^2+\dots;\\\sqrt x=1+\frac{x-1}2-\frac18\left(x-1\right)^2+\dots\end{array}$

Simplificamos el límite sacando factor común:

$\left(\sqrt[3]{n^3-3}-\sqrt{n^2+4}\right)=n\left(\sqrt[3]{1-\frac3{n^3}}-\sqrt{1+\frac4{n^2}}\right)$

Identificando adecuadamente las "$x$" de los desarrollos obtenemos:

$\begin{array}{l}x=1-\frac3{n^3}\Rightarrow\sqrt[3]{1-\frac3{n^3}}=1+\frac{-\frac3{n^3}}3+\dots\\x=1+\frac4{n^2}\Rightarrow\sqrt{1+\frac4{n^2}}=1+\frac{\frac4{n^2}}2+\dots\end{array}$

luego:

$\begin{array}{l}n\left(\sqrt[3]{1-\frac3{n^3}}-\sqrt{1+\frac4{n^2}}\right)=n\left(1+\frac{-\frac3{n^3}}3+\dots-1-\frac{\frac4{n^2}}2-\dots\right)=\\n\left(-\frac1{n^3}-\frac2{n^2}+O\left(n^{-2}\right)\right)=-\frac1{n^2}-\frac2n+O\left(n^{-1}\right)=-\frac2n+O\left(n^{-1}\right)\end{array}$

Entonces la serie original equivale a $\sum_{n=0}^\infty\left(-\frac2n+O\left(n^{-1}\right)\right)$, que si la comparamos con la serie $\sum_{n=0}^\infty\frac1{n^p}$, que es convergente para $p&gt;1$, vemos que $\frac2n&gt;\frac1{n^p}$ para $p&gt;1$, y por tanto la serie original será divergente.

![separador2](/taller-matematicas/assets/images/separador2-150x50.png)

**5. **Estudiar la convergencia de la serie $\sum_{n=1}^\infty\left(1-\cos\left(\frac1n\right)\right).$

El término general tiende a cero: $\lim_{n\rightarrow\infty}\left(1-\cos\left(\frac1n\right)\right)=1-\lim_{n\rightarrow\infty}\cos\left(\frac1n\right)=1-\cos\left(0\right)=0$, luego la serie en principio puede ser convergente. Para ver si realmente lo es, escribimos algunos términos:

$\begin{array}{l}a_n=1-\cos\left(\frac1n\right)\Leftrightarrow\left(a_n\right)=\left\{1-\cos\left(1\right),1-\cos\left(\frac12\right),1-\cos\left(\frac13\right),\cdots\right\}=\\\left\{0.4597,0.1224,\;0.0550,\;0.0311,\;0.0199,\dots\right\}\end{array}$

vemos que decrecen bastante rápido, probemos con el criterio de comparación, usando la serie $\sum_{n=1}^\infty\frac1{n^p}$ que sabemos que es convergente para $p&gt;1$, o sea que planteamos la desigualdad $1-\cos\left(\frac1n\right)&lt;\frac1{n^p}$. Para resolverla nos auxiliamos con el desarrollo de Taylor en serie de potencias de la función  $y=\cos\left(\frac1x\right)$. Para la función $cos(x)$ y usando el valor $x=0$ tenemos:

$\begin{array}{l}\cos\left(x\right)=\cos\left(0\right)+\frac{D\cos\left(0\right)}{1!}x+\frac{D^2\cos\left(0\right)}{2!}x^2+\dots+\frac{D^n\cos\left(0\right)}{n!}x^n+\dots=\\1+(-\sin\left(0\ri
ght))x+\frac12\left(-\cos\left(0\right)\right)x^2+\frac16(\sin\left(0\right))x^3+\frac1{24}\left(\cos\left(0\right)\right)x^4+\dots=\\1-\frac12x^2+\frac1{24}x^4+\dots\end{array}$

Haciendo el cambio de $x$ por $1/x$ obtenemos la serie de de Taylor de $y=\cos\left(\frac1x\right)$, que es: $1-\frac12\frac1{x^2}+\frac1{24}\frac1{x^4}+\dots$, y por tanto

$1-\cos\left(\frac1n\right)=1-\left(1-\frac12\frac1{n^2}+\frac1{24}\frac1{n^4}+\dots\right)=\frac12\frac1{n^2}-\frac1{24}\frac1{n^4}+\dots$

que es una serie alternada. Aplicamos el criterio de comparación: $\frac12\frac1{n^2}-\frac1{24}\frac1{n^4}+\dots&lt;\frac1{n^p}$, vemos que se cumple, por ejemplo, para $p=2$, ya que $\frac12\frac1{n^2}-\frac1{24}\frac1{n^4}+O\left(\frac1{n^5}\right)&lt;\frac1{n^2}$, teniendo en cuenta que los términos sucesivos  $O\left(\frac1{n^5}\right)$ son menores que $-\frac1{24}\frac1{n^4}$. Por tanto por el criterio de comparación la serie es convergente.

![separador2](/taller-matematicas/assets/images/separador2-150x50.png)**6.** Estudiar si la serie $\sum_{n=0}^\infty\frac{2n+1}{2^n}$ es convergente, y si lo es, obtener su suma.
El término general es un cociente, e incluye un exponente en el denominador, parece buena idea probar con el criterio del cociente o el de la raíz.

$\begin{array}{l}\frac{a_{n+1}}{a_n}=\frac{\left(2\left(n+1\right)+1\right)/2^{n+1}}{\left(2n+1\right)/2^n}=\frac{2n+3}{2\left(2n+1\right)};\\\lim_{n\rightarrow\infty}\frac{a_{n+1}}{a_n}=\lim_{n\rightarrow\infty}\frac{2n+3}{2\left(2n+1\right)}=\frac24&lt;1\end{array},$

por tanto por el criterio del cociente la serie converge. Por el criterio de la raíz obtenemos el mismo resultado:

$\begin{array}{l}\sqrt[n]{a_n}=\sqrt[n]{\frac{2n+1}{2^n}}=\frac{\sqrt[n]{2n+1}}2;\\\lim_{n\rightarrow\infty}\sqrt[n]{a_n}=\lim_{n\rightarrow\infty}\frac{\sqrt[n]{2n+1}}2=\frac12\lim_{n\rightarrow\infty}\sqrt[n]{2n+1}\end{array}.$

Para obtener la suma, viendo que los términos del numerador forman una sucesión aritmética, y los del denominador una sucesión geométrica, la técnica habitual es restar los términos de la serie de ella misma, multiplicando por algún factor, para despejar luego la suma. En nuestro caso podemos hacer:

$\begin{array}{l}S_n=\sum_{k=0}^n\frac{2k+1}{2^k}=1+\frac32+\frac5{2^2}+\frac7{2^3}+\dots+\frac{2n+1}{2^n};\\\frac12S_n=\frac12\sum_{k=0}^n\frac{2k+1}{2^k}=\sum_{k=0}^n\frac{2k+1}{2^{k+1}}=\frac12+\frac3{2^2}+\frac5{2^3}+\frac7{2^4}+\dots+\frac{2n+1}{2^{n+1}}\end{array}$

Restando término a término:

$\begin{array}{l}S_n-\frac12S_n=\\\left$1+\frac32+\frac5{2^2}+\frac7{2^3}+\dots+\frac{2n+1}{2^n}\right$-\left$\frac12+\frac3{2^2}+\frac5{2^3}+\frac7{2^4}+\dots+\frac{2n+1}{2^{n+1}}\right$=\\\\1+\left(\frac32-\frac12\right)+\left(\frac5{2^2}-\frac3{2^2}\right)+\left(\frac7{2^3}-\frac5{2^3}\right)\dots+\left(\frac{2n+1}{2^n}-\frac{2\left(n-1\right)+1}{2^n}\right)-\frac{2n+1}{2^{n+1}}=\\1+\left$1+\frac12+\frac1{2^2}+\dots+\frac1{2^{n-1}}\right$-\frac{2n+1}{2^{n+1}}=\\1+\sum_{k=0}^{n-1}\frac1{2^k}-\frac{2n+1}{2^{n+1}}.\end{array}.$

La suma $\sum_{k=0}^{n-1}\frac1{2^k}$ viene dada por la fórmula de suma parcial de una serie geométrica de razón r:

$\sum_{k=0}^nr^k=\frac{1-r^{n+1}}{1-r}$

Lo aplicamos:

$\sum_{k=0}^{n-1}\frac1{2^k}=\frac{1-{\displaystyle\frac1{2^n}}}{1-{\displaystyle\frac12}}=2-\frac1{2^{n-1}}$

Sustituyendo:

$\begin{array}{l}\frac{S_n}2=1+\sum_{k=1}^{n-1}\frac1{2^k}-\frac{2n+1}{2^{n+1}}=1+2-\frac1{2^{n-1}}-\frac{2n+1}{2^{n+1}}\Leftrightarrow\\S_n=6-\frac1{2^n}-\frac{2n+1}{2^{n+2}}\end{array}$

Pasando al límite:

$\sum_{k=0}^\infty\frac{2n+1}{2^n}=\lim_{n\rightarrow\infty}\left(6-\frac1{2^n}-\frac{2n+1}{2^{n+2}}\right)=\boxed6.$

![separador2](/taller-matematicas/assets/images/separador2-150x50.png)

**7.** Ver si la serie $1-\frac12+\frac13-\frac1{2^2}+\frac1{3^2}\dots$ es convergente,  si es absolutamente convergente , y hallar su suma si es posible.
Es una serie alternada, el criterio de Leibnitz para series alternadas nos dice que si la sucesión $(a_n)$ es monótona decreciente y converge a cero, entonces la serie alternada $\overset\infty{\underset{k=0}{\sum\left(-1\right)^n}}a_n$ es convergente. En nuestro caso, ¿cuál es el término general de la sucesión? Separando en dos casos:

$1-\frac12+\frac13-\frac1{2^2}+\frac1{3^2}\dots=\left\{\begin{array}{l}\frac1{3^{\left(n-1\right)/2}}\;\text{si n es impar}\\\frac{-1}{2^{n/2}}\;\text{si n es par}\end{array}\right.$

Es evidente que las dos sucesiones cumplen el criterio de Leibnitz, luego la serie es convergente. Estudiemos ahora la convergencia absoluta. Agrupando los términos:

$\begin{array}{l}1+\frac12+\frac13+\frac1{2^2}+\frac1{3^2}\dots=\left(1+\frac13+\frac1{3^2}+\dots\right)+\left(\frac12+\frac1{2^2}+\dots\right)=\\\sum_{k=0}^\infty\frac1{3^k}+\sum_{k=1}^\infty\frac1{2^k}\end{array}$

Tenemos la suma de dos series geométricas con razones $1/3$ y $1/2$, ambas menores que 1, luego ambas son convergentes y su suma también lo será. Para hallar su suma usaremos la fórmula de la suma parcial de una serie geométrica para pasar luego al límite.

$\begin{array}{l}\sum_{k=0}^n\frac1{3^k}=\frac{1-{\displaystyle\frac1{3^{n+1}}}}{1-{\displaystyle\frac13}}=\frac32-\frac1{2\cdot3^n}\xrightarrow\infty\frac32;\\\sum_{k=1}^\infty\frac1{2^k}=\frac{1-{\displaystyle\frac1{2^{n+1}}}}{1-{\displaystyle\frac12}}-\frac1{2^0}=2-\frac1{2^n}-1\xrightarrow\infty1.\end{array}$

Observad que hemos restado el término $a_0=1/2^0$ en la segunda sucesión debido a que la fórmula de la suma empieza en el índice 0, y nosotros queremos sumar a partir del índice 1. En conclusión, la serie es absolutamente convergente, y su suma vale $1+\frac12+\frac13+\frac1{2^2}+\frac1{3^2}\dots=\frac32+1=\frac52.$ La suma de la serie alternada es $3/2-1=1/2$.

![separador2](/taller-matematicas/assets/images/separador2-150x50.png)**8.** Ver si la serie $\sum_{k=0}^\infty\left(-1\right)^k\frac{k^3}{k!}$ es convergente y si es absolutamente convergente.

Aplicamos el criterio de Leibnitz, primero, ver si la sucesión de término general $\left(a_n\right)=\frac{n^3}{n!}$ es monótona decreciente, para ello, estudiamos la desigualdad $a_{n+1}\leq a_n$, que es:

$\begin{array}{l}\left(a_{n+1}\right)=\frac{\left(n+1\right)^3}{\left(n+1\right)!}\Rightarrow\\\left(a_{n+1}\right)\leq\left(a_n\right)\Leftrightarrow\frac{\left(n+1\right)^3}{\left(n+1\right)!}\leq\frac{n^3}{n!}\Leftrightarrow\frac{\left(n+1\right)^3}{n^3}\leq\left(n+1\right)\Leftrightarrow\frac{\left(n+1\right)^2}{n^3}\leq1.\end{array}$

La última desigualdad se cumple a partir del tercer término $n\geq3$; no es necesario resolver la inecuación exactamente, basta con probar algunos términos, ya que $\frac{\left(n+1\right)^2}{n^3}\leq1\Leftrightarrow n^3\geq\left(n+1\right)^2\Leftrightarrow n^3-\left(n+1\right)^2\geq0$, y la función $f(x)=x^3-\left(x+1\right)^2$ es creciente (puede verse estudiando el signo de su derivada) para $x\geq\1$ (o sea, para $n\geq\1$), por tanto si encontramos un término que cumpla la condición, todos los términos siguientes también lo cumplirán.  Tenemos pues que la sucesión es monótona decreciente. Veamos que converge a cero:

$\begin{array}{l}\lim_{n\rightarrow\infty}\frac{n^3}{n!}=\lim_{n\rightarrow\infty}\frac{n\cdot n\cdot n}{n\left(n-1\right)\left(n-2\right)\dots}\leq\lim_{n\rightarrow\infty}\frac{n\left(n-1\right)\left(n-2\right)}{n\left(n-1\right)\left(n-2\right)\dots}=\\\lim_{n\rightarrow\infty}\frac1{\left(n-3\right)!}=0.\end{array}$

Como la sucesión es de términos positivos, y su límite es menor o igual a cero, forzosamente ha de tener límite igual a cero. Por tanto, por el criterio de Leibnitz, la serie alternada
es convergente.

Para estudiar la convergencia absoluta aplicamos el criterio del cociente:

$\lim_{n\rightarrow\infty}\frac{a_{n+1}}{a_n}=\lim_{n\rightarrow\infty}\frac{\left(n+1\right)^3/\left(n+1\right)!}{n^3/n!}=\lim_{n\rightarrow\infty}\frac{\left(n+1\right)^3}{n^3\left(n+1\right)}=\lim_{n\rightarrow\infty}\frac{\left(n+1\right)^2}{n^3}=0$

por ser el grado del denominador mayor que el del numerador; la serie es absolutamente convergente.

**NOTA**: la convergencia absoluta implica la convergencia de la serie alternada, luego hubiera sido mucho más rápido empezar por la segunda parte. En general, si nos piden estudiar ambas convergencias, empezaremos siempre por la absoluta; si es absolutamente convergente, hemos terminado, si no lo es, entonces habrá que estudiar la convergencia condicional. Aquí hemos procedido en el mismo orden que dicta el enunciado por razones didácticas: ver ambos métodos.

![separador2](/taller-matematicas/assets/images/separador2-150x50.png)

# Bibliografía

 

Sucesiones y series infinitas (Curso programado de Cálculo C.E.M.). Un libro antiguo e injustamente olvidado, en mi opinión. El Curso programado sigue la didáctica [constructivista](https://es.wikipedia.org/wiki/Constructivismo_%28pedagog%C3%ADa%29), introduciendo cada concepto con ejemplos, de forma que el alumno va construyendo su conocimiento en vez de simplemente memorizarlo.
{% endraw %}
