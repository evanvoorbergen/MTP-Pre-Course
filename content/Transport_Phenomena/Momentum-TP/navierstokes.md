# Navier-Stokes


```{admonition} Connection to MTP
* Chapter 6: Navier-Stokes
* Chapter 6: Electro-osmosis
```
## Theory

### Video on Navier Stokes


## Exercises

**Analysis of the Navier-Stokes equations in cylindrical coordinates**

Consider a laminar single phase flow through a straight cylindrical pipe, with the flow direction being the $z$ direction. We will use conservation equations to derive a velocity profile. For mass, this conservation is also known as the 'continuity equation', while the momentum conservation equations are better known as the 'Navier-Stokes equations'. In cylindrical coordinates, these *four* equations read:

**Continuity Equation**
$
 0 = \frac{1}{r} \frac{\partial }{\partial r} \left( r v_r\right) + \frac{1}{r} \frac{\partial }{\partial \theta} \left( v_{\theta} \right) + \frac{\partial }{\partial z} \left( v_z \right)
$

**Navier-Stokes: $\theta$-direction**  

$$
\begin{split}
\rho\left(\frac{\partial v_r}{\partial t}+v_r\frac{\partial v_r}{\partial r}+\frac{v_\theta}{r}\frac{\partial v_r}{\partial \theta}-\frac{v_\theta^2}{r}+v_z\frac{\partial v_r}{\partial z}\right) = \\
- \frac{\partial p}{\partial r} + \eta \left[ \frac{1}{r} \frac{\partial }{\partial r} \left( r \frac{\partial v_r}{\partial r}\right) -\frac{v_r}{r^2} +\frac{1}{r^2} \frac{\partial ^2}{\partial \theta^2} \left( v_r \right) - \frac{2}{r^2} \frac{\partial }{\partial \theta} \left( v_{\theta} \right)+ \frac{\partial ^2}{\partial z^2} \left( v_r\right) \right]
\end{split}
$$


**Navier-Stokes: r-direction**  

$$
\begin{split}
\rho\left(\frac{\partial v_\theta}{\partial t}+v_r\frac{\partial v_\theta}{\partial r}+\frac{v_\theta}{r}\frac{\partial v_\theta}{\partial \theta}-\frac{v_rv_\theta}{r}+v_z\frac{\partial v_\theta}{\partial z}\right) = \\
-\frac{1}{r}\frac{\partial p}{\partial \theta} + \eta \left[ \frac{1}{r} \frac{\partial }{\partial r} \left( r \frac{\partial v_{\theta}}{\partial r}\right) -\frac{v_{\theta}}{r^2} +\frac{1}{r^2} \frac{\partial ^2}{\partial \theta^2} \left( v_{\theta}\right)  + \frac{2}{r^2} \frac{\partial }{\partial \theta} \left( v_{r} \right)+ \frac{\partial ^2}{\partial z^2} \left( v_{\theta}\right) \right]
\end{split}
$$

**Navier-Stokes: z-direction**  

$$
\begin{split}
\rho\left(\frac{\partial v_z}{\partial t}+v_r\frac{\partial v_z}{\partial r}+\frac{v_\theta}{r}\frac{\partial v_z}{\partial \theta}+v_z\frac{\partial v_z}{\partial z}\right) = \\
-\frac{\partial p}{\partial z} + \eta \left[ \frac{1}{r} \frac{\partial }{\partial r} \left( r \frac{\partial v_z}{\partial r}\right) +\frac{1}{r^2} \frac{\partial ^2}{\partial \theta^2} \left( v_z \right) + \frac{\partial ^2}{\partial z^2} \left( v_z \right) \right]
\end{split}
$$

with $v_r$, $v_{\theta}$, and $v_z$ being the velocity components in the $r$, $\theta$, and $z$-direction.



```{exercise}
:label: Exercise1NV
Simplify the continuity equation as much as possible. When you eliminate terms, explain why. 
```
```{solution} Exercise1NV
:label: Solution1NV
:class: dropdown
There is no angular and radial velocity component in steady unidirectional laminar flow in the cylindrical pipe: $v_r = v_\theta = 0$, which directly leads to $\frac{\partial v_z}{\partial z} = 0$. In other words: the continuity equation for incompressible unidirectional flow tells that the flow is fully developed, i.e. the velocity component $v_z$ does not depend on the coordinate $z$. 
```


```{exercise}
:label: Exercise2NV
 Simplify the Navier-Stokes equations. When you eliminate terms, explain why.
```
```{solution} Exercise2NV
:label: Solution2NV
:class: dropdown
With $v_r = 0$, Navier-Stokes in the r-direction simplifies to $\partial p/\partial r = 0$. In other words, the pressure is the same in the cross section. 

With $v_{\theta} = 0$, Navier-Stokes in the $\theta$-direction reduces to $\partial p/\partial \theta = 0$. This gives no additional information. 

For Navier-Stokes in the z-direction, the only non-zero terms are the pressure gradient $\partial p/\partial z$ in the $z$-direction and the viscous terms. Since there is no $\theta$-dependence in a system that is axisymmmetric, the viscous term with the $\theta$-derivative drops.  
```

```{exercise}
:label: Exercise3NV
Use the simplified continuity equation to further simplify the Navier-Stokes equations. Show that this leads to $\frac{\partial p(z)}{\partial z} = \eta \frac{1}{r} \frac{\partial }{\partial  r}\left( r \frac{\partial  v_z}{\partial  r} \right)$.
```
```{solution} Exercise3NV
:label: Solution3NV
:class: dropdown
The continuity equation (see solution for {numref}`Exercise2NV`) dictates that $\partial v_z/\partial z = 0$ such that the viscous term $\eta \frac{\partial^2v_z}{\partial z^2} $ equals zero. 

The Navier-Stokes equations hence simplify to 
$$ 0 = \frac{\partial p}{\partial z} -  \frac{\eta}{r} \frac{\partial }{\partial r}\left( r \frac{\partial v_z}{\partial r} \right)$$  
```

```{exercise}
:label: Exercise4NV
Integrate this equation twice with respect to $r$.
```
```{solution} Exercise4NV
:label: Solution4NV
:class: dropdown
$v_z(r) = \frac{1}{4\eta}\frac{\partial p(z)}{\partial z}r^2+C_1 \ln{r}+C_2$, with $C_1$ and $C_2$ the two constants of integration.
```

```{exercise}
:label: Exercise5NV
Give the boundary conditions to find the two integration constants introduced when integrating twice in {numref}`Exercise4NV`. Use the boundary conditions to determine the integration constants and give the resulting expression for the velocity profile $v_z(r)$. 
```
```{solution} Exercise5NV
:label: Solution5NV
:class: dropdown
BC1: $\partial v_z/\partial r (r=0) = 0$ (due to symmetry).  
BC2: $v_z(r=d/2) = 0$ (no slip at the wall).  

Using these boundary conditions gives:  
$C_1 = 0$ and $C_2 = -\frac{1}{4\eta}\frac{\partial p(z)}{\partial z}(d/2)^2$. 

The resulting velocity profile is:  
$v_z (r) = \frac{1}{4 \eta} \left(-\frac{\partial p}{\partial z}\right) \left[ (d/2)^2 - r^2\right]$
```

```{exercise}
:label: Exercise6NV
Determine the volumetric flow rate $Q$ from the obtained velocity profile.
```
```{solution} Exercise6NV
:label: Solution6NV
:class: dropdown
The volumetric flow rate $Q$ depends on the mean velocity according to: $Q = A \cdot \overline{v_z}$, where $A$ is the cross-sectional area of the pipe given by: $A = \pi(d/2)^2$. The mean velocity $\overline{v_z}$ can be derived from the following expression:  
$
\overline{v_z} = \frac{\int_{r=0}^{d/2} v_z(r) 2 \pi r dr}{\int_{r=0}^{d/2} 2 \pi r dr}
$

Working this out yields:  
$
\overline{v_z} = \frac{d^2}{ 32 \eta} \left( - \frac{\partial p}{\partial z}\right)
$
   
Hence, $Q  = A \cdot  \frac{d^2}{ 32 \eta} \left( - \frac{\partial p}{\partial z}\right) = \frac{\pi d^4}{ 128 \eta} \left( -\frac{\partial p}{\partial z}\right)$.
```

```{exercise}
:label: Exercise7NV
Determine the pressure difference $\Delta p$ over the pipe length $L$ as a function of the flow rate $Q$ using the expression derived in (f).
```
```{solution} Exercise7NV
:label: Solution7NV
:class: dropdown
$\Delta P = -\frac{128\eta}{\pi}\frac{L}{d^4}Q$
```
