# Mass Diffusion and Convection

```{admonition} Connection to MTP
 Any macroscopic/continuum treatment of mass transport is done through a microbalance/shell balance.  
 * Applies to Chapters 4, 5, 6.
```

## Exercises

**Setting up and solving a one-dimensional microbalance for species transport in Cartesian coordinates.**  

Consider `dispersed plug flow' in a straight tube of uniform cross-section $A$ and length $L$. At the left side the tube is connected to a vessel containing pure water. Water from this tank flows into the tube with a velocity $v$. The exit of the tube is connected to a vessel that contains water with species A in a concentration $c_{A0}$. In this assignment, assume that both vessels are so large that the concentration of species A in these vessels is constant in time. 

```{exercise}
:label: Exercise1md
Make a sketch of the problem, indicating all relevant variables.
```
`````{solution} Exercise1md
:class: dropdown
```{figure} ../../images/mass_dif_conv/q7sketch.png
:width: 50%
:align: center
```
`````


```{exercise}
:label: Exercise2md
Consider a relevant control volume and set up a microscopic balance to derive the one-dimensional mass balance for
species A in the tube. State the boundary conditions. You may assume that the diffusion coefficient $D$ does not depend on the $x$-position and the velocity $v$ is independent of $x$.
```
```{solution} Exercise2md
:label: Solution2md
:class: dropdown
Microbalance: $\frac{\partial  (c_A A \partial x)}{\partial t} = \left[ -D A \frac{\partial c_A}{\partial x}\right]_x + \left[ v A c_A \right]_x - \left[ -D A \frac{\partial c_A}{\partial x}\right]_{x+\partial x} - \left[ v A c_A \right]_{x+\partial x}$.

Dividing by $\partial x$ and taking the limit $\partial x \rightarrow 0$ we find: $\frac{\partial  c_A}{\partial t} = \frac{\partial }{\partial x} \left( D \frac{\partial c_A}{\partial x} \right) - \frac{\partial }{\partial x}\left( vc_A \right)$.

Since the diffusion coefficient $D$ does not depend on the $x$-position and the velocity $v$ is independent of $x$, we find $\frac{\partial c_A}{\partial t} =  D \frac{\partial ^2c_A}{\partial x^2} - v \frac{\partial c_A}{\partial x}$. 

Two boundary conditions are needed to solve this second-order ODE. They are: $c_A(x=0,t)=0$ and $c_A(x=L,t)=c_{A0}$. 
```

```{exercise}
:label: Exercise3md
Consider the case that concentration profile in the tube reaches a steady profile. Assume diffusion can be neglected. Determine the concentration profile $c_A(x)$ in the tube. 
```
```{solution} Exercise3md
:label: Solution3md
:class: dropdown
The balance in {numref}`Exercise2md` directly gives $0 = \frac{dc_A}{dx}$. Integration shows that the concentration is constant along the length of the tube. 

The integration constant is determined using the boundary condition: $c_A(x=0) = 0$, which shows that $c_A(x) = 0$ (except at $x=L$). 

Logical? Yes, diffusion is the only means by which A is transported into the tube from the vessel on the right. If there is no diffusion, there is no way for A to enter the tube so the concentration in the tube is zero (except at the exit of the tube, where the concentration is $c_{A0}$). 
```

```{exercise}
:label: Exercise4md
Do the same as in {numref}`Exercise3md`, but now assuming the velocity is very small. What will the concentration profile look like?
```
```{solution} Exercise4md
:label: Solution4md
:class: dropdown
The balance in {numref}`Exercise2md` directly gives  $0 =  \frac{d^2c_A}{dx^2}$. Integrating twice gives $c_A(x) = c_1 + c_2 x$, with $c_1$ and $c_2$ the two integration constants. Using the two boundary conditions, we obtain: $c_A(x) / c_{A0} = x/L$. 
```

```{exercise}
:label: Exercise5md
Solve the full differential equation derived in {numref}`Exercise2md` with the convective and diffusive term under steady state. Compare the outcome with your answers to  {numref}`Exercise3md` and {numref}`Exercise4md`. Explain the differences and observations.
```

```{hint}
:class: dropdown
Try a solution of the form  $c_A = e^{\lambda x}$
```

```{solution} Exercise5md
:label: Solution5md
:class: dropdown
We solve the steady-state version of the ODE (setting $\partial c_A/\partial t = 0$):  
$
    D\frac{d^2c_A}{dx^2} - v\frac{dc_A}{dx} = 0.
$

This is a second-order linear ODE with constant coefficients. We try the a solution of the form $c_A = e^{\lambda x}$, substituting:  
$
    D\lambda^2 - v\lambda = 0 \implies \lambda(D\lambda - v) = 0 \implies \lambda = 0 \quad \text{or} \quad \lambda = \frac{v}{D}.
$  

The general solution is therefore:  
$
    c_A(x) = C_1 + C_2\, e^{vx/D}.
$  

Applying the boundary conditions:  
1. $c_A(0) = 0$: $\quad C_1 + C_2 = 0 \implies C_1 = -C_2$
1. $c_A(L) = c_{A0}$: $\quad C_1 + C_2\,e^{vL/D} = c_{A0} \implies C_2(e^{vL/D} - 1) = c_{A0} \implies C_2 = \dfrac{c_{A0}}{e^{vL/D}-1}$

Substituting back:  
$
    \boxed{c_A(x) = c_{A0}\,\frac{e^{vx/D} - 1}{e^{vL/D} - 1}.}
$

This is logical: if convective transport is much stronger compared to diffusive transport, i.e. $v/D$ is very large, or more precisely $vL/D\gg1$, this indeed yields $c(x) = 0$ as found in {numref}`Exercise3md`. 

This follows from $c_A(x) / c_{A0} \approx \left(e^{vL/D \cdot x/L} \right)/ \left(e^{vL/D} \right)=  \left(1/e^{(1 - x/L)}\right)^{vL/D}  \approx 0$.  
  
Note that the last step follows from the term $\left(1/e^{(1 - x/L)}\right)$ being positive but smaller than 1 for the entire tube (except at $x=L$), such that raising it to a very large number yields 0. If $vL/D$ is very small (but non-zero), use a Taylor series (i.e. $e^y \approx 1 + y$ for $y\ll1$) to demonstrate that the answer in {numref}`Exercise4md` is found.

```

```{exercise}
:label: Exercise6md
State the dimensionless number that compares diffusive and convective transport in the system under consideration (and naturally appears in the expression for the concentration in {numref}`Exercise5md`).
```
```{solution} Exercise6md
:label: Solution6md
:class: dropdown
The dimensionless number that naturally appears in the concentration profile is $vL/D$, which is known as the Peclet number ($Pe$). It can be interpreted as the time scale required to travel through the tube by diffusion, i.e. $L^2 / D$, to the time scale required to travel through the tube by convection, i.e. $L/v$. For large $Pe$, the time required for diffusion is much longer than for convection and hence diffusive transport can be neglected compared to convective transport.
```
