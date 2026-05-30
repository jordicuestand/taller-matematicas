---
layout: post
title: "El teorema de los números primos"
date: 2015-09-20 11:24:23 +0000
categories:
  - "Matemáticas"
tags:
  - "números primos"
math: true
---
{% raw %}

Los números primos son a la vez simples y terriblemente complejos, siendo uno de los campos siempre activos de investigación matemática. Son simples porque son fáciles de entender: son aquellos números naturales que sólo son divisibles por 1. Son complicados en cuanto intentamos descubrir sus propiedades como números.

En la antigüedad se intentó investigar estas propiedades exclusivamente usando la Aritmética y la imaginación, tratando de ver modos de ver y de demostrar cómo se comportan los números primos, cómo se distribuyen, si hay infinitos o no, etc. Llegados al siglo XVIII los matemáticos ya se habían dado cuenta de que no se podía avanzar más por ese camino, y empezaron a usar métodos más potentes: curiosamente, se necesitan números complejos para descubrir las propiedades de los simples enteros primos.

# Teorema de los números primos

Hay muchos teoremas sobre los números primos, pero sólo uno ha merecido el nombre de "El teorema de los números primos": el que establece cuantos hay en un cierto intervalo de los números enteros. Para ver el razonamiento, partimos de las [series de números reales](/taller-matematicas/2015/07/25/series-de-numeros-reales/), concretamente de la[ serie geométrica](https://ca.wikipedia.org/wiki/S%C3%A8rie_geom%C3%A8trica):
$\sum\nolimits_{k=0}^\infty\frac1{x^k}=1+\frac1x+\frac1{x^2}+\cdots$

de razón $r=1/x$, que converge al valor $\frac1{1-r}=\frac1{1-x^{-1}}$ siempre que $r &lt; 1$, o sea que $x &gt; 1$.

Apliquemos este hecho tomando como x algunos números primos:

$\begin{array}{l}\sum\nolimits_{k=0}^\infty\frac1{2^k}=1+\frac12+\frac1{2^2}+\cdots=\frac1{1-2^{-1}};\\\sum\nolimits_{k=0}^\infty\frac1{3^k}=1+\frac13+\frac1{3^2}+\cdots=\frac1{1-3^{-1}};\\\sum\nolimits_{k=0}^\infty\frac1{5^k}=1+\frac15+\frac1{5^2}+\cdots=\frac1{1-5^{-1}};\end{array}$

Multipliquemos ahora entre sí estos desarrollos:

$\frac1{1-2^{-1}}\times\frac1{1-3^{-1}}\times\frac1{1-5^{-1}}=\left(1+\frac12+\frac1{2^2}+\cdots\right)\left(1+\frac13+\frac1{3^2}+\cdots\right)\left(1+\frac15+\frac1{5^2}+\cdots\right)$

Los términos de la derecha son una suma infinita del tipo $\frac1{2^\alpha}\cdot\frac1{3^\beta}\cdot\frac1{5^\gamma}$ con $0\leq\alpha,\beta,\gamma\leq+\infty$; por ejemplo, algunos términos son $\frac12,\;\frac1{2\cdot3^2},\frac1{3^3\cdot5^2},\frac1{2^8\cdot3^2\cdot5},\dots$. Pero los denominadores de éstos términos son de hecho una descomposición en factores primos de enteros: $\frac12,\;\frac1{2\cdot3^2}=\frac1{18},\frac1{3^3\cdot5^2}=\frac1{67},\frac1{2^8\cdot3^2\cdot5}=\frac1{11520},\dots$. Entonces, la suma infinita comprenderá todos los enteros que pueden descomponerse en los factores primos 2, 3, 5, ya que las potencias $\alpha,\beta,\gamma$ toman todos los valores posibles. Por ejemplo, para 1/540 tenemos el término 1/2²·3³·5.

Si en vez de limitarnos a los primos 2, 3 y 5 tomamos todos los primos:

$\frac1{1-2^{-1}}\times\frac1{1-3^{-1}}\times\frac1{1-5^{-1}}\times\dots\frac1{1-p^{-1}}\times\dots$

entonces en el lado derecho tendremos todas la fracciones con denominadores iguales a cualquier combinación de potencias de cualquier primo ... esto es, la descomposición en factores primos de cualquier número entero, o sea, ¡todos los números enteros!

$\frac1{1-2^{-1}}\times\frac1{1-3^{-1}}\times\frac1{1-5^{-1}}\times\dots\frac1{1-p^{-1}}\times\dots=\frac11+\frac12+\frac13+\dots+\frac1n+\dots$
## Formula de Euler

Recordando de nuevo la serie geométrica, pero sustituyendo x por la potencia s-ésima de un número primo p cualquiera, obtenemos $\sum\nolimits_{k=0}^\infty\frac1{\left(p^s\right)^k}=1+\frac1{p^s}+\frac1{p^{2s}}+\cdots$, con suma $\frac1{1-p^{-s}}$. Esta formula fue descubierta por Euler hacia el año 1737:

$\frac1{1-2^{-s}}\times\frac1{1-3^{-s}}\times\frac1{1-5^{-s}}\times\dots\frac1{1-p^{-s}}\times\dots=\frac1{1^s}+\frac1{2^s}+\frac1{3^s}+\dots+\frac1{n^s}+\dots$

Que suele escribirse en forma más compacta, usando los símbolos sumatorio y productorio:

$\boxed{\sum\nolimits_{n=1}^\infty\frac1{n^s}=\underset{}{\prod_p\frac1{1-p^{-s}}}},$

donde el subíndice "p" debajo del símbolo del productorio simboliza que se realiza el producto tomando todos los número primos. Esta es una fomula notable, pues relaciona todo el conjunto de número primos con el de los enteros.

La serie $\sum\nolimits_{n=1}^\infty\frac1{n^s}$ por comparación con la [serie armónica](https://es.wikipedia.org/wiki/Serie_arm%C3%B3nica_%28matem%C3%A1tica%29) que es divergente, puede demostrarse que es convergente sólo para s < 1. Entonces tiene sentido definir una función basada en esa serie: $f\left(s\right)=\sum\nolimits_{n=1}^\infty\frac1{n^s}$, que aunque hemos discutido sólo para valores s enteros, es válida para números reales siempre que s > 1. Nadie ha encontrado una expresión analítica para esta función, sus valores se calculan con ordenador; algunos de sus valores son (obtenidos sumando los 200 primeros términos de la serie):

 

| **s** 
| 1,01 
| 1,13 
| 1,25 
| 1,50 
| 2,00 
| 2,50 
| 3,00 
| 3,50 
| 5,00 
| 10,00 

| **f(s)** 
| 5,70 
| 4,45 
| 3,52 
| 2,47 
| 1,64 
| 1,34 
| 1,20 
| 1,08 
| 1,04 
| 1,00 

Una primera consecuencia de la formula de Euler es:

existen infinitos números primos

En efecto, tomando s=1 su formula es $\sum\nolimits_{n=1}^\infty\frac1n=\prod\frac1{1-p^{-1}}$, como la serie armónica diverge, el producto $\prod\frac1{1-p^{-1}}=\frac1{1-2^{-1}}\cdot\frac1{1-3^{-1}}\cdot\frac1{1-5^{-1}}\dots$ da infinito como resultado, y eso sólo será posible si hay infinitos términos primos.

Otra consecuencia es:

Teorema de Euler: la suma de los recíprocos de los números primos, $\frac12+\frac13+\frac15+\dots+\frac1p+\dots$ diverge.

Esta es una propiedad que no es evidente, pues los recíprocos de los números primos disminuyen rápidamente al aumentar el número primo. Por ejemplo, para los 100 primeros primos la suma de los recíprocos es $\frac12+\frac13+\frac15+\dots+\frac1{541}=2,1063421215$, para los 1.000 primeros es $\frac12+\frac13+\frac15+\dots+\frac1{7919}=2,4574112767,$ si sumamos los 10.000 primeros primos obtenemos $\frac12+\frac13+\frac15+\dots+\frac1{104729}=2,7092582488$, etc. Parece que la suma ha de estancarse en algún valor límite pero no es así, simplemente crece muy despacio.

Para ver que la suma diverge,  en la formula de Euler tomamos logaritmos:

$\log\left(\sum\nolimits_{n=1}^\infty\frac1{n^s}\right)=\log\left(\prod_p\frac1{1-p^{-s}}\right)$

El productorio sobre los primos se transforma en una suma:

$\log\left(\prod_p\frac1{1-p^{-s}}\right)=\sum_p\log\left(\frac1{1-p^{-s}}\right)$

Utilizando el desarrollo de Taylor siguiente: $\log\left(1+x\right)=\sum\nolimits_{n=1}^\infty\left(-1\right)^{n+1}\frac{x^n}n$, tomando $x=-p^{-s}$, la suma de logaritmos queda como:

$\sum_p\log\left(\frac1{1-p^{-s}}\right)=\underset p{-\sum}log\left(1-p^{-s}\right)=-\sum_p\sum\nolimits_{n=1}^\infty\left(-1\right)^{n+1}\frac{\left(-p^{-s}\right)^n}n$

Arreglamos un poco la expresión de la suma interna:

$-\sum\nolimits_{n=1}^\infty\left(-1\right)^{n+1}\frac{\left(-p^{-s}\right)^n}n=\sum\nolimits_{n=1}^\infty\left(-1\right)^n\left(-1\right)^n\frac{\left(p^{-s}\right)^n}n=\sum\nolimits_{n=1}^\infty\frac{p^{-ns}}n$

Hacemos s  = 1 para obtener la serie $\sum\nolimits_{n=1}^\infty\frac{p^{-n}}n=\frac1p+\frac1{2p^2}+\frac1{3p^3}+\dots.$ Esta serie es convergente, pues la serie geométrica $\sum\nolimits_{n=1}^\infty\frac1{p^n}=\frac1p+\frac1{p^2}+\dots$ de razón 1/p tiene términos mayores que ella, y converge: $\sum\nolimits_{n=1}^\infty\frac1{p^n}=\frac1p+\frac1{p^2}+\dots=\frac1{1-{\displaystyle\frac1p}}=\frac
p{p-1}$.

Como la serie es convergente, podemos tomar sólo el primer término y consideramos la suma de los restantes términos:

$\sum\nolimits_{n=1}^\infty\frac{p^{-n}}n=\frac1p+\left(\frac1{2p^2}+\frac1{3p^3}+\dots\right)&lt;\frac1p+\left(\frac1{p^2}+\frac1{p^3}+\dots\right)=\frac1p+\frac1{p^2}\left(1+\frac1p+\frac1{p^2}+\dots\right).$

La serie es geométrica, de razón 1/p, y su suma es $\frac1{1-1/p}=\frac p{p-1}$. O sea que:

$\sum\nolimits_{n=1}^\infty\frac{p^{-n}}n&lt;\frac1p+\frac1{p^2}\left(\frac p{p-1}\right)\;\;=\frac1p+\frac1{p\left(p-1\right)}$

Lo podemos expresar así: $\sum\nolimits_{n=1}^\infty\frac{p^{-n}}n=\frac1p+C_p$, con $C_p&lt;\frac1{p\left(p-1\right)}$

Entonces la igualdad inicial con logaritmos se reduce a:

$\log\left(\sum\nolimits_{n=1}^\infty\frac1n\right)=\sum_p\left(\frac1p+C_p\right)=\sum_p\frac1p+\sum_pC_p$

Para la suma de $C_p$ para todos los primos, podemos hacer las siguientes comparaciones:

$\sum_pC_p&lt;\sum_p\frac1{p\left(p-1\right)}&lt;\sum_p\frac1{\left(p-1\right)^2}&lt;\sum\nolimits_{n=1}^\infty\frac1{n^2}$

La serie $\sum\nolimits_{n=1}^\infty\frac1{n^2}$ converge, mientras que la serie $\left(\sum\nolimits_{n=1}^\infty\frac1n\right)$  es la serie armónica, que diverge, luego la suma $\sum_p\frac1p$ también ha de ser divergente.

 Euler llegó a otro resultado más preciso:

La suma de los recíprocos de todos los primos hasta el primo *p* es del orden de *Ln(Ln(p))*.

Ya hemos visto que $\log\left(\sum\nolimits_{n=1}^\infty\frac1n\right)\approx\sum_p\frac1p$; por otro lado el mismo Euler provó que:

$\underset{n\rightarrow\infty}{lim}\left$\left(\sum\nolimits_{n=1}^\infty\frac1n\right)-\ln\left(n\right)\right$=\gamma=0.5772156649\dots$

donde la constante $\gamma$ se conoce por la [constante de Euler-Mascheroni](https://en.wikipedia.org/wiki/Euler%E2%80%93Mascheroni_constant); usando esta igualdad llegamos a:

$\underset{n\rightarrow\infty}{lim}\sum\nolimits_{n=1}^\infty\frac1n=\gamma+\underset{n\rightarrow\infty}{lim}ln\left(n\right)$

y por tanto,

$\log\left(\sum\nolimits_{n=1}^\infty\frac1n\right)=\log\left(\log\left(n\right)\right)\approx\sum_p\frac1p$

para enteros n y primos p muy grandes.
{% endraw %}
