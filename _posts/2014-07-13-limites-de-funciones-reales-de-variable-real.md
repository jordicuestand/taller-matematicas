---
layout: post
title: "Límites de funciones reales de variable real"
date: 2014-07-13 16:33:05 +0000
categories:
  - "Cálculo en R"
  - "Funciones reales de variable real"
  - "Matemáticas"
tags:
  - "función de Dirichlet"
  - "límite función"
  - "límites de funciones racionales"
  - "límites laterales"
math: true
---
{% raw %}

# Introducción

![limit_funció_1](/taller-matematicas/assets/images/limit_funció_1.png) El límite de f(x) en x=a es L si y=f(x) se acerca al valor L a medida que x se acerca al valor a

Intuitivamente, decimos que el límite de la función $f(x)$ en el punto $x=a$ es $L$, y escribimos $\lim_{x\rightarrow a}f(x)=L$, si se cumple que, cuanto más nos acercamos al punto $x=a$, más se acerca el valor correspondiente de la función a $L$.

Más formalmente (o sea, con más exactitud), definimos:

**Definición 1**: **límite de una función $f(x)$  en un punto $x=a$**
Sea la función $f(x)$ con dominio A. Decimos que $\lim_{x\rightarrow a}f(x)=L$ si y sólo si para cada entorno del punto $L$ con radio $R$, $B(L, R)$, existe otro entorno del punto $a$  con radio $r$, $B(a, r)$, tal que los valores $f(x)$ de la función pertenecen al entorno $B(L, R)$ para todo $x\in B^\ast(a,r)\bigcap A$. La notación $B^\ast(a,r)$ indica un *entorno reducido* de $a$, que es igual al entorno  al cual se le ha "extraído" el propio punto $a$: $B^\ast(a,r)=B(a,r)-\left\{a\right\}$.

En particular, tanto el punto $a$ como el límite $L$ pueden tomar valores infinitos $\infty$.

Nota: El uso del entorno reducido $B^\ast(a,r)$  es equivalente a decir que el punto $a$ pertenenece al conjunto de puntos de acumulación del dominio $A$ de la función: $a\in Acum\left(A\right)$.  Dicho con menos tecnicismo: en cualquier entorno del punto $a$ han de haber puntos del dominio de la función, excluido el propio $a$.

Las definiciones matemáticas, exactas, sin ambigüedades,  suelen sin embargo ser "oscuras" para los no "iniciados", por ello vamos a ver algunos ejemplos.

**Ejemplo 1. Limite finito en un punto. **

![limit_funció_2](/taller-matematicas/assets/images/limit_funció_21.png)

 
La función $f(x)=x^2$ tiene dominio $A=\mathbb{R}$. El límite de $f(x)$ en $x=\frac12$ es $L=\frac14$. Entonces, dado un $R&gt;0$, por ejemplo $R=0.001$ (se suelen tomar valores "pequeños" de R, para comprobar que podemos acercarnos al límite $L$ todo lo que queramos), existirá un $r&gt;0$, por ejemplo tomemos $r=0.0001$, tal que para cualquier punto $x$ dentro del entorno $B(\frac12, 0.0001)$, la imágen $y=f(x)$ estará dentro del entorno  $B(\frac14, 0.001)$. En efecto,

$x\in B(\frac12,0.0001)\Leftrightarrow\frac12-0.0001\leq x\leq\frac12+0.0001\Leftrightarrow0.4999\leq x\leq0.5001$

Elevando al cuadrado:

$0.24990001\leq x^2\leq0.25001\Leftrightarrow0.249\;\leq x^2\leq0.251\Leftrightarrow\frac12-0.001\leq f(x)\leq\frac12+0.001$,

por tanto se cumple la condición. Lo hemos probado para un valor concreto de $R$, y hemos encontrado el valor correspondiente $r$ por tanteo. Para hacerlo bien, habría que demostrar que podemos encontrar un $r$ para cualquier $R$ dado. En los ejercicios resueltos lo veremos.

**Ejemplo 2. Límite infinito en un punto. Límite en el infinito.**

![limit_funció_3](/taller-matematicas/assets/images/limit_funció_3.png)

El dominio de la función $Ln(x)$ es $\mathbb{R}^+-\left\{0\right\}$, o, equivalentemente, $\left\{x\left|0&lt;x&lt;+\infty\right.\right\}$.

En el caso $\lim_{x\rightarrow0}Ln(x)=-\infty$ tenemos que el límite $L$ en un punto tiene un valor infinito. ¿Cómo afecta entonces la definición que hemos dado usando entornos? Siendo $L=-\infty$ el entorno $B(L, R)$  se convierte en $B(-\infty, R)$ que equivale al valor $-\infty$, ya que para cualquier $R$ los entornos de $-\infty$ estan en el $-\infty$. Por tanto la definición de límite es ahora: dado cualquier valor $-\infty&lt;L&lt;0$, existirá un $r&gt;0$ tal que, si $x\in B^\ast(0,r)\bigcap A$, entonces $f(x)&gt;L$. Observemos que $x\in B^\ast(0,r)\bigcap A\Leftrightarrow0&lt;x&lt;r$.

El otro caso interesante es $\lim_{x\rightarrow\infty}Ln(x)=+\infty$, no es un límite en un punto $x=a$ sino en el infinito. La definición con entornos también ha de ajustarse en este caso. Intuitivamente, $\lim_{x\rightarrow\infty}Ln(x)=+\infty$ indica que cuando  los valores de $x$ se hacen arbitrariamente grandes, los valores de la función  también lo hacen.

**Ejemplo 3. Límite finito en el infinito.**

![limit_funció_4](/taller-matematicas/assets/images/limit_funció_4.png)

$\lim_{x\rightarrow\infty}\frac1x=0$, el límite en el infinito és un valor finito, en este caso cero.

**Proposición 1, unicidad del límite:**

Si existe el límite $L=\lim_{x\rightarrow a}f(x)$ entonces $L$ es el único limite de la función $f(x)$ en el punto $x=a$.

# Límites laterales

Consideremos la función $y=f(x)=tg(x)=\frac{\sin(x)}{\cos(x)}$, y fijémonos en una parte de su gráfica, entre los puntos $x=0$ y $x=\mathrm\pi$

![limit_funció_5](/taller-matematicas/assets/images/limit_funció_5.png)

¿Que vale el límite $\lim_{\mathrm x\rightarrow\mathrm\pi/2}\mathrm f(\mathrm x)$? Cerca del punto $x=\mathrm\pi/2 \approx 1.57$ el valor de $f(x)$ se hace infinito, pero con distinto signo dependiendo si nos acercamos por la izquierda, $+\infty$ en este caso, o por la derecha, $-\infty$. De hecho, el punto $x=\mathrm\pi/2$ no es del dominio de la función, pero ya sabemos que esto no es un problema para el cálculo de límites, basta con que sea un punto de acumulación del dominio.

Entonces en este caso no está bien definido el $\lim_{x\rightarrow\frac{\mathrm\pi}2}\tan\left(x\right)$, en cambio sí lo tenemos definido si lo calculamos o bien por la derecha o bien por la izquierda. Por tanto, tiene sentido definir los límites laterales:

**Definición 2**: **límite lateral por la izquierda de una función $f(x)$  en un punto $x=a$**

Si el punto $a$ pertenece al conjunto de puntos de acumulación del dominio $A$ del la función $f(x)$, definimos el conjunto $A^-=\left(-\infty,a\right)\cap A$, y el **límite lateral por la izquierda en $a$ es**

$\begin{array}{l}\lim_{x\rightarrow a^{-\;\;}}f(x)=\lim_\overset{x\rightarrow a}{x\in A^-}f(x)\\\end{array}$

**Definición 3**: **límite lateral por la derecha de una función $f(x)$  en un punto $x=a$**
Si el punto $a$ pertenece al conjunto de puntos de acumulación del dominio $A$ de la función $f(x)$, definimos el conjunto $A^+=\left(a,+\infty\right)\cap A$ y el **límite lateral por la derecha en $a$ es**

$\begin{array}{l}\lim_{x\rightarrow a^{+\;\;}}f(x)=\lim_\overset{x\rightarrow a}{x\in A^+}f(x)\end{array}$

 **Proposición 2, límites laterales y convergéncia:**
El $\lim_{x\rightarrow a}f(x)$ existe si y solo si existen los  límites laterales y además coinciden entre sí:  $\lim_{x\rightarrow a^+}f(x)=\lim_{x\rightarrow a^-}f(x)=\lim_{x\rightarrow a^{}}f(x)$

**Ejemplo 4: no coincidencia de límites laterales en la función $tg(x)$**

$\lim_{x\rightarrow\frac{\mathrm\pi}2^+}tg(x)=-\infty,\lim_{x\rightarrow\frac{\mathrm\pi}2^-}tg(x)=+\infty$. Por tanto el $\lim_{x\rightarrow\frac{\mathrm\pi}2^{}}tg(x)$ no existe, la función $tg(x)$ no es convergente en el punto $x=\frac{\mathrm\pi}2$

**Ejemplo 5: no coincidencia de límites laterales en la función parte entera.**

La función parte entera se define así:
$f(x)=\left\{\begin{array}{l}x\;\text{si }x\in\mathbb{Z}\\max\;\left\{k\in\mathbb{Z}\left|k\leq x\right.\right\}\end{array}\right.$

Por ejemplo, $f(1) =1$ , $f(1.5) = 1$, pues 1 es el mayor entero menor o igual a 1.5 .

![part_entera](/taller-matematicas/assets/images/part_entera.png)

Si estudiamos los límites laterales en, por ejemplo, $x=1$:
$\lim_{x\rightarrow1^-}f(x)=0,\;\lim_{x\rightarrow1+}f(x)=1$

Por tanto no existe el $\lim_{x\rightarrow1}f(x)=0$. En cambio, en el punto $x=1.5$ si coinciden los límites laterales: $\lim_{x\rightarrow1.5^-}f(x)=1,\;\lim_{x\rightarrow1.5+}f(x)=1$, luego $\lim_{x\rightarrow1.5}f(x)=1$.

**Ejemplo 6: una función no convergente en ningún punto.**

Sea la [función de Dirichlet](http://es.wikipedia.org/wiki/Funci%C3%B3n_de_Dirichlet):
 $f(x)=\left\{\begin{array}{l}x\;\text{si }x\in\mathbb{Q}\\0\;\text{si }x\not\in\mathbb{Q}\end{array}\right.$

Entonces para cualquier punto $a\in\mathbb{R}$ no existen los límites laterales en ese punto, y por tanto la función no tiene límite en ningún punto.  Esto es debido a las propiedades de los números reales: entre dos números racionales cualquiera, hay infinitos números reales e infinitos números racionales, y al acercarnos lateralmente la función va tomando valores distintos, sin converger a ningún valor particular.

 
# Propiedades de los límites de funciones

**Propiedades de orden**

Si $f:A\rightarrow\mathbb{R}$  tiene límite $L$ en $x=a$, y $g:A\rightarrow\mathbb{R}$  tiene límite $M$ en $x=a$, y además se cumple que $f(x)\leqg(x)$, entonces $L\leqM$.

Si $f,g,h:A\rightarrow\mathbb{R}$ , $f(x)\leqg(x)\leqh(x)$ y además $\lim_{x\rightarrow a}f(x)=\lim_{x\rightarrow a}h(x)=L$, entonces $\lim_{x\rightarrow a}g(x)=L$.

**Propiedades aritmèticas**

$\lim_{x\rightarrow a}\left(f\pm g\right)(x)=\lim_{x\rightarrow a}f(x)\pm\lim_{x\rightarrow a}g(x)$

$\lim_{x\rightarrow a}\left(f\cdot g\right)(x)=\lim_{x\rightarrow a}f(x)\cdot\lim_{x\rightarrow a}g(x)$

$\lim_{x\rightarrow a}\left(f/g\right)(x)=\lim_{x\rightarrow a}f(x)/\lim_{x\rightarrow a}g(x)$ siempre que $\lim_{x\rightarrow a}g(x)\neq0$.

**Límite de un polinomio**

Si $f(x)=a_nx^n+a_{n-1}x^{n-1}+\dots+a_1x+a_0$, entonces $\lim_{x\rightarrow a}f(x)=f(a)$.

**Ejemplo 7**

$\lim_{x\rightarrow\frac{\mathrm\pi}2}x^2\sin\left(x\right)=\lim_{x\rightarrow\frac{\mathrm\pi}2}x^2\cdot\lim_{x\rightarrow\frac{\mathrm\pi}2}\sin\left(x\right)=\frac{\mathrm\pi^2}4\cdot1=\frac{\mathrm\pi^2}4$  por la propiedad de la suma de límites.
# Límites** de funciones racionales**

Una función racional $f(x)$ es la que tiene como expresión un cociente de polinomios $\frac{g(x)}{h(x)}$. En general hemos visto que $\lim_{x\rightarrow a}\frac{g(x)}{h(x)}=\frac{\lim_{x\rightarrow a}g(x)}{\underset{x\rightarrow a}{\lim\;h(x)}}$, excepto si $\underset{x\rightarrow a}{\lim\;h(x)}=0$. Vamos a estudiar este caso.

**Caso particular $f(x)=\frac1{\left(x-a\right)^n}$ **

Comencemos por la función racional $f(x)=\frac1{\left(x-a\right)^n}$ estudiando el límite $\lim_{x\rightarrow a}f(x)$. Supongamos que $n$ es un entero par. En este caso, el denominador $\left(x-a\right)^n$ será mayor que cero para todo $x$. En la siguiente figura vemos representada la función para $n=2$ y $a=1$.

![racional1](/taller-matematicas/assets/images/racional1.png) f(x) = 1/(x-1)²
Vemos que los límites laterales en $x=a$ son ambos coincidentes y valen $+\infty$.  En el caso de que $n$ sea impar, el signo de $\left(x-a\right)^n$  será positivo para $x&gt;a$ y negativo para  $x&lt;a$. En la siguiente figura vemos el caso $f(x)=\frac1{x-1}$.

![racional3](/taller-matematicas/assets/images/racional3.png) f(x) = 1/(x-1)
Ahora los límites laterales en $x=1$ no coinciden, así que no tenemos ĺimite en ese punto.

Concluimos pues:

 	- Si $n$ es par, $\lim_{x\rightarrow a}\frac1{\left(x-a\right)^n}=+\infty$

 	- Si $n$ es impar, no existe el límite $\lim_{x\rightarrow a}\frac1{\left(x-a\right)^n}$

**Caso general**

Estudiamos ahora $L=\lim_{x\rightarrow a}\frac{a_nx^n+a_{n-1}x^{n-1}+\dots+a_1x+a_0}{b_mx^m+b_mx^{m-1}+\dots+b_1x+b_0}=\lim_{x\rightarrow a}\frac{g(x)}{h(x)}$.  Observemos que el numerador es un polinomio de grado $n$ y el denominador otro polinomio de grado $m$.

**1)** Si $h(a)\neq0$ entonces simplemente $L=f(a)$.

**2)** Si $h(a)=0$, pero $g(a)\neq0$, significa que $x=a$ es una raíz (o un "cero") del polinomio $h(x)$ con multiplicidad $p$, lo cual significa que se cumple la siguiente igualdad:

$h(x)=\left(x-a\right)^p\cdot h_r(x)$

donde $p$ es un entero menor o igual al grado $m$ del polinomio, y $h_r(x)$ es otro polinomio de grado $m-p$ que cumple $h_r(a)\neq0$. En notación de división de polinomios:

$\begin{array}{l}h(x)\;\left|\underline{\left(x-a\right)}^p\right.\\\underline0\;\;\;\;\;\;\;h_r(x)\end{array}$

Entonces:

$L=\underset{x\rightarrow a}{\lim\;\;}\frac{g(x)}{h(x)}=\underset{x\rightarrow a}{\lim\;\;}\frac{g(x)}{\left(x-a\right)^p\cdot h_r(x)}=\underset{x\rightarrow a}{\lim\;\;}\frac1{\left(x-a\right)^p}\cdot\underset{x\rightarrow a}{\lim\;\;}\frac{g(x)}{h_r(x)}$

Pero del caso particular que hemos estudiado sabemos que

$\underset{x\rightarrow a}{\lim\;\;}\frac1{\left(x-a\right)^p}=\left\{\begin{array}{l}+\infty\text{ si }p\;\text{es par}\\\text{no existe si }p\;\text{es impar}\;\end{array}\right.$

Por tanto

$L=\left\{\begin{array}{l}+\infty\text{ si }p\;\text{es par}\\\text{no existe si }p\;\text{es impar}\;\end{array}\right.$

**3) **Si $g(a)\eq0$ pero $h(a)\neq0$ entonces $L\eq0$.

**4)** El último caso posible es $g(a)\eq0$ y simultáneamente $h(a)\eq0$, con lo que tenemos un límite indeterminado del tipo $\frac00$. Sabemos que $x\eqa$ es una raíz tanto del numerador como del denominador:

$\left.\begin{array}{r}g(x)=\left(x-a\right)^pg_r(x)\\h(x)=\left(x-a\right)^qh_r(x)\end{array}\right\}\Rightarrow\frac{g(x)}{h(x)}=\frac{\left(x-a\right)^pg_r(x)}{\left(x-a\right)^qh_r(x)}=\left(x-a\right)^{p-q}\frac{g_r(x)}{h_r(x)}$,

con $g_r(a)\ne0$ y $h_r(a)\ne0$. Entonces:

 	- Si $p-q&gt;0$ entonces $L=0·\frac{g_r(a)}{h_r(a)}=0$.

 	- Si $p-q&lt;0$ vale lo dicho en el caso 2: $L=\left\{\begin{array}{l}+\infty\text{ si }p\;\text{es par}\\\text{no existe si }p\;\text{es impar}\;\end{array}\right.$

 	- Si $p-q=0$ entonces $L = 1·\frac{g_r(a)}{h_r(a)}=\frac{g_r(a)}{h_r(a)}$.

**Ejemplos de límites de funciones racionales**

Sea la función $f(x)=\frac{x+1}{x^2-1}$.

**(a) **$L=\lim_{x\rightarrow0}f(x)=\frac{0+1}{0-1}=-1.$

**(b)** $L=\lim_{x\rightarrow1}f(x)=\frac20=?$. Observamos que $a=1$ es una raíz del polinomio $h(x)=x^2-1$, ¿cuál es su multiplicidad $p$? Igualando a cero y resolviendo la ecuación: $x^2-1=0\Rightarrow x^2=1\Rightarrow x=\pm1$, la multiplicidad $p=1$, un número impar, por lo tanto no existe el límite $L$. En efecto, si estudiamos los límites laterales en $x=1$ vemos que no coinciden:

$\left\{\begin{array}{l}\lim_{x\rightarrow1^-}\frac{x+1}{x^2-1}=\frac2{0^-}=-\infty\\\lim_{x\rightarrow1^+}\frac{x+1}{x^2-1}=\frac2{0^+}=+\infty\end{array}\right.$

**(c)** $L=\lim_{x\rightarrow-1}f(x)=\frac00=?$. ¿Cuál es la multiplicidad de la raíz $a=-1$? En este caso es inmediato ver que tanto para el numerador como para el denominador la multiplicidad es 1.  Por tanto,  $L=\lim_{x\rightarrow-1}\frac{x+1}{x^2-1}=\lim_{x\rightarrow-1}\frac{x+1}{\left(x+1\right)\left(x-1\right)}=\lim_{x\rightarrow-1}\frac1{\left(x-1\right)}=\frac1{-2}$.

**(d)** Sea ahora la función $f(x)=\frac{\left(x+1\right)^3}{x^2-1}$. ¿Qué vale el límite de la función en el punto $x=-1$?. Si sustituimos el valor resulta $\frac00=?$. Evidentemente, la multiplicidad del numerador es $p=3$, y la del numerador hemos visto antes que es $q=1$.  Así pues $p-q&gt;0$, y por tanto $L=0$.

---

[Ir a problemas resueltos de límites de funciones ]({{ site.baseurl }}/2014/08/15/problemas-resueltos-de-limites-de-funciones-reales/)
{% endraw %}