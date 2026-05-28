---
layout: post
title: "Introducción a las probabilidades"
date: 2015-09-25 10:24:00 +0000
categories:
  - "Estadística"
  - "Probabilidades"
tags:
  - "Álgebra de sucesos"
  - "axiomas probabilidad"
  - "combinatoria"
  - "espacio muestral"
  - "predicción"
  - "probabilidad"
  - "probabilidad condicionada"
  - "Probabilidad total"
  - "punto muestral"
  - "regla de Laplace"
  - "sucesos condicionados"
  - "sucesos dependientes"
  - "sucesos exluyentes"
  - "sucesos independientes"
  - "Teorema de Bayes"
math: true
---
{% raw %}

- Introducción

 	- Probabilidad y predicción

 	Precisión

 	- Cálculo de probabilidades

 	- Interpretación de la probabilidad como una frecuencia teórica

 	- Resultados no equiprobables

 	- Combinación de casos independientes

 	- Definiciones: Espacio muestral de un experimento aleatorio, puntos muestrales, sucesos.

 	- Álgebra de sucesos

 	- Regularidad estadística. Primera definición de probabilidad

 	- Segunda definición de probabilidad: regla de Laplace, combinatoria

 	- Tercera definición de probabilidad: axiomas y propiedades

 	- Probabilidad condicionada. sucesos independientes

 	- Teoremas de la probabilidad total y de Bayes

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Introducción

Históricamente la Estadística, en sus inicios, no usaba la teoría de las probabilidades, de hecho, ambas ramas de la Matemática en sus inicios fueron independientes; esto es así debido a que la Estadística era de naturaleza descriptiva, como se ha visto en el tema [Estadística descriptiva, análisis de datos](http://tallermatematic.eu/wp/?p=1341). Con el tiempo, empezó a usarse para predecir sucesos a partir de datos anteriores, y también para llegar a conclusiones globales usando datos parciales, es lo que se denomina [inferencia estadística](https://es.wikipedia.org/wiki/Estad%C3%ADstica_inferencial). Pero estas predicciones y conclusiones no deben nunca interpretarse como precisas, como puede ser en Ciencias Exactas, sino que siempre están limitadas por conceptos como "margen de confianza", "valor estimado", "hipótesis" y también "probabilidad". En este post vemos una introducción breve y simple a la teoría de la probabilidad aplicada a la Estadística.

# Probabilidad y predicción

El concepto de probabilidad es la base de la Estadística, y no es un concepto fàcil de entender. La utilidad de los datos del pasado es comprender el presente y poder hacer predicciones sobre el futuro. También, la utilidad de tener unos datos parciales, una **muestra** de datos, es la de poder hacer predicciones sobre el conjunto total de los datos, o **población**. A estas predicciones en Estadística las llamamos inferencias, y al conjunto de técnicas para lograrlo, técnicas de **inferencia Estadística**.

Pero en Estadística estas inferencias no son nunca predicciones exactas sino aproximadas. Para dar una valoración de cuan aproximadas son, utilizamos el concepto de probabilidad. Así, una predicción con una probabilidad asociada del 100% tendría certeza absoluta, y en el otro extremo, con una probabilidad asociada del 0% tendría falsedad absoluta: nunca se cumpliría. En las aplicaciones prácticas, estos valores extremos nunca se alcanzan.

### Precisión

$caption id="attachment_536" align="alignnone" width="300"$[![Torres Petronas](/taller-matematicas/assets/images/Petronas.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/12/Petronas.png) Torres Petronas
Si leyéramos que la altura de la [torres Petronas](http://ca.wikipedia.org/wiki/Torres_Petronas) en Kuala Lumpur es de 452,340 metros, podríamos pensar, con razón, que no tiene mucho sentido detallar los decímetros, centímetros y milímetros de la altura, con lo metros sería suficiente, debido a que unos milímetros más o menos no tienen importancia en este caso concreto.

La valoración del número de decimales correcto es una dificultad para muchos estudiantes; es típico usar una calculadora y dar como resultado demasiados decimales. ¿Cuál es el número correcto de decimales? Depende del problema que estemos resolviendo.

$caption id="attachment_537" align="alignnone" width="300"$[![calculadora](/taller-matematicas/assets/images/calculadora-300x181.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/12/calculadora.png) El número de decimales de un cálculo frecuentemente es infinito. El número de decimales significativo depende del problema concreto que estamos resolviendo: la media de calificaciones, las medidas de un estante, la longitud de una pieza de relojería, etc.
En Estadística los resultados nunca son precisos, al contrario se intenta averiguar cuanta probabilidad de certeza tiene una afirmación, una hipótesis o un resultado.

### Cálculo de probabilidades

Usaremos el clásico ejemplo de la moneda. Es de conocimiento general que, si la moneda no está trucada, la probabilidad de obtener cara o cruz al lanzarla es la misma: 1/2 para los dos resultados. ¿Qué significa realmente esta afirmación?  Significa que, en un gran número de tiradas, las frecuencias de obtención de cara y de cruz serían aproximadamente la mitad del total. En la tabla siguiente vemos una simulación por ordenador del lanzamiento de la moneda:

 

| **lanzamientos** 
| **caras** 
| **% caras** 
| **cruces** 
| **% cruces** 

| 10 
| 4 
| 40.00% 
| 6 
| 60.00% 

| 100 
| 41 
| 41.00% 
| 59 
| 59.00% 

| 200 
| 108 
| 54.00% 
| 92 
| 46.00% 

| 500 
| 280 
| 56.00% 
| 220 
| 44.00% 

| 1000 
| 485 
| 48.50% 
| 515 
| 51.50% 

Vemos que al aumentar el número de lanzamientos, los porcentajes de caras y cruces se van aproximando al 50% predicho. Pero en ningún caso ha coincido exactamente en ese 50%. Es una predicción aproximada, tanto más precisa como mayor sea el número de tiradas de la moneda. A este concepto de probabilidad, una aproximación a la frecuencia esperada, le podemos dar una definición más matemática:

**Definición 1**: Dado uno de los posibles resultados de un experimento, el cual repetimos *n* veces, la probabilidad de ese resultado se define como el límite, cuando *n* es muy grande, de la frecuencia relativa del resultado respecto al número total de repeticiones; si *x* es el número de veces que hemos obtenido el resultado, la frecuencia relativa es *x/n* y la probabilidad será
$P(\text{resultado})=\lim_{n\rightarrow\infty}\frac xn$

En el ejemplo de la moneda, la probabilidad 1/2 se obtiene de realizar infinitos lanzamientos de la moneda:

$P(cara)=\lim_{n\rightarrow\infty}\frac{\text{número de caras}}n$

**Regla de Laplace**

Para el cálculo práctico de las probabilidades no se usa la definición anterior, sino otros métodos, el más simple de ellos es la conocida regla de Laplace:

$P(\text{resultado})=\frac{\text{número de casos favorables}}{\text{número de casos totales}}$

Es un hecho notable que el valor de la probabilidad calculada con la regla de Laplace coincida con la de la definición 1, que usa límites.  La regla de Laplace tal como se ha dado supone que cada caso posible es igualmente probable, de lo contrario no funcionará.

**Ejemplo 1**: la regla aplicada al lanzamiento de la moneda, para obtener la probabilidad de obtener cara en un lanzamiento, es:

$P(\text{cara})=\frac{\text{número de caras}}{\text{número de casos totales}}=\frac12$

Esto es correcto siempre que todos los resultados (cara y cruz) sean igualmente probables. Si realizamos dos lanzamientos de la moneda y queremos saber la probabilidad de obtener al menos una cara, tendremos que contar los casos favorables y los posibles; abreviando por C el resultado "sale cara" y por "X" el resultado "sale cruz", los casos son:

casos posibles: CC, CX, XC, XX

casos favorables: CC, CX, XC

por tanto la P(al menos una cara en dos lanzamientos) = 3/4.

### Interpretación de la probabilidad como una frecuencia teórica

De la definición 1 podemos obtener una igualdad útil en los problemas:

$P(\text{resultado})=\lim_{n\rightarrow\infty}\frac xn\Leftrightarrow x\xrightarrow[\infty]{}n\cdot P(\text{resultado})$

Para el caso de un número de repeticiones muy elevado, tendremos la igualdad $x\approx n\cdot P(\text{resultado})$, donde $x$ es el número de repeticiones del resultado estudiado.

**Ejemplo 2**: La probabilidad de que una bombilla halógena recién fabricada sea defectuosa es del 0,01%. ¿Cuántas bombillas defectuosas esperamos encontrar en una remesa de 10.000 bombillas? Aplicamos la fórmula anterior, teniendo en cuenta que el número de "repeticiones" considerado (el número de bombillas) es elevado: $\text{número de defectuosas}\approx10.000\cdot\frac{0.01}{100}=1.$ Recordemos que esta cifra es solo una aproximación.

### Combinación de casos independientes

Volvamos al lanzamiento de dos monedas (o al lanzamiento de una moneda dos veces). Los resultados posibles eran CC, CX, XC, XX. Si nos preguntamos por la probabilidad de obtener cualquiera de estos resultados, como por ejemplo "sacar dos caras", obtenemos para todos ellos el valor 1/4 (un caso favorable de cuatro posibles), pero la probabilidad de obtener una cara es 1/2. Vemos que P(CC) = 1/4 = 1/2 · 1/2 = P(C)·P(C). Para tres monedas, los casos posibles son ocho: CCC, CCX, CXC, XCC, XXC, XCX, CXX, XXX, y la probabilidad de obtener cualquiera de estos resultados es de 1/8 = 1/2 · 1/2 · 1/2 = P(C)·P(C)·P(C). En general, la probabilidad de cada combinación posible al realizar n veces el lanzamiento se obtiene
multiplicando las probabilidades de todos los resultados que intervienen en la combinación, siempre que cada lanzamiento sea independiente del anterior, esto es, que los resultados no estén influenciados por los obtenidos anteriormente.

### Resultados no equiprobables

Cuando cada caso tiene una probabilidad distinta, no podemos aplicar la regla de Laplace. Debemos estudiar la probabilidad de cada caso.

**Ejemplo 3**: siguiendo con las bombillas del ejemplo 2, si compramos 3 bombillas, y las probamos ¿cuál es la probabilidad de que la primera sea defectuosa y las otras dos no?

La probabilidad de que una bombilla sea defectuosa es 0.0001, y de que no lo sea de 0.9999. Entonces como cada bombilla es independiente de las demás, la probabilidad del caso "defectuosa, correcta, correcta" será 0.0001·0.9999·0.9999=0.000099.

**Ejemplo 4**: siguiendo con las bombillas del ejemplo 2, si compramos 3 bombillas, ¿cuál es la probabilidad de que una sea defectuosa?

Llamemos C al resultado "pruebo una bombilla y es correcta", y D al resultado "pruebo una bombilla y es defectuosa". Las combinaciones posibles son CCC, CCD, CDC, DCC, DDC, DCD, CDD, DDD. No son igualmente probables, luego no podemos aplicar Laplace. La probabilidad de cada una de ellas se obtiene multiplicando las probabilidades de todos los resultados que intervienen en la combinación, teniendo en cuenta que P(C)=0.9999, P(D)=0.001. Obtenemos:

 

| **Caso** 
| **Probabilidad** 

| CCC 
| 0.99970003 

| CCD 
| 0.00009998 

| CDC 
| 0.00009998 

| DCC 
| 0.00009998 

| DDC 
| 0.00000001 

| DCD 
| 0.00000001 

| CDD 
| 0.00000001 

| DDD 
| 1E-012 

La probabilidad pedida "una es defectuosa", comprende tres casos: CCD, CDC, DCC. Sumemos ahora sus probabilidades: 0.00009998 + 0.00009998 + 0.00009998 = 0.00029994. 

Por otro lado, si sumamos las probabilidades de todos los casos posibles, el resultado es 1. Esta es una regla fundamental: la suma de probabilidades de todos los casos posibles es siempre igual a 1.

# Espacio muestral de un experimento aleatorio

Damos algunas definiciones básicas, y luego vemos sus propiedades y aplicaciones.
****Definición 2**: Dado un [experimento aleatorio](https://es.wikipedia.org/wiki/Experimento_aleatorio) (ver el tema [Estadística descriptiva, análisis de datos](http://tallermatematic.eu/wp/?p=1341)), su **espacio muestral** Ω es el conjunto de todos los posibles resultados del experimento. Ejemplos:

 	- Lanzamiento de un dado: Espacio muestral Ω = {1,2,3,4,5,6}, un conjunto de  6 elementos.

 	- Medición de la temperatura en un reactor químico: Ω contiene todos los valores reales positivos (espacio muestral infinito).

**Definición 3**: **Puntos muestrales **son cada uno de los posibles resultados de un experimento aleatorio; también podemos decir que son los elementos que componen el conjunto espacio muestral Ω del experimento. Ejemplos:  en el caso del dado los puntos muestrales son {1}, {2}, ... {6}.

**Definición 4**: **Sucesos.** Un suceso S es un subconjunto cualquiera del espacio muestral Ω de un experimento aleatorio. Ejemplo: para el experimento "lanzar un dado y anotar la puntuación" un suceso puede ser el subconjunto S = {2, 4, 6}. En particular un **suceso elemental** es un subconjunto formado por un único punto muestral, como S = {2}.

# [![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

# Álgebra de sucesos

Temporalmente, nos situamos en otra área: la [lógica de proposiciones](https://es.wikipedia.org/wiki/L%C3%B3gica_proposicional), aplicándola al caso de sucesos aleatorios.
**Definición 5**: Una **proposición lógica** P será una afirmación cualquiera sobre el resultado de un experimento aleatorio. Por ejemplo, en el caso del dado, algunas proposiciones son:

 	- P1: "Ha salido un número par"

 	- P2: "Ha salido un número mayor que 4"

 	- P3: "No ha salido mayor que 4"

 	- P4: "Ha salido un número par que es mayor que 2 y menor que 5"

La  correspondencia que estamos definiendo entre las proposiciones lógicas y los sucesos ha de cumplir:

 	- Cada proposición lógica se entenderá que se está refiriendo a algún suceso del espacio muestral Ω de un experimento aleatorio; este suceso es único: no pueden haber dos sucesos distintos relacionados con la misma proposición.

 	- En cambio, dado un suceso, podemos asociarle muchas proposiciones lógicas

En otras palabras, la relación entre entre el conjunto de proposiciones Σ de un experimento y el conjunto de sucesos Ψ del mismo experimento es una aplicación inyectiva (o de uno-a-muchos).

Ejemplo 5: para el experimento de lanzar un dado, con Ω = {1,2,3,4,5,6}:

 	- P1: "Ha salido un número par", se relaciona con el suceso S1 = {2, 4, 6}

 	- P2: "Ha salido un número mayor que 4", se relaciona con el suceso S2 = {5, 6}

 	- P3: "No ha salido mayor que 4", se relaciona con el suceso S3 = {1,2,3,4}

 	- P4: "Ha salido un número par que es mayor que 2 y menor que 5", se relaciona con el suceso S4 = {4}

Todas las proposiciones posibles respecto al experimento aleatorio son válidas, incluso aquellas que no tienen sentido, o son triviales:

 	- P5: "Ha salido un número mayor que 6", se relaciona con el subconjunto vacío S = ø, a este suceso se le llama suceso imposible.

 	- P6: "Ha salido un número entre 1 y 6", se relaciona con el conjunto total S = Ω = {1,2,3,4,5,6}, a este suceso se le llama suceso seguro.

**Álgebra de sucesos**
Dentro del conjunto de proposiciones se pueden definir operaciones lógicas que le proporcionan estructura algebraica: el [álgebra de Boole](https://es.wikipedia.org/wiki/%C3%81lgebra_de_Boole). Las [operaciones](https://es.wikipedia.org/wiki/%C3%81lgebra_de_Boole#Operaciones_en_.C3.A1lgebra_de_Boole) son: AND (y), OR (o), NOT (no). El resultado de una operación lógica entre proposiciones es otra proposición lógica.

**Ejemplo 6**:

 	- AND: P1: "Ha salido un número par", P2: "Ha salido un número mayor que 4", P = P1 y P2: "Ha salido un número par y mayor que 4".

 	- NOT: P1: "Ha salido un número par"; negación: P = No "Ha salido un número par"

 	- OR: P3: "No ha salido mayor que 4", P5: "Ha salido un número mayor que 6", P = P4 o P5: "O bien no ha salido mayor que 4, o bien ha salido un número mayor que 6"

También tenemos una correspondencia entre las operaciones lógicas y las operaciones en el espacio muestral:

   

| operación lógica** 
| **Operación entre conjuntos de ****Ω** 

| AND ("y") 
| Intersección de conjuntos, símbolo ∩ 

| OR ("o") 
| Unión de conjuntos, símbolo ∪ 

| NOT ("no") 
| Complementario de un conjunto S es Sc 

**Ejemplo 7**:

 	- A la proposición P = (P1 y P2) = ("Ha salido un número par" y "Ha salido un número mayor que 4") corresponde el suceso (S1∩ S2) = {2,4,6}∩ {5,6 } = {6}

 	- A la proposición P = no ("Ha salido un número par") corresponde el suceso complementario del {2,4,6} que es {1,3,5}

 	- **Sucesos excluyentes**: son aquellos que no tienen elementos en común, es decir, que su intersección es nula.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Regularidad estadística. Primera definición de probabilidad

Supongamos que realizamos N repeticiones de un experimento aleatorio y que formamos la tabla de frecuencias relativas. Entonces, el [principio de regularidad Estadística](https://en.wikipedia.org/wiki/Statistical_regularity) afirma que, conforme N se hace más grande, las frecuencias relativas de todos los resultados tienden a ser constantes.

**Ejemplo 8**: lanzamiento de una moneda. Tabla de frecuencias relativas
     

| 
Punto muestral

 
| 
N=10

 
| 
N=100

 
| 
N=1000

 

| 
“cara”

 
| 
4/10 = 0.4

 
| 
46/100 = 0.46

 
| 
502/1000 = 0.502

 

| 
“cruz”

 
| 
6/10 = 0.6

 
| 
54/100 = 0.54

 
| 
498/100 = 0.498

 

Se observa que las frecuencias relativas se estabilizan alrededor del valor 0.5. Tomamos este valor límite de la frecuencia relativa cuando N es muy grande como la primera definición de probabilidad:

**Definición 5**: **Probabilidad (frecuencialista) de un suceso S**. Dado un suceso S asociado al espacio muestral Ω de un experimento aleatorio, del cual podamos realizar un número cualquiera N de ejecuciones, la probabilidad P(S) del suceso viene dada por:
$P(S)=\underset{N\rightarrow\infty}{lim}f(S)$

donde f(S) representa la frecuencia relativa del suceso S cuando hacemos N repeticiones del experimento aleatorio.
**Ejemplo 9**: la probabilidad de S: "ha salido cara" en el experimento de lanzar la moneda es 0.5, pues ese el valor obtenido al simular por ordenador el lanzamiento un número elevado de repeticiones.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Segunda definición de probabilidad: regla de Laplace, combinatoria

Esta primera definición de probabilidad como límite de frecuencias relativas es útil para interpretar resultados de cálculos, pero no lo es para obtener probabilidades, pues obliga a realizar un límite de una frecuencia relativa, para la cual en general no tenemos ninguna expresión analítica. La siguiente definición, debida a Laplace, soluciona este inconveniente:

**Definición 6**: **Probabilidad de un suceso S, regla de Laplace. **Dado un suceso S asociado al espacio muestral Ω de un experimento aleatorio, si el número de puntos muestrales de S es card(S) y el número de puntos muestrales de Ω es card(Ω), la probabilidad P(S) del suceso viene dada por:
$P(S)=\frac{\text{card }\left(S\right)}{\text{card }\left(\Omega\right)}$

Ejemplo: la probabilidad de S: "ha salido cara" en el experimento de lanzar la moneda se calcula contando el número de puntos muestrales de S = {"cara"}, que es 1, y del espacio Ω = {"cara", "cruz"}, que es 2. Luego P("cara") = 1/2 = 0.5.

**Ejemplo 10**: la probabilidad de sacar un número par al lanzar un dado, según la regla de Laplace, es:

$P(par)=\frac{\text{card }\left(par\right)}{\text{card }\left(\Omega\right)}=\frac{\text{card }\left(\left\{2,4,6\right\}\right)}{\text{card }\left\{1,2,3,4,5,6\right\}}=\frac36=\frac12$

**Teoría combinatoria**
En casos simples es inmediato aplicar la regla de Laplace pero en general no será tan simple. Consideremos por ejemplo el siguiente problema: "*Una lotería está formada por N números, de los que m tendrán premio. Calcular la probabilidad de que nos toque algún premio si hemos comprado k números* ". Calcular el número de puntos muestrales ahora no es trivial. La [teoría combinatoria](https://en.wikipedia.org/wiki/Enumerative_combinatorics) proporciona técnicas directas para hacerlo; en nuestro caso la solución viene dada por:

$P(premio)=1-P(no\;premio)=1-\frac{C_{N-m,k}}{C_{N,k}}=1-\frac{\left(N-k\right)!\left(N-m\right)
}{N!\left(N-m-k\right)!}$
donde $C_{a,b}$ representan la combinaciones de a elementos tomados de b en b, y el símbolo ! representa la operación factorial. No trataremos esta teoría aquí, aunque en este blog hay una[ introducción a la teoría](http://tallermatematic.eu/wp/?p=1449) y se pueden encontrar algunos [problemas resueltos de combinatoria](http://tallermatematic.eu/wp/?p=1311).

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Tercera definición de probabilidad: axiomas y propiedades

La definición más moderna de probabilidad se debe a [Kolmogorov](https://es.wikipedia.org/wiki/Andr%C3%A9i_Kolmog%C3%B3rov):
**Definición 7**: **Probabilidad de un suceso S, Kolmogorov. **Dado un suceso S asociado al espacio muestral Ω de un experimento aleatorio, probabilidad es toda función P que asigna a cada suceso S de un espacio muestral un número P (S) comprendido en el intervalo [0, 1] y que además verifica las siguientes propiedades (axiomas de la probabilidad):
1. P (Ω) = 1
2. Si A, B son sucesos excluyentes, entonces P (A ∪ B) = P (A) + P (B)

Se puede demostrar que esta definición es más general que las dos anteriores: La regla de Laplace y el límite de la frecuencia relativa verifican los axiomas, pero hay probabilidades que no se pueden calcular con la regla de Laplace ni con frecuencias, y si según la definición de Kolmogorov.

De la definición de Kolmogorov se pueden deducir otras propiedades de la probabilidad:

 	- 
P(no S) = P(Sc) = 1 – P(S)

 	- 
P(suceso imposible) = P(ø) = 0

 	- 
P(A o B) = P(A∪ B) = P(A) + P(B) – P(A∩ B)

 	- Si el espacio muestral Ω se puede considerar dividido en n subconjuntos disjuntos entre sí, Ω = A1 ∪ A2 ∪ ... ∪ An, entonces P(A1) + P(A2) + ... + P(An) = 1

En las aplicaciones y problemas, se suele usar la definición 2 (Laplace) para calcular, la definición 1 para interpretar el significado de la probabilidad, y las propiedades de la probabilidad para simplificar los cálculos.

**Ejemplo 11:** *Calcular la probabilidad de que al lanzar dos dados simultáneamente, o bien la suma de las puntuaciones de ambos dados mayor que 6, o bien la puntuación de ambos dados sea al menos de 4. Si realizamos ese experimento 100 veces, ¿en cuantas de ellas esperaremos que se cumpla que "las puntuaciones de ambos dados mayor que 6 o bien la puntuación de ambos dados sea al menos de 4*"?

Definimos los sucesos S: "la suma de las puntuaciones de ambos dados mayor que 6", y T: "la puntuación de ambos dados sea al menos de 4". Para hallar las probabilidades por la regla de Laplace necesitamos contar los puntos muestrales (resultados posibles) de cada suceso y también del espacio total.

Resultados posibles para S: {1+6, 2+5, 2+6, 3+4, 3+5, 3+6, 4+3, 4+4, 4+5, 4+6, 5+2, 5+3, 5+4, 5+5, 5+6, 6+1, 6+2, 6+3, 6+4, 6+5, 6+6}, total 21

Resultados posibles para T:  {4+4, 4+5, 4+6, 5+4, 5+5, 5+6, 6+4, 6+5, 6+6}, total 9

Resultados posibles totales: tantos como parejas (a, b) podemos formar siendo a,b números entre 1 y 6: son 6·6 = 36.

Ahora aplicamos la tercera propiedad de Kolmogorov: P(S o T) = P(S∪T) = P(S) + P(T) – P(S ∩ T). Necesitamos calcular el número de puntos del conjunto (S ∩ T) = {1+6, 2+5, 2+6, 3+4, 3+5, 3+6, 4+3, 4+4, 4+5, 4+6, 5+2, 5+3, 5+4, 5+5, 5+6, 6+1, 6+2, 6+3, 6+4, 6+5, 6+6} ∩ {4+4, 4+5, 4+6, 5+4, 5+5, 5+6, 6+4, 6+5, 6+6} = {4+4, 4+5, 4+6, 5+4, 5+5, 5+6, 6+4, 6+5, 6+6} = T; esto sucede porque T está incluido en S (T es un subconjunto de S).

También se puede visualizar gráficamente: en una cuadrícula de 6 x 6 marcamos las casillas con una suma superior a 6 con un 1, y las que cumplen que los dos valores son al menos 4 las resaltamos en amarillo:

[![Valores posibles de las puntuaciones del lanzamiento de dos dados](/taller-matematicas/assets/images/exper_dos_daus.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/exper_dos_daus.png) Valores posibles de las puntuaciones del lanzamiento de dos dados; hay 21 combinaciones con suma > 6, y 9 combinaciones con los dos valores mayores o iguales a 4
Probabilidades según Laplace: P(S) = 21/36, P(T) = 9/36. P(S ∩ T) = 9/36

Probabilidad P(S o T) = P(S∪T) = 21/36 + 9/36 - 9/36 = 21/36.

Si repetimos N = 100 veces el lanzamiento de los dos dados, usando la definición 4 de probabilidad, esperaremos que en 100·21/36 = 58 ocasiones suceda que se cumpla que "la suma de puntuaciones de ambos dados mayor que 6 o bien la puntuación de ambos dados sea al menos de 4".

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Probabilidad condicionada. Sucesos independientes

Cuando tenemos un conocimiento parcial del resultado de un experimento aleatorio podemos utilizarlo para mejorar nuestras predicciones. Por ejemplo: sabemos que en un dado ha salido al menos un 4. ¿Cuál es ahora la probabilidad de que sea un número par? Si no utilizamos la información "ha salido al menos un 4" será, por la regla de Laplace:

P(par) = card {2,4,6} / card {1,2,3,4,5,6} = 3/6

Si en cambio utilizamos la información "extra", entonces el espacio muestral queda restringido a ser los puntos del suceso "ha salido al menos un 4" que son {4,5,6} y en el
suceso "número par" habrá que eliminar el punto {2} que es incompatible. Por lo tanto será:

P ("par" condicionada por "ha salido al menos un 4") = card {4,6} / card {4,5,6} = 2/3

En general:

**Definición 8**: Diremos que el **suceso A está condicionado por el suceso B** cuando el conocimiento parcial del resultado B modifica el espacio muestral original Ω, reduciéndolo a otro Ω', de tal modo que la probabilidad de A respecto a Ω' es diferente a la original respecto a Ω. La notación para la probabilidad de A condicionada a B es P (A | B).

Se puede demostrar fácilmente que la nueva función de probabilidad P (S | B) verifica los axiomas y propiedades de la probabilidad de Kolmogorov, y por tanto está bien definida.

**Sucesos independientes**

En el ejemplo anterior hemos visto que si A = {"un número par"} y B = {"ha salido al menos un 4"} entonces P (A) = 3/6 = 1/2, P (A | B) = 2/3, y las probabilidades no son las mismas. ¿Siempre será así? En general no.

**Definición 9**: Cuando tengamos que  P (A | B) = P (A) diremos que los sucesos A y B son **independientes**. El condicionamiento impuesto por B no afecta a A. En cambio cuando el condicionamiento si afecte a la probabilidad, diremos que los sucesos son **dependientes**,

En general se cumple que:
$P\left(A\vert B\right)=\frac{P\left(A\cap B\right)}{P\left(B\right)}$

Si los sucesos A, B son independientes, entonces:
$P\left(A\vert B\right)=\frac{P\left(A\cap B\right)}{P\left(B\right)}=P\left(A\right)\Rightarrow\boxed{P\left(A\cap B\right)=P\left(A\right)P\left(B\right)}$ [1]

 

**Interpretar correctamente la probabilidad condicionada**
Los conceptos de dependencia e independencia de sucesos, así como el condicionamiento suelen ser mal comprendidos la primera vez que los vemos. Por ejemplo, en los enunciados de problemas hay que distinguir claramente cuando nos están hablando de probabilidad condicionada o de probabilidad conjunta de dos sucesos; en el primer caso hay una información previa: un suceso se supone que ya ha sucedido, el otro no, mientras que en la probabilidad conjunta no hay esa información previa. Por ejemplo: En una urna hay 4 bolas de color azul, 6 de color rojo y 3 de color amarillo. Sacamos una bola al azar sin mirarla; suponiendo que alguien nos dice "no es de color amarillo", ¿cuál es la probabilidad de que sea roja? Esta es una probabilidad condicionada, pues ya ha sucedido el suceso "no es de color amarillo" (la información previa), y por tanto calcularemos:

P(roja | no es de color amarillo ) = P(roja ∩ no es de color amarillo ) / P(no es de color amarillo )

En cambio si sacamos una bola al azar y la pregunta es ¿cuál es la probabilidad de que simultáneamente suceda que la bola no sea amarilla y sea roja? el cálculo será simplemente P(roja ∩ no es de color amarillo ).

Consideremos otro experimento con la misma urna: sacamos una bola que resulta ser roja; la devolvemos a la urna, y a continuación volvemos a sacar una bola. Nos preguntamos por la probabilidad de que vuelva a ser roja. Aquí entra un nuevo elemento: si consideramos que las distintas extracciones (que son las repeticiones del mismo experimento aleatorio) son independientes entre sí, entonces la probabilidad entre extracciones no varia, dado que hemos devuelto la bola a la urna para que haya exactamente el mismo número de bolas en la segunda extracción. Entonces:

P(bola roja en cada extracción) = 6 / (4 + 6 + 3) = 6 / 13

P((roja en 1ª) Y (roja en 2ª extracción)) = P(roja en 1ª) · P(roja en 2ª extracción) = 6 / 13 · 6 / 13 = 36 / 13²

Aquí hemos usado la igualdad [1] para calcular la probabilidad P((roja en 1ª) Y (roja en 2ª extracción)), teniendo en cuenta que las extracciones son independientes.

**Sucesos realmente independientes**

¿Cuando podemos considerar que dos sucesos son independientes? Siempre que no se afecten el uno al otro por cualquier medio, ni queden afectados por agentes externos. Por ejemplo, en un laboratorio realizamos, por primera vez, un experimento con una cierta medida *M*, y la repetimos unos días después. Nos preguntamos por la probabilidad de haber cometido un error absoluto en la medida respecto al valor real *R*, *|R - M|*, mayor que una tolerancia e: P(|R - M| > e). ¿Esta probabilidad será la misma el primer dia y el segundo dia? Aquí es más delicado suponer independencia de sucesos, ya que hay diversos factores externos que pueden influir, por ejemplo, la segunda vez se tiene la experiencia de la primera, y podría ser que se procediera mejor en la preparación previa del experimento. También podría ser que los con los resultados de la primera prueba hubiéramos intercambiado información con otros compañeros de trabajo sobre el experimento en cuestión, de forma que en la segunda ocasión sabemos algo más. Por ello en esta situación es más arriesgado suponer que los sucesos son independientes.

**Ejemplo 11:** ([Nonplussed!: Mathematical Proof of Implausible Ideas](http://www.amazon.es/gp/product/B0046A9M7C/ref=as_li_ss_tl?ie=UTF8&camp=3626&creative=24822&creativeASIN=B0046A9M7C&linkCode=as2&tag=tallerma-21)![](http://ir-es.amazon-adsystem.com/e/ir?t=tallerma-21&l=as2&o=30&a=B0046A9M7C) - by Julian Havil): *Como condición para ser aceptado en un club de tenis un jugador novato N ha de jugar tres partidos contra dos miembros del club, que les llamaremos B (jugador de nivel bueno) y M (jugador de nivel medio). Para ser aceptado, N debe ganar dos partidos consecutivos de los tres. N debe elegir uno de las dos posibilidades: jugar en el orden  M, B, M o en el orden B, M, B. La pregunta es: ¿cuál es la mejor opción?*

Este es un buen ejemplo de que en ocasiones las probabilidades no son intuitivas en absoluto. Sin hacer ningún cálculo, de forma intuitiva, creeremos que el más importante es jugar lo menos posible con el jugador B, y por tanto la mejor opción es escoger el orden de juego M, B, M i no el B, M, B. Vamos a hacer el cálculo de probabilidades.

Supongamos que la probabilidad de que N venza a M es m, y de que venza a B es b, y que los sucesos son independientes (no afecta al partido siguiente el resultado del anterior).  En el orden de juego M, B, M, todas las combinaciones para vencer dos partidos consecutivos son: (vencer M, vencer B, vencer M), (vencer M, vencer B, perder M), (perder M, vencer B, vencer M). ¿Cuáles son las probabilidades de estas combinaciones? Son:

 	- P(vencer M, vencer B, vencer M) = m·b·m

 	- P(vencer M, vencer B, perder M) = m·b·(1-m)

 	- P(perder M, vencer B, vencer M) = (1-m)·b·m

Observar que para calcular la probabilidad de perder aplicamos la 1ª propiedad de la probabilidad de Kolmogorov: P(no S) = 1 – P(S). La probabilidad de vencer dos partidos consecutivos en el orden M, B, M será la suma de las anteriores probabilidades, ya que los sucesos (vencer M, vencer B, vencer M), (vencer M, vencer B, perder M), (perder M, vencer B, vencer M) son mutuamente excluyentes: la suma es mbm + mb(1-m) + (1-m)bm = bm(m + 1 - m + 1 - m) = bm(2 - m).

Hacemos lo mismo para el orden de juego B, M, B. Las combinaciones y sus probabilidades son:

 	- P(vencer B, vencer M, vencer B) = b·m·b

 	- P(vencer B, vencer M, perder B) = b·m·(1-b)

 	- P(perder B, vencer M, vencer B) = (1-b)·m·b

La suma es b·m·b + b·m·(1-b) + (1-b)·m·b = bm(b + 1 - b + 1 - b) = bm(2 - b)

Como b < m (menos probabilidad de ganar el jugador bueno que el medio), resulta que bm(2 - b) > bm(2 - m), o sea que en el orden de juego B, M, B el jugador novicio tiene más probabilidades de vencer en dos partidos consecutivos que en el orden M, B, M, !incluso siendo  que deberá jugar dos partidos contra el mejor jugador en vez de sólo uno! Un resultado contra intuitivo, pero rigurosamente cierto.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

**Ejemplo 12:  **Consideremos el mismo problema del club de tenis pero esta vez incorporando aspectos subjetivos; si el jugador novicio gana en un partido al jugador de mejor nivel B, consideraremos que su motivación aumenta y también mejorará su nivel de juego; por otro lado si pierde contra el jugador de nivel medio M entonces bajará ligeramente. **
**

 	- si gana a B, sus probabilidades de ganar en el siguiente partido, que eran m, b respectivamente, pasan a ser m', b', que cumplirán m < m' < 1, b < b' < 1. Concretamente, es P( ganar a M | haber ganado B) = m', P( ganar a B | haber ganado B) = b'

 	- si pierde con M, sus probabilidades de ganar en el siguiente partido, que eran m, b respectivamente, pasan a ser m'', b'', que cumplirán m'' < m < 1, b'' < b < 1

Ahora estamos considerando probabilidades condicionadas: la probabilidad de ganar un partido depende del resultado del partido anterior. Rehacemos los cálculos; para el orden de juego M, B, M

 	- P(vencer M, vencer B, vencer M) = m·b·m'

 	- P(vencer M, vencer B, perder M) = m·b·(1-m)

 	- P(perder M, vencer B, vencer M) = (1-m)·b''·m'

La suma de estas probabilidades es m·b·m' + m·b·(1-m) + (1-m)·b''·m' = mbm' + mb - m²b + m'b'' - mm'b'' = mm'(b - b'') + mb(1 - m) + m'b''

para el orden de juego B, M, B. Las combinaciones y sus probabilidades son:

 	- P(vencer B, vencer M, vencer B) = b·m'·b'

 	- P(vencer B, vencer M, perder B) = b·m'·(1-b')

 	- P(perder B, vencer M, vencer B) = (1-b)·m·b

La suma de estas probabilidades es b·m'·b' + b·m'·(1-b') + (1-b)·m·b = bm'b' + bm' - bm'b' + mb - b²m = bm' + bm - bbm

¿Cuál es ahora la mejor opción? Para simplificar, damos valores concretos a las probabilidades: m = 0.7, b = 0.5, m'=0.8, b'= 0.6, m''= 0.6, b''=0.4. Sustituimos:

 	- P(ingresar en el club jugando M, B, M) =  mm'(b - b'') + mb(1 - m) + m'b'' = 0.7·0.8·(0.5 - 0.4) + 0.7·0.5(1 - 0.7) + 0.8·0.4 = 0.481

 	- P(ingresar en el club jugando B, M, B) = bm' + bm - bbm = 0.5·0.8 + 0.5·0.7 - 0.5·0.5·0.7 = 0.575

Vemos que sigue siendo la mejor opción la que incluye más partidos contra el mejor jugador.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

**Ejemplo 13**: En una encuesta, al 29% le gusta la música clásica. Este 29% se desglosa en un 17% que no les gusta la música moderna y un 12% que también les gusta la música moderna. Por otro lado en un 68% sólo les gusta la música moderna y a un 3% no les gusta la música. Planteamos el experimento aleatorio: preguntar a una persona al azar sobre sus gustos musicales. Sean los sucesos siguientes:

 	- M: le gusta la música moderna

 	- X: sólo le gusta un tipo de música

La pregunta que nos hacemos es: ¿Son M y X independientes? Dicho de otro modo, el conocimiento previo de que a una persona les guste la música moderna condiciona el que le guste sólo ese tipo de música?

Representamos los datos en un diagrama:

[![condicionada](/taller-matematicas/assets/images/condicionada-300x143.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/09/condicionada.png)

Hacemos los cálculos teniendo en cuenta el diagrama:

 	- P(M) =P("sólo moderna" O "clásica y también moderna") = 0.68 + 0.12 = 0.8

 	- P(X) = P("sólo moderna" O "sólo clásica") = 0.68 + 0.17 = 0.85

 	- P(X ∩ M) = P(“sólo un tipo de música” Y “sí la moderna”) = P("sólo moderna" ) = 0.68

 	- P(X)·P(M) = 0.85 · 0.8 = 0.68

Resulta que P(X∩ M) = P(X) · P(M), por tanto X, M son independientes

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

# Teoremas de la probabilidad total y de Bayes

**Teorema 1 (de la probabilidad total)**: Si tenemos un conjunto de sucesos B1, B2, ..., Bn excluyentes entre sí de tal forma que el espacio muestral Ω pueda expresarse como la unión = B1∪ B2∪ ...∪ Bn, (decimos queB1, B2, ..., Bn es una **partición de Ω**)  y además conocemos las probabilidades P(B1), P(B2) ... P(Bn), entonces para cualquier suceso A se cumple:

$P(A)=\sum_{i=1}^nP\left(A\vert B_i\right)\cdot P\left(B_i\right)$

**Teorema 2 (de Bayes)**: En las mismas condiciones del teorema anterior tendremos que:
$P(B_k\;\vert\;A)=\frac{P\left(B_k\right)\cdot P\left(A\;\vert\;B_k\right)}{\sum_{i=1}^nP\left(A\;\vert\;B_i\right)\cdot P\left(B_i\right)}$

Equivalentemente, usando el teorema de la probabilidad total:

$P(B_k\;\vert\;A)=\frac{P\left(B_k\right)\cdot P\left(A\;\vert\;B_k\right)}{P\left(A\right)}$

**Ejemplo 14**: El 20% de cierta población tiene estudios superiores, el 60% medios y el 20% básicos. Sabemos que leen habitualmente algún periódico local el 40% de los que tienen estudios superiores, el 25% de lo que tienen estudios medios y el 10% de los que tienen estudios básicos. Elegida una persona al azar resulta que lee habitualmente algún
 periódico. ¿Cuál es la probabilidad de que tenga estudios superiores?

La población total está dividida en tres conjuntos disjuntos B1: estudios superiores, B2: medios, B3: básicos. Sabemos las probabilidades condicionadas siguientes: si escogemos al azar una persona, y resulta que tiene estudios superiores, entonces P(leer | B1) = 0.4. Igualmente, P(leer | B2) = 0.25, P(leer | B3) = 0.1. La probabilidad pedida tiene una información previa: "resulta que lee habitualmente algún periódico", por tanto es condicionada, es: P(estudios superiores | lee). Usamos el teorema de Bayes:

$P(superiores\;\vert\;lee)=\frac{P\left(superiores\right)\cdot P\left(lee\;\vert\;superiores\right)}{\sum_{i=1}^nP\left(lee\;\;\vert\;B_i\right)\cdot P\left(B_i\right)}$

Calculamos primero el denominador, que es la probabilidad total de leer un periódico en esa población, sin tener en cuenta el factor estudios:

$\sum_{i=1}^nP\left(lee\;\;\vert\;B_i\right)\cdot P\left(B_i\right)=0.4\cdot0.2+0.25\cdot0.60+0.10\cdot0.20=0.25$

Un 25% de la población lee habitualmente un periódico. Sustituimos en el teorema de Bayes:

$P(superiores\;\vert\;lee)=\frac{0.2\cdot0.4}{0.25}=0.32$

La probabilidad de que una persona con estudios superiores sea lector es superior a la media de la población, 25%, como era de esperar.

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Bibliografia

***Métodos Estadísticos***: Lo utilicé cuando estudiaba en la UNED, y tengo un buen recuerdo, porque no era muy extenso pero contenía todo el temario bastante bien explicado. Otra parte que me gustó fue que cada capítulo tiene una lista de problemas (ejercicios de autocomprobación) con las soluciones, perfecto para estudiar a distancia. En definitiva, no es una biblia de la Estadística Aplicada ni mucho menos, pero para introducirte en los temas básicos (Estadística descriptiva, probabilidades, variables aleatorias, funciones de distribución, intervalos de confianza, contrastes de hipótesis y ANOVA) cumple bien.
{% endraw %}