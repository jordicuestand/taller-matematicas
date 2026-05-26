---
layout: post
title: "Trabajo, calor, 1r principio de la Termodinámica"
date: 2018-07-31 13:09:27 +0000
categories:
  - "Fí­sica"
  - "Termodinámica"
tags:
  - "bomba de calor"
  - "Carnot"
  - "ciclo térmico"
  - "diagrama Clapeyron"
  - "diagrama PV"
  - "ecuación de estado"
  - "Energía interna"
  - "irreversibilidad"
  - "primer principio"
  - "reversibilidad"
  - "trabajo"
  - "transformación isobárica"
  - "transformación isócora"
  - "transformación isotéŕmica"
math: true
---
{% raw %}

La *Termo-dinámica* se ocupa de la dinámica (movimiento, transferencia) térmica, y utiliza las magnitudes temperatura, volumen, presión, energía, calor y trabajo para relacionarlas entre sí. El intercambio calor-energía-trabajo supondremos que se realiza entre un "sistema" - una parte del Universo delimitada por un volumen cerrado - y su entorno - el resto del Universo - , aunque a menudo restringiremos el entorno a las denominadas "fuentes térmicas" que definiremos. Entonces, hay magnitudes que utilizaremos para definir el *estado termodinámico del sistema*, y otras para definir su evolución o cambio de estado. Si tenemos alguna ecuación matemática que relacione entre sí las magnitudes que definen el estado, la llamaremos *ecuación de estado*; un ejemplo conocido de ecuación de estado es la de los gases perfectos, PV = nRT.

### Diagramas PV de Clapeyron

Una herramienta útil para entender y trabajar con cambios de estado es el diagrama de presión y volumen, que muestra como un punto cada valor de esas magnitudes, y como una línea su evolución estado a estado.  Por ejemplo, consideremos un gas encerrado en un cilindro con un émbolo encima del cual hemos colocado un conjunto de pequeños pesos, que vamos quitando uno a uno (figura 1).

$caption id="attachment_150669" align="alignnone" width="168"$![](/taller-matematicas/assets/images/gas-piston.png) Fig. 1: un gas comprimido en un pistón con una presión P que variamos quitando unos pequeños pesos[/caption]

El  gas, cuando no tocamos los pesos, y si lo hemos dejado en reposo, estará en *equilibrio termodinámico*: no hay flujo de calor y la presión y volumen están estables; tendrá una presión P y un volumen V representados por el punto A del diagrama PV (figura 2).

$caption id="attachment_150671" align="alignnone" width="376"$![](/taller-matematicas/assets/images/clapeyron1.png) Fig.2: diagrama PV de Clapeyron, mostrando cambios irreversibles AB, BA', A'B', ...[/caption]

Entonces levantamos uno de los pesos y la presión disminuye bruscamente: el sistema está ahora en el punto B, que no es un estado de equilibrio (no es estable), entonces el gas se expande espontáneamente hasta alcanzar el punto A' que vuelve a ser de equilibrio.  Vamos repitiendo el procedimiento con los otros pesos, y el gas va pasando por los estados  A",  A''', ...etc hasta llegar al estado final C. La línea continua azul que une todos los estados de equilibrio A, A', ..., C representa una transformación suave desde el estado inicial A hasta el final C sin que el sistema deje de estar en equilibrio.

En general, un cambio brusco en una magnitud saca del equilibrio al sistema: decimos que es un* cambio de estado irreversible*; sólo si los cambios son tan progresivos y suaves que, en cada momento, el sistema sólo se desvía del equilibrio una cantidad infinitesimal, de forma que podemos considerar que el sistema evoluciona estando siempre en equilibrio, entonces diremos que es un *cambio de estado reversible*. Los cambios que se ven como una función escalonada en el diagrama de Clapeyron son todos irreversibles, mientras que la línea azul continua que une estados de equilibrio A y C representa una transformación reversible.

Para estar siempre en equilibrio y no obstante cambiar de estado, las variaciones han de ser continuas: imaginemos que en lugar de los pesos de la figura 1 usamos arena, y que vamos quitando la arena grano a grano, entonces tendremos una buena aproximación a una transformación reversible; se llama así porque en cualquier estado intermedio entre A y C podríamos volver a poner los granos de arena y el sistema recorrería el camino inverso de C hacia A de forma suave: se puede revertir con una modificación infinitesimal. En cambio si realizamos una transformación brusca irreversible como la A->B, si queremos "deshacerla" no basta con una modificación infinitesimal de la presión, pues la presión exterior ha variado bruscamente y una modificación infinitesimal de la presión no detendrá la expansión del gas que seguirá evolucionando hacia el estado B. En definitiva:
Una transformación reversible mantiene al sistema siempre en equilibrio, y puede revertirse cambiando infinitesimalmente las condiciones. Una transformación irreversible aleja al sistema del equilibrio y no  puede revertirse cambiando infinitesimalmente las condiciones.
El estudio de las tranformaciones irreversibles, la *termodinámica de los procesos irreversibles,* es considerablemente más complicada que la de los procesos reversibles, a las cuales dedicaremos el resto de este artículo.
### Cambios isobáricos, isotérmicos, isócoros

En el ejemplo del gas en un cilindro de la figura 1, en el cambio brusco de estado AB varia la presión pero no el volumen, que aumenta: decimos que es una *transformación isócora*. Cuando el gas se expande en el cambio BA', lo hace a presión constante: es una *transformación isobárica*.

$caption id="attachment_150672" align="alignnone" width="596"$![](/taller-matematicas/assets/images/bany-tèrmic.png) Fig. 3: sistema de la figura 1 envuelta en un baño térmico a temperatura constante[/caption]

Si mantenemos la temperatura constante, por ejemplo fabricando el cilindro de un material muy conductor del calor y rodeándolo de un baño térmico (un entorno que no varia de temperatura por su gran capacidad calorífica, por ejemplo, una habitación acondicionada o una piscina, figura 3) entonces es una *transformación isotérmica;* supongamos que el sistema es un gas perfecto, entonces se cumplirá, para una transformación isotérmica, que PV = cte, y la representación gráfica de la curva de estados de equilibrio del gas ideal en el diagrama PV será una hipérbola con asíntotas en los ejes, tal como la línea azul de la figura 2.
### Trabajo realizado por dilatación

Supongamos que tenemos un sistema delimitado por una superficie S, sujeto a una presión exterior P, que se está dilatando. El trabajo W realpizado al desplazarse una distancia x contra una fuerza F es W = S·x, y la fuerza total ejercida por la presión F sobre la superfície S es F = P·S. Pensemos en una dilatación infinitesimal del sistema, de forma que sus límites se muevan una distancia dx y su superfície aumente en dS; el trabajo elemental realizado contra la presión exterior será dW = dF·dx = P·dS·dx, pero el producto dS·dx es igual al incremento de volumen dV = dS·dx. luego dW = P·dV, integrando entre el volumen inicial y el volumen final nos queda
$W=\int_{V_1}^{V_2}P\operatorname dV$ [1]

En el diagrama PV, esta integral coincide con el área bajo la curva de cambio de estado (figura 4)

$caption id="attachment_150673" align="alignnone" width="341"$![](/taller-matematicas/assets/images/treball-pv.png) Fig. 4: El trabajo realizado por el sistema al expandirse de A a B es el área rayada[/caption]

Si en vez de una expansión tenemos una contracción, el desplazamiento cambia de signo, y el trabajo resultante es negativo: es trabajo realizado sobre el sistema. Tenemos pues: si el sistema realiza un trabajo W, éste tendrá un valor positivo, y si se realiza un trabajo sobre el sistema, tendrá un valor negativo.
### Transformaciones cíclicas

$caption id="attachment_150675" align="alignnone" width="324"$![](/taller-matematicas/assets/images/cicle.png) Fig.5: una transformación termodinámica PV cíclica, o brevemente, un ciclo[/caption]

Son transformaciones que empiezan y acaban en el mismo estado. En la figura 5 vemos representado un ciclo en el diagrama PV recorrido en el sentido de las agujas del reloj; al recorrer la rama superior el trabajo de dilatación realizado será igual al área bajo la curva roja, en cambio al recorrer la rama inferior el sistema se contrae, luego el trabajo es negativo, y será igual al área bajo la curva azul cambiada de signo. El trabajo total del ciclo será la suma de los dos anteriores, y se ve claramente que será igual al área contenida dentro del ciclo y tendrá un valor positivo (trabajo neto realizado por el sistema).

Si recorremos el ciclo en sentido inverso a las agujas de reloj, los signos de los trabajos cambian, y el trabajo del ciclo será negativo, el ciclo recibirá un trabajo neto.
### Primer principio de la Termodinámica

El principio de conservación de la energía enuncia que ésta nunca se pierde sino que se transforma de unos tipos a otros; en termodinámica hemos visto que los tipos de energías que estudiamos son la *energía térmica* o calor Q, y el resto de energías que puedan tener un papel en las transformaciones las agrupamos todas bajo la denominación genérica "energía E", con mención especial a la energía genérica interna del sistema que estudiamos, que denominaremos *energía interna* del sistema. La energía se puede invertir en realizar un trabajo, y aquí es dónde llegamos a enunciar el primer principio de la termodinámica, que relaciona calor y trabajo:
1r principio: Si un sistema absorbe una cantidad de calor Q i una cantidad de trabajo W, y emite una cantidad de calor Q' y realiza una cantidad de trabajo W, se cumple siempre que:
*Q + Q' = W + W' [2]*

$caption id="attachment_150677" align="alignnone" width="487"$![](/taller-matematicas/assets/images/1r-principi-Termo.png) Fig. 6: balance entre calor absorbido y emitido, y trabajo absorbido y realizado[/caption]

El 1r principio no es más que un balance energético donde usamos el trabajo para explicar lo que sucede con el calor que "desaparece"; observemos los convenios de signo: el trabajo realizado por el sistema y el calor absorbido por él se consideran de signo positivo, mientras que el calor emitido por el sistema y el trabajo recibido sobre él son negativos. Pero no significa que el trabajo sea una forma de energía; parecería pues que el 1r principio violaría la conservación de la energía, veamos que esto no es así.
### Energía interna y magnitudes conservativas

Consideremos la transformación A->B de la figura 5, que es parte de un clclo, una expansión del sistema que generará un trabajo W > 0 dado por la expresión 1. Supongamos que el sistema absorbe un calor Q > 0  en esa transformación; la diferencia entre calor absorbido y trabajo realizado, Q - W, debe de "ir a algún sitio"; diremos que se utiliza para aumentar la energía interna del sistema:

$\triangle E_{A\rightarrow B}=Q-W$

Cerrando el ciclo, la transformación B->A es una compresión, luego se genera trabajo sobre el sistema, W' < 0, y quizá el sistema libere calor Q' < 0, de nuevo, la diferencia Q' - W' se empleará en variar la energía interna del sistema:

$\triangle E_{B\rightarrow A}=Q'-W'$

Si consideramos ahora todo el ciclo A->B->A, como el sistema queda en el mismo estado inicial, la energía interna también ha de ser la misma; sumando las dos igualdades anteriores:

$\begin{array}{l}\begin{array}{l}\triangle E_{AB}=Q-W\\\triangle E_{BA}=Q'-W'\end{array}\\---------\\\triangle E_{ABA}=\left(Q+Q'\right)-\left(W-W'\right)\end{array}$

Luego

$\left(Q+Q'\right)-\left(W-W'\right)=0\Leftrightarrow\boxed{Q+Q'=W-W'}$

recuperamos el 1r principio; vemos que nos faltaba para entender la conservación de la energía la energía interna del sistema: la energía térmica, el trabajo, y la energía interna se van equilibrando en cada transformación termodinámica. Enunciamos ahora unas propiedades importante:
P1) La energía interna E del sistema es una **función del estado** del sistema: a cada estado le corresponde una única energía definida.
Por ejemplo si un sistema queda totalmente definido por las magnitudes presión P y Volumen V, entonces la energía interna es función de P, V: E = f(P, V).
P2) El trabajo W no es una función de estado del sistema, para cada estado no es posible asignar un único valor de W.
En efecto, sabemos que el valor del trabajo es igual al área definida por la curva de cambio de estado PV y el eje V; en la figura 7 vemos tres trayectorias distintas entre los mismos estados A, B, y cada una representa un trabajo distinto. Este hecho también se enuncia diciendo que *el trabajo no es una magnitud conservativa*, significando que si hacemos un ciclo ABA, el trabajo total no tiene porque ser nulo, pues dependerá de las trayectorias seguidas. En cambio* la energía interna es una magnitud conservativa*, pues siempre la recuperaremos en un ciclo (variación total nula) independientemente del camino seguido.

$caption id="attachment_150679" align="alignnone" width="312"$![](/taller-matematicas/assets/images/treball-no-conservatiu.png) Fig. 7: El trabajo ralizado en una tranasformación no depende sólo de los estados inicial A y final B[/caption]

Con esto podemos reformular el 1r principio en una forma equivalente:
1r principio: El calor absorbido por un sistema se invierte íntegramente en el trabajo realizado por él más su incremento de energía interna, $Q=W+\triangle E$. [3]
### Energía interna y temperatura

Diferenciando la expresión 3, $\operatorname dQ=\operatorname dW+\operatorname dE$, y recordando la expresión 1 para el trabajo: $\operatorname dQ=P\operatorname dV+\operatorname dE$. [4]

Por otra parte, el calor absorbido y el incremento de temperatura están relacionados con el coeficiente calorífico *c*, $\triangle Q=nc\triangle T$, siendo una medida de la masa del sistema (como por ejemplo el número de moles); sucede que *c* toma valores distintos en transformaciones isóbaras que en isócoras:
a V = cte, $\triangle Q=nc_V\triangle T$,

a P = cte, $\triangle Q=nc_P\triangle T$.

Tomemos un proceso a V = cte y diferenciemos: $\operatorname dQ=nc_V\operatorname dT$. Comparando con 4:

$P\operatorname dV+\operatorname dE=nc_V\operatorname dT\Leftrightarrow\operatorname dE=nc_V\operatorname dT$

pues V es constante y dV = 0. integrando:
$\triangle E=nc_V\triangle T$ [5]

que nos da la variación de energía interna respecto a la variación de temperatura en un proceso a volumen constante. Pero la energía es una función de estado, y su variación sólo depende de los estados, no de los procesos, por ello, la expresión 5 es válida en general, y nos da la variación de la energía interna en función del cambio de temperatura para cualquier transformación.
### Transformaciones adiabáticas; aplicación a los gases perfectos.

Si no hay intercambio de calor, el 1r principio dice que $Q=0\Rightarrow W+\triangle E=0$. Hemos visto que podemos relacionar el incremento de energía interna en un sistema termodinámico con un incremento de temperatura (ecuación 5):
$\operatorname dW+nc_v\operatorname dT=0\Leftrightarrow P\operatorname dV+nc_v\operatorname dT=0$ [6]

ecuación que nos da la relación entre diferenciales de volumen y temperatura cuando Q = 0.

**Aplicación a los gases perfectos**

La ecuación de estado es PV = nRT, aislando P y sustituyendo en 6:

$\frac{nRT}V\operatorname dV+nc_v\operatorname dT=0$

dividimos todo por nCvT e integramos:

$\int\frac R{c_v}\frac{\operatorname dV}V+\int\frac{\operatorname dT}T=0\Leftrightarrow\frac R{c_v}\ln\left(V\right)+\ln\left(T\right)=\mathrm C$

donde C es una constante de integracion; operamos con los logaritmos, y además definimos la constante $\gamma=c_p/c_v$, y usamos la [relación de Mayer](https://es.wikipedia.org/wiki/Relaci%C3%B3n_de_Mayer), $c_p-c_v=R$ para obtener:

$\left.\begin{array}{r}\frac R{c_v}\ln\left(V\right)+\ln\left(T\right)=\mathrm C\\c_p-c_v=R;\;\gamma=\frac{c_p}{c_v}\end{array}\right\}\Rightarrow\frac{c_p-c_v}{c_v}\ln\left(V\right)+\ln\left(T\right)=\mathrm C\Rightarrow\ln\left(\mathrm{TV}^{\mathrm\gamma-1}\right)=\mathrm C$

Volvemos a utilizar la ecuación de estado ideal PV = nRT para eliminar T de la expresión anterior:

$\ln\left(\frac{PV}{nR}V^{\mathrm\gamma-1}\right)=\mathrm C\Leftrightarrow\ln\left(\frac1{\mathrm{nR}}\mathrm{PV}^\mathrm\gamma\right)=\mathrm C$

Como 1/nR es una constante, lo incorporamos a la constante de integración, y concluimos:

$\ln\left(\frac1{\mathrm{nR}}\mathrm{PV}^\mathrm\gamma\right)=\mathrm C\Rightarrow\ln\left(\mathrm{PV}^\mathrm\gamma\right)=\mathrm{cte}\Rightarrow\boxed{\mathrm{PV}^\mathrm\gamma=\mathrm{cte}}$

que nos da la *ecuación de los estados de las transformaciones adiabáticas de gases perfectos*;  sabiendo que $c_p-c_v=R&gt;0$, deducimos que $c_p=R+c_v&gt;c_v$ y por tanto que $\gamma&gt;1$.

La figura 8 compara gráficamente las transformaciones adiabáticas con las isotérmicas de gases perfectos, en las que PV = cte:

$caption id="attachment_150683" align="alignnone" width="467"$![](/taller-matematicas/assets/images/adiabátiques-PV.png) Fig.8: transformaciones isoterma y adiabáticas de gases perfectos en el diagrama PV[/caption]

Observamos que la isotérmica tiene una pendiente menor que todas las adiabáticas, pues $\gamma&gt;1$. Asintóticamente todas coinciden en los ejes P y V.
### Máquina térmica de Carnot para gases perfectos

Pensemos ahora en un ciclo de transformaciones reversibles como el mostrado en la figura 9, recorido en el sentido de las agujas del reloj, 1-2-3-4, y con las siguientes condiciones:

![](/taller-matematicas/assets/images/Carnot-1.png)

 	- 1-2: isotérmica, T=cte, absorbe Q > 0

 	- 2-3: adiabática, Q = 0, T variable pasa a ser T'

 	- 3-4: isotérmica, T'=cte, emite Q' < 0

 	- 4-1: adiabática, Q = 0, T'=cte

El diagrama tiene la geometría correcta, pues hemos visto que las curvas adiabáticas tienen mayor pendiente que las isotérmicas, al menos lo hemos visto para gases perfectos, y nos restringimos a este caso en lo que sigue.

En las isotérmicas la energía interna debe de ser constante según la ecuación 5, y en este caso por el 1r principio, el trabajo ha de ser igual al calor, Q = W(12) y Q'=W(34). Además, el valor del área 112'1' coincide con el valor de Q, y el del área 44'33' coincide con el valor de Q',

En cambio en las adiabáticas hay cambios de temperatura y de energía interna, y por el 1r principio W(23) = incremento E(23) y W(41) = incremento E(41). Además, los valores de las áreas 11'44' y 22'3'3 coinciden con los cambios de energía interna. Como el cambio de energía interna del ciclo completo ha de ser cero, se deduce que las áreas 11'44' y 22'3'3 han de ser iguales (en el diagrama no lo son).

Las variaciones de temperatura, en las transformaciones adiabáticas, viene dadas por (5) y son:

$\triangle T=\frac{nc_v}{\triangle E}=\frac{nc_v}{-W}\left\{\begin{array}{l}&lt;0\text{ en expansión adiabática}\\&gt;0\text{ en compresión adiabática}\end{array}\right.$

Como en la adiabática 23 la variación de temperatura es negativa, implica que T > T': *el ciclo de Carnot opera entre dos fuentes térmicas a temperaturas distintas, absorbiendo calor Q de la fuente más caliente y cediendo calor Q' a la fuente más fría, y realizando un trabajo neto W = Q - Q'.*

**Ciclo inverso de Carnot: bomba de calor**

Siendo un ciclo reversible puede invertirse en cualquier momento y hacerse en sentido contrario al del reloj; en el sentido 4321 la 32 es una compresión adiabática, que implica un aumento de temperatura, luego T > T' como en el ciclo directo; en la 21 tenemos compresión isoterma que libera calor Q, y en cambio en 43 se absorbe: *el ciclo inverso absorbe calor de la fuente fría, cede calor a la fuente caliente y consume un trabajo W, por ello decimos que bombea calor de la fuente fría a la cálida, es decir, que la refrigera*.

**Rendimiento de un ciclo**

Nos preguntamos, ¿que trabajo neto W obtenemos a cambio de inyectar un calor neto Q + Q' en el ciclo? (recordemos que Q' tendrá signo negativo). Este último calor suele provenir de la combustión (fuente térmica a alta temperatura), se genera un trabajo y se libera un calor residual al medio ambiente Q'.  Definimos el índice de rendimiento del ciclo r = W / Q, que idealmente seria 1 (todo el calor se convierte en trabajo). Vemos que r = (Q  + Q') / Q. Se puede demostrar que, para un ciclo de Carnot, se cumple
$r=\frac{T-T'}T=1-\frac{T'}T$ [6]

que sólo depende de las temperaturas de los focos térmicos, y será siempre menor que 1 excepto en el caso extremo de T' = 0 (medio exterior en el cero absoluto de temperaturas). Se puede definir un índice análogo para bombas de calor.
{% endraw %}