---
layout: post
title: "Funciones"
date: 2015-05-08 09:24:03 +0000
math: true
---
{% raw %}

Este post es una breve  introducción a la teoría de funciones, un tema extenso, que aquí solo pretende repasar y aclarar algunos conceptos que, quizás, no han quedado claros o no se han visto en el bachillerato y en cambio se dan por sabidos en los primeros cursos de carrera.

	- Relaciones entre conjuntos

	- Correspondencia inversa

	- Relaciones inyectivas, exhaustivas y biyectivas

	- Funciones.

	- Función inversa

	- Composición de funciones

	- Relación entre función inversa y composición

	- Aplicaciones prácticas de la composición y la inversa de funciones

	- Tipos de funciones

	- 
Ecuaciones trascendentes: inversas  de funciones trascendentes especiales

[![separador2](/taller-matematicas/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

# Relaciones entre conjuntos

En teoria de conjuntos, una relación o una correspondencia,, es una regla R o conjunto de reglas que nos definen cómo asignar a objetos de un conjunto O otros objetos de un conjunto D. La notación suele ser $O\xrightarrow RD$ o bien, considerando los elementos x, y de O, D respectivamente, por $x\in O\xrightarrow Ry\in D$ o más brevemente por $y=R(x)$.  Se suele recurrir a los [diagramas de Venn](http://es.wikipedia.org/wiki/Diagrama_de_Venn) para representar gráficamente una correspondencia entre conjuntos:

[caption id="attachment_1049" align="alignnone" width="300"][![Correspondéncia entre dos conjuntos](/taller-matematicas/assets/images/correspondencia-300x294.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/05/correspondencia.png) Figura 1: Correspondencia entre dos conjuntos[/caption]
En una correspondencia R pueden haber tanto elementos de O como de D que no participen en R; denominamos dominio de R al subconjunto de elementos de O que están relacionados con elementos de D, y recorrido de R al subconjunto de elementos de D que están relacionados con elementos de O. También pueden haber elementos de O que estén relacionados con varios elementos de D, y elementos de D relacionados con varios elementos de O.

**Ejemplo 1**: Definimos una relación R entre el conjunto de los números reales $\mathbb{R}$ y el de los enteros $\mathbb{Z}$ por las siguientes reglas:

	- Si  $x\in\mathbb{R}$ es negativo o cero, le hacemos corresponder el número entero cero

	- Si  $x\in\mathbb{R}$ es entero positivo y par, le hacemos corresponder el número entero 1

	- Si  $x\in\mathbb{R}$ no entra en ninguno de los casos anteriores, le hacemos corresponder el número entero obtenido tomando sólo la parte entera de x y truncando los decimales

Ejemplos de esta correspondencia: a x=-2 le corresponde el 0, a x=6 le corresponde el 1, a x=π le corresponde el entero 3. El dominio de esta relación R son todos los reales, y el recorrido todos los enteros no negativos.

### Correspondencia inversa

Si tenemos una correspondencia R entre los conjuntos A, B, entonces para cada valor x de A que tenga alguna imagen en B podemos escribir  $y=R(x)$ para algún y de B; entonces definimos la correspondencia inversa $R^{-1}$ por  $R^{-1}(y)=x$. Al elemento x le llamamos la antimagen de x.

**Ejemplo 2**: Dada la relación R del ejemplo 1, la relación inversa $R^{-1}$ seguirá las siguientes reglas:

	- Al número cero le hacemos corresponder todos los reales no positivos

	- Al entero 1 le corresponde todos los entero positivo y pares, y todo el intervalo abierto (0, 2)

	- A cada entero z > 1 le corresponde el intervalo (z, z+1)

###  Relaciones inyectivas, exhaustivas y biyectivas

Según el número de imágenes que tenga cada elemento, tenemos las siguientes clasificaciones:

	- Una aplicación es inyectiva si cada elemento de B es la imagen de como máximo un elemento de A

	- Una aplicación es exhaustiva si cada elemento de B es la imagen de como mínimo un elemento de A

	- Una aplicación es biyectiva si cada elemento de B es la imagen de exactamente un elemento de A

Esta clasificación no incluye a todas las relaciones: hay relaciones que no pertenecen a ninguna de estas categorías.
**Ejemplo 3**:  La relación del ejemplo 1 es claramente exhaustiva, pues a cada entero de B le corresponde un mínimo de un elemento real de A (de hecho infinitos). La relación del ejemplo 2 no es ni inyectiva, ni exhaustiva, ni biyectiva. La relación que asigna a cada número entero su cuadrado, $x\xrightarrow Rx^2$, es biyectiva.

# Funciones.

Una función (o aplicación) entre dos conjuntos A, B es* una relación R en la cual para cada x de A existe un único y de B que se corresponde con x*. Lo contrario no tiene porque cumplirse: a cada y de B le puede corresponder cualquier número de elementos de A. En vez de usar la letra R se suelen usar las letras f, g, h ,... para representar funciones.

**Ejemplo 4**: En el ejemplo de la figura 1, la correspondencia R no es una aplicación, pues hay un elemento de O al cual le corresponde más de un elemento de D. En cambio la relación R del ejemplo 1 sí es una aplicación. Cuando una relación es una aplicación, a los elementos y de B les llamamos las imágenes de los elementos x por la aplicación R.

**Ejemplo 5**: La relación del ejemplo 1 es una aplicación exhaustiva de los números reales en los enteros no negativos, pues las imágenes son los enteros no negativo, y cada uno de ellos está relacionado con más de un número real, de hecho, con infinitos. Por otro lado, cada número real tiene asociado una única imagen. Por ejemplo, el intervalo real [2, 3) contiene infinitos reales, y todos ellos están relacionados con el entero y=2.

**Ejemplo 6**: La aplicación f que hace corresponder a cada cuadrado de lado L el valor de su área, y = f(x) = L², es una aplicación biyectiva, pues a cada real L corresponde un y = L² único, y viceversa, a cada área L² le corresponde un único cuadrado de lado L.

**Ejemplo 7**: La aplicación f del conjunto A de los reales positivos en el conjunto B de los reales que relaciona cada  x con su raíz $y = f(x) = \sqrt x$ es inyectiva, pues hay elementos de B que no corresponden con ningún elemento de A (los números negativos no son la raíz de ningún real positivo) y los que sí son raíces de algún x lo son de uno y solo uno.

### Función inversa

Dada una función f definimos su función inversa $f^{-1}$ de la misma forma que para las relaciones inversas: dada una imagen y cualquiera tal que y = f(x), entonces $x = f^{-1}(x)$. A diferencia de las relaciones, en las que la relación inversa siempre existe, la existencia de la función inversa no está asegurada: debido a la restricción que ha de cumplir toda aplicación, * para cada x de A existe un único y de B que se corresponde con x, *la inversa de una aplicación f será también una aplicación si y sólo si f es inyectiva o biyectiva. Si la función es exhaustiva, entonces su inversa será una relación, pero no una función.

**Ejemplo 8**: La aplicación f del ejemplo 7 es inyectiva, por tanto tiene función inversa; para determinarla, planteamos $y=f(x)=\sqrt x\Leftrightarrow x=y^2$, entonces la inversa asigna a cada número real x su cuadrado x².

### Composición de funciones

Sean dos funciones f, g y tomemos la imagen y=f(x);
 si aplicamos la función g a la imagen obtenemos un nuevo valor $z=g(y)=f\left(g\left(x\right)\right)$. A la aplicación sucesiva, encadenada, de funciones, le llamamos composición de funciones, y lo notamos por $z=g(y)=f\left(g\left(x\right)\right)=f\circ g\left(x\right).$

La composición de dos funciones $f\circ g$ solo es posible *si el conjunto recorrido de g está incluido en el dominio de f. *Además*, *al componer funciones el dominio y el recorrido de la función compuesta quedará restringido por sus funciones componentes.

**Ejemplo 9**: La función f(x) = x² tiene como dominio todos los reales y como recorrido los números reales positivos, lo simbolizamos por $\begin{array}{l}\mathbb{R}\;\xrightarrow{x^2}\;\mathbb{R}^+\\\end{array}$,  mientras que la función g(x) = 1/x tiene por dominio todos los reales excepto el cero y por recorrido todos los reales: $\begin{array}{l}\mathbb{R}_0\;\xrightarrow{1/x}\;\mathbb{R}\\\end{array}$.

Cuando componemos las dos funciones en el orden $f\circ g$, el recorrido de g está incluido en el dominio de f; el dominio de la función compuesta coincide con el de g: todos los reales excepto el cero, y su recorrido será el mismo que el de f: todos los reales positivos. Su expresión será $f\circ g\left(x\right)=f\left(\frac1x\right)=\frac1{x^2}.$

Cuando componemos las dos funciones en el orden $g\circ f$, el recorrido de f incluye el cero, que no pertenece al dominio de g, por tanto del dominio de la función compuesta tenemos que excluir el cero, $\mathbb{R}_0$;  su recorrido será el mismo que el de g: todos los reales positivos. Su expresión será $\begin{array}{l}g\circ f\left(x\right)=g\left(x^2\right)=\frac1{x^2}\;,\;x\neq0\\\end{array}.$

En el último ejemplo el resultado de las composiciones $f\circ g$ y $g\circ f$ coinciden, pero en general no es así: $f\circ g\neq g\circ f.$

Ejemplo 10: El resultado de la composición de la función exponencial $e^x$ y la función cuadrática $x^2$ depende del orden; en efecto, $e^x\circ x^2=e^{x^2}$, pero $x^2\circ e^x=\left(e^x\right)^2=e^{2x}.$

### Relación entre función inversa y composición de funciones

 Si una función f tiene inversa $f^{-1}$, entonces se cumple que $f\circf^{-1}=f^{-1}\circf=Id$, donde denotamos por Id la función identidad: $Id(x)=x$. Además, la función inversa es la única función que cumple esta regla:

**Proposición 1**: Sean dos funciones f, g; si se cumple que $f\circ g=g\circ f=Id$, entonces f, g son una inversa de la otra: $f^{-1}=g, g^{-1}=f$.

En general, para dos funciones f, g cualquiera que tengan inversa, se cumple:

**Proposición 2**: $\left(f\circ g\right)^{-1}=g^{-1}\circ f^{-1}$

 **Ejemplo 11:** comprobar que la función inversa de $y=f\left(x\right)=\sqrt x$ es $y=x^2$. Componemos las dos funciones en los dos sentidos, debería resultar la función identidad:

$\begin{array}{l}\sqrt x\circ x^2=\sqrt{x^2}=x;\\x^2\circ\sqrt x=\left(\sqrt x\right)^2=x.\end{array}$

## Aplicaciones prácticas de las funciones inversas

Frecuentemente en los problemas necesitamos resolver ecuaciones que incluyen funciones, y para resolver la ecuación puede ser necesario utilizar la inversa de las funciones y la composición.
**Ejemplo 12**: La tensión en un circuito RC en corriente continua viene dada por $V(t)=V_0e^{-t/RC}$; cuando se establece la corriente el condensador está descargado y la tensión es máxima: $t=t_0, V=V_0$. A medida que circula corriente el condensador adquiere carga eléctrica que produce un campo eléctrico de signo contrario al de la corriente que lo carga, oponiéndose a la corriente, y reduciendo la tensión V. Teóricamente este proceso de carga no termina nunca, pero en la práctica V se reduce muy rápidamente. Un problema típico consiste en responder preguntas como por ejemplo: ¿cuánto tiempo tardará la tensión en caer a la mitad de su valor inicial?

[caption id="attachment_1067" align="alignnone" width="192"][![Circuito RC](/taller-matematicas/assets/images/Screenshot-from-2015-05-07-144723.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/05/Screenshot-from-2015-05-07-144723.png) Circuito RC, fuente: Wikipedia[/caption]
Planteamos la ecuación $\frac12V_0=V_0e^{-t/RC}\Leftrightarrow\frac12=e^{-t/RC}$. Para "despejar" t de esta igualdad usamos la función inversa y la composición de funciones del siguiente modo: la inversa de la función (trascendente) exponencial $e^x$ es la función (trascendente) logaritmo natural $\ln\left(x\right)$. Aplicando la proposición 1 obtenemos $\ln\left(x\right)\circ e^x=e^x\circ\ln\left(x\right)=x$. Entonces, tomando la igualdad $\frac12=e^{-t/RC}$ como una igualdad entre funciones $f(t)=\frac12=g(t)=e^{-t/RC}$, les aplicamos a ambas la composición con la función $\ln\left(t\right):$

$\begin{array}{l}\ln\left(t\right)\circ f(t)=\ln\left(t\right)\circ\frac12=\ln\left(t\right)\circ g(t)=\ln\left(t\right)\circ e^{-t/RC}\Rightarrow\\\ln\left(\frac12\right)=-t/RC\end{array}$

De esta ecuación obtenemos fácilmente $t=-RC\cdot\ln\left(\frac12\right)$; aplicando la propiedad $\ln\left(\frac AB\right)=\ln\left(A\right)-\ln\left(B\right)$ y sabiendo que $ln(1)=0$, obtenemos finalmente $t=RC\cdot\ln\left(2\right).$

 Habitualmente en el proceso de obtener una incógnita x de una ecuación en la que tenemos una función f(x) tal como $f(x)=c$ por medió de la inversa $f^{-1}\left(x\right)\circ f\left(x\right)=f^{-1}\left(x\right)\circ c\Leftrightarrow x=f^{-1}\left(x\right)\circ c$ se omite decir que estamos haciendo precisamente eso, aplicar las propiedades de las inversas y la composición de funciones, pero realmente la base matemática es la que hemos expuesto.

## Tipos de funciones

Se denominan **funciones algebraicas** a aquellas que pueden expresarse por una secuencia de operaciones algebraicas (+, -, X, /) o bien por composición o inversión de expresiones algebraicas. Ejemplos: $f(x)=3x^2-5x+1,\;g(x)=\frac{x-1}{3x^2-5x+1},h(x)=f\circ g\left(x\right),\;\cdots.$

Se denominan **funciones trascendentes** a aquellas que no son algebraicas. Ejemplos: la función exponencial y=e^x, las trigonométricas $f(x)=\sin\left(x\right),\;g\left(x\right)=\cos\left(x\right),\;h\left(x\right)=\tan\left(x\right),\dots$, la función logaritmo, etc. Al no tener expresión algebraica, en general no existe un método para obtener las inversas de las funciones trascendentes, que a su vez también serán trascendentes.

Las funciones que vienen dadas en** forma explícita** son de la forma y=f(x); en cambio las funciones en **forma implícita** tienen la expresión F(x,y)=0, y no siempre pueden convertirse a forma explícita. Ejemplo: $F(x,y)=e^y\cos(x)-1=0$ define y como función de x de forma impĺicita, y  en este caso puede convertirse a forma explícita operando: $e^y\cos\left(x\right)-1=0\Leftrightarrow e^y=\frac1{\cos\left(x\right)}\Leftrightarrow y=\ln\left(\left|\frac1{\cos\left(x\right)}\right|\right).$

Las **funciones analíticas** son aquellas que pueden expresarse como una suma infinita de la forma $f(x)=a_0+a_1\left(x-x_0\right)+\cdots+a_n\left(x-x_0\right)^n+\cdots.$ La mayoria de funciones trascendentes son analíticas. El que una función sea analítica tiene implicaciones respecto a su derivabilidad: se dice que toda función analítica es "suave", significando es derivable con derivada continua.

##  Ecuaciones trascendentes: inversas  de funciones trascendentes especiales

En las aplicaciones prácticas a menudo se encuentran ecuaciones en las que se igualan funciones trascendentes distintas; al no poder simplificarse mediante operaciones algebraicas, a veces sólo podemos ver que sucede si invertimos las funciones, esperando que las inversas nos den más información.

**Ejemplo 13**: La ecuación $\ln\left(x\right)=Ax^B$ es trascendente, pues iguala entre sí dos funciones trascendentes diferentes. La solución en este caso se puede obtener usando la función inversa de $xe^x$, que es la denominada **función [W
 de Lambert](http://mathworld.wolfram.com/LambertW-Function.html)**: $\left(xe^x\right)^{-1}=W(x)$; usando esta función puede demostrarse que $\ln\left(x\right)=Ax^B\Rightarrow x=exp\left(-\frac{W\left(A\cdot B\right)}B\right)$. Siendo W también una función trascendente, no tenemos una expresión algebraica que nos permita obtener sus valores, que deben ser obtenidos mediante algoritmos computacionales. La función W la encontramos en diversas aplicaciones, como por ejemplo la relación entre el voltaje, corriente y resistencia en un diodo, trayectorias de proyectiles balísticos en presencia de resistencia del aire,  ingeniería de películas delgadas o hidrología.

# Bibliografía
{% endraw %}