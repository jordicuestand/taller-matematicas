---
layout: post
title: "Límites de sucesiones de funciones"
date: 2014-07-31 18:34:32 +0000
categories:
  - "Cálculo en R"
  - "Funciones reales de variable real"
  - "Matemáticas"
  - "Sucesiones"
tags:
  - "Convergencia puntual"
  - "Convergencia uniforme"
  - "sucesión funcional"
math: true
---

Recientemente he estado ayudando a un alumno con un problema relativo a la convergencia de una sucesión de funciones; a parte de la técnica de resolución, que puede más o menos aprenderse de memoria, comprobé que mi alumno no había entendido ni el significado ni la utilidad de los conceptos, de forma que, por así decirlo, navegaba entre la niebla. De hecho, recordé que yo mismo en mi época de estudiante tampoco lo entendí. Estoy seguro de que se debe a la forma de explicarlo, demasiado formal. Voy a intentar en este post explicar claramente tres conceptos, que son:

 	- Sucesión de funciones

 	- Convergencia puntual de una sucesión de funciones

 	- Convergencia uniforme de una sucesión de funciones

---

 
# Sucesión de funciones

Una sucesión de funciones, a semejanza de una [sucesión numérica](http://mathseng.blogspot.com.es/2014/06/sucesiones-en-r.html), es una colección infinita de funciones. Por ejemplo:

$\begin{array}{l}f_1(x)=x,\\f_2(x)=x^2,\\f_3(x)=x^3,\\\dots,\\f_n(x)=x^n\end{array}$
Más formalmente, si tenemos una función $F:\mathbb{N}\rightarrow\Omega$, donde $\mathbb{N}$: números naturales,  $\Omega$: conjunto de funciones reales de variable real, tal que a cada número natural n hace corresponder una función real $f_n(x)$, diremos que tenemos definida una sucesión de funciones reales. En el ejemplo anterior:

$\begin{array}{l}1\rightarrow f_1(x)=x,\\2\rightarrow f_2(x)=x^2,\\3\rightarrow f_3(x)=x^3,\\\dots,\\n\rightarrow f_n(x)=x^n\end{array}$

A la función de la sucesión correspondiente al número n, $f_n(x)$ se le llama el **término general de la sucesión**.

**Ejemplo 1**: Escribir los tres primeros términos de la sucesión de funciones de término general $f_n(x)=\frac1{1-nx^2}$.

Son:

$\begin{array}{l}n=1\rightarrow f_1(x)=\frac1{1-x^2},\\n=2\rightarrow f_2(x)=\frac1{1-2x^2},\\n=3\rightarrow f_3(x)=\frac1{1-3x^2}\end{array}$

---

# Convergencia puntual de una sucesión de funciones

En las sucesiones numéricas ya se ha visto el concepto de convergencia: informalmente hablando, es un número x al que progresivamente se va acercando la sucesión, sin alcanzarlo nunca. Extendiendo el concepto a sucesiones de funciones, el límite también ha de ser una función a la que la sucesión de funciones se va acercando, pero, ¿que entendemos por "acercarse a una función"? Con números reales $x, y$ sabemos que si la diferencia $\left|x-y\right|$ es pequeña, entonces los números  $x, y$  estan cerca. ¿Cómo lo hacemos con funciones? Bueno, hay varias formas de hacerlo.

**Definición 1**: Convergencia puntual de una sucesión de funciones.

Sean las funciones $f_n\left(x\right)$ con dominio $D$. Si existe una función $f(x)$ tal que se cumpla, para todo $x\in D$:

$\lim_{n\rightarrow\infty}f_n\left(x\right)=f\left(x\right)$

diremos que $f(x)$ es la función límite de la sucesión $f_n\left(x\right)$ y que esta sucesión converge puntualmente a $f(x)$.

**Ejemplo 2**: La sucesión $f_n(x)=\frac1{1+nx^2}$ tiende a la función

$f(x)=\left\{\begin{array}{l}0\;\text{si }x\neq0\\1\;\text{si }x=0\end{array}\right.$

en efecto:

$\lim_{n\rightarrow\infty}\frac1{1+nx^2}=\left\{\begin{array}{l}\frac1{1+\infty\cdot x^2}=\frac1{\infty}=0\;\text{si }x\neq0\\\frac1{1+n\cdot0}=\frac11=1\;\text{si }x=0\end{array}\right.$

Gráficamente, representamos los términos 1, 2, 3, 50 y 1000 de la sucesión :

[caption id="attachment_118" align="alignnone" width="616"][![fn(x) = 1/(1+nx²)](/assets/images/sucesion-funcional1.jpg)](http://tallermatematic.eu/wp/wp-content/uploads/2014/07/sucesion-funcional1.jpg) fn(x) = 1/(1+nx²)[/caption]

Vemos que,  a medida que avanzamos en la sucesión, la gráfica de $f_n(x)$ se va estrechando; en el límite vale cero en todo punto excepto en $x=0$, donde vale 1.

En este ejemplo vemos que, aun siendo todas las funciones de la sucesión $f_n(x)$ funciones continuas, la función límite $f(x)$ no lo es. Por tanto, la definición que hemos dado de convergencia de series de funciones no conserva la continuidad. En el siguiente apartado encontramos la segunda definición de convergencia que conservará la continuidad.

---

 
# Convergencia uniforme de una sucesión de funciones

Para ver el motivo de por qué la convergencia puntual no conserva la continuidad, y como puede solucionarse, veamos un ejemplo. Sea la sucesión funcional definida por $f_n(x)=\frac{\left|x\right|}{1+nx^2}$. En la imagen hemos representado los términos $n=1, 2, 3, 100$, así como las rectas $y=0.3$, e $y=-0.3$.

[caption id="attachment_120" align="alignnone" width="580"][![fn(x) = |x| / (1 + nx²)](/assets/images/sucesion-funcional2.jpg)](http://tallermatematic.eu/wp/wp-content/uploads/2014/07/sucesion-funcional2.jpg) fn(x) = |x| / (1 + nx²). Los términos a partir del tercero  estan dentro de la franja -0,3 < y < 0,3.[/caption]

La función límite es:

$\lim_{n\rightarrow\infty}f_n(x)=\frac{\left|x\right|}{1+nx^2}=\left\{\begin{array}{l}0\;\text{si }x=0\\\frac{\left|x\right|}{1+\infty}\rightarrow0\;\text{si }x\neq0\end{array}\right.$
Luego $f(x)=0$. En la imagen observamos que, a partir de cierto término (el tercero, $f_3(x)$) todas las funciones quedan dentro de la franja delimitada por las rectas $y=0,3$, e $y=-0,3$, o sea que la distancia entre la gráfica de $f(x)$ y de $f_n(x)$ es menor que $d=0,3$.  Dicho de otro modo,  toda la gráfica de cada función $f_n(x)$ se acerca uniformemente a la función límite $f(x)=0$. Cuando sucede esto, queda asegurada la continuidad de la función límite, como en este caso sucede. Tenemos pues una nueva definición de convergencia:

**Definición 2:** Convergencia uniforme de una sucesión de funciones.

$f_n(x)$ tiende uniformemente a $f(x)$ si converge puntualmente a $f(x)$ y además, dada una distancia $d$ cualquiera, la separación entre la función límite y todas las funciones de la sucesión a partir de una de ellas es menor que $d$.

**Ejemplo 3**:  la sucesión funcional $f_n(x)=\frac{\left|x\right|}{1+nx^2}$ converge puntualmente a $f(x)=0$. ¿Convergerá uniformemente? Sea un número $d&gt;0$ cualquiera; queremos que

$\left|f_n\left(x\right)-f\left(x\right)\right|=\left|\frac{\left|x\right|}{1+nx^2}-0\right|=\frac{\left|x\right|}{1+nx^2}&lt;d\Leftrightarrow\frac x{1+nx^2}&lt;d$

siempre que $n&gt;n_0$. Operando:

$\frac x{1+nx^2}&lt;d\Leftrightarrow-ndx^2+x-d&gt;0\Leftrightarrow n&gt;\frac{x-d}{dx^2}.$

Para asegurar que se cumpla la última desigualdad para todo $x$, buscamos el valor máximo del término de la derecha; lo consideramos una función de $x$, derivamos respecto $x$ e igualamos a cero:

$D_x\left(\frac{x-d}{dx^2}\right)=\frac{1\left(dx^2\right)-\left(x-d\right)\cdot2dx}{\left(dx^2\right)^2}=0\Leftrightarrow-dx^2+2d^2x=0\Leftrightarrow x=2d.$

Para ver que es un máximo y no un mínimo basta con observar que la expresión $\frac{x-d}{dx^2}$ tiende al valor cero para $x\rightarrow\infty$, mientras que si sustituimos el valor $x=2d$ obtenemos el valor $\frac{2d-d}{d\cdot4d^2}=\frac d{4d^3}=\frac1{4d^2}&gt;0.$.

Así pues, dado un valor $d&gt;0$ cualquiera (de hecho, se supone que damos valores "pequeños" a $d$) hemos encontrado que, tomando los términos $n&gt;n_0$ con $n_0=\frac1{4d^2}$, todos ellos cumpliran la condición $\left|f_n\left(x\right)-f\left(x\right)\right|&lt;d$. Por ejemplo, sea $d=0,3$ (recordar que en la imagen anterior hemos trazado la región $-0,3 &lt; y &lt;0,3$); entonces $n_0=\frac1{4d^2}=\frac1{4\cdot0,3^2}=2,7.\;$. Cogiendo $n\geq3$ todos los términos iguales o posteriores al tercero entrarán dentro de la franja $-0,3 &lt; y &lt;0,3$, tal como se observa en la figura anterior. Por tanto concluimos que esta sucesión de funciones converge uniformemente a $f(x)=0$.

---

# Procedimiento práctico para estudiar la convergencia puntual y la convergencia uniforme de sucesiones de funciones

**1.** Dada una sucesión de funciones $f_n(x)$, primero estudiamos el límite $\lim_{n\rightarrow\infty}f_n\left(x\right)$ para ver si es puntualmente convergente. Hay que tener en cuenta al hacer el límite que la variable $x$ puede tomar cualquier valor en el dominio de la función. Si no es puntualmente convergente hemos terminado, pues ya no puede ser uniformemente convergente.

**2.** Si las funciones $f_n(x)$ son continuas pero la función límite es discontinua, también hemos terminado, pues no puede ser uniformemente convergente, dado que uniformemente convergente $\Rightarrow$ se conserva la continuidad en la función límite.

**3.** Si tenemos convergencia puntual a la función $f(x)$ y queremos comprobar la convergencia uniforme, podemos aplicar la definición 2, demostrando que para todo $d&gt;0$ siempre existe un $n_0$ tal que, para todo $n&gt;n_0$ se cumple la desigualdad $\left|f_n\left(x\right)-f\left(x\right)\right|&lt;d$. Esto puede ser inmediato, o no. En los casos que no sea fácil, podemos intentar aplicar un criterio equivalente:

**Criterio de convergencia uniforme de una sucesión $f_n(x)$**

$f_n(x)$ converge uniformemente al límite puntual $f(x)$ siempre que se cumpla:

$\lim_{n\rightarrow\infty}{\text{Sup}}_x\left|f_n\left(x\right)-f\left(x\right)\right|\text{=0}$.

**Ejemplo 4**: La sucesión $f_n(x)=\frac1{1+nx^2}$ de los ejemplos 1 y 2 no converge uniformemente a su límite puntual $f(x)=0$ para $x\neq0$,  $f(x)=1$ para $x=0$, pues todas las funciones $\frac1{1+nx^2}$ son continuas en todo su dominio, pero la función límite es discontinua.

**Ejemplo 5**: apliquemos el criterio de convergencia uniforme a la sucesión del ejemplo 3. Primero calculamos el valor ${\text{Sup}}_x\left|f_n\left(x\right)-f\left(x\right)\right|$:

${\text{Sup}}_x\left|\frac{\left|x\right|}{1+nx^2}-0\right|={\text{Sup}}_x\frac{\left|x\right|}{1+nx^2}\text{.}$

Derivamos la expresión para obtener el valor máximo:

$D_x\left(\frac x{1+nx^2}\right)=\frac{1\left(1+nx^2\right)-x\left(2nx\right)}{\left(1+nx^2\right)^2}=0\Rightarrow1-nx^2=0\Rightarrow x=\frac1{\sqrt n}.$

Hemos ignorado el valor absoluto pues la expresión $h(x)=\frac x{1+nx^2}$ es impar: $h(-x)=-h(x)$, entonces un máximo digamos en un punto $x_0$ implica un mínimo en $-x_0$ y viceversa.

Tenemos que ${\text{Sup}}_x\frac{\left|x\right|}{1+nx^2}\text{=}\frac1{\sqrt n}$ (observamos que no puede ser un mínimo pues para $x=0$ la expresión vale $0$). Pasamos ahora al límite:

$\lim_{n\rightarrow\infty}{\text{Sup}}_x\frac{\left|x\right|}{1+nx^2}\text{=}\lim_{n\rightarrow\infty}\frac1{\sqrt n}\text{=0.}$

Efectivamente se cumple la condición dada por el criterio, luego la sucesión converge uniformemente.

**Ejemplo 6:** Estudiar la convergencia de la sucesión $f_n\left(x\right)=\frac{\sin\left(nx\right)}{\sqrt n}$.

$\lim_{n\rightarrow\infty}f_n\left(x\right)=\lim_{n\rightarrow\infty}\frac{\sin\left(nx\right)}{\sqrt n}=0$, ya que el valor del numerador oscila entre -1 y 1 mientras que el denominador tiende a $\infty$. Luego la función límite es $f(x)=0$.

${\text{Sup}}_x\left|f_n\left(x\right)-f\left(x\right)\right|={\text{Sup}}_x\left|\frac{\sin\left(nx\right)}{\sqrt n}\right|=\frac1{\sqrt n}$, por la misma razón:  el valor del numerador oscila entre -1 y 1. Pasamos al límite: $\lim_{n\rightarrow\infty}\frac1{\sqrt n}=0$, luego la sucesión converge uniformemente. En la imagen siguiente vemos los términos 1, 5 y 100 de la serie (éste último en rojo). La amplitud de las oscilaciones tiende a $0$.

[caption id="attachment_134" align="alignnone" width="529"][![sin(nx) / n^(1/2)](/assets/images/sucesion-funcional4.jpg)](http://tallermatematic.eu/wp/wp-content/uploads/2014/07/sucesion-funcional4.jpg) sin(nx) / n^(1/2)[/caption]
**Ejemplo 7**: Estudiar la convergencia de la sucesión $f_n\left(x\right)=\frac{x^{2n}}{1+x^{2n}}$.

$\begin{array}{l}\lim_{n\rightarrow\infty}\frac{x^{2n}}{1+x^{2n}}=\left\{\begin{array}{c}0\;\text{si }x=0\\\frac12\;\text{si }x=1\\1\;\text{si }\left|x\right|&gt;1\end{array}\right.\\\end{array}$

La función límite es discontinua, pero las funciones de la sucesión son todas continuas, por tanto no puede ser uniformemente convergente. En la figura siguiente vemos los términos 1, 2, 3 y 10, éste último en rojo. Todas las funciones de la sucesión pasan por el punto $(x,y)=(1, 0.5)$. En el límite, este punto pasa a ser un punto aislado de la gráfica, resultando una función límite discontínua.

[caption id="attachment_135" align="alignnone" width="623"][![(x^2n)/(1+x^2n)](/assets/images/sucesion-funcional5.jpg)](http://tallermatematic.eu/wp/wp-content/uploads/2014/07/sucesion-funcional5.jpg) (x^2n)/(1+x^2n)[/caption]
**Ejemplo 8**: Estudiar la convergencia de la sucesión $\begin{array}{l}f_n\left(x\right)=x\left(1+\frac1n\right)\\\end{array}$.

$\begin{array}{l}\lim_{n\rightarrow\infty}x\left(1+\frac1n\right)=x\\\end{array}$, luego la función límite es $f(x)=x$. Todas las funciones de la sucesión, y también la función límite, son continuas, por lo que no podemos decir nada de la convergencia uniforme, debemos comprobarla.

$\begin{array}{l}{\text{Sup}}_x\left|x\left(1+\frac1n\right)-x\right|={\text{Sup}}_\mathrm x\left|\frac{\mathrm x}{\mathrm n}\right|\\\end{array}$. Esta expresión no está acotada, no existe el supremo. No obstante, si nos restringimos a cualquier intervalo $(a, b)$ de la recta real, entonces:

$\begin{array}{l}{\text{Sup}}_\mathrm x\left|\frac{\mathrm x}{\mathrm n}\right|=\frac{\mathrm b}{\mathrm n}\;\text{si }\mathrm x\in\left(\mathrm a,\mathrm b\right)\\\end{array}$

Pasando al límite:

$\begin{array}{l}\lim_{n\rightarrow\infty}\frac{\mathrm b}{\mathrm n}=0\;\text{si }\mathrm x\in\left(\mathrm a,\mathrm b\right)\\\end{array}$.

Por tanto la función es uniformemente convergente en cualquier intervalo $(a, b)$ pero no lo es en todo el dominio $\mathbb{R}$.

[![separador2](/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

# Bibliografía

 

Análisis Matemático: un buen libro de teoría de nivel más bien elevado; el capítulo 9 se dedica a las series funcionales