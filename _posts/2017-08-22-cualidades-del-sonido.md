---
layout: post
title: "Cualidades del sonido"
date: 2017-08-22 09:04:30 +0000
categories:
  - "Acústica"
  - "Fí­sica"
tags:
  - "armónicos"
  - "audición"
  - "bel"
  - "decibel"
  - "infrasonidos"
  - "sonido"
  - "timbre"
  - "tono"
  - "ultrasonidos"
math: true
---
{% raw %}

### Sonidos musicales y sonidos ruidosos

Las vibraciones de un cuerpo, al afectar al aire que lo rodea, producen un movimiento ondulatorio de ese aire, o sea, una propagación de las vibraciones del cuerpo, que cuando llega a nuestros oídos podemos percibir como sonido. Las vibraciones del aire toman la forma de [ondas de presión](https://es.wikipedia.org/wiki/Onda_de_presi%C3%B3n). Cuando las vibraciones son periódicas, esto es, repetitivas en el tiempo, sentimos ese sonido como musical, en otro caso lo calificamos como ruido.

[caption id="attachment_150528" align="alignnone" width="1280"]![](/assets/images/20170822_084811.jpg) Fig. 1: un diapasón, una varilla rectangular doblada en forma de horquilla, vibra de forma armónica simple al ser golpeado en un extremo[/caption]
### Tono de un sonido

Es la frecuencia de la vibración del cuerpo que produce el sonido. El diapasón de la figura 1 produce un sonido que vibra a una frecuencia muy precisa, de 136 Hz (un Hertz, o Hz, es un ciclo vibratorio completo por segundo). Percibimos el tono más grave o más agudo dependiendo de su frecuencia, de menor a mayor, respectivamente; el tono del sonido también se conoce por altura del sonido.

[caption id="attachment_150529" align="alignnone" width="300"]![](/assets/images/so-1-300x183.png) Fig.2: ondas sinusoidales, como las que produce un diapasón. La línea azul representa un sonido de la mitad de tono que la linea roja.[/caption]

En la figura 2 vemos las formas sinusoidales de los sonidos puros, como el producido por un diapasón;  las abscisas representan el tiempo y las ordenadas la amplitud de la vibración. Las dos sinusoides tienen la misma amplitud pero diferente frecuencia: la curva roja presenta dos ciclos completos, la azul sólo uno, por lo que el tono del sonido en el primer caso es el doble que en el segundo. Los instrumentos musicales pueden emitir sonidos en diferentes rangos de frecuencias; los del violín están entre 250 y 15.000 Hz, la voz humana, entre 125 y 9.000 Hz. El rango de frecuencias audibles para los humanos es de 20 a 20.000 Hz.
### Intensidad de un sonido

Se relaciona con la amplitud de la vibración. En la figura 3 vemos dos sonidos sinusoidales con la misma frecuencia (los dos oscilan dos veces completas en el mismo intervalo de tiempo) pero el representado en rojo tiene el triple de amplitud que el azul. Si fueran sonidos de diapasones, las dos curvas serian diapasones idénticos, sólo que uno ha sido golpeado con una fuerza tres veces superior al otro; en cambio, en la figura 2, serian dos diapasones distintos golpeados con la misma fuerza impulsora.

[caption id="attachment_150530" align="alignnone" width="300"]![](/assets/images/so-2-300x185.png) Fig. 3: dos oscilaciones sinusoidales de la misma frecuencia y distinta amplitud.[/caption]

El tímpano del oído humano es muy sensible a las vibraciones del aire, de forma que para producir un sonido audible ([umbral de audición](https://es.wikipedia.org/wiki/Umbral_de_audici%C3%B3n)) es suficiente con muy poca energía vibratoria: la potencia de la vibración sonora generada cuando conversamos es de sólo 10⁻⁵ Wats, o sea, que para generar 1W de potencia sonora, deberíamos reunir 100.000 personas conversando a la vez.
### Timbre de un sonido

Los sonidos musicales consistentes en una única vibración simple, con una frecuencia e intensidad únicas, como la sinusoidal del diapasón, no son lo habitual, al contrario, las vibraciones sonoras suelen ser una superposición de vibraciones simples, suele haber una onda predominante, o **oscilación fundamental**, acompañada de otras secundarias, que la deforman (figura 4).

[caption id="attachment_150531" align="alignnone" width="600"]![](/assets/images/so-3.png) Fig. 4: sonido de un instrumento, en este caso de la tecla de un piano, mostrando pequeñas deformaciones que acompañan a la onda fundamental.[/caption]

Las vibraciones que deforman la onda fundamental, pero manteniendo su periodicidad (sino fuera así, ya no seria un sonido musical, seria un ruido), se denominan **armónicos del sonido**. Cuando oímos dos sonidos de la misma intensidad y tono, pero procedentes de dos instrumentos musicales distintos, los percibimos como distintos debido a que sus armónicos lo son, decimos que los dos sonidos **difieren en timbre** cuando difieren sus armónicos. Tono, intensidad y timbre determinan completamente un sonido.
### Audición. Decibelios.

[caption id="attachment_150532" align="alignnone" width="706"]![](/assets/images/so-4.png) Fig. 5: Área normal de audición, en frecuencias-decibelios.[/caption]

El oído no es igualmente sensible a todas las frecuencias, de forma que las intensidades mínimas audibles (umbral de la audición) dependen de las frecuencias. Además, también hay un límite superior para la potencia que el tímpano puede soportar: vibraciones demasiado potentes pueden dañarlo, deja de producirse la sensación auditiva y pasamos a sentir dolor (umbral del dolor). En la figura 5, en el eje de abscisas están las frecuencias, aproximadamente entre 16Hz y 16.000Hz; como el rango es muy amplio, la escala no es lineal (no nos cabría el gráfico en horizontal) sino logarítmica; lo mismo podemos decir de la escala de ordenadas. Se ha representado en ese eje las teclas de un piano para hacernos una idea del rango de frecuencias.  Para una frecuencia dada, por ejemplo la de más a la izquierda del piano, trazando una línea vertical cortará al área audible, resultando un segmento que nos dice el rango de intensidades audibles para esa frecuencia, que es prácticamente de cero a 120.

Para la medida de intensidades se utilizan los decibelios. La ley de Weber y Fechner establece que la sensación S percibida no es lineal, sino que depende del logaritmo de la intensidad I:
$S=A\log\left(I\right)+B$ [1]

donde A, B son dos constantes que dependen de las unidades físicas que tomemos. Si al valor umbral de la intensidad audible lo llamamos $I_0$, entonces:
$0=A\log\left(I_0\right)+B\Leftrightarrow B=-A\log\left(I_0\right)$

sustituyendo en [1]:

$S=A\log\left(I\right)-A\log\left(I_0\right)=A\left(\log\left(I\right)-\log\left(I_0\right)\right)=A\log\left(\frac I{I_0}\right)$

Definiendo la unidad de sensación sonora, el bel, como aquella que hace que A = 1, resulta que la sensación de intensidad sonora, en bels, es:

$S=\log\left(\frac I{I_0}\right)$

La unidad más usada no obstante es la décima parte del bel, o decibel: $S=10\log\left(\frac I{I_0}\right)$ cuando $I, I_0$ vienen dadas en decibels. como en la figura 5. Siendo el oído no igualmente sensible a todas las frecuencias, un sonido de 20db de 300Hz se percibirá más débil que otro también de 20db pero a 1000Hz. La sensibilidad máxima del oído está aproximadamente a 2500Hz.

### Infrasonidos y ultrasonidos

Las frecuencias demasiado bajas para ser audibles por los humanos se denominan infrasonidos, y las demasiado altas, ultrasonidos. En explosiones, erupciones volcánicas, golpes bruscos, se generan ruidos de diversas frecuencias, también en el rango de infrasonidos, que algunos animales sí pueden detectar. Los ultrasonidos pueden generarse artificialmente mediante una lámina de cristal de cuarzo vibrando entre dos electrodos de metal, aprovechando el [efecto piezoeléctrico](https://es.wikipedia.org/wiki/Piezoelectricidad).  El cristal, colocado en un campo eléctrico alterno, se contrae y se dilata periódicamente a alta frecuencia, de hasta millones de Hz. Los ultrasonidos se difractan poco en el agua, pueden dirigirse muy bien, y a frecuencias adecuadas, se amortiguan lentamente, recorriendo decenas de km bajo el agua, por lo que son útiles para el sondaje del mar.
#### Bibliografía usada

Ambas obras están descatalogadas, siendo textos excelentes, he intentado aprovechar la información que daban para que no se pierda en el olvido. Las figuras 4 y 5 proceden de la primera obra:

 	- M. Catalán, Andres León: Física y Química - Madrid, 1945

 	- J. Fernandez, M. Pujal: Iniciación a la Física - Barcelona, 1975
{% endraw %}