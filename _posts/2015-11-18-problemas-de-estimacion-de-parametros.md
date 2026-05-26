---
layout: post
title: "Problemas de estimación de parámetros"
date: 2015-11-18 11:15:38 +0000
math: true
---
{% raw %}

**1.** Se da a un grupo de 9 personas un curso de Estadística, realizando a cada persona un test de conocimientos antes y después del curso, para ver si se ha obtenido mejora; los resultados obtenidos fueron:
 

| Antes 
| 7 
| 6 
| 5 
| 3 
| 6 
| 2 
| 6 
| 5 
| 7 

| Después 
| 8 
| 6 
| 4 
| 6 
| 7 
| 6 
| 5 
| 6 
| 7 

 Suponiendo que los resultados del test siguen una distribución normal de igual media antes y después del curso, calcular la probabilidad de que, repitiendo el curso y el test con otro grupo de 9 alumnos distintos, se obtenga una diferencia de medias muestrales mayor que la anterior (o sea que se obtenga una mejora superior en el segundo grupo que en el primero), suponiendo que la cuasi-varianza muestral sea la misma en los dos grupos.

**Solución**: Como el test antes y después del curso se hace con las mismas personas, las muestras no son independientes, son pareadas. En este caso se trabaja con una nueva variable D: la diferencia de los valores antes y después del curso. La muestra de D está formada por la diferencia de valores *puntos del test después del curso - puntos del test antes del curso*, y es:

 

| D: 
| 1 
| 0 
| -1 
| 3 
| 1 
| 4 
| -1 
| 1 
| 0 

En las condiciones del enunciado, población normal de igual media antes y después del curso, tenemos que el siguiente estadístico T tiene una distribución de probabilidad t-Student con n-1 = 8 grados de libertad:

$T=\frac{\overline D}{s_d/\sqrt n}\sim t_{n-1}$

donde $s_d$ es la cuasi-varianza:

$s_d=\sqrt{\frac1{n-1}\sum_{i=1}^n\left(D_i-\overline D\right)^2}$

La media de los valores D resulta ser $\overline D=8/9$; sustituyendo valores en las diferencias  $(D-\overline D)^2$ resulta:
 

| D 
| 1 
| 0 
| -1 
| 3 
| 1 
| 4 
| -1 
| 1 
| 0 

| $(D-\overline D)^2$ 
| 0,0123 
| 0,7901 
| 3,5679 
| 4,4568 
| 0,0123 
| 9,6790 
| 3,5679 
| 0,0123 
| 0,7901 

Sumando, dividiendo por n - 1 = 8 obtenenos la cuasi-varianza, 2.8611, y haciendo la raíz cuadrada, obtenemos $s_d=1,6915$.

Calculamos el valor del estadístico T para la muestra 1:

$T_1=\frac{\overline D_1}{s_d/\sqrt n}=\frac{8/9}{1,6915/\sqrt9}\approx1,58$

Ahora podemos contestar la pregunta que nos formularon:   probabilidad de que la media de medias muestrales sea mayor en el segundo grupo que en el primero se expresa como $P(\overline{D_2}&gt;\overline{D_1})$, usamos el hecho de que T sigue una distribución de Student:

$P(\overline{D_2}&gt;\overline{D_1})=P\left(\frac{\overline{D_2}}{s_d/\sqrt n}&gt;\frac{\overline{D_1}}{s_d/\sqrt n}\right)=P(T_2&gt;T_1)=P(T_2&gt;1,58)$

Como $T_2$ también sigue una distribución t de 8 grados de libertad, esta última probabilidad la podemos buscar en las tablas: resulta valer **0.08**. Esta es la respuesta.

[![separador](/taller-matematicas/assets/images/separador.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador.png)**2.** Usando el método de máxima verosimilitud, estimar el parámetro p de una distribución binomial de N=10 a partir de una muestra de n=7 repeticiones, con valores {7, 6, 2, 5, 6, 3, 7}.
**Solución**: La interpretación del enunciado es la siguiente: tenemos una variable X que sigue una distribución de probabilidad binomial, B(N, p), con N = 10, y X tomando valores en el intervalo [0, 10] (desde 0 éxitos hasta 10 éxitos). En 7 repeticiones de un experimento aleatorio se obtuvieron, de un máximo de 10 éxitos, los valores {7, 6, 2, 5, 6, 3, 7}. ¿Cuál es el valor estimado del parámetro p de la binomial?

La función de verosimilitud es:

$L(x_1,\cdots,x_7,p)=\prod_{i=1}^7f\left(x_i,p\right)=\prod_{i=1}^7\begin{pmatrix}10\\x_i\end{pmatrix}p^{x_i}\left(1-p\right)^{10-x_i}$

donde $f(x,p)$ es la función de probabilidad; para hallar la estimación de p por el método de máxima verosimilitud, planteamos la ecuación de verosimilitud:

$\frac{\partial\log\left(L(x_1,\cdots,x_n,p)\right)}{\partial p}=0$

que en nuestro caso es:

$\begin{array}{l}\frac\partial{\partial p}\log\left(\prod_{i=1}^7f\left(x_i,p\right)\right)=\frac\partial{\partial p}\sum_{i=1}^7\log\left(f\left(x_i,p\right)\right)=\sum_{i=1}^7\frac\partial{\partial p}\log\left(\begin{pmatrix}10\\x_i\end{pmatrix}p^{x_i}\left(1-p\right)^{10-x_i}\right)\\=\sum_{i=1}^7\frac\partial{\partial p}\left$\log\left(\begin{pmatrix}10\\x_i\end{pmatrix}\right)+x_i\log\left(p\right)+\left(10-x_i\right)\log\left(1-p\right)\right$\end{array}$

derivando respecto a p cada término de la suma:

$\frac\partial{\partial p}\left$log\left(\begin{pmatrix}10\\x_i\end{pmatrix}\right)+x_ilog\left(p\right)+\left(10-x_i\right)log\left(1-p\right)\right$=\frac{x_i}p-\frac{10-x_i}{1-p}$

sumando todos los términos e igualando a cero:

$\begin{array}{l}\sum_{i=1}^7\left(\frac{x_i}p-\frac{10-x_i}{1-p}\right)=\frac{\sum_{i=1}^7x_i}p-\frac{\sum_{i=1}^710-\sum_{i=1}^7x_i}{1-p}=0\Leftrightarrow\\\left(1-p\right)\sum_{i=1}^7x_i-7\cdot10p+p\sum_{i=1}^7x_i=0\Leftrightarrow\sum_{i=1}^7x_i-7\cdot10p=0\Leftrightarrow\\p=\frac{\sum_{i=1}^7x_i}{7\cdot10}=\frac{\overline x}{10}\\\end{array}$

En general, para n muestras de una binomial B(N,p), llamando $$ a la estimación del parámetro p, tendremos:

$\widehat p=\frac{\sum_{i=1}^nx_i}{n\cdot N}=\frac{\overline x}N.$

Así pues, la estimación de p será:

$\frac1{10}\frac{7+6+2+5+6+3+7}7=\frac{18}{35}\approx0.5143.$

[![separador](/taller-matematicas/assets/images/separador.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador.png)**3.** Usando el método de máxima verosimilitud, estimar el parámetro p de una distribución discreta de probabilidad con la siguiente función de probabilidad:

| **x:** 
| 1 
| 2 
| 3 
| 4 

| **P(X=x):** 
| $p^3$ 
| $3p^2q$ 
| $3pq^2$ 
| $q^3$ 

de la cual tenemos una muestra de tamaño n = 10 con los siguientes valores: {1,1,1,2,2,2,3,3,4,4}.

**Solución**:

La función de verosimilitud es $L(x_1,\cdots,x_{10},p,q)=\prod_{i=1}^{10}f\left(x_i,p\right)$, donde $f(x,p)$ es la función de probabilidad que nos dan en el enunciado:

$L(x,p,q)=\prod_{i=1}^{10}f\left(x_i,p,q\right)=\left(p^3p^3p^3\right)\cdot\left(3p^2q\cdot3p^2q\cdot3p^2q\right)\cdot\left(3pq^2\cdot3pq^2\right)\cdot\left(q^3q^3\right)=3^5p^{17}q^{13}$

Hemos
 puesto entre paréntesis los valores correspondientes a las $x_i$ repetidas, por ejemplo hay tres valores $x=1$. Antes de seguir, hay que tener en cuenta la normalización de la función de probabilidad que nos dan: la suma de probabilidades  ha de ser uno: $p^3+3p^2q+3pq^2+q^3=1\Leftrightarrow\left(p+q\right)^3=1\Leftrightarrow p+q=1.$

La función de verosimilitud se reduce a $L(x,p)=3^5p^{17}\left(1-p\right)^{13}$. Planteamos ahora la ecuación de verosimilitud:

$\begin{array}{l}\frac\partial{\partial p}\log\left(3^5p^{17}\left(1-p\right)^{13}\right)=0\Leftrightarrow\\\frac\partial{\partial p}\left$5\log\left(3\right)+17\log\left(p\right)+13\log\left(1-p\right)\right$=0\end{array}$

Derivando:

$\frac{17}p-\frac{13}{1-p}=0\Leftrightarrow\boxed{\widehat p=\frac{17}{30}}$

Observar que en el paso final hemos sustituido el parámetro p por su estimador $\widehat p$, pues realmente el parámetro p es desconocido, los que hacemos es realizar una estimación.
{% endraw %}