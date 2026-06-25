# Heat Conduction - Cartesian

```{admonition} Connection to MTP
 Setting up and solving microbalances is integral to Chapters 4-6.
```

## Theory

### Video on Setting Up Cartesian Microbalances:

<iframe width="560" height="315" src="https://www.youtube.com/embed/6miItvM-vME?si=srPZe5s7Pe2aEEOF&amp;start=90" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Exercises

**Setting up and solving a one-dimensional microbalance for energy transport in Cartesian coordinates.**  

Consider a metal cylinder of length $L$, which is insulated except for its ends. 



```{exercise}
:label: Exercise1cart
The cylinder has a constant heat conduction coefficient, $\lambda_0$. At the left, its temperature is fixed to $T_0$ and at the right it is fixed to $T_1$. Determine the steady state one-dimensional temperature profile in the cylinder and calculate the heat flux.
```
```{solution} Exercise1cart
:label: Solution1cart
:class: dropdown
The full microbalance becomes: $\frac{\partial }{\partial t} \left( \rho c_p A \partial x T \right) = \left[ - \lambda \frac{\partial T}{\partial x} \right]_{x} - \left[ - \lambda \frac{\partial T}{\partial x} \right]_{x+\partial x}$,  with $A$ the cross sectional area of the cylinder; fluxes are based on Fourier's law. 

Dividing the microbalance by $A\,\partial x$ and taking $\partial x \to 0$:  
$
    \rho c_p \frac{\partial T}{\partial t} = \lambda_0 \frac{\partial^2 T}{\partial x^2}.
$  

At steady state this reduces to $d^2T/dx^2 = 0$, which integrates to $T(x) = C_1 x + C_2$, i.e. a linear profile. 

Applying $T(0)=T_0$ and $T(L)=T_1$:  
$
    \boxed{T(x) = T_0 + \frac{T_1 - T_0}{L}\,x,} \qquad \boxed{q = -\lambda_0\frac{dT}{dx} = -\lambda_0\frac{T_1-T_0}{L}.}
$  

The flux is constant along the cylinder, as expected with no heat sources.
```

```{exercise}
:label: Exercise2cart
(*Additional*) Repeat 1, but now for a heat conduction coefficient that depends on the axial $x$ position according to $\lambda(x) = 0.5 \lambda_0 \left( 1 + x/L\right)$.  
```
```{hint}
Use separation of variables to solve the resulting differential equation.
```

```{solution} Exercise2cart
:label: Solution2cart
:class: dropdown
At steady state, $d[\lambda(x)\,dT/dx]/dx = 0$, so the flux $\lambda(x)\,dT/dx = C_1$ is constant. 

Separating variables with $\lambda(x) = 0.5\lambda_0(1+x/L)$:  
$
    dT = \frac{2C_1}{\lambda_0}\cdot\frac{dx}{1+x/L} \implies T(x) = \frac{2C_1 L}{\lambda_0}\ln\!\left(1+\frac{x}{L}\right) + C_2.
$  

Applying $T(0)=T_0$ gives $C_2 = T_0$, and $T(L)=T_1$ gives $2C_1L/\lambda_0 = (T_1-T_0)/\ln 2$, so:  
$
    \boxed{\frac{T(x)-T_0}{T_1-T_0} = \frac{\ln(1+x/L)}{\ln 2},} \qquad \boxed{q = -\frac{\lambda_0(T_1-T_0)}{2L\ln 2}.}
$
```
