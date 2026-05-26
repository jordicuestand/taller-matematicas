---
layout: post
title: "Física -> Problemas de Mecánica -> Dinámica: campo gravitatorio"
date: 2016-05-09 05:16:00 +0000
categories:
  - "Fí­sica"
  - "Mecánica"
math: true
---

**1** - Un objeto se aleja de la Tierra a una velocidad radial de 5 m/s; observamos que 20 minutos después su velocidad ha pasado a ser de 4.5 m/s. ¿Cuál es la intensidad media del campo gravitatorio terrestre en ese intervalo?

Solución:

Llamando g(r) a la intensidad del campo gravitatorio a una distancia r de la Tierra, la fuerza gravitatoria sobre una masa m será F=mg(r); sabemos que en t=0 la velocidad era de 5 m/s, y en t=20·60=1200s era de 4.5 m/s, luego la aceleración media ha sido

$a=\frac{\triangle v}{\triangle t}=\frac{4.5-5}{1200}=-\frac1{2400}\frac m{s^2}$

Aplicando la 2ª ley de Newton F=ma, e igualando con la fuerza gravitatoria, obtenemos

$F=ma=\frac m{2400}=mg\Rightarrowboxed{g=\frac1{2400}\frac m{s^2}}$

![separador2](/assets/images/separador2.png)

**2**. Dos objetos de masas m y M se atraen con una fuerza gravitatoria de 80N cuando están a una cierta distancia d; ¿con que fuerza se atraerán dos objetos de masa 10m y M situados a una distancia de 4d?

Solución:

En el primer caso la fuerza gravitatoria será $F=G\frac{mM}{d^2}=80N$ y en el segundo será $F'=G\frac{10mM}{\left(4\dright)^2}=G\frac{10mM}{16d^2}=\frac{10}{16}\left(G\frac{mM}{d^2}\right)=\frac58F=\frac5880=\boxed{50N}$

![separador2](/assets/images/separador2.png)

**3.** Calcular a que altura la intensidad del campo gravitatorio terrestre se reduce a la mitad del que tiene en la superficie,

Solución:

La intensidad del campo gravitatorio es $g=GM_T/R^2$; en la superficie tenemos $R=R_T$, el radio de la Tierra, y a una altura h tenemos $R=R_T+h$. La proporción entre intensidades es

$\frac g{g'}=\frac{GM_T/R_T^2}{GM_T/\left(R_T+hright)^2}=\frac{1/R_T^2}{1/\left(R_T+h\right)^2}=\frac{\left(R_T+h\right)^2}{R_T^2}=\left(\frac{R_T+h}{R_T}\right)^2$

Como esa proporción queremos que valga $g/g'=g/(0.5g)=1/0.5=2$, sustituimos y despejamos h:

$h=2639 Km$

Este resultado es fácilmente generalizable a cualquier proporción p>1: $h=\left(sqrt {p-1}\right)R_T$

![separador2](/assets/images/separador2.png)