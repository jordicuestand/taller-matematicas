---
layout: post
title: "Sistemas de EDOs"
date: 2015-06-21 13:12:44 +0000
math: true
---
{% raw %}

###### 

	- Introducción

	- Reducción de sistemas a ecuaciones, y reducción del orden de un sistema

	Reducción de un sistema de ecuaciones de primer orden a una única ecuación

	- Reducción de un sistema de n ecuaciones de orden m a una única ecuación de orden n+m

	- Reducción de una EDO de orden superior a un sistema de EDOs de primer orden

	- Reducción de un sistema de EDOs de orden superior a un sistema de EDOs de primer orden

	- EDOs lineales con coeficientes constantes

	Método de operadores y determinante operacional

	- Conjunto de soluciones de un sistema de EDOs lineales

	- EDOs lineales de primer orden

	Solución general del sistema homogéneo asociado, caso de coeficientes constantes

	- Método de valores propios

	- Soluciones particulares

	- Transformada de Laplace

	- Resumen de métodos

# [![separador2](/taller-matematicas/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

# Introducción

Las EDO (Ecuaciones Diferenciales Ordinarias) son igualdades que contienen una función incógnita y=f(x), sus derivadas, y funciones F(x), G(x), ... de la variable independiente, como por ejemplo y'' - x·y' + cos(x)·y = sin(x). Frecuentemente en la práctica se presentan problemas en los que tenemos que encontrar no una función y(x) sino dos, y(x), z(x), o más de dos, de forma simultánea; en el caso de dos funciones, tenemos un sistema de dos EDO. La forma general de un sistema de EDO de primer orden, en las cuales sólo tenemos derivadas hasta el primer orden, es:

$\left.\begin{array}{r}F(x,y,z,y',z')=0\\G(x,y,z,y',z')=0\end{array}\right\}$

Por ejemplo:

$\left.\begin{array}{r}\frac{\operatorname dI_1}{\operatorname dt}+25I_1-25I_2=50\\2\frac{\operatorname dI_1}{\operatorname dt}-3\frac{\operatorname dI_2}{\operatorname dt}-5I_2=0\end{array}\right\},$

es un sistema de EDO de primer orden lineales con coeficientes constantes que aparece al resolver el problema de encontrar las intensidades $I_1, I_2$ de corriente en una red eléctrica con dos circuitos interconectados.

Si las ecuaciones del sistema no tienen las incógnitas "mezcladas", entonces podemos resolver cada ecuación del sistema por separado:

**Ejemplo 1**: para resolver el sistema $y'=y/x, z'=0$ integramos cada ecuación por separado; para la primera hacemos $dy/dx = y/x$ que es de variables separables: $dy/y = dx/x$ luego $\ln(y)=\ln(x)+C_1$ o sea $y=C_1x$. La segunda ecuación es inmediata: $z=C_2$.

En el caso general no podrá hacerse así, y necesitaremos métodos específicos para sistemas de EDOs.

# [![separador2](/taller-matematicas/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

# Reducción de sistemas a ecuaciones, y reducción del orden de un sistema

A continuación vemos algunas técnicas útiles para reducir sistemas de ecuaciones a una única ecuación de orden superior, que puede intentar resolverse con los métodos adecuados, o bien para reducir el orden de un sistema transformándolo en un sistema de primer orden.

### Reducción de un sistema de ecuaciones de primer orden a una única ecuación

En este método convertimos un sistema de dos ecuaciones en una única ecuación pero de grado superior; consiste en derivar una de las ecuaciones, obteniendo una tercera ecuación, o sea que tenemos dos incógnitas y tres ecuaciones, con lo que podemos intentar (no siempre será posible) eliminar una de las incógnitas para obtener una única ecuación, una EDO, que intentaremos resolver.

**Ejemplo 2**: En el sistema de dos funciones incógnitas y(x), z(x) siguiente: $y'=3x+y+z, z'=x-2y-z$, derivamos la primera ecuación: $y''=3+y'+z'$, y ahora intentamos eliminar z, z' usando las tres ecuaciones, como si fuera un sistema algebraico, por los métodos de igualación, sustitución y reducción:

$\begin{array}{l}\left.\begin{array}{r}y'=3x+y+z\\z'=x-2y-z\\y''=3+y'+z'\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}y'=3x+y+z\\z'=x-2y-z\\z'=y''-3-y'\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}y'+z'=4x-y\\z'=y''-3-y'\end{array}\right\}\Leftrightarrow y'+\left(y''-3-y'\right)=4x-y\Leftrightarrow\\y''+y=4x+3\end{array}$

Nos ha quedado una [EDO lineal de 2º orden](http://tallermatematic.eu/wp/?p=987) en la función y(x), cuya solución general es $y=C_1\cos(x)+C_2\sin(x)+4x+3$. Sustituyendo en la primera de las ecuaciones del sistema:

$\begin{array}{l}\begin{array}{l}\left.\begin{array}{r}y'=3x+y+z\\y=C_1\cos(x)+C_2\sin(x)+4x+3\end{array}\right\}\Leftrightarrow\\-C_1\sin(x)+C_2\cos(x)+4=3x+C_1\cos(x)+C_2\sin(x)+4x+3+z\Leftrightarrow\end{array}\\z=C_1\left(-\cos(x)-\sin(x)\right)+C_2\left(\cos(x)-\sin(x)\right)-7x+1=\\\left(C_2-C_1\right)\cos(x)-\left(C_1+C_2\right)\sin(x)-7x+1.\end{array}$

 Si el sistema es de tres ecuaciones de primer orden, que contendrá las funciones y(x), z(x), u(x) y sus derivadas y'(x), z'(x), u'(x), el método consiste en derivar dos veces una de las ecuaciones y derivar una vez las otras dos, para obtener un total de 3+2+2=7 ecuaciones, de las que intentamos eliminar dos funciones y sus derivadas, para obtener, como antes, una única ecuación de tercer orden.

### Reducción de un sistema de n ecuaciones de orden m a una única ecuación de orden n+m

El procedimiento anterior se puede generalizar a sistemas de cualquier orden.
**Ejemplo 3**: el siguiente sistema de dos ecuaciones de segundo orden,

$\left.\begin{array}{r}y''-2z'+3y=0\\z''+y'-2z=e^{2x}\end{array}\right\}$

puede reducirse a una única ecuación de orden 2 + 2 = 4 derivando la primera ecuación dos veces y una vez la segunda, y después eliminando una ecuación:

$\left.\begin{array}{r}y''-2z'+3y=0\\z''+y'-2z=e^{2x}\\y^{\left(4\right)}-2z^{\left(3\right)}+3y''=0\\z^{\left(3\right)}+y''-2z'=2e^{2x}\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}y''-2z'+3y=0\\z''+y'-2z=e^{2x}\\y^{\left(4\right)}-2z^{\left(3\right)}+3y''=0\\2z^{\left(3\right)}+2y''-4z'=4e^{2x}\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}y''-2z'+3y=0\\z''+y'-2z=e^{2x}\\y^{\left(4\right)}+5y''-4z'=4e^{2x}\end{array}\right\}$

En la última ecuación usamos la primera para eliminar z:

$\left.\begin{array}{r}-2z'=-y''-3y\\z''+y'-2z=e^{2x}\\y^{\left(4\right)}+3y''-4z'=4e^{2x}\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}\\z''+y'-2z=e^{2x}\\y^{\left(4\right)}+5y''+2\left(-y''-3y\right)=4e^{2x}\end{array}\right\}$

Vemos que la última ecuación, $y^{\left(4\right)}+5y''+2\left(-y''-3y\right)=4e^{2x}\Leftrightarrow y^{\left(4\right)}+3y''-6y=4e^{2x}$, sólo contiene la función y(x), y es lineal de coeficientes constantes de cuarto orden, que podremos resolver con los métodos de [EDOs lineales de orden superior](http://tallermatematic.eu/wp/?p=987). Una vez obtenida y(x), la sustituimos en la ecuación $z''+y'-2z=e^{2x}$ para obtener z(x).

### Reducción de una EDO de orden superior a un sistema de EDOs de primer orden

Esta transformación es útil para resolver EDOs no lineales de orden superior, ya que al transformarlas en sistemas de primer orden, quizá podamos resolverlas o  bien podremos aplicar uno de los eficientes métodos numéricos existentes
 para sistemas de EDOs de primer orden. El método és sencillo: basta con introducir nuevas variables para representar cada una de las derivadas de orden superior.

**Ejemplo 4**: Para transformar la ecuación de tercer orden $y''' + y'' + y' - 5y = cos(2x)$ definimos tres variables auxiliares $y_1=y, y_1'=y'=y_2, y_2'=y''=y_3$, las sustituimos en la ecuación, y junto con las definiciones de las variables $y_1, y_2, y_3$ nos dan un sistema de 3 ecuaciones de primer orden:

$\left.\begin{array}{r}y_3'+\;y_3\;+\;y_2\;-\;5y_1\;=\;\cos(2x)\\y_1'=y_2\\y_2'=y_3\end{array}\right\}$

### Reducción de un sistema de EDOs de orden superior a un sistema de EDOs de primer orden

Podemos aplicar el mismo método para transformar cualquier sistema de EDOs de orden n en otro sistema de EDOs de primer orden: bastará con definir, para cada función incógnita y(x), z(x), ..., tantas variables auxiliares como indique el orden de la derivada de cada ecuación, $y_1=y, y_2=y_1', y_3=y_2', ..., z_1=z, z_2=z_1', ...$. Este hecho nos dice que el estudio de sistemas de primer orden es de gran importancia, pues cualquier sistema de orden superior será reducible a primer orden.

**Ejemplo 5**: el sistema del ejemplo 3 es lineal de orden 2, para transformarlo en un sistema de cuatro ecuaciones de orden 1 es definimos las variables $y_1=y, y_2=y_1', z_1=z, z_2=z_1'$ y sustituimos:

$\left.\begin{array}{r}y''-2z'+3y=0\\z''+y'-2z=e^{2x}\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}y_2'-2z_2+3y_1=0\\z_2'+y_2-2z_1=e^{2x}\\y_2=y_1'\\z_2=z_1'\end{array}\right\}$.

# [![separador2](/taller-matematicas/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

# EDOs lineales de coeficientes constantes

Cuando aplicamos los métodos generales anteriores a sistemas lineales, se observa que las operaciones de eliminación de ecuaciones y variables produce nuevas ecuaciones lineales. Utilizando el [operador derivación D](http://tallermatematic.eu/wp/?p=1030) se puede simplificar el proceso.

**Ejemplo 6**: el sistema del ejemplo 3 era lineal; lo escribimos de nuevo usando el operador D:

$\left.\begin{array}{r}y''-2z'+3y=0\\z''+y'-2z=e^{2x}\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}\left(D^2+3\right)y-2Dz=0\\Dy+\left(D^2-2\right)z=e^{2x}\end{array}\right\}$

Ahora procedemos como en los sistemas de ecuaciones algebraicas lineales, usando los operadores D como si fueran constantes, por ejemplo, usamos el método de reducción para eliminar z, multiplicando en cruz las dos ecuaciones, para después restarlas:

$\begin{array}{l}\left.\begin{array}{r}\left(D^2+3\right)y-2Dz=0\\\mathrm{Dy}+\left(D^2-2\right)z=e^{2x}\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}\left(D^2-2\right)\left(D^2+3\right)y-2D\left(D^2-2\right)z=0\\-2D^2y-2D\left(D^2-2\right)z=-2De^{2x}\end{array}\right\}\Leftrightarrow\end{array}$

restando las ecuaciones:

$\begin{array}{l}\left.\begin{array}{r}\left(D^2+3\right)y-2Dz=0\\\mathrm{Dy}+\left(D^2-2\right)z=e^{2x}\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}\left(D^2-2\right)\left(D^2+3\right)y-2D\left(D^2-2\right)z=0\\-2D^2y-2D\left(D^2-2\right)z=-2De^{2x}\end{array}\right\}\Leftrightarrow\end{array}$

que es la misma ecuación obtenida en el ejemplo 3, pero ahora lo hemos conseguido de forma más directa.

### Método de operadores y determinante operacional

Hemos visto que gracias a la linealidad del operador D, se puede trabajar con los sistemas de EDOs lineales de coeficientes constantes casi como si fueran sistemas algebraicos. En particular, se puede aplicar un homólogo de la [regla de Cramer](http://es.wikipedia.org/wiki/Regla_de_Cramer); lo exponemos para un sistema de dos ecuaciones lineales de primer orden:

$\left.\begin{array}{r}P_1\left(D\right)y+P_2\left(D\right)z=F_1\left(x\right)\\P_3\left(D\right)y+P_4\left(D\right)z=F_2\left(x\right)\end{array}\right\}$

donde los $P_i(D)$ son polinomios en D. Entonces, se cumple que:

$\begin{array}{l}\left.\begin{array}{r}P_1\left(D\right)y+P_2\left(D\right)z=F_1\left(x\right)\\P_3\left(D\right)y+P_4\left(D\right)z=F_2\left(x\right)\end{array}\right\}\Leftrightarrow\\\begin{vmatrix}P_1\left(D\right)&amp;P_2\left(D\right)\\P_3\left(D\right)&amp;P_4\left(D\right)\end{vmatrix}y=\begin{vmatrix}F_1\left(x\right)&amp;P_2\left(D\right)\\F_2\left(x\right)&amp;P_4\left(D\right)\end{vmatrix},\\\;\begin{vmatrix}P_1\left(D\right)&amp;P_2\left(D\right)\\P_3\left(D\right)&amp;P_4\left(D\right)\end{vmatrix}z=\begin{vmatrix}P_2\left(D\right)&amp;F_1\left(x\right)\\P_4\left(D\right)&amp;F_2\left(x\right)\end{vmatrix}\end{array}$

El operador $\;\begin{vmatrix}P_1\left(D\right)&amp;P_2\left(D\right)\\P_3\left(D\right)&amp;P_4\left(D\right)\end{vmatrix}=P_1\left(D\right)\cdot P_4\left(D\right)-P_2\left(D\right)\cdot P_3\left(D\right)$ se llama determinante operacional del sistema lineal.

**Ejemplo 7**: Consideremos de nuevo el sistema del ejemplo 6, un sistema lineal de EDOs de segundo orden, tenemos que el determinante operacional es:

$\begin{array}{l}\left.\begin{array}{r}\left(D^2+3\right)y-2Dz=0\\\mathrm{Dy}+\left(D^2-2\right)z=e^{2x}\end{array}\right\}\Rightarrow\;\begin{vmatrix}P_1\left(D\right)&amp;P_2\left(D\right)\\P_3\left(D\right)&amp;P_4\left(D\right)\end{vmatrix}=\;\begin{vmatrix}D^2+3&amp;-2D\\D&amp;D^2-2\end{vmatrix}=\\D^4+3D^2-2D^2-6+2D^2=D^4+3D^2-6\end{array}$

Entonces:

$\left(D^4+3D^2-6\right)y=\begin{vmatrix}0&amp;-2D\\e^{2x}&amp;D^2-2\end{vmatrix}=0+2De^{2x}=4e^{2x}$

y para la función z(x):

$\left(D^4+3D^2-6\right)z=\begin{vmatrix}D^2+3&amp;0\\D&amp;e^{2x}\end{vmatrix}=\left(D^2+3\right)e^{2x}-0=7e^{2x}$

que es equivalente a las ecuaciones:

$\begin{array}{l}\left(D^4+3D^2-6\right)y=4e^{2x}\Leftrightarrow y=\frac1{D^4+3D^2-6}4e^{2x}\\\;\left(D^4+3D^2-6\right)z=7e^{2x}\Leftrightarrow z=\frac1{D^4+3D^2-6}7e^{2x}\end{array}$

que se resuelven con los [métodos del operador D para EDOs lineales](http://tallermatematic.eu/wp/?p=1030).

### Conjunto de soluciones de un sistema de EDOs lineales

Un sistema de n ecuaciones lineales homogéneas de primer orden con n funciones incógnitas tendrá también n soluciones linealmente independientes.

**Ejemplo 8**: El sistema lineal homogéneo de primer orden con coeficientes constantes $y'=4y-3z, z'=6y-7z$ puede resolverse aplicando el método de derivar la 1ª ecuación y eliminar una variable usando las tres ecuaciones resultantes:

$\begin{array}{l}\left.\begin{array}{r}y'=4y-3z\\z'=6y-7z\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}7y'-28y+21z=0\\y''-4y'+3z'=0\\3z'-18y+21z=0\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}7y'-3z'-10y=0\\y''-4y'+3z'=0\end{array}\right\}\Leftrightarrow\\y''-4y'+\left(7y'-10y\right)=0\Leftrightarrow y''+3y'-10y=0\end{array}$

La ecuación homogénea de segundo orden en y es inmediata: la ecuación característica es $r^2+3r-10=0\Rightarrow r=2,\;-5$ y la solución general $y=C_1e^{2x}+C_2e^{-5x}$. Para la otra función z(x), sustituimos la función y(x) en la primera ecuación:

$\begin{array}{l}y=C_1e^{2x}+C_2e^{-5x}\Rightarrow y'=2C_1e^{2x}-5C_2e^{-5x};\\y'=4y-3z\Rightarrow2C_1e^{2x}-5C_2e^{-5x}=4\left(C_1e^{2x}+C_2e^{-5x}\right)-3z\Rightarrow\\z=\frac23C_1e^{
2x}+3C_2e^{-5x}\end{array}$.

El sistema se puede expresar matricialmente en la forma DY=AY:

$D\begin{pmatrix}y\\z\end{pmatrix}=\begin{pmatrix}4&amp;-3\\6&amp;-7\end{pmatrix}\begin{pmatrix}y\\z\end{pmatrix}$

y también la solución obtenida en la forma Y=CX, donde X es el vector que contiene a las funciones linealmente independientes:

$\begin{pmatrix}y\\z\end{pmatrix}=\begin{pmatrix}C_1&amp;C_2\\\frac23C_1&amp;3C_2\end{pmatrix}\begin{pmatrix}e^{2x}\\e^{-5x}\end{pmatrix}$

Recordemos que para asegurar que dos funciones son linealmente independientes podemos calcular su Wronskiano, que debe ser distinto de cero:

$W\begin{pmatrix}e^{2x}\\e^{-5x}\end{pmatrix}=det\begin{pmatrix}e^{2x}&amp;e^{-5x}\\2e^{2x}&amp;-5e^{-5x}\end{pmatrix}=-5e^{2x}e^{-5x}-2e^{2x}e^{-5x}=-7e^{-3x}\neq0$,

pero en el caso de los sistemas homogéneos lineales de coeficientes constantes, como el de este ejemplo, la comprobación no es necesaria, siempre obtendremos soluciones linealmente independientes.

# [![separador2](/taller-matematicas/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

# EDOs lineales de primer orden con coeficientes variables

En este apartado vemos métodos de resolución de sistemas de EDO de primer orden con n funciones incógnitas $y_1,y_2,...,y_n$ y coeficientes variables, o sea, funciones de x que supondremos continuas; es conveniente usar la notación matricial en vez de denominar a las funciones incógnitas y(x), z(x), etc. El sistema que consideramos es:

$\left.\begin{array}{r}y_1'=a_{11}\left(x\right)y_1+\dots+a_{1n}\left(x\right)y_n+F_1\left(x\right)\\\vdots\\y_n'=a_{n1}\left(x\right)y_1+\dots+a_{nn}\left(x\right)y_n+F_n\left(x\right)\end{array}\right\}$

que puede escribirse en forma matricial como sigue:

$\begin{pmatrix}y_1'\\\vdots\\y_n'\end{pmatrix}=\begin{pmatrix}a_{11}\left(x\right)&amp;\dots&amp;a_{1n}\left(x\right)\\\vdots&amp;\vdots&amp;\vdots\\a_{n1}\left(x\right)&amp;\dots&amp;a_{nn}\left(x\right)\end{pmatrix}\begin{pmatrix}y_1\\\vdots\\y_n\end{pmatrix}+\begin{pmatrix}F_1\left(x\right)\\\vdots\\F_n\left(x\right)\end{pmatrix}$

o más conciso: $Y'=AY+F$, donde las funciones Y(x), F(x) son funciones vectoriales, esto es, toman un real x como parámetro y devuelven un vector de n componentes:
$Y(x)=\begin{pmatrix}y_1\left(x\right)\\\vdots\\y_n\left(x\right)\end{pmatrix},\;F(x)=\begin{pmatrix}F_1\left(x\right)\\\vdots\\F_n\left(x\right)\end{pmatrix}$

De la misma forma que para EDOs lineales, la solución general del sistema puede expresarse como la suma de la solución general del sistema homogéneo asociado $Y'=AY$ más una solución particular cualquiera del sistema completo $Y'=AY+F$ (principio de superposición). Hemos visto que, para un sistema de n ecuaciones de primer grado, obtendremos n vectores. En forma vectorial, podemos expresarlo como n vectores de n componentes:

$Y_1=\begin{pmatrix}y_{11}\\\vdots\\y_{1n}\end{pmatrix},\;Y_2=\begin{pmatrix}y_{21}\\\vdots\\y_{2n}\end{pmatrix},\dots,Y_n=\begin{pmatrix}y_{n1}\\\vdots\\y_{nn}\end{pmatrix},$

Si tenemos n funciones vectoriales linealmente independientes $Y_1, Y_2, ..., Y_n$ que son todas ellas solución del sistema homogéneo, entonces la solución general será la combinación lineal

$C_1Y_1+C_2Y_2+\dots+C_nY_n=C_1\begin{pmatrix}y_{11}\\\vdots\\y_{1n}\end{pmatrix}+C_2\begin{pmatrix}y_{21}\\\vdots\\y_{2n}\end{pmatrix}+\dots+C_n\begin{pmatrix}y_{n1}\\\vdots\\y_{nn}\end{pmatrix}$

### Solución general del sistema homogéneo asociado, caso de coeficientes constantes

En la sección "Método de operadores y determinante operacional" hemos visto que se pueden encontrar las soluciones de un sistema lineal de coeficientes constantes resolviendo una ecuación diferencial para cada incógnita, ecuación que, para un sistema de dos ecuaciones, es de la forma:

$\begin{vmatrix}P_1\left(D\right)&amp;P_2\left(D\right)\\P_3\left(D\right)&amp;P_4\left(D\right)\end{vmatrix}y=\begin{vmatrix}F_1\left(x\right)&amp;P_2\left(D\right)\\F_2\left(x\right)&amp;P_4\left(D\right)\end{vmatrix}$

si el sistema es homogéneo, entonces:

$\begin{vmatrix}P_1\left(D\right)&amp;P_2\left(D\right)\\P_3\left(D\right)&amp;P_4\left(D\right)\end{vmatrix}y=\begin{vmatrix}0&amp;P_2\left(D\right)\\0&amp;P_4\left(D\right)\end{vmatrix}=0$
y resulta una ecuación lineal también homogénea para y: $\left(P_1\left(D\right)P_4\left(D\right)-P_2\left(D\right)P_3\left(D\right)\right)y=0.$ Es sabido (ver por ejemplo [EDOs lineales de orden superior](http://tallermatematic.eu/wp/?p=987)) que las soluciones de las ecuación lineales  homogéneas de coeficientes constantes son siempre del tipo $Ce^{rx}$, por tanto se puede probar directamente con funciones de este tipo, sustituyendo en el sistema. Además, las ecuaciones que resultan para las otras incógnitas son las mismas, para z(x) será:

$\begin{vmatrix}P_1\left(D\right)&amp;P_2\left(D\right)\\P_3\left(D\right)&amp;P_4\left(D\right)\end{vmatrix}z=\begin{vmatrix}P_1\left(D\right)&amp;0\\P_3\left(D\right)&amp;0\end{vmatrix}=0\Leftrightarrow\left(P_1\left(D\right)P_4\left(D\right)-P_2\left(D\right)P_3\left(D\right)\right)z=0$

Así pues, ensayamos la misma función $e^{rx}$ para todas las incógnitas, sólo puede cambiar la constante: $y=C_1e^{rx}, z=C_2e^{rx}, ...$

**Ejemplo 9**: Para el sistema del ejemplo 8 podemos ensayar soluciones $y=C_1e^{rx}, z=C_2e^{rx}$, que sustituidas en el sistema original dan:

$\begin{array}{l}y=C_1e^{rx},\;z=C_2e^{rx}\Rightarrow y'=C_1re^{rx},\;z'=C_{2r}e^{rx};\\\left.\begin{array}{r}y'=4y-3z\\z'=6y-7z\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}C_1re^{rx}=4C_1e^{rx}-3C_2e^{rx}\\C_{2}re^{rx}=6C_1e^{rx}-7C_2e^{rx}\end{array}\right\}\end{array}$

eliminando el factor común $e^{rx}$ queda un sistema lineal algebraico:

$\left.\begin{array}{r}rC_1=4C_1-3C_2\\rC_2=6C_1-7C_2\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}\left(4-r\right)C_1-3C_2=0\\6C_1+\left(-7-r\right)C_2=0\end{array}\right\}$

En general, para un sistema homogéneo cualquiera de dos ecuaciones de orden 1 con coeficientes constantes, obtendremos un sistema algebraico para determinar las constantes $C_1, C_2$ tal como:

$\left.\begin{array}{r}y'=a_{11}y+a_{12}z\\z'=a_{21}y+a_{22}z\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}\left(a_{11}-r\right)C_1+a_{12}C_2=0\\a_{21}C_1+\left(a_{22}-r\right)C_2=0\end{array}\right\}$

Este sistema lineal, al ser homogéneo, sólo tendrá solución distinta de $C_1=C_2=0$ si su determinante asociado es cero:

$\begin{vmatrix}a_{11}-r&amp;a_{12}\\a_{21}&amp;a_{22}-r\end{vmatrix}=0\Leftrightarrow\left(a_{11}-r\right)\left(a_{22}-r\right)-a_{12}a_{21}=0\Leftrightarrow r^2-r\left(a_{11}+a_{22}\right)-a_{12}a_{21}=0$

Si esta ecuación de segundo grado tiene dos soluciones $r_1, r_2$, entonces nos proporciona dos parejas de soluciones:

$\begin{array}{l}y_1=C_1e^{r_1x},\;z_1=C_2e^{r_1x};\;y_2=C_1e^{r_2x},\;z_2=C_2e^{r_2x}\\Y=\begin{pmatrix}y_1\\y_2\end{pmatrix}=C_1\begin{pmatrix}e^{r_1x}\\e^{r_2x}\end{pmatrix},\;Z=\begin{pmatrix}z_1\\z_2\end{pmatrix}=C_2\begin{pmatrix}e^{r_1x}\\e^{r_2x}\end{pmatrix}\end{array}$

la solución general del sistema homogéneo será la combinación lineal de las parejas de soluciones:

$\begin{array}{l}y=A_1\cdot C_1y_1+B_1\cdot C_1y_2=A_1C_1e^{r_1x}+B_1C_1e^{r_2x}\\z=A_2\cdot C_2z_1+B_2\cdot C_2z_2=A_2C_2e^{r_1x}+B_2C_2e^{r_2x}\end{array}$

**Ejemplo 10**: el determinante del sistema lineal del ejemplo 8, y sus raíces, son:

$\begin{vmatrix}4-r&amp;-3\\6&amp;-7-r\end{vmatrix}=r^2-10+3r=0\Leftrightarrow r=2,-5$

para la primera raíz, el sistema algebraico que determina las constantes de integración es:

$\left.\begin{array}{r}\left(a_{11}-r\right)C_1+a_{12}C_2=0\\a_{21}C_1+\left(a_{22}-r\right)C_2=0\end{array}\right\}=\left.\begin{array}{r}\left(4-2\right)C_1-3C_2=0\\6C_1+\left(-7-2\right)C_2=0\end{array}\right\}=\left.\begin{array}{r}2C_1-3C_2=0\\6C_1-9C_2=0\end{array}\right\}$

sistema indeterminado que nos proporciona la relación $C_2=C_1·2/3$, y por tanto una pareja de soluciones es $y=C_1e^{2x},\;z=(2/3)C_1e^{2x}$. Usando la segunda raíz $r=-5$ del mismo modo, obtenemos la relación $C_2=3C_1$ y la segunda pareja de soluciones es $y=C_2e^{-5x},\;z=3C_2e^{-5x}.$

# [![separador2](/taller-matematicas/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

###  Método de valores propios

En este apartado usaremos algunos conceptos básicos del Álgebra lineal: vectores, espacio vectorial, independencia lineal, base de un espacio vectorial, valores y vectores propios de una matriz.

El determinante que hemos usado en el apartado anterior para encontrar las raíces r que determinan los exponentes $e^{rx}$ es formalmente idéntico al usado en Álgebra Lineal para encontrar los [valores propios de una matriz A](http://es.wikipedia.org/wiki/Vector_propio_y_valor_propio):

$A=\begin{pmatrix}a_{11}&amp;a_{12}\\a_{21}&amp;a_{22}\end{pmatrix}\Leftrightarrow\begin{vmatrix}a_{11}-r&amp;a_{12}\\a_{21}&amp;a_{22}-r\end{vmatrix}=0$

Esto no es casualidad; si escribimos el sistema homogéneo en forma matricial,

$Y'=AY=\begin{pmatrix}a_{11}&amp;a_{12}\\a_{21}&amp;a_{22}\end{pmatrix}Y$
y ensayamos soluciones de la forma $Y=Ve^{rx}$ siendo V un vector constante, tenemos: $Vre^{rx}=AVe^{rx}\Leftrightarrow AV=rV$, que en el lenguaje del Álgebra Lineal significa que el vector V es un vector propio de la matriz A, con valor propio r. Entonces podemos aplicar el sistema siguiente para resolver el sistema homogéneo:

	- encontrar los n valores propios r de la matriz del sistema lineal A

	- encontrar un sistema de n vectores V, linealmente independientes, asociados a los valores propios r

	- formar la solución general: $Y=C_1V_1e^{r_1x}+C_2V_2e^{r_2x}+\dots+C_nV_2e^{r_nx}$

Quizá el lector habrá notado que, en las secciones anteriores, no hemos tratado el caso de tener raíces dobles (o triples, o en general de multiplicidad mayor que 1), ni de tener raíces complejas, en la resolución del sistema lineal asociado; hemos dejado este tema para resolverlo ahora, usando el método de valores propios. No obstante, sólo lo trataremos superficialmente pues necesitaríamos más material de Álgebra Lineal, concretamente para el punto 2, sobre cómo obtener un sistema de n vectores V linealmente independientes asociados a los valores propios r.

**Ejemplo 11**: Resolver el sistema lineal homogéneo siguiente, de tres funciones y(x), z(x), u(x),  usando el método de los valores propios:

$\left.\begin{array}{r}y'=-6y-3z+14u\\z'=4y+3z-8u\\u'=-2y-z+5u\end{array}\right\}$

Paso 1: La matriz del sistema, y el determinante que proporciona los valores propios, son:

$A=\begin{pmatrix}-6&amp;-3&amp;14\\4&amp;3&amp;-8\\-2&amp;-1&amp;5\end{pmatrix};\;\text{det }\left(A-rI\right)=\begin{vmatrix}-6-r&amp;-3&amp;14\\4&amp;3-r&amp;-8\\-2&amp;-1&amp;5-r\end{vmatrix}=r^3-2r^2-r+2$

Resolvemos la ecuación $det(A-rI)=0$ igualando el polinomio a cero y aplicando el método de Ruffini; obtenemos $r=1, -1, 2$.

Paso 2: Planteamos un sistema lineal $(A-rI)v=0$ para cada valor de r.

Para r=1 planteamos el sistema (A-I)V=0 y lo resolvemos (no damos los detalles):

 $\left(A-I\right)V=\begin{pmatrix}-7&amp;-3&amp;14\\4&amp;3&amp;-9\\-2&amp;-1&amp;4\end{pmatrix}\begin{pmatrix}v_1\\v_2\\v_3\end{pmatrix}=0\Rightarrow v_1=2v_3,\;v_2=0$

luego podemos hacer, por ejemplo, V=(2, 0, 1). Los otros dos sistemas y sus soluciones son:

$\begin{array}{l}\left(A+I\right)V=\begin{pmatrix}-5&amp;-3&amp;14\\4&amp;4&amp;-8\\-2&amp;-1&amp;6\end{pmatrix}\begin{pmatrix}v_1\\v_2\\v_3\end{pmatrix}=0\Rightarrow v_1=4v_3,\;v_2=-2v_3;\\\left(A-2I\right)V=\begin{pmatrix}-8&amp;-3&amp;14\\4&amp;1&amp;-8\\-2&amp;-1&amp;3\end{pmatrix}\begin{pmatrix}v_1\\v_2\\v_3\end{pmatrix}=0\Rightarrow v_1=\frac52v_3,\;v_2=-2v_3\end{array}$

Tomamos como vectores solución (4, -2, 1) y (5, -4, 2). Entonces la solución general del sistema es la combinación lineal de les vectores multiplicados por  los factores $e^{x}, e^{-x}, e^{2x}$ respectivamente:

$\begin{pmatrix}y\\z\\w\end{pmatrix}=C_1\begin{pmatrix}2\\0\\1\end{pmatrix}e^x+C_2\begin{pmatrix}4\\-2\\1\end{pmatrix}e^{-x}+C_2\begin{pmatrix}5\\-4\\2\end{pmatrix}e^{2x},$

que equivale, sin usar vectores, a:

$\begin{array}{l}y\left(x\right)=2C_1e^x+4C_2e^{-x}+5C_3e^{2x}\\z\left(x\right)=-2C_2e^{-x}-4C_3e^{2x}\\u\left(x\right)=C_1e^x+C_2e^{-x}+2C_3e^{2x}\end{array}$

 **Ejemplo 12**: Resolver el sistema $y_1'=3y_1+y_2,\;y_2'=-y_1+y_2,\;y_3'=y_1+y_2+2y_3$ usando el método de los valores propios.

La matriz del sistema, y el determinante que proporciona los valores propios, son:

$\begin{array}{l}A=\begin{pmatrix}3&amp;1&amp;0\\-1&amp;1&amp;0\\1&amp;1&amp;2\end{pmatrix};\;\text{det}\;\left(A-rI\right)=\begin{vmatrix}3-r&amp;1&amp;0\\-1&amp;1-r&amp;0\\1&amp;1&amp;2-r\end{vmatrix}=\left(2-r\right)\begin{vmatrix}3-r&amp;1\\-1&amp;1-r\end{vmatrix}=\\\left(2-r\right)\left[\left(3-r\right)\left(1-r\right)+1\right]=-\left(r-2\right)^3=0\Rightarrow r=2\end{array}$

Hay un único valor propio, r=2, con multiplicidad triple; esto significa que el método del ejemplo anterior no proporcionará todas las tres soluciones. Restando este valor a la diagonal de la matriz A y planteando el sistema (A-2I)V=0 obtenemos:

$\begin{pmatrix}1&amp;1&amp;0\\-1&amp;-1&amp;0\\1&amp;1&amp;0\end{pmatrix}V=\begin{pmatrix}0\\0\\0\end{pmatrix}\Leftrightarrow v_1+v_2=0$

con el tercer componente del vector V indeterminado; por ejemplo, el vector $V_1=(1, -1, 0)$ cumple el sistema, y es un vector propio asociado al valor propio r=2. Otro vector que cumple con el sistema planteado, y que además es linealmente independiente del primero, es $V_2=(1, -1, 1)$. En el lenguaje algebraico, decimos que los vectores ${V_1, V_2}$ son una base del núcleo de la aplicación lineal con matriz A-2I; como el rango de la matriz A-2I es 1 (sólo hay una de sus filas linealmente independiente), por un teorema del Álgebra Lineal resulta que no existe ningún otro vector $V_3$ linealmente independiente de ${V_1, V_2}$ tal que $(A-2I)V_3=0$: los vectores $V_1,V_2$ forman una base del subespacio vectorial $(A-2I)V=0$. Por el momento, la solución que hemos encontrado es $Y=C_1V_1e^{2x}+C_2V_2e^{2x}$, pero siendo un sistema de tres ecuaciones diferenciales, esperamos que la solución general contenga la combinación de tres funciones. ¿Cómo encontramos la tercera función?

Una forma de intentarlo es ensayar una solución similar a las obtenidas, pero multiplicando por la variable x, concretamente de esta forma: $Y=Vxe^{2x}+We^{2x}$, siendo V, W vectores constantes a determinar. Sustituimos esta tentativa de solución en la ecuación matricial del sistema Y'=AY, simplificamos, y obtenemos dos ecuaciones vectoriales:

$\begin{array}{l}Y'=AY\Leftrightarrow Ve^{2x}\left(1+2x\right)+2We^{2x}=A\left(Vxe^{2x}+We^{2x}\right);\\\left.\begin{array}{r}AVxe^{2x}-Ve^{2x}2x=0\\AWe^{2x}-2We^{2x}=Ve^{2x}\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}AV-V\cdot2=0\\AW-2W=V\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}\left(A-2I\right)V=0\\\left(A-2I\right)W=V\end{array}\right\}\end{array}$

donde I simboliza la matriz identidad, con unos en la diagonal y ceros fuera de ella. La primera ecuación ya está resuelta: sus soluciones son los vectores $V_1, V_2$ y sus combinaciones lineales, o sea que cualquier vector V que cumpla $\left(A-2I\right)V=0$ ha de ser de la forma $V=c_1V_1+c_2V_2$. Para la segunda ecuación con el vector W, planteamos: $\left(A-2I\right)W=V\Leftrightarrow\left(A-2I\right)V=\left(A-2I\right)^2W=0$.
 Calculamos la matriz $(A-2I)^2$ que resulta ser la matriz nula:

$\left(A-2I\right)\cdot\left(A-2I\right)=\begin{pmatrix}1&amp;1&amp;0\\-1&amp;-1&amp;0\\1&amp;1&amp;0\end{pmatrix}\cdot\begin{pmatrix}1&amp;1&amp;0\\-1&amp;-1&amp;0\\1&amp;1&amp;0\end{pmatrix}=\begin{pmatrix}0&amp;0&amp;0\\0&amp;0&amp;0\\0&amp;0&amp;0\end{pmatrix}$

por tanto la ecuación $\left(A-2I\right)^2W=0$ se cumple para todo vector W. Planteamos ahora $\left(A-2I\right)W=V=c_1V_1+c_2V_2$, que nos da:

$\begin{pmatrix}1&amp;1&amp;0\\-1&amp;-1&amp;0\\1&amp;1&amp;0\end{pmatrix}\cdot\begin{pmatrix}w_1\\w_2\\w_3\end{pmatrix}=c_1\begin{pmatrix}1\\-1\\0\end{pmatrix}+c_2\begin{pmatrix}1\\-1\\1\end{pmatrix}\Rightarrow\begin{pmatrix}w_1+w_2\\-w_1-w_2\\w_1+w_2\end{pmatrix}=\begin{pmatrix}c_1+c_2\\-c_1-c_2\\c_2\end{pmatrix}$

se deduce que debe de ser $c_1=0$ y por tanto $V=c_2V_2$; cogemos por ejemplo $c_2=1$, y $V=V_2$, cogemos además $W=(1,0,0)$ (comprobad que este vector satisface las condiciones) Entonces la tercera solución linealmente independiente del sistema es:

$Y_3=Vxe^{2x}+We^{2x}=\left(V_2x+W\right)e^{2x}=\left[\begin{pmatrix}1\\-1\\1\end{pmatrix}x+\begin{pmatrix}1\\0\\0\end{pmatrix}\right]e^{2x}=\begin{pmatrix}x+1\\-x\\1\end{pmatrix}e^{2x}$

y la solución general del sistema es:

$\begin{array}{l}Y=C_1V_1e^{2x}+C_2V_2e^{2x}+C_3\left(V_2x+W\right)e^{2x}=\\C_1\begin{pmatrix}1\\-1\\0\end{pmatrix}e^{2x}+C_2\begin{pmatrix}1\\-1\\1\end{pmatrix}e^{2x}+C_3\begin{pmatrix}x+1\\-x\\1\end{pmatrix}e^{2x}\end{array}$

# [![separador2](/taller-matematicas/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

###  Soluciones particulares

Para encontrar una solución particular de un sistema lineal de primer orden se pueden generalizar los métodos usados en[ EDOs lineales de primer orden](http://tallermatematic.eu/wp/?p=897): los métodos de coeficientes indeterminados y variación de constantes. Aquí sólo emplearemos el primero.

**Método de coeficientes indeterminados  para sistemas de EDOs lineales de 1r orden con coef. constantes**

Dado el sistema $F(y,y')=f(x)$ donde F y f simbolizan vectores, este método para encontrar una solución particular $y_p$ es efectivo cuando el término $f(x)$ es un polinomio en x, o bien una exponencial $e^{rx}$, o bien una función $sin(kx)$ o $cos(kx)$, o bien es una suma de esas funciones. El método consiste en ensayar como solución una combinación lineal parecida a $f(x)$:

	- si $f(x)$ es un polinomio de grado n, ensayamos para $y_p$ un polinomio del mismo grado y coeficientes indeterminados

	- si $f(x)=pe^{qx}$, ensayamos para $y_p$ una función $y_p=Ae^{Bx}$

	- si $f(x)=sin(kx)$ , ensayamos para $y_p$ una función $y_p=Asin(kx)+Bcos(kx)$

	- si $f(x)$ es una suma  de los tipos anteriores, aplicamos la proposición 1 (superposición): encontraremos soluciones particulares para cada tipo por separado, la solución buscada será la suma de las anteriores.

**Ejemplo 12**: Encontrar una solución particualr del sistema lineal de 1r orden usando el método de coeficientes indeterminados:

$\left.\begin{array}{r}y'=4y-3z+e^x\\z'=6y-7z+x^2\end{array}\right\}$

Viendo que el sistema es de coeficientes constantes y que el término $F(x)$ es el vector $\begin{pmatrix}e^x\\x^2\end{pmatrix}$ ensayamos una solución particular que sea una combinación lineal de esas dos funciones:

$\begin{pmatrix}y_p\\z_p\end{pmatrix}=\begin{pmatrix}Ae^x+Bx^2+Cx+D\\Ee^x+Fx^2+Gx+H\end{pmatrix}$

Derivando:

$\begin{pmatrix}y'_p\\z'_p\end{pmatrix}=\begin{pmatrix}Ae^x+Bx+C\\Ee^x+Fx+G\end{pmatrix}\Rightarrow$

sustituimos en el sistema:

$\begin{pmatrix}Ae^x+Bx+C\\Ee^x+Fx+G\end{pmatrix}=\begin{pmatrix}4\left(Ae^x+Bx^2+Cx+D\right)-3\left(\mathrm{Ee}^x+Fx^2+Gx+H\right)+e^x\\6\left(Ae^x+Bx^2+Cx+D\right)-7\left(\mathrm{Ee}^x+Fx^2+Gx+H\right)+x^2\end{pmatrix}$

Agrupamos los coeficientes según si afectan a las funciones $e^x,x^2,x$ y coeficientes constantes, para obtener un sistema de ocho ecuaciones lineales con las incógnitas A,B,C,D,E,F,G,H;

$\begin{array}{l}Ae^x=4e^x-3e^x+e^x\Rightarrow A=4-3+1=3;\\0=4Bx^2-3Fx^2\Rightarrow0=4B-3F;\\2Bx=4Cx-3Hx\Rightarrow2B=4C-3H;\\C=4D-3H;\\\dots\end{array}$

Resolviendo el sistema obtenemos: A=3, B=3/10, C=9/50, D=57/100, E=9/4, F=2/5, G=1/25, H=23/250, por tanto la solución particular buscada es:

$\begin{pmatrix}y_p\\z_p\end{pmatrix}=\begin{pmatrix}Ae^x+Bx^2+Cx+D\\Ee^x+Fx^2+Gx+H\end{pmatrix}=\begin{pmatrix}3e^x+\frac34x^2+\frac9{50}x+\frac{57}{100}\\\frac94e^x+\frac25x^2+\frac1{25}x+\frac{23}{250}\end{pmatrix}.$

# [![separador2](/taller-matematicas/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

### Método de la transformada de Laplace

Cuando tengamos que resolver un sistema de EDO lineales de cualquier orden con coeficientes constantes y condiciones iniciales, el método de la transformada de Laplace lo transforma en un sistema de ecuaciones lineales, no hay necesidad de resolver primero el sistema homogéneo y después encontrar una solución particular, y por tanto puede ser ventajoso usarlo en esas condiciones. La técnica es la misma que la explicada para EDO en el post [Transformada de Laplace](http://tallermatematic.eu/wp/?p=1075).

**Ejemplo 13**:

Resolver el sistema lineal de segundo orden

$\left.\begin{array}{r}2y''=-6y'+2z\\z''=2y-2z+40\sin\left(3x\right)\end{array}\right\}$

con las condiciones iniciales $y(0)=y'(0)=z(0)=z'(0)=0$ usando la transformada de Laplace.

Definimos: $Y=\mathcal{L}\left(y\right),\;Z=\mathcal{L}\left(z\right)$, y por las propiedades de la transformada de Laplace:

$\begin{array}{l}\mathcal{L}\left(y'\right)=sY-y(0)\;=sY;\;\\\mathcal{L}\left(y''\right)=s\mathcal{L}\left(y'\right)-y'(0)=s^2Y-y(0)-y'(0)=s^2Y\end{array}$

y de la misma forma para z: $\mathcal{L}\left(z''\right)=s^2Z-z(0)-z'(0)=s^2Z$. Usamos también la propiedad

$L(\sin\left(ax\right))=\frac a{z^2+a^2}\;\text{para }z>0$

Sustituimos estas expresiones en el sistema de EDOs para obtener un sistema lineal de ecuaciones algebraicas:

$\left.\begin{array}{r}2s^2Y=-6Y+2Z\\s^2Z=2Y-2Z+40\frac3{s^2+9}\end{array}\right\}\Leftrightarrow\left.\begin{array}{r}\left(s^2+3\right)Y-Z=0\\-2Y+\left(s^2+2\right)Z=\frac{120}{s^2+9}\end{array}\right\}$

Lo resolvemos por reducción:

$\left.\begin{array}{r}-2\left(s^2+3\right)Y+2Z=0\\-2\left(s^2+3\right)Y+\left(s^2+3\right)\left(s^2+2\right)Z=\left(s^2+3\right)\frac{120}{s^2+9}\end{array}\right\}\Leftrightarrow\left[\left(s^2+3\right)\left(s^2+2\right)-2\right]Z=\left(s^2+3\right)\frac{120}{s^2+9}$

y para la otra variable:

$\left.\begin{array}{r}\left(s^2+2\right)\left(s^2+3\right)Y-\left(s^2+2\right)Z=0\\-2Y+\left(s^2+2\right)Z=\frac{120}{s^2+9}\end{array}\right\}\Leftrightarrow\left[\left(s^2+2\right)\left(s^2+3\right)-2\right]Y=\frac{120}{s^2+9}$

despejamos las incógnitas Y, Z:

$Z=\frac{120\left(s^2+3\right)}{\left(s^2+9\right)\left[\left(s^2+3\right)\left(s^2+2\right)-2\right]},\;Y=\frac{120}{\left(s^2+9\right)\left[\left(s^2+2\right)\left(s^2+3\right)-2\right]}$

Ahora aplicamos la transformada inversa para obtener $y=\mathcal{L}^{-1}(Y),\;z=\mathcal{L}^{-1}(Z)$, primero arreglamos un poco las ecuaciones completando los cuadrados: planteamos $\left(s^2+2\right)\left(s^2+3\right)-2=\left(s^2+A\right)\left(s^2+B\right)\Leftrightarrow A=1,B=4$,  entonces queda:

$z=\mathcal{L}^{-1}\left\{\frac{120\left(s^2+3\right)}{\left(s^2+9\right)\left[\left(s^2+1\right)\left(s^2+4\right)\right]}\right\},\;y=\mathcal{L}^{-1}\left\{\frac{120}{\left(s^2+9\right)\left[\left(s^2+1\right)\left(s^2+4\right)\right]}\right\}$

El siguiente paso es  descomponer las fracciones en suma de fracciones simples; para la fracción asociada a la función y(x) planteamos:

$\frac{120}{\left(s^2+9\right)\left[\left(s^2+1\right)\left(s^2+4\right)\right]}=120\left[\frac{As+\widetilde A}{s^2+9}+\frac{Bs+\widetilde B}{s^2+1}+\frac{Cs+\widetilde C}{s^2+4}\right]$,

donde $A,\widetilde A,B,\widetilde B, C,\widetilde C$ son contantes a determinar; operando obtenemos:

$\left(As+\widetilde A\right)\left(s^2+1\right)\left(s^2+4\right)+\left(Bs+\widetilde B\right)\left(s^2+9\right)\left(s^2+4\right)+\left(Cs+\widetilde C\right)\left(s^2+9\right)\left(s^2+1\right)=1$,

usando las raíces del denominador,  que son los números imaginarios s=i, 2i, 3i, para simplificar la expresión:

$s=i\Rightarrow\left(Ai+\widetilde A\right)\cancel{\left(-1+1\right)}\left(-1+4\right)+\left(Bi+\widetilde B\right)\left(-1+9\right)\left(-1+4\right)+\left(Ci+\widetilde C\right)\left(-1+9\right)\cancel{\left(-1+1\right)}=1\Rightarrow B=0,\widetilde B=1$,

etc. De esta forma procederemos con los otros coeficientes. Dejando los detalles, obtenemos:

$\begin{array}{l}z=\mathcal{L}^{-1}\left\{\frac{120\left(s^2+3\right)}{\left(s^2+9\right)\left[\left(s^2+1\right)\left(s^2+4\right)\right]}\right\}=\;\mathcal{L}^{-1}\left\{\frac{10}{s^2+9}+\frac8{s^2+1}+\frac{18}{s^2+4}\right\}\\y=\mathcal{L}^{-1}\left\{\frac{120}{\left(s^2+9\right)\left[\left(s^2+1\right)\left(s^2+4\right)\right]}\right\}=\mathcal{L}^{-1}\left\{\frac5{s^2+9}-\frac8{s^2+1}+\frac3{s^2+4}\right\}\end{array}$.

Para calcular las transformadas inversas usamos una tabla de transformadas, o bien recordando que la transformada de Laplace es lineal y usando la propiedad

$L(\sin\left(ax\right))=\frac a{z^2+a^2}\;\text{para }z>0$

obtenemos $\mathcal{L}^{-1}\left\{\frac a{z^2+a^2}\right\}=\sin\left(ax\right)\Leftrightarrow\mathcal{L}^{-1}\left\{\frac1{z^2+a^2}\right\}=\frac1a\sin\left(ax\right)$, por tanto:

$\begin{array}{l}z=\;\mathcal{L}^{-1}\left\{\frac{-18}{s^2+9}+\frac{10}{s^2+1}+\frac8{s^2+4}\right\}=-6\sin\left(3x\right)+10\sin\left(x\right)+4\sin\left(2x\right);\\y=\mathcal{L}^{-1}\left\{\frac3{s^2+9}+\frac5{s^2+1}-\frac8{s^2+4}\right\}=\sin\left(3x\right)+5\sin\left(x\right)-4\sin\left(2x\right)\end{array}$

es la solución particular del sistema tal que cumple las condiciones iniciales dadas.

# [![separador2](/taller-matematicas/assets/images/separador2-300x37.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

# Resumen de métodos

Damos a continuación un resumen de los métodos expuestos para que sirva de guía, ya que cuando estudiamos este tema por primera vez es fácil que nos perdamos un poco en los diferentes casos y posibilidades.
   

| **Método** 
| **Aplicable a...** 

| Reducción a un sistema de EDOs de primer orden 
| En principio a cualquier sistema de EDO 

| Reducción a una única ecuación de grado superior 
| EDOs de primer orden 

| Operador D 
| EDOs lineales de primer orden con coeficientes constantes 

| Valores y vectores propios 
| EDOs lineales homogéneas de primer orden con coeficientes constantes 

| Coeficientes indeterminados 
| Solución particular de EDOs lineales con coeficientes constantes 

| Variación de parámetros 
| Solución particular de EDOs lineales con coeficientes constantes 

| Transformada de Laplace 
| Solución particular de EDOs lineales con coeficientes constantes y condiciones iniciales dadas
{% endraw %}