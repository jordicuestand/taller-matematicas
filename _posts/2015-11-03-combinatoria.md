---
layout: post
title: "Combinatoria"
date: 2015-11-03 13:26:37 +0000
math: true
---

La combinatoria es la teoría matemática que trata de las técnicas para contar el número de elementos de un subconjunto, o el número de subconjuntos de un conjunto, o el número de listas de elementos del conjunto determinados por un criterio. Algunos problemas de [probabilidades](http://tallermatematic.eu/wp/?p=1389) utilizan estas técnicas, de las que  aquí vemos un repaso breve.

**Ejemplo 1**: ¿de cuántas formas se puede escoger un comité de tres personas de entre cinco candidatos? Aquí el conjunto son los cinco candidatos, y queremos saber el número de subconjuntos distintos de tres elementos, el criterio es simplemente que cada subconjunto tenga tres personas, sin importar nada más.

## Combinaciones de elementos

Dado un conjunto de n elementos, si queremos saber cuantos subconjuntos de m elementos podemos formar, sin tener ningún criterio adicional de selección, entonces estamos combinando n elementos tomados de m en m, y la solución al problema viene dada por el número combinatorio $C_{m,n}=\begin{pmatrix}m\\n\end{pmatrix}$, que se calcula del siguiente modo:

$\begin{pmatrix}n\\m\end{pmatrix}=\frac{n!}{\left(n-m\right)!\cdot m!}=\frac{n\cdot\left(n-1\right)\cdot\left(n-m+1\right)}{m!}$ [1]

**Ejemplo 2**: La solución a la pregunta planteada en el ejemplo 1 es $\begin{pmatrix}5\\3\end{pmatrix}=\frac{5!}{\left(5-3\right)!\cdot3!}=\frac{5\cdot4\cdot3}{3!}=\frac{60}6=10$

## Variaciones

Dados m objetos distintos, queremos saber el número de listas ordenadas distintas de n elementos que podemos formar con los m objetos; el criterio de formación incluye la ordenación: el orden de selección de los elementos afecta el resultado. Decimos que realizamos variaciones de n elementos tomados de n en n, y la notación será $V_{m,n}$.

**Ejemplo 3**: ¿de cuántas formas se puede escoger un presidente, un secretario y un vocal de entre cinco candidatos? Aquí el conjunto son los cinco candidatos, y queremos formar una lista (presidente, secretario, vocal), de forma que el primer candidato seleccionado será el presidente, el segundo será secretario y el tercero será el vocal. Son por tanto variaciones de m = 5 elementos tomados de n = 3 en 3:  $V_{5,3}$.

La fórmula que nos da el número de variaciones es:

$V_{m,n}=\frac{m!}{n!}=m\cdot\left(m-1\right)\cdot\dots\cdot\left(m-n\right)$ [2]

Entonces la solución del ejemplo 3 es:

$V_{m,n}=\frac{5!}{2!}=5\cdot4\cdot3=60$

## Permutaciones

Dados m objetos distintos, queremos saber el número de listas ordenadas distintas de m elementos que podemos formar con los m objetos. Es el mismo caso de las variaciones, pero las listas escogen todos los m elementos. Diremos que estamos permutando los elementos del conjunto, y el número de permutaciones lo representamos y calculamos así:

$P_m=m!$. [3]

**Ejemplo 4**: Tres amigos van al cine y se sientan juntos en la misma fila; ¿de cuántas formas distintas pueden hacerlo? Son permutaciones de 3 elementos, y su número es $P_3=3!=6$.

### Relación entre combinaciones, variaciones y permutaciones

Observará el lector que:

$C_{m,n}=\frac{m!}{\left(m-n\right)!\cdot n!}=\frac{m!}{\left(m-n\right)!}\frac1{n!}=\frac{V_{m,n}}{P_n}$
Esta relación se puede interpretar del siguiente modo: *al dividir el número de listas ordenadas de n elementos por el número de ordenaciones de n elementos, es como si no contáramos el orden, por lo cual obtenemos las combinaciones*.

**Ejemplo 5**: Tres amigos van al cine pero esperan a tres amigos más, así que se sientan en una fila de 6 asientos; ¿de cuantas formas pueden escoger sus tres asientos, a) teniendo en cuenta el orden, b) sin importar el orden en que se sientan?

En el caso a son variaciones de m=6, n= 3, por tanto: $V_{6,3}=6·5·4=120$; en el segundo caso, al no importar el orden, "descontamos" de los casos anteriores las permutaciones de los tres amigos entre sí, que son $P_3=3!=6$, resulta 120/6 = 20. El mismo resultado obtenemos aplicando directamente la formula de las combinaciones: $C_{6,3}=\frac{6!}{\left(6-3\right)!\cdot3!}=\frac{6\cdot5\cdot4}6=20=\frac{V_{6,3}}{P_3}$.

## Repeticiones

Si cuando formamos grupos o listas tomados de un conjunto de m objetos podemos escoger más de una vez cada objeto, decimos que hay repeticiones. Dependiendo del caso, tendremos combinaciones con repetición, variaciones con repetición, o permutaciones con repetición.
### Combinaciones con repetición

Dado un conjunto de objetos de m tipos distintos, si queremos saber cuantos subconjuntos de n elementos podemos formar, sin tener en cuenta el orden, en los cuales cada elemento del conjunto puede ser seleccionado más de una vez, vendrá dado por:
$CR_{m,n}=\begin{pmatrix}m+n-1\\n\end{pmatrix}=\frac{\left(m+n-1\right)!}{\left(m-1\right)!\cdot n!}$ [4]

**Ejemplo 6**: Una urna contiene un gran número de bolas blancas y  bolas rojas. Sacamos 4 bolas. Atendiendo sólo a los colores,  ¿cuantas posibilidades tenemos?

Llamando B a la bola blanca y R a la roja, obtendremos secuencias como RRBB, RBBB, etc. El orden "interno" entre las bolas blancas, y entre las bolas rojas no importa. El número m = 2, y n = 4, así pues:

$CR_{2,4}=\begin{pmatrix}2+4-1\\4\end{pmatrix}=\begin{pmatrix}5\\4\end{pmatrix}=5$

### Variaciones con repetición

Dados m objetos distintos, queremos saber el número de listas ordenadas distintas de n elementos que podemos formar con los m objetos, tenciendo en cuenta que podemos elegir cada elemento más de una vez en las listas:
$VR_{m,n}=m^n$ [5]

**Ejemplo 7**: Tenemos que escoger un delegado de curso, un coordinador de excursiones, y un tutor de prácticas, de entre un grupo de 10 profesores. Sabiendo que un mismo profesor puede acumular varios cargos, ¿de cuantas formas posibles podremos hacerlo?

Hay que formar listas ordenadas (delegado, coordinador, tutor) de n=3 nombres de profesores, de entre 10 posibles, esto son variaciones, pero teniendo en cuenta que los tres nombres pueden ser iguales: variaciones con repetición,

$VR_{m,n}=m^n=10^3$

### Permutaciones con repetición

Dados m objetos, de los cuales hay grupos iguales entre sí de $k_1, k_2, ...k_p$  elementos, si queremos formar listas ordenadas de todos los m elementos, las formas posibles de hacerlo son:
$PR_{m,h_1,h_2,\dots,h_p}=\frac{m!}{h_1\cdot h_2!\cdot\dots\cdot h_p!}$ [6]

**Ejemplo 8**: Dado el conjunto de 9 vocales {A,A,E,E,I,O,O,O,U}, ¿cuantas palabras distintas de 9 letras podemos formar con ellas?

Cada palabra será una permutación de las 9 vocales, como por ejemplo {A,E,E,A,I,O,U,O,O}, pero al haber vocales repetidas no podemos aplicar la formula de permutaciones [3], sino que hay que aplicar la [6], teniendo en cuenta que las repeticiones son: 2 para la A y la E, 3 para la U:

$PR_{9,2,2,1,3,1}=\frac{9!}{2!\cdot2!\cdot1\cdot3!\cdot1!}=15120$

## Criterios complejos de formación de las listas

La dificultad de los problemas de combinatoria se presenta cuando tenemos criterios de formación de los subconjuntos o listas que son complicados de relacionar con los conceptos vistos. En ese caso hay que combinar los conceptos anteriores con el ingenio. Un ejemplo clásico:

**Ejemplo 6**: Cinco mujeres y tres hombres van al cine y se sientan en ocho asientos contiguos. ¿De cuantas formas pueden sentarse que cumplan la condición "al lado de un hombre siempre hay una mujer"? Consideramos los hombres indistinguibles entre sí, y lo mismo con las mujeres.

La condición
 que nos dan no coincide con ninguna de las vistas, hay que recurrir al ingenio; representemos por H y M a un hombre y una mujer cualquieras; sentemos a los tres hombres con al menos un asiento de separación entre ellos:

[H][ ][H][ ][H]

 En los asientos entre hombres coloquemos mujeres cualesquiera:

[H][M][H][M][H]

Nos quedan 3 mujeres y 3 asientos por ocupar; como los hombres ya tienen una mujer al lado, las restantes las podemos colocar en cualquier sitio restante, que puede ser al principio, entre el 1º y 2º hombres, entre el 2º y el 3º, o al final, por ejemplo:

**[M]**[H][M][H][M][H]**[M][M] **o [H][M]**[M]**[H]**[M][M]**[M][H], etc ...**
**

Por tanto hay 4 posiciones posibles distintas para las mujeres restantes: 1[H][M]2[H][M]3[H]4, escogemos 3 posiciones, teniendo en cuenta que podemos repetirlas; por ejemplo los dos ejemplos anteriores corresponden a las selecciones 144, 233 respectivamente. Así pues, escogemos tres cifras de un conjunto de 4, con repetición, y sin que importe el orden (la selección 144 equivale a la selección 441): son combinaciones con repetición de 4 elementos tomados de 3 en 3:

$CR_{4,3}=\begin{pmatrix}4+3-1\\3\end{pmatrix}=\begin{pmatrix}6\\3\end{pmatrix}=\frac{6!}{3!\cdot3!}=\frac{6\cdot5\cdot4}6=20$.

**Ejemplo 7**: Es importante entender bien los conceptos para no errar al aplicarlos; para verlo, consideremos una "solución alternativa" al ejemplo 6: esta vez consideramos que, como cada hombre ha de tener una mujer al lado, manejamos parejas en vez de sujetos aislados. Sean las parejas HM, HM, HM, ¿de cuántas formas podemos sentarlas en los 8 asientos? Como cada pareja ocupa dos asientos, es como si consideramos asientos dobles, tendremos 8/2 = 4 asientos dobles, y tres parejas para sentar: $C_{4,3}=\begin{pmatrix}4\\3\end{pmatrix}=\frac{4!}{3!\cdot1!}=4$ formas posibles. Una vez colocadas las parejas, nos quedan 2 mujeres por colocar en 2 asientos libres, que pueden ser cualesquiera: el análisis es el mismo de antes, las posiciones pueden ser cuatro, a la izquierda, entre la pareja 1 y 2, entre la 2 y 3, o al final, y las dos mujeres pueden ir en la misma posición: combinaciones con repetición de 4 elementos tomados de dos en dos: $CR_{4,2}=\begin{pmatrix}4+2-1\\2\end{pmatrix}=\begin{pmatrix}5\\2\end{pmatrix}=\frac{5!}{2!\cdot3!}=\frac{5\cdot4}2=10$. El total de combinaciones serà 10·4 = 40. Pero además, podemos considerar las parejas en el orden MH, MH, MH, y repitiendo todo el razonamiento tenemos 40 posibilidades más, luego en total son 80 ... un momento ... ¡nos han resultado cuatro veces más combinaciones que por el método anterior! ¿Dónde está el error? Queda como ejercicio, podeis comentar vuestra solución en el [FB del blog](https://www.facebook.com/tallermatematic/). ¡Ánimo!