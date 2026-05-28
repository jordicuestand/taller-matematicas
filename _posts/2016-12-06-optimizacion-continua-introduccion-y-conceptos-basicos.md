---
layout: post
title: "Optimización continua: introducción y conceptos básicos"
date: 2016-12-06 12:38:52 +0000
categories:
  - "Optimización"
tags:
  - "descenso más rápido"
  - "forma cuadrática"
  - "función cuadrática"
  - "gradiente"
  - "método del gradiente"
math: true
---
{% raw %}

### Introducción

Este artículo y otros de la categoria "Optimización"  se basan en mis apuntes como estudiante en la asignatura Optimización Continua, impartida en la Facultad de Matemáticas de la UPC en Barcelona por el catedrático Narcís Nabona.

El campo de la **optimización matemática** tiene como objetivo encontrar un conjunto de valores $x_1,...,x_n$ que minimicen (o maximicen) una función$f(x_1,...,x_n)$ posiblemente sujeto a una serie de restricciones sobre las variables. Cuando las funciones son reales y derivables, el campo se restringe a la denominada **optimización continua**. En general, en las aplicaciones prácticas, los problemas suelen ser demasiado grandes y complicados para obtener una solución exacta por un método analítico, incluso si la función es lineal, por lo que se recurre a cálculo computacional usando algoritmos matemáticos para resolver, por iteraciones sucesivas, el problema hasta un cierto grado de precisión. Las aplicaciones son muy numerosas, podemos citar el análisis de estabilidad reacciones químicas, análisis de estabilidad de sistemas complejo,  síntesis en una red de reactores químicos, estimación de parámetros y reconciliación de datos,  óptica, y diseño atómico y molecular de compuestos.

**Ejemplo 1**: ([Optimization Problems Arising in Optics and Mechanics](http://orfe.princeton.edu/~rvdb/talks/Cornell04/TwoProbs.pdf) - Robert. J Vanderbei) En la búsqueda de posibles planetas que puedan albergar vida semejante a la nuestra, se necesita detectar planetas de un tamaño similar a la Tierra, orbitando en torno a estrellas parecidas al Sol; la luz reflejada por esos planetas es del orden de $10^{-10}$ veces menor a la luz emitida por la estrella, por tanto son fuentes de luz extraordinariamente débiles, pero además, dadas las distancias astronómicas a las que están, la separación por los telescopios de la imagen de la estrella y del planeta necesita tratar con una separación angular del orden de 0.1 segundos de arco, o sea una ángulo de $10^{-5}$ grados. Para ello se utiliza un telescopio con un espejo curvo de 40m de diámetro, el problema que se encuentra es la aparición de anillos de difracción, que enmascaran la luz del planeta que se quiere observar, para ello se recurre a encontrar una forma óptima que minimice la difracción, resultando un problema en un número infinito de dimensiones ([**infinite-dimensional optimization**](https://en.wikipedia.org/wiki/Infinite-dimensional_optimization)).

En lo que sigue supondremos que estamos buscando el máximo de una función real de variable vectorial, $f:\mathbb{R}^n\rightarrow\mathbb{R}$.

## Formas cuadráticas

**Definición 1**: Si Q es una matriz cuadrada simétrica de orden n, la aplicación de $\mathbb{R}^n$ en $\mathbb{R}$,  *f(x) = x'Qx [1]*, es una forma cuadrática (real) donde x es un vector real y x' su transpuesto.

**Ejemplo 2**. La matriz  de orden 2 $Q=\begin{pmatrix}1&amp;-1\\-1&amp;2\end{pmatrix}$ es cuadrada y simétrica,, y define la forma cuadrática real

$f\left(x\right)=x'Qx=\begin{pmatrix}x_1&amp;x_2\end{pmatrix}\begin{pmatrix}1&amp;-1\\-1&amp;2\end{pmatrix}\begin{pmatrix}x_1\\x_2\end{pmatrix}=\begin{pmatrix}x_1-x_2&amp;-x_1+2x_2\end{pmatrix}\begin{pmatrix}x_1\\x_2\end{pmatrix}=\\x_1\left(x_1-x_2\right)+x_2\left(-x_1+2x_2\right)=x_1^2-x_1x_2-x_2x_1+2x_2^2=\\x_1^2-2x_1x_2+2x_2^2$.
## Descomposición espectral de una matriz simétrica

Las matrices simétricas siempre tienen valores propios reales: $Qu_i=\lambda_iu_i,\;\lambda_i\in\mathbb{R}$. Recordemos que los vectores propios $u_i$ de una matriz Q son independientes entre sí, y si además la matriz es simétrica, tambien serán ortogonales entre sí: $u_iu_j=\delta_{ij}=1\;\text{si }i=j,\;0\;\text{si }i\neq j$. Si los normalizamos, $v_i=\frac{u_i}{\parallel u_i\parallel}$, y los disponemos en forma de matriz (que será una matriz ortogonal), $V=\begin{bmatrix}v_1&amp;\dots&amp;v_n\end{bmatrix}$, se cumplirá que $<em>VQV'</em> =\Lambda$, donde $\Lambda$ es la matriz diagonal que tiene por elementos los valores propios. Multiplicando esta igualdad a izquierda y derecha por V' y por V respectivamente, y teniendo en cuenta que VV' = I (pues la traspuesta de una matriz ortogonal es igual a su inversa), nos queda $Q=V'\Lambda V$. Este producto se llama la **descomposición espectral** de la matriz Q.

**Ejemplo 3**:

$Q=\begin{pmatrix}1&amp;-2\\-2&amp;4\end{pmatrix}=V\Lambda V'=\frac1{\sqrt5}\begin{pmatrix}-1&amp;2\\2&amp;1\end{pmatrix}\begin{pmatrix}5&amp;0\\0&amp;0\end{pmatrix}\frac1{\sqrt5}\begin{pmatrix}-1&amp;2\\2&amp;1\end{pmatrix}^T$
## Signo de una forma cuadrática

Si en la definición [1] sustituimos Q por su descomposición espectral obtenemos la expresión

$f(x)=x'\left(V'\Lambda V\right)x=\left(x'V'\right)\Lambda\left(Vx\right)=\left(Vx\right)'\Lambda\left(Vx\right)={\textstyle\sum_i}x_i^2\lambda_i$

cuyo signo sólo depende del signo de los valores propios $\lambda_i$:

**Definición 2**: signo de la forma cuadrática Q.

 	- Q es **definida positiva** si todos los $\lambda_i&gt;0$

 	- Q es **definida negativa** si todos los $\lambda_i&lt;0$

 	- Q es **semidefinida positiva** si todos los $\lambda_i\geq0$

 	- Q es **semidefinida negativa** si todos los $\lambda_i\leq0$

 	- Q es **indefinida** en cualquier otro caso

**Ejemplo 4: **La forma quadràtica de matriz Q del ejemplo 3 es semidefinida positiva, y la forma del ejemplo 2 al tener valores propios positivos $\lambda=\frac12\left(3\pm\sqrt5\right)$ es definida positiva.
## Gráfica de una forma cuadrática

Si *Q* es definida positiva, la gráfica de x'Qx forma un paraboloide elíptico en el cuadrante positivo XYX (fig. 1, izquierda).

$caption id="attachment_150330" align="alignnone" width="500"$![Gráfica de x](/taller-matematicas/assets/images/optimitzacio-3.png) Fig. 1: Gráfica de x'Qx para x: vector de R², siendo Q def.+ o indefinida
Las curvas de nivel son elipses, todos con los mismos ejes cuyas direcciones vienen determinadas por los vectores propios. Si Q es indefinida, entonces x'Qx forma un paraboloide hiperbólico (una "silla de montar", fig.1, derecha).

## Máximos y mínimos de funciones convexas; aplicación a formas cuadráticas

El concepto de [función convexa](http://tallermatematic.ovh/wp/index.php/2014/12/13/aplicaciones-de-las-derivadas/#concavidad) que se estudia en Cálculo es importante en Optimización debido a la siguiente
**Propiedad 1**:  Si una función real es convexa en un intervalo, y en ese intervalo tiene un mínimo local en $x_0$, entonces ese mínimo es absoluto.

La siguiente propiedad relaciona funciones convexas con formas cuadráticas:
**Propiedad 2**: Una forma cuadrática es una función convexa si y sólo si es definida positiva.

Así pues, si una forma cuadrática definida positiva tiene un mínimo en $x_0$, entonces ese mínimo es absoluto.
## Convergencia de algoritmos iterativos

Como comentábamos en la introducción, en Optimización se utilizan algoritmos para aproximar, por iteraciones sucesivas, el óptimo de una función dada. En esta sección repasamos algunos conceptos básicos de tales algoritmos.

**Definición 3**: Eficiencia computacional de un algoritmo.

Es una medida del número de operaciones de cálculo y de su complejidad que necesita ejecutar el algoritmos en cada iteración.

**Definición 4**: Convergencia global.

Un algoritmo que se acerca al óptimo $x^*$  todo lo que queramos por aproximaciones sucesivas ${x_0,x_1,..._x_n,...}$ es globalmente convergente si converge al óptimo sea cual sea el punto inicial $x_0$ tomado.

**Definición 5**: Convergencia local.

Se refiere a la "velocidad" de aproximación al óptimo $x^*$ de un algoritmo cuando estamos en la iteración n-ésima y el valor actual $x_n$ está dentro de un entorno $B(x^*,r)$ de radio r "pequeño". Suele suceder que las primeras iteraciones avanzan rápido, pero cuando nos acercamos al óptimo la convergencia es más lenta, por eso tiene sentido este indicador de convergencia local.

A continuación detallamos un poco estas dos últimas definiciones.

## Convergencia global

El método clásico de asegurar la convergencia global es el de las direcciones de descenso:  dado el punto $x_k$ de la iteración actual el algoritmo ha de buscar una dirección $D_k$ (una recta) a lo largo de la cual se moverá para hallar el próximo punto $x_{k+1}$, la distancia será un parámetro $\alpha$, de forma que podemos definir una función de una variable real $g(\alpha)=f(x_k+\alpha D_k)$; encontrando el valor $\alpha$ que minimice $g(\alpha)$ obtendremos el nuevo punto $x_{k+1}=x_k+\alpha D_k$. A este proceso de minimización a lo largo de la recta $x_k+\alpha D_k$ se le llama *busqueda lineal* (**line search**).

**Propiedad 3**: condición necesaria (no suficiente) de convergencia global.

Para tener convergencia global es necesario que las $D_k$ sean **direcciones de descenso** para la función $f(x)$ que se minimiza, esto es, queremos que se cumpla $f\left(x_k+\alpha D_k\right)&lt;f\left(x_k\right)$ para $\alpha&gt;0$.

¿Qué caracteriza a una dirección de descenso? Desarrollemos en serie de Taylor $f(x_k+\alpha D_k)$ alrededor del punto $x_k$ hasta la primera derivada:

$f\left(x_k+\alpha D_k\right)\approx f\left(x_k\right)+\alpha D_k\nabla f\left(x_k\right)$,

imponiendo la condición de descenso:

$f\left(x_k+\alpha D_k\right)&lt;f\left(x_k\right)+\alpha D_k\nabla f\left(x_k\right)\Rightarrow\alpha D_k\nabla f\left(x_k\right)&lt;0\Rightarrow\boxed{D_k\nabla f\left(x_k\right)&lt;0}$ [1]

Recordando que el gradiente $\nabla f$ y la dirección $D_k$ son vectores, la condición anterior nos dice que su producto escalar ha de ser negativo, intuitivamente, "*las direcciones de descenso apuntan al lado contrario que el vector gradiente*".

## Convergencia local

¿Cómo podemos medir la convergencia local? Lo haremos de forma semejante a las series de números reales, usando los conceptos de orden de convergencia y tasa de convergencia. Dada una sucesión convergente $x_1, x_2, ..., x_k, ...$ con límite $x^*$,
**Definición 6**: orden y tasa de convergencia

diremos que el orden de convergencia es p, un número entero, si p es el mayor entero tal que  el siguiente límite existe:

$\lim_{k\rightarrow\infty}\frac{\left\|x_{k+1}-x^\ast\right\|}{\left\|x_k-x^\ast\right\|^p}=\beta$ [2]

siendo $\beta$ la tasa de convergencia.

En general no es fácil establecer establecer el orden y tasa de convergencia de un algoritmo. En el siguiente apartado vemos el importante algoritmo del gradiente.

## Minimización de funciones cuadráticas con el algoritmo del gradiente

**Definición 7**: función cuadrática

Es toda función vectorial de variable real de la forma $q\left(x\right)=\frac12x'Qx-c'x$, donde $x,c\in\mathbb{R}^n$, $x',c'$ son los vectores transpuestos (vectores fila), y Q es una matriz cuadrada simétrica y definida positiva, con lo cual el término $\frac12x'Qx$ es una forma cuadrática.

La minimización de funciones cuadráticas es importante desde el punto de vista teórico y práctico. De hecho el mínimo $x^*$ es fácil de encontrar de forma analítica, derivando e igualando a cero: $\frac{\operatorname dq}{\operatorname dx}=Qx-c=0\Rightarrow x^\ast=Q^{-1}c$. Si hacemos la segunda derivada, $\frac{\operatorname d^2q}{\operatorname dx^2}=Q$, que al ser Q definida positiva, asegura que el valor $x^*$ es un mínimo. Usaremos las funciones cuadráticas para analizar el comportamiento del algoritmo del gradiente. Empezamos con una definición.

### Definición 8: función error.

Si $x^*$ es el mínimo de una función cuadrática, definimos la función error asociada como

$\varepsilon\left(x\right)=\frac12\left(x-x^\ast\right)^TQ\left(x-x^\ast\right)$ [3]

donde el superíndice T signfica transposición. Desarrollando esta expresión:

$\varepsilon\left(x\right)=\frac12x'Qx-\frac12x'Qx^\ast-\frac12x^{\ast'}Qx+\frac12x^{\ast'}Qx^\ast$

**Ejemplo 5**: La función cuadrática $q\left(x\right)=2x_1^2+x_2^2-x_1-2x_2$, que puede expresarse matricialmente como

$q\left(x\right)=\frac12\begin{pmatrix}x_1&amp;x_2\end{pmatrix}\begin{pmatrix}4&amp;0\\0&amp;2\end{pmatrix}\begin{pmatrix}x_1\\x_2\end{pmatrix}-\begin{pmatrix}1&amp;2\end{pmatrix}\begin{pmatrix}x_1\\x_2\end{pmatrix}=\frac12x'Qx-cx$

tiene el mínimo absoluto (es una función convexa) en $x^\ast=\begin{pmatrix}\frac14&amp;1\end{pmatrix}$; en la siguiente figura representamos sus curvas de nivel, correspondientes a los valores q = 0, 1 y 2, que son una família de elipses concénticas, y el vector óptimo $x^\ast$

![Curvas de nivel y posición del óptimo de la función cuadrática q(x)](/taller-matematicas/assets/images/optimitzacio-4.png)

Dado el punto x=(2,2), su función error es

$\varepsilon\left(x\right)=\frac12\begin{pmatrix}2-\frac12&amp;2-1\end{pmatrix}\begin{pmatrix}4&amp;0\\0&amp;2\end{pmatrix}\begin{pmatrix}2-\frac12\\2-1\end{pmatrix}=5.5$.

El gradiente  de la función es

$\nabla q=\begin{pmatrix}4x_1-1\\2x_2-2\end{pmatrix}$
## Algoritmo del descenso más rápido

Los métodos que obtienen la dirección de descenso usando el vector gradiente son la família de **métodos del gradiente**. Una posible dirección de descenso es precisamente la opuesta al gradiente, evidentemente cumple con la condición de descenso [1]: $D=-\nabla q$. Si actuamos así, estamos usando el **método del descenso más rápido** (***steepest descent method***). Tomando el punto inicial x = (0, 0), el punto siguiente será

$x=\left(0,0\right)+\alpha D=\left(0,0\right)-\alpha\begin{pmatrix}4\cdot0-1\\2\cdot0-2\end{pmatrix}=\begin{pmatrix}\alpha\\2\alpha\end{pmatrix}$

El valor de la función en ese nuevo punto será $q\left(\alpha,2\alpha\right)=2\alpha^2+4\alpha^2-\alpha-4\alpha=6\alpha^2-5\alpha=f\left(\alpha\right)$, una función del parámetro $\alpha$, procedemos a encontrar el mínimo de esta función de una variable: $f'\left(\alpha\right)=12\alpha-5=0\Rightarrow\alpha=5/12$, que es un mínimo ya que $f''\left(\alpha\right)=12&gt;0$. Para este valor, obtenemos el siguiente punto,

$\left(x_1,x_2\right)=\left(0,0\right)+\frac5{12}\begin{pmatrix}1\\2\end{pmatrix}=\begin{pmatrix}5/12\\5/6\end{pmatrix}$

Si repetimos este proceso con el nuevo punto, esto es, calcular el gradiente en ese punto, obtener la función $f(\alpha )$ y minimizarla para encontrar $\alpha$, y así obtener el punto siguiente, obtenemos el siguiente punto de la sucesión, que es (1/4, 1.4). En la figura vemos el avance del algoritmo:
![optimitzacio-8](/taller-matematicas/assets/images/optimitzacio-8.png)

Observad que en el primer paso, el que obtiene el primer vector $x_1$, se toma la dirección perpendicular a la curva de nivel (línea de puntos) que pasa por el punto inicial (0. 0); de hecho este método procede siempre así, en todo punto. Las instrucciones precisas son:

**Método del descenso más rápido (*steepest descent method*)**

Para minimizar una función real $f\left(x\right):\mathbb{R}^n\rightarrow\mathbb{R}$, dado un punto inicial $x_0$, y una tolerancia $\varepsilon$, poner k = 1

 	- paso 1) Calcular la dirección de descenso  $D_k=-\nabla f\left(x_k\right)$

 	- paso 2) obtener $\min_\alpha f\left(x_k+\alpha D_k\right)$ (exploración lineal)

 	- paso 3) obtener el siguiente punto $x_{k+1}=x_k+\alpha D_k$

 	- paso 4) Calcular $\left\|\nabla f\left(x_{k+1}\right)\right\|$

 	- paso 5) si $\left\|\nabla f\left(x_{k+1}\right)\right\|&lt;\varepsilon$, SALIR: óptimo encontrado, $x^\ast\approx x_{k+1}$, en otro caso, incrementar k := k +1, SALTAR al paso 1.

Si especializamos este método a las funciones cuadráticas, obtenemos:

**Método del descenso más rápido para funciones cuadráticas**

Para minimizar una función cuadrática $q\left(x\right)=\frac12x'Qx-c'x$$q\left(x\right):\mathbb{R}^n\rightarrow\mathbb{R}$, dado un punto inicial $x_0$, y una tolerancia $\varepsilon$, poner k = 1

 	- paso 1) Calcular la dirección de descenso  $D_k=-\nabla f\left(x_k\right)=-Qx_k+c$

 	- paso 2) obtener $\min_\alpha f\left(x_k+\alpha D_k\right)$ (exploración lineal), que es $\alpha=\frac{\left\|D_k\right\|^2}{D_k^{'}\cdot Q\cdot D_k}$

 	- paso 3) obtener el siguiente punto $x_{k+1}=x_k+\alpha D_k$

 	- paso 4) Calcular $\left\|\nabla f\left(x_{k+1}\right)\right\|=\left\|-Qx_{k+1}+c\right\|$

 	- paso 5) si $\left\|\nabla f\left(x_{k+1}\right)\right\|&lt;\varepsilon$, SALIR: óptimo encontrado, $x^\ast\approx x_{k+1}$, en otro caso, incrementar k := k +1, SALTAR al paso 1.

**Ejemplo 6**: Aplicando el método del descenso más rápido a la función del ejemplo 5, con el punto inicial (0, 0) y una tolerancia 0.001, obtenemos la secuencia de iteraciones siguiente:

![Fig. 6: iteraciones del método del descenso más rápido, función cuadrática](/taller-matematicas/assets/images/optimitzacio-6.png) Fig. 6: iteraciones del método del descenso más rápido, función cuadrática
En 7 iteraciones obtenemos el mínimo aproximado (0.2499, 0.9996) que está cerca del exacto, (0,25, 1).

## Coste computacional y tasa de convergencia

En algoritmos numéricos, el coste computacional es una estimación del orden de magnitud del número de operaciones aritméticas efectuadas por el algoritmo. En el método del descenso más rápido para funciones cuadráticas, los pasos más costosos son el 1 y el 2: obtener el producto de la matriz Q de dimensión n x n, con el vector x, de dimensión n, necesita n² operaciones, y el producto x'Qx necesita n² + n² operaciones. Como solo nos interesa el orden de magnitud, concluimos que el coste es del orden de n².

Para obtener la tasa de convergencia recordamos la expresión [3] de la función error en el punto $x_k$ a la que añadimos el término $QQ^{-1}$ que es igual a la matriz identidad:

$\begin{array}{l}\varepsilon\left(x\right)=\frac12\left(x-x^\ast\right)'Q\left(x-x^\ast\right)=\frac12\left(x-x^\ast\right)'\left(QQ^{-1}\right)Q\left(x-x^\ast\right)\\\end{array}$

Aplicamos ahora que $Qx_k-c$ es igual al gradiente de q(x), lo llamamos $C_k$, y también usamos que para el vector óptimo $x^*$ se cumple que $Qx^*=c$, con ello obtenemos:

$\begin{array}{l}\varepsilon\left(x\right)=\frac12\left(x_k-x^\ast\right)'\left(QQ^{-1}\right)Q\left(x_k-x^\ast\right)=\frac12\left$-x_k^{\ast'}Q+x_k'Q\right$Q^{-1}\left$Qx_k-Qx_k^\ast\right$=\\\frac12\left$-c'+c'+C_k\right$Q^{-1}\left$C_k+c-c\right$=\frac12C_kQ^{-1}C_k\\\end{array}$

Para la función error en el vector $x_{k+1}$ obtenemos $\frac12C_{k+1}Q^{-1}C_{k+1}$. Recordando que en el paso 3 del algoritmo hacemos $x_{k+1}=x_k+\alpha D_k$, siendo $\alpha=\frac{\left\|D_k\right\|^2}{D_k^{'}\cdot Q\cdot D_k}$ y $D_k=-C_k$, vemos que:

$x_k-x_{k+1}=-\alpha D_k=\frac{\left\|C_k\right\|^2}{C_k'QC_k}C_k$

sustituimos esta expresión en la de la función error:

$\begin{array}{l}\varepsilon\left(x_k\right)-\varepsilon\left(x_{k+1}\right)=\frac12\left(x_k-x^\ast\right)'Q\left(x_k-x^\ast\right)-\frac12\left(x_{k+1}-x^\ast\right)'Q\left(x_{k+1}-x^\ast\right)=\\\frac12\left(x_k-x_{k+1}\right)'Q\left(x_k-x_{k+1}\right)=\frac12\left(\frac{\left\|C_k\right\|^2}{C_k'QC_k}C_k\right)'Q\left(\frac{\left\|C_k\right\|^2}{C_k'QC_k}C_k\right)=\\\frac12\frac{\left\|C_k\right\|^2}{C_k'QC_k}\left(\cancel{C_k'QC_k}\right)\frac{\left\|C_k\right\|^2}{\cancel{C_k'QC_k}}=\frac12\frac{\left\|C_k\right\|^4}{C_k'QC_k}\end{array}$

Entonces el error relativo es:

$\frac{\varepsilon\left(x_k\right)-\varepsilon\left(x_{k+1}\right)}{\varepsilon\left(x_k\right)}=\frac{\left\|C_k\right\|^4}{\left(C_k'Q^{-1}C_k\right)\left(C_k'QC_k\right)}$

Necesitamos ahora el siguiente resultado:
**Lema**: aplicando la [desigualdad de Kantorovich](https://en.wikipedia.org/wiki/Kantorovich_inequality) al caso de la función cuadrática, resulta que se cumple

$\frac{\left\|C_k\right\|^4}{C_k'QC_k}\geq\frac{4Aa}{\left(A+a\right)^2}$

siendo *A*, *a*, los valores propios mayor y menor, respectivamente, de la matriz Q.

Aplicando el lema, llegamos a una cota superior para la tasa de convergencia:
$\beta=\frac{\varepsilon_{k+1}}{\varepsilon_k}\leq\frac{\left(A-a\right)^2}{\left(A+a\right)^2}\leq1$

El algoritmo del descenso más rápido aplicado a una función cuadrática tiene una tasa de convergencia que depende de los valores propios de la forma cuadrática.
Como consecuencia, si A >> a, entonces $\beta$ tiende a 1, y el error tiende a ser constante: el algoritmo se estanca, no avanza. En el otro caso extremo, si A = a, entonces $\beta=0$: el algoritmo alcanza el mínimo en un solo paso. La distribución de los valores propios tiene una relación directa con la geometría de las curvas de nivel. Esta situación sugiere que, cambiando la escala del problema, se puede convertir la geometría de forma que se igualen los valores propios de Q, consiguiendo que el método sea eficiente en casos generales. Esto efectivamente es posible, y conduce a los métodos de gradiente conjugado.

$caption id="attachment_150348" align="alignnone" width="626"$![optimitzacio-9](/taller-matematicas/assets/images/optimitzacio-9.png) Izquierda: la dirección de máximo descenso es la misma para todas las curvas de nivel cuando son esferas concéntricas. Derecha: cuando son elipsoides muy achatados, las direcciones de máximo descenso cambian continuamente, produciendo pasos muy cortos y perjudicando la tasa de convergencia.
**Ejemplo 7**: La tasa de convergencia del método aplicado a la función cuadrática  del ejemplo 5, con A = 4, a = 2, es $\beta=\frac{\varepsilon_{k+1}}{\varepsilon_k}\leq\frac{\left(4-2\right)^2}{\left(4+2\right)^2}=\frac4{36}=\frac19$, estimación que coincide bastante bien con el descenso en el valor del módulo del gradiente observado en el ejemplo 6.
{% endraw %}