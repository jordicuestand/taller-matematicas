---
layout: post
title: "Acústica: música"
date: 2017-08-26 11:18:09 +0000
categories:
  - "Acústica"
  - "Fí­sica"
tags:
  - "acorde musical"
  - "armónicos"
  - "Escala atemperada"
  - "frecuencia de resonancia"
  - "frecuencias propias"
  - "intervalo musical"
  - "nodo"
  - "ondas estacionarias"
  - "resonancia"
  - "tubos sonoros"
math: true
---
{% raw %}

La sucesión de sonidos con ciertas características especiales la denominamos *música*. El oído es capaz de percibir, dados dos sonidos emitidos en sucesión, la relación entre sus frecuencias (o tonos), esa relación se denomina *intervalo musical*. Por ejemplo, dados dos sonidos a 300Hz y 150Hz, el oído notará que entre ellos existe la misma relación que entre otros dos de 800Hz y 400Hz, ya que el intervalo es el mismo para las dos secuencias, 300:150 = 800:400 = 2. En la siguiente grabación puede escucharse dos secuencias de 11 notas cada una formando las denominadas escalas musicales (concretamente la escala pentatónica);  las relaciones de frecuencias entre las notas son las mismas en ambas escalas, pero la primera escala tiene una frecuencia superior.

[audio m4a="http://tallermatematic.ovh/wp/wp-content/uploads/2017/08/Veu-023.m4a" mp3="http://tallermatematic.ovh/wp/wp-content/uploads/2017/08/Veu-023.mp3"][/audio]

Si se producen dos sonidos simultáneamente, o muy cercanos en el tiempo, nos producirá una sensación agradable (*acorde musical*) cuanto más simple sea su intervalo musical. Los más simples son 2:1 (intervalo llamado *octava*), 3:2 (*quinta*), 4:3 (*cuarta*) y 5:4 (*tercera mayor*), que eran los más utilizados en la música clásica antigua.
### Escalas musicales

Como la musicalidad de una secuencia de sonidos no depende de sus frecuencias sino de la relación entre sus frecuencias, podemos escoger libremente una frecuencia base cualquiera. Tomemos un sonido de frecuencia f como base (tono fundamental, o *tónico*), y lo denominamos *do*. A continuación definimos los intervalos musicales, por ejemplo, si tomamos los intervalos (5:4)f, (4:3)f, (3:2)f, (5:3)f y (2:1)f obtendremos los sonidos que, relativos al base *do*, se denominan *mi, fa, sol, la, do'*.  Habremos obtenido una escala musical. ¿Que relación guardan entre si las frecuencias de esta escala? En la siguiente tabla vemos las relaciones f:f' de cada nota respecto a la fundamental do, una columna donde, multiplicando las relaciones f:f' por el factor 12 se convierten a enteros, y una última columna que descompone en producto de dos factores esos enteros.
   

|  **Nota** 
| **f:f’** 
| **12·f:f’** 
| **factores** 

| **do** 
| 1 
| 12 
| 4x3 

| **mi** 
| 1 1/4 
| 15 
| 5x3 

| **fa** 
| 1 1/3 
| 16 
| 4x4 

| **sol** 
| 1 1/2 
| 18 
| 6x3 

| **la** 
| 1 2/3 
| 20 
| 5x4 

| **do’** 
| 2 
| 24 
| 6x4 

Hay subgrupos de tres acordes con relaciones especialmente simples: do-mi-sol y fa-la-do', sus tablas de relaciones son:
  

|  **Nota** 
| **f:f’** 
| **4·f:f’** 

| **do** 
| 1 
| 4 

| **mi** 
| 1 1/4 
| 5 

| **sol** 
| 1 1/2 
| 6 

|  
|  
|  

|  **Nota** 
| **f:f’** 
| **3·f:f’** 

| **fa** 
| 1 1/3 
| 4 

| **la** 
| 1 2/3 
| 5 

| **do’** 
| 2 
| 6 

Vemos que sus frecuencias tienen relaciones simples iguales entre sí, de 4:5:6. La denominada escala diatónica natural añade otras dos notas, siendo 8 en total: *re*, con relación (9:8)f, y *si*, con relación (15/8)f. La tabla de relaciones queda:
   

| **Nota** 
| **f:f’** 
| **24·f:f’** 
| **factores** 

| **do (base)
** 
| 1 
| 24 
| 8x3 

| **re (segunda mayor)
** 
| 1 1/8 
| 27 
| 9x3 

| **mi (tercera mayor)
** 
| 1 1/4 
| 30 
| 6x5 

| **fa (cuarta)
** 
| 1 1/3 
| 32 
| 8x4 

| **sol (quinta)
** 
| 1 1/2 
| 36 
| 9x4 

| **la (sexta)
** 
| 1 2/3 
| 40 
| 8x5 

| **si (séptima)
** 
| 1 7/8 
| 45 
| 9x5 

| **do’ (octava)
** 
| 2 
| 48 
| 8x6 

Con estas dos notas, encontramos un nuevo acorde de tres notas especialmente simple: re-sol-si, con una relación mutua de frecuencias de  3:4:5. En Música, además de la nomenclatura do, re, mi, etc. se usa también la abreviada con letras A, B, C, ...
### Instrumentos musicales de cuerda

Una cuerda tensa, pulsada o bien frotada, oscilará con un *movimiento armónico simple amortiguado*; al hacerlo, presionará el aire que la rodea de forma que generará una onda de presión de frecuencia constante: un sonido de tono dado. La frecuencia de vibración es más alta como menor sea la longitud de la cuerda, y como más tensa esté; el grosor de la cuerda también interviene, cuanto más grosor, menos frecuencia.

Instrumentos como el piano o el arpa tienen una cuerda dedicada a cada nota (o frecuencia); en la guitarra acústica y en el violín el músico varía la frecuencia modificando la longitud de la cuerda vibrante. Si pulsamos la cuerda no por el centro exacto sino por diferentes puntos se obtendrá la misma nota pero con diferente timbre (vibraciones adicionales, o *armónicos*, añadidas a la vibración fundamental de la cuerda), y un oído entrenado podrá detectarlo.

![](/taller-matematicas/assets/images/so-5.png) Fig. 1: oscilaciones del tono fundamental y del primer armónico (octava del fundamental)
### Cuerdas vibrantes en música

Una *cuerda* es un hilo elástico con sección pequeña comparada con su longitud. Cuando una cuerda tensada por sus extremos se golpea, pulsa o frota en un punto, la perturbación se propaga por la cuerda hasta los extremos, donde se reflejan e interactúan entre sí formando vibraciones en forma de *ondas estacionarias* con los nodos en los extremos, y cada punto de la cuerda describe un movimiento armónico simple; para ello, la cuerda ha de contener o bien media onda (dos nodos), o una onda completa (tres nodos, dos en los extremos y uno en el centro), o una onda y media (cinco nodos), y en general un número impar de nodos y un múltiplo entero de "medias ondas completas".  Por ello, las vibraciones de la cuerda cumplen que la longitud l de la cuerda ha de ser un múltiplo entero de la semilongitud de la onda: $l=n\frac\lambda2$, y la frecuencia sonora será $f=\fracv\lambda=n\fracv{2l}$ para n = 1, 2, 3, .... , donde v es la velocidad de transmisión de la perturbación en la cuerda, que depende del material y de la tensión de la cuerda. A estas frecuencias se les llama *frecuencias propias* de la cuerda. Si intentamos hacer vibrar a una cuerda con frecuencias distintas de las propias, la vibración se amortiguará muy rápidamente debido a que la interferencia de la onda transmitida y la reflejada será destructiva: una anula a la otra.
### Escala atemperada

En las guitarras, también en los violines, el músico puede variar la frecuencia del sonido a voluntad de forma continúa, variando la posición del dedo que pulsa la cuerda.

![](/taller-matematicas/assets/images/escala-atemperada.png) Fig. 2: Parte del teclado de un piano mostrando la escala atemperada de 13 notas, las teclas negras son los semitonos.

En cambio en el piano, instrumento en el que la cuerda se golpea con un pequeño martillo siempre en la misma posición, las frecuencias son fijas. Cuando se quiere acompañar con el instrumento musical a la voz de una cantante, con las frecuencias variables se puede ajustar la escala musical a la frecuencia de la voz

demos hacerlo, pero para solventar en parte este problema se recurre a la denominada *escala atemperada*: se parte de la escala natural que se divide en 12 intervalos iguales (por tanto contiene 13 notas) añadiendo nuevas notas llamadas *semitonos*, o *notas sostenidas*, marcadas con el símbolo #. Las nuevas notas sostenidas se destacan en negro.
La escala atemperada completa queda así:

*do, do#, re, re#, mi, fa, fa#, sol, sol#, la, la#, si, do'*

Al dividir la escala natural en 12 intervalos en vez de los 7 originales sucede que las frecuencias de las notas de la escala atemperada no coinciden con la natural, excepto en las notas inicial y final (do y do'). Esta escala facilita la acomodación de frecuencias a la voz, pero incluyendo una pequeña variación de las relaciones de frecuencias, perceptible al oído entrenado musicalmente.

[Más sobre escalas musicales](https://www.lpi.tel.uva.es/~nacho/docencia/ing_ond_1/trabajos_05_06/io2/public_html/escalas.html).
### Instrumentos de viento

Cuando se vacía una vasija de agua, se percibe el borboteo como una sucesión de notas que van disminuyendo de tono a medida que se vacía, o sea, cuando la cavidad de aire se hace mayor. Se produce una vibración del aire (*onda longitudinal*) dentro de la vasija, un sonido, con una *frecuencia inversamente proporcional a la longitud de la columna de aire vibrante*, igual que sucede con las cuerdas vibrantes.

En los tubos sonoros, cilindros llenos de aire, se generan sonidos al hacer vibrar el aire que contienen. También se presentan modos fundamentales de vibración y modos armónicos en las columnas de aire, sólo que en este caso hay que diferenciar los casos en que el tubo sea semi-abierto al aire (fig. 3), o sea cerrado sólo en un extremo, o totalmente abierto; en el primer caso, en la pared de cierre para todos los modos vibratorios siempre habrá un *nodo* (punto de vibración nula), mientras que para los tubos abiertos los nodos están en el interior, y en los extremos abiertos siempre encontramos *vientres* (puntos de vibración máxima).

![](/taller-matematicas/assets/images/tub_acustic_obert_BO.png) Fig. 3: tercer armónico y modo fundamental de vibración en un tubo sonoro semiabierto

En los *tubos sonoros* la onda longitudinal de aire generada en un extremo se refleja en el otro extremo, la onda interfiere consigo misma, formando un sistema de *ondas estacionarias*. Si el tubo es semiabierto, la onda al chocar con la pared del extremo cerrado cambia 90⁰ de fase, y las dos ondas, transmitida y reflejada, se anulan en ese punto, formando un nodo; en el extremo abierto, que es donde generamos la vibración, tenemos un vientre. En el modo fundamental (fig. 3 a la derecha) en el tubo hay un sólo nodo y un sólo vientre, como la onda completa comprende dos nodos y dos vientres, llamando $\lambda$ a la longitud de onda y l a la longitud del tubo, tendremos la relación, para el modo fundamental, $l=\frac\lambda4$, y la frecuencia f de ese modo será $f=\fracv\lambda=\fracv{4l}$, donde v es la velocidad del sonido. En general si se presentan n nodos en el tubo, estando uno de ellos siempre en el extremo cerrado, teniendo en cuenta que cada dos nodos corresponden a una longitud de onda de distancia, tendremos que los n nodos ocupan dentro del tubo una distancia $n\lambda/2$, desde el último nodo hasta el extremo abierto del tubo hay una distancia $\lambda/4$ (pues hay un vientre en el extremo), y por tanto la longitud total l del tubo se distribuye así:
$l=n\frac\lambda2+\frac\lambda4=\frac{2n\lambda+\lambda}4=\left(2n+1\right)\frac\lambda4$

y por tanto la frecuencia del modo con n nodos es:
$f=\frac v\lambda=\left(2n+1\right)\frac v{4l}$.

El factor (2n + 1) nos indica que en los tubos semiabiertos sólo se emiten los armónicos impares (las frecuencias de los armónicos sin múltiplos impares de la frecuencia fundamental). Queda como ejercicio demostrar que esto no sucede en los tubos abiertos.

En los *órganos* hay un tubo de longitud fija para cada tono, de forma semejante a los pianos (fig. 4), en cambio en la flauta la longitud efectiva del tubo la puede variar el músico con los dedos.

![](/taller-matematicas/assets/images/sagrada-familia-organo-205x300.jpg) Fig. 4: tubos del órgano de la basílica de la Sagrada Familia, en Barcelona
### Resonancia acústica

Dos sistemas vibratorios con la misma frecuencia pueden interactuar y producir fenómenos de resonancia, en el que las energías de los dos sistemas se suman, o bien se transmite la energía de un sistema al otro.

![](/taller-matematicas/assets/images/resonancia-acustica.png) Fig. 5: resonancia entre un diapasón y una columna de aire cercana

En la figura 5 se presenta un experimento de resonancia acústica: tomamos un tubo semiabierto con agua dispuesto de forma que podamos variar la altura del líquido (vaso comunicante), cerca del extremo abierto hacemos sonar un diapasón, veremos que el tubo también emite un sonido, pues el aire que contiene vibra por efecto del diapasón. Si vamos probando a variar la altura del líquido hasta que una de las frecuencias del tubo coincida con la del diapasón, más exactamente, cuando la longitud de la columna de aire sea un múltiplo de un cuarto de la longitud de onda del diapasón, en ese momento entrarán en resonancia y el tubo emitirá un sonido intenso, ya que se estará transmitiendo eficientemente la energía vibratoria del diapasón al aire del tubo.  Esta transmisión eficiente provoca que el sonido del diapasón se disipe rápidamente, pues transfiere toda su energía al aire del tubo. Las cajas de madera de algunos instrumentos (guitarra, violín) se utilizan para reforzar los sonidos por resonancia, y por ello se denominan *cajas de resonancia*.
#### Bibliografía usada

Ambas obras están descatalogadas, siendo textos excelentes, he intentado aprovechar la información que daban para que no se pierda en el olvido. La figura 5 proceden de la primera obra:

 	- M. Catalán, Andres León: Física y Química – Madrid, 1945

 	- J. Fernandez, M. Pujal: Iniciación a la Física – Barcelona, 1975
{% endraw %}