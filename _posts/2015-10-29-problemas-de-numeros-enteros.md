---
layout: post
title: "Problemas de números enteros"
date: 2015-10-29 20:27:22 +0000
math: true
---
{% raw %}

**1.** ¿Cuál es el dígito correspondiente a las unidades del número 7²⁰¹⁴? Por ejemplo, el dígito correspondiente a las unidades del número 56789 es el 9. Ayuda: siendo 7²⁰¹⁴ demasiado grande para usar la calculadora, hay que utilizar la propiedades de las potencias de números enteros, concretamente una que dice así: *el dígito de las unidades para las potencias sucesivas de cualquier número entero toma siempre unos valores determinados de forma cíclica*; por ejemplo: 4¹ = 4, 4² = 16, 4³ = 64, 4⁴ = 256, 4⁵ = 1024, ... vemos que para las potencias de 4 las unidades siempre son o 4 o 6.

Solución: Tenemos que encontrar los valores que toman las unidades para las potencias sucesivas de 7, buscando un patrón repetitivo:

	- 7¹ = 7

	- 7² = 49

	- 7³ = 343

	- 7⁴ = 2401

	- 7⁵ = 16807

	- 7⁶ = 117649

	-  . . .

Vemos que la secuencia de valores distintos de las unidades es 7, 9, 3, 1, y después se repiten sucesivamente los valores. Entonces, para el número 7²⁰¹⁴, ¿cuál de esos valores tomará? Son 4 valores distintos, cada valor de las unidades aparece en unas potencias determinadas, que son:

	- unidades = 7: potencias 7¹, 7⁵, 7⁹, 7¹³, ...

	- unidades = 9: potencias 7², 7⁶, 7¹⁰, 7¹⁴, ...

	- unidades = 3: potencias 7³, 7⁷, 7¹¹, 7¹⁵, ...

	- unidades = 1: potencias 7⁴, 7⁷, 7¹¹, 7¹⁵, ...

Cada valor de la unidad tiene una sucesión aritmética de potencias asociada. Es fácil ver que los términos generales son, respectivamente:

	- unidades = 7: potencias 1+4(n-1), n=1,2,...

	- unidades = 9: potencias 2+4(n-1), n=1,2,...

	- unidades = 3: potencias 3+4(n-1), n=1,2,...

	- unidades = 1: potencias 4+4(n-1), n=1,2,...

¿En cuál de estas sucesiones está la potencia 7²⁰¹⁴? Probamos una por una:

	- la del 7) 2014 = 1+4(n-1) => n resulta ser no entero, descartado

	- la del 9) 2014 = 2+4(n-1) => n = 504

	- la del 3) 2014 = 3+4(n-1) => n resulta no ser entero, descartado

	- la del 1) 2014 = 4+4(n-1) => n resulta no ser entero, descartado

O bien, más rápido, viendo que todas las sucesiones van de 4 en 4, dividimos por 4 el número 2014 y nos fijamos en el resto de la división:

$\begin{array}{l}2014\;\;\;\;\left|\underline{4\;\;\;\;\;}\right.\\\;\;\;\;\;\;2\;\;\;\;\;503\end{array}$

Como el resto es 2, pertenece a la segunda sucesión, la del primer término igual a 2. En conclusión, las unidades de 7²⁰¹⁴ son: 9.

![separador2](/taller-matematicas/assets/images/separador2.png)

**1.** ¿Cuál es el dígito correspondiente a las unidades del número 1234²⁰¹⁴?

Solución: aplicar el método del problema anterior directamente es poco recomendable, pues las potencias de 1234 crecen demasiado rápidamente.  Nos fijamos en cómo se calculan las potencias sucesivas con multiplicaciones; para 1234² = 1234 x 1234 resulta:

![unitats](/taller-matematicas/assets/images/unitats.png)

Vemos que las unidades de 1234² se obtienen tomando las de 4 x 4. Para las potencias sucesivas de 1234 tenemos lo mismo: sólo tenemos que considerar el 4. Busquemos pues el patrón de las potencias de 4:

	- 4¹ = 4

	- 4² = 16

	- 4³ = 64

	- 4⁴ = 256

	- . . .

Vemos que simplemente el patrón es: para potencias impares las unidades son 4, y para las pares son 6. Por tanto las unidades de 1234²⁰¹⁴, siendo la potencia 2014 par, es 6.

![separador2](/taller-matematicas/assets/images/separador2.png)

**3.** ¿Cuantas cifras tiene el número 7²⁰¹⁴?

 Solución: en el sistema decimal cada cifra de un número se multiplica por una potencia de 10 para obtener el número dado; por ejemplo, el número 3456 es igual a 3 x 103 + 4 x 102 + 5 x 101 + 6 x 100. Entonces la cantidad N de cifras que contiene un número dado puede obtenerse dividiendo el número por 10 repetidamente, hasta que el cociente sea menor que 1:

![division_consecutiva](/taller-matematicas/assets/images/division_consecutiva.png)

Como hemos hecho cuatro divisiones, el número tiene 4 cifras. Otra forma de verlo es: si un número tiene 4 cifras, entonces podemos dividirlo como máximo por 103, para obtener un cociente mayor que 1, en efecto, 3456 / 103 = 3, pero 3456 / 104 = 0. En general:
Dado un número entero X, su número de cifras decimales N es el número para el que se cumple X / 10N ≥ 1 y además X / 10(N+1) < 1.
Si aplicamos esta regla al número 7²⁰¹⁴ obtenemos  7²⁰¹⁴ / 10N ≥ 1 , 7²⁰¹⁴ /10(N+1)  < 1.Para la segunda inecuación obtenemos, inviertiéndola,  10(N+1) / 7²⁰¹⁴ > 1, tomando logaritmos decimales:

$\begin{array}{l}\log\left(\frac{10^{(N+1)}}{7^{2014}}\right)\;\;\;\;&gt;\;\log\left(1\right)\Leftrightarrow\\\log\left(10^{(N+1)}\right)-\log\left(7^{2014}\right)&gt;0\Leftrightarrow\\\left(N+1\right)\cdot\log\left(10\right)-2014\cdot\log\left(7\right)&gt;0\Leftrightarrow\\N+1&gt;2014\cdot\log\left(7\right)\Leftrightarrow\\N&gt;2014\cdot\log\left(7\right)-1\approx1701,03\end{array}$

Por tanto el número  7²⁰¹⁴  tiene N = 1702 cifras decimales.

![separador2](/taller-matematicas/assets/images/separador2.png)
{% endraw %}