---
layout: post
title: "Estadística Aplicada -> Contrastes de Hipótesis"
date: 2016-06-16 15:07:54 +0000
categories:
  - "Estadística"
  - "Estadística aplicada"
  - "Matemáticas"
tags:
  - "contrastes"
  - "hipótesis"
  - "test"
math: true
---
{% raw %}

Supongamos que hemos comprado un saco de nueces que contiene unas 1000, y que al llegar a casa cogemos una al azar, resultando que está seca, incomestible. Un optimista pensará, "¡bah! he ido a coger la única que está pasada, no importa", mientras que un pesimista pensará "buenoo ... este saco estará lleno de nueces podridas".  Cualquiera de los dos puede tener razón. Para saberlo, sin tener que vaciar todo el saco, podemos tomar una muestra representativa, esto es, suficientemente grande (por ejemplo, 20 nueces) y bien tomada (mezclamos bien las nueces, cogemos una de arriba, otra del lado derecho, otra de abajo, etc., cambiando de sitio cada vez de forma aleatoria). Después, observando el número de nueces buenas de la muestra, podemos intentar inferir cuantas nueces buenas habrá en el saco. Este procedimiento de comprobación de un producto comercial es parte del proceso de control de calidad, que se hace tanto por parte del fabricante (control de calidad de producción) como del comprador (control de calidad a la recepción del producto). La herramienta estadística que permite, con cierto grado de certeza (denominado nivel de confianza), decidir si una compra como la del saco de nueces es acertada o por el contrario debemos reclamar al fabricante es el contraste de hipótesis estadísticas. Por supuesto, como siempre en Estadística, no podremos saber realmente cuantas nueces están estropeadas a menos que las miremos una por una: aceptar las conclusiones del contraste conllevan un riesgo, como vemos en el siguiente apartado.

### Problemas y  errores que podemos cometer en los contrastes

Supongamos que el fabricante, a través de su control de calidad de producción, está convencido de que sólo un 1% de sus nueces envasadas pueden llegar en mal estado al consumidor, y que el consumidor acepta este máximo, y quiere comprobarlo a la recepción del producto, así que aceptará como máximo ese 1% defectuoso. El comprador entonces extrae una muestra para comprobarla ... pero puede suceder que esa muestra resulte ser peor de lo que realmente es la producción (el término estadístico correcto sería la población), con lo cual reclamará al fabricante sin motivo real, erróneamente; este error se denomina error-α o  error de tipo I.  También puede suceder lo contrario, que por azar la muestra resulte ser mucho mejor que la población, el comprador aceptará erróneamente la compra siendo defectuosa, es el error-β o error de tipo II.

Por ejemplo si los pesos de un dulce tienen una media de *20gr* y sólo uno de cada 100 se desvía de ese peso más de 1gr, en una muestra de tamaño n = 30, el comprador podría pensar de rechazar su pedido si encuentra un sólo dulce que se desvíe más de 1gr del peso medio, pues 30·1/100 = 0.3, la proporción en la muestra no llega a la unidad. Si cada dulce, al ser pesado, tiene una probabilidad 1/100 de salirse de la tolerancia, cuando pesamos uno por uno los 30 dulces de la muestra, la probabilidad de que uno se salga de la tolerancia viene dada por la [distribución de probabilidad binomial](https://es.wikipedia.org/wiki/Distribuci%C3%B3n_binomial), y vale 0.2242, que es un valor alto (un 22,42%), peor aún, la probabilidad de que encontremos uno o más de uno fuera de tolerancia es  α = 26%. Y eso que hemos supuesto que el fabricante dice la verdad. Vemos que este procedimiento de control en la recepción del producto produce un alto error tipo I, con un valor de α = 0.26.

Veamos ahora que pasa con el caso contrario: el fabricante no dice la verdad, y realmente está produciendo un 5% de dulces fuera de tolerancia; ¿qué probabilidad hay de que el comprador no se de cuenta y acepte la compra realizada? Según la [distribución binomial](https://es.wikipedia.org/wiki/Distribuci%C3%B3n_binomial), con un 5% de probabilidad de dulce "erróneo", la probabilidad de que no aparezca ninguno en la muestra de 30 dulces es β = 21,5%, que seria la probabilidad de cometer error de tipo II. Este ejemplo muestra claramente que se necesita un procedimiento eficaz para realizar un control de calidad correcto que no perjudique al fabricante con errores de tipo I ni al comprador con errores de tipo II.

En la figura 1 se muestra el aspecto de las probabilidades de aceptación de una muestra en función de la fracción defectuosa en la población; la línea vertical simboliza la tolerancia anunciada por el fabricante, si la fracción defectuosa es menor, la producción es mejor de lo que anuncia, y si es mayor, la producción resulta peor de lo anunciado. Por supuesto, si la fracción defectuosa es cero (producción perfecta) seguro que aceptaremos cualquier muestra, y no hay error posible. Pero entre el valor de cero y la tolerancia de 0,01 vemos que la probabilidad de no aceptar (rechazar) la muestra va aumentando, en esa región se produce el error de tipo I o α. Por otro lado, cuando la producción es más defectuosa de lo anunciado, sigue habiendo una probabilidad significativa de aceptar la muestra (región β).

$caption id="attachment_1744" align="alignnone" width="515"$![](/taller-matematicas/assets/images/hipotesis-1.png) Fig. 1: Curva de aceptación de una muestra, dependiendo de la proporción real de defectos en la población[/caption]
Así, la curva divide el cuadrante XY en cuatro regiones: las de error I y II, y las otras dos regiones que corresponden a cuando acertamos en el control: aceptamos la muestra que proviene de una población correcta, o bien rechazamos la muestra que proviene de una población incorrecta.

### La matemática del contraste de hipótesis

La Estadística teórica proporciona modelos matemáticos de [distribuciones de probabilidad](https://es.wikipedia.org/wiki/Distribuci%C3%B3n_de_probabilidad): funciones con ciertas propiedades que nos permiten calcular probabilidades de forma sistemática. Los contrastes de hipótesis usan estos modelos para poder decidir si un control de calidad es o no es válido, y lo hacen del siguiente modo:

 	- Dado un problema real en el que extraemos una muestra de una población para comprobar si un cierto valor (un parámetro de la población) es correcto, identificamos qué modelo matemático es el más adecuado para esa situación, atendiendo al tipo de población y al tamaño de la muestra.

 	- Planteamos dos hipótesis: la denominada **hipótesis nula**, hipótesis de trabajo, o H0, y la **hipótesis alternativa**, o H1. La H0 supone que los parámetros dados para la población son correctos, que el modelo de distribución de probabilidad escogido en el paso anterior es también correcto, y que la muestra que tenemos pertenece efectivamente a la población; la hipótesis H1 supone que las afirmaciones anteriores no son correctas (una, algunas o todas)

 	- Suponiendo que la hipótesis de trabajo es cierta, calculamos, usando el modelo de distribución de probabilidad, un valor numérico, denominado **estadístico de contraste**, que es una [variable aleatoria](https://es.wikipedia.org/wiki/Variable_aleatoria) función de la muestra.

 	- Usando las probabilidades dadas por el modelo de distribución de probabilidad, comprobamos si el valor anterior es "creíble" o por el contrario es francamente poco probable que suceda; en el primer caso, damos por verificada la hipótesis H0, en el segundo, rechazamos H0 por ser poco probable y aceptamos la alternativa H1.

**Ejemplo 1**: comprobar si una moneda es simétrica. Queremos averiguar si, en el lanzamiento al aire de una moneda, realmente el número de caras y de cruces obtenidas son iguales o no. Para ello lanzamos al aire la moneda n = 100 veces y anotamos el número de caras y de cruces, que ha resultados ser 52 y 48, respectivamente. Para decidir si la moneda es simétrica respecto al número de caras y de cruces procedemos sistemáticamente.

 	- Cada lanzamiento de la moneda nos da un valor binario, cara o cruz, cada uno con una cierta probabilidad que llamamos P(cara) = p, P(cruz) = q. Si repetimos el lanzamiento n veces, y nos preguntamos el número de caras X (o de cruces) obtenidas en esos lanzamientos, esa variable X es, por definición, una variable aleatoria con distribución de probabilidad binomial. Tenemos pues el modelo matemático.

 	- En principio, suponemos (hay que comprobarlo) que la moneda es simétrica, o sea que las probabilidades p y q son iguales a 1/2: p = q = 1/2. Nuestra hipótesis H0 será: la variable X número de caras sigue la distribución de probabilidad binomial con p = 1/2. La hipótesis H1 será: o bien X no sigue la distribución de probabilidad binomial, o bien p no es igual a 1/2.

 	- Suponiendo H0 cierta, la proporción de caras obtenidas en la muestra n = 100 lanzamientos, que llamaremos p' = 52/100, debería no estar muy alejada de p = 1/2. Nuestro estadístico de contraste en este caso será simplemente p'.

 	- Suponiendo H0 cierta, ¿cuál es la probabilidad de obtener p' = 0.52 en n = 100 lanzamientos de la moneda? Este planteamiento es demasiado estricto, pues dará una probabilidad baja, concretamente da P(X = 52) = 0.07, porque obtener precisamente 52 caras es totalmente aleatorio, si volvemos a lanzar la moneda otras 100 veces seguramente obtendremos otro valor distinto, así que si seguimos este método estaremos trabajando con una probabilidad grande de cometer  error de tipo I: rechazar una hipótesis que era verdadera. Lo que se hace en contrastes de hipótesis es trabajar siempre con intervalos aceptables de valores, no con valores puntuales; por ejemplo, ¿en qué intervalo de valores esperamos encontrar el número de caras X, en n = 100 lanzamientos, con una probabilidad del 95%? Calculamos el intervalo [a, b] tal que  P(a <= X  <= b) = 0.95; siendo n bastante grande, el cálculo se simplifica aproximando la binomial por una distribución normal, concretamente aplicamos el siguiente resultado:

**Teorema 1**: Si H0 es cierta, y n es grande, entonces el estadístico de contraste
$Z=frac{p'-p}{sqrt{displaystylefrac{pleft(1-pright)}n}}$

sigue una distribución de probabilidad Normal estándard.
O sea que para nuestra moneda tendremos

$Z=frac{0.52-0.5}{sqrt{displaystylefrac{0.5left(1-0.5right)}{100}}}=frac25=0.4$

¿Entre qué valores esperamos que Z esté, con una probabilidad del 95%, siendo Z una variable normal estándar? Consultando las tablas de la Normal encontramos que *P(-1.96 < Z < 1.96) = 0.95*. Vemos que el valor obtenido del estadístico de contraste, Z = 0.4,  cae dentro de este intervalo, por tanto "todo cuadra", es lo que esperábamos al suponer H0 cierta, por lo que concluimos que, efectivamente, la moneda es simétrica.

### Intervalos de aceptación de H0 y H1, p-valor

En el ejemplo 1, el intervalo que hemos obtenido, [-1.96, 1.96], se llama **intervalo de aceptación de la hipótesis H0**. En seguida deducimos que existe otro intervalo de aceptación de la hipótesis alternativa, que será el complementario: $left(-infty,-1.96right)cupleft(1.96,+inftyright)$, es el **intervalo de aceptación de la hipótesis H1. **Decidir con qué hipótesis nos quedamos, con H0 o H1, es simplemente ver en cual de estos dos intervalos "cae" el estadístico de contraste.

Claro que estos intervalos son bastante arbitrarios: en el ejemplo 1 lo hemos obtenido a partir de una probabilidad del 95%: el estadístico de contraste Z, debe de estar en [-1.96, 1.96] en un 95% de los casos, siempre que la hipótesis H0 sea cierta; pero, ¿por qué 95%, y no 80%, 70% o 100%? En la siguiente tabla vemos otras elecciones para la probabilidad, su intervalo de aceptación de H0, y la conclusión obtenida al comparar el estadístico de contraste Z = 0.4 con el intervalo:

 

| **Probabilidad** 
| **intervalo aceptación H0** 
| ** ** 
| **Conclusión** 

| 100,00% 
| -∞ 
| +∞ 
| H0 cierta 

| 99,00% 
| -2,5758293035 
| 2,5758293035 
| H0 cierta 

| 95,00% 
| -1,9599639845 
| 1,9599639845 
| H0 cierta 

| 90,00% 
| -1,644853627 
| 1,644853627 
| H0 cierta 

| 80,00% 
| -1,2815515655 
| 1,2815515655 
| H0 cierta 

| 70,00% 
| -1,0364333895 
| 1,0364333895 
| H0 cierta 

| 60,00% 
| -0,8416212336 
| 0,8416212336 
| H0 cierta 

| 50,00% 
| -0,6744897502 
| 0,6744897502 
| H0 cierta 

| 40,00% 
| -0,5244005127 
| 0,5244005127 
| H0 cierta 

| 30,00% 
| -0,3853204664 
| 0,3853204664 
| H0 falsa 

| 20,00% 
| -0,2533471031 
| 0,2533471031 
| H0 falsa 

| 10,00% 
| -0,1256613469 
| 0,1256613469 
| H0 falsa 

| 0,00% 
| 0 
| 0 
| H0 falsa 

Sea cual sea la probabilidad escogida, se le llama **nivel de confianza del contraste**, y se le denota por (1 - α); la probabilidad α también tiene nombre: es el **nivel de significación del contraste**. Así, en el ejemplo 1 hemos elegido un nivel de confianza del 95%, o equivalentemente, un nivel de significación del 5%.

Recordemos que en todo contraste, al decidir con qué hipótesis nos quedamos, podemos cometer errores, de tipo I o II; el error de tipo I, rechazar H0 cuando era cierta, sería el caso de haber obtenido con una moneda simétrica, por ejemplo, 60 caras en 100 lanzamientos, ya que en este caso obtenemos un estadístico Z = 2, que cae fuera del intervalo de aceptación de H0, [-1.96, 1.96]. Es difícil que esto ocurra, pero no imposible: la probabilidad de obtener un Z fuera del intervalo [-1.96, 1.96] es precisamente del 5%, el nivel de significación, y al mismo tiempo, es ésta la probabilidad de cometer el error de tipo I:

**
El nivel de significación α es la probabilidad de cometer, en un contraste, el error de tipo I

 Así pues, al escoger la probabilidad (1 - α) del intervalo de aceptación, al mismo tiempo estamos escogiendo con que probabilidad vamos a cometer el error de tipo I. Evidentemente, queremos que sea baja, por lo que los valores de la tabla 0%, 10%, etc para (1 - α) quedan descartados. En la práctica suelen usarse de forma estándar niveles de confianza del 90%, 95% o 99%, equivalentes a niveles de significación de 10%, 5% o 1%. ¿Y por qué no tomamos (1 - α) con lo cual α = 0 y seguro que no cometemos error de tipo I? En la tabla vemos que el intervalo de aceptación de H0 es toda la recta real: sea cual sea el valor del estadístico Z aceptaremos H0: el contraste no hace nada, siempre responde lo mismo, que H0 es cierta, !incluso siendo falsa!. Si lo queremos de otro modo:

Al reducir mucho la probabilidad α de cometer error de tipo I, aumentamos mucho la probabilidad β de cometer error de tipo II.

Dada esta arbitrariedad de elección del nivel de confianza (o del de significación), es útil otra forma alternativa de decidir entre H0 y H1, que consiste en, dado el estadístico z, y la variable aleatoria Z de la población, calcular la probabilidad P(Z > z) = P(z < Z < +∞). Esperamos que esta probabilidad no sea "demasiado pequeña" para aceptar H0, concretamente la comparamos con los niveles de significación habituales, 10%, 5% o 1%. A la probabilidad P(Z > z) se la conoce con el nombre de p-valor del contraste asociado al estadístico Z, o simplemente, el **p-valor**.

**Ejemplo 2:** siguiendo con el caso de la moneda, el p-valor correspondiente a z = 0.4 es P(Z > 0.4)  = 0.3446 = p-valor, o expresado en %, es de 34,46%; comparando con los niveles 10%, 5% o 1% vemos que es mayor que todos ellos, así que aceptamos H0 tanto para la significación 10% como para  5% o 1%.

En la realidad sucede a menudo que no está tan claro si aceptar H0 o no, pues depende del nivel de significación finalmente elegido. Por ejemplo, si en el lanzamiento n = 100 veces de la moneda hubiéramos obtenido 60 caras, con lo cual es estadístico z = 2, y el p-valor = 0.0227, o 2.27%, es un valor pequeño, menor que α = 10% o α =5%, pero mayor que α = 1%; entonces, ¿qué decidimos? Diríamos: con unas probabilidades de cometer error I del 10% o del 5%, rechazamos que la moneda sea simétrica, pero con una probabilidad de cometer error I de sólo 1%, lo aceptamos. Todo depende de hasta que punto queramos evitar caer en el error de tipo I: rechazar H0 cuando era cierta.

El p-valor nos informa de la probabilidad de cometer error de tipo I en el contraste: para significaciones α > p-valor, aceptamos H1, para α < p-valor, aceptamos H0.

### Contrastes unilaterales y bilaterales

Volvamos al ejemplo de los dulces, sus pesos tienen una media de *20gr* y según el fabricante sólo uno de cada 100 se desvía de ese peso más de 1gr. El comprador quiere saber cómo proceder, en una muestra de tamaño n = 30, para decidir si la compra es aceptable o bien si ha de reclamar. Además, nos dice que no le preocupa que el peso real esté por encima de la media ya que en ese caso estará comprando más barato, tendrá más dulce por el mismo precio, lo que le preocupa es pagar por dulces a los que les falte peso para llegar a la media.

En seguida planteamos las hipótesis que darán respuesta al problema planteado:

 	- H0: El peso de los dulces, que tiene una distribución de probabilidad normal, tiene una media de al menos *20gr*,

 	- H1: El peso de los dulces no llega a los 20gr, o bien la distribución real del peso no sigue una distribución normal

Hemos supuesto que la distribución teórica del peso de los dulces es normal, pues así suele suceder. Cuando en la hipótesis de trabajo H0 planteamos una desigualdad respecto a la media, como ahora que hacemos media ≥ 20, diremos que hacemos un **contraste unilateral**, mientras que si trabajamos con una igualdad, como en el caso de la moneda simétrica en el que suponíamos que p = 1/2, es un **contraste bilateral**.

 	- $H_0:;mu=mu_0$ contraste bilateral

 	- $H_0:;mugeqmu_0,;H_0:;muleqmu_0$ contraste unilateral a la derecha o a la izquierda, respectivamente

Simbólicamente escribimos:

$begin{array}{l}left.begin{array}{r}H_0:;;mugeq20\H_1:;mu&lt;20end{array}right}\;end{array}$

También tenemos contrastes unilaterales cuando H0 es una igualdad, pero H1 es una desigualdad estricta:

$begin{array}{l}left.begin{array}{r}H_0:;;mu=mu_0\H_1:;muneqmu_0end{array}right},left.begin{array}{r}H_0:;;mu=mu_0\H_1:;mu&gt;mu_0end{array}right},;left.begin{array}{r}H_0:;;mu=mu_0\H_1:;mu&lt;mu_0end{array}right}\;end{array}$

El primer contraste es bilateral, los otros dos son unilaterales a la derecha o a la izquierda, respectivamente. Aunque no hay unanimidad la corriente mayoritaria considera, por motivos formales, que lo correcto es mantener la igualdad en la hipótesis H0 y en todo caso manejar desigualdades en la hipótesis H1. Siguiendo este convenio, el contraste sobre los dulces quedaría:

$begin{array}{l}left.begin{array}{r}H_0:;;mu=20\H_1:;mu&lt;20end{array}right}\;end{array}$

entendiendo que si aceptamos H0 significa que el peso es como mínimo de 20gr, ya que se ha rechazado la hipótesis alternativa.

En la práctica el que el contraste sea bilateral o unilateral afecta a los intervalos de aceptación de H0 y H1. Resolvamos ahora el problema del control de calidad a la recepción de los dulces.

**Ejemplo 3**: Un comprador de dulces al por mayor quiere saber, al tomar una muestra de n = 20 dulces, qué criterio ha de seguir para saber si aceptar o rechazar la compra, con una probabilidad de error tipo I del 10%, suponiendo que los pesos de los dulces siguen una distribución normal de media 20gr.

Ya sabemos que la forma del contraste será

$begin{array}{l}left.begin{array}{r}H_0:;;mu=20\H_1:;mu&lt;20end{array}right}\;end{array}$

Para calcular el estadístico de contraste en este caso particular necesitamos el siguiente resultado:

**Teorema 2**: Si la población es normal y H0 es cierta, sabemos la media μ de la población pero desconocemos su desviación típica σ, entonces el estadístico

$T=frac{overline x-mu}{s/sqrt n}$

es una variable aleatoria que sigue una [distribución de probabilidad t-Student ](https://es.wikipedia.org/wiki/Distribuci%C3%B3n_t_de_Student)con *n-1* grados de libertad, siendo s la desviación típica de la muestra.

Conocemos la media y el valor de n, así que:

$T=frac{overline x-20}{s/sqrt{20}}$

Para aceptar H0 con una significación de α = 10%, el intervalo de aceptación de H0 ha de "abarcar" un 100% - 10% = 90% de probabilidad, y el de H1 el 10% restante. Pero siendo que sólo nos interesa el caso $mu&lt;20$ para H1, no consideraremos que valores grandes de la media afecten a H1, en otras palabras, el intervalo de aceptación de H1 ha de ser del tipo (-∞, t), siendo t un valor tal que P(-∞ < T < t) = 0.1. Este valor, buscado en las tablas de la distribución t-Student, resulta ser t = -1.328, con lo cual el intervalo de aceptación de H1 es (-∞, -1.328) y  el de H0 será [-1.328, +∞). Para aceptar H0 por tanto debe de cumplirse que

$T=frac{overline x-20}{s/sqrt{20}}inlbrack-1.328,+infty)Leftrightarrowfrac{overline x-20}{s/sqrt{20}}geq-1.328Rightarrowboxed{frac{overline x-20}sgeqfrac{-1.328}{sqrt{20}}}$

Así que nuestra recomendación al comprador de dulces será:

"Calcule usted la media $overline x$ y la desviación típica *s* de la muestra de 20 dulces, y sustituya esos valores en la expresión $frac{overline x-20}s$; si le resulta un valor mayor o igual a -0.2969, acepte la compra, de lo contrario, podrá reclamar al fabricante, con una probabilidad del 10% de error de equivocarse al hacerlo."

Supongamos que nos hace caso y le resulta $overline x=19.5$, s = 1.1; entonces resultará $frac{19.9-20}{1.1}=-0.09;&gt; -0.2969$ y le recomendamos aceptar el pedido.

**Ejemplo 4**: El comprador de dulces se da cuenta de que no ha usado una información importante: el fabricante afirma que sólo uno de cada 100 dulces se desvía de ese peso más de 1gr; con este dato podemos estimar cual es la desviación típica de la población, y afinar más el contraste. La afirmación equivale a decir que P(20 - 1 < X < 20 + 1) = 99/100, siendo la población normal, podemos hacer un cambio de variable para convertirla en normal estándar $Z=frac{X-mu}sigma$:

$Pleft(19&lt;X&lt;21right)=P(frac{19-20}sigma&lt;Z&lt;frac{21-20}sigma)=Pleft(frac{-1}sigma&lt;Z&lt;frac{1}sigmaright)=0.99$

Mirando en las tablas de la normal estándar vemos que para que se cumpla la desigualdad anterior ha de ser $frac1sigma=2.576Leftrightarrowsigma=0.3882$. Para utilizar esta información sobre la población en el contraste necesitamos otra propiedad matemática:

**Teorema 3**: Si la población es normal y H0 es cierta, sabemos la media μ de la población y su desviación típica σ, entonces el estadístico

$z=frac{overline x-mu}{sigma/sqrt n}$

es una variable aleatoria que sigue una distribución normal estándard.

Calculamos el valor del estadístico: $z=frac{19.9-20}{0.3882/sqrt{20}}=-1.15$. Buscamos en las tablas de la normal estándar la probabilidad P(Z > z), que es, según hemos definido, el p-valor, y resulta ser p = 0.12507, la situación se representa en la figura

$caption id="attachment_1750" align="aligncenter" width="615"$![Intervalos de aceptación de H0 y H1 según el p-valor](/taller-matematicas/assets/images/intervals-acceptacio.png) Intervalos de aceptación de H0 y H1 según el p-valor[/caption]
Entonces, para una significación de 0.01 < p-valor, concluimos que no rechazamos H0, la conclusión no ha cambiado respecto al ejemplo anterior.  Si en vez de usar el p-valor usamos el método de buscar en las tablas el intervalo de aceptación de H0, tendremos que encontrar un z tal que P(Z > z) = 0.90 que resulta ser -1.282, el intervalo de aceptación de H0 es [-1.282, +∞), como z = -1.15 cae dentro del intervalo, aceptamos H0.

### Potencia de un contraste

Si comparamos los intervalo para H0 de los eje del ejemplos 3 y 4, que son   [-1.328, +∞) y [-1.282, +∞), vemos que el ejemplo 4 es algo más estrecho; por ejemplo, para un valor del estadístico de contraste de -1.3, en el ejemplo 3 aceptaríamos H0 pero en el ejemplo 4 no. Siendo que en los dos ejemplos la significación es la misma, del 10% (que recordemos que es la probabilidad de cometer error de tipo I), ¿porqué hay esta diferencia?

Recordemos que el error de tipo II es: aceptar H0 cuando realmente es falsa; diremos que, a igualdad de significación, un contraste es más potente que otro, si tiene menor probabilidad $beta$ de cometer el error de tipo II. Lo que sucede con los ejemplos 3 y 4 es que el contraste de este último es más potente que el del primero; esto es así porque en el ejemplo 4 usamos más información que en el 3: sabemos la desviación típica de la población. En general, interesa maximizar la potencia del contraste a utilizar, usando toda la información disponible.

### Otros contrastes de hipótesis

En los ejemplos anteriores hemos visto como se contrasta el valor de la media (el peso medio de los dulces) y el de la proporción (en el problema de la moneda y las caras y cruces). Otros contrastes de hipótesis decidirán sobre otros parámetros: sobre la varianza, sobre la diferencia de medias entre dos poblaciones, o la diferencia de proporciones.

**Ejemplo 5**: Nuestro comprador de dulces decide probar con otro fabricante que asegura que sus dulces tienen un peso medio de 22gr con una desviación típica de 1.3gr. La pregunta que nos hace es: ¿con base a una muestra de $n_1 = 20, n_2 = 20$ dulces del fabricante 1 y del fabricante 2, cómo puedo estar seguro de que efectivamente el fabricante 2 produce dulces con un peso 2gr superior al fabricante 1, con un 10% de posibilidad de error tipo I?

Formalmente, suponiendo que los pesos de las dos poblaciones de dulces de los dos fabricantes siguen una distribución de probabilidad normal, el contraste se establece como sigue:

 	- H0: no hay diferencias entre los pesos medios, $mu_1=mu_2$

 	- H1: $mu_1&gt;mu_2$

Para cada tipo de contraste se necesita un teorema que nos proporcione el estadístico de contraste a utilizar, tal como hemos visto en los ejemplos anteriores; para esta comparación de medias de dos poblaciones normales con desviaciones típicas conocidas usaríamos:

$x=frac{left(overline{x_1}-overline{x_2}right)-d_0}{sqrt{displaystylefrac{sigma_1^2+sigma_2^2}{n_1+n_2}}}$

### Contrastes no paramétricos

En muchos casos prácticos interesa formular hipótesis estadísticas en las que no tenemos conocimiento teórico de la población (no tenemos sus parámetros); por ejemplo, queremos comparar las calificaciones obtenidas en una prueba de idiomas por los alumnos antes y después de un viaje a Inglaterra, para saber si ha surtido algún efecto, la muestra es:

 

|  
| Alumno 1 
| Alumno 2 
| Alumno 3 
| Alumno 4 
| Alumno 5 

| Antes viaje 
| 7,25 
| 8,00 
| 6,00 
| 8,00 
| 9,00 

| Después viaje 
| 8,25 
| 7,82 
| 6,36 
| 9,69 
| 8,59 

A simple vista parece que sí que ha surtido efecto, pero queremos saber si las diferencias observadas son estadísticamente significativas y que no sean producto del azar. Si no podemos suponer normalidad en la variable, necesitamos aplicar un contraste no paramétrico, por ejemplo uno muy sencillo es el de los signos: observamos los signos de las diferencias entre notas:

 

|  
| Alumno 1 
| Alumno 2 
| Alumno 3 
| Alumno 4 
| Alumno 5 

| Antes viaje 
| 7,25 
| 8,00 
| 6,00 
| 8,00 
| 9,00 

| Después viaje 
| 8,25 
| 7,82 
| 6,36 
| 9,69 
| 8,59 

| Diferéncia 
| 1 
| -0,18 
| 0,36 
| 1,69 
| -0,41 

| Signo 
|  + ** 
| ** -** 
| ** +** 
| ** +** 
| ** -** 

Establecemos el contraste:

 	- H0: no hay diferencias en las calificaciones obtenidas en la prueba de idiomas de los alumnos antes y después del viaje a Inglaterra

 	- H1: sí hay diferencias en las calificaciones obtenidas en la prueba de idiomas de los alumnos antes y después del viaje a Inglaterra

 
Si H0 es cierta, esperaríamos que los signos de las diferéncias fueran por igual positivos que negativos, la proporción para ambos ha de ser 1/2 ; tenemos 3 positivos y 2 negativos.
{% endraw %}