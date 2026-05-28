---
layout: post
title: "Física -> problemas resueltos -> Vibraciones y Ondas"
date: 2016-11-21 20:24:39 +0000
categories:
  - "Fí­sica"
  - "Mecánica"
tags:
  - "movimiento ondulatorio"
  - "movimiento oscilatorio"
  - "movimiento vibratorio"
math: true
---
{% raw %}

**1** - Una masa de 300 gr está encima de una superficie horizontal con rozamiento despreciable.  Fijamos la masa a un resorte de constante k = 22 N/m, y a continuación impulsamos la masa, que alcanza una velocidad inicial de 2 m/s. Debido a la fuerza variable del resorte, la masa describe un movimiento vibratorio armónico. ¿Cuál será su posición y velocidad  2 s después del instante inicial? ¿Cuál será su energía cinética cuando esté a 10c m del punto de equilibrio de la oscilación?

Solución:

La ecuación del movimiento vibratorio armónico es:

$x=A\sin\left(\omega t+\varphi\right)$ [1]
donde x es el desplazamiento respecto la posición de equilibrio, $\omega$ es la pulsación del movimiento (relacionada con la velocidad angular) y $\varphi$ es la fase inicial, relacionada con la posición del cuerpo en el instante inicial t = 0. En nuestro caso, para t = 0 tenemos una velocidad inicial de 2m/s, pero el resorte en ese instante inicial no está ni comprimido ni estirado, luego podemos tomar x = 0:

$0=A\sin\left(\omega\cdot0+\varphi\right)\Rightarrow\sin\left(\varphi\right)=0\Rightarrow\varphi=0.$

La fase inicial es cero. Como en un movimiento vibratorio armónico la velocidad es máxima  cuando el móvil pasa por el punto de equilibrio x = 0, tendremos que esa velocidad máxima vale  2 m/s. La velocidad viene dada por la derivada de la posición respecto del tiempo:

$x=A\sin\left(\omega t\right)\Rightarrow v=\frac{\operatorname dx}{\operatorname dt}=A\omega\cos\left(\omega t\right)$ [2]

y la velocidad máxima es $v_{max}=A\omega=2$.  Pasemos ahora a utilizar los otros datos: el resorte ejerce una fuerza $F=-kx=-22x$, esta fuerza producirá una aceleración $a=F/m=-22x/0.3$ [3] en $m/s^2$. ¿Cuál es la aceleración  del movimiento vibratorio armónico?

$a=\frac{\operatorname dv}{\operatorname dt}=-A\omega^2\sin\left(\omega t\right)$

Igualamos esta aceleración con la [3], y sustituimos el desplazamiento x por el dado por [1], y simplificamos:

$\begin{array}{l}-A\omega^2\sin\left(\omega t\right)=-22x/0.3\Rightarrow\\A\omega^2\sin\left(\omega t\right)=\frac{220}3A\sin\left(\omega t\right)\Rightarrow\omega^2=\frac{220}3\Rightarrow\boxed{\omega=\sqrt{\frac{220}3}}\\\end{array}$

hemos obtenido la pulsación $\omega$.  Para determinar completamente el movimiento necesitamos también su amplitud A. Una forma directa de hacerlo es a través del cálculo de la energía mecánica: inicialmente la masa tiene una energía cinética $E_c=\frac12mv^2=0.5\cdot0.3\cdot2^2=0.6J$. y cuando se detiene por la fuerza del resorte, éste tendrá una energía potencial elástica  $\frac12kA^2$, igualando ámbas energías:

$\frac1222\cdot A^2=0.6\Rightarrow A=\sqrt{2\cdot0.6/22}\approx0.23m$

entonces la ecuación de este movimiento es

$x=0.23\sin\left(\sqrt{\frac{220}3}t\right)\approx0.23\sin\left(8.6t\right)$

Cuando t = 2, la posición será $x=0.23\sin\left(8.6\cdot2\right)=0.07$, y la velocidad viene dada por [2]:  $v=A\omega\cos\left(\omega t\right)=0.23\cdot8.6\cos\left(8.6\cdot2\right)=1.89\;m/s$.

Para x = 0.1 el tiempo es $0.1=0.23\sin\left(8.6t\right)\Rightarrow t=\frac1{8.6}\sin^{-1}\left(\frac{0.1}{0.23}\right)=3s$, y la velocidad es $v=0.23\cdot8.6\cos\left(8.6\cdot3\right)=1.78\;m/s$, luego la energía cinética será $E_c=0.5\cdot0.3\cdot1.78^2=0.48\;J$.  Otra forma de calcular la energía cinética para x = 0.1 es usando la energía mecánica total; la energía potencial del resorte en x = 0.1 es $E_p=0.5\cdot22\cdot0.1^2=0.11$, y la energía mecánica total se conserva, pues no hay rozamiento, y ha de ser la misma en todo el recorrido, como inicialmente, en x = 0, solo hay energía cinética, y sabemos que vale 0.6, igualamos energía mecánicas en x = 0 y x = 0.1:

$0.6\;=E_c+0.11\Rightarrow E_c=0.49$

obtenemos el mismo resultado con un error de una centésima de Joule, debido a los errores de redondeo.

*

**2** - Una onda transversal de 0.2 m de amplitud y 200Hz de frecuencia tarda 30s en llegar a un punto situado a 300m del foco. En la posición x = 30m, y el tiempo t = 10s, ¿cuál es la amplitud del movimiento y su velocidad de oscilación?  ¿Cuál es la diferencia de fase de dos puntos situados a 50m de distancia?

Solución:  la ecuación de una onda transversal es

$\omega=2\pi f,\;k=\frac{2\pi}\lambda\Rightarrow y\left(x,t\right)=A\sin\left(2\pi\left(\frac x\lambda-ft\right)+\varphi\right)$ [1]

La velocidad de transmisión es $v=f· \lambda$, si tarda 30s en llegar a un punto situado a 300m del foco, esta velocidad es 300/30 = 10 m/s, por tanto $\lambda=v/f=10/200=1/20 m$

Sustituimos valores, tomando la fase inicial igual a cero:

$y\left(x,t\right)=0.2\sin\left(2\pi\left(\frac x{1/20}-200t\right)\right)=0.2\sin\left(40\pi\left(x-10t\right)\right)$ [2]

En la posición x = 30m, y el tiempo t = 10s,  la amplitud es:

$y\left(30,10\right)=0.2\sin\left(40\pi\left(30-10\cdot10\right)\right)=-0.08 m$

El módulo de la velocidad es:

$v_y=\frac{\operatorname dy\left(x,t\right)}{\operatorname dt}=2\pi fA\cos\left(2\pi\left(\frac x\lambda-ft\right)\right)$

Y su valor:

$v_y=2\pi\cdot200\cdot0.14\cos\left(2\pi\left(\frac{30}{1/20}-200\cdot10\right)\right)=-161\;m/s$

La fase en un punto x y un instante t es $\left(2\pi\left(20x-200\cdot t\right)\right)=40\pi\left(x-10t\right)$. La diferencia de fase es

$\left$40\pi\left(\left(x+50\right)-10t\right)\right$-\left$40\pi\left(x-10t\right)\right$=40\pi\cdot50=2000\pi$,

que debemos reducir a fracciones de $2\pi$ haciendo la división entera y tomando el resto (operación módulo): $2000\pi\;\text{Mod  }2\pi=0$,  luego la diferencia de fase es cero. Este resultado también puede deducirse viendo que la distancia 50 m es un múltiplo entero de la longitud de onda $\lambda=1/20$, siendo $50=1000·\lambda$.

![separador2](/taller-matematicas/assets/images/separador2-300x38.png)

**3** - Dos piezas A y B, de 20 y 40 Kg respectivamente, estan unidas por un resorte de masa despreciable, estando el conjunto sobre un soporte horizontal S. La pieza A está oscilando verticalmente con una amplitud de 2 cm y frecuencia de 5 Hz. ¿Qué fuerzas ejerce el conjunto sobre el soporte?

![prob_vidal_421](/taller-matematicas/assets/images/Prob_Vidal_421.png)

**Solución**: las fuerzas *F* sabemos que estan relacionadas con las aceleraciones *a* según *F = ma*; y la aceleración de un movimiento armónico es  *a = *- ω2x* donde x mide la desviación de la posición de equilibrio del muelle, que puede ser positiva o negativa. La pulsación se relaciona con la frecuencia *f* por *ω= 2πf*. Por otro lado tenemos que tener en cuenta la fuerza de la gravedad, y la posición de A.

Cuando x > 0 el muelle ejercerá sobre A una fuerza dirigida hacia abajo, el diagrama de fuerzas sobre las piezas A y B será:

$caption id="attachment_150302" align="aligncenter" width="265"$![prob_vidal_421b](/taller-matematicas/assets/images/Prob_Vidal_421b.png) Situación cuando el muelle está distendido[/caption]
Fuerzas y aceleración sobre A: $-F_m-M_Ag=-M_A\omega^2x$, fuerzasy aceleración sobre B (observemos que B no se mueve): $F_m+N-M_Bg=0$. Operando:

$\left.\begin{array}{r}F_m+N-M_Bg=0\\-F_m-M_Ag=-M_A\omega^2x\end{array}\right\}\Rightarrow\left.\begin{array}{r}N=M_Bg-F_m\\F_m=M_A\left(\omega^2x-g\right)\end{array}\right\}\Rightarrow N=M_Bg-M_A\left(\omega^2x-g\right)=\boxed{\left(M_A+M_B\right)g-M_A\omega^2x}$

La fuerza normal N es la que ejercen entre sí el bloque B y el soporte S; es variable, dependiendo de la posición x, la cual en el movimiento armónico sabemos que viene dada por $x=A\sin\left(\omega t\right)$, siendo A la amplitud, por tanto: $N=\left(M_A+M_B\right)g-M_A\omega^2A\sin\left(\omega t\right)$.  Vemos que la fuerza sobre el soporte es igual al peso total de los dos bloques, $\left(M_A+M_B\right)g$, menos la fuerza producida por la aceleración del movimiento armónico sobre el bloque A, $M_A\omega^2A\sin\left(\omega t\right)$. De hecho esta expresión también será válida cuando x < 0, como podéis comprobar fácilmente:

$caption id="attachment_150305" align="aligncenter" width="268"$![Situación cuando el muelle está comprimido, y x <0. Conduce a la misma expresión para N](/taller-matematicas/assets/images/Prob_Vidal_421d.png) Situación cuando el muelle está comprimido, y x <0; conduce a la misma expresión para N.[/caption]
Sustituimos los valores del enunciado:

$N=\left(20+40\right)9.8-20\cdot\left(2\mathrm\pi\cdot5\right)^2\cdot0.02\cdot\sin\left(2\mathrm\pi\cdot5t\right)=\boxed{588-395\sin\left(10\mathrm{πt}\right)}$

La fuerza mínima N sobre el soporte sucederá cuando x sea igual a la amplitud A, o equivalentemente, cuando la fase sea tal que el seno valga 1: $N_{min}=588-395\cdot1=193\;N$. Será máxima cuando x sea negativa e igual a A, o sea cuando el seno de la fase valga -1: $N_{min}=588-395\cdot\left(-1\right)=983\;N$. Finalmente, cuando x = 0 el muelle no ejerce fuerza, y sobre el soporte solo actúa el peso del conjunto: $N_{x=0}=588-395\cdot\left(0\right)=588\;N$.

![separador2](/taller-matematicas/assets/images/separador2-300x38.png)
{% endraw %}