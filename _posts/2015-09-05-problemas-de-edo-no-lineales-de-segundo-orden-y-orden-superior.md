---
layout: post
title: "Problemas de EDO no lineales, de segundo orden y orden superior"
date: 2015-09-05 09:42:47 +0000
math: true
---

**1.** Resolver $y'''+y''-2y'=-e^x$

**Solución**:
Es una ecuación lineal de tercer orden de coeficiente constantes del tipo $y'''+Ay''+By'=F(x)$. Planteamos primero la ecuación homogénea asociada, $y'''+y''-2y'=0$, con ecuación característica $r^3+r^2-2r=0$, una raíz es $r=0$, las otras raíces lo son de $r^2+r-2=0$, que nos da los valores $r=-2, 1$. La solución general de la homogénea es:  $y_h=C_1+C_2e^{-2x}+C_3e^x$. Para tener la solución general *y* de la ecuación completa basta con obtener una solución particular $y_p$ y sumar ambas: $y=y_h+y_p$.

De los diversos métodos que tenemos para encontrar una solución particular, en este caso vemos que el término $F(x)$ es una función exponencial; generalmente, cuando F(x) sea una exponencial, un polinomio, una función trigonométrica o una combinación lineal de los anteriores el método más simple es el de [coeficientes indeterminados](http://tallermatematic.eu/wp/?p=987#indeterminados): ensayar $y_p=Ae^x$; pero en este caso, $Ae^x$ es una solución de la homogénea asociada, y por tanto se anula al sustituir en la ecuación completa. ensayamos $y_p=x^aF(x)$  siendo $a$ el menor valor entero posible tal que $y_p$ no es solución de la homogénea asociada; tal valor dependerá de la ecuación característica asociada a la homogénea: si tiene raíces simples bastará con tomar a = 1 si tiene raíces dobles tomamos a = 2. En nuestro caso hacemos pues $y_p=Axe^x$; derivando y sustituyendo en la ecuación completa:

$\begin{array}{l}y'=Ae^x+Axe^x=A(x+1)e^x;\;y''=Ae^x+A(x+1)e^x=A(x+2)e^x;\\y'''=Ae^x+A(x+2)e^x=A(x+3)e^x;\\y'''+y''-2y'=A(x+3)e^x+A(x+2)e^x-2A(x+1)e^x=3Ae^x;\\\end{array}$

Igualando al término independiente $F(x)$ obtenemos $3Ae^x=-e^x\Leftrightarrow A=-\frac13$, y la solución general es $y=y_h+y_p=C_1+C_2e^{-2x}+C_3e^x-\frac13xe^x.$

[![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

 **2.** Resolver $y''-2y'=(x^2-2x+1)e^{-x}$.

**Solución**:

Es una ecuación lineal de segundo orden de coeficiente constantes del tipo $y''+Ay'=F(x)$. Planteamos primero la ecuación homogénea asociada, $y''-2y'=0$, con ecuación característica $r^2-2r=0$, que tiene las raíces $r=0, 2$, por lo que las solución general de la homogénea es $y_h=C_1+C_2e^{2x}$. Para encontrar una solución particular de la completa, estudiamos la forma del término $F(x)$, que en este caso es un producto de una exponencial por un polinomio, por tanto no aplicaremos el método de coeficientes indeterminados (no tenemos una suma de exponencial y polinomio sino un producto), sino el [método del operador D](http://tallermatematic.eu/wp/?p=1030), que funciona bien con productos de exponenciales por funciones. Convertimos pues la ecuación a la notación de operadores D, resulta: $(D^2-2D)y=(x^2-2x+1)e^{-x}$, equivalentemente,  $D(D-2)y=(x^2-2x+1)e^{-x}$. Por tanto:

$\begin{array}{l}(D^2-2D)y=(x^2-2x+1)e^{-x}\Leftrightarrow y=\frac1{D^2-2D}(x^2-2x+1)e^{-x}=\\e^{-x}\frac1{\left(D-1\right)^2-2\left(D-1\right)}(x^2-2x+1)=e^{-x}\frac1{D^2-4D+3}(x^2-2x+1)\end{array}$.

Desarrollamos en serie de potencias crecientes de D la fracción, dividiendo 1 por el polinomio P(D), hasta que el resto tenga grado mayor que el polinomio en x, que es de grado 2:

$\begin{array}{l}1\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\left|\underline{\;3-4D+D^2}\right.\\\underline{1-\frac43D-\frac13D^2\;\;}\;\;\;\;\;\;\;\;\frac13+\frac49D+\frac{13}{27}D^2\\\;\;\;\;\;\frac43D-\frac13D^2\\\;\;\;\;\;\underline{\frac43D-\frac{16}9D^2+\frac49D^3}\\\;\;\;\;\;\;\;\;\;\;\;\;\;\;\frac{16}9D^2+\frac49D^3\end{array}$

 Nos quedamos sólo con el cociente, y lo aplicamos al polinomio:

$\begin{array}{l}\left(\frac13+\frac49D+\frac{13}{27}D^2\right)\left(x^2-2x+1\right)=\frac{x^2-2x+1}3+\frac49D\left(x^2-2x+1\right)+\frac{13}{27}D^2\left(x^2-2x+1\right)=\\\frac{x^2-2x+1}3+\frac49\left(2x-2\right)+\frac{13}{27}2=\frac{x^2}3+\frac{2x}9+\frac{11}{27}\end{array}$

La solución particular buscada es $y_p=e^{-x}\left(\frac{x^2}3+\frac{2x}9+\frac{11}{27}\right)$ y la solución general $y=C_1+C_2e^{2x}+e^{-x}\left(\frac{x^2}3+\frac{2x}9+\frac{11}{27}\right).$

[![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)**3.** Resolver $x^2y''+xy'+y=\ln(x)$.

**Solución**:

Es una ecuación lineal de segundo orden de coeficientes variables del tipo $P(x)y''+Q(x)y'+R(x)y=F(x)$. Si nos fijamos bien, vemos que el orden de los polinomios P, Q, R coincide con el orden de la derivada: $x^2$ para $y''$, $x para y'$, $x^0$ para y: es la denominada ecuación de Euler, que se reduce a una de coeficientes constantes con el cambio $x=e^t$, y se integra con los métodos de ecuaciones de coeficientes constantes:

$\begin{array}{l}x=e^t\Leftrightarrow t=\ln\left(x\right)\\y'=\frac{\operatorname dy}{\operatorname dx}=\frac{\operatorname dy}{\operatorname dt}\frac{\operatorname dt}{\operatorname dx}=\frac{\operatorname dy}{\operatorname dt}\frac1x=\frac{\operatorname dy}{\operatorname dt}e^{-t}\\y''=\frac{\operatorname d^2y}{\operatorname dx^2}=\frac\operatorname d{\operatorname dx}\frac{\operatorname dy}{\operatorname dx}=\frac\operatorname d{\operatorname dx}\frac{\operatorname dy}{\operatorname dt}e^{-t}=\frac{\operatorname dt}{\operatorname dx}\frac\operatorname d{\operatorname dt}\frac{\operatorname dy}{\operatorname dt}e^{-t}=\\\frac1x\cdot\left(\frac{\operatorname d^2y}{\operatorname dt^2}e^{-t}-\frac{\operatorname dy}{\operatorname dt}e^{-t}\right)=e^{-2t}\left(\frac{\operatorname d^2y}{\operatorname dt^2}-\frac{\operatorname dy}{\operatorname dt}\right)\end{array}$

Sustituimos en la ecuación:

$\begin{array}{l}e^{2t}\cdot e^{-2t}\left(\frac{\operatorname d^2y}{\operatorname dt^2}-\frac{\operatorname dy}{\operatorname dt}\right)+e^t\cdot\frac{\operatorname dy}{\operatorname dt}e^{-t}+y=t\Leftrightarrow\\\frac{\operatorname d^2y}{\operatorname dt^2}+y=t\end{array}$

La ecuación característica de la homogénea asociada es $r^2+1=0$ con raíces imaginarias $r=\pm i$, luego la solución general de la homogénea es $y_h=C_1e^{it}+C_2e^{-it}=C_1\sin\left(t\right)+C_2\cos\left(t\right).$ Para encontrar una solución particular como el segundo miembro $F(t)$ es un polinomio de grado 1, ensayamos otro polinomio de grado 1 con un coeficiente indeterminado:  $y_p=Ct+D\Rightarrow y'_p=C,\;y''_p=0$, sustituimos en la ecuación completa: $0+Ct+D=t\Rightarrow C=1,\;D=0$, la solución particular es $y_p=t$, y la solución general de la completa es $y=C_1\sin\left(x\right)+C_2\cos\left(x\right)+t$; deshacemos el cambio: $y=C_1\sin\left(t\right)+C_2\cos\left(t\right)+t=C_1\sin\left(\ln\left(x\right)\right)+C_2\cos\left(\ln\left(x\right)\right)+\ln\left(x\right).$

[![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

**4.**  Determinar el parámetro r de forma que la ecuación $x^2y'-x^2y^2+xy+1=0$ admita la solución particular $y=x^r$, y resolver la ecuación.

Sustituimos $y=x^r$ en la ecuación y operamos:

$\begin{array}{l}x^2rx^{r-1}-x^2x^{2r}+xx^r+1=0\Rightarrow rx^{r+1}-x^{2r+2}+x^{r+1}+1=0\Rightarrow\\x^{r+1}\left(r-x^{r+1}+1\right)=-x^0\Leftrightarrow r=-1\end{array}$

Por tanto tenemos la solución particular $y_p=x^{-1}$. La ecuación $x^2y'-x^2y^2+xy+1=0$ equivale a $y'=y^2-\frac1xy-\frac1{x^2}=P(x)y^2+Q(x)y+R(x)$ que es del tipo [Ricatti](http://tallermatematic.eu/wp/?p=913#bernoulli): se resuelven con el cambio de variable $y=y_p+1/u(x)$ que las convierte
 en lineales:

$y=y_p+\frac1u=\frac1x+\frac1u;\;y'=\frac{-1}{x^2}+\frac{-1}{u^2}u';y^2=y_p^2+\frac1{u^2}+\frac{2y_p}u;$

Sustituimos en la ecuación y simplificamos:

$\begin{array}{l}\cancel{\frac{-1}{x^2}}+\frac{-1}{u^2}u'=\cancel{\frac1{x^2}}+\frac1{u^2}+\frac2{ux}-\frac1x\left(\cancel{\frac1x}+\frac1u\right)\cancel{-\frac1{x^2}}\Leftrightarrow\\u'=-1-\frac{2u}x+\frac ux\Leftrightarrow\boxed{u'+\frac ux=-1}\\\end{array}$

Efectivamente obtenemos una ecuación lineal que resolvemos usando la fórmula general (ver [EDOs lineales de primer orden](http://tallermatematic.eu/wp/?p=897)):

$\begin{array}{l}U=exp\int\frac1x=x;\\V=\int\left(-1\cdot exp\int-\frac1x\right)=-\int exp(-\ln\left(x\right))=-\int\frac1x=-\ln\left(x\right);\\u\left(x\right)=U\left[C+V\right]=x\left[C-\ln\left(x\right)\right]\\\end{array}$

Deshacemos el cambio de variable:

$\begin{array}{l}y=y_p+\frac1{u(x)}\Leftrightarrow u(x)=\frac1{y-y_p}=\frac1{y-1/x}\Rightarrow\\\\\frac1{y-1/x}=x\left[C-\ln\left(x\right)\right]\Rightarrow\frac1{x\left(C-\ln\left(x\right)\right)}=y-\frac1x\Rightarrow\boxed{y=\frac1x\left(1+\frac1{C-\ln\left(x\right)}\right)}\end{array}$

[![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)**5. **Resolver la ecuación lineal de segundo orden con coeficientes variables siguiente: $\left(x+2\right)^2y''+4\left(x+2\right)y'+2y=-3\ln\left(x+2\right)$

Vemos que el coeficiente variable $(x+2)$ está elevado a una potencia que coincide con el orden de la derivada de la función y, hecho que nos hace pensar en la [ecuación de Euler](http://tallermatematic.eu/wp/?p=987#euler); si hacemos el cambio de variable $x+2=t$, que implica $\frac{\operatorname dy}{\operatorname dx}=\frac{\operatorname dy}{\operatorname dt}\frac{\operatorname dt}{\operatorname dx}=\frac{\operatorname dy}{\operatorname dt}\frac{\operatorname d(x+2)}{\operatorname dx}=\frac{\operatorname dy}{\operatorname dt}$, la ecuación queda en la forma de Euler: $t^2y''+4ty'+2y=-3\ln\left(t\right)$, dónde ahora y es función de t. Procedemos con el método general para ecuaciones de Euler:

Paso 1) resolver la homogénea asociada ensayando la solución $y=t^r$ que resulta:

$y=t^r;\;y'=rt^{r-1};\;y''=r\left(r-1\right)t^{r-2};$

$t^2y''+4ty'+2y=0\Leftrightarrow t^2r\left(r-1\right)t^{r-2}+4trt^{r-1}+2t^r=0\Leftrightarrow$

$\begin{array}{l}t^2y''+4ty'+2y=0\Leftrightarrow t^2r\left(r-1\right)t^{r-2}+4trt^{r-1}+2t^r=0\Leftrightarrow\\t^r\left[r\left(r-1\right)+4r+2\right]=0\Leftrightarrow r^2+3r+2\Leftrightarrow r=-2,\;-1\end{array}$

La solución general de la homogénea es: $y=C_1t^{-2}+C_2t^{-1}=\frac{C_1}{\left(x+2\right)^2}+\frac{C_2}{\left(x+2\right)}$

Paso 2) Aplicar el cambio $t=e^u$ que convierte la ecuación en lineal de coeficientes constantes, y entonces encontrar una solución particular. El cambio de variable implica que:

$\begin{array}{l}t=e^u\Leftrightarrow u=\ln\left(t\right);\;\frac{\operatorname dy}{\operatorname dt}=\frac{\operatorname dy}{\operatorname du}\frac{\operatorname du}{\operatorname dt}=\frac{\operatorname dy}{\operatorname du}\frac1t;\;\\\frac{\operatorname d^2y}{\operatorname dt^2}=\frac{\operatorname d{}}{\operatorname dt}\left(\frac{\operatorname dy}{\operatorname du}\frac1t\right)=\left(\frac\operatorname d{\operatorname du}\frac{\operatorname dy}{\operatorname du}\frac{\operatorname du}{\operatorname dt}\right)\frac1t+\frac{\operatorname dy}{\operatorname du}\frac{\operatorname d{}}{\operatorname dt}\frac1t=\frac{\operatorname d^2y}{\operatorname du^2}\frac1{t^2}-\frac{\operatorname dy}{\operatorname du}\frac1{t^2}=\frac1{t^2}\left(\frac{\operatorname d^2y}{\operatorname du^2}-\frac{\operatorname dy}{\operatorname du}\right)\end{array}$,

sustituimos en la ecuación diferencial, y obtenemos:

$\begin{array}{l}e^{2u}\frac1{e^{2u}}\left(\frac{\operatorname d^2y}{\operatorname du^2}-\frac{\operatorname dy}{\operatorname du}\right)+4e^u\frac{\operatorname dy}{\operatorname du}\frac1{e^u}+2y=-3\ln\left(e^u\right)\Leftrightarrow\\\frac{\operatorname d^2y}{\operatorname du^2}+3\frac{\operatorname dy}{\operatorname du}+2y=-3u\\\end{array}$

que es una ecuación lineal de segundo orden con coeficientes contantes; queremos una de sus soluciones particulares, viendo que el miembro de la derecha es un polinomio de primer grado, lo más sencillo es ensayar una solución particular del mismo tipo $y_p=Au+B$, probamos: $0+3\cdot A+2Au+2B=-3u\Leftrightarrow A=-\frac32,\;B=\frac94\Leftrightarrow y_p=-\frac32u+\frac94$. Sumando esta solución particular a la de la homogénea y deshaciendo los cambios de variable  obtenemos la solución general:

$y=y_h+y_p=\boxed{\frac{C_1}{\left(x+2\right)^2}+\frac{C_2}{\left(x+2\right)}-\frac32\ln\left(x+2\right)+\frac94}$

[![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

**5.** Encontrar una solución particular de la ecuación $y''+4y'=\sin^2(x)$ usando el método de variación de constantes (también llamado variación de parámetros).

Necesitamos encontrar la solución general de la homogénea, como es una ecuación lineal de coeficientes constantes ésto se reduce a resolver la ecuación característica $r^2+4r=0$ que tiene las raíces $r=0, r=\pm2i$, por tanto la solución de la homogénea es $y_h=C_1\sin\left(2x\right)+C_2\cos\left(2x\right).$ El método de variación de constantes ensaya una solución particular igual a la solución de la homogénea pero cambiando las constantes (variando las constantes) por funciones desconocidas $u(x), v(x)$; calculemos el Wronskiano de las funciones solución de la homogénea:

$W=\begin{vmatrix}\sin\left(2x\right)&amp;\cos\left(2x\right)\\2\cos\left(2x\right)&amp;-2\sin\left(2x\right)\end{vmatrix}=-2\sin^2\left(2x\right)-2\cos^2\left(2x\right)=-2\left(\sin^2\left(2x\right)+\cos^2\left(2x\right)\right)=-2$

La función $u(x)$ viene dada por:

$u\left(x\right)=\frac{\begin{vmatrix}\sin^2\left(x\right)&amp;\cos\left(2x\right)\\2\sin\left(x\right)\cos\left(x\right)&amp;-2\sin\left(2x\right)\end{vmatrix}}W=\frac{-2\sin^2\left(x\right)\sin\left(2x\right)-2\sin\left(x\right)\cos\left(x\right)\cos\left(2x\right)}2;$

Usando las identidades $\sin\left(2x\right)=2\sin\left(x\right)\cos\left(x\right),\;\cos\left(2x\right)=\cos^2\left(x\right)-\sin^2\left(x\right)$ para simplificar la expresión, obtenemos:

$u\left(x\right)=\sin\left(x\right)\cos\left(x\right)\left(2\sin^2\left(x\right)+\cos\left(2x\right)\right)=\sin\left(x\right)\cos\left(x\right)$

Para la función $v(x)$ calculamos:

$\begin{array}{l}u\left(x\right)=\frac{\begin{vmatrix}\sin\left(x\right)&amp;\sin^2\left(x\right)\\2\cos\left(2x\right)&amp;2\sin\left(x\right)\cos\left(x\right)\end{vmatrix}}W=\frac{2\sin\left(x\right)\cos\left(x\right)\sin\left(2x\right)-2\sin^2\left(x\right)\cos\left(2x\right)}2=\\2\sin^2\left(x\right)\cos\left(x\right)-\sin^2\left(x\right)\cos\left(2x\right)=\sin^2\left(x\right)\end{array}$

La solución particular es:

$\begin{array}{l}y=u\left(x\right)\cdot\sin\left(2x\right)+v\left(x\right)\cdot\cos\left(2x\right)=\\-\sin\left(x\right)\cos\left(x\right)\cdot\sin\left(2x\right)-\sin^2\left(x\right)\left[2\cos^2\left(x\right)+\cos\left(2x\right)\right]\cdot\cos\left(2x\right)\end{array}$