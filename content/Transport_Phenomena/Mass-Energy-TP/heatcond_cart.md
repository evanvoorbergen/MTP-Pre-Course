# Mass Diffusion - Cartesian

```{admonition} Connection to MTP
 Setting up and solving microbalances is integral to Chapters 4-6.
```

## Theory

### Video on Setting Up Cartesian Microbalances:

<iframe width="560" height="315" src="https://www.youtube.com/embed/6miItvM-vME?si=srPZe5s7Pe2aEEOF&amp;start=90" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Exercises

**Setting up and solving a one-dimensional microbalance for mass transport in Cartesian coordinates.**  

Consider a cylindrical tube of length $L$, which is impermeable along its walls.


```{exercise}
:label: Exercise1cart
The tube has a constant mass diffusion coefficient, $D$. At the left end, the concentration is fixed at $C_0$, and at the right end it is fixed at $C_1$. Determine the steady-state one-dimensional concentration profile in the tube and calculate the diffusive mass flux.
```
```{solution} Exercise1cart
:label: Solution1cart
:class: dropdown

Setting up the microbalance provides:  
$0 =  \left[ -D A \frac{\partial c}{\partial x} \right]_{x} - \left[ -D A \frac{\partial c}{\partial x} \right]_{x+dx} $ 
where $A$ is the cross-sectional area of the cylinder and flux is based on Fick's law. 


Dividing the microbalance by $D A\,\partial x$ and taking $\partial x \to 0$,  
this reduces to $\frac{\partial^2 C} {\partial x^2} = 0$, which integrates to $C(x) = K_1 x + K_2$, i.e. a linear profile, where $K_1$ and $K_2$ are constants of integration.

Applying $C(0)=C_0$ and $C(L)=C_1$:  
$
    \boxed{C(x) = C_0 + \frac{C_1 - C_0}{L}\,x}
$  

The flux is constant along the cylinder, as provided below:  
$
\boxed{J = -D\frac{\partial C}{\partial x} = -D\frac{\partial}{\partial x}\big(C_0 + \frac{C_1 - C_0}{L}x \big) = -D\frac{C_1-C_0}{L}}
$
```

```{exercise}
:label: Exercise2cart
(*Additional*) Repeat {numref}`Exercise1cart`, but now for a diffusion coefficient that depends on the axial position according to  
$
D(x) = 0.5 D_0 \left(1 + \frac{x}{L}\right).
$
```
```{hint}
:class: dropdown
Use separation of variables to solve the resulting differential equation.
```

```{solution} Exercise2cart
:label: Solution2cart
:class: dropdown
At steady state, $ \frac{d}{dx}\left(D(x)\frac{dC}{dx}\right)=0 $, which implies that the diffusive mass flux is constant:

$ J=-D(x)\frac{dC}{dx}$, where $J$ is the constant diffusive mass flux.

Substituting $D(x)=0.5D_0\left(1+\frac{x}{L}\right)$ into Fick's law and rearranging gives $dC = -\frac{2J}{D_0} \frac{dx}{1+x/L}$

Integrating, $C(x) = -\frac{2JL}{D_0} \ln\!\left(1+\frac{x}{L}\right) + A$

Applying the boundary conditions, $C(0)=C_0,\qquad C(L)=C_1$ gives $ A=C_0$ and $-\frac{2JL}{D_0} = \frac{C_1-C_0}{\ln2}$

Hence,
$
\boxed{\frac{C(x)-C_0}{C_1-C_0} = \frac{\ln\!\left(1+x/L\right)}{\ln2}}
$

and the constant diffusive mass flux is

$
\boxed{J = -\frac{D_0(C_1-C_0)}{2L\ln2}}
$

```
