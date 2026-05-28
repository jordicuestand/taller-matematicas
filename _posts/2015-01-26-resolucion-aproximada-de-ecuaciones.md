---
layout: post
title: "Resolución aproximada de ecuaciones"
date: 2015-01-26 20:45:14 +0000
math: true
---
{% raw %}

- Introducción

	- Aproximaciones, errores, algoritmos

	- Búsqueda de una raíz de una ecuación

	- Algoritmo de bisección

	- Algoritmo de Newton

	- Algoritmo de la secante

	- Estratégias para la búsqueda de raíces

![separador2](/taller-matematicas/assets/images/separador2.png)

 
## Introducción

Consideremos el estudio del crecimiento de poblaciones; el crecimiento de la población puede representarse para intervalos breves de tiempo $\triangle t$ suponiendo que en ese intervalo de tiempo la población crece continuamente con un aumento proporcional al número de individuos presentes en el inicio del intervalo de tiempo; llamando $N(t)$ al número de individuos en el tiempo $t$ entonces $\frac{\triangle N(t)}{\triangle t}=\lambda N(t),$ donde $\lambda$ es la denominada tasa de natalidad. Llevando al límite $\triangle t\rightarrow0$ obtenemos:

$\lim_{\triangle t\rightarrow0}\frac{\triangle N(t)}{\triangle t}=\frac{\operatorname{d}N(t)}{\operatorname{d}t}=N'(t)=\lambda N(t).$

Si además tenemos en cuenta que podemos tener inmigración, supongamos para simplificar que a una velocidad de llegada constante $v_0$, entonces tenemos:

$v(t)=N'(t)=\lambda N(t)+v_0,$

 que es una ecuación diferencial cuya solución es:

$N(t)=N_0e^{\lambda t}+\frac{v_0}\lambda\left(e^{\lambda t}-1\right),$

donde $N_0$ es la población inicial en el instante inicial $t=0$. Supongamos ahora que esta valor inicial es de 10⁶ individuos, que 435.000 inmigran anualmente y que, pasado un año, la población asciende a 1.564.000 individuos. Si con estos datos queremos hallar la tasa de natalidad $\lambda$ tendremos que resolver la ecuación:

$1.564.000=10^6\cdot e^{\lambda}+\frac{435.000}\lambda\left(e^{\lambda}-1\right),$

que es una [ecuación trascendente](http://es.wikipedia.org/wiki/Ecuaci%C3%B3n_trascendente), esto es, que no tiene solución analítica. Esta situación se da frecuentemente en las aplicaciones prácticas, y ha de resolverse de forma aproximada empleando los **métodos numèricos** que vamos a ver en este post. Estos métodos usan algoritmos que se implementan en un ordenador.

## Aproximaciones, errores, algoritmos

Cuando utilizamos métodos numéricos para aproximar valores, el valor resultado del cálculo diferirá del valor real exacto: cometeremos un error de aproximación. Hay varias formas de expresar este error:
**Definición 1***: Si $x^*$ es una aproximación de $x$, el **error absoluto** cometido está dado por $\left|x-x^\ast\right|$ y el **error relativo** por $\frac{\left|x-x^\ast\right|}{\left|x\right|},$ siempre que $x\neq 0$. *

**Ejemplo 1**: Cada uno de los vagones de un tren de mercancías tiene un peso aproximado en vacío de 20.000 $\pm$100Kg , y una longitud de 25 metros $\pm$0.5. Los errores absolutos cometidos son 100Kg y 0.5m, y los relativos 100/20.000 = 1/200 y 0.5/25 = 1/50 respectivamente. Observemos que el error absoluto del peso es, en las unidades dadas, mucho mayor que el error absoluto en la longitud, en cambio con los errores relativos pasa lo contrario.

**Definición 2**: *Si $x^*$ es una aproximación de $x$ con $t$ **dígitos significativos**, entonces $t$ es el mayor entero no negativo tal que *

*$\frac{\left|x-x^\ast\right|}{\left|x\right|}&lt;5\cdot10^{-t}$*

*o sea que el error relativo es menor que $5\cdot10^{-t}.$*

**Ejemplo 2**: Supongamos que queremos aproximar el valor $x=20.000$ con cuatro dígitos significativos, entonces ha de ser:

$\begin{array}{l}\frac{\left|20000-x^\ast\right|}{\left|20000\right|}&lt;5\cdot10^{-4}\Leftrightarrow\left|20000-x^\ast\right|&lt;20000\cdot5\cdot10^{-4}=10\Leftrightarrow\\19990&lt;x^\ast&lt;20010\end{array}.$

**Definición 3**: *Cuando aproximamos un número $x$ por su forma de punto flotante con k dígitos, o notación científica estándar, $x=0.d_1d_2...d_k·10^n$, el error cometido se llama **error de redondeo**. *

**Ejemplo 3**: Si "cortamos" el número $\mathrm\pi=3.14159265\dots$ a k=4 obtenemos  en notación de punto flotante  $\mathrm\pi=0.3141\cdot10^1$, si "redondeamos" a 4 decimales como a partir del dígito 5 se suma una unidad al siguiente dígito obtenemos $\mathrm\pi=0.3142\cdot10^1.$ En ambos casos el error cometido será el error de redondeo.

#### Pérdida de precisión en calculadoras y ordenadores digitales

La representación digital de los números decimales no es exacta, además, las operaciones aritméticas que realizan tampoco son exactas. Hay algunos casos concretos en que los errores pueden ser inaceptables, conviene conocerlos para intentar evitarlos. Son:

	- división de un número con decimales por un número pequeño

	- multiplicación de un número con decimales por un número grande

	- sustracción de dos números casi iguales

Cuando en un algoritmo de cálculo se realizan las operaciones anteriores repetidas veces, el error producido se propaga y puede ir aumentando hasta producir un error total inaceptable. Para evitarlo, es conveniente reformular los cálculos para evitar caer en alguna de las situaciones anteriores.

**Ejemplo 4**: Resolver $x^2+10^4x+1=0$ con la máxima precisión permitida por la calculadora (por ejemplo, 8 dígitos). Si usamos la fórmula estándar obtenemos:

$x=\frac{-10^4\pm\sqrt{10^8-4}}2=-0.5\cdot10^4\pm4999.9999$

Con la solución $x_1=-0.5\cdot10^4-4999.9999=-9999.9999$ no hay problema, pero con la otra solución sí, pues restamos dos números casi iguales: $x_1=-0.5\cdot10^4+4999.9999=-0.1\cdot10^3.$ En efecto, comprobemos las dos soluciones obtenidas sustituyendo en la ecuación:

$\begin{array}{l}x_1^2+10^4x_1+1=9999.9999^2-10^4\cdot9999.9999+1=0\\x_2^2+10^4x_2+1=0.001^2-10^4\cdot0.001+1=-8.999999\end{array}$

Vemos que la segunda solución no es aceptable. Para remediarlo, tenemos que evitar restar las dos cantidades tan parecidas al obtener $x_2$, lo podemos conseguir racionalizando:

$\begin{array}{l}x_2=\frac{-b+\sqrt{b^2-4ac}}{2a}\cdot\frac{-b-\sqrt{b^2-4ac}}{-b-\sqrt{b^2-4ac}}\\=\frac{b^2-b^2-4ac}{2a\left(-b-\sqrt{b^2-4ac}\right)}=\frac{-2c}{a\left(-b-\sqrt{b^2-4ac}\right)}\end{array},$

sustituimos valores en la calculadora:

$\frac{-2c}{a\left(-b-\sqrt{b^2-4ac}\right)}=\frac{-2}{-10^4-\sqrt{10^8-4}}=-1.00000001\cdot10^{-4},$

volvemos a comprobar este valor en la ecuación: $x_2^2+10^4x_2+1=\left(1.00000001\cdot10^{-4}\right)^2-10^4\cdot1.00000001\cdot10^{-4}+1=0.$

#### Algoritmos de cálculo numérico

***Definición 4**: Un **algoritmo de cálculo numérico** es una descripción precisa de cómo realizar una sucesión de cálculos en un orden específico, en vista a obtener un resultado deseado de forma aproximada. Cada paso del algoritmo proporciona un valor aproximado, y en cada paso necesitamos realizar unos cálculos. De esta forma obtenemos, paso a paso, una sucesión de aproximaciones al resultado deseado. Cuando esta sucesión converge al resultado diremos que el algoritmo es convergente. Cada ejecución del conjunto de pasos se llama una iteración del algoritmo.*

**Ejemplo 5**: algoritmo de división para calcular el cociente $a/b$ donde $a&lt;b$ y obtener el resultado con una precisión $\varepsilon$ usando las operaciones DIV (división entera) y MOD (resto de la división entera)

	- Variables de entrada: $a, b$ enteros tales que $a&lt;b; \varepsilon&gt;0$

	- Variables de salida: resultado
 $D$

	- Paso 0: hacer $D=0, n=1$

	- Paso 1: $q = 10a$ DIV $b$

	- Paso 2: $r = 10a $MOD$ b$

	- Paso 3: $D = D + q/10^n$

	- Paso 4: si $r \neq 0$ y $q/10^n &gt; \varepsilon,$ entonces hacer $a = r, n=n+1$, saltar al paso 1; de lo contrario, escribir "Resultado = " $D$, finalizar.

Si seguimos los pasos de este algoritmo usando los valores $a=3, b=7, \varepsilon=0.001$ obtenemos la siguiente secuencia de aproximaciones:

	- Paso 0: hacer $D=0, n=1$

	- Iteración 1

	Paso 1: $q = 10·3 DIV 7 = 4$

	- Paso 2: $r = 10·3 MOD 7 = 2$

	- Paso 3: $D = 0 + 4/10^1 = 0.4,$ esta es la primera aproximación obtenida

	- Paso 4: como $r \neq 0$ y $q/10^1 = 0.4 &gt; 0.001,$ hacemos $a=r=2, n = 1 + 1 = 2$ y saltamos de nuevo al paso 1

	- Iteración 2

	Paso 1: $q = 10·2 DIV 7 = 2$

	- Paso 2: $r = 10·3 MOD 7 = 6$

	- Paso 3: $D = 0.4 + 2/10^2 = 0.42,$ esta es la segunda aproximación obtenida

	- Paso 4: como $r \neq 0$ y $q/10^2 = 0.02 &gt; 0.01,$ hacemos $a=r=6, n = 1 + 1 = 3$ y saltamos de nuevo al paso 1

	- Iteración 3

	Paso 1: $q = 10·6 DIV 7 = 8$

	- Paso 2: $r = 10·6 MOD 7 = 4$

	- Paso 3: $D = 0.42 + 8/10^3 = 0.428,$ esta es la tercera aproximación obtenida

	- Paso 4: tenemos $r \neq 0$ pero  $4/10^3 = 0.004 &lt; 0.01,$ por tanto escribir "Resultado = 0.428", finalizar.

Hemos necesitado tres iteraciones del algoritmo para obtener la precisión deseada. Es sencillo implementar este algoritmo usando una hoja de cálculo, con lo cual podemos obtener una precisión elevada, con 10 iteraciones obtenemos $3/7$ con 10 decimales de precisión:

   

| **Iteración** 
| **a** 
| **b** 
| **q** 
| **r** 
| **D** 
| **n** 

| 0 
| 3 
| 7 
|  
|  
| 0 
| 1 

| 1 
| 2 
| 7 
| 4 
| 2 
| 0.4 
| 2 

| 2 
| 6 
| 7 
| 2 
| 6 
| 0.42 
| 3 

| 3 
| 4 
| 7 
| 8 
| 4 
| 0.428 
| 4 

| 4 
| 5 
| 7 
| 5 
| 5 
| 0.4285 
| 5 

| 5 
| 1 
| 7 
| 7 
| 1 
| 0.42857 
| 6 

| 6 
| 3 
| 7 
| 1 
| 3 
| 0.428571 
| 7 

| 7 
| 2 
| 7 
| 4 
| 2 
| 0.4285714 
| 8 

| 8 
| 6 
| 7 
| 2 
| 6 
| 0.42857142 
| 9 

| 9 
| 4 
| 7 
| 8 
| 4 
| 0.428571428 
| 10 

| 10 
| 5 
| 7 
| 5 
| 5 
| **0.4285714285** 
| 11 

![separador2](/taller-matematicas/assets/images/separador2.png)

## Búsqueda de una raíz de una ecuación

Dada una función $f(x)$ uno de los problemas básicos del cálculo numérico es el encontrar un valor $x_0$ tal que $f(x_0)=0$, al valor $x_0$ se le denomina una **raíz de** $f(x).$ En general, dada una ecuación $f(x)=c$ podemos definir $g(x)=f(x)-c$ y hallando una raíz de $g(x)$ resolvemos la ecuación.

### Separación de las raíces de una función

Cuando $f(x)$ tenga más de una raíz, será necesario para aplicar los algoritmos el establecer intervalos $[a,b]$ tales que en cada uno de ellos sólo haya una única raíz; a este proceso se le llama separación de las raíces de la función. Para ello será de gran ayuda tener al menos una idea de la forma de la gráfica de la función. También puede ser de gran ayuda el Teorema de Bolzano (ver [Funciones continuas](http://tallermatematic.eu/wp/?p=377), teorema 4) que reproducimos aquí:

**Teorema 1 (de Bolzano)**: Si $f:I\rightarrow\mathbb{R}$ es una función continua definida en un intervalo cualquiera $I=(a,b)$, y $f(a)$ tiene signo distinto a $f(b)$, entonces existe al menos un punto $c$ intermedio entre $a$ y $b$ tal que $f(c)=0$.

Una especialización de este teorema, especialmente útil para separar raíces, es el siguiente:

**Teorema 2, unicidad de la raíz en un intervalo**: Si $f:I\rightarrow\mathbb{R}$ es una función continua definida en un intervalo cualquiera $I=(a,b)$,  $f(a)$ tiene signo distinto a $f(b)$, y además $f'(x)$ tiene un signo constante en $(a,b$), entonces existe un único punto $c$ intermedio entre $a$ y $b$ tal que $f(c)=0$.

**Ejemplo 6**: separar las raíces de la función $y=x^3+x^2+3.$

| 
![exemple2_equacions](/taller-matematicas/assets/images/exemple2_equacions-150x150.png)

 
| Es una función continua. La gráfica de la función muestra una única raíz cerca del valor $x=-2$; sabemos que los polinomios tienen como máximo tantas raíces como indica su grado, tres en este caso. ¿Puede ser que existan más raíces que no vemos? La derivada $y'=3x^2+2x$ para $x&lt;-2$ toma valores positivos, luego en el intervalo $\left(-\infty,-2\right)$ la función es siempre creciente, además, $\lim_{x\rightarrow-\infty}f(x)=-\infty.$ 

Por otra parte $\lim_{x\rightarrow\infty}f(x)=\infty,$ y también para $x&gt;1$ la derivada es siempre positiva, luego la gráfica no puede volver a cortar el eje X. Así pues hay una única raíz, que separamos diciendo que está, por ejemplo en el intervalo $[-2.5,-1.5].$ En efecto, $f(-2.5)=-51/8&lt;0$ y $f(-1.5)=15/8&gt;0,$ luego por el Teorema de Bolzano ha de existir un $x_0\in\left$-2.5,2.5\right$$ tal que $f(x_0)=0.$
## Algoritmo de bisección

Supongamos que hemos separado una raíz de la función continua $f(x)$ en el intervalo $(a,b)$ de forma que
 $f(a)$ tiene distinto signo que $f(b)$. Sea el punto intermedio $p_1=(a+b)/2$; al calcular $f(p_1)$, si resulta ser que $f(p_1)\approx0$, o más precisamente, dada la precisión $\varepsilon$ resulta que $\left|f(p_1)\right|&lt;\varepsilon,$ entonces tenemos la raíz aproximada $x_0=p_1$ y hemos terminado. Caso contrario, o bien $f(p_1)&gt;0$ o bien $f(p_1)&lt;0$, también tendremos que  o bien $f(p_1)0$ tiene el mismo signo que $f(a)$ o bien $f(p_1)$tiene el mismo signo que $f(b)$. En el primer caso, definimos un nuevo intervalo de separación de la raíz, más estrecho, que será $(p_1,b)$, en el segundo caso el nuevo intervalo será $(a,p_1)$. Repetimos entonces el proceso con el nuevo intervalo, obteniendo en cada iteración un intervalo más estrecho en el cual ha de estar la raíz. Describamos el algoritmo:

**Algoritmo de bisección**

Para encontrar la raíz $p$ de la función continua $f(x)$ situada en el intervalo $(a,b)$ con una tolerancia $\varepsilon:$

	- Paso 0: $n = 1,$ introducir el número de iteraciones máximo MAXITER, la tolerancia $\varepsilon$  y el intervalo $(a,b)$

	- Paso 1: Si $n \leq$MAXITER entonces seguir al paso siguiente, de lo contrario parar con el mensaje: "número máximo de iteraciones excedido"

	- Paso 2: Calcular $p=(a+b)/2$

	- Paso 3: Si $\left|f\left(p\right)\right|&lt;\varepsilon$ o $(b-a)/2&lt;\varepsilon$ entonces parar, el resultado es $p$, mensaje: "raíz encontrada", en otro caso seguir

	- Paso 4: n = n +1; si $f(a)$ tiene el mismo signo que $f(p)$ entonces hacer $a = p$, si no hacer $b = p$. Ir al paso 1.

**Ejemplo 7**: para hallar la raíz de la función  del ejemplo 6, $y=x^3+x^2+3$, en el intervalo $x_0\in\left$-2.5,2.5\right$$ aplicamos el algoritmo de bisección con una tolerancia $\varepsilon=0.001$ y fijando el número máximo de iteraciones en 20; lo implementamos con hoja de cálculo:

| **n** 
| **a** 
| **b** 
| **p** 
| **f(a)** 
| **f(b)** 
| **f(p)** 
| **(b-a)/2** 

| 1 
| -2.5 
| 2.5 
| 0 
| -6.375 
| 24.875 
| 3 
| 2.5 

| 2 
| -2.5 
| 0 
| -1.25 
| -6.375 
| 3 
| 2.609375 
| 1.25 

| 3 
| -2.5 
| -1.25 
| -1.875 
| -6.375 
| 2.609375 
| -0.076171875 
| 0.625 

| 4 
| -1.875 
| -1.25 
| -1.5625 
| -0.076171875 
| 2.609375 
| 1.6267089844 
| 0.3125 

| 5 
| -1.875 
| -1.5625 
| -1.71875 
| -0.076171875 
| 1.6267089844 
| 0.876739502 
| 0.15625 

| 6 
| -1.875 
| -1.71875 
| -1.796875 
| -0.076171875 
| 0.876739502 
| 0.4270820618 
| 0.078125 

| 7 
| -1.875 
| -1.796875 
| -1.8359375 
| -0.076171875 
| 0.4270820618 
| 0.1823334694 
| 0.0390625 

| 8 
| -1.875 
| -1.8359375 
| -1.85546875 
| -0.076171875 
| 0.1823334694 
| 0.0548227429 
| 0.01953125 

| 9 
| -1.875 
| -1.85546875 
| -1.865234375 
| -0.076171875 
| 0.0548227429 
| -0.0102362856 
| 0.009765625 

| 10 
| -1.865234375 
| -1.85546875 
| -1.8603515625 
| -0.0102362856 
| 0.0548227429 
| 0.0224024495 
| 0.0048828125 

| 11 
| -1.865234375 
| -1.8603515625 
| -1.8627929688 
| -0.0102362856 
| 0.0224024495 
| 0.0061104308 
| 0.0024414063 

| 12 
| -1.865234375 
| -1.8627929688 
| -1.8640136719 
| -0.0102362856 
| 0.0061104308 
| -0.0020560847 
| 0.0012207031 

| 13 
| -1.8640136719 
| -1.8627929688 
| **-1.8634033203** 
| -0.0020560847 
| 0.0061104308 
| **0.002028883** 
| **0.0006103516** 

Hemos obtenido el valor aproximado de la raíz $p=-1.863$, para el cual $f(p)=0.004726353$, el algoritmo se ha parado en la iteración 13 debido a que $(b-a)/2= 0.0006103516 &lt; \varepsilon.$ Observar que damos el valor de $p$ con tres decimales, pues la precisión viene dada por el intervalo $(b-a)/2.$

El algoritmo de bisección tiene la propiedad de converger siempre a una solución, pero si el intervalo inicial es demasiado grande, puede ser necesario un número elevado de iteraciones. Dicho en otros términos, tenemos asegurada la convergencia pero ésta puede ser muy lenta. Hay además otro posible fallo: podría ser que se terminara con un valor $(b-a)/2$ muy pequeño pero en cambio $f(p)$ fuera bastante distinto de cero.

**Ejemplo 8**: El polinomio $f(x)=x^7-3x^6-12x^5+12^4-27x^3+34x^2-14x+18$ tiene una raíz en $(-4,-3)$ pues $f(-2)=782, f(-1)=-117$. Aplicando el algoritmo de bisección con $\varepsilon=10^{-5}$ y fijando el número máximo de iteraciones en 50 obtenemos, después de 16 iteraciones, $(b-a)/2=1.526E-005, p=-3.183014, f(p)=-0.03$ que no nos da una precisión elevada. Continuando hasta 30 iteraciones conseguimos $p=-3.183022, f(p)=2.878E-006.$

## Algoritmo de Newton

Este algoritmo puede ser explicado usando el desarrollo en serie de Taylor de primer orden de la función $f(x)$ de la cual queremos encontrar una raíz. Sea $x_0$ una aproximación inicial a la raíz $x^*$. Sabemos que $f\left(x\right)\approx f\left(x_0\right)+f'\left(x_0\right)\cdot\left(x-x_0\right).$ Igualando a cero y operando:

$\begin{array}{l}f\left(x\right)=0\Rightarrow f\left(x_0\right)+f'\left(x_0\right)\cdot\left(x-x_0\right)\approx0\Rightarrow x-x_0\approx-f\left(x_0\right)/f'\left(x_0\right)\Rightarrow\\x\approx x_0-\frac{f\left(x_0\right)}{f'\left(x_0\right)}.\end{array}$

Tomando el valor $x$ como siguiente aproximación $x_1$ y repitiendo el proceso obtenemos el algoritmo de Newton:
**Algoritmo de Newton**

Para encontrar la raíz $x^*$ de la función continua $f(x)$ situada en el intervalo $(a,b)$ con una tolerancia $\varepsilon:$

	- Paso 0: $n = 1,$ introducir el número de iteraciones máximo MAXITER, la tolerancia $\varepsilon$  y el valor inicial $x_0$

	- Paso 1: Si $n \leq$MAXITER entonces seguir al paso siguiente, de lo contrario parar con el mensaje: "número máximo de iteraciones excedido"

	- Paso 2: Calcular $x_n=x_0-\frac{f\left(x_0\right)}{f'\left(x_0\right)}$

	- Paso 3: Si $\left|x_n-x_0\right|&lt;\varepsilon$ entonces parar, el resultado es $x_n$, mensaje: "raíz encontrada", en otro caso seguir

	- Paso 4:hacer $x_0 = x_n$, n = n + 1;   Ir al paso 1.

**Ejemplo 9**: El método de Newton aplicado al polinomio $f(x)=x^7-3x^6-12x^5+12^4-27x^3+34x^2-14x+18$ con $x_0=-1.5$  y con $\varepsilon=10^{-9}$,  fijando el número máximo de iteraciones en 10 obtiene:

| **n** 
| **X_0** 
| **x_n** 
| **f(x_0)** 
| **f'(x_0)** 
| **error** 

| 1 
| -3.5 
| -3.2799249935 
| -2204.226 
| 10015.796 
| 0.2200750065 

| 2 
| -3.2799249935 
| -3.1950472585 
| -492.453 
| 5801.9121 
| 0.084877735 

| 3 
| -3.1950472585 
| -3.1832336086 
| -53.912 
| 4563.559 
| 0.0118136499 

| 4 
| -3.1832336086 
| -3.1830216906 
| -0.933 
| 4406.065 
| 0.000211918 

| 5 
| -3.1830216906 
| -3.1830216234 
| -0.0003 
| 4403.272 
| 6.722E-008 

| 6 
| -3.1830216234 
| **-3.1830216234** 
| **-2.837E-011** 
| 4403.271 
| **0** 

Comparando con el ejemplo 8, vemos que el algoritmo de Newton obtiene mejores resultados: con solo 6 iteraciones hemos conseguido un valor muy exacto $x=-3.1830216234$ tal que $f(x)\approx-2.8E-011$,  no obstante el método tiene también desventajas.

#### Propiedades del método de Newton

	- No es válido si resulta que $f'(x_n)=0$ para alguna de las iteraciones

	- Si el valor inicial $x_0$ está demasiado lejos del valor exacto $x^*$ el método puede ser divergente: no encontrarà la raíz, de hecho, se alejará de ella

	- Cuando es convergente, es más rápido que el de bisección, excepto si $f'(x)$ toma valores cercanos a 1, en cuyo caso será muy lento (necesitará muchas iteraciones).

	- Para aplicarlo, necesitamos la derivada de $f(x)$; en las aplicaciones prácticas, esto puede suponer un problema.

 
## Algoritmo de la secante

 El método de Newton puede verse desde el punto de vista geométrico como la aproximación local de la función por su recta tangente en cada punto $x_n$. por ejemplo, en la imagen siguiente, para encontrar $y=f(x)=0$ (línia en negro) por Newton usando como aproximación inicial $x_0=3$ aproximamos la función por su tangente en ese punto (línea amarilla) y hallamos su punto de corte con el eje X, que es la siguiente aproximación $x_1=2$. En el método de la secante usamos un intervalo inicial $(p_0,p_1)$ (como en el método de bisección) y aproximamos la función por la recta secante en el intervalo: en la imagen el intervalo es $(0,3)$, el corte de la secante con el eje X es precisamente en $x=0$ donde $f(x)=0$: el  método encuentra la raíz en un solo paso, ya que hemos tenido la suerte de escoger como extremo del intervalo la solución de la ecuación.

![Recta tangente y recta secante a la gráfica de la función y=f(x)](/taller-matematicas/assets/images/recta_tangent.png) Recta tangente y recta secante a la gráfica de la función y=f(x)

Caso de que la secante tomada en el intervalo$(p_0,p_1)$ no nos dé el resultado, tomamos una nueva recta secante pasando por los puntos $(p_1,p).$
**Algoritmo de la secante**

Para encontrar la raíz $x^*$ de la función continua $f(x)$ situada en el intervalo $(a,b)$ con una tolerancia $\varepsilon:$

	- Paso 0: $n = 1,$ introducir el número de iteraciones máximo MAXITER, la tolerancia $\varepsilon$  y el intervalo inicial $(p_0,p_1)$

	- Paso 1: Si $n \leq$MAXITER entonces seguir al paso siguiente, de lo contrario parar con el mensaje: "número máximo de iteraciones excedido"

	- Paso 2: Calcular $q_0=f(p_0),q_1=f(p_1), p=p_1-q_1\frac{p_1-p_0}{q_1-q_0}$

	- Paso 3: Si $\left|p-1_1\right|&lt;\varepsilon$ entonces parar, el resultado es $p$, mensaje: "raíz encontrada", en otro caso seguir

	- Paso 4: hacer $p_0 = p_1, q_0=q_1, p_1=p, q_1=f(p), n = n + 1$;   Ir al paso 1.

**Ejemplo 10**: El método de la secante aplicado al polinomio $f(x)=x^7-3x^6-12x^5+12^4-27x^3+34x^2-14x+18$ con el intervalo inicial $(-4,-3)$  y con $\varepsilon=10^{-9}$,  fijando el número máximo de iteraciones en 10 obtiene:
  

| **n** 
| **p0** 
| **p1** 
| **q0=f(p0)** 
| **q1=f(p1)** 
| **p** 
| **f(p)** 
| **|p-p1|** 

| 1 
| -4.000000 
| -3.000000 
| -10966 
| 609 
| -3.052613 
| 470.9336 
| 0.05261 

| 2 
| -3.000000 
| -3.052613 
| 609.00 
| 470.933 
| -3.232074 
| -232.340 
| 0.1794 

| 3 
| -3.052613 
| -3.232074 
| 470.933 
| -232.340 
| -3.172785 
| 44.3865 
| 0.05928 

| 4 
| -3.232074 
| -3.172785 
| -232.340 
| 44.3865 
| -3.182295 
| 3.19515 
| 0.0095 

| 5 
| -3.172785 
| -3.182295 
| 44.3865 
| 3.19515 
| -3.183033 
| -0.04947 
| 0.0007 

| 6 
| -3.182295 
| -3.183033 
| 3.1951 
| -0.04946 
| -3.183022 
| 5.3810E-005 
| 1.12468E-005 

| 7 
| -3.183033 
| -3.183022 
| -0.0494 
| 5.38105E-005 
| **-3.183022** 
| 9.02993E-010 
| 1.22203E-008 

El valor obtenido, con 8 cifras de precisión, es $p=-3.18302162.$ Comparando con el método de Newton, ha realizado una iteración más para obtener menor precisión, pero a cambio no ha sido necesario calcular la derivada de la función.

De forma parecida al método de Newton, el de la secante puede diverger si el intervalo inicial es demasiado amplio.
## Estratégias para la búsqueda de raíces

Para encontrar las raíces de una función el primer paso será separarlas, como se ha explicado en el apartado Separación de raíces. Para cada intervalo aplicaremos alguno de los algoritmos anteriores. Si algún intervalo es demasiado ámplio los métodos de Newton y de la secante pueden diverger, en ese caso podemos mejorar el intervalo realizando algunas iteraciones del método de bisección, para posteriormente aplicar Newton o la secante. Como ejemplo, resolveremos la ecuación planteada al principio del post, en el problema del crecimiento de las poblaciones.

**Ejemplo 11**: resolver $1.564.000=10^6\cdot e^{\lambda}+\frac{435.000}\lambda\left(e^{\lambda}-1\right).$

Lo expresamos como una función $f(\lambda)=1564000-10^6e^\lambda-\frac{435000}\lambda\left(e^\lambda-1\right)=0$ de la que queremos buscar raíces. La función es continua excepto quizá en $\lambda=0$, para ver que pasa en ese punto hacemos el límite:

$\begin{array}{l}\lim_{\lambda\rightarrow0}\frac{435000}\lambda\left(e^\lambda-1\right)=\frac00=\lim_{\lambda\rightarrow0}\frac{D_\lambda\left$435000\left(e^\lambda-1\right)\right$}{D_\lambda\left$\lambda\right$}\\=\lim_{\lambda\rightarrow0}\frac{435000e^\lambda}1=435000\end{array}$

Por tanto la función es continua en todo su dominio. Tenemos que encontrar un intervalo $(a,b)$ tal que haya un cambio de signo en los extremos del intervalo. Para $\lambda=0$ hemos visto que la función toma el valor $+435000$, y se ve claramente que para valores suficientemente grandes de $\lambda$ el signo será negativo. Si probamos con $\lambda=1$ obtenemos $-406829$, por tanto el intervalo inicial puede ser $(0,1)$. Para no tener que derivar la función usaremos el método de la secante, exigiendo una tolerancia de $10^{-10}$ y con un máximo de 10 iteraciones; hay que tener en cuenta que para $\lambda=0$ obtendremos un error de división por cero, por eso cogemos un valor próximo como extremo inferior del intervalo $a=10^{-6}$, obtenemos:

      

| **n** 
| **p0** 
| **p1** 
| **q0=f(p0)** 
| **q1=f(p1)** 
| **p** 
| **f(p)** 
| **|p-p1|** 

| 1 
| 0.000001 
| 1.000000 
| 998999 
| -406829 
| 0.710613 
| 162480 
| 0.2893 

| 2 
| 1.000000 
| 0.710613 
| -406829 
| 162481 
| 0.793204 
| 17364 
| 0.0825 

| 3 
| 0.710613 
| 0.793204 
| 162481 
| 17364 
| 0.803086 
| -866 
| 0.0098 

| 4 
| 0.793204 
| 0.803086 
| 17364 
| -867 
| 0.802616 
| 4.3290 
| 0.0004 

| 5 
| 0.803086 
| 0.802616 
| -867 
| 4.32906 
| 0.802619 
| 0.00107 
| 0.000002 

| 6 
| 0.802616 
| 0.802619 
| 4.329056 
| 0.00107 
| **0.80261862306** 
| 0 
| 5.7838E-010 

La convergencia ha sido rápida porque el intervalo inicial es suficientemente bueno.
{% endraw %}