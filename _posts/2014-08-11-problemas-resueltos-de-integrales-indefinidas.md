---
layout: post
title: "Problemas resueltos de integrales indefinidas"
date: 2014-08-11 17:20:07 +0000
categories:
  - "Integración"
  - "Matemáticas"
tags:
  - "integración cambio de variable"
  - "integración fracciones racionales"
  - "integración por partes"
  - "integral indefinida"
  - "integral inmediata"
math: true
---
{% raw %}

**[Apuntes de Matemáticas](http://tallermatematic.eu/math/) -> Integración ****de funciones reales de variable real -> Problemas resueltos de integrales indefinidas**

---

 

**1.** Calcular $\int\frac{2x^3-7x^2+9x-5}{x^4-x^3}.$

Paso 1: encontrar las raíces del denominador:

$x^4-x^3=0\Leftrightarrow x^3\left(x-1\right)=0$, tenemos una raíz real triple en $x=0$ y otra simple en $x=1$.

Paso 2: descomponer la fracción en suma de fracciones simples.

$\frac{2x^3-7x^2+9x-5}{x^4-x^3}=\frac{2x^3-7x^2+9x-5}{x^3\left(x-1\right)}=\frac Ax+\frac B{x^2}+\frac C{x^3}+\frac D{x-1}.$

Operamos, haciendo denominador común:

$\frac{2x^3-7x^2+9x-5}{x^3\left(x-1\right)}=\frac Ax+\frac B{x^2}+\frac C{x^3}+\frac D{x-1}=\frac{Ax^2\left(x-1\right)+Bx\left(x-1\right)+C\left(x-1\right)+Dx^3}{x^3\left(x-1\right)}.$

Igualamos numeradores:

$2x^3-7x^2+9x-5=Ax^2\left(x-1\right)+Bx\left(x-1\right)+C\left(x-1\right)+Dx^3.$

Para encontrar los coeficientes, usamos algunos valores de $x$ para obtener las cuatro ecuaciones independientes necesarias:

$x=1\Rightarrow2\cdot1-7\cdot1+9\cdot1-5=A\cdot1\left(1-1\right)+B\cdot1\left(1-1\right)+C\left(1-1\right)+D\cdot1\;\Leftrightarrow-1=D.$

$x=0\Rightarrow2\cdot0-7\cdot0+9\cdot0-5=A\cdot0\left(0-1\right)+B\cdot0\left(0-1\right)+C\left(0-1\right)+D\cdot0\;\Leftrightarrow5=C.$

$\begin{array}{l}x=-1\Rightarrow-2-7-9-5=A\cdot1\left(-1-1\right)+B\cdot\left(-1\right)\left(-1-1\right)+C\left(-1-1\right)+D\cdot\left(-1\right)\;\Leftrightarrow\\-23=-2A+2B-2\cdot5-\left(-1\right)\Leftrightarrow\\-14=-2A+2B.\end{array}$

$\begin{array}{l}x=2\Rightarrow2\cdot2^3-7\cdot2^2+9\cdot2-5=A\cdot2^2\left(1\right)+B\cdot2\left(1\right)+C\left(1\right)+D\cdot2^3\;\Leftrightarrow\\1=4A+2B+C+8D=4A+2B+5+8\left(-1\right)\Leftrightarrow\\4=4A+2B.\end{array}$

Nos queda el sistema en $A, B$:

$\begin{array}{l}\underline{\left\{\;\begin{array}{l}-14\;=-2A+2B\\\;+4\;=+4A+2B\end{array}\right.}\\-18=-6A\;\Leftrightarrow A=3.\\B=\frac12\left(4-4A\right)=\frac{-8}2=-4\end{array}.$

La descomposición de la fracción racional es:

$\frac{2x^3-7x^2+9x-5}{x^3\left(x-1\right)}=\frac3x+\frac{-4}{x^2}+\frac5{x^3}+\frac{-1}{x-1}.$

Paso 3: integrar las fracciones simples.

$\begin{array}{l}\int\frac3x=3\ln\left(x\right).\\\int\frac{-4}{x^2}=-4\frac{x^{-1}}{-1}=\frac4x.\\\int\frac5{x^3}=5\frac{x^{-2}}{-2}=\frac{-5}{2x^2}.\\\int\frac{-1}{x-1}=-\ln\left(x-1\right).\end{array}.$

Resultado: $I=3\ln\left(x\right)+\frac4x+\frac{-5}{2x^2}-\ln\left(x-1\right)+C.$

---

**2.** Calcular $I=\int e^{2x}\cos^2\left(x\right)\operatorname{d}x.$

Si probamos por partes:

$\begin{array}{l}\operatorname{d}v=e^{2x},v=\frac12e^{2x},u=\cos^2\left(x\right),\;\operatorname{d}u=-2\cos\left(x\right)\sin\left(x\right)\operatorname{d}x\Rightarrow\\I=\frac12e^{2x}\cos^2\left(x\right)+\int\frac12e^{2x}\cdot2\cos\left(x\right)\sin\left(x\right)\operatorname{d}x.\end{array},$

la integral no se simplifica; si cambiamos los papeles a $V, u$:

$\operatorname{d}v=\cos^2\left(x\right)\operatorname{d}x,\;v=\int\cos^2\left(x\right)\operatorname{d}x,$

que tampoco nos simplifica el trabajo. La principal complicación de esta integral proviene del cuadrado de la función coseno. Podemos quitarlo usando la identidad trigonométrica:
$\cos\left(2x\right)=2\cos^2\left(x\right)-1.$

Entonces:

$I=\int e^{2x}\left(\cos\left(2x\right)+1\right)\frac12\operatorname{d}x=\frac12\int e^{2x}\cos\left(2x\right)\operatorname{d}x+\frac12\int e^{2x}\operatorname{d}x.$

La segunda integral es inmediata: $\int e^{2x}\operatorname{d}x=\frac12e^{2x}$; para la primera provamos por partes:

$\begin{array}{l}u=\cos\left(2x\right),\;\operatorname{d}u=-2\sin\left(2x\right)\operatorname{d}x,\;\operatorname{d}v=e^{2x},\;v=\frac12e^{2x}\Rightarrow\\\int e^{2x}\cos\left(2x\right)\operatorname{d}x=\frac12e^{2x}\cos\left(2x\right)+\int\frac12e^{2x}\cdot2\sin\left(2x\right)\operatorname{d}x.\end{array}.$

Queda una integral similar a la original, cambiando coseno por seno; repetimos la integración por partes para esta integral con seno:

$\begin{array}{l}u=\sin\left(2x\right),\;\operatorname{d}u=2\cos\left(2x\right)\operatorname{d}x,\;\operatorname{d}v=e^{2x},\;v=\frac12e^{2x}\Rightarrow\\\int e^{2x}\sin\left(2x\right)\operatorname{d}x=\frac12e^{2x}\sin\left(2x\right)-\int\frac12e^{2x}\cdot2\cos\left(2x\right)\operatorname{d}x.\Rightarrow\\\int e^{2x}\cdot\cos\left(2x\right)\operatorname{d}x=\frac12e^{2x}\cos\left(2x\right)+\frac12e^{2x}\sin\left(2x\right)-\int e^{2x}\cdot\cos\left(2x\right)\operatorname{d}x\Leftrightarrow\\\int e^{2x}\cdot\cos\left(2x\right)\operatorname{d}x=\frac14e^{2x}\left(\sin\left(2x\right)+\cos\left(2x\right)\right).\end{array}.$

Resultado:

$I=\frac18e^{2x}\left(\sin\left(2x\right)+\cos\left(2x\right)\right)+\frac14e^{2x}=\frac18e^{2x}\left(\sin\left(2x\right)+\cos\left(2x\right)+2\right)+C.$

---

**3.** Calcular $\int\frac{\left(\ln\left(x\right)\right)^3}x\operatorname{d}x.$

Observemos que $\int\frac{\left(\ln\left(x\right)\right)^3}x\operatorname{d}x=\int\left(\ln\left(x\right)\right)^3\cdot\frac{\operatorname{d}x}x=\int\left(\ln\left(x\right)\right)^3\cdot\operatorname{d}\left(\ln\left(x\right)\right)$, que se corresponde con la [integral inmediata](http://tallermatematic.eu/wp/?p=138#tabla_inmediatas) del tipo (3). Por tanto:

$\int\left(\ln\left(x\right)\right)^3\cdot\operatorname{d}\left(\ln\left(x\right)\right)=\frac14\left(\ln\left(x\right)\right)^4+C.$

---

 

**4.** Calcular $\int\frac{x^2+x+2}{\left(x^2+2\right)}\operatorname{d}x.$

Es una [integral del tipo racional](http://tallermatematic.eu/wp/?p=138#racionales), pero antes de proceder según el método habitual, observemos que

$\frac{x^2+x+2}{\left(x^2+2\right)^2}=\frac{x^2+2}{\left(x^2+2\right)^2}+\frac x{\left(x^2+2\right)^2}=\frac1{\left(x^2+2\right)^{}}+\frac x{\left(x^2+2\right)^2}.$

Ambas [integrales son inmediatas](http://tallermatematic.eu/wp/?p=138#tabla_inmediatas):

$\int\frac1{\left(x^2+2\right)^{}}\operatorname{d}x=\frac1{\sqrt2}\tan^{-1}\left(\frac x{\sqrt2}\right),\;\int\frac x{\left(x^2+2\right)^2}\operatorname{d}x=\frac{-1}2\int\left(x^2+2\right)^{-2}\left(-2x\right)\operatorname{d}x=\frac{-1}2\left(x^2+2\right)^{-1}.$

Queda pues: $I=\frac1{\sqrt2}\tan^{-1}\left(\frac x{\sqrt2}\right)-\frac12\frac1{\left(x^2+2\right)}+C.$

---

** 5.** Calcular $\int x\cdot\cos^{-1}\left(x^2\right)\operatorname{d}x.$

Probamos por partes:

$\begin{array}{l}u=\cos^{-1}\left(x^2\right),\;\operatorname{d}u=\frac{-2x}{\sqrt{1-x^4}}\operatorname{d}x,\;\operatorname{d}v=\operatorname{d}x,\;v=\frac{x^2}2\Rightarrow\\\int x\cdot\cos^{-1}\left(x^2\right)\operatorname{d}x=\frac{x^2}2\cos^{-1}\left(x^2\right)-\int\frac{x^2}2\frac{-2x}{\sqrt{1-x^4}}\operatorname{d}x=\\\frac{x^2}2\cos^{-1}\left(x^2\right)+\int\frac{x^3}{\sqrt{1-x^4}}\operatorname{d}x=\\\frac{x^2}2\cos^{-1}\left(x^2\right)-4\int\left(1-x^4\right)^\frac{-1}2\frac{-1}4\operatorname{d}\left(1-x^4\right)x^3\operatorname{d}x=\\\frac{x^2}2\cos^{-1}\left(x^2\right)-4\frac{\left(1-x^4\right)^\frac12}{\displaystyle\frac12}+C.\end{array}.$

Nota: para la $du$ hemos usado la derivada de la función inversa del coseno y la regla de la cadena de derivación: $\frac\operatorname{d}{\operatorname{d}x}\cos^{-1}\left(x\right)=\frac{-1}{\sqrt{1-x^2}}.$

---

 

**6.** Calcular $\int e^x\sin\left(\frac x2\right)\operatorname{d}x.$

Siendo un producto de funciones, parece aplicable la integración por partes:

$\begin{array}{l}u=\sin\left(\frac x2\right),\;\operatorname{d}u=\frac12\cos\left(\frac x2\right)\operatorname{d}x,\;\operatorname{d}v=e^x\operatorname{d}x,\;v=e^x\Rightarrow\\\I=int e^x\sin\left(\frac x2\right)\operatorname{d}x=e^x\sin\left(\frac x2\right)-\int e^x\frac12\cos\left(\frac x2\right)\operatorname{d}x.\end{array}$

Volvemos a integrar por partes la última integral del coseno:

$\begin{array}{l}u=\cos\left(\frac x2\right),\;\operatorname{d}u=\frac{-1}2\sin\left(\frac x2\right)\operatorname{d}x,\;\operatorname{d}v=e^x\operatorname{d}x,\;v=e^x\Rightarrow\\\int e^x\cos\left(\frac x2\right)\operatorname{d}x=e^x\cos\left(\frac x2\right)-\int e^x\frac{-1}2\sin\left(\frac x2\right)\operatorname{d}x=\\e^x\cos\left(\frac x2\right)+\frac12I.\end{array}$

Resumiendo todo:

$\begin{array}{l}I=e^x\sin\left(\frac x2\right)-\frac12\left$e^x\cos\left(\frac x2\right)+\frac12I\right$\Leftrightarrow\\I\left(1+\frac14\right)=e^x\left(\sin\left(\frac x2\right)-\frac12\cos\left(\frac x2\right)\right)\Leftrightarrow\\I=\frac54e^x\left(\sin\left(\frac x2\right)-\frac12\cos\left(\frac x2\right)\right)+C.\\\end{array}$

---

 

**7.** Calcular  $\int\frac{2x^6+4x^4+3x^2+2x-1}{x^6+2x^4+x^2}.$
Es una integral de tipo racional $\int\frac{P\left(x\right)}{Q\left(x\right)}\operatorname{d}x$; antes de aplicar el método de descomposición, recordamos que para ello el grado del polinomio denominador $Q$ ha de ser mayor que el grado del polinomio numerador $P$; como no es el caso, primero tendremos que efectuar la división de los polinomios:

$\begin{array}{l}2x^6+4x^4+3x^2+2x-1\;\left|\underline{x^6+2x^4+x^2}\right.\;\\2x^6+4x^4+2x^2\;\;\;\;\;\;\;\;\;\;\;\;\;\;2\\\overline{0x^6+0x^4+x^2+2x-1}\end{array}.$

Luego:

$\int\frac{2x^6+4x^4+3x^2+2x-1}{x^6+2x^4+x^2}\operatorname{d}x=\int2\operatorname{d}x+\int\frac{x^2+2x-1}{x^6+2x^4+x^2}.$

La primera integral del segundo miembro es simplemente $\int2\operatorname{d}x=2x.$ En la segunda integral aplicamos el método de descomposición en fracciones simples:

Paso 1: encontrar las raíces del denominador $Q$.

$x^6+2x^4+x^2=0\Leftrightarrow x^2\left(x^4+2x^2+1\right)=0.$

El punto $x=0$ es una raíz doble debido al cuadrado que afecta a $x$. La ecuación $x^4+2x^2+1=0$ es bicuadrada, hacemos el cambio $t=x^2$:

$t^2+2t+1=0\Rightarrow t=\frac{-2\pm\sqrt{4-4}}2=-1.$

Tenemos una raíz doble en $t=-1$. Como $x=\sqrt t=\sqrt{-1}$ es un número complejo, el polinomio $x^4+2x^2+1$ no tiene raíces reales, es irreducible en factores simples. Lo que aún podemos hacer es simplificarlo, viendo que es igual al cuadrado de un binomio:

$x^4+1+2x^2=\left(x^2\right)+1^2+2\cdot x^2\cdot1=\left(x^2+1\right)^2.$

La descomposición de $Q$ queda: $Q\left(x\right)=x^2\left(x^2+1\right)^2$, y la segunda integral se convierte en:

$\int\frac{x^2+2x-1}{x^2\left(x^2+1\right)^2}=\int\frac Ax+\int\frac B{x^2}+\int\frac{C+Dx}{x^2+1}+\int\frac{E+Fx}{\left(x^2+1\right)^2}.$

Paso 2: Hallar los coeficientes indeterminados.

Igualando la fracción original con la descomposición en fracciones simples y haciendo común denominador:

$\begin{array}{l}\frac{x^2+2x-1}{x^2\left(x^2+1\right)^2}=\frac Ax+\frac B{x^2}+\frac{C+Dx}{x^2+1}+\frac{E+Fx}{\left(x^2+1\right)^2}\Leftrightarrow\\\frac{x^2+2x-1}{x^2\left(x^2+1\right)^2}=\frac{Ax\left(x^2+1\right)^2+B\left(x^2+1\right)^2+\left(C+Dx\right)x^2\left(x^2+1\right)+\left(E+Fx\right)x^2}{x^2\left(x^2+1\right)^2}\Leftrightarrow\\x^2+2x-1=Ax\left(x^2+1\right)^2+B\left(x^2+1\right)^2+\left(C+Dx\right)x^2\left(x^2+1\right)+\left(E+Fx\right)x^2.\end{array}.$
Probamos algunos valores bien escogidos para simplificar la expresión. Este método funciona muy bien cuando todas las raíces son reales y simples, que no es el caso, aquí de las seis posibles raíces (tantas como el grado de $Q(x)$) solo tenemos una real que además es doble. Para esta raíz doble $x=0$:

$\begin{array}{l}0^2+2\cdot0-1=A\cdot0\left(x^2+1\right)^2+B\left(1\right)^2+\left(C+Dx\right)0\left(0+1\right)+\left(E+Fx\right)0\Leftrightarrow\\-1=B.\end{array}.$

Obtenemos un coeficiente, faltan otros cinco, así pues necesitamos cinco ecuaciones independientes. Reescribimos la expresión racional con el valor obtenido:

$\begin{array}{l}\begin{array}{l}x^2+2x-1=Ax\left(x^2+1\right)^2-\left(x^2+1\right)^2+\left(C+Dx\right)x^2\left(x^2+1\right)+\left(E+Fx\right)x^2\Leftrightarrow\end{array}\\x^2+2x-1+\left(x^4+1+2x^2\right)=Ax\left(x^4+1+2x^2\right)+\left(C+Dx\right)x^2\left(x^2+1\right)+\left(E+Fx\right)x^2\Leftrightarrow\\x^4+3x^2+2x=A\left(x^5+x+2x^3\right)+\left(Cx^4+Dx^5+Cx^2+Dx^3\right)+\left(Ex^2+Fx^3\right).\end{array}$

Igualamos coeficientes con sus respectivos términos, haciendo factor común para cada potencia de $x$:

$\begin{array}{l}x^4+3x^2+2x=A\left(x^5+x+2x^3\right)+\left(Cx^4+Dx^5+Cx^2+Dx^3\right)+\left(Ex^2+Fx^3\right).\\0x^5=x^5\left(A+D\right)\\x^4=x^4\left(C\right)\\0x^3=x^3\left(2A+D+F\right)\\3x^2=x^2\left(C+E\right)\\2x=x\left(A\right)\end{array}$

Queda el sistema de ecuaciones:

$\begin{array}{l}0=\left(A+D\right)\\1=\left(C\right)\\0=\left(2A+D+F\right)\\3=\left(C+E\right)\\2=\left(A\right)\end{array}$

del cual deducimos:

$\begin{array}{l}0=\left(2+D\right)\\0=\left(4+D+F\right)\\3=\left(1+E\right)\\\end{array}$

o sea:

$\begin{array}{l}0=\left(4-2+F\right)\Leftrightarrow F=-2\\3=\left(1+E\right)\Leftrightarrow E=2\\\end{array}$

En definitiva:

$A=2, B=-1, C=1, D=-2, E=2, F=-2.$

Paso 3: integrar las fracciones.

Las inmediatas son:

$\begin{array}{l}\int\frac2x=2\ln\left(x\right),\\\int\frac{-1}{x^2}=\frac1x,\\\int\frac{1-2x}{x^2+1}=\int\frac1{x^2+1}-\int\frac{2x}{x^2+1}=\tan^{-1}\left(x\right)-\ln\left(x^2+1\right).\end{array}$

La última integral es no inmediata, la separamos así:

$\begin{array}{l}\int\frac{2-2x}{\left(x^2+1\right)^2}\operatorname{d}x=-\int\frac{2x}{\left(x^2+1\right)^2}\operatorname{d}x+2\int\frac1{\left(x^2+1\right)^2}\operatorname{d}x;\\-\int\frac{2x}{\left(x^2+1\right)^2}\operatorname{d}x=-\int\left(x^2+1\right)^{-2}\operatorname{d}\left(x^2+1\right)=-\frac{\left(x^2+1\right)^{-2+1}}{-2+1}=\frac1{x^2+1}.\end{array}$

La integral $\int\frac1{\left(x^2+1\right)^2}\operatorname{d}x;$ hay que separarla también:

$\begin{array}{l}\int\frac1{\left(x^2+1\right)^2}=\int\frac{1+x^2-x^2}{\left(x^2+1\right)^2}=\int\frac{1+x^2}{\left(x^2+1\right)^2}+\int\frac{-x^2}{\left(x^2+1\right)^2}=\\\int\frac1{x^2+1}-\int\frac{-x^2}{\left(x^2+1\right)^2}=\tan^{-1}\left(x\right)-\int\frac{-x^2}{\left(x^2+1\right)^2}.\end{array}$

La integral que queda, $\int\frac{x^2}{\left(x^2+1\right)^2}$ , hay que hacerla por partes:

$\begin{array}{l}u=x,\;\operatorname{d}u=\operatorname{d}x,\;\operatorname{d}v=\frac x{\left(x^2+1\right)^2}\operatorname{d}x,\;v=\int\frac x{\left(x^2+1\right)^2}\operatorname{d}x=\frac{-1}{x^2+1}\Rightarrow\\\int\frac{x^2}{\left(x^2+1\right)^2}=x\frac{-1}{x^2+1}-\int\frac{-1}{x^2+1}\operatorname{d}x=\frac{-x}{x^2+1}+\tan^{-1}\left(x^2+1\right).\end{array}$

Resumiendo:

$\begin{array}{l}\int\frac{2-2x}{\left(x^2+1\right)^2}\operatorname{d}x=\frac1{x^2+1}+2\left(\tan^{-1}\left(x\right)-\frac x{x^2+1}+\tan^{-1}\left(x^2+1\right)\right)=\\\frac{1-2x}{x^2+1}+2\tan^{-1}\left(x\right)+2\tan^{-1}\left(x^2+1\right).\end{array}$

y juntando todos los resultados, concluimos que:

$\int\frac{2x^6+4x^4+3x^2+2x-1}{x^6+2x^4+x^2}=2x+2\ln\left(x\right)+\frac1x-\ln\left(x^2+1\right)+\frac{1-2x}{x^2+1}+3\tan^{-1}\left(x\right)+2\tan^{-1}\left(x^2+1\right)+C.$

NOTA: El procedimiento para calcular las integrales del tipo general $\int\frac{Mx+N}{\left$\left(x-r\right)^2+s^2\right$^p}\operatorname{d}x$ que aparecen cuando tenemos raíces complejas múltiples, es siempre el que se ha visto: separar en dos integrales, una inmediata, la otra del tipo $\int\frac1{\left$\left(x-r\right)^2+s^2\right$^p}\operatorname{d}x$, que también se separa en dos, sumando y restando al numerador el valor $x^2$, resultando una inmediata y otra por partes. si el exponente $p$ es mayor que 2, habrá que repetir la integración por partes para ir bajando el exponente en cada paso.

Si en vez de $\int\frac{Mx+N}{\left$\left(x-r\right)^2+s^2\right$^p}\operatorname{d}x$  tenemos $\int\frac1{\left$x^2+bx+c\right$^p}\operatorname{d}x$, podemos convertir esta forma en la primera con el procedimiento de completar cuadrados:

$x^2+bx+c=\left(x+M\right)^2+N\Rightarrow M=\frac b2,\;N=c-\frac{b^2}4.$

El caso $ax^2+bx+c$ se trata simplemente sacando $a$ fuera de la integral: $ax^2+bx+c=a\left(x^2+\frac bzx+\frac ca\right).$:

$\int\frac1{ax^2+bx+c}=\frac1a\int\frac1{x^2+{\displaystyle\frac ba}x+\displaystyle\frac ca}.$

Por ejemplo:

$\begin{array}{l}\int\frac1{2x^2+3x+4}=\frac12\int\frac1{x^2+{\displaystyle\frac32}x+\displaystyle\frac42};\\x^2+\frac32x+\frac42=(x+N)^2+M=\left(x+\frac34\right)^2+\left(\frac42-\frac{9/4}4\right)=\left(x+\frac34\right)^2+\frac{23}{16};\\\frac12\int\frac1{x^2+{\displaystyle\frac32}x+\displaystyle\frac42}=\frac12\int\frac1{\displaystyle\left(x+\frac34\right)^2+\frac{23}{16}}.\end{array}$

Estas integrales son siempre del tipo $\int\frac1{1+x^2}dx=\tan^{-1}\left(x\right)$, aunque hay que hacer algunos arreglos para verlo:

$\begin{array}{l}\int\frac{dx}{\displaystyle\left(x+\frac34\right)^2+\frac{23}{16}}=\int\frac{dx}{\displaystyle\frac{23}{16}\left$\frac{16}{23}\left(x+\frac34\right)^2+1\right$}=\\\frac{16}{23}\int\frac{dx}{\left({\displaystyle\frac4{\sqrt{23}}}x+\displaystyle\frac3{\sqrt{23}}\right)^2+1}=\frac{16}{23}\int\frac{dt}{{\displaystyle t}^2+1}\frac{\sqrt{23}}4=\\\frac4{\sqrt{23}}\tan^{-1}\left(t\right)=\frac4{\sqrt{23}}\tan^{-1}\left(\frac4{\sqrt{23}}x+\frac3{\sqrt{23}}\right).\end{array}$

donde hemos hecho el cambio de variable: $t=\left(\frac4{\sqrt{23}}x+\frac3{\sqrt{23}}\right)\Rightarrow dt=\frac4{\sqrt{23}}dx.$

---

**8.** Calcular $\int\frac1{\sin\left(3x\right)+\sin\left(x\right)}.$

La dificultad está en la función $sin\left(3x\right)$, en estos casos es muy útil recordar algunas fórmulas trigonométricas para transformar la integral. Usemos la igualdad
$\sin\left(A\right)+\sin\left(B\right)=2\sin\left(\frac{A+B}2\right)\cos\left(\frac{A-B}2\right).$

Resulta $\sin\left(3x\right)+\sin\left(x\right)=2\sin\left(\frac{4x}2\right)\cos\left(\frac{2x}2\right)=2\sin\left(2x\right)\cos\left(x\right).$ Aún tenemos el ángulo doble $2x$, usamos la identidad del ángulo doble:
$\sin\left(2x\right)=2\sin\left(x\right)\cos\left(x\right)$

Entonces: $2\sin\left(2x\right)\cos\left(x\right)=4\sin\left(x\right)\cos^2\left(x\right)$. Tenemos la integral $\int\frac1{4\sin\left(x\right)\cos^2\left(x\right)}\operatorname{d}x$. Ahora que ya no tenemos múltiplos de $x$, las integrales con combinaciones de $sin(x), cos(x), tan(x)$ muchas veces se resuelven con los cambios de variable $t=sin(x), t=cos(x), t=tan(x)$. Probemos $t=cos(x)$:

$\begin{array}{l}t=\cos\left(x\right),\operatorname{d}t=-\sin\left(x\right)\operatorname{d}x\Rightarrow\operatorname{d}x=\frac{-\operatorname{d}t}{\sin\left(x\right)}=\frac{-\operatorname{d}t}{\sqrt{1-t^2}}\Rightarrow\\\int\frac1{4\sin\left(x\right)\cos^2\left(x\right)}\operatorname{d}x=\frac14\int\frac{-1}{\sqrt{1-t^2}t^2}\frac{-\operatorname{d}t}{\sqrt{1-t^2}}=\frac14\int\frac{-1}{\left(1-t^2\right)t^2}\operatorname{d}t.\end{array}$

que es una integral de tipo racional. El denominador se descompone en factores simples:

$\int\frac1{\left(1-t^2\right)t^2}\operatorname{d}t=\int\frac1{\left(1-t\right)\left(1+t\right)t^2}=\int\frac A{\left(1-t\right)}+\int\frac B{\left(1+t\right)}+\int\frac Ct+\int\frac D{t^2}.$

Haciendo común denominador:

$\frac A{\left(1-t\right)}+\frac B{\left(1+t\right)}+\frac Ct+\frac D{t^2}=\frac{A\left(1+t\right)t^2+B\left(1-t\right)t^2+Ct\left(1+t\right)\left(1-t\right)+D\left(1+t\right)\left(1-t\right)}{\left(1+t\right)\left(1-t\right)t^2}.$

Igualando numeradores: $A\left(1+t\right)t^2+B\left(1-t\right)t^2+Ct\left(1+t\right)\left(1-t\right)+D\left(1+t\right)\left(1-t\right)=1$. Ahora damos los valores de las raíces (que son $t=0, 1, -1$) a esta expresión:

$\begin{array}{l}t=0\Rightarrow D=1.\\t=1\Rightarrow2A=1\Rightarrow A=1/2.\\t=-1\Rightarrow2B=1\Rightarrow B=1/2.\end{array}$

Queda un coeficiente; sustituimos los valores ya determinados:

$\begin{array}{l}A\left(1+t\right)t^2+B\left(1-t\right)t^2+Ct\left(1+t\right)\left(1-t\right)+D\left(1+t\right)\left(1-t\right)=\\\frac12\left(1+t\right)t^2+\frac12\left(1-t\right)t^2+Ct\left(1+t\right)\left(1-t\right)+\left(1+t\right)\left(1-t\right)=1\end{array}$

Una buena elección para simplificar la expresión es tomar $t=\sqrt2$ ya que se anularan los $t^2$ con los $1/2$:

$\begin{array}{l}t=\sqrt2\Rightarrow\left(1+\sqrt2\right)+\left(1-\sqrt2\right)-C\sqrt2-1=1\Leftrightarrow\\1-C\sqrt2=1\Leftrightarrow C=0.\\\end{array}$

Integramos y deshacemos el cambio $t=cos(x)$:

$\begin{array}{l}\frac{-1}4\int\frac1{\left(1-t^2\right)t^2}\operatorname{d}t=\frac{-1}4\left$\int\frac1{t^2}+\frac12\int\frac1{1+t}+\frac12\int\frac1{1-t}\right$=\\\frac{-1}4\left$\frac{-1}t+\frac12\left(-\ln\left(1-t\right)+\ln\left(1+t\right)\right)\right$=\\\frac{-1}4\left$\frac{-1}t+\frac12\ln\left(\frac{1+t}{1-t}\right)\right$=\\\frac14\left$\frac1{\cos\left(x\right)}+\frac12\ln\left(\frac{1-\cos\left(x\right)}{1+\cos\left(x\right)}\right)\right$+C.\end{array}$

---

**9.** Calcular $\int\frac{x^2+2x+3}{\left(x+1\right)\left(x^2+x+1\right)}dx.$

Es del tipo racional, el denominador no puede descomponerse más, ya es irreducible. Planteamos la descomposición en fracciones:

$I=\int\frac{x^2+2x+3}{\left(x+1\right)\left(x^2+x+1\right)}dx=\int\frac A{x+1}dx+\int\frac{Bx+C}{x^2+x+1}=I_1+I_2.$

Haciendo denominador común llegamos a la igualdad $A\left(x^2+x+1\right)+\left(Bx+C\right)\left(x+1\right)=x^2+2x+3.$ Damos el valor de la única raíz real del denominador de la integral que tenemos, $x=-1$, para obtener $A\left(1\right)+\left(Bx+C\right)\left(0\right)=2\Rightarrow A=2.$ Ahora nos queda operar y resolver el sistema de ecuaciones resultante:

$\begin{array}{l}2\left(x^2+x+1\right)+\left(Bx+C\right)\left(x+1\right)=x^2+2x+3\Rightarrow\\2x^2+2x+2+Bx^2+Bx+Cx+C=x^2+2x+3\Rightarrow\end{array}$

$\left\{\begin{array}{l}2+B=1\Rightarrow\boxed{B=-1}\\2+B+C=2\\2+C=3\Rightarrow\boxed{C=1}\end{array}\right.$

La segunda ecuación es redundante, nos sirve para comprobar que no nos hemos equivocado: $2+B+C=2\Leftrightarrow2-1+1=2\;\text{Ok}$

La integral queda:

$I=\int\frac2{x+1}dx+\int\frac{-x+1}{x^2+x+1}=I_1+I_2.$

La primera integral es inmediata: $I_1=\int\frac2{x+1}dx=2\ln\left(x+1\right).$

La segunda integral la descomponemos en dos, una del tipo $\int\frac{f'\left(x\right)}{f\left(x\right)}=\ln\left(f\left(x\right)\right)$ y otra del tipo $\int\frac1{ax^2+bx+c}$, la primera es inmediata, la segunda necesita algunos retoques, tal como se ha visto en el problema 7, en la nota al final del problema::

$I_2=\int\frac{-x+1}{x^2+x+1}=-\frac12\int\frac{2x+1}{x^2+x+1}dx+\frac32\int\frac1{x^2+x+1}dx=I_3+I_4.$

La inmediata del tipo logaritmo es:

$I_3=-\frac12\int\frac{2x+1}{x^2+x+1}dx=-\frac12\ln\left(x^2+x+1\right).$

La última integral $I_4$ es del tipo $\int\frac{dx}{1+x^2}=\tan^{-1}\left(x\right)$, operamos con ella. Primero, completamos cuadrados:

$\begin{array}{l}x^2+x+1=\left(x+M\right)^2+N=x^2+M^2+2Mx+N\Leftrightarrow\\M=1/2,\;N=1-1/4=3/4.\end{array}$

Ahora sustituimos en $I_4$ y hacemos un cambio de variable:

$\begin{array}{l}I_4=\frac32\int\frac{dx}{\left(x+\displaystyle\frac12\right)^2+\displaystyle\frac34}=\frac32\int\frac{dx}{{\displaystyle\frac34}\left${\displaystyle\frac43}\left(x+\displaystyle\frac12\right)^2+\displaystyle1\right$}=\\\frac32\frac43\int\frac{dx}{\displaystyle\left(\frac2{\sqrt3}x+\frac1{\sqrt3}\right)^2+1}=2\int\frac{dt}{t^2+1}\frac{\sqrt3}2=\\\sqrt3\tan^{-1}\left(t\right)=\sqrt3\tan^{-1}\left(\frac2{\sqrt3}x+\frac1{\sqrt3}\right).\end{array}$

Lo ponemos todo junto:

$\begin{array}{l}I=I_1+I_2=2\ln\left(x+1\right)+I_3+I_4=\\2\ln\left(x+1\right)-\frac12\ln\left(x^2+x+1\right)+\sqrt3\tan^{-1}\left(\frac2{\sqrt3}x+\frac1{\sqrt3}\right)+C.\\.\end{array}$

---

**10.** Calcular $I=\int ArcSin^2\left(x\right)\operatorname{d}x.$
En las tablas de integrales inmediatas no encontraremos la integral $\int ArcSin(x)\operatorname{d}x$, no tiene una integral inmediata. Esto significa que el procedimiento de integración por partes (pensando en que $ArcSin^2(x)= ArcSin(x) \cdot ArcSin(x)$ no será de ayuda, ya que si por ejemplo intentamos $u=ArcSin\left(x\right),\;dv=ArcSin\left(x\right)\operatorname{d}x$ no podremos obtener $v=\int ArcSin\left(x\right)\operatorname{d}x$ fácilmente.

Por otra parte si que tenemos la derivada de la función: $\frac{\operatorname{d}{}}{\operatorname{d}x}ArcSin\left(x\right)=\frac1{\sqrt{1-x^2}},$ entonces podemos intentar un cambio de variable para "quitar" la función $ArcSin(x)$ de la integral:

$t=ArcSin\left(x\right)\Rightarrow x=\sin\left(t\right),$

ya que la función $ArcSin(x)$ es la inversa de la función $sin(x)$; derivando:

$dx=\cos\left(t\right)dt\Rightarrow I=\int t^2\cos\left(t\right)\operatorname{d}t.$

Esta integral en la variable $t$ si la podemos hacer por partes:

$\begin{array}{l}u=t^2,dv=\cos\left(t\right)dt,\;du=2t\operatorname{d}t,\;v=\sin\left(t\right)\Rightarrow\\I=t^2\sin\left(t\right)-\int2t\sin\left(t\right)\operatorname{d}t.\end{array}$

La segunda integral también la hacemos por partes:

$\begin{array}{l}u=t,dv=\sin\left(t\right)dt,\;du=\operatorname{d}t,\;v=-\cos\left(t\right)\Rightarrow\\I=t^2\sin\left(t\right)-2\left(-t\cos\left(t\right)-\int-\cos\left(t\right)\operatorname{d}t\right)=\\t^2\sin\left(t\right)+2\left(t\cos\left(t\right)-\sin\left(t\right)\right)=\\\left(t^2-2\right)\sin\left(t\right)+2t\cos\left(t\right).\end{array}$

Deshacemos el cambio:

$\begin{array}{l}\left(t^2-2\right)\sin\left(t\right)+2t\cos\left(t\right)\;=\\\left(ArcSin^2\left(x\right)-2\right)x+2ArcSin\left(x\right)\cdot\cos\left(ArcSin\left(x\right)\right)+C.\end{array}$

Se puede simplificar la expresión un poco teniendo en cuenta que $ArcSin(x)$ es, por definición, el ángulo $\theta$ tal que $sin(\theta)=x,$ por tanto:

$\begin{array}{l}\theta=ArcSin\left(x\right)\Leftrightarrow\sin\left(\theta\right)=x\Rightarrow\\\cos\left(ArcSin\left(x\right)\right)=\cos\left(\theta\right).\end{array}$

 Como sabemos que $\sin^2\left(\theta\right)+\cos^2\left(\theta\right)=1\Rightarrow\cos\left(\theta\right)=\sqrt{1-\sin^2\left(\theta\right)},\;$ podemos expresar el resultado así:

$I=\left(ArcSin^2\left(x\right)-2\right)x+2ArcSin\left(x\right)\cdot\sqrt{1-x^2}+C.$

---

**11**. Calcular  $\int\frac{\sin\left(x\right)}{5+2\cos^2\left(x\right)}.$

Como se apunta en el problema 8, las integrales con combinaciones de $sin(x), cos(x), tan(x)$ muchas veces se resuelven con los cambios de variable $t=sin(x), t=cos(x), t=tan(x)$. Probemos $t=cos(x)$ para obtener:

$\begin{array}{l}t=\cos\left(x\right)\Rightarrow\operatorname{d}t=-\sin\left(x\right)\operatorname{d}x\Rightarrow\\\int\frac{\sin\left(x\right)\operatorname{d}x}{5+2\cos^2\left(x\right)}=\int\frac{-\operatorname{d}t}{5+2t^2}\end{array},$

que es una integral del tipo racional tal que el denominador tiene raíces complejas, es del tipo $\int\frac{\operatorname{d}u}{u^2+a^2}=\frac1a\tan^{-1}\left(\frac ua\right)$ (ver el post [Integración de funciones -> funciones racionales](http://tallermatematic.eu/wp/?p=138#racionales)), la "arreglamos":

$\begin{array}{l}\int\frac{-\operatorname{d}t}{5+2t^2}=-\int\frac{\operatorname{d}t}{2\left(t^2+{\displaystyle\frac52}\right)}=-\frac12\int\frac{\operatorname{d}t}{t^2+\left(\sqrt{\displaystyle\frac52}\right)^2}=\\-\frac12\frac1{\sqrt{\frac52}}\tan^{-1}\left(\frac t{\sqrt{\frac52}}\right)=\frac{-1}{\sqrt{10}}\tan^{-1}\left(\frac{\sqrt2t}{\sqrt5}\right).\end{array}$

Deshacemos el cambio de variable:

$I=\frac{-1}{\sqrt{10}}\tan^{-1}\left(\sqrt{\frac25}\cos\left(x\right)\right).$

---
{% endraw %}