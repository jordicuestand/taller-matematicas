---
layout: post
title: "Problemas de EDOs de primer orden"
date: 2015-04-28 13:07:16 +0000
math: true
---
{% raw %}

**Enunciados**

**1.** Resolver la ecuación lineal de primer orden $y'x+y=x\sin(x)$.

**2.** Resolver la ecuación de Bernouilli $y'+\frac yx=y^2\frac{x\cos\left(x\right)-\sin\left(x\right)}x$

**3.**  Integrar la ecuación de Lagrange $y=-x+\frac{1-y'}{1+y'}$.

**4. **Integrar la ecuación diferencial exacta $\left(2x+\frac1y\right)\operatorname dx+\left(\frac1y-\frac x{y^2}\right)\operatorname dy=0.$

 
**Soluciones**

![separador2](/taller-matematicas/assets/images/separador2.png)

 

 

**1.** Resolver la ecuación lineal de primer orden $y'x+y=x\sin(x)$.

**Solución**: Ponemos la ecuación en la forma estándard $y'+P(x)y=Q(x)$, dividiendo todo por x: $y'+(1/x)y=\sin(x)$, identificamos $P(x)=1/x, Q(x)=\sin(x)$. Calculamos $u=exp(-\int e^{P(x)}\operatorname dx), \;v=\int Q(x)\cdot\left$\int e^{P(x)}\operatorname dx\right$\operatorname dx$ y la solución será $y=u(C+v)$:

$\begin{array}{l}u=e^{\int-\frac1x\operatorname dx}=e^{-\ln\left(x\right)}=\frac1x;\;\\v=\int\sin\left(x\right)\left$e^{\int\frac1x\operatorname dx}\right$\operatorname dx=\int\sin\left(x\right)\cdot x\operatorname dx=\sin\left(x\right)-x\cos\left(x\right)\end{array}$

la última integral se puede hacer por partes. La integral general queda:

$y=u\left(C+v\right)=\frac1x\left(C+\sin\left(x\right)-x\cos\left(x\right)\right).$

![separador2](/taller-matematicas/assets/images/separador2.png)

 

 

**2.** Resolver la ecuación de Bernouilli $y'+\frac yx=y^2\frac{x\cos\left(x\right)-\sin\left(x\right)}x$

**Solución**: Con el cambio $y=1/u$ se transforma en una ecuación lineal:

$v'-\frac1xv=-\frac{x\cos\left(x\right)-\sin\left(x\right)}x$

Para resolver la ecuación lineal, que es del tipo $y'+P(x)y=Q(x)$, hallamos $v=-\int e^{P(x)}\operatorname dx,\;w=\int Q(x)\cdot\left$\int e^{P(x)}\operatorname dx\right$\operatorname dx$ y la solución será $y=v(C+w)$; obtendremos: $u=Cx-\sin(x)$, deshaciendo el cambio, $y=(Cx-\sin(x))^{-1}$.

![separador2](/taller-matematicas/assets/images/separador2.png)

 

 

**3.**  Integrar la ecuación de Lagrange $y=-x+\frac{1-y'}{1+y'}$.

**Solución**: Las ecuaciones de Lagrange por lo general no pueden resolverse de forma explícita, esto es, dando una expresión $y=f(x)$, si no que ha darse en forma paramétrica: $x=f(p), y=g(p)$. El procedimiento es como sigue:

1. Hacemos el cambio $y'=p$, resulta: $y=-x+\frac{1-p}{1+p}=F(x)+G(p)$

2. Derivamos toda la ecuación respecto de x, teniendo en cuenta que $\frac{\operatorname d{G(p)}}{\operatorname dx}=\frac{\operatorname d{G(p)}}{\operatorname dp}\frac{\operatorname dp}{\operatorname dx}$, resulta: $p=-1+\frac{-1\left(1+p\right)-\left(1-p\right)1}{\left(1+p\right)^2}\frac{dp}{dx}$

 

3. Reordenamos, considerando x como función de p, obtenemos una ecuación lineal en x(p), que en este caso es además separable, que podemos resolver:

$y=-x+\frac{1-p}{1+p}=F(x)+G(p)$

4. Sustituyendo esta expresión de x en la ecuación original, cambiando y' por p, obtenemos la y en función del parámetro p:

$\begin{array}{l}y=-x+\frac{1-p}{1+p}=\frac{-1}{\left(1+p\right)^2}-C+\frac{1-p}{1+p}=-C+\frac{-1+\left(1-p\right)\left(1+p\right)}{\left(1+p\right)^2}=\\-C-\frac{p^2}{\left(1+p\right)^2}\\\\\end{array}$

El conjunto de la dos igualdades para x, y nos da el haz de curvas solución en función del parámetro p=y', que es la pendiente de la curva:

$\left.\begin{array}{r}x=\frac1{\left(1+p\right)^2}+C\\y=-C-\frac{p^2}{\left(1+p\right)^2}\end{array}\right\}$

![separador2](/taller-matematicas/assets/images/separador2.png)

 

 

**4. **Integrar la ecuación diferencial exacta $\left(2x+\frac1y\right)\operatorname dx+\left(\frac1y-\frac x{y^2}\right)\operatorname dy=0.$

**Solución**: Comprobamos que es exacta: la ecuación $M\left(x,y\right)\operatorname dx+N\left(x,y\right)\operatorname dy=0$ es exacta cuando $\frac{\partial M}{\partial y}=\frac{\partial N}{\partial x}$, en efecto:

$\begin{array}{l}\frac{\partial M}{\partial y}=\frac{\partial\left(2x+\frac1y\right)}{\partial y}=-\frac1{y^2};\\\frac{\partial N}{\partial x}=\frac{\partial\left(\frac1y-\frac x{y^2}\right)}{\partial x}=-\frac1{y^2};\end{array}$

Integramos los dos miembros de la ecuación, respecto a x o a y:

$\begin{array}{l}\int\left(2x+\frac1y\right)\operatorname dx=x^2+\frac xy+C\left(y\right);\\\int\left(\frac1y-\frac x{y^2}\right)\operatorname dy=\ln\left(y\right)+\frac xy+C\left(x\right);\end{array}$

Igualamos ambos resultados:

$\begin{array}{l}x^2+\frac xy+C\left(y\right)=\ln\left(y\right)+\frac xy+C\left(x\right)\Leftrightarrow\left\{\begin{array}{l}C\left(x\right)=x^2\\C\left(y\right)=\ln\left(y\right)\end{array}\right.\\\end{array}$

La solución es $F(x,y)=C$ donde $F\left(x,y\right)=\int M\operatorname dx=\int N\operatorname dy=x^2+\frac xy+\ln\left(y\right)$, o sea, queda en forma implícita, no damos una expresión $y=f(x)$, sino:
$x^2+\frac xy+\ln\left(y\right)=C$

![separador2](/taller-matematicas/assets/images/separador2.png)
{% endraw %}