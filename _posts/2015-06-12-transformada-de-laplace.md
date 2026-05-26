---
layout: post
title: "Transformada de Laplace"
date: 2015-06-12 15:11:47 +0000
math: true
---
{% raw %}

# Introducción

	- Transformadas integrales; transformada de Laplace

	- Tablas de transformadas

	- Transformada inversa

	- Aplicación a la resolución de EDOs lineales de primer orden con coeficientes constantes

	- Aplicación a EDOs lineales de orden superior

[![separador2](/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Transformadas integrales; transformada de Laplace

La transformada integral es una aplicación entre funciones, que hace corresponder a cada $f(x)$ otra aplicación $F(z)$ obtenida calculando la siguiente integral:

$T\left(f\left(x\right)\right)=\int_DN(z,t)\cdot f\left(t\right)\operatorname dt=F\left(z\right)$

La función $N(z,t)$ se denomina núcleo de la transformada; hay por tanto tantas aplicaciones transformadas como posibles funciones $N(z,t).$
**Ejemplo 1**: La transformada de Hilbert, útil en procesamiento de señales, emplea la siguiente integral:

$T\left(f\left(x\right)\right)=\int_D\frac1{\mathrm\pi}\frac1{z-t}\cdot f\left(t\right)\operatorname dt=F\left(z\right)$

La idea detrás de las transformadas integrales es, en un problema dado convertir una función en otra más simple. Para el caso de las ecuaciones diferenciales tenemos la transformada de Laplace:
**Definición**: La **transformada de Laplace** es una transformada integral que usa como núcleo de la transformación la función $e^{-zt}$, resultando la integral:

$L\left(f\left(x\right)\right)=\int_De^{-zt}\cdot f\left(t\right)\operatorname dt=F\left(z\right)$

El dominio de integración es $\left[0,\infty\right],$ tenemos pues una integral impropia.
**Ejemplo 2**: La transformada de Laplace de la función $f(x)=e^x$ es:

$L\left(e^x\right)=\int_De^{-zt}\cdot e^t\operatorname dt=\int_0^\infty e^{\left(1-z\right)t}\operatorname dt=\left[\frac{e^{\left(1-z\right)t}}{1-z}\right]_0^\infty$

esta integral impropia se resulve por paso al límite:

$\lim_{b\rightarrow\infty}\left[\frac{e^{\left(1-z\right)t}}{1-z}\right]_0^b=\frac1{1-z}\left[\lim_{b\rightarrow\infty}e^{\left(1-z\right)b}-1\right]=-\frac1{1-z}\text{si }z&gt;1$

Así pues $L\left(e^x\right)=\frac1{z-1}$ siempre que $z&gt;1$. Esto es la regla común: al calcular la transformada habitualmente tendremos que restringir los valores de la variable independiente z para que la integral exista.

**Ejemplo 3**: La transformada de la función $y=Cx^n$ nos lleva a la integral $L(Cx^n)=\int_0^\infty e^{-zt}Ct^n\operatorname dt$ que podemos hacer por partes:

$\begin{array}{l}L(Cx^n)=\int_0^\infty e^{-zt}Ct^n\operatorname dt=C\left[-t^n\frac1ze^{-zt}\right]_0^\infty+C\int_0^\infty\frac1ze^{-zt}nt^{n-1}\operatorname dt\\u=t^n,\;\operatorname du=nt^{n-1},\operatorname dv=e^{-zt},v=-\frac1ze^{-zt}\end{array}$

El primer miembro es cero, y para el segundo miembro volviendo a hacer por partes la integral $\frac nz\int_0^\infty e^{-zt}t^{n-1}\operatorname dt$ reducimos el orden del exponente de t; reiterando el procedimiento llegamos a la integral $\frac{n!}{z^n}\int_0^\infty e^{-zt}\operatorname dt=\frac{n!}{z^n}\left[-\frac1ze^{-zt}\right]_0^\infty=\frac{n!}{z^{n+1}}$. Por tanto nos queda $L(Cx^n)=C\frac{n!}{z^{n+1}}.$

# Tablas de transformadas

En la práctica no suele ser necesario calcular integrales para obtener la transformada de Laplace, sino que se recurre a tablas de transformadas y a la linealidad de la transformada:
**Teorema 1**: *la transformada de Laplace es una operación lineal; sean f,g dos funciones y A,B dos constantes, entonces $L(Af+Bg)=AL(f)+BL(g)$.*

**Ejemplo 4**: en el ejemplo 3 hemos visto que $L(Cx^n)=C\frac{n!}{z^{n+1}}.$ Aplicando el teorema 1 tenemos la transformada de un polinomio:

$L(C_nx^n+C_{n-1}x^{n-1}+\cdots+C_1x^1+C_0)=C_n\frac{n!}{z^{n+1}}+C_{n-1}\frac{\left(n-1\right)!}{z^n}+\cdots+C_1\frac1{z^2}+C_0\frac1z.$

Con lo visto hasta aquí podemos formar una primera tabla de transformadas:
#### Tabla de transformadas de Laplace: versión 1.0

	- $L(C_nx^n)=C_n\frac{n!}{z^{n+1}}$

	- $L(e^{ax})=\frac1{z-a}$

	- $L(\sin\left(ax\right))=\frac a{z^2+a^2}\;\text{para }z&gt;0$

	- $L(\cos\left(ax\right))=\frac z{z^2+a^2}\;\text{para }z&gt;0$

# Transformada inversa

Para las aplicaciones es importante poder "deshacer" la transformación de Laplace, esto es, si tenemos una F tal que $F(z)=L(f(x))$ ser capaces de encontrar la función $f(x)$ realizando la transformada inversa: $f(x)=L^{-1}(F(z))$. ¿Puede hacerse? Recordemos que la inversa de una función solo existe si esta función no es exhaustiva (ver por ejemplo el post [Funciones](http://tallermatematic.eu/wp/?p=1029)). el siguiente teorema nos dice que esto es así para la transformada de Laplace:

***Teorema 2**: Si dos funciones f, g con transformadas F, G verifican que F(z) = G(z), entonces f(x)=g(x) siempre que f, g sean continuas. Dicho de otro modo: la transformada de Laplace es una aplicación inyectiva, y por tanto admite inversa.*

Para las aplicaciones a las EDO veremos a continuación que se utiliza la siguiente técnica.

	- A la ecuación original $\psi(x,y',y'',...,y^{(n})=0$ se la transforma, obteniendo otra ecuación que no tiene derivadas, sólo contiene la nueva variable z y la transformada de la y: $\varphi(z, F)=0$

	- De la anterior ecuación se despeja F, que es la transformada de y: $F = \Psi(z)$

	- Se obtiene la función y aplicando la transformada inversa: $y = \mathcal{L}^{-1}\left(\Psi\left(z\right)\right)$

En el tercer paso se necesita saber obtener la transformada inversa de Laplace. Por este motivo ampliaremos la tabla de transformadas, y daremos algunas propiedades adicionales que necesitaremos.

#### Tabla de transformadas de Laplace: versión 2.0

	- $L(C_nx^n)=C_n\frac{n!}{z^{n+1}}$

	- $L(e^{ax})=\frac1{z-a}$

	- $L(\sin\left(ax\right))=\frac a{z^2+a^2}\;\text{para }z&gt;0$

	- $L(\cos\left(ax\right))=\frac z{z^2+a^2}\;\text{para }z&gt;0$

	- $L\left(xf\left(x\right)\right)=-\frac{\operatorname d{}}{\operatorname dz}F\left(z\right)$

	- $L\left(x^nf\left(x\right)\right)=\left(-1\right)^n\frac{\operatorname d{}}{\operatorname dz^n}F\left(z\right)$

	- 

# Aplicación a la resolución de EDOs lineales con coeficientes constantes

Supongamos que tenemos que resolver una EDO lineal de primer orden $ay'+by=f(x)$ con unas condiciones iniciales $y(0)=y_0$. Apliquemos la transformada a toda la ecuación: $L\left(ay'+by\right)=L\left(f\left(x\right)\right)\Rightarrow aL\left(y'\right)+bL\left(y\right)=L\left(f\left(x\right)\right).$ Para calcular la transformada de la derivada usaremos la siguiente propiedad:
***Teorema 3**: Bajo ciertas condiciones de continuidad, derivabilidad y crecimiento acotado, se cumple que $L(f'(x))=z·L(f(x)) - f(0) = sF(z) - f(0)$*

Por tanto:

$\begin{array}{l}a\left(zL(y)-y(0)\right)+bL\left(y\right)=L\left(f\left(x\right)\right);\\\left(az+b\right)L\left(y\right)=L\left(f\left(x\right)\right);\\L\left(y\right)=\frac{L\left(f\left(x\right)\right)}{az+b};\\y=L^{-1}\left(\frac{L\left(f\left(x\right)\right)}{az+b}\right)\\\end{array}.$
**Ejemplo 5: **En un circuito eléctrico que contiene una resistencia R y una [inductancia](http://es.wikipedia.org/wiki/Inductancia) L (abreviadamente, [circuito RL](http://es.wikipedia.org/wiki/Circuito_RL)) la intensidad de corriente (que es una función del tiempo t) generada al aplicar una tensión V constante viene dada por la ecuación  $RI=V-LI'$. Esta es una ecuación diferencial lineal de primer orden que está resuelta en el post [Ecuaciones diferenciales lineales de primer orden](http://tallermatematic.eu/wp/?p=897), ejemplo 5. Supongamos ahora que tenemos la condición inicial $I(0)=I_0$. Transformamos la ecuación:

$RI=V-LI'\Leftrightarrow\mathcal{L}\left(RI\right)=\mathcal{L}\left(V\right)-\mathcal{L}\left(LI'\ri
ght)\Leftrightarrow R\mathcal{L}\left(I\right)=\mathcal{L}\left(V\right)-L\mathcal{L}\left(I'\right)$

Hemos indicado la transformación de Laplace por el símbolo $\mathcal{L}$ para no confundirlo con la letra L de la inductancia. Ahora aplicamos la propiedad de la transformada de la derivada y reordenamos:

$\begin{array}{l}R\mathcal{L}\left(I\right)=\mathcal{L}\left(V\right)-L\mathcal{L}\left(I'\right)\Leftrightarrow R\mathcal{L}\left(I\right)=\mathcal{L}\left(V\right)-L\left[z\mathcal{L}\left(I\right)-I\left(0\right)\right];\\\mathcal{L}\left(I\right)\left[R+Lz\right]=LI\left(0\right)+\mathcal{L}\left(V\right);\\\mathcal{L}\left(I\right)=\frac{LI\left(0\right)+\mathcal{L}\left(V\right)}{R+Lz}\end{array}$

Consideremos ahora el segundo miembro como una fracción racional en la variable z, y tengamos en cuenta que como V es constante será $\mathcal{L}\left(V\right)=\frac Vz$  (tabla de transformadas, línea 1). Descomponemos en suma de fracciones simples:

$\begin{array}{l}\frac{LI\left(0\right)+\mathcal{L}\left(V\right)}{R+Lz}=\frac{LI\left(0\right)+V/z}{R+Lz}=\frac{zLI\left(0\right)+V}{z\left(R+Lz\right)}=\frac Az+\frac B{R+Lz}\Rightarrow\\\frac{AR+ALz+Bz}{z\left(R+Lz\right)}=\frac{zLI\left(0\right)+V}{z\left(R+Lz\right)}\Leftrightarrow\left\{\begin{array}{l}AR=V\Leftrightarrow A=V/R\\AL+B=LI\left(0\right)\Leftrightarrow B=L\left(I\left(0\right)-\frac VR\right)\end{array}\right.\end{array}$

La transformada inversa de la primera fracción simple es $\mathcal{L}^{-1}\left(\frac{V/R}z\right)=\frac VR$ (aplicamos la tabla de transformadas, línea 1). La transformada inversa de la segunda fracción simple es $\mathcal{L}^{-1}\left(\frac{L\left(I\left(0\right)-\frac VR\right)}{R+Lz}\right)=L\left(I\left(0\right)-\frac VR\right)\mathcal{L}^{-1}\left(\frac{1/L}{z-\left(-R/L\right)}\right)=\left(I\left(0\right)-\frac VR\right)e^{-\frac RLt}$, donde hemos aplicado la tabla de transformadas, línea 2, y llamamos a la variable independiente t en vez de x. Nos queda:

$I\left(t\right)=\frac VR+\left(I\left(0\right)-\frac VR\right)e^{-\frac RLt}$

Para el caso $I(0)=0$ obtenemos $I\left(t\right)=\frac VR+\left(-\frac VR\right)e^{-\frac RLt}=\frac VR\left(1-e^{-\frac RLt}\right)$ que coincide con la solución dada en [Ecuaciones diferenciales lineales de primer orden](http://tallermatematic.eu/wp/?p=897), ejemplo 5.

# Aplicación a EDOs lineales de orden superior

Para derivadas de orden superior el procedimiento es el mismo, aplicando la siguiente propiedad:
**Teorema 4**: la transformada de la derivada n-ésima viene dada por $\mathcal{L}\left(f^{(n}\right)=z^n\mathcal{L}\left(f\right)-z^{n-1}f(0)-z^{n-2}f'(0)-\dots-f^{(n-1}\left(0\right)$

**Ejemplo 6: **Resolver  la ecuación de las oscilaciones forzadas no amortiguadas de una masa conecatada con un resorte $x''+\omega_0^2x=F\sin\left(\omega t\right)$ con las condiciones iniciales $x(0)=x'(0)=0$.

Transformamos la ecuación usando la transformada de la función seno y de la derivada segunda:

$\begin{array}{l}\mathcal{L}\left(x''+\omega_0^2x\right)=\mathcal{L}\left(F\sin\left(\omega t\right)\right)\Leftrightarrow\\z^2\mathcal{L}\left(x\right)+z\cancel{x'(0)}+\cancel{x(0)}+\omega_0^2\mathcal{L}\left(x\right)=F\mathcal{L}\left(\sin\left(\omega t\right)\right)\Leftrightarrow\\\mathcal{L}\left(x\right)\left[z^2+\omega_0^2\right]=F\mathcal{L}\left(\sin\left(\omega t\right)\right)\Leftrightarrow\\\mathcal{L}\left(x\right)=\frac{F\mathcal{L}\left(\sin\left(\omega t\right)\right)}{z^2+\omega_0^2}=\frac{F{\displaystyle\frac\omega{z^2+\omega^2}}}{z^2+\omega_0^2}\Leftrightarrow\\x\left(t\right)=\mathcal{L}^{-1}\left[\frac{F\omega}{\left(z^2+\omega_0^2\right)\left(z^2+\omega^2\right)}\right]\end{array}$

Para encontrar la transformada inversa descomponemos la fracción en suma de fracciones simples:

$\begin{array}{l}\frac1{\left(z^2+\omega_0^2\right)\left(z^2+\omega^2\right)}=\frac A{z^2+\omega_0^2}+\frac B{z^2+\omega^2}=\frac{\left(A+B\right)z^2+A\omega^2+B\omega_0^2}{\left(z^2+\omega_0^2\right)\left(z^2+\omega^2\right)}\Leftrightarrow\\B=-A;\;A\left(\omega^2-\omega_0^2\right)=1\Rightarrow A=\frac1{\omega^2-\omega_0^2}\end{array}$

entonces, usando la tabla de transformadas, tenemos que el desplazamiento x(t) es:

$\begin{array}{l}x\left(t\right)=\mathcal{L}^{-1}\left[\frac{F\omega}{\left(z^2+\omega_0^2\right)\left(z^2+\omega^2\right)}\right]=\mathcal{L}^{-1}\left[\frac{F\omega}{\omega^2-\omega_0^2}\left(\frac1{z^2+\omega_0^2}-\frac1{z^2+\omega^2}\right)\right]=\\\frac{F\omega}{\omega^2-\omega_0^2}\left[\mathcal{L}^{-1}\left(\frac1{z^2+\omega_0^2}\right)-\mathcal{L}^{-1}\left(\frac1{z^2+\omega^2}\right)\right]=\\\frac{F\omega}{\omega^2-\omega_0^2}\left[\frac1{\omega_0}\sin\left(\omega_0t\right)-\frac1\omega\sin\left(\omega t\right)\right]\end{array}$
{% endraw %}