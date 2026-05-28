---
layout: post
title: "Diferenciación e integración numérica"
date: 2015-06-12 17:25:20 +0000
math: true
---
{% raw %}

## Introducción

En las aplicaciones prácticas, a menudo sucede que tenemos valores de la variación de una función en algunos puntos sin tener su expresión analítica, y queremos inferir de ellos la función derivada en algún otro punto. De la misma forma, podemos necesitar la integral definida de esa función de la que sólo sabemos sus valores en algunos puntos; en el caso de la integral además, puede darse el caso de que, incluso teniendo la expresión analítica de la función a integrar, y siendo la función integrable, no exista la función primitiva. En estos casos la solución pasa por aproximar la derivada y la integral usando los métodos del cálculo numérico.

**Ejemplo 1**: Por experiencia previa sabemos que la velocidad media de transmisión de datos $V(t)$ de una línea de comunicaciones digitales es, en función de la hora, la siguiente:

| 
Hora:

 
| 10:00 
| 12:00 
| 14:00 
| 16:00 
| 18:00 
| 20:00 

| 
Velocidad (Mbits/s):

 
| 80 
| 70 
| 68 
| 69 
| 72 
| 80 

Nos interesa conocer (a) el valor de la función derivada $V'(t)$ para el tiempo t=15:00, (b) el valor de la integral definida de la función  $V(t)$ en el intervalo de tiempo $[10:00, 20:00].$ La derivada $V'(t)$ puede usarse para estudiar el porqué de las variaciones de la velocidad de transmisión durante el día, y la integral está relacionada con el tráfico total de datos a lo largo del día.

## Derivación aproximada por interpolación

 Si tenemos una función continua y derivable en un intervalo $[a,b]$ de la cual tenemos sus valores en n+1 puntos diferentes $x_0, x_1, \cdots, x_n$, y queremos saber el valor de su derivada en algún punto x del intervalo, una forma posible de hacerlo es:

	- calcular el polinomio interpolador que aproxima a la función en los puntos dados

	- derivar el polinomio y evaluar la derivada en x

Los detalles del cálculo del polinomio interpolador pueden verse en el post [Interpolación polinómica](http://tallermatematic.eu/wp/?p=822).

**Ejemplo 2**: evaluar un valor aproximado para la función derivada $V'(t)$ en el tiempo t=15:00 de la función del ejemplo 1. Formamos la tabla de interpolación:

| **x** 
| **f(x)** 
| **Dif 1** 
| **Dif 2** 
| **Dif 3** 
| **Dif 4** 
| **Dif 5** 

| 10 
| **80** 
|  
|  
|  
|  
|  

| 12 
| 70 
| **-5** 
|  
|  
|  
|  

| 14 
| 68 
| -1 
| **-1** 
|  
|  
|  

| 16 
| 69 
| 0.5 
| -0.375 
| **0.1041666667** 
|  
|  

| 18 
| 72 
| 1.5 
| -0.25 
| 0.0208333333 
| **-0.0104166667** 
|  

| 20 
| 80 
| 4 
| -0.625 
| -0.0625 
| -0.0104166667 
| 0 

El polinomio interpolador es:

$\begin{array}{l}80-5(x-10)-1(x-10)(x-12)+0.1041666667(x-10)(x-12)(x-14)+(x-10)(x-12)(x-14)(x-16)\times(-0.0104166667)\\=-0.0104167x^4+0.645833x^3-15.2083x^2+150.417x-445\end{array}$ y la derivada es $-0.0416667x^3+1.9375x^2-30.4167x+150.417,$

sustituyendo el valor $x=15$ obtenemos $f'(15)=-10.5$.

| 

![Polinomio interpolador](/taller-matematicas/assets/images/polinomi_interpolant_derivació_num1.png) Polinomio interpolador 
| 

![Derivada del polinomio](/taller-matematicas/assets/images/derivada_interpolada1.png) Derivada del polinomio 

**Ejemplo 3**: De una función de la que desconocemos su expresión analítica sabemos su valor en tres puntos, son: $\left(0,1\right),\;\left(\frac{2\mathrm\pi}6,0.5\right),\;\left(\frac{\mathrm\pi}2,0\right).$ Evaluar el valor de la derivada de la función en el punto $x=\frac{\mathrm\pi}4.$

Formamos la tabla de interpolación:

 

| **x** 
| **f(x)** 
| **$f\left$x_{i-1},x_i\right$$** 
| **$f\left$x_{i-2},x_{i-1},x_i\right$$** 

| 0 
| 1 
|  
|  

| $\frac{2\mathrm\pi}6$ 
| 0.5 
| -0.477 
|  

| $\frac{\mathrm\pi}2$ 
| 0 
| -0.955 
| -0.304 

El polinomio interpolador es:

$P(x)=1-0.477\left(x-0\right)-0.304\left(x-0\right)\left(x-\frac{2\mathrm\pi}6\right)=-0.304x^2-0.159x+1,$

derivando y sustituyendo el valor pedido: $P'(x)=-0.608x-0.159;\;P'(\frac{\mathrm\pi}4)=-0.608\frac{\mathrm\pi}4-0.159=-0.637;$, por tanto el valor aproximado es $f'(\frac{\mathrm\pi}4)\approx-0.637;$. Los valores del enunciado realmente corresponden a la función $y=cos(x)$, con derivada $y'=-sin(x)$, y el valor exacto es $-sin(\frac{\mathrm\pi}4)=-0.707$, la precisión obtenida no es muy alta debido a que sólo hemos usado tres puntos de interpolación.
## Integración aproximada por interpolación

Dada una función [integrable Riemann](http://tallermatematic.eu/wp/?p=674) $f(x)$ de la cual no podemos obtener su función primitiva $F\left(x\right)=\int f\left(x\right)$, pero sí sabemos sus valores en un conjunto de puntos interior al intervalo $(a,b)$, entonces podemos calcular la integral definida $F\left(x\right)=\int_a^bf\left(x\right)$ con el siguiente método aproximado: consideramos una partición del intervalo $(a,b)$ según $n+1$ puntos equidistantes $x_0=a, x_1, ..., x_{n-1}, x_n=b$;  podemos aproximar la función $f(x)$ en cada subintervalo $(x_{i-1},x_i)$ por su polinomio interpolador de grado 1, o sea una recta. El área comprendida entre la gráfica de la función y el eje X podrá aproximarse sumando las áreas de los trapecios formados por los puntos $x_{i-1},x_i, f(x_{i-1}),f(x_i)$, como muestra la figura:

![integración por interpolación de grado 1: trapecios](/taller-matematicas/assets/images/formula_Trapeci.png) integración por interpolación
 de grado 1: trapecios. Se muestra la gráfica de f(x) y los segmentos rectos que aproximan a la función en cada intervalo, así como uno de los trapecios: entre los puntos segundo y tercero.

El área del trapecio formado por esos puntos es:

$A_{i-1,i}=f\left(x_{i-1}\right)\cdot\triangle x+\frac12\left|f\left(x_{i-1}\right)-f\left(x_i\right)\right|\cdot\triangle x=\frac12\left|f\left(x_{i-1}\right)+f\left(x_i\right)\right|\cdot\triangle x=\frac12\left(f\left(x_{i-1}\right)+f\left(x_i\right)\right)\cdot\triangle x$

donde hemos denominado $\triangle x$ a la longitud de los subintervalos. Sumando todos los n trapecios obtenemos la denominada fórmula del trapecio para la integral:

$\begin{array}{l}\int_a^bf\left(x\right)\operatorname dx\approx\sum\nolimits_1^nA_{i-1,i}=\sum\nolimits_1^n\frac12\left(f\left(x_{i-1}\right)+f\left(x_i\right)\right)\cdot\triangle x=\\\frac{\triangle x}2\left(f\left(x_0\right)+2f\left(x_1\right)+2f\left(x_2\right)+\dots+2f\left(x_{n-1}\right)+f\left(x_n\right)\right)\end{array}$

**Ejemplo 4**: Para la función $f(x)=x^3-x^2+1$ aproximamos su integral definida I en el intervalo [0, 1] con n = 4 subintervalos, obtenemos:

valores de f(x) en los puntos de interpolación:

| x 
| 0 
| 0,25 
| 0,5 
| 0,75 
| 1 

| y 
| 1 
| 0,953125 
| 0,875 
| 0,859375 
| 1 

anchura de cada subintervalo: (1 - 0)/4 = 0.25; aplicamos la fórmula del trapecio:

$\int_0^1f\left(x\right)\operatorname dx\approx\frac{0.25}2\left(1+2\cdot0.953+2\cdot0.875+2\cdot0.859+1\right)=0.922$

Si calculamos el valor exacto, usando la función primitiva, hallamos el valor $0.91\overset\frown6.$
### Fórmula de Simpson

Con el mismo procedimiento de dividir el intervalo de integración en n subintervalos, pero usando polinomios interpoladores de grado 2 en cada subintervalo, obtenemos la denominada fórmula de Simpson, omitimos los detalles del cálculo:

$\int_a^bf\left(x\right)\operatorname dx\approx\frac{\triangle X}3\left(f\left(x_0\right)+4f\left(\frac{x_0+x_1}2\right)+2f\left(x_1\right)+4f\left(\frac{x_1+x_2}2\right)+2f\left(x_2\right)+\dots+2f\left(x_{n-1}\right)+4f\left(\frac{x_{n-1}+x_n}2\right)+f\left(x_n\right)\right).$

En cada subintervalo se usan tres puntos: los extremos y el punto medio, para n subintervalos tenemos un total de 2n+1 puntos. Lógicamente esperamos que la fórmula de Simpson sea más precisa que la de los trapecios.

**Ejemplo 5**: Obtener $\int_0^1\ln\left(\cos^2\left(x\right)\right)\operatorname dx$ por el método de Simpson, con n=4.

Calculamos los valores de la función que aparecen en la fórmula de Simpson:
   

| **x** 
| 0 
| 0,125 
| 0,25 
| 0,375 
| 0,5 
| 0,625 
| 0,75 
| 0,875 
| 1 

| **y** 
| 0 
| -0,0156658605 
| -0,0631621025 
| -0,1440500235 
| -0,2611684809 
| -0,4190654025 
| -0,6247997958 
| -0,8894614471 
| -1,2312529408 

Sustituimos los valores en la fórmula:

$\int_0^1\ln\left(\cos^2\left(x\right)\right)\operatorname dx\approx\frac{0.25}6\left$0+4\cdot\left(-0,01567\right)+2\cdot\left(-0,0632\right)+\dots+\left(-1,2313\right)\right$=-0,3751.$
{% endraw %}