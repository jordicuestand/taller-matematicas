---
layout: post
title: "Tensores en Física"
date: 2017-01-31 04:58:17 +0000
categories:
  - "Fí­sica"
  - "Vectores"
tags:
  - "campo tensorial"
  - "tensor"
  - "tensor de conductividad"
  - "tensor de esfuerzo"
  - "tensor de inercia"
math: true
---
{% raw %}

## Magnitudes tensoriales

En Física nos encontramos frecuentemente con **magnitudes escalares** que son aquellas que numéricamente se expresan mediante un único número real, como el tiempo o la temperatura, también con **magnitudes vectoriales** que se expresan mediante un vector (ver [vectores en Física](http://tallermatematic.ovh/wp/index.php/2016/08/11/vectores/)), como la fuerza o el campo eléctrico. A menudo estas magnitudes se refieren a puntos del espacio o bien a objetos puntuales, como por ejemplo objetos puntuales, cargas eléctricas puntuales, etc. Así, hablamos de "el vector fuerza **F** aplicado a un punto material P de masa m", que ejercerá una aceleración, etc, como vemos a la izquierda de la figura 1, y todo queda bien determinado conociendo la posición de P, su masa m, y la fuerza **F**.

Para objetos no puntuales, como el de la figura 1 a la derecha, nos encontramos que una misma fuerza **F** aplicada en partes distintas del cuerpo C produce efectos distintos: el cuerpo C girará sobre sí mismo de forma distinta según el punto de aplicación de la fuerza. Notemos que, a pesar de haber rotulado las fuerzas $F_1,F_2,F_3$ de distinto modo, de hecho como vectores tienen la misma representación numérica, ya que tienen el mismo módulo, dirección y sentido (se dice que son vectores equipolentes). Entonces tenemos que la masa m del cuerpo C, un escalar, por sí sola, no nos da suficiente información para deducir la velocidad angular del cuerpo en función de la fuerza aplicada.

[caption id="attachment_150167" align="alignnone" width="457"]![Fig. 1: fuerza F aplicada sobre un objeto puntual (izquierda) y sobre un cuerpo (derecha)](/taller-matematicas/assets/images/tensors1.png) Fig. 1: fuerza F aplicada sobre un objeto puntual (izquierda) y sobre un cuerpo (derecha)[/caption]
Otro ejemplo lo encontramos en el electromagnetismo en la materia: cuando aplicamos un campo eléctrico **E** a un material susceptible de [polarización](https://es.wikipedia.org/wiki/Polarizabilidad), se induce la creación de [dipolos eléctricos](https://es.wikipedia.org/wiki/Dipolo_el%C3%A9ctrico#Momento_dipolar_de_una_distribuci.C3.B3n_de_carga) atómicos, caracterizados por la magnitud  [momento dipolar P](https://es.wikipedia.org/wiki/Dipolo_el%C3%A9ctrico#Densidad_volum.C3.A9trica_dipolar_y_densidades_de_carga_ligada) que es proporcional al campo: $\overrightarrow P=\alpha\overrightarrow E$, donde $\alpha$ es una constante escalar que depende del material; ahora bien, para los sólidos cristalinos, como por ejemplo la calcita, la constante de proporcionalidad  depende de la dirección del campo eléctrico aplicado. De nuevo la información proporcionada por la constante escalar $\alpha$ es insuficiente para definir la situación física.

Vemos pues que abundan las situaciones reales en las que las magnitudes escalares y vectoriales aportan información insuficiente para describir la situación; en estos casos necesitamos las **magnitudes tensoriales**:

Las magnitudes tensoriales son útiles para describir propiedades físicas que varían con la dirección en la que se aplica una magnitud vectorial.

##  Tensores y vectores

Consideremos un sólido localizado según unos ejes en el espacio XYZ al que aplicamos una fuerza **F** paralela al eje X; dependiendo del punto de aplicación sobre el sólido, éste girará de forma distinta, expresada por las velocidades angulares $\Omega$.

[caption id="attachment_150170" align="alignnone" width="349"]![Fig. 2: vectores fuerza equipolentes y vectores velocidad angular producidos](/taller-matematicas/assets/images/tensors2.png) Fig. 2: vectores fuerza equipolentes y vectores velocidad angular producidos[/caption]
En general, para una fuerza $\overrightarrow F=\left(F_x,0,0\right)$ obtendremos una velocidad angular proporcional a la fuerza pero que puede tener cualquier dirección: $\overrightarrow\Omega=\left(\alpha_xF_x,\alpha_yF_x,\alpha_zF_x\right)$, donde los coeficientes $\alpha_x,\alpha_y,\alpha_z$ son las constantes de proporcionalidad, propiedades del material. Si ahora aplicamos la fuerza F paralelamente al eje Y, obtendremos unas velocidades angulares distintas, con unas constantes de proporcionalidad también distintas, para distinguirlas de las obtenidas en la dirección del eje X, añadimos un subíndice:

 	- fuerza en la dirección del eje X: $\overrightarrow\Omega=\left(\alpha_{xx}F_x,\alpha_{xy}F_x,\alpha_{xz}F_x\right)$

 	- fuerza en la dirección del eje Y: $\overrightarrow\Omega=\left(\alpha_{yx}F_x,\alpha_{yy}F_x,\alpha_{yz}F_x\right)$

Por último, consideramos que la fuerza es paralela al eje Z, entonces:

 	- fuerza en la dirección del eje Z: $\overrightarrow\Omega=\left(\alpha_{zx}F_x,\alpha_{zy}F_x,\alpha_{zz}F_x\right)$

Para una fuerza en dirección arbitraria, sabemos que la podemos descomponer en suma de tres fuerzas, cada una en la dirección de un eje: $\overrightarrow F=F_x\widehat x+F_y\widehat y+F_z\widehat z$, entonces la velocidad angular resultante será también la suma de la producida para cada componente de la fuerza:

$\overrightarrow\Omega=\left(\alpha_{xx}F_x,\alpha_{xy}F_x,\alpha_{xz}F_x\right)+\left(\alpha_{yx}F_y,\alpha_{yy}F_y,\alpha_{yz}F_y\right)+\left(\alpha_{zx}F_z,\alpha_{zy}F_z,\alpha_{zz}F_z\right)=\;\sum_{ij}\alpha_{ij}\cdot{\overrightarrow F}_i\cdot\widehat j[1]$

donde el sumatorio recorre los índices i, j con los valores X, Y, Z, o bien 1, 2, 3, identificando el eje X como el primero, etc, y el vector $\widehat j$ simboliza el vector unitario en la dirección de cada eje coordenado.

En la expresión [1] tenemos que la relación entre los vectores **F** y $\overrightarrow\Omega$ viene dada por 3 x 3 = 9 escalares $\alpha_{ij}$; en general, dados dos vectores $\overrightarrow a, \overrightarrow b$ si la relación entre ellos viene dada por una doble suma sobre los coeficientes $\alpha_{ij}$, diremos que los $\alpha_{ij}$ son un **tensor de rango 2** (de rango 2 significa que el tensor tiene dos índices, el i y el j):

 
$a_j=\underset{1\leq i\leq3}{\sum\alpha_{ij}b_i}[2]$

**Definición 1**:  *un tensor de rango 2 en el espacio R³ es un conjunto de 3 x 3 = 3² = 9 valores $\alpha_{ij},\; 1\leq i,j\leq3$ que sirven para transformar un vector en otro vector*.

## Ejemplos de tensores en Física

 	- En mecánica, un objeto sólido que gira alrededor de un eje fijo tiene un vector [momento angular](https://es.wikipedia.org/wiki/Momento_angular) L proporcional al vector velocidad angular $\Omega$, y la proporcionalidad viene dada por el [**tensor de inercia**](https://es.wikipedia.org/wiki/Tensor_de_inercia) I del sólido: $\overrightarrow L=I\cdot\overrightarrow\Omega$, un tensor de rango 2.

 	- En electromagnetismo los vectores polarización P inducida sobre un sólido por el  vector campo eléctrico E vienen relacionados por el **tensor de polarizabilidad** del sólido, $\overrightarrow P=\alpha\cdot\overrightarrow E$, un tensor de rango 2.

 	- Cuando una corriente eléctrica recorre un cristal conductor, la relación entre el vector densidad de corriente j y el vector campo eléctrico E viene dada por el **tensor de conductividad** del cristal, $\overrightarrow j=\sigma\cdot\overrightarrow E$, un tensor de rango 2.

 	- Dado un vector axial v (o pseudovector), sus componentes $v_x,v_y,v_z$ forman un tensor de rango 2 que sólo tiene 3 componentes distintas de cero; se comprueba aplicando la expresión [2] al vector axial, para comprobar que para todo vector b la expresión [2] produce un vector a (ver la definición 1). En general, las componentes de todo producto vectorial a x b forman un tensor de grado 2.

 	- En un sólido sometido a una fuerza externa, las fuerzas internas de resistencia dependen de la dirección de la fuerza externa aplicada y también del punto de aplicación; para cada punto (x,y,z), la relación entre el vector fuerza y el vector deformación es el [**tensor de esfuerzo**](https://es.wikipedia.org/wiki/Tensor_tensi%C3%B3n) del material en ese punto, $\overrightarrow F=S\left(x,y,z\right)\cdot\left(x,y,z\right)$. Como para cada punto (x,y,z) tenemos un tensor de esfuerzo S(x,y,z), para caracterizar todo el sólido necesitamos una función S(x,y,z) que asigna a cada punto del sólido un tensor de grado 2, a estas funciones se les llama [**campos tensoriales**](https://es.wikipedia.org/wiki/Campo_tensorial), por analogía a los [**campos vectoriales**](https://es.wikipedia.org/wiki/Campo_vectorial), que asignan un vector a cada punto (x,y,z) del espacio.

 	- En un sólido elástico sometido a una fuerza externa, las deformaciones en cada punto dependen del punto considerado, formando un tensor de rango 2 de deformaciones T; el valor de estas deformaciones dependen a su vez del tensor de esfuerzos S en ese punto, también de rango 2; aquí tenemos pues una relación entre tensores, no entre vectores como en los ejemplos anteriores. No es difícil ver que para relacionar dos tensores de rango 2 entre sí, cada uno con 9 componentes, necesitamos 9 x 9 = 81 componentes, organizados en 4 índices de 3 valores (ejes x, y, z), que forman un **tensor de rango superior**, concretamente de rango 4: $T_{ij}=\sum_{k,l}\alpha_{ijkl}S_{kl}$. Es el **tensor de deformación elástica**.
{% endraw %}