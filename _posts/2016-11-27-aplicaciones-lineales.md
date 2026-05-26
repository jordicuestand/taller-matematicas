---
layout: post
title: "Aplicaciones lineales"
date: 2016-11-27 13:37:06 +0000
categories:
  - "Álgebra"
  - "Matemáticas"
tags:
  - "aplicación lineal"
  - "automorfismo"
  - "cambio de base"
  - "endomorfismo"
  - "imagen"
  - "linealidad"
  - "matriz de una aplicación"
  - "núcleo"
  - "rango de una aplicación"
math: true
---

**Competencias**:

 	- Calcular el  núcleo e imagen de una aplicación lineal.

 	- Determinar una aplicación lineal conociendo las imágenes de los vectores de una base.

**Conceptos**:

 	- Conocer el concepto de aplicación lineal y su relación con las matrices.

![separador2](/assets/images/separador2.png)
# Aplicaciones lineales

Las aplicaciones lineales, como todas las aplicaciones, son un tipo de correspondencia entre conjuntos, en este caso entre vectores de dos espacios vectoriales (para un recordatorio de las correspondencias entre conjuntos, ver el artículo [Funciones](http://tallermatematic.ovh/wp/index.php/2015/05/08/funciones/)), de hecho son funciones (o aplicaciones), pero con dos condiciones adicionales:

**Definición 1**: **aplicación lineal entre espacios vectoriales**. Una aplicación lineal es una función *f* que asigna vectores **u** de un espacio vectorial U a vectores *f*(**u**) = **v **de otro espacio vectorial V, cumpliendo las siguientes **condiciones de linealidad**:

 	- f(**u** + **u**') = f(**u**) + f(**u'**) = **v** + **v'**, siendo **u**, **u**' vectores cualesquiera de U, y **v**, **v**' vectores de V

 	- k·f(**u**) = f(k·**u**) para cualquier vector **u** de U

**Ejemplo 1**: La correspondencia *f* que relaciona cada vector **u** del plano $V_2$ con el propio vector u girado 90⁰ en sentido horario, ¿es una aplicación lineal? Antes que nada, establecemos que es una aplicación: a cada vector **u** le corresponde un único vector f(**u**). Comprobemos ahora las condiciones de linealidad. La primera nos pregunta que pasa con las sumas de vectores: ¿es lo mismo sumar dos vectores **u** + **u**' y luego girar el resultado, que primero girar cada vector **u**, **u**' y luego sumar los vectores girados? Se puede ver gráficamente que esto es cierto sin dificultad (fig. 1)

[caption id="attachment_150258" align="aligncenter" width="357"]![Fig. 1: comprobación gráfica de que f(u + v) = f(u) + f(v)](/assets/images/aplica_lineals1.png) Fig. 1: comprobación gráfica de que f(u + v) = f(u) + f(v)[/caption]
La demostración general, algebraica, pasa por determinar cómo se transforman las componentes de un vector cualquiera **u** = (x, y) al aplicar el giro, resultando f(**u**) = **v** = (x', y'); la figura 2 nos muestra las relaciones entre (x, y), (x', y'):

[caption id="attachment_150259" align="aligncenter" width="341"]![Fig. 2: coordenadas de un giro cualquiera en el plano](/assets/images/aplica_lineals2.png) Fig. 2: coordenadas de un giro de 90⁰ en el plano[/caption]
$\begin{array}{l}x'=u\cos\left(90^0-\alpha\right)=u\sin\left(\alpha\right)=y;\;\\y'=u\sin\left(90^0-\alpha\right)=-u\cos\left(\alpha\right)=-x\end{array}$

Por tanto la rotación lo que hace es intercambiar valores i cambiar un signo: (x' , y') = (y, -x). Comprobemos ahora la propiedad 1 de linealidad:

$\begin{array}{l}f\left(\boldsymbol u+\boldsymbol v\right)=f\left(\left(x_1,y_1\right)+\left(x_2,y_2\right)\right)=f\left(\left(x_1+x_2,y_1+y_2\right)\right)=\left(y_1+y_2,-x_1-x_2\right);\\f\left(\boldsymbol u\right)+f\left(\boldsymbol v\right)=f\left(\left(x_1,y_1\right)\right)+f\left(\left(x_2,y_2\right)\right)=\left(y_1,-x_1\right)+\left(y_2,-x_2\right)=\left(y_1+y_2,-x_1-x_2\right).\end{array}$

En efecto coinciden, luego queda demostrada la propiedad 1. La otra propiedad es inmediata:

$\begin{array}{l}f\left(k\boldsymbol u\right)=f\left(k\left(x_1,y_1\right)\right)=f\left(\left(kx_1,ky_1\right)\right)=\left(ky_1,-kx_1\right);\\kf\left(\boldsymbol u\right)=kf\left(\left(x_1,y_1\right)\right)=k\left(y_1,-x_1\right)=\left(ky_1,-kx_1\right).\end{array}$

Por tanto la aplicación f de giro es una aplicación lineal.

Se suele expresar la relación de correspondencia de una aplicación lineal entre vectores por un diagrama como:
$\begin{array}{l}f:\;U\rightarrow V\\\;\;\;\;u\rightarrow\;f(u)=v\end{array}$,

indicando que la aplicación es entre los espacios vectoriales U y V. En el ejemplo 1, el de la rotación, ambos espacios son el mismo $V_2$ de vectores del plano: $f:\;V_2\rightarrow V_2$, pero en general U y V pueden ser distintos.
# Núcleo e imagen de una aplicación lineal

En una aplicación lineal *f* siempre se cumple que f(**0**) = **0**, pero puede suceder que ningún otro vector **u** se relacione con el vector nulo, o bien que la ecuación f(**u**) = **0** tenga más soluciones que **u** = **0**.  El conjunto de vectores u que son soluciones de f(**u**) = **0**  se llama el **núcleo de la aplicación lineal** *f*. El núcleo como mínimo contiene el vector nulo **0**.

Por otro lado, la ecuación **v** = f(**u**) siendo **u** la incógnita, no siempre tiene solución, y entonces no existe ningún vector **u** del espacio vectorial U al que le corresponda el vector **v** del espacio V. Definimos el **conjunto imagen de la aplicación lineal** *f* como el subconjunto de vectores v del espacio V tales que la ecuación **v** = f(**u**) tiene solución.

**Ejemplo 2**: La aplicación giro del ejemplo 1 tiene como Núcleo sólo el vector nulo **0**,  pues ningún vector **u** al girarlo 90⁰ quedará reducido al **0**.  Su conjunto imagen será todo el espacio $V_2$, pues para cualquier vector **v**, existe un vector **u** que cumple  **v** = f(**u**): basta con girar  **v** 90⁰ en sentido antihorario para obtener la solución **u**.

**Ejemplo 3**: Sea la aplicación *f* una proyección sobre el plano coordenado XY, entre el espacio $V_3$ y el espacio $V_3$, tal que f (x, y, z) = (x, y, 0). Cualquier vector (0, 0, z) del subespacio vectorial k · (0, 0, 1), generado por el vector unitario **ẑ** = (0, 0, 1), se corresponde con el vector nulo (0, 0, 0); por tanto el Núcleo de f es el subespacio vectorial {k ·**ẑ}** siendo k un escalar cualquiera. Por otro lado la ecuación **v** = f(**u**) sólo tiene solución u si el vector v está en el plano XY; por ejemplo, el vector v = (1, 2, 3) no puede ser la proyección en el plano XY de ningún vector u = (x, y, z), pues no está contenido en el plano XY. Vemos que el subconjunto Imagen de la aplicación f son los vectores (x, y, 0)  del plano XY, pues son los únicos que se generan por la acción de f sobre $V_3$.

**NOTA 1**: Siendo la imagen de f todo el plano XY, también podríamos haber definido f según el esquema:

$\begin{array}{l}f:\;V_3\rightarrow V_2\\(x,y,z)\rightarrow(x,y)\end{array}$

En este caso, la imagen de f no es un subconjunto, sino que coincide con todo el espacio $V_2$.

**NOTA 2**: las aplicaciones lineales en las que coinciden los dos espacios vectoriales, $f:\;U\rightarrow U$, se llaman **endomorfismos**.

Tenemos las siguientes propiedades y definiciones importantes de las aplicaciones lineales:

**Propiedad 1**

 	- Para toda aplicación lineal $f:\;U\rightarrow V$, su núcleo y su imagen son subespacios vectoriales de U y de V, respectivamente.

 	- Para toda aplicación lineal (en dimensión no infinita) $f:\;U\rightarrow V$, se cumple que ***dimensión(U) = dimensión(subespacio núcleo de f) + dimensión(subespacio imagen de f)***

 	- La aplicación lineal *f* es **inyectiva **si y sólo si núcleo(f) = {**0**}. En ese caso f se llama un **monomorfismo**.

 	- La aplicación lineal $f:\;U\rightarrow V$ es exhaustiva si y sólo si el subespacio imagen(*f*) coincide con el espacio V. En ese caso f se llama un **epimorfismo**

 	- Si la aplicación *f* cumple la propiedad 3 y la 4 simultáneamente, entonces decimos que es una aplicación lineal biyectiva: un **isomorfismo**. Si además f es tal que $f:\;U\rightarrow U$, o sea que también es un endomorfismo, diremos que f es un **automorfismo**.

**Ejemplo 4**: la aplicación giro 90⁰ de los ejemplos 1 y 2 es un endomorfismo de $V_2$; además cumple la propiedad 1.3, luego es inyectiva, y monomorfismo. También cumple la 1.4, luego es biyectiva, y como es endomorfismo biyectivo, es un automorfismo. Su núcleo es el vector {**0**}, un subespacio vectorial de $V_2$ de dimensión cero, y su imagen es todo el espacio $V_2$, con dimensión 2, luego se cumple la igualdad 1.2 y también la propiedad 1.1.

**Ejemplo 5**: para calcular la dimensión de la imagen de la aplicación lineal definida por

$\begin{array}{l}f\left(1,1,0\right)=\left(2,2,0\right)\\f\left(1,0,1\right)=\left(-3,0,-3\right)\\f\left(2,2,1\right)=\left(0,0,0\right)\end{array}$

miramos si los tres vectores imagen son linealmente independientes entre sí, planteando la ecuación a(2,2,0) + b(-3,0,-3) + c(0,0,0) = 0, siendo a, b, c escalares, si sólo se cumple la igualdad con a = b = c = 0 entonces son linealmente independientes:

$\begin{array}{l}a\left(2,2,0\right)+b\left(-3,0,-3\right)+c\left(0,0,0\right)=\left(0,0,0\right)\Rightarrow\\2a-3b=0;\;2a=0;-3b=0\Rightarrow\boxed{a=0,\;b=0}\end{array}$

Como c queda indeterminado (puede tomar cualquier valor) resulta que los tres vectores son linealmente dependientes, así que la dimensión del espacio imagen es menor que tres. Evidentemente (2,2,0) y (-3,0,-3) sí son independientes entre sí, luego forman una base del subespacio imagen, el cual tiene dimensión 2 (pues hay dos vectores imagen linealmente independientes).

Por la propiedad 2, deducimos que la dimensión del núcleo de la aplicación es 3 - 2 = 1. Y por la propiedad 3, deducimos que la aplicación no es inyectiva.

Cualquier vector v que pertenezca al subespacio imagen ha de ser combinación lineal de la base {(2,2,0), (-3,0,-3)}; por ejemplo, para saber si el vector (1, -1, 1) pertenece al subespacio imagen, planteamos (1, -1, 1) = a(2,2,0) + b(-3,0,-3) = (2a-3b, 2a, -3b), igualando componentes obtenemos 2a - 3b = 1, 2a = -1, -3b = 1, por tanto a = -1/2, b = -1/3, pero la igualdad 2a - 3b = 1 no se cumple, luego (1, -1, 1) no pertenece al subespacio imagen.

**Definición 2**:** Rango de una aplicación lineal**

Se llama **rango de una aplicación lineal** f a la dimensión de su subespacio imagen.

**Ejemplo 6**: la aplicación giro 90⁰ de los ejemplos 1 y 2 tiene rango 2, y la aplicación del ejemplo 3 también tiene rango 2.

# Aplicaciones lineales y bases vectoriales

Antiguamente, se identificaban las funciones con las fórmulas analíticas explícitas usadas para obtener las correspondencias, como por ejemplo f(x, y) = (2x -1, x + y). Actualmente el concepto de función es más amplio, no está vinculado necesariamente a una expresión analítica. En el caso de las aplicaciones lineales, hay una propiedad importante en este sentido:

**Propiedad 2**: Se puede determinar completamente una aplicación lineal entre espacios vectoriales, $f:U\rightarrow V$, dando los vectores transformados por *f* de una base vectorial cualquiera del espacio origen *U*.

**Ejemplo 7**: para determinar la aplicación del ejemplo 3, una proyección $f:V_3\rightarrow V_3$ sobre el plano coordenado XY, tomamos una base $\left\{e_1,e_2,e_3\right\}$ de $V_3$. por ejemplo la [base canónica](https://es.wikipedia.org/wiki/Base_can%C3%B3nica) {(1, 0, 0), (0, 1, 0), (0, 0, 1)}, y obtenemos sus imágenes por *f*:  *f*(1, 0, 0) = (1, 0, 0), *f*(0, 1, 0) = (0, 1, 0), *f*(0, 0, 1) = ( 0, 0, 0). Entonces, dado un vector de $V_3$ cualquiera, **u** = (x, y, z), podemos obtener su imagen así:

1º) expresamos **u** como combinación lineal de los vectores de la base $\left\{e_1,e_2,e_3\right\}$, que expresamos así: $u=\left(x,y,z\right)=u_1e_1+u_2e_2+u_3e_3$. Los coeficientes $u_1,u_2,u_3$ se llaman componentes del vector u en la base $\left\{e_1,e_2,e_3\right\}$

2º) obtenemos $f\left(u\right)=f\left(x,y,z\right)=f\left(u_1e_1+u_2e_2+u_3e_3\right)=u_1f\left(e_1\right)+u_2f\left(e_2\right)+u_3f\left(e_3\right)$

En nuestro ejemplo, con la base canónica, los coeficientes son inmediatos: (x, y, z) = x(1, 0, 0) + y(0, 1, 0) + z(0, 0, 1), luego f(x, y, z) = x·f(1, 0, 0) + y·f(0, 1, 0) + z·f(0, 0, 1) = x(1, 0, 0) + y(0, 1, 0) + 0 = (x, y, 0).

En el ejemplo 6 hemos usado la base canónica pues es la más simple, tan simple que al aplicar la propiedad 2 se obtienen resultados evidentes, lo cual ayuda a entender el significado de la propiedad, pero parece ser poco útil en la práctica; de hecho es todo lo contrario: en las aplicaciones prácticas y los problemas a menudo encontramos dificultades para encontrar expresiones analíticas de funciones, y  en cambio usando la propiedad 2 con bases adecuadas (no las canónicas) podemos determinar la aplicación lineal. En el siguiente ejemplo vemos una situación así.

**Ejemplo 8**: Consideremos un plano P en el espacio, tal que corta a los planos coordenados XZ y YZ a 45⁰ (figura 3)

![aplica_lineals3](/assets/images/aplica_lineals3.png)

Definimos la aplicación $f:P\rightarrow P$ realizando una rotación de 90⁰, según un eje perpendicular a P, en sentido antihorario, que afecta a todos los vectores contenidos en el plano P.  Dado un vector cualquiera u = (x, y, z) del plano P, ¿cuál es su vector imagen por *f*?

Podríamos obtener la expresión analítica de f tal como hemos hecho en el ejemplo 1, pero será mucho más fácil usar la propiedad 2 y nuestros conocimientos de espacios vectoriales: notemos que el plano P es un subespacio vectorial de $V_3$, y que f es un endomorfismo de P en P.

¿Qué base de P podemos tomar? En la figura 3 vemos que los vectores **u** (contenido en el plano XZ) y **v** (contenido en el plano YZ) están contenidos en P, y además son linealmente independientes; como la dimensión de P es 2, deducimos que el conjunto {**u**, **v**} es una base vectorial de P. Observad que no hemos dado componentes a los vectores **u**, **v, **de momento pueden ser cualesquiera, siempre que  estén en los planos XZ y con el YZ y formen un ángulo de 45⁰ con X y con Z, o con Y y con Z, respectivamente.

¿Cuales son las imágenes de **u**, **v** por *f*? Demos ahora valores a estos vectores, por ejemplo **u** = (1, 0, 1), **v** = (0, 1, 1) cumplen las condiciones exigidas. El giro de 90⁰ lleva al vector **u** a coincidir con el vector **v**: f(**u**) = **v**; y al vector **v** lo gira hacia el plano (-X)(-Z): f(**v**) = (-1, 0 ,-1) = -**u**. Ahora ya podemos expresar la imagen de cualquier vector **w** = (x, y, z) de P:

1º) Dado un vector **w** =(x, y, z) de $V_2$, sus coeficientes han de cumplir $\left(x,y,z\right)=\lambda\boldsymbol u+\mu\boldsymbol v=\lambda\left(1,1,0\right)+\mu\left(0,1,1\right)$, con esto obtenemos los coeficientes $\lambda,\;\mu$

2º) obtenemos la imagen: $f\left(x,y,z\right)=f\left(\lambda\boldsymbol u+\mu\boldsymbol v\right)=\lambda f\left(\boldsymbol u\right)+\mu f\left(\boldsymbol v\right)=-\lambda\boldsymbol v-\mu\boldsymbol u$

Por ejemplo, el vector **w** = (2, 1, 3) pertenece al plano $V_2$, pues (2, 1, 3) = 2·(1, 0, 1) + 1·(0, 1, 1) = 2**u** + **v**; ¿cuál es la imagen por f del vector (1, 2, 1)? Será:

$f\left(2,1,3\right)=f\left(2\boldsymbol u+1\boldsymbol v\right)=2f\left(\boldsymbol u\right)+1f\left(\boldsymbol v\right)=-2\boldsymbol v-\boldsymbol u=2\left(0,1,1\right)-\left(1,0,1\right)=\left(-1,2,1\right)$,

y podemos comprobar fácilmente que el vector f(w) tambien está en el plano $V_2$, ya que $\left(-1,2,1\right)=-\left(1,0,1\right)+2\cdot(0,1,1)=-\boldsymbol u+2\boldsymbol v$.

# Matriz de una aplicación lineal

Dada una aplicación lineal $f:U\rightarrow V$ entre dos espacios vectoriales, siendo la base de U los vectores $\left\{u_1,u_2,\dots,u_n\right\}$, su matriz asociada es la siguiente  disposición de las imágenes de los vectores de la base de U:

$\begin{pmatrix}f\left(u_1\right)&amp;f\left(u_2\right)&amp;\dots&amp;f\left(u_n\right)\end{pmatrix}$

Como cada vector $f(u_i)$ tendrá n componentes, se obtiene u cuadro numérico en el que cada columna representa las componentes del vector $f(u_i)$.

**Ejemplo 9**: la aplicación lineal$f:P\rightarrow P$ del ejemplo 7 verifica que la base del espacio P (un plano) es {**u** , **v**} y sus imágenes por *f* son f(**u**) = **v**, f(**v**) = -**u**; entonces, la matriz asociada a *f* en las bases {**u**, **v**} es:

$\begin{pmatrix}f\left(u\right)&amp;f\left(v\right)\end{pmatrix}=\begin{pmatrix}0&amp;-1\\1&amp;0\end{pmatrix}$

Observad que las componentes de los vectores imagen se disponen "en vertical", que hay dos columnas, una para cada vector de la base {**u**, **v**}, y cada columna tiene dos componentes. La primera columna indica que f(**u**) = 0·**u** + 1·**v**, y la segunda que f(**v**)=-1·**u** + 0·**v**.

#### Rango de una matriz

Antes se ha definido el rango de una aplicación lineal *f* como la dimensión de su espacio imagen; dada una matriz A cualquiera, su **rango por columnas** es el número máximo de columnas que, tomadas como vectores, son linealmente independientes. Si la matriz A es la matriz asociada a la aplicación *f*, entonces el rango de A coincide con el rango de *f*.  Por ejemplo, la matriz del ejemplo 8 tiene rango 2, pues sus dos columnas, vistas como vectores, son independientes, y por tanto la aplicación asociada tiene rango 2, equivalentemente, su espacio imagen tiene dimensión 2.

Por otro lado, dada una matriz A, definimos su **rango por filas** como el número máximo de filas que, tomadas como vectores, son linealmente independientes. Se cumple que los rangos por filas y por columnas siempre coinciden, así que podemos calcular el rango de la matriz como mejor nos convenga.

#### Matrices cuadradas y matrices rectangulares

Si una aplicación f hace corresponder espacios vectoriales de la misma dimensión n, entonces la matriz asociada tendrá n columnas (una por cada vector de la base) y n filas (pues cada columna se expresará según la misma base de n componentes): diremos que es una **matriz cuadrada**. En cambio si los espacios tienen dimensiones distintas, las matrices asociadas tendrán distinto número de filas que de columnas, serán matrices rectangulares. Por ejemplo, la aplicación de la nota 1 corresponde $V_3$ con $V_2$,  luego su matriz contendrá 3 columnas y dos filas, su aspecto será:

$\begin{pmatrix}\square&amp;\square&amp;\square\\\square&amp;\square&amp;\square\end{pmatrix}$
#### Matrices y bases

En el ejemplo 8, hemos expresado los vectores de la base de U, y sus imágenes, respecto a la propia base de U, {**u** , **v**}. Pero cualquier base vectorial es válida para expresar los vectores del espacio. Por ello, la matriz de la aplicación lineal depende de la base del espacio origen U y también de la base en la que se expresen los vectores imagen; cuando no se indica que base se está utilizando, se supondrá que las bases son las canónicas.

#### Operaciones con aplicaciones y con sus matrices

Se pueden definir las operaciones suma de funciones (f + g) y producto de una función por un escalar k·f de la siguiente forma:

*(f + g)(x) = f(x) + g(x); k·f(x) = f(kx)*

Resulta que estas operaciones tienen las propiedades habituales de la suma: asociativa, conmutativa, elemento neutro y elemento inverso), y las propiedades distributiva k*(f + g) = k·f + k·g*, *(k + p)**f** = kf + p·f*,  asociativa *(kp)·f = k(p·f)*, y elemento neutro escalar*1·f = f. *Con ello podemos decir que el conjunto de aplicaciones lineales, junto con las operaciones definidas, es también un espacio vectorial.

Por otro lado, podemos hacer lo mismo con las matrices: definimos la suma de dos matrices (han de ser de las mismas dimensiones, o sea, número de filas y de columnas):

$\begin{pmatrix}a_1^1&amp;\dots&amp;a_1^n\\\vdots&amp;\vdots&amp;\vdots\\a_m^1&amp;\cdots&amp;a_m^n\end{pmatrix}+\begin{pmatrix}b_1^1&amp;\dots&amp;b_1^n\\\vdots&amp;\vdots&amp;\vdots\\b_m^1&amp;\cdots&amp;b_m^n\end{pmatrix}=\begin{pmatrix}a_1^1+b_1^1&amp;\dots&amp;a_1^n+b_1^n\\\vdots&amp;\vdots&amp;\vdots\\a_m^1+b_m^1&amp;\cdots&amp;a_m^n+b_m^n\end{pmatrix}$

y el producto de un escalar por una matriz:

$k\begin{pmatrix}a_1^1&amp;\dots&amp;a_1^n\\\vdots&amp;\vdots&amp;\vdots\\a_m^1&amp;\cdots&amp;a_m^n\end{pmatrix}=\begin{pmatrix}ka_1^1&amp;\dots&amp;ka_1^n\\\vdots&amp;\vdots&amp;\vdots\\ka_m^1&amp;\cdots&amp;ka_m^n\end{pmatrix}$

Con estas operaciones,** las matrices forman un espacio vectorial**.

Además tenemos la siguinte propiedad:
**Propiedad 1**: Dadas dos aplicaciones lineales f, g, con matrices asociadas F, G,  y un escalar k, se cumple que:

 	- la aplicación *k·f* tiene por matriz *k·F*

 	- la aplicación suma *f + g* tiene por matriz *F + G*

Hay otra operación con funciones que es importante: **la composición de funciones**; recordemos que dadas dos funciones f, g su composición se describe por $\left(f\circ g\right)\left(x\right)=f\left(g\left(x\right)\right)$. También recordemos la definición de **función inversa**: dada la función f, su función inversa $f^{-1}$ es aquella tal que al componerla con f resulta la función identidad: $f\circ f^{-1}=I$.

La composición de aplicaciones lineales y la inversa de una aplicación lineal también tienen correspondencias con las matrices: definimos el **producto de matrices** según la siguiente igualdad:

$\begin{pmatrix}a_1^1&amp;\dots&amp;a_1^n\\\vdots&amp;\vdots&amp;\vdots\\a_m^1&amp;\cdots&amp;a_m^n\end{pmatrix}\cdot\begin{pmatrix}b_1^1&amp;\dots&amp;b_1^m\\\vdots&amp;\vdots&amp;\vdots\\b_n^1&amp;\cdots&amp;b_n^m\end{pmatrix}=\begin{pmatrix}{\textstyle\sum_{i=1}^n}a_1^ib_i^1&amp;\dots&amp;\textstyle\sum_{i=1}^na_1^ib_i^n\\\vdots&amp;\vdots&amp;\vdots\\\textstyle\sum_{i=1}^na_m^ib_i^1&amp;\dots&amp;\textstyle\sum_{i=1}^na_m^ib_i^m\end{pmatrix}$

Que puede entenderse mejor siguiendo esta regla de formación: para hallar el elemento fila1-columna1 del producto de matrices A·B multiplicamos uno por uno los elementos de la 1ª fila de A por los elementos de la 1ª columna de B:

![Fig. 4: obtención del primer elemento del producto de matrices](/assets/images/aplica_lineals4.png)

Fig. 4: obtención del primer elemento del producto de matrices

En general, multiplicamos uno por uno los elementos de la fila n de A por los elementos de la columna m de B para obtener el elemento de la fila n y columna m de A·B:

[caption id="attachment_150273" align="alignnone" width="307"]![Fig. 5: obtención del último elemento de la 1ª fila del producto de matrices A·B](/assets/images/aplica_lineals5.png) Fig. 5: obtención del último elemento de la 1ª fila del producto de matrices A·B[/caption]
**NOTA**: las operaciones con matrices pueden, y creo que deberían hacerse en el siglo XXI, con calculadora o ordenador; hay numerosas páginas que hacen cálculo matricial on-line, como por ejemplo [https://matrixcalc.org/es/](https://matrixcalc.org/es/)  o la potente página [Wolfram Alpha](https://www.wolframalpha.com/examples/Math.html) que todo estudiante debería conocer y utilizar,

También se puede definir la **inversa de una matriz** (A), como la matriz $\left(A\right)^{-1}$ tal que el producto de ambas es igual a la matriz identidad, una matriz con unos en la diagonal y ceros en el resto de posiciones:

$A\cdot\left(A\right)^{-1}=\begin{pmatrix}1&amp;0&amp;\dots&amp;0&amp;0\\0&amp;1&amp;0&amp;0&amp;0\\\vdots&amp;\vdots&amp;\vdots&amp;\vdots&amp;\vdots\\0&amp;\dots&amp;0&amp;1&amp;0\\0&amp;0&amp;\dots&amp;0&amp;1\end{pmatrix}$

Tenemos la siguiente **propiedad importante**:
**Propiedad 2**: la aplicación composición de funciones $f\circ g$ tiene por matriz el producto de matrices *F·G, *siendo F y G las matrices de f, g respectivamente dadas en las bases, y la aplicación inversa $f^{-1}$ tiene por matriz la matriz inversa $\left(A\right)^{-1}$

**Ejemplo 10**: Llamemos f a la función proyección sobre el plano $V_2$ del ejemplo 3,

$\begin{array}{l}f:V_3\rightarrow V_2\\\left(x,y,z\right)\rightarrow\left(x,y,0\right)\end{array},$

y llamemos g a la función giro en el plano del ejemplo 1:

$\begin{array}{l}g:V_2\rightarrow V_2\\\left(x,y\right)\rightarrow\left(y,-x\right)\end{array}$

La composición $g\circ f$ será:

$\begin{array}{l}g\circ f:V_3\rightarrow V_2\rightarrow V_2\\\left(x,y,z\right)\rightarrow\left(x,y\right)\rightarrow\left(y,-x\right)\end{array}$

(recordemos que $\left(g\circ f\right)\left(x\right)=g\left(f\left(x\right)\right)$, literalmente, "primero se aplica f, y despues se aplica g".

Las matrices de f, g, en las bases canónicas, son:

$\left(F\right)=\begin{pmatrix}1&amp;0&amp;0\\0&amp;1&amp;0\end{pmatrix},\;\left(G\right)=\begin{pmatrix}0&amp;1\\-1&amp;0\end{pmatrix}$

entonces la matriz de la composición $g\circ f$ se puede obtener multiplicando la matrices (G)·(F):

$\left(G\right)\cdot\left(F\right)=\begin{pmatrix}0&amp;1\\-1&amp;0\end{pmatrix}\cdot\begin{pmatrix}1&amp;0&amp;0\\0&amp;1&amp;0\end{pmatrix}\;=\begin{pmatrix}0&amp;1&amp;0\\-1&amp;0&amp;0\end{pmatrix}$

**NOTA**: observad que las matrices tienen dimensiones acordes con la aplicación a la que representan, si $f:V_3\rightarrow V_2$ entonces (F) tiene 2 filas y 3 columnas (matriz de 2x3), y si $g:V_2\rightarrow V_2\$ entonces (G) tiene 2 filas y 2 columnas (matriz de 2x3), en general si $f:V_n\rightarrow V_m\$ entonces (F) tiene m filas y n columnas (matriz de m x n).

#### Obtención de la imagen de un vector *u* por la función *f* a partir de la matriz *(F)* de la función

Para hallar la imagen *f(**u**)* dada la matriz (F) de la aplicación *f*, simplemente disponemos los elementos del vector u en forma de **matriz columna**, *(u)*, y realizamos el producto de (F)·(u):

$f\left(\boldsymbol u\right)=\left(F\right)\cdot\begin{pmatrix}u_1\\u_2\\\vdots\\u_n\end{pmatrix}$

Para que esto funcione, la matriz (F) ha de tener el mismo número de  columnas que el número de elementos del vector **u**.

**Ejemplo 11**: La imagen del vector (-3, 5, 6) por la aplicación lineal $g\circ f$ del ejemplo 9, una proyección en el plano XY seguida de un giro, se obtiene matricialmente así:

$f\left(\boldsymbol u\right)=\begin{pmatrix}0&amp;1&amp;0\\-1&amp;0&amp;0\end{pmatrix}\cdot\begin{pmatrix}-3\\5\\6\end{pmatrix}=\begin{pmatrix}5\\3\end{pmatrix}$

#### Matrices de cambio de base

Si tenemos una matriz de una aplicación *f* expresada según unas bases de los espacios vectoriales y queremos obtener la matriz de la misma aplicación *f* pero expresada en bases distintas, la podemos obtener mediante la siguiente propiedad:

**Propiedad 3** (matrices del cambio de base). Si tenemos una aplicación lineal $f:U\rightarrow V$ , tomando las bases $({\overrightarrow{au}}_1,{\overrightarrow{au}}_2,...,{\overrightarrow{au}}_n)$ del espacio U y $({\overrightarrow{av}}_1,{\overrightarrow{av}}_2,...,{\overrightarrow{av}}_n)$ del espacio V, entonces la matriz de la aplicación lineal contendrá las imágenes de los vectores $\overrightarrow{au}$ expresados en la base de losvectores $\overrightarrow{av}$, llamemos a esta matriz (A).

Por otro lado,   si tomamos otras bases $({\overrightarrow{bu}}_1,{\overrightarrow{bu}}_2,...,{\overrightarrow{bu}}_n)$ del espacio U y $({\overrightarrow{bv}}_1,{\overrightarrow{bv}}_2,...,{\overrightarrow{bv}}_n)$ del espacio V, la matriz asociada a la aplicación será distinta, la llamaremos (B).

Entonces se cumple la relación entre matrices (B) = (Q)·(A)·(P), donde:

(Q) es la matriz que tiene por columnas los vectores $\overrightarrow{bu}$ expresados en la base de los vectores $\overrightarrow{au}$ (suele decirse: "*los vectores de la nueva base de U expresados en la base antigua de U*")

(P) es la matriz que tiene por columnas los vectores $\overrightarrow{av}$ expresados en la base de los vectores $\overrightarrow{bv}$ (suele decirse: "*los vectores de la antigua  base de V expresados en la nueva base de V*")

**Ejemplo 12**:  la matriz A de la aplicación del  ejemplo 7, dada en el ejemplo 8, utiliza la base {**u**, **v**}, si tomamos otra base {**u'**, **v'**} dada por **u**' = **u** + **v**, **v** ' = **u** - **v**, ¿cuál será la matriz B de la aplicación en la nueva base?

Identificamos las matrices  de cambio de base (P), (Q):

**Matriz Q**: *nueva base {**u'**, **v'**} expresada en la base antigua* de U, la {**u**, **v**}, es evidente que

$Q=\begin{pmatrix}1&amp;1\\1&amp;-1\end{pmatrix}$

**Matriz P**:  *vectores de la antigua  base {**u**, **v**}**,  expresados en la nueva base {**u'**, **v'**};* observamos que **u**' + **v**' = 2**u** y que **u**' - **v**' = 2**v**, luego **u **= (1/2)(**u**' + **v**') y **v** = (1/2)(**u**' - **v**' ), luego:

$P=\frac12\begin{pmatrix}1&amp;1\\1&amp;-1\end{pmatrix}$

Aplicamos la propiedad 3:

$\begin{array}{l}\left(B\right)=\left(Q\right)\left(A\right)\left(P\right)=\begin{pmatrix}1&amp;1\\1&amp;-1\end{pmatrix}\cdot\begin{pmatrix}0&amp;-1\\1&amp;0\end{pmatrix}\cdot\frac12\begin{pmatrix}1&amp;1\\1&amp;-1\end{pmatrix}=\\\frac12\begin{pmatrix}1&amp;1\\1&amp;-1\end{pmatrix}\cdot\begin{pmatrix}-1&amp;1\\1&amp;1\end{pmatrix}=\frac12\begin{pmatrix}0&amp;2\\-2&amp;0\end{pmatrix}=\begin{pmatrix}0&amp;1\\-1&amp;0\end{pmatrix}\end{array}$