---
layout: post
title: "Ordinary Differential Equations: Introduction"
date: 2015-02-12 13:12:12 +0000
categories:
  - "Mathematics"
math: true
---
{% raw %}

## Motivation

The equations studied in Algebra, such as $x^{3}+7x^{2}+41=0$,
they express static numerical relationships, and their solution is numbers that fulfill the equation. Now, the most interesting natural phenomena involve dynamic relationships and are best expressed with relationships between variable quantities, that is, with equations that are not static, but express variations and relationships between changing magnitudes: they are the differential equations.

Recall that the derivative of a function $dy/dt=f&#39;(t)$ can be interpreted as the proportion of change of the dependent variable $y$ with respect to the changes in the dependent variable $t$. That is why equations describing changes use derivatives of functions.

***Definition 1**: An equation containing an unknown function and one or more of its derivatives is called a **differential equation**. By solving it, we get functions $y = f(x)$ that verify the equation. If the function has only one independent variable, the equation is called the **ordinary differential equation**. If the function depends on two or more variables, the derivatives will be partial and the equation is called **the partial differential equation**. The order of a differential equation is that of the highest derivative that appears in the equation*.

In this post we will only introduce ordinary differential equations, giving some definitions, and solving the most immediate ones.

**Example 1**: The variation of the temperature *T* of a body with respect to time is proportional to the difference $(T-A)$ where *A* is the temperature of the environment ([Newton's cooling law](http://es.wikipedia.org/wiki/Enfriamiento_newtoniano)). The physical law is represented by a first-order ordinary differential equation (EDO of order 1):

$frac{dT}{dt}=kleft(T-Aright)$

**Example 2**: The variation with respect to the time of a population $P(t)$ with constant rates of birth and mortality is proportional to the size of the population, and is also an EDO of order 1:

$frac{dP}{dt}=kP$

**Example 3**: [Torricelli's law](http://es.wikipedia.org/wiki/Teorema_de_Torricelli) states that the variation with respect to the time of volume *V* of water in a tank being emptied is proportional to the square root of the depth *and* water of the reservoir:

$frac{dV}{dt}=-ky^{1/2}$

**Example 4**: The distance $x(t)$ traveled in the accelerated motion of a mass body *m* subjected to a variable force $F(t)$ is given by an EDO of order 2:

$frac{d^{2}x}{dt}=frac{F(t)}{m}$

**Definition 2**: *A function $y = f(x)$ is called **a solution of a differential equation** if the equation is fulfilled when $y$ and its derivatives are replaced by $f(x)$ and their derivatives, respectively. A **particular solution** of a differential equation is any solution that is obtained by assigning concrete values to the constants in the general solution. In practice, particular solutions are obtained from initial conditions that provide the value of the dependent variable or any of its derivatives for a particular value of the independent variable.*

**Example 5**: of the differential equation $y&#39;&#39;-y=0$ are solutions: a) $y=sin(x)$, b) $y=4e^{-x}$  c) $y=Ce^{-x}$ for any real *C* value. Solution (b) is a particular solution obtained from general solution (c). Although less obvious, also solution a) is a particular solution obtained from the general solution (it can be seen using Taylor's developments of the exponential function and the sine function).
### Bundle of curves and first-order differential equations

Another way to introduce differential equations is from the geometric point of view. Consider the graph of the function $y=Cx^2$ for all possible real values of *C*. The image represents the values *C=1, 2, 4, 8*.

$caption id="attachment_847" align="alignnone" width="497"$[![Curve beam y=Cx²](/taller-matematicas/assets/images/feix_corbes.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/02/feix_corbes.png) Curve beam y=Cx²
A **bundle of plane curves** is the set of all curves that are graphs of a general function $y=F(x,C)$. When we give *C* all possible values, the generated curves fill an *R* region of the plane; in the case of the image above that region is the entire upper half-plane $xinleft(-infty,inftyright),;yinleft[0,inftyright).$ In general the *R* region will depend on the beam.

We ask ourselves now: for each point $(x,y)$ of the plane there will be a single value *C* such that it defines us unequivocally the function $y=F(x,C)$ that passes through that point? We can put it in these terms: fixing $x=x_0$ the function *F* becomes dependent only on *C*: $y=F(x_0,C)=f(C)$; For each value of *and* will there be a unique value of *C*? This will be the case as long as the function *f* is strictly increasing or decreasing in *R*, and that will happen when its derivative is not overridden: $frac{operatorname df}{operatorname dC}neq0$. In this case it is as if we had another function $C=psi(x,y)$ of two variables that determines *C* for each point in the plane.

In the example of the previous image, fixing $x=x_0$ any we obtain $y=f(C)=Cx_0^2, f&#39;(C)=x_0^2$, this value is always non-zero except in the origin of coordinates, therefore for the beam $y=Cx^2$ we have uniqueness in the sense that given a $left(x, yright)neqleft(0,0right)$ there is a single value $C=psi(x,y)=y/x^2$ that determines the curve that passes through that point; by the origin $(0,0)$ instead all the curves of the beam pass.

If we derive the equation from the beam we obtain $y&#39;=2Cx$, then, substituting the previous value $C=psi(x,y)$ we eliminate *the C* to obtain: $y&#39;=2Cx=2left(frac y{x^2}right)x=frac{2y}x$, which is **the differential equation of the bundle of curves, **which is a first-order equation.

**Example 6**: Find the differential equation of the plane curved beam $y=Csin(x).$

The R region is the union of the +X+Y and -X-Y quadrants, some curves are shown in the figure.

$caption id="attachment_848" align="alignnone" width="503"$[![Beam of curves y=C·Sin(x)](/taller-matematicas/assets/images/feix_corbes1.png)](http://tallermatematic.eu/wp/wp-content/uploads/2015/02/feix_corbes1.png) Beam of curves y=C·Sin(x)

Setting $x=x_0$ any we get $y=Csinleft(x_0right)=fleft(Cright);f&#39;left(Cright)=sinleft(x_0right)$. This value will be zero whenever $x_0=kmathrmpi,;mathrm k=0,1,dots.$ In this set of points all the curves of the beam coincide, and in the rest of the points we have uniqueness: a single curve for each point, given by: $C=frac y{sinleft(xright)}=psi(x,y)$.

Deriving the equation of the beam: $y&#39;=Ccdotcosleft(xright).$ We substitute the value of *C*:

$left.begin{array}{r}y&#39;=Ccdotcosleft(xright)\C=frac y{sinleft(xright)}end{array}right}Rightarrow y&#39;=frac{ycosleft(xright)}{sinleft(xright)}=frac y{tanleft(xright)}$
***Definition 2**: The beam of curves $y=f(C,x)$ is the **general solution of the ordinary differential equation**; if we fix a value of $C=C_0$, we obtain a single curve of the beam, which we call **the particular solution of the ordinary differential equation**.*

**Example 7**: The curve beam $y=Csin(x)$ is the general solution of the differential equation $y&#39;=frac y{tanleft(xright)}$. By the point $left(frac{mathrmpi}2,3right)$ passes a single curve, $y=3Sin(x)$, which is a particular solution of the differential equation.

### Existence and uniqueness of the solution of a first-order differential equation

We have seen that to obtain the differential equation of a beam of curves you have to derive and eliminate the constant. We now pose the inverse problem: given any differential equation, is there "its" bundle of curves as we have defined it? The following theorem answers us for the case of first-order equations.

**Theorem 1**: **existence and uniqueness**. If we have a differential equation given in the form $y&#39;=f(x,y)$ such that the function f is derivable from all orders (there are all derivatives of any order) in an environment of $(x_0,y_0)$, then there exists a single curve $y(x)$ such that it passes through the point $(x_0,y_0)$ and satisfies the equation $y&#39;=f(x, and).$

## Immediate first-order ordinary differential equations

We see in this section only the 1st order OEDs simplest to solve, in other posts we will see the more general cases.
### Equations of type $dy/dx=fleft(xright)$

They are integrable directly, writing them as $dy=f(x)Rightarrow y=int f(x)dx+C.$

**Example 8**: Solving the differential equation $y&#39;+x^{2}-1=e^{x}.$

The equation is equivalent to $dy/dx=e^{x}-x^{2}+1Rightarrow y=intleft(e^{x}-x^{2}+1right)dx+C=e^{x}-frac{1}{3}x^{3}+x+C.$
### Equations of type $dy/dx=ky$

If $y = f(x)$ is a function, the equations of type $dy / dx = ky$ have as a solution the set of functions $y (x) = Ce ^ {kx}$ where C is any real number. In general, a differential equation has infinite solutions.

**Example 9**: The solution of the equation $frac {dP} {dt} = kp$ which establishes the evolution of a population $P(t)$ with constant birth and mortality rates is any function of the form $y(x) = Ce^{kx}$.

**Example 10**: Suppose $P(t)$ is the population of a colony of bacteria at time *t,* that the population in $t = 0$ is 1000, and that the population doubles in one hour. Then we can say that

$1000 = P(0)=C$
$2000 = P(1)=Ce^{k}$

therefore $C=$1000 and $k=ln2$, then $P(t)=1000e^{xtext{·} ln2}$.
The condition $P(0) = $1000 is called the **initial condition** because normally the value $t = $0 is taken as the initial state. When we give an initial condition, the solution of the differential equation will no longer have infinite solutions in general, but will have only one, or perhaps none if the conditions are incompatible. Equivalently, by giving an initial condition we pass, if it exists, from the general solution to the particular solution that satisfies that condition. Thus, the initial condition $P (0) = - $1000 has no solution of the type $P(t) = Ce^{kt}$.

**Example 11**: To solve the equation $dy / dx = frac{x} {left (x^{2} +9 right)^{1/2}}$ with the initial condition $y(4)=2$ we do $y(x)=intfrac{x}{left(x^{2}+9right)^{1/2}}dx=left(x^{2}+9right)^{1/2}+C$, as $y(4)=left(16+9right)^{1/2}+C=5+C$ must be $C=-3$.

[![separator2](/taller-matematicas/assets/images/separador2.png)](http://tallermatematic.eu/wp/wp-content/uploads/2014/08/separador2.png)
# Bibliography

DIFFERENTIAL EQUATIONS - Theoretical summary and collection of solved and proposed exercises.
{% endraw %}