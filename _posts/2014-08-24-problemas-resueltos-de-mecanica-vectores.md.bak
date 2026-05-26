---
layout: post
title: "Problemas resueltos de Mecánica->Vectores"
date: 2014-08-24 09:52:41 +0000
math: true
---
{% raw %}

**1.** Escribir la ecuación vectorial de un plano que tiene por vector normal el vector unitario $n$ y que está a una distancia $d$ del origen de coordenadas. ¿Cuál es la distancia de un punto $Q$ cualquiera a ese plano?

Para fijar ideas, imaginemos un plano paralelo al plano coordenado $XY$, que corta al eje $Z$ en un punto $P$, a una distancia $d$ del origen $O$. El vector normal $\overrightarrow n$ es perpendicular al plano, y será paralelo al eje vertical $OZ$. El vector $OP$ será también paralelo a $OZ$, y por tanto paralelo al vector $\overrightarrow n$. Esto significa que $OP=\lambda\overrightarrow n$ para un cierto $\lambda$.

 [![Pla1](/taller-matematicas/assets/images/Pla1.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/Pla1.png)

Pero la distancia $OP$ es igual a la distancia entre el plano y el origen $O$, luego  $\lambda=d$. Entonces $OP=d\overrightarrow n$.

Sea un punto $Q$ cualquiera del plano, y $\overrightarrow{r_Q}$ su vector posición; la ecuación general del plano en forma vectorial es:
$\overrightarrow{r_Q}\cdot\overrightarrow n+C=0$

para un cierto número real $C$. Si aplicamos esta ecuación al punto $P$ obtenemos:
$\overrightarrow{r_P}\cdot\overrightarrow n+C=d\o$

ya que $\overrightarrow n\cdot\overrightarrow n=1$ por ser $\overrightarrow n$ un vector unitario. La ecuación del plano que resulta es:
$\overrightarrow r\cdot\overrightarrow n-d=0$

para el vector de posición $\overrightarrow r=\left(x,y,z\right)$ de cualquier punto del plano.
Si hubiéramos pensado en un plano general para fijar ideas, y no en uno paralelo al plano $XY$, el resultado sería el mismo: la distancia $d$ desde el orígen $O$ al plano siempre vendrá dada por un vector $OP$ paralelo a $\overrightarrow n$, y el argumento sería el mismo.

Hallemos ahora la distancia entre un punto cualquiera $r_0$ del espacio y el plano $\pi:\;\overrightarrow r\cdot\overrightarrow n-d=0$. Consideramos una recta perpendicular al plano $\pi$ que pasa por $r_0$ y corta al plano $\pi$ por el punto $Q$. De nuevo, el vector $Qr_0$ es paralelo al vector normal $\overrightarrow n,$ así que se cumple que:

$r_0=Q+\lambda\cdot\overrightarrow n\Rightarrow Q=r_0-\lambda\cdot\overrightarrow n$.

[![Pla](/taller-matematicas/assets/images/Pla.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/Pla.png)

y la distancia que nos piden es precisamente el valor $\lambda$. Pero para cualquier punto $Q$ del plano se ha de cumplir la ecuación ${\overrightarrow r}_Q\cdot\overrightarrow n-d=0$, así que:

$\left.\begin{array}{r}{\overrightarrow r}_Q=\overrightarrow{r_0}-\lambda\overrightarrow n\\{\overrightarrow r}_Q\cdot\overrightarrow n-d=0\end{array}\right\}\Rightarrow\left(\overrightarrow{r_0}-\lambda\overrightarrow n\right)\cdot\overrightarrow n-d=0\Rightarrow\overrightarrow{r_0}\cdot\overrightarrow n-\lambda-d=0\Rightarrow\boxed{\lambda=\overrightarrow{r_0}\cdot\overrightarrow n-d}.$

La distancia pedida es $\lambda=\overrightarrow{r_0}\cdot\overrightarrow n-d.$

Ejemplo: Sea el vector normal unitario $\overrightarrow n=(0,0,1)$, la distancia del plano al origen $d=2$ y el punto $Q=(1,2,3)$. Entonces la ecuación de ese plano es:

$\overrightarrow r\cdot\overrightarrow n-d=\left(x,y,z\right)\cdot\left(0,0,1\right)-2=z-2=0\Rightarrow z=2,$

y la distancia entre el plano y el punto $Q$ es:

$\overrightarrow{r_Q}\cdot\overrightarrow n-d=\left(1,2,3\right)\cdot\left(0,0,1\right)-2=3-2=1.$

---

**2.** Dados los vectores $\overrightarrow u=\left(2,3,1\right),\;\overrightarrow v=(1,6,-1)$, obtener el vector $\overrightarrow w$ proyección de $\overrightarrow u$ sobre $\overrightarrow v$.

Cuando hacemos el producto escalar de dos vectores $\overrightarrow A,\;\overrightarrow B$, el resultado puede interepretarse como el módulo de la proyección de uno de los vectores multiplicado por el módulo del otro vector: $\overrightarrow A\cdot\overrightarrow B=A\cdot B\cdot\cos\;\widehat{\overrightarrow A\overrightarrow B}$

[caption id="attachment_286" align="alignnone" width="283"][![Fuente: http://www.physicsmynd.com](/taller-matematicas/assets/images/producte_esalar.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/producte_esalar.png) Fuente: http://www.physicsmynd.com[/caption]

Por tanto el vector proyección de $\overrightarrow u$ sobre $\overrightarrow v$ se expresará como $\overrightarrow w=\overrightarrow e\cdot\left(\overrightarrow u\cdot\overrightarrow v\right)=\overrightarrow e\cdot u\cdot v\cdot\cos\;\widehat{\overrightarrow u\overrightarrow v}$, donde $\overrightarrow e$ es el vector unitario en la dirección de $\overrightarrow v$: $\overrightarrow e=\frac{\overrightarrow v}v=\frac{\left(1,6,1\right)}{\sqrt{1^2+6^2+1^2}}=\frac{\left(1,6,1\right)}{\sqrt{38}},$ queda por tanto:

---

**3.** Dados los vectores $\overrightarrow A,\;\overrightarrow B$ calcular $\left(\overrightarrow A\times\;\overrightarrow B\right)^2+\left(\overrightarrow A\cdot\;\overrightarrow B\right)^2.$

Sabemos que el resultado del producto vectorial $\left(\overrightarrow A\times\;\overrightarrow B\right)$ es otro vector perpendicular al plano formado por $\overrightarrow A,\;\overrightarrow B$ cuyo mòdulo es $A·B·cos(AB)$.

[caption id="attachment_287" align="alignnone" width="300"][![Fuente: Wikipedia](/taller-matematicas/assets/images/producte_vectorial-300x232.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/producte_vectorial.png) Fuente: Wikipedia[/caption]

Entonces $\left(\overrightarrow A\times\;\overrightarrow B\right)^2=\left(\overrightarrow A\times\;\overrightarrow B\right)\cdot\left(\overrightarrow A\times\;\overrightarrow B\right)$ es el producto escalar de ese vector perpendicular consigo mismo, que será igual a su módulo al cuadrado:

$\left(\overrightarrow A\times\;\overrightarrow B\right)^2=\left(\overrightarrow A\times\;\overrightarrow B\right)\cdot\left(\overrightarrow A\times\;\overrightarrow B\right)=\left(AB\sin\left(AB\right)\right)^2=A^2B^2\sin^2\left(AB\right).$

En cuanto al segundo operando: $\left(\overrightarrow A\cdot\;\overrightarrow B\right)^2=\left(\overrightarrow A\cdot\;\overrightarrow B\right)\cdot\left(\overrightarrow A\cdot\;\overrightarrow B\right)=\left(AB\cos\left(AB\right)\right)^2=A^2B^2\cos^2\left(AB\right).$

Sumando obtenemos:

$\begin{array}{l}\left(\overrightarrow A\times\;\overrightarrow B\right)^2+\left(\overrightarrow A\cdot\;\overrightarrow B\right)^2=A^2B^2\sin^2\left(AB\right)+A^2B^2\cos^2\left(AB\right)=\\A^2B^2\left(\sin^2\left(AB\right)+\cos^2\left(AB\right)\right)=\boxed{A^2B^2}.\end{array}$

Otra forma, más pesada, de resolver el ejercicio es realizando los productos componente a componente:

$\begin{array}{l}\left(\overrightarrow A\times\;\overrightarrow B\right)=\left(A_yB_z-A_zB_y,\;A_xB_z-A_zB_x,\;A_xB_y-A_yB_x\right);\\\left(\overrightarrow A\times\;\overrightarrow B\right)^2=\left(A_yB_z-A_zB_y\right)^2+\left(A_xB_z-A_zB_x\right)^2+\left(\;A_xB_y-A_yB_x\right)^2;\\\left(\overrightarrow A\cdot\;\overrightarrow B\right)=A_xB_x+A_yB_y+A_zB_z;\\\left(\overrightarrow A\cdot\;\overrightarrow B\right)^2=\left(A_xB_x+A_yB_y+A_zB_z\right)^2;\\\left(\overrightarrow A\times\;\overrightarrow B\right)^2+\left(\overrightarrow A\cdot\;\overrightarrow B\right)^2=\left(A_xB_x\right)^2+\left(A_yB_y\right)^2+\left(A_zB_z\right)^2+\left(A_zB_y\right)^2+\left(A_xB_z\right)^2+\left(A_zB_x\right)^2+\left(A_yB_x\right)^2+\left(A_yB_z\right)^2+\left(A_xB_y\right)^2=\\\left(A_x^2+A_y^2+A_z^2\right)\cdot\left(B_x^2+B_y^2+B_z^2\right)=A^2B^2.\\\end{array}$

Nota: si el lector está dudando sobre si podiamos interpretar el cuadrado del producto vectorial asi: $(\overrightarrow A\times\overrightarrow B)^2=(\overrightarrow A\times\overrightarrow B)\times(\overrightarrow A\times\overrightarrow B),$ observe que resultaria una expresión incompatible, pues el resutlado del doble producto vectorial es un vector, y no podemos sumar un vector con el resultado del producto escalar $\overrightarrow{(A}\cdot\overrightarrow B)^2$ que es un número real.

---

**4.** Dados los vectores $\overrightarrow A(5t^2,\;t,\;-t^3),\;\overrightarrow B(sin(t),\;-cos(t),\;0)$, calcular $\frac{\operatorname{d}{}}{\operatorname{d}t}\left(\overrightarrow A\times\overrightarrow B\right).$

Calculamos el producto vectorial:

$\begin{array}{l}\left(\overrightarrow A\times\;\overrightarrow B\right)=\left(A_yB_z-A_zB_y,\;A_xB_z-A_zB_x,\;A_xB_y-A_yB_x\right)=\\\left(t\cdot0+t^3(-\cos(t)),\;5t^2\cdot0+t^3\sin(t),\;5t^2(-\cos(t))-t\sin\left(t\right)\right)=\\\left(-t^3\cos(t),t^3\sin(t),\;-5t^2(\cos(t))-t\sin\left(t\right)\right).\\\end{array}$

Derivamos respecto a $t$:

$\begin{array}{l}\frac{\operatorname{d}{}}{\operatorname{d}t}\left(\overrightarrow A\times\;\overrightarrow B\right)=\left(-3t^2\cos(t)+t^3\sin(t),\;3t^2\sin(t)+t^3\cos(t),-11t\cos(t)+5t^2\sin(t)-\sin(t)\right).\\\end{array}$

---

**5.** Un cierto vector dependiente del tiempo $\overrightarrow A(t)$ mantiene siempre su dirección constante; ¿que podemos decir sobre su vector derivada respecto al tiempo $\frac{\operatorname{d}\overrightarrow A}{\operatorname{d}t}?$

Si la dirección es constante entonces solo varia el módulo del vector, esto lo podemos expresar como $\overrightarrow A(t)=A(t)\cdot\overrightarrow u,$ donde $\overrightarrow u$ es un vector unitario en la dirección del vector. Derivando: $\frac{\operatorname{d}{}}{\operatorname{d}t}\overrightarrow A(t)=\frac{\operatorname{d}{}}{\operatorname{d}t}\left(A(t)\cdot\overrightarrow u\right)=\frac{\operatorname{d}A(t)}{\operatorname{d}t}\cdot\overrightarrow u,$ ya que $\overrightarrow u$ es constante. Si comparamos el vector $\overrightarrow A(t)$ con su derivada, vemos que ambos vectores son paralelos, pues ambos tienen la misma dirección constante $\overrightarrow u$; en efecto: :

$\left.\begin{array}{r}\overrightarrow A(t)=A(t)\cdot\overrightarrow u\\\frac{\operatorname{d}\overrightarrow A(t)}{\operatorname{d}t}=\;\frac{\operatorname{d}A(t)}{\operatorname{d}t}\cdot\overrightarrow u\end{array}\right\}\Rightarrow\overrightarrow A(t)\times\frac{\operatorname{d}\overrightarrow A(t)}{\operatorname{d}t}=A(t)\cdot\frac{\operatorname{d}A(t)}{\operatorname{d}t}\cdot\left(\overrightarrow u\times\overrightarrow u\right)=0,$

pues el producto vectorial de un vector consigo mismo es cero, así como tambien es cero el producto de dos vectores paralelos. Por consiguiente, los vectores $\overrightarrow A(t),\;\frac{\operatorname{d}\overrightarrow A(t)}{\operatorname{d}t}$ son paralelos.

 

---

**6.** ¿Es posible que la suma $w=u+v$ de dos vectores de mòdulos $u=2$ y $v=5$ tenga módulo 1? Justifica la respuesta.

[caption id="attachment_303" align="alignnone" width="194"][![Suma gráfica de los vectores u + v = w: forman un triángulo](/taller-matematicas/assets/images/suma_vectors.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/suma_vectors.png) Suma gráfica de los vectores u + v = w: forman un triángulo. (Fuente: wikipedia)[/caption]
Los vectores que se suman y su resultante forman un triángulo. Por [la desigualdad triangular](http://es.wikipedia.org/wiki/Desigualdad_triangular) la suma de dos lados cualesquiera de un triángulo siempre es mayor que el otro lado. Si tuviéramos un triángulo de lados $u=2, v=5, w=1$ se vulneraría la desigualdad triangular, pues $u + w = 3 &lt; v = 5$. Por tanto no es posible la situación del enunciado.

Otra forma de verlo es pensando en la regla del paralelogramo para la suma de vectores:

[caption id="attachment_304" align="alignnone" width="236"][![Regla del paralelogramo para la suma de vectores: el vector suma es la hipotenusa del rectángulo que tiene por catetos los vectores que sumamos. Fuente: Wikipedia.](/taller-matematicas/assets/images/suma_vectors2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/suma_vectors2.png) Regla del paralelogramo para la suma de vectores: el vector suma es la hipotenusa del rectángulo que tiene por catetos los vectores que sumamos. Fuente: Wikipedia.[/caption]
La hipotenusa del triángulo es mayor que cualquiera de los catetos, por tanto $w$ sería mayor que $u$ y que $v$; la excepción es cuando  $u$ y $v$ son paralelos con sentidos opuestos, en este caso el triángulo degenera en una recta, y la longitud mínima de $w$ será $v-u=3&gt;1.$

---

** 7.** Dados dos vectores $a, b$, dar la expresión del vector unitario $u$ perpendicular al plano formado por $a, b$.

El producto vectorial $c=a\times b$ es un vector perpendicular al plano formado por $a, b$. Luego dividiendo $c$ por su módulo, obtendremos el vector unitario pedido: $u=\frac{a\times b}{\left\|a\times b\right\|}.$

---
{% endraw %}