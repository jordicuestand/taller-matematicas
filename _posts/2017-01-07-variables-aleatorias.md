---
layout: post
title: "Variables aleatorias"
date: 2017-01-07 10:48:12 +0000
categories:
  - "Estadística"
  - "Matemáticas"
  - "Probabilidades"
tags:
  - "distribución de probabilidad"
  - "función de densidad de probabilidad"
  - "probabilidad"
  - "variable aleatoria"
math: true
---
{% raw %}

- Concepto de variable aleatoria

 	- Variable aleatoria discreta: funciones de probabilidad y distribución

 	- Variable aleatoria continua: funciones de densidad y distribución

 	- Esperanza matemática

 	- Varianza

 	- Desigualdad de Txebixef

 	- Variable aleatoria bidimensional

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Concepto de variable aleatoria

Es la generalización de las variables estadísticas que se han visto en el tema [Estadística descriptiva, análisis de datos](http://tallermatematic.eu/wp/?p=1341) ; la definición era:
****Variable estadística**: una característica numérica de la población que nos interesa estudiar
Pues bien, una **variable aleatoria** (v.a.) es:

 	- O bien una variable estadística

 	- O bien una función de una variable estadística

**Ejemplo 1** :
1. El resultado de lanzar un dado es una v.a.: X = {1, 2, 3, 4, 5, 6}
2. La (función) suma de puntos de dos dados: S = X1 + X2 = {2, 3, 4, ..., 12}
3. La temperatura del aula en días sucesivos: T = {17, 17.3, ...}
4. El consumo de energía E en calefacción en el aula en función de la temperatura T,  $E(T) = Ke^{T-C}$, donde C es una constante. Siendo la temperatura T una variable aleatoria, la función E(T) también lo será.

**Variables aleatorias discretas y continuas**
Si la variable estadística es discreta (toma valores enteros) entonces la variable aleatoria también lo será (como en los ejemplos 1 y 2). Si la variable estadística es continua (toma valores reales) entonces la variable aleatoria también lo será (como en los ejemplos 3 y 4).

**Notación para las variables aleatorias**
Usaremos letras mayúsculas para las variables aleatorias, tales como X, Y, T, ..., y letras minúsculas para valores concretos de la variable: x = 17.3.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Variable aleatoria discreta: funciones de probabilidad y distribución

Cada valor que toma la variable aleatoria es: o bien un punto muestral (ver: [introducción a las probabilidades](http://tallermatematic.eu/wp/?p=1389)) o bien una función de un punto muestral. Como cada punto muestral tiene asociada una probabilidad, también la tendrá la variable aleatoria. Cuando la v.a. es discreta (todos sus valores son enteros), llamamos **función de probabilidad** a la asignación de probabilidades para cada valor posible:

| 
**Valores de la v.a. X**

 
| 
**Probabilidad**

 

| 
X = x1

 
| 
p1 = P(X = x1)

 

| 
...

 
| 
...

 

| 
X = xn

 
| 
pn = P(X = xn)

 

En general tendremos $P (X = x_i) = p_i$. Por las propiedades de la probabilidad es inmediato que $P (X = x_i) &gt; 0$ para todos los puntos $x_i$. La suma de valores de la función de probabilidad valdrá 1: $\sum_iP(X=x_i)=1.$

La función de probabilidad podemos verla como la generalización de la frecuencia relativa (ver [Estadística descriptiva](http://tallermatematic.eu/wp/?p=1341), análisis de datos). Definimos la **función de distribución** para v.a. discreta, F(x), como la probabilidad de que la v.a. X tome valores más pequeños o iguales al valor $x_k$:

$F (x_k) = P (X &lt;= x_k)$

La relación con la función de probabilidad es inmediata:
$F\left(x_k\right)=\sum_{1\leq i\leq k}P\left(X\leq x_i\right)=P\left(X\leq x_k\right)$

La función de probabilidad viene a ser la generalización de la frecuencia relativa acumulada (ver [Estadística descriptiva](http://tallermatematic.eu/wp/?p=1341), análisis de datos).

**Ejemplo 2**: Lanzamos un dado dos veces y definimos la variable aleatoria X restando a los puntos obtenidos en el primer lanzamiento los obtenidos en el segundo lanzamiento. Los valores posibles que puede tomar X son {0, 1, 2, 3, 4, 5, -1, -2, -3, -4, -5}. Para calcular la probabilidad de obtener cada uno de esos valores enumeramos los casos posibles para cada uno de ellos; la probabilidad, por la regla de Laplace, será P(caso) = casos posibles / casos totales, teniendo en cuenta que el número de casos totales es 6·6 = 36 combinaciones de puntuaciones, y que los sucesos son excluyentes (si sucede un caso no puede suceder ningún otro). Por ejemplo, para X = 4 tenemos dos casos: (6, 2) y (5, 1), cada uno de ellos tiene probabilidad 1/36, la probabilidad de que suceda uno o el otro, siendo excluyentes, es la suma 1/36 + 1/36. Procediendo de esta forma obtenemos la función de probabilidad de la v.a. X:

  

| x** 
| **puntuaciones** 
| **cuenta** 
| **probabilidad: f(x)** 

| 0 
| 1-1, 2-2, 3-3, 4-4, 5-5, 6-6 
| 6 
| 6/36 

| 1 
| 6-5, 5-4, 4-3, 3-2, 2-1 
| 5 
| 5/36 

| 2 
| 6-4, 5-3, 4-2, 3-1 
| 4 
| 4/36 

| 3 
| 6-3, 5-2, 4-1 
| 3 
| 3/36 

| 4 
| 6-2, 5-1 
| 2 
| 2/36 

| 5 
| 6-1 
| 1 
| 1/36 

Para los valores que faltan en la tabla, {-1, -2, -3, -4, -5}, las probabilidades son las mismas que para {1, 2, 3, 4, 5}. Así pues la función de probabilidad viene dada por la tabla:

| **x** 
| 0 
| 1 
| 2 
| 3 
| 4 
| 5 
| -1 
| -2 
| -3 
| -4 
| -5 

| **f(x)** 
| 6/36 
| 5/36 
| 4/36 
| 3/36 
| 2/36 
| 1/36 
| 5/36 
| 4/36 
| 3/36 
| 2/36 
| 1/36 

Como comprobación, siempre tenemos que obtener la suma de todos los valores f(x), que ha de valer 1 (una de las propiedades de las probabilidades: si el espacio muestral Ω se puede considerar dividido en n subconjuntos disjuntos entre sí, Ω = A1 ∪ A2 ∪ … ∪ An, entonces P(A1) + P(A2) + … + P(An) = 1 (ver Introducción a las probabilidades, tercera definición de probabilidad). En efecto: 6/36 + 5/36 + 4/36 + 3/36 + 3/36 + 1/36 + 5/36 + 4/36 + 3/36 + 3/36 + 1/36 = 36/36 = 1.

Para obtener la función de distribución de X basta con calcular la tabla de probabilidades acumuladas:
             

| 
**x**

 
| 
0

 
| 
1

 
| 
2

 
| 
3

 
| 
4

 
| 
5

 
| 
-1

 
| 
-2

 
| 
-3

 
| 
-4

 
| 
-5

 

| 
**f(x)**

 
| 
6/36

 
| 
5/36

 
| 
4/36

 
| 
3/36

 
| 
2/36

 
| 
1/36

 
| 
5/36

 
| 
4/36

 
| 
3/36

 
| 
2/36

 
| 
1/36

 

| 
**F(x)**

 
| 
6/36

 
| 
11/36

 
| 
15/36

 
| 
18/36

 
| 
20/36

 
| 
21/36

 
| 
26/36

 
| 
30/36

 
| 
33/36

 
| 
35/36

 
| 
36/36

 

La gráfica de la función de probabilidad es:


La función de distribución suele representarse como una función escalonada:


**Propiedades inmediatas de las funciones de distribución discretas F (x)**

 	- El valor de F(x) está en el intervalo [0, 1]

 	- F(x) es no decreciente

 	- La probabilidad $P(X &gt; x_k)$ és igual a $1 – F(x_k)$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Variable aleatoria continua: funciones de densidad y distribución

Cuando la variable es continua sabemos que se trabaja con intervalos de la variable (ver [Estadística Descriptiva](http://tallermatematic.eu/wp/?p=1341) => Agrupación de datos en intervalos). La asignación de probabilidades se hará por tanto para cada intervalo que definamos. 

En el tema [Estadística Descriptiva](http://tallermatematic.eu/wp/?p=1341) la anchura de cada intervalo la definíamos arbitrariamente según el número de intervalos y el recorrido de la variable. Ahora hay que generalizar para intervalos de cualquier anchura: supongamos que el recorrido de la variable aleatoria es [max, min]; entonces definimos una **función**** de densidad de probabilidad f(x) de la v.a. continua X** como cualquiera que verifica las tres condiciones siguientes:

 	- No negatividad: f(x) >= 0

 	- Probabilidad de un intervalo: $P\left(X\in\left$a,b\right$\right)=\int_a^bf\left(x\right)\operatorname dx$

 	- Normalización: $P\left(X\in\left$max,\;min\right$\right)=\int_{min}^{max}f\left(x\right)\operatorname dx=1$

Se deducen las siguientes propiedades:

 	- La probabilidad en las variables continuas se calcula con una integral sobre un intervalo (2ª propiedad de las funciones de densidad)

 	- La probabilidad de un punto siempre es cero: P (X = x) = P (x <= X <= x) = 0 pues coinciden los límites de la integral (es un intervalo de longitud nula)

 	- En cambio f (x) no tiene porque ser cero en ningún punto

 	- La gráfica de la función de densidad es la generalización del histograma de frecuencias relativas ([Estadística Descriptiva](http://tallermatematic.eu/wp/?p=1341)).

Definimos la **función**** de distribución para v.a. continuas,** F (x), como la probabilidad de que X tome valores más pequeños que a x: F (x) = P (X < x_k).  La relación con la función de densidad es inmediata: si el valor mínimo de la v.a. X es min, entonces tendremos que:

$F\left(x_0\right)=P\left(X\in\left$min,\;x_0\right$\right)=\int_{min}^{x_0}f\left(x\right)\operatorname dx$

Si la expresión anterior la expresamos para un valor x genérico y la derivamos respecto ese valor x,  aplicando el [primer teorema fundamental del cálculo](https://es.wikipedia.org/wiki/Teorema_fundamental_del_c%C3%A1lculo#Primer_teorema_fundamental_del_c.C3.A1lculo) obtenemos otra relación importante entre las funciones de densidad y de distribución continuas:

$F'\left(x\right)=\frac{\operatorname d{}}{\operatorname dx}\int_{min}^xf\left(t\right)\operatorname dt=f\left(x\right)$

Que se expresa como "*La derivada de la función de distribución es la función de densidad*"

La función de distribución continua tiene ciertas propiedades:

 	- Asíntotas horizontales izquierda y derecha: F (-∞) = 0, F (+∞) = 1

 	- F (x) es continua y no decreciente

 	- La probabilidad de un
intervalo [a, b] es igual a F (b) - F (a)

**Ejemplo 3**: Sea la función de densidad de probabilidad 

$f\left(x\right)=\left\{\begin{array}{l}0\;\;\;\;\;\;\;\;\;\;\;\;\;\text{si }x\not\in\left$0,\;1\right$\\\frac23\left(x+1\right)\;\text{si }x\in\left$0,\;1\right$\end{array}\right.$

Calcular $P(0\leq X\leq0.5)$, $P(-3\leq X\leq0.5)$, $P(0\leq X\leq1)$

Según la propiedad 2 de las funciones de densidad: $P(0\leq X\leq0.5)=\int_0^{0.5}f\left(x\right)\operatorname dx=\int_0^{0.5}\frac23\left(x+1\right)\operatorname dx=\frac23\left$\frac{x^2}2+x\right$_0^{0.5}=\frac23\left(\frac{0.5^2}2+0.5-0\right)=\frac5{12}$.

Para el segundo intervalo hemos de tener en cuenta los intervalos de definición de la función f(x):

$P(-3\leq X\leq0.5)=\int_{-3}^{0.5}f\left(x\right)\operatorname dx=\int_{-3}^00\operatorname dx+\int_0^{0.5}\frac23\left(x+1\right)\operatorname dx=0+\frac5{12}=\frac5{12}$

Para el tercer intervalo tenemos:

$P(-3\leq X\leq0.5)=\int_0^1f\left(x\right)\operatorname dx=\int_0^1\frac23\left(x+1\right)\operatorname dx=\frac23\left$\frac{x^2}2+x\right$_0^1=\frac23\left(\frac12+1-0\right)=1$

un resultado esperado, pues es la condición de normalización de las funciones de densidad.
{% endraw %}