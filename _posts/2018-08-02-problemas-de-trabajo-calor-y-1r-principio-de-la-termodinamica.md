---
layout: post
title: "Problemas de trabajo, calor y 1r principio de la termodinámica"
date: 2018-08-02 15:32:06 +0000
categories:
  - "Fí­sica"
  - "Termodinámica"
tags:
  - "adiabático"
  - "Energía interna"
  - "gas perfecto"
  - "isotermo"
  - "reversible"
  - "trabajo"
math: true
---

### Problemas resueltos

**1** - Determinar el trabajo de expansión realizado por un mol de una sustancia al pasar del estado sólido al estado líquido bajo la presión de 1 atm, sabiendo que su volumen específico en el estado líquido supera al del estado sólido en 0,16 cm³/gr. Otros datos: masa de un mol de la sustancia: 60gr/mol.

**Solución**: el trabajo de expansión viene dado por (ver [Trabajo, calor y 1r principio de la termodinámica](http://tallermatematic.ovh/wp/index.php/2018/07/31/trabajo-calor-1r-principio-de-la-termodinamica/). ecuación [1]):
$W=\int_{V_1}^{V_2}P\operatorname dV$[1]

La fusión del sólido ocurre a presión constante, luego
$W=\int_{V_1}^{V_2}P\operatorname dV=P\int_{V_1}^{V_2}\operatorname dV=P\left(V_2-V_1\right)=P\triangle V$[a]

¿Cuál es el incremento de volumen de un mol cuando se funde? Tenemos 60gr por mol, y el incremento de volumen por gramo es 0,16 cm³/gr, luego el incremento de volumen total es 60gr/mol · 0,16 cm³/gr = 9.6 cm³/mol. Sólo queda pasar todas la unidades a sistema internacional y aplicar [a]:

1 atm = 1. 013·10⁵ N/m²; 9.6 cm³ = 9.6 · 10⁻⁶m³;

W = 1. 013·10⁵ N/m² · 9.6 · 10⁻⁶m³ = 0.972 Nm = 0.972 J (en Joules).

---

**2** - Se comprime de forma reversible e isotérmica un mol de un gas ideal a T = 18⁰C desde la presión inicial de 0.8 atm hasta la presión final de 3.5 atm. ¿Qué trabajo se ha realizado sobre el gas?

**Solución**: El trabajo de expansión viene dado por (ver [Trabajo, calor y 1r principio de la termodinámica](http://tallermatematic.ovh/wp/index.php/2018/07/31/trabajo-calor-1r-principio-de-la-termodinamica/). ecuación [1]):
$W=\int_{V_1}^{V_2}P\operatorname dV$[1]

En nuestro caso es una compresión, luego el trabajo será negativo (producido *sobre* el gas, y no producido *por* el gas). Siendo una gas ideal, se cumple la ecuación de estado PV = nRT, y como T es constante, se cumple PV = cte, o sea que $P_1V_1=P_2V_2$. Además, P=nRT/V, sustituyendo en [1]:

$W=\int_{V_1}^{V_2}\frac{nRT}V\operatorname dV=nRT\int_{V_1}^{V_2}\frac{\operatorname dV}V=nRT\left(\ln\left(V_2\right)-\ln\left(V_1\right)\right)=nRT\ln\left(\frac{V_2}{V_1}\right)$

Expresamos el volumen en función de la presión usando $P_1V_1=P_2V_2\Leftrightarrow\frac{V_2}{V_1}=\frac{P_1}{P_2}$, y el trabajo en función de las presiones queda

$W=nRT\ln\left(\frac{P_1}{P_2}\right)$

Sustituyendo los valores numéricos:

0.8 atm = 0.8 · 1. 013 · 10⁵ N/m² = 0.8104 · 10⁵ N/m² ,

3.5 atm = 3.5 · 1. 013 · 10⁵ N/m² = 3.5455 · 10⁵ N/m² ,

18⁰C = 18 + 273⁰K = 291⁰K,

$W=1\cdot8314\cdot291\cdot\ln\left(\frac{0.8104}{3.5455}\right)=-3496\;J$.

---

**3**. Un gas ideal encerrado en un émbolo a 25⁰C y presión inicial P = 2 atm (estado A) se calienta suministrándole un calor Q sin variar el volumen (émbolo fijado). A continuación, una vez absorbido el calor por el gas (estado B) se libera el émbolo permitiendo que el gas se expanda adiabáticamente, de forma que la presión final es 1,1 atm y la temperatura final la misma que la inicial, 25⁰C (estado C). Calcular la presión y la temperatura en el estado intermedio B, y el calor suministrado. Se supone que todos los cambios son reversibles. Datos adicionales: masa del gas m = 1Kg, calor específico molar a volumen constante c = 5R/2, siendo R la constante universal del los gases perfectos.

**Solución**. En la imagen 1 vemos los estados del sistema y su evolución en un diagrama PV. La línea vertical AB es a volumen constante, y el sistema absorbe un calor Q, aumentando su presión; por el punto A se ha dibujado en discontinuo la curva isoterma correspondiente a la T = 25⁰C, observemos que el estado final C, al estar a la misma temperatura, está también sobre la isoterma, debe de ser así pues al ser todo el proceso reversible, el estado C es de equilibrio, y al estar A, C  a la misma temperatura, han de estar unidos por una isoterma. La curva BC es adiabática de temperatura variable.

[caption id="attachment_150691" align="alignnone" width="285"]![](/assets/images/Exercici-3-Termo-1.png) Fig.1: las transformaciones del problema en el diagrama PV[/caption]

Resumimos lo que sabemos y lo que desconocemos:

 	- Estado A: PA = 2 atm, VA = ? , TA = 25⁰C

 	- Estado B: PB = ?, VB = VA, TB = ?

 	- Estado C: PC = 1.1 atm, VC = ?, TC = 25⁰C

 	- Transformación A->B a volumen constante

 	- Transformación B->C adiabática Q = 0

Para el estado A es immediato calcular VA, usando PV = nRT -> VA = nRTA / PA = (100·R·295) / (2·1.013·10⁵) = 295R/2026 m³. Luego también tenemos VB = VA = 295R/2026 m³.

Lo mismo sucede con el estado C: VC = nRTC / PC = (100·R·295) / (1.1·1.013·10⁵) = 2950R/11143 m³. Los estados A y C quedan totalmente determinados, y del B nos falta la presión y el volumen.

**Transformación B->C**. Es una adiabática, aplicaremos lo visto en [Trabajo, calor, 1r principio de la Termodinámica](http://tallermatematic.ovh/wp/index.php/2018/07/31/trabajo-calor-1r-principio-de-la-termodinamica/) apartado Transformaciones adiabáticas; aplicación a los gases perfectos: $\mathrm{PV}^\mathrm\gamma=\mathrm{cte}$ siendo $\gamma=c_p/c_v$ y además se cumple la [relación de Mayer](https://es.wikipedia.org/wiki/Relaci%C3%B3n_de_Mayer), $c_p-c_v=R$. Con  los datos del enunciado, encontramos el valor de la constante gamma:

$\mathrm\gamma=\frac{{\mathrm c}_\mathrm p}{{\mathrm c}_\mathrm v}=\frac{\mathrm R+{\mathrm c}_\mathrm v}{{\mathrm c}_\mathrm v}=\frac{\mathrm R+{\displaystyle\frac{5\mathrm R}2}}{\displaystyle\frac{5\mathrm R}2}=\frac75=1.4$

Por tanto, en la transformación B->C, $PV^{1.4}=cte$, y podemos escribir:

$P_BV_B^{1.4}=P_CV_C^{1.4}\Rightarrow P_B=P_C\frac{V_C^{1.4}}{V_B^{1.4}}=1.1\frac{2950\cdot2026}{295\cdot11143}=2.31\;atm$

Nos falta TB . Veamos la transformación A->B.

**Transformación A-B**. Siendo un gas ideal se cumple PV = nRT, y como el volumen es fijo, se cumple la *ley de Gay-Lussac* (que se deduce directamente de la ecuación PV=nRT considerando el volumen constante):
$\frac{P_A}{T_A}=\frac{P_B}{T_B}\Leftrightarrow T_B=T_A\frac{P_B}{P_A}=298\frac{2.31}2=344$,

Las presiones no las hemos convertido a sistema internacional pues el cociente $\frac{P_B}{P_A}$ vale lo mismo en atmósferas que en Pascales. Ahora podemos obtener el calor absorbido por el sistema, que es absorbido a volumen constante; el incremento de temperatura viene dado por:

$Q=nc_V\triangle T=100\cdot\frac528,314\cdot\left(344-298\right)=95611J\;\simeq\;96KJ.$,

o en kilocalorias, aproximadamente 23 Kcal.

---

**4**. Una máquina térmica que sigue un ciclo de Carnot trabaja entre las temperaturas de 150⁰C y 50⁰C. ¿Cuál es la cantidad de calor que absorbe si la máquina tiene una potencia de 75 KW?

**Solución**: En la teoría [Trabajo, calor, 1r principio de la Termodinámica](http://tallermatematic.ovh/wp/index.php/2018/07/31/trabajo-calor-1r-principio-de-la-termodinamica/) apartado Máquina térmica de Carnot para gases perfectos se muestra que "*el ciclo de Carnot opera entre dos fuentes térmicas a temperaturas distintas T, T', absorbiendo calor Q de la fuente más caliente y cediendo calor Q' a la fuente más fría, y realizando un trabajo neto W = Q - Q'.*"; una potencia de 75 KW equivale a desarrollar un trabajo de 75 KJ por segundo, luego Q - Q' = 75000 J. Además, sabemos que el rendimiento de los ciclos de Carnot cumplen:
$r=\frac WQ=\frac{T-T'}T$

En nuestro caso,

$r=\frac{75000}Q=\frac{\left(150+270\right)-\left(50+270\right)}{\left(150+270\right)}=\frac5{21}\Rightarrow Q=\frac{21}575000=315000J$

Hay que suministrar 315 KJ por segundo, o sea 315 KW en forma de energía térmica a la máquina para obtener 75 KW de potencia; la máquina tiene un rendimiento de 5/21, en tanto por ciento es de solo el 23.8%: de cada 100 J suministrados en forma de calor, 23.8 J se transforman en calor, y el resto, 76.2 J, se devuelven en forma de calor no aprovechable. El rendimiento de las máquinas térmicas es pues bajo, y mucho menor que el de los motores eléctricos, que rondan el 80% de eficiencia.

---

### Preguntas cortas

**1** - Un gas perfecto se dilata reversiblemente en dos fases, la primera es isoterma, la segunda adiabática, recorriendo tres estados, el inicial A, el intermedio B y el final C. Tenemos conocimiento completo de les estados A y C, pero no sabemos nada del estado intermedio B. ¿Es posible calcular el trabajo de expansión realizado por el sistema?

**Respuesta**. No es posible, y no lo es porque el trabajo realizado en una transformación de diversos estados depende de cada uno de los estados intermedios. En la figura 2 vemos en un diagrama PV dos posibles caminos ABC y AB'C entre los mismos estados A y C, recordando que el trabajo realizado coincide con el área bajo la curva, vemos claramente que las áreas delimitadas por los dos caminos son distintas, luego conocer el estado intermedio B es necesario para calcular el trabajo.

[caption id="attachment_150698" align="alignnone" width="297"]![](/assets/images/treball-no-conservatiu-2.png) Fig. 2: el trabajo realizado en una transformación de estados depende de todos los estados, no sólo del inicial y el final[/caption]

---

**2** - Un gas perfecto se dilata reversible y adiabáticamente desde el estado inicial A al final B. Conocemos las temperaturas en A y B pero  no los volúmenes. ¿Es posible calcular el trabajo de expansión realizado por el sistema?

**Respuesta**. Sí es posible, pues en un proceso adiabático *Q = 0*, y por el 1r principio *Q = W + E -> 0 = W + E -> W = -E*, el trabajo realizado será igual al cambio de energía interna cambiado de signo (pues en la expansión se pierde energía interna), además sabemos que en los gases perfectos el cambio de energía interna sólo depende del cambio en la temperatura $\triangle E=nc_V\triangle T$.

---

**3** - Es conocido el hecho de que, al inflar a mano un neumático con una bomba de aire, ésta se calienta, el efecto es muy notable con los neumáticos de bicicleta de carretera, que han de hincharse a presiones elevadas (de unos 7kg/cm² para un ciclista de 70kg), y no puede explicarse por simple rozamiento, ¿a que es debido? Considerar que el aire se comporta como un gas perfecto.

**Respuesta**. La bomba comprime el aire y lo inyecta en la cámara del neumático; para hacerlo realizamos trabajo sobre el aire (la fuerza que aplicamos a la bomba), lo que *no* suministramos es calor: nosotros no calentamos el aire poniéndolo en contacto con una fuente térmica cálida, nos limitamos a realizar un trabajo. Por el 1r principio, *Q = W + E*, el incremento de energía interna es igual al trabajo suministrado (signo negativo, recordemos el convenio de signos, el trabajo realizado por el sistema es positivo), *-W = E*, pero en los gases perfectos el cambio de energía interna sólo depende del cambio en la temperatura $\triangle E=nc_V\triangle T$, así pues, el gas se ha de calentar si aumenta su energía interna.

---

**4**. Un ciclo de un gas ideal tiene forma rectangular en el diagrama Presión-Volumen. ¿Qué aspecto tendrá en un diagrama Presión-Temperatura?

**Respuesta**. En la figura 2 vemos el diagrama PV, indicando el carácter de cada transformación entre los cuatro estados ABCD. Siendo un gas ideal, tenemos la ecuación de estado PV = nRT. Veamos que no dice para cada transformación respecto a las variables P, T:

[caption id="attachment_150699" align="alignnone" width="366"]![](/assets/images/Rectangle-PV.png) Fig.2: diagrama PV en forma de rectángulo[/caption]

**A->B**: dilatación a presión constante, se produce trabajo, $V=\left(\frac{nR}P\right)T$, la temperatura depende linealmente del volumen, a más volumen, más temperatura; esto sólo es posible si hay una aportación de calor Q al gas, que se expandirá y calentará a presión constante. P = cte implica que será una linea horizontal en el plano PT.

**B->C**: Descompresión a volumen constante, $P=\left(\frac{nR}V\right)T$, dependencia lineal, la temperatura disminuye con la presión, manteniendo el volumen constante, implica que no se produce trabajo, y por el 1r principio la disminución de energía interna (debido al descenso de temperatura) es igual al calor emitido: se debe quitar calor al gas para disminuir la presión a volumen constante. En el diagrama PT será una línea con pendiente positiva $\frac{nR}V$

**C->D**: reducción de volumen a presión constante, se recibe trabajo (trabajo negativo), $V=\left(\frac{nR}P\right)T$, la temperatura depende linealmente del volumen, desciende con éste, y se desprende calor (1r principio, Q = W + E, ambos negativos). En el diagrama PT será una línea horizontal.

**D->A**: compresión a volumen constante, $P=\left(\frac{nR}V\right)T$, dependencia lineal, la temperatura aumenta con la presión, manteniendo el volumen constante, implica que no se produce trabajo, luego Q = E, el gas absorbe calor. En el diagrama PT será una línea con la misma pendiente que B->C.

Con todo ello nos resulta un ciclo con forma de paralelogramo:

[caption id="attachment_150701" align="alignnone" width="259"]![](/assets/images/diagrama-PV-en-PT.png) Fig. 3: diagrama PT equivalente[/caption]

---