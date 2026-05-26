---
layout: post
title: "Vectores y valores propios, diagonalización de matrices"
date: 2016-12-19 07:45:15 +0000
categories:
  - "Álgebra"
  - "Matemáticas"
tags:
  - "diagonalización"
  - "polinomio característico"
  - "valor propio"
  - "vector propio"
math: true
---

## Vectores propios y valores propios

**Definición 1**: dado un endomorfismo f de un espacio vectorial E, $f:E\rightarrow E$, si existen vectores $\boldsymbol v\in E$ tales que su imagen por f es otro vector proporcional a **v**, $f\left(\boldsymbol v\right)=k\boldsymbol v\in E$, siendo k un escalar, diremos que **v** es un **vector propio** de f, con **valor propio** k.

**Ejemplo 1**: La aplicación lineal $f:\mathbb{R}^2\rightarrow\mathbb{R}^2$ con matriz (en la base canónica)

$\begin{pmatrix}3/5&amp;4/5\\4/5&amp;-3/5\end{pmatrix}$

cumple que, para el vector (2, 1),

$\begin{pmatrix}3/5&amp;4/5\\4/5&amp;-3/5\end{pmatrix}\begin{pmatrix}2\\1\end{pmatrix}=\begin{pmatrix}6/5+4/5\\8/5-3/5\end{pmatrix}=\begin{pmatrix}2\\1\end{pmatrix}$

luego (2, 1) es un vector propio de *f*, con valor propio k = 1.

**Condición para que existan valores y vectores propios**

Teóricamente para encontrar los posibles valores propios de una aplicación lineal *f* planteamos la ecuación  lineal

$f\left(\boldsymbol v\right)=k\boldsymbol v\Leftrightarrow f\left(\boldsymbol v\right)-k\boldsymbol v=\mathbf0\Leftrightarrow\left(f-k\mathbb{I}\right)=\mathbf0$ [1]

, donde $\mathbb{I}$ es la aplicacion identidad, $\mathbb{I}\left(\boldsymbol v\right)=\boldsymbol v\right$, y el símbolo **0** representa el vector nulo. Esto puede interpretarse como: los vectores propios de *f* han de ser vectores del núcleo de la aplicación $\left(f-k\mathbb{I}\right)$. Recordando que para que el núcleo de una aplicación no sea el conjunto vacío se ha de cumplir que su determinante sea nulo, obtenemos la condición de existencia de valores y vectores propios:

$\text{det}\;\begin{pmatrix}a_{11}-1&amp;\dots&amp;a_{1n}\\\vdots&amp;\dots&amp;\vdots\\a_{n1}&amp;\cdots&amp;a_{nn}-1\end{pmatrix}=0$ [2]

**Ejemplo 2**: La aplicación del ejemplo 1 cumple la condición de existencia de vectores y valores propios:

$\text{det}\begin{pmatrix}3/5-1&amp;4/5\\4/5&amp;-3/5-1\end{pmatrix}=\begin{vmatrix}-\frac25&amp;\frac45\\\frac45&amp;-\frac85\end{vmatrix}=\frac{16}{25}-\frac{16}{25}=0$

**Polinomio característico de la aplicación lineal**

Para encontrar vectores propios de f, hemos visto que será lo mismo que encontrar los vectores del núcleo de la aplicación lineal $\left(f-k\mathbb{I}\right)$ para los valores posibles de k. Estos valores k han de cumplir la condición [2]:

$\text{det}\;\begin{pmatrix}a_{11}-k&amp;\dots&amp;a_{1n}\\\vdots&amp;\dots&amp;\vdots\\a_{n1}&amp;\cdots&amp;a_{nn}-k\end{pmatrix}=0$ [3].

Al desarrollar este determinante, obtenemos un polinomio de grado n en la variable k, denominado **polinomio característico de la aplicación lineal f**. Para cada raíz de este polinomio, obtendremos uno de los valores propios de f.

**Ejemplo 3**: La aplicación del ejemplo 1 tiene por polinomio característico:

$\text{det}\begin{pmatrix}3/5-k&amp;4/5\\4/5&amp;-3/5-k\end{pmatrix}=-\frac9{25}+k^2-\frac{16}{25}=k^2-1$

con raíces k = +1, -1, que son los valores propios de f.

**Propiedad 1**: Una propiedad importante del polinomio característico es que no depende de las bases en la que expresemos la matriz de la aplicación f, por este motivo se le llama característico de f.

**Determinación de los vectores propios**

Para cada valor propio encontrado con el polinomio característico, planteamos la ecuación lineal [1], que será un sistema con *n* incógnitas del tipo indeterminado, pues su determinante es nulo (condición [2]). Las soluciones formaran un subespacio vectorial: el del núcleo de la aplicación $\left(f-k\mathbb{I}\right)$.

**Ejemplo 4**: para el valor propio k = 1 de la aplicación del ejemplo 1, planteamos y resolvemos el sistema siguiente:

$\begin{array}{l}\begin{pmatrix}3/5-1&amp;4/5\\4/5&amp;-3/5-1\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix}=\begin{pmatrix}0\\0\end{pmatrix}\Rightarrow\left.\begin{array}{r}-\frac25x+\frac45y=0\\\frac45x-\frac85y=0\end{array}\right\}\Rightarrow\\\left.\begin{array}{r}-\frac45x+\frac85y=0\\\frac45x-\frac85y=0\end{array}\right\}\Rightarrow x-2y=0\Rightarrow\boxed{x=2y}\end{array}$

Cualquier vector que cumpla esta condición será un vector propio de f con valor propio k = 1, como por ejemplo los vectores (2, 1), (10, 5), (-4, -2), ...

Cuando el polinomio característico tiene raíces múltiples, no siempre será posible encontrar todos los vectores propios, como establece la siguiente propiedad:

**Propiedad 2**: la dimensión del subespacio Núcleo de $\left(f-k\mathbb{I}\right)$ para raíces múltiples k es menor o igual  que la multiplicidad.

**Ejemplo 5**: La aplicación lineal que tiene por matriz

$\begin{pmatrix}6&amp;3&amp;1\\-27&amp;-14&amp;-5\\65&amp;36&amp;13\end{pmatrix}$

cumple la condición [2] de existencia de valores y vectores propios (comprobado con una calculadora de determinantes en línea). Calculemos su polinomio característico:

$\begin{array}{l}\text{det }\begin{pmatrix}6-k&amp;3&amp;1\\-27&amp;-14-k&amp;-5\\65&amp;36&amp;13-k\end{pmatrix}=\left(6-k\right)\begin{vmatrix}-14-k&amp;-5\\36&amp;13-k\end{vmatrix}+27\begin{vmatrix}3&amp;1\\36&amp;13-k\end{vmatrix}-65\begin{vmatrix}3&amp;1\\-14-k&amp;-5\end{vmatrix}=\\\left(6-k\right)\left(-182+14k-13k+k^2+180\right)+27\left(39-3k-36\right)+65\left(-15+14+k\right)=\\\left(6-k\right)\left(k^2+k-2\right)+27\left(3-3k\right)-65+65k=\\6k^2+6k-12-k^3-k^2+2k+81-81k-65+65k=\\-k^3+5k^2-8k+4=0\end{array}$

En casos reales deberíamos obtener las raíces de forma aproximada con ordenador, en este ejemplo didáctico las raíces son enteras, por Ruffini probamos con los divisores del término independiente, 4:

$\begin{array}{l}\;\;\begin{array}{cccc}-1&amp;5&amp;-8&amp;4\end{array}\\1\;\;\underline{\;\begin{array}{cccc}&amp;-1&amp;4&amp;-4\end{array}}\\\begin{array}{cccc}\;\;-1&amp;4&amp;-4&amp;\boxed0\end{array}\;\\\end{array}$

Tenemos el primer valor propio, k = 1, es una raíz simple (multiplicidad = 2), y el subespacio vectorial asociado de valores propios tendrá, pues, dimensión 1 (geométricamente es una recta). Hemos reducido la ecuación característica a segundo grado, $-k^3+5k^2-8k+4=\left(k-1\right)\left(-k^2+4k-4\right)$, la resolvemos directamente:

$-k^2+4k-4=0\Rightarrow k=\frac{-4\pm\sqrt{16-4\cdot(-1)\cdot(-4)}}{-2}=2$

El valor propio k = 2 es una raíz doble (multiplicidad = 2), el subespacio vectorial asociado de valores propios puede tener dimensión 1 (una recta) o 2 (un plano).

## Diagonalización de endomorfismos (y matrices)

**Propiedad 3**: los vectores propios correspondientes a valores propios distintos de un endomorfismo f son linealmente independientes.

Por la propiedad 3, en una aplicación f en un espacio de dimensión n, no pueden haber más de n valores propios distintos, pues ese es el número máximo de vectores linealmente independientes.

**Definición 2**: dado un endomorfismo f de un espacio vectorial E, $f:E\rightarrow E$ de dimensión n, si existen exactamente n valores propios de f, diremos que el endomorfismo (y su matriz) es diagonalizable.

El nombre "diagonalizable" proviene del hecho de que, si existen n vectores propios independientes, formaran una base del espacio, y si expresamos la matriz de f en esa base, entonces la matriz será diagonal, y sus elementos seran precisamente los valores propios. En efecto, si ${u_1,u_2,...,u_n}$ es la base de vectores propios, con valores propios ${k_1,k_2,...,k_n}$, entonces la matriz de f en esa base está formada por las imágenes $f(u_i)=k_iu_i$ expresadas en la misma base ${u_1,u_2,...,u_n}$, que es la matriz diagonal:

$\begin{pmatrix}k_1&amp;&amp;\\&amp;\ddots&amp;\\&amp;&amp;k_n\end{pmatrix}$

**Ejemplo 6**: la aplicación lineal del ejemplo 1, sobre el espacio $\mathbb{R}^2$, tiene dos valores propios, luego será diagonalizable: podemos tomar una base de $\mathbb{R}^2$ formada por vectores propios cualesquiera de f, y en esa base la matriz de f será:

$\begin{pmatrix}1&amp;0\\0&amp;-1\end{pmatrix}$

**Ejemplo 7**: la aplicación lineal f del ejemplo 5 tiene una raíz doble k = 2, para que sea diagonalizable ha de suceder que la dimensión del núcleo de (f - 2I) sea también 2. Vamos a comprobarlo, recordando que los vectores (x, y, z) del núcleo son aquellos que tienen por imagen el vector nulo, planteamos:

$\left(f-2\mathbb{I}\right)\begin{pmatrix}x\\y\\z\end{pmatrix}=0\Leftrightarrow\begin{pmatrix}4&amp;3&amp;1\\-27&amp;-16&amp;-5\\65&amp;36&amp;11\end{pmatrix}\begin{pmatrix}x\\y\\z\end{pmatrix}=\begin{pmatrix}4x+3y+z\\-27x-16y-5z\\65+6y+11z\end{pmatrix}=\begin{pmatrix}0\\0\\0\end{pmatrix}$

un sistema lineal homogéneo, que simplificamos:

$\begin{array}{l}\begin{array}{c}27\cdot\\4\cdot\\\end{array}\begin{pmatrix}4x+3y+z\\-27x-16y-5z\\65+36y+11z\end{pmatrix}\sim\begin{pmatrix}108x+81y+27z\\-108x-64y-20z\\65+36y+11z\end{pmatrix}\sim\begin{pmatrix}4x+3y+z\\0x+17y+7z\\65+36y+11z\end{pmatrix}\sim\\\begin{array}{c}65\cdot\\\\-4\end{array}\begin{pmatrix}4x+3y+z\\0x+17y+7z\\65+36y+11z\end{pmatrix}\sim\begin{pmatrix}260x+195y+65z\\0x+17y+7z\\-260x-144y-44z\end{pmatrix}\sim\begin{pmatrix}4x+3y+z\\0x+17y+7z\\0x-51y-21z\end{pmatrix}\sim\\\begin{array}{c}\\51\\17\end{array}\begin{pmatrix}4x+3y+z\\0x+17y+7z\\0x-51y-21z\end{pmatrix}\sim\begin{pmatrix}4x+3y+z\\0x+867y+357z\\0x-867y-357z\end{pmatrix}\sim\begin{pmatrix}4x+3y+z\\0x+17y+7z\\0x+0y+0z\end{pmatrix}\end{array}$

Vemos que nos quedan 2 ecuaciones independientes: la dimensión del núcleo de (f - 2I) es 1, no coincide con la multiplicidad del valor propio k = 2, luego la matriz no es diagonalizable. Resolviendo el sistema indeterminado podemos obtener los vectores propios del valor propio k = 2:

$\begin{array}{l}\left.\begin{array}{r}4x+3y+z=0\\17y+7z=0\end{array}\right\}\Rightarrow\left.\begin{array}{r}4x+3y+z=0\\\boxed{y=-7z/17}\end{array}\right\}\Rightarrow4x-\left(21/17\right)z+z=0\Rightarrow\\4x-\left(4/17\right)z=0\Rightarrow\boxed{x=\left(1/17\right)z}\end{array}$

o sea que nos queda los vectores (x, y, z) en función de z; por ejemplo, dado z = 17, entonces x =1 , y = -7, y obtenemos el vector propio (1, -7, 17) para el valor propio k = 2.

Obtengamos ahora un vector propio para el valor k = 1, o sea, resolvemos la ecuación (f - 1·I)v = 0, donde v = (x, y, z); esta vez usamos una hoja de cálculo para los detalles aritméticos:

![pivote](/assets/images/pivote.png)

Resolviendo las dos ecuaciones independientes:

$\begin{array}{l}\left.\begin{array}{r}5x+3y+z=0\\6y+2z=0\end{array}\right\}\Rightarrow\left.\begin{array}{r}5x+3y+z=0\\\boxed{y=-z/3}\end{array}\right\}\Rightarrow4x-z+z=0\Rightarrow\boxed{x=0}\\\end{array}$

Por ejemplo, para z = 3, obtenemos el vector propio (0, -1, 3). Como f no diagonaliza, no tenemos una base de vectores propios de f; lo que sí podemos hacer es completar los vectores propios de f con otro vector linealmente independiente para obtener una base que "casi diagonaliza". Por ejemplo, el vector (1, 0, 1) es claramente independiente de (1, -7, 17) y de (0, -1, 3). Tenemos pues la base {(1, -7, 17) , (0, -1, 3) , (1, 0, 1)}. ¿cuál será la matriz de f en esta base? Determinemos f((1, 0, 1), que resulta ser (7, -32, 78). ¿Cómo se expresa este vector en la base dada? Planteamos (7, -32, 78) = x·(1, -7, 17)+y·(0, -1, 3) + z·(1, 0, 1)  resolvemos este sistema, esta vez usamos una de las muchas páginas de Internet gratuitas que hacen el trabajo pesado ([http://wims.unice.fr/wims/wims.cgi](http://wims.unice.fr/wims/wims.cgi)). obtenemos:

![pivote2](/assets/images/pivote2.png)

Entonces concluimos que la matriz de f en la base que hemos diseñado es:

$\begin{pmatrix}1&amp;0&amp;-\frac{25}3\\0&amp;2&amp;-\frac{79}3\\0&amp;0&amp;\frac{46}3\end{pmatrix}$.

**Ejemplo 8**: comprobar si la matriz siguiente diagonaliza, teniendo en cuenta que está expresada en la base {(1, 1, 0), (1, 0, 1), (2, 2, 1)},

$\begin{pmatrix}2&amp;-3&amp;0\\2&amp;0&amp;0\\0&amp;-3&amp;0\end{pmatrix}$.

Antes que nada, si queremos comprobar que  {(1, 1, 0), (1, 0, 1), (2, 2, 1)} es realmente una base, calculamos el determinante que tiene por columnas los vectores, si son independientes el resultado ha de ser distinto de cero, lo hacemos con la web [WolframAlpha](http://www.wolframalpha.com):

![determ](/assets/images/determ.png)

Vemos que es distinto de cero, luego efectivamente los vectores forman base. A continuación calculamos el polinomio característico del determinante, que recordemos que no depende de la base usada (propiedad 1), planteamos

$det\begin{pmatrix}2-k&amp;-3&amp;0\\2&amp;-k&amp;0\\0&amp;-3&amp;-k\end{pmatrix}$

y lo resolvemos de nuevo con WolframAlpha: el código es det {{2-k, 2, 0}, {-3, -k, -3}, {0, 0, -k}}, y el resultado $-k (k^2 - 2 k + 6)$, este polinomio tiene una única raíz real, k = 0, con lo cual la matriz no es diagonalizable (ver definición 2).