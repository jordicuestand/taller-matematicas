---
layout: post
title: "Mecánica Ondulatoria"
date: 2017-08-04 12:48:48 +0000
categories:
  - "Fí­sica"
  - "Mecánica Cuántica"
  - "Mecánica Ondulatoria"
tags:
  - "cuantización"
  - "estados estacionarios"
  - "función de onda"
  - "niveles energéticos"
  - "Schrödinger"
math: true
---
{% raw %}

El estudio del comportamiento de sistemas muy pequeños, como las moléculas y los átomos, utilizando la ecuación de ondas de Schrödinger es una parte de la Mecánica Cuántica conocida por el nombre de Mecánica Ondulatoria; este post la trata a nivel técnico, para un introducción menos técnica a la ecuación de Schrödinger y a la Mecánica Cuántica en general recomiendo mi serie de artículos en el blog [http://matfisfil.blogspot.com.es/](http://matfisfil.blogspot.com.es/), concretamente el post [Entendiendo la mecánica cuántica](http://matfisfil.blogspot.com.es/2012/01/entendiendo-la-mecanica-cuantica.html).
# La ecuación de Schrödinger

En 1926 Erwin Schrödinger sugirió la siguiente ecuación para representar la función de onda de probabilidad de una partícula puntual de masa *m*:
$-\frac{\hslash^2}{2m}\nabla^2\psi+V\psi=i\hslash\frac{\partial\psi}{\partial t}$ [1]

La constante $\hslash$ se llama constante de Plank reducida: h es la [constante de Planck](https://es.wikipedia.org/wiki/Constante_de_Planck), que es nada menos que una de las constantes básicas universales, la de la acción física mínima posible, siendo la acción el producto de la energía por el tiempo durante el cual actúa esa energía; cuando se utiliza en el contexto de ondas o fenómenos vibracionales, periódicos, es útil para ahorrar escritura usar la versión reducida de la constante, que es $\hslash=\frac h{2\mathrm\pi}$. El operador $\nabla^2$ es el [Laplaciano](https://es.wikipedia.org/wiki/Operador_laplaciano), un operador diferencial vectorial que se utiliza para expresar los cambios en una función derivable cuando variamos la posición de la partícula. *V* representa la energía potencial de la partícula. Y el elemento clave de la ecuación es la función de onda $\psi$ de la partícula, que es una función compleja (observemos la constante i, que es el número imaginario $i=\sqrt{-1}$.

En la parte izquierda de la ecuación [1] tenemos la variación (diferencial) de la función de onda con la posición de partícula y el producto de la función por el potencial, en la derecha tenemos la variación de la función de onda con el tiempo; ambos miembros son idénticos, esto es lo que nos dice la ecuación.

Siendo $\psi$ una función compleja, su interpretación física no es directa, sucede como en otras áreas de la Física donde se utilizan complejos para simplificar los cálculos y la escritura, ver por ejemplo el post [Los números complejos. ]({{ '/2016/10/12/los-numeros-complejos/' | relative_url }})La interpretación es la siguiente: El módulo al cuadrado del número complejo  $\psi\left(x,y,z,t\right)$, que representamos por $\left|\psi\left(x,y,z,t\right)\right|^2$, es la [densidad de probabilidad](https://es.wikipedia.org/wiki/Funci%C3%B3n_de_densidad_de_probabilidad) de encontrar la partícula en el punto (x, y, z) en el instante t; entonces, la probabilidad de encontrar la partícula en un cierto volumen infinitesimal $\operatorname d\tau$ es, por definición de densidad de probabilidad, el producto $\left|\psi\left(x,y,z,t\right)\right|^2\operatorname d\tau$, y la probabilidad de encontrarla en un volumen finito $\Omega$ viene dada por la integral de volumen
$\int_\Omega\left|\psi\left(x,y,z,t\right)\right|^2\operatorname d\tau$ [2]

Si el volumen $\Omega$ es todo el espacio, se demuestra que
$\int_{espacio}\left|\psi\left(x,y,z,t\right)\right|^2\operatorname d\tau=1$,

lo que significa que la partícula siempre está en algún sitio, no "desparece", hay una probabilidad igual a 1, o del 100%, de que esté en algún sitio.
## Flujo de probabilidad de encontrar la partícula

La función $\psi$ se extiende por todo el espacio y es variable con el tiempo. La probabilidad de que la partícula esté en un volumen $\Omega$ fijo será pues variable, es como si la función "fluyera" por el volumen $\Omega$, a veces habrá más probabilidad acumulada dentro del volumen, otras veces habrá menos probabilidad. Si nos preguntamos por la variación de esa probabilidad, según [2] vendrá dada por
$\frac{\operatorname d{}}{\operatorname dt}\int_\Omega\left|\psi\left(x,y,z,t\right)\right|^2\operatorname d\tau$ [3]

Para entender lo que sigue podemos simplificar la situación y considerar un movimiento rectilíneo, o sea, en una única dimensión espacial x; además, utilizaremos la igualdad $\left|\psi\left(x,t\right)\right|^2=\psi^\ast\left(x,t\right)\cdot\psi\left(x,t\right)$, donde $\psi^\ast$ es el [complejo conjugado](https://es.wikipedia.org/wiki/Conjugado_(matem%C3%A1tica)) de $\psi$. Con todo esto, la expresión [2] queda:
$\frac{\partial{}}{\partial t}\int_\Omega\left|\psi\left(x,t\right)\right|^2\operatorname d\tau=\int_\Omega\left\{\psi^\ast\left(x,t\right)\frac{\partial\psi}{\partial t}+\psi\left(x,t\right)\frac{\partial\psi^\ast}{\partial t}\right\}\operatorname d\tau$. [4]

Conjugando la ecuación [1]:

$\left(-\fracℏ{2m}\nabla^2\psi+V\psi\right)^\ast=\left(i\hslash\frac{\partial\psi}{\partial t}\right)^\ast\Leftrightarrow-\fracℏ{2m}\nabla^2\psi^\ast+V\psi^\ast=-i\hslash\frac{\partial\psi^\ast}{\partial t}$,

despejando la derivada temporal de la función de onda en [1] y de su conjugada:

$\begin{array}{l}-\fracℏ{2m}\nabla^2\psi+V\psi=i\hslash\frac{\partial\psi}{\partial t}\Leftrightarrow\frac{\partial\psi}{\partial t}=-\fracℏ{2mi\hslash}\nabla^2\psi+\frac V{i\hslash}\psi;\\-\fracℏ{2m}\nabla^2\psi^\ast+V\psi^\ast=-i\hslash\frac{\partial\psi^\ast}{\partial t}\Leftrightarrow\frac{\partial\psi^\ast}{\partial t}=\fracℏ{2mi\hslash}\nabla^2\psi-\frac V{i\hslash}\psi^\ast\end{array}$

Usando estas igualdades en la expresión de la derecha de [4]:

$\begin{array}{l}\psi^\ast\frac{\partial\psi}{\partial t}+\psi\frac{\partial\psi^\ast}{\partial t}=-\frac{\hslash^2}{2mi\hslash}\psi^\ast\nabla^2\psi+\cancel{\frac V{i\hslash}\psi^\ast\psi}+\frac{\hslash^2}{2mi\hslash}\psi\nabla^2\psi-\cancel{\frac V{i\hslash}\psi\psi^\ast}\\=\frac{\hslash i}{2m}\left(\psi^\ast\nabla^2\psi-\psi\nabla^2\psi\right).\\\end{array}$,

donde hemos usado que $1/i = -i$. Particularizando para el caso unidimensional, la expresión [4] queda así:

$\frac\partial{\partial t}\int_\Omega\left|\psi\left(x,t\right)\right|^2\operatorname d\tau=\frac{\hslash i}{2m}\int_{x_1}^{x_2}\left(\psi^\ast\frac{\partial^2\psi}{\partial x^2}-\psi\frac{\partial^2\psi^\ast}{\partial x^2}\right)\operatorname dx$,

que se puede integrar por partes, y resulta:

$\frac\partial{\partial t}\int_\Omega\left|\psi\left(x,t\right)\right|^2\operatorname d\tau=\frac{\hslash i}{2m}\left.\left(\psi^\ast\frac{\partial\psi}{\partial x}-\psi\frac{\partial\psi^\ast}{\partial x}\right)\right|_{x_1}^{x_2}.$

Esta variación de la probabilidad dentro del volumen $\Omega$ puede considerarse que es causado por una "corriente de probabilidad" que atraviesa la frontera del volumen; definimos la corriente de densidad de probabilidad por
$j\left(x,t\right)=\frac{\hslash i}{2m}\left.\left(\psi^\ast\frac{\partial\psi}{\partial x}-\psi\frac{\partial\psi^\ast}{\partial x}\right)\right|$ [5]

que en el caso general de tres dimensiones es
$j\left(x,y,z,t\right)=\frac{\hslash i}{2m}\left.\left(\psi^\ast\nabla\psi-\psi\nabla\psi^\ast\right)\right|$. [6]

## Posición esperada de la partícula

El vector posición r de la partícula no tiene una posición definida, todo lo que tenemos son probabilidades de que apunte dentro de algún volumen $\Omega$ del espacio, lo que sí podemos calcular es el valor promedio del vector posición; en Estadística se explica que, dada una variable aleatoria continua x con densidad de probabilidad f(x), el valor promedio de x viene dado por

$\overline x=\int_a^bx\cdot f\left(x\right)\operatorname dx$;

si lo aplicamos al vector de posición:

$\overline r=\int_{espacio}r\cdot\left|\psi\left(r\right)\right|^2\operatorname d\tau$.
## Caso de variables separables y potencial estático

Si el potencial V no depende del tiempo sino sólo de la posición, clásicamente la energía mecánica se conserva. Supongamos además que la función de onda $\psi$ es separable, lo que significa que podemos expresarla como producto de dos funciones, una función de la posición u(r) y otra del tiempo v(t): $\psi=u(r)v(t)$; sustituyendo en [1],

$\begin{array}{l}-\frac{\hslash^2}{2m}\nabla^2\left(u\left(r\right)v\left(t\right)\right)+Vu\left(r\right)v\left(t\right)=i\hslash\frac{\partial\left(u\left(r\right)v\left(t\right)\right)}{\partial t}\Leftrightarrow\\-\frac{\hslash^2}{2m}v\left(t\right)\nabla^2u\left(r\right)+Vu\left(r\right)v\left(t\right)=i\hslash u\left(r\right)\frac{\partial v\left(t\right)}{\partial t}\end{array}$,

y dividiendo toda la expresión por uv:
$\begin{array}{l}-\frac{\hslash^2}{2mu\left(r\right)}\nabla^2u\left(r\right)+V=\frac{i\hslash}{v\left(t\right)}\frac{\partial v\left(t\right)}{\partial t}\Leftrightarrow\\\frac1{u\left(r\right)}\left(-\frac{\hslash^2}{2m}\nabla^2u\left(r\right)+Vu\left(r\right)\right)=\frac{i\hslash}{v\left(t\right)}\frac{\partial v\left(t\right)}{\partial t}.\end{array}$ [7]

El miembro de la izquierda de [7] depende solo del vector posición r, y el miembro de la derecha solo del tiempo; la igualdad [7] expresa por tanto la igualdad de dos funciones que dependen de variables distintas, la única forma que se cumpla esto es que ambas funciones sean iguales a una constante, que llamaremos E:
$\begin{array}{l}\frac1{u\left(r\right)}\left(-\frac{\hslash^2}{2m}\nabla^2u\left(r\right)+Vu\left(r\right)\right)=E;\\\frac{i\hslash}{v\left(t\right)}\frac{\partial v\left(t\right)}{\partial t}=E.\end{array}$ [8]

La segunda igualdad es una ecuación diferencial inmediata:

$\frac{i\hslash}v\frac{\operatorname dv}{\operatorname dt}=E\Rightarrow\int\frac{i\hslash}v\operatorname dv=\int E\operatorname dt\Rightarrow i\hslash\ln\left(v\right)=Et+C\Rightarrow v=C\cdot exp\left(\frac{Et}{i\hslash}\right)$,

donde C es una constante de integración; la función de onda toma la forma $\psi\left(r,t\right)=C\cdot u\left(r\right)\cdot exp\left(\frac{Et}{i\hslash}\right)=C\cdot u\left(r\right)\cdot exp\left(\frac{-iEt}{\hslash}\right)$.  La exponencial compleja $exp\left(\frac{-iEt}ℏ\right)$ tiene módulo 1, así que el módulo de la función de onda viene determinado por la función u(r), en efecto:

$\begin{array}{l}\left|\psi\left(r,t\right)\right|^2=\psi^\ast\left(r,t\right)\cdot\psi\left(r,t\right)=\left$u\left(r\right)\cdot exp\left(\frac{-iEt}ℏ\right)\right$^\ast\cdot\left$u\left(r\right)\cdot exp\left(\frac{-iEt}ℏ\right)\right$=\\u^2\left(r\right)\left$\left(\cos\left(z\right)+i\sin\left(z\right)\right)\right$\cdot\left$\left(\cos\left(z\right)-i\sin\left(z\right)\right)\right$=u^2\left(r\right)\end{array}$

donde hemos aplicado la [fórmula de Euler](https://es.wikipedia.org/wiki/F%C3%B3rmula_de_Euler) para la exponencial compleja. Vemos que aunque la función de onda depende del tiempo, la densidad de probabilidad de encontrar la partícula en algun sitio es constante en el tiempo: los estados cuánticos en los que se cumple esto se llaman **estados estacionarios**.
## Partícula libre, energía cinética cuántica

Si el potencial V es nulo, la partícula se mueve libremente sin fuerzas que actúen sobre ella; la primera de las ecuaciones [8] queda:
$-\frac{\hslash^2}{2m}\nabla^2u\left(r\right)=Eu\left(r\right)\Leftrightarrow\nabla^2u\left(r\right)=-\frac{2mE}{\hslash^2}u\left(r\right)$,

ecuación diferencial de segundo orden que, en una dimensión r = x, tiene soluciones de la forma $u\left(r\right)=Ce^{ikx}$, con C una constante de integración y $k=\sqrt{2mE}/\hslash$. La función de onda toma por tanto la forma

$\psi\left(x,t\right)=Ce^{i\frac{\sqrt{2mE}\hslash}x}\cdot e^{i\frac{-E\hslash}t}=Ce^{i\frac{\sqrt{2mE}\hslash}x-i\frac{-E\hslash}t}$,

comparando esta expresión con la general de una [onda plana en su forma compleja](https://es.wikipedia.org/wiki/Onda_plana), $\psi\left(x,t\right)=Ce^{i\left(kx-\omega t\right)}$, donde k es el número de onda y $\omega$ es la pulsación, identificamos el número de onda k de la función de onda $\psi$ con $k=\frac{\sqrt{2mE}}\hslash$. Por otro lado, la [ecuación de De Broglie](https://es.wikipedia.org/wiki/Ondas_de_materia) relaciona este número de onda con el momento mecánico de la partícula: $\lambda=\frac{\hslash}p\Leftrightarrow\frac1k=\frac{\hslash}p\Leftrightarrow p=\hslash k$, por tanto

$p=\hslash k=\hslash\frac{\sqrt{2mE}}\hslash=\sqrt{2mE}\Leftrightarrow E=\frac{p^2}{2m}$,

o sea que la constante E es la energía cinética (clásica, no relativista) de la partícula, que también el caso cuántico se conserva. La primera ecuación [8] se llama **ecuación de Schrödinger independiente del tiempo**, que en su forma unidimensional e incorporando el potencial V es:

$-\frac{\hslash^2}{2m}\frac{\operatorname d^2u\left(x\right)}{\operatorname dx^2}+V\left(x\right)u\left(x\right)=Eu\left(x\right)$ [9]

## Ejemplo de aplicación: barrera de potencial

*Una partícula cuántica está confinada a moverse en un segmento rectilíneo de anchura 2a; describir la ecuación de su posición y calcular su energía mecánica*.

El confinamiento en una región puede modelarse mediante un potencial V(x) tal que sea cero dentro de la región y sea infinito fuera de la región, ya que la energía total es la suma del potencial más la energía cinética, $E = V + E_c$, cuando V = 0 sólo hay energía cinética, y fuera de la región permitida se violaría la conservación de la energía total.

![](/taller-matematicas/assets/images/barrera_potencial.png) Barrera de potencial unidimensional: la partícula sólo puede moverse dentro de la región (-a, +a)

Siendo V = 0 dentro del recinto, podemos aplicar la ecuación [8], que es una ecuación diferencial lineal de segundo orden, con solución general (real):

$u\left(x\right)=A\sin\left(\frac{\sqrt{2mE}}{\hslash}x\right)+B\cos\left(\frac{\sqrt{2mE}}{\hslash}x\right)$; las condiciones de contorno son u = 0 para x = -a o x = a, además obligaremos a que la función u(x) sea continua en el intervalo -a < x < a (esta es una presunción estándar para la  función de onda), sustituyendo:

$\left.\begin{array}{r}A\sin\left(\frac{\sqrt{2mE}}{\hslash}a\right)+B\cos\left(\frac{\sqrt{2mE}}{\hslash}a\right)=0\\A\sin\left(-\frac{\sqrt{2mE}}{\hslash}a\right)+B\cos\left(-\frac{\sqrt{2mE}}{\hslash}a\right)=0\end{array}\right\}$

Usando las propiedades $\sin\left(-\alpha\right)=-\sin\left(\alpha\right),\;\cos\left(-\alpha\right)=\cos\left(\alpha\right)$, y sumando las dos igualdades:

$\left.\begin{array}{r}A\sin\left(\frac{\sqrt{2mE}}{\hslash}a\right)+B\cos\left(\frac{\sqrt{2mE}}{\hslash}a\right)=0\\-A\sin\left(\frac{\sqrt{2mE}}{\hslash}a\right)+B\cos\left(\frac{\sqrt{2mE}}{\hslash}a\right)=0\end{array}\right\}\Rightarrow2B\cos\left(\frac{\sqrt{2mE}}{\hslash}a\right)=0\Rightarrow\frac{\sqrt{2mE}}{\hslash}a=n\pi,$

con n = 0, 1, 2, ... ; si las restamos obtenemos la segunda familia de soluciones:

$\left.\begin{array}{r}A\sin\left(\frac{\sqrt{2mE}}{\hslash}a\right)+B\cos\left(\frac{\sqrt{2mE}}{\hslash}a\right)=0\\-A\sin\left(\frac{\sqrt{2mE}}{\hslash}a\right)+B\cos\left(\frac{\sqrt{2mE}}{\hslash}a\right)=0\end{array}\right\}\Rightarrow2A\sin\left(\frac{\sqrt{2mE}}{\hslash}a\right)=0\Rightarrow\frac{\sqrt{2mE}}{\hslash}a=n\frac\pi2$.

Físicamente, para conseguir que la expresión $\frac{\sqrt{2mE}}{\hslash}a$ tome un conjunto de valores discretos, obliga a que tomen valores discretos o bien la energía E, o bien la masa m, o bien ámbas; asumiendo que la masa de la partícula es un valor único, ha de ser la energía E la que tome valores discretos:

$\begin{array}{l}\frac{\sqrt{2mE}}{\hslash}a=n\frac\pi2\Rightarrow E=\hslash^2n^2\frac{\pi^2}{8ma^2},\;n=0,1,2\dots\\\frac{\sqrt{2mE}}{\hslash}a=n\pi\Rightarrow E=\hslash^2n^2\frac{\pi^2}{2ma^2},\;n=0,1,2\dots\end{array}$

La segunda de estas secuencias está incluida en la primera, así pues llegamos a la expresión de las energías permitidas para la partícula confinada a una región:
$E_n=\frac{\hslash^2n^2\pi^2}{8ma^2},\;n=1,2\dots$ [9]

Este es un resultado fundamental, la cuantización de la energía, que sirve de base para entender la estructura de los átomos; hemos eliminado el valor n = 0 pues implica una función de onda nula, o sea, una probabilidad nula de encontrar la partícula. Las energías fundamentales, n = 1, 2, 3 ,... estan bien separadas entre sí:  los cocientes entre niveles vienen dados por (n+1)²/n² = 4, 9/4, 16/9, 25/16, ... que para n grandes tienden a 1: para energias muy altas la diferencia de niveles energéticos es practicamente nula, es lo que sucede en nuestro mundo macroscópico, en el que se ve la energia como un valor continuo, no discreto.

La función de onda u(x) debe ser nula en los extremos x = -a, x = +a; para que se cumpla simultáneamente tenemos que definirla como una función con doble definición:

$\psi\left(x\right)=\left\{\begin{array}{l}A\sin\left(\frac{n\mathrm\pi}{2a}\right),\;n=2,4,6,\dots\\B\cos\left(\frac{n\mathrm\pi}{2a}\right),\;n=1,3,5,\dots\end{array}\right.$

En la gráfica siguiente se representa la densidad de probabilidad u(x)² para los niveles n = 1, n = 2; en este segundo nivel la partícula nunca se encuentra en el centro de la región x = 0.

![](/taller-matematicas/assets/images/nivells-energia-basics.png) Densidad de probabilidad para los primeros niveles energéticos permitidos, caso de partícula confinada en una región (-a, a). La escala de la abcisa viene dada en fraciones de a.

Estas formas de la función de densidad de probabilidad recuerdan a las de las [ondas estacionarias de la cuerda vibrante](https://es.wikipedia.org/wiki/Cuerda_vibrante), que también presentant modos de vibración parecidos a los niveles energéticos cuánticos.
{% endraw %}