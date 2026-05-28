---
layout: post
title: "Ecuaciones diferenciales ordinarias: introducción"
date: 2015-02-12 13:12:12 +0000
categories:
  - "Ecuaciones Diferenciales"
  - "Matemáticas"
tags:
  - "ecuación diferencial"
  - "ecuación diferencial ordinaria"
  - "ecuación diferencial del haz de curvas"
  - "existencia y unicidad"
  - "haz de curvas planas"
  - "solución general de la ecuación diferencial ordinaria"
  - "solución particular de la ecuación diferencial ordinaria"
math: true
---
{% raw %}

## Motivación

Las ecuaciones que se estudian en el Álgebra, tales como $x^{3}+7x^{2}+41=0$,
expresan relaciones numéricas estáticas, y su solución son números que cumplen la ecuación. Ahora bien, los fenómenos naturales más interesantes implican relaciones dinámicas y se expresan mejor con relaciones entre cantidades variables, esto es, con ecuaciones que no son estáticas, sino que expresan variaciones y relaciones entre magnitudes cambiantes: son las ecuaciones diferenciales.

Recordemos que la derivada de una función $dy/dt=f'(t)$ se puede interpretar como la proporción de cambio de la variable dependiente $y$ respecto a los cambios en la variable dependiente $t$. Es por ello las ecuaciones que describen cambios utilizan derivadas de funciones.

***Definición 1**: una ecuación que contiene una función desconocida y una o más de una de sus derivadas se llama **ecuación diferencial**. Al resolverla, obtenemos funciones $y = f (x)$ que verifican la ecuación. Si la función sólo tiene una variable independiente, la ecuación se llama **ecuación diferencial ordinaria**. Si la función depende de dos o más variables, las derivadas serán parciales y la ecuación se llama **ecuación en derivadas parciales**. El orden de una ecuación diferencial es el de la derivada más alta que aparece en la ecuación*.

En este post sólo introduciremos las ecuaciones diferenciales ordinarias, dando algunas definiciones, y resolviendo las más inmediatas.

**Ejemplo 1**: La variación de la temperatura *T* de un cuerpo con respecto al tiempo es proporcional a la diferencia $(T-A)$ donde *A* es la temperatura del medio ambiente ([ley de enfriamiento de Newton](http://es.wikipedia.org/wiki/Enfriamiento_newtoniano)). La ley física se representa por una ecuación diferencial ordinaria de primer orden (EDO de orden 1):

$\frac{dT}{dt}=k\left(T-A\right)$

**Ejemplo 2**: La variación con respecto al tiempo de una población $P(t)$ con índices constantes de nacimiento y mortalidad es proporcional al tamaño de la población, y también es una EDO de orden 1:

$\frac{dP}{dt}=kP$

**Ejemplo 3**: La [ley de Torricelli](http://es.wikipedia.org/wiki/Teorema_de_Torricelli) establece que la variación respecto al tiempo del volumen *V* de agua en un depósito que se está vaciando es proporcional a la raíz cuadrada de la profundidad *y* del agua del depósito:

$\frac{dV}{dt}=-ky^{1/2}$

**Ejemplo 4**: La distancia $x(t)$ recorrida en el movimiento acelerado de un cuerpo de masa *m* sometido a una fuerza variable $F(t)$  viene dada por una EDO de orden 2:

$\frac{d^{2}x}{dt}=\frac{F(t)}{m}$

**Definición 2**: *una función $y = f (x)$ se llama **solución de una ecuación diferencial** si la ecuación se cumple cuando se sustituyen $y$ y sus derivadas por $f (x)$ y sus derivadas, respectivamente. Una **solución particular** de una ecuación diferencial es cualquier solución que se obtiene asignando valores concretos a las constantes en la solución general. En la práctica, las soluciones particulares se obtienen a partir de condiciones iniciales que proporcionan el valor de la variable dependiente o de alguna de sus derivadas para un valor particular de la variable independiente.*

**Ejemplo 5**:  de la ecuación diferencial $y''-y=0$ son soluciones: a)  $y=sin(x)$,  b) $y=4e^{-x}$  c) $y=Ce^{-x}$ para cualquier valor *C* real. La solución b) es una solución particular obtenida a partir de la solución general c). Aunque es menos obvio, también la solución a) es una solución particular obtenida a partir de la solución general (puede verse usando los desarrollos de Taylor de la función exponencial y de la función seno).
### Haz de curvas y ecuaciones diferenciales de primer orden

Otra forma de introducir las ecuaciones diferenciales es desde el punto de vista geométrico. Consideremos la gráfica de la función $y=Cx^2$ para todos los posibles valores reales de *C*. En la imagen se representan los valores *C=1, 2, 4, 8*.

![Haz de curvas y=Cx²](/taller-matematicas/assets/images/feix_corbes.png) Haz de curvas y=Cx²
Se denomina **haz de curvas planas** al conjunto de todas las curvas que son gráficas de una función general $y=F(x,C)$. Cuando damos a *C* todos los valores posibles, las curvas generadas van llenando una región *R* del plano; en el caso de la imagen anterior esa región es todo el semiplano superior $x\in\left(-\infty,\infty\right),\;y\in\left[0,\infty\right).$ En general la región *R* dependerá del haz.

Nos preguntamos ahora: ¿para cada punto $(x,y)$ del plano existirá un único valor *C* tal que nos define de forma unívoca la función $y=F(x,C)$ que pase por ese punto? Podemos plantearlo en estos términos: fijando $x=x_0$ la función *F* pasa a depender sólo de *C*: $y=F(x_0,C)=f(C)$; ¿para cada valor de *y* habrá un único valor de *C*? Será así siempre que la función *f* sea estrictamente creciente o decreciente en *R*, y eso sucederá cuando su derivada no se anule: $\frac{\operatorname df}{\operatorname dC}\neq0$. En este caso es como si tuviéramos otra función $C=\psi(x,y)$ de dos variables que determina *C* para cada punto del plano.

En el ejemplo de la imagen anterior, fijando $x=x_0$ cualquiera obtenemos $y=f(C)=Cx_0^2, f'(C)=x_0^2$, este valor es siempre distinto de cero excepto en el origen de coordenadas, por tanto para el haz $y=Cx^2$ tenemos unicidad en el sentido de que dado un $\left(x,y\right)\neq\left(0,0\right)$ existe un único valor $C=\psi(x,y)=y/x^2$ que determina la curva que pasa por ese punto; por el origen $(0,0)$ en cambio pasan todas las curvas del haz.

Si derivamos la ecuación del haz obtenemos $y'=2Cx$, entonces, sustituyendo el valor anterior $C=\psi(x,y)$ eliminamos la *C* para obtener: $y'=2Cx=2\left(\frac y{x^2}\right)x=\frac{2y}x$, que es la **ecuación diferencial del haz de curvas, **que es una ecuación de primer orden.

**Ejemplo 6**: Hallar la ecuación diferencial del haz de curvas plano $y=Csin(x).$

La región R es la unión de los cuadrantes +X+Y  y -X-Y, en la figura se muestran algunas curvas.

![Haz de curvas y=C·Sin(x)](/taller-matematicas/assets/images/feix_corbes1.png) Haz de curvas y=C·Sin(x)

Fijando $x=x_0$ cualquiera obtenemos $y=C\sin\left(x_0\right)=f\left(C\right);f'\left(C\right)=\sin\left(x_0\right)$. Este valor será cero siempre que $x_0=k\mathrm\pi,\;\mathrm k=0,1,\dots.$ En este conjunto de puntos todas las curvas del haz coinciden, y en el resto de puntos tenemos unicidad: una única curva para cada punto, dada por: $C=\frac y{\sin\left(x\right)}=\psi(x,y)$.

Derivando la ecuación del haz: $y'=C\cdot\cos\left(x\right).$ Sustituimos el valor de *C*:

$\left.\begin{array}{r}y'=C\cdot\cos\left(x\right)\\C=\frac y{\sin\left(x\right)}\end{array}\right\}\Rightarrow y'=\frac{y\cos\left(x\right)}{\sin\left(x\right)}=\frac y{\tan\left(x\right)}$
***Definición 2**: El haz de curvas $y=f(C,x)$ es la **solución general de la ecuación diferencial ordinaria**; si fijamos un valor de $C=C_0$, obtenemos una única curva del haz, que denominamos **solución particular de la ecuación diferencial ordinaria**.*

**Ejemplo 7**: el haz de curvas $y=Csin(x)$ es la solución general de la ecuación diferencial $y'=\frac y{\tan\left(x\right)}$. Por el punto $\left(\frac{\mathrm\pi}2,3\right)$ pasa una única curva, $y=3Sin(x)$, que es una solución particular de la ecuación diferencial.

### Existencia y unicidad de la solución de una ecuación diferencial de primer orden

Hemos visto que para obtener la ecuación diferencial de un haz de curvas hay que derivar y eliminar la constante. Planteamos ahora el problema inverso: ¿dada una ecuación diferencial cualquiera, existe "su" haz de curvas  tal como lo hemos definido? El siguiente teorema nos responde para el caso de ecuaciones de primer orden.

**Teorema 1**: **existencia y unicidad**. Si tenemos una ecuación diferencial dada en la forma  $y'=f(x,y)$  tal que la función f es derivable de todos los órdenes (existen todas las derivadas de cualquier orden) en un entorno de $(x_0,y_0)$, entonces existe una única curva $y(x)$ tal que pasa por el punto $(x_0,y_0)$ y cumple la ecuación $y'=f(x,y).$

## Ecuaciones diferenciales ordinarias de primer orden inmediatas

Vemos en este apartado sólo las EDO de 1r orden más simples de resolver, en otros posts veremos los casos más generales.
### Ecuaciones del tipo $dy/dx=f\left(x\right)$

Son integrables directamente, escribiéndolas como $dy=f(x)\Rightarrow y=\int f(x)dx+C.$

**Ejemplo 8**: Resolver la ecuación diferencial $y'+x^{2}-1=e^{x}.$

La ecuación es equivalente a $dy/dx=e^{x}-x^{2}+1\Rightarrow y=\int\left(e^{x}-x^{2}+1\right)dx+C=e^{x}-\frac{1}{3}x^{3}+x+C.$
### Ecuaciones del tipo $dy/dx=ky$

Si $y = f (x)$ es una función, las ecuaciones del tipo $dy / dx = ky$ tienen por solución al conjunto de funciones $y (x) = Ce ^ {kx}$ donde C es un número real cualquiera. En general una ecuación diferencial tiene infinitas soluciones.

**Ejemplo 9**: la solución de la ecuación $\frac {dP} {dt} = kp$  que establece la evolución de una población $P(t)$ con índices constantes de nacimiento y mortalidad es cualquier función de la forma $y (x) = Ce^{kx}$.

**Ejemplo 10**: Supongamos que $P(t)$ es la población de una colonia de bacterias en el tiempo *t,* que la población en $t = 0$ es de 1000, y que la población se duplica en una hora. Entonces podemos decir que

$1000 = P(0)=C$
$2000 = P(1)=Ce^{k}$

por tanto $C=1000$ y $k=\ln2$, luego $P(t)=1000e^{x\text{·}\ln2}$.
La condición $P(0) = 1000$ se llama **condición inicial** pues normalmente el valor $t = 0$ se toma como el estado inicial. Cuando damos una condición inicial, la solución de la ecuación diferencial ya no tendrá en general infinitas soluciones, sino que tendrá sólo una,  o quizá ninguna si las condiciones son incompatibles. Equivalentemente, al dar una condición inicial pasamos, si existe, de la solución general a la solución particular que cumple esa condición. Así, la condición inicial $P (0) = - 1000$ no tiene ninguna solución del tipo $P(t) = Ce^{kt}$.

**Ejemplo 11**: Para resolver la ecuación $dy / dx = \frac{x} {\left (x^{2} +9 \right)^{1/2}}$ con la condición inicial $y(4)=2$ hacemos $y(x)=\int\frac{x}{\left(x^{2}+9\right)^{1/2}}dx=\left(x^{2}+9\right)^{1/2}+C$, como  $y(4)=\left(16+9\right)^{1/2}+C=5+C$ ha de ser $C=-3$.

![separador2](/taller-matematicas/assets/images/separador2.png)
# Bibliografía

ECUACIONES DIFERENCIALES - Resumen teórico y colección de ejercicios resueltos, y propuestos.
{% endraw %}