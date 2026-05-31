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

1. The cylinder has a constant heat conduction coefficient, $\lambda_0$. At the left, its temperature is fixed to $T_0$ and at the right it is fixed to $T_1$. Determine the steady state one-dimensional temperature profile in the cylinder and calculate the heat flux.

2. (*Additional*) Repeat 1, but now for a heat conduction coefficient that depends on the axial $x$ position according to $\lambda(x) = 0.5 \lambda_0 \left( 1 + x/L\right)$.  


## Solutions

```{dropdown} Exercise 1
The full microbalance becomes: $\frac{\partial }{\partial t} \left( \rho c_p A \partial x T \right) = \left[ - \lambda \frac{\partial T}{\partial x} \right]_{x} - \left[ - \lambda \frac{\partial T}{\partial x} \right]_{x+\partial x}$,  with $A$ the cross sectional area of the cylinder; fluxes are based on Fourier's law. Turn this into a differential equation yourself. Then, show yourself that the steady-state profile is linear.
```

```{dropdown} Exercise 2
Hint: use separation of variables to solve the resulting differential equation. Final answer: $\left( T(x) - T_0 \right) / \left( T_1 - T_0 \right)  = \ln{(1 + x/L)} /  \ln{(2)} $.
```
