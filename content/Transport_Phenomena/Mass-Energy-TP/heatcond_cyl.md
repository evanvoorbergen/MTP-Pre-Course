# Heat Conduction - Cylindrical

```{admonition} Connection to MTP
 Setting up and solving microbalances is integral to Chapters 4-6.
```

## Theory

### Video on Setting Up Cylindrical Microbalances:
<iframe width="560" height="315" src="https://www.youtube.com/embed/6miItvM-vME?si=srPZe5s7Pe2aEEOF&start=450" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Exercises

**Setting up and solving a one-dimensional microbalance for energy transport in cylindrical coordinates.**  


```{exercise}
:label: Exercise1cyl
Consider a long hollow cylinder (length $L$, inner diameter $d_1$, outer diameter $d_2$, density $\rho$, heat conduction coefficient $\lambda$, heat capacity $c_p$). The temperature of the inner and outer surfaces are fixed to $T_1$ and $T_2$, respectively. The ends are insulated. Set up the problem from scratch to arrive at the temperature profile in the radial direction $T(r)$, $r$ being the radial coordinate. 

Pay attention to the volume and surface areas of the control volume you consider! 
```
```{solution} Exercise1cyl
:label: Solution1cyl
:class: dropdown
Energy balance over the control volume leads to:  
$$
\frac{\partial }{\partial t}\left(\rho c_p V T\right) = -\lambda \left(2 \pi L r \frac{\partial T}{\partial r} \right)_r - -\lambda \left(2 \pi L r \frac{\partial T}{\partial r}\right)_{r+\partial r}
$$  
with $V$ the volume of the control volume, equal to $V =  \pi (r+\partial r)^2 L - \pi r^2 L = \pi L \cdot (2r\partial r+\partial r^2)$.  

Substituting this expression for $V$ in the energy balance and diving both sides by $\pi L \partial r$ gives:  
$$
\frac{\partial }{\partial t}\left(\rho c_p (2r+\partial r) T\right) =\frac{\lambda (2  r \frac{\partial T}{\partial r})_{r+\partial r} - \lambda (2  r \frac{\partial T}{\partial r})_{r}}{\partial r}
$$  

Now, taking the limit $\partial r\rightarrow 0$, the microbalance turns into a differential equation:  
$$
\frac{\partial }{\partial t} \left(\rho c_p T\right)= \lambda \frac{1}{r}\frac{\partial  }{\partial r}\left(r \frac{\partial T}{\partial r}\right) $$  

For steady state, this balance reduces to  
$$0 = \frac{1}{r}\frac{d }{dr}\left(r \frac{dT}{dr}\right) $$  

Integrating twice leads to the following general expression for the temperature profile: $T(r) = C_1 \ln(r) + C_2$. Using the following two boundary conditions: $T(r = R_1) = T_1$  and $T(r = R_2) = T_2$, we find the two constants of integration and the resulting temperature profile:  
$$\frac{T - T_2}{T_1 - T_2} = \frac{\ln (\frac{r}{R_2})}{\ln(\frac{R_1}{R_2})}$$

Epilogue: for educational purposes, we kept the term $\partial r^2$ in the volume of the cylindrical shell to show that this term gets eliminated once taking the limit $\partial r \rightarrow 0$. Having seen this and understanding it, you may in future leave out this term from the start and use $V = 2\pi r \partial r L$ as the volume of the cylindrical shell.
```
