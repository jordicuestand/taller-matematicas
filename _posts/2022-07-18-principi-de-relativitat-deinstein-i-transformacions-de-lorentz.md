---
layout: post
title: "Principi de Relativitat d'Einstein i Transformacions de Lorentz"
date: 2022-07-18 11:16:20 +0000
categories:
  - "Fí­sica"
  - "Mecánica relativista"
tags:
  - "Lorentz"
  - "Minkowski"
  - "Principi de Relativitat d&#039;Einstein"
  - "tensor"
math: true
---
{% raw %}

En aquest article exposem les bases de la Teoria de la Relativitat Especial tal com va ser concebuda per Einstein, seguint la seva exposició del llibre "El significado de la Relatividad" editat a Espanya per Espasa-Calpe. No és una exposició simple tal com es dona en els primers cursos dels graus, va al fons de la qüestió de la naturalesa de l'espai i del temps. 

## L'escenari espai i temps clàssics

La Mecànica Clàssica estudia els moviments en l'espai tridimensional i el temps unidimensional, un espai modelat per un conjunt infinit de punts als que podem assignar *una posició *descrita per tres coordenades, una per cada dimensió de l'espai, i un temps modelat per un nombre real que es va incrementant al mateix ritme en tot l'espai; si la posició canvia a mesura que el temps avança el punt està en moviment. La posició coordenada de cada punt cal prendre-la a partir d'una posició de referència que en principi es considera fixa i s'anomena *orígen de coordenades*. Podem prendre qualsevol punt *O* com a referència i partir de ell definir qualsevol sistema d'assignació de les coordenades, amb la qual cosa tindrem definit una *referència coordenada*; segons els sistema triat, les coordenades d'un punt qualsevol fix $x_1,x_2,x_3$ en l'espai seran diferents, però sempre podrem convertir les coordenades donades en un sistema *O* en un altre *O'* usant *equacions de canvi de coordenades*. 

## Coordenades cartesianes, canvis de coordenades i intervals

En un espai euclidià es compleixen els [postulats de Euclides](https://ca.wikipedia.org/wiki/Geometria_euclidiana#Les_nocions_comunes_i_els_postulats_d), En aquest espai de forma antural es defineixen les coordenades cartesianes per com tres eixos perpendiculars entre sí que es tallen en un punt orígen O; les coordenades de qualsevol punt P són les projeccions en cada eix del segment OP. 

Imaginem un cos rígid (no elàstic, de dimensions i forma estàtiques) en l'espai; el segment de recta que uneix dos qualsevol dels seus punts P, Q tindrà una longitud i una orientació en l'espai també fixa, però els dos punts extrems tindran coordenades diferents segons la referència triada.

**Propietat** (no la demostrem): si independentment de la orientació del interval la seva longitud és sempre la mateixa, llavors la *referència és euclidiana* i les *coordenades són cartesianes*. En aquest cas la suma de diferencies de coordenades entre els dos punts P, Q del interval, que serà igual a la longitud al quadrat del interval, és independent de la referència.


$s^2=\left(x_{1P}-x_{1Q}\right)^2+\left(x_{2P}-x_{2Q}\right)^2+\left(x_{3P}-x_{3Q}\right)^2=\triangle{x^2}_1+\triangle{x^2}_2+\triangle{x^2}_3$


Els canvis de coordenades poden ser del tipus translació dels eixos, rotació dels eixos, o canvi d'escala; en el que segueix suposem que definim un segment unitari per tots els sistemes, així que tot canvi serà de translació i/o de rotació. Considerem ara quisns canvis de coordenades cartesianes produexen altres coordenades cartetesianes, i ho fem usant el fet de que els intervals han de tenir la mateixa longitud en qualsevol sistema, sent aquesta suma de diferències al quadrat: $\sum_\nu\triangle x_\nu^2=r^2$; en una altre referència R' la expressió és la mateixa, $\sum_\nu\triangle{x'_\nu}^2=r^2$.

Expressem ara les x' com funcions derivables de les x, x'(x), i les desenvolupem en sèrie de Taylor: 

$$\begin{equation} \label{eq:poly}\triangle x'_\nu={\textstyle\sum_\alpha}\frac{\partial x_\nu'}{\partial x_\alpha}\triangle x_\alpha+\frac12{\textstyle\sum_{\alpha\beta}}\frac{\partial^2x_\nu'}{\partial x_\alpha\partial x_\beta}\triangle x_\alpha\triangle x_\beta+\dots\end{equation}$$

Per veure que això és així considerem una funció f tal que x'=f(x), i un punt intermedi a dins l'interval $(x_2. x_1)$; desenvolupant f(x) al voltant del punt a (i suposant que el interval és petit):

$f\left(x_2\right)={\textstyle\sum_\alpha}\frac{\partial f\left(a\right)}{\partial x_\alpha}\left(x_2-a\right)+\cdots;\\f\left(x_1\right)={\textstyle\sum_\alpha}\frac{\partial f\left(a\right)}{\partial x_\alpha}\left(x_1-a\right)+\cdots;\\\triangle x'=f\left(x_2\right)-f\left(x_1\right)=\sum_\alpha\frac{\partial f\left(a\right)}{\partial x_\alpha}\left(x_2-a-x_1+a\right)+\dots=\sum_\alpha\frac{\partial f\left(a\right)}{\partial x_\alpha}\triangle x+\cdots$ 

Si substituïm aquesta expressió dels intervals en la expressió del interval x' i la igualem a la del interval  amb x, doncs totes dues són iguals a la longitud del segment, obtenim una equació que s'hauria de complir sempre, per tota funció x'(x) que relacioni les x' amb les x:

${\textstyle\sum_\nu}\left(\triangle x'_\nu\right)^2={\textstyle\sum_\nu}\left${\textstyle\sum_\alpha}\frac{\partial x_\nu'}{\partial x_\alpha}\triangle x_\alpha+\frac12{\textstyle\sum_{\alpha\beta}}\frac{\partial^2x_\nu'}{\partial x_\alpha\partial x_\beta}\triangle x_\alpha\triangle x_\beta+\dots\right$^2$

La condició de que aquesta equació es compleixi  sempre, per tota funció x'(x) que relacioni les x' amb les x, és molt forta, tant, que de seguida veiem que només passarà si la funció x'(x) és ben simple: una relació lineal 

$$\begin{equation}\label{eq:canvi}x'_\nu=x_\nu+{\textstyle\sum_\alpha}b_{\nu\alpha}x_\alpha\end{equation}$$

que en termes de intervals equival a 

$$\begin{equation}\label{eq:canvi2}\triangle x'_\nu={\textstyle\sum_\alpha}b_{\nu\alpha}\triangle x_\alpha\end{equation}$$

Aquestes transformacions lineals de coordenades cartesianes són les úniques que preserven la longitud dels segments. Igualant el quadrat del interval en dos sistemes de coordenades i usant   [1] trobem una relació important:

$s^2={\textstyle\sum_\nu}{\textstyle\triangle}{\textstyle x'_\nu^2}{\textstyle=}\left({\textstyle\sum_\alpha b_{\nu\alpha}\triangle x_\alpha}\right){\textstyle\left(\sum_\beta b_{\nu\beta}\triangle x_\beta\right)}=\\{\textstyle\;}{\textstyle\sum_{\alpha\beta}}{\textstyle b_{\nu\alpha}}{\textstyle b_{\nu\beta}}{\textstyle\triangle}{\textstyle x_\alpha}{\textstyle\triangle}{\textstyle x_\beta}{\textstyle=}{\textstyle\sum_\nu}{\textstyle\triangle}{\textstyle x_\nu^2}{\textstyle\Rightarrow}{\textstyle\boxed{b_{\nu\alpha}b_{\nu\beta}=\delta_{\alpha\beta}}}$ 

La relació  

\begin{equation}\label{eq:ortogonal}b_{\nu\alpha}b_{\nu\beta}=\delta_{\alpha\beta}\end{equation}

utilitza el símbol [delta de Kronecker](https://ca.wikipedia.org/wiki/Delta_de_Kronecker) (recordem que $\delta_{\alpha\beta}=1\;si\;\alpha=\beta,\;0\;altrament$) es diu *condició d'ortogonalitat* del canvi de coordenades, i ens diu que les transformacions lineals de coordenades cartesianes són també *transformacions ortogonals*. 

## Transformació de rectes i de vectors

Considerem l'equació d'una recta en forma paramètrica $P_\nu=Q_\nu+\lambda B_\nu$, on cada punt P de la recta verifica que les seves coordenades són igual a les coordenades d'un punt de referència Q al que sumem lambda vegades el desplaçament del vector director B que suposem unitari; ho podem simplificar escrivint la equació com un interval $\left(P_\nu-Q_\nu\right)=\lambda B_\nu\Leftrightarrow\triangle x_\nu=\lambda B_\nu$ i llavors és fàcil fer el canvi de coordenades a x': multiplicant aquest darrera igualtat per $b_{\beta\nu}$ i sumant per tots els valors  $\nu$ resulta

${\textstyle\sum_\beta}b_{\beta\nu}\triangle x_\nu=\lambda{\textstyle\sum_\beta}{\textstyle b_{\beta\nu}}B_\nu\Leftrightarrow\triangle x'_\nu=\lambda B'_\nu$ 

on hem definit 

${\textstyle B}{\textstyle'_\beta}{\textstyle=}{\textstyle\sum_\nu}{\textstyle b_{\beta\nu}}B_\nu$, 

veiem llavors que* les rectes es transformen sota canvis de coordenades cartesianes com els intervals.*  Això sovint s'expressa com que l*es rectes són **covariants** respecte les transformacions ortogonals lineals de coordenades*.

Pensem ara en un vector com un segment entre dos punts O, P amb un sentit definit; si O és l'orígen de coordenades el vector v = OP té per coordenades les del punt P, altrament seran v = P - O, però en tot xas el vector és un interval amb un sentit, per tant és evident que sota canvis de coordenades cartesianes també es transformarà com ho fan els intervals.

## Tensors

Considerem ara una superfície de 2n grau arbitraria en l'espai euclidià, com ara una esfera o un el·lipsoide, amb centre P; donat un punt Q qualsevol de la superfície, les projeccions $\left(\zeta_1,\zeta_2,\zeta_3\right)$ del segment PQ sobre els eixos coordenats verifiquen una expressió quadràtica com ara

\begin{equation}\label{eq:segongrau}{\textstyle\sum_{}}A_{\mu\nu}\zeta_\mu\zeta_\nu+C=0\Leftrightarrow{\textstyle\sum_{}}{\textstyle a_{\mu\nu}}{\textstyle{\scriptstyle\zeta}_\mu}{\textstyle{\scriptstyle\zeta}_\nu}{\textstyle=}{\textstyle1}{\textstyle,}{\textstyle\;}{\textstyle{\scriptstyle a}_{\mu\nu}}{\textstyle=}{\textstyle{\scriptstyle A}_{\mu\nu}}{\textstyle/}{\textstyle C}\end{equation} 

Per exemple, la expressió x² - 4y² +6z² +xy -yz +3yz = 24 correspon a un hiperboloide d'una fulla, i es pot expressar també com x²/24 - y²/6 +z²/4 +xy/24 -yz/24 +yz/8  =1.

![](/taller-matematicas/assets/images/hiperboloide.gif)Fig. 1: Exemple de superfície de 2n grau

A partir d'ara usarem quan convingui la notació abreviada d'Einstein per els sumatoris:

${\textstyle\sum_{\mu\nu}}{\textstyle a_{\mu\nu}}{\textstyle\zeta_\mu}{\textstyle\zeta_\nu}\equiv{\textstyle a_{\mu\nu}}{\textstyle\zeta_\mu}{\textstyle\zeta_\nu}$

Com es transforma la igualtat (\ref{eq:segongrau}) en un canvi de coordenades cartesianes? Fem el canvi de les coordenades $\zeta$ com fins ara:

$\textstyle1=a_{\mu\nu}\zeta_\mu\zeta_\nu=a_{\mu\nu}\left(\sum_\sigma b_{\sigma\mu}\zeta'_\sigma\right)\cdot\left(\sum_\tau b_{\tau\nu}\zeta'_\nu\right)=\\a_{\mu\nu}b_{\sigma\mu}b_{\tau\nu}\zeta'_\sigma\zeta'_\nu$

El canvi de coordenades hauria de produir una expressió tal com

$a_{'\sigma\tau}\zeta'_\sigma\zeta'_\tau$

per tant

\begin{equation} \label{eq:tensor}{\textstyle{\scriptstyle a}_{'\sigma\tau}}{\textstyle\zeta}{\textstyle{\scriptstyle'}_\sigma}{\textstyle\zeta}{\textstyle{\scriptstyle'}_\tau}{\textstyle=}{\textstyle{\scriptstyle a}_{\mu\nu}}{\textstyle{\scriptstyle b}_{\sigma\mu}}{\textstyle{\scriptstyle b}_{\tau\nu}}{\textstyle\zeta}{\textstyle{\scriptstyle'}_\sigma}{\textstyle\zeta}{\textstyle{\scriptstyle'}_\nu}{\textstyle\Rightarrow}\boxed{\textstyle a_{'\sigma\tau}=a_{\mu\nu}b_{\sigma\mu}b_{\tau\nu}}\end{equation}

Veiem que els nombres $a_{ij}$ que defineixen la superfície de 2n grau canvien sota un canvi de coordenades com (\ref{eq:tensor}), no com els segments o els vectors, ara el canvi té més termes i subíndexs; la transformació (\ref{eq:tensor}) és homogènia (els zeros es converteixen en zeros) i de 1r grau en $a_{ij}$, i els termes $a_{ij}$ diem que defineixen un*** tensor de 2n grau*** (de 2n grau per els dos sistemes de subíndexs).  

## Principi de Relativitat Especial

Les referències en moviment relatiu de translació a velocitat constant (anomenades **referències inercials**) són totes equivalents respecte a les equacions de les lleis de la Física. 

 En el cas de les equacions de Maxwell de l'electromagnetisme, contenen la velocitat *c* de transmissió de les ones electromagnètiques com una característica intrínseca de l'electromagnetisme, independent de la referència; per tant un raig de llum viatjarà a velocitat c "vista" des de qualsevol referència inercial, fins i tot si el focus emissor també és mou! Suposar el contrari contradiu el principi de relativitat: haurien referències inercials on les equacions de Maxwell són diferents. 

El la Física clàssica tenim la **[transformació de Galileu](https://ca.wikipedia.org/wiki/Transformaci%C3%B3_de_Galileu) **per fer el canvi de coordenades entre dos referències K, K' en translació relativa de velocitat v i eixos paral·lels (no rotats):

x' = x - vtt' = t 

Aquesta transformació és covariant amb els intervals s² de la Física clàssica; per exemple per la 2a llei de Newton dx'/dt' = d(x - vt)/dx' =  d(x - vt)/dt · dt/dt' = (dx/dt - v)·1, derivant de nou d²x'/dt² = d²x/dt² i veiem que les acceleracions (i les forces) no varien al canviar de referència.

 Però en canvoi no compleix el principi de relativitat especial; en efecte: en la figura representem les referències K, K', que després d'un temps $t =  t_0 = t'$ estan separades per una distància A, des de la referència K veiem que s'emet llum des del focus F a velocitat c, ens preguntem quina velocitat veurà la referència K', apliquem les transformacions de Galileo identificant x, x' com l'espai recorregut per la llum: x' = x -vt, com x = ct, és x' = ct - vt; derivant respecte del temps t' i recordant que t = t': dx'/dt' = c' = c - v, veiem que des de K' es diu que la llum es mou amb menor velocitat, contradient el P. Relativitat Especial.

![](/taller-matematicas/assets/images/Galileo.png)Fig. 2: Referències inercials paral·leles i emissió de llum

## Constància de c i invariant associat

La constància del interval clàssic $s^2={\textstyle\sum_\nu}\triangle x_\nu^2$ no queda assegurada si hem de imposar la constància de c; això és fàcil de veure: considerem el interval definit per el raig de llum que emet F entre l'instant t = 0 i l'instant $t=t_0$; des de la referència K la longitud s del interval serà simplement $s=ct_0$, quina serà des de K'? La posició de F segons K' retrocedirà una distància $-vt_0$ però com la velocitat de la llum per K' també és c, la longitud s' vista serà $s'=ct_0+vt_0$ per tant K' veurà l'interval més gran que K, o dit al contrari, K mesurarà un interval més curt que K, fenomen conegut com contracció de longitud d'una referència mòbil.

Per tant ens cal definir un altre invariant que estigui d'acord amb la constància de c; pensant que la distància recorreguda per la llum, en qualsevol referència inercial i independentment de la velocitat relativa del foco de llum és $c\triangle t$, s'ha de complir que la longitud segons els eixos cartesians del interval recorregut, ${\textstyle\sum_\nu}\triangle x_\nu^2$ ha de ser igual a $c\triangle t$, per tant:

\begin{equation} \label{eq:invariant}{\textstyle\sum_\nu}\triangle x_\nu^2-c^2\triangle t^2={\textstyle\sum_\nu}{\textstyle\triangle}{\textstyle x_\nu^{'2}}{\textstyle-}{\textstyle c^2}{\textstyle\triangle}{\textstyle t}{\textstyle'^2}{\textstyle=}{\textstyle0}\end{equation}

Les transformacions de coordenades que respecten (\ref{eq:invariant}) les anomenem **transformacions de Lorentz**.

## Espai-temps de Minkowski

Clàssicament es defineix un espai amb coordenades $\left(x_1,x_2,x_3\right)$ que depenen del sistema de coordenades i a banda un temps absolut t que no depén; la constància absoluta de c en canvi substitueix a la de t, que passa a ser depenent també del sistema de coordenades, i per tant el presentem com una coordinada més: $\left(x_1,x_2,x_3,t\right)$, aquest escenari ja no és un espai i un temps, és un **espai-temps**, tot un. En l'espai de tres coordenades (o dimensions) el quadrat de l'interval, que és invariant, s'expressa en cartesianes com ${\textstyle s^2=\sum_\nu}\triangle x_\nu^2$ però veient la expressió  (\ref{eq:invariant}) trobem que la coordenada temps es resta en comptes se sumar-se: [Minkowski](https://en.wikipedia.org/wiki/Hermann_Minkowski) va proposar fer el canvi $x_4=ict$ on "i" és el nombre imaginari $i=\sqrt{-1}\Rightarrow i^2=-1$, llavors:

${\textstyle s^2=\sum_{\nu=1,2,3}}\triangle x_\nu^2-c^2\triangle t^2={\textstyle\sum_{\nu=1,2,3}}\triangle x_\nu^2+\left(ic\triangle t\right)^2={\textstyle\sum_{\nu=1,2,3,4}}{\textstyle\triangle}{\textstyle{\scriptstyle x}_\nu^2}$ 

Per tant podem redefinir el quadrat del interval amb la mateixa forma però ara en l'espai-temps de 4 dimensions, que serà invariant: $s^2={\textstyle\sum_\nu}{\textstyle\triangle}{\textstyle x_\nu^2}$.

El canvi sembla que sigui només afegir una coordenada més, però cal recordar que aquesta és una dimensió *imaginaria*; això porta complicacions i novetats addicionals respecte a l'espai euclidià real de tres dimensions. De fet el incloure nombre imaginaris només és un artifici matemàtic per incloure el comportament del temps com a coordenada al costat de les coordenades espacials.

## Transformacions de Lorentz

Considerem ara les transformacions ortogonals lineals en l'espai de 4 coordinades $x'_nu=a_nu+b_{\nu\alpha}x_\alpha$; poden ser translacions o rotacions. Les translacions no ofereixen novetats, són moviments lineals de l'origen i en el cas de la coordenada temps només impliquen canvis del origen del temps en cada referència. On trobem novetats és en les rotacions. Recordem que una matriu de rotació M és tota matriu tal que $M^T=M,\;det\left(M\right)=1$, com ara la següent matriu que descriu una rotació en torn a l'eix $x_3$ que canvia $x_1, x_2$ i deixa invariant $x_3$ i $x_4$, amb coeficients

![](/taller-matematicas/assets/images/gir_real.png)

![](/taller-matematicas/assets/images/rotacio-real.png)Gir amb eix z d'eixos cartesians, el eix del temps no es representa

Les equacions del canvi de coordenades corresponent a la rotació M són

$\left{\begin{array}{l}x'_1=x_1\cos\left(\varphi\right)-x_2\sin\left(\varphi\right)\x'_2=x_1\sin\left(\varphi\right)+x_2\cos\left(\varphi\right)\x'_3=x_3\x'_4=x_4\end{array}\right.$

Veiem que la coordenada temps és idèntica en les dos referències, com en la Física clàssica. Ara bé, formalment podem pensar en una altre rotació que sí afecti al eix dels temps, com ara aquesta que afecta a les coordenades 1 i 4:

![](/taller-matematicas/assets/images/gir_imaginari.png)

amb equacions de canvi $x'_2=x_2, x'_3=x_3$ que no varien, i les que sí varien:

\begin{equation}  \label{eq:gircomplex}x'_1=x_1\cos\left(\psi\right)-x_4\sin\left(\psi\right)\x'_4=x_1\sin\left(\psi\right)+x_4\cos\left(\psi\right)\end{equation}

Aquest gir és formalment correcte malgrat no es pot representar gràficament, ara bé, què significa físicament? Per que tingui sentit matemàtic hem de imposar la condició de que $x'_4$ sigui un nombre imaginari pur (doncs aquesta coordenada la hem definit així) i que $x'_1$ sigui un nombre real (*condicions de realitat*); això no es compleix amb cap angle de gir real, ha de ser un **angle imaginari**. Fem un repàs breu a aquests angles imaginaris.

### Angles complexos i imaginaris

Un nombre complex *z = a + bi* pot ser considerat un angle complex usant les igualtats

$\cos\left(a+bi\right)=\cos\left(a\right)\cos h\left(b\right)-i\sin\left(a\right)\sin h\left(b\right)\\sin\left(a+bi\right)=\sin\left(a\right)\cos h\left(b\right)+\cos\left(a\right)\sin h\left(b\right)$

on *sinh* i *cosh* són el sinus hiperbòlic i el cosinus hiperbòlic: en el cas d'un z imaginari pur

$\cos\left(bi\right)=\cos h\left(b\right)\\sin\left(bi\right)=i\cdot\sin h\left(b\right)$

Si substituïm l'angle $\psi$ de (\ref{eq:gircomplex}) per $\psi=i\beta$ (un angle imaginari pur), les equacions es transformen usant les propietats dels angles complexos, i veiem que efectivament compleixen les *condicions de realitat*:

$x'_4=x_1\cdot i\sin h\left(\beta\right)+x_4\cos h\left(\beta\right)\;\in\mathbb{C};$, efectivament és un nombre imaginari pur.

$x'_1=x_1\cdot\cos h\left(\beta\right)-x_4\cdot i\sin h\left(\beta\right)\;=\\;x_1\cdot\cos h\left(\beta\right)-ict\cdot i\sin h\left(\beta\right)=\x_1\cdot\cos h\left(\beta\right)+ct\cdot\sin h\left(\beta\right)\;\in\;\mathbb{R}$,efectivament és un nombre real. Però encara no sabem quin significat físic té aquest gir imaginari de l'espai-temps quadridimensional. 

### Significat físic de la rotació imaginaria d'eixos

Per definició $x'_4=ict'=il'$ on l' és el *temps-llum*; equivalentment $l'=x'_4/i=-ix'_4$ per les propietats del nombre imaginari i; substituint l'expressió per $x'_4$ donada per (\ref{eq:gircomplex}):

$l'=-i\left(x_1\sin\left(\psi\right)+il\cos\left(\psi\right)\right)=-ix_1\sin\left(\psi\right)+l\cos\left(\psi\right)$

Anem a veure a continuació que aquest gir imaginari representa un moviment de translació de K respecte de K' com el de la figura 2, això és, un moviment a velocitat constant v paral·lel a l'eix $x_1$. Situem-nos ara en el orígen O' de coordenades de la referència K', tindrem $x'_{O'1}=0$, aplicant el canvi de coordenades del gir:

$0=x'{O'1}=x{O'1}\cos\left(\psi\right)-x_4\sin\left(\psi\right)=x_{O'1}\cos\left(\psi\right)-ict\cdot\sin\left(\psi\right)$

Derivem respecte el temps la expressió anterior:

$\frac{\partial x'{O'1}}{\partial t}=\frac\partial{\partial t}\left(x{O'1}\cos\left(\psi\right)-ict\cdot\sin\left(\psi\right)\right)=v\cos\left(\psi\right)-ic\cdot\sin\left(\psi\right)=0$

on hem dit v a la derivada respecte al temps t de la referencia K del punt O' orígen de la referència K'.   Veiem que

$v=ic\cdot\frac{\sin\left(\psi\right)}{\cos\left(\psi\right)}=ic\cdot\tan\left(\psi\right)$

com c no és zero i la tangent d'un angle només s'anul·la si l'angle és zero, veiem que aquesta velocitat v és no nul·la, i per tant tenim una translació de la referència K' respecte a la K a velocitat v tal com hem dit.  

Situem-nos ara en el orígen O' de coordenades de la referència K' que es mou a la velocitat v respecte K, en la qual ha de ser $x'_{O'1}=0$; en la referència K serà $x_{O'1}=vt$. Usant aquestes igualtats en la expressió de $x'_{O'1}$ donada per  (\ref{eq:gircomplex}):

$x'_{O'1}=vt\cdot\cos\left(\psi\right)-il\cdot\sin\left(\psi\right)=0$

Definim ara la velocitat relativa a c, $\widetilde v=v/c$, com $l=ct$ implica que $vt=\widetilde v \cdot ct =\widetilde v \cdot l$, substituïm en la darrera expressió:

$\widetilde vl\cdot\cos\left(\psi\right)-il\cdot\sin\left(\psi\right)=0\Rightarrow\widetilde  v\cdot\cos\left(\psi\right)-i\cdot\sin\left(\psi\right)=0\Rightarrow\widetilde  v=i\cdot\tan\left(\psi\right)$

i per tant,

$\tan\left(\psi\right)=\widetilde v/i=-i\cdot\widetilde v=\frac{\sin\left(\psi\right)}{\cos\left(\psi\right)}\Rightarrow\sin\left(\psi\right)=-i\cdot\widetilde v\cdot\cos\left(\psi\right)$

Com sin²(A) + cos²(A) = 1 per tot angle A,

$\left(-i\cdot\widetilde v\cdot\cos\left(\psi\right)\right)^2+\cos^2\left(\psi\right)=1\Rightarrow\left(-\widetilde v^2+1\right)\cos^2\left(\psi\right)=1\Rightarrow\\cos\left(\psi\right)=\frac1{\sqrt{1-\widetilde v^2}}$

De seguida podem deduir que

$\sin\left(\psi\right)=\frac{-i\widetilde v}{\sqrt{1-\widetilde v^2}}$

 i usant aquestes igualtats trigonomètriques en (\ref{eq:gircomplex}):

$x'_1=\frac{x_1-\widetilde{vl}}{\sqrt{1-\widetilde v^2}},\;l'=\frac{l-v\cdot{\widetilde x}_1}{\sqrt{1-\widetilde v^2}},\;x'_2=x_2,\;x'_3=x_3$

que són les ***equacions de la transformació especial de Lorentz***; hem vist que es dedueixen d'un gir imaginari en el 4-espai de Minkowski. La interpretació física és que per complir el Principi de Relativitat Especial cal que un a translació a velocitat constant v de la referència K' respecte a la referència K en la direcció d'un eix imposi un canvi de la escala del temps i de l'espai mesurat al llarg de l'eix, un resultat ben diferent del que exposa la Física clàssica. En particular fixem-nos que la expressió 

$\frac1{\sqrt{1-\widetilde v^2}}$

 ens obliga a només admetre velocitats v menors o iguals que c per obtenir coordenades reals, i per tant ens diu que la velocitat *c és una velocitat límit que no pot ser superada*. 

## Equacions de Maxwell i Relativitat Especial

L'article original d'Einstein que va publicar per primer cop les idees de la Relativitat Especial tenia per títol "*Sobre l'electrodinàmica dels cossos en moviment*", així que no podem passar per alt la relació entre l'electromagnetisme i la Relativitat Especial. Les **equacions de Maxwell **expliquen tots els fenomens electromagnètics, des de la electrostàtica passant pel magnetisme fins la propagació d'ones electromagnètiques, i en la seva versió original són equacions diferencials vectorials que es pot demostrar que són invariants Lorentz, malgrat no és evident. Podem convertir aquestes equacions en covariants explícites passant dels vectors de tres dimensions (i el temps per separat, a la manera clàssica) als quadrivectors on el temps és la quarta component, i dels vectors als tensors. Em vist abans que un quadrivector es pot considerar com un tensor de rang 1, també hem de tenir en compte algunes propietats de la diferenciació de tensors de rang 1 com ara el fet de que la divergència d'un tensor de grau 2 és un tensor de grau 1 (un quadrivector). Recordar també que el vector camp magnètic en realitat no ho és de vector, doncs és el producte vectorial de dos vectors $\overrightarrow B=\overrightarrow\nabla\times\overrightarrow A$ on $\overrightarrow\nabla$ és l'operador vectorial 'laplaciana' i $\overrightarrow A$ és el potencial vector elèctric; el producte vectorial de dos vectors no és un vector, això és: no es transforma sota un canvi de coordenades com un vector, és de fet un *pseudovector* o *vector axial* (mentre que els vectors habituals són *vectors polars*), veure per exemple [Vectores en Física]({{ '/2016/08/11/v/' | relative_url }}ectores/) en aquest mateix blog. Les equacions de l'electromagnetisme en forma de tensors simplifiquen aquestes diferencies entre vectors polars i axials i a més a més són clarament covariants.

## Equació de continuïtat elèctrica tensorial

La equació de continuïtat elèctrica es relaciona el canvi temporal de densitat de càrrega en cada punt de l'espai amb la variació de la intensitat de corrent elèctrica, i formalment és $\frac{\partial\rho}{\partial t}=-\overrightarrow\nabla\cdot\overrightarrow J$ on $\rho$ és la densitat de càrrega i J la intensitat de corrent (un vector); el producte escalar de l'operador vectorial nabla i del vector J és un escalar (un camp escalar per ser exactes). 

Definim el **quadrivector corrent-càrrega **com $J_\mu=\left$\overrightarrow J;ic\rho\right$$ on usem la notació tensorial (tensor d'ordre 1), recordant que els quadrivectors relativistes tenen tres components de tipus espai i el quart component de tipus temps, veiem que el vector intensitat de corrent correspon a les components de tipus espai i la densitat de corrent a la de tipus temps (amb la convenció de Minkowski de multiplicar per el nombre imaginar i). Usant aquest quadrivector veiem que:

$\frac{\partial J_\mu}{\partial x_\mu}=\left(\frac{\partial J_1}{\partial x_1}+\frac{\partial J_2}{\partial x_2}+\frac{\partial J_3}{\partial x_3}\right)+\frac{\partial\left(ic\rho\right)}{\partial\left(ict\right)}=\boxed{\nabla\cdot\overrightarrow J+\frac{\partial\rho}{\partial t}=0}$

que és la *equació de continuïtat elèctrica en forma tensorial*. 

## Potencials elèctrics en forma tensorial

El potencial escalar, el potencial vectorial, i les densitats de càrrega i de corrent estan relacionades clàssicament per dues equacions, una vectorial i l'altre escalar:

$\Delta^2\overrightarrow A-\frac1{c^2}\frac{\partial^2\overrightarrow A}{\partial t^2}=-\frac{4\mathrm\pi}c\overrightarrow J;\;\Delta^2\phi-\frac1{c^2}\frac{\partial^2\phi}{\partial t^2}=-4\pi\rho$.

Definim el **quadrivector potencial elèctric** $A_\mu=\left$\overrightarrow A;i\phi\right$$; veiem com es transformen les dues equacions clàssiques dels potencials escalar i vectorial: per fer-ho definim *l'operador diferencial tensorial* $\square^2=\Delta^2+\frac{\partial^2}{\partial\left(ict\right)^2}=\Delta^2-\frac1{c^2}\frac{\partial^2}{\partial t^2}$. Apliquem aquest operador al quadrivector potencial:

$\square^2A_\mu=\left(\Delta^2\overrightarrow A-\frac1{c^2}\frac{\partial^2\overrightarrow A}{\partial t^2}\right)+\left(\Delta^2\phi-\frac1{c^2}\frac{\partial^2\phi}{\partial t^2}\right)$

Usem ara les igualtats dels potencials en la darrera expressió:

$\Delta^2\overrightarrow A-\frac1{c^2}\frac{\partial^2\overrightarrow A}{\partial t^2}=-\frac{4\mathrm\pi}c\overrightarrow J;i\left(\Delta^2\phi-\frac1{c^2}\frac{\partial^2\phi}{\partial t^2}\right)=-4\mathrm{πρi}\Rightarrow$

i ens queda una expressió molt compacte *equivalent a les dues igualtats clàssiques dels potencials*:

$\square^2{\mathrm A}_{\mathrm\mu}=-4\mathrm\pi\left(\frac1{\mathrm c}\overrightarrow{\mathrm J}+\mathrm{iρ}\right)\Rightarrow\square^2{\mathrm A}_{\mathrm\mu}=-\frac{4\mathrm\pi}{\mathrm c}\left(\overrightarrow{\mathrm J}+\mathrm{icρ}\right)\Rightarrow\boxed{\square^2{\mathrm A}_{\mathrm\mu}=-\frac{4\mathrm\pi}{\mathrm c}{\mathrm J}_{\mathrm\mu}}$.

## Camps elèctric i magnètic com a quadrivectors

Expressem ara els camps vectorials elèctric i magnètic en funció dels potencials vector i escalar:

$\overrightarrow E=-\nabla\phi-\frac1c\frac{\partial\overrightarrow A}{\partial t};\;\overrightarrow B=\nabla\times\overrightarrow A$.

Utilitzem el quadrivector potencial $A_\mu=\left$\overrightarrow A;i\phi\right$$ per convertir les expressions vectorials en quadrivectorials; comencem per el camp E, per simplificar ens limitem a considerar només la primera component:

$\frac{\partial A_1}{\partial t}=\frac{\partial A_1}{\partial\left({\displaystyle\frac{x_4}i}\right)}=i\frac{\partial A_1}{\partial x_4};\;\frac{\partial\phi}{\partial x_1}=\frac{\partial\left({\displaystyle\frac{A_4}i}\right)}{\partial x_1}=-i\frac{\partial A_4}{\partial x_1}$,

per tant,

$E_1=i\frac{\partial A_4}{\partial x_1}-\frac1c\frac{\partial A_1}{\partial x_4}\Rightarrow i\cdot E_1=-\frac{\partial A_4}{\partial x_1}+\frac1c\frac{\partial A_1}{\partial x_4}$

Passem al vector B, només la 1a component, que traiem directament del producte vectorial:

$B_1=\frac{\partial A_3}{\partial x_2}-\frac{\partial A_2}{\partial x_2}$

Veiem que les components dels camps E i B en notació quadridimensional tenen una estructura molt semblant mentre que la vectorial en canvi eren ben diferents; és un dels avantatges de "relativitzar" les equacions de l'electromagnetisme, que permeten presentar formalment els camps E i B com part d'un mateix fenomen. Si fem el desenvolupament amb la resta de components dels camps veurem  que també segueixen la mateixa estructura $\frac{\partial A_\nu}{\partial x_\mu}-\frac{\partial A_\mu}{\partial x_\nu}$, que ens permet definir el **tensor del camp electromagnètic**:

$F_{\mu\nu}=\frac{\partial A_\nu}{\partial x_\mu}-\frac{\partial A_\mu}{\partial x_\nu}$

que és un tensor antisimétric ($F_{\mu\nu}=F_{\nu\mu}=$) amb zeros a la diagonal ($F_{\mu\mu}=0$). Exemples: 

$F_{23}=\frac{\partial A_3}{\partial x_2}-\frac{\partial A_2}{\partial x_3}=B_1;\;F_{11}=\frac{\partial A_1}{\partial x_1}-\frac{\partial A_1}{\partial x_1}=0;\;F_{32}=\frac{\partial A_2}{\partial x_3}-\frac{\partial A_3}{\partial x_2}=-B_1$

 Les components del tensor són (veure per exemple *Electrodinàmica Clàssica - Jackson*): 

![](/taller-matematicas/assets/images/tensor-electromagnetic.png)

## Equacions de Maxwell amb quadrivectors i tensors

Usant tot el vist en els apartats anteriors pot demostrar-se ( veure per exemple *Electrodinàmica Clàssica - Jackson*) que les quatre equacions vectorials de Maxwell es redueixen a dues tensorials:


$\frac{\partial F_{\mu\nu}}{\partial x_\nu}=\frac{4\pi}cJ_\mu;\;\frac{\partial F_{\mu\nu}}{\partial x_\lambda}+\frac{\partial F_{\lambda\mu}}{\partial x_\nu}+\frac{\partial F_{\nu\lambda}}{\partial x_\mu}=0$
{% endraw %}

