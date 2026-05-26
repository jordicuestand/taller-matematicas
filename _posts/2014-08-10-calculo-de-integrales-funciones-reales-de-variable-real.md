---
layout: post
title: "Càlculo de integrales (funciones reales de variable real)"
date: 2014-08-10 08:41:49 +0000
categories:
  - "Cálculo en R"
  - "Funciones reales de variable real"
  - "Integración"
  - "Matemáticas"
tags:
  - "integración cambio de variable"
  - "Integración de funciones racionales"
  - "integración por descomposición en fracciones simples"
  - "integración por partes"
  - "Integrales casi inmediatas"
  - "integrales inmediatas"
  - "teorema fundamental del cálculo"
math: true
---
{% raw %}

Este es un post eminentemente práctico: se dan métodos de obtención de la función primitiva $F(x)$ de una función real de variable real $f(x)$ dada, simbólicamente:
$F(x)=\int f(x)\operatorname{d}x$

 	- [Integrales inmediatas](#inmediatas)

 	- [Integrales casi inmediatas](#casi)

 	- [Integración por partes](#partes)

 	- [Integración por cambio de variable](#cambio)

 	- [Integración de funciones racionales](#racionales)

---

 
# Integrales inmediatas

Tiene este nombre debido a que son las más sencillas de calcular, se trata de aplicar algunas fórmulas que solo tienen validez para funciones continuas. En Internet y en la bibliografía se encuentran muchas tablas de integrales inmediatas, a continuación presentamos la que vamos a utilizar aquí:

### Tabla de integrales inmediatas

En esta tabla, $a$ es un número real cualquiera, $u(x)$ una función derivable cualquiera, y $du$ su diferencial.

 	- $\int a\operatorname{d}x=ax$

 	- $\int af(x)\operatorname{d}x=a\int f(x)\operatorname{d}x$

 	- $\int u^n(x)\operatorname{d}u=\frac{u^{n+1}(x)}{n+1}$, siendo $n$ un número real cualquiera diferente de -1

 	- $\int\frac{\operatorname{d}u}u=\ln\left|u\right|$, siendo $u(x)$ una función derivable cualquiera distinta de cero, $du$ su diferencial

 	- $\int e^udu=e^u$,

 	- $\int a^udu=\frac{a^u}{\ln\left(a\right)}$, siendo $a$ un real positivo distinto de 1.

 	- $\int\sin\left(u\right)du=-\cos\left(u\right)$

 	- $\int\cos\left(u\right)du=\sin\left(u\right)$

 	- $\int\tan\left(u\right)du=-\ln\left|\cos\left(u\right)\right|$

 	- $\int\cot\left(u\right)du=\int\frac{du}{\tan\left(\right)}=\ln\left|\sec\left(u\right)\right|$

 	- $\int\sec\left(u\right)du=\int\frac{du}{\cos\left(u\right)}=\ln\left|\sec\left(u\right)+\tan\left(u\right)\right|$

 	- $\int\csc\left(u\right)du=\int\frac{du}{\sin\left(u\right)}=\ln\lef$

 	- $\int\frac{du}{u^2+a^2}=\frac1a\tan^{-1}\left(\frac ua\right)$, siendo $a$ distinto de cero

 	- $\int\frac{du}{u^2-a^2}=\frac1{2a}\ln\left|\frac{u-a}{u+a}\right|$, siempre que $u+a$ no valga $0$.

 	- $\int\frac{du}{a^2-u^2}=\frac1{2a}\ln\left|\frac{a+u}{a-u}\right|$ siempre que $a-u$ no valga $0$.

 	- $\int\frac{du}{\sqrt{a^2-u^2}}=\sin^{-1}\left(\frac ua\right)$, siendo $a$ distinto de cero

 	- $\int\frac{du}{\sqrt{a^2+u^2}}=\ln\left|u+\sqrt{u^2+a^2}\right|$

 	- $\int\frac{du}{\sqrt{u^2-a^2}}=\ln\left|u+\sqrt{u^2-a^2}\right|$, siempre que $u^2-a^2\geq0$

 	- $\int\frac{du}{u\sqrt{u^2-a^2}}=\frac1a\sec^{-1}\left|\frac ua\right|$ siempre que $u^2-a^2\geq0$ y $a$ no sea cero.

 	- $\int\frac{du}{u\sqrt{u^2+a^2}}=\frac{-1}a\ln\left|\frac{a+\sqrt{u^2+a^2}}u\right|$, siempre que $u$ y $a$ no sean cero.

 	- $\int\frac{du}{u\sqrt{a^2-u^2}}=\frac{-1}a\ln\left|\frac{a+\sqrt{a^2-u^2}}u\right|$,  siempre que $u$ y $a$ no sean cero.

**Nota**: Al calcular la primitiva $F(x)$ de una función $f(x)$, también llamada integral indefinida, se suele añadir al resultado una constante (un número real), que suele denominarse $C$. Esto es una consecuencia del [teorema fundamental del cálculo](http://es.wikipedia.org/wiki/Teorema_fundamental_del_c%C3%A1lculo), según el cual existe no una única función primitiva, sino infinitas, tantas como valores puede tomar la constante $C$. Entonces todas la primitivas de la tabla anterior pueden expresarse con la $C$ añadida. Por ejemplo la primera de la lista: $\int a\operatorname{d}x=ax+C$

 **Ejemplo 1**: $\int3x^2\operatorname{d}x=3\int x^2\operatorname{d}x=3\frac{x^3}3+C=x^3+C$. Hemos aplicado las fórmulas (1) y (3) de la tabla.

**Ejemplo 2**: $\int\sqrt[3]x\operatorname{d}x=\int x^\frac13\operatorname{d}x=\frac{x^{\frac13+1}}{\frac13+1}+C=\frac34\sqrt[3]{x^4}+C$. Hemos aplicado la fórmula (3) de la tabla.
**NOTA**: la diferencial de una función, a efectos prácticos, podemos asimilarla a la derivada de la función, añadiendo el $\operatorname{d}x$, como vemos en el siguiente ejemplo:

**Ejemplo 3**: $\int\frac{-2\sin\left(x\right)}{\cos\left(2x\right)}\operatorname{d}x=\int\frac{\operatorname{d}u}u=\ln\left|u\right|+C=\ln\left|\cos\left(2x\right)\right|+C$, ya que la derivada del denominador es igual al numerador $\operatorname{d}\left(\cos\left(2x\right)\right)=-2\sin\left(2x\right)\operatorname{d}x$.

# Integrales casi inmediatas

Son aquellas que mediante transformaciones algebraicas sencillas pueden expresarse en la forma de una de las integrales inmediatas.

**Ejemplo 4:**

$\int5\sin\left(x\right)\cos^2\left(x\right)\operatorname{d}x=5\int\left(\cos\left(x\right)\right)^2\sin\left(x\right)\operatorname{d}x=5\int\left(-\cos\left(x\right)\right)^2\operatorname{d}\left(-\cos\left(x\right)\right)=5\frac{-\left(\cos\left(x\right)\right)^3}3+C$. Hemos aplicado la fórmula (3), teniendo en cuenta que la derivada de $cos(x)$ es $-sin(x)$, hemos tenido que añadir el signo menos para que sea aplicable.

**Ejemplo 5:**

$\int e^x\frac{e^{2x}+5}{\sqrt{e^{2x}+4}}\operatorname{d}x=\int\left[\frac{e^x\left(e^{2x}+4\right)}{\sqrt{e^{2x}+4}}+\frac{e^x}{\sqrt{e^{2x}+4}}\right]\operatorname{d}x=\int e^x\sqrt{e^{2x}+4}\operatorname{d}x+\int\frac{e^x}{\sqrt{e^{2x}+4}}\operatorname{d}x.$

La primera integral es del tipo (3):

$=\int e^x\sqrt{e^{2x}+4}\operatorname{d}x=\int e^x\left(e^{2x}+4\right)^\frac12\operatorname{d}x=\frac12\int2e^x\left(e^{2x}+4\right)^\frac12\operatorname{d}x=\frac12\int\left(e^{2x}+4\right)^\frac12\operatorname{d}\left(e^{2x}+4\right)=\frac12\frac{\left(e^{2x}+4\right)^\frac32}{\displaystyle\frac32}=\frac{\sqrt[{}]{\left(e^{2x}+4\right)^3}}3.$

La segunda integral es del tipo (7):

$=\int\frac{e^x}{\sqrt{e^{2x}+4}}\operatorname{d}x=\int\frac{e^x}{\sqrt{\left(e^x\right)^2+4}}\operatorname{d}x=\int\frac{\operatorname{d}\left(e^x\right)}{\sqrt{e^{2x}+4}}=\ln\left|e^x+\sqrt{e^{2x}+4}\right|.$

Resultado: $\int e^x\frac{e^{2x}+5}{\sqrt{e^{2x}+4}}\operatorname{d}x==\frac{\sqrt[{}]{\left(e^{2x}+4\right)^3}}3+\ln\left|e^x+\sqrt{e^{2x}+4}\right|+C.$
# Integración por partes

**Teorema**: Sean $u(x)$, $v(x)$ dos funciones derivables con derivada continua. Entonces se cumple que

$\int u(x)\operatorname{d}v(x)=u(x)\cdot v(x)-\int v(x)\operatorname{d}u(x)$

La aplicación práctica consiste en, dado un problema de integración $I=\int f(x)\operatorname{d}x$ que no es inmediato y en el cual la función a integrar sea el producto de otras funciones, identificar a qué llamaremos $u(x)$ y a qué llamaremos $\operatorname{d}v(x)$, de esa forma la integral original se divide en dos partes: hallar $v(x)$ integrando $\operatorname{d}v(x)$, y a continuación hallar $\int v(x)\operatorname{d}u(x)$.

**Ejemplo 6**:

 $I=\int e^x\sin\left(x\right)\operatorname{d}x=\int u(x)\operatorname{d}v(x)$, donde $u(x)=e^x,\;\operatorname{d}v(x)=\sin\left(x\right)\operatorname{d}x.$

Primera parte, hallar $v(x)=\int\sin\left(x\right)\operatorname{d}x=-\cos\left(x\right)$.

Segunda parte,  calcular $\int v(x)\operatorname{d}u(x)=\int-\cos\left(x\right)\operatorname{d}\left(e^x\right)=-\int\cos\left(x\right)e^x\operatorname{d}x.$

De momento tenemos:

 $I=u(x)\cdot v(x)-\int v(x)\operatorname{d}u(x)=-e^x\cos\left(x\right)-\int-\cos\left(x\right)e^x\operatorname{d}x.$

La segunda integral es parecida a la original, cambiando la función seno por la función coseno. Aplicamos de nuevo el mètodo de integración por partes a esta segunda integral, que llamamos $I_2$:

$I_2=\int\cos\left(x\right)e^x\operatorname{d}x.\;u(x)=e^x,\;\operatorname{d}v(x)=\cos\left(x\right)\operatorname{d}x,\;\operatorname{d}u(x)=e^x\operatorname{d}x,\;v(x)=\int\cos\left(x\right)\operatorname{d}x=\sin\left(x\right).$

Aplicamos el teorema de integración por partes a la integral $I_2$:

$I_2=e^x\sin\left(x\right)-\int\sin\left(x\right)e^x\operatorname{d}x=e^x\sin\left(x\right)-I.$

Hemos recuperado la integral original $I$. Ordenando todo lo que tenemos:

$\begin{array}{l}I=-e^x\cos\left(x\right)+\;I_2=-e^x\cos\left(x\right)+e^x\sin\left(x\right)-I\Leftrightarrow\\2I=-e^x\cos\left(x\right)+e^x\sin\left(x\right)\Leftrightarrow\\I=\frac12e^x\left(\sin\left(x\right)-\cos\left(x\right)\right)+C.\end{array}$.

**Ejemplo 7**:

$\begin{array}{l}I=\int x\cos\left(x\right)\operatorname{d}x;\;\\u(x)=x,\;\operatorname{d}u(x)=1\cdot dx;\;\operatorname{d}v(x)=\cos\left(x\right)\operatorname{d}x,\;v(x)=\int\cos\left(x\right)\operatorname{d}x=\sin\left(x\right).\\I=x\sin\left(x\right)-\int1\cdot\sin\left(x\right)\operatorname{d}x=x\sin\left(x\right)-\left(-\cos\left(x\right)\right)+C=x\sin\left(x\right)+\cos\left(x\right)+C.\end{array}$
# Integración por cambio de variable

En ocasiones al integrar $I=\int f\left(x\right)\operatorname{d}x$ podemos darnos cuenta de que si hiciéramos un cambio de variable $x=g(t)$ la integral con la nueva variable $t$ es más sencilla. Hay que tener en cuenta que el cambio también afecta a la diferencial de x:

$I=\int f\left(x\right)\operatorname{d}x=\int f\left(g\left(t\right)\right)\operatorname{d}\left(g\left(t\right)\right).$

**Ejemplo 8**:

La integral $I=\int\frac1{\sqrt{1-x^2}}\operatorname{d}x$ no es inmediata. Recordando la identidad trigonométrica $sin^2\left(x\right)+\cos^2\left(x\right)=1\Leftrightarrow1-\;\sin^2\left(x\right)=\cos^2\left(x\right)$ vemos que si en vez de la $x^2$ tuviéramos un $sin^2\left(x\right)$ podríamos anular la raíz con el $x=\cos^2\left(t\right)$. Intentamos pues el cambio de variable $x=\sin\left(t\right)$:

$\begin{array}{l}x=\sin\left(t\right)\Rightarrow\\I=\int\frac1{\sqrt{1-\left(\sin\left(t\right)\right)^2}}\operatorname{d}\left(\sin\left(t\right)\right)=\\\int\frac1{\cos\left(t\right)}\cos\left(t\right)\operatorname{d}t=\int\operatorname{d}t=t+C.\end{array}$

Deshaciendo el cambio: $x=\sin\left(t\right)\Rightarrow t=\sin^{-1}\left(x\right)\Rightarrow I=\sin^{-1}\left(x\right)+C.$

**Ejemplo 9**:

$\begin{array}{l}I=\int e^x\sin\left(e^x\right)\operatorname{d}x.\;\\e^x=t\Rightarrow x=\ln\left(\left|t\right|\right)\Rightarrow\operatorname{d}x=\frac1t\operatorname{d}t.\\I=\int t\sin\left(t\right)\frac1t\operatorname{d}t=\int\sin\left(t\right)\operatorname{d}t=-\cos\left(t\right)+C=-\cos\left(e^x\right)+C.\end{array}.$

**Ejemplo 10**:

$\begin{array}{l}I=\int x^3\cos\left(x^4\right)\operatorname{d}x.\\t=x^4;\;\operatorname{d}t=4x^3\operatorname{d}x.\\I=\frac14\int\cos\left(x^4\right)4x^3\operatorname{d}x=\frac14\int\cos\left(t\right)\operatorname{d}t=\frac14\sin\left(t\right)+C=\frac14\sin\left(x^4\right)+C.\end{array}.$

# Integración de funciones racionales

Para las integrales de la forma "cociente de polinomios", $\int\frac{P\left(x\right)}{Q\left(x\right)}\operatorname{d}x$ tendremos en cuenta lo siguiente:

 	- Si el grado $n$ del numerador es superior al grado $m$ del denominador, dividimos para obtener $\frac{P\left(x\right)}{Q\left(x\right)}=D\left(x\right)+\frac{R\left(x\right)}{Q\left(x\right)}$, donde $D$ es un polinomio de grado $n-m$ y el polinomio $R$ es el resto de la división, con grado $r$ menor que $m$. Entonces: $\int\frac{P\left(x\right)}{Q\left(x\right)}=\int D\left(x\right)+\int\frac{R\left(x\right)}{Q\left(x\right)}$, la integral de un polinomio (inmediata) y otra integral racional con grado del numerador inferior al grado del denominador.

 	- Si el grado $n$ del numerador es inferior al grado $m$ del denominador, descomponemos la fracción racional según el siguiente Teorema:

**Teorema**: todo polinomio $P(x)$ con coeficientes reales admite una descomposición en producto de factores de dos tipos:

 	- $\left(x-a\right)^p$, donde $a$ es una[ raíz del polinomio](http://es.wikipedia.org/wiki/Ra%C3%ADz_de_una_funci%C3%B3n) $P(x)$

 	- $\left(\alpha x^2+\beta x+\gamma\right)^n$, un polinomio de grado 2 con raíces complejas.

La dificultad práctica en la aplicación de este teorema reside en cómo hallar las raíces (equivalentemente, los ceros) del polinomio. En casos simples puede aplicarse la regla de Ruffini (para raíces enteras) pero en general para polinomios de grado superior a cuatro se necesitan métodos numéricos aproximados. En todo caso, el mètodo de integración es el siguiente:

### Método de integración por descomposición en fracciones simples (Bernoulli, 1702)

Sea la integral $\int\frac{P\left(x\right)} Q\left(x\right)}\operatorname{d}x$ donde $P$ y $Q$ son polinomios tales que el grado $n$ del numerador es inferior al grado $m$ del denominador.

**1r paso)** Resolver la ecuación $Q(x)=0$, calculando todas las raíces tanto reales como complejas (polinomios de grado 2 sin raíces reales). Por el teorema de descomposición, podremos escribir:

$Q(x)=\left(x-a\right)^{m_1}\left(x-b\right)^{m_2}\dots\left(\alpha_1x^2+\beta_1x+\gamma_1\right)^{n_1}\left(\alpha_2x^2+\beta_2x+\gamma_2\right)^{n_2}\dots.$

**2n paso) **Para cada factor de la forma $\left(x-a\right)^{m}$ tendremos una suma de $m$ fracciones

$\frac{A_1}{\left(x-a\right)^1}+\frac{A_2}{\left(x-a\right)^2}+\dots+\frac{A_m}{\left(x-a\right)^m},$

y para cada factor $\left(\alpha_1x^2+\beta_1x+\gamma_1\right)^{n}$ tendremos una suma de $n$ fracciones

$\frac{B_1x+C_1}{\left(\alpha_{}x^2+\beta_{}x+\gamma_{}\right)}+\frac{B_2x+C_2}{\left(\alpha_{}x^2+\beta_{}x+\gamma_{}\right)^2}+\dots+\frac{B_nx+C_n}{\left(\alpha_{}x^2+\beta_{}x+\gamma_{}\right)^n}.$

Determinamos todos los coeficientes indeterminados $A_1, A_2, \dots, A_m, B_1, \dots, B_n, C_1, \dots, C_n$ igualando la suma de todas las fracciones generadas a $\frac{P\left(x\right)} Q\left(x\right)}$, que nos proporciona un sistema de ecuaciones.

**3r paso)** La integral nos ha quedado en la forma:

$\int\frac{P(x)}{Q(x)}=\int\frac{A_1}{\left(x-a\right)}+\int\frac{A_2}{\left(x-a\right)^2}+\cdots+\int\frac{A_m}{\left(x-a\right)^m}+\int\frac{B_1x+C_1}{\left(\alpha_{}x^2+\beta_{}x+\gamma_{}\right)}+\int\frac{B_2x+C_2}{\left(\alpha_{}x^2+\beta_{}x+\gamma_{}\right)^2}+\dots+\int\frac{B_nx+C_n}{\left(\alpha_{}x^2+\beta_{}x+\gamma_{}\right)^n}.$

Casi todas estas integrales son inmediatas:

$\begin{array}{l}\int\frac{A_1}{\left(x-a\right)}=A_1\ln\left(x-a\right)\\\int\frac{A_2}{\left(x-a\right)^2}=\frac{A_2}{\left(x-a\right)}\\\int\frac{A_m}{\left(x-a\right)^m}=\frac{A_m}{\left(1-m\right)\left(x-a\right)^{m-1}}\\\int\frac{B_1x+C_1}{\left(\alpha_{}x^2+\beta_{}x+\gamma_{}\right)}=\int\frac{B_1x}{\left(\alpha_{}x^2+\beta_{}x+\gamma_{}\right)}+\int\frac{C_1}{\left(\alpha_{}x^2+\beta_{}x+\gamma_{}\right)}\end{array}.$

Las dos últimas integrales son inmediata del tipo (4) y casi inmediata del tipo (13), respectivamente.

Las integrales con raíces complejas múltiples del tipo $\int\frac{B_{}x+C_{}}{\left(\alpha_{}x^2+\beta_{}x+\gamma_{}\right)^n}$ no son inmediatas, pueden resolverse por partes, reduciendo progresivamente el orden del exponente.

**Ejemplo 11: **$\int\frac1{x^2-5x+6}.$

**1)** Resolvemos $x^2-5x+6=0$

$x^2-5x+6=0\Rightarrow x=\frac{5\pm\sqrt{25-24}}2=\left\{\begin{array}{l}3\\2\end{array}\right.$

**2)** Descomponemos la fracción original:

$\begin{array}{l}\begin{array}{l}x^2-5x+6=\left(x-3\right)\left(x-2\right)\Leftrightarrow\\\frac1{x^2-5x+6}=\frac{A_1}{x-3}+\frac{A_2}{x-2}\Leftrightarrow\end{array}\\\frac1{x^2-5x+6}=\frac{A_1\left(x-2\right)+A_2\left(x-3\right)}{\left(x-3\right)\left(x-2\right)}\Rightarrow\\A_1\left(x-2\right)+A_2\left(x-3\right)=1.\\\end{array}$

Todas las raíces son reales y simples. Para hallar los coeficientes hay varios métodos. Uno de ellos, de aplicación aquí, es útil cuando todas las raíces son reales simples, y consiste en sustituir en la expresión anterior la variable $x$ por los valores de las raíces:

$\begin{array}{l}x=2\Rightarrow A_1\left(2-2\right)+A_2\left(2-3\right)=1\Leftrightarrow-A_2=1\Leftrightarrow A_2=1.\\x=3\Rightarrow A_1\left(3-2\right)+A_2\left(3-3\right)=1\Leftrightarrow A_1=1.\\\end{array}$

**3)** Usamos la tabla de integrales inmediatas:

$\begin{array}{l}\int\frac1{x-3}=\ln\left(x-3\right),\;\int\frac{-1}{x-3}=-\ln\left(x-2\right)\Rightarrow\\\int\frac1{x^2-5x+6}=\ln\left(x-3\right)-\ln\left(x-2\right)+C.\end{array}$

**Ejemplo 12**: $\int\frac{x-1}{x\left(x^2+1\right)}.$

**1)** En el denominador una raíz es evidente que es $x=0$. El factor $x^2+1$ es irreducible (no tiene raíces reales).

**2)** Descomponemos la fracción:

$\begin{array}{l}\int\frac{x-1}{x\left(x^2+1\right)}=\int\frac Ax+\int\frac{Bx+C}{x^2+1}\Leftrightarrow\\\frac{x-1}{x\left(x^2+1\right)}=\frac{A\left(x^2+1\right)+\left(Bx+C\right)x}{x\left(x^2+1\right)}\Leftrightarrow\\x-1=A\left(x^2+1\right)+\left(Bx+C\right)x.\end{array}.$

Para el valor $x=0$:

$x=0\Leftrightarrow0-1=A\left(0^2+1\right)+\left(B0+C\right)0\Leftrightarrow-1=A.$

Para los otros dos valores indeterminados, operamos como sigue:

$\begin{array}{l}x-1=-\left(x^2+1\right)+\left(Bx+C\right)x\Leftrightarrow\\x-1=-x^2-1+Bx^2+Cx\Leftrightarrow\\x-1=x^2\left(B-1\right)+Cx-1.\\\end{array}.$

Comparando los polinomios a ambos lados de la igualdad concluimos que:

$\begin{array}{l}\left\{\begin{array}{l}B-1=0\Rightarrow B=1\\C=1\end{array}\right.\\\end{array}.$

**3)** Integramos, tenemos dos inmediatas y una casi inmediata:

$\begin{array}{l}I=\int\frac{-1}x+\int\frac{x+1}{x^2+1}=-\ln\left(x\right)+\int\frac1{x^2+1}+\int\frac x{x^2+1}=\\-\ln\left(x\right)+\tan^{-1}\left(x\right)+\frac12\int\frac{2x}{x^2+1}=\\-\ln\left(x\right)+\tan^{-1}\left(x\right)+\frac12\ln\left(x^2+1\right).\\\end{array}.$
{% endraw %}