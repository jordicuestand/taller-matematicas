---
layout: post
title: "Mètodos operacionales: el operador D"
date: 2015-05-01 09:35:31 +0000
categories:
  - "Ecuaciones Diferenciales"
  - "Matemáticas"
tags:
  - "ecuación diferencial"
  - "ecuaciones lineales de coeficientes constantes"
  - "operador D"
  - "operador diferencial"
math: true
---
{% raw %}

**Introducción**
Los métodos de resolución de EDO vistos en los post anteriores han sido parecidos "recetas" matemáticas, en el sentido de que no hemos visto ninguna justificación de por que funcionan. Así, nos hemos encontrado con rectas del tipo "*si la ecuación es lineal homogénea de coeficientes constantes, entonces tenemos que encontrar las raíces de su ecuación característica asociada, y ...*".  En este post vemos una introducción a los métodos basados en el operador derivación D que nos permiten justificar algunos de los métodos anteriores, y nos proporciona uno de de nuevo para encontrar soluciones particulares.  También señalaremos que este método es más "algebraico" que los anteriores, de hecho, utiliza conceptos del Álgebra Lineal, que nosotros, en nuestra introducción práctica, no necesitaremos.

 	- El operador diferencial D

 	- Integración de ecuaciones lineales de coeficientes constantes usando operadores diferenciales

 	- Generalización a otras ecuaciones

 	- Ejercicios

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)

# El operador diferencial D

Un "operador" lo podemos definir como un objeto matemático que toma una función y nos devuelve otra. Por ejemplo la operación de derivar hace precisamente ésto. dada la función $y=f(x)$ nos devuelve otra función $y'=df/dx$ que llamamos derivada de la función original. Lo que hacemos a continuación es definir el operador asociado a la derivación.

**Definición 1**: El operador D aplicado a la función y, $Dy$, devuelve la derivada de la función: $Dy=y'$.

Aplicando el operador D repetidas veces obtenemos las derivadas sucesivas de la función:

$D(Dy)=D^2y=y'', D(D^2y)= D^3y=y''', ... , D^ny=y^{(n}$

Como ya sabemos, la operación inversa de la derivación es la integración; parece pues lógico definir:
**Definición 2**: El operador $D^{-1}$ aplicado a la función y, $D^{-1}y$,  devuelve la función primitiva (integral indefinida) de la función: $D^{-1}y=\int y\operatorname dx$.

Aplicando el operador$D^{-1}$ repetidas veces obtenemos las integrales reiteradas: $D^{-n}y=\int\dots\int y\operatorname dx^n.$

Recordemos que la derivación es una operación lineal: $(C_1f(x)+C_2g(x))' = C_1f'(x)+C_2g'(x)$, por lo tanto el operador D también será lineal. Podemos is más allá y definir polinomios en D. Para no ser tan teóricos, los definiremos aplicándolos a EDO.
**Definición 3**: Dada una EDO $F(x,y,y',y'', ...,y^{(n})=0$ definimos su operador diferencial P(D) sustituyendo cada derivada $y^{(k}$ por su operador $D^k$.

**Ejemplo 1**: El operador diferencial correspondiente a la EDO $y'''-xy''+2e^xy'+10y-x=0$ es $P(D)=D^4-xD^2+2e^xD+10)$, de forma  que la ecuación se puede escribir $P(D)y-x=0$.

Veamos ahora algunas propiedades de los operadores (polinómicos) diferenciales P(D) que nos servirán para resolver EDO.
**Propiedad 1**: Efecto de P(D) sobre la función exponencial $y=e^x$. La función exponencial $y=e^x$ viene a ser el "elemento neutro" del operador D, pues $De^x=e^x$. Aplicando esta propiedad a un polinomio $P(D)=a_nD^n+\cdots+a_1D+a_0$ resulta $P(D)e^x=a_ne^x+\cdots+a_1e^x+a_0e^x=e^x\left(a_n+\cdots+a_1+a_0\right)=e^xP(1)$. Si en vez de $e^x$ tenemos $e^{rx}$ entonces obtenemos la expresión más general $P(D)e^{rx}=a_nr^ne^{rx}+\cdots+a_1re^{rx}+a_0e^{rx}=e^{rx}\left(a_nr^n+\cdots+a_1r+a_0\right)=e^xP(r).$

**Propiedad 2**: Efecto de los operadores (D+a) y (D-a) sobre la función exponencial $y=e^{rx}$. En este caso es fácil ver, derivando, que se cumple:

$\begin{array}{l}\left(D+a\right)e^{rx}=re^{rx}+ae^{rx}=\left(r+a\right)e^{rx}\\\left(D-a\right)e^{rx}=re^{rx}-ae^{rx}=\left(r-a\right)e^{rx}\end{array}$

**Propiedad 3**: Efecto de los operadores (D+a) y (D-a) sobre la función $y=e^{rx}·f(x)$, donde $f(x)$ es una función derivable cualquiera. Derivando obtenemos:

$\begin{array}{l}\left(D+a\right)e^{rx}\cdot f=re^{rx}\cdot f+e^{rx}f'+a\left(e^{rx}f\right)=e^{rx}\left(rf+f'+af\right)=e^{rx}\left(D+r+a\right)f;\\\left(D-a\right)e^{rx}\cdot f=re^{rx}\cdot f+e^{rx}Df-a\left(e^{rx}f\right)=e^{rx}\left(r+f'-af\right)=e^{rx}\left(D+r-a\right)f;\end{array}$

Vemos que los operadores (D+a) y (D-a) aplicaos al factor $e^{rx}$ causan que el factor "pase al otro lado" y se modifica el operador sumándole r.  Si tenemos un polinomio P(D) que puede descomponerse en producto de binomios, entonces podemos aplicar reiteradamente la propiedad 3.

**Ejemplo 2**: El operador $P(D)=D^2-1$ se descompone como $P(D)=(D-1)(D+1)$, luego para calcular $P(D)e^{5x}\cos(x)$ hacemos:

$\begin{array}{l}\left(D+1\right)e^{5x}\cdot\cos\left(x\right)=e^{5x}\left(D+6\right)\cos\left(x\right);\\P(D)e^{5x}\cdot\cos\left(x\right)=\left(D-1\right)e^{5x}\left(D+6\right)\cos\left(x\right)=e^{5x}\left(D+4\right)\left(D+6\right)\cos\left(x\right)\end{array}$
**Propiedad 4**: $P(D)\left$e^{at}\cdot f\left(t\right)\right$=e^{at}P\left(D+a\right)f\left(t\right)$. Es una consecuencia de la propiedad 3. Además, tomando $f(t)=1$ obtenemos la propiedad 1, por tanto esta propiedad incluye a la primera como caso especial.

**Propiedad 5**: Inversa de un operador P(D); se cumple que $\frac1{P\left(D\right)}\left$e^{at}f\left(t\right)\right$=e^{at}\frac1{P\left(D+a\right)}f\left(t\right)$. Es una consecuencia de la propiedad 4: definimos $g(t)=\frac1{P\left(D+a\right)}f\left(t\right)$ y le aplicamos la propiedad 4:

$\begin{array}{l}P\left(D\right)e^{at}g(t)=e^{at}P\left(D+a\right)g(t)=e^{at}P\left(D+a\right)\frac1{P\left(D+a\right)}f\left(t\right)=e^{at}f\left(t\right)\Rightarrow\\\frac1{P\left(D\right)}P\left(D\right)e^{at}g(t)=\boxed{e^{at}\frac1{P\left(D+a\right)}f\left(t\right)=\frac1{P\left(D\right)}\left$e^{at}f\left(t\right)\right$}.\end{array}$

**Ejemplo 3**: Aplicando la propiedad 5:

$\begin{array}{l}\frac1{D^2-2D+1}\frac{e^t}t=e^t\frac1{\left(D+1\right)^2-2\left(D+1\right)+1}\frac1t=\\e^t\frac1{D^2+1+2D-2D-2+1}\frac1t=e^t\frac1{D^2}\frac1t\end{array}.$

Aplicando la definición 1: $e^t\frac1{D^2}\frac1t=e^t\int\operatorname dt\int\frac1t\operatorname dt=e^t\int\ln\left(t\right)\operatorname dt=e^tt\left(\ln\left(t\right)-1\right)$, la última integral se hace por partes.

**Ejemplo 4**: Por la propiedad 4,

$\frac1{D^2-D-2}t^2e^{2t}=e^{2t}\frac1{\left(D+2\right)^2-\left(D+2\right)-2}t^2=e^{2t}\frac1{D^2+3D}t^2$

Para calcular $\frac1{D^2+3D}t^2$ se recurre a la siguiente técnica de desarrollo en serie de $1/P(D)$ en potencias crecientes: dividimos $P(D)$ por 1 para obtener un cociente $C(D)$ y un resto $R(D)$ que tenga grado superior al polinomio $t^2$, o sea, grado superior a 2:

$\begin{array}{l}1\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\underline{\left|3D+D^2\right.}\\\underline{-1-\frac13D}\;\;\;\;\;\;\;\frac13D^{-1}-\frac19+\frac1{27}D\\\;\;\;\;\;\;\;\;-\frac13D\\\;\;\;\;\;\;\;\;\;\underline{\;\;\frac13D+\frac19D^2}\\\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\frac19D^2\\\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\underline{-\frac19D^2-\frac1{27}D^3}\\\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;-\frac1{27}D^3\\\end{array}$

Obtenemos pues $C(D)=\frac13D^{-1}-\frac19+\frac1{27}D, R(D)=\frac1{27}D^3$, o sea,

$\frac1{3D+D^2}=\left(\frac13D^{-1}-\frac19+\frac1{27}D\right)+\frac{-\frac1{27}D^3}{3D+D^2}$

Ahora lo aplicamos al polinomio $t^2$, teniendo en cuenta que $D^3t^2=0$ ya que la derivada es de orden superior al exponente:

$\begin{array}{l}\frac1{3D+D^2}t^2=\left(\frac13D^{-1}-\frac19+\frac1{27}D\right)t^2+\frac{-\frac1{27}D^3}{3D+D^2}t^2=\\\frac13\int t^2-\frac19t^2+\frac1{27}Dt^2-\frac{\left(\frac1{27}D^3t^2\right)}{3D+D^2}=\\t^3-\frac19t^2+\frac1{27}2t-\frac0{3D+D^2}=t^3-\frac19t^2+\frac1{27}2t\end{array}$

Nos queda:

$\frac1{D^2-D-2}t^2e^{2t}=t^2=e^{2t}\frac1{D^2+3D}t^2=\boxed{e^{2t}\left(t^3-\frac19t^2+\frac1{27}2t\right)}$

En general esto sucederá siempre: el resto de la división $1/P(D)$ anulará el polinomio, y no es necesario calcularlo cada vez. De
este ejemplo podemos dar una regla general:
**Propiedad 6:** Cálculo de $\frac1{P(D)}Q\left(t\right)$ donde $Q(t)$ es un polinomio de grado n.

a) dividimos 1 por P(D), obtenemos operadores cociente C(D) y resto R(D) con grado superior a n

b) planteamos $\frac1{P(D)}Q\left(t\right)=C(D)\cdot Q\left(t\right)$ donde C(D) es un polinomio, que calculamos término a término

En lo que sigue aplicaremos el operador P(D) a la resolución de EDO de coeficientes constantes.

**Ejemplo 5**: integración de ecuaciones homogéneas de coeficientes constantes
Una ecuación homogénea se expresa como $P(D)y=0$. Suponiendo que P(D) puede descomponerse en producto de binomios (ésto es, si el polinomio tiene todas sus raíces reales, que pueden ser múltiples), tendremos:

$\begin{array}{l}P(D)=a_0\left(D-r_1\right)^{m_1}\left(D-r_2\right)^{m_2}\dots\left(D-r_k\right)^{m_k};\\P(D)y=0\Leftrightarrow a_0\left(D-r_1\right)^{m_1}\left(D-r_2\right)^{m_2}\dots\left(D-r_k\right)^{m_k}y=0\end{array}$

Esta ecuación se descompone en k ecuaciones:

$\begin{array}{l}\left(D-r_1\right)^{m_1}y=0\\\left(D-r_2\right)^{m_2}y=0\\\dots\\\left(D-r_k\right)^{m_k}y=0\end{array}$

Multiplicamos cada una de ellas por el factor exponencial $e^{-mx}$, queda:

$\begin{array}{l}e^{-r_1x}\left(D-r_1\right)^{m_1}y=0\\e^{-r_2x}\left(D-r_2\right)^{m_2}y=0\\\dots\\e^{-r_kx}\left(D-r_k\right)^{m_k}y=0\end{array}$

Aplicando a cada una la propiedad 3 las simplificamos y resolvemos:

$\begin{array}{l}e^{-r_1x}\left(D-r_1\right)^{m_1}y=D^{m_1}e^{-r_1x}y=0\Rightarrow e^{-r_1x}y=Q_{m_1-1}\left(x\right)\\e^{-r_2x}\left(D-r_2\right)^{m_2}y=D^{m_2}e^{-r_2x}y=0\Rightarrow e^{-r_2x}y=Q_{m_2-1}\left(x\right)\\\dots\\e^{-r_kx}\left(D-r_k\right)^{m_k}y=D^{m_k}e^{-r_kx}y=0\Rightarrow e^{-r_kx}y=Q_{m_k-1}\left(x\right)\end{array}$

donde los $Q(x)_{m-1}$ son polinomios de grado m-1, pues entonces la derivada m-ésima será cero: $D^m Q(x)_{m-1}=0$. Despejando las y de cada ecuación y combinándolas obtenemos la solución general:

$\begin{array}{l}y=e^{r_1x}Q_{m_1-1}\left(x\right)+e^{r_2x}Q_{m_2-1}\left(x\right)+\dots+e^{r_kx}Q_{m_k-1}\left(x\right)\end{array}$

**Ejemplo 6**: Integrar $y'''-2y''-5y'+6y=0$. El operador es $P(D)=D^3-2D^2-5D+6$, lo descomponemos en producto de factores simples, $P(D)=(D-1)(D+2)(D-3)$, todos con multiplicidad 1, luego para cada factor el polinomio Q es de grado 0 (una constante), y la solución general es $y=C_1e^x+C_2e^{-2x}+C_3e^{3x}$

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)
# Integración de ecuaciones lineales de coeficientes constantes usando operadores diferenciales

Para las ecuaciones lineales del tipo

$y^{(n}+P_1y^{(n-1}+\dots+P_{n-2}y^{''}+P_{n-1}y^'+P_ny=e^{rx}Q\left(x\right)$

donde $Q(x)$ es un polinomio tenemos ya un procedimiento para encontrar una solución particular: si la escribimos en la forma $P(D)y=e^{rx}Q\left(x\right)$, entonces $y=\frac1{P(D)}e^{rx}Q\left(x\right)$, aplicando la propiedad 5, $y=e^{rx}\frac1{P(D+r)}Q\left(x\right)$, y aplicando la propiedad 6, $y=e^{rx}\frac1{P(D+r)}Q\left(x\right)=e^{rx}C(D)e^{rx}.$

**Ejemplo 7**: Encontrar una solución particular de $y''-2y'=(x^2-2x+1)e^{-x}$.

Planteamos la ecuación con operadores D:

$(D^2-2D)y=(x^2-2x+1)e^{-x}\Leftrightarrow y=\frac1{D\left(D-2\right)}(x^2-2x+1)e^{-x}$

Aplicamos primero la propiedad 5:

$\frac1{D^2-2D}(x^2-2x+1)e^{-x}=e^{-x}\frac1{\left(D-1\right)^2-2\left(D-1\right)}(x^2-2x+1)=\frac1{D^2-4D+3}(x^2-2x+1)$

Ahora la propiedad 6, dividimos $1:P(D)$ en potencias crecientes de D hasta obtener un resto con grado superior a 2, ya que el polinomio Q(t) en este ejemplo es $x^2-2x+1$, obtenemos:

$\begin{array}{l}1\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\underline{\left|3-4D+D^2\right.}\\\underline{-1+\frac43D-\frac13D^2}\;\;\;\;\;\;\frac13+\frac49D\\\;\;\;\;\;\;\frac43D-\frac13D^2\\\;\;\;-\frac43D+\frac{16}9D^2-\frac49D^3\end{array}$

Entonces:

$\begin{array}{l}\frac1{D^2-4D+3}(x^2-2x+1)=\left(\frac13+\frac49D\right)(x^2-2x+1)=\frac13(x^2-2x+1)+\frac49(2x-2)=\\\frac13x^2+\frac29x-\frac59\end{array}$

y la solución particular buscada es $y=e^{-x}\left(\frac13x^2+\frac29x-\frac59\right).$

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)

Si el término de la derecha de la ecuación es una suma de términos de la forma $e^{rx}Q\left(x\right)$, aplicando el principio de superposición de soluciones de las ecuaciones lineales encontramos una solución particular para cada término, y las sumamos todas.

**Ejemplo 8**: Encontrar una solución particular de $y''-2y'=(x^2-2x+1)e^{-x}+x·e^{2x}.$

Tenemos  $P(D)y=F(x)+G(x)$, separamos dos problemas, el primero es $(D^2-2D)y=(x^2-2x+1)e^{-x}$ que hemos resuelto en el ejemplo anterior; el segundo es $(D^2-2D)y=x·e^{2x}$. Procedemos como antes:

$\begin{array}{l}(D^2-2D)y=x\cdot e^{2x}\Leftrightarrow y=\frac1{D^2-2D}\left(x\cdot e^{2x}\right)=e^{2x}\frac1{\left(D+2\right)^2-2\left(D+2\right)}x=\\e^{2x}\frac1{D^2-4D+3}x=e^{2x}\left(\frac13\right)x=\frac13xe^{2x}\end{array}$

En la división $1:P(D)$ hemos aprovechado la del problema anterior, pero ahora es más corta, pues el polinomio $Q(x)=x$ es de grado 1:

$\begin{array}{l}1\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\underline{\left|3-4D+D^2\right.}\\\underline{-1+\frac43D-\frac13D^2}\;\;\;\;\;\;\frac13\\\;\;\;\;\;\;\frac43D-\frac13D^2\\\;\;\;\end{array}$

Superponiendo las dos soluciones encontradas, obtenemos la solución particular requerida:

$y=e^{-x}\left(\frac13x^2+\frac29x-\frac59\right)+\frac13xe^{2x}$

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)

# Generalización a otras ecuaciones

El método que hemos visto se puede generalizar a ecuaciones con el término de la derecha distinto de $e^{rx}Q\left(x\right)$, e incluso se puede aplicar a ecuaciones con coeficientes variables. Además, el factor exponencial $e^{rx}$ también puede generalizarse con exponentes imaginarios$e^{irx}$; en éste último caso aplicando la propiedad 1 se cumple que

$P(D^2)e^{irt}=e^{irt}P\left(\left(ir\right)^2\right)=e^{irt}P\left(-r^2\right)$

Usando la identidad $e^{irt}=\cos\left(rt\right)+i\sin\left(rt\right)$ en la expresión anterior, e igualando partes reales e imagnarias, obtenemos una nueva propiedad del operador D:

$\begin{array}{l}P(D^2)\left(\cos\left(rt\right)+i\sin\left(rt\right)\right)=P(D^2)\cos\left(rt\right)+P(D^2)i\sin\left(rt\right)=\\e^{irt}P\left(-r^2\right)=P\left(-r^2\right)\cos\left(rt\right)+P\left(-r^2\right)i\sin\left(rt\right)\Rightarrow\\\boxed{\begin{array}{l}P(D^2)\cos\left(rt\right)=P\left(-r^2\right)\cos\left(rt\right),\;\\P(D^2)\sin\left(rt\right)=P\left(-r^2\right)i\sin\left(rt\right).\end{array}}\end{array}$

**Ejemplo 9**: Empleamos exponentes complejos para simplificar la siguiente expresión:

$\begin{array}{l}\frac1{D^2-2D+2}te^t\cos\left(t\right)=e^t\frac1{D^2+1}t\cos\left(t\right)=e^t\boldsymbol R\boldsymbol e\left\{\frac{\mathbf1}{\mathbf D^\mathbf2\boldsymbol+\mathbf1}\mathbf t\mathbf e^{\mathbf i\mathbf t}\right\}=\\e^t\boldsymbol R\boldsymbol e\left\{\mathrm e^\mathrm{it}\frac1{\left(\mathrm D+\mathrm i\right)^2+1}\mathrm t\right\}\boldsymbol=e^t\boldsymbol R\boldsymbol e\left\{\mathrm e^{it}\frac1{\mathrm D^2+2\mathrm{iD}}\mathrm
t\right\}\boldsymbol=\end{array}$

el símbolo $\boldsymbol R\boldsymbol e$ significa "parte real de..."; ahora dividimos:

$\begin{array}{l}1\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\underline{\left|2iD+D^2\right.}\\\underline{-1-\frac1{2i}D}\;\;\;\;\;\frac1{2i}D^{-1}\\\;\;\;\;\;\;-\frac1{2i}D\end{array}$

entonces:

$\begin{array}{l}e^t\boldsymbol R\boldsymbol e\left\{\mathrm e^{it}\frac1{\mathrm D^2+2\mathrm{iD}}\mathrm t\right\}=e^t\boldsymbol R\boldsymbol e\left\{\mathrm e^{it}\frac1{2\mathrm i}\mathrm D^{-1}\mathrm t\right\}=\\e^t\boldsymbol R\boldsymbol e\left\{\left(\frac{-\sin\left(\mathrm t\right)}2+\frac{\mathrm i}2\cos\left(\mathrm t\right)\right)\mathrm D^{-1}\mathrm t\right\}=e^t\frac{-\sin\left(\mathrm t\right)}2\int t\operatorname dt=-\frac{t^2}4e^t\sin\left(t\right)\end{array}.$

![separador2](/taller-matematicas/assets/images/separador2-300x37.png)

## Ejercicios

**1.** Resolver $y''-2y'=(x^3-2x+1)e^{-x}$.

**2.** Resolver $y''-2y'=x^2-5$

**3.** Resolver $y''-2y'+2y=e^x\cdot\cos(x)$ usando exponenciales complejas para representar la función coseno.
{% endraw %}