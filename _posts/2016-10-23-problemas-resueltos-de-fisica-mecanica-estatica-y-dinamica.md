---
layout: post
title: "Problemas resueltos de Física -> Mecánica -> Estática"
date: 2016-10-23 13:34:03 +0000
categories:
  - "Fí­sica"
  - "Mecánica"
tags:
  - "estática"
  - "momento fuerza"
  - "rozamiento"
math: true
---
{% raw %}

Colección de problemas resueltos de Estática a nivel medio, tratando los conceptos de equilibrio de fuerzas y momentos de las fuerzas.

**1** - Un cuerpo está sostenido por tres cables que forman unos ángulos con la vertical de 28⁰, 47⁰ y 53⁰. Las tensiones de los cables son 12, 10 y 16,2 kilopondios. ¿Cuál es el peso del cuerpo?

[caption id="attachment_150227" align="aligncenter" width="287"]![Fig. 1: diagrama de fuerzas estáticas](/assets/images/estatica1.png) Fig. 1: diagrama de fuerzas estáticas (los ángulos de las tensiones no se corresponden con los del enunciado)[/caption]
Como el cuerpo esté en reposo, tiene aceleración nula, y por tanto la suma (vectorial) de fuerzas ha de ser nula. La figura 1 muestra las cuatro fuerzas que intervienen; las descomponemos según los ejes XY e igualamos su suma a cero:

$\begin{array}{l}\left.\begin{array}{r}X)\;-12\sin\left(28\right)-10\sin\left(47\right)+16.2\sin\left(53\right)=0\\Y)\;12\cos\left(28\right)+10\cos\left(47\right)+16.2\cos\left(53\right)-mg=0\end{array}\right\}\\\end{array}$

La 1ª ecuación es una igualdad que ha de cumplirse, no hay incógnitas en ella; si no se cumpliera, es por que hemos equivocado el esquema de fuerzas (figura 1): obsérvese que no sabíamos por el enunciado si eran como muestra la figura. Se ha supuesto así por lógica: para que se anulen la componente horizontal de la suma de tres fuerzas, dos de ellas han de ir en sentido contrario que la tercera, y hemos supuesto que las dos de módulo menor, 12 y 10 Kp van en un sentido y la mayor, de 16,2Kp va en el otro sentido. En general se podría plantear la 1ª ecuación como $\;l_112\sin\left(28\right)+l_210\sin\left(47\right)+l_316.2\sin\left(53\right)=0$, con los coeficientes $l_1,l_2,l_3$ que pueden valer 1 o -1, pero de forma que dos de ellos tengan el mismo signo y el tercero signo contrario. Hay 6 combinaciones posibles, y para cada una con hoja de cálculo vemos que valor toma la primera igualdad:

   

| **l1** 
| **l2** 
| **l3** 
| **Ec1** 

| 1 
| 1 
| -1 
| 0 

| 1 
| -1 
| 1 
| 11,2 

| -1 
| 1 
| 1 
| 14,6 

| -1 
| -1 
| 1 
| 0 

| -1 
| 1 
| -1 
| -11,2 

| 1 
| -1 
| -1 
| -14,6 

Vemos que hay dos combinaciones posibles; la segunda, (-1, -1, 1) es la que hemos tomado, la otra es la versión simétrica, que también era posible, y nos lleva al mismo resultado. Pero de hecho observad que no necesitamos la 1ª ecuación para nada, para calcular la masa podemos ir directamente a la ecuación 2, de la que despejamos la masa del cuerpo:

$\begin{array}{l}12\cos\left(28\right)+10\cos\left(47\right)+16.2\cos\left(53\right)-mg=0\Rightarrow\\m=27,2Kp\;/\;g\;=\;\boxed{27,2Kg}\end{array}$

![separador2](/assets/images/separador2.png)

**2**. Una escalera de 20 peldaños, 20Kg de peso y 5,5m de longitud se apoya, sin rozamiento apreciable, en una pared vertical. El extremo inferior de la escalera está a una distancia de 3,2m de la pared. El coeficiente de rozamiento entre la escalera y el suelo vale 0,4. Un operario, que pesa P kilogramos, empieza a subir por la escalera. Deducir si la escalera deslizará antes de que el operario llegue arriba en función de su peso P, y decir en qué peldaño estará cuando ocurra el deslizamiento.

En la figura 1 vemos la geometría del problema, con las fuerzas en juego (en rojo).

[caption id="attachment_150213" align="aligncenter" width="380"]![Fig. 1: problema del operario y la escalera](/assets/images/dinamica_basica1.png) Fig. 1: problema del operario y la escalera[/caption]
El peso P se supone aplicado en el centro de gravedad del operario, situado a una distancia variable *x* de la base de la escalera, mientras que el peso de la escalera está aplicado en el punto medio de la escalera. Hay una única fuerza de rozamiento $F_R$ variable aplicada a la base de la escalera, y dos fuerzas normales N, una en el suelo y otra en la pared. La escalera empezará a deslizar cuando la fuerza de rozamiento $F_R$ tenga alcance su valor máximo, a partir del cual no podrá garantizarse el equilibrio de todas la fuerzas; **este equilibrio obliga a que la suma (vectorial) de todas las fuerzas sea cero**: ${\textstyle\sum_i}{\overrightarrow F}_i=0$. Usando como ejes el propio suelo y la pared, y origen de coordenadas el punto O, el equilibrio de fuerzas se expresa así:

$\left.\begin{array}{r}N_2-F_R=0\\N_1-P-20g=0\end{array}\right\}$[1]

Hay demasiadas incógnitas, necesitamos más relaciones; nos las proporcionan la **condición de equilibrio de los momentos de las fuerzas**: el momento total de todas las fuerzas respecto a cualquier punto arbitrario ha de ser cero en situación de equilibrio.  Recordemos que el momento de una fuerza F que es aplicada en un punto p respecto a otro punto q es el producto vectorial

${\overset\rightharpoonup M}_q=\overrightarrow{qp}\times\overrightarrow F$ [2]

donde ${\overset\rightharpoonup M}_q$ es el **pseudovector momento** respecto al punto q (para repasar el concepto de pseudovector tenéis mi artículo [Vectores en Física](http://tallermatematic.ovh/wp/index.php/2016/08/11/vectores/)).

Calculemos los momentos respecto al punto O:

Momento de la fuerza $N_2$: en la figura 2 vemos que las componentes del vector fuerza son $\left(N_2,0\right)$ y las del vector posición del punto de aplicación p de la fuerza, respecto al origen de momentos O, es $\overrightarrow{Op}=\left(0,4.5\right)$, el valor 4,5 viene de aplicar el T. de Pitágoras al triángulo rectángulo escalera-suelo-pared.

[caption id="attachment_150214" align="aligncenter" width="270"]![Fig. 2: cálculo del momento](/assets/images/dinamica_basica2.png) Fig. 2: cálculo del momento[/caption]
Calculamos el producto vectorial:

$\overrightarrow{Op}\times{\overrightarrow N}_2=\begin{vmatrix}\widehat i&amp;\widehat i&amp;\widehat k\\0&amp;4.5&amp;0\\N_2&amp;0&amp;0\end{vmatrix}=\left(0,0,-4.5N_2\right)={\overset\rightharpoonup M}_O\left({\overrightarrow N}_2\right)$

El  momento que obtenemos es perpendicular al plano, dirigido hacia abajo; en realidad, el producto vectorial de dos vectores perpendiculares siempre es perpendicular al plano que los contiene y tiene por módulo su producto de módulos y una dirección dada por la "regla del tornillo" o ["de la mano derecha"](https://es.wikipedia.org/wiki/Regla_de_la_mano_derecha);  si los vectores son paralelos entonces su producto vectorial vale cero.

Momento de la fuerza $N_1$: hay que multiplicar el vector $ON_1$ = (3.2, 0) por el vector ${\overrightarrow N}_1=(0,N_1)$, como ambos son  perpendiculares, usando la regla mencionada, resulta ${\overset\rightharpoonup M}_O\left({\overrightarrow N}_1\right)=(0,0,3.2N_1)$.

Momento de la fuerza $F_R$: como el vector posición $OF_R$ es paralelo a la fuerza $F_R$, el momento es cero.

Momentos de las fuerzas peso del operario P y peso de la escalera: El momento del peso del operario lo obtenemos a partir del vector de posición del operario, Oq, dónde q es el punto situado a x metros del punto de apoyo de la escalera sobre el suelo; sus componentes son $\overrightarrow{Oq}=\left(3.2-\frac{32x}{55},\frac{45x}{55},0\right)$, las distancias las calculamos usando las razones de los triángulos semejantes (figura 3).

[caption id="attachment_150216" align="aligncenter" width="247"]![Fig. 3: cálculo del vector de posición del operario, Oq](/assets/images/dinamica_basica3.png) Fig. 3: cálculo del vector de posición del operario, Oq[/caption]
El momento del peso del operario es:

${\overset\rightharpoonup M}_O\left(\overrightarrow P\right)=\begin{vmatrix}\widehat i&amp;\widehat j&amp;\widehat k\\3.2-\frac{32x}{55}&amp;\frac{45x}{55}&amp;0\\0&amp;-P&amp;0\end{vmatrix}=-P\left(3.2-\frac{32x}{55}\right)\widehat k$

NOTA: cuando todos los vectores fuerza y posición están en el mismo plano, los momentos siempre serán perpendiculares al plano, con sentido dado por la regla de la mano derecha; entonces para determinar el módulo se puede recurrir a imaginar que el vector fuerza se desliza por su línea de acción hasta quedar perpendicular al vector posición, tomando la nueva distancia, más reducida, para calcular el momento:  en la figura 4 el vector peso se ha deslizado hasta quedar perpendicular al vector OO', donde O' es el nuevo punto de aplicación del peso del operario. Calculamos entonces por triángulos semejantes la distancia l, y la OO' = 3,2 - l. Resulta ser 3.2 - 3.2x/5.5. Por tanto el momento será un vector perpendicular al plano, dirigido hacia "abajo" (el sentido de giro del vector peso respecto a O es en el sentido de las agujas del reloj), y de módulo $P\left(3.2-\frac{32x}{55}\right)$, resultado que coincide con el encontrado por producto vectorial.

[caption id="attachment_150217" align="aligncenter" width="280"]![Fig. 4: deslizamiento del vector peso P hasta quedar perpendicular al vector posición OP para el cálculo del momento respecto a O](/assets/images/dinamica_basica4.png) Fig. 4: deslizamiento del vector peso P hasta quedar perpendicular al vector posición OP para el cálculo del momento respecto a O[/caption]
El último momento es el de la escalera, que usando el método de vector deslizante y la regla de la mano derecha vale (3.2/2)·20 dirigido hacia abajo.

Sumamos todos los momentos e igualamos a cero (sólo consideramos las componentes no nulas, las otras ya son cero):

$\begin{array}{l}-P\left(3.2-\frac{32x}{55}\right)-\frac{3.2\cdot20}2+3.2N_1-4.5N_2=0\Leftrightarrow\\3.2N_1-4.5N_2+\frac{32x}{55}P=3.2P+32\end{array}$ [3]

Todavía tenemos más incógnitas $N_1,N_2,F_R,x$ que ecuaciones, tres de momento, las [1] y la [3]. Recordemos ahora que la fuerza de rozamiento cumple, en general, $F_R\leq\mu\cdot N$ siendo N la fuerza normal de reacción aplicada entre las superficies en contacto y $\mu$ el coeficiente de rozamiento; como estamos buscando el límite de deslizamiento, la fuerza de rozamiento será máxima: $F_R=0.4\cdot N_1$. Sustituimos en la primera de las dos ecuaciones [1] y obtenemos:

$\left.\begin{array}{r}N_2-0.4N_1=0\\N_1-P-20g=0\end{array}\right\}\Rightarrow\boxed{N_1=P+20g};\;\Rightarrow\boxed{N_2=0.4\left(P+20g\right)}$

Sustituimos en la [3], despejando *x*, dejando el peso P como parámetro:

$\begin{array}{l}\left[3.2P+64g\right]-\left[3.2-\frac{3.2}{5.5}x\right]P-32g-\left[1.8P+36g\right]=0\Rightarrow\\\boxed{x=\frac{5.5}{3.2}\left(1.8+\frac{4g}P\right)}\end{array}.$

Para ver como afecta el peso P del operario a la distancia máxima x alcanzada subiendo los peldaños, introducimos la expresión anterior en una hoja de cálculo y creamos un gráfico peso-distancia x: ![Fig. 5: relación entre el peso P y la distancia x subiendo las escaleras](/assets/images/dinamica_basica5.png)

Fig. 5: relación entre el peso P y la distancia x subiendo las escaleras
Para llegar arriba de la escalera el operario debería pesar sólo unos 2Kg, a partir de ese peso la distancia x decrece rápidamente pero se estabiliza a partir de los 20Kg de peso, quedando prácticamente constante, cercano a x = 3,2m, que son unos (3,2/5,5)·20 = 12 peldaños. En efecto, haciendo el límite en la expresión de x: $\lim_{P\rightarrow\infty}\frac{5.5}{3.2}\left(1.8+\frac{4g}P\right)=\frac{5.5}{3.2}1.8=3,09375$, vemos la distancia x prácticamente no varía, entre 11 y 12 peldaños para un peso P > 40Kg.

![separador2](/assets/images/separador2.png)
{% endraw %}