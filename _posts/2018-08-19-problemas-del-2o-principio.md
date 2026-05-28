---
layout: post
title: "Problemas del 2º principio"
date: 2018-08-19 08:17:35 +0000
categories:
  - "Fí­sica"
  - "Termodinámica"
math: true
---
{% raw %}

**1.** En un ciclo de Carnot ¿en qué isoterma se producirá mayor variación de entropía del sistema?**
**

Respuesta: En un clclo cualquiera la variación de entropía del sistema es nula; un ciclo de Carnot incluye dos transformaciones adiabáticas y dos isotermas, el sistema no sufre variación de entropía en las adiabáticas pues Q = 0 y el ciclo es reversible (luego $\begin{array}{l}\triangle S=\int\frac{dQ}T\\\end{array}$) así que toda la variación de entropía ocurre en las isotermas, pero siendo nula la global, por fuerza las dos isotermas han de producir la misma variación de entropía del sistema, y con signo contrario, para que una anule a la otra.

![](/taller-matematicas/assets/images/separador2.png)

**2.** Dos de las siguientes afirmaciones son falsas, y una es incompleta; identificarlas y explicarlas. A) La entropía es constante en toda transformación isotérmica. B) La entropía es constante en toda transformación adiabática. C) La entropía es constante en toda transformación a volumen V constante.

Respuesta: A) es falsa, pues en una transformación isotérmica la temperatura se mantiene constante, pero puede haber transferencia de calor y trabajo, como sucede en los ciclos de Carnot, en los cuales precisamente en las transformaciones isotérmicas es en donde se producen las variaciones de entropía (ver problema 1). B) es parcialmente cierta, pues sólo se cumple en las transformaciones adiabáticas que además son reversibles, pero no en las irreversibles. C) es falsa, pues V = cte implica que no se produce un trabajo, W = 0, pero por el primer principio Q = ΔE, se puede producir una transferencia de calor y puede variar la entropía.

![](/taller-matematicas/assets/images/separador2.png)

**3**. Un sistema recorre un ciclo una de cuyas transformaciones es irreversible. ¿De qué signo será la variación de entropía del sistema?

Respuesta: Siendo un ciclo, la variación de entropía S del sistema ha de ser nula, pues S es una función del estado del sistema, y en un ciclo siempre se retorna al estado inicial.

![](/taller-matematicas/assets/images/separador2.png)

**4**. Un gramo de agua helada a 0ºC se calienta poniéndola en contacto con una fuente térmica a 200ºC y 1º) se funde, 2º) se calienta hasta 100ºC y 3º) se evapora, siempre a presión constante de 1 atm. De los tres procesos, ¿cuál aumenta más la entropía? Datos: calor de fusión = 80 cal/gr,  calor de vaporización = 540 cal/gr, calor específico: 1 cal/gr·K

Respuesta: la primera transformación se realiza a T = cte, y P = cte, y podemos considerarla reversible, pues en los cambios de fase el sistema siempre está en equilibrio. Entonces, usando los datos y convirtiendo a sistema mks:

A) $\triangle S=\int\frac{\operatorname dQ}T=\frac1T\int\operatorname dQ=\frac1T\triangle Q=\frac1{273}1\cdot80\cdot4.1868=1.23\;J/K$

La transformación B en cambio es irreversible pues la diferencia de temperaturas entre el agua y la fuente teŕmica aleja a la primera del equilibrio. Imaginemos una transformación reversible que lleve del estado A (T= 0ºC, P = 1 atm) hasta B (T= 100ºC, P = 1 atm), supondremos que el volumen se mantiene constante (una aproximación bastante buena) y que el agua se va calentando poniéndose en contacto con una fuente sólo ligeramente más caliente; si el agua está a T, la fuente estará a T + dT. Entonces,

B) $\triangle S=\int\frac{\operatorname dQ}T=\int_{273}^{373}\frac{mc_p\operatorname dT}T=1\cdot1\cdot4.1868\cdot\ln\left(\frac{373}{273}\right)=1.31\;J/K$

La transformación C es reversible pues vuelve a ser un cambio de fase, luego:

$\triangle S=\int\frac{\operatorname dQ}T=\frac1T\int\operatorname dQ=\frac1T\triangle Q=\frac1{373}1\cdot540\cdot4.1868=6.06\;J/K$

Claramente la evaporación es la que aumenta más la entropía.

![](/taller-matematicas/assets/images/separador2.png)

**5.** Sean 3·10⁻² moles de un gas ideal en el estado A definido por P=1 atm, V=R m³, (R: constante de los gases perfectos), T = 300⁰K que evoluciona irreversiblemente hasta el estado B definido por P=2 atm, V=4R/3 m³, T = 400⁰K según la transformación 1 que puede verse en el diagrama PV (figura 1). Supondremos el valor 1 para el coeficiente térmico a volumen constante, $c_v=1$. Calcular la variación de entropía.

$caption id="attachment_150717" align="alignnone" width="438"$![](/taller-matematicas/assets/images/entropia-irreversible.png) Fig.1: diagrama PV de un sistema que evoluciona irreversiblemente entre los estados A, B[/caption]

Solución: Para calcular la variación de entropía, buscamos una transformación reversible, o sea, que respete en cada instante los estados de equilibrio dados por la ecuación de estado PV = nRT. Imaginemos el camino 2 de A->C que mantiene el volumen constante, luego P/T = nR/V = cte, llevando el sistema hasta la temperatura del estado B; todos los estados en equilibrio a temperatura $T_B=400$ están sobre la isoterma en rojo, la isoterma en azul corresponde a T = 300. A continuación, imaginamos que el sistema evoluciona reversiblemente desde C hasta A por la isoterma T =400. La variación de entropía entre A y B será la suma de las entropías A->C más la de C->B. Vamos por ello:

$S_{AC}=\int_{AC_{REV}}\frac{\operatorname dQ}T=nc_v\int_{300}^{400}\frac{\operatorname dT}T=3\cdot10^{-2}\ln\left(\frac43\right)$,

para la entropía del paso A->C; sobre la isotérmica, PV = cte, por el 1r principio, Q = W pues el gas perfecto no cambia su energía interna si no lo hace la temperatura; el trabajo W realizado es:

$W_{CA}=\int_{CA_{REV}}P\operatorname dV=\int_{CA_{REV}}\frac{nRT}V\operatorname dV=nR\ln\left(\frac{V_2}{V_1}\right)=12R\ln\left(\frac43\right)$,

la variación de entropía a T = cte es:

$S_{CA}=\frac{Q_{CA}}T=\frac{12R\ln\left({\displaystyle\frac43}\right)}{400}=3\cdot10^{-2}R\ln\left(\frac43\right)$

y la variación de entropía total:

$S_{AB}=S_{AC}+S_{CA}=3\cdot10^{-2}R\ln\left(\frac43\right)+3\cdot10^{-2}\ln\left(\frac43\right)=3\cdot10^{-2}\left(R+1\right)\ln\left(\frac43\right)$.

![](/taller-matematicas/assets/images/separador2.png)

**6**. Un gramo de agua calentado a 100ºC al convertirse en vapor a la presión de 1atm ocupará un volumen de 1671 cm³, absorbiendo 2257J de energía calorífica. Si evaporamos 1Kg de agua, ¿cuál será su aumento de energía interna y de entropía?

**Solución**: Los cambios de fase (evaporación, solidificación, sublimación ...) son transformaciones de estado especiales pues siendo reales son reversibles (el sistema permanece en equilibrio durante el cambio de fase). En la figura 2 vemos el diagrama PV de la evaporación del agua, a presión y temperatura constante, el volumen específico aumenta linealmente.

$caption id="attachment_150748" align="alignleft" width="528"$![](/taller-matematicas/assets/images/PV-canvi-de-fase.png) Fig.2: diagrama PV de un cambio de fase líquido a gas, caso del agua ( por cm³)[/caption]

Por el 1r principio: Q = W + ΔE; el trabajo realizado por el vapor correspondiente a 1gr de agua al expandirse bajo una presión constante de  P = 1atm (101.325 Pascales) es W = PΔV = 101.325Pa · (1671 - 1)·10⁻⁶m³ = 169.21 J. El calor absorbido sabemos que vale 2257J, luego ΔE = Q - W = 2257 - 169.21 = 2087.79 J.

El incremento de entropía, al ser un proceso reversible y suceder a temperatura constante, es simplemente ΔS = Q/T = 2257 J / (100+273)K = 6.05 J·K⁻¹ . Siendo la energía interna y la entropía [propiedades extensivas](https://es.wikipedia.org/wiki/Propiedades_intensivas_y_extensivas) (o sea que son propiedades conservativas), para un Kg de agua simplemente multiplicamos por 1000 los resultados anteriores:

 	- ΔE total = 1000 · 2087.79 = 2,088 · 10⁶ J

 	- ΔS total = 1000 · 6.05 = 6050 J·K⁻¹.

![](/taller-matematicas/assets/images/separador2.png)

**7**. Ponemos en contacto 2kg de agua a T=20ºC con una fuente térmica a 100ºC, dejando que al agua se caliente hasta los 100ºC. Calcular las variaciones de entropía del agua, de la fuente y del Universo.

**Solución**: cuando hay una transferencia de calor debido a una diferencia de temperaturas el proceso es irreversible pues el sistema (el agua) deja de estar en estado de equilibrio mientras se calienta, para que sea reversible ha de calentarse lentamente, cuasiestáticamente, esto es, con una fuente a T = 20C + dT (una diferencia infinitesimal de temperatura), seguida de otra fuente a T = 20C + 2·dT, ... etc.  Como la entropía S es función de estado, imaginamos un proceso así reversible entre los estados inicial y final para calcular la variación de S, y el resultado valdrá para todo proceso entre esos estados.

Sea pues una fuente a T = 20C + dT; como la diferencia de T es infinitesimal, suponemos el proceso isotérmico (T=cte). tendremos una variación dS = dQ/T = cm·dT / T donde c es el coeficiente de absorción de calor del agua, c = 1 cal/gr, m es la masa de agua. Integrando (o sea sumando todos los pasos dT desde 20C hasta 100C):

$\triangle S_{agua}=\int_{293}^{373}cm\frac{dT}T4180\cdot1\cdot\ln\left(\frac{373}{293}\right)=1009\;JK^{-1}$.

La fuente térmica permanece a T=cte pues se supone que tiene una capacidad calorífica muy grande, entregando una cantidad de calor total Q (por el convenio de signos, será negativa). Si suponemos que la fuente, por tener una capacidad calorífica muy grande, se mantiene en un estado casi estacionario, su proceso se puede considerar reversible, y entonces:

$\triangle S_{fuente}=\frac Q{T_{fuente}}=\frac{-mc\triangle T_{agua}}{T_{fuente}}=\frac{-1\cdot4187\cdot80}{373}=-898\;JK^{-1}$, [1]

que es negativo pues el calor es cedido. El incremento de entropía de todo el conjunto será la suma: 1009 - 898 = 111 JK⁻¹, que es positivo de acuerdo al 2º principio de la termodinámica.

Si en cambio suponemos que la fuente también está saliendo del equilibrio (capacidad calorífica grande pero no infinita) el proceso será irreversible, y también deberemos aproximarlo por uno de reversible: supongamos que la fuente cede un dQ estando a temperatura T = cte, y siendo dQ el dado por [1]; entonces:

$\triangle S=\int\frac{\operatorname dQ}T=\frac{-mc}T\int_{293}^{373}\operatorname dT=-\frac{1\cdot4187}{373}\left(373-293\right)=898\;J/K$,

resultado que coincide con el anterior cálculo, donde considerábamos el proceso de la fuente como reversible, era pues una aproximación muy buena.![](/taller-matematicas/assets/images/separador2.png)

**8**. Demostrar que en una transferencia de calor irreversible entre un sistema y una fuente de calor la entropía del universo siempre aumenta.

Solución: Supongamos que el sistema pasa de la temperatura T a la T', siendo T'> T, y que la fuente es isotérmica. Imaginando un calentamiento reversible del sistema, la variación de entropía es, suponiendo que el coeficiente calorífico c no varía con la temperatura:

$\triangle S_s=\int\frac{\operatorname dQ}T=\int_T^{T'}\frac{mc\operatorname dT}T=mc\ln\left(\frac{T'}T\right)$

La fuente térmica se mantiene a una temperatura T'' > T', y cede de forma reversible un salor Q  (pues permanece en equilibrio al tener una capacidad calorífica virtualmente infinita), luego:

$\triangle S_f=\int\frac{-\operatorname dQ}T=\frac1{T''}\int_{}^{}-\operatorname dQ=-\frac{mc\left(T'-T\right)}{T''}$

La variación total de S será la suma:

$\triangle S_s+\triangle S_f=mc\ln\left(\frac{T'}T\right)-\frac{mc\left(T'-T\right)}{T''}=mc\left$\ln\left(\frac{T'}T\right)-\frac{T'-T}{T''}\right$$ [1]

Veamos que esta expresión será siempre mayor que cero; sabiendo que T < T' > T'' se sigue que

$\frac{T'-T}{T''}&lt;\frac{T'-T}{T'}=1-\frac T{T'}$ [2]

Comparemos ahora $1-\frac T{T'}$ con $\ln\left(\frac{T'}T\right)$: llamemos $x=\frac{T'}T; f(x)=\ln\left(x\right); g(x) = 1 - 1/x$; derivando las funciones f, g vemos que sus pendientes son f'(x) = 1/x, g'(x) = 1/x², ambas funciones son crecientes, pero la segunda  crece a menor tasa pues 1/x² < 1/x. Los valores mínimos de f, g se dan para x = 1 (que se corresponde con T = T') en donde coinciden, f(1) = g(1) = 0. Así pues, f(x) es siempre mayor que g(x) y por tanto [1] será siempre positiva: la entropía del universo siempre aumenta. En la figura se representan las funciones f(x) (azul) y g(x) (rojo), la diferencia en vertical entre las dos líneas es la variación de entropía del universo en función de x = T' / T. En el caso de T'' > T' la diferencia será mayor.

$caption id="attachment_150756" align="alignnone" width="497"$![](/taller-matematicas/assets/images/compara_entropia.png) Comparación de la funciones de variación de entropía del sistema y de la fuente térmica[/caption]
{% endraw %}