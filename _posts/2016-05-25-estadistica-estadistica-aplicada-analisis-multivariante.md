---
layout: post
title: "Estadística -> Estadística Aplicada -> Análisis Multivariante"
date: 2016-05-25 07:47:16 +0000
categories:
  - "Estadística"
  - "Estadística aplicada"
  - "Métodos multivariantes"
tags:
  - "análisi estadístico"
  - "análisis factorial"
  - "componentes principales"
  - "correlación"
  - "multivariante"
  - "R"
math: true
---

En esta entrada sólo pretendemos dar una introducción breve a un tema extenso y complejo como es el análisis estadístico multivariante, y lo haremos de forma constructiva, partiendo de un ejemplo simple pero real que iremos desarrollando. No se incluyen demostraciones matemáticas, sólo nos centramos en el "para qué sirve?" y en el "cómo se hace?". Espero que sea de utilidad para los estudiantes no especialistas en Estadística que necesitan tener las ideas claras en esta materia sin perderse en detalles técnicos. En este primer artículo sólo introducimos conceptos, y luego aplicamos dos técnicas relacionadas con la simplificación y reducción de datos: componentes principales y factores; en un segundo artículo trataremos de la otra posibilidad del análisis multivariante: la detección de grupos y clasificación de los individuos.

**Contenidos**:

 	- Análisis Multivariante: ¿para qué sirve?

 	- Reducir el número de variables: análisis de componentes principales

 	- Reducir el número de variables: análisis factorial

![separador2](/assets/images/separador2-300x38.png)
### Análisis Multivariante: ¿para qué sirve?

En los estudios estadísticos de casos reales es frecuente encontrarse con que tenemos que manejar no sólo muchos datos, sino también muchas variables; el tener un gran número de variables dificulta la comprensión del problema así como la interpretación de los resultados estadísticos. En el siguiente ejemplo vemos un caso multivariante típico:

**Ejemplo 1**: En un centro educativo han estado experimentando en los tres últimos cursos académicos con una nueva técnica pedagógica, que se ha aplicado a cinco grupos distintos de alumnos de bachillerato en distintas asignaturas, un total de 125 alumnos. Se quiere realizar un estudio estadístico para averiguar hasta qué punto la nueva técnica ha sido efectiva en términos no sólo de mejora de calificaciones, si no también de otras variables como la participación activa del alumno en la clase, la mejora de habilidades atencionales y de estudio, y la satisfacción en general del alumno en la clase. Además, se considera importante tener en cuenta en el estudio otras variables que pueden condicionarlo, como por ejemplo la edad, la clase social, la asignatura en la que se utilizó la técnica, el nivel de estudios de los padres, y el profesor que la aplicó. Para comparar resultados, se toman también los datos de otros 125 alumnos con los que no se aplicó la nueva técnica. Se trabajará por tanto con una muestra de 250 alumnos y 11 variables. A continuación se muestran las primeras filas de esta tabla, que puede descargarse de aquí.

| **TEC** 
| **CAL** 
| **PAR** 
| **ATE** 
| **EST** 
| **SAT** 
| **EDAD** 
| **CLA** 
| **ASIG** 
| **PROF** 
| **ESTP** 

| 0 
| 1 
| 0 
| 1 
| 0 
| 3 
| 16 
| 0 
| 2 
| 3 
| 0 

| 0 
| 1 
| 0 
| 1 
| 0 
| 1 
| 17 
| 0 
| 3 
| 5 
| 0 

| 0 
| 1 
| 0 
| 0 
| 1 
| 7 
| 18 
| 2 
| 2 
| 4 
| 3 

| 0 
| 2 
| 1 
| 1 
| 0 
| 2 
| 19 
| 2 
| 3 
| 5 
| 0 

| 0 
| 2 
| 0 
| 1 
| 2 
| 5 
| 18 
| 2 
| 1 
| 1 
| 0 

Los significados de cada variable son:

 

| TEC 
| 1: aplicamos nueva técnica, 0: no lo hacemos 

| CAL 
| Calificación obtenida 

| PAR 
| Medida de la participación activa en clase 

| ATE 
| Medida de la atención en clase 

| EST 
| Medida de las técnicas de estudio personales 

| SAT 
| Medida de la satisfacción en clase 

| EDAD 
| Edad del alumno 

| CLA 
| Clase social: 0 baja, 1 media, 2 alta 

| ASIG 
| Asignatura en la que se aplicó la técnica: 1 MAT, 2 CIENCIAS, 3 HISTORIA 

| PROF 
| Profesor que la aplicó, valores 1,2 (MAT), 3,4 (CIENC), 5 (HIST) 

| ESTP 
| Nivel de estudios padres: 0 sin estudios, 1 básicos, 2 medios, 3 superiores 

Sucede a menudo que las variables consideradas no son independientes entre si, al contrario, hay relaciones entre ellas. También a menudo se pueden clasificar los individuos estudiados (los estudiantes en el ejemplo 1) en grupos homogéneos, y realizar un estudio detallado para cada grupo: en el ejemplo 1 podríamos descubrir que agrupando los alumnos según el profesor que aplicó la técnica hay grandes diferencias entre los grupos y resultados parecidos dentro de los grupos. De todo este análisis se ocupan los métodos multivariantes, concretamente lo que hacen es:

 	- investigar si las variables tienen relaciones entre ellas;

 	- dado un gran número de variables, posiblemente relacionadas entre ellas, reducirlas a un número menor de variables, mostrando las posibles relaciones entre las variables originales, para así simplificar el problema y poder sacar conclusiones;

 	- dado un conjunto de datos individuales, asociados con ciertas variables, formar grupos de individuos parecidos usando las variables para clasificarlos.

Veamos a continuación ejemplos y técnicas para estas aplicaciones.

### Reducir el número de variables: análisis de componentes principales

Usaremos el método de análisis de componentes principales; una vez cargados los datos en el entorno R, accedemos a *Estadísticos -> Análisis dimensional -> análisis de componentes principales*. Seleccionamos todas las variables y en Opciones marcamos "*Añadir componentes principales al conjunto de datos*"; cuando nos pregunta cuantos componentes vamos a incluir, estamos diciendo a cuantas variables queremos reducir las 11 originales, pondremos 3 (idealmente reduciremos a 4 como máximo, para que los datos sean manejables), y aceptamos. R efectúa el análisis y nos proporciona este informe:

[caption id="attachment_1667" align="alignnone" width="368"]![multivariant1](/assets/images/multivariant1.png) Fig. 1: Componentes principales: coeficientes de las combinaciones[/caption]
R siempre generará tantos componentes principales como variables originales, 11 en este caso. En la figura 1 no se muestran las columnas 4, 5, ... 11, pues nos interesa estudiar sólo 3. Lo que ha hecho R es crear nuevas variables Comp.1, Comp.2, ..., por combinación lineal de las originales, siendo los coeficientes de las combinaciones los que vemos en la figura 1. O sea que se cumple que:

$Comp.1;=;0.06cdot ASIG;-;0.453cdot ATE;-;0.558cdot CAL;+;...;-;0.187cdot TEC$

Para el componente principal 2:

$Comp.2;=;-0.686cdot ASIG;-;0.012cdot ATE;+;0.029cdot CAL;+;...;;+0.264cdot TEC$

etc. En el mismo informe de R encontramos esta otra sección:

[caption id="attachment_1670" align="alignnone" width="466"]![Fig. 2: importancia de cada componente principal](/assets/images/multivariant2.png) Fig. 2: importancia de cada componente principal[/caption]
Nos fijamos en la fila *Cumulative Proportion*: nos da la "representatividad" acumulada de las nuevas variables, en tanto por uno; vemos que tomando los tres primeras componentes quedan representados en un 0.50 todas las variables, o en un 50%, por tanto si pasamos de 11 a tres variables perdemos la mitad de la información. Parece una pérdida importante ... si cogemos más componentes principales, perdemos menos información, pero ampliamos de nuevo el número de variables, por ejemplo ampliando a 5 llegamos al 69% de representatividad, con 6 llegamos al 77% y con 7 componentes cubrimos hasta el 85% de la información original, pero la reducción de número de variables es ya escasa:

[caption id="attachment_1671" align="alignnone" width="559"]![Fig. 3: ampliando el número de componentes con los que trabajar](/assets/images/multivariant3.png) Fig. 3: ampliando el número de componentes con los que trabajar[/caption]
La elección del número de componentes principales con los que trabajar es una elección del experimentador; los problemas "de clase" suelen venir preparados de forma que con pocos componentes principales, 2 o 3, se resumen bien los datos, pero en los problemas reales no suele ser tan evidente.

Para saber cómo se relacionan las nuevas variables con las originales podemos usar la **matriz de correlaciones entre pares de variables**: en R haremos *Estadísticos -> Resúmenes -> Matriz de correlación*, escogemos todas las variables, y marcamos la opción *Parejas de datos*. En la matriz de correlaciones resultante nos fijamos en la columna correspondiente al componente principal PC1, para el cual las correlaciones son:

 

|  
| **PC1** 

| ASIG 
| 0.009634422 

| ATE 
| -0.690929281 

| CAL 
| -0.8508779590 

| CLA 
| 0.0891672163 

| EDAD 
| 0.233171700 

| EST 
| -0.67173527 

| ESTP 
| 0.093915413 

| PAR 
| -0.712555990 

| PC1 
| 1.000000e+00 

| PC2 
| 1.006389e-17 

| PC3 
| -5.316147e-17 

| PROF 
| 0.006182726 

| SAT 
| -0.120799459 

| TEC 
| -0.28527228 

Analizemos estas correlaciones: vemos que PC1 está fuertemente correlacionada (más de un 0,5 por uno, o 50%) con las variables ATE (Medida de la atención en clase, valor negativo), CAL (Calificación obtenida, valor negativo, es la correlación más fuerte), EST (Medida de las técnicas de estudio personales, valor negativo) y PAR (Medida de la participación activa en clase, valor negativo), débilmente correlacionada (entre 10-50%) con EDAD (valor positivo), SAT (Medida de la satisfacción en clase, valor negativo) y TEC (1: aplicamos nueva técnica, 0: no lo hacemos, con valores negativos), y prácticamente nada con las demás.

Los valores negativos de correlación indican que si aumentan esas variables disminuye PC1, y viceversa. A la vista de estas correlaciones podemos interpretar que los valores reducidos de PC1 se consiguen sobre todo con valores altos de atención en clase, técnicas de estudio personales y participación activa en clase, y más marginalmente con la elevada satisfacción en clase y la aplicación de la nueva técnica de estudio, de forma que podemos relacionar valores altos de PC1 con la la falta de buenos hábitos (atención en clase, técnicas de estudio, participación activa)  y bajas calificaciones; la edad tiene signo contrario. a más edad más valor de PC1, y peores resultados. Hay que recordar que PC1 sólo recoge un 21% de la información original (figura 2). Si tuviéramos que dar un nombre a PC1, podría ser "altas calificaciones y buenos hábitos de estudio". El mismo análisis se haría para los componentes PC2 y PC3: PC2 tiene un -0.97 de correlación con la variable ASIG (asignatura) y con las demás variables casi es nula, por tanto PC2 viene a representar a ASIG. En cuanto a PC3 tiene -0.65 con ESTP (nivel de estudios padres) y 0.38 con CLA (clase social), o sea que se relaciona con la familia del estudiante.

Recordar que este método produce variables (los componentes principales) que, a diferencia de las variables originales, no estan correlacionadas entre sí; por ejemplo, el **diagrama de dispersión** de PC1-PC2 no muestra ninguna tendencia:

[caption id="attachment_1674" align="alignnone" width="410"]![Fig. 5: de diagrama de dispersión de dos componentes principales cualesquiera no mostrará ninguna relación](/assets/images/multivariant5.png) Fig. 4: de diagrama de dispersión de dos componentes principales cualesquiera no mostrará ninguna relación[/caption]
Hemos podido realizar este diagrama de dispersión gracias a haber seleccionado la opción  , que añade a la hoja de datos original las nuevas variables como columnas adicionales.

[caption id="attachment_1677" align="alignnone" width="576"]![Fig. 5: R añade 3 nuevas columnas a la hoja de datos, son los componentes principales elegidos por el usuario](/assets/images/multivariant6.png) Fig. 5: R añade 3 nuevas columnas a la hoja de datos, son los componentes principales elegidos por el usuario[/caption]
Como conclusión de este estudio con componentes principales podemos decir:

*la nueva técnica de enseñanza sí que parece tener cierta influencia, pues su variable asociada está incluida en el componente PC1 de "buenas prácticas y buenas calificaciones", aunque su efecto parece ser menor (29% de correlación) en comparación a las otras buenas prácticas: atención en clase, etc. Por otro lado la asignatura donde se ha probado el método, que es el componente PC2, no tiene ninguna relación (no hay correlación) con PC1, esto es bueno, nos dice que en cualquier asignatura las "buenas prácticas" tienen los mismos efectos. Lo mismo podemos decir del entorno familiar, representado por PC3.*

### Reducir el número de variables: análisis factorial

El análisis factorial es otra técnica diseñada para reducir el número de variables, creando unas de nuevas, llamadas factores, por combinación lineales de las originales, que intentan mostrar condiciones que directamente no son fácilmente reconocibles. El software estadístico de análisis factorial permite realizar las llamadas "rotaciones" de variables, una transformación matemática que pretende simplificar al máximo la nueva descripción de variables. Los resultados no son los mismos que usando componentes principales, pues el método matemático es distinto.

En R, vamos a *Estadísticos -> Análisis dimensional -> Análisis factorial*, y escogemos todas las variables originales del problema. Nos pregunta el número de factores a retener, probamos con 3. El resultado es este resumen:

Uniquenesses:
 ASIG   ATE   CAL   CLA  EDAD   EST  ESTP   PAR  PROF   SAT   TEC 
0.077 0.541 0.262 0.983 0.952 0.722 0.986 0.293 0.005 0.995 0.956 

Loadings:
     Factor1 Factor2 Factor3
ASIG  **0.961**                 
ATE           **0.672**         
CAL           **0.769**   0.381 
CLA                  -0.116 
EDAD                 -0.198 
EST           0.456   0.258 
ESTP                        
PAR           0.289   **0.789** 
PROF  **0.997**                 
SAT                         
TEC                   0.158 

               Factor1 Factor2 Factor3
SS loadings      1.947   1.356   0.925
Proportion Var   0.177   0.123   0.084
Cumulative Var   0.177   0.300   0.384

Test of the hypothesis that 3 factors are sufficient.
The chi square statistic is 22.73 on 25 degrees of freedom.
The p-value is 0.593
Nos proporciona los coeficientes de las combinaciones lineales para cada factor (tabla *Loadings*) que siempre están en el intervalo [-1, 1], la variabilidad explicada por cada factor, la acumulada (para los tres factores sumados tenemos un 38.4% de variabilidad explicada) y un contraste de hipótesis Chi² donde H0: los tres factores son suficientes, H1: no lo son. Vemos que el resultado del contraste es que el p-valor = 0.593, lo que significa que, para los niveles de significación estándar de aceptación de H0,  10%, 5% y 1%, aceptamos H0 (recordemos que H0 se acepta si la significación es menor que el p-valor). Si se hubiera rechazado la hipótesis nula, hubiéramos repetido el análisis con un factor más.

También, para las conclusiones, podemos mirar los datos denominados "*Uniquenesses*": nos da la proporción de variabilidad no explicada por los factores de la variable en cuestión. Por ejemplo, para la variable ASIG es de 0.077, un 7.7% no explicada por los factores, o sea que está bien resumida con los tres factores. En cambio para CLA vale más del 90%, por lo cual los factores no informan bien de esta variable. También los coeficientes (en valor absoluto) de las combinaciones lineales nos informan de la importancia de cada variable en la composición del factor: entre 0% y 100%; por ello hemos destacado en negrita los coeficientes más importantes (más del 50%).

Así pues, resumimos las 11 variables por tres factores, con la siguiente composición:

 	- $F1 = 0.961· ASIG + 0.997·PROF$; este factor considera la asignatura y el profesor que la imparte como un factor importante en el estudio.

 	- $F2 = 0.672·ATE + 0.769·CAL + 0.456·EST + 0.289·PAR$;este segundo factor tiene en cuenta la atención en clase, la calificación, las técnicas de estudio y la participación activa en clase, de forma parecida al componente principal PC1 del apartado anterior.

 	- $F3 = 0.381·CAL - 0.116·CLA - 0.198·EDAD + 0.258·EST + 0.789·PAR + 0.158·TEC$; el tercer factor considera la relación entre calificación, clase social, edad, técnicas de estudio, participación activa en clase y la aplicación de la nueva técnica de estudio, en éste último caso con un peso más bien bajo, 0.158.

Las conclusiones que podemos obtener son:

*en este análisis la variable TEC que estudiamos no parece desempeñar ningún papel, sólo entra en el factor 3 con un peso del 15.8%, y además queda no explicada en un 95.6% (Uniquenesses). Las variables relacionadas que tienen más peso son CAL y ATE en el factor 2, lo que sugiere que la atención en clase es la variable mas correlacionada con la calificación obtenida; en el factor 3 la variable dominante es PAR, participación activa, que tiene una relación más bien débil con la calificación (38.1%) y aún más débil con las otras variables.*