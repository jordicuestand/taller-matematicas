---
layout: post
title: "Espacios vectoriales"
date: 2016-11-02 08:09:48 +0000
categories:
  - "Álgebra"
  - "Matemáticas"
tags:
  - "álgebra vectorial"
  - "base"
  - "espacio vectorial"
  - "Grassmann"
  - "subespacio vectorial"
  - "suma directa"
  - "vector"
math: true
---
{% raw %}

**Competencias**:

 	- Distinguir vectores linealmente independientes, de vectores linealmente dependientes.

 	- Determinar bases de subespacios vectoriales concretos.

**Conceptos**:

 	- Conocer las estructuras de espacio vectorial y subespacio vectorial.

# Dependencia e independencial lineal de vectores

**Definición 1**: Un vector $\overrightarrow v$ es una **combinación lineal de los vectores** ${\overrightarrow u}_1,{\overrightarrow u}_2,\cdots,{\overrightarrow u}_n$, si existen *n* números reales (o *escalares*) tales que se cumple $\overrightarrow v=c_1{\overrightarrow u}_1+c_2{\overrightarrow u}_2+\cdots+c_n{\overrightarrow u}_n$

**Ejemplo 1**: El vector $\overrightarrow w=(2,4,6)$ se obtiene del vector $\overrightarrow v=(1,3,6)$ por multiplicación por el escalar 2:  $\overrightarrow w=2\cdot \overrightarrow v$. Luego $\overrightarrow w$ es combinación lineal de un único vector $\overrightarrow v$, con $c=2$

**Ejemplo 2**: El vector $\overrightarrow w=(2,4,6)$ no puede ser combinación lineal de los vectores $\overrightarrow v_1=(1,0,0),\overrightarrow v_1=(0,1,0)$, pues $\left(2,4,6\right)=c_1\left(1,0,0\right)+c_2\left(0,1,0\right)$ implica que, tomando componentes uno a uno, $2=c_1,\;4=c_2,\;6=0$, lo cual no tiene sentido.

**Definición 2**: Cuando un vector $\overrightarrow v$ sea una combinación lineal de otros vectores, diremos que **el conjunto** $\left\{\overrightarrow v,{\overrightarrow u}_1,{\overrightarrow u}_2,\cdots,{\overrightarrow u}_n\right\}$ **es linealmente dependiente**.

**Ejemplo 3**:  El vector $\overrightarrow w=(2,4,6)$ del ejemplo 1, junto con el vector  $\overrightarrow v=(1,3,6)$, forman un conjunto $\left\{\overrightarrow v,\overrightarrow w\right\}$ linealmente dependiente.

Determinar si un conjunto dado de vectores ${\overrightarrow u}_1,{\overrightarrow u}_2,\cdots,{\overrightarrow u}_n$ es linealmente dependiente  pasa por ver si alguno de sus vectores puede expresarse como combinación lineal de los demás; esto puede ser pesado de comprobar. Afortunadamente, la siguiente propiedad nos facilita el trabajo:

**Propiedad 1**: dado un conjunto de vectores ${\overrightarrow u}_1,{\overrightarrow u}_2,\cdots,{\overrightarrow u}_n$ será linealmente dependiente si existe una combinación lineal de todos ellos que sea igual al vector nulo, $c_1{\overrightarrow u}_1+c_2{\overrightarrow u}_2+\cdots+c_n{\overrightarrow u}_n=\overrightarrow 0$, sin que sean todos los coeficientes $c_1,c_2,...c_n$ todos nulos.

**Ejemplo 4**:  Los vectores $\overrightarrow w=(2,4,6),\overrightarrow v_1=(1,0,0),\overrightarrow v_1=(0,1,0)$ no son linealmente dependientes, pues si intentamos aplicar la propiedad 1, todos los coeficientes de anulan:

$\begin{array}{l}c_1\left(2,4,6\right)+c_2\left(1,0,0\right)+c_3\left(0,1,0\right)=\left(0,0,0\right)\Leftrightarrow\\\left.\begin{array}{r}\begin{array}{l}2c_1+c_2=0\\4c_1+c_3=0\\6c_1=0\end{array}\\\end{array}\right\}\Rightarrow c_1=0,\;c_2=0,\;c_3=0\end{array}$

**Definición 3**: si un conjunto de vectores no es linealmente dependiente, diremos que es un conjunto **linealmente independiente**.

**Ejemplo 5**: El conjunto de vectores del ejemplo 4 es linealmente independiente.

**NOTA 1**: geométricamente, se puede visualizar la dependencia o independencia lineal usando la regla del paralelogramo para la suma de vectores; en la figura 1, el vector w puede verse como la diagonal de un paralelogramo  formado por los vectores u, v, convenientemente "alargados" según unos coeficientes, con ello concluimos que {u, v, w} son linealmente dependientes, pues existe una combinación lineal que expresa w en función de u, v. Equivalentemente, si {u, v, w} son linealmente dependientes, significa que existe una combinación, que en la figura es w = 2u + v; entonces es inmediato que puede hacerse w - 2u - v = 0, una combinación lineal con los escalares 1, -2, -1 que resulta ser cero, con coeficientes no todos nulos, y por la propiedad 1 el conjunto {u, v, w} es linealmente dependiente (l.d.)

$caption id="attachment_150244" align="aligncenter" width="387"$![Fig.1 : vectores linealmente dependientes](/taller-matematicas/assets/images/dependencia_lineal.png) Fig.1 : Con dos vectores linealmente independientes en el plano puede formarse un paralelogramo; un tercer vector será necesariamente dependiente de los dos primeros, pues podrá expresarse en función de ellos mediante la regla del paralelogramo para la suma de vectores.[/caption]
En el plano los vectores tienen sólo dos componentes; implica que, geométricamente, dos vectores u, w del plano son l.d. si y sólo si no se puede formar con ellos ningún paralelogramo, o sea, si u, w están en la misma recta (son *colineales*). Con vectores de tres componentes distintos, podremos tener un conjunto l.d. si y sólo si no podemos formar un paralelepípedo con ellos, o sea, si dos de ellos, al menos, son colineales (figura 3).

$caption id="attachment_150246" align="aligncenter" width="298"$![Fig. 2: dependencia lineal con vectores en el espacio; tres vectores pueden ser linealmente independientes si forman un paralelepípedo, un cuarto vector siempre se podrá expresar como una combinación lineal de los anteriores.](/taller-matematicas/assets/images/dependencia_lineal2.png) Fig. 2: dependencia lineal con vectores en el espacio; tres vectores pueden ser linealmente independientes si forman un paralelepípedo, un cuarto vector siempre se podrá expresar como una combinación lineal de los anteriores.[/caption]
# Espacios vectoriales

**Definición 4**: un **espacio vectorial** es una estructura matemática formada por un conjunto de vectores, un conjunto de escalares, una operación suma entre vectores (con las propiedades habituales de la suma: asociativa, conmutativa, elemento neutro y elemento inverso), y una operación producto de vector por escalar con las propiedades distributiva *a(**u** + **v**) = a**u** + a**v***, *(a + b)**u** = a**u** + b***u**,  asociativa *(ab)**u** = a(b**u**)*, y elemento neutro escalar *1**u** = **u*** (los vectores se indican en negrita, los escalares en letra normal).

**Ejemplo 6**: El sistema de dos ecuaciones con dos incógnitas

$\left.\begin{array}{r}c_1^1x_1+c_2^1x_2=0\\c_1^2x_1+c_2^2x_2=0\end{array}\right\}$

si admite una solución $x_1,\;x_2$ significa que al sustituir esos valores en las ecuaciones se cumplen las igualdades; si existe una segunda solución$x_1^',\;x_2^'$ distinta de la primera, entonces la suma $x=\left(x_1+x_1^'\right),\;y=\left(x_2+x_2^'\right)$ también será una solución, así como su producto por cualquier escalar  k (numero real), $kx=\left(x_1+x_1^'\right),\;ky=\left(x_2+x_2^'\right)$. Definiendo como vectores (x, y) a las soluciones del sistema, con la operación suma de soluciones y producto por un real k, el conjunto de soluciones del sistema es un espacio vectorial.

**Ejemplo 7**: los vectores del plano real, con la suma habitual (a, b) + (c, d) = (a + b, c + d), y el producto de un vector por un escalar k, k(a, b) = (ka, kb), es un espacio vectorial; esta suma vectorial coincide con la regla del paralelogramo usada para sumar vectores en Física.

**NOTA 2**: Estrictamente hablando, en Álgebra se definen los espacios vectoriales V (conjunto de vectores) sobre un "cuerpo" de escalares K, donde la palabra *cuerpo* denota otra estructura algebraica formada por un conjunto y unas operaciones; aquí estamos suponiendo que el cuerpo de escalares es el conjunto de los números reales$\mathbb{R}$, y que los vectores están formados por listas ordenadas de números reales (a, b, c, ...): son espacios vectoriales reales sobre el cuerpo de los reales, $\mathbb{R}$. Pero en general pueden definirse espacios vectoriales más abstractos, por ejemplo, podemos definir un espacio de vectores complejos y usar como cuerpo escalar el conjunto de números racionales $\mathbb{Q}$.

### Conjuntos, o sistemas de vectores, generadores del espacio, y bases del espacio. Dimensión de un espacio vectorial.

Hay una importante relación entre espacios vectoriales y el concepto de dependencia/independencia lineal, que nos viene dada por la siguiente propiedad:

**Propiedad 2**: los (posiblemente infinitos) vectores de un espacio vectorial pueden obtenerse a partir de un número limitado de algunos de sus vectores, por combinación lineal de ellos.  Tal conjunto de vectores se denomina **conjunto generador** del espacio.

**Ejemplo 8**: Los vectores (1,1), (-1,0), (0,3) forman un sistema generador de todos los vectores del espacio vectorial $V_2$ de vectores reales (x,y), ya que siempre podremos encontrar coeficientes escalares a, b, c tales que (x,y) = a(1,1) + b(-1,0) +  c(0,3) para cualquier vector (x, y).

Se pueden formar muchos sistemas generadores válidos para cualquier espacio vectorial $V_n$, con un número variable de vectores; ahora bien, vimos en el apartado anterior que en $V_2$ se necesitan como mínimo dos vectores para formar, por combinación lineal (o la regla del paralelogramo) el resto de vectores (fig. 1), y en el caso de $V_3$ se necesitan tres vectores (fig.2). Cuando un sistema generador tiene el mínimo posible de vectores, se denomina una **base del espacio vectorial**.

**Ejemplo 9**: Los vectores (1,1), (-1,0), (0,3) del ejemplo 8 son  un sistema generador de $V_2$, pero no son base, pues el mínimo necesario de vectores reales en $V_2$ hemos visto que es dos. Si cogemos el sistema de dos vectores {(1,1), (-1,0)}, como son independientes (no son colineales, si lo fueran, sus componentes serian proporcionales) generan también todo $V_2$, luego son una base. Tomando el sistema {(-1,0), (0,3)} vemos que también son independientes, luego son base.

**Definición 5**: el número de vectores que contiene cualquier base de un espacio vectorial $V_n$ se llama **dimensión del espacio**.

**NOTA 3**: todas las bases de un espacio tienen el mismo número de vectores siempre que el espacio vectorial sea de dimensión finita; para espacios de dimensión infinita no es cierto. Un ejemplo importante de espacio de dimensión infinita es el [espacio de Hilbert](https://es.wikipedia.org/wiki/Espacio_de_Hilbert),  con diversas aplicaciones científicas.

# Subespacios vectoriales

Si tomamos una parte de los vectores de un espacio vectorial de dimensión n, $V_n$, ¿es posible que ese subconjunto de vectores sea también un espacio vectorial?  Para serlo, debería cumplir las condiciones de la definición 4. La siguiente propiedad nos da una herramienta más directa para saberlo.

**Propiedad 3**: dado un subconjunto W de los vectores de $V_n$, W será espacio vectorial si y sólo si se cumple que:

1 - para cualquier par de vectores **u**, **w** de W, el vector **u** + **w** también pertenece a W

2- para cualquier vector **u** de W, y cualquier escalar k, se cumple que el vector k**u** también pertenece a W

Cuando tal subconjunto W sea también espacio vectorial, diremos que es un **subespacio vectorial** de $V_n$.

**Ejemplo 10**: Tomemos el subconjunto de vectores W de $V_2$ expresados por c·(1, 1), donde c es un escalar cualquiera. Geométricamente, W es una recta que pasa por el origen y por el punto (1, 1). ¿Es subespacio vectorial? Veamos: dos vectores cualesquiera de W serán c(1, 1) y c'(1, 1), si los sumamos obtenemos c(1, 1) + c'(1, 1) = (c + c')(1, 1) que también pertenece a W, pues c + c' es un escalar. Por otra parte, k·c(1, 1) = (k·c)(1, 1) que también es de W, Luego por la propiedad 3, W es subespacio vectorial de $V_2$

En general, la dimensión de un subespacio vectorial W será menor que la del espacio total V; de hecho, si fueran iguales, entonces el subespacio no es tal, sino que hay una igualdad, W = V. También en general, dada una base de V, no será una base de W. En cambio, si tomamos cada vector de la base de V, y generamos todos los vectores posibles por combinación lineal, sí obtenemos subespacios vectoriales:

**Propiedad 4**: si tenemos una base de $V_n$, con n vectores, entonces las combinaciones lineales de esos vectores, tomados de uno en uno, de dos en dos, etc, forman subespacios vectoriales de dimensiones uno, dos, etc.

**Ejemplo 11**: una base de $V_3$ es {**u**=(1,0,0), **v**=(-1, 1,0), **w**=(0,1,1)}; las combinaciones lineales de uno en uno  k**u**, k**v**, k**w **con k un escalar cualquiera forman tres subespacios vectoriales de dimensión 1 (son rectas que pasan por el origen), las combinaciones lineales de dos en dos  a**u** + b**v,** a**u** + b**w**, a**v** + b**w**, con a,b escalares cualesquiera, forman tres subespacios vectoriales de dimensión 2 (son planos que pasan por el origen), y si tomamos los tres vectores, a**u** + b**v** + c**w**, el subespacio generado coincide con el espacio total $V_3$.  Por ejemplo, (x, y, z) = a(1,0,0) + b(-1, 1,0) = (a-b, -b, 0) es un subespacio vectorial de dimensión 2 en  $V_3$: un plano que pasa por el origen de coordenadas.

###  Unión e intersección de subespacios vectoriales

Los conjuntos admiten las operaciones de unión e intersección; siendo los subespacios vectoriales subconjuntos, es lógico pensar que también admitirán esas operaciones. No obstante, se presenta una dificultad con las uniones de subespacios: si prolongamos dos vectores u, v distintos, obtenemos dos rectas U, W (figura 3), cada recta es un subespacio vectorial de dimensión 1, generado por el vector correspondiente. La intersección de las dos rectas es un punto, que se puede hacer corresponder con un subespacio de dimensión cero, pero la unión de las dos rectas (el conjunto de puntos que pertenece a U o a W) no cumple la condición 1 de la propiedad 3: para cualquier par de vectores **u**, **v** de $U\cup W$, el vector **u** + **v** no pertenece a$U\;\cup\;W$, pues vemos en la figura que la suma **u** + **v** por la regla del paralelogramo no pertenece ni a U ni a W.

$caption id="attachment_150251" align="aligncenter" width="417"$![Fig. 3: dos rectas obtenidas por prolongación de dos vectores independientes generan dos subespacios vectoriales](/taller-matematicas/assets/images/subespais.png) Fig. 3: dos rectas obtenidas por prolongación de dos vectores independientes generan dos subespacios vectoriales[/caption]

Tenemos la siguiente propiedad para las uniones e intersecciones de subespacios vectoriales:
**Propiedad 5:** La intersección  $U\cap W$ de subespacios vectoriales U, W siempre será también un subespacio vectorial, pero la unión $U\cup W$ no lo será, excepto en casos especiales.

Para solventar esta dificultad con las uniones de subespacios se recurre a definir otro subespacio vectorial que incluya a los vectores de $U\cup W$ más los mínimos adicionales que aseguren que se cumplen las condiciones exigidas por la propiedad 3. La siguiente propiedad nos dice como lograrlo.

**Propiedad 6: **dados dos subespacios U, V, el mínimo subespacio vectorial que incluye todos los vectores de la unión $U\cup W$ es el generado por el conjunto $\left\{u+v\;\vert\;u\in U,\;v\in V\right\}$. Designamos a este subespacio por U + V, el subespacio **suma de subespacios**.

**Ejemplo 12**: El subespacio U generado por la prolongación del vector **u** = (1,1,1), que es a**u**, y el subespacio V generado por **v** = (1, 0, -1), que es b**v**, siendo a, b escalares cualesquiera, tienen como suma el subespacio $\left\{a\left(1,1,1\right)+b\left(1,0,-1\right)\vert\;a,\;b\in\mathbb{R}\right\}=\left\{\left(a+b,a,a-b\right)\;\vert\;a,\;b\in\mathbb{R}\right\}$

La siguiente propiedad relaciona las dimensiones de los subespacios U, V con sus sumas e intersecciones.

**Propiedad 7 (fórmula de Grassmann): **dados dos subespacios U, V, se cumple que

$\text{dim }U\;+\;\text{dim }V=\text{dim }\left(U+V\right)+\text{dim }\left(U\cap V\right)$

**Ejemplo 13**: siguiendo con los subespacios U, V del ejemplo 12, la intersección de ambos es:

$\left\{a\left(1,1,1\right)\right\}\cap\left\{b\left(1,0,-1\right)\right\}=\left\{\left(a,a,a\right)\right\}\cap\left\{\left(b,0,-b\right)\right\}=\left\{\left(0,0,0\right)\right\}$

luego dim($U\cap V$) = 0 (un punto aislado se considera de dimensión cero). Por la fórmula de Grassmann, la dimensión del subespacio suma será igual a la suma de las dimensiones de U, V, ambas valen 1 (son rectas en el espacio), luego dim(U \cup V) = 1 + 1 = 2, que es un plano en el espacio, que comprende las dos rectas U, V.

**Definición 6**: si la intersección de dos subespacios U, V es el vector cero, diremos que la suma de subespacios U + V es una **suma directa de subespacios**, y se escribe así: $U\oplus V$.

 **Ejemplo 14**: siguiendo con los subespacios U, V de los ejemplos 12 y 13, como su intersección es el vector nulo, su suma es directa:

$U\oplus V=\left\{\left(a+b,a,a-b\right)\;\vert\;a,\;b\in\mathbb{R}\right\}$

**NOTA 3**: El vector nulo **0** está presente en cualquier espacio o subespacio vectorial (es el elemento neutro de la suma de vectores), por ello, la intersección de subespacios siempre contiene al vector nulo. Geométricamente, los subespacios son rectas, planos o hiperplanos que pasan por el origen de coordenadas. La intersección de subespacios U, V sólo será distinta del conjunto {**0**} cuando o bien U esté contenido en V o bien V esté contenido en U. Por ejemplo, la intersección del plano U: (x, y, z) = a·(1,0,0) + b(0,1,0) con la recta V: c·(-1, 3, 0) es la propia recta V, pues V está contenida en U. En este ejemplo la suma U + V no es directa, el subespacio intersección tiene dimensión 1 y el subespacio suma tiene dimensión 2 (y se cumple la fórmula de Grassmann, como podeis verificar fácilmente).

![separador2](/taller-matematicas/assets/images/separador2.png)
{% endraw %}