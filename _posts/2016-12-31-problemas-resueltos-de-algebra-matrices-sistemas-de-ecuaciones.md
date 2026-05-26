---
layout: post
title: "Problemas resueltos de Álgebra -> Matrices, Sistemas de ecuaciones"
date: 2016-12-31 11:51:15 +0000
categories:
  - "Álgebra"
  - "Matemáticas"
tags:
  - "imagen"
  - "matriz de una aplicación"
  - "núcleo"
  - "rango"
  - "subespacio vectorial"
math: true
---
{% raw %}

**1** - Dada la aplicación lineal f con matriz A en bases canónicas dada por

![matriu](/assets/images/matriu.png)

Determinar una base de los subespacios núcleo e imagen de f.

**Solución**:
Interesa saber las dimensiones de los subespacios núcleo e imagen de f, para saber cuantos vectores tiene cada base, así como las ecuaciones que identifican a sus vectores. Recordemos que el rango de la matriz de la aplicación lineal coincide con la dimensión del subespacio imagen de f, por tanto determinemos el rango de A; lo haremos por el método del pivote (una alternativa es por determinantes y menores de la matriz), usando una hoja de cálculo para quitarnos el trabajo pesado:

![matriu2](/assets/images/matriu2.png)

En cada paso o bien se escoge un elemento como "pivote" (marcado en negrita) para anular los elementos que tiene debajo, o bien se simplifican filas enteras dividiendo sus elementos por un divisor común. Vemos que quedan 3 filas con ceros, y la matriz final tiene 5 filas independientes, luego el rango es 5, y la dimensión del subespacio imagen también es 5; de forma inmediata deducimos que la dimensión del subespacio núcleo ha de ser 3, pues la dimensión de la matriz es de 8 (la aplicación es un endomorfismo de *R*⁸).

Seguimos reduciendo la matriz, que ahora es de 5 filas por 8 columnas, por el método del pivote:

![matriu3](/assets/images/matriu3.png)

Encontremos ahora las ecuaciones que nos determinan el subespacio núcleo, pues es más sencillo empezar con el subespacio núcleo que con la imagen; en efecto, las ecuaciones del núcleo son A**x** = **0**,  donde **x** es un vector de *R*⁸ y **0** es el vector nulo, si transformamos las ecuaciones por el método del pivote, el término independiente 0 no cambia, por tanto si llamamos Â a la matriz reducida, la ecuación matricial del núcleo es Â**x** = **0**. Las ecuaciones del subespacio imagen son A**x** ≠ **0**, una desigualdad, más incómodas de trabajar.

Desarrollando Â**x** = **0 **por componentes:

$x_1=0; x_2-x_6+x_7-x_8=0; x_3-x_6+x_7=0;x_4-x_6-x_8=0;-x_5+x_7=0$

Nos quedan 7 incógnitas (pues $x_1$ queda determinada) y 4 ecuaciones, tenemos pues que elegir tres incógnitas como parámetros y poner las demás en función de éstas; sean $x_6, x_7, x_8$ los parámetros:

$\begin{array}{l}x_2=x_6-x_7+x_8\\x_3=x_6-x_7\\x_4=x_6+x_8\\x_5=-x_7\end{array}$ [1]

Estas son las ecuaciones del subespacio núcleo, como tiene dimensión 3, hay 3 "grados de libertad" para escoger las componentes, que son los 3 parámetros $x_6, x_7, x_8$. Vamos a dar algunos valores, escogidos inteligentemente de forma que generen vectores independientes, para obtener una base del subespacio núcleo:

 	- Tomando $x_6=1, x_7=0, x_8=0$, resulta que $x_2=x_3=x_4=1,x_5=0$, y obtenemos el vector **u** = (0, 1, 1, 1, 0, 1, 0, 0).

 	- Tomando $x_6=0, x_7=1, x_8=0$, resulta que $x_2=x_3=-1,x_4=0,x_5=-1$, y obtenemos el vector **v** = (0, -1, -1, 0, -1, 0, 1, 0).

 	- Tomando $x_6=0, x_7=0, x_8=1$, resulta que $x_2=1,x_3=0,x_4=1,x_5=0$, y obtenemos el vector **w** = (0, 1, 0, 1, 0, 0, 0, 1).

Por tanto, una base del subespacio núcleo es {(0, 1, 1, 1, 0, 1, 0, 0), (0, -1, -1, 0, -1, 0, 1, 0), (0, 1, 0, 1, 0, 0, 0, 1)}.

Con la hoja de cálculo es fácil comprobar este resultado, usando las funciones de producto de matrices, por ejemplo comprobamos que A**u** = **0**:

![matriu4](/assets/images/matriu4.png)

Para encontrar una base del subespacio imagen necesitamos 5 vectores que sean linealmente independientes entre sí, y que no cumplan las ecuaciones [1], o sea, queA**x** ≠ **0**. Podemos tomar los vectores de la base del núcleo y cambiar adecuadamente alguna componente,  por ejemplo:

 	- **u** = (0, 1, 1, 1, 0, 1, 0, 0) -> cambiamos $x_5$, **u**' = (0, 1, 1, 1, 1, 1, 0, 0), cambiamos $x_4$, **u**'' = (0, 1, 1, 0, 0, 1, 0, 0)

 	- **v** = (0, -1, -1, 0, -1, 0, 1, 0) -> cambiamos $x_5$, **v'** = (0, -1, -1, 0, 0, 0, 1, 0), cambiamos $x_4$, **v**'' = (0, 1, 1, 1, -1, 1, 0, 0)

 	- **w** = (0, 1, 0, 1, 0, 0, 0, 1) -> cambiamos $x_5$, **w'** = (0, 1, 0, 1, 1, 0, 0, 1)

Si lo hemos hecho bien, los vectores serán linealmente independientes entre sí, y con los cambios que hemos hecho, no pertenecerán al subespacio núcleo, formando una base del subespacio imagen:

{(0, 1, 1, 1, 1, 1, 0, 0), (0, 1, 1, 0, 0, 1, 0, 0), (0, -1, -1, 0, 0, 0, 1, 0), (0, 1, 1, 1, -1, 1, 0, 0), (0, 1, 0, 1, 1, 0, 0, 1)}

Si queremos estar seguros de que forman base, lo podemos comprobar viendo el rango de la matriz formada por los vectores u', u'', v', v'', w', por ejemplo, usando la función *row reduce* de [Wolfram Alpha](http://www.wolframalpha.com) (situamos los vectores por filas):

![matriu5](/assets/images/matriu5.png)

Vemos que ninguna fila se anula, luego el rango es 5, los cinco vectores son linealmente independientes entre sí.

![separador2](/assets/images/separador2.png)
{% endraw %}