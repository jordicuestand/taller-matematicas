---
layout: post
title: "Problemas resueltos de límites de funciones reales"
date: 2014-08-15 19:14:29 +0000
math: true
---
{% raw %}

**[Apuntes de Matemáticas](http://tallermatematic.eu/math/) -> Funciones reales de variable real**** -> Problemas resueltos de límites de funciones**

---

 

**1.** Calcular $\lim_{x\rightarrow\infty}\frac{x\sin\left(x\right)}{x^2+1}.$

Por las propiedades de los límites, podemos separarlo en producto de límites, por un lado la fracción racional. por el otro la función seno:

$\lim_{x\rightarrow\infty}\frac{x\sin\left(x\right)}{x^2+1}=\lim_{x\rightarrow\infty}\frac x{x^2+1}\cdot\lim_{x\rightarrow\infty}\sin\left(x\right)=L_1\cdot L_{2.}$
El límite de la función racional es inmediato: siendo el grado del denominador mayor que el del numerador será $0$, podemos comprobarlo dividiendo numerado y denominador por $x^2$ (o sea por $x$ elevado al grado del denominador:

$\lim_{x\rightarrow\infty}\frac x{x^2+1}=\lim_{x\rightarrow\infty}\frac{x/x^2}{\left(x^2+1\right)^2/x^2}=\lim_{x\rightarrow\infty}\frac{1/x}{\left(x+1/x\right)^2}=\frac0\infty=0.$

El límite de la función seno no existe, pues los valores de $sen(x)$ oscilan indefinidamente en el intervalo $[0,1]$, en todo caso los valores estan acotados: $-1\leq L_2\leq1\Leftrightarrow\left|L_2\right|\leq1.$ Así pues el producto  de límites cumple: $\left|L_1L_2\right|\leq0\cdot1=0\Rightarrow L=L_1L_2=0.$

Si hubiéramos tenido un límite como $\lim_{x\rightarrow\infty}\frac{x^2\sin\left(x\right)}{x^2+1}$ el resultado seria distinto, pues ahora la fracción racional tiende a 1:

$\lim_{x\rightarrow\infty}\frac{x^2}{\left(x^2+1\right)^2}=\lim_{x\rightarrow\infty}\frac{x^2/x^2}{\left(x^2+1\right)^2/x^2}=\lim_{x\rightarrow\infty}\frac1{\left(1+1/x\right)^2}=\frac11=1.$

Pero ahora el producto del seno por la función racional es oscilante, luego no existe: $1\cdot\lim_{x\rightarrow\infty}\sin\left(x\right)=?.$

---

**2.** Calcular $\lim_{x\rightarrow\infty}\left(\sqrt{x\left(x+1\right)}-x\right).$

Es del tipo indeterminado $\lim_{x\rightarrow\infty}\left(\sqrt{x\left(x+1\right)}-x\right)=\infty-\infty=?$, para simplificarlo, viendo que hay un binomio con una raíz del tipo $\left(\sqrt A-B\right)$ podemos convertirlo a fracción racional aplicando $\left(\sqrt A-B\right)=\frac{\left(\sqrt A-B\right)\left(\sqrt A+B\right)}{\left(\sqrt A+B\right)}=\frac{A-B^2}{\left(\sqrt A+B\right)}:$

$\lim_{x\rightarrow\infty}\left(\sqrt{x\left(x+1\right)}-x\right)=\lim_{x\rightarrow\infty}\frac{x\left(x+1\right)-x^2}{\sqrt{x\left(x+1\right)}+x}=\lim_{x\rightarrow\infty}\frac x{\sqrt{x\left(x+1\right)}+x}.$

En esta fracción racional el grado del numerador y del denominador valen ambos 1; dividimos todo pues por $x^1$:

$\lim_{x\rightarrow\infty}\frac x{\sqrt{x\left(x+1\right)}+x}=\lim_{x\rightarrow\infty}\frac{x/x}{\left(\sqrt{x\left(x+1\right)}+x\right)/x}=\lim_{x\rightarrow\infty}\frac1{\left(\sqrt{1+1/x}+1\right)}=\frac1{\sqrt{1+0}+1}=\frac12.$

Puede ser útil dar algunos valores de $x$ y $f(x)$ para ver como efectivamente el límite deducido es correcto:

| **$x$** 
| $\left(\sqrt{x\left(x+1\right)}-x\right)$ 

| 0 
| 0 

| 1 
| 0.4142135624 

| 10 
| 0.4880884817 

| 100 
| 0.4987562112 

| 1000 
| 0.4998750625 

| 10000 
| 0.4999875006 

 

---

 

**3.** Calcular  $\lim_{x\rightarrow\infty}\sqrt[3]{x^2\left(x+1\right)}-x}.$

Es del tipo indeterminado $\\lim_{x\rightarrow\infty}\sqrt[3]{x^2\left(x+1\right)}-x}=\infty-\infty=?$, para simplificarlo, vemos que es un binomio del tipo $\sqrt[3]A-B$. Para convertirlo en una expresión racional habrá que deducir alguna formula de conversión.

En el caso de raices cuadradas, se usa la propiedad "producto de suma por diferencia igual a diferencia de cuadrados":

$\left(a+b\right)\left(a-b\right)=a^2-b^2\Rightarrow\sqrt a-b=\frac{\left(\sqrt a-b\right)\left(\sqrt a+b\right)}{\left(\sqrt a+b\right)}=\frac{a-b^2}{\left(\sqrt a+b\right)}.$

Para el caso de raíces cúbicas, necesitamos una combinación de $a, b$, esto es, una función $g(a,b)$, para que al multiplicarla por $a-b$ resulte $a^3-b^3$:
$\left(a-b\right)\cdot g\left(a,b\right)=a^3-b^3.$

Como la expresión de la derecha es un polinomio en $a,b$ de grado 3, y a la izquierda el primer miembro es de grado 1, seguro que $g(a,b)$ es un polinomio en $a,b$ de grado 2: $g(a,b)=\alpha_1a^2+\alpha_2b^2+\beta ab+\gamma_1a+\gamma_2b.$ Operando:

$\begin{array}{l}\left(a-b\right)\cdot g(a,b)=\alpha_1a^3+\alpha_2ab^2+\beta a^2b+\gamma_1a^2+\gamma_2ab-\alpha_1a^2b-\alpha_2b^3-\beta ab^2-\gamma_1ab-\gamma_2b^2=\\\alpha_1a^3-\alpha_2b^3+\left(\alpha_2-\beta\right)ab^2+\left(\beta-\alpha_1\right)a^2b+\gamma_1a^2-\gamma_2b^2+\left(\gamma_2-\gamma_1\right)ab.\end{array}$

Igualando a $a^3-b^3$:

$\begin{array}{l}\alpha_1a^3-\alpha_2b^3+\left(\alpha_2-\beta\right)ab^2+\left(\beta-\alpha_1\right)a^2b+\gamma_1a^2-\gamma_2b^2+\left(\gamma_2-\gamma_1\right)ab=a^3-b^3\Rightarrow\\\alpha_1=\alpha_2=1,\\\alpha_2-\beta=\beta-\alpha_1=\gamma_1=\gamma_2=\left(\gamma_2-\gamma_1\right)=0\Rightarrow\\\beta=1.\end{array}$

Nos queda la función $g(a,b)=a^2+b^2+ab$, ahora podemos racionalizar la expresión $\left(\sqrt[3]a-b\right)$:

$\left(\sqrt[3]a-b\right)=\frac{\left(\sqrt[3]a-b\right)\left(\left(\sqrt[3]a\right)^2+\left(b\right)^2+\sqrt[3]ab\right)}{\left(\left(\sqrt[3]a\right)^2+\left(b\right)^2+\sqrt[3]ab\right)}=\frac{\sqrt[3]{a^3}-b^3}{\left(\left(\sqrt[3]a\right)^2+b^2+b\sqrt[3]a\right)}=\frac{a-b^3}{\left(\left(\sqrt[3]a\right)^2+b^2+b\sqrt[3]a\right)}.$

Considerando que $a=x^2\left(x+1\right),\;b=x:$

$\begin{array}{l}\lim_{x\rightarrow\infty}\sqrt[3]{x^2\left(x+1\right)}-x=\lim_{x\rightarrow\infty}\frac{x^2\left(x+1\right)-x^3}{\left(\sqrt[3]{x^2\left(x+1\right)}\right)^2+x^2+\left(x\sqrt[3]{x^2\left(x+1\right)}\right)^{}}=\\\lim_{x\rightarrow\infty}\frac{x^2}{\left(x^3+x^2\right)^{2/3}+x^2+\left(x^6+x^5\right)^{1/3}}.\end{array}$

Tanto el grado del numerador como del denominador son 2, dividimos todo por $x^2$:

$\begin{array}{l}\lim_{x\rightarrow\infty}\frac{x^2/x^2}{\left(x^3+x^2\right)^{2/3}/x^2+x^2/x^2+\left(x^6+x^5\right)^{1/3}/x^2}=\\\lim_{x\rightarrow\infty}\frac1{\left(1+x^{-1}\right)^{2/3}+1+\left(1+x^{-1}\right)^{1/3}}=\\\frac1{1+1+1}=\frac13.\end{array}$

De nuevo, podemos dar algunos valores para comprobar el resultado:

| **$x$** 
| $\sqrt[3]{x^2\left(x+1\right)}-\sqrt[3]{x^2}$ 

| 0 
| 0 

| 1 
| 0.2599210499 

| 10 
| 0.3228011546 

| 100 
| 0.3322283542 

| 1000 
| 0.3332222839 

| 10000 
| 0.3333222228 

 

---

 

**4.** Calcular $\lim_{x\rightarrow\infty}\sqrt[6]{x^4-x^3}-\sqrt[{}]{\left(x+1\right)^4}.$
Es del tipo indeterminado $\infty-\infty=?$, para simplificarlo, el método habitual es convertirlo en fracción racional. Para hacerlo, usamos el siguiente resultado:

Sea la expresión $\sqrt[n]a-\sqrt[n]b$, donde $a$ y $b$ son polinomios en $x$. Entonces el polinomio

$g=a^\frac{n-1}n+b^\frac{n-1}n+a^\frac{n-2}nb^\frac1n+a^\frac{n-3}nb^\frac2n+\dots+a^\frac2nb^\frac{n-3}n+a^\frac1nb^\frac{n-2}n$

verifica que $\left(\sqrt[n]a-\sqrt[n]b\right)g=a-b.$

Es fácil comprobar esta afirmación, realizando el producto  $\left(\sqrt[n]a-\sqrt[n]b\right)g$ y viendo como se cancelan todos los términos excepto $a, b$.

Vamos a usarlo para el cálculo del límite propuesto: llamemos $a=x^4-x^3,\;b=\left(x+1\right)^4$, entonces tendremos:

$\begin{array}{l}\lim_{x\rightarrow\infty}\sqrt[6]{x^4-x^3}-\sqrt[{}]{\left(x+1\right)^4}=\lim_{x\rightarrow\infty}\frac{\left(\sqrt[6]{x^4-x^3}-\sqrt[{}]{\left(x+1\right)^4}\right)\cdot g(x)}{g(x)}=\\\lim_{x\rightarrow\infty}\frac{\left(x^4-x^3\right)-\left(x+1\right)^4}{\left(x^4-x^3\right)^\frac56+\left(x+1\right)^{4\frac56}+\left(x^4-x^3\right)^\frac46\left(x+1\right)^{4\frac16}+\left(x^4-x^3\right)^\frac36\left(x+1\right)^{4\frac26}+\left(x^4-x^3\right)^\frac26\left(x+1\right)^{4\frac36}+\left(x^4-x^3\right)^\frac16\left(x+1\right)^{4\frac46}}=\end{array}$

$\begin{array}{l}\lim_{x\rightarrow\infty}\frac{-5x^3-6x^2-4x-1}{\left(x^4-x^3\right)^\frac56+\left(x+1\right)^\frac{10}3+\left(x^4-x^3\right)^\frac23\left(x+1\right)^\frac23+\left(x^4-x^3\right)^\frac12\left(x+1\right)^\frac43+\left(x^4-x^3\right)^\frac13\left(x+1\right)^2+\left(x^4-x^3\right)^\frac16\left(x+1\right)^\frac83}.\end{array}$

El grado del numerador es 3, mientras que el del denominador es 10/3, por tanto mayor. En este caso el límite en el infinito siempre será cero. Para verlo, basta con dividir numerador y denominador por $x^3$ o bien por $x^{10/3}$; las operaciones con los exponentes fraccionarios del denominador son un poco pesadas, pero no es necesario hacerlas en detalle, basta con ver que habiendo algunos exponentes de grado 10/3 al dividir por $x^3$ quedaran exponentes positivos $x^p$ en el denominador, mientras que en el numerador quedará $-5-6x^{-1}-4x^{-2}-x^{-3}$. Entonces, al hacer el límite $x\rightarrow\infty$, todos los exponentes negativos tienden a cero y los positivos a $\infty$:

$L=\lim_{x\rightarrow\infty}f(x)=\frac{-5+0}{\infty+0}=0.$

Comprobando con la hoja de cálculo vemos que coinciden los valores con el límite 0, si bien la convergéncia es muy lenta (el eje X tiene escala logarítmica).

[![limit_arrel_6](/taller-matematicas/assets/images/limit_arrel_6.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/limit_arrel_6.png)

---

**5.** Calcular $L=\lim_{x\rightarrow\infty}\sqrt[3]{27x^2\left(x-1\right)}-\sqrt{9x^2+1}.$

Es del tipo indeterminado $\infty-\infty=?$ con la dificultad adicional de que los radicandos no tienen el mismo grado, uno es raíz cúbica y el otro es raíz cuadrada y no podemos racionalizarlo directamente. Pero podemos calcular el mcm (mínimo común múltiplo) de los grados: mcm(3, 2) = 6, y convertirlos en raíces del mismo grado:

$\sqrt[3]{27x^2\left(x-1\right)}-\sqrt{9x^2+1}=\sqrt[6]{\left(27x^2\left(x-1\right)\right)^2}-\sqrt[6]{\left(9x^2+1\right)^3}.$

Ahora podemos aplicar el método de racionalización visto en el ejercicio anterior, con $a=\left(27x^2\left(x-1\right)\right)^2,\;b=\left(9x^2+1\right)^3,\;n=6$:

$\begin{array}{l}L=\lim_{x\rightarrow\infty}\sqrt[3]{27x^2\left(x-1\right)}-\sqrt{9x^2+1}=\lim_{x\rightarrow\infty}\frac{\left(\sqrt[6]{\left(27x^2\left(x-1\right)\right)^2}-\sqrt[6]{\left(9x^2+1\right)^3}\right)\cdot g\left(x\right)}{g\left(x\right)}=\\\lim_{x\rightarrow\infty}\frac{\left(27x^2\left(x-1\right)\right)^2-\left(9x^2+1\right)^3}{\left(27x^2\left(x-1\right)\right)^{2\frac56}+\left(9x^2+1\right)^{3\frac56}+\left(27x^2\left(x-1\right)\right)^{2\frac46}\left(9x^2+1\right)^{3\frac16}+\dots+\left(27x^2\left(x-1\right)\right)^{2\frac16}\left(9x^2+1\right)^{3\frac46}}.\end{array}$

Operando en el numerador obtenemos $-1485x^5+O_-\left(x^4\right)$, donde $O_-\left(x^4\right)$ simboliza "términos de orden igual o inferior a $x^4$". En el denominador operamos teniendo en cuenta solo los términos de grado superior, grado cinco en este caso:

$\begin{array}{l}27^\frac{10}6x^{3\frac{10}6}+9^\frac{15}6x^5+27^\frac86x^{3\frac86}9^\frac36x+\dots+27^\frac13x^{3\frac13}9^2x^4+O_-\left(x^4\right)=\\243x^5+243x^5+243x^5+\dots+243x^5+O_-\left(x^4\right)=\\1458x^5+O_-\left(x^4\right).\end{array}$

Nos queda:

$L=\lim_{x\rightarrow\infty}\sqrt[3]{27x^2\left(x-1\right)}-\sqrt{9x^2+1}=\lim_{x\rightarrow\infty}\frac{1458x^5+O_-\left(x^4\right)}{1458x^5+O_-\left(x^4\right)}=1.$

---
{% endraw %}