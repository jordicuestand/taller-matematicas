---
layout: post
title: "Los números complejos"
date: 2016-10-12 09:05:14 +0000
categories:
  - "Matemáticas"
tags:
  - "argumento complejo"
  - "complejo conjugado"
  - "complejos"
  - "forma polar"
  - "número imaginario"
  - "plano complejo"
  - "potencia complejo"
  - "raíz complejo"
math: true
---
{% raw %}

#### Motivación

Antes de escribir este artículo ha mirado qué hay sobre el tema en Internet, pues siempre que encuentro material de calidad sobre un tema, bien explicado, con buenos ejemplos, decido no añadir nada, pues no es necesario. En el caso de los números complejos y en castellano he encontrado apuntes de nivel bachillerato, bastante aceptables, y apuntes muy completos, incluso libros de 400 páginas en PDF a nivel alto, también con buena calidad; lo que no he encontrado es ninguna introducción que explique claramente para qué se utilizan los complejos, como mucho hay introducciones históricas que los relacionan con la resolución de ecuaciones. Es por esto que he decidido participar en el tema.

Este artículo es introductorio, a nivel de bachillerato - 1º curso universitario, pero mostrando las aplicaciones prácticas, que a menudo son de un nivel superior. Esta intenta ser mi aportación al tema: mostrar cómo funcionan los números complejos a nivel básico, y mostrar para qué se utilizan actualmente.

#### Los números imaginarios

Es bien sabido que no podemos calcular la raíz cuadrada de un número negativo, de forma que tenemos infinitos números reales sin raíz cuadrada, como $\sqrt{-1},\sqrt{-2},\cdots$, y por tanto hay infinitas ecuaciones cuadráticas *ax² + bx + c = 0* sin solución, concretamente, todas las que tengan un discriminante *b² - 4ac* negativo. Esto no sucede con la operación inversa de la radicación, la exponenciación: el cuadrado de un número *x* existe para todo *x*. Así que tenemos tres obstáculos: hay ecuaciones cuadráticas sin solución, hay números sin raíz cuadrada, y existe una asimetría entre exponenciación y su operación inversa la radicación. Además, sucedía que en ciertos cálculos algebraicos se encontraban resultados intermedios como por ejemplo $\left(\sqrt{-1}+\sqrt{-2}\right)\cdot\sqrt{-1}$[1], que en principio parecía que obligaban a detenerse ahí, pues ninguna de esas raíces "existía"; no obstante, algo parecido sucedió históricamente con los números negativos, que parecían algo inexistente, pero al multiplicarlos entre sí resultaba un número "existente" positivo, como por ejemplo en (-1)·(-2) = +2. Quizá se podría hacer algo parecido con las raíces de números negativos...

Los historiadores nos dicen que fue [Rafael Bombelli](https://es.wikipedia.org/wiki/Rafael_Bombelli) el que ideó el número imaginario $i=\sqrt{-1}$; de esta definición se deduce que $i^2=\left(\sqrt{-1}\right)^2=-1$, y por extensión, podemos representar cualquier raíz de un número negativo en función del imaginario i: $\sqrt{-x}=\sqrt{-1\cdot x}=\sqrt{-1}\cdot\sqrt x=i\cdot x$. Entonces, expresiones algebraicas como la [1] pueden simplificarse:

$\left(\sqrt{-1}+\sqrt{-2}\right)\cdot\sqrt{-1}=\left(i+i\sqrt2\right)\cdot i=i^2+i^2\sqrt2=-1-\sqrt2,$

vemos que el producto de imaginarios resulta ser, en este caso, un número real.

También gracias a los números imaginarios todas las ecuaciones cuadráticas (de hecho todas las ecuaciones algebraicas, de cualquier grado) tienen soluciones, pues si el discriminante *b² - 4ac* es negativo podemos expresarlo como (-1)·(-*b² + 4ac*) siendo (-*b² + 4ac*) positivo, y al hacer la raíz aparece el número i:

$x=\frac{-b\pm\sqrt{b^2-4c}}{2a}=\frac{-b\pm\sqrt{\left(-1\right)\left(b^2-4c\right)}}{2a}=\frac{-b\pm\sqrt{\left(-1\right)\left(-b^2+4c\right)}}{2a}=\frac{-b\pm i\sqrt{\left(-b^2+4c\right)}}{2a}$[2]

Así la introducción del número imaginario i parece que soluciona los problemas planteados; lo curioso del caso es que, posteriormente, se descubrió que eran muchísimo más útiles de lo que nadie podía sospechar.

#### Los números complejos

Un número complejo no es más que la combinación de un imaginario y un real que se suman o restan, formando una expresión que en aritmética se llama un binomio; así, son ejemplos de complejos las combinaciones 2 + 3i, -1 + i, 34 - 6i, etc. Las soluciones de ecuaciones cuadráticas con discriminante negativo conducen a números complejos.

**Ejemplo 1**: resolver x² + 4x + 5 = 0.

Aplicamos la fórmula [2]:

$x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}=\frac{-4\pm\sqrt{16-20}}2=-2\pm\frac{\sqrt{-4}}2=-2\pm\frac{i\sqrt4}2=-2\pm i$

Hay dos soluciones complejas, -2 + i, -2 - i; a los complejos que tienen iguales sus partes reales pero el signo cambiado de sus partes imaginarias se les llama **complejos conjugados**.

En el ejemplo 1 se ha mostrado que las ecuaciones cuadráticas con discriminante negativo producen soluciones complejas *a + bi,* *a - bi* que son conjugadas; estos complejos tienen las siguientes propiedades interesantes:

Propiedad 1: la suma de complejos conjugados es un número real; (*a + bi) +* (*a - bi) = 2a.*

Propiedad 2: el producto de complejos conjugados es un número real (*a + bi) ·* (*a - bi) = a² + b² +abi + abi = a² + b² *

La segunda propiedad se puede usar para simplificar fracciones de números complejos por el método de multiplicar el denominador por su conjugado.

**Ejemplo 2**: simplificar $\frac{2-3i}{1+2i}$

Multiplicando el denominador por su conjugado:

$\frac{2-3i}{1+2i}\cdot\frac{1-2i}{1-2i}=\frac{\left(2-3i\right)\cdot\left(1-2i\right)}{1^2-\left(2i\right)^2}=\frac{2-4i-3i+6i^2}{1-4i^2}=\frac{2-7i-6}{1+4}=-\frac45-\frac{7i}5.$

#### El plano complejo; forma polar de un complejo

El binomio *a + bi* se puede representar en un plano coordenado, tomando como eje horizontal la recta real, y como eje vertical la recta imaginaria; en la figura 1 vemos el plano, con varios complejos representados por cruces. Por ejemplo el complejo 2 + 2i se representa por el punto (2, 2) en el plano.

![Plano complejo: reales en eje horizontal, imaginarios en eje vertical](http://3.bp.blogspot.com/-PNlXSOKQBO8/UBk6P2PvhWI/AAAAAAAAAhc/-MnFGJN2QV4/s1600/Argand_diagram.gif) fig. 1: Plano complejo: reales en eje horizontal, imaginarios en eje vertical, y algunos puntos en el plano
La representación de los complejos en el plano proporciona una forma alternativa de expresarlos, denominada **forma polar del complejo**: en la figura 2 vemos que para cualquier complejo (a, b) podemos trazar un segmento de recta desde el origen de coordenadas hasta el punto (a, b); este segmento tendrá una longitud r, llamada **módulo del complejo**,  y formará con ele eje de los números reales un ángulo α, llamado **argumento del complejo**. Estos dos números, (r, α), bastan para localizar el punto (a, b), y son la representación en forma polar del complejo a + bi.

![Fig. 2: el número complejo 3 + 4i se representa en el plano complejo como el punto (3, 4), y puede localizarse como el punto que dista del origen una longitud r con un ángulo α respecto al eje horizontal](/taller-matematicas/assets/images/imaginarios.png) Fig. 2: el número complejo 3 + 4i se representa en el plano complejo como el punto (3, 4), y puede localizarse como el punto que dista del origen una longitud r con un ángulo α respecto al eje horizontal
**Cálculo del módulo y del argumento de un complejo**

Usando trigonometría en la figura 2 es evidente que:

$r=\sqrt{a^2+b^2},\;\alpha=\tan^{-1}\left(\frac ba\right)$[2]

En el ejemplo de la figura 2, $r=\sqrt{3^2+4^2}=5,\;\alpha=\tan^{-1}\left(\frac43\right)\approx53^o\approx0.3\pi$. La forma polar de un complejo a + bi suele representarse con la notación $r_\alpha$, en el caso del complejo de la figura 2, será $5_{0.3\pi}$.

Si el punto que representa el complejo z está en el primer cuadrante del plano, el argumento $\alpha$ viene dado directamente por [2], pero si está en otros cuadrantes, habrá que modificarlo según la siguiente tabla (en radianes):

![Los cuatro cuadrantes y las respectivas correcciones al argumento del complejo](/taller-matematicas/assets/images/quadrants.png) Fig. 3: Los cuatro cuadrantes y las respectivas correcciones (en radianes)  al argumento del complejo
En esos casos para usar la tabla de la figura 3 cogeremos los valores absolutos en el cálculo del argumento de la fórmula 2:

$\alpha=\tan^{-1}\left(\frac{\left|b\right|}{\left|a\right|}\right)$

Por ejemplo, el complejo (-1, -2) está en el cuadrante IV; su argumento en radianes será

$2\pi-\tan^{-1}\left(\frac21\right)\approx2\pi-0.35\pi=1.65\pi$.

La forma polar resulta tener ventaja respecto a la binomial a + bi o la del plano (a, b) cuando efectuamos las operaciones de producto, cociente, radiación o exponenciación de complejos; lo vemos en las siguientes propiedades.

**Propiedad 3**: el producto de dos complejos dados en forma polar $r_\alpha, r'_{\alpha'}$ es:

$r_\alpha\cdot r'_{\alpha'}={\left(r\cdot r'\right)}_{\alpha+\alpha'}$[3]

Literalmente: "*el producto de dos complejos tiene como módulo el producto de los módulos y como argumento la suma de los argumentos* ".

**Propiedad 4**: el cociente de dos complejos dados en forma polar $r_\alpha, r'_\alpha'$ es:

$\frac{r_\alpha}{r'_{\alpha'}}={\left(\frac r{r'}\right)}_{\alpha-\alpha'}$[4]

Literalmente: "*el cociente de dos complejos tiene como módulo el cociente de los módulos y como argumento la diferéncia de los argumentos* ".

**Propiedad 5**: La poténcia n-ésima de un complejo $r_\alpha$ es:

$\left(r_\alpha\right)^n={\left(r^n\right)}_{n\alpha}$[5]

Literalmente: "*la n-ésima potencia de un complejo  tiene como módulo la n-ésima potencia del módulo y como argumento el producto de n por el argumento* ".

**Ejemplo 3**: Dados los complejos $z_1=2 + i, z_2=-1 -2i$, calcular $z_1·z_2, z_1/z_2$.

El producto lo podemos hacer directamente usando las expresiones binomiales:

$z_1\cdot z_2=\left(2+i\right)\left(-1-2i\right)=-2-4i-i-2i^2=-5i$.

Para el cociente podemos convertir el denominador en un número real usando su conjugado:

$\frac{z_1}{z_2}=\frac{\left(2+i\right)}{\left(-1-2i\right)}=\frac{\left(2+i\right)}{\left(-1-2i\right)}\frac{\left(-1+2i\right)}{\left(-1+2i\right)}=\frac{-4+3i}5=-\frac45+\frac{3i}5$

Pasemos ahora los complejos a su forma polar usando las fórmulas [2] y las correcciones necesarias de los cuadrantes (el complejo (-1, -2) está en el cuadrante III):

$\begin{array}{l}z_1=\left(2,1\right)\Rightarrow r_1=\sqrt{2^2+1^2}=\sqrt5;\;\alpha_1=\tan^{-1}\left(\frac12\right)\approx0.15\pi;\\z_2=\left(-1,-2\right)\Rightarrow r_1=\sqrt{1^2+2^2}=\sqrt5;\;\alpha_2=\mathrm\pi+\tan^{-1}\left(\frac21\right)\approx1.35\pi\end{array}$

Multiplicamos y dividimos los complejos usando su forma polar:

$\begin{array}{l}z_1={\sqrt5}_{0.15\pi},\;z_2={\sqrt5}_{1.35\pi}\\z_1\cdot z_2={\left(\sqrt5\cdot\sqrt5\right)}_{0.15\pi+1.35\pi}=5_{1.5\pi}==5_{3\pi/2};\\\frac{z_1}{z_2}={\left(\frac{\sqrt5}{\sqrt5}\right)}_{0.15\pi-1.35\pi}=1_{-1.2\pi}=1_{0.8\pi}\end{array}$

El producto y el cociente calculados de las dos formas deben de coincidir; en el caso del producto $z_1·z_2$ se ve a simple vista, pues su argumento 3π/2 nos dice que está sobre el eje imaginario negativo, y siendo su módulo 5 ha de ser  $z_1·z_2=(0,-5)=-5i$ como esperábamos. Para el cociente convertiremos la forma polar $r_\alpha$ a forma binomial a + bi usando que

$\begin{array}{l}a=r\cos\left(\alpha\right)\\b=r\sin\left(\alpha\right)\end{array}$, [6]

lo que resulta es:

$\begin{array}{l}\frac{z_1}{z_2}=1_{0.8\pi}\Rightarrow r=1,\;\alpha=0.8\pi;\\a=1\cdot\cos\left(0.8\pi\right)\approx-0.8;\;b=1\cdot\sin\left(0.8\pi\right)\approx0.6\end{array}$

que coincide con el resultado anterior, pues 4/5 = 0.8 y 3/5 = 0.6.

**Ejemplo 4**: Dado el complejo z = (3, -2), calcular z⁴.

Si lo hacemos usando la forma binomial o bien tenemos que calcular (3 -2i)·(3 -2i)·(3 -2i)·(3 -2i) o bien usamos la regla del [binomio de Newton](https://es.wikipedia.org/wiki/Teorema_del_binomio), pero usando la forma polar y la fórmula [5] los cálculos se acortan:

$\begin{array}{l}z=3-2i\Rightarrow r=\sqrt{9+4}=\sqrt{13},\;\alpha=2\pi-\tan^{-1}\left(\frac23\right)\approx1.82\mathrm\pi;\\\mathrm z^4={\left(\sqrt{13}^4\right)}_{1.82\mathrm\pi\cdot4}={\left(13^2\right)}_{7.28\mathrm\pi}={169}_{1.28\mathrm\pi}\end{array}$

Observar que los ángulos $\alpha$ mayores de 2π los simplificamos tomando el resto de la división entera $\alpha/2\pi$ (equivalentemente, para ángulos de más de 360⁰):

$\begin{array}{l}7.28\mathrm\pi\;\;\;\left|\underline{2\mathrm\pi}\right.\\1.28\mathrm\pi\;\;\;\;\;3\end{array}$

#### Los números complejos no son vectores

Una confusión que debe evitarse es la de tomar un complejo (a, b) como si fuera un vector, no lo es. Los vectores del plano real son también parejas de valores (a, b), pero ambos números son reales, mientras que en un complejo uno de ellos es real y el otro es imaginario. Además, aunque la suma y la resta de vectores y de complejos son formalmente iguales, (a, b) + (c, d) = (a +b, c + d), el resto de operaciones no lo son: para multiplicar dos vectores usamos o bien el producto escalar o bien el producto vectorial, que tienen reglas distintas al producto de dos complejos.

Por otra parte, sí que es verdad que pueden definirse vectores complejos: por ejemplo un vector complejo de dos componentes será una pareja $(z_1,z_2)$ de dos complejos, teniendo cada complejo una componente real y otra imaginaria, por tanto el vector complejo tendrá un total de 4 componentes.

A la recta real (conjunto de todos los números reales) se la suele representar por $\mathbb{R}$ mientras que al plano complejo se le representa por la letra $\mathbb{C}$. Los vectores de n componentes reales se representan por $\mathbb{R}^n$ y los vectores de n componentes  complejos por $\mathbb{C}^n$.

#### Raíces de números complejos

Para hallar la raíz de un número complejo siempre lo haremos a partir de su expresión en forma polar. Para la raíz cuadrada del complejo $\sqrt{r_\alpha}$ tenemos la fórmula:

$\sqrt{r_\alpha}=\left\{\begin{array}{l}{\left(\sqrt r\right)}_\frac\alpha2\\{\left(\sqrt r\right)}_\frac{\alpha+\mathrm\pi}2\end{array}\right.$ [7]

La fórmula general para la raíz n-ésima es:

$\sqrt[n]{r_\alpha}={\left(\sqrt[n]r\right)}_\frac{\alpha+k\mathrm\pi}n,\;k=0,1,\dots,n-1$[8]

que nos proporciona n raíces.

**Ejemplo 5**: Calcular $\sqrt[3]{27-9i}$

Convertimos el complejo *z = 27 - 9i* a forma polar:

$z=27-9i\Rightarrow r=\sqrt{27^2+9^2}=9\sqrt{10};\;\alpha=2\pi-\tan^{-1}\left(\frac9{27}\right)\approx1.9\pi$

Aplicamos [8]:

$\begin{array}{l}\sqrt[3]{9{\sqrt{10}}_{1.9\mathrm\pi}}={\left(\sqrt[3]{9\sqrt{10}}\right)}_\frac{1.9\mathrm\pi+k\mathrm\pi}3,\;k=0,1,2\;\Rightarrow\\3.{05}_\frac{1.9\mathrm\pi}3,\;3.{05}_\frac{2.9\mathrm\pi}3,\;3.{05}_\frac{3.9\mathrm\pi}3\end{array}$

Ya sabemos que podemos recuperar la expresión binomial / punto del plano aplicando [6], por ejemplo para la primera raíz:

$z=3.{05}_\frac{1.9\mathrm\pi}3\Rightarrow z=3.05\left(\cos\left(\frac{1.9\mathrm\pi}3\right)+i\sin\left(\frac{1.9\mathrm\pi}3\right)\right)\cong\left(-1.22,2.78\right)$

#### Algunas aplicaciones prácticas de los números complejos

 Hemos visto que al multiplicar un complejo $z=r_\alpha$ por otro $z'=r'_{\alpha'}$ el resultado z·z' tiene un argumento que es la suma de los anteriores, $\alpha+{\alpha'}$; esto puede verse como si el complejo z' girara al complejo z un ángulo ${\alpha'}$. Así pues, el producto de complejos puede verse en parte como una rotación.

Sucede que en la ciencia y en la técnica nos encontramos con muchos sistemas que están en movimiento oscilatorio: la corriente alterna, vibraciones de máquinas, oscilaciones de estructuras (puentes, edificios, ...), ondas de todo tipo (sísmicas, electromagnéticas), moléculas en un sólido, etc. etc. Y el movimiento oscilatorio puede describirse usando composiciones de rotaciones, y las funciones trigonométricas.  Por ejemplo, la amplitud de las oscilaciones producidas por una onda simple puede expresarse por $y(t)=A\sin\left(\omega t+\theta\right)$[9]; pero en casos reales nos encontramos con cosas complicadas como superposición de ondas, ondas que se amortiguan debido a la resistencia del medio, ondas forzadas por un elemento impulsor, etc. Si usamos la expresión [9] para estos casos los cálculos algebraicos se vuelven largos y pesados; es aquí cuando los números complejos acuden en nuestra ayuda, simplificando las expresiones. En el caso de la onda simple, puede expresarse como una exponencial compleja, $y(t)=Ae^{\left(\omega t+\theta\right)i}$, más fácilmente manipulable que la expresión [9] con sus funciones seno y coseno.

Así pues, en toda aplicación práctica en que tengamos oscilaciones complicadas, los complejos serán de ayuda. Y esto sucede en estos casos, entre otros:

 	- La [impedancia](https://es.wikipedia.org/wiki/Impedancia), que es una medida de la oposición que presenta un circuito a una corriente eléctrica, de forma parecida a la resistencia eléctrica (la generaliza); cuando la corriente es alterna y variable con el tiempo, la impedancia se representa como una cantidad compleja.

 	- En la [resolución de ecuaciones diferenciales lineales](http://tallermatematic.ovh/wp/index.php/2015/04/26/edos-lineales-de-orden-superior/#EDO_lineales), muy frecuente en ciencia y técnica, aparecen raíces complejas, que indican precisamente la existencia de soluciones oscilantes.

 	- En Física Cuántica, la [ecuación de Schrödinger](https://es.wikipedia.org/wiki/Ecuaci%C3%B3n_de_Schr%C3%B6dinger) nos proporciona la evolución en el tiempo y el espacio de la onda de probabilidad de una partícula, usando número complejos (observar que incluye el número imaginario i):

![Ecuación de Schrödinger (fuente: Wikipedia)](https://wikimedia.org/api/rest_v1/media/math/render/svg/327546c3f8bd78d7d533c5c04f7602086862dfd4) Ecuación de Schrödinger (fuente: Wikipedia)

 	- En la teoría de la Relatividad restringida, una de las formas de presentarla es a través del espacio-tiempo de Minkowski, en el cual el tiempo se toma como si fueran números imaginarios; también en Relatividad General, y en Cosmología, se usan tiempos que son números imaginarios, no por motivos "esotéricos", si no para simplificar las complicadas ecuaciones de la relatividad. Ver por ejemplo mi post [La naturaleza del espacio y del tiempo (II)](http://matfisfil.blogspot.com/2012/08/la-naturaleza-del-espacio-y-del-tiempo.html).
{% endraw %}