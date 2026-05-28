---
layout: post
title: "Examen-2 de Cálculo"
date: 2016-10-16 09:02:41 +0000
categories:
  - "Cálculo en R"
  - "Derivación"
  - "Funciones continuas"
  - "Funciones reales de variable real"
  - "Matemáticas"
tags:
  - "Cálculo"
  - "problemas resueltos de cálculo"
math: true
---
{% raw %}

**1**. Calcular $\underset{n\rightarrow\infty}{lim}\frac{\sqrt{n^2+1}-\sqrt{9n^2+2}}{3n-2+\sqrt{4n^2-3}}$

**Solución**: $\underset{n\rightarrow\infty}{lim}\frac{\sqrt{n^2+1}-\sqrt{9n^2+2}}{3n-2+\sqrt{4n^2-3}}=\frac{\sqrt{\infty+1}-\sqrt{\infty+2}}{\infty-2+\sqrt{\infty-3}}=\frac{\infty-\infty}\infty=?$ tenemos dos indeterminaciones, una en el numerador, $\infty-\infty$, otra en la fracción $\frac{\infty}\infty$. Viendo que el grado máximo de n es 1, dividimos numerador y denominador por n, y volvemos a aplicar el límite:

$\begin{array}{l}\underset{n\rightarrow\infty}{lim}\frac{\sqrt{n^2+1}-\sqrt{9n^2+2}}{3n-2+\sqrt{4n^2-3}}\frac{1/n}{1/n}=\underset{n\rightarrow\infty}{lim}\frac{\sqrt{n^2/n^2+1/n^2}-\sqrt{9n^2/n^2+2/n^2}}{3n/n-2/n+\sqrt{4n^2/n^2-3/n^2}}=\\\underset{n\rightarrow\infty}{lim}\frac{\sqrt{1+1/n^2}-\sqrt{9+2/n^2}}{3-2/n+\sqrt{4-3/n^2}}=\frac{\sqrt{1+0}-\sqrt{9+0}}{3-0+\sqrt{4-0}}=\boxed{-\frac25}\end{array}$

Como comprobación calculamos algunos términos con hoja de cálculo, llamando L al límite:

| **n** 
| **f(n)** 
| **|L-f(n)|** 

| 1 
| -0,951206 
| 0,551206 

| 10 
| -0,416974 
| 0,016974 

| 100 
| -0,401609 
| 0,001609 

| 1000 
| -0,400160 
| 0,000160 

| 10000 
| -0,400016 
| 0,000016 

| 100000 
| -0,400002 
| 0,000002 

Vemos que la diferencia entre la expresión y el límite tiende progresivamente a cero.

![separador2](/taller-matematicas/assets/images/separador2.png)

**2**. ¿En qué puntos la gráfica de la función $f(x)=x^3-x^2+2$ tiene su recta tangente paralela al eje X?
**Solución**: La recta tangente a la gráfica de $f(x)$ en un punto $x_0$ de su dominio tiene la ecuación $y=mx+n$ donde la pendiente de la recta es $m=f'(x_0)$; recordemos que la pendiente de la recta es la tangente del ángulo que forma con el eje X: $m=\tan\left(\alpha\right)$. Si esa recta tangente es paralela al eje X, quiere decir que el ángulo $\alpha$ es cero, o sea que $\tan\left(\alpha\right)=\tan\left(0\right)=0$, o sea que $m=0=f'(x_0)$. Por tanto, tenemos que hallar los puntos x para los que la derivada es nula:

$f'(x)=3x^2-2x=0\Rightarrow x\left(3x-2\right)=0\Rightarrow\left\{\begin{array}{l}x=0\\x=2/3\end{array}\right.$

![examen-2](/taller-matematicas/assets/images/examen-2.png)
Sustituyendo estos dos valores de x en f(x) obtenemos sus imágenes, que son y=2, y = 50/27, respectivamente, que son también las ecuaciones de las rectas tangentes, ya que para ellas y=mx + n = 0·x+n = n (rectas y = cte) como vemos en la gráfica.

![separador2](/taller-matematicas/assets/images/separador2.png)**3**.  Estudiar el límite $\underset{\left(x,y\right)\rightarrow\left(0,0\right)}{lim}\frac{x^2+y^3}{x^2+y^2}.$

**Solución**: Es indeterminado del tipo 0/0. Siendo un límite de dos variables, procede el cambio de variables a coordenadas polares:

$\begin{array}{l}\underset{\left(x,y\right)\rightarrow\left(0,0\right)}{lim}\frac{x^2+y^3}{x^2+y^2}=\underset{r\rightarrow0}{lim}\frac{r^2\cos^2\left(\theta\right)+r^3\sin^3\left(\theta\right)}{r^2cos^2\left(\theta\right)+r^2sin^2\left(\theta\right)}=\underset{r\rightarrow0}{lim}\frac{cos^2\left(\theta\right)+sin^3\left(\theta\right)}{cos^2\left(\theta\right)+sin^2\left(\theta\right)}=\\\underset{r\rightarrow0}{lim}\frac{cos^2\left(\theta\right)+sin^3\left(\theta\right)}1\end{array}$

este límite no existe, pues a medida que el radio r se acerca a cero, el numerador no tiende a ningún valor en concreto, depende del ángulo.

![separador2](/taller-matematicas/assets/images/separador2.png)**4**.  ¿Cuáles son los puntos críticos de la función $f(x,y)=x^3y^3+xy$?

**Solución**: Son aquellos en los que se anulan las derivadas parciales; la derivada parcial respecto a x la igualamos a cero:

$\frac{\partial{}}{\partial x}\left(x^3y^3+xy\right)=3x^2y^3+y=0\Rightarrow\left\{\begin{array}{l}\boxed{y=0}\\3x^2y^2+1=0\end{array}\right.$

la segunda opción no tiene solución, pues $x^2y^2$ siempre es positivo. Para la derivada parcial respecto a y tenemos un resultado parecido:

$\frac{\partial{}}{\partial y}\left(x^3y^3+xy\right)=3x^3y^2+x=0\Rightarrow\left\{\begin{array}{l}\boxed{x=0}\\3x^2y^2+1=0\end{array}\right.$

Así pues el único punto crítico es x=0, y=0.

![separador2](/taller-matematicas/assets/images/separador2.png)
{% endraw %}