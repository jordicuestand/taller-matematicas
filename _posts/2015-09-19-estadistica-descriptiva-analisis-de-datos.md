---
layout: post
title: "Estadística descriptiva, análisis de datos"
date: 2015-09-19 10:56:42 +0000
categories:
  - "Estadística aplicada"
tags:
  - "centil"
  - "cuartil"
  - "datos agrupados"
  - "decil"
  - "desviación típica"
  - "desviación media"
  - "estadísticos"
  - "frecuencia absoluta"
  - "frecuencia relativa"
  - "Histograma"
  - "media"
  - "moda"
  - "percentil"
  - "recorrido"
  - "varianza"
math: true
---
{% raw %}

- Estadística: concepto, contenido, aplicaciones

 	- Concepto de población, muestra, individuo y variable estadística

 	- Clasificación de las variables estadísticas

 	- Distribución de frecuencias. representaciones gráficas

 	- Agrupación de datos en intervalos

 	- Estadísticos muestrales

[![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Estadística: concepto, contenido, aplicaciones

## Fenómenos y experimentos deterministas y aleatorios.

Los fenómenos y experimentos en los que hay definidos una causa y su efecto de forma determinista pueden, en principio, ser formulados con ecuaciones matemáticas exactas:

 	- *F = ma* Ley de Newton: dada una fuerza F y una masa m, determinamos su aceleración a.

 	- *V = IR* Ley de Ohm: dado un potencial V y una resistencia R, determinamos la intensidad de corriente I

 	- PV = nRT Ley de los gases perfectos: dadas la presión P, la temperatura T y el número de moles n de un gas, determinamos el volumen V del gas

 	- Etc...

En la realidad se presenta una variabilidad no predecible que da lugar a los fenómenos y experimentos con cierto grado de aleatoriedad:

 	- F = ma + E, donde E es el error experimental, variable en cada repetición del experimento, aleatorio, indeterminado a priori

 	- Lanzamiento de un dado (condiciones iniciales no controlables)

 	- Encuesta de opinión sobre una población (componente psicológico aleatorio)

 	- Electrón que pasa a través de una barrera de potencial (incertidumbre cuántica)

En los ejemplos anteriores el grado de aleatoriedad no es el mismo: en el primer ejemplo tenemos un comportamiento en principio exacto y determinado, F = ma, sólo que debido a errores de medición, de preparación del experimento, humanos, etc, los resultados realmente obtenidos no coinciden con la teoría: es el error experimental, que idealmente tiende a cero. En los ejemplos del dado y de la encuesta de opinión no conocemos ninguna ecuación que nos permita hacer predicciones, aunque quizá existan, pero son desconocidas, por tanto son experimentos totalmente aleatorios. El último ejemplo es distinto, la aleatoriedad es intrínseca al electrón, no puede haber ninguna ley determinista por la propia naturaleza del experimento.

## Estadística: objeto

**
La Estadística estudia los fenómenos aleatorios, midiendo las fuentes de variabilidad y permitiendo hacer predicciones sobre el comportamiento de un experimento aleatorio.

### Aplicaciones de la Estadística

**Estadística descriptiva**: a partir de los resultados de un número de repeticiones de un experimento aleatorio, obtenemos una descripción numérica resumida (parámetros estadísticos) y unos gráficos descriptivos.

[caption id="attachment_1342" align="alignnone" width="600"][![Resumir datos: parámetros y gráficos estadísticos ](/assets/images/grafic_est_descrip.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/grafic_est_descrip.png) Resumir datos: parámetros y gráficos estadísticos[/caption]
**Estadística matemática**: utiliza la teoría de la probabilidad y las herramientas del análisis matemático para elaborar modelos matemáticos probabilistas que describen el comportamiento del fenómeno aleatorio en estudio.

**Inferencia estadística**: a partir de un número limitado de experimentos aleatorios elabora una estimación del comportamiento del fenómeno en general. Por ejemplo, sabiendo, por datos históricos, que el número medio de accidentes laborales en un año en cierto polígono industrial es de 3 accidentes, calcular la probabilidad de que ocurra al menos un accidente antes del mes de junio del año actual.

[caption id="attachment_1343" align="alignnone" width="619"][![De los datos experimentales a las predicciones](/assets/images/inferencia_esquema.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/inferencia_esquema.png) De los datos experimentales a las predicciones[/caption]
**Control de calidad y de fiabilidad**: utilizando una muestra de la producción, realiza inferencia sobre las calidad de toda la producción siguiendo un conjunto estándar de normas.

### Fases de un trabajo estadístico

Típicamente, en un estudio estadístico pasamos por las siguientes fases de trabajo:

 	- Recogida de datos (laboratorio, encuestas, ...)

 	- Descripción, representación y análisis de los datos recogidos (Estadística Descriptiva)

 	- Cotejo de los datos con el modelo teórico adecuado (Estadística Matemática)

 	- Obtención de inferencias o conclusiones (Estadística Inferencial)

**Ejemplo 1**: En el estudio de siniestralidad laboral en un cierto polígono industrial se han recogido los siguientes datos históricos:

| **Año** 
| **Accidentes** 

| 2000 
| 4 

| 2001 
| 3 

| 2002 
| 2 

| 2003 
| 4 

| 2004 
| 3 

| 2005 
| 2 

Obtenemos algunos parámetros y gráficos estadísticos:

[caption id="attachment_1344" align="alignnone" width="502"][![Fase 1: Estadística descriptiva resumen de los datos](/assets/images/fase1_estad.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/fase1_estad.png) Fase 2: Estadística descriptiva resumen de los datos[/caption]
En la siguiente fase utilizamos el modelo matemático de Poisson, que es útil para el estudio de la siniestralidad en general, para comparar los datos experimentales con los teóricos suministrados por el modelo, asegurando que el modelo teórico es válido en este caso.

Por último, podemos responder a preguntas como "*calcular la probabilidad de que ocurra al menos un accidente
antes del mes de junio del año actual*" usando el modelo matemático: resulta ser del 77%.

[![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

# Concepto de población, muestra, individuo y variable estadística

**Población**: el conjunto de todos las posibles realizaciones de un experimento aleatorio.
**Ejemplo 2**: Encuesta de opinión dirigida a universitarios, población: todos los universitarios. Lanzamiento de un dado, población infinita (todos los posibles lanzamientos). Estudio de calidad de un componente electrónico, población: todos los componentes fabricados en un cierto periodo de tiempo.

**Muestra**: subconjunto representativo de la población de un experimento aleatorio.
**Ejemplo 3**: Encuesta a 20 estudiantes elegidos al azar de cada universidad en la zona de estudio. Lanzamos 100 veces un dado (de las infinitas veces que podemos hacerlo, nos conformamos con 100). Estudiamos 20 unidades del componente electrónico fabricados en cierto día.

**Individuo**: cada elemento de la población o de la muestra (un universitario, un lanzamiento del dado, una unidad del componente electrónico)

**Variable estadística**: una característica numérica de la población que nos interesa estudiar
**Ejemplo 4**: preguntamos a cada estudiante si está de acuerdo o no con cierta ley, definimos la variable estadística asignando el valor 1 a la respuesta afirmativa y el valor 0 en la negativa. En el lanzamiento de un dado, la variable es el número de puntos obtenidos.  En el estudio del componente electrónico, la variable puede ser la resistencia eléctrica, o el tiempo de servicio hasta que queda inservible, etc.

## Clasificación de las variables estadísticas

**Variables discretas**: el conjunto de diferentes valores que puede tomar (dominio de la variable) es finito o infinito numerable (un entero). Ejemplo: lanzamiento de un dado, con dominio {1,2,3,4,5,6}.

**Variables continuas**: el dominio es infinito no numerable (un intervalo de la recta real). Ejemplo: tiempo de servicio de un componente electrónico.
#  [![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

# Distribución de frecuencias. representaciones gráficas

En Estadística Descriptiva el conjunto de valores a estudiar siempre se representa en forma de tabla de frecuencias observadas. Los programas de estadística toman estas tablas como dato de entrada y nos devuelven parámetros y representaciones gráficas

**Ejemplo 5**: Sea el experimento aleatorio: lanzamiento N = 10 veces de un dado. Tipo de variable: discreta. Población infinita. Muestra con N = 10. Resultados muestrales: {3, 4, 6, 1, 5, 2, 4, 6, 6, 1}. Con ellos formamos la tabla de frecuencias sin agrupar y el [histograma](https://es.wikipedia.org/wiki/Histograma) de frecuencias absolutas:

[caption id="attachment_1347" align="alignnone" width="637"][![Ejemplo de tabla de frecuencias y su representación gráfica](/assets/images/est-descrp.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/est-descrp.png) Ejemplo de tabla de frecuencias y su representación gráfica[/caption]

El software permite generar una gran variedad de gráficos estadísticos con facilidad, es tarea del analista escoger cuál de ellos es el más adecuado para resumir los datos del estudio y mostrar las propiedades que desea poner de manifiesto.

[caption id="attachment_1348" align="alignnone" width="543"][![Opciones de tipo de gráfico en OpenOffice](/assets/images/graph_types.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/graph_types.png) Opciones de tipo de gráfico en OpenOffice[/caption]

La utilidad de los gráficos estadísticos es:

 	- Mostrar de forma explícita la distribución de valores de la variable, para hacernos una idea rápida de su distribución (uniforme, no uniforme, homogénea, heterogénea, máximos, mínimos, etc.)

 	- Poner de manifiesto tendencias y efectos que de otra forma pueden quedar ocultos

** Ejemplo 6**: uso práctico de gráficos en el control de calidad de un proceso de fabricación. En una cierta fábrica de bizcochería industrial se han recibido algunas quejas de clientes debido a que sus departamentos de calidad han detectado que en las remesas recibidas los bizcochos tienen un peso medio inferior al esperado, que es de 220 gramos con una tolerancia de ±10 gr. Para comprobarlo, se realiza una muestra aleatoria del peso en gramos del bizcocho producido que puede ser elaborado por dos máquinas diferentes (1 y 2) atendidas indistintamente por dos operarios (A y B), tomando una muestra diaria aleatoriamente de una de las máquinas y uno de los operarios (nota: realmente esto no se hace exactamente así, sólo es un ejemplo), los resultados han sido:

 

| Dia** 
| **Peso (gr)** 
| **Máquina** 
| **Operario** 

| 1 
| 195,0 
| M2 
| B 

| 2 
| 228,5 
| M1 
| A 

| 3 
| 217,6 
| M1 
| B 

| 4 
| 207,2 
| M2 
| B 

| 5 
| 213,8 
| M2 
| A 

| 6 
| 217,6 
| M2 
| A 

| 7 
| 211,5 
| M1 
| A 

| 8 
| 202,7 
| M1 
| A 

| 9 
| 207,8 
| M1 
| B 

| 10 
| 203,1 
| M1 
| A 

| 11 
| 204,0 
| M1 
| B 

| 12 
| 215,7 
| M2 
| B 

| 13 
| 202,7 
| M1 
| B 

| 14 
| 225,6 
| M1 
| A 

| 15 
| 230,3 
| M1 
| B 

| 16 
| 216,6 
| M2 
| B 

| 17 
| 217,3 
| M1 
| B 

| 18 
| 223,3 
| M2 
| A 

| 19 
| 221,9 
| M2 
| A 

| 20 
| 220,1 
| M1 
| A 

Representando todos los pesos en un histograma, en el que agrupamos los datos en las categorías [200, 205), [205, 210), [210, 215), [215, 220), [220, 225), [225, 230), [230, 235], resulta:

[caption id="attachment_1350" align="alignnone" width="572"][![Histograma de datos agrupados en categorías](/assets/images/descript_tots.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/descript_tots.png) Histograma de datos agrupados en categorías[/caption]
Las dos líneas verticales rojas representan los límites de tolerancia: vemos que efectivamente el proceso de producción está desviado a la izquierda, produce demasiadas unidades por debajo del peso mínimo establecido. Para saber cuál puede ser el orígen del problema, representamos de nuevo los datos pero esta vez separando por categorias: por máquinas y por operarios. Obtenemos:

[caption id="attachment_1351" align="alignnone" width="760"][![Datos según las categorías máquinas y operarios](/assets/images/descript-categories.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/descript-categories.png) Datos según las categorías máquinas y operarios[/caption]
Vemos que hay una diferencia acusada entre las dos máquinas, pues la M1 presenta pesos mucho más dispersos del peso medio (220 gr), y con mayor número de unidades en la gama baja de pesos. En cambio entre operarios hay pocas diferencias. En conclusión, parece que debemos revisar la máquina 1.

 [![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Agrupación de datos en intervalos

 En el ejemplo anterior hemos visto que los datos de una variable continua (peso en gramos) es más cómodo agruparlos en intervalos de valores. Esto se hace más patente cuando aumenta el tamaño de la muestra. Supongamos que en vez de 20 pesos de bizcochos tenemos 160. Para organizar esos datos en intervalos procedemos como sigue:

 	- Hallamos el valor mínimo (redondeado), por ejemplo: 207

 	- Hallamos el valor máximo (redondeado), por ejemplo: 231

 	- calculamos el **recorrido** = Valor máximo valor mínimo =  231 - 207 =  24

 	- Fijamos el número de intervalos, que suele estar entre 6 y 10, por ejemplo k = 8

 	- Calculamos la anchura de cada intervalo  = recorrido / k = 24 / 8  = 3

Los intervalos (o **clases**) serán pues: [207, 210), [210, 213), ... [228, 231]. Entonces contamos cuantos de los datos caen en cada intervalo, formando la tabla de frecuencias:

[caption id="attachment_1354" align="alignnone" width="722"][![ ](/assets/images/taula_freq.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/taula_freq.png) Tabla de datos agrupados en clases, con las frecuencias absolutas y relativas[/caption]
La marca de clase es simplemente el punto medio del intervalo que define a la clase. La frecuencia relativa se obtiene dividiendo la absoluta por el número N de datos. Las frecuencias acumuladas son sumas parciales de frecuencias.

[![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Estadísticos muestrales

Un estadístico muestral, también llamado parámetro estadístico, es una función de los datos que devuelve un número, intentando resumir el conjunto de datos en un único indicador. El típico ejemplo es la media aritmética de N datos.

## Estadísticos de posición

Resumen la distribución de datos muestrales dando un valor que los representa atendiendo a la posición que ocupan en la recta real. Hay de dos tipos: de posición central y de posición no central.

### Estadísticos de posición central

 Resumen todos los datos con un único valor que intenta ser central a todos. 

**Media aritmética**: Si tenemos N datos $x_1, ..., x_N$ la media aritmética es simplemente $\overline x=\frac1N\sum\nolimits_{i=1}^Nx_i$;  si tenemos los datos agrupados por frecuencias de forma que hay k clases, con k marcas de clase diferentes $x_1, ..., x_k$, con frecuencias absolutas $F_1, ..., F_k$ y un total de $N=\sum\nolimits_{i=1}^kF_i$ datos, la media aritmética es:

$\overline x=\frac1N\sum\nolimits_{i=1}^kx_iF_i=\frac{\sum_{i=1}^kx_iF_i}{\sum_{i=1}^kF_i}$

**Mediana**
Si ordenamos en orden creciente los datos no agrupados {x_1, ... x_N} la mediana m ocupa la posición central. Para N impar resulta ser el dato que ocupa la posición (N + 1) / 2; para N par la definimos como la media de los datos que ocupan las posiciones (N / 2) y (N / 2) +1.
Si los datos vienen agrupados en intervalos entonces usamos la fórmula de los centiles Ci (ver más bajo) con i = 50.

**Moda**
Es el valor que presenta la frecuencia máxima. Puede haber más de una moda (distribución de datos multimodal).

**Ejemplo**:  la serie de 9 datos ordenados de menor a mayor {2, 5, 6, 6, 7, 9, 9, 9, 10} tiene moda = 9 (dato con más ocurrencia), mediana = 7 (pues con 9 datos el que ocupa la posición central es el quinto dato, que es el número 7) y la media aritmética = 7 (en este caso coincide con la mediana, pero no tiene porque ser así)
### De posición no central

Proporcionan valores que, ordenando los datos en orden creciente, dividen la distribución en partes iguales.

 	- **Cuartiles**: son tres valores que hacen cuatro partes iguales

 	- **Deciles**: son nueve valores que hacen diez partes iguales (10% de los datos)

 	- **Centiles o percentiles**: son noventa nueve valores que hacen cien partes iguales (1% de los datos).

Evidentemente, se cumple que Primer cuartil = 25º centil, segundo cuartil = 50º centil, .... También, primer decil = 10º centil, segundo decil = 20º centil, .... Además, la Mediana = 50 centil.

[caption id="attachment_1356" align="alignnone" width="684"][![Los tres quartiles dividen el rango de datos en cuatro partes iguales, con un 25% de los datos cada una ](/assets/images/quartils.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/quartils.png) Los tres cuartiles dividen el rango de datos en cuatro partes iguales, con un 25% de los datos cada una[/caption]

Con N datos no agrupados, el centil $C_i$ es el número que ocupa la posición $(iN / 100)$, donde $1\leq i\leq N$. Con datos agrupados en intervalos usamos la formula:

$C_i=L_{j-1}+\frac{{\displaystyle\frac{i\left(N-1\right)}{100}}+1-N_{j-1}}{n_j}a_j$

donde:

$N_{j-1}$: frecuencia absoluta acumulada del intervalo anterior
$L_{j-1}$: extremo inferior del intervalo donde está el dato que ocupa la posición (N-1) / 100
$a_j$: anchura del intervalo donde está el dato que ocupa la posición (N-1) / 100
$n_j$: frecuencia absoluta del intervalo donde está el dato que ocupa la posición (N-1) / 100
Los percentiles pueden calcularse gráficamente usando el diagrama de frecuencias relativas acumuladas, con líneas que unen los puntos, obtenemos el denominado polígono de frecuencias acumuladas. Para encontrar digamos el percentil $c_{20}$ hallamos la abscisa correspondiente a la ordenada Y = 20:

[caption id="attachment_1358" align="alignnone" width="663"][![Polígono acumulativo de frecuencias, y obtención del percentil 20](/assets/images/poligon_acumulatiu.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/poligon_acumulatiu.png) Polígono acumulativo de frecuencias, y obtención del percentil 20[/caption]

De hecho la formula que hemos dado no es más que una semejanza entre triángulos; en la figura, si nos fijamos en los dos triángulos semejantes delimitados por los puntos (200, 5%), (C, 20%), y (205, 25%) planteamos:

[caption id="attachment_1360" align="alignnone" width="220"][![Triángulos semejantes en el polígono de frecuencias acumuladas](/assets/images/percentils.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/percentils.png) Triángulos semejantes en el polígono de frecuencias acumuladas[/caption]

$\frac{205-200}{25-5}=\frac{205-C}{25-20}\Rightarrow C=205-\frac5{20}5=203.8$

Por tanto el percentil 20 vale 203.8. En general, la formula que se deriva del método gráfico será:

$\frac{X_{sup}-X_{inf}}{Y_{sup}-Y_{inf}}=\frac{X_{sup}-C}{Y_{sup}-p}\Rightarrow C=X_{sup}-\frac{X_{sup}-X_{inf}}{Y_{sup}-Y_{inf}}\left(Y_{sup}-p\right)$
donde p es es porcentaje para el que buscamos el percentil (por ejemplo, para $C_{20}$ será p=20), C es el valor del percentil, $Y_{sup}$ es un porcentaje superior a p,  $Y_{inf}$ es un porcentaje inferior a p, y $X_{sup}, X_{inf}$ los valores de abscisas correspondientes.

Al aplicar las dos formulas de percentiles, la primera que es útil para trabajar con tablas de frecuencias y la segunda para gráficas de frecuencias, encontraremos diferencias en los resultados, debido a que ninguno de los dos son métodos exactos sino aproximaciones. Esto es así debido a que un percentil $C_p$, en sentido estricto, es un valor de la distribución que la divide en dos partes, con el p% de valores por un lado y el 100-p%  por el otro, pero es posible que ese valor no exista realmente en la distribución, lo que tomamos es una aproximación. Además al trabajar con tablas de frecuencias en vez de con los datos originales siempre tenemos alguna pérdida de información.

Esto se aprecia fácilmente con la mediana, que equivale al percentil 50. Tomemos por ejemplo la siguiente distribución de 19  valores:

$\left\{107,\;113,\;119,\;125,\;131,\;135,\;146,\;147,\;147,\;149,\;160,\;162,\;172,\;173,\;177,\;187,\;191,\;193,\;193\right\}$

Siendo un número impar de valores, la mediana es el valor que ocupa la posición (N + 1) / 2 = (19 + 1) / 2 = 10, que es el valor X = 149, exactamente.

Agrupemos ahora los datos en una tabla de frecuencias, por ejemplo con cuatro intervalos:

   

| **Xinf** 
| **Xsup** 
| **freq.** 
| ** freq %** 
| **F % acum** 

| 0 
| 100 
| 0 
| 0 
| 0 

| 100 
| 125 
| 4 
| 21,1 
| 21,1 

| 125 
| 150 
| 6 
| 31,6 
| 52,6 

| 150 
| 175 
| 4 
| 21,1 
| 73,7 

| 175 
| 200 
| 5 
| 26,3 
| 100,0 

En amarillo se destaca el intervalo donde debe de estar la mediana, pues su frecuencia acumulada supera el 50%. Si aplicamos ahora las dos formulas aproximadas, obtenemos los valores 150 y 148 respectivamente; en este caso el valor exacto se sitúa en el punto medio entre los dos valores aproximados.
## Medidas de dispersión

 Indican numéricamente si los valores de los datos están agrupados en torno a la media o dispersos.

 	- **Recorrido** = valor máximo - valor mínimo

 	- **Desviación media**: $D=\frac1N\sum\nolimits_{i=1}^n\left|x_i-\overline x\right|$

 	- **Varianza**: $\sigma^2=\frac1N\sum\nolimits_{i=1}^n\left(x_i-\overline x\right)^2$

 	- **Desviación típica**:
$\sigma=\sqrt{\sigma^2}=\sqrt{\frac1N\sum\nolimits_{i=1}^n\left(x_i-\overline x\right)^2}$

 	- **Coeficiente de variación** (Pearson). Proporciona un valor de la dispersión independiente de las unidades. Útil para comparar dispersiones de variables diferentes: $V=\sigma/\overline x$

Las fórmulas de la desviación media, varianza y desviación típica han de adaptarse para trabajar con datos de tablas de frecuencias; llamando $n_i$ a la frecuencia absoluta del valor $x_i$ serán: $D=\frac1N\sum\nolimits_{i=1}^n\left|x_i-\overline x\right|n_i$, $\sigma^2=\frac1N\sum\nolimits_{i=1}^n\left(x_i-\overline x\right)^2n_i$ y $\sigma=\sqrt{\sigma^2}=\sqrt{\frac1N\sum\nolimits_{i=1}^n\left(x_i-\overline x\right)^2n_i}$ respectivamente.
**Ejemplo 8**: En una panadería quieren comparar la distribución de pesos de dos de sus productos, las piezas de pan de 1Kg y las de 1/4Kg. Para ello pesan 20 piezas de cada producto, en días distintos, obteniendo estos resultados, en gramos:

         

| Pan 1Kg (gr) 
| 986 
| 976 
| 1000 
| 965 
| 961 
| 987 
| 1009 
| 1001 
| 961 
| 999 
| 1010 
| 964 
| 978 
| 989 
| 969 
| 1007 
| 971 
| 997 
| 980 
| 982 

| Pan 1/4 Kg (gr) 
| 243 
| 238 
| 249 
| 233 
| 231 
| 243 
| 254 
| 250 
| 231 
| 249 
| 254 
| 233 
| 239 
| 244 
| 235 
| 253 
| 236 
| 248 
| 240 
| 241 

Con la hoja de cálculo, sin agrupar los datos por frecuencias, obtenemos:

      

|  
| Media 
| Mediana 
| Varianza 
| Desv.Tip 
| Desv. Media 
| Coef.Var 
| Recorrido 

| Pan 1Kg (gr) 
| 984,5 
| 983,8 
| 274,1 
| 16,6 
| 14,0 
| 0,02 
| 49,6 

| Pan 1/4 Kg (gr) 
| 242,1 
| 241,8 
| 59,7 
| 7,7 
| 6,5 
| 0,03 
| 23,1 

Analizando estos parámetros, vemos que:

 	- la media de los dos productos está ligeramente por debajo del peso anunciado.

 	- La media y la mediana son muy parecidas; esto sucede cuando la distribución de valores cumple que tanto los valores altos como los bajos tienen frecuencias parecidas, de forma simétrica respecto al valor medio.

 	- Lo mismo sucede con las desviaciones típica y media, son parecidas entre sí. Además, las desviaciones son medidas absolutas que han de comparase con la media para hacerse una idea de su significado. En la barra de 1Kg la desviación típica, 16.6gr, viene a ser un 16.6·100/984.5 = 1.7%; en general, en los procesos productivos, las desviaciones han de ser lo menor posible, este valor de 1.7% puede ser aceptable para una empresa familiar, pero no serlo para un gran fabricante, pues implica un desconocimiento del peso real de cada unidad.

 	- Para comparar las desviaciones entre los dos productos, usamos el coeficiente de variación, y vemos que es superior en la barra de 1/4.

Si queremos una representación gráfica, agrupamos los valores por intervalos para formar la tabla de frecuencias. Por ejemplo escogemos el número de intervalos k = 4, teniendo en cuenta los recorridos, calculamos las anchuras de los intervalos: para las barras de 1Kg será 49,6/4 = 12,4 y para las de 1/4 tenemos 24/4 = 6. Los valores mínimos son 960 y 230 respectivamente. Establecemos los siguientes intervalos: [960, 973), [973, 986), [986, 999) y [999, 1012] para las barras de 1Kg, [230, 236), [236, 242), [242, 248) y [248, 254] para las barras de 1/4. La tabla de frecuencias es:

      

| **desde** 
| **hasta** 
| **frecuencia** 
|  
| **desde** 
| **hasta** 
| **frecuencia** 

| 960 
| 973 
| 6 
|  
| 230 
| 236 
| 6 

| 973 
| 986 
| 5 
|  
| 236 
| 242 
| 4 

| 986 
| 999 
| 4 
|  
| 242 
| 248 
| 4 

| 999 
| 1012 
| 5 
|  
| 248 
| 254 
| 6 

|  
|  
| 0 
|  
|  
|  
|  

El histograma de frecuencias absolutas, para el pan de 1Kg, con indicación del valor medio, es:

[caption id="attachment_1368" align="alignnone" width="440"][![Histograma de frecuencias absolutas](/assets/images/exemple1_descriptiva.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/exemple1_descriptiva.png) Histograma de frecuencias absolutas[/caption]
En este ejemplo vemos que la media aritmética no parece ser un buen representante de la distribución de pesos, simplemente es un valor central.

[![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
{% endraw %}