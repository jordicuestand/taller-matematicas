---
layout: post
title: "Problemas de límites y continuidad en el plano real"
date: 2014-07-17 09:07:54 +0000
categories:
  - "Cálculo en R"
  - "Cálculo en varias variables"
  - "Continuidad de funciones de varias variables"
  - "Funciones continuas"
  - "Funciones reales de dos variables"
  - "Límites de funciones de varias variables"
  - "Matemáticas"
tags:
  - "Cálculo"
  - "problemas resueltos de cálculo"
math: true
---
{% raw %}

**1.** Ver si la función f(x,y) es continua en (0,0), donde
$f(x,y)=\left\{\begin{array}{l}\frac{x^3}{x^2-y^2}\;\;\text{si }x^2-y^2\neq0\\0\;\;\text{si }\;x^2-y^2=0\end{array}\right.$

**Solución:**

Para ser continua en (0,0) debe cumplirse que $\lim_{\left(x,y\right)\rightarrow\left(0,0\right)}f(x,y)=f(0,0)$. Según la definición de la función, en (0, 0) se cumple la condición $x^2-y^2=0$, luego $f(0,0)=0$. Para calcular el límite debemos usar la otra expresión de la función válida en $x^2-y^2\neq0$: $\lim_{\left(x,y\right)\rightarrow\left(0,0\right)}\frac{x^3}{x^2-y^2}=?$. Para calcular este límite, usamos el siguiente teorema:

Teorema: *criterio de convergencia para funciones de dos variables reales*
Una condición necesaria y suficiente para que $\lim_{\left(x,y\right)\rightarrow\left(a,b\right)}f(x,y)=L$ es que, al hacer el cambio de variables de cartesianas a polares:

$x=\rho\cos\left(\theta\right),\;y=\rho\sin\left(\theta\right), 0\leq\theta&lt;2\pi$,

con lo que la función $f(x,y)$ se transforma en $f\left(\rho,\theta\right)$, se cumpla lo siguiente:

Para cada valor $\varepsilon&gt;0$ , por pequeño que sea, existe un $\delta&gt;0$, tal que si $0&lt;\rho&lt;\delta$ entonces se verifica que $\left|f\left(\rho,\theta\right)-L\right|&lt;\varepsilon$, independientemente del valor que tome $\theta$

 Hacemos el cambio de variables de cartesianas a polares:
$f(x,y)=\left\{\begin{array}{l}\frac{x^3}{x^2-y^2}\;\;\text{ si }x^2-y^2\neq0\Rightarrow\frac{\rho^3\cos^3\left(\theta\right)}{\rho^2\left(\cos^2\left(\theta\right)-\sin^2\left(\theta\right)\right)}\;\text{ si }\rho^2\left(\cos^2\left(\theta\right)-\sin^2\left(\theta\right)\right)\neq0\\0\;\;\text{si}\;x^2-y^2=0\Rightarrow0\;\;\text{si }\rho^2\left(\cos^2\left(\theta\right)-\sin^2\left(\theta\right)\right)=0\end{array}\right.$

 En nuestro caso actual, queremos ver si $L=0$ para $\left(x,y\right)=\left(0,0\right)$. Deberá cumplirse que
$\left|\frac{\rho^3\cos^3\left(\theta\right)}{\rho^2\left(\cos^2\left(\theta\right)-\sin^2\left(\theta\right)\right)}-0\right|&lt;\varepsilon$

$\Leftrightarrow\rho\left|\frac{\cos^3\left(\theta\right)}{\cos^2\left(\theta\right)-\sin^2\left(\theta\right)}\right|&lt;\varepsilon$

La $\rho$ ha salido fuera del valor absoluto porque $\rho&gt;0$.  Esta desigualdad ha de cumplirse para valores todo lo pequeños que queramos, independientemente de $\theta$, siempre que $0&lt;\rho&lt;\delta$. Para ello será necesario que la expresión $\frac{\cos^3\left(\theta\right)}{\cos^2\left(\theta\right)-\sin^2\left(\theta\right)}$ sea acotada, y lo será siempre que el denominador no se anule. ¿Cuándo se anulará el denominador?
$\cos^2\left(\theta\right)-\sin^2\left(\theta\right)=0\Leftrightarrow\theta=\frac{\mathrm\pi}4,\frac{\mathrm\pi}4+\frac{\mathrm\pi}2,\frac{\mathrm\pi}4+\mathrm\pi$

Entonces, sea cual sea el valor que damos a $\rho$, cuando nos acercamos a alguno de esos valores de $\theta$:
$\lim_{\theta\rightarrow\frac{\mathrm\pi}4}\frac{\cos^3\left(\theta\right)}{\cos^2\left(\theta\right)-\sin^2\left(\theta\right)}=\frac{1/\sqrt2}{1/2-1/2}=\infty$

O sea que no se cumple la condición necesaria y suficiente para todo $\theta$, por tanto la función no es contínua en $\left(0,0\right)$.

Para que quede más claro, veamos un ejemplo: fijamos $\varepsilon=0.01$, y queremos conseguir que
$\rho\left|\frac{\cos^3\left(\theta\right)}{\cos^2\left(\theta\right)-\sin^2\left(\theta\right)}\right|&lt;0.01$,

y lo queremos para cualquier $0\leq\theta&lt;2\pi$. Entonces:
$0&lt;\rho&lt;0.01\left|\frac{\cos^2\left(\theta\right)-\sin^2\left(\theta\right)}{\cos^3\left(\theta\right)}\right|$,

pero cuando $\theta=\frac{\mathrm\pi}4,\frac{\mathrm\pi}4+\frac{\mathrm\pi}2,\frac{\mathrm\pi}4+\mathrm\pi$, resulta que $\left|\frac{\cos^2\left(\theta\right)-\sin^2\left(\theta\right)}{\cos^3\left(\theta\right)}\right|=0$, y no existe ningún $0&lt;\rho$ que verifique la condición. $\square$

---

**2.** Calcular $\lim_{x\rightarrow\infty}\frac{x\sin\left(x\right)}{x^2+1}$

**Solución**:

$\lim_{x\rightarrow\infty}\frac{x\sin\left(x\right)}{x^2+1}=\frac\infty\infty=?$; separemos el límite en dos componentes: la fracción racional y la función trigonométrica:

$\lim_{x\rightarrow\infty}\frac{x\sin\left(x\right)}{x^2+1}=\lim_{x\rightarrow\infty}\frac x{x^2+1}\cdot\lim_{x\rightarrow\infty}\sin\left(x\right)=L_1\cdot L_2$.

El primer límite es:

$L_1=\lim_{x\rightarrow\infty}\frac x{x^2+1}=\lim_{x\rightarrow\infty}\frac{x/x^2}{\left(x^2+1\right)/x^2}\lim_{x\rightarrow\infty}\frac{1/x}{1+1/x^2}=\frac0{1+0}=0.$

El segundo límite no existe, pues la función $\sin(x)$ es oscilante; ahora bien, el producto de los límites sí existe, pues $L_1=0$ y $L_2$ está acotado entre los valores $\left[-1,1\right]$, por tanto el producto $L_1·L_2$ es igual a $0$. $\square$

---

**3.** Calcular $\lim_{x\rightarrow\infty}\left(\sqrt{x\left(x+1\right)}-x\right)$.

**Solución**:

Es indeterminado: $\lim_{x\rightarrow\infty}\left(\sqrt{x\left(x+1\right)}-x\right)=\infty-\infty=?$. Podemos convertirlo al tipo fracción racional para deshacer la indeterminación:

$\lim_{x\rightarrow\infty}\left(\sqrt{x\left(x+1\right)}-x\right)=\lim_{x\rightarrow\infty}\frac{\left(\sqrt{x\left(x+1\right)}-x\right)\left(\sqrt{x\left(x+1\right)}+x\right)}{\left(\sqrt{x\left(x+1\right)}+x\right)}=\lim_{x\rightarrow\infty}\frac{x\left(x+1\right)-x^2}{\sqrt{x\left(x+1\right)}+x}=\lim_{x\rightarrow\infty}\frac x{\sqrt{x\left(x+1\right)}+x}=\frac\infty\infty$,

que sigue siendo indeterminado.  Dividimos numerador y denominador por $x$ elevado al mayor exponente de ambos:

$\lim_{x\rightarrow\infty}\frac x{\sqrt{x\left(x+1\right)}+x}=\lim_{x\rightarrow\infty}\frac{x/x}{\left(\sqrt{x\left(x+1\right)}+x\right)/x}=\lim_{x\rightarrow\infty}\frac1{\left(\sqrt{\displaystyle\frac{x\left(x+1\right)}{x^2}}+1\right)}=\lim_{x\rightarrow\infty}\frac1{\left(\sqrt{1+\displaystyle\frac1x}+1\right)}=\frac12. \square$

---

**4.** Calcular $\lim_{x\rightarrow0}e^\frac{\left|x\right|}x$.

**Solución**:

La expresión del exponente vale:

$\frac{\left|x\right|}x=\left\{\begin{array}{l}1\;\text{ si }x&gt;0\\-1\;\text{ si }x&lt;0\end{array}\right.$,

para $x=0$ la expresión no está definida, y es precisamente en este punto que nos piden el límite. Por tanto debemos calcular los límites laterales, y comprobar si coinciden.

$\lim_{x\rightarrow0^-}e^\frac{\left|x\right|}x=e^{-1}=\frac1e$

$\lim_{x\rightarrow0+}e^\frac{\left|x\right|}x=e^1=e$.

Vemos que no coinciden, luego el límite en $x=0$ no existe. $\square$

---

**5.**  Calcular $L=\lim_{x\rightarrow\infty}x^{2/3}\left(\sqrt[3]{x+1}-\sqrt[3]x\right)$.

**Solución**:
Es un límite indeterminado debido al signo menos entre las dos raíces cúbicas: $\lim_{x\rightarrow\infty}x^{2/3}\left(\sqrt[3]{x+1}-\sqrt[3]x\right)=\infty\cdot\left(\infty-\infty\right)=?$. Cuando tenemos un límite indeterminado que contiene raíces cuadradas tal como $\left(\sqrt a-\sqrt b\right)$ lo que hacemos es usar la igualdad $\left(\sqrt a+\sqrt b\right)\left(\sqrt a-\sqrt b\right)=a-b$ para transformar la expresión original en una expresión racional que no tiene diferencias  entre raíces:

$\left(\sqrt a-\sqrt b\right)=\frac{\left(\sqrt a-\sqrt b\right)\left(\sqrt a+\sqrt b\right)}{\left(\sqrt a+\sqrt b\right)}=\frac{a-b}{\left(\sqrt a+\sqrt b\right)}$.

Ahora nos interesa hacer lo mismo, pero con raíces cúbicas, usando alguna expresión combinando $a^3$ y $b^3$ para dar $a^3-b^3$. Esta expresión es:

$\left(a-b\right)\left(\left(a+b\right)\left(a+b\right)\right)=\left(a-b\right)\left(a^2+b^2+ab\right)=a^3+ab^2+a^2b-ba^2-b^3-ab^2=a^3-b^3$.

Identificando $a=x^\frac23\sqrt[3]{x+1}=\sqrt[3]{x^2\left(x+1\right)};\;b=x^\frac23\sqrt[3]x=\sqrt[3]{x^3}=x$ y usando la expresión

$\left(a-b\right)=\frac{\left(a-b\right)\left(a^2+b^2+ab\right)}{a^2+b^2+ab}=\frac{a^3-b^3}{a^2+b^2+ab}$

obtenemos:

$L=\lim_{x\rightarrow\infty}\frac{x^2\left(x+1\right)-x^3}{\left(x^2\left(x+1\right)\right)^{2/3}+x^2+\sqrt[3]{x^5\left(x+1\right)}}=\lim_{x\rightarrow\infty}\frac{x^2}{\left(x^3+x^2\right)^{2/3}+x^2+\left(x^6+x^5\right)^{1/3}}$,

 un límite en el infinito de una expresión racional (polinomios en el numerador y en el denominador), podemos aplicar la regla que dice: fíjate sólo en los términos de mayor grado del numerador y del denominador, ignorando los de grado inferior:

$L=\lim_{x\rightarrow\infty}\frac{x^2}{\left(x^3+x^2\right)^{2/3}+x^2+\left(x^6+x^5\right)^{1/3}}=\lim_{x\rightarrow\infty}\frac{x^2}{\left(x^3\right)^{2/3}+x^2+\left(x^6\right)^{1/3}}=\lim_{x\rightarrow\infty}\frac{x^2}{x^2+x^2+x^2}=\lim_{x\rightarrow\infty}\frac{x^2}{3x^2}=\frac13.$

Formalmente, llegamos al mismo resultado dividiendo numerador y denominador por el término de mayor grado:
$L=\lim_{x\rightarrow\infty}\frac{\displaystyle\frac{x^2}{x^2}}{\displaystyle\frac{\left(x^3+x^2\right)^\frac23+x^2+\left(x^6+x^5\right)^{\displaystyle\frac13}}{x^2}}$

Simplificando, y luego haciendo el paso al límite:

$L=\lim_{x\rightarrow\infty}\frac1{\left({\displaystyle\frac{x^3+x^2}{x^3}}\right)^{\displaystyle\frac23}+1+\left({\displaystyle\frac{x^6+x^5}{x^6}}\right)^{\displaystyle\frac13}}=\frac1{\left(1+0\right)^\frac23+1+\left(1+0\right)^\frac13}=\frac13.\square$

---

**6.** Calcular $L=\lim_{x\rightarrow2}\frac1{x^2-4}-\frac3{x^3-2x^2-4x+8}$.

**Solución**:

$L=\lim_{x\rightarrow2}\frac1{x^2-4}-\frac3{x^3-2x^2-4x+8}=\frac10-\frac10=\infty-\infty=?$. Fijémonos en que es un límite en un punto, no en el infinito, así pues, debemos deshacer la indeterminación de otro modo. El hecho de que los dos denominadores valgan cero en el punto $x=2$ significa que este punto es una raíz de esos polinomios, y por tanto podemos descomponerlos en producto de binomios para simplificar la expresión:

$x^2-4=\left(x+2\right)\left(x-2\right);\;x^3-2x^2-4x+8=\left(x-2\right)\cdot P(x)$

Obtenemos el polinomio $P(x)$ como el resto de la división de $x^3-2x^2-4x+8$ entre $x-2$, usando la regla de Ruffini:

$\begin{array}{l}2\;\left|+1\;-2\;-4\;+8\right.\\\;\;\;\;\underline{\;\;\;\;\;\;\;+2\;\;\;0\;\;-8}\\\;\;\;\;\;+1+0\;-4\;\;\;\left|\underline0\right.\end{array}$.

Tenemos que $P(x)=x^2-4$, por tanto:

$\frac1{x^2-4}-\frac3{x^3-2x^2-4x+8}=\frac1{\left(x+2\right)\left(x-2\right)}-\frac3{\left(x^2-4\right)\left(x-2\right)}=\frac1{x-2}\left(\frac1{x+2}-\frac3{x^2-4}\right)$

Pasando al límite:

$\lim_2\frac1{x-2}\left(\frac1{x+2}-\frac3{x^2-4}\right)=\frac10\left(\frac14-\frac30\right)=\infty\cdot\left(-\infty\right)=-\infty$

Siempre que tengamos un límite infinito en un punto debemos calcular los límites laterales, pues es posible que tengamos un cambio de signo:

$\lim_{2^-}\frac1{x-2}\left(\frac1{x+2}-\frac3{x^2-4}\right)=\frac1{0^-}\left(\frac1{4^-}-\frac3{0^-}\right)=-\infty\cdot\left(+\infty\right)=-\infty$

$\lim_{2^+}\frac1{x-2}\left(\frac1{x+2}-\frac3{x^2-4}\right)=\frac1{0^+}\left(\frac1{4^+}-\frac3{0^+}\right)=+\infty\cdot\left(-\infty\right)=-\infty$

En este caso coinciden, la función $f(x)=\frac1{x^2-4}-\frac3{x^3-2x^2-4x+8}$ tiene una asíntota vertical en $x=2$:

[caption id="attachment_109" align="alignnone" width="432"][![problema4-tema4-apunts](/assets/images/problema4-tema4-apunts.jpg)](http://tallermatematic.eu/wp/wp-content/uploads/2014/07/problema4-tema4-apunts.jpg) Realizado con http://fooplot.com/[/caption]

---

 

**7.** Estudiar la continuidad y la existencia de derivadas parciales de la función
$f\left(x\right)=\left\{\begin{array}{l}x\cos\left(\frac1{x^2+y^2}\right),\;\left(x,y\right)\neq\left(0,0\right)\\0,\;\;\left(x,y\right)=\left(0,0\right)\end{array}\right.$

En $\left(x,y\right)\neq\left(0,0\right)$ la función es claramente continua, por serlo la función $cos(x)$ así como el cociente $\frac1{x^2+y^2}$. El punto dudoso es pues el $(0,0)$. En él debemos aplicar la definición de continuidad:

La función $f(x)$ es continua en el punto $x_0$ si y solo si se cumple la condición:

$\lim_{x\rightarrow x_0}f\left(x\right)=f\left(x_0\right)$

Lo aplicamos pues:

$\begin{array}{l}\lim_{\left(x,y\right)\rightarrow\left(0,0\right)}x\cos\left(\frac1{x^2+y^2}\right)=\lim_{r\rightarrow0}r\cos\left(\theta\right)\cos\left(\frac1{r^2\cos^2\left(\theta\right)+r^2\sin^2\left(\theta\right)}\right)=\\\lim_{r\rightarrow0}r\cos\left(\theta\right)\cos\left(\frac1{r^2}\frac1{\cos^2\left(\theta\right)+\sin^2\left(\theta\right)}\right).\end{array}$

Sabiendo que la función $cos$ está acotada, podemos tomar el valor absoluto de este límite y acotarlo:

$\underset{r\rightarrow0}{\lim\;}\left|r\cos\left(\theta\right)\cos\left(\frac1{r^2}\right)\right|\leq\underset{r\rightarrow0}{\lim\;}\left|r\cos\left(\theta\right)\right|\leq\underset{r\rightarrow0}{\lim\;}\left|r\right|=0.$

Por tanto $\lim_{\left(x,y\right)\rightarrow\left(0,0\right)}f\left(x,y\right)=0=f\left(0,0\right)$ y la función es continua en todo el dominio.

Para ver la existencia de derivadas parciales, vemos que si $\left(x,y\right)\neq\left(0,0\right)$ la función tiene las siguientes derivadas parciales:

$\begin{array}{l}\frac{\partial f}{\partial x}=\cos\left(\frac1{x^2+y^2}\right)-x\sin\left(\frac1{x^2+y^2}\right)\cdot\frac{-2x}{\left(x^2+y^2\right)^2},\\\frac{\partial f}{\partial y}=-x\sin\left(\frac1{x^2+y^2}\right)\cdot\frac{-2y}{\left(x^2+y^2\right)^2}.\end{array}$

En el punto $\left(x,y\right)=\left(0,0\right)$ no podemos derivar con las reglas usuales pues tenemos la bifurcación de la definición de la función, hay que usar la definición de derivada parcial:

$\begin{array}{l}\frac{\partial f\left(0,0\right)}{\partial x}=\lim_{h\rightarrow0}\frac{f\left(0+h,0\right)-f\left(0,0\right)}h=\\\lim_{h\rightarrow0}\frac{h\cos\left({\displaystyle\frac1{h^2}}\right)-0}h=\lim_{h\rightarrow0}\cos\left(\frac1{h^2}\right).\end{array}$

Pero este límite no existe, pues el $cos$ oscila entre $[-1,1]$ indefinidamente, luego no existe la derivada parcial respecto a $x$ en el punto $(0,0)$. Para la otra derivada parcial:

$\begin{array}{l}\frac{\partial f\left(0,0\right)}{\partial y}=\lim_{h\rightarrow0}\frac{f\left(0,0+h\right)-f\left(0,0\right)}h=\\\lim_{h\rightarrow0}\frac{0\cdot\cos\left({\displaystyle\frac1{h^2}}\right)-0}h=0.\end{array}$

Luego sí existe  la derivada parcial respecto a $y$ en el punto $(0,0)$, y por tanto en todos los puntos. Tenemos pues que esta función es contínua en todos los puntos, también tiene derivada parcial respecto a $y$, pero en el punto $(0,0)$ no tiene derivada parcial respecto a x.

---

**8.** Calcular el límite de la función vectorial de variable vectorial $\lim_{\left(x,y\right)\rightarrow\left(0,0\right)}\left(x\sin\left(x+y\right),\left(1+x\right)^x\right).$

Se trata de una función $f(x,y)$ que asigna a cada vector $(x,y)$ del plano otro vector del plano, de forma que podemos ver este segundo vector imágen del primero como el resultado de aplicar dos funciones vectoriales de variable real, que juntas componen la función original:

$f\left(x,y\right)=\left(x\sin\left(x+y\right),\left(1+x\right)^x\right)=\left(f_1\left(x,y\right),f_2\left(x,y\right)\right).$

Calculamos el límite por separado para cada función componente, pasando a coordenadas polares $x=r\cos\left(\theta\right), y=r\sin\left(\theta\right)$:

$\begin{array}{l}\lim_{r\rightarrow0}f_1\left(x,y\right)=r\cos\left(\theta\right)\cdot\sin\left(r\cos\left(\theta\right)+r\sin\left(\theta\right)\right)=\\\lim_{r\rightarrow0}r\cos\left(\theta\right)\cdot\sin\left(r\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)=\\0\cdot\cos\left(\theta\right)\cdot\sin\left(0\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)\right)=0\cdot0\;=\;0\end{array}$

ya que la función coseno está acotada, y al multiplicarla por cero resulta cero, y la expresión $\left(\cos\left(\theta\right)+\sin\left(\theta\right)\right)$ también está acotada, al multiplicarla por cero da cero, y la función seno en cero también vale cero. Para la segunda función componente:

$\begin{array}{l}f_2\left(x,y\right)=\left(1+x\right)^\frac1x\Rightarrow f_2\left(r,\theta\right)=\left(1+r\cos\left(\theta\right)\right)^\frac1{r\cos\left(\theta\right)}\Rightarrow\\\underset{\left(x,y\right)\rightarrow\left(0,0\right)}{\lim\;}f_2\left(x,y\right)\;=\lim_{r\rightarrow0\;}\left(1+r\cos\left(\theta\right)\right)^\frac1{r\cos\left(\theta\right)}=\left(1+0\right)^\frac10=1^\infty=?\end{array}$

tenemos una indeterminación del tipo:

$\lim_{x\rightarrow x_0}\left(1+\frac1{f\left(x\right)}\right)^{f\left(x\right)}=e.$

Operando:

$\lim_{r\rightarrow0\;}\left(1+r\cos\left(\theta\right)\right)^\frac1{r\cos\left(\theta\right)}=\lim_{r\rightarrow0\;}\left(1+\frac1{\left({\displaystyle\frac1{r\cos\left(\theta\right)}}\right)}\right)^\frac1{r\cos\left(\theta\right)}=e.$

En conclusión, $\lim_{\left(x,y\right)\rightarrow\left(0,0\right)}\left(x\sin\left(x+y\right),\left(1+x\right)^x\right)=\left(0,e\right).$

---
{% endraw %}