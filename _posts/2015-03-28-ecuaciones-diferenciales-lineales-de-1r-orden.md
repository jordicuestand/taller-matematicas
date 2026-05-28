---
layout: post
title: "Ecuaciones diferenciales lineales de 1r orden"
date: 2015-03-28 17:30:38 +0000
categories:
  - "Ecuaciones Diferenciales"
  - "Matemáticas"
tags:
  - "ecuación diferencial lineal homogénea"
  - "ecuación lineal de primer orden"
  - "solución general de la ecuación diferencial ordinaria"
  - "solución particular de la ecuación diferencial ordinaria"
  - "Soluciones singulares"
  - "variación de constantes"
math: true
---
{% raw %}

# Ecuación diferencial lineal de primer orden

Es la que tiene la forma
$y'+X(x)y=F(x)$

donde $X(x)$ y $F(x)$ son funciones cualesquiera que sólo dependen de la variable independiente $x$.

**Ejemplo 1**: Las siguientes ecuaciones de primer orden son lineales

 	- $y'+y·sin(x)=cos(x)$

 	- $2y'-5ye^x+x=0$, pues operando se convierte en $y'+y·(-5/2)e^x = -x$

 	- $x^2y'-e·y+3Ln(x)=0$, pues podemos expresar la ecuación como $y'-\frac e{x^2}\cdot y=-\frac{3Ln(x)}{x^2}$.

En este ejemplo podemos darnos cuenta de que las ecuaciones son lineales en y, no en x. Cuando hay términos no lineales en y, la ecuación deja de ser lineal.

**Ejemplo 2**: Las siguientes ecuaciones de primer orden no son lineales, pues incluyen términos no lineales en la variable y, que no podemos linealizar:

 	- $y'-\frac1{x^2}\cdot y^2=x$

 	- $yy'-y\;=2x\;$

 	- $xy'+e^y\;=2xy\;$

## Solución de la ecuación lineal de primer orden

### Ecuaciones lineales homogéneas

Primero nos fijamos en el caso especial de que $F(x)=0$, denominado **ecuación diferencial lineal homogénea**: $y'+X(x)y=0.$ En este caso, podemos expresarla en la forma de una [ecuación de variables separadas](http://tallermatematic.eu/wp/#separables):

$\begin{array}{l}y'+X(x)y=0\;\Leftrightarrow\frac{\operatorname dy}{\operatorname dx}=-X(x)y\Leftrightarrow\frac{\operatorname dy}y=-X(x)\operatorname dx\Leftrightarrow\\\int\frac{\operatorname dy}y=-\int X(x)\operatorname dx\Leftrightarrow\ln\left(y\right)=-\int X(x)\operatorname dx+C\Leftrightarrow\\\boxed{y=C\cdot exp\left(-\int X(x)\operatorname dx\right)=C\eta\left(x\right)}\end{array}.$

**Ejemplo 3**: La ecuación diferencial lineal homogénea $y'+cos(x)y=0$ tiene por solución $y=C\cdot exp\left(-\int\cos\left(x\right)\operatorname dx\right)=C\cdot exp\left(-\sin\left(x\right)\right).$

**NOTA**: No debemos confundir las ecuaciones lineales homogéneas, $y'+X(x)y=0$, con las denominadas [ecuaciones diferenciales homogéneas](http://tallermatematic.eu/wp/#homogeneas) $y'=F(x,y)$ ni con las funciones homogéneas $F(x,y)$, que son tales que cumplen la propiedad $F\left(\lambda x,\lambda y\right)=\lambda^nF\left(x,y\right).$ No tienen nada que ver en absoluto.

### Soluciones particulares y solución general

Supongamos ahora que tenemos una ecuación lineal $y'+X(x)y=F(x)$ para la que conocemos una solución particular $y_p(x).$ Entonces, si resolvemos la ecuación homogénea asociada $y'+X(x)y=0$, con solución $y_h(x)$, se cumple que la solución general de la ecuación "completa" será $y=Cy_h+y_p$. Es fácil comprobar que es solución sustituyendo en la ecuación completa:

$\begin{array}{l}y=Cy_h+y_p\Rightarrow y'=Cy'_h+y'_p\Rightarrow\\y'+X(x)y=\left(Cy'_h+y'_p\right)+X(x)\cdot\left(Cy_h+y_p\right)=\\Cy'_h+X(x)\cdot Cy_h+y'_p+X(x)\cdot y_p=\\C\left(y'_h+X(x)\cdot y_h\right)+\left(y'_p+X(x)\cdot y_p\right)=C\cdot0+F(x)=F(x).\end{array}$

Por tanto, *en las ecuaciones lineales, si tenemos una solución particular, entonces sabemos hallar la solución general*.

**Ejemplo 4**: La ecuación lineal $y'-3xy=xe^{2x^2}$ tiene la solución particular $y_p=e^{2x^2}$. Obtenemos la solución de la lineal homogénea asociada, $y'-3xy=0$, que es $y_h=C\cdot exp\left(-\int e^{2x^2}\operatorname dx\right)=C\cdot\frac{-1}{4x}e^{2x^2}$. Entonces, la solución general es $y=e^{2x^2}+C\cdot\frac{-1}{4x}e^{2x^2}.$

### Método de variación de constantes

La propiedad anterior con la cual obtenemos la solución general, en la práctica exige el conocimiento de una solución particular de la ecuación, que por lo general no tendremos; no obstante, tenemos un método que puede llevarnos a la obtención de una solución particular conociendo la solución de la ecuación homogénea asociada.

El método de variación de las constantes sustituye la constante C de la solución de la homogénea $y_h=C·\eta(x)$ por una función de x, en principio desconocida: $C(x)$. Se trata entonces de ver si $y=C(x)·\eta(x)$ puede ser una solución particular; para ello, la derivamos y sustituimos en la ecuación lineal completa:

$\begin{array}{l}y=C(x)\cdot\eta(x)\Rightarrow y'=C'(x)\cdot\eta(x)+C(x)\cdot\eta'(x);\\y'+X(x)y=F(x)\Leftrightarrow\left(C'(x)\cdot\eta(x)+C(x)\cdot\eta'(x)\right)+X(x)\left(C(x)\cdot\eta(x)\right)=F(x)\Leftrightarrow\\C(x)\cdot\left(\eta'(x)+X(x)\cdot\eta(x)\right)+C'(x)\cdot\eta(x)=F(x)\\\end{array},$

teniendo en cuenta que $\eta'(x)+X(x)\eta(x)=0$ (basta tomar $C=1$ en la solución de la homogénea $y_h=C·\eta(x)$, nos queda:

$\begin{array}{l}C(x)\cdot\left(\cancel{\eta'(x)+X(x)\cdot\eta(x)}\right)+C'(x)\cdot\eta(x)=F(x)\Leftrightarrow\\C'(x)\cdot\eta(x)=F(x)\Leftrightarrow\frac{\operatorname dC}{\operatorname dx}\eta(x)=F(x)\Leftrightarrow\operatorname dC=\frac{F(x)}{\eta(x)}\operatorname dx\Leftrightarrow\\C(x)=\int\frac{F(x)}{\eta(x)}\operatorname dx\\\\\end{array}.$

Si podemos resolver esta integral, entonces tenemos una solución particular de la ecuación lineal, $y_p=C(x)·\eta(x)$, que es:

$\begin{array}{l}y_p=C(x)\cdot\eta(x)=\int\frac{F(x)}{\eta(x)}\operatorname dx\cdot\eta(x)=e^{-\int X\left(x\right)\operatorname dx}\cdot\int\frac{F(x)}{\eta(x)}\operatorname dx\Leftrightarrow\\\\\boxed{y_p=e^{-\int X\left(x\right)\operatorname dx}\cdot\int F(x)\cdot e^{\int X\left(x\right)\operatorname dx}\operatorname dx.}\end{array}$

Ahora también podemos dar la expresión general de la solución completa, obtenida por el método de variación de las constantes:

$\begin{array}{l}\begin{array}{l}y=Cy_h+y_p=\\C\cdot e^{-\int X\left(x\right)\operatorname dx}+e^{-\int X\left(x\right)\operatorname dx}\cdot\int F(x)\cdot e^{\int X\left(x\right)\operatorname dx}\operatorname dx\Rightarrow\\\boxed{y=e^{-\int X\left(x\right)\operatorname dx}\cdot\left$C+\int F(x)\cdot e^{\int X\left(x\right)\operatorname dx}\operatorname dx\right$}.\end{array}\\\end{array}$

Se puede simplificar un poco esta expresión usando la función solución de la ecuación homogénea $\eta\left(x\right)$, queda:

$\boxed{y(x)=\eta\left(x\right)\cdot\left$C+\int F(x)\cdot\eta^{-1}\left(x\right)\operatorname dx\right$}$

Por tanto, en el caso de las ecuaciones lineales de primer orden, *tenemos una fórmula que las reduce al cálculo de dos integrales*.  El método de variación de constantes es general: veremos que se puede aplicar a otras ecuaciones diferenciales.

**Ejemplo 5**: En un circuito eléctrico que contiene una resistencia R y una [inductancia](http://es.wikipedia.org/wiki/Inductancia) L (abreviadamente, [circuito RL](http://es.wikipedia.org/wiki/Circuito_RL)) la intensidad de corriente generada al aplicar una tensión V viene dada por la ecuación

$RI(t)=V(t)-LI'(t)$

 que es una ecuación diferencial lineal en la variable $I(t)$, pues:

$RI(t)=V(t)-LI'(t)\Leftrightarrow I'(t)+\frac RLI(t)=V(t)$

Si la tensión es constante, $V(t)=V$, y la ecuación es $I'(t)+\frac RLI(t)=V.$ La ecuación homogénea asociada es $I'(t)+\frac RLI(t)=0$ que es de variables separables:

$\begin{array}{l}\frac{\operatorname dI}{\operatorname dt}=-\frac RLI(t)\Leftrightarrow\frac{\operatorname dI}{I(t)}=-\frac RL\operatorname dt\Leftrightarrow\int\frac{\operatorname dI}{I(t)}=-\int\frac RL\operatorname dt\Leftrightarrow\\\ln\left(I(t)\right)=-\frac RLt+C\Leftrightarrow I(t)=C\cdot exp\left(-\frac RLt\right)=C\eta\left(t\right)\end{array}$

La solución general viene dada por

$\begin{array}{l}I(t)=\eta\left(t\right)\cdot\left$C+\int X(t)\cdot\eta^{-1}\left(t\right)\operatorname dt\right$;\\\int X(t)\cdot\eta^{-1}\left(t\right)\operatorname dt=\int\frac VL\cdot e^{\frac RLt}\operatorname dt=\frac VL\cdot\frac LRe^{\frac RLt}=\frac VRe^{\frac RLt};\\I(t)=e^{-\frac RLt}\cdot\left$C+\frac VRe^{\frac RLt}\right$=\boxed{Ce^{-\frac RLt}+\frac VR}.\\\end{array}$

En la práctica se asume
que para $t=0$ ha de ser $I(0)=0$, por tanto $I(0)=C+\frac VR=0\Rightarrow C=-\frac VR$ y la expresión de la intensidad queda así:

$I(t)=-\frac VRe^{-\frac RLt}+\frac VR=\frac VR\left$1-e^{-\frac RLt}\right$$

El término $-e^{-\frac RLt}$ vale 1 para t = 0 y se atenúa ràpidamente, pasando a ser prácticamente nulo: es el denominado régimen transitorio del circuito; después, solo queda el término constante $I(t) = V/R$ ([Ley de Ohm](http://es.wikipedia.org/wiki/Ley_de_Ohm)): es el régimen estacionario:

![Intensidad I(t) en un circuito RL](/taller-matematicas/assets/images/circuit-RL.png) Intensidad I(t) en un circuito RL
###  Unicidad de la solución

El teorema siguiente nos asegura que, en ciertas condiciones, la solución de una ecuación diferencial lineal de primer orden es única, o equivalentemente, que no existen [soluciones singulares](http://tallermatematic.eu/wp/?p=855#singulares), toda posible solución está incluida en la solución general.

***Teorema 1**: Unicidad de la solución de la ecuación diferencial lineal de primer orden.*

*Dada la ecuación $y'+X(x)y=F(x)$, si las funciones $X(x)$ y $F(x)$ son continuas en un entorno abierto I que contiene a $x_0$, entonces el problema de valor inicial*

*$y'+X(x)y=F(x), y(x_0)=y_0$,*

*tiene una única solución (la que hemos obtenido, dando un valor adecuado a la constante C).*

#
{% endraw %}