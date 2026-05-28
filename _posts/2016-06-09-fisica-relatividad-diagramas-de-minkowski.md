---
layout: post
title: "Física - > Relatividad -> Diagramas de Minkowski"
date: 2016-06-09 15:22:21 +0000
categories:
  - "Fí­sica"
  - "Mecánica relativista"
tags:
  - "Lorentz"
  - "Minkowski"
  - "referencia inercial"
math: true
---
{% raw %}

Las transformaciones de Lorentz pueden ser a veces algo laboriosas de utilizar en cierto problemas, dando lugar a largos cálculos; H. Minkowski introdujo en 1908 unos diagramas en donde se representa el espacio-tiempo de forma que permite obtener las transformaciones de Lorentz de forma gráfica. En el eje de abscisas se representa el espacio unidimensional, *x*, y en el eje de abscisas el tiempo, pero multiplicado por *c*.

![](/taller-matematicas/assets/images/Minkowski1b.png)
Para resolver transformaciones de Lorentz entre dos sistemas inerciales S y S', éste último moviéndose a velocidad v con respecto al primero, se considera que los ejes *x, ct* de S son rectangulares, y en ese caso los ejes x', ct' de S' serán oblicuos. La línea punteada en la figura 1 representa la trayectoria en el espacio-tiempo de una señal luminosa que en el tiempo $t = 0$ parte del origen de coordenadas, y es la bisectriz de los ejes x, ct, pues la luz recorre en un tiempo ct = 1 -> t = 1/c una distancia x = c·t = c/c = 1, de hecho se escoge la escala de tiempos ct por esta razón.

Además, cualesquiera otros ejes x', ct' relacionados con una referencia S' que se mueve a velocidad v < c tendrán también como bisectriz a la línea punteada de la señal luminosa, ya que c es la misma para todos los sistemas de referencia. Como mayor sea v, más cercanos estarán los ejes x' , ct' la la línea bisectriz. En efecto, en un tiempo ct = 1 -> t = 1/c el sistema S' recorrerá una distancia x = vt = v/c; el ángulo $theta$ entre el eje ct' y el eje x cumplirá

$tanleft(thetaright)=frac1{v/c}=frac cv$ [1]

Supondremos que en $t=0$ los orígenes de ambos sistemas de referencia coinciden. Siendo c la velocidad límite, cualquier otra referencia móvil tendrá unos ejes más cercanos a la bisectriz.

**Ejemplo 1**: Si el sistema de referencia S' se mueve a v = c/2 con respecto a S', entonces

$theta=tan^{-1}left(frac c{c/2}right)=tan^{-1}left(2right)=63.4^text o$

Aunque para dibujar los ejes es más sencillo simplemente dibujar primero ct' usando la ratio "una unidad según el eje de abscisas corresponde a 1/2 del eje de ordenadas".


En general, si S' se mueve a velocidad v, entonces su recta ct' pasará por los puntos (0, 0) y (v/c, 1). En cuanto a la recta x', pasará por los puntos (0, 0 ) y (1, v/c). No es necesario calcular el ángulo $theta$ para dibujarlos. En la figura 3 vemos un S' con v=c/2 y otro S'' con v=c/3.

### Unidad de medida en las referencias móviles

Es importante recordar que la escala de los ejes no es la misma para la referencia S que para las S', S'', etc. No podemos usar la misma regla de medir en S que en los demás sistemas. Para definir la distancia unidad en cada referencia se usa el denominado **invariante espacio-tiempo**:

$x^2-left(ctright)^2=1$ [2]

Haciendo una tabla de valores (x, ct) para esta ecuación, encontramos los puntos que la cumplen, que resultan formar una hipérbola (en amarillo en la figura 3):

| **x** 
| **ct** 

| 1 
| 0 

| 1,1180339887 
| 0,5 

| 1,4142135624 
| 1 

| 1,8027756377 
| 1,5 

| 2,2360679775 
| 2 

| 2,6925824036 
| 2,5 

| 3,1622776602 
| 3 


Vemos que la hipérbola corta al eje x en el punto 1, use acerca asintóticamente a la línea espacio-tiempo de la luz; *los puntos de corte con los ejes x', x'', etc, de las otras referencias determinan la unidad de longitud en esas referencias vistas desde la referencia x en reposo*. Claramente se ve que la longitud unidad, en cualquier sistema en movimiento, vista desde el reposo, es mayor que la unidad del sistema en reposo, tendiendo a infinito para referencias que se muevan a velocidades cercanas a la de la luz, esto es una consecuencia de la fórmula de la contracción de longitudes de Lorentz:

$triangle x=gammatriangle x'=gammacdot1xrightarrow{vrightarrow c}infty$

**Ejemplo 2**: Si el sistema de referencia S' se mueve a v = c/2 con respecto a S', dibujar la hipérbola de calibración para obtener la distancia equivalente a x = 2 en el sistema S' en el instante t = 0.


Con la hipérbola obtenemos su punto de corte del eje x', la distancia entre el origen y ese punto será la distancia unidad, la duplicamos sobre el eje x' para llegar al punto A' de coordenadas en el sistema S' (x'=2, t' = 0).

**Ejemplo 3**: con los mismos sistemas S, S' del ejemplo anterior, situar en el diagrama los sucesos A: x = 1, ct = 1 y B: x' = 1, ct' = 1.


 El punto A es inmediato: estará sobre la línea espacio-tiempo de la luz. Para el punto B usamos la hipérbola de calibración que nos da la coordenada (x'=1, ct'=0) sobre el eje x'. Esta misma distancia la medimos sobre el eje ct' (con una regla o la trasladamos con un compás) para obtener el punto (x'=0, ct'=1); entonces trazamos por estos puntos paralelas a los ejes (líneas punteadas en rojo en la figura), la intersección de estas líneas nos da el punto B(x'=1, ct'=1).

**Ejemplo 4**: Mediante el diagrama obtener las coordenadas en S' del punto A, y las coordenadas en S del punto B del ejemplo anterior.


Para el punto A trazamos paralelas a los ejes x', ct', los puntos de corte con esos ejes (rombos azules en la figura) nos dan las coordenadas, vemos que son, aproximadamente, x' = 0.6 (recordar que hay que comparar con la unidad de longitud en el sistema S', dada por la hipérbola de calibración) y ct' = 0.5. Si trazamos el gráfico en papel milimetrado y usamos herramientas de dibujo lineal la precisión mejorará bastante.

Para el punto B trazamos paralelas a los ejes x,  ct, obtenemos aproximadamente x = 1.6, ct = 1.6.

Para comparar procedimientos y comprobar resultados, vamos a calcular las coordenadas analíticamente. Para pasar de A: x = 1, ct = 1 a una referencia que se mueve a velocidad v = 0.5c usamos:

$begin{array}{l}gamma=left(1-frac{v^2}{c^2}right)^{-1/2}=left(1-frac{left(c/2right)^2}{c^2}right)^{-1/2}=left(frac34right)^{-1/2}=frac2{sqrt3};\x'=gammaleft(x-vtright)=frac2{sqrt3}left(1-0.5ccdotfrac1cright)=frac1{sqrt3}approx0.58;\t'=gammaleft(t-vx/c^2right)=frac2{sqrt3}left(frac1c-0.5ccdot1/c^2right)=frac1{csqrt3}approxfrac{0.58}cend{array}$

Recordemos que en el diagrama de Minkowski el tiempo viene multiplicado por c; así, el valor ct = 1 implica que t = 1/c. De la misma forma, en el resultado final para t', si multiplicamos por c para obtener ct', el resultado es el mismo que en el diagrama, $ct'=frac{ccdot0.58}c=0.58$.

**Ejemplo 5**: El siguiente diagrama representa una nave espacial moviéndose a velocidad v = 0.5c, en el punto-suceso A se produce una explosión, propagándose la radiación en todas direcciones a velocidad c. La nave despliega un escudo anti-radiación en el punto-suceso B. La pregunta que nos hacemos es, ¿cuando la radiación alcance la nave, estará protegida por el escudo, o por el contrario lo habrá desplegado demasiado tarde?


La radiación viajará a velocidad c tanto en el sentido positivo como en el negativo; las dos trayectorias opuestas estarán a 90⁰ entre sí, y a 45⁰ con los ejes x, ct


La radiación que viaja en el sentido negativo de x alcanza al eje ct' en el punto marcado en rojo, ese punto tiene coordenada x'=0, lo que significa que la radiación ha alcanzado a la nave, pero además lo ha hecho un poco antes de que se despliegue el escudo (suceso B), por tanto la nave ha tenido mala suerte con este diagrama. Ejercicio para el lector: ¿cómo se resolvería este problema usando transformaciones de Lorentz?
{% endraw %}