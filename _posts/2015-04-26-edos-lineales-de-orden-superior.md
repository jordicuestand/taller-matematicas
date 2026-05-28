---
layout: post
title: "EDOs lineales de orden superior"
date: 2015-04-26 19:07:18 +0000
categories:
  - "Ecuaciones Diferenciales"
  - "Matemáticas"
tags:
  - "coeficientes indeterminados"
  - "combinación lineal"
  - "determinante Wronskiano"
  - "ecuación característica"
  - "ecuación de Euler"
  - "ecuación homogénea"
  - "eucación diferencial de segundo orden"
  - "independencia lineal"
  - "principio de superposición"
  - "variación de constantes"
math: true
---
{% raw %}

- [EDOs lineales de segundo orden](#EDO_lineales)

 	- [Ecuaciones lineales homogéneas de segundo orden](#EDO_lineales)

 	[Combinaciones lineales de soluciones e independencia lineal](#independencia)

 	- [Caso de coeficientes constantes: ecuación característica](#caracteristica)

 	- [Caso de que la ecuación característica tenga solución única](#unica)

 	- [Caso de que la ecuación característica tenga soluciones complejas](#complejas)

 	- [Ecuaciones lineales de segundo orden no homogèneas](#no_homogeneas)

 	[Método de los coeficientes indeterminados](#indeterminados)

 	- Método de variación de constantes

 	- [EDOs lineales de coeficientes constantes de orden superior](#superior)

 	- [Ecuación de Euler](#euler)

![separador2](/taller-matematicas/assets/images/separador2.png)

# EDOs lineales de segundo orden

Tienen la forma $A(x)y''+B(x)y'+C(x)y=F(x).$ En el caso de que $F(x)=0$ se llaman ecuaciones homogéneas, que discutimos ahora.
## Ecuaciones lineales homogéneas de segundo orden

La ecuación homogénea $A(x)y''+B(x)y'+C(x)y=0$ asociada a la ecuación lineal completa$A(x)y''+B(x)y'+C(x)y=F(x)$ tiene la siguiente propiedad:

***Proposición 1 (principio de superposición)***: Si $y_{1},y_{2}$ son dos soluciones independientes de la ecuación lineal, entonces $y=c_{1}y_{1}+c_{2}y_{2}$ es la solución general de la ecuación lineal, siendo $c_{1},c_{2}$ valores reales cualesquiera.

Observemos que el principio de superposición se aplica por igual a ecuaciones lineales homogéneas y completas. Además, exige que las dos soluciones sean independientes. Después del siguiente ejemplo lo aclaramos.

**Ejemplo 1**:  $y_{1}=\cos x$ e $y_{2}=\sin x$ son dos soluciones independientes de la ecuación $\mbox{y''+y=0}$, por tanto $y=c_{1}\cos x+c_{2}\sin x$ es la solución general.

#### ![separador2](/taller-matematicas/assets/images/separador2.png)

#### Combinaciones lineales de soluciones e independencia lineal

Las funciones $y_{1}=\cos x$ e $y_{2}=2\cos x$ som ámbas soluciones de la ecuación del ejemplo 1, pero no son linealmente independientes, pues podemos escribir la segunda en función de la primera: $y=C\sin\left(x\right).$ En general, si tenemos dos funciones $y_1,y_2$ que pueden escribirse una en función de la otra, podremos ponerlas en la forma $C_1y_1+C_2y_2=0;$ derivando respecto de x obtenemos una segunda condición: $C_1y'_1+C_2y'_2=0$. Las dos ecuaciones anteriores forman un sistema de ecuaciones con dos incógnitas:

$\left.\begin{array}{r}C_1y_1+C_2y_2=0\\C_1y'_1+C_2y'_2=0\end{array}\right\}$

Si este sistema tiene soluciones $C_1, C_2$, entonces las funciones $y_1,y_2$ no son independientes; esto sucederá cuando el determinante del sistema no valga cero; por tanto, la condición de independencia será que ese determinante valga cero:

$\begin{bmatrix}y_1&amp;y_2\\y'_1&amp;y'_2\end{bmatrix}=0\Rightarrow y_1,y_2\;\text{linealmente independientes}$

Al determinante anterior formado con las funciones $y_1,y_2$ y sus derivadas se le conoce por el nombre de** determinante Wronskiano** del conjunto de funciones ${y_1,y_2}$, y se generaliza fácilmente a conjuntos de n funciones $\left\{y_1,y_{2,\dots,}y_n\right\}.$

**Ejemplo 2**: Las funciones $e^x, e^{-x},Cosh(x)$ no son linealmente independientes, pues su Wronskiano es:

$\begin{bmatrix}e^x&amp;e^{-x}&amp;Cosh\left(x\right)\\e^x&amp;-e^{-x}&amp;Sinh\left(x\right)\\e^x&amp;e^{-x}&amp;Cosh\left(x\right)\end{bmatrix}=0$

pues la primera y la última fila del determinante son iguales,y por la propiedades de los determinantes, el resultado es cero.

#### ![separador2](/taller-matematicas/assets/images/separador2.png)

#### Caso de coeficientes constantes: ecuación característica

Cuando los  coeficientes $A(x), B(x), C(x)$ de la ecuación homogénea son constantes $A, B, C$, que no dependen de $x$, sabemos que las funciones del tipo $y=e^{rx}$ son soluciones particulares, pues:

$y=e^{rx}\Rightarrow Ay''+By'+Cy=Ar^2e^{rx}+Bre^{rx}+Ce^{rx}=e^{rx}\left(Ar^2+Br+C\right)$

así que la ecuación homogénea equivale a:

$e^{rx}\left(Ar^2+Br+C\right)=0\Rightarrow Ar^2+Br+C=0$,

que se reduce a una ecuación algebraica de segundo grado en r, la cual se denomina ecuación característica de la ecuación diferencial lineal homogénea. Resolviéndola, obtenemos dos valores $r_{1},r_{2}$, y la solución general, por la proposición 1,  será la combinación lineal $y=c_{1}e^{r_{1}x}+c_{2}e^{r_{2}x}$.

**Ejemplo 3**: Resolver $y''-6y'=0$

La ecuación característica se obtiene directamente sustituyendo la "y" por "r" y el orden de la derivada por el exponente correspondiente:  $r^2-6r=0$; la solución es $r^2-6r=0\Rightarrow r_1=0,\;r_2=6$, y la solución general es $y=c_1e^{0x}+c_2e^{6x}=c_1+c_2e^{6x}$.
#### ![separador2](/taller-matematicas/assets/images/separador2.png)

#### Caso de que la ecuación característica tenga solución única

Si la ecuación característica tiene una raíz doble $r_{1}=r_{2}=r$ entonces  no tenemos dos soluciones independientes $y_{1},y_{2}$ ; en tal caso la solución general viene dada por $y=\left(c_{1}+c_{2}x\right)e^{rx}.$

**Ejemplo 4**: Resolver $y''-2y'+y=0.$

La ecuación característica $r^{2}-2r+1=0$ tiene una única solución $r=1$, y por tanto la solución general será $y=\left(c_{1}+c_{2}x\right)e^{x}$.
#### ![separador2](/taller-matematicas/assets/images/separador2.png)

#### Caso de que la ecuación característica tenga soluciones complejas

Cuando la ecuación característica tenga un par de raíces complejas conjugadas $r_{1}=a+bi, r_{2}=a-bi$, entonces la solució general viene dada por $y=e^{ax}\left(c_{1}\cos bx+c_{2}\sin bx\right)$.

**Ejemplo 5**: Resolver $y''-4y'+5y=0$.

La ecuación característica $r^{2}-4r+5=0$ tiene raíces complejas $r_{1}=2+i, r_{2}=2-i$, la solución general és $y=e^{2x}\left(c_{1}\cos x+c_{2}\sin x\right)$.

![separador2](/taller-matematicas/assets/images/separador2.png)
## Ecuaciones lineales de segundo orden no homogèneas

La ecuación lineal no homogènea $A(x)y''+B(x)y'+C(x)y=F(x)$, por ser lineal,  tiene la propiedad de que, si tenemos una solución particular cualquiera $y_{p}(x)$, y si sabemos resolver la ecuación homogénea asociada $A(x)y''+B(x)y'+C(x)y=0$, siendo $y_{h}(x)$ la solución general
de la homogènea, entonces la solución general de la ecuación no homogénea es $y(x)=y_{h}(x)+y_{p}(x)$. Acabamos de ver que si los coeficientes son constantes, siempre podremos encontrar la solución general de la homogènea.

**Ejemplo 6**: la función $y_{p}(x)=3x$ es una solución particular de $y''+4y=12x$. Si resolvemos la ecuación homogènia $y''+4y=0$ obtenemos  $y_{h}(x)=c_{1}\cos x+c_{2}\sin x$, así pues la solución general de la no homogénea es $y=3x+c_{1}\cos x+c_{2}\sin x$.

####  ![separador2](/taller-matematicas/assets/images/separador2.png)

## Método de los coeficientes indeterminados

Si en la ecuación lineal completa $A(x)y''+B(x)y'+C(x)y=F(x)$ el término $F(x)$ es un polinomio en x, o bien una exponencial $e^{rx}$, o bien una función $sin(kx)$ o $cos(kx)$, o bien es una suma de esas funciones, entonces podemos intentar aplicar este método para encontrar una solución particular de la ecuación.

El método consiste en ensayar como solución una combinación lineal parecida a $f(x)$:

 	- si $f(x)$ es un polinomio de grado n, ensayamos para $y_p$ un polinomio del mismo grado y coeficientes indeterminados

 	- si $f(x)=pe^{qx}$, ensayamos para $y_p$ una función $y_p=Ae^{Bx}$

 	- si $f(x)=sin(kx)$ , ensayamos para $y_p$ una función $y_p=Asin(kx)+Bcos(kx)$

 	- si $f(x)$ es una suma  de los tipos anteriores, aplicamos la proposición 1 (superposición): encontraremos soluciones particulares para cada tipo por separado, la solución buscada será la suma de las anteriores.

**Ejemplo 7:** Para encontrar una solución particular de $y''+y=2x^3$ ensayamos $y_p=Ax^3+Bx^2+Cx+D$. Derivamos y sustituimos en la ecuación:

$\begin{array}{l}y_p=Ax^3+Bx^2+Cx+D;\\y'_p=3Ax^2+2Bx+C;\\y''_p=6Ax+2B;\\y''+y=2x^3\Leftrightarrow\left(6Ax+2B\right)+\left(Ax^3+Bx^2+Cx+D\right)=2x^3\end{array}$

Operando e igualando términos:

$\begin{array}{l}Ax^3+Bx^2+\left(C+6A\right)x+\left(2B+D\right)=2x^3\Leftrightarrow\\A=2,B=0,\\6A+C=0\Leftrightarrow12+C=0\Leftrightarrow C=-12,\\2B+D=0\Leftrightarrow D=0\end{array}$

Hemos obtenido una solución particular: $y_p=2x^3-12x.$

**Ejemplo 8**:  Para encontrar una solución particular de $y''+y=2x^3-2e^x$ primero ensayamos $y_p=Ax^3+Bx^2+Cx+D$ y después ensayamos $y_p=me^x$. La primera solución particular la hemos obtenido en el ejemplo anterior, para la segunda, derivamos y sustituimos:

$\begin{array}{l}y_p=me^x\Rightarrow y'_p=y''_p=y;\\y_p''+y_p=-2e^x\Leftrightarrow2y_p=2me^x=-2e^x\Rightarrow m=-1\end{array}$

entonces la solución particular será la suma de las obtenidas: $y_p=2x^3-12x-e^x.$

![separador2](/taller-matematicas/assets/images/separador2.png)

### Caso de que la solución particular a ensayar sea solución de la homogénea asociada

Cuando en la ecuación lineal completa $A(x)y''+B(x)y'+C(x)y=F(x)$ el término $F(x)$ sea una solución de la homogénea asociada $A(x)y''+B(x)y'+C(x)y=0$ el método anterior fallará; en ese caso ensayamos $y_p=x^a·F(x)$ siendo $a$ el menor valor entero posible tal que $y_p$ no es solución de la homogénea asociada; tal valor dependerá de la ecuación característica asociada a la homogénea: si tiene raíces simples bastarà con tomar $a=1$, si tiene raíces dobles tomamos $a=2$.

**Ejemplo 9**:  Para encontrar la solución general de $y''-y=2-2e^x$ primero encontramos la solución general de la homogénea: $r^2-1=0$ y tenemos las raíces $r=\pm1\Rightarrow y_h=C_1e^x+C_2e^{-x}$. Para encontrar la solución general no podemos ensayar $y_p=me^x$ pues es una solución de la homogénea, $y_p=me^x\Rightarrow y''-y=me^x-me^x=0$, pero podemos provar $y_p=mx^a·e^x$, tomando a=1 pues la multiplicidad de las raíces de la homogénea es 1:

$\begin{array}{l}y_p=mxe^x\Rightarrow y'_p=me^x+mxe^x=\left(1+x\right)me^x;y''_p=me^x+\left(1+x\right)me^x=\left(2+x\right)me^x;\;\\y''-y=\left(2+x\right)me^x-mxe^x=2me^x=-2e^x\Rightarrow m=-1\end{array}$

Tenemos pues la solución general $y=y_h+y_p=C_1e^x+C_2e^{-x}-xe^x.$

## ![separador2](/taller-matematicas/assets/images/separador2.png)

## 

## Método de variación de constantes

El mètodo de coeficientes indeterminados suele ser el más simple para obtener soluciones particulares, pero sólo es útil para ecuaciones con términos independientes de las formas a) polinomios en x, b) exponenciales $e^{rx}$, c) sen(kx) o cos(kx), d) una combinación lineal de los anteriores. En este apartado vemos un método que, en principio, puede aplicarse siempre, claro que puede generar integrales demasiado complicadas, pero no hay una limitación genérica como sucede con el método de coeficientes indeterminados.

Si tenemos la ecuación lineal de segundo orden completa $y''+P(x)y'+Q(x)y=F(x)$, de la cual hemos obtenido la solución $y_h=C_1y_1+C_2y_2$ de la homogénea asociada $y''+P(x)y'+Q(x)y=0$, el método de variación de contantes ensaya una solución $y=u_1y_1+u_2y_2$ en la que usamos las funciones $y_1, y_2$ de la $y_h$ pero substituimos las contantes $C_1, C_2$ por funciones desconocidas $u_1, u_2$ (de ahí el nombre "variación de constantes"). Entonces tenemos dos incógnitas, $u_1, u_2$, y una única ecuación que deben cumplir, $y''+P(x)y'+Q(x)y=F(x)$, teniendo más incógnitas que ecuaciones la solución queda indeterminada; podemos añadir una segunda ecuación para eliminar la indeterminación, ¿cuál?

 Derivando la y: $y'=u_1'y_1+u_1y_1'+u_2'y_2+u_2y_2'=\left(u_1'y_1+u_2'y_2\right)+\left(u_1y_1'+u_2y_2'\right)$, en este método se impone que se anule el miembro $\left(u_1'y_1+u_2'y_2\right)$, de forma que la expresión de la derivada de y se simplifica: $y'=\left(u_1'y_1+u_2'y_2\right)+\left(u_1y_1'+u_2y_2'\right)=u_1y_1'+u_2y_2'$. Volviendo a derivar para obtener la segunda derivada: $y''=u_1'y_1'+u_1y_1''+u_2'y_2'+u_2y_2''=\left(u_1'y_1'+u_2'y_2'\right)+\left(u_1y_1''+u_2y_2''\right$

Pero tanto $y_1$ como $y_2$ son soluciones de la ecuación homogénea asociada, y cumplirán: $$y''+P(x)y'+Q(x)y=0\Leftrightarrow y_1''=-P(x)y_1'-Q(x)y_1,\;y_2''=-P(x)y_2'-Q(x)y_2$$

Sustituimos las expresiones de $y_1'', y_2''$ en la expresión de y'':

$\begin{array}{l}y''=\left(u_1'y_1'+u_2'y_2'\right)+\left(u_1y_1''+u_2y_2''\right)=\\\left(u_1'y_1'+u_2'y_2'\right)+u_1\left(-P(x)y_1'-Q(x)y_1\right)+u_2\left(-P(x)y_2'-Q(x)y_2\right)=\\\left(u_1'y_1'+u_2'y_2'\right)-\left(u_1y_1'+u_2y_2'\right)P(x)-\left(u_1y_1+u_2y_2\right)Q(x)=\\\left(u_1'y_1'+u_2'y_2'\right)-y'P(x)-yQ(x)\\\end{array}$

Substituyendo en la ecuación completa queda reducida a $\begin{array}{l}\left$\left(u_1'y_1'+u_2'y_2'\right)-y'P(x)-yQ(x)\right$+P(x)y'+Q(x)y=F(x)\Leftrightarrow\\u_1'y_1'+u_2'y_2'=F(x)\\\\\end{array}$.

En definitiva, el método reduce la ecuación de segundo orden lineal  completa a un sistema de dos ecuaciones lineales de orden 1:

$\left.\begin{array}{r}u_1'y_1'+u_2'y_2'=F(x)\\u_1'y_1+u_2'y_2=0\end{array}\right\}$

**Ejemplo 10**: Resolver $y''+y=\tan\left(x\right)$.

La ecuación característica de la homogénea asociada es $r^2+1=0$ con raíces $\pmi$, y por tanto la solución general de la homogénea es $y_h=C_1\sin\left(x\right)+C_2\cos\left(x\right)$, identificamos $y_1=\sin\left(x\right), y_2=\cos\left(x\right)$, derivamos ambas: $y_1'=\cos\left(x\right), y_2'=-\sin\left(x\right)$, y escribimos el sistema de ecuaciones:

$\left.\begin{array}{r}u_1'\cos\left(x\right)-u_2'\sin\left(x\right)=\tan\left(x\right)\\u_1'\sin\left(x\right)+u_2'\cos\left(x\right)=0\end{array}\right\}$

Multiplicamos la 1a ecuación por cos(x) y la 2a por sen(x):

$\left.\begin{array}{r}u_1'\cos^2\left(x\right)-u_2'\cos\left(x\right)\sin\left(x\right)=\tan\left(x\right)\\u_1'\sin^2\left(x\right)+u_2'\sin\left(x\right)\cos\left(x\right)=0\end{array}\right\}$

Sumamos ambas ecuaciones para eliminar una de las incógnitas, obtenemos una única EDO que en este caso es separable:

$\begin{array}{l}u_1'\left(\cos^2\left(x\right)+\sin^2\left(x\right)\right)=\tan\left(x\right)\Leftrightarrow u_1'=\tan\left(x\right)\Leftrightarrow\operatorname du=\tan\left(x\right)\operatorname dx\Leftrightarrow\\u_1=\int\tan\left(x\right)\operatorname dx=-\ln\left(\cos\left(x\right)\right)\end{array}$

Substituyendo en alguna de las ecuaciones del sistema, por ejemplo en la primera, obtenemos:

$u_1'\sin\left(x\right)+u_2'\cos\left(x\right)=0\Leftrightarrow u_2'=-u_1'\tan\left(x\right)=-\tan^2\left(x\right)$

Ahora que ya tenemos $u_1, u_2$ podemos escribir la solución particular:

$\begin{array}{l}y_p=u_1y_1+u_2y_2=-\ln\left(\cos\left(x\right)\right)\cdot\sin\left(x\right)-\tan^2\left(x\right)\cdot\cos\left(x\right)=\\-\sin\left(x\right)\left$\ln\left(\cos\left(x\right)\right)+\tan\left(x\right)\right$\end{array}$

y la solución general la obtenemos sumando la de la homogénea y la particular:

$y=y_h+y_p=C_1\cos\left(x\right)+C_2\sin\left(x\right)-\sin\left(x\right)\left$\ln\left(\cos\left(x\right)\right)+\tan\left(x\right)\right$.$

**NOTA**: De hecho el sistema de dos ecuaciones se puede resolver de forma general, por ejemplo aplicando la regla de Cramer:

$\left.\begin{array}{r}u_1'y_1'+u_2'y_2'=F(x)\\u_1'y_1+u_2'y_2=0\end{array}\right\}\Rightarrow u_1'=\frac{\begin{vmatrix}F(x)&amp;y_2'\\0&amp;y_2\end{vmatrix}}{\begin{vmatrix}y_1'&amp;y_2'\\y_1&amp;y_2\end{vmatrix}}=\frac{F(x)y_2}{y_1'y_2-y_2'y_1}$

que nos proporciona la primera incógnita:

$u_1=\int\frac{F(x)y_2}{y_1'y_2-y_2'y_1}\operatorname dx$

y para la segunda tenemos:

$u_2'=\frac{\begin{vmatrix}y_1'&amp;F(x)\\y_1&amp;0\end{vmatrix}}{\begin{vmatrix}y_1'&amp;y_2'\\y_1&amp;y_2\end{vmatrix}}=\frac{F(x)y_1}{y_1'y_2-y_2'y_1}\Rightarrow u_2=\int\frac{F(x)y_1}{y_1'y_2-y_2'y_1}\operatorname dx$,

con lo cual, para el caso de EDO lineales de segundo orden, obtenemos la denominada **fórmula de variación de parámetros**, aplicándola, no es necesario seguir los pasos del método:

$u_1=\int\frac{F(x)y_2}{y_1'y_2-y_2'y_1}\operatorname dx,\;u_2=\int\frac{F(x)y_1}{y_1'y_2-y_2'y_1}\operatorname dx$

De paso, observemos que el determinante del denominador es equivalente al Wronskiano de las funciones $y_1, y_2$, por tanto siempre que estas soluciones de la homogénea sean linealmente independientes el sistema tendrá solución y existirá la solución particular.

De hecho, la fórmula de variación de parámetros puede generalizarse a EDOs lineales de orden n: si llamamos $W_i$ al determinante que resulta de substituir la columna i-ésima del Wronskiano por el término independiente del sistema $\begin{bmatrix}F(x)\\0\\\vdots\\0\end{bmatrix}$, resulta la fórmula que nos da cada función $u_i(x)$, que es simplemente:

$\boxed{u_i=\int\frac{F(x)W_i}W\operatorname dx}$

## EDOs lineales de coeficientes constantes de orden superior

Todo lo visto hasta ahora para EDOs lineales de segundo orden puede generalizarse para órdenes superiores.
**Ejemplo 11**: la ecuación lineal homogénea de tercer orden $y'''+y''-2y'=0$ tiene la ecuación característica $r^3+r^2-2r=0$ cuyas raíces podemos encontrar fácilmente, son $r=0, 1, -2$, entonces la solución general de la ecuación es $y=C_1+C_2e^x+C_3e^{-2x}.$

Para la ecuación lineal completa de orden n $a_ny^{(n}+a_{n-1}y^{(n-1}+\dots a_1y^'+a_0y=F(x)$ tendremos que resolver primero la homogénea asociada encontrando las n raíces de la ecuación característica, obteniendo n soluciones independientes de la homogénea, y después necesitaremos obtener una solución particular independiente de la completa, para expresar la solución general como $y=y_h+y_p=\left(A_ny_{h_n}+A_{h_{n-1}}y+\dots A_1y_{h_1}\right)+y_p$ La independencia de n soluciones puede comprobarse calculando el Wronskiano, que contiene las funciones y sus derivadas hasta el orden n-1:

$\begin{bmatrix}y_1&amp;\cdots&amp;y_n\\\vdots&amp;\vdots&amp;\vdots\\y_1^{(n-1}&amp;&amp;y_n^{(n-1}\end{bmatrix}\neq0$

 **Ejemplo 12**: Resolver la ecuación lineal de cuarto orden $y^{(4}-y=3cos(x)$.

La ecuación característica es $r^4-1=0$ con raíces $r^4-1=0\Leftrightarrow r^2=\pm1\Leftrightarrow r=\pm1,\pm\sqrt{-1}=\pm i$, como hemos visto en un apartado anterior, las soluciones independientes de la homogénea son $e^x, e^{-x}, cos(x), sin(x)$, y la solución general de la homogénea es $y_h=C_1e^x+C_2e^{-x}+C_3\cos\left(x\right)+C_4\sin\left(x\right).$ Para la solución particular, como el término independiente es $F(x)=3\cos(x)$ el método de coeficientes indeterminados sugiere $y_p=A\cos(x)+B\sin(x)$ pero en este caso esta función forma parte de la solución de la homogénea, con multiplicidad 1, por tanto tomamos $y_p=Ax\cos(x)+Bx\sin(x)$, derivando cuatro veces obtenemos $y_p^{(4}=(4A+Bx)\sin(x)+(Ax-4B)\cos(x)$, sustituimos en la ecuación completa:

$\begin{array}{l}\begin{array}{l}y^{(4}-y=3cos(x)\Leftrightarrow\\(4A+Bx)\sin(x)+(Ax-4B)\cos(x)-Ax\cos(x)+Bx\sin(x)=3cos(x)\Leftrightarrow\end{array}\\4A\sin(x)-4Bcos(x)=3cos(x)\Rightarrow A=0,\;B=-\frac34\end{array},$

obtenemos la solución general:

$y=C_1e^x+C_2e^{-x}+C_3\cos\left(x\right)+C_4\sin\left(x\right)-\frac34x\cdot\sin\left(x\right)$

 ![separador2](/taller-matematicas/assets/images/separador2.png)

## Ecuación de Euler

Todo los que hemos visto hasta ahora son ecuaciones lineales con coeficientes constantes, pues las de coeficientes variables son en general o muy difíciles o imposibles de resolver analíticamente. Uno de los pocos casos resolubles es el de la ecuación de Euler:

$a_nx^ny^{(n}+\dots+a_1xy'+a_0y=F(x)$

o sea es del tipo en el que *las potencias de x disminuyen como los órdenes de derivación de y*, incluso cuando no coinciden la potencia y el orden en cada término, ya que entonces podemos multiplicar (o dividir según convenga) toda la ecuación por la potencia de x conveniente. Por ejemplo, la ecuación $3x^2y^{'''}+5xy''-y'\;+\frac yx=e^x$ se convierte en el tipo Euler multiplicándola por x para obtener $3x^3y^{'''}+5x^2y''-xy'\;+y=xe^x.$

Para resolver la homogénea asociada se ensaya $y_h=x^r$, que proporcionará una ecuación en r. Para encontrar una solución particular se realiza el cambio $x=e^t$ que convierte la ecuación de Euler en otra de coeficientes constantes.

**Ejemplo 13**: Resolver $3x^3y^{'''}+5x^2y''-xy'\;+y=x.$

Probamos $y_h=x^r$ en la homogénea; calculamos las derivadas sucesivas y sustituimos en la ecuación homogénea:

$\begin{array}{l}y_h=x^r;\;y'=rx^{r-1};\;y''=r\left(r-1\right)x^{r-2};\;y_h^{(3}=r\left(r-1\right)\left(r-2\right)x^{r-3}\Rightarrow\\3x^3y^{'''}+5x^2y''-xy'\;+y=0\Rightarrow\\3x^3r\left(r-1\right)\left(r-2\right)x^{r-3}+5x^2r\left(r-1\right)x^{r-2}-xrx^{r-1}+x^r=0\Rightarrow\\3r\left(r-1\right)\left(r-2\right)+5r\left(r-1\right)-r+1=0\Leftrightarrow\end{array}$

Resolvemos la ecuación: una raíz es inmediato ver que es $r=1$, dividiendo por $r-1$ obtenemos la ecuación $3r^2-r-1=0$ con raíces $\frac{1\pm\sqrt{13}}6.$ La solución de la homogénea es pues:

$y_h=C_1x+C_2x^{\frac{1+\sqrt{13}}6}+C_3x^{\frac{1-\sqrt{13}}6x}$

Para encontrar una solución particular de la completa, la transformamos con el cambio $x=e^t$, primero obtenemos las derivadas de y respecto de la variable t, aplicando la igualdad $\frac{\operatorname dy}{\operatorname dx}=\frac{\operatorname dy}{\operatorname dt}\frac{\operatorname dt}{\operatorname dx}$, comanzando por y':

$y'=\frac{\operatorname dy}{\operatorname dx}=\frac{\operatorname dy}{\operatorname dt}\frac{\operatorname dt}{\operatorname dx}=\frac{\operatorname dy}{\operatorname dt}\left(\frac{\operatorname dx}{\operatorname dt}\right)^{-1}=\frac{\operatorname dy}{\operatorname dt}\left(\frac{\operatorname de^t}{\operatorname dt}\right)^{-1}=\frac{\operatorname dy}{\operatorname dt}e^{-t}$

y aplicando la misma técnica reiteradamente:

$\begin{array}{l}y''=\frac{\operatorname dy'}{\operatorname dx}=\frac d{dx}\left(\frac{\operatorname dy}{\operatorname dt}e^{-t}\right)=\frac d{dt}\left(\frac{\operatorname dy}{\operatorname dt}e^{-t}\right)\frac{\operatorname dt}{\operatorname dx}=\left(\frac{\operatorname d^2y}{\operatorname dt^2}e^{-t}-\frac{\operatorname dy}{\operatorname
dt}e^{-t}\right)e^{-t}=e^{-2t}\left(\frac{\operatorname d^2y}{\operatorname dt^2}-\frac{\operatorname dy}{\operatorname dt}\right);\\y'''=\frac{\operatorname dy''}{\operatorname dx}=\frac d{dx}\left$e^{-2t}\left(\frac{\operatorname d^2y}{\operatorname dt^2}-\frac{\operatorname dy}{\operatorname dt}\right)\right$=\frac d{dt}\left$e^{-2t}\left(\frac{\operatorname d^2y}{\operatorname dt^2}-\frac{\operatorname dy}{\operatorname dt}\right)\right$\frac{\operatorname dt}{\operatorname dx}=\\\left$-2e^{-2t}\left(\frac{\operatorname d^2y}{\operatorname dt^2}-\frac{\operatorname dy}{\operatorname dt}\right)+e^{-2t}\left(\frac{\operatorname d^3y}{\operatorname dt^3}-\frac{\operatorname d^2y}{\operatorname dt^2}\right)\right$e^{-t}=\\e^{-3t}\left$\frac{\operatorname d^3y}{\operatorname dt^3}-3\frac{\operatorname d^2y}{\operatorname dt^2}+2\frac{\operatorname dy}{\operatorname dt}\right$\\\end{array}$

Sustituimos en la ecuación original:

$\begin{array}{l}3x^3y^{'''}+5x^2y''-xy'\;+y=x\Leftrightarrow\\3e^{3t}e^{-3t}\left$\frac{\operatorname d^3y}{\operatorname dt^3}-3\frac{\operatorname d^2y}{\operatorname dt^2}+2\frac{\operatorname dy}{\operatorname dt}\right$+5e^{2t}e^{-2t}\left(\frac{\operatorname d^2y}{\operatorname dt^2}-\frac{\operatorname dy}{\operatorname dt}\right)-e^t\frac{\operatorname dy}{\operatorname dt}e^{-t}+y=e^t\end{array}$,

operando, nos queda una ecuación lineal con coeficientes constantes:

$3\frac{\operatorname d^3y}{\operatorname dt^3}-4\frac{\operatorname d^2y}{\operatorname dt^2}+y=e^t$

ensayamos una solución del tipo $Ate^t$, ya que $Ae^t$ es una solución de la homogénea:

$\begin{array}{l}y=Ate^t;\;\frac{\operatorname dy}{\operatorname dt}=\left(1+t\right)Ae^t;\frac{\operatorname d^2y}{\operatorname dt^2}=\left(2+t\right)Ae^t;\frac{\operatorname d^3y}{\operatorname dt^3}=\left(3+t\right)Ae^t;\\3\frac{\operatorname d^3y}{\operatorname dt^3}-4\frac{\operatorname d^2y}{\operatorname dt^2}+y=e^t\Leftrightarrow\left$3\left(3+t\right)-4\left(2+t\right)+t\right$Ae^t=e^t\Leftrightarrow A=1\end{array}$

La solución particular la obtenemos deshaciendo el cambio de variable: $y_p=te^t=\ln\left(x\right)\cdot x;\;$ y la solución general será:

$y=y_h+y_p=C_1x+C_2x^{\frac{1+\sqrt{13}}6}+C_3x^{\frac{1-\sqrt{13}}6x}+x\ln\left(x\right)\;$.
{% endraw %}