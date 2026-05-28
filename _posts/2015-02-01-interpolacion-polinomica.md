---
layout: post
title: "Interpolación polinómica"
date: 2015-02-01 12:20:48 +0000
math: true
---
{% raw %}

## Introducción

A continuación tenemos una tabla con el censo de población de una província de España en el período de tiempo entre 1920 y 1970 del siglo XX:


Nos preguntamos: ¿podemos usar  estos datos para estimar la población en, digamos, 1965? ¿y para hacer una estimación de la población en el año 1910? Si tuviéramos una función *población=f(año)* que, para los años dados en la tabla, proporcionase exactamente los valores de la población de la tabla, entonces podríamos usar esa función para aproximar los valores desconocidos. En este post estudiamos cómo conseguir una función polinómica que realizará esa función. Para justificar que realmente se puede hacer, tenemos el siguiente teorema:

***Teorema de aproximación polinómica de Weierstrass**: Si $f:\left$a,b\right$\rightarrow\mathbb{R}$ es continua, entonces dado un $\varepsilon&gt;0$ cualquiera, existirá un polinomio $P(x)$ tal que $\left|f\left(x\right)-P\left(x\right)\right|&lt;\varepsilon$ para todo $x\in\left$a,b\right$.$*

## Polinomio interpolador de Newton

Queremos calcular los coeficientes de un polinomio $P(x)$ tal que coincida exactamente con la tabla de valores dados $\left(x_0,y_0\right),\;\left(x_1,y_1\right),\dots,\left(x_n,y_n\right).$ Supongamos para empezar que solo tenemos dos puntos $(x,y)$ tales como $\left(x_0,y_0\right),\left(x_1,y_1\right).$ El polinomio $P(x)$ más simple que pasa por esos dos puntos es la recta dada por los puntos:

$\begin{array}{l}\left.\begin{array}{r}\begin{array}{l}y_0=A+Bx_0\\y_1=A+Bx_1\end{array}\end{array}\right\}\Rightarrow y_1-y_0=B\left(x_1-x_0\right)\Rightarrow B=\frac{y_1-y_0}{x_1-x_0};\\A=y_0-Bx_0=y_0-\frac{y_1-y_0}{x_1-x_0}x_0=\frac{y_0\left(x_1-x_0\right)-\left(y_1-y_0\right)x_0}{x_1-x_0}=y_0\end{array},$

o sea la recta de ecuación $y=y_0+\frac{y_1-y_0}{x_1-x_0}x.$ Veamos ahora que esta recta puede ponerse en la forma $P(x)=a_0+a_1\left(x-x_0\right),$ en efecto:

$\begin{array}{l}y_0=P(x_0)=a_0+a_1\left(x_0-x_0\right)=a_0\Rightarrow y_0=a_0\\y_1=P(x_1)=a_0+a_1\left(x_1-x_0\right)=y_0+a_1\left(x_1-x_0\right)\Rightarrow\;a_1=\frac{y_1-y_0}{x_1-x_0}\;\end{array}.$

Podemos generalizar este polinomio al caso de n+1 puntos (se demuestra por el [razonamiento por inducción](http://es.wikipedia.org/wiki/Inducci%C3%B3n_matem%C3%A1tica)):

$P\left(x\right)=a_0+a_1\left(x-x_0\right)+a_2\left(x-x_1\right)\left(x-x_0\right)+\dots+a_n\left(x-x_n\right)\dots\left(x-x_0\right),$

pues tenemos que:

$\begin{array}{l}P\left(x_0\right)=a_0+a_1\left(x_0-x_0\right)+a_2\left(x_0-x_1\right)\left(x_0-x_0\right)+\dots+a_n\left(x_0-x_n\right)\dots\left(x_0-x_0\right)=a_0;\\P\left(x_1\right)=a_0+a_1\left(x_1-x_0\right)+a_2\left(x_1-x_1\right)\left(x_1-x_0\right)+\dots+a_n\left(x_1-x_n\right)\dots\left(x_1-x_0\right)=a_0+a_1\left(x_1-x_0\right)\\\cdots\\\end{array}.$
De las anteriores igualdades se deduce $a_0=y_0,\;a_1=\frac{y_1-y_0}{x_1-x_0};$ para el resto de coeficientes es más cómodo en vez de plantear las ecuaciones usar el denominado **método de diferencias divididas**; para ello introducimos la siguiente notación:

	- diferencias divididas de orden cero: $f\left$x_i\right$=f\left(x_i\right)$

	- diferencias divididas de orden uno: $f\left$x_{i-1},x_i\right$=\frac{f\left$x_i\right$-f\left$x_{i-1}\right$}{x_i-x_{i-1}}$

	- diferencias divididas de orden dos: $f\left$x_{i-2},x_{i-1},x_i\right$=\frac{f\left$x_{i-1},x_i\right$-f\left$x_{i-2},x_{i-1}\right$}{x_i-x_{i-2}}$

	- diferencias divididas de orden k: $f\left$x_{i-k},\dots,x_i\right$=\frac{f\left$x_{i-k+1},\dots,x_i\right$-f\left$x_{i-k},\dots,x_{i-1}\right$}{x_i-x_{i-k}}$

Con esta notación, el polinomio interpolador de Newton es:

$P\left(x\right)=f\left$x_0\right$+f\left$x_0,x_1\right$\left(x-x_0\right)+f\left$x_0,x_1,x_2\right$\left(x-x_0\right)\left(x-x_1\right)+\dots+f\left$x_0,x_1,\dots,x_n\right$\left(x-x_0\right)\left(x-x_1\right)\dots\left(x-x_{n-1}\right).$

**Ejemplo 1**: Calcular el polinomio interpolador de Newton para los datos del censo dados en la introducción, para los años 1950-60-70.

Formamos la tabla de diferencias divididas:

   

| **x** 
| **dif orden 0** 
| **dif.orden 1** 
| **dif.orden 2** 

| 1950 
| 49 
|  
|  

| 1960 
| 69 
| $\frac{(69-49)}{(1960-1950)}=2$ 
|  

| 1970 
| 133 
| $\frac{(133-69)}{(1970-1960)}=6.4$ 
| $\frac{6.4-2}{(1970-1950)}=\frac{11}{50}$ 

Los coeficientes del polinomio vienen dados por la diagonal de la tabla: 49, 2, 11/50, de forma que el polinomio es de grado 2: $P\left(x\right)=49+2\left(x-1950\right)+\frac{11}{50}\left(x-1950\right)\left(x-1960\right).$

**Ejemplo 2**: Calcular el polinomio interpolador de Newton para los datos del censo dados en la introducción, para los años 1940-60-70

Ampliamos la tabla anterior con una nueva fila y una nueva columna, los cálculos que ya teníamos se mantienen
    

| x 
| dif orden 0 
| dif.orden 1 
| dif.orden 2 
| dif. Orden 3 

| 1940 
| 48 
|  
|  
|  

| 1950 
| 49 
| $\frac{(49-48)}{(1950-1940)}=0.1$ 
|  
|  

| 1960 
| 69 
| 2 
| $\frac{(2-0.1)}{(1960-1940)}=0.095$ 
|  

| 1970 
| 133 
| 6.4 
| $\frac{11}{50}$ 
| $\frac{({\displaystyle\frac{11}{50}}-0.095)}{(1970-1940)}=\frac1{240}$ 

Los coeficientes son 48, 0.1, 0.095, 1/240, y el polinomio es de grado 3:

$P\left(x\right)=48+0.1\left(x-1940\right)+0.095\left(x-1940\right)\left(x-1950\right)+\frac1{240}\left(x-1940\right)\left(x-1950\right)\left(x-1960\right).$

En el siguiente gràfico se representan: (a) los valores reales del censo (puntos azules), (b) el polinomio de grado 2 (rojo), (c) el polinomio de grado 3 (amarillo):

[![Cens_interpolacio](/taller-matematicas/assets/images/Cens_interpolacio.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/01/Cens_interpolacio.png)
Observad que el polinomio de grado 2 coincide exactamente con 3 valores reales, los de 1950-60-70, mientras que el de grado 3 lo hace con cuatro valores, 1940-50-60-70. En el caso de 1930 prácticamente coincide, pero no exactamente, necesitaríamos el polinomio de grado 4 para ello, y para tener coincidencia exacta en todos los puntos hay que obtener el de grado 5. Esta es la regla general: con n+1 puntos podemos formar un polinomio de grado n que coincidirá con todos los valores dados. Los cálculos pueden automatizarse fácilmente en una hoja de cálculo.

**Ejemplo 3**: Obtener el polinomio interpolador de grado 5 de los datos del censo, y dar un valor aproximado de la población en el año 1965.

La tabla completa, obtenida con hoja de cálculo, es:

     

| **x** 
| ** orden 0** 
| **orden 1** 
| **orden 2** 
| **orden 3** 
| **orden 4** 
| **orden 5** 

| 1920 
| 36 
|  
|  
|  
|  
|  

| 1930 
| 40 
| 0.4 
|  
|  
|  
|  

| 1940 
| 48 
| 0.8 
| 0.02 
|  
|  
|  

| 1950 
| 49 
| 0.1 
| -0.035 
| -1.83E-003 
|  
|  

| 1960 
| 69 
| 2 
| 0.095 
| 4.33E-003 
| 1.54E-004 
|  

| 1970 
| 133 
| 6.4 
| 0.22 
| 4.17E-003 
| -4.16E-006 
| -3.16E-006 

En la misma hoja de cálculo disponemos los valores anteriores y formamos una tabla de valores $(x,y)$:
 

| **x** 
| **P(x)** 

| 1920 
| 36.0 

| 1930 
| 40.0 

| 1940 
| 48.0 

| 1950 
| 49.0 

| 1960 
| 69.0 

| **1965** 
| **95.0** 

| 1970 
| 133.0 

Observad que todos los valores del polinomio de grado 5 son coincidentes con los de la tabla, hemos incluido el valor interpolado del año 1965.
## Limitaciones y mejoras del polinomio interpolador de Newton. Splines.

Cuando el número de puntos a interpolar es grande, caso frecuente en las aplicaciones prácticas, los polinomios serán también de un grado elevado. Aunque el teorema de Weierstrass nos  asegura que podemos aproximar por un polinomio cualquier número n de puntos dados, en la práctica debido a los errores de redondeo y de precisión de los ordenadores esto no es así, de hecho este error aumenta progresivamente con n. Se han propuesto diversas soluciones:

**Polinomios interpolantes con distribución de puntos variable**: la distancia entre los puntos a interpolar se reduce en los extremos de la distribución. Por ejemplo, para interpolar 100 puntos en el intervalo $[-10,10]$ podemos tomar la distribución de puntos de Chebyshev:

$x_k=10\cos\left(\frac{\mathrm{πk}}n\right)=\left\{10\cos\left(0\right),10\cos\left(\frac\pi n\right),\dots10\cos\left(\mathrm\pi\right)\right\}$


**Interpolación polinómica por intervalos**
Otra solución consiste en evitar el uso de polinomios de grado elevado, interpolando por trozos (subintervalos). Por ejemplo, si tenemos 100 puntos a interpolar, podemos tomarlos de tres en tres, y para cada subconjunto generamos un polinomio de grado 2 que pase por esos puntos. El problema que se presenta entonces está en los puntos de unión de cada subintervalo; si por ejemplo lo aplicamos al problema del censo obtenemos tres polinomios con los intervalos de tiempo 1920-30-40, 1940-50-60 y 1960-70 (éste último con sólo dos puntos es una recta); en los puntos de unión de cada polinomio pueden haber cambios bruscos de dirección que implican la no-derivabilidad en esos puntos:


Siendo la derivabilidad una condición deseable, este procedimiento puede resultar no aconsejable. Para solucionarlo, se pueden emplear la denominada [interpolación por splines](http://es.wikipedia.org/wiki/Spline), un tipo de interpolación polinómica a trozos que asegura la derivabilidad, y es muy empleada en diseño industrial para aproximar matemáticamente formas diversas.
{% endraw %}