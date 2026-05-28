---
layout: post
title: "Aplicaciones de las derivadas"
date: 2014-12-13 18:34:12 +0000
math: true
---
{% raw %}

- Màximos y mínimos locales

	- [Teoremas de valores intermedios](http://tallermatematic.eu/wp/?p=547#intermedios)

	- [Concavidad y convexidad](http://tallermatematic.eu/wp/?p=547#concavidad)

	- [Fórmula de Taylor](http://tallermatematic.eu/wp/?p=547#taylor)

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)
## Máximos y mínimos locales

**Definición 1**: La función $f:A\rightarrow\mathbb{R}$ tiene un máximo local en el punto $a\in A$ si existe un entorno $B(a,r)$ con $r&gt;0$ tal que $f(x)\leq f(a)$ para todo $x\in B(a,r)$. De forma similar, la función $f:A\rightarrow\mathbb{R}$ tiene un mínimo local en el punto $a\in A$ si existe un entorno $B(a,r)$ con $r&gt;0$ tal que $f(x)\geq f(a)$ para todo $x\in B(a,r)$
**Ejemplo 1**: la función $y=0.2x^4-1.8x^3+4.2x^2+0.2x-6$ presenta un máximo local en el punto $x=2.5$ (aproximadamente) y dos mínimos locales en los puntos $x=0$ y $x=4.3$:

![Máxximos y mínimos locales](/taller-matematicas/assets/images/maxims_i_minims_entorn-300x169.png) Máximos y mínimos locales
En la figura se ha trazado un entorno $B(x,r)$ del punto $x=0$  con un radio $r=0.5$, y para ese entorno se muestra, en líneas verticales tenues, los valores $f(x)$ para $x\in B(0,0.5)$. Se aprecia que $f(0)$ es menor (su valor es -6) que cualquier otro valor $f(x)$ del entorno, por tanto es un mínimo local. Claro que, con el gráfico no basta, hay que demostrarlo analíticamente, pero no suele ser fácil. Por ello, esperamos a ver los siguientes apartados.

El adjetivo "local" indica que el máximo o mínimo lo es sólo en un entorno, no en todo el dominio de la función. Por ejemplo, en la figura anterior tenemos un mínimo local entre $x=4$ y $x=5$, con un valor aproximado $y=-2$, pero el otro mínimo local en $x=0$ claramente tiene un valor inferior $y=-6$. De hecho este último mínimo es **global** (o **absoluto**) en el sentido de que no hay ningún otro valor $y(x)$ menor que -6 en todo el dominio de la función.

**Teorema 1**: Si $f(x)$ tiene un máximo o un mínimo local en el punto $x=a$, y la función es derivable en ese punto, entonces necesariamente la derivada en el punto es nula: $f'(a)=0$. La afirmación contraria no tiene porque ser cierta.
Gráficamente es fácil ver que es así:

![Rectas tangentes en los puntos máximos y mínimos](/taller-matematicas/assets/images/maxims_i_minims1-300x154.png) Rectas tangentes en los puntos máximos y mínimos
En cada uno de los máximos y mínimos, la recta tangente a la gráfica de la función és una recta horizontal (las tres líneas en rojo), o sea con pendiente nula; recordando que la pendiente de la recta tangente en un punto es precisamente la derivada de la función en ese punto, llegamos al teorema.

**Ejemplo 2**: Para la función del ejemplo 1, derivando, obtenemos $y'=0.8x^3-5.4x^2+8.4x+0.2$, igualando a cero y resolviendo la ecuación resultante (en este caso hay que hacerlo por métodos numéricos o gráficamente) obtenemos 0, 2.5 y 4.3. Cada uno de estos valores es candidato a ser un máximo o un mínimo local, pero aún no podemos asegurarlo.

**Ejemplo 3**: La función $y=x^3$ tiene derivada $y'=3x^2$ que se anula para $x=0$, pero esta función no tiene ni máximos ni mínimos locales. Simplemente sucede que la tangente a la gráfica en $x=0$ es horizontal:

![y= x³](/taller-matematicas/assets/images/x^3-300x127.png) Gráfica de la función y= x³, con tangente horizontal en x=0
## Teoremas de valores intermedios

Vemos algunos teoremas relativos a la relación entre derivadas y  valores de la función en un intervalo. No los demostramos aquí, sólo intentamos entenderlos y ver alguna aplicación práctica.

**Teorema 2 (de Rolle)**: Si $f:\lbrack a,b\rbrack\rightarrow\mathbb{R}$ es derivable (y por tanto continua) y además $f(a)=f(b)$, entonces existe al menos un punto intermedio $c\in\lbrack a,b\rbrack$ tal que la derivada en ese punto se anula, $f'(c)=0$. 

![Ejemplo del teorema de Rolle](/taller-matematicas/assets/images/T-Rolle1.png) Ejemplo del teorema de Rolle
**Ejemplo 4**: la función $y=x^2-4x-2$ toma el mismo valor $y=1$ (recta horizontal amarilla) en los extremos del intervalo $\lbrack a,b\rbrack=\lbrack2-\sqrt2,2+\sqrt2\rbrack$. Como $y=f(x)$ es derivable, debe de haber al menos un punto intermedio entre $2-\sqrt2$ y $2+\sqrt2$ tal que la tangente a la gráfica sea horizontal; ese punto en este caso es único, y es $x=2$ (con recta tangente y=4, en rojo).

Intuitivamente, si la gráfica debe de pasar por la misma altura y en los dos puntos $(a,b)$ y la función no es constante (una recta horizontal) entonces en algún punto intermedio deberá ser horizontal, de otro modo, si siempre es $f'(x)&gt;0$, entonces será siempre creciente  y $f(b)&gt;f(a)$, si $f'(x)&lt;0$, entonces será siempre decreciente  y $f(b)&lt;f(a)$, y si es creciente y decreciente al mismo tiempo, entonces por ser una función contínua en algún lugar ha de haber una transición en el cambio de signo de la derivada de menos a más o al revés, esto es, un lugar con derivada cero.

**Teorema 3 del incremento finito, o del valor medio (Lagrange)**: Si $f:\lbrack a,b\rbrack\rightarrow\mathbb{R}$ es derivable en $(a,b)$ y continua en $\lbrack a,b\rbrack$, entonces existe al menos un punto intermedio $c\in(a,b)$ tal que $f'(c)=\frac{f(b)-f(a)}{b-a}$.

**Ejemplo 5**: La función $-\left(\frac x4-2\right)^2+4$ es continua en todo $\mathbb{R}$; en particular si nos fijamos en el intervalo $\lbrack 2,8\rbrack$ y calculamos el cociente $\frac{f(b)-f(a)}{b-a}=\frac{4-1.75}{8-2}=0.375$, el teorema nos asegura que debe existir un punto intermedio $c$ tal que $f'(c)=0.375$. en efecto, derivando, $f'(x) = 1-\fracx8$, igualamos: $1-\frac x8=0.375\Leftrightarrow x=5$, el punto intermedio es $c=5$.

![Teorema del incremento finito](/taller-matematicas/assets/images/incremento_finito_bo-300x227.png) Teorema del incremento finito
La interpretación geométrica es la siguiente: dado el triángulo de lados $(a,b)$ y $(f(a),f(b)$ con longitudes $b-a$ y $f(b)-f(a)$, el cociente $\frac{f(b)-f(a)}{b-a}$ nos da la tangente del ángulo $\theta$ del triángulo (ver la figura). El teorema afirma que existe el punto c tal que la tangente a la gráfica en ese punto tiene una pendiente que también es $\theta$, o lo que es lo mismo, la tangente en c es paralela a la hipotenusa del triángulo. También lo podemos ver así: dado el triángulo, existirá alguna recta tangente paralela a la hipotenusa del triángulo.

**Aplicación práctica: crecimiento y decrecimiento**

Como aplicación práctica de este teorema, si una función tiene derivada positiva $f'(x)&gt;0$ en todo el intervalo $(a,b)$, siendo $b-a&gt;0$, tendremos que $f'(c)&gt;0\Rightarrow\frac{f(b)-f(a)}{b-a}&gt;0\Rightarrow f(b)-f(a)&gt;0\Rightarrow f(b)&gt;f(a)$, o sea que la función es creciente en ese intervalo. Por el contrario, si $f'(x)&lt;0$ en todo el intervalo $(a,b)$ entonces la función será decreciente en ese intervalo. Por último si  $f'(x)=0$ en todo el intervalo $(a,b)$ entonces la función es constante en ese intervalo.

**Ejemplo
 6**: La función del ejemplo 5, $-\left(\frac x4-2\right)^2+4$, tiene por derivada $f'(x) = 1-\fracx8$, que es mayor que cero en el intervalo $\left(-\infty,8\right)$, cero en el punto $x=8$ y menor que cero en el intervalo $\left(8,+\infty\right)$ es creciente en $\left(-\infty,8\right)$ y decreciente en $\left(-\infty,8\right)$. En el punto $x=8$ de derivada nula tiene claramente un máximo.

![Crecimiento y decrecimiento](/taller-matematicas/assets/images/incremento_finito1-300x297.png) Crecimiento y decrecimiento

**Teorema 4 del valor medio (Cauchy)**

Si la funciones $f,g:\lbrack a,b\rbrack\rightarrow\mathbb{R}$ son derivables en $(a,b)$ y continuas en $\lbrack a,b\rbrack$, entonces existe al menos un punto intermedio $c\in(a,b)$ tal que$\left(f(b)-f(a)\right)g'(c)=\left(g(b)-g(a)\right)f'(c)$ La interpretación geométrica no es es de ayuda en este caso; todo lo que podemos hacer para ver que nos está diciendo este teorema es relacionarlo con el del incremento finito: para cada una de las funciones $f,g$ es teorema del incremento finito asegura que existen puntos $c_1, c_2$ tales que:

$\begin{array}{l}\frac{f(b)-f(a)}{b-a}=f'(c_1)\\\frac{g(b)-g(a)}{b-a}=g'(c_2)\end{array}$

dividiendo las dos expresiones (suponiendo que $g(b)-g(a)$ no es cero) obtenemos:

$\frac{f(b)-f(a)}{g(b)-g(a)}=\frac{f'(c_1)}{g'(c_2)}\Leftrightarrow\left(f(b)-f(a)\right)g'(c_2)=\left(g(b)-g(a)\right)f'(c_1)$

que es casi lo que nos dice el teorema de Cauchy, añadiendo además que $c_1=c_2=c$: existe al menos un punto $c$ que lo cumple. De hecho, en el caso especial de que $g(x)=x$, este teorema se reduce al del incremento finito de Lagrange.

**Aplicación práctica:  regla de l'Hôpital para el cálculo de límites**
En el teorema de Cauchy si consideramos que f(a)=g(a)=0 y llmamos $b=x$ obtenemos la igualdad $\frac{f(x)}{g(x)}=\frac{f'(c)}{g'(c)}$, donde $0&lt;c&lt;x$. Hagamos el límite $\\lim_{x\rightarrow b}$,  nos queda  $\lim_{x\rightarrowb}\frac{f(x)}{g(x)}=\lim_{x\rightarrowb}\frac{f'(x)}{g'(x)}$, pues cuando $x\rightarrow b$ el punto $c$  intermedio tenderá también con $x$ a $b$. El límite $\lim_{x\rightarrow0}\frac{f(x)}{g(x)}=\frac00$ es indeterminado, pero vemos que, si existe, será igual al límite $\lim_{x\rightarrow0}\frac{f'(x)}{g'(x)}$, que puede usarse para resolver la indeterminación. La regla tambien puede usarse para el caso $\lim_{x\rightarrow b}f(x)=\lim_{x\rightarrow b}g(x)=\infty$ que produce otro límite indeterminado $\lim_{x\rightarrow b}\frac{f(x)}{g(x)}=\frac\infty\infty$:

**Teorema 5 (Regla de l'Hôpital)**: El límite $\lim_{x\rightarrowb}\frac{f(x)}{g(x)}=\frac00=L$ es igual al límite $\lim_{x\rightarrowb}\frac{f'(x)}{g'(x)}=L$ siempre que este último límite exista, que $f,g$ sean derivables en $x=b$, y con valores $f(b)=g(b)=0$. El límite $\lim_{x\rightarrowb}\frac{f(x)}{g(x)}=\frac\infty\infty=L$ es igual al límite $\lim_{x\rightarrowb}\frac{f'(x)}{g'(x)}=L$  siempre que este último límite exista, y que $f,g$ sean derivables. 
**Ejemplo 8**: $\lim_{x\rightarrow1}\frac{x^2-1}{x^2+x-2}=\frac00$, como las funciones del numerador y del denominador son ambas derivables con valor cero en $x=1$, podemos aplicar L'Hôpital, derivando: $\lim_{x\rightarrow1}\frac{x^2-1}{x^2+x-2}=\lim_{x\rightarrow1}\frac{2x}{2x+1}=\frac23.$

**Ejemplo 9**: $\lim_{x\rightarrow0}\frac{\tan\left(x\right)}{1/x}=\frac\infty\infty.$ Aplicamos L'Hôpital:

$\lim_{x\rightarrow0}\frac{\tan\left(x\right)}{1/x}=\frac\infty\infty=\lim_{x\rightarrow0}\frac{\displaystyle\frac1{\cos^2\left(x\right)}}{\displaystyle\frac{-1}{x^2}}=\lim_{x\rightarrow0}\frac{-x^2}{\cos^2\left(x\right)}=\frac01=0.$

### Concavidad y convexidad

![Función convexa: las rectas secantes quedan por encima de la gráfica](/taller-matematicas/assets/images/secant-300x231.png) Función convexa: las rectas secantes quedan por encima de la gráfica
Dada una función continua y un intervalo $x\in(a,b)$ definimos la **recta secante** como la recta que pasa por los puntos $P=(a,f(a)), Q=(b,f(b))$. En la imagen anterior, $a=1, f(a)=1, b=4, f(b)=4$, la recta secante está en rojo, la función es $f(x)=(x-2)^2$. La ecuación de la recta secante es:

$y=\frac{f(b)-f(a)}{b-a}\left(x-a\right)+f(a)$

En la imagen anterior, $y=\frac{4-1}{4-1}\left(x-1\right)+1=x.$ En lo que sigue, nos referiremos a la recta secante a $f(x)$ por $(a,b)$ como $r_s(a,b)$.

**Definición 2**: Diremos que **$f(x)$ es** **convexa en $(a,b)$** si para todo $x\in(a,b)$ se cumple que $f(x)&lt;r_s(a,b)$, o equivalentemente, usando la  expresión de la recta secante, si:
$\frac{f(x)-f(a)}{x-a}&lt;\frac{f(b)-f(a)}{b-a}$

Diremos que **$f(x)$ es cóncava en $(a,b)$** si para todo $x\in(a,b)$ se cumple que $f(x)&gt;r_s(a,b)$, o equivalentemente, usando la  expresión de la recta secante, si:
$\frac{f(x)-f(a)}{x-a}&gt;\frac{f(b)-f(a)}{b-a}$

![Función cóncava: la recta secante queda por debajo de la gráfica.](/taller-matematicas/assets/images/concava.png) Función cóncava: la recta secante queda por debajo de la gráfica.
Equivalentemente, podemos definir la concavidad y la convexidad mediante la recta tangente:

**Definición 2b**: Diremos que $f(x)$ es convexa en $(a,b)$ si para todo $x\in(a,b)$ se cumple que la recta tangente a $f(x)$ queda por debajo de la gráfica de la función, y diremos que $f(x)$ es cóncava en $(a,b)$ si la recta tangente a $f(x)$ queda por encima de la gráfica de la función.

![recta_tangent_6](/taller-matematicas/assets/images/recta_tangent_6.png) Función cóncava: la recta tangente queda por encima de la gráfica

La definición es intuitivamente clara, se puede visualizar fácilmente, pero es poco operativa en los problemas. Veamos una propiedad que nos permite calcular la convexidad o concavidad de una función.

**Proposición 1**: Si $f(x)$ es derivable dos veces en $(a,b)$ y la derivada segunda $f''(x)&gt;0$ en en $(a,b)$, entonces la función es convexa en $(a,b)$.
**Ejemplo 10**: La función $y=x^2$ tiene derivada segunda $y''=2&gt;0$ por lo que es convexa en todo $\mathbb{R}.$

**Ejemplo 11**: La función $f(x)=\sin\left(x\right)$ tiene derivada segunda $f''(x)=-\sin\left(x\right)$ que es mayor que cero en los intervalos $(\mathrm\pi,2\mathrm\pi),\left(3\mathrm\pi,4\mathrm\pi\right),\dots\left(\left(2\mathrm k+1\right)\mathrm\pi,\left(2\mathrm k+2\right)\mathrm\pi\right)\;\mathrm k=0,1,2,\cdots$, en todos esos intervalos la función es convexa.

**Definición 3**: El punto $x_0$ es un punto de inflexión de $f(x)$ si existe un intervalo que contiene ese punto, $a&lt;x_0&lt;b$, tal que o bien f(x) es cóncava en $(a,x_0)$ y convexa en $(x_0, b)$, o bien  f(x) es convexa en $(a,x_0)$ y cóncava en $(x_0, b)$
**Ejemplo 12**: $y=x^3$ tiene por derivada $y'=3x^2$ y por derivada segunda $y''=6x$, que es menor que cero para $x&lt;0$, luego es cóncava para esos valores, mientras que para $x&gt;0$ la derivada segunda es positiva, luego la función es convexa. En el punto $x_0=0$ cualquier intervalo $a&lt;0&lt;b$ cumplirá que la función es cóncava para $(a,0)$ y convexa para $(0,b$), luego $x_0=0$ es un punto de inflexión.

![y= x³](/taller-matematicas/assets/images/x^3-300x127.png) y= x³ es cóncava para x0

**Propiedades de las funciones convexas (o cóncavas)**

	- Si $f(x)$ es convexa, entonces
 $-f(x)$ es cóncava, y viceversa.

	- Si $f(x)$ es convexa o es cóncava, entonces es continua

	- Si una función es cóncava en un intervalo, y en ese intervalo tiene un máximo local en $x_0$, entonces en $x_0$ hay un máximo absoluto.

	- Si una función es convexa en un intervalo, y en ese intervalo tiene un mínimo local en $x_0$, entonces en $x_0$ hay un mínimo absoluto.

**Ejemplo 13**:

	- La función $f(x)=x^2$ hemos visto que es convexa en todo $\mathbb{R}$ (ejemplo 10). Su derivada $f'(x)=2x$ se anula para $x=0$, para $x&lt;0$ es negativa (luego la función es decreciente en ese intervalo) y para $x&gt;0$ es positiva (luego la función es creciente en ese intervalo): en $x=0$ tenemos un mínimo local. Como la función es convexa, el mínimo es absoluto.

	- Como $f(x)=x^2$ es convexa, $g(x)=-f(x)=-x^2$ es cóncava en todo $\mathbb{R}$. Con un razonamiento similar al anterior, veremos que en $x=0$ hay un máximo local y también global de $g(x)$.

### Fórmula de Taylor

**Aproximación local usando la tangente**

En el post [Funciones derivables](http://tallermatematic.eu/wp/?p=461) ya vimos una introducción al estudio local de una función, decíamos que la derivada nos daba una estimación de la variación local de la función. Esto implica que la recta tangente en un punto a la gráfica de la función tendrá localmente la misma variación que la función: será una aproximación local. Por ejemplo la función $y=exp(x/3)*sin(x)$ tiene por derivada $y'=1/3 e^(x/3) (sin(x)+3 cos(x))$, en el punto $x_0=3$ la derivada vale aproximadamente -2.56, y la recta tangente en ese punto es $y=-2.56x+8.1$, gráficamente:

![Aproximación local de una función por la tangente](/taller-matematicas/assets/images/aprox_local_1-247x300.png) Aproximación local de una función por la tangente
Vemos que en las inmediaciones de $x_0=3$ la tangente coincide (aproxima) a la función; al ser la expresión de la tangente más simple que la de la función, estamos simplificando el cálculo de valores; esto tiene diversas aplicaciones prácticas.

**Aproximación local usando un polinomio de grado 2**

Nos preguntamos ahora: ¿podemos mejorar la aproximación local de forma que el entorno de aplicación sea más amplio, y sea buena también para funciones más complicadas? Se puede: en vez de la tangente, que es una función lineal, usamos una función cuadrática, esto es, una parábola $y=ax^2+bx+c$:

![Aproximación local de segundo orden](/taller-matematicas/assets/images/Taylor_ordre_2-300x266.png) Aproximación local por función cuadrática
Vemos que el ajuste de la función (en negro) por la parábola (en rojo) cerca del punto $x=3$ ha mejorado respecto a la aproximación por la tangente. Los coeficientes de la función cuadrática vienen dados por la siguiente definición.

**Definición 4: Polinomio de Taylor**
Si la función $f(x)$ es n veces derivable en un punto $a$ de su dominio, definimos el **polinomio de Taylor de grado n** de $f(x)$ en $a$ como:

$P_n\left(x\right)=f(a)+\frac{f'\left(a\right)}{1!}\left(x-a\right)+\frac{f''\left(a\right)}{2!}\left(x-a\right)^2+\dots+\frac{f^n\left(a\right)}{n!}\left(x-a\right)^n.$

**Ejemplo 14**: Obtendremos el $P_4(x)$ para $f(x)=sin(x)$ en el punto $a=0$, primero calculamos las derivadas:

$\begin{array}{l}f'(x)=cos(x);f'(0)=cos(0)=1;\\f''(x)=-\sin(x);f''(0)=-\sin(0)=0;\\f^3(x)=-\cos(x);f^3(0)=-\cos(0)=-1;\\f^4(x)=\sin(x);\;f^4(0)=\sin(0)=0.\end{array}$

Sustituimos en la fórmula y simplificamos:

$\begin{array}{l}P_4\left(x\right)=0+1\cdot\left(x-0\right)+\frac0{2!}\left(x-0\right)^2-\frac1{3!}\left(x-0\right)^3+\frac0{4!}\left(x-0\right)^4=\\x-\frac{x^3}6.\end{array}$

Este polinomio aproxima localmente a la función $f(x)=sin(x)$ cerca del punto $a=0$; como hemos usado hasta la cuarta derivada, la aproximación se llama de orden 4. ¿Hasta que punto es buena la aproximación? El siguiente teorema nos da la respuesta.

**Teorema 7 (fórmula de Taylor)**: Si la función $f(x)$ es n veces derivable en un cierto intervalo $\left$a,b\right$$, y la derivada n-ésima $f^n(x)$ es continua en $\left$a,b\right$$, entonces para todo $x\in\left(a,b\right)$ se cumple que$f(x)=P_n(x)+\varepsilon(x)$donde $P_n(x)$ es el polinomio de Taylor de grado n que aproxima localmente a $f(x)$ en el punto $c\in\left(a,b\right)$, y $\varepsilon(x)$ se denomina término de error (o residuo de Lagrange):$\varepsilon_n(x)=\frac{f^{n+1}(d)}{\left(n+1\right)!}\left(x-c\right)^{n+1}$con $d\in\left(a,c\right).$
**Ejemplo 15**: Para el polinomio $P_4(x)$ para $f(x)=sin(x)$ en el punto $a=0$,el residuo es:

$\varepsilon_4(x)=\frac{f^{4+1}(d)}{\left(4+1\right)!}\left(x-0\right)^{4+1}=\frac{f^5(d)}{5!}\left(x\right)^5=\frac{\cos\left(d\right)}{120}x^5$

para algun $d\in\left(0,x\right)$. Por ejemplo para $x=0.1$ valdrá $\varepsilon_4(0.1)=\frac{\cos\left(d\right)}{120}0.1^5=8.3\cdot10^{-8}\cos\left(d\right)$, teniendo en cuenta que la función seno toma el valor máximo para $d=0$, podemos acotar el error: $\varepsilon_4(0.1)=8.3\cdot10^{-8}\cos\left(d\right)\leq8.3\cdot10^{-8}\cos\left(0\right)=8.3\cdot10^{-8}.$

**Aplicación del teorema de Taylor al cálculo de máximos y mínimos relativos**

Supongamos que $f(x)$ es derivable *n* veces en el punto *a*, y que las primeras *n-1* derivadas en ese punto son cero,  $f'(a)=f''(a)=\cdots=f^{n-1}(a)=0$ pero la n-ésima no lo es, $f^n(x)\neq0$. Entonces, por la fórmula de Taylor:

$\begin{array}{l}f\left(x\right)=f(a)+\frac{f'\left(a\right)}{1!}\left(x-a\right)+\frac{f''\left(a\right)}{2!}\left(x-a\right)^2+\dots+\frac{f^n\left(a\right)}{n!}\left(x-a\right)^n+\varepsilon_n\left(x\right)\\=f(a)+0+0+\dots+\frac{f^n\left(a\right)}{n!}\left(x-a\right)^n+\varepsilon_n\left(x\right)\Leftrightarrow\\\frac{f\left(x\right)-f(a)}{\left(x-a\right)^n}=\frac{f^n\left(a\right)}{n!}+\frac{\varepsilon_n\left(x\right)}{\left(x-a\right)^n}\end{array}$

Tenemos la siguiente propiedad, que no demostramos:

***Proposición 1**: $\lim_{x\rightarrow a}\frac{\varepsilon_n\left(x\right)}{\left(x-a\right)^n}=0$*

Entonces, si nos acercamos suficientemente al punto *a*, tendremos que $\frac{f\left(x\right)-f(a)}{\left(x-a\right)^n}\approx\frac{f^n\left(a\right)}{n!}\Leftrightarrow f\left(x\right)\approx f(a)+\frac{f^n\left(a\right)}{n!}\left(x-a\right)^n$ en un entorno de *a*. Nos fijamos ahora en el signo del término $\frac{f^n\left(a\right)}{n!}\left(x-a\right)^n$ para lelgar a la siguiente conclusión:

**Regla 1: determinar máximos y mínimos locales**

	- *Si $f^n(a)&gt;0$ y n es par, entonces $f(x)&gt;f(a)$ en un entorno de a: la función tiene un mínimo relativo en a.*

	- *Si $f^n(a)&lt;0$ y n es par, entonces $f(x)&lt;f(a)$ en un entorno de a: la función tiene un máximo relativo en a.*

	- *Si n es impar, entonces el signo de $(x-a)^n$ cambia según si nos acercamos al punto a por la derecha o por la izquierda, y no tenemos ni mínimo ni máximo.*

**Ejemplo 16**: la función del ejemplo 1, $y=0.2x^4-1.8x^3+4.2x^2+0.2x-6$, tiene la  primera derivada $y'=0.8x^3-5.4x^2+8.4x+0.2$ , los puntos 0, 2.5 y 4.3 verifican que $y'=0$; la segunda derivada es $y''(x)=2.4x^2-10.8x+8.4$ y sus valores en los puntos anteriores son $y''(0)=8.4&gt;0, y''(2.5)=-3.6&lt;0, y''(4.3)=6.3&gt;0$, por tanto, la regla anterior nos asegura que hay mínimos locales en $x=0, x=4.3$ y máximo local en $x=2.5,$ como ya habíamos anticipado. En un entorno del punto $a=0$ tendremos que podemos
 aproximar la función por una parábola:

$\begin{array}{l}f\left(x\right)\approx f(a)+\frac{f^n\left(a\right)}{n!}\left(x-a\right)^n=f(0)+\frac{f^n\left(0\right)}{2!}\left(x-0\right)^2\\=-6+\frac{8.4}2x^2=-6+4.2x^2\end{array}$

por ejemplo, para $x=0.1$, calculando: $f\left(0.1\right)=-6+4.2\cdot0.1^2=-5.9580,$ el valor exacto es $f(0.1)=-5.9598$, el valor aproximado difiere del real en milésimas.

**Aplicación del teorema de Taylor a la determinación de la concavidad y convexidad**

Supongamos ahora que $f'(a)\neq0,\;f''(a)=f'''(a)=\dots=f^{\left(n-1\right)}(a)=0,\;f^{\left(n\right)}(a)\neq0.$ Entonces por la fórmula de Taylor:

$\begin{array}{l}f\left(x\right)=f(a)+\frac{f'\left(a\right)}{1!}\left(x-a\right)+\frac{f''\left(a\right)}{2!}\left(x-a\right)^2+\dots+\frac{f^n\left(a\right)}{n!}\left(x-a\right)^n+\varepsilon_n\left(x\right)\\=f(a)+f'\left(a\right)\left(x-a\right)+\frac{f^n\left(a\right)}{n!}\left(x-a\right)^n+\varepsilon_n\left(x\right)\\=r_t\left(a\right)+\frac{f^n\left(a\right)}{n!}\left(x-a\right)^n+\varepsilon_n\left(x\right)\end{array}$

donde $r_t(a)$ es la recta tangente a $f(x)$ en el punto $x=a$ (ver [Funciones derivables](http://tallermatematic.eu/wp/?p=461), apartado Recta tangente en un punto a la gráfica de $y=f(x)$). Entonces $f(x)-r_t(a)=\frac{f^{\left(n\right)}\left(a\right)}{n!}(x-a)^n$ en un entorno de$x=a$. Recordando la definición 2b de concavidad y convexidad, llegamos a la siguiente regla:

**Regla 2: determinar concavidad y convexidad**

	- Si $f^{(n)}(a)&gt;0$ y *n* es par, entonces $f(x)&gt;r_t(x)$ y la función es convexa en un entorno de *a*

	- Si $f^{(n)}(a)&lt;0$ y *n* es par, entonces $f(x)&lt;r_t(x)$ y la función es cóncava en un entorno de *a*

	- Si  *n* es impar, entonces el signo de $f(x)-r_t(x)$ varia según si nos acercamos a a por la izquierda o por la derecha: en a hay un punto de inflexión

**Ejemplo 17**: Consideremos la función $f(x)=\frac{x^2+1}{x^2-4}$ definida en $x\in\mathbb{R}-\left\{-2,+2\right\}.$ Derivamos:

$\begin{array}{l}f'(x)=\frac{D\left(x^2+1\right)\cdot\left(x^2-4\right)-\left(x^2+1\right)\cdot D\left(x^2-4\right)}{\left(x^2-4\right)^2}\\=\frac{\left(2x\right)\cdot\left(x^2-4\right)-\left(x^2+1\right)\cdot2x}{\left(x^2-4\right)^2}=\frac{-10x}{\left(x^2-4\right)^2}\end{array}$

$\begin{array}{l}f''(x)=\frac{D\left(-10x\right)\cdot\left(x^2-4\right)^2-\left(-10x\right)\cdot D\left(x^2-4\right)^2}{\left(x^2-4\right)^4}\\=\frac{\left(-10\right)\cdot\left(x^2-4\right)^2+10x\cdot2\left(x^2-4\right)\cdot2x}{\left(x^2-4\right)^4}=\frac{30x^4-80x^2-160}{\left(x^2-4\right)^4}\end{array}$

¿En qué puntos se anula $f'(x)$? Sólo en uno: $\frac{-10x}{\left(x^2-4\right)^2}=0\Leftrightarrow x=0.$ ¿En qué puntos se anula $f''(x)$?

$\begin{array}{l}\frac{30x^4-80x^2-160}{\left(x^2-4\right)^4}=0\Leftrightarrow30x^4-80x^2-160=0\Leftrightarrow3\left(x^2\right)^2-8\left(x^2\right)-16=0\\\Leftrightarrow x^2=\frac{8\pm\sqrt{8^2+4\cdot3\cdot16}}6=\frac{8\pm16}6=\left\{\begin{array}{l}4\Rightarrow x=\pm2\\-8/6\Rightarrow x\not\in\mathbb{R}\end{array}\right.\end{array}$

En $x=0$ tenemos $f(0)=-1/4, f'(0)=0, f''(0)=-5/8&lt;0$; por la regla 1, siendo $n=2$ (par) y $f^{n}(0)&lt;0$ tendremos un máximo local en $x=0$.

En los puntos $x\neq0$ tenemos que $f(x)\neq0, f'(x)\neq0$; si $x\not\in\left\{\pm\2\right\}$ entonces $f''(x)\neq0$, aplicando la regla 2, tomando $n=2$, que es par, tendremos que en los puntos donde $f''(x)&gt;0$ la función será convexa, y en donde $f''(x)&lt;0$ la función será cóncava:

Convexidad: $\begin{array}{l}\frac{30x^4-80x^2-160}{\left(x^2-4\right)^4}&gt;0\Leftrightarrow3\left(x^2\right)^2-8\left(x^2\right)-16&gt;0\\\Leftrightarrow x^2&gt;4\Leftrightarrow x&lt;-2,\;x&gt;2\end{array}$

Concavidad: $\begin{array}{l}\frac{30x^4-80x^2-160}{\left(x^2-4\right)^4}&lt;0\Leftrightarrow3\left(x^2\right)^2-8\left(x^2\right)-16&lt;0\\\Leftrightarrow x^2&lt;4\Leftrightarrow-2&lt;x&lt;2\end{array}$

En los puntos en que se anula $f''(x)$ tenemos $f'(\pm2)=-\frac{10\cdot\left(\pm2\right)}{\left(4-4\right)^2}=\infty$, de hecho la función no está definida en esos puntos.

La gráfica de la función es:

![save (2)](/taller-matematicas/assets/images/save-2.png)
{% endraw %}