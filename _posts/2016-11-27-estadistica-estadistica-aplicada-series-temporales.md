---
layout: post
title: "Estadística -> Estadística Aplicada -> Series Temporales"
date: 2016-11-27 10:09:39 +0000
categories:
  - "Estadística aplicada"
  - "Matemáticas"
tags:
  - "autocorrelación"
  - "cambios cíclicos"
  - "ciclos seriales"
  - "correlación serial"
  - "estacionalidad"
  - "estacionariedad"
  - "media móvil"
  - "serie temporal"
  - "suavización de la serie"
  - "tendencia de la serie"
math: true
---
{% raw %}

**

### Series temporales, tendencia, estacionalidad

Las **series temporales** (de datos estadísticos) relacionan eventos parecidos acaecidos en diferentes épocas, buscando detectar algún patrón de comportamiento, alguna tendencia, que permita hacer predicciones futuras.

**Ejemplo 1**: Comparar las importaciones y exportaciones anuales de una empresa en los últimos 15 años, comparándolas, analizando su evolución temporal.

Puede ser un problema complicado, ya que frecuentemente sucede que las sucesivas observaciones no son independientes entre sí, como por ejemplo las ventas de un comercio en un mes pueden no ser independientes de las ventas del mes anterior.

##### Las variables utilizadas en las series temporales

Hay variables estadísticas, que miden cantidades, de la que puede determinarse su valor, al menos en teoría, en cualquier momento del tiempo; por ejemplo, el número de parejas de hecho que residen en una cierta localidad. Es un número variable, pero puede hacerse un censo y determinar su número en un cierto día escogido obviando dificultades técnicas, quizá la población es demasiado numerosa para completar el censo en un sólo día, pero no es una limitación de base, sino una de recursos disponibles, de hecho, el número de parejas de hecho está claramente definido en cualquier hora de cualquier día.

Por otro lado, hay variables estadísticas que miden flujos o variaciones de otras cantidades, en las que siempre debemos determinar su valor en un intervalo de tiempo más o menos amplio; por ejemplo, el número de uniones de parejas en el juzgado en un día determinado puede ser cero, mientras que el día siguiente será mayor que cero. En éste último caso cogeremos un intervalo de tiempo suficientemente amplio y trataremos con "uniones civiles en el juzgado por día" por ejemplo, dividiendo por el número de días del período.

**Ejemplo 2:** Gráfico de ventas de unos grandes almacenes.

[caption id="attachment_1703" align="alignnone" width="602"]![Fig.1: gráficos de ventas, izquierda, anuales, derecha, trimestrales](/taller-matematicas/assets/images/serie_temporal1.png) Fig.1: gráficos de ventas, izquierda, anuales, derecha, trimestrales[/caption]
##### Tendencia general

A menudo los datos cuando se representan en intervalos largos de tiempo presentan una curva de evolución  suave, como en la figura 1 a la izquierda, que muestra las ventas totales de unos almacenes por años mostrando una tendencia general de crecimiento constante; en cambio los mismos datos tomados a intervalos de tiempo más cortos presentan fuertes oscilaciones, como vemos en la figura a la derecha, que muestra las ventas trimestrales en dos años consecutivos, no se ve una tendencia clara.

##### Estacionalidad

Al reducir el intervalo temporal, puede suceder que salgan a la luz influencias periódicas particulares que varían los datos en tiempos fijados, como por ejemplo campañas de Navidad, rebajas de agosto, influencia del turismo en ciertas épocas de cada año, etc; en este caso diremos que la serie temporal presenta estacionalidad. Hemos visto dos características importantes de las series temporales (de datos estadísticos): la tendencia general y las influencias periódicas.

##### Ciclos

Si representamos de nuevo el gráfico de ventas por meses, las oscilaciones aumentan, pero aún podemos observar la tendencia general ascendente, la estacionalidad (en el mes 6, junio, y en el 6+12 = 18, junio del año siguiente, las ventas presentan máximos) y la aparición de ciclos (cambios recurrentes a medio plazo), que son períodos en los que los datos presentan un aspecto parecido: en la figura 2 la estructura entre los meses 1 y 12 es algo semejante, pero incrementada, a la de los meses 13 a 24 del año siguiente.

[caption id="attachment_1704" align="alignnone" width="687"]![Fig. 2: tendencia general, estacionalidad y ciclos](/taller-matematicas/assets/images/serie_temporal2.png) Fig. 2: tendencia general, estacionalidad y ciclos[/caption]
##### Variaciones erráticas o aleatorias

Además de las causas anteriores de variabilidad, encontraremos en la práctica variaciones que no son debidas a ninguna de esas causas, y por ello las atribuiremos al azar.

Así pues, el modelo clásico de tratamiento de series temporales supone que las variaciones entre datos pueden explicarse por una, varias o todas estas fuentes de variación:

 	- una tendencia general

 	- una estacionalidad

 	- aparición de ciclos de variaciones

 	- variaciones aleatorias

### Análisis de series temporales

Las cuatro causas anteriores de variabilidad se combinan entre sí matemáticamente, formando un modelo teórico con el cual se pueden explicar los comportamientos del los datos y hacer predicciones. Los datos se procesan con un programa de Estadística, en el cual, en las opciones, deberemos indicar de que forma combinaremos las causas; los modelos caen en dos categorías:

 	- **Modelos estáticos**

 	**Modelo multiplicativo**: considera que la variabilidad total observada es el producto de las producidas por cada factor, o sea por la tendencia general, estacionalidad, etc

 	- **Modelo aditivo**: considera que la variabilidad total observada es la suma de las producidas por cada factor, o sea por la tendencia general, estacionalidad, etc

 	- **Modelos dinámicos**: las variaciones en el tiempo t se calculan tomando las variaciones de los factores en tiempos anteriores de la serie, t-1, t-2, etc.

Los modelos dinámicos contemplan una complicación típica de las series temporales que es la presencia de correlación serial o relaciones entre datos contiguos (la no independencia de datos que comentábamos); toda la Estadística en general se simplifica cuando los datos son independientes entre sí, y se complica cuando no lo son. Un ejemplo en el que podemos esperar encontrar correlación serial sería el caso de las ventas de los almacenes: después de un mes de ventas elevadas es posible inferir que las ventas pueden bajar debido a que los clientes habituales ya han hecho sus compras importantes el mes anterior y posiblemente no gasten mucho dinero en dos meses consecutivos. En cambio en una serie temporal mensual del número de turistas que visitan una ciudad, los turistas son independientes entre sí, no repiten la visita cada mes, así que no podemos inferir nada de la cantidad de turistas de un mes para el siguiente.

Otra complicación que puede aparecer es la presencia de valores inusuales, atípicos, denominados valores influyentes; cuando un evento extraordinario modifica la tendencia natural se producen estos valores singulares que nos pueden llevar a un análisis erróneo si no los detectamos y aislamos.

Por suerte, los programas estadísticos proporcionan "filtros" para detectar, dados los datos de una serie temporal, su tendencia general, estacionalidad, periodicidad, sus ciclos, sus correlaciones seriales y sus valores influyentes.

### Determinación de la tendencia por regresión, suavización de la serie, detección de ciclos: ejemplo práctico

Consideremos los datos de tasa de paro en España entre los años 1978 y 2013, que reproducimos parcialmente:

| Año** 
| **Tasa** 

| 1978 
| 7 

| 1979 
| 9 

| 1980 
| 12 

| 1981 
| 14 

| 1982 
| 16 

| 1983 
| 18 

| 1984 
| 21 

| 1985 
| 22 

(...)

| 2008 
| 13,9 

| 2009 
| 18,1 

| 2010 
| 20 

| 2011 
| 21,7 

| 2012 
| 25,1 

| 2013 
| 26,3 

Observamos la gráfica de puntos de la serie:

[caption id="attachment_1708" align="alignnone" width="685"]![Fig.3: gráfica de serie temporal](/taller-matematicas/assets/images/serie_temporal3.png) Fig.3: gráfica de serie temporal[/caption]
La línea roja marca la media de todos los datos; vemos que los valores parecen oscilar en torno a la media, aunque la oscilación se hace mayor en los últimos años; cuando se observa esta oscilación en torno a la media, decimos que la serie presenta **estacionariedad **en media. Además, la serie parece presentar cierta pauta de variación, hay unos mínimos muy parecidos en los años 70 y en el 2005, y unos máximos en los años 80 y 90, así que podemos pensar que la serie presenta **cambios** **cíclicos** (no estacionalidad, pues no se aprecia repetición de pauta en años concretos, más bien son cambios a medio-largo plazo).

Observamos ahora el gráfico de las desviaciones respecto a la media, obtenidas haciendo las diferencias $X_t-\overline{X_t}$ para cada dato de la serie:

[caption id="attachment_1709" align="alignnone" width="675"]![Fig. 4: Gráfica de desviaciones respecto de la media total](/taller-matematicas/assets/images/serie_temporal4.png) Fig. 4: Gráfica de desviaciones respecto de la media total[/caption]
De nuevo vemos que hay una oscilación de las desviaciones en torno del valor cero, oscilación que se amplifica en los últimos años (quizá debido a la crisis financiera del 2008 y siguientes): hay una estacionariedad en la desviación respecto de la media.

Para concretar si las variaciones observadas son cíclicas y/o estacionarias, interesa quitar de la serie las oscilaciones aleatorias y eliminar, si la hay, la tendencia general (si hay por ejemplo una tendencia general al aumento de la tasa de desempleo, se hace más difícil ver las oscilaciones de cada período). A este proceso le denominamos **suavizar la serie. **

El primer paso será determinar la tendencia de la serie, hay dos métodos para hacerlo, en el primero se usa **regresión** para ajustar una curva a la gráfica de la serie temporal:  en la hoja de cálculo hacemos clic-derecho sobre la gráfica de la serie y escogemos agregar línea de tendencia, que puede seguir diversos modelos matemáticos: lineal, logarítmico, polinómico, etc. Hay que ensayar algunos, observando para cada prueba el coeficiente de determinación, por ejemplo:

[caption id="attachment_1710" align="alignnone" width="686"]![Fig 5: tendencia lineal y polinómica de grado 3 para la serie temporal](/taller-matematicas/assets/images/serie_temporal5.png) Fig 5: tendencia lineal y polinómica de grado 3 para la serie temporal[/caption]
En la figura 5 se ha ensayado ajuste lineal, con un coeficiente R² muy bajo, del 0.009, y polinómica de grado 3, con un coeficiente R² bastante bueno, 0,69; se presenta también la ecuación del ajuste polinómico. No es necesario un ajuste muy bueno, sólo queremos captar la tendencia general, así que daríamos por aceptable el ajuste polinómico. Un economista podría sugerirnos que esa tendencia está siguiendo alguno de los [ciclos económicos](https://es.wikipedia.org/wiki/Ciclo_econ%C3%B3mico), vemos que hay un máximo de paro laboral en 1988 y otro en 2014, y hay mínimos en 1978 y en 2004, con un intervalo entre máximos y mínimos de unos 25 años; los máximos de paro podrían achacarse a la [reconversión industrial del los años 80](https://es.wikipedia.org/wiki/Reconversi%C3%B3n_industrial), y a a incorporación a la Comunidad Económica Europea (1986) que obligó a un proceso culminante de desmantelamiento industrial a partir de 1986, y a [la crisis financiera del 2008 y siguientes](https://es.wikipedia.org/wiki/Crisis_financiera_de_2008).

[caption id="attachment_150313" align="alignnone" width="498"]![serie_temporal6](/taller-matematicas/assets/images/serie_temporal6.png) Fig. 6: la línia en rojo representa la serie de datos a la que se ha restado la curva de tendencia[/caption]
 En la figura 6 hemos restado de la serie de datos original la tendencia, el resultado es la serie representada por puntos rojos; las oscilaciones ahora están en torno al valor cero, y son de más corto plazo que las anteriores: cada cinco años, aproximadamente, que coinciden con otro ciclo económico: el [ciclo de Kitchin](https://es.wikipedia.org/wiki/Ciclo_de_Kitchin), debido a oscilaciones en la producción de las empresas y sus ajustes a la demanda real. Al restar la tendencia hemos supuesto que la serie se ajusta bien al modelo sumativo, que supone que la variabilidad total observada es la suma de las producidas por cada factor, o sea por la tendencia general, estacionalidad, etc.

### Correlación serial, determinación de la tendencia por el método de las medias móviles: ejemplo

Siguiendo con los datos del paro en España,  como sospechamos que puede haber una **correlación serial** (la tasa de paro de cada año condiciona la del año siguiente, pues es un índice que no se cambia fácilmente de un año para otro) calculamos el **coeficiente de correlación serial** definido como

$r=\frac{\text{cov}\left(X_t,X_{t-1}\right)}{S_{X_t}\cdot S_{X_{t-1}}}$ [1]
donde $X_t$ son los datos en el período t, y  $X_{t-1}$ son los datos en el año anterior:
  

| **Año** 
| **Xt** 
| **Xt-1** 

| 1978 
| 7 
| - 

| 1979 
| 9 
| 7 

| 1980 
| 12 
| 9 

| 1981 
| 14 
| 12 

(...)
  

| 2010 
| 20 
| 18,1 

| 2011 
| 21,7 
| 20 

| 2012 
| 25,1 
| 21,7 

| 2013 
| 26,3 
| 25,1 

| 2014 
| - 
| 26,3 

La $\text{cov}\left(X_t,X_{t-1}\right)$ es la covarianza de las dos variables, y las S son sus desviaciones típicas, resulta: $S_t=4,94$, $S_{t-1}=5,11$, Cov = 23,39, autocorrelación = **0,93. **La autocorrelación, que se interpreta igual que la [correlación de Pearson](https://es.wikipedia.org/wiki/Coeficiente_de_correlaci%C3%B3n_de_Pearson#Interpretaci.C3.B3n), es muy alta, del 93%, confirmando nuestra suposición de que la tasa de un año influye en la siguiente. Las causas principales de autocorrelación son las tendencias o ciclos, así que en este segundo análisi de los datos también llegamos al mismo punto: parece que las variaciones en la tasa de desempleo son cíclicas en el tiempo.

Para determinar los ciclos procedemos como antes: hay que determinar la tendencia de la serie y proceder a suavizarla.  Para determinar la tendencia ya hemos visto que podemos hacerlo por regresión, pero ahora lo haremos con un método alternativo: el de las **medias móviles**. Consiste en sustituir los datos originales por las medias de 2 datos correlativos (medias móviles de orden 1), de 3 datos (medias móviles de orden 2), etc. Reproducimos algunas de esas medias en la siguiente tabla, donde "media movil-2" significa media de dos datos (media de orden 1), "media movil-3" significa media de tres datos (media de orden 2), etc.:

 

| **Año** 
| **Tasa** 
| **media móvil-2** 
| **media móvil-3** 
| **media móvil-4** 

| 2013 
| 26,3 
|  
|  
|  

| 2012 
| 25,1 
| 25,7 
|  
|  

| 2011 
| 21,7 
| 23,4 
| 22,9 
|  

| 2010 
| 20 
| 20,9 
| 20,2 
| 23,3 

| 2009 
| 18,1 
| 19,1 
| 17,9 
| 21,2 

| 2008 
| 13,9 
| 16,0 
| 16,1 
| 18,4 

| 2007 
| 8,3 
| 11,1 
| 14,7 
| 15,1 

| 2006 
| 8,1 
| 8,2 
| 13,6 
| 12,1 

| 2005 
| 9,2 
| 8,7 
| 12,8 
| 9,9 

| 2004 
| 10,4 
| 9,8 
| 12,3 
| 9,0 

Lógicamente, a medida que vamos aumentando el orden de la media móvil, tenemos menos datos, pasando de los *N* originales a *N-1* medias de orden 1, *N-2* de orden 2, ... *N-m* de orden m.

En la figura 7 vemos estas series de medias moviles. Si nos fijamos en las medias de orden 3, la línia roja, y la comparamos la tendencia polinómica de grado 3 de la figura 5 veremos que coinciden mucho: las medias de orden 3 son una buena aproximación a la tendencia de esta serie.

[caption id="attachment_150314" align="alignnone" width="498"]![Fig. 7: representación de las series de medias móviles](/taller-matematicas/assets/images/serie_temporal7.png) Fig. 7: representación de las series de medias móviles[/caption]
A partir de aquí procederíamos como en la sección anterior: restando la tendencia (las medias móviles de orden 3) de los datos de la serie original para obtener la serie suavizada.

### Conclusión

Este artículo es sólo una breve introducción práctica al estudio de las series temporales, presentando los aspectos básicos. En el estudio de las series de datos en el tiempo interesa analizar sus variaciones para detectar sus posibles causas, normalmente interesa reducir esas variaciones (tasa de empleo constante, por ejemplo) o bien mantenerlas siempre positivas (aumento continuo de las ventas), e incluso, más difícil, hacer predicciones de futuro.
{% endraw %}