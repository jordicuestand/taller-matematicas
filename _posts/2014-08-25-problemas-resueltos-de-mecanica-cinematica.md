---
layout: post
title: "Problemas resueltos de Física-> Mecánica->Cinemática"
date: 2014-08-25 06:21:14 +0000
categories:
  - "Fí­sica"
  - "Mecánica"
tags:
  - "aceleración centrípeta"
  - "aceleración de frenada"
  - "aceleración instantánea"
  - "aceleración media"
  - "aceleración normal"
  - "aceleración tangencial"
  - "caída libre"
  - "cambio de unidades"
  - "movimiento relativo"
  - "movimiento uniformemente acelerado"
  - "trayectoria rectilínea"
  - "velocidad relativa"
math: true
---
{% raw %}

Problemas de Física -> Mecánica -> Cinemática

**1.** Deducir el factor de conversión desde $\frac m{s^2}$ hasta $\frac{Km}{h^2}$. ¿Qué valor tendrá la aceleración de la gravedad $g=9.8\frac m{s^2}$ expresada en $\frac{Km}{h^2}$?

Para hacer el cambio de unidades físicas, usamos el método habitual de encadenar cambios:

$1\frac m{s^2}\frac1{1000}\frac{Km}m\frac{3600^2}{1^2}\frac{s^2}{h^2}=12.96\times10^3\frac{Km}{h^2}.$

Lo aplicamos a la constante física $g$:

$9.8\frac m{s^2}=9.8\cdot12.96\times10^3\frac{Km}{h^2}=1.27\times10^5\frac{Km}{h^2}.$

![separador](/taller-matematicas/assets/images/separador2.png)
**2.** Un vehiculo pasa por nuestro lado a 110 Km/h cuando empieza a frenar con deceleración constante, y recorre 2300m hasta detenerse completamente. ¿Cuanto tiempo ha necesitado para frenar, y que aceleración ha aplicado?

Es un movimiento uniformemente acelerado, con aceleración negativa. Las fórmulas que necesitamos son dos:

 	- espacio recorrido: $x=x_0+v_0t-\frac12at^2$

 	- velocidad final: $v_f=v_0-at$

Desconocemos las variables $t$ y $x$, por tanto tenemos dos ecuaciones y dos incógnitas. Si dividimos la primera por $t$ y sustituimos la segunda en la primera:

$\begin{array}{l}\left.\begin{array}{r}\frac xt=\frac{x_0}t+v_0-\frac12at\\v_f-v_0=-at\end{array}\right\}\Rightarrow\\\frac xt=\frac{x_0}t+v_0+\frac12\left(v_f-v_0\right)=\frac{x_0}t+\frac12\left(v_f+v_0\right).\end{array}$

Damos valores: $v_0=110km/h,\;v_f=0,\;x=2.3km,$ resulta:

$\begin{array}{l}\frac{2.3}t=\frac0t+\frac12\left(0+110\right)\Rightarrow\\t=\frac{2.3}{55}=41.8\times10^{-3}h=41.8\times10^{-3}h\frac{3600}1\frac sh=150.5s\end{array}$
Observar que hemos pasado los metros recorridos a km, para que sean coherentes todas las unidades; al final, lo hemos pasado de horas a segundos. Ahora usamos la segunda ecuación para obtener la aceleración de frenada:

$110=at\Leftrightarrow a=\frac{110}{\displaystyle\frac{23}{550}}=\frac{60500}{23}=2.63\times10^3\frac{km}{h^2}.$

Para pasar la aceleración a $m/s^2$ usamos el factor de conversión del problema 1:

$2.63\times10^3\frac{km}{h^2}\frac1{1.27\times10^5}\frac{h^2}{km}\frac m{s^2}=0.203\frac m{s^2}.$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

 
**3.** Un objeto se deja caer desde una altura $h$. Cuando lleva cayendo $t_0$ segundos, empezamos a cronometrarlo, y observamos que desciende 150 metros en 15 segundos. ¿Cuántos metros en total habrá descendido y en cuánto tiempo?

| 


| 
Llamando $h$ a la altura total recorrida, la altura caída previamente a empezar a cronometrar será $h-150$.

Como es un movimiento uniformemente acelerado, usaremos dos ecuaciones:

 	- espacio recorrido: $x=x_0+v_0t+0.5gt^2$

 	- velocidad instantánea: $v=v_0t+at$

 

Aplicamos la primera ecuación a la sección de caída libre de 150 metros:

$150=v_0\cdot3+\frac129.8\cdot3^2\Rightarrow v_0=35.3\;\frac ms.$
Esta es la velocidad que lleva el objeto cuando empezamos a cronometrarlo. Usamos ahora la segunda ecuación aplicada a la sección inicial de $h-150$m, en esa sección la velocidad inicial es $v_0=0$ y la velocidad final es 35.3 m/s:

$v=v_0+gt\Rightarrow35.3=0+9.8t\Rightarrow t=3.6s.$

Ese es el tiempo que llevaba cayendo cuando empezamos a cronometrarlo. Para saber cuanta altura había caído en ese tiempo, volvemos a la ecuación 1, teniendo en cuenta que ahora estamos en la primera sección de la caída, con $v_0=0$:

$h-150=0\cdot3.6+\frac129.8\cdot3.6^2=63.6m\Rightarrow h=213.6m.$

El tiempo total de caída es $3.6+3=6.6s.$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
**4.** Una barca ha de cruzar un río de 80 m de anchura. La barca es capaz de alcanzar una velocidad de 10 Km/h. La velocidad del agua del río es de 1.5 m/s. (a) ¿Cuanto tiempo tardará en cruzar suponiendo que la velocidad relativa de la barca con respecto al río es transversal a la corriente, y que distancia habrá recorrido? (b) ¿Cuanto tiempo tardará en cruzar suponiendo que la velocidad absoluta de la barca con respecto al río es transversal a la corriente?

(a) En el esquema vemos los vectores velocidad que necesitamos: $v_r$ es la velocidad relativa de la barca con respecto al río, $v_a$ la velocidad de la corriente de agua, que arrastra a la barca, $v=v_r+v_s$ es la velocidad absoluta resultante de la barca.


Expresando los vectores en componentes: $v_a=(0,-1.5), v_r=(10/3.6,0), v=(10/3.6,-1.5).$
Usamos ahora la ecuación del movimiento con velocidad constante, expresada por cada coordenada $(x,y)$ por separado: $x=x_0+v_xt,\;y=y_0+v_yt.$ Sustituyendo valores:

$\begin{array}{l}80=0+v_rt=\frac{10}{3.6}t\Rightarrow t=\frac{3.6\cdot80}{10}=28.8s,\\d=0+v_at=1.5\cdot28.8=43.2m.\end{array}$

La distancia total recorrida es la hipotenusa del triángulo formado por la anchura de río y la distancia según el eje y: $\sqrt{80^2+43.2^2}=90.9m.$
(b) En el esquema vemos que ahora la velocidad absoluta es transversal, luego la velocidad relativa ha de ser oblicua. Usamos las mismas ecuaciones que antes, descomponiendo en componentes $(x,y)$:


La componente $x$ de la velocidad relativa ha de ser igual a la velocidad transversal con la que cruza el río, mientras que la componente $y$ ha de contrarrestar la velocidad de la corriente de agua: $\overrightarrow{v_r}=\left(v,-v_a\right).$ Entonces:

$\left\|\overrightarrow{v_r}\right\|=\sqrt{v^2+v_a^2}=\frac{10}{3.6},\;v_a=1.5\;\Rightarrow v=\sqrt{\left(\frac{10}{3.6}\right)^2-1.5^2}=2.3\;\frac ms.$

Con esa velocidad transversal, el tiempo invertido será $t=80/2.3=34.2s.$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
**5.** Una partícula se mueve en una trayectoria rectilínea con un desplazamiento dado por la ecuación $x=4t^3-3t^2-6$ (en metros y segundos). Partiendo del reposo, ¿cuanto tiempo tardará en alcanzar una velocidad de $6 m/s$? ¿Qué aceleración tendrá en ese tiempo?

La velocidad viene dada por la derivada del desplazamiento respecto del tiempo: $\frac{dx}{dt}=12t^2-6t.$ Igualando al valor dado de la velocidad, obtenemos el tiempo:

$12t^2-6t=6\Rightarrow2t^2-t-1=0\Rightarrow t=\frac{1\pm\sqrt{1+8}}4=1s.$

La aceleración viene dada por la derivada de la velocidad respecto del tiempo: $\frac d{dt}\left(12t^2-6t\right)=24t-6,$ luego para $t=1, a=24-6=18 m/s^2.$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

**6.** El humo de la chimenea de un barco que marcha rumbo NNE con una velocidad de 20 nudos forma un ángulo de 20⁰ con su dirección. Sabemos que hay viento del W. ¿Cuál es la velocidad del viento?  Datos: 1 nudo = 0.5 m/s, para las direcciones de los rumbos, ver [rumbos en Wikipedia](http://es.wikipedia.org/wiki/Rosa_de_los_vientos#El_rumbo).

El rumbo NNE forma un ángulo de $\theta=\frac78\frac\pi2=\frac{7\pi}{16}$ radianes con el eje $x$ (o equivalentemente, con el rumbo E).  Entonces el humo del barco formará un ángulo con el eje $x$ de $\theta+20\frac\pi{180}=\frac{7\pi}{16}+\frac{2\pi}9=\frac{95\pi}{144}$ radianes (ver figura).


La velocidad del barco es de $v=10 m/s$, que será una componente de la velocidad del humo $v_h$, a la que debemos añadir la velocidad del viento $v_v$ para obtener la velocidad absoluta del humo $v_h$:

$\begin{array}{l}\overrightarrow v=10\left(\cos\left(\frac{7\pi}6\right),\sin\left(\frac{7\pi}6\right)\right),\\\overrightarrow{v_v}=\left(-v_v,0\right),\\v_h=\overrightarrow v+\overrightarrow{v_v}=\left(-v_v+10\cos\left(\frac{7\pi}6\right),10\sin\left(\frac{7\pi}6\right)\right).\end{array}$

Para relacionar la velocidad del humo con su dirección, usamos la igualdad válida para cualquier vector $v$:

$\overrightarrow v=\left(v_x,v_y\right)\Rightarrow\alpha=\tan^{-1}\left(\frac{v_y}{v_x}\right),$

donde $\alpha$ es el ángulo del vector con el eje $x$. Por tanto:

$\begin{array}{l}\tan^{-1}\left(\frac{10\sin\left({\displaystyle\frac{7\pi}{16}}\right)}{-v_v+10\cos\left({\displaystyle\frac{7\pi}{16}}\right)}\right)=\frac{95\pi}{144}\Rightarrow\\\frac{10\sin\left(\frac{7\pi}{16}\right)}{\tan\left(\frac{95\pi}{144}\right)}+10\cos\left(\frac{7\pi}{16}\right)=-v_v=-3.43\;m/s\Rightarrow\\\boxed{v_v=3.43\;\frac ms}.\end{array}$

 [![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

**7.** Al parar el motor de una lancha rápida ésta adquiere una aceleración negativa que es proporcional al cuadrado de su velocidad instantánea. A los 30s de haber parado el motor, su velocidad ha pasado de 20 m/s a 8 m/s. ¿Cuál es la aceleración en el momento de parar el motor? ¿Cuál es el espacio recorrido y cuál su velocidad a los 15s de parar el motor? ¿Cuál es la velocidad después de 400m de recorrido con el motor apagado?

La aceleración instantánea en el momento de detener el motor no la conocemos directamente, sólo sabemos la aceleración media entre t=0 y t=30: $\overline a=\frac{\triangle v}{\triangle t}=\frac{8-20}{30-0}=\frac{-2}5\frac m{s^2}$. Para obtener la aceleración instantánea, obtendremos primero la velocidad instantánea, y después derivando calcularemos la aceleración.

Sabemos que $\frac{dv}{dt}=-kv^2,$ y que la velocidad, función del tiempo, toma los valores $v(0)=20, v(30)=8.$ Integrando:

$\begin{array}{l}\frac{dv}{dt}=-kv^2\Rightarrow dv=\;-kv^2dt\Rightarrow\int dv=\;\int-kv^2dt\Rightarrow\\\int\frac1{v^2}dv=\;\int-kdt\Rightarrow\frac{-1}v=-kt+C.\end{array}$

Dando el valor $t=0$:

$\frac{-1}{v\left(0\right)}=\frac{-1}{20}=-k\cdot0+C\Rightarrow k=\frac{-1}{20},$

luego:

$\frac1v=kt+\frac1{20}.$

Dando ahora el valor $t=30:$

$\frac18=k\cdot30+\frac1{20}\Rightarrow k=\frac{\frac18-\frac1{20}}{30}=\frac1{400}.$

Nos queda la expresión de la velocidad:

$\frac1v=\frac t{400}+\frac1{20}.$

Derivamos:

$\begin{array}{l}\frac{\operatorname{d}{}}{\operatorname{d}t}\left(\frac1v\right)=\frac{\operatorname{d}{}}{\operatorname{d}t}\left(\frac t{400}+\frac1{20}\right)\Rightarrow\\\frac{-1}{v^2}\frac{dv}{dt}=\frac1{400}\Rightarrow\\a=\frac{dv}{dt}=-\frac{v^2}{400}.\end{array}$

Sustituimos la expresión que tenemos para $v$:

$a=\frac{dv}{dt}=-\frac{v^2}{400}=-\frac1{400\left({\displaystyle\frac t{400}}+\displaystyle\frac1{20}\right)^2}=-\frac1{\left({\displaystyle\frac t{20}}+1\right)^2}.$

La aceleración vemos que es variable con el tiempo. Para el instante inicial t=0: $a=-\frac1{\left({\displaystyle\frac0{20}}+1\right)^2}=-1\frac m{s^2}.$

Para saber el espacio recorrido a los 15s de parar el motor no podemos usar la conocida ecuación $s=s_0+v_0t+\frac12at^{2\;}$ pues solo es válida cuando la aceleración es constante (movimiento uniformemente acelerado). Tendremos pues que integrar la velocidad:

$\begin{array}{l}x=\int\frac{\operatorname{d}x}{\operatorname{d}t}dt=\int\left(\frac1{400}t+\frac1{20}\right)^{-1}dt=400\int\frac{1/400}{\frac1{400}t+\frac1{20}}dt=\\400\ln\left(\frac1{400}t+\frac1{20}\right)+C.\end{array}$

Suponiendo que el espacio recorrido es cero cuando $t=0$:

$\begin{array}{l}\begin{array}{l}x(0)=400\ln\left(\frac1{400}0+\frac1{20}\right)+C=0\Leftrightarrow C=-400\ln\left(\frac1{20}\right)=400\ln\left(20\right)\Rightarrow\\x(t)=400\left$\ln\left(\frac1{400}t+\frac1{20}\right)+\ln\left(20\right)\right$=.\end{array}\\400\ln\left(20\left(\frac1{400}t+\frac1{20}\right)\right)=400\ln\left(\frac t{20}+1\right).\end{array}$

Para t = 15s obtenemos $x(15)=400\ln\left(\frac1{20}15+1\right)=224m.$

La velocidad en ese instante es $v(15)=\left(\frac1{400}15+\frac1{20}\right)^{-1}=11.4\frac ms.$

Una vez recorridos 400m, tendremos $x(t)=400\ln\left(\frac1{20}t+1\right)=400\Rightarrow t=20\left(e-1\right)=53.37s,$ y la velocidad en ese instante es:

$v(t)=\left(\frac1{400}20\left(e-1\right)+\frac1{20}\right)^{-1}=7.4\frac ms.$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)

**8.** Una locomotora recorre una vía circular de 280 m de radio, partiendo de un punto inicial con velocidad nula, acelerando de forma uniforme, y recorre un arco de 120⁰, alcanzando una velocidad de 85 km/h. ¿Qué tiempo ha empleado en ello? ¿Cuáles son las aceleraciones tangencial, centrípeta y total?

 El arco recorrido mide $120\frac\pi{180}=\frac23\pi$ radianes, y la velocidad dada, 85 km/h, es el módulo de la velocidad tangencial en el instante en que completa ese arco. La distancia recorrida es $\frac23\pi\cdot280=\frac{560\pi}3m$. Como el movimiento es uniformemente acelerado, se cumplen las ecuaciones:

$\begin{array}{l}s=s_0+v_0t+\frac12at^2\\v=v_0+at\end{array}$

En nuestro caso:

$\left.\begin{array}{r}\frac{560\pi}3=\frac12at^2\\\frac{85}{3.6}=at\end{array}\right\}\Rightarrow\frac{560\pi}3=\frac12\frac{85}{3.6}t\Rightarrow t=\frac{560\pi\cdot2\cdot3.6}{3\cdot85}=49.7s.$

La aceleración tangencial instantánea, como es constante, coincide con la aceleración media:

$a_t={\overline a}_t=\frac{\triangle v}{\triangle t}=\frac{85/3.6}{49.7}=0.475\frac m{s^2}.$

La aceleración centrípeta, o normal, $a_n$, no es constante, sino que vale $a_n=\frac{v^2}r=\frac{\left(at\right)^2}r=\frac{0.475^2t^2}{280}=0.806\times10^{-3}t^2\frac m{s^2}.$ Al completar el arco, esta aceleración tangencial normal vale $a_n=0.806\times10^{-3}\cdot49.7^2=1.99\frac m{s^2}.$ La aceleración total es el módulo del vector que tiene por componentes $(a_t,a_n)$, y vale $\sqrt{1.99^2+0.48^2}=2.05\;\frac m{s^2}.$

[![separador2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
{% endraw %}