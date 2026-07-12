# Mass Diffusion - Cylindrical

```{admonition} Connection to MTP
 Setting up and solving microbalances is integral to Chapters 4-6.
```

## Theory

### Video on Setting Up Cylindrical Microbalances:
<iframe width="560" height="315" src="https://www.youtube.com/embed/6miItvM-vME?si=srPZe5s7Pe2aEEOF&start=450" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Exercises

**Setting up and solving a one-dimensional microbalance for mass transport in cylindrical coordinates.**  



```{exercise}
:label: Exercise1cyl_diffusion
Consider a long hollow cylinder (length $L$, inner diameter $d_1$, outer diameter $d_2$) made of a solid material through which a solute can diffuse, with diffusion coefficient $D$. The concentration of the diffusing species at the inner and outer surfaces is fixed to $c_1$ and $c_2$, respectively. The ends of the cylinder are impermeable (no mass flux through them). Set up the problem from scratch to arrive at the concentration profile in the radial direction $c(r)$, $r$ being the radial coordinate.

Pay attention to the volume and surface areas of the control volume you consider!
```

```{solution} Exercise1cyl_diffusion
:label: Solution1cyl_diffusion
:class: dropdown

We consider a thin cylindrical shell of radius $r$, thickness $\partial r$, and length $L$ as our control volume, and set up a mass balance on the diffusing species (accumulation = in − out, since there is no reaction):

$$
\frac{\partial }{\partial t}\left(c \, V\right) = -D \left(2 \pi L r \frac{\partial c}{\partial r} \right)_r - \left[-D \left(2 \pi L r \frac{\partial c}{\partial r}\right)_{r+\partial r}\right]
$$

with $V$ the volume of the control volume, equal to $V = \pi (r+\partial r)^2 L - \pi r^2 L = \pi L \cdot (2r\partial r+\partial r^2)$.

Here $-D \, 2\pi L r \, \partial c/\partial r$ is the molar (or mass) flow rate of the diffusing species crossing the cylindrical surface at radius $r$, by Fick's law, with $2\pi r L$ the area of that surface.

Substituting this expression for $V$ in the mass balance and dividing both sides by $\pi L \, \partial r$ gives:

$$
\frac{\partial }{\partial t}\left((2r+\partial r) c\right) = \frac{D \left(2 r \frac{\partial c}{\partial r}\right)_{r+\partial r} - D\left(2 r \frac{\partial c}{\partial r}\right)_{r}}{\partial r}
$$

Now, taking the limit $\partial r \rightarrow 0$, the microbalance turns into a differential equation:

$$
\frac{\partial c}{\partial t} = D \, \frac{1}{r}\frac{\partial }{\partial r}\left(r \frac{\partial c}{\partial r}\right)
$$

For steady state, this balance reduces to

$$
0 = \frac{1}{r}\frac{d }{dr}\left(r \frac{dc}{dr}\right)
$$

Integrating twice leads to the following general expression for the concentration profile: $c(r) = C_1 \ln(r) + C_2$. Using the two boundary conditions $c(r = R_1) = c_1$ and $c(r = R_2) = c_2$, we find the two constants of integration and the resulting concentration profile:

$$
\frac{c - c_2}{c_1 - c_2} = \frac{\ln \left(\frac{r}{R_2}\right)}{\ln\left(\frac{R_1}{R_2}\right)}
$$



Epilogue: For educational purposes, we kept the term $\partial r^2$ in the volume of the cylindrical shell to show that this term gets eliminated once taking the limit $\partial r \rightarrow 0$. Having seen this and understanding it, you may in future leave out this term from the start and use $V = 2\pi r \partial r L$ as the volume of the cylindrical shell.
```

