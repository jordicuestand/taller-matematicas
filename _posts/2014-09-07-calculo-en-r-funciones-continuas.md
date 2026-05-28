---
layout: post
title: "Cálculo en R -> Funciones continuas"
date: 2014-09-07 16:39:47 +0000
math: true
---
{% raw %}

## Definición de continuidad

Intuitivamente la continuidad de una función es un concepto muy simple: una función es continua cuando podemos dibujar su gráfica sin tener que levantar el lápiz en ningún punto. En la imagen vemos, a la izquierda, la función $sen(x)$ que es continua en todos los puntos, a la derecha la función $tan(x)$ que es continua solo en intervalos, ya que tiene infinitos puntos en los que la función toma valores infinitos, y "hay que levantar el lápiz" en esos puntos.


También podemos verlo de otro modo: las aplicaciones continuas tienen la propiedad de que, dado un punto $x_1$ y su imagen $y_1=f(x_1)$, si tomamos otro punto $x_2$ "cercano" a $x_1$, entonces su imagen $y_2=f(x_2)$ también estará "cercana" a $y_1$.


Cuando se trata de definir rigurosamente este concepto, entonces tenemos que abandonar la intuición y dar una definición operativa, ya que no queda claro que entendemos por "estar cerca del punto". Damos una definición que usa límites:

**Definición 1**: Si $f:A\subset\mathbb{R}\rightarrow\mathbb{R}$ y el punto $a$ pertenece al conjunto de puntos de acumulación de $A$, $a\in\text{Acum}\left(A\right)$, diremos que $f$ es continua en $a$ si existe el límite $L=\lim_{x\rightarrow a}f\left(x\right)\neq\pm\infty$ y además se cumple que $L=f(a)$. 
Nota: un punto a de A es un punto de acumulación de A si en todo entorno B(a, r) encontramos puntos de A, aparte del propio punto a. El conjunto de puntos de acumulación de A lo abreviamos por Acum(A). Puede repasarse el concepto en [Cálculo en R -> Topologia de R](http://mathseng.blogspot.com.es/2014/02/topologia-de-r.html).

La definición se refiere a la continuidad de la función en un único punto $x=a$, por lo que decimos que es una definición (o propiedad) local. Si resulta ser que $f$ es continua en todos los puntos de un subconjunto $B$ de su dominio $A$, diremos que $f$ es continua en el conjunto $B$  y entonces la propiedad pasa a ser  global. En este caso usaremos la notación $f\in\text{Co}\left(B\right)$, que viene a leerse como "f pertenece al conjunto de funciones continuas en B".

**Ejemplo 1**: La función $sen(x)$ verifica que $L=\lim_{x\rightarrow a}\sin\left(x\right)=f\left(a\right)$, luego es continua en todo su dominio, que son todos los números reales:  $sin(x)\in\text{Co}\left(\mathbb{R}\right)$

**Ejemplo 2**: La función $tan(x)$, en los puntos $x=\frac\pi2,\frac{3\pi}4,\frac{5\pi}2,\dots,\frac\pi2+k\pi$ con $k=0,1,2, ..."$ cumple que $L=\lim_{x\rightarrow a}\tan\left(x\right)=\pm\infty$, luego no es continua en esos puntos.  Es continua en la unión infinita de intervalos abiertos $B=\left(0,\frac\pi2\right)\cup\left(\frac\pi2,\frac{3\pi}4\right)\cup\left(\frac{3\pi}4,\frac{5\pi}2\right)\cup\dots$, que es a su vez un conjunto abierto.

**Ejemplo 3**: La función $f(x)=\frac1x$ es continua en todo punto $x$ excepto en el origen, ya que $L=\lim_{x\rightarrow0}\frac1x=\frac10=\pm\infty.$ Esto podemos expresarlo como $f\in\text{Co}\left(\mathbb{R}-\left\{0\right\}\right)$, f es continua en todo el conjunto $\mathbb{R}$ excepto en el punto aislado 0.

**Ejemplo 4**: Sea la función

$f\left(x\right)=\left\{\begin{array}{l}\frac12\;\text{si }0&lt;x\leq1\\0\;\text{si }x=0\\\frac{-1}2\;\text{si }-1\leq x&lt;0.\end{array}\right.$

El dominio de la función es $A=[-1, 1]$; en el punto $x=0$ tenemos un valor específico, debemos pues comprobar que exista el límite en ese punto, haciendo los límites laterales:

$\lim_{x\rightarrow0^-}f\left(x\right)=\frac{-1}2;\;\lim_{x\rightarrow0^+}f\left(x\right)=\frac12$

Luego el límite en $x=0$ no existe al no coincidir los límites laterales en ese punto, y la función no puede ser continua en $x=0$. En la imagen, las líneas horizontales no llegan al punto $x=0$, ya que en ese punto la función toma el valor 0, es decir, pasa por el punto $(0,0)$.


**Significado de la definición**: cuando nos acercamos al punto $a$ tanto por la izquierda como por la derecha (esto es, en el límite $\lim_{x\rightarrow a}f\left(x\right)$), si la función es continua entonces las imágenes $f(x)$ también deberían acercarse progresivamente al valor de la funciòn en el punto, $f(a)$. La condición de que $a$ sea un punto de acumulación es para excluir puntos $a$ aislados, en los cuales la definición no tendría sentido. Por ejemplo:

$f(x)=\left\{\begin{array}{l}x\;\text{si }x&gt;0\\1\;\text{si }x=-1\end{array}\right.$

tiene como dominio $A=\left\{-1\right\}\cup\left\{x&gt;0\right\}$, y el punto $x=-1$ es un punto aislado, en el que no podemos hacer ningún límite pues no existe ningún entorno del punto aparte de él mismo con imágenes $f(x)$.


El conjunto de puntos de acumulación de esta función es $\text{Acum}\left(A\right)=\left\{x\geq0\right\}=A-\left\{x=-1\right\}.$

---

## Propiedades de las funciones continuas

**Propiedad 1**: Si $f,g$ son ambas funciones continuas en $A$, entonces las funciones $f+g,$ $f-g,$ $f·g$ y $f/g$ son continuas en A (en el último caso, siempre que $g(x)\neq0$).

**Ejemplo 5:** Sean $f=sin(x)$ y $g=tan(x)$; definimos la función $h(x)=f(x)-g(x)$ en el dominio $A=\left(0,\pi/4\right)$. Como las dos funciones $f,g$ son continuas en $A$, también lo será la función $h=sin(x)+tan(x)$ en $A$. Lo mismo podemos decir de $sin(x)-tan(x)$, de $sin(x)\cdot tan(x)$ y de $sin(x)/tan(x)$, recordando en este último caso que $tan(x)$ no toma valores nulos en el intervalo $\left(0,\pi/4\right)$.

Por otro lado las funciones polinómicas $\;a_0+a_1x^1+a_2x^2+\dots+a_kx^k$ también son funciones continuas ya que son sumas de monomios $\;ax^n$ que a su vez son funciones continuas en todos los puntos.

**Funciones compuestas**

Sean dos funciones $f, g$ con dominios A, B, respectivamente, y supongamos que $f(x)\in B$ para todo $x)\in A$. Definimos la función compuesta $g\circ f$ de la siguiente forma:

$\left(g\circ f\right)(x)=g\left(f\left(x\right)\right)$

Ejemplo de función compuesta: sea $f(x)=x^2$ y $g(x)=sin(x)$. Los dominios de ambas funciones son todos los números reales. Podemos definir las funciones compuestas $g\circ f$ y $f\circ g$:

$\begin{array}{l}\left(f\circ g\right)\left(x\right)=f\left(g\left(x\right)\right)=f\left(\sin\left(x\right)\right)=\sin^2\left(x\right),\\\left(g\circ
 f\right)\left(x\right)=g\left(f\left(x\right)\right)=g\left(x^2\right)=\sin\left(x^2\right).\end{array}$

**Propiedad 2**: Si $f$ es continua en el punto $a$, y $g$ es continua en el punto $y=f(a)$, entonces la función compuesta $g\circ f$ es continua en $a$.

**Ejemplo 6:** Sea $f(x)=x^2,\;g(x)=\sin\left(x\right),\;\left(g\circ f\right)\left(x\right)=g\left(f\left(x\right)\right)=\sin\left(x^2\right).\;$ Siendo las funciones $f, g$ continuas en todo $\mathbb{R}$, también lo será la función compuesta $\sin\left(x^2\right).$

**Ejemplo 7**: Con las mismas funciones $f,g$ formamos la composición $\;\left(f\circ g\right)\left(x\right)=f\left(g\left(x\right)\right)=\left(\sin\left(x\right)^2\right)=\sin^2\left(x\right).\;$ Observemos que la composición de funciones no es conmutativa: $\;\left(f\circ g\right)\left(x\right)\neq\;\left(g\circ f\right)\left(x\right)$, no obstante, la propiedad 2 sigue cumpliéndose, y la función compuesta $\sin^2\left(x\right)$ es continua en todos los puntos, por ser composición de funciones continuas.

**Funciones inversas**

Recordemos: una función es inyectiva siempre que, si $f(x)=f(y)$, entonces forzosamente $x=y$, o dicho llanamente, puntos distintos tienen imágenes distintas. Por ejemplo, la función $f(x)=x^2$ no es inyectiva, pues $f(a)=f(-a)=a^2$ para cualquier número $a$. En cambio la función $f(x)= x^3$ es inyectiva: $f(x)=f(y)\Rightarrow x^3=y^3\Rightarrow x=y.\;$ Gráficamente se ve enseguida si una función es inyectiva: si trazando una línea horizontal cortamos a la gráfica de la función en como máximo un único punto, entonces es inyectiva.


Sólo las funciones inyectivas tienen función inversa, es por esto que hay este requerimiento en la propiedad 3. Recordemos también que, dada una función inyectiva $f(x)$, definimos su función inversa $f^{-1}(x)$ así: si $y=f(x)$, entonces $f^{-1}(y)=x.$

**Propiedad 3**: Si $f(x)$ es una función inyectiva y continua, entonces su función inversa $f^{-1}(x)$ es también continua.

 **Ejemplo 8**: Dada la función inyectiva $y=f(x)=x^3$, que es continua, su inversa es $f^{-1}(x)=\sqrt[3]y\;$, que también es continua. En la imagen vemos las gràficas de ambas en el primer cuadrante. Es una propiedad a destacar que las gráficas de una función y de su inversa son siempre simétricas respecto a la recta $y=x$.


En cambio para la función $y=x^2$ si trazamos la gràfica simétrica respecto a la recta $y=x$ no obtenemos una función, ya que dado un punto cualquiera $x=a$ tenemos dos posibles imágenes, $\sqrt a$ y $-\sqrt a$, y esto no puede darse en ninguna función, por definición.


---

## Continuidad en conjuntos compactos

Recordemos la propiedad fundamental de los **conjuntos compactos**: Todo conjunto cerrado y acotado de **R**, es compacto (Teorema de Heine-Borel). Enunciamos cuatro teoremas relativos a funciones, conjuntos compactos y continuidad.

**Teorema 1**: Si $f:K\rightarrow\mathbb{R}$ es continua y $K$ es un conjunto compacto, entonces el conjunto imagen $f\left(K\right)=\left\{y=f(x),\;x\in K\right\}$ es tambien compacto. Dicho de forma más "literaria": las funciones continuas transforman conjuntos compactos en compactos, o también, las funciones continuas conservan la propiedad de compacidad.
**Ejemplo 9**: Sea la función continua $y=f(x)=x^2$; el conjunto $K=[-1, 1]$ es compacto por que es cerrado (el intervalo incluye los extremos) y acotado. Entonces su imagen $f(K)$ será también compacto. En efecto, $f(K)=[0,1]$, cerrado y acotado, luego compacto.

**Teorema 2, de Weierstrass**: Si $f:K\rightarrow\mathbb{R}$ es continua y $K$ es un conjunto compacto, entonces existen dos puntos $M$ y $m$ en $K$, denominados máximo de $f$ en $K$ y mínimo de $f$ en $K$ respectivamente, tales que

$f(m)\leq f(x)\leq f(M)\;\text{para todo }x\in K.$

Además, $f(m)$ es el ínfimo del conjunto imagen $f(K)$, y $f(M)$ es el supremo. (Recordatorio: el ínfimo és el valor mayor de las cotas inferiores del conjunto, si pertenece al conjunto, entonces también es el mínimo del conjunto, análogamente para supremo y máximo).
**Ejemplo 10**: una función continua siempre ha de tomar un valor máximo y un valor mínimo en cualquier intervalo cerrado que consideremos. La función $0.35x^4-5x^3+23x^2+41x+23$ considerada en el intervalo cerrado $[0.2, 6]$ se presenta en la figura:


 

En cambio una función discontinua no tiene por que tener máximo y mínimo en todo intervalo cerrado y acotado.

En la imagen vemos parte de la gráfica de la función $y=1/(x-5)$ en el intervalo $[5, 6]$, resulta que en $x=5$ la función toma valor infinito, y no tenemos máximo, en cambio en el otro extremo, $x=6$, tenemos un mínimo, $y=1$.

 

 

 

 

**Teorema 3 (de los valores intermedios): **Si $f:I\rightarrow\mathbb{R}$ es una función continua definida en un intervalo cualquiera $I$ (puede ser abierto, cerrado, o ninguno de los anteriores), y los puntos $a,\;b\;\in I$, entonces para cualquier $y$ en el intervalo $\left(f\left(a\right),f\left(b\right)\right)$ existe un $x$ en el intervalo $(a,b)$ tal que $y=f(x)$. Dicho de forma no rigurosa: "la función $f$ toma todos los valores comprendidos entre $f(a)$ y $f(b)$".
**Ejemplo 11**: La función $y=f(x)=x^2$ es continua; si consideramos el intervalo $(a,b)=(1,2)$,  su imagen es $f(a),f(b)=(1,4)$. Dado cualquier valor $y$ en el intervalo $(1,4)$, existirá un $x$ en el intervalo $(1,2)$ tal que $y=f(x)=x^2$. Por ejemplo, para $y=3$ tenemos $x=\sqrt3\approx1.73\in\left(1,2\right).$

**Teorema 4 (de Bolzano)**: Si $f:I\rightarrow\mathbb{R}$ es una función continua definida en un intervalo cualquiera $I=(a,b)$, y $f(a)$ tiene signo distinto a $f(b)$, entonces existe al menos un punto $c$ intermedio entre $a$ y $b$ tal que $f(c)=0$.


Intuitivamente podemos razonar que si el gráfico de una función continua está por debajo del eje de abcisas en el extremo inferior de $(a,b)$ y por encima en el extremo superior, entonces el gráfico debe de cortar al eje en algún punto.

**Ejemplo 12:  **Demostrar que la ecuación $x^3+x^2+3$ tiene alguna solución en el intervalo $(-2,0)$.

Consideramos la función $f(x)=x^3+x^2+3$ definida en el intervalo $(-2,0)$. La gráfica de esta función la tenemos en la imagen. Vemos que $f(-2)=-1$ y que $f(0)=3$, la función tiene signo distinto en los extremos del intervalo. Además $f$ es continua por ser un polinomio. Por el teorema de Bolzano ha de existir al menos un $c\in(-2,0)$ tal que $f(c)=0$. En este caso, el punto es aproximadamente $c=-1.865$.

## Continuidad uniforme

La definición que hemos dado de continuidad decíamos que era local: es una propiedad de la función en un punto $x=a$, y podemos extenderla a un conjunto $I$ siempre que se cumpla definición en todos los puntos de $I$. Para utilizar el concepto de continuidad en otros ámbitos más generales que el de las funciones reales de variable real se hace necesario dar otra definición que sea directamente global, esto es, que se aplique a un conjunto, y no a sus puntos. Esta definición es la de continuidad uniforme.

En la primera definición hemos usado el concepto de límite:  decíamos que debe existir el límite $L=\lim_{x\rightarrow a}f\left(x\right)\neq\pm\infty$ y además cumplirse que $L=f(a)$.  Si existe el límite, entonces por la definición de límite de una función en un punto (ver por ejemplo: [Límites de funciones de variable real, teoria](http://tallermatematic.eu/wp/?p=47)) se cumplirá la condición:

para cada entorno del punto $L$ con radio $R$, $B(L, R)$, existe otro entorno del punto $a$  con radio $r$, $B(a, r)$, tal que los valores $f(x)$ de la función pertenecen al entorno $B(L, R)$ para todo $x\in B^\ast(a,r)\bigcap A$.

En general, dado un cierto valor del radio $R$, el radio $r$ dependerá del punto $x=a$ considerado.


**Ejemplo 12.** Para la función $y=f(x)=x^2$, tomemos $R=0.1$. Entonces, para $a=1$, el valor $r$ correspondiente ha de cumplir que, si $1-r\leq x\leq1+r$ entonces $1-R\leq f(x)\leq1+R$, es decir, que

$0.9\leq x^2\leq1.1\Leftrightarrow\left|\sqrt{0.9}\right|\leq x\leq\left|\sqrt{1.1}\right|\Leftrightarrow0.949\leq x\leq1.049$

aproximadamente, por tanto podemos decir que para $R=0.1$ se cumple la condición siempre que $r=0.049$. Si ahora buscamos $r$ pero para el punto $a=2$ obtenemos:

$4-0.1\leq x^2\leq4+0.1\Leftrightarrow\left|\sqrt{3.9}\right|\leq x\leq\left|\sqrt{4.1}\right|\Leftrightarrow1.975\leq x\leq2.025\Leftrightarrow x=2\pm0.025,$

o sea que ahora es $r=0.025$. Vemos pues que, sin variar $R=0.1$, el valor $r$ depende del punto $a$ considerado.

Podemos dar ahora la definición:

**Definición 2**: Si $f:A\subset\mathbb{R}\rightarrow\mathbb{R}$ es continua en todo punto de un conjunto  $I\subset A$, y además se cumple que, dado cualquier $R&gt;0$, existe un $r&gt;0$ que cumple la definición de límite para cualquier punto $a\in I$, entonces diremos que $f$ es uniformemente continua en $I$. 
Por tanto la función $y=x^2$ no está claro que sea uniformemente continua, ya que hemos visto que no existe un único valor $r$ para cualquier $a$. De hecho, solo hemos visto que para $a=1$ y $a=2$ los valores de $r$ difieren, no hemos estudiado otros puntos del dominio, así que todavía no podemos afirmar nada.

**Ejemplo 13**: La función $y=f(x)=x^2$ es uniformemente continua an $I=(0,1]$.  Para verlo, aplicamos la definición 2 a un punto cualquiera $a\in(0,1\rbrack:$

$a^2-R\leq y\leq a^2+R\Leftrightarrow\left|a^2-y\right|\leq R,$

como $y=x^2$, esto equivale a $\left|a^2-x^2\right|\leq R,$ que se puede expresar como producto de suma por diferencia  $\left|\left(a-x\right)\left(a+x\right)\right|\leq R;$ ahora, sabiendo que tanto $a$ como $x$ estan en el intervalo $(0,1]$, resulta que $\left|\left(a+x\right)\right|\leq2,$ y por tanto $\left|\left(a-x\right)\left(a+x\right)\right|\leq2\left|a-x\right|;$ por otro lado si queremos que $\left|\left(a-x\right)\right|\leq r,$ entonces ha de ser $\left|\left(a-x\right)\left(a+x\right)\right|\leq2r.$ Comparando las dos expresiones que hemos obtenido:

$\left.\begin{array}{r}\left|\left(a-x\right)\left(a+x\right)\right|\leq R\\\left|\left(a-x\right)\left(a+x\right)\right|\leq2r\end{array}\right\}\rightarrow R=2r\rightarrow r=\frac R2.$

Por tanto, para cualquier $R$ dado, bastará con tomar $r=R/2$ para que se cumpla la condición de continuidad, sea cual sea el punto $a$, con lo que hemos probado que la función es uniformemente continua en $(0,1]$.

**Interpretación de la continuidad uniforme**

Para una función uniformemente continua, dada una variación en el valor de la función $y=f(x)$, podemos hacer una estimación de la variación del valor $x$, sin importar el valor absoluto de $x$ ni de $y$. La estimación vale para cualquiera valor. La continuidad uniforme es una propiedad global de la función en un intervalo.

En general es complicado establecer si una función es uniformemente continua aplicando la definición; en la práctica hay formas de verlo si recurrir a los límites.

**Teorema 5**. Una función que es continua en un conjunto cerrado y acotado (por tanto compacto) es necesariamente uniformemente continua en ese conjunto.
**Ejemplo 14.** Volviendo a la función $y=f(x)=x^2$ sabemos que es continua en todo intervalo cerrado de $\mathbb{R}$, por tanto por el teorema 5 será uniformemente continua en todo intervalo cerrado.  En cambio no lo es en todo $\mathbb{R}.$ Esto es debido al rápido crecimiento de la función. En efecto, si tomamos un $R&gt;0$ y dos puntos $y_1,y_2$ tales que $\left|y_1-y_2\right|\leq R$, debería existir un $r&gt;0$ tal que $\left|x_1-x_2\right|\leq r$ siendo $y_1=f(x_1),y_2=f(x_2)$. Pero $\left|y_1-y_2\right|\leq R\Leftrightarrow\left|x_1^2-x_2^2\right|\leq R,$ supongamos que $x_2=x_1+\varepsilon,\;\varepsilon\leq r;$ entonces $\left|x_1^2-\left(x_1+\varepsilon\right)^2\right|\leq R\Leftrightarrow\left|\varepsilon^2-2\varepsilon x_1\right|\leq R\Leftrightarrow\varepsilon\left|\varepsilon-2x_1\right|\leq R, $ y observando esta última desigualdad vemos que, a medida que vamos tomando $x$ más i más grandes, el valor absoluto $\left|\varepsilon-2x_1\right|$ crecerá y no será posible que permanezca menor que $R$. A medida que $x$ aumenta, el valor $r$ necesario ha de reducirse, para un $R$ fijo dado.  En la figura vemos la función $y=x^2$ para el intervalo de valores $x$ entre 0 y 8; observemos que, para un $R=5$ fijo tomado en el eje de ordenadas, el intervalo $y\in\left$5,15\right$$ se relaciona con el intervalo $x\in\left$\sqrt5,\sqrt{15}\right$\approx\left$2.2,\;3.9\right$$, pero para el intervalo $y\in\left$45,55\right$$ obtenemos  $x\in\left$\sqrt{45},\sqrt{55}\right$\approx\left$6.7,\;7.4\right$,$ que es más estrecho que el anterior. A medida que $x$ crece, el intervalo de $x$ que se relacionan con $f(x)\pm R$ se hace más estrecho: $r$ disminuye, y eventualmente
 tiende a cero.


Si nos limitamos a un intervalo cerrado cualquiera, entonces bastará con tomar $r$ suficientemente pequeño para que se satisfaga la condición en todo el intervalo de $x$, y tendremos la continuidad uniforme asegurada.
{% endraw %}