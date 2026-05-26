---
layout: post
title: "Uso de diferenciales en Física"
date: 2016-05-10 09:07:30 +0000
categories:
  - "Fí­sica"
tags:
  - "diferencial"
math: true
---

Frecuentemente encontramos en los libros de texto y apuntes de clase, en las demostraciones de leyes físicas, que aparecen "cantidades diferenciales". Estas diferenciales tienen relación con el concepto de diferencial de una función y con su derivada en Matemáticas, pero a veces puede quedar un poco oscura esta relación. En este breve artículo pretendemos aclarar conceptos con algunos ejemplos.

### Magnitudes diferenciales en Física

Definición 1: Dada una magnitud X denotamos por $\triangle X$ la variación de esa magnitud, o equivalentemente, un intervalo en la magnitud.

Ejemplo 1: Si la magnitud es el tiempo t, entonces $\triangle t$ es un intervalo de tiempo.

Ejemplo 2:  Si la magnitud es una longitud L, entonces $\triangle L$ es un intervalo de longitud, un segmento.

Definición 2: Dada una magnitud X que supondremos continua, denotamos por $\operatorname dX$ su **diferencial**, y el concepto asociado es un intervalo $\triangle X$ "infinitesimal", esto es , un intervalo *prácticamente* nulo. A pesar de que matemáticamente es demasiado ambiguo hablar de "intervalo prácticamente nulo", el concepto es muy útil en Física, y es usado muy frecuentemente.

Ejemplo 3: El número de electrones N que circulan por segundo por un conductor no es una magnitud continua, sino entera, así que en principio no podemos definir su diferencial; ahora bien, en los casos prácticos, este número es tan elevado que podemos suponer que sí es contínuo, y pensar en diferenciales de N, dN.

Ejemplo 4: Sea un cable que está conduciendo corriente eléctrica

[caption id="attachment_1652" align="aligncenter" width="300"]![Fig. 4: sección de un conductor recorrido por una corriente de electrones](/assets/images/element_corrent-300x146.png) Fig. 4: sección de un conductor recorrido por una corriente de electrones[/caption]
El número de electrones que se estan moviendo por el cable es muy elevado, del orden de $10^{20}$ por $cm^3$; queremos considerar aquellos que se hallen en una cierta posición x, medida desde el extremo del cable. Si consideramos que los electrones estan distribuidos de forma más o menos uniforme y contínua por el cable, podemos definir la densidad de electrones N por $cm^3$, pero exactamente en la posición x no podemos calcular cuantos hay; el artificio que se usa consiste en considerar un elemento infinitesimal (muy corto pero no nulo) de longitud $\operatorname dL$, que empieza en la posición x y termina en la posición x+dL, que tendrá un volumen infinitesimal dV=S·dL (donde S es el área de la sección transversal del cable), y por tanto un número de electrones N·dV=NS·dL. Entonces aproximamos el número de electrones en la posición x por NS·dL.

### Relación con la derivación de funciones

Nos podemos encontrar también con que a veces se relacione el cociente de diferenciales con la derivación. Para la descripción matemática de la derivada podemos consultar mi post [Cálculo ->Funciones derivables → Introducción al estudio local de una función](http://tallermatematic.ovh/wp/?p=461), del que reproduzco aquí un párrafo:

![derivada-incrementos](/assets/images/derivada-incrementos.png)

Ejemplo 5:  La intensidad de corriente se define como la cantidad de carga que pasa por una sección S por unidad de tiempo, $I=\frac{\triangle q}{\triangle t}$, si la intensidad es variable, entonces se define en un intervalo de tiempo infinitesimal, tan corto que podemos considerar que la intensidad es prácticamente constante ("no la da tiempo" a cambiar), o sea $I=\frac{\operatorname dq}{\operatorname dt}$.

Ejemplo 6: siguiendo con el ejemplo 5 del cable eléctrico, la carga que está contenida en una sección de longitud L y sección S, teniendo una densidad de N electrones por $m^3$, será $eNSL$, siendo *e* la carga del electrón.  Entonces la intensidad será

$I=\frac{\operatorname dq}{\operatorname dt}=\frac{\operatorname d\left(eNSL\right)}{\operatorname dt}=\frac{eNS\operatorname dL}{\operatorname dt}=eNSv$

 Fijémonos que la diferencial de $eNSL$ se ha igualado a $eNS·dL$, pues no estamos considerando intervalos en la magnitudes *e* (una constante universal) ni *N* o *S* (constantes del cable) sinó solo de *L* (un desplazamiento longitudinal).