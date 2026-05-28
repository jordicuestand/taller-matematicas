---
layout: post
title: "Campo eléctrico"
date: 2018-11-17 18:23:26 +0000
categories:
  - "Electricidad y Magnetismo"
  - "Fí­sica"
tags:
  - "ángulo sólido"
  - "campo central"
  - "campo newtoniano"
  - "dipolo eléctrico"
  - "flujo campo"
  - "ley de Coulomb"
  - "Teorema de Gauss"
math: true
---
{% raw %}

### Vector campo eléctrico

En [electrostática](http://tallermatematic.ovh/wp/index.php/2018/10/07/electrostatica/) se estudia la fuerza que se ejercen mutuamente dos cargas eléctricas puntuales Q, Q' entre ellas; si fijamos sólo en una de las cargas, digamos la Q, nos damos cuenta de que si colocamos cualquier carga Q' en cualquier posición del espacio que rodea a Q, se ejercerá una fuerza sobre Q', es como si el espacio que rodea a Q tuviera una nueva propiedad, la de ejercer una fuerza sobre cualquier carga Q' en cualquier posición que la situemos.

Situemos una pequeña carga de prueba q de valor conocido en cualquier posición del espacio dada por el vector de posición **v**; si vemos que se ejerce una fuerza **F** (un vector) sobre la carga por el simple hecho de estar situada en ese punto, inferimos que el espacio está afectado por alguna otra carga Q desconocida que crea ese efecto, y entonces se cumplirá la ley de Coulomb,

**F** = **r**·k·qQ/r³ [1]

donde **r** es el vector de posición de q relativo a Q. La figura 1 muestra las cargas q, Q, sus vectores de posición **v**, **w**, el vector de posición relativo de q a Q, **r = v - w**, y la fuerza resultante **F**, en la dirección de **r**, que se supone repulsiva (las cargas son del mismo signo y se repelen entre sí).

![](/taller-matematicas/assets/images/camp_electr.png) Fig.1: fuerza electrostática entre dos cargas
Asumiendo el punto de vista de que el espacio alrededor de Q está afectado por esa carga, pues se ejerce una fuerza a distancia sobre cualquier carga q en cualquier posición **v**, podemos definir un vector **E** tal que la fuerza ejercida sobre cualquier carga q sea simplemente **F** = q**E** a partir de la expresión [1]:

**E** = k(**r/**r³**)**·Q [2]

Este vector se denomina **vector campo eléctrico**, y no depende de la carga de prueba q, sólo de la carga causante Q. Si tomamos dos cargas de prueba q, q', y medimos los vectores fuerza **F**, **F**', buscando la intersección de las rectas soporte de las fuerzas encontraremos el origen del campo: la posición de la la carga Q que lo genera (figura 2). Además, la magnitud de la fuerza **F**, conocida la carga q, nos determina también la carga Q a través de la ecuación [1], y por tanto nos determina el campo **E**.

![](/taller-matematicas/assets/images/camp_electr2.png) Fig.2: dos cargas de prueba q, q' determinan el origen del campo eléctrico, la carga Q, y el vector campo E
La propiedad de que todas las rectas soportes de las fuerzas electrostáticas se corten en un punto se puede expresar diciendo que **el campo eléctrico es un campo central** pues *todas las fuerzas parten de un punto central del espacio*.

En Física se utiliza el [concepto campo](https://es.wikipedia.org/wiki/Campo_(f%C3%ADsica)) para describir cómo se "reparte" una magnitud física medible por el espacio; así, podemos hablar de campos eléctricos, campos magnéticos, e incluso de campos de velocidades en un fluido. Si la magnitud es escalar, el campo lo será, si es [vectorial](http://tallermatematic.ovh/wp/index.php/2016/08/11/vectores/), el campo es vectorial, y si la magnitud es un [tensor](http://tallermatematic.ovh/wp/index.php/2017/01/31/tensores-en-fisica/), el campo será tensorial. La matemática específica para describir campos se ha estudiado en profundidad, dando lugar a la rama de la Física Matemática conocida como [Teoría de Campos](https://es.wikipedia.org/wiki/Teor%C3%ADa_de_campos).

### Campo eléctrico producido por varias cargas puntuales

$caption id="attachment_150804" align="alignleft" width="135"$![](/taller-matematicas/assets/images/camp_electr3.png) Fig.3: las líneas del campo eléctrico de una única carga puntual son rectas que se cortan en la carga
En el caso de una única carga puntual hemos visto que todas las las rectas soportes de las fuerzas, rectas que llamaremos **líneas de fuerza del campo** o simplemente líneas del campo  parten de un punto central donde se sitúa la única carga (fig. 3).

¿Qué pasa con las líneas si el campo es generado por dos cargas? Dado que la fuerza electrostática es acumulativa (se suman las contribuciones de todas las cargas) el campo eléctrico **E** también lo será, y en cada punto del espacio se sumaran los vectores de campo correspondientes a cada carga. Además, la fuerza **F** y el campo **E** decrecen con el cuadrado de la distancia, por ello, las líneas del campo se curvan; por cada punto del espacio pasa una línea de campo, de tal modo que el campo eléctrico en ese punto es tangente a la línea. En la figura 4 se representan dos cargas positivas iguales, y una pequeña carga de prueba en la que se suman los dos vectores E, E' generados por las fuentes del campo. Los vectores resultantes no apuntan a ningún centro, el campo resultante deja de ser central, y las líneas de campo (en color negro en la figura) se curvan.

$caption id="attachment_150806" align="alignnone" width="387"$![](/taller-matematicas/assets/images/camp_electr4b.png) Fig. 4: campo y lineas de campo generadas por dos cargas puntuales iguales

Hay que tener en cuenta que toda carga generará su propio campo eléctrico que se superpondrá a los ya existentes; por ello en lo expuesto hasta ahora hablamos de colocar "cargas de prueba" que se suponen mucho menores que las cargas generadoras del campo, de forma que se puede despreciar su contribución. Además, las cargas fuente, incluso siendo de mucha mayor magnitud que las de prueba, se supone que son de dimensiones puntuales para evitar complicaciones matemáticas.
### Campo del dipolo eléctrico

Un caso particular importante es el del denominado **dipolo eléctrico**, que son dos cargas de igual magnitud q y de signo contrario separadas por una distancia d pequeña (fig. 5).

![](https://upload.wikimedia.org/wikipedia/commons/d/df/VFPt_dipole_electric.svg) Fig. 5: líneas de campo producidas por un dipolo eléctrico, fuente: By Geek3 [GFDL (http://www.gnu.org/copyleft/fdl.html) or CC BY-SA 3.0 (https://creativecommons.org/licenses/by-sa/3.0)], from Wikimedia CommonsSe define el **momento eléctrico del dipolo**, **p**, por el vector
**p** = q**d**, [3]

siendo **d** el vector que parte de la carga negativa y acaba en la carga positiva. La distancia d se supone que es mucho menor que las distancias a las cuales colocaremos las cargas de prueba donde mediremos el campo **E**, ello permite simplificar su expresión matemática, que se obtiene de sumar las contribuciones de cada carga al campo total, resultando ser:
$\boldsymbol E=qk\left(3\frac{d\cos\left(\theta\right)}{r^4}\boldsymbol r-\frac{\boldsymbol d}{r^3}\right)$ [4]

donde r es el vector que parte del punto central del dipolo (entre sus dos cargas); alternativamente, usando [3]:
$\boldsymbol E=k\left(3p\frac{d\cos\left(\theta\right)}{r^4}\boldsymbol r-\frac{\boldsymbol p}{r^3}\right)$ [5]

---

Ejemplo 1: Situamos una carga de +10⁻³C en el origen de coordenadas, y otra carga de -10⁻³C en el punto (1, 0, 0). Calcular el campo eléctrico en el punto P(0.5, 1, 1). Si colocamos en ese punto una pequeña carga de +10⁻⁶C, ¿qué fuerza ejercerá el campo sobre ella?
El campo E' debido a la primera carga será, aplicando [2]:

$\begin{array}{l}E'=k\cdot\lbrack{(0.5,1,1)-(0,0,0)}/\sqrt{(0.5²+1²+1²)\rbrack}^3\cdot(10⁻³)=\\\;(0.5,\;1,\;1)\cdot\frac{10⁻³k}{\left(3/2\right)^3}\end{array}$

Para la segunda carga:

$\begin{array}{l}E''=k\cdot\lbrack{(0.5,1,1)-(1,0,0)}/\sqrt{(0.5²+1²+1²)\rbrack}^3\cdot(-10⁻³)=\\-\;(-0.5,\;1,\;1)\cdot\frac{10⁻³k}{\left(3/2\right)^3}\end{array}$

El campo total será la suma de los anteriores:

$E=10^{-3}k\left(\frac23\right)^3\left(1,0,0\right)$.

La fuerza ejercida sobre la carga de prueba q viene dada por  **F** = q**E:**

$\boldsymbol F=q\boldsymbol E=10^{-6}\cdot10^{-3}\cdot k\left(\frac23\right)^3\left(1,0,0\right)=9\cdot\cancel{10^9}\cdot\bcancel{10^{-9}}\frac8{27}\left(1,0,0\right)=\left(1,0,0\right)$

una fuerza de 1 Newton en la dirección del eje X.

---

### Campo eléctrico creado por una distribución de cargas

Cuando en vez de cargas puntuales tenemos cuerpos materiales cargados los modelamos como si contuvieran cargas puntuales distribuidas por el cuerpo, de forma que el campo eléctrico producido por el cuerpo se obtiene sumando las contribuciones de las cargas puntuales; dependiendo de la forma matemática que demos a la distribución, la suma puede ser más o menos directa, sencilla, o complicada. En el caso límite, que es de hecho el habitual, en el que consideremos que hay una infinidad de cargas puntuales será necesario usar el cálculo diferencial y el integral.

#### Campo eléctrico creado por una distribución de cargas plana y homogénea

El caso más sencillo de distribución de infinidad de cargas puntuales es el de una barra delgada de longitud 2L que tiene cargas sólo en una cara y además están distribuidas de forma uniforme; llamemos ρ a la densidad de carga eléctrica por unidad de longitud, que evidentemente será ρ = Q/2L siendo Q la carga total de la barra. y limitémonos a calcular al campo eléctrico en un punto P situado sobre la bisectriz de la barra, a una altura h:

$caption id="attachment_150810" align="alignnone" width="452"$![](/taller-matematicas/assets/images/camp_electr5.png) Fig. 6: geometría para el cálculo del campo E producido por una línea homogénea de carga en un punto situado sobre la bisectriz de la línea
Tomando un elemento diferencial de longitud dx y situado a una distancia x del centro de la barra, por la geometría del problema vemos que la distancia r² será igual a x² + h², y la carga diferencial de ese elemento será dQ =  ρ·dx, por ello el campo diferencial creado por ese elemento en el punto P (punto azul en la figura) tendrá un módulo

$\operatorname dE_1=k\frac{dQ}{r^2}=k\frac{\rho\cdot dx}{x^2+h^2}$

Dada la situación simétrica el punto P con respecto a la barra, existirá otro elemento dx situado en -x que producirá un campo diferencial $dE_2$ tal que al sumar los vectores $dE_1$ con $dE_2$ se anularan las componentes horizontales y la resultante será vertical, dE con un módulo:

$\operatorname dE=\operatorname dE_1\sin\left(\theta\right)+\operatorname dE_2\sin\left(\theta\right)=2\cdot k\frac{\rho\cdot dx}{x^2+h^2}\cdot\sin\left(\theta\right)$

Esto sucederá a lo largo de toda la barra, por ello concluimos que el campo resultante ha de ser vertical. Tenemos ahora que sumar todas las contribuciones diferenciales a lo largo de la barra:

$E=\int_0^L\operatorname dE=2k\int_0^L\frac{\rho\cdot dx}{x^2+h^2}\cdot\sin\left(\theta\right)$

Notemos que los límites de integración son [0, L] y no [-L, L] pues para cada elemento dx a la derecha de la barra (en x) ya hemos sumado la contribución del elemento simétrico a la izquierda (en -x). Teniendo en cuenta que $\sin\left(\theta\right)=\frac hr=\frac h{\sqrt{x^2+h^2}}$ llegamos a la integral

$E=2k\int_0^L\frac{\rho\cdot dx}{x^2+h^2}\cdot\frac h{\sqrt{x^2+h^2}}=2kh\rho\int_0^L\frac{dx}{\left(x^2+h^2\right)^{3/2}}$

Sin entrar en detalles del cálculo de la integral (podemos calcularla por ejemplo usando WolframAlpha), nos quedará:

$E=2kh\rho\frac L{h^2\sqrt{h^2+L^2}}=\frac{2k\rho L}{h\sqrt{h^2+L^2}}$

En el caso de que la barra sea muy larga comparado con la distancia h, o sea L >> h, podemos simplificar el valor del campo:

$\lim_{L\rightarrow\infty}E=\frac{2k\rho}h\lim_{L\rightarrow\infty}\frac L{\sqrt{h^2+L^2}}=\frac{2k\rho}h$ [6]

El valor del campo variará según 1/h.

---

### Flujo del campo vectorial. Ańgulo sólido

En el apartado anterior hemos visto que incluso en un caso simple (línea unidimensional de carga, homogénea, campo en un punto de la bisectriz...) cuando calculamos campos debidos a distribuciones continuas de cargas en seguida aparecen integrales complicadas, o muy complicadas. En este apartado y el siguiente vemos un punto de vista de la cuestión basado en la geometria que a menudo simplifica mucho los cálculos,

Consideremos un **campo vectorial central**, que es aquel que hace corresponder a cada punto P del espacio un vector **V** que sigue la dirección OP, siendo O el centro del campo, un punto fijo (figura 7).

$caption id="attachment_150816" align="alignnone" width="219"$![](/taller-matematicas/assets/images/Camp-central.png) Fig.7: Campo central, la masa agente situada en O
El caso especial de la forma **V** = **r**·c/r² donde r es el módulo de OP (la distancia al centro del campo), **r** el vector unitario que indica la dirección de OP, y c es una constante que denominamos *masa agente del campo*; se denomina **campo newtoniano**. Son campos newtonianos el campo electrico, el campo magnético y el campo gravitatorio. Vamos a definir el [flujo del campo vectorial a través de una superfície](https://es.wikipedia.org/wiki/Flujo_de_un_campo_vectorial) infinitesimal dS, que denominamos $d\phi$, como el producto escalar **V**·d**S**, donde d**S** es el vector perpendicular a la superfície; siendo dS infinitesimal (muy pequeña), consideraremos que su curvatura es despreciable, y por tanto es plana (figura 8):

$caption id="attachment_150817" align="alignnone" width="219"$![](/taller-matematicas/assets/images/flux_vector.png) Fig. 8: elemento diferencial de superficie, vector dS, y campo vectorial V que suponemos pasa por el centro de la superficie
$\operatorname d\phi=V\cdot dS=V\cdot dS\cdot\cos\left(\theta\right)$ [7]

Definamos a continuación el [ángulo sólido](https://es.wikipedia.org/wiki/%C3%81ngulo_s%C3%B3lido) de la superficie dS con respecto al origen del campo central O. Unamos los extremos de la superficie dS con el punto O usando líneas OP, y definamos una esfera C de radio 1 con centro en O; las lineas OP cortaran a la esfera definiendo sobre ella una pequeña superficie dΩ a la que llamamos ángulo sólido de dS sobre C (figura 9).

$caption id="attachment_150818" align="alignnone" width="410"$![](/taller-matematicas/assets/images/angle_sòlid.png) Fig. 9: ángulo sólido subtendido sobre la esfera C por el elemento de superficie dS

Veamos ahora una propiedad geometrica de los campos newtonianos: el flujo del campo a través de dS es:

$\operatorname d\phi=V\cdot dS=V\cdot dS\cdot\cos\left(\theta\right)=\frac c{r^2}dS\cdot\cos\left(\theta\right)=\frac c{r^2}dS'$ [8]
donde hemos igualado $dS\cdot\cos\left(\theta\right)=dS'$, que es la proyección de la superficie dS sobre la perpendicular al vector de campo V. Las superficies dS' y dΩ (Fig. 10) son paralelas, y están unidas por las mismas rectas al punto central O, se cumple entonces que la razón de sus áreas es igual a la razón de sus distancias al centro O al cuadrado:

$caption id="attachment_150819" align="alignnone" width="367"$![](/taller-matematicas/assets/images/angle_sòlid2.png) Fig. 10: dS' y dΩ son paralelas, y están unidas por las mismas rectas al punto central O
$\frac{\operatorname d\phi}{dS'}=\frac1{r^2}\Leftrightarrow dS'=r^2\operatorname d\phi$

Si no ve el por qué el lector, piense que el área de la esfera es 4*π*r², el área de la esfera unitaria es 4*π*, y el área de una esfera que pase por dS' es 4*π*r², luego la razón de áreas es 4*π*r² : 4*π* = r². Usando esta proporción en la ecuación [8] obtenemos:

$\operatorname d\phi=\frac c{r^2}r^2\cdot d\Omega=c\cdot d\Omega$ [9]

que nos dice que *el flujo del vector campo newtoniano a través de una superficie diferencial cualquiera no depende de la distancia r, y es directamente igual al producto de la masa agente del campo por el ángulo sólido subtendido por la superficie sobre la esfera unidad centrada en el origen del campo*.

### Flujo del campo a traves de superficies cerradas

El producto escalar definido en [7] puede ser positivo o negativo dependiendo de la orientación relativa de los vectores campo **V** y d**S;** consideremos una superficie cerrada S, pdemos calcular el flujo total del campo a través de S integrando para cada elemento dS:

$\phi=\int_S\operatorname d\phi=\int_SV\cdot dS$  [10]

Si el flujo total es positivo, diremos que es un *flujo entrante en S*, y si es negativo, será un *flujo saliente de S*. Si el centro del campo O está en el exterior de S, las lineas OP desde el centro que pasen por S cortaran a S en un número par de puntos; en cambio si O está en el interior de S, las lineas cortaran a S en un número impar de puntos (figura 11).

$caption id="attachment_150820" align="alignnone" width="570"$![](/taller-matematicas/assets/images/flux_vector2.png) Fig.11: flujos provenientes del centro O a través de superficies cerradas
Por tanto en el caso exterior cada linea creará una sucesión de flujos entrante-saliente-entrante-saliente-etc en número par, o sea, de flujos positivos y negativos alternados; hemos visto que el flujo no depende de la distancia al centro (ecuación [9]) sino sólo del ángulo sólido subtendido, que será el mismo para cada elemento de superficie sobre las lineas que parten de O. Por ello, para un punto O exterior, los flujos entrantes y salientes tienen el mismo valor y se anulan entre sí, resultando un flujo total nulo:

En un campo newtoniano, el flujo total a través de una superficie cerrada que no contiene al centro del campo es nulo.

En cambio si la superficie contiene al centro del campo tendremos un número impar de flujos entrantes-salientes, y su suma no se anulará; de hecho su valor viene dado por el **teorema de Gauss**, que se deriva de las ecuaciones [9] y [10]:

$\phi=\int_S\operatorname d\phi=\int_Sc\cdot\operatorname d\Omega=c\cdot\int_S\operatorname d\Omega=4\pi c$  [11]

Expresado en palabras:

En un campo newtoniano, el flujo total a través de una superficie cerrada que contiene al centro del campo es igual a $4\pi$ multiplicado por el valor de la masa agente.

En el caso del campo eléctrico, la masa agente vale k·Q, siendo Q la carga eléctrica.

Si tenemos un conjunto de cargas, cada carga creará su flujo de campo, y el flujo total será la suma de todos ellos.

### Campo creado por una distribución infinita de cargas, plana y homogenea, usando el teorema de Gauss

Como ejemplo de la utilidad del concepto de flujo de campo y del teoriema de Gauss calcularemos el campo electrico creado por una placa cargada uniformemente, que supondremos de extensión muy grande, sobre un punto P situado a una altura h del plano.  Imaginemos otro punto P' situado al otro lado del plano, simétrico a P, y pensemos en un cilindro con eje PP' y de àrea superior dS (en la figura 12 vemos una vista lateral del plano cargado y de la situación).

$caption id="attachment_150821" align="alignnone" width="421"$![](/taller-matematicas/assets/images/Gauss.png) Fig. 12: usando el teorema de Gauss para calcular el campo eléctrico E
Por simetría el campo **E** ha de ser vertical y en las direcciones indicadas en la figura; los vectores d**S** normales a las bases del cilindro tendrán la misma dirección que **E**, luego el producto escalar resultante, teniendo en cuenta que no habrá flujo de **E** en las paredes laterales del cilindro por ser paralelas al campo (luego el vector normal a las paredes es perpendicular a **E** y su producto escalar, nulo) es $\operatorname d\phi=E\cdot dS+E\cdot dS=2E\cdot dS$.  Si llamamos $\sigma$ a la densidad de carga por unidad de superfície de la placa, la carga encerrada dentro del cilindro será $\operatorname dQ=\sigma\cdot\operatorname dS$. Por el teorema de Gauss, el flujo ha de ser entonces $\operatorname d\phi=4\mathrm\pi\cdot\mathrm k\cdot\mathrm\sigma\cdot\operatorname d\mathrm S$; igualando las dos expresiones para el flujo obtenemos:

$d\phi=4\pi k\sigma\cdot\cancel{dS}=2E\cdot\cancel{dS}\Leftrightarrow\boxed{E=2\pi k\sigma}$

Vemos que la ingensidad de campo E creada por una placa infinita cargada homogéneamente no depende de la distancia h a la placa, un resultado notable.

### Problemas

 	- Calcular el campo eléctrico producido por una esfera cargada con densidad de carga homogenea, tanto en el interior de la esfera como en el exterior.

 	- Una esfera  cargada con densidad de carga homogenea tiene una cavidad esférica en su interior, los centros de la esfera cargada y la cavidad estan a una distancia d. Calcular el campo electrico en la cavidad.

![](/taller-matematicas/assets/images/Esfera_carregada.png)

 

---

### Soluciones

**Problema 1** - En la figura vemos la geometría del problema: representamos una superficie esférica S interior y concéntrica  a la esfera cargada (en azul) y sobre S un punto cualquiera P, por la que trazamos una línea que pasa por el centro O y divide a las esferas en dos mitades simétricas; por simetría, el vector campo **E**(P) en el punto P no puede estar dirigido hacia ninguno de las dos mitades en particular, así que ha de ser radial. Además, el punto P podría ser cualquier punto situado en S pues tenemos simetría esférica, luego el módulo del campo E será el mismo en todo S, es decir, el valor de E depende sólo del radio de S.

$caption id="attachment_150832" align="alignnone" width="341"$![](/taller-matematicas/assets/images/TGauss.png) Por simetría del problema respecto cualquier recta que pase por O, el campo E ha de tener el mismo módulo en toda esfera S interior, y ha de ser radial
Vamos a aplicar el teorema de Gauss a la superficie S: primero de todo damos forma matemática a las consideraciones anteriores sobre el campo E:

$\overrightarrow E(P)=\frac1rE(r)\cdot\overrightarrow{OP}$,

o sea el vector campo **E** es igual al módulo E(r) por el vector radial **OP** dividido por el módulo de OP, que es r. Equivalentemente podemos definir el vector unitario radial $\widehat r=\frac{\overrightarrow{OP}}r$ y la expresión del campo en todo punto P de S queda más compacto: $\overrightarrow E(P)=E(r)\cdot\widehat r$.

Ahora calculamos el flujo de E a través de la superfície S, aplicando [10]:

$\phi=\int_S\operatorname d\phi=\int_S\overrightarrow E\cdot d\overrightarrow S=\int_SE\left(r\right)\widehat r\cdot d\overrightarrow S=E\left(r\right)\int_SdS=E\left(r\right)\cdot4\pi r^2$

donde hemos aplicado que el elemento diferencial vectorial de superfície d**S** es un vector radial de módulo dS, y por tanto su producto escalar con el vector radial unitario es simplemente dS, además E(r) es constante sobre S, luego puede salir fuera de la integral, y esta integral sobre S del elemento dS es simplemente la superfície de la esfera S. Este flujo que hemos calculado, según el  teorema de Gauss [11], ha de ser igual a $\phi=4\pi kQ$, donde Q es la carga contenida en el volumen interior a S; llamando $\rho$ a la densidad de carga por unidad de volumen, tenemos que:

$Q=\int_V\rho\cdot\operatorname dV=\frac43\rho\pi r^3\Rightarrow\phi=4\pi k\cdot\frac43\rho\pi r^3=\frac{16}3k\rho\pi^2r^3$ [12]

Igualando este flujo dado por el teorema de Gauss con el que hemos calculado antes, hallamos el módulo del campo **E**:

$E(r)\cdot4\pi r^2=\frac{16}3k\rho\pi^2r^3\Rightarrow\boxed{E(r)=\frac43k\rho\pi r}$ [13]

Vemos que la dependencia E(r) es lineal: aumenta linealmente con r. En el sistema internacional de unidades la constante k se expresa en funcion de la denominada *permitividad eléctrica del vacío* $\varepsilon_0$, y el campo se reduce a

$E(r)=\frac43\frac1{4\pi\varepsilon_0}\rho\pi r=\frac1{3\varepsilon_0}\rho r$. [14]

Esta expresión vale para $r\leq a$, siendo *a* el radio de la esfera cargada. Para distancias *r* al centro de la esfera que sean mayores que el radio *a* el cálculo es muy parecido, sólo que el valor de la carga *Q* es constante, siendo la carga total de la esfera, $Q=\frac43\pi a^3\rho$, y al sustituirla en el teorema de Gauss, el flujo total a través de una superficie de radio *r* > *a* vale$\phi=\frac43\pi a^3\rho\cdot4\pi k$, igualando este flujo con el calculado vectorialmente:*
*

$\phi=\frac43\pi a^3\rho\cdot\cancel{4\pi}k=E\left(r\right)\cdot\cancel{4\pi}r^2\Leftrightarrow\boxed{E\left(r\right)=\frac43\pi\frac{a^3}{r^2}\rho k}$ [14b]

que en función de $\varepsilon_0$ valdrá

$E\left(r\right)=\frac43\pi\frac{a^3}{r^2}\rho\frac1{4\pi\varepsilon_0}=\frac{\rho a^3}{3\varepsilon_0r^2}$. [15]

O sea que en el interior de la esfera el campo E crece linealmente con la distancia a centro, y en el exterior decrece cuadráticamente:

$caption id="attachment_150834" align="alignnone" width="321"$![](/taller-matematicas/assets/images/camp_esfera.png) Variación del campo E con la distancia r al centro en el caso de una esfera de radio a cargada uniformemente

**Problema 2** - La complicación de este problema está en ver como tratar la cavidad dentro de la esfera; la forma más fácil consiste en darse cuenta de que la situación es equivalente, en cuanto al cálculo del campo E, a suponer que la esfera, de radio R y centro en O, está cargada uniformemente en su totalidad con una densidad de carga $\rho$, y que la cavidad es otra superficie esférica, de radio r < R y centro O', a la que añadimos, superponiéndola, otra densidad de carga de igual valor pero signo contrario, $-\rho$, con ello, la carga neta en la cavidad será cero. Entonces, debido a que el campo electrico es acumulativo, podemos calcular el campo E por superposición del campo creado por toda la esfera de radio R, al que llamamos $E_O$, más el campo creado por la carga negativa en la esfera de radio r, al que llamamos $E'_O$. La geometría de este esquema lo vemos en la imagen, donde hemos dibujado un punto P cualquiera dentro de la cavidad, los dos campos generados en ese punto y el campo total.

![](/taller-matematicas/assets/images/Esfera_carregada2.png) Vectores E y geometria del problema

Para calcular cada campo aplicamos [13] pues el punto P es interior a las dos esferas consideradas:
$\overrightarrow E\left(P\right)={\overrightarrow E}_O\left(P\right)+\overrightarrow E'_O\left(P\right)=\frac43k\pi\rho r\cdot\widehat r-\frac43k\pi\rho r'\cdot\widehat r'=\frac43k\pi\rho\left(r\cdot\widehat r-r'\cdot\widehat r'\right)$

Tenemos que $r\cdot\widehat r=\overrightarrow r,\;r'\cdot\widehat r'=\overrightarrow r'$ y observando la figura deducimos que $r\cdot\widehat r-r'\cdot\widehat r=\overrightarrow r-\overrightarrow r'=\overrightarrow{OP}-\overrightarrow{O'P}=\overrightarrow{OO}'$.  Por tanto nos queda la siguiente expresión para el campo en el interior de la cavidad:
$\overrightarrow E\left(P\right)=\frac43k\pi\rho\cdot\overrightarrow{OO}'=\frac43k\pi\rho\cdot\overrightarrow d$

Observemos que E es un vector constante dirigido según la recta OO' (el vector **d** de módulo igual a la distancia *d* entre centros).

![](/taller-matematicas/assets/images/esfera_cavitat.png) El campo en el interior de una cavidad dentro de una esfera uniformemente cargada es constante
{% endraw %}