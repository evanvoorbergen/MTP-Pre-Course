# Macroscopic Momentum Balances

```{admonition} Connection to MTP
* Chapter 4: Langevin Theory
This forms the basis for modeling diffusion of a solute particle in a liquid.
```

## Theory
### Worked Solution Video for a Similar Exercise
<iframe width="560" height="315" src="https://www.youtube.com/embed/hixxkQuwgHE?si=GOd_MZ1LwREHp_iF" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## Exercises

Consider a small sphere submersed in stagnant water (density $1000 \ \text{kg m}^{-3}$, viscosity $\eta = 1 \ \text{mPa s}$). The radius of the sphere is $10 \ \mu\text{m}$ and its density is $1 \ \text{kg m}^{-3}$.

```{exercise}
:label: Exercise1macromom
Make a sketch of the sphere and draw the forces acting on the sphere.
```
`````{solution} Exercise1macromom
:class: dropdown
```{figure} ../../images/macro_mom/ex4ball.png
:width: 50%
:align: center
```
`````


```{exercise}
:label: Exercise2macrom
Derive a force balance to compute the steady rise velocity of the sphere.  You may assume that $Re\ll 1$.
```

```{hint}
:class: dropdown
Drag force can be written as $F = 6 \pi \eta R v $

This law follows from the general law using $C_d(Re) =24/Re$, which is valid for a spherical small object moving slowly; or more precisely, for a spherical object with a low Reynolds number ($Re\ll 1$).
```

```{solution} Exercise2macrom
:label: Solution2macrom
:class: dropdown
At steady (terminal) velocity, the net force on the sphere is zero. Three forces act on the sphere:  
1. Gravity (downward): $F_g = \rho_s V g = \rho_s \tfrac{4}{3}\pi R^3 g$  
1. Buoyancy (upward): $F_b = \rho_f V g = \rho_f \tfrac{4}{3}\pi R^3 g$  
1. Stokes drag (downward, opposing upward motion): $F_d = 6\pi\eta R v$  

Since $\rho_s \ll \rho_f$, the buoyancy exceeds gravity and the sphere rises. The force balance at steady state is:  
$
    F_b - F_g = F_d
    \implies
    (\rho_f - \rho_s)\tfrac{4}{3}\pi R^3 g = 6\pi\eta R v.
$  

Solving for the rise velocity $v$:  
$
    v = \frac{2R^2 g\left(\rho_f - \rho_s\right)}{9\eta}.
$  

Substituting the known values:  
$
    v = \frac{2\times(10^{-5})^2\times 9.81 \times (1000-1)}{9\times10^{-3}}
    = 2.18\times10^{-4} \ \text{m/s}.
$
```
