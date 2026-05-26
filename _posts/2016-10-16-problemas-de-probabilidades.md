---
layout: post
title: "Problemas de probabilidades"
date: 2016-10-16 08:54:07 +0000
categories:
  - "Probabilidades"
tags:
  - "problemas probabilidades"
math: true
---

**1.** En una red local hay las conexiones mostradas en la figura, donde los números indican las probabilidades de que cada rama esté abierta en un cierto intervalo de tiempo dado. Suponiendo que las probabilidades son independientes entre sí, calcular la probabilidad de que haya transmisión de datos entre A y D por cualquier camino. Suponiendo que hay transmisión de datos entre A y D, calcular la probabilidad de que se esté transmitiendo por la ruta ACD.

[![graf_probabilitats](/assets/images/graf_probabilitats.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/04/graf_probabilitats.png)
 Para transmitir entre A y D hay tres caminos: ABD, AD, ACD; si cualquiera de ellos está abierto, hay comunicación entre A y D. ¿cuáles son las posibilidades?

 	- ABD abierto, AD y ACD cerrados

 	- AD abierto, ABD y ACD cerrados

 	- ACD abierto, ABD y AD cerrados

 	- ABD y AD abiertos, ACB cerrado

 	- ...

 	- ABD, AD y ACB abiertos

Vemos que hay bastantes posibilidades a considerar; en estos casos es conveniente pensar en el suceso contrario: ¿cuándo no habrá transmisión entre A y D? Sólo cuando ABD, AD y ACB estén todos cerrados. El camino ABD estará cerrado si AB lo está, o bien BD lo está; teniendo en cuenta que los sucesos son independientes, la probabilidad de "ABD cerrado" es:

$\begin{array}{l}\text{P}\left(\text{ABD cerrado}\right)\;=\text{P}\left(\text{AC cerrado}\cup\text{CD cerrado}\right)\;=\text{P}\left(\text{AC cerrado}\right)+\text{P}\left(\text{CD cerrado}\right)\text{-P}\left(\text{AC cerrado}\cap\text{CD cerrado}\right)=\\0.1+0.2-0.1\cdot0.2=0.28\end{array}$

ya que P(A cerrado) = 1 - P(A abierto) = 1 - 0.9, e idénticamente para B. La probabilidad de "ACD cerrado" es numéricamente la misma:

P(ACD $\;$ cerrado) = P(AC $\;$ cerrado $\cup$ CD $\;$ cerrado) = P(AC $\;$ cerrado) + P(CD $\;$ cerrado) - P(AC $\;$ cerrado $\cap$  CD $\;$ cerrado) = 0.2 + 0.1 - 0.2 = 0.28.

Entonces P(no se transmite entre A y D)=P(ABD, AD y ACB todos cerrados)  = P(ABD cerrado $\cap$ AD cerrado $\cap$ ACB cerrado) = P(ABD cerrado})·P(AD cerrado)·P(ACB cerrado) = 0.28·0.3·0.28 = 0.02352.

Por tanto P(se transmite entre A y D) = 1 - P(no se transmite entre A y D) = 1 - 0.02352 = 0.97648.

**NOTA**: puede ser didáctico realizar simulaciones de probabilidades con hoja de cálculo para verificar experimentalmente los cálculos. En este ejercicio es simple de hacer: usando la función *aleatorio()* que llevan todas las hojas de cálculo, y con la función lógica =*SI(condición; valor_si_cierto;valor_si falso*), se puede crear una hoja que presente el valor 1 siempre que el valor aleatorio esté en el intervalo $[0,p]$ siendo p las probabilidades dadas de la red:

| **AB** 
| **BD** 
| **AD** 
| **AC** 
| **CD** 

| 1 
| 1 
| 1 
| 0 
| 1 

| 1 
| 1 
| 1 
| 1 
| 1 

| 0 
| 0 
| 0 
| 0 
| 1 

| 1 
| 1 
| 1 
| 1 
| 1 

| 1 
| 1 
| 1 
| 1 
| 1 

| 1 
| 1 
| 1 
| 1 
| 1 

| 1 
| 1 
| 1 
| 1 
| 1 

| 1 
| 1 
| 1 
| 1 
| 1 

| 0 
| 1 
| 0 
| 1 
| 1 

Así, por ejemplo, la columna AB presenta un 1 siempre que en esa casilla se haya generado un valor aleatorio en el intervalo $[0, 0.9]$; cuando hay un 1 significa que la ruta AB está abierta, con un 0 está cerrada. Observad que los valores de esta tabla son binarios, con 1=cierto (hay transmisión), 0=falso (no hay transmisión).

Ampliamos ahora con más columnas:

 

| **AB y BD** 
| **AC y CD** 
| **(AB·BD)+AD+(AC·CD)** 

| 1 
| 0 
| 2 

| 1 
| 1 
| 3 

| 0 
| 0 
| 0 

| 1 
| 1 
| 3 

| 1 
| 1 
| 3 

| 1 
| 1 
| 3 

| 1 
| 1 
| 3 

| 1 
| 1 
| 3 

| 0 
| 1 
| 1 

En "AB y AD" multiplicamos las columnas AB por AD, en "AC y AD" lo mismo, pero en la columna (AB·BD)+AD+(AC·CD) al sumar no obtenemos un número binario: si éste valor es cero significa que no hay transmisión entre A y D (todo cerrado) y con un valor superior a cero hay transmisión entre A y D (alguna ruta abierta). Contando el número de celdas superiores a cero de ésta última columna y dividiendo por el número de filas obtenemos una estimación de la probabilidad pedida, tanto mejor como más filas haya. Con 1000 filas se obtienen valores del orden de 0.98.

[![separador2](/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

 **2.**  Se elige al azar un número de 3 bits $x_1x_2x_3$ donde $x_i=0$ o $x_i=1$. Definimos las variables aleatorias X: el número de ceros que tienen conjuntamente los dos primeros bits, Y: número total de unos entre los tres bits. Calcular la tabla de distribución conjunta de probabilidad de X,Y. ¿Cuál es la covarianza de X,Y?

 Para calcular las probabilidades conjuntas tenemos que saber primero las posibles combinaciones de valores, son: X puede valer {0, 1, 2}, Y puede valer {0, 1, 2, 3}. Por tanto tendremos 3·4 = 12 combinaciones de valores (X,Y), que son {(0,0), (0,1), (0,2), (0,3), ..., (2,2), (2,3)}.

Vamos por las probabilidades conjuntas: dado un suceso A de la variable X y un suceso B de la variable Y, la probabilidad conjunta de A y B es $P\left(A\cap B\right)=P(A\vert B)\cdot P(B)$, que será igual a $P(A)·P(B)$ sólo si A, B son sucesos independientes; en este caso, no podemos presuponer independencia entre X, Y, luego aplicamos la primera igualdad.

Veamos un ejemplo de cálculo: sea A el suceso X=1, B el suceso Y=2; la probabilidad condicionada P(X = 1 | Y = 2) se obtiene considerando todos los casos Y=2 y viendo en que proporción de ellos se cumple X=1.

Si Y=2 los bits $x_1x_2x_3={(1,1,0), (1,0,1), (0,1,1)}$, observando los dos primeros bits, vemos que en dos casos, ${(1,0,1), (0,1,1)}$, tenemos un cero en uno de los bits; luego la proporción de casos X=1 dentro de Y=2 es de 2/3.

Calculamos ahora la P(Y = 2) como la proporción de casos en que tenemos
2 unos respecto al total de combinaciones de los tres bits, que son 2³=8; la proporción es pues 3/8. Por tanto, $P\left(A\cap B\right)=\frac23\cdot\frac38=\frac28=\frac14.$ Por otro lado, la P(X = 1) se obtiene con la proporción de casos en que tenemos 1 cero en los dos primeros bits respecto al total de casos en esos dos primeros bits: {(1,0),(0,1),(1,1),(0,0)}, por tanto es P(X = 1) = 3/4. La probabilidad P(X = 1)·P(Y = 2) = 3/4 · 3/8 = 9/32 que es distinta de la obtenida para $P\left(A\cap B\right)$, luego los sucesos no son independientes.

Obviamente no vamos a hacer un cálculo tan largo para las otras 11 combinaciones (X,Y), lo abreviamos haciendo una discusión de casos simples:

 	- Si el número de unos es de 3 (Y=3), entonces no hay ningún cero, luego X debe valer cero con seguridad (X=1 con probabilidad 100%).

 	- Si el número de unos es de 0 (Y=0), entonces todos los bits son cero, luego X debe valer 2 con seguridad (X=2 con probabilidad 100%).

 	- El caso X=0, Y=0 es imposible (sucesos incompatibles), ya que X=0 implica que hay dos unos en los dos primeros bits, luego Y tiene que valer al menos 2; por tanto el caso X=0, Y=1 también es imposible.

 	- Si Y=2 hay un sólo cero en los tres bits, luego X no puede valer 2; tenemos que P(X = 2 | Y = 2) = 0.

 	- Si Y=1, los bits han de ser {(1,0,0), (0,1,0), (0,0,1)}; luego P(X = 1|Y = 1) = 2/3, P(X = 2|Y = 1) = 1/3.

Resumimos todo lo que tenemos en una tabla de probabilidades condicionadas P(X | Y), marcamos las casillas que hemos visto que tienen probabilidad 0 (sucesos incompatibles):

[caption id="attachment_997" align="alignnone" width="360"][![Probabilidades condicionadas P(X | Y)](/assets/images/conjunta1.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/04/conjunta1.png) Probabilidades condicionadas P(X | Y)[/caption]
Para obtener la tabla de probabilidades conjunta $P\left(A\cap B\right)$ usaremos la fórmula $P\left(A\cap B\right)=P(A\vert B)\cdot P(B)$ y algunas propiedades útiles:

 	- la suma de probabilidades por filas (distribución marginal de X) coincide con las probabilidades P(X),

 	- la suma de probabilidades por columnas (distribución marginal de Y) coincide con las probabilidades P(Y), y

 	- la suma total ha de ser 1.

Para aplicarlo, será útil tener la tabla de probabilidades para la variable Y:

 

| **Y** 
| 0 
| 1 
| 2 
| 3 

| **P(Y)** 
|  1/8 
|  3/8 
|  3/8 
|  1/8 

y también para la variable X:

 

| **X** 
| 0 
| 1 
| 2 

| **P(X)** 
| ¼ 
| ½ 
| ¼ 

Obtenemos la tabla conjunta X,Y:

[caption id="attachment_998" align="alignnone" width="497"][![Probabilidades conjuntas](/assets/images/conjunta2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/04/conjunta2.png) Probabilidades conjuntas[/caption]

Las casillas en azul se han obtenido aplicando las propiedades 1 y 2, no ha sido necesario el cálculo de probabilidades.

Para calcular la covarianza usamos la fórmula:

$Cov\left(X,Y\right)=\sum_x\sum_y\left(x-\mu_x\right)\left(y-\mu_y\right)P\left(x,y\right)$

Necesitamos los valores medios de las variables:

$\mu_x=\underset x{\sum x}\cdot P(x),\;\mu_y=\underset y{\sum y}\cdot P(y)$

Los obtenemos de las tablas de probabilidades para X e Y:
 

| **Y** 
| 0 
| 1 
| 2 
| 3 
|  

| **P(Y)** 
|  1/8 
|  3/8 
|  3/8 
|  1/8 
|  

| **Y·P(Y)** 
| 0 
| 0.375 
| 0.75 
| 0.375 
| **suma=1.5** 

|  
|  
|  
|  
|  
|  

| **X** 
| 0 
| 1 
| 2 
|  
|  

| **P(X)** 
|  1/4 
|  1/2 
|  1/4 
|   
|  

| **X·P(X)** 
| 0 
| 0.5 
| 0.5 
| **suma=1** 
|  

Los elementos que entran en el cálculo de la covarianza los disponemos también en forma de tabla:
 

|  
| **Y** 

| **X** 
| **0** 
| **1** 
| **2** 
| **3** 

| **0** 
| 0 
| 0 
| -0.0625 
| -0.1875 

| **1** 
| 0 
| 0 
| 0 
| 0 

| **2** 
| -0.1875 
| -0.0625 
| 0 
| 0 

La suma de todos ellos es la covarianza: -0.5, un valor negativo indica dependencia inversa:  valores de X  grandes implican pequeños valores de Y.

[![separador2](/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)