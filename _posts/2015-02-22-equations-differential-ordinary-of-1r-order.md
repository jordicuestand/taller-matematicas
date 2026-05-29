---
layout: post
title: "1st-order ordinary differential equations"
date: 2015-02-22 17:46:06 +0000
categories:
  - "Mathematics"
math: true
---
{% raw %}

- [Separable equations](#separables)

 	- [Unique solutions](#singulares)

 	- [Enveloping curve of a beam of curves](#envolvente)

 	- [Homogeneous functions. Application to differential equations](#homogeneas)

 	- [Exact equations](#exactas)

![separator2](/taller-matematicas/assets/images/separador2.png)
## Separable equations

The separable differential equations are those of the form $dy / dx = H (x, y)$ where $H (x, y)$ can be expressed either as the quotient $H (x, y) = f (x) / g (y)$ or as the product $H (x, y) = f (x) text {·} g (y)$.

In the first case, $dy / dx = f (x) / g (y) Rightarrow g (y) dy = f (x) dx Rightarrow int g (y) dy = int f (x) dx + C$, while in the second case $dy/dx=f(x) text{·} g(y) Rightarrow g^{-1}(y)dy=f(x)dx Rightarrow int g^{-1}(y)dy = int f(x)dx+C.$

**Example 1**: Solve the differential equation $x^{2}frac{dy}{dx}=frac{x^{2}+1}{3y^{2}+1}.$
Let's take $H(x,y)=frac{left(x^{2}+1right)/x^{2}}{3y^{2}+1}=frac{f(x)}{g(y)}$ so that $int f(x)dx=intfrac{x^{2}+1}{x^{2}}dx=x-frac{1}{x},
int g(y)dy=intleft(3y^{2}+1right)dy=y^{3}+y$ and therefore the solution will be given implicitly by $y^{3}+y=x-frac{1}{x}+C.$

**Example 2**: Find all the solutions of the equation $dy/dx=2xsqrt{y-1}.$

Let's $H(x,y) = 2x sqrt{y-1} = f(x) text{·} g(y),$ and let's integrate each function: $int f(x)dx=int2xdx=x^{2};
int g^{-1}(y)dy=intfrac{1}{sqrt{y-1}}dy=2sqrt{y-1}.$ Solutions are $2sqrt{y-1}=x^{2}+CRightarrow y=left(frac{x^{2}+C}{2}right)^{2}+1
.$ Note that the function $y (x) = 1$ is also a solution of the equation, but it is not included in the general solution $y = left ( frac {x ^ {2} + C} {2} right) ^ {2} +1,$ that is to say that for all *C* we will have $y = left (frac {x ^ {2} + C} {2} right) ^ {2} +1 neq1$. We call solutions not included in the general solution **singular solutions** of the differential equation.

![separator2](/taller-matematicas/assets/images/separador2.png)

## Unique solutions

In example 2 we have seen that we can have solutions that are not included in the general solution, called singular solutions. When will this happen and how can we find those other solutions? Let's remember what we have seen in the post [Ordinary differential equations: introduction]({{ site.baseurl }}/2015/02/12/ecuaciones-diferenciales-ordinarias-introduccion/), section "Bundle of curves and differential equations of the first order": the general solution of the ordinary differential equation $y&#39;=F(x,y)$ represents a bundle of curves $y=f(C,x)$ such that each curve of that beam satisfies the equation, that is, for each point $(x, y)$ the slope of any of the curves $y=f(C,x)$ at that point fulfills $y&#39;=F(x,y)$.

### Enveloping curve of a bundle of curves and singular solution

![Two one-beam lines (blue and red) and beam envelope curve (green)](/taller-matematicas/assets/images/Feix_corbes_env1.png) Two one-beam lines (blue and red) and beam envelope curve (green)
Given a bundle of curves $F(x,y,C)=0$ the curve $f(x,y)$ is called the beam envelope curve such that it is tangent to all the curves of the beam.

**Example 3**: The image shows two lines of the line bundle $y=(1-10/C)*x+(10-C)$, specifically the two lines corresponding to the values $C=3$ in red and $C=6$ in blue, and the enveloping curve of the beam, which is tangent to the first line at a point close to $x=1,  y=5$ and the second line about $x=3.5, y=1.5$.

Remember that we can associate to any bundle of curves $F(x,y,C)=0$ a differential equation $y&#39;=f(x,y)$ such that the beam is the general solution of the equation: for each value of C, we have a curve of the beam such that its derivative verifies$y&#39;=f(x,y)$. But we have seen that the enveloping curve is tangent to all the curves of the beam, that is, its derivative at each point coincides with the derivative of one of the curves of the beam; this is why the enveloping curve is also a solution of the differential equation of the beam.

**Example 4**.Consider the parabolal bundle $4y=(x + C)^2$, all curves are tangent to the X axis at some point; the image depicts three of the beam curves, tangent to $y=$0 at points $x=-3, -2, -$1.

![Parabola beam 4y=(x + C)²](/taller-matematicas/assets/images/Feix_corbes_env.png) Parabola beam 4y=(x + C)²
What is the differential equation of the curve beam? We derive with respect to *x *the equation of the beam: $4y&#39;=2(x + C)$, and eliminate the constant *C* using this equality and the equation of the beam:

$left.begin{array}{r}4y&#39;=2(x+C)Rightarrow C=2y&#39;-x\4y=(x;+; C)^2end{array}right}Rightarrow4y=(2y&#39;{)^2=4y&#39;^2}Rightarrow y=y&#39;^2.$
Note that the line $y=0$, being tangent to all the curves of the beam, has the same derivative as the curves of the beam at each point on the X axis; therefore, it also verifies the differential equation of the beam. In general: if there exists an enveloping curve that is tangent to all the curves of a beam, then that curve will be a singular solution of the differential equation of the beam.

#### Calculating the envelope of a beam of curves

Given any value $x=x_0$, the envelope will have the same derivative at that point as some curve of the beam, that is, there will be a constant C, dependent on $x=x_0$, such that the derivative of the beam curve $F(x_0,y,C)=0$ will have the same value at that point. We dispense with $x_0$: in general for each x we will have a C(x). Let us derive with respect to x the expression of the beam, taking into account that y also depends on x, using the rule of the chain and the implicit derivation:

$F(x,y,C)=0Rightarrowfrac{operatorname d{F(x,y,C)}}{operatorname dx}=frac{partial F(x,y,C)}{partial x}+frac{partial F(x,y,C)}{partial y}frac{operatorname dy}{operatorname dx}=frac{partial F(x,y,C)}{partial x}+frac{partial F(x,y,C)}{partial y}y&#39;=0$

We clear y' to obtain the derivative at any point of any curve of the beam:

$y&#39;=-frac{partial F(x,y,C)}{partial x}left(frac{partial F(x,y,C)}{partial y}right)^{-1}.$

We now turn to the enveloping curve; at the contact points $(x,y)$ between each curve and the envelope the derivatives match the curves of the beam; in each given value x we will have determined a C(x), as the value y(x) also coincides with that of the beam, we will have that at the point of contact $F(x,y,C(x))$ is fulfilled. We derive again with respect to x:

$begin{array}{l}F(x,y,Cleft(xright))=0Rightarrow\frac{operatorname d{F(x,y,Cleft(xright))}}{operatorname dx}=frac{partial F(x,y,C)}{partial x}+frac{partial F(x,y,C)}{partial y}frac{operatorname dy}{operatorname dx}+frac{partial F(x,y,C)}{partial C}frac{operatorname dC}{operatorname dx}\=frac{partial F(x, y,C)}{partial x}+frac{partial F(x,y,C)}{partial y}y&#39;+frac{partial F(x,y,C)}{partial C}C&#39;=0end{array}.$

We clear and':

$y&#39;=left(frac{partial F(x,y,C)}{partial y}right)^{-1}left[frac{partial F(x,y,C)}{partial x}+frac{partial F(x,y,C)}{partial C}C'right].$

The two expressions for the derivative y' must be equal:

$y&#39;=left(frac{partial F(x,y,C)}{partial y}right)^{-1}left[frac{partial F(x,y,C)}{partial x}+frac{partial F(x,y,C)}{partial C}C'right]=left(frac{partial F(x,y,C)}{partial y}right)^{-1}left[frac{partial F(x,y,C)}{partial x}right].$

We see that it must be: $frac{partial F(x,y,C)}{partial C}C&#39;=0,$ that has two possible solutions, the trivial $C&#39;=0Rightarrow C=cte$ and the condition $frac{partial F(x,y,C)}{partial C}=0.$ The first is an unimportant solution because it tells us that the constant C will not depend
of x (degenerate curve beam: all curves are equal), while the second is the general condition to be met by the envelope.

**Example 5**: Find the expression of the enveloping curve of the line bundle of example 3, $y=(1-10/C)*x+(10-C).$

We express it in the form $F(x,y,C)=y-(1-10/C)ast x-(10-C)=0$ to derive with respect to C and equal to zero:

$frac{partial{F(x,y,C)}}{partial C}=frac{-10}{C^2}x+1=0Rightarrow C=sqrt{10x}.$

We substitute this value in the expression of the beam to remove C and get the equation of the envelope:

$F(x,y)=y(1-frac{10}{sqrt{10x}})x+(10-sqrt{10x})=y-10-x+2sqrt{10x}=0.$

The envelope is $y=10+x-2sqrt{10x}.$

**Example 6**: Calculate the envelope of the curve beam $4y=(x + C)^2$ of example 4.

$begin{array}{l}F(x,y,C)=4y-(x+C)^2=0;\frac{partial F}{partial C}=2(x+C)=0Rightarrow C=-x;\F(x,y)=4y-(x-x)^2=4y=0Rightarrowboxed{y=0}.end{array}$

![separator2](/taller-matematicas/assets/images/separador2.png)
## Homogeneous functions. Application to differential equations.

A function $F(x,y)$ is homogeneous of degree n if $F(lambda x,lambda y)=lambda^nF(x,y)$ for every parameter $lambdaneq0.$ Per example, the function $F(x,y)=xy-x^2$ is homogeneous of degree 2, since $F(lambda x,lambda y)=lambda xlambda y- ( lambda x)^2=lambda^2F(x,y).$

In the special case that $F(x,y)$ is homogeneous of degree 0 we have $F(lambda x,lambda y)=F(x,y)$, and gives us a method of solving differential equations $y&#39;=F(x,y)$ in which the F is homogeneous of degree 0: with the change of variable $u=y/x$ they become equations of separate variables. Indeed:

$begin{array}{l}u=y/xLeftrightarrow y=uxRightarrow y&#39;=u&#39;x+u;\y&#39;=F(x,y)Leftrightarrow u&#39;x+u=F(x,ux)=F(1,u)end{array}$

where we have used the x instead of the $lambda$ as a parameter of the homogeneous. Then

$begin{array}{l}frac{du}{dx}x+u=F(u)Leftrightarrowfrac{du}{dx}x=F(u)-uLeftrightarrowfrac{du}{F(u)-u}=frac{dx}xLeftrightarrow\intfrac{du}{F(u)-u}=intfrac{dx}x=lnleft(xright)+Cend{array}.$

**Example 7**: Solve $y&#39;=frac y{sqrt{x^2+y^2}-x}.$

$F(lambda x,lambda y)=frac{lambda y}{sqrt{lambda^2x^2+lambda^2y^2}-lambda x}=frac{lambda y}{lambdaleft(sqrt{x^2+y^2}-xright)}=frac y{sqrt{x^2+y^2}-x}$ then it is homogeneous of degree 0. We make the change $u=y/x$ to get it to be of separate variables:

$begin{array}{l}y&#39;=u&#39;x+u=frac{ux}{sqrt{x^2+u^2x^2}-x}=frac u{sqrt{1+u^2}-1};\frac{du}{dx}x=frac u{sqrt{1+u^2}-1}-u=frac{uleft(sqrt{1+u^2}+1right)}{1+u^2-1}-u=frac{sqrt{1+u^2}+1}u-u=\frac{sqrt{1+u^2}+1-u^2}u;\frac{udu}{sqrt{1+u^2}+1-u^2}= frac{dx}x\end{array}.$

Then $intfrac{udu}{sqrt{1+u^2}+1-u^2}=intfrac{dx}x=lnleft(xright)+C.$ In the first integral we make the variable change $1+u^2=t^2$ that makes it:

$intfrac{udu}{sqrt{1+u^2}+1-u^2}=intfrac{toperatorname dt}{t+1-left(t^2-1right)}=intfrac{toperatorname dt}{-t^2+t+2},$

that it is of a rational type; we decompose into simple fractions:

$begin{array}{l}intfrac{toperatorname dt}{-t^2+t+2}=intfrac{-1/3}{t+1}+intfrac{-2/3}{t-2}=-frac13lnleft(t+1right)-frac23lnleft(t-2right)\=-frac13lnleft(left(t+1right)left(t-2right)^2right)=lnleft(left(t+1right)left(t-2right)^2right)^{-1/3}end{array}.$

We equate the two integrals, and undo the changes to obtain the general solution implicitly:

$begin{array}{l}lnleft(left(t+1right)left(t-2right)^2right)^{-1/3}=lnleft(xright)+CLeftrightarrow\Cx=left(left(t+1right)left(t-2right)^2right)^{-1/3}=left(t^3-3t^2+4right)^{-1/3}Leftrightarrow\frac C{x^3}=left(u^2+1right)^{3/2}-3u^2+1Leftrightarrow\C=x^3left$left(left(frac yxright)^2+1right)^frac32-3left(frac yxright)^2+1right$.end{array}.$

#### Reduction to homogeneous

The rational functions of form

$F(x,y)=frac{ax+by+c}{a&#39;x+b&#39;y+c&#39;}$
they are only homogeneous of degree 0 when $c=c&#39;=0$, however if we think of the numerator and denominator of the function as if they were two lines $ax+by+c=0,;a&#39;x+b&#39;y+c&#39;=0$, we can try to find its intersection point $(x_0,y_0)$, if it exists, then the variable change $X = x - x_0,  Y = y - y_0$ (which is a translation of the xy axes to the XY axes, taking as the coordinate origin the point $(x_0,y_0)$), converts the function into homogeneous of degree 0.

**Example 8**: Solve $y&#39;=frac{y-x-1}{x+y-1}.$

We find the intersection of the lines:

$left.begin{array}{r}y-x-1=0\x+y-1=0end{array}right}y=1,;x=0$

we make the change $X=x, Y=y-1$ which transforms the equation into:

$y&#39;=frac{y-x-1}{x+y-1}Leftrightarrow Y&#39;=frac{Y-X}{X+Y}$

containing a homogeneous $f(X,Y)$ function of degree 0; we make the change $u=Y/X$ to separate the variables:

$begin{array}{l}u&#39;X+u=frac{u-1}{1+u}Leftrightarrowfrac{operatorname du}{operatorname dX}X=frac{u-1}{1+u}-u=frac{-1-u^2}{1+u}=-frac{1+u^2}{1+u};\intfrac{1+u}{1+u^2}operatorname du=intfrac{operatorname dX}X=lnleft(Xright)+Cend{array}.$

We decompose the first integral:

$begin{array}{l}intfrac{1+u}{1+u^2}=intfrac1{1+u^2}+intfrac u{1+u^2}=tan^{-1}left(uright)+frac12intfrac{2u}{1+u^2}=\tan^{-1}left(uright)+frac12lnleft(1+u^2right)end{array}.$

We equalize integrals and undo the change:

$begin{array}{l}-tan^{-1}left(uright)-frac12lnleft(1+u^2right)=lnleft(Xright)+C=lnleft(CXright)Leftrightarrow\-tan^{-1}left(frac YXright)=lnleft(CXleft(1+left(frac YXright)^2right)right);\lnleft(Cxleft(1+left(frac{y-1}xright)^2right)right)+tan^{-1}left(frac{y-1}xright)=0.\end{array}$

#### Special case: the lines are parallel

In the special case that the two lines have no intersection, then they are parallel, with proportional director vectors: $frac ba=frac{b&#39;}{a&#39;}=r$; but then we can do

$F(x,y)=frac{ax+by+c}{a&#39;x+b&#39;y+c}=frac{a&#39;rx+b&#39;ry+c}{a&#39;x+b&#39;y+c}=frac{rleft(a&#39;x+b&#39;yright)+c}{a&#39;x+b&#39;y+c},$

with variable change $Y=a&#39;x+b&#39;y$ becomes

$begin{array}{l}F(x,Y)=frac{rY+c}{Y+c&#39;};;y=frac{Y-a&#39;x}{b&#39;}Rightarrowfrac{operatorname dy}{operatorname dx}=frac1{b&#39;}left(frac{operatorname dY}{operatorname dx}-a&#39;right);\frac{operatorname dy}{operatorname dx}=F(x,y)Leftrightarrowfrac1{b&#39;}left(frac{operatorname dY}{operatorname dx}-a&#39;right)=frac{rY+c}{Y+c&#39;}Leftrightarrow\frac{operatorname dY}{operatorname dx}=b&#39;frac{rY+c}{ Y+c&#39;}+a&#39;end{array}$

which is of separate variables.

**Example 9**: $y&#39;=frac{x+y+1}{x+y-1}.$

The lines $x+y+1=0$ and $x+y-1$ have no intersection, they are parallel; we make the change $Y=x+y, Y&#39;=1+y&#39;$ to obtain:

$begin{array}{l}Y&#39;-1=frac{Y+1}{Y-1};;frac{operatorname dY}{operatorname dx}=frac{Y+1}{Y-1}+1=frac{Y+1+Y-1}{Y-1}=frac{2Y}{Y-1};\intfrac{Y-1}{2Y}operatorname dY=intoperatorname dx;\frac12intleft(1-frac1Yright)operatorname dY=x+C;\Y-lnleft(Yright)=2x+C;\x+y-lnleft(x+yright)=2x+C;\y=x+lnleft(x+yright)+C.end{array}$

![separator2](/taller-matematicas/assets/images/separador2.png)

## Exact equations

The equations of the form $M (x, y) + N (x, y) frac {dy} {dx} = 0,$ or equivalently, $M (x, y) dx + N (x, y) dy = 0$, we will say that they are exact as long as M and N are continuous functions and
check the condition $frac {partial M} {partial y} = frac {partial N} {partial x}.$

The solution will be given implicitly by $F (x, y) = C$ where $frac {partial F} {partial x} = M, : frac {partial F} {partial y} = N.$

**Example 10**: The equation $y^{3} dx + 3xy^{2} dy = 0$ is exact, because $N = 3xy^{2}, frac{partial N} {partial x} = 3y^{2}, : M = y^{3}, : frac {partial M} {partial y} = 3y^{2}.$ As $frac {partial F} {partial x} = M,$ will be $F (x, y) = int MDX = xy^{3} + C (y)$ and also $F (x, y) = int Ndy = xy^{3} + C (x);$ equalizing the two expressions we have $F (x,  y) = xy^{3}, C(x) = C(y) = 0,$ so the general solution is $xy^{3} = C.$

**Example 11**: Solve the differential equation $left (6xy-y^{3} right) dx + left (4y + 3x^{2} -3xy^{2} right) dy = 0.$

As $M = 6xy-y^{3}, N = 4y + 3x^{2} -3xy^{2}, frac {partial N} {partial x} = 6x-3y^{2} = frac {partial M} {partial y},$ the equation is exact. Then

$F (x, y) = int Ndy = 2y^{2} + 3x^{2} y-xy^{3} + C (x), F (x, y) = int MDX = 3x^{2} y-xy^{3} + C(y),$

and when we equalize the two expressions we get $C (y) = 2y^{2}.$
{% endraw %}