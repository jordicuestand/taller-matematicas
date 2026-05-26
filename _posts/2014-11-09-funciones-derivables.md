---
layout: post
title: "Funciones derivables"
date: 2014-11-09 20:44:40 +0000
categories:
  - "Uncategorized"
math: true
---
{% raw %}

## Introducción al estudio local de una función

El estudio de la variación de los valores que toma una función en las proximidades de un punto $x$ es un tema de gran interés práctico por sus posibles aplicaciones, como por ejemplo:

- Si $f(x)$ es la función que nos proporciona la posición de un objeto en movimiento, entonces la variación de los valores de la función cerca de $x=a$ con respecto al tiempo nos informa de la velocidad del objeto en las inmediaciones de $x=a$.

- Si $f(x)$ es el [perfil topográfico](http://en.wikipedia.org/wiki/File:Courbe_niveau.svg) de una colina, la variación local del perfil nos informa de la pendiente de la colina en ese punto.

- Si $f(x)$ es la intensidad de corriente que circula por un aparato eléctrico en un cierto instante de tiempo, su variación alrededor de ese instante se interpreta como la poténcia eléctrica consumida.

![](/assets/images/variacio_local-300x226.png)Variación de la función y=x³ al pasar del punto a al punto x

En la figura podemos observar que la variación de la función al pasar del punto $x$ al punto $a$ es $f(x)-f(a)$. Entonces, el cociente $\frac{f(x)-f(a)}{x-a}$ nos proporciona un valor promedio de la variación de la función en el intervalo $(a,x)$. Observemos además que podemos formar un triángulo recto tomando como lados los segmentos  $f(x)-f(a)$ y  $x-a:$

[![Relación entre pendiente y ángulo](/assets/images/Tan-300x233.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/10/Tan.png)Relación entre pendiente y ángulo

En este triángulo se cumple que $\tan\left(A\right)=\frac{f(x)-f(a)}{x-a}$.

## Pendiente de una función en un punto. Definición de función derivada.

Podemos escribir la fórmula del incremento medio de la función en términos más generales, usando puntos genéricos i el operador incremento $\nabla$:

$\frac{f(x_2)-f(x_1)}{x_2-x_1}=\frac{y_2-y_1}{x_2-x_1}=\frac{\nabla y}{\nabla x}.$

En una función lineal $f(x)=ax+b$, la pendiente es constante, y por tanto el incremento medio de la función es constante en todos los puntos y para cualquier intervalo:

$\frac{f(x_2)-f(x_1)}{x_2-x_1}=\frac{\left(ax_2+b\right)-\left(ax_1+b\right)}{x_2-x_1}=\frac{a\left(x_2-x_1\right)}{x_2-x_1}=a.$

Para una función no lineal, la pendiente es diferente en cada punto, y  el incremento medio de la función depende de la longitud del intervalo $(x_1,x_2)$ y de los propios puntos $x_2,x_1$. Por ejemplo, en la función $y=x^3$, para el punto $x_1=1$ y el punto  $x_2=2$, la pendiente media del intervalo$(x_1,x_2)$ es $\frac{2^3-1^3}{2-1}=7$, mientras que para el intervalo $(1,1.5)$ es $\frac{1.5^3-1^3}{1.5-1}=4.75$.

Entonces, si nos interesa la pendiente de una función cualquiera en un punto, para una función lineal no hay problema, pero para una función no lineal, el incremento medio de la función no nos sirve, ya que depende de la longitud del intervalo que consideremos. La definición de derivada de la función en un punto soluciona el problema.

**Definición 1**: Derivada de una función en un punto. Función derivable.

Sea la función $f:A\rightarrow\mathbb{R}$ definida en el conjunto abierto $A$. Si existe el límite $L=\lim_{x\rightarrow a}\frac{f\left(x\right)-f\left(a\right)}{x-a}$ y es finito, entonces decimos que la función es derivable en $x=a$, y que su derivada en el punto $a$ es $L$. 

La notación usual para la derivada en un punto es $f'(a)$. La derivada de una función en un punto es un número que nos proporciona una medida de la variación local de la función en ese punto. Concretamente, no de la variación absoluta $\nabla y=f(x_2)-f(x_1)$, sino de la variación de la función relativa a la variación de la variable, o ratio de variación $\frac{\nabla y}{\nabla x}=\frac{f(x_2)-f(x_1)}{x_2-x_1}.$

**Ejemplo 1**

Sea la función $y=x^2$. En los puntos $x_1=1, x_2=3$ toma los valores $y_1=1, y_2=9$. La variación absoluta media en ese intervalo es $\nabla y=9-1=8$, la variación en $x$ es $\nabla x=3-1=2$, y la ratio de variación es $\frac{\nabla y}{\nabla x}=8/2=4$. Dependiendo de la función y de los puntos considerados,  la ratio de variación puede ser positiva, negativa o nula.

Por otro lado, la derivada de la función en el punto $a=1$ es el límite de la ratio de variación entre ese punto y los puntos $x$ cercanos:

$\lim_{x\rightarrow1}\frac{x^2-1^2}{x-1}=\lim_{x\rightarrow1}\frac{\left(x-1\right)\left(x+1\right)}{x-1}=\lim_{x\rightarrow1}\left(x+1\right)=2.$

De la misma forma, para el punto $a=6$:

$\lim_{x\rightarrow3}\frac{x^2-3^2}{x-3}=\lim_{x\rightarrow1}\frac{\left(x-3\right)\left(x+3\right)}{x-3}=\lim_{x\rightarrow3}\left(x+3\right)=6.$ Vemos que el valor de la ratio de variación media, 4, está entre los valores de la derivada en cada punto: 2 y 6.

**Definición 2**:  Función derivada.

Si la derivada $f'(a)$ existe en todo punto del dominio $A$ de la función, decimos que la función es derivable (en su dominio), y definimos la función derivada $f'(x)$ de tal forma que asigna a cada $a$ de $A$ el valor $f'(a)$. 

**Ejemplo 2**: para la función $y=x^3$ con dominio todos los números reales, dado un punto cualquiera $a$, aplicando la definición:

$L=\lim_{x\rightarrow a}\frac{f\left(x\right)-f\left(a\right)}{x-a}=\lim_{x\rightarrow a}\frac{x^3-a^3}{x-a}=\lim_{x\rightarrow a}\frac00=?$

Para resolver la indeterminación, consideramos que $x=a+h$ siendo $h$ el incremento $x-a$; entonces el límite se transforma en:

$L=\lim_{x\rightarrow a}\frac{f\left(x\right)-f\left(a\right)}{x-a}=\lim_{h\rightarrow0}\frac{f\left(a+h\right)-f(a)}h.$

Este límite se utiliza frecuentemente como definición alternativa de derivada.  Operando:

$\begin{array}{l}\lim_{h\rightarrow0}\frac{f\left(a+h\right)-f(a)}h=\lim_{h\rightarrow0}\frac{\left(a+h\right)^3-a^3}h=\lim_{h\rightarrow0}\frac{h^3+3h^2a+3hx^2}h=\\\lim_{h\rightarrow0}\left(h^2+3ha+3x^2\right)=3x^2.\end{array}.$

Así pues, $f'(x)=3x^2$.

**Ejemplo 3**: La función

$f(x)=\left\{\begin{array}{l}+x\;\;\text{si }x\geq0\\-x\;\text{si }x&lt;0\end{array}\;\right.$

no es derivable en $x=0$ pues no existe el límite en ese punto, ya que los límites laterales no coinciden:

$\lim_{x\rightarrow0}f(0)=\left\{\begin{array}{l}\lim_{x\rightarrow0^+}\frac{f(x)-f(0)}x=\frac{x-0}x=1\;\\\lim_{x\rightarrow0^-}\frac{f(x)-f(0)}x=\frac{-x-0}x=-1\end{array}\;\right.$

[![Función no derivable en el origen: la pendiente en ese punto no está definida](/assets/images/no_derivable-300x230.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/10/no_derivable.png)Función no derivable en el origen: la pendiente en ese punto no está definida

**Ejemplo 4**: en un cierto punto de una carretera vemos una señal de tráfico que indica una pendiente del 10%. Sea $f(x)$ la función que proporciona el perfil de la carretera. ¿Cuál es el valor de la derivada en el punto considerado?

Usamos la relación entre pendiente y tangente del ángulo, tomando el límite:

$\tan\left(A\right)=\lim_{x\rightarrow a}\frac{f(x)-f(a)}{x-a}=f'(a)$

En topografía, a una pendiente del 100% le corresponde un ángulo de 45⁰; de hecho, la pendiente es precisamente la tangente del ángulo de inclinación en el punto (esto es, $\tan\left(45^0\right)=1$). Entonces:

$\tan\left(A\right)=\frac{10}{100}=f'(a)=0.1$

##  Propiedades de las derivadas

- Si $f(x)$ es derivable en $x=a$, entonces es contínua en ese punto. La afirmación inversa no tiene porque ser cierta: $\text{derivable}\begin{array}{c}\Rightarrow\\\nLeftarrow\end{array}\text{continua}.$

- Si $f, g$ son derivables, entonces también lo son $f+g, f-g, f·g, f/g$, en el último caso sólo para los puntos $x$ en los que $g(x) \neq 0$. Las derivadas son:

$(f+g)'=f'+g'$

- $(f-g)'=f'-g'$

- $(f·g)'=f'·g+f·g'$

- $\left(\frac fg\right)'=\frac{f'g-fg'}{g^2}$

**Ejemplo 5**: La derivada de $f(x)=Ax$ donde $A$ es un número real, es:

$\lim_{x\rightarrow a}\frac{f(x)-f(a)}{x-a}=\lim_{x\rightarrow a}\frac{Ax-Aa}{x-a}=\lim_{x\rightarrow a}\frac{x-a}{x-a}A=A.$

La derivada de $f(x)=Ax^2$ la calculamos usando la propiedad $(f·g)'=f'·g+f·g'$, y denotando por $Df(x)$ la derivada de $f(x)$:

$D\left(Ax^2\right)=D\left(Ax\cdot x\right)=D\left(Ax\right)\cdot x+Ax\cdot D(x)=A\cdot x+Ax\cdot1=2Ax$.

La derivada de $f(x)=Ax^n$ es $nAx^{n-1}$, como puede comprobarse por [inducción matemática](http://es.wikipedia.org/wiki/Inducci%C3%B3n_matem%C3%A1tica):

- Para n=1 es $f(x)=Ax$ y ya lo hemos comprobado: $f'(x)=Ax^0=A$

- Supongamos que es cierto para $n-1$; entonces para $n$:

$D(Ax^n)=D(Ax^{n-1}\cdot x)=D\left(Ax^{n-1}\right)\cdot x+Ax^{n-1}\cdot D(x)=\left(n-1\right)Ax^{n-2}\cdot x+Ax^{n-1}\cdot1=nAx^{n-1}.$

**Ejemplo 6**:  La derivada del polinomio de grado n $A_nx^n+A_{n-1}x^{n-1}+\dots+A_1x+A_0$ es el polinomio de grado n-1 $nA_nx^{n-1}+\left(n-1\right)A_{n-1}x^{n-2}+\dots+A_1.$ La comprobación se hace tomando la regla $D\left(Ax^n\right)=nAx^{n-1}$ y la propiedad $(f+g)'=f'+g'.$

**Ejemplo 7**: La derivada de la función $f(x)=\frac1{x^n}$ la calculamos aplicando la propiedad $\left(\frac fg\right)'=\frac{f'g-fg'}{g^2}:$

$D\left(\frac1{x^n}\right)=\frac{D\left(1\right)\cdot x^n-1\cdot D\left(x^n\right)}{\left(x^n\right)^2}=\frac{0\cdot x^n-1\cdot nx^{n-1}}{x^{2n}}=-\frac n{x^{2n-\left(n-1\right)}}=-\frac n{x^{n+1}}.$

##  Recta tangente en un punto a la gráfica de y=f(x)

| 
 

[![Recta tangente y recta secante a la gráfica de la función y=f(x)](/assets/images/recta_tangent.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/10/recta_tangent.png)Recta tangente y recta secante a la gráfica de la función y=f(x)

En la imágen vemos una curva, en negro, que es la gráfica de la función $y=\frac1{10}x^3$, y dos rectas que cortan a la gráfica en el punto P con coordenadas $x=3,y=f(3)=2.7$, de forma que las tres gráficas coinciden en el punto P. La recta en rojo $r_s$ además corta a la función $y=\frac1{10}x^3$ en otro punto, el $(0,0)$, mientras que la recta en amarillo $r_t$ sólo corta a  $y=\frac1{10}x^3$ en el punto P. Sin dar la definición formal, diremos que las rectas tales como la $r_s$ que cortan a la gràfica $y=f(x)$ en dos puntos son **rectas secantes** a $y=f(x)$, mientras que las rectas semejantes a $r_t$ que sólo "tocan"  la gráfica en un punto P son **rectas tangentes** a $y=f(x)$ en el punto P.

Admitiremos sin demostración la siguiente propiedad: *dado un punto P y una gráfica $y=f(x)$, hay infinitas rectas secantes que pasan por P pero sólo una recta tangente que pase por P*. Si llamamos Q al otro punto de la gràfica $y=f(x)$ cortada por la recta secante $r_s$ (en la figura Q seria el origen de coordenadas), y nos imaginamos que giramos la recta $r_s$ en torno al punto P, entonces el punto Q de intersección entre $y=f(x)$ y $r_s$ se va acercando al punto P, y en el límite, cuando P y Q coinciden, la recta secante $r_s$ se superpone a la recta tangente  $r_t$.

Nos preguntamos ahora ¿cómo podemos determinar la recta tangente a $y=f(x)$ en un punto cualquiera P con coordenadas $(x_0,y_0=f(x_0))$? La ecuación cartesiana de una recta cualquiera es $y=mx+b$ donde $m$ expresa la pendiente de la recta. En el ejemplo 4 vimos la relación entre pendiente, dada por un ángulo A, y derivada en el punto $a$:

$\tan\left(A\right)=\lim_{x\rightarrow a}\frac{f(x)-f(a)}{x-a}=f'(a)$

Así que, para la pendiente en un punto $x_0$, podemos decir que  es $m=f'(x_0)$; el valor del parámetro $b$, llamado intercepción (porque es la ordenada del punto de intersección de la recta con el eje de ordenadas) lo encontramos simplemente sustituyendo en la expresión de la función:

$y_0=m\cdot x_0+b\Rightarrow b=y_0-m\cdot x_0$

Nos queda la ecuación de la recta tangente a $y=f(x)$ en un punto cualquiera P con coordenadas $(x_0,y_0=f(x_0))$:

$y=mx+(y_0-m\cdot x_0)\;=f'(x_0)x+(y_0-f'(x_0)\cdot x_0)$

**Ejemplo** **8**: Encontremos la recta tangente $y=mx+b$ a la función $y=\frac1{10}x^3$ en la abcisa $x_0=3$ (corresponde a la anterior ilustración de esta apartado). Derivamos el [monomio](http://es.wikipedia.org/wiki/Monomio) según la regla dada en el ejemplo 5: $D(Ax^n)=an\cdot x^{n-1}$, lo aplicamos a la función dada: $D(\frac1{10}x^3)=\frac3{10}x^2$, sustituimos el valor $x_0=3$ resultando $m=\frac3{10}3^2=2.7$. Hallamos $b=y_0-m\cdot x_0=\frac1{10}3^3-2.7\cdot3=-5.4$, y la recta tangente tiene la ecuación $y=2.7x-5.4$, que en la ilustración está representada en color rojo.

**NOTA: sobre aproximación local de funciones y recta tangente**

[![Aproximación local a la función y=f(x) mediante su recta tangente](/assets/images/recta_tangent_21.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/10/recta_tangent_21.png)Aproximación local a la función y=f(x) mediante su recta tangente

Si en la imagen de la recta tangente "hacemos zoom" podemos observar que, en la inmediaciones del punto P de contacto, la gráfica de la función $y=f(x)$ y su recta tangente en ese punto prácticamente coinciden. Este es un hecho de gran importáncia práctica, pues nos permite usar, en un cierto entorno de P, la recta tangente en vez de la función original, que puede tener una expresión muy complicada, e incluso desconocida. Volveremos sobre ello más adelante, cuando estudiemos la fórmula de Taylor.

**Ejemplo 9**: La función de distribución Normal o de Gauss es

$y=\frac{e^{-{\displaystyle\frac{\left(x-\mu\right)^2}{2\sigma^2}}}}{\sqrt{2\pi}\sigma}$

donde $\mu, \sigma$ son parámetros. Sabiendo que, para los valores  $\mu=2,&nbsp;\sigma=1$, en el punto x=1 y(1) vale 0.2419707245 y su derivada también vale 0.2419707245, podemos encontrar fácilmente algunos de los valores de $f(x)$ usando la función tangente $y=f'(x_0)x+(y_0-m\cdot x_0)$, resultando $\begin{array}{l}y=f'\left(x_0\right)+\left(y_0-f'\left(x_0\right)\cdot x_0\right)=0.24197x+(0.24197-0.24197\cdot1)\Rightarrow\\y=0.24197x.\end{array}$.

Vemos que el cálculo de valores con la recta tangente es más simple. ¿Hasta qué punto es buena la aproximación? En la siguiente tabla de valores vemos los cálculos realizados con la función original, con la recta tangente, y el error relativo producido:

| **x** | **f(x)** | **recta tangente** | **error relativo** 
| 0.5 | 0.130 | 0.121 | 6.59% 
| 0.6 | 0.150 | 0.145 | 3.04% 
| 0.7 | 0.171 | 0.169 | 1.16% 
| 0.8 | 0.194 | 0.194 | 0.31% 
| 0.9 | 0.218 | 0.218 | 0.04% 
| 1 | 0.242 | 0.242 | 0.00% 
| 1.1 | 0.266 | 0.266 | 0.03% 
| 1.2 | 0.290 | 0.290 | 0.23% 
| 1.3 | 0.312 | 0.315 | 0.74% 
| 1.4 | 0.333 | 0.339 | 1.66% 
| 1.5 | 0.352 | 0.363 | 3.09% 

Observamos que, en el punto $x=1$ el error es cero, ya que en ese punto la función y la recta tangente coinciden totalmente. A medida que nos alejamos de ese punto, el error relativo va aumentando. En el intervalo mostrado, $[0.5, 1.5]$, el error no supera el 7%.

## Derivadas de funciones compuestas y funciones inversas

Hasta ahora para calcular derivadas solo tenemos la definición, que utiliza límites, y la regla de derivación de polinomios. Necesitamos herramientas más generales para trabajar con funciones cualesquiera. En este apartado y en el siguiente nos dedicamos a ello.

**Teorema 1 (regla de la cadena):** Si tenemos dos funciones $f, g$ tales que $f$ es derivable en el punto $x=a$, esto es, existe el límite  $L=\lim_{x\rightarrow a}\frac{f\left(x\right)-f\left(a\right)}{x-a}$, y además $g$ es derivable en el punto $y=f(a)$, entonces la  Funciones continuas" href="http://tallermatematic.eu/wp/?p=377/#FuncionCompuesta" target="_blank" rel="noopener">función compuesta $\left(g\circ f\right)\left(x\right)$ es también derivable en $x=a$, y su derivada vale:

$\left(g\circ f\right)'\left(a\right)=g'\left(f\left(a\right)\right)\cdot f'\left(a\right)=\left(g'\circ f\right)\left(a\right)\cdot f'\left(a\right)$

**Ejemplo 10:** Calcular la derivada de $y=\sin^3\left(x\right)$ usando la regla de la cadena, y sabiendo que la derivada de la función $sin(x)$ es la función $cos(x)$.

Definimos $g(x)=x^3, f(x)=sin(x)$, de forma que $\left(g\circ f\right)\left(x\right)=g\left(f\left(x\right)\right)=\left(\sin\left(x\right)\right)^3=\sin^3\left(x\right).$ Por la regla de la cadena:

$\begin{array}{l}\left(g\circ f\right)'\left(x\right)=g'\left(f\left(x\right)\right)\cdot f'\left(x\right);\\g'(x)=3x^2,\;f'\left(x\right)=\cos\left(x\right);\\g'\left(f\left(x\right)\right)=3\left(\sin\left(x\right)\right)^2=3\sin^2\left(x\right);\\D\sin^3\left(x\right)=3\sin^2\left(x\right)\cdot\cos\left(x\right).\end{array}$

**Ejemplo 11**: calcular la derivada de $f(x)=\frac1{\sin^2\left(x\right)}.$

Observemos que $f(x)=\frac1{x^2}\circ\sin\left(x\right)$, aplicamos la regla de la cadena :

$\begin{array}{l}\left(\frac1{x^2}\circ\sin\left(x\right)\right)'=\left(\frac1{x^2}\right)'\circ\sin\left(x\right)\cdot\left(\sin\left(x\right)\right)'=\\\left(\frac{-2}{x^3}\right)\circ\sin\left(x\right)\cdot\cos\left(x\right)=\\\frac{-2}{\sin^3\left(x\right)}\cdot\cos\left(x\right)=\frac{-2\cos\left(x\right)}{\sin^3\left(x\right)}.\end{array}$

La derivada del cociente $\frac1{x^2}$ puede obtenerse aplicando la propiedad $\left(\frac fg\right)'=\frac{f'g-fg'}{g^2}$, o bien de forma más directa haciendo $\frac1{x^2}=x^{-2}$ y aplicando la regla de derivación $Dx^n=nx^{n-1}$, o sea: $Dx^{-2}=-2x^{-2-1}=-2x^{-3}=-\frac2{x^3}.$

**Teorema 2 (derivada de la función inversa)**:

Si la función $f:A\rightarrow\mathbb{R}$ es inyectiva, $A$ es un intervalo, y la derivada de $f$ para cualquier punto $a$ de $A$ es diferente de cero, entonces la  Funciones continuas" href="http://tallermatematic.eu/wp/?p=377/#funcion_inversa" target="_blank" rel="noopener">función inversa es derivable en el punto $f(a)$, y su derivada es:

$\left(f^{-1}\right)'\left(x\right)=\frac1{f'\left(x\right)\circ f^{-1}\left(x\right)}$

**Ejemplo 12**: La función $f(x)=x^3$ es inyectiva (queda como ejercicio para el lector) y su inversa es $f^{-1}\left(x\right)=\sqrt[3]x$. Tenemos que $f'(x)=3x^2$, por tanto:

$\begin{array}{l}f'\left(x\right)\circ f^{-1}\left(x\right)=\left(3x^2\right)\circ\left(\sqrt[3]x\right)=3\sqrt[3]{x^2}\Rightarrow\\\left(f^{-1}\right)'\left(x\right)=\frac1{3\sqrt[3]{x^2}}.\end{array}$

## Cálculo práctico de derivadas

Para resolver problemas de cálculo de derivadas de forma eficiente se utilizan tablas de funciones y sus derivadas. Con estas tablas, la regla de la cadena, y el teorema de la derivada de la función inversa, pueden resolverse la gran mayoría de problemas, siendo necesario utilizar la definición de derivada, calculando límites, sólo en casos concretos, como se verá en los ejercicios.

**Tabla de derivadas de las funciones más usuales**

| **Función $y=f(x)$** | **Función $y'=f'(x)$** 
| $y=sin(x)$ | $y'=cos(x)$ 
| $y=cos(x)$ | $y'=-sin(x)$ 
| $y=tan(x)$ | $y'=sec^2(x)$ 
| $y=x^n$ | $y'=n·x^{n-1}$ 
| $y=C$ (una constante) | $y'=0$ 
| $y=Ae^x$ | $y'=Ae^x$ 
| $y=A^x$ | $y'=A^x·Ln(a)$ 
| $y=Ln(x)$ | $y'=\frac1{x}$ 
| $y=Log_a(x)$ | $y'=\frac1x\frac1{Ln\left(a\right)}$ 

Usando la regla de la cadena se puede obtener una tabla análoga a la anterior, sustituyendo en ella la variable $x$ por una función derivable arbitraria $g(x)$:

**Tabla de derivadas de las funciones compuestas más usuales**

| **Función $y=f(x)$** | **Función $y'=f'(x)$** 
| $y=sin(g(x))$ | $y=g'(x)·cos(x)$ 
| $y=cos(g(x))$ | $y=-g'(x)·sin(x)$ 
| $y=tan(g(x))$ | $y=g'(x)·sec^2(x)$ 
| $y=g^n(x)$ | $y'=g'(x)·n·g^{n-1}(x)$ 
| $y=Ae^g(x)$ | $y=g'(x)·Ae^g(x)$ 
| $y=A^x$ | $y=g'(x)·A^x·Ln(a)$ 
| $y=Ln(g(x))$ | $y=g'(x)·\frac1{x}$ 
| $y=Log_a(g(x))$ | $g'(x)·\frac1x\frac1{Ln\left(a\right)}$ 

Usando el teorema de la derivada de la función inversa puede obtenerse otra tabla:

**Tabla de derivadas de las funciones inversas más usuales**

| **Función $y=f(x)$** | **Función $y'=f'(x)$** 
| $y=sin^{-1}(g(x))$ | $y=\frac{g'(x)}{\sqrt{1-g^2(x)}}$ 
| $y=cos^{-1}(g(x))$ | $y=-\frac{g'(x)}{\sqrt{1-g^2(x)}}$ 
| $y=tan^{-1}(g(x))$ | $y=\frac{g'(x)}{1+g^2(x)}$ 

Combinando estas tablas con las propiedades de las derivadas podemos abordar la mayoría de problemas. En el caso de funciones compuestas exponenciales del tipo $f(x)^{g(x)}$, puede ser útil la técnica de aplicar logaritmos:

Para encontrar la derivada de $y=f(x)$, aplicamos logaritmos,  $Ln(y)=Ln(f(x))$,  derivamos, $\frac{y'}{Ln\left(y\right)}=\frac{f'\left(x\right)}{f(x)}\Rightarrow y'=\frac{f'\left(x\right)}{f(x)}Ln\left(y\right)$

**Ejemplo 13**: Calcular la derivada de $y=(sen(x))^{cos(x)}$.

Esta derivada es del tipo $f(x)^{g(x)}$, aplicando logaritmos, derivando, y usando las tablas y la derivada del producto de funciones:

$\begin{array}{l}Ln\left(y\right)=Ln\left((sen(x))^{cos(x)}\right)=\cos\left(x\right)Ln\left(\sin\left(x\right)\right)\rightarrow\\\frac{y'}y=\left(\cos\left(x\right)\right)'\cdot Ln\left(\sin\left(x\right)\right)+\cos\left(x\right)\cdot\left(Ln\left(\sin\left(x\right)\right)\right)'=\\-\sin\left(x\right)\cdot Ln\left(\sin\left(x\right)\right)+\cos\left(x\right)\cdot\frac{\cos\left(x\right)}{\sin\left(x\right)};\end{array}$

Despejando $y'$ del lado izquierdo de la igualdad anterior:

$\begin{array}{l}y'=y\cdot\left(-\sin\left(x\right)\cdot Ln\left(\sin\left(x\right)\right)+\cos\left(x\right)\cdot\frac{\cos\left(x\right)}{\sin\left(x\right)}\right)=\\(sen(x))^{\cos(x)}\cdot\left(-\sin\left(x\right)\cdot Ln\left(\sin\left(x\right)\right)+\cos\left(x\right)\cdot\frac{\cos\left(x\right)}{\sin\left(x\right)}\right).\end{array}$.

[![separador2](/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
{% endraw %}